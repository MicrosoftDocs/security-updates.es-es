---
TOCTitle: 'MS13-APR'
Title: Resumen del boletín de seguridad de Microsoft de abril 2013
ms:assetid: 'ms13-apr'
ms:contentKeyID: 61225444
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-apr(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de abril 2013
===========================================================

Publicado: martes, 9 de abril de 2013 | Actualizado: martes, 25 de junio de 2013

**Versión:** 4.0

Este resumen del boletín enumera los boletines de seguridad publicados para abril de 2013.

Con la publicación de los boletines de seguridad de abril de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de abril de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/gg309152.aspx).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 10 de abril de 2013, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de abril](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538640&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538640&culture=en-us).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285215">MS13-028</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2817183)  <br />
<br />
</strong>Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286679">MS13-029</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el cliente de Escritorio</strong> <strong>remoto podría permitir la ejecución remota de código (2828223)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad en el cliente de Escritorio remoto de Windows de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visualiza una página web especialmente diseñada. Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286577">MS13-030</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en SharePoint podría permitir la divulgación de información (2827663)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft SharePoint Server. La vulnerabilidad podría permitir la divulgación de información si un atacante determinar la dirección o la ubicación de una lista de SharePoint concreta y obtuviera acceso al sitio de SharePoint donde se mantiene la lista. Para aprovechar esta vulnerabilidad, el atacante debe poder atender las solicitudes de autenticación del sitio de SharePoint.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=282388">MS13-031</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades del</strong> <strong>kernel</strong> <strong>de Windows</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (2813170)  <br />
<br />
</strong>Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=280660">MS13-032</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Active</strong> <strong>Directory</strong> <strong>podría provocar la denegación de servicio (2830914)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Active Directory. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía una consulta especialmente diseñada al servicio de protocolo ligero de acceso a directorios (LDAP).</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286700">MS13-033</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el subsistema de tiempo de ejecución de cliente-servidor (CSRSS) de Windows podría permitir la elevación de privilegios (2820917)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en todas las ediciones compatibles de Windows XP, Windows Vista, Windows Server 2003 y Windows Server 2008. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=276805">MS13-034</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el Cliente de Microsoft Malware podría permitir la elevación de privilegios (2823482)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad en el Cliente de Microsoft Antimalware de la que se ha informado de forma privada. La vulnerabilidad podría permitir la elevación de privilegios debido a los nombres de ruta de acceso que usa el Cliente de Microsoft Antimalware. Un atacante que consiga aprovechar esta vulnerabilidad podría ejecutar código arbitrario y tomar el control completo de un sistema afectado. De esta forma, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Para aprovechar esta vulnerabilidad, el usuario debe tener unas credenciales de inicio de sesión válidas. Los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Software de seguridad de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285672">MS13-035</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el componente de saneamiento de HTML podría permitir la elevación de privilegios (2821818)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la elevación de privilegios si un atacante envía un contenido especialmente diseñado a un usuario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=281927">MS13-036</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el controlador modo</strong> <strong>kernelpodrían</strong> <strong>permitir la elevación de privilegios (2829996)</strong> <br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en el software de Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar las vulnerabilidades más graves, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
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
  
**¿Cómo se usa esta tabla?**  
  
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285215">MS13-028</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Internet Explorer después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1303">CVE-2013-1303</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285215">MS13-028</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Internet Explorer después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1304">CVE-2013-1304</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285215">MS13-028</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Internet Explorer después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1338">CVE-2013-1338</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286679">MS13-029</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en control ActiveX de RDP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1296">CVE-2013-1296</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286577">MS13-030</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en el acceso incorrecto a los derechos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1290">CVE-2013-1290</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=282388">MS13-031</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución del kernel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1284">CVE-2013-1284</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=282388">MS13-031</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución del kernel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1294">CVE-2013-1294</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=280660">MS13-032</a></td>
<td style="border:1px solid black;">Vulnerabilidad de consumo de memoria</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1282">CVE-2013-1282</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=286700">MS13-033</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con CSRSS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1295">CVE-2013-1295</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">En Windows Server 2003 y Windows XP Professional x64 Edition, se trata de una vulnerabilidad de elevación de privilegios.<br />
<br />
En Windows XP, Windows Vista y Windows Server 2008, se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=276805">MS13-034</a></td>
<td style="border:1px solid black;">Vulnerabilidad de nombres de ruta de acceso incorrectos en Microsoft Antimalware</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0078">CVE-2013-0078</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=285672">MS13-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de saneamiento de HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1289">CVE-2013-1289</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft es consciente de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=281927">MS13-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1283">CVE-2013-1283</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=281927">MS13-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1292">CVE-2013-1292</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
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
<th colspan="7" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=f7b699b1-7655-4c8f-bd1a-535ff210b338)   
(2817183)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e9f9848e-b926-4487-9dc2-b2a6b6f5f98e)   
(2817183)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4cf0de09-2e8d-4be0-bbbf-d040164f22e0)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=353812de-b1eb-4245-82e3-7829cb72bba3)  
(2813345)  
(Crítica)  
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=1754fdde-4744-4783-b6d3-e38eb2874b58)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=69de7e3c-d99b-432a-b286-f45841edc4a7)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=8adb6ced-6065-454b-ba67-b0acd621df76)  
(2801109)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f47a73d3-05f6-4c7d-b063-c83dd0070c2d)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=75914c2a-37bb-4541-81ed-a602acb27a14)  
(2808735)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=4496bce8-809e-458c-b199-49b32eef7b21)   
(2817183)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9d792ad9-c2d7-4972-9f27-4580af04571c)   
(2817183)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c3bdbbb8-57a2-4474-9b86-239f7a77e658)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=f413845a-84e0-48d9-b5bc-56a37109ab33)  
(2813345)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=74855fb1-cad1-463f-a02d-1c27a39667c9)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=9fb780b9-bbca-45ec-98db-da413f0ccddf)  
(2801109)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c143a028-2c38-469f-a563-be8030ec76e3)  
(2820917)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20a1f311-5cdc-4675-a228-32993d8be3f9)  
(2808735)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=8d834fd2-eaa0-4742-a8a2-93277ca41f91)   
(2817183)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b0cbbaaf-be40-4088-b3d3-ca85410807b7)  
(2817183)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=cd2731b3-406e-4b73-bd70-4f2bb16dfb08)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=75b00750-80c3-4ffa-adbf-5f40a41309b9)  
(2813345)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2c242d48-8dbe-4474-ba39-f7e3ebe9a604)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=c27666a5-67ff-4e2d-b9d7-2cef19da1edd)  
(2772930)  
(Importante)  
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=13eb9459-0a39-4652-b577-6d8509801f62)  
(2801109)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=63ffbd1a-79a9-47c8-a904-b6e9a0fb626f)  
(2820917)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0722d681-eda8-48af-b079-36d45eb20f98)  
(2808735)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=7149ecda-78d3-4289-81b2-5133cd9b4564)   
(2817183)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=f22de9fa-96e0-4a09-8923-8731e0de38c9)  
(2817183)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=08c55acd-4c5e-4d5e-b524-19fd449e5c50)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=7efb8816-ca23-4a75-a0cc-53a663eac3a9)  
(2813345)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b7af0c30-0d09-434a-85d6-69e7e9ee9e29)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=1b009894-8503-42b6-85d1-1285ed14bef9)  
(2772930)  
(Importante)  
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=30c0c8d8-df70-4637-bea4-96e2e4d2cb28)  
(2801109)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bf96696e-13a4-4b01-a8d9-60654d7d1ac5)  
(2820917)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fc5f39a7-e89b-4ef0-887c-873ad546fb65)  
(2808735)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=b10b94db-b281-46b6-b301-58f14de327d2)   
(2817183)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9d799925-5f8e-43c8-8674-19437a7a6c99)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=54e286a0-22f5-4b34-a246-c98c0647f093)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=0b65be9e-724d-469d-ba3b-93d8b174aecb)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c56d776a-4293-4d3c-bcac-cd5f50eeb328)  
(2820917)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=dd159949-e0f0-4515-876d-837758a3fd51)  
(2808735)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5591feef-5bc6-4e3e-9bbb-cd2205757340)  
(2817183)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e244c3f1-3c4e-4648-b1f9-e216b0009f1e)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=190a78a5-e557-44f3-b214-7d3c904f7bd8)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=20500712-2c0f-41e2-95a8-db1a5dcf717a)  
(2813345)  
(Crítica)  
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=1bf2935a-2fa4-4a26-bccf-fe0b63a16b37)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7f1aa4bd-a14e-4797-b542-4220e3d9d0d7)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=e1b1a3b4-7aae-4934-96cc-990cd1ce962d)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=10664eeb-f759-4a0e-b1df-c463aae43902)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3881a7f9-a5f1-4a28-b652-7b7f20c05259)  
(2808735)  
(Importante)  
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=55d753f3-b912-401c-bca6-61c212ffa0df)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=1bcd238f-2758-49f7-a347-7ec998637d5c)  
(2817183)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c35f53d6-eceb-4966-9487-2dfc2652c775)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=6cfdb0d5-9c47-405f-bc60-0e4dd3eaff12)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c6f006c-fcb8-499f-bd91-9c8acb3ec3c3)  
(2813345)  
(Crítica)  
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=201eb194-e7c9-479c-bb03-646b22f2bbd1)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d6b3ef0e-16e3-42cb-bffe-4b046f995771)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=ca2182ae-cd47-48d7-9bb0-4aeda4ee26cc)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c12ce8b7-e8e2-47ac-bdaa-874dff5a6115)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e5ba88a4-e0ec-45d7-8c0a-611521351890)  
(2808735)  
(Importante)  
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=89f1556f-442f-4888-b21a-ffbedaa8792e)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=09bd431a-e94f-4fc5-bea9-569ebc17b0f3)  
(2817183)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=76f96697-0f07-49ad-9169-47cfe2f6a362)  
(2817183)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=2d8c4080-ff7a-42ef-95f4-36b642c0a089)   
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=92bd1819-46f9-4a9b-bf2b-ea6aaaee9890)  
(2813345)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=527ea8cd-88db-448a-b8e4-0fdf87fa369c)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=dd955bf1-e51f-4738-82bf-759e9dea0895)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=31561241-07c8-4396-ad80-9c62a2394658)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e598863e-7ca1-42a6-9cb4-3f3a10f0ce71)  
(2808735)  
(Importante)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a4bdfe68-4de2-41fa-a593-2e07de105081)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e46e002e-40b2-4bb3-89ad-63d320273ffa)  
(2817183)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b93153dc-f83a-4891-8230-765e3472614d)  
(2817183)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=08abb2ce-0a07-4f25-b9ad-5ec87c07f0bf)   
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=6518cdc6-10a6-46ed-a2f6-6f58216fe319)  
(2813345)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=604709f7-8712-4162-ab86-5988b19084f9)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=38d1cd8c-977b-47be-b703-a326a1b4f445)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=46ef3ace-30b2-4099-aa9d-142de82b0257)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a9dd92b5-4137-47d1-85a3-506f1eaacee0)  
(2808735)  
(Importante)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1c36a50c-023d-420d-830a-d4cb2eda6ef2)  
(2840149)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b0d20b3f-f6cb-4cbc-9af1-1d33b4a6dfb2)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 6.1](http://www.microsoft.com/downloads/details.aspx?familyid=4807c3fe-bc54-4db6-a9b0-ee21bdd9820f)  
(2813345)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6133c84a-b2ce-4a2e-8afc-7386caf80cc8)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=94971d7b-df42-4566-97eb-0a7572b0e2da)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3e9ccb95-284a-478e-b521-f3a0acbae8da)  
(2808735)  
(Importante)  
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=738b2263-e1eb-4ada-a7f0-5165f42bc5c9)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ec9c221a-065b-4f5c-95b6-9b650c24cffa)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=041fd330-0998-44b5-bedd-d3e47965370d)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=d7623f17-783d-431a-8274-17d71df72202)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=90d2c454-c31c-4ac4-ab94-b341d1244ee6)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=37b3e861-35fb-471b-b81a-a8b58bd26647)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=1abeaf49-c458-4046-a001-8aee0ba35b3a)  
(2808735)  
(Importante)  
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=808ac8c6-394d-406b-b34e-07d03c760c27)  
(2840149)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ec9c221a-065b-4f5c-95b6-9b650c24cffa)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=041fd330-0998-44b5-bedd-d3e47965370d)   
(2817183)  
(Crítica)  
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=cf49622e-8494-4082-a9aa-a6699711d827)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.1](http://www.microsoft.com/downloads/details.aspx?familyid=d7623f17-783d-431a-8274-17d71df72202)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=90d2c454-c31c-4ac4-ab94-b341d1244ee6)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=37b3e861-35fb-471b-b81a-a8b58bd26647)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1abeaf49-c458-4046-a001-8aee0ba35b3a)  
(2808735)  
(Importante)  
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=808ac8c6-394d-406b-b34e-07d03c760c27)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=01f4b588-38e3-43a7-ae5c-674b9c03fc42)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ac93c656-2c9c-4378-9ae3-a60636b8ce6f)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=5595efaa-3d57-4c9a-8b53-7cfa06093f1e)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ebc1ea79-158f-4c81-ab49-3d3fca870363)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=94d19c2a-2457-4fa7-ade6-ad37d0e7f56a)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=84275cfd-f5a3-4830-895d-beaf162cdc27)  
(2808735)  
(Importante)  
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=737a0cd0-eee6-4095-b9b1-2822024dd825)  
(2840149)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=01f4b588-38e3-43a7-ae5c-674b9c03fc42)  
(2817183)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ac93c656-2c9c-4378-9ae3-a60636b8ce6f)   
(2817183)  
(Crítica)  
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=775536fa-a8a2-4733-a0f0-08e742be1122)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.1](http://www.microsoft.com/downloads/details.aspx?familyid=5595efaa-3d57-4c9a-8b53-7cfa06093f1e)  
(2813347)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ebc1ea79-158f-4c81-ab49-3d3fca870363)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=94d19c2a-2457-4fa7-ade6-ad37d0e7f56a)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=84275cfd-f5a3-4830-895d-beaf162cdc27)  
(2808735)  
(Importante)  
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=737a0cd0-eee6-4095-b9b1-2822024dd825)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d8ffa592-6336-494d-bcd0-535ea2821525)  
(2817183)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7f68500e-6699-4341-b129-2dbd5bc508ac)   
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=79c870b9-b800-4f59-a5ea-19a5c890af52)  
(2813347)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=dbbd2e3d-1b37-4173-9955-e6fceb7bcd45)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=78d11246-06b0-4a22-a2b0-c772aa60e726)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=cbaac7fb-b673-4cf5-8c6f-57bedcb5285d)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=3e96483f-ec2d-4335-8c50-8686eed06018)  
(2840149)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d8ffa592-6336-494d-bcd0-535ea2821525)  
(2817183)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7f68500e-6699-4341-b129-2dbd5bc508ac)   
(2817183)  
(Moderada)  
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=752ffe45-b251-4cdf-9848-4d15f75d4452)   
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.1](http://www.microsoft.com/downloads/details.aspx?familyid=79c870b9-b800-4f59-a5ea-19a5c890af52)  
(2813347)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=dbbd2e3d-1b37-4173-9955-e6fceb7bcd45)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=78d11246-06b0-4a22-a2b0-c772aa60e726)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cbaac7fb-b673-4cf5-8c6f-57bedcb5285d)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3e96483f-ec2d-4335-8c50-8686eed06018)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2dec754b-4d51-4792-bee6-67e94a1a8157)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=c7047403-8c2a-42de-bea5-d7354847730a)  
(2813347)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=5cfc2f18-4cde-4e21-8604-f694d69da535)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=6c577423-cd17-4317-98a3-5f6e767513c0)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3f1abf13-14c3-4a92-b4c1-4caa40e29e7b)  
(2840149)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2dec754b-4d51-4792-bee6-67e94a1a8157)  
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto 7.1](http://www.microsoft.com/downloads/details.aspx?familyid=c7047403-8c2a-42de-bea5-d7354847730a)  
(2813347)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5cfc2f18-4cde-4e21-8604-f694d69da535)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6c577423-cd17-4317-98a3-5f6e767513c0)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3f1abf13-14c3-4a92-b4c1-4caa40e29e7b)  
(2840149)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación** **de gravedad acumulada**
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
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=159c43ec-beaf-4ac3-8c3a-06a9716ac9ae)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=02d6d10e-3708-4424-8618-88414694c973)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=c7a7ba4d-1fe1-40ed-81f2-6fbb6dde2cf6)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=882f2d67-b8e0-4859-871b-6a7cef27e3e5)  
(2808735)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=3309f621-4087-4688-b991-c2ef54532cb6)   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=18992e76-70f3-43a2-b47f-199c9728c7ca)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=bafaac33-2bef-4a5e-9451-23ca69c0a132)  
(2772930)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=852dac0f-75fe-443f-9b3d-1dbcac166b3d)  
(2808735)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2012
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=5015e763-6fb8-4737-9305-2e5850ef853d)   
(2817183)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=ef106525-c42b-4b25-83bf-e290e2bcad5a)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=209e3d5f-9333-469e-8b2c-212dc4ec764a)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=fbf53f06-1ee2-49c4-a5a8-3b1e9823b1b9)  
(2808735)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10<sup>[1]</sup>   
(2817183)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(2808735)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS13-028**](http://go.microsoft.com/fwlink/?linkid=285215)
</td>
<td style="border:1px solid black;">
[**MS13-029**](http://go.microsoft.com/fwlink/?linkid=286679)
</td>
<td style="border:1px solid black;">
[**MS13-031**](http://go.microsoft.com/fwlink/?linkid=282388)
</td>
<td style="border:1px solid black;">
[**MS13-032**](http://go.microsoft.com/fwlink/?linkid=280660)
</td>
<td style="border:1px solid black;">
[**MS13-033**](http://go.microsoft.com/fwlink/?linkid=286700)
</td>
<td style="border:1px solid black;">
[**MS13-036**](http://go.microsoft.com/fwlink/?linkid=281927)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=527ea8cd-88db-448a-b8e4-0fdf87fa369c) (instalación Server Core)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=dd955bf1-e51f-4738-82bf-759e9dea0895)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=31561241-07c8-4396-ad80-9c62a2394658) (instalación Server Core)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e598863e-7ca1-42a6-9cb4-3f3a10f0ce71) (instalación Server Core)  
(2808735)  
(Importante)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a4bdfe68-4de2-41fa-a593-2e07de105081) (instalación Server Core)  
(2840149)  
(Moderada)
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=604709f7-8712-4162-ab86-5988b19084f9) (instalación Server Core)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=38d1cd8c-977b-47be-b703-a326a1b4f445)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=46ef3ace-30b2-4099-aa9d-142de82b0257) (instalación Server Core)  
(2820917)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a9dd92b5-4137-47d1-85a3-506f1eaacee0) (instalación Server Core)  
(2808735)  
(Importante)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1c36a50c-023d-420d-830a-d4cb2eda6ef2) (instalación Server Core)  
(2840149)  
(Moderada)
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=dbbd2e3d-1b37-4173-9955-e6fceb7bcd45)(instalación Server Core)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=78d11246-06b0-4a22-a2b0-c772aa60e726)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=cbaac7fb-b673-4cf5-8c6f-57bedcb5285d)(instalación Server Core)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=3e96483f-ec2d-4335-8c50-8686eed06018)(instalación Server Core)  
(2840149)  
(Moderada)
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
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=dbbd2e3d-1b37-4173-9955-e6fceb7bcd45) (instalación Server Core)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=78d11246-06b0-4a22-a2b0-c772aa60e726)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cbaac7fb-b673-4cf5-8c6f-57bedcb5285d) (instalación Server Core)  
(2808735)  
(Importante)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3e96483f-ec2d-4335-8c50-8686eed06018) (instalación Server Core)  
(2840149)  
(Moderada)
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
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=ef106525-c42b-4b25-83bf-e290e2bcad5a) (instalación Server Core)  
(2813170)  
(Importante)
</td>
<td style="border:1px solid black;">
[Servicios de Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=209e3d5f-9333-469e-8b2c-212dc4ec764a)  
(2772930)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=fbf53f06-1ee2-49c4-a5a8-3b1e9823b1b9) (instalación Server Core)  
(2808735)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-028, MS13-031 y MS13-036**

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-035**](http://go.microsoft.com/fwlink/?linkid=285672)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=63f6a338-a195-4923-908e-8c21713c7373)  
(2687422)  
(Sin clasificación de gravedad)<sup>[1]</sup>
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f1cd73d2-411b-4a58-b8c0-04fd58922dae)  
(2760406)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=ae2069d0-55b5-4dfe-9131-41888d6bbec3)  
(2687422)  
(Sin clasificación de gravedad)<sup>[1]</sup>
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f206071a-4502-432a-9e5b-50bb4e3f1757)  
(2760406)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
</tr>
</table>
 
**Notas para MS13-035**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado porque las vías de ataque conocidas para la vulnerabilidad están bloqueadas.

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
[**MS13-030**](http://go.microsoft.com/fwlink/?linkid=286577)
</td>
<td style="border:1px solid black;">
[**MS13-035**](http://go.microsoft.com/fwlink/?linkid=285672)
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
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2010 Service Pack 1 (wosrv)](http://www.microsoft.com/downloads/details.aspx?familyid=6c7d007f-5c8d-464c-af04-4e7800a2e2a6)<sup>[1]</sup>
(2687421)  
(Importante)  
[Microsoft SharePoint Server 2010 Service Pack 1 (coreserver)](http://www.microsoft.com/downloads/details.aspx?familyid=c59c0d25-8d6c-4dda-a06b-e42891a9ddae)<sup>[1]</sup>
(2760408)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2013 (coreserverloc)](http://www.microsoft.com/downloads/details.aspx?familyid=2e5b1e49-0355-4111-a464-224bb2192029)<sup>[1]</sup>
(2737969)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Groove Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-030**](http://go.microsoft.com/fwlink/?linkid=286577)
</td>
<td style="border:1px solid black;">
[**MS13-035**](http://go.microsoft.com/fwlink/?linkid=285672)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Groove Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Groove Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d63ee461-b823-4eb1-9e6d-82f380627fb5)  
(2687424)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft SharePoint Foundation
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-030**](http://go.microsoft.com/fwlink/?linkid=286577)
</td>
<td style="border:1px solid black;">
[**MS13-035**](http://go.microsoft.com/fwlink/?linkid=285672)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Foundation 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ac805c46-8661-4e99-84da-c395dc05beb0)  
(2810059)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-030**

<sup>[1]</sup>Esta actualización requiere la instalación previa de la actualización acumulativa de Project Server 2013 (2768001). Para obtener más información acerca de la actualización, incluidos los vínculos de descarga, vea el [artículo 2768001 de Microsoft Knowledge Base](http://support.microsoft.com/kb/2768001).

**Notas para MS13-035**

<sup>[1]</sup>Para las ediciones compatibles de Microsoft SharePoint Server 2010, además de los paquetes de actualización de seguridad de Microsoft SharePoint 2010 (2687421 y 2760408), los clientes también deben instalar la actualización de seguridad para Microsoft SharePoint Foundation 2010 (2810059) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Microsoft Office Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-035**](http://go.microsoft.com/fwlink/?linkid=285672)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1d35b235-305a-45c8-a395-7658792d177e)  
(2760777)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-035**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de seguridad de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Software antimalware
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-034**](http://go.microsoft.com/fwlink/?linkid=276805)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Defender para Windows 8 y Windows RT
</td>
<td style="border:1px solid black;">
Windows Defender para Windows 8 y Windows RT<sup>[1]</sup>   
(2781197)   
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-034**

<sup>[1]</sup>Esta actualización está disponible a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS13-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

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

**MS13-028**

-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad en el uso de Internet Explorer después de la liberación (CVE-2013-1303)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad en el uso de Internet Explorer después de la liberación (CVE-2013-1304)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de Internet Explorer después de la liberación (CVE-2013-1338)
-   Un investigador anónimo, por colaborar con nosotros en los cambios de defensa en profundidad incluidos en este boletín

**MS13-029**

-   c1d2d9acc746ae45eeb477b97fa74688, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de ejecución remota de código en control ActiveX de RDP (CVE-2013-1296)

**MS13-031**

-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de condición de ejecución del kernel (CVE-2013-1284)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de condición de ejecución del kernel (CVE-2013-1294)

**MS13-033**

-   George Georgiev Valkov, por informar de la vulnerabilidad de daños en la memoria relacionada con CSRSS (CVE-2013-1295)

**MS13-034**

-   Bruce Monroe, de [Intel](http://www.intel.com/), por informar de la vulnerabilidad de nombres de ruta de acceso incorrectas en Microsoft Antimalware (CVE-2013-0078)
-   Shai Sarfaty, por informar de la vulnerabilidad de nombres de ruta de acceso incorrectas en Microsoft Antimalware (CVE-2013-0078)
-   Tony Robotham, de Centrica, por informar de la vulnerabilidad de nombres de ruta de acceso incorrectas en Microsoft Antimalware (CVE-2013-0078)

**MS13-035**

-   Drew Hintz y Andrew Lyons, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de saneamiento de HTML (CVE-2013-1289)

**MS13-036**

-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de condición de ejecución de Win32k (CVE-2013-1283)
-   Wang Yu, de [Qihoo 360 Security Center](http://www.360.cn/), por informar de la vulnerabilidad de análisis de fuentes Win32k (CVE-2013-1291)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de condición de ejecución de Win32k (CVE-2013-1292)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por colaborar con nosotros en la vulnerabilidad de anulación de referencia de puntero nulo de NTFS (CVE-2013-1293)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de abril de 2013): Publicación del resumen del boletín.
-   V1.1 (10 de abril de 2013): para MS13-029, se ha corregido el número de versión de Cliente de Conexión a Escritorio remoto en Windows 7 Service Pack 1 y Windows Server 2008 R2 Service Pack 1 de 7.0 a 7.1. Se trata únicamente de un cambio informativo. No había cambios en los archivos de la actualización de seguridad.
-   V2.0 (11 de abril de 2013): para MS13-036, se eliminaron los vínculos a la actualización de seguridad 2823324 debido a un problema de instalación conocido. Consulte el boletín para obtener más detalles.
-   V3.0 (23 de abril de 2013): para MS13-036, se ha reemplazado la actualización 2823324 por la actualización 2840149 para NTFS.sys cuando está instalado en ediciones compatibles de Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2. Vea el boletín para obtener más detalles.
-   V3.1 (24 de abril de 2013): para MS13-028, se ha corregido la evaluación de explotabilidad en **Índice de** **explotabilidad** para CVE-2013-1338. Se trata únicamente de un cambio informativo.
-   V4.0 (25 de junio de 2013): para MS13-029, se ha revisado el boletín para volver a publicar la actualización 2813347 para Cliente de Conexión a Escritorio remoto 7.0 en Windows XP Service Pack 3. Vea el boletín para obtener más detalles.

*Built at 2014-04-18T01:50:00Z-07:00*
