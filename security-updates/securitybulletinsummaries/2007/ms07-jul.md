---
TOCTitle: 'MS07-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio 2007
ms:assetid: 'ms07-jul'
ms:contentKeyID: 61225377
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms07-jul(v=Security.10)'
--- 

Summary

Resumen del boletín de seguridad de Microsoft de julio 2007
===========================================================

Publicado: martes, 10 de julio de 2007 | Actualizado: martes, 25 de marzo de 2008

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2007.

Con la publicación de los boletines de julio de 2007, este resumen de boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de julio de 2007. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft realizará un webcast para atender las consultas de los clientes sobre estos boletines el 11 de julio de 2007, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de julio](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032343783&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Crítica (3)
-----------

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-036                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Microsoft Excel podrían permitir la ejecución remota de código (936542)**](http://technet.microsoft.com/security/bulletin/ms07-036)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Resumen ejecutivo**                 | Esta actualización crítica resuelve una vulnerabilidad de la que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada además de otros problemas de seguridad detectados durante la investigación. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Software afectado**                 | **Office, Excel**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-039                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Windows Active Directory podría permitir la ejecución remota de código (926122)**](http://technet.microsoft.com/security/bulletin/ms07-039)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en implementaciones de Active Directory en Windows 2000 Servidor y Windows Server 2003 que podría permitir la ejecución remota de código o una condición de denegación de servicio. Lo más probable es que los intentos de aprovechar esta vulnerabilidad tengan como consecuencia la denegación de servicio. Sin embargo, podría darse la ejecución remota de código. En Windows Server 2003 un atacante debe tener credenciales de inicio de sesión válidas para aprovechar esta vulnerabilidad. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Software afectado**                 | **Windows**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-040                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en .NET Framework podrían permitir la ejecución remota de código (931212)**](http://technet.microsoft.com/security/bulletin/ms07-040)                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Resumen ejecutivo**                 | Esta actualización resuelve tres vulnerabilidades de las que se ha informado de forma privada. Dos de estas vulnerabilidades podrían permitir la ejecución remota de código en sistemas cliente con .NET Framework instalado y una podría permitir la divulgación de información en servidores web que ejecutan ASP.NET. En todos los casos de ejecución remota de código, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que los usuarios que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Software afectado**                 | **.NET Framework**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

Importante (2)
--------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-037                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Microsoft Office Publisher podría permitir la ejecución remota de código (936548)**](http://technet.microsoft.com/security/bulletin/ms07-037)                                                                                                                                                                                                                                                                                                                                                                                      |
| **Resumen ejecutivo**                 | Esta actualización de seguridad importante resuelve una vulnerabilidad de la que se ha informado de forma pública. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario consulta un archivo de Microsoft Office Publisher especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. La intervención del usuario es necesaria para aprovechar esta vulnerabilidad. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Software afectado**                 | **Office, Publisher**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-041                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Servicios de Microsoft Internet Information Server podría permitir la ejecución remota de código (939373)**](http://technet.microsoft.com/security/bulletin/ms07-041)                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Resumen ejecutivo**                 | Esta actualización de seguridad importante resuelve una vulnerabilidad de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir la ejecución remota de código si un atacante envía solicitudes de dirección URL especialmente diseñadas a una página web alojada por Servicios de Internet Information Server (IIS) 5.1 en Windows XP Professional Service Pack 2. IIS 5.1 no forma parte de una instalación predeterminada de Windows XP Professional Service Pack 2. Un atacante que aprovechara con éxito esta vulnerabilidad podría obtener el control completo del sistema afectado. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Software afectado**                 | **Windows XP Professional**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

Moderada (1)
------------

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-038                                                                                                                                                                                                                                                                 |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Firewall de Windows Vista podría permitir la divulgación de información (935807)**](http://technet.microsoft.com/security/bulletin/ms07-038)                                                                                                                                      |
| **Resumen ejecutivo**                 | Esta actualización de seguridad moderada resuelve una vulnerabilidad de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir que el tráfico de red no solicitado entrante tuviera acceso a una interfaz de red. Un atacante podría recopilar información acerca del host afectado. |
| **Gravedad máxima**                   | [Moderada](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                          |
| **Consecuencia de la vulnerabilidad** | Divulgación de información                                                                                                                                                                                                                                                                                 |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                    |
| **Software afectado**                 | **Windows Vista**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                        |

Ubicaciones de descarga y software afectado
-------------------------------------------

**¿Cómo se usa esta tabla?**  

Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si un componente o programa aparece, se indica la consecuencia de la vulnerabilidad y también se proporciona un vínculo a la actualización de software disponible.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

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
<th style="border:1px solid black;" >
Detalles        
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS07-036**](http://technet.microsoft.com/security/bulletin/ms07-036)
</td>
<td style="border:1px solid black;">
[**MS07-037**](http://technet.microsoft.com/security/bulletin/ms07-037)
</td>
<td style="border:1px solid black;">
[**MS07-038**](http://technet.microsoft.com/security/bulletin/ms07-038)
</td>
<td style="border:1px solid black;">
[**MS07-039**](http://technet.microsoft.com/security/bulletin/ms07-039)
</td>
<td style="border:1px solid black;">
[**MS07-040**](http://technet.microsoft.com/security/bulletin/ms07-040)
</td>
<td style="border:1px solid black;">
[**MS07-041**](http://technet.microsoft.com/security/bulletin/ms07-041)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Software de Windows afectado
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 2000 Server Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=812e62c5-6e19-4b3b-8a10-861b871e1b41)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=fccbfe90-f838-47df-8310-352e2fb47132)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=28e84603-8159-4429-aaff-a1020531e84f)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=28e84603-8159-4429-aaff-a1020531e84f)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=107902f9-be94-457f-a936-519efbd64779)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=107902f9-be94-457f-a936-519efbd64779)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
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
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=e5e5b425-fe7d-49d5-973f-f3fd7a1e04eb)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
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
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=e5e5b425-fe7d-49d5-973f-f3fd7a1e04eb)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=e9b64746-6afa-4a30-833d-e058e000c821)
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
Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=0df5d190-3ad7-42d5-8629-43c47ec450cb)
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
Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 x64 Edition
</td>
<td style="border:1px solid black;">
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
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Componentes del sistema operativo Windows afectados
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft .NET Framework 1.0  
(KB928367)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=91d7afe4-069b-4ce8-976e-9a01345a8603)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.0  
(KB930494)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=829a2c5b-11ec-4ed7-91ab-6961034147bc)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1  
(KB928366)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=281fb2cd-c715-4f05-a01f-0455d2d9ebfb)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1  
(KB933854)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=2495e656-1e0a-4b83-90da-821e68067a71)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1  
(KB929729)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7eea368d-7b82-4583-8537-30351718a4e9)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0  
(KB928365)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=ba3ceb78-8e1b-4c38-adfd-e8bc95ae548d)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0  
(KB929916)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=cbc9f3cf-c3c3-45c4-82e3-e11398bc2cd2)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Software de Office afectado
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Excel 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=83d94d8e-dda6-4d74-b40d-476c2f0a3af4)
</td>
<td style="border:1px solid black;">
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
Excel 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=9d93c0ce-5124-4234-ba84-3c27005e010f)
</td>
<td style="border:1px solid black;">
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
Excel 2003 Viewer
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=11f42977-8828-494a-a183-d1aba827b708)
</td>
<td style="border:1px solid black;">
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
Excel 2007
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=9ab28283-0320-4527-b033-5e80ef32cd34)
</td>
<td style="border:1px solid black;">
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
Paquete de compatibilidad de Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=e592ae5b-09ac-4f5b-b457-a54c9850ad4a)
</td>
<td style="border:1px solid black;">
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
Publisher 2007
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=25d272e7-f2dd-4342-92be-7ebc2e770b44)
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

**Microsoft Baseline Security Analyzer y herramienta Enterprise Update Scan Tool**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx).

Cuando MBSA 1.2.1 no puede realizar la detección de una actualización de seguridad especifica, Microsoft publica una versión de la herramienta Enterprise Update Scan Tool (EST) para dicha actualización de seguridad específica. Para obtener más información acerca de EST, visite [Enterprise Update Scan Tool](http://support.microsoft.com/default.aspx?id=894193).

**Nota** Después del 9 de octubre de 2007, el archivo MSSecure.XML que usa MBSA 1.2.1 ya no se actualizará. Después de esa fecha, no se agregará ninguna actualización de seguridad nueva al archivo MSSecure.XML que usa MBSA 1.2.1 y no se publicará ninguna versión nueva de la herramienta Enterprise Scan Tool. Para obtener más información, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx).

**Software Update Services**

Software Update Services (SUS) permite a los administradores implementar con rapidez y confiabilidad las actualizaciones críticas y de seguridad más recientes en servidores basados en Windows 2000 y Windows Server 2003, y en sistemas de escritorio donde se ejecute Windows 2000 Professional o Windows XP Professional.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Software Update Services, visite [Software Update Services](http://go.microsoft.com/fwlink/?linkid=21133).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. Para obtener más información acerca de cómo pueden utilizar SMS 2003 los administradores para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

Tenga en cuenta que esta herramienta **no** se distribuye mediante Software Update Services (SUS).

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU, WSUS y SUS

Para este mes:

-   Microsoft ha publicado dos actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update (MU) y Windows Server Update Services (WSUS).
-   Microsoft ha publicado una actualización **no relacionada con la seguridad** de alta prioridad para Windows en Windows Update (WU) y Software Update Services (SUS).

Tenga en cuenta que esta información **sólo** pertenece a actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update, Windows Update, Windows Server Update Services y Software Update Services publicadas el mismo día que el resumen del boletín de seguridad. **No** se proporcionará información sobre las actualizaciones **no relacionadas con la seguridad** publicadas en otros días.

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

-   Dinis Cruz, de [OWASP](http://www.owasp.org/), por informar de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   Paul Craig, de [Security Assessment](http://www.smsiinc.com/), por informar de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   Jeroen Frijters, de [Sumatra](http://www.sumatra.nl/), por informar de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   [ProCheckUp](http://www.procheckup.com/), en colaboración con [UK CPNI](http://www.cpni.gov.uk/), por informar originalmente de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   Ferruh T. Mavituna, de [Portcullis Computer Security Ltd.](http://www.portcullis-security.com/), por colaborar con Microsoft y proporcionar información adicional acerca de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   Johannes Gumbel, de [TrueSec](http://www.truesec.com/), por colaborar con Microsoft y proporcionar información adicional acerca de un problema descrito en [MS07-040](http://technet.microsoft.com/security/bulletin/ms07-040).
-   Peter Winter-Smith, de [NGSSoftware](http://www.nextgenss.com/), por informar de un problema descrito en [MS07-039](http://technet.microsoft.com/security/bulletin/ms07-039).
-   Neel Mehta, de [IBM Internet Security Systems x-Force](http://xforce.iss.net/), por informar de un problema descrito en [MS07-039](http://technet.microsoft.com/security/bulletin/ms07-039).
-   [eEye](http://www.eeye.com/), por informar de un problema descrito en [MS07-037](http://technet.microsoft.com/security/bulletin/ms07-037).
-   Jim Hoagland y Ollie Whitehouse, de [Symantec](http://www.symantec.com/), por informar de un problema descrito en [MS07-038](http://technet.microsoft.com/security/bulletin/ms07-038).
-   Jonathan Afek y Adi Sharabani, de [Watchfire](http://www.watchfire.com/), por colaborar con Microsoft y proporcionar información adicional sobre un problema descrito en [MS07-041.](http://technet.microsoft.com/security/bulletin/ms07-041)
-   Peter Winter-Smith, de [NGSSoftware](http://www.nextgenss.com/), por colaborar con Microsoft y proporcionar información adicional acerca de un problema descrito en [MS07-041](http://technet.microsoft.com/security/bulletin/ms07-041).

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (10 de julio de 2007): Publicación del resumen del boletín.
-   V2.0 (25 de marzo de 2008): Se han agregado Windows Vista Service Pack 1, Windows Vista x64 Edition Service Pack 1, Windows Server 2008, Windows Server 2008 para sistemas con Itanium y Windows Server 2008 x64 Edition a la tabla Software afectado.

*Built at 2014-04-18T01:50:00Z-07:00*
