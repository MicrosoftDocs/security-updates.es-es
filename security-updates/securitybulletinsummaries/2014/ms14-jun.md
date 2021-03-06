---
TOCTitle: 'MS14-JUN'
Title: Resumen del boletín de seguridad de Microsoft de junio de 2014
ms:assetid: 'ms14-jun'
ms:contentKeyID: 62490095
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-jun(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de junio de 2014
==============================================================

Publicado: 10 de junio de 2014 | Actualizado: 17 de junio de 2014

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2014.

Con la publicación de los boletines de seguridad de junio de 2014, este resumen del boletín reemplaza a la notificación de avance de boletines publicada originalmente el 5 de junio de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 11 de junio de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032572980&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Software afectado**.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2969262)<br />
<br />
</strong>Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma pública y cincuenta y siete vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el componente de gráficos de Microsoft podrían permitir la ejecución remota de código (2967487)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows, Microsoft Office y Microsoft Lync. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo o una página web especialmente diseñados. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft Office, Microsoft Lync</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400971">MS14-034</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Word podría permitir la ejecución remota de código (2969261)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una versión afectada de Microsoft Word. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=398119">MS14-033</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft XML Core Services podría permitir la divulgación de información (2966061)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la divulgación de información si un usuario que ha iniciado sesión visita un sitio web especialmente diseñado para invocar Microsoft XML Core Services (MSXML) a través de Internet Explorer. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos a un sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o una solicitud de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400969">MS14-032</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Lync Server podría permitir la divulgación de información (2969258)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Lync Server. La vulnerabilidad podría permitir la divulgación de información si un usuario intenta unirse a una reunión de Lync haciendo clic en una dirección URL de reunión especialmente diseñada.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Lync Server</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396824">MS14-031</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el protocolo TCP podría permitir la denegación de servicio (2962478)<br />
</strong><br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía una secuencia de paquetes especialmente diseñados al sistema de destino.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400970">MS14-030</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Escritorio remoto podría permitir la alteración (2969259)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la alteración si un atacante obtiene acceso al mismo segmento de red que el sistema de destino durante una sesión de protocolo de Escritorio remoto (RDP) activa y, a continuación, envía paquetes RDP especialmente diseñados al sistema de destino. De forma predeterminada, RDP no está habilitado en ningún sistema operativo Windows. Los sistemas que no tienen RDP habilitado no están expuestos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Alteración</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
 
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/security/cc998259).
  
En las columnas siguientes, “Última versión de software” hace referencia al software en cuestión y “Versiones de software anteriores” hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas “Software afectado” y “Software no afectado” del boletín.
  
<p> </p>
<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><strong>Título de vulnerabilidad</strong></td>
<td style="border:1px solid black;"><strong>Identificador CVE</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad para la última versión de software</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad para la versión de software anterior</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad de denegación de servicio</strong></td>
<td style="border:1px solid black;"><strong>Notas clave</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400970">MS14-030</a></td>
<td style="border:1px solid black;">Vulnerabilidad de MAC en RDP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0296">CVE-2014-0296</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de alteración.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396824">MS14-031</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en TCP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1811">CVE-2014-1811</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400969">MS14-032</a></td>
<td style="border:1px solid black;">Vulnerabilidad de saneamiento de contenido en Lync Server</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1823">CVE-2014-1823</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=398119">MS14-033</a></td>
<td style="border:1px solid black;">Vulnerabilidad de URI en entidad de MSXML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1816">CVE-2014-1816</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400971">MS14-034</a></td>
<td style="border:1px solid black;">Vulnerabilidad de fuentes incrustadas</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2778">CVE-2014-2778</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0282">CVE-2014-0282</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1762">CVE-2014-1762</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1764">CVE-2014-1764</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1766">CVE-2014-1766</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1769">CVE-2014-1769</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1770">CVE-2014-1770</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de renegociación de certificado de servidor de TLS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1771">CVE-2014-1771</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1772">CVE-2014-1772</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1773">CVE-2014-1773</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1774">CVE-2014-1774</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1775">CVE-2014-1775</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1777">CVE-2014-1777</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1778">CVE-2014-1778</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1779">CVE-2014-1779</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1780">CVE-2014-1780</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1781">CVE-2014-1781</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1782">CVE-2014-1782</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1783">CVE-2014-1783</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1784">CVE-2014-1784</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1785">CVE-2014-1785</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1786">CVE-2014-1786</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1788">CVE-2014-1788</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1789">CVE-2014-1789</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1790">CVE-2014-1790</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1791">CVE-2014-1791</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1792">CVE-2014-1792</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1794">CVE-2014-1794</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1795">CVE-2014-1795</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1796">CVE-2014-1796</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1797">CVE-2014-1797</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1799">CVE-2014-1799</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1800">CVE-2014-1800</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1802">CVE-2014-1802</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1803">CVE-2014-1803</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1804">CVE-2014-1804</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1805">CVE-2014-1805</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2753">CVE-2014-2753</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2754">CVE-2014-2754</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2755">CVE-2014-2755</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2756">CVE-2014-2756</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2757">CVE-2014-2757</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2758">CVE-2014-2758</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2759">CVE-2014-2759</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2760">CVE-2014-2760</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2761">CVE-2014-2761</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2763">CVE-2014-2763</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2764">CVE-2014-2764</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2765">CVE-2014-2765</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2766">CVE-2014-2766</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2767">CVE-2014-2767</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2768">CVE-2014-2768</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2769">CVE-2014-2769</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2770">CVE-2014-2770</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2771">CVE-2014-2771</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2772">CVE-2014-2772</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2773">CVE-2014-2773</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2775">CVE-2014-2775</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2776">CVE-2014-2776</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2777">CVE-2014-2777</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400972">MS14-035</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2782">CVE-2014-2782</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el procesador de scripts Unicode</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1817">CVE-2014-1817</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Windows afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el procesador de scripts Unicode</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1817">CVE-2014-1817</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Office afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el procesador de scripts Unicode</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1817">CVE-2014-1817</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Lync afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de imágenes en GDI+</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1818">CVE-2014-1818</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Windows afectado.<br />
<br />
Se trata de una vulnerabilidad de denegación de servicio en el software más reciente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de imágenes en GDI+</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1818">CVE-2014-1818</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Office afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=400968">MS14-036</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de imágenes en GDI+</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1818">CVE-2014-1818</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta evaluación de explotabilidad corresponde al software de Microsoft Lync afectado.</td>
</tr>
</tbody>
</table>
  
Software afectado  
-----------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
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
Internet Explorer 6  
(2957689)  
(Importante)  
Internet Explorer 7  
(2957689)  
(Importante)  
Internet Explorer 8  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2003 Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)  
Microsoft XML Core Services 6.0  
(2957482)  
(Baja)
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
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2957689)  
(Importante)  
Internet Explorer 7  
(2957689)  
(Importante)  
Internet Explorer 8  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2003 x64 Edition Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)  
Microsoft XML Core Services 6.0  
(2957482)  
(Baja)
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
(2957689)  
(Importante)  
Internet Explorer 7  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)  
Microsoft XML Core Services 6.0  
(2957482)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2957689)  
(Crítica)  
Internet Explorer 8  
(2957689)  
(Crítica)  
Internet Explorer 9  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Vista Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2957189)  
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
Internet Explorer 7  
(2957689)  
(Crítica)  
Internet Explorer 8  
(2957689)  
(Crítica)  
Internet Explorer 9  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2957689)  
(Importante)  
Internet Explorer 8  
(2957689)  
(Importante)  
Internet Explorer 9  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2957189)  
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
Internet Explorer 7  
(2957689)  
(Importante)  
Internet Explorer 8  
(2957689)  
(Importante)  
Internet Explorer 9  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows 7**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2957689)  
(Crítica)  
Internet Explorer 9  
(2957689)  
(Crítica)  
Internet Explorer 10  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2963950)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2957689)  
(Crítica)  
Internet Explorer 9  
(2957689)  
(Crítica)  
Internet Explorer 10  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2963950)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2957689)  
(Importante)  
Internet Explorer 9  
(2957689)  
(Importante)  
Internet Explorer 10  
(2957689)  
(Importante)  
Internet Explorer 11  
(2957689)  
(Importante)  
Internet Explorer 11  
(2963950)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Internet Explorer 10  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistema de 32 bits  
(gdi32)  
(2964736)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(gdi32)  
(2964736)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2963950)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(gdi32)  
(2964736)  
(Crítica)  
Windows 8.1 para sistemas de 32 bits  
(gdi32)  
(2965155)  
(Crítica)  
Windows 8.1 para sistemas de 32 bits  
(DirectWrite)  
(2964718)  
(Crítica)  
Windows 8.1 para sistemas de 32 bits  
(DirectWrite)  
(2965161)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)  
Microsoft XML Core Services 3.0  
(2966631)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2957189)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2961858)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2965788)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2966034)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2957689)  
(Crítica)  
Internet Explorer 11  
(2963950)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(gdi32)  
(2964736)  
(Crítica)  
Windows 8.1 para sistemas x64  
(gdi32)  
(2965155)  
(Crítica)  
Windows 8.1 para sistemas x64  
(DirectWrite)  
(2964718)  
(Crítica)  
Windows 8.1 para sistemas x64  
(DirectWrite)  
(2965161)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)  
Microsoft XML Core Services 3.0  
(2966631)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2957189)  
(Importante)  
Windows 8.1 para sistemas x64  
(2961858)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2965788)  
(Importante)  
Windows 8.1 para sistemas x64  
(2966034)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2957689)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(gdi32)  
(2964736)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2957689)  
(Importante)  
Internet Explorer 11  
(2963950)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(gdi32)  
(2964736)  
(Crítica)  
Windows Server 2012 R2  
(gdi32)  
(2965155)  
(Crítica)  
Windows Server 2012 R2  
(DirectWrite)  
(2964718)  
(Crítica)  
Windows Server 2012 R2  
(DirectWrite)  
(2965161)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)  
Microsoft XML Core Services 3.0  
(2966631)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2957189)  
(Importante)  
Windows Server 2012 R2  
(2961858)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2965788)  
(Importante)  
Windows Server 2012 R2  
(2966034)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(gdi32)  
(2964736)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2957689)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(gdi32)  
(2964736)  
(Crítica)  
Windows RT 8.1  
(DirectWrite)  
(2964718)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-035**](http://go.microsoft.com/fwlink/?linkid=400972)
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-033**](http://go.microsoft.com/fwlink/?linkid=398119)
</td>
<td style="border:1px solid black;">
[**MS14-031**](http://go.microsoft.com/fwlink/?linkid=396824)
</td>
<td style="border:1px solid black;">
[**MS14-030**](http://go.microsoft.com/fwlink/?linkid=400970)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación de Server Core) (Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(Windows GDI+)  
(2957503)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(usp10)  
(2957509)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 y Microsoft XML Core Services 6.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
Windows Server 2012 (instalación Server Core)  
(gdi32)  
(2964736)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2957189)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2965788)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(gdi32)  
(2964736)  
(Crítica)  
Windows Server 2012 R2 (instalación Server Core)  
(gdi32)  
(2965155)  
(Crítica)  
Windows Server 2012 R2 (instalación Server Core)  
(DirectWrite)  
(2964718)  
(Crítica)  
Windows Server 2012 R2 (instalación Server Core)  
(DirectWrite)  
(2965161)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0  
(2939576)  
(Baja)  
Microsoft XML Core Services 3.0  
(2966631)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2957189)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2961858)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2965788)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2966034)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-036**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Conjuntos de programas y software de Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-034**](http://go.microsoft.com/fwlink/?linkid=400971)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3  
(2878233)  
(Importante)  
Microsoft Office 2007 Service Pack 3  
(2881069)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Word 2007 Service Pack 3  
(2880515)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-034**](http://go.microsoft.com/fwlink/?linkid=400971)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2863942)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2767915)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)  
(2863942)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)  
(2767915)  
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
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2863942)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2767915)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)  
(2863942)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)  
(2767915)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Paquete de compatibilidad de Microsoft Office**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-034**](http://go.microsoft.com/fwlink/?linkid=400971)
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
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2880513)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-036**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Software y plataformas de comunicaciones de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="3">
**Consola Microsoft Live Meeting 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-032**](http://go.microsoft.com/fwlink/?linkid=400969)
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
</tr>
<tr>
<td style="border:1px solid black;">
Consola Microsoft Live Meeting 2007
</td>
<td style="border:1px solid black;">
Consola Microsoft Live Meeting 2007  
(2968966)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Lync 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-032**](http://go.microsoft.com/fwlink/?linkid=400969)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 (32 bits)  
(2963285)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 (64 bits)  
(2963285)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de usuario)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de usuario)  
(2963282)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de administración)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de administración)  
(2963284)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Server 2010
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Lync Server 2010  
(Web Components Server)  
(2963286)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Lync 2013**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-036**](http://go.microsoft.com/fwlink/?linkid=400968)
</td>
<td style="border:1px solid black;">
[**MS14-032**](http://go.microsoft.com/fwlink/?linkid=400969)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 (32 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 Service Pack 1 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 Service Pack 1 (32 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (32 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 Service Pack 1 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 Service Pack 1 (32 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 (64 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 Service Pack 1 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 Service Pack 1 (64 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (64 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 Service Pack 1 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 Service Pack 1 (64 bits)  
(2881013)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Server 2013
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Lync Server 2013  
(Web Components Server)  
(2963288)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-036**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Hay disponibles varios recursos para ayudar a los administradores a implementar las actualizaciones de seguridad.

Microsoft Baseline Security Analyzer (MBSA) permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan y las configuraciones de seguridad incorrectas más comunes.

Windows Server Update Services (WSUS), Systems Management Server (SMS) y System Center Configuration Manager ayudan a los administradores a distribuir las actualizaciones de seguridad.

Los componentes del Evaluador de compatibilidad de aplicaciones incluidos con el kit de herramientas de compatibilidad de aplicaciones contribuyen a optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas.

Para obtener información acerca de estas y otras herramientas que hay disponibles, vea [Herramientas de seguridad para profesionales de TI](http://technet.microsoft.com/security/cc297183). 

Agradecimientos
---------------

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

**MS14-030**

-   Andrew Swoboda y Tyler Reguly, de [Tripwire](http://www.tripwire.com/), por informar de la vulnerabilidad de MAC en RDP (CVE-2014-0296)

     

**MS14-033**

-   Christian Kulenkampff, por informar de la vulnerabilidad de URI en entidad de MSXML (CVE-2014-1816)

     

**MS14-034**

-   s3tm3m, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de fuentes incrustadas (CVE-2014-2778)

     

**MS14-035**

-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-0282)
-   Renguang Yuan, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-0282)
-   AbdulAziz Hariri, Matt Molinyawe y Jasiel Spelman, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1762)
-   [VUPEN](http://www.vupen.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-1764)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1766)
-   Andreas Schmidt, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1766)
-   IronRock, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1766)
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1766)
-   Atte Kettunen, de [OUSPG](https://www.ee.oulu.fi/research/ouspg/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1769)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1769)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1769)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1769)
-   [Chen Zhang (demi6od)](http://weibo.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1769)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1770)
-   El equipo Prosecco de Institut National de Recherche en Informatique et en Automatique (INRIA), por informar de la vulnerabilidad de renegociación de certificado de servidor de TLS (CVE-2014-1771)
-   [Omair](http://krash.in/), en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1772)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1772)
-   Jack Tang, de [Trend Micro](http://www.trendmicro.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1772)
-   [Venustech Active-Defense Laboratory](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1772)
-   John Villamil y Sean Larsson, por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1773)
-   [Chen Zhang (demi6od)](http://weibo.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1773)
-   AMol NAik, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1774)
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com/) en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1775)
-   Hui Gao, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1775)
-   Arezou Hosseinzad-Amirkhizi, de Vulnerability Research Team, TELUS Security Labs, por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1775)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de divulgación de información en Internet Explorer (CVE-2014-1777)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-1778)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1779)
-   [Soroush Dalili](http://www.secproject.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1780)
-   [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1781)
-   lokihardt@ASRT, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   ZhaoWei de [knownsec](http://www.knownsec.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   35c27308b34d55904da10770e5303503, en colaboración con [iSIGHT Partners GVP Program](https://gvp.isightpartners.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   IronRock, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1782)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1783)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1784)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1784)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1784)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1785)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1785)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1785)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1786)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1788)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1789)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1789)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1790)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1791)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1792)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1792)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1794)
-   Xiaobo Chen, de [FireEye](http://www.fireeye.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1795)
-   Hui Gao, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1796)
-   Gareth Heyes, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1797)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1799)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1799)
-   0016EECD9D7159A949DAD3BC17E0A939, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1799)
-   Sweetchip, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1799)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1800)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1802)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1803)
-   Royce Lu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1804)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1804)
-   lokihardt@ASRT, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1805)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2753)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2754)
-   Xin Ouyang, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2755)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2755)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2756)
-   0016EECD9D7159A949DAD3BC17E0A939, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2756)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2757)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2758)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2759)
-   Sabre, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2759)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2760)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2761)
-   0016EECD9D7159A949DAD3BC17E0A939, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2761)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2763)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2764)
-   [Chen Zhang (demi6od)](http://weibo.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2764)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2764)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2765)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2766)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2767)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2768)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2768)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2769)
-   [Venustech Active-Defense Laboratory](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2769)
-   Xin Ouyang, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2770)
-   Royce Lu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2771)
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com/) en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2772)
-   [Keen Team](http://www.k33nteam.org/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2773)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2773)
-   AbdulAziz Hariri, Matt Molinyawe y Jasiel Spelman, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2775)
-   AbdulAziz Hariri, Matt Molinyawe y Jasiel Spelman, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2776)
-   [VUPEN](http://www.vupen.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-2777)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-2782)
-   Noriaki Iwasaki, de [Cyber Defense Institute, Inc.](http://www.cyberdefense.jp/), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en este boletín

     

**MS14-036**

-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad en el procesador de scripts Unicode (CVE-2014-1817)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de análisis de imágenes en GDI+ (CVE-2014-1818)

Información adicional:
----------------------

### Herramienta de eliminación de software malintencionado de Microsoft Windows

Para la publicación de boletines el segundo martes de cada mes, Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga. No hay disponible ninguna versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows para las publicaciones de boletín de seguridad fuera de ciclo.

### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](https://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/wsus/bb456965). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumerados en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201).

### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](https://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

### Soporte técnico

El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).

Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/security/bb980617)

Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)

Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra “tal cual”, sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

### Revisiones

-   V1.0 (10 de junio de 2014): Publicación del resumen del boletín.
-   V1.1 (17 de junio de 2014): para MS14-035, se ha corregido la evaluación de explotabilidad en Índice de explotabilidad para CVE-2014-2782. Se trata únicamente de un cambio informativo.

*Página generada el 2014-09-18 16:14Z-07:00.*
