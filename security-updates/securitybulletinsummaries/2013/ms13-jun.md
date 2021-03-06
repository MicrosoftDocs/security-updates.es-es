---
TOCTitle: 'MS13-JUN'
Title: Resumen del boletín de seguridad de Microsoft de junio 2013
ms:assetid: 'ms13-jun'
ms:contentKeyID: 61225450
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-jun(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de junio 2013
===========================================================

Publicado: martes, 11 de junio de 2013

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2013.

Con la publicación de los boletines de seguridad de junio de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 6 de junio de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 12 de junio de 2013, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538733&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538733&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Software afectado**.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299498">MS13-047</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2838727)  <br />
<br />
</strong>Esta actualización de seguridad resuelve diecinueve vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara la más grave de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301748">MS13-048</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el</strong> <strong>kernel</strong> <strong>de Windows</strong> <strong>podría permitir la divulgación de información (2839229)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Windows. La vulnerabilidad podría permitir la divulgación de información si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada o convence a un usuario local con la sesión iniciada de ejecutar una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Es importante mencionar que la vulnerabilidad no permitirá al atacante ejecutar código o elevar directamente sus derechos de usuario, pero podría servir para producir información útil que pudiera usarse para tratar de sacar más provecho de un sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301749">MS13-049</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores modo</strong> <strong>kernel</strong> <strong>podría permitir la denegación de servicio (2845690)</strong> <strong><br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía paquetes especialmente diseñados al servidor. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299243">MS13-050</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los componentes del administrador de trabajos de impresión podría permitir la elevación de privilegios (2839894)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios cuando un atacante autenticado elimina una conexión de impresora. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=296303">MS13-051</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office podría permitir la ejecución remota de código (2839571)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un documento de Office especialmente diseñado con una versión afectada del software de Microsoft Office o bien obtiene una vista previa o abre un mensaje de correo electrónico especialmente diseñado en Outlook con Microsoft Word como el lector de correo electrónico. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
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
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.
  
| Identificador del boletín                                 | Título de vulnerabilidad                                   | Identificador CVE                                                                 | Evaluación de explotabilidad para la última versión de software                                                               | Evaluación de explotabilidad para la versión de software anterior                                                       | Evaluación de explotabilidad de denegación de servicio | Notas clave                                                                                  |  
|-----------------------------------------------------------|------------------------------------------------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|----------------------------------------------------------------------------------------------|  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3110](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3110)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3111](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3111)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3112](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3112)  | [2](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3113](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3113)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3114](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3114)  | [2](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3116](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3116)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3117](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3117)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3118](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3118)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No está afectada                                                                                                        | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3119](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3119)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3120](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3120)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No está afectada                                                                                                        | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3121](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3121)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| MS13-047                                                  | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3122](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3122)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| MS13-047                                                  | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3123](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3123)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3124](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3124)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013- 3125](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3125) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No está afectada                                                                                                        | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3139](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3139)  | No aplicable                                                                                                                  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | Se trata de una medida de defensa en profundidad en el software más reciente.                |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3141](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3141)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-047](http://go.microsoft.com/fwlink/?linkid=299498) | Vulnerabilidad de daños en la memoria de Internet Explorer | [CVE-2013-3142](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3142)  | [2](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                                                    |  
| [MS13-048](http://go.microsoft.com/fwlink/?linkid=301748) | Vulnerabilidad de divulgación de información del kernel    | [CVE-2013-3136](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3136)  | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad          | Permanente                                             | Esta vulnerabilidad afecta a la divulgación de información.                                  |  
| [MS13-049](http://go.microsoft.com/fwlink/?linkid=301749) | Vulnerabilidad de desbordamiento de enteros en TCP/IP      | [CVE-2013-3138](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3138)  | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad          | Permanente                                             | Se trata de una vulnerabilidad de denegación de servicio.                                    |  
| [MS13-050](http://go.microsoft.com/fwlink/?linkid=299243) | Vulnerabilidad del administrador de trabajos de impresión  | [CVE-2013-1339](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1339)  | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | Permanente                                             | (Ninguna)                                                                                    |  
| [MS13-051](http://go.microsoft.com/fwlink/?linkid=296303) | Vulnerabilidad de desbordamiento del búfer en Office       | [CVE-2013-1331](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1331)  | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad | No aplicable                                           | Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad. |
  
Software afectado  
-----------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="5" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
**Ninguna**
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
Internet Explorer 6   
(2838727)  
(Crítica)  
Internet Explorer 7   
(2838727)  
(Crítica)  
Internet Explorer 8   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2839229)  
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
(2838727)  
(Crítica)  
Internet Explorer 7   
(2838727)  
(Crítica)  
Internet Explorer 8   
(2838727)  
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
<th colspan="5" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2838727)  
(Moderada)  
Internet Explorer 7  
(2838727)  
(Moderada)  
Internet Explorer 8  
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2839229)  
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
(2838727)  
(Moderada)  
Internet Explorer 7  
(2838727)  
(Moderada)  
Internet Explorer 8  
(2838727)  
(Moderada)
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
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2838727)  
(Moderada)  
Internet Explorer 7  
(2838727)  
(Moderada)
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
<th colspan="5" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
Internet Explorer 7  
(2838727)  
(Crítica)  
Internet Explorer 8  
(2838727)  
(Crítica)  
Internet Explorer 9   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2839229)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2838727)  
(Crítica)  
Internet Explorer 8  
(2838727)  
(Crítica)  
Internet Explorer 9   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
Internet Explorer 7  
(2838727)  
(Moderada)  
Internet Explorer 8  
(2838727)  
(Moderada)  
Internet Explorer 9   
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2839229)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2838727)  
(Moderada)  
Internet Explorer 8  
(2838727)  
(Moderada)  
Internet Explorer 9   
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2839894)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2838727)  
(Crítica)  
Internet Explorer 9   
(2838727)  
(Crítica)  
Internet Explorer 10   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2839229)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2839894)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2838727)  
(Crítica)  
Internet Explorer 9   
(2838727)  
(Crítica)  
Internet Explorer 10   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2838727)  
(Moderada)  
Internet Explorer 9   
(2838727)  
(Moderada)  
Internet Explorer 10   
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2839894)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2839229)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2845690)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2839894)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2845690)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2838727)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2845690)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2838727)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT  
(2845690)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2839894)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS13-047**](http://go.microsoft.com/fwlink/?linkid=299498)
</td>
<td style="border:1px solid black;">
[**MS13-048**](http://go.microsoft.com/fwlink/?linkid=301748)
</td>
<td style="border:1px solid black;">
[**MS13-049**](http://go.microsoft.com/fwlink/?linkid=301749)
</td>
<td style="border:1px solid black;">
[**MS13-050**](http://go.microsoft.com/fwlink/?linkid=299243)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2839229)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2839894)  
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2839894)  
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2845690)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2839894)  
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
Windows Server 2012 (instalación Server Core)  
(2845690)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2839894)  
(Importante)
</td>
</tr>
</table>
 

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
[**MS13-051**](http://go.microsoft.com/fwlink/?linkid=296303)
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
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3  
(2817421)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
Microsoft Office para Mac 2011  
(2848689)  
(Importante)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

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

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet.microsoft.com/es-es/library/cc749197) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971).

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

**MS13-047**

-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad en la memoria de Internet Explorer (CVE-2013-3110)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3111)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3112)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3113)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3114)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3116)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3117)
-   [Omair](http://krash.in/)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3118)
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com) en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3119)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3120)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3121)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3122)
-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3123)
-   [Omair](http://krash.in/)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3124)
-   Amol Naik, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3124)
-   [Omair](http://krash.in/)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3125)
-   Amol Naik, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3125)
-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la depuración de scripts en Internet Explorer (CVE-2013-3126)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3141)
-   Toan Pham Van, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3142)

**MS13-048**

-   [Mateusz ru “j00" Jurczyk](http://j00ru.vexillium.org/)
-   de
-   [Google](http://www.google.com/)
-   por informar de la vulnerabilidad de divulgación de información del kernel (CVE-2013-3136)

**MS13-051**

-   Andrew Lyons y Neel Mehta de [Google Inc](http://www.google.com/), por informar de la vulnerabilidad de desbordamiento del búfer en Office (CVE-2013-1331)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (11 de junio de 2013): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
