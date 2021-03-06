---
TOCTitle: 'MS12-OCT'
Title: Resumen del boletín de seguridad de Microsoft de octubre 2012
ms:assetid: 'ms12-oct'
ms:contentKeyID: 61225442
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms12-oct(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de octubre 2012
=============================================================

Publicado: martes, 9 de octubre de 2012 | Actualizado: martes, 23 de octubre de 2012

**Versión:** 1.3

Este resumen del boletín enumera los boletines de seguridad publicados para octubre de 2012.

Con la publicación de los boletines de seguridad de octubre de 2012, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de octubre de 2012. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft realizará un webcast para atender las consultas de los clientes sobre estos boletines el 10 de octubre de 2012, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de octubre](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032522558&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032522558&culture=en-us).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=260965">MS12-064</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Word</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2742319)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario abre un archivo RTF especialmente diseñado u obtiene una vista previa de él. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263959">MS12-065</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Works podría permitir la ejecución remota de código (2754670)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Works. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Microsoft Word especialmente diseñado con Microsoft Works. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=260957">MS12-066</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el componente de saneamiento de HTML podría permitir la elevación de privilegios (2741517)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Office, plataformas de Microsoft Communications, software de servidor de Microsoft y Microsoft Office Web Apps. La vulnerabilidad podría permitir la elevación de privilegios si un atacante envía un contenido especialmente diseñado a un usuario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft,<br />
Microsoft Lync</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=259736">MS12-067</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el análisis de FAST</strong> <strong>Search</strong> <strong>Server 2010</strong> <strong>for</strong> <strong>SharePoint podrían permitir la ejecución remota de código (2742321)</strong> <br />
<br />
Esta actualización de seguridad resuelve vulnerabilidades que se han divulgado de forma pública en Microsoft FAST Search Server 2010 for SharePoint. Las vulnerabilidades podrían permitir la ejecución remota de código en el contexto de seguridad de una cuenta de usuario con un token restringido. FAST Search Server for SharePoint solo está afectado por este problema cuando Advanced Filter Pack está habilitado. De forma predeterminada, Advanced Filter Pack está deshabilitado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=257912">MS12-068</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el</strong> <strong>kernel</strong> <strong>de</strong> <strong>Windows podría permitir la elevación de privilegios (2724197)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en todas las versiones compatibles de Microsoft Windows, excepto Windows 8 y Windows Server 2012. Esta actualización de seguridad se considera importante para todas las ediciones compatibles de Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2.<br />
<br />
La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263962">MS12-069</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en</strong> <strong>Kerberos</strong> <strong>podría permitir la denegación de servicio (2743555)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante remoto envía una solicitud de sesión especialmente diseñada al servidor Kerberos. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263997">MS12-070</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en SQL Server podría permitir la elevación de privilegios (2754849)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft SQL Server en sistemas con SQL Server Reporting Services (SSRS). Se trata de una vulnerabilidad de scripts de sitios (XSS) que podría permitir la elevación de privilegios, lo que permitiría que un atacante ejecutar comandos arbitrarios en el sitio SSRS en el contexto del usuario atacado. Un atacante podría aprovechar esta vulnerabilidad enviando al usuario un vínculo especialmente diseñado y convenciéndole de que haga clic en él. Un atacante también podría hospedar un sitio web que contuviera una página web diseñada para aprovechar la vulnerabilidad. Además, los sitios web vulnerables y los sitios web que aceptan u hospedan contenido o anuncios proporcionados por el usuario podrían incluir contenido especialmente diseñado que permita aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft SQL Server</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=260965">MS12-064</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la sección PAPX de Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-0182">CVE-2012-0182</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=260965">MS12-064</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de listid en el archivo RTF después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2528">CVE-2012-2528</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263959">MS12-065</a></td>
<td style="border:1px solid black;">Vulnerabilidad del montón en Works</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2550">CVE-2012-2550</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=260957">MS12-066</a></td>
<td style="border:1px solid black;">Vulnerabilidad de saneamiento de HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2520">CVE-2012-2520</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=259736">MS12-067</a></td>
<td style="border:1px solid black;">Advanced Filter Pack para FAST Search Server 2010 for SharePoint contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;">Oracle Outside In contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">*Varias vulnerabilidades, vea el boletín MS12-067 para obtener detalles.<br />
<br />
Estas vulnerabilidades se han divulgado de forma pública.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=257912">MS12-068</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento de enteros en el kernel de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2529">CVE-2012-2529</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263962">MS12-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de anulación de referencia nula de Kerberos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2551">CVE-2012-2551</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=263997">MS12-070</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS reflejado</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2552">CVE-2012-2552</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6aa1e4b3-273a-49ff-8086-0d2c16dd14f3)   
(KB2724197)  
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
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3c509cc0-63a1-4cc7-b7f9-cc9f0f12b378)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6c7dd00a-a983-477b-88b1-dc16f1b5e42a)   
(KB2724197)  
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
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eaac4dae-62e6-4020-8b4d-a95e7e0e11f1)   
(KB2724197)  
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
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=315cc115-1496-471f-8887-f334a1ca8246)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=828ca8a2-777c-4b41-8d97-caed894a37cb)   
(KB2724197)  
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
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=731d67dc-e028-42e4-8ef3-454f74835593)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=526f786b-7aef-4a1f-b03d-587baadf3f5b)   
(KB2724197)  
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5697076c-541f-42b7-8dc3-e8bd4a25fda8)   
(KB2724197)  
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
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6216b875-c7a6-4d62-8062-49996ac7a478)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=593a29c3-c459-4a39-9f25-016a5268fc7d)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=4ffa9c0e-26b1-4309-bfb4-fa5374f28d6c)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=593a29c3-c459-4a39-9f25-016a5268fc7d)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=4ffa9c0e-26b1-4309-bfb4-fa5374f28d6c)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=2d273f99-3460-4e84-9f2d-2a349bfc7ce6)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d5584b7d-434f-49fc-9c30-ef16c40d475f)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2d273f99-3460-4e84-9f2d-2a349bfc7ce6)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d5584b7d-434f-49fc-9c30-ef16c40d475f)   
(KB2743555)  
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
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=848af16d-c5f7-4a70-b6a9-39f4e7999f1f)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d7210047-788c-4b33-953d-e3134f52f897)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=848af16d-c5f7-4a70-b6a9-39f4e7999f1f)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d7210047-788c-4b33-953d-e3134f52f897)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ded1f351-022a-463c-9f5f-84b6081e6173)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=7dc47f1d-8af8-4f31-9f96-3ae226632723)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ded1f351-022a-463c-9f5f-84b6081e6173)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7dc47f1d-8af8-4f31-9f96-3ae226632723)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-068**](http://go.microsoft.com/fwlink/?linkid=257912)
</td>
<td style="border:1px solid black;">
[**MS12-069**](http://go.microsoft.com/fwlink/?linkid=263962)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead** **acumulada**
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=526f786b-7aef-4a1f-b03d-587baadf3f5b) (instalación Server Core)   
(KB2724197)  
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5697076c-541f-42b7-8dc3-e8bd4a25fda8) (instalación Server Core)   
(KB2724197)  
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=848af16d-c5f7-4a70-b6a9-39f4e7999f1f)(instalación Server Core)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d7210047-788c-4b33-953d-e3134f52f897)(instalación Server Core)   
(KB2743555)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=848af16d-c5f7-4a70-b6a9-39f4e7999f1f) (instalación Server Core)   
(KB2724197)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d7210047-788c-4b33-953d-e3134f52f897) (instalación Server Core)   
(KB2743555)  
(Importante)
</td>
</tr>
</table>
 

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
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-065**](http://go.microsoft.com/fwlink/?linkid=263959)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Word 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e49eadec-0fe1-43ce-9c25-a92aad17d940)   
(KB2687483)  
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
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Word 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=be58b650-ee4f-405e-ab3c-c28aca48345b)<sup>[1]</sup>   
(KB2687315)  
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
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Word 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=be58b650-ee4f-405e-ab3c-c28aca48345b)<sup>[1]</sup>   
(KB2687315)  
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
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=27e07115-d569-438c-b95f-203e444d4408)   
(KB2553488)  
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
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=30f9efac-3ecd-48a6-adcf-922f4d4d18d4)   
(KB2553488)  
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
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-065**](http://go.microsoft.com/fwlink/?linkid=263959)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Word Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=1e392ff8-92e9-408d-bb14-1e0a6b4b6c9d)   
(KB2687485)  
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
Paquete de compatibilidad de Microsoft Office Service Pack 2
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=301446f7-991e-4abd-a06e-4a854f05ac84)   
(KB2687314)  
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
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=301446f7-991e-4abd-a06e-4a854f05ac84)   
(KB2687314)  
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
Microsoft InfoPath 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a0989a9f-3a7a-4343-9dd0-b2d694a0813b)   
(KB2687439)  
(Importante)  
[Microsoft InfoPath 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=29330e1a-6bac-4c54-98ef-b9a831801247)   
(KB2687440)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=a0989a9f-3a7a-4343-9dd0-b2d694a0813b)   
(KB2687439)  
(Importante)  
[Microsoft InfoPath 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=29330e1a-6bac-4c54-98ef-b9a831801247)   
(KB2687440)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=724b12b9-84bf-4102-912e-56aa9ee0878c)   
(KB2687436)  
(Importante)  
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b0be62c6-4eae-458e-8cf5-754742393e4c)   
(KB2687417)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=17b36fa3-9964-480a-bff8-b028619c5dfd)   
(KB2687436)  
(Importante)  
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=6e5a7817-345e-4b75-aeca-94f74691c0e0)   
(KB2687417)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Works 9
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 9](http://www.microsoft.com/downloads/details.aspx?familyid=7e48cd96-4b91-4f7b-b8a0-2b88131ba51d)   
(KB2754670)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para MS12-064**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Para Microsoft Office Word 2007, además del paquete de actualizaciones de seguridad KB2687315, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office (KB2687314) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

**Nota par MS12-066**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft SharePoint Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
<td style="border:1px solid black;">
[**MS12-067**](http://go.microsoft.com/fwlink/?linkid=259736)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
Microsoft SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a8a818bb-67a3-4558-aac1-aaa33c6f4584)<sup>[1]</sup>   
(KB2687405)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2007 Service Pack 3 (coreserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a8a818bb-67a3-4558-aac1-aaa33c6f4584)<sup>[1]</sup>   
(KB2687405)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=93f4e385-880a-4edc-9cde-24f38a11a41d)<sup>[1]</sup>   
(KB2687405)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2007 Service Pack 3 (coreserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=93f4e385-880a-4edc-9cde-24f38a11a41d)<sup>[1]</sup>   
(KB2687405)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Word Automation Services](http://www.microsoft.com/downloads/details.aspx?familyid=3582ab6c-930b-4660-afcd-e2423ce56d8f)   
(KB2598237)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2010 Service Pack 1 (wosrv)](http://www.microsoft.com/downloads/details.aspx?familyid=af3ade8e-349f-4eec-a5c3-c5a70071582d)   
(KB2687435)  
(Importante)  
[Microsoft SharePoint Server 2010 Service Pack 1 (coreserver)](http://www.microsoft.com/downloads/details.aspx?familyid=5518b70b-cac9-4aff-b049-156d3c08b04b)   
(KB2589280)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft FAST Search Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
<td style="border:1px solid black;">
[**MS12-067**](http://go.microsoft.com/fwlink/?linkid=259736)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft FAST Search Server 2010 for SharePoint
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Advanced Filter Pack](http://www.microsoft.com/downloads/details.aspx?familyid=17909d1f-c679-4a20-b39d-b99f9cc7dbc1)  
(KB2553402)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Groove Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
<td style="border:1px solid black;">
[**MS12-067**](http://go.microsoft.com/fwlink/?linkid=259736)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
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
Microsoft Groove Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Groove Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80552d2c-98f2-4c99-bfc6-e091fd1d51c4)   
(KB2687402)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows SharePoint Services y Microsoft SharePoint Foundation
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
<td style="border:1px solid black;">
[**MS12-067**](http://go.microsoft.com/fwlink/?linkid=259736)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 32 bits):
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 32 bits):](http://www.microsoft.com/downloads/details.aspx?familyid=e3a31cd4-bba3-4572-ab24-7b1dd0c4c01c)   
(KB2687356)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e3a31cd4-bba3-4572-ab24-7b1dd0c4c01c)   
(KB2687356)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 64 bits):
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 64 bits):](http://www.microsoft.com/downloads/details.aspx?familyid=77cab67c-be97-4808-9fb4-4defad563851)   
(KB2687356)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=77cab67c-be97-4808-9fb4-4defad563851)   
(KB2687356)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[Microsoft SharePoint Foundation 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=79724c7c-7cdf-44c9-9e25-577104c5004b)   
(KB2687434)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Office Web Apps
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-064**](http://go.microsoft.com/fwlink/?linkid=260965)
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
<td style="border:1px solid black;">
[**MS12-067**](http://go.microsoft.com/fwlink/?linkid=259736)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
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
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e7a2dd61-36d5-4313-a8dc-15456b275b9c)   
(KB2687401)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e7a2dd61-36d5-4313-a8dc-15456b275b9c)   
(KB2687401)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS12-064**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS12-066**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Para las ediciones compatibles de Microsoft SharePoint Server 2007, además del paquete de actualización de seguridad de Microsoft SharePoint 2007 (KB2687405), los clientes también deben instalar la actualización de seguridad para Microsoft Windows SharePoint Services 3.0 (KB2687356) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

#### Software y plataformas de Microsoft Communications

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Communicator
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Communicator 2007 R2
</td>
<td style="border:1px solid black;">
[Microsoft Communicator 2007 R2](http://www.microsoft.com/downloads/details.aspx?familyid=a228c1dd-9e57-48cb-8db4-896d6c499b46)   
(KB2726391)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Lync
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-066**](http://go.microsoft.com/fwlink/?linkid=260957)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync 2010 (32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Lync 2010 (32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=6ea3afea-baa2-4b74-9747-8051c544ddf7)   
(KB2726382)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 (64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Lync 2010 (64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=670c20e6-4f26-47b9-b6e0-25f195bf7000)   
(KB2726382)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee
</td>
<td style="border:1px solid black;">
[Microsoft Lync 2010 Attendee](http://www.microsoft.com/downloads/details.aspx?familyid=7f98cb55-027a-40bf-b539-d8fa38ffcc83)   
(instalación de nivel de administración)  
(KB2726388)  
(Importante)  
[Microsoft Lync 2010 Attendee](http://www.microsoft.com/downloads/details.aspx?familyid=32860684-998e-4e55-b719-c44532bc753d)<sup>[1]</sup>   
(instalación de nivel de usuario)  
(KB2726384)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS12-066**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Esta actualización solo está disponible en el Centro de descarga de Microsoft.

#### Microsoft SQL Server

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
SQL Server 2000
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-070**](http://go.microsoft.com/fwlink/?linkid=263997)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2000 Reporting Services Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2000 Reporting Services Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1c70a2cb-e8a9-439f-b34a-7d1641daf325)   
(KB983814)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
SQL Server 2005
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-070**](http://go.microsoft.com/fwlink/?linkid=263997)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación** **de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=623841cc-06f7-4475-b2c0-531aed9972a3)<sup>[1]</sup>   
(GDR)  
(KB2716429)  
(Importante)  
[Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=16cc7b80-ea4c-4b17-9ac2-250b771a569a)<sup>[1]</sup>   
(QFE)  
(KB2716427)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas de 32 bits Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas de 32 bits Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=623841cc-06f7-4475-b2c0-531aed9972a3)<sup>[1]</sup>   
(GDR)  
(KB2716429)  
(Importante)  
[Microsoft SQL Server 2005 para sistemas de 32 bits Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=16cc7b80-ea4c-4b17-9ac2-250b771a569a)<sup>[1]</sup>   
(QFE)  
(KB2716427)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas x64 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas x64 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=623841cc-06f7-4475-b2c0-531aed9972a3)<sup>[1]</sup>   
(GDR)  
(KB2716429)  
(Importante)  
[Microsoft SQL Server 2005 para sistemas x64 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=16cc7b80-ea4c-4b17-9ac2-250b771a569a)<sup>[1]</sup>   
(QFE)  
(KB2716427)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas con Itanium Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas con Itanium Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=623841cc-06f7-4475-b2c0-531aed9972a3)<sup>[1]</sup>   
(GDR)  
(KB2716429)  
(Importante)  
[Microsoft SQL Server 2005 para sistemas con Itanium Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=16cc7b80-ea4c-4b17-9ac2-250b771a569a)<sup>[1]</sup>   
(QFE)  
(KB2716427)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
SQL Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-070**](http://go.microsoft.com/fwlink/?linkid=263997)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1bf8dc30-2a90-4196-814c-717ccd74ea13)<sup>[1]</sup>   
(GDR)  
(KB2716434)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d8b1b25-45ad-4f19-ba50-e77debf2b463)<sup>[1]</sup>   
(QFE)  
(KB2716433)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=04621a83-c2e2-4a60-9198-10104372b120)<sup>[1]</sup>   
(GDR)  
(KB2716436)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4c4597d2-dea0-49b9-a5a9-a7771a3d64c0)<sup>[1]</sup>   
(QFE)  
(KB2716435)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1bf8dc30-2a90-4196-814c-717ccd74ea13)<sup>[1]</sup>   
(GDR)  
(KB2716434)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d8b1b25-45ad-4f19-ba50-e77debf2b463)<sup>[1]</sup>   
(QFE)  
(KB2716433)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=04621a83-c2e2-4a60-9198-10104372b120)<sup>[1]</sup>   
(GDR)  
(KB2716436)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4c4597d2-dea0-49b9-a5a9-a7771a3d64c0)<sup>[1]</sup>   
(QFE)  
(KB2716435)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1bf8dc30-2a90-4196-814c-717ccd74ea13)<sup>[1]</sup>   
(GDR)  
(KB2716434)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d8b1b25-45ad-4f19-ba50-e77debf2b463)<sup>[1]</sup>   
(QFE)  
(KB2716433)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=04621a83-c2e2-4a60-9198-10104372b120)<sup>[1]</sup>   
(GDR)  
(KB2716436)  
(Importante)  
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4c4597d2-dea0-49b9-a5a9-a7771a3d64c0)<sup>[1]</sup>   
(QFE)  
(KB2716435)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
SQL Server 2008 R2
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-070**](http://go.microsoft.com/fwlink/?linkid=263997)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=215a9184-71c5-41e6-b4d5-03602182a88f)<sup>[1]</sup>   
(GDR)  
(KB2716440)  
(Importante)  
[Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cdc4fc03-dfba-41d4-b651-d7967a067eea)<sup>[1]</sup>   
(QFE)  
(KB2716439)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=215a9184-71c5-41e6-b4d5-03602182a88f)<sup>[1]</sup>   
(GDR)  
(KB2716440)  
(Importante)  
[Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cdc4fc03-dfba-41d4-b651-d7967a067eea)<sup>[1]</sup>   
(QFE)  
(KB2716439)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=215a9184-71c5-41e6-b4d5-03602182a88f)<sup>[1]</sup>   
(GDR)  
(KB2716440)  
(Importante)  
[Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cdc4fc03-dfba-41d4-b651-d7967a067eea)<sup>[1]</sup>   
(QFE)  
(KB2716439)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
SQL Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-070**](http://go.microsoft.com/fwlink/?linkid=263997)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravead acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2012 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2012 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=e79b4e5b-1549-4e76-afef-b771b432365b)<sup>[1]</sup>   
(GDR)  
(KB2716442)  
(Importante)  
[Microsoft SQL Server 2012 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=ebfcb341-e240-4107-92f1-ab75cc28151a)<sup>[1]</sup>   
(QFE)  
(KB2716441)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2012 para sistemas x64
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2012 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=e79b4e5b-1549-4e76-afef-b771b432365b)<sup>[1]</sup>   
(GDR)  
(KB2716442)  
(Importante)  
[Microsoft SQL Server 2012 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ebfcb341-e240-4107-92f1-ab75cc28151a)<sup>[1]</sup>   
(QFE)  
(KB2716441)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS12-070**

<sup>[1]</sup>Esta actualización solo se ofrece a los clientes que ejecuten SQL Server Reporting Services (SSRS).

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS12-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, vea [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/wsus/default).

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de System Center Configuration Manager, vea [Recursos técnicos de System Center](http://technet.microsoft.com/es-es/systemcenter/bb980621).

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

-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.hpenterprisesecurity.com/products/hp-tippingpoint-network-security/), por informar de un problema descrito en MS12-064
-   Un investigador anónimo, en colaboración con el programa [SecuriTeam Secure Disclosure de Beyond Security](http://www.beyondsecurity.com/ssd.html), por informar de un problema descrito en MS12-064
-   Drew Hintz y Andrew Lyons, de [Google Security Team](http://www.google.com/), por informar de un problema descrito en MS12-066
-   Will Dorman, de [CERT/CC](http://www.cert.org/), por colaborar con nosotros en 13 problemas descritos en MS12-067
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS12-068

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de octubre de 2012): Publicación del resumen del boletín.
-   V1.1 (10 de octubre de 2012): para MS12-068 y MS12-069, se ha corregido la evaluación de explotabilidad correspondiente a la última versión del software en **Índice de** **explotatibiliad** para CVE-2012-2529 y CVE-2012-2551, respectivamente. Para MS12-066, se han corregido los números de KB para Microsoft Lync 2010 Attendee (instalación de nivel administrativo) y Microsoft Lync 2010 Attendee (instalación de nivel de usuario).
-   V1.2 (17 de octubre de 2012): Para MS12-066, se han corregido los números de KB para Microsoft Lync 2010 Attendee (instalación de nivel administrativo) y Microsoft Lync 2010 Attendee (instalación de nivel de usuario).
-   V1.3 (23 de octubre de 2012): para MS12-066, se agregaron Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 32 bits) y Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versión de 64 bits) a la sección **Ubicaciones de descarga y software** **afectado** . Se trata únicamente de un cambio informativo. No había cambios en la lógica de detección o en los archivos de la actualización de seguridad.

*Built at 2014-04-18T01:50:00Z-07:00*
