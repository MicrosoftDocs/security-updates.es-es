---
TOCTitle: 'MS07-AUG'
Title: Resumen del boletín de seguridad de Microsoft de agosto 2007
ms:assetid: 'ms07-aug'
ms:contentKeyID: 61225373
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms07-aug(v=Security.10)'
--- 

Summary

Resumen del boletín de seguridad de Microsoft de agosto 2007
============================================================

Publicado: martes, 14 de agosto de 2007 | Actualizado: martes, 24 de junio de 2008

**Versión:** 4.0

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2007.

Con la publicación de los boletines de agosto de 2007, este resumen de boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de agosto de 2007. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft realizará un webcast para atender las consultas de los clientes sobre estos boletines el 15 de agosto de 2007, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de agosto](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032344688&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Crítica (6)
-----------

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-042                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Microsoft XML Core Services podría permitir la ejecución remota de código (936227)**](http://technet.microsoft.com/security/bulletin/ms07-042)                                                                                                                                                                                                                                                                                                                                                                                          |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. La vulnerabilidad se podría aprovechar mediante ataques a Microsoft XML Core Services. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Software afectado**                 | **Windows, XML Core Services.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                 |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-043                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en la automatización OLE podría permitir la ejecución remota de código (921503)**](http://technet.microsoft.com/security/bulletin/ms07-043)                                                                                                                                                                                                                                                                                                                                                                                        |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada. La vulnerabilidad se podría aprovechar mediante ataques a la vinculación e incrustación de objetos (OLE). Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el equipo.                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Software afectado**                 | **Windows, Visual Basic, Office para Mac**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                             |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-044                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Microsoft Excel podría permitir la ejecución remota de código (940965)**](http://technet.microsoft.com/security/bulletin/ms07-044)                                                                                                                                                                                                                                                                                                                                                  |
| **Resumen ejecutivo**                 | Esta actualización resuelve una vulnerabilidad de la que se ha informado de forma privada, además de otros problemas de seguridad detectados durante la investigación. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                        |
| **Software afectado**                 | **Office**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                 |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-045                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Actualización de seguridad acumulativa para Internet Explorer (937143)**](http://technet.microsoft.com/security/bulletin/ms07-045)                                                                                                                                                                                                                                                                                                                                             |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve tres vulnerabilidades de las que se ha informado de forma privada. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                           |
| **Software afectado**                 | **Windows, Internet Explorer**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                  |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-046                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en GDI podría permitir la ejecución remota de código (938829)**](http://technet.microsoft.com/security/bulletin/ms07-046)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada. Existe una vulnerabilidad de ejecución remota de código en la forma en que el motor de representación de gráficos trata las imágenes especialmente diseñadas. Un atacante podría aprovechar esta vulnerabilidad mediante la creación de una imagen especialmente diseñada que podría permitir la ejecución remota de código si el usuario abre los datos adjuntos especialmente diseñados de un correo electrónico. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Software afectado**                 | **Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-050                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el lenguaje de marcado vectorial podría permitir la ejecución remota de código (938127)**](http://technet.microsoft.com/security/bulletin/ms07-050)                                                                                                                                                                                                                                                                                                                                                               |
| **Resumen ejecutivo**                 | Esta actualización de seguridad se resuelve una vulnerabilidad de la que se ha informado de forma privada en la implementación del lenguaje de marcado vectorial (VML) en Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Software afectado**                 | **Windows, Internet Explorer**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                           |

Importante (3)
--------------

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-047                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el Reproductor de Windows Media podría permitir la ejecución remota de código (936782)**](http://technet.microsoft.com/security/bulletin/ms07-047)                                                                                                                                                                                                                                                                                               |
| **Resumen ejecutivo**                 | Esta actualización de seguridad importante resuelve dos vulnerabilidades de las que se ha informado de forma privada. Estas vulnerabilidades podrían permitir la ejecución de código si un usuario ve un archivo especialmente diseñado en Reproductor de Windows Media. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                     |
| **Software afectado**                 | **Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                             |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-048                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en gadgets de Windows podrían permitir la ejecución remota de código (938123)**](http://technet.microsoft.com/security/bulletin/ms07-048)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Resumen ejecutivo**                 | Esta actualización de seguridad importante resuelve dos vulnerabilidades de las que se ha informado de forma privada, además de otras vulnerabilidades detectadas durante la investigación. Estas vulnerabilidades podrían permitir a un atacante remoto anónimo ejecutar código con los privilegios del usuario que ha iniciado la sesión. Si un usuario se ha suscrito a una fuente RSS malintencionada de RSS del gadget Encabezados de la fuente, ha agregado un archivo de contactos malintencionado en el gadget Contactos o ha hecho clic en un vínculo malintencionado del gadget El tiempo, un atacante podría ejecutar código en el sistema. En todos los casos de ataque, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Software afectado**                 | **Windows** **Vista.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-049                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Virtual PC y Virtual Server podría permitir la elevación de privilegios (937986)**](http://technet.microsoft.com/security/bulletin/ms07-049)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Resumen ejecutivo**                 | Esta actualización de seguridad importante resuelve una vulnerabilidad de la que se ha informado de forma privada. Se trata de una vulnerabilidad de elevación de privilegios. La vulnerabilidad en Microsoft Virtual PC y Microsoft Virtual Server podría permitir que un usuario del sistema operativo invitado ejecutara código en el host o en otros sistemas operativos invitados. Sólo los usuarios del sistema operativo invitado a los que se conceden permisos administrativos al sistema operativo invitado podrían aprovechar esta vulnerabilidad. Los usuarios del sistema operativo invitado a los que no se conceden permisos administrativos al sistema operativo invitado no podrían aprovechar esta vulnerabilidad. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Elevación de privilegios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Software afectado**                 | **Virtual PC, Virtual Server.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

Ubicaciones de descarga y software afectado
-------------------------------------------

**¿Cómo se usa esta tabla?**  

Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si un componente o programa aparece, se indica la consecuencia de la vulnerabilidad y también se proporciona un vínculo a la actualización de software disponible.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Ubicaciones de descarga y software afectado para MS07-042 a MS07-046

**Ubicaciones de descarga y software afectado**

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS07-042**](http://technet.microsoft.com/security/bulletin/ms07-042)
</td>
<td style="border:1px solid black;">
[**MS07-043**](http://technet.microsoft.com/security/bulletin/ms07-043)
</td>
<td style="border:1px solid black;">
[**MS07-044**](http://technet.microsoft.com/security/bulletin/ms07-044)
</td>
<td style="border:1px solid black;">
[**MS07-045**](http://technet.microsoft.com/security/bulletin/ms07-045)
</td>
<td style="border:1px solid black;">
[**MS07-046**](http://technet.microsoft.com/security/bulletin/ms07-046)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Gravedad máxima**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Software de Windows afectado
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=5c35b6e8-732a-4451-b5d4-23ed63e6e792)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=8fc8340b-c2b3-4559-835c-caa00cf086b9)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=6e8de050-8589-4831-ae19-075c93509485)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=dc29475d-c0bb-4d35-8dd6-4ca1cac32315)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=b85bb583-dc61-4d37-b458-208f5bb07ece)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=3c81730a-981a-4649-b2d9-45144230d512)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=b85bb583-dc61-4d37-b458-208f5bb07ece)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=15d4d4fa-9bab-4da5-978e-f89c78c8086a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=5374583d-de68-4d65-bca8-598d6b98b8b3)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=15d4d4fa-9bab-4da5-978e-f89c78c8086a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=6608d722-3ef8-4085-b771-7b17bb0ba06e)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=c3359f27-e03e-4a4f-b896-3bda39f69f7e)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=6608d722-3ef8-4085-b771-7b17bb0ba06e)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=fc04451a-0696-4a21-b2b6-f02d4e2c33bf)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=92822479-2060-4357-a340-ed096f180b2b)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=fc04451a-0696-4a21-b2b6-f02d4e2c33bf)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Componentes del sistema operativo Windows afectados
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 5.01 Service Pack 4 en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=fcf9440f-bb36-4ed1-9b6b-74a4f055650b)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 Service Pack 1 cuando está instalado en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=8db75461-4dca-43db-aa30-c7e67ce954ad)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=5d31d916-867f-4dbf-b8a4-c75ea83f4f51)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 para Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=b15b2442-d6da-41dd-a424-11c9893be595)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=f2f9fb69-0399-4df0-9f5b-8f42a130c581)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=d0bd886d-2c80-4dd7-82b7-1bd1f8d398cc)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=bf41033a-d6f0-451e-9b69-4cbe2bb3f804)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=7a2b4395-eaba-45ec-8d0c-932ebcc3d344)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 para Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=cd7ed4d5-7790-41db-8b68-cfd59105ca36)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=4f8daed8-9925-494d-b2f5-1e29f4040f6a)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=34669ca2-46b0-4fbf-8fbd-ad7a13920103)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=5bd7bcbd-528a-4a16-a39a-a5ff5f69a2e2)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 en Windows Vista
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=9ae27b2f-aca4-4758-8ce4-a98f1ff6ba70)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 en Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=53497e53-d10c-43af-ad56-9f07739a5284)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=245214ea-76f9-4755-8a14-a74232e20c1c)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=dea6a48f-fb00-43f3-a374-3220f9759c2d)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=b8862ca9-1203-4056-a257-29271838ac0d)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=12618ad0-aefd-4c9a-a769-4b14a7603d6e)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=61bf00a9-aeea-431a-86d3-526a4a373bb7)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=b0285dd7-bf66-4226-9948-26e8aae99046)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows Vista
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=c734d7de-5d87-4904-81c3-714db2cb8b0d)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 3.0 (KB936021) en Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=0a465d77-a737-4d26-82a1-570f9c788a8a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) en Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2008 para sistemas de x64
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0 (KB936181) cuando está instalado en Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=021e12f5-cb46-43df-a2b8-185639ba2807)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0  
(KB933579) cuando está instalado en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) cuando está instalado en Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) cuando está instalado en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) cuando está instalado en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) cuando está instalado en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) cuando está instalado en Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=70c92e77-9e5a-41b1-a9d2-64443913c976)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) en Windows Vista
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=14270529-3ae5-43bf-a471-722ab010d81e)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft XML Core Services 6.0 (KB933579) en Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=928da3d2-b0b9-447a-b37a-4350497fe563)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Software de Office afectado
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Excel 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=082b98f7-9556-4f1f-823a-c41ddf5a7c9a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Excel 2002 Service Pack 3
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=91308769-2577-4f9f-8209-06f2c8c8a86f)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Excel 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=b0130e9e-8845-4d79-aaa1-a21cc9388abe)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 2 con Microsoft XML Core Services 5.0 (KB936048)
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=a339cb7b-e08a-47f8-ac0b-df449191424a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Excel Viewer 2003
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=c4a87572-3128-44f7-8069-95535a78500a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Word Viewer 2003 con Microsoft XML Core Services 5.0 (KB936048)
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=a339cb7b-e08a-47f8-ac0b-df449191424a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/mac/downloads.aspx)
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/mac/downloads.aspx)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
2007 Office System con Microsoft XML Core Services 5.0 (KB936960)
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7a97478a-832c-4a6b-b074-0e18b1e4ed33)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Groove Server 2007 con Microsoft XML Core Services 5.0 (KB936056)
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=e875613b-2f32-4f28-a635-664a25c95c18)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server con Microsoft XML Core Services 5.0 (KB936056)
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=e875613b-2f32-4f28-a635-664a25c95c18)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Otro software de afectado
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Basic 6.0 Service Pack 6 (KB924053)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=e1646fb0-29d5-4a6e-a8d2-304c4d7735b7)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
</table>
 
**Notas**

**<sup>[1]</sup>** Hay una actualización de seguridad disponible para este sistema operativo. Para obtener información, consulte el software o el componente afectado en la tabla y el boletín de seguridad apropiado.

#### Ubicaciones de descarga y software afectado para MS07-047 a MS07-050

**Ubicaciones de descarga y software afectado**

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
<th style="border:1px solid black;" >
Detalles        
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS07-047**](http://technet.microsoft.com/security/bulletin/ms07-047)
</td>
<td style="border:1px solid black;">
[**MS07-048**](http://technet.microsoft.com/security/bulletin/ms07-048)
</td>
<td style="border:1px solid black;">
[**MS07-049**](http://technet.microsoft.com/security/bulletin/ms07-049)
</td>
<td style="border:1px solid black;">
[**MS07-050**](http://technet.microsoft.com/security/bulletin/ms07-050)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Gravedad máxima**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Software de Windows afectado
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=49a5bd84-da71-4529-b4d3-ac57dab59e01)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=24443f59-b908-480b-9b72-7094d4b5e128)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Componentes del sistema operativo Windows afectados
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 5.01 Service Pack 4 en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=31e63d6f-b6b7-41d7-8ae6-dd7fcf89d477)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 Service Pack 1 cuando está instalado en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7099d33a-0ef6-423f-824e-757482517612)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=4447d74f-09ea-4be0-9dae-c243ce657fb7)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 para Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=98ccd207-f4d0-4625-aeab-0ebf1643a5fd)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=463535aa-e04e-4a30-b3ab-8cd6d8cdd13c)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=9d4375d4-fb9b-4771-bd6f-e5d23eedbc6b)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 6 para Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=c7be313b-3405-42e1-9e4b-0cb6bf3d2cb1)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=9f5da816-194c-478e-8a96-9421a0c52c9f)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 para Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=1c3168a9-d959-4137-868a-ec70da737c21)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=59884e97-4912-4a9a-8a31-8182ea2d24db)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=42060e27-de14-4d0c-92a0-138cb57fe2b5)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 para Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=a536206e-9d1b-49a8-81a1-53d46f2de973)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Internet Explorer 7 en Windows Vista
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=2dd908a4-6152-4976-aaaa-01f5f37c9143)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 7 en Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=592435bc-1d43-4544-bd8a-4a2d829dc1a1)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 7.1 en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=9f46b1fc-ee7b-437f-9492-67d003711021)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Reproductor de Windows Media 9 cuando está instalado en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=bd4a6474-5fde-415e-840e-7d973cb71c95)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 9 en Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=bd4a6474-5fde-415e-840e-7d973cb71c95)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Reproductor de Windows Media 10 cuando está instalado en Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=48f5a9d3-b859-4cb6-a68e-abde76a14782)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 10 en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=949580be-cbb3-4271-8ca0-0ead7f2d8801)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Reproductor de Windows Media 10 en Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=8d9f1fdf-6d4c-44d4-9b5f-bdbe8ac28d7f)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 10 en Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=2c04c7f2-728e-43bd-8574-26e411fcd129)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Reproductor de Windows Media 11 cuando está instalado en Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=a690d042-1137-4aaf-bd0e-565ea04d1f2b)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 11 en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=bdc89f34-c1ff-46ab-b52d-c02d51c5c373)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Reproductor de Windows Media 11 en Windows Vista
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=80e5167c-4f75-4ce3-8b15-2f50958deec8)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Reproductor de Windows Media 11 en Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=bf30b714-d6e7-47ea-b79e-84c18370a661)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Otro software de afectado
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual PC 2004
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=cbdeaa50-7115-4673-97c4-10009f9c5c42)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual PC 2004 Service Pack 1
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=17ffe5a2-3551-4858-93b6-5e25af87d808)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 Standard Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=bc02ea6d-2884-4637-9894-3413a71329ee)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 Enterprise Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=da474b6f-9f0c-43f6-b432-050f7e76967d)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 R2 Standard Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=43fa1327-8e5e-4c92-901f-1ff2a0a087b4)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 R2 Enterprise Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=c2fc16c4-1fb0-4c09-b04a-684b40df8517)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual PC para Mac versión 6.1
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/mac/downloads.aspx)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual PC para Mac versión 7
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/mac/downloads.aspx)
</td>
<td style="border:1px solid black;">
</td>
</tr>
</table>
 
**Notas**

**<sup>[1]</sup>** Hay una actualización de seguridad disponible para este sistema operativo. Para obtener información, consulte el software o el componente afectado en la tabla y el boletín de seguridad apropiado.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://www.microsoft.com/spain/technet/security/default.mspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “revisión de seguridad” podrá encontrarlas fácilmente. Finalmente, las actualizaciones de seguridad se pueden descargar del Catálogo de actualizaciones de Windows. Para obtener más información sobre el Catálogo de actualizaciones de Windows, consulte el [artículo 323166 de Microsoft Knowledge Base](http://support.microsoft.com/kb/323166).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS), Extended Security Update Inventory Tool y Enterprise Update Scan Tool (EST). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer y herramienta** **Enterprise** **Update Scan Tool**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/security/tools/mbsa/default.mspx).

Cuando MBSA 1.2.1 no puede realizar la detección de una actualización de seguridad especifica, Microsoft publica una versión de la herramienta Enterprise Update Scan Tool (EST) para dicha actualización de seguridad específica. Para obtener más información acerca de EST, visite [Enterprise Update Scan Tool](http://support.microsoft.com/default.aspx?id=894193).

**Nota** Después del 9 de octubre de 2007, el archivo MSSecure.XML que usa MBSA 1.2.1 ya no se actualizará. Después de esa fecha, no se agregará ninguna actualización de seguridad nueva al archivo MSSecure.XML que usa MBSA 1.2.1 y no se publicará ninguna versión nueva de la herramienta Enterprise Scan Tool. Para obtener más información, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/security/tools/mbsa/default.mspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. Para obtener más información acerca de cómo pueden utilizar SMS 2003 los administradores para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para este mes:

-   Microsoft ha publicado dos actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update (MU) y Windows Server Update Services (WSUS).
-   Microsoft ha publicado dos actualizaciones **no relacionadas con la seguridad** de alta prioridad para Windows en Windows Update (WU).

Tenga en cuenta que esta información **sólo** se refiere a actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update, Windows Update y Windows Server Update Services publicadas el mismo día que el resumen del boletín de seguridad. **No** se proporcionará información sobre las actualizaciones **no relacionadas con la seguridad** publicadas en otros días.

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de revisiones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de las prácticas recomendadas de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “revisión de seguridad” (security patch) podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Un investigador anónimo, en colaboración con [VeriSign iDefense VCP](http://idefense.com/), por informar de un problema descrito en [MS07-042](http://technet.microsoft.com/security/bulletin/ms07-042).
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en [MS07-042](http://technet.microsoft.com/security/bulletin/ms07-042).
-   Un investigador anónimo, en colaboración con [VeriSign iDefense VCP](http://idefense.com/), por informar de un problema descrito en [MS07-043](http://technet.microsoft.com/security/bulletin/ms07-043).
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en [MS07-043](http://technet.microsoft.com/security/bulletin/ms07-043).
-   Dyon Balding, de [Secunia](http://secunia.com/), por informar de un problema descrito en [MS07-044](http://technet.microsoft.com/security/bulletin/ms07-044).
-   [NSFocus Security Team](http://www.nsfocus.com/) por informar de un problema descrito en [MS07-045](http://technet.microsoft.com/security/bulletin/ms07-045).
-   Brett Moore, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de un problema descrito en [MS07-045](http://technet.microsoft.com/security/bulletin/ms07-045).
-   [eEye Digital Security](http://www.eeye.com/), por informar de un problema descrito en [MS07-046](http://technet.microsoft.com/security/bulletin/ms07-046).
-   Piotr Bania, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayintiative.com/), por informar de un problema descrito en [MS07-047](http://technet.microsoft.com/security/bulletin/ms07-047).
-   Aviv Raff, de [Finjan](http://www.finjan.com/), por informar de un problema descrito en [MS07-048](http://technet.microsoft.com/security/bulletin/ms07-048).
-   Aviv Raff, en colaboración con [iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en [MS07-048](http://technet.microsoft.com/security/bulletin/ms07-048).
-   Rafal Wojtczuk, de [McAfee Avert Labs](http://www.avertlabs.com/), por colaborar con Microsoft en un problema descrito en [MS07-049](http://technet.microsoft.com/security/bulletin/ms07-049).
-   [eEye Digital Security](http://www.eeye.com/) por informar de un problema descrito en [MS07-050](http://technet.microsoft.com/security/bulletin/ms07-050).

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de agosto de 2007): Publicación del resumen del boletín.
-   V1.1 (29 de agosto de 2007): Actualización de la tabla Software afectado para cambiar Software de Office afectado para MS07-044 de “Office 2000”, “Office XP” y “Office 2003” a “Excel 2000”, “Excel 2002” y “Excel 2003”, respectivamente.
-   V2.0 (13 de noviembre de 2007): Actualización de la tabla Software afectado para incluir vínculos de descarga actualizados para MS07-049. Ya está disponible una actualización de seguridad revisada para instalarla para Microsoft Virtual PC 2004, Microsoft Virtual PC 2004 Service Pack 1, Microsoft Virtual Server 2005 Standard Edition, Microsoft Virtual Server 2005 Enterprise Edition, Microsoft Virtual Server 2005 R2 Standard Edition y Microsoft Virtual Server 2005 R2 Enterprise Edition.
-   V3.0 (9 de enero de 2008): Se ha actualizado la tabla de software afectado para agregar Microsoft Word Viewer 2003 en MS07-042. La misma actualización para Microsoft Office 2003 Service Pack 2 se aplica a Microsoft Word Viewer 2003.
-   V4.0 (24 de junio de 2008): Actualización de la tabla Software afectado para agregar Windows XP Service Pack 3, Windows Vista Service Pack 1, Windows Vista x64 Edition Service Pack 1, Windows Server 2008 para sistemas de 32 bits, Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas con Itanium en MS07-042 para la actualización KB936181 de Microsoft XML Core Services 4.0. Se trata únicamente de un cambio de detección. No había cambios en los archivos binarios.

*Built at 2014-04-18T01:50:00Z-07:00*
