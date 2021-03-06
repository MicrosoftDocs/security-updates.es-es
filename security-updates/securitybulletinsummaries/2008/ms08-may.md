---
TOCTitle: 'MS08-MAY'
Title: Resumen del boletín de seguridad de Microsoft de mayo 2008
ms:assetid: 'ms08-may'
ms:contentKeyID: 61225392
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms08-may(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de mayo 2008
==========================================================

Publicado: martes, 13 de mayo de 2008

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para mayo de 2008.

Con la publicación de los boletines de mayo de 2008, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 8 de mayo de 2008. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 14 de mayo de 2008, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de mayo](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032357221&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Crítica (3)
-----------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-026                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Microsoft Word podrían permitir la ejecución remota de código (951207)**](http://technet.microsoft.com/security/bulletin/ms08-026)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Word que podrían permitir la ejecución remota de código si un usuario abre un archivo de Word especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Nivel de gravedad máxima**          | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Software afectado**                 | **Microsoft Office.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-027                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Microsoft Publisher podría permitir la ejecución remota de código (951208)**](http://technet.microsoft.com/security/bulletin/ms08-027)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Publisher que podría permitir la ejecución remota de código si un usuario abre un archivo de Publisher especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Nivel de gravedad máxima**          | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Software afectado**                 | **Microsoft Office.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-028                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el motor de base de datos Microsoft Jet (Jet) podría permitir la ejecución remota de código (950749)**](http://technet.microsoft.com/security/bulletin/ms08-028)                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de seguridad en el motor de base de datos Microsoft Jet (Jet) en Windows. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario**.** Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Nivel de gravedad máxima**          | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

Moderada (1)
------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-029                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en el motor de protección contra malware de Microsoft podrían permitir la denegación de servicio (952044)**](http://technet.microsoft.com/security/bulletin/ms08-029)                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el motor de protección contra malware de Microsoft. Un atacante podría aprovechar cualquiera de las vulnerabilidades con la creación de un archivo especialmente diseñado que podría permitir la denegación de servicio cuando se recibiera en el equipo de destino y se analizara con el motor de protección contra malware de Microsoft. Un atacante que aprovechara cualquier vulnerabilidad podría provocar que el motor de protección contra malware de Microsoft dejara de responder y se reiniciara automáticamente. |
| **Nivel de gravedad máxima**          | [Moderada](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Consecuencia de la vulnerabilidad** | Denegación de servicio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Detección**                         | El software afectado ofrece mecanismos integrados para la detección y la implementación automáticas de actualizaciones. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Software afectado**                 | **Windows Live OneCare, Microsoft Antigen, Microsoft Windows Defender, Microsoft Forefront Security.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                  |

Ubicaciones de descarga y software afectado
-------------------------------------------

**¿Cómo se usa esta tabla?**  

Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Servidores y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Windows 2000</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-028"><strong>MS08-028</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Windows 2000 Service Pack 4</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0de12d09-e675-4cf0-bc6f-e42eeb4784a1">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows XP</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-028"><strong>MS08-028</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows XP Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3247433f-0aa9-49b8-9e40-c5463a95bcff">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows XP Professional x64 Edition</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4915ebc4-5e7b-493e-b8c4-321d40d9a701">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows Server 2003</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-028"><strong>MS08-028</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=86e3ed62-98f7-46ec-96ab-5e8c123b1288">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2003 x64 Edition</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5dfc867b-74b7-4818-9fc2-d71e7c9d2e38">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 con SP1 para sistemas con Itanium</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3452119b-ba4c-4272-82ec-97396b2c2c3d">Motor de base de datos Microsoft Jet 4.0</a><br />
(Crítica)</td>
</tr>
</tbody>
</table>
 

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<caption>Conjuntos de programas, sistemas y componentes de Microsoft Office</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-026"><strong>MS08-026</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-027"><strong>MS08-027</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office 2000 Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=9215ff71-38c0-416a-b89a-fe3474160f41">Microsoft Word 2000 Service Pack 3</a><br />
(KB950250)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8675b9b6-fbf0-4ad2-9210-285e2cc10556">Microsoft Publisher 2000 Service Pack 3</a><br />
(KB950682)<br />
(Crítica)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office XP Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b348a518-221e-4567-a797-999715a8b2ef">Microsoft Word 2002 Service Pack 3</a><br />
(KB950243)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=df623784-6e26-42c0-9e21-e7960b849e1e">Microsoft Publisher 2002 Service Pack 3</a><br />
(KB950129)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bc33d144-f917-47b8-961f-744ca847e14c">Microsoft Word 2003 Service Pack 2</a><br />
(KB950241)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=c18b060b-9828-4952-8e80-5328c0832d83">Microsoft Publisher 2003 Service Pack 2</a><br />
(KB950213)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office 2003 Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bc33d144-f917-47b8-961f-744ca847e14c">Microsoft Word 2003 Service Pack 3</a><br />
(KB950241)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=c18b060b-9828-4952-8e80-5328c0832d83">Microsoft Publisher 2003 Service Pack 3</a><br />
(KB950213)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">2007 Microsoft Office System</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=071ceaa2-12e3-4401-9331-2a54a93e2550">Microsoft Word 2007</a><br />
(KB950113)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e4b647c2-79a3-49e0-9b1d-741667fdbcca">Microsoft Publisher 2007</a><br />
(KB950114)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=071ceaa2-12e3-4401-9331-2a54a93e2550">Microsoft Outlook 2007</a><br />
(KB950113)<br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">2007 Microsoft Office System Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=071ceaa2-12e3-4401-9331-2a54a93e2550">Microsoft Word 2007 Service Pack 1</a><br />
(KB950113)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e4b647c2-79a3-49e0-9b1d-741667fdbcca">Microsoft Publisher 2007 Service Pack 1</a><br />
(KB950114)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=071ceaa2-12e3-4401-9331-2a54a93e2550">Microsoft Outlook 2007 Service Pack 1</a><br />
(KB950113)<br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
</tbody>
</table>

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Office para Mac</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-026"><strong>MS08-026</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office 2004 para Mac</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=99f54471-ccf9-4d94-a882-a05ecd128adc">Microsoft Office 2004 para Mac</a><br />
(KB952332)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office 2008 para Mac</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=395d1487-a3a6-4106-a0f8-4d6e1d6d89d2">Microsoft Office 2008 para Mac</a><br />
(KB952331)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Otro software de Microsoft Office</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-026"><strong>MS08-026</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Word Viewer</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bce7ea31-2bf0-4930-aff9-837bcc82a682">Microsoft Word Viewer 2003</a><br />
(KB950625)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=bce7ea31-2bf0-4930-aff9-837bcc82a682">Microsoft Word Viewer 2003 Service Pack 3</a><br />
(KB950625)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Paquete de compatibilidad de Microsoft Office</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=2d718f37-c5d1-4e15-a7e1-5a15fedef52f">Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007</a><br />
(KB951808)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=2d718f37-c5d1-4e15-a7e1-5a15fedef52f">Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1</a><br />
(KB951808)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

#### Otro software de Microsoft

**Nota** Las siguientes entradas no tienen asociados vínculos de descarga porque el software identificado ofrece mecanismos integrados para la detección y la implementación automáticas de actualizaciones.

 
<p> </p>
<table style="border:1px solid black;">
<caption>Antimalware de Microsoft</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-029"><strong>MS08-029</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nivel de gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Moderada</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Live OneCare</td>
<td style="border:1px solid black;">Windows Live OneCare<br />
(Moderada)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Antigen</td>
<td style="border:1px solid black;">Microsoft Antigen para Exchange<br />
(Moderada)<br />
<br />
Microsoft Antigen para puerta de enlace SMTP<br />
(Moderada)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Windows Defender</td>
<td style="border:1px solid black;">Microsoft Windows Defender<br />
(Moderada)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Forefront Security</td>
<td style="border:1px solid black;">Microsoft Forefront Client Security<br />
(Moderada)<br />
<br />
Microsoft Forefront Security para Exchange Server<br />
(Moderada)<br />
<br />
Microsoft Forefront Security para SharePoint<br />
(Moderada)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sistema independiente de limpieza (malware)</td>
<td style="border:1px solid black;">Sistema independiente de limpieza (malware) que se encuentra en Diagnostics and Recovery Toolset 6.0<br />
(Baja)</td>
</tr>
</tbody>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://www.microsoft.com/spain/technet/security/default.mspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como “MS07-036”), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/security/tools/mbsa/default.mspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, consulte:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199): Cambios de contenido de Software Update Services y Windows Server Update Services para 2008. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/bb466214.aspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Jun Mao, en colaboración con [iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS08-026.
-   Wushi de [team509](http://www.team509.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-026
-   Cocoruder, de [Fortinet Security Research](http://www.fortinet.com/), por informar de un problema descrito en MS08-027
-   [CERT/CC](http://www.cert.org/) por informar de un problema descrito en MS08-028
-   [ISC/SANS](http://isc.sans.org/) por informar de un problema descrito en MS08-028
-   Aaron Portnoy, de [TippingPoint DVLabs](http://dvlabs.tippingpoint.com/), por informar de un problema descrito en MS08-028
-   SoWhat, de [Nevis Labs](http://www.nevisnetworks.com), por informar de dos problemas descritos en MS08-029

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (13 de mayo de 2008): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
