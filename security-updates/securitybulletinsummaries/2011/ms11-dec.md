---
TOCTitle: 'MS11-DEC'
Title: Resumen del boletín de seguridad de Microsoft de diciembre 2011
ms:assetid: 'ms11-dec'
ms:contentKeyID: 61225422
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms11-dec(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de diciembre 2011
===============================================================

Publicado: martes, 13 de diciembre de 2011 | Actualizado: miércoles, 22 de febrero de 2012

**Versión:** 2.1

Este resumen del boletín enumera los boletines de seguridad publicados para diciembre de 2011.

Con la publicación de los boletines de seguridad de diciembre de 2011, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 28 de diciembre de 2011. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 14 de diciembre de 2011, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de diciembre](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032487961). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre el boletín de seguridad fuera de ciclo el 29 de diciembre de 2011, a la 1:00 p.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad el 29 de diciembre a la 1:00 p.m](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032502798&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-087">MS11-087</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores en modo kernel de Windows podría permitir la ejecución remota de código (2639417)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un documento especialmente diseñado o visita una página web malintencionada que inserta archivos de fuentes TrueType.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-090">MS11-090</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa de bits de interrupción de ActiveX (2618451)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el software de Microsoft. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada que use un comportamiento binario específico en Internet Explorer. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. Esta actualización también incluye bits de interrupción para cuatro controles ActiveX de terceros.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-092">MS11-092</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows Media podría permitir la ejecución remota de código (2648048)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en Reproductor de Windows Media y Windows Media Center de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de grabación de vídeo digital de Microsoft (.dvr-ms) especialmente diseñado. En todos los casos, no se puede obligar al usuario a que abra el archivo; para que el ataque se lleve a cabo, se debe convencer al usuario de que lo abra.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-088">MS11-088</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office IME (chino) podría permitir la elevación</strong> <strong>de privilegios (2652016)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office IME (chino). La vulnerabilidad podría permitir la elevación de privilegios si un usuario con la sesión iniciada realizara acciones específicas en un sistema donde esté instalada una versión afectada del editor de métodos de entrada (IME) de Microsoft Pinyin (MSPY) para chino simplificado. Un atacante que consiguiera aprovechar esta vulnerabilidad podría ejecutar código arbitrario en modo kernel. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos administrativos. Solo las implementaciones de Microsoft Pinyin IME 2010 están afectadas por esta vulnerabilidad. Otras versiones de IME de chino simplificado y otras implementaciones de IME no están afectadas.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-089">MS11-089</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office podría permitir la ejecución remota de código (2590602)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Word especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-091">MS11-091</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Publisher podrían permitir la ejecución remota de código (2607702)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades más graves podrían permitir la ejecución remota de código si un usuario abre un archivo de Publisher especialmente diseñado. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-093">MS11-093</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en OLE podría permitir la ejecución remota de código (2624667)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en todas las ediciones compatibles de Windows XP y Windows Server 2003. Esta actualización de seguridad se considera importante para todas las ediciones compatibles de Windows XP y Windows Server 2003. Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 no están afectados por la vulnerabilidad.<br />
<br />
La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo que contiene un objeto OLE especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-094">MS11-094</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft PowerPoint podrían permitir la ejecución remota de código (2639142)</strong> <br />
<br />
Esta actualización de seguridad resuelve dosvulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de PowerPoint especialmente diseñado. Un atacante que aprovechara cualquiera de las vulnerabilidades podría lograr el control total de un sistema afectado. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-095">MS11-095</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Active Directory podría permitir la ejecución remota de código (2640045)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Active Directory, Active Directory Application Mode (ADAM) y servicio de directorio ligero de Active Directory (AD LDS). La vulnerabilidad podría permitir la ejecución remota de código si un atacante inicia sesión en un dominio de Active Directory y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, el atacante primero debe adquirir las credenciales para iniciar sesión en un directorio de Active Directory.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-096">MS11-096</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Excel podría permitir la ejecución remota de código (2640241)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La instalación y configuración de Validación de documento de Office (OFV) para prevenir la apertura de archivos sospechosos bloquea las vías de ataque para aprovechar las vulnerabilidades descritas en CVE-2011-3403.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-097">MS11-097</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el subsistema de tiempo de ejecución de cliente-servidor de Windows podría permitir la elevación de privilegios (2620712)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada para enviar un mensaje de evento de dispositivo a un proceso de mayor integridad. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-098">MS11-098</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el kernel de Windows podría permitir la elevación de privilegios (2633171)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada para aprovechar la vulnerabilidad. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-099">MS11-099</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2618444 )</strong> <br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario abre un archivo de lenguaje de marcado de hipertexto (HTML) legítimo que se encuentre en el mismo directorio que un archivo de biblioteca de vínculos dinámicos (DLL) especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-100">MS11-100</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en .NET Framework podrían permitir la elevación de privilegios (2638420)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y tres vulnerabilidades de las que se ha informado de forma privada en Microsoft .NET Framework. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un atacante no autenticado envía una solicitud web especialmente diseñada al sitio de destino. Un atacante que consiguiera aprovechar esta vulnerabilidad podría realizar cualquier acción en el contexto de una cuenta existente en el sitio ASP.NET, incluida la ejecución de comandos arbitrarios. Para aprovechar esta vulnerabilidad, el atacante debe poder registrar una cuenta en el sitio ASP.NET y debe conocer un nombre de usuario existente.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft .NET Framework</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.
  
| Identificador del boletín                                                 | Título de vulnerabilidad                                                                        | Identificador CVE                                                                | Evaluación de explotabilidad para la última versión de software                                                               | Evaluación de explotabilidad para la versión de software anterior                                                             | Evaluación de explotabilidad de denegación de servicio | Notas clave                                                                                                                                                                                                                                                         |  
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS11-087](http://technet.microsoft.com/es-es/security/bulletin/ms11-087) | Vulnerabilidad de análisis de fuentes TrueType                                                  | [CVE-2011-3402](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3402) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | Esa vulnerabilidad ya se ha divulgado.                                                                                                                                                                                                                              |  
| [MS11-088](http://technet.microsoft.com/es-es/security/bulletin/ms11-088) | Vulnerabilidad de elevación de privilegios en IME de Pinyin                                     | [CVE-2011-2010](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-2010) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No está afectada                                                                                                              | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-089](http://technet.microsoft.com/es-es/security/bulletin/ms11-089) | Vulnerabilidad en el uso de Word después de la liberación                                       | [CVE-2011-1983](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1983) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-090](http://technet.microsoft.com/es-es/security/bulletin/ms11-090) | Vulnerabilidad de ejecución remota de código de Microsoft Time                                  | [CVE-2011-3397](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3397) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-091](http://technet.microsoft.com/es-es/security/bulletin/ms11-091) | Vulnerabilidad de índice de matriz fuera de los límites en Publisher                            | [CVE-2011-3410](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3410) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-091](http://technet.microsoft.com/es-es/security/bulletin/ms11-091) | Vulnerabilidad de puntero no válido en Publisher                                                | [CVE-2011-3411](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3411) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-091](http://technet.microsoft.com/es-es/security/bulletin/ms11-091) | Vulnerabilidad de daños en la memoria relacionada con Publisher                                 | [CVE-2011-3412](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3412) | No está afectada                                                                                                              | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-092](http://technet.microsoft.com/es-es/security/bulletin/ms11-092) | Vulnerabilidad de daños en la memoria relacionada con DVR-MS en Reproductor de Windows Media    | [CVE-2011-3401](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3401) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-093](http://technet.microsoft.com/es-es/security/bulletin/ms11-093) | Vulnerabilidad de propiedad OLE                                                                 | [CVE-2011-3400](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3400) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-094](http://technet.microsoft.com/es-es/security/bulletin/ms11-094) | Vulnerabilidad en la carga de bibliotecas no seguras en PowerPoint                              | [CVE-2011-3396](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3396) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | Microsoft PowerPoint 2010 está afectado únicamente si no está instalado el último Service Pack.                                                                                                                                                                     |  
| [MS11-094](http://technet.microsoft.com/es-es/security/bulletin/ms11-094) | Vulnerabilidad de ejecución remota de código en formas de OfficeArt                             | [CVE-2011-3413](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3413) | No está afectada                                                                                                              | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-095](http://technet.microsoft.com/es-es/security/bulletin/ms11-095) | Vulnerabilidad de desbordamiento de búfer en Active Directory                                   | [CVE-2011-3406](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3406) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | Solo los sistemas que ejecutan Active Directory, AD LDS o ADAM están afectados.                                                                                                                                                                                     |  
| [MS11-096](http://technet.microsoft.com/es-es/security/bulletin/ms11-096) | Vulnerabilidad de daños en la memoria relacionada con registros                                 | [CVE-2011-3403](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3403) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-097](http://technet.microsoft.com/es-es/security/bulletin/ms11-097) | Vulnerabilidad de elevación de privilegios locales en CSRSS                                     | [CVE-2011-3408](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3408) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-098](http://technet.microsoft.com/es-es/security/bulletin/ms11-098) | Vulnerabilidad del controlador de excepciones del kernel de Windows                             | [CVE-2011-2018](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-2018) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-099](http://technet.microsoft.com/es-es/security/bulletin/ms11-099) | Vulnerabilidad de divulgación de información en el filtro XSS                                   | [CVE-2011-1992](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1992) | [3](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código que aproveche la vulnerabilidad     | [3](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código que aproveche la vulnerabilidad     | No aplicable                                           | Esta vulnerabilidad afecta a la divulgación de información.                                                                                                                                                                                                         |  
| [MS11-099](http://technet.microsoft.com/es-es/security/bulletin/ms11-099) | Vulnerabilidad en la carga de bibliotecas no seguras en Internet Explorer                       | [CVE-2011-2019](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-2019) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No está afectada                                                                                                              | No aplicable                                           | (Ninguna)                                                                                                                                                                                                                                                           |  
| [MS11-100](http://technet.microsoft.com/es-es/security/bulletin/ms11-100) | Vulnerabilidad de colisiones en HashTable que pueden provocar la denegación de servicio         | [CVE-2011-3414](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3414) | [3](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código que aproveche la vulnerabilidad     | [3](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código que aproveche la vulnerabilidad     | Temporal                                               | Esta vulnerabilidad solo es una denegación de servicio y se ha divulgado de forma pública.[Las vulnerabilidades de denegación de servicio reciben una clasificación de índice de explotabilidad de "3".](http://technet.microsoft.com/en-us/security/cc998259.aspx) |  
| [MS11-100](http://technet.microsoft.com/es-es/security/bulletin/ms11-100) | Vulnerabilidad de omisión de la autenticación de formularios de ASP.Net                         | [CVE-2011-3416](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3416) | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | Elevación de privilegios: control de cuenta                                                                                                                                                                                                                         |  
| [MS11-100](http://technet.microsoft.com/es-es/security/bulletin/ms11-100) | Vulnerabilidad de almacenamiento en caché de vale de la autenticación de formularios de ASP.Net | [CVE-2011-3417](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-3417) | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | No aplicable                                           | Elevación de privilegios: control de cuenta                                                                                                                                                                                                                         |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows
  
**Tabla 1**

 
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
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b01bb041-005c-48c4-a606-66aa264ba0fa)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=21b4b999-2dbf-4921-80bd-cc7ab2cd1190)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d85091b5-69bb-4d0f-839a-a65cd94e2887)  
(KB2619339)  
(Crítica)  

[Windows XP Media Center Edition 2005 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=03bc6446-7cf3-47c4-8ed1-a53a4d53a429)  
(KB2619340)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=73531165-f299-4b62-b738-52fca410eaae)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=3b816964-d3c3-4f05-94c3-f54a6f54ca73)  
(KB2626416)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=edb594a4-14d2-4ffe-8d1c-2c283689fe8c)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0a872cd2-5f4d-400c-a1c4-a2d194746fb6)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=126e8092-980d-471a-867d-d5939671b7df)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d1d1e9a-603c-4895-a69f-b61186a75ad5)  
(KB2619339)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a98bb7cf-9939-4927-8d21-ccb3845e7cb7)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=986f0087-c674-4060-8710-af3496adbfdd)  
(KB2626416)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9e1273e2-7775-40b4-b939-ab530677cd4a)  
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
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e84e6964-1580-41ef-9d3e-4d0c3ad4cb69)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dfb948c5-8aee-4bcd-babf-3564b78712dd)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6b555040-1117-4b06-a48c-02f0e1b686d8)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=01caf06f-777d-4ea8-95ca-e11d60a973ad)  
(KB2621146)  
(Importante)  

[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=6f7c7ccd-22a3-4fbc-bf21-bd0e42ab1da5)  
(KB2626416)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a14057e5-e2c2-4dde-8d26-542a9f162e98)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9d9f3667-3fd6-4948-83db-282783599f41)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2d37a8cb-2316-4db4-980c-11b6dcbdc696)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb17782c-f754-42ab-905b-6f141df008c3)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=e1ba50cf-fc6b-4668-b71c-e9f75a8ac638)  
(KB2621146)  
(Importante)  

[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=1b610eb3-456c-4125-94b7-1ead4face8e3)  
(KB2626416)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7f595fd6-bdfd-4075-97e5-70efb7d49dff)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=1ecf72cd-6732-4cf3-aa22-8caf15ea633e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=7726ddbe-0578-44fb-a40f-49b804a45989)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=4cdde8a9-6d44-41fa-82c0-a25404cdfbb5)  
(Importante)
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=74099261-60ad-4c68-906c-60e131818955)  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=147ec6d3-3401-4aa3-a409-55346bcc7bd7)  
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
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7f69ec9d-43ad-4106-90ef-c191e7ec43af)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1dd069a2-fb1a-4f31-88cc-bc031c3e2c80)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e9130fad-de8c-4be0-aea1-62cbaa310b76)  
(KB2619339)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=470da512-2c8b-4ba9-b7bb-b9e6c45cd33f)  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fa6e6d91-4aca-49a6-a6e8-c33ec413097e)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ae1f1f86-6f13-4e1e-9f93-4f70b6c9927e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=60fd5bf6-e820-44f6-8081-b98c0103acc1)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b7c4bf05-eb2d-48ac-a6df-8afd88e811d8)  
(KB2619339)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=8daf9a49-60cb-4813-ac7a-e9a4bf296889)  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c9794756-803d-48ba-86db-350fb577f01b)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
<td style="border:1px solid black;">
Ninguna
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
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c4ba344d-dd0d-4cfb-81d9-d364d7f37e25)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f485d4c3-a4af-4ae6-9404-e79afcbb4f6e)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=6f9ddcdb-a471-4e00-a697-92a24e4ea8d4)\*  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6f934885-b134-400c-a452-50fd4eeedd5e)\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=058963f6-9654-41d0-86d2-f25a0c2ad416)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=28598ef6-13fb-44fd-8c76-599af7b0a01d)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=5253477b-422f-404a-941e-8b69da5a2670)\*  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7ade3832-bc20-4fce-8eac-8a3d072d2f1c)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=42cd1c33-11a7-4a29-ae85-f7272a626f91)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5915e19c-b576-453b-b621-5737774f5955)  
(Sin clasificación de gravedad<sup>[1]</sup>)
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
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4bd7a02b-c6d8-4eb5-a46d-e494a1233dc8)  
(Importante)
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
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0526727a-f2fb-4846-9b04-f1899f52f1f6)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d112623c-86ce-434a-8fe1-ec3e3e632763)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b6e44069-dec5-48f6-8fc4-8ab375a10b4e)  
(KB2619339)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=d2e87199-6469-4bc0-a721-f43e817e4344)  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0666bdf5-9eed-44c9-84ee-b45f9b3e14b3)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cfd42c42-1595-419a-bf04-b23b64663629)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=81114ecd-0c73-4ca6-8a66-09c6c636a5db)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f7997ab8-27e0-4714-845a-d237f4326587)  
(KB2619339)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=ba8d7aa9-8299-49a3-b0c0-b8b5eab48434)  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=620f94f9-1f61-45a0-a22e-e7510b56b9b8)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-087**](http://go.microsoft.com/fwlink/?linkid=233008)
</td>
<td style="border:1px solid black;">
[**MS11-090**](http://go.microsoft.com/fwlink/?linkid=232507)
</td>
<td style="border:1px solid black;">
[**MS11-092**](http://go.microsoft.com/fwlink/?linkid=232517)
</td>
<td style="border:1px solid black;">
[**MS11-093**](http://go.microsoft.com/fwlink/?linkid=232516)
</td>
<td style="border:1px solid black;">
[**MS11-095**](http://go.microsoft.com/fwlink/?linkid=232666)
</td>
<td style="border:1px solid black;">
[**MS11-097**](http://go.microsoft.com/fwlink/?linkid=232663)
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
Ninguna
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d64a31ca-cccd-488a-98fd-c059b9e9e1ea)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=bc018647-08cb-431a-8e7c-5dc04980eaa9)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Active Directory y servicio de directorio ligero de Active Directory (AD LDS)](http://www.microsoft.com/downloads/details.aspx?familyid=a3e0d27c-8b29-4981-bdef-bcd037fd3408)\*  
(KB2621146)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=04878e9a-539a-4549-a5af-11d45add91da)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b46f6da7-6d24-4262-8e55-3b657db39813)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9323b9b9-e9b0-4941-afe0-196d22df9ab4)  
(Sin clasificación de gravedad<sup>[1]</sup>)
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
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5b2ebec4-cebb-47b6-864a-12d59a9a3e18)  
(Importante)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*\*\*La instalación de Server Core está afectada.** Esta actualización se aplica, con una clasificación de gravedad inferior, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, cuando se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Nota para MS11-090**

<sup>[1]</sup>Este sistema operativo específico no está afectado por la vulnerabilidad descrita en este boletín. La actualización disponible establece los bits de interrupción para los controles de terceros.

**Tabla 2**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=7a6fcf8d-8c7b-4882-90d3-02db79a75238)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=caa9360b-2fd8-4f46-99e6-2decf1b60ca7)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=dc6dcd8c-c39f-4c4b-b5b2-b4c18c36973b)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f3906245-b6f6-464a-84b6-e1b6b195df95)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff633f7-abd9-45cc-acbd-4885123dbed2)  
(KB2656352)  
  
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=2fa77733-70f5-46ff-9cfe-2262d292b870)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a0c55d9b-8529-4d3d-910d-1a822a825be2)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=3e60e996-8850-4d25-b994-39646e2cc25e)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff633f7-abd9-45cc-acbd-4885123dbed2)  
(KB2656352)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=281e5bd4-4582-4aa9-af88-518ad3152132)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=759041cf-fd8b-4e04-b289-d74112bf978b)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b1b4af92-3ff1-4727-9ba3-52764a7b81bb)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=1cbe9469-05f4-4305-bbfd-76b4a04cd598)  
(Baja)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7538762a-50e9-4f13-a60e-ff99aa8fbbf8)  
(KB2656358)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff633f7-abd9-45cc-acbd-4885123dbed2)  
(KB2656352)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=5587eca8-86e9-4a63-81cb-81f68178a6c0)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7a87f890-f106-41ab-bc53-4ca44dc99cb1)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=a42fa727-482c-4578-9a30-61fdf14ed4da)  
(Baja)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff633f7-abd9-45cc-acbd-4885123dbed2)  
(KB2656352)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=02d5c057-d551-411b-917b-43d7795111bc)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2fccb214-6c79-4ef6-9d6e-df4f16ef792e)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff633f7-abd9-45cc-acbd-4885123dbed2)  
(KB2656352)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a6c7c960-768d-40d4-8fe5-7d59f48ead1d)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0adc422f-73f2-46ee-973f-9b7603a76d1e)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4327147b-0481-4172-a835-8786abc50596)  
(Importante)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=a0b19b35-1d48-4419-ba3d-66063cc472a7)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49050cf2-949a-40e5-b2ee-6257a3837294)  
(KB2656362)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=8a3f2351-380b-4566-b186-906dca426d39)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=987f0966-01de-4edf-a0d6-4032d1d72966)  
(Importante)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c951044b-4596-462f-bc8f-bdd9d6734297)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49050cf2-949a-40e5-b2ee-6257a3837294)  
(KB2656362)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5a4443f8-fec8-42be-ad67-8475920f1460)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=eaf587f0-9951-4480-a08b-377e61aaf72b)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8f5af52f-dece-4f0c-9fc0-d4973e4f7b1a)\*\*  
(Baja)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c03e65d6-4f92-4bc1-94b5-2f0183d0133e)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)\*\*  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49050cf2-949a-40e5-b2ee-6257a3837294)\*\*  
(KB2656362)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)\*\*  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)\*\*<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2f18fc98-984a-4c02-951f-b8438a9e4f6b)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=808d26f7-c8fa-446d-9d2f-e8c0babb0c4a)\*\*  
(Baja)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b7a582f3-0a18-4fbf-9b99-21c664bfd979)\*\*  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)\*\*  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49050cf2-949a-40e5-b2ee-6257a3837294)\*\*  
(KB2656362)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)\*\*  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)\*\*<sup>[1]</sup>
(KB2656351)
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=fc62df39-7185-448b-b356-25a5a07886ec)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=471e1f51-c79c-4285-9f1e-aee1e4c4f189)  
(KB2656353)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49050cf2-949a-40e5-b2ee-6257a3837294)  
(KB2656362)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=306acd0a-bea2-40dd-a639-f381587c9eb7)  
(KB2657424)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=eb2bd108-5ef1-45be-9157-e7cbfc8afd2a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=018610bb-e80a-432a-8f32-f50451f71ad9)  
(Importante)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ec2046a6-f069-4f02-9600-7640e57be0a3)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=2de28d32-1efd-4177-82e6-19a08266096c)  
(KB2656355)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)  

Windows 7 para sistemas de 32 bits Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=26e0b56d-9228-49cf-9276-0741257567a9)  
(KB2656356)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
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
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=dbe85b05-e252-4029-8e25-f2452db1c017)  
(Importante)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=4c773b3d-0ca3-4b9b-af9a-9d6edcd261f7)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=2de28d32-1efd-4177-82e6-19a08266096c)  
(KB2656355)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)  

Windows 7 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=26e0b56d-9228-49cf-9276-0741257567a9)  
(KB2656356)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-098**](http://go.microsoft.com/fwlink/?linkid=232424)
</td>
<td style="border:1px solid black;">
[**MS11-099**](http://go.microsoft.com/fwlink/?linkid=232505)
</td>
<td style="border:1px solid black;">
[**MS11-100**](http://go.microsoft.com/fwlink/?linkid=232432)
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
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2108b4ef-942f-4727-a1fc-ee7d0abb427c)\*\*  
(Baja)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=72c1654e-526f-4ece-b7ad-767a0710e076)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=2de28d32-1efd-4177-82e6-19a08266096c)\*  
(KB2656355)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=26e0b56d-9228-49cf-9276-0741257567a9)\*  
(KB2656356)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)\*<sup>[1]</sup>
(KB2656351)
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
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=74614510-e13c-43e8-90e7-d81e63895cf2)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=2de28d32-1efd-4177-82e6-19a08266096c)  
(KB2656355)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)  

Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=26e0b56d-9228-49cf-9276-0741257567a9)  
(KB2656356)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=37a8fb34-e3ad-4605-980b-28361889ce72)<sup>[1]</sup>
(KB2656351)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Nota para MS11-099**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado porque las vías de ataque conocidas para la vulnerabilidad tratada en este boletín están bloqueadas en una configuración predeterminada. No obstante, como medida de defensa en profundidad, Microsoft recomienda que los clientes de este software apliquen esta actualización de seguridad.

**Nota para MS11-100**

<sup>[1]</sup>**.NET Framework 4 y .NET Framework 4 Client Profile están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/es-es/library/5a4x27ek.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="6" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-088**](http://go.microsoft.com/fwlink/?linkid=227070)
</td>
<td style="border:1px solid black;">
[**MS11-089**](http://go.microsoft.com/fwlink/?linkid=225739)
</td>
<td style="border:1px solid black;">
[**MS11-091**](http://go.microsoft.com/fwlink/?linkid=235287)
</td>
<td style="border:1px solid black;">
[**MS11-094**](http://go.microsoft.com/fwlink/?linkid=232493)
</td>
<td style="border:1px solid black;">
[**MS11-096**](http://go.microsoft.com/fwlink/?linkid=232696)
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
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Publisher 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=13f3e884-37bf-4ed2-b3ed-a0e7fb48e44f)  
(KB2553084)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=5859014f-afc5-4958-82ea-6ba45a5ad4b3)  
(KB2596954)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2 y Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2 y Microsoft Office 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e924cd85-5764-4056-bd32-b0e57dc25146)  
(KB2596785)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Publisher 2007 Service Pack 2 y Microsoft Publisher 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2856821e-f1fd-424b-b03c-e443685eea6d)  
(KB2596705)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d0c3156c-c87c-4d3e-aca2-3fab9ff78711)  
(KB2596764)  
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
[Microsoft Pinyin IME 2010 (versión de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d812621e-c35a-4cb0-ba26-928363f3422d)  
(KB2596511)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e47c0694-a9a5-4dd7-bfba-e470d9855c28)  
(KB2589320)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=fd32d083-46e7-4835-ba83-c33332b920bd)  
(KB2553185)  
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
[Microsoft Pinyin IME 2010 (versión de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=c8d3ac17-5aca-4da3-961f-b753be4a3634)  
(KB2596511)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=6c2d5273-eef9-4ff6-be6f-8d86f417f004)  
(KB2589320)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f28b8cf6-8946-448a-ae4e-d11f8a76a679)  
(KB2553185)  
(Importante)
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
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-088**](http://go.microsoft.com/fwlink/?linkid=227070)
</td>
<td style="border:1px solid black;">
[**MS11-089**](http://go.microsoft.com/fwlink/?linkid=225739)
</td>
<td style="border:1px solid black;">
[**MS11-091**](http://go.microsoft.com/fwlink/?linkid=235287)
</td>
<td style="border:1px solid black;">
[**MS11-094**](http://go.microsoft.com/fwlink/?linkid=232493)
</td>
<td style="border:1px solid black;">
[**MS11-096**](http://go.microsoft.com/fwlink/?linkid=232696)
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
<td style="border:1px solid black;">
Ninguna
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
Microsoft Office 2004 para Mac
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
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=ef3b559c-0bd2-45dd-8049-6946f6431a2a)  
(KB2644358)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
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
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=2c4d0381-f7ab-49ed-a0c0-b381387d1e68)  
(KB2644354)  
(Importante)
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
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=3c8017d6-232c-42a6-a133-96efe3ad3385)  
(KB2644347)  
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
<th colspan="6" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-088**](http://go.microsoft.com/fwlink/?linkid=227070)
</td>
<td style="border:1px solid black;">
[**MS11-089**](http://go.microsoft.com/fwlink/?linkid=225739)
</td>
<td style="border:1px solid black;">
[**MS11-091**](http://go.microsoft.com/fwlink/?linkid=235287)
</td>
<td style="border:1px solid black;">
[**MS11-094**](http://go.microsoft.com/fwlink/?linkid=232493)
</td>
<td style="border:1px solid black;">
[**MS11-096**](http://go.microsoft.com/fwlink/?linkid=232696)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft PowerPoint Viewer 2007 Service Pack 2
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
[Microsoft PowerPoint Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4417592a-8db0-4e35-9895-d589bc341077)  
(KB2596912)  
(Importante)
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e799f654-7e2d-40c7-a3b8-32e44d1aa6ee)  
(KB2596843)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Pinyin SimpleFast Style 2010 y Microsoft Office Pinyin New Experience Style 2010 (versión de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office Pinyin SimpleFast Style 2010 y Microsoft Office Pinyin New Experience Style 2010 (versión de 32 bits)<sup>[1]</sup>
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
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Pinyin SimpleFast Style 2010 y Microsoft Office Pinyin New Experience Style 2010 (versión de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office Pinyin SimpleFast Style 2010 y Microsoft Office Pinyin New Experience Style 2010 (versión de 64 bits)<sup>[1]</sup>
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
No aplicable
</td>
</tr>
</table>
 
**Nota para MS11-088**

<sup>[1]</sup>Ya no se ofrece soporte para esta versión de Microsoft Office Pinyin.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Últimas actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/default.aspx).

**System Center Configuration Manager 2007**

La administración de actualizaciones de software de Configuration Manager 2007 simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con Configuration Manager 2007, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en Configuration Manager 2007 detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en Configuration Manager 2007 se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar Configuration Manager 2007 para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx). Para obtener más información acerca de Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx).

**Systems Management Server 2003**

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

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Symantec y Laboratory of Cryptography and System Security (CrySyS), por colaborar con nosotros en un problema descrito en MS11-087
-   Yang Yanbei, por informar de un problema descrito en MS11-088
-   Nikita Tarakanov (equipo de investigación de CISS) y Alexey Sintsov (Digital Security Research Group), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-089
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de un problema descrito en MS11-090
-   Will Dormann, de [CERT/CC](http://www.cert.org/), por informar de tres problemas descritos en MS11-091
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de un problema descrito en MS11-092
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de un problema descrito en MS11-093
-   Greg MacManus, de [iSIGHT Partners Labs](http://www.isightpartners.com/), por informar de un problema descrito en MS11-094
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-094
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de un problema descrito en MS11-096
-   Alex Ionescu, de Winsider Seminars &amp; Solutions Inc., por informar de un problema descrito en MS11-097
-   Matthew Jurczyk, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-098
-   Thomas Stehle, por informar de un problema descrito en MS11-099
-   Tavis Ormandy, de [Citrix Security Team](http://www.citrix.com), por informar de un problema descrito en MS11-099
-   [Robert Swiecki](http://www.swiecki.net/)
-   , de
-   [Google Inc.](http://www.google.com/)
-   , por informar de un problema descrito en MS11-099
-   [Yosuke Hasegawa](http://utf-8.jp/)
-   , por colaborar con nosotros en un problema descrito en MS11-099
-   [Jan Schejbal](http://janschejbal.wordpress.com/)
-   , por colaborar con nosotros en los cambios de defensa en profundidad incluidos en MS11-099
-   Irene Abezgauz, de [Seeker](http://www.seekersec.com), por informar de un problema descrito en MS11-100
-   Kestutis Gudinavicius, de [SEC Consult](https://www.sec-consult.com/), por informar de un problema descrito en MS11-100
-   Oliver Dewdney, de [LBi](http://www.lbi.com/), por informar de un problema descrito en MS11-100

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY (1-866-727-2338). Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, vea [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico internacional](http://go.microsoft.com/fwlink/?linkid=21155).

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (13 de diciembre de 2011): Publicación del resumen del boletín.
-   V1.1 (13 de diciembre de 2011): Para MS11-099, se han corregido las clasificaciones de gravedad en la tabla Software afectado. Para MS11-088, se ha corregido la nota clave en el índice de explotabilidad. Sólo son cambios informativos. No había cambios en los archivos de la actualización de seguridad o en la lógica de la detección.
-   V2.0 (29 de diciembre de 2011): Se ha agregado al boletín de seguridad de Microsoft MS11-100: Vulnerabilidades en .NET Framework podrían permitir la elevación de privilegios (2638420). También se ha agregado un vínculo de webcast de boletín para este boletín de seguridad fuera de ciclo.
-   V2.1 (22 de febrero de 2012): Para MS11 -088, se ha aclarado el estado de soporte técnico de Microsoft Office Pinyin SimpleFast Style 2010 y Microsoft Office Pinyin New Experience Style 2010. Ya no se ofrece soporte técnico para estas versiones de Microsoft Office Pinyin. Consulte el boletín para obtener más detalles.

*Built at 2014-04-18T01:50:00Z-07:00*
