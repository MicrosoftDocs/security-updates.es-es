---
TOCTitle: 'MS08-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio 2008
ms:assetid: 'ms08-jul'
ms:contentKeyID: 61225389
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms08-jul(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de julio 2008
===========================================================

Publicado: martes, 8 de julio de 2008 | Actualizado: miércoles, 11 de febrero de 2009

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2008.

Con la publicación de los boletines de julio de 2008, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de julio de 2008. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 9 de julio de 2008, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de julio](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032374629&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Importante (4)
--------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-040                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Microsoft SQL Server podrían permitir la elevación de privilegios (941203)**](http://technet.microsoft.com/security/bulletin/ms08-040)                                                                                                                                                                                                                                                        |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada. La más grave de las vulnerabilidades podría permitir a un atacante ejecutar código y tomar el control completo de un sistema afectado. De esta forma, un atacante autenticado podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos administrativos. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Elevación de privilegios                                                                                                                                                                                                                                                                                                                                                                                             |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                              |
| **Software afectado**                 | **Microsoft Windows, Microsoft SQL Server.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                        |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-038                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el Explorador de Windows podría permitir la ejecución remota de código (950582)**](http://technet.microsoft.com/security/bulletin/ms08-038)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el Explorador de Windows podría permitir la ejecución remota de código cuando se abre y guarda un archivo de búsqueda especialmente diseñado. Si un usuario inicia sesión con derechos de usuario administrativos, un intruso que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-037                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en DNS podrían permitir la suplantación de identidad (spoofing) (953230)**](http://technet.microsoft.com/security/bulletin/ms08-037)                                                                                                                                                                                                                                                                                                  |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el Sistema de nombres de dominio de Windows (DNS) que podrían permitir la suplantación de identidad (spoofing). Estas vulnerabilidades existen tanto en el cliente DNS como en el servidor DNS y podrían permitir que un atacante remoto redirigiera el tráfico de red destinado a sistemas en Internet a los sistemas propios del atacante. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                       |
| **Consecuencia de la vulnerabilidad** | Suplantación                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                                                                                                    |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                   |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-039                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Outlook Web Access para Exchange Server podrían permitir la elevación de privilegios (953747)**](http://technet.microsoft.com/security/bulletin/ms08-039)                                                                                                                                                                                                                                                                       |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Outlook Web Access (OWA) para Microsoft Exchange Server. Un atacante que aprovechase esta vulnerabilidad podría obtener acceso a los datos de sesión de un cliente de OWA, lo que permitiría la elevación de privilegios. El atacante podría realizar cualquier acción que el usuario pudiera llevar a cabo en la sesión OWA del cliente. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                    |
| **Consecuencia de la vulnerabilidad** | Elevación de privilegios                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                |

Ubicaciones de descarga y software afectado
-------------------------------------------

**¿Cómo se usa esta tabla?**  

Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Windows 2000
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-040**](http://technet.microsoft.com/security/bulletin/ms08-040)
</td>
<td style="border:1px solid black;">
[**MS08-038**](http://technet.microsoft.com/security/bulletin/ms08-038)
</td>
<td style="border:1px solid black;">
[**MS08-037**](http://technet.microsoft.com/security/bulletin/ms08-037)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Gravedad máxima del boletín**
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=269c219c-9d6b-4b12-b621-c70cd07cdd22)  
(Importante)  
Actualización de servidor DNS:  
[Microsoft Windows 2000 Server Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=332aa92f-a1ad-42a0-87d0-485d2d41335b)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-040**](http://technet.microsoft.com/security/bulletin/ms08-040)
</td>
<td style="border:1px solid black;">
[**MS08-038**](http://technet.microsoft.com/security/bulletin/ms08-038)
</td>
<td style="border:1px solid black;">
[**MS08-037**](http://technet.microsoft.com/security/bulletin/ms08-037)
</td>
</tr>
<tr>
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ed989a33-7a9e-4423-93a8-b38907467cdf)  
(Importante)  
Ninguna actualización de servidor DNS aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a2b016fa-b108-4e8e-b41b-4ca89002907b)  
(Importante)  
Ninguna actualización de servidor DNS aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-040**](http://technet.microsoft.com/security/bulletin/ms08-040)
</td>
<td style="border:1px solid black;">
[**MS08-038**](http://technet.microsoft.com/security/bulletin/ms08-038)
</td>
<td style="border:1px solid black;">
[**MS08-037**](http://technet.microsoft.com/security/bulletin/ms08-037)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Gravedad máxima del boletín**
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2000 Desktop Engine (WMSDE)](http://www.microsoft.com/downloads/details.aspx?familyid=1c0ae18b-1f17-44b3-a337-b36e7de437a7)  
(KB948110)  
(Importante)  
[Windows Internal Database (WYukon) Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48f6aaa5-49fc-4a16-bc34-8514e214b8cf)  
(KB948109)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4ef5033c-9843-4e0b-bfad-fcaf05d7dab9)  
(Importante)  
Actualización de servidor DNS:  
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d1fcb794-e6a5-4c28-b3b3-9cd88f468a42)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2000 Desktop Engine (WMSDE)](http://www.microsoft.com/downloads/details.aspx?familyid=1c0ae18b-1f17-44b3-a337-b36e7de437a7)  
(KB948110)  
(Importante)  
[Windows Internal Database (WYukon) x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48f6aaa5-49fc-4a16-bc34-8514e214b8cf)  
(KB948109)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=66624a1f-38bf-4af7-936d-3131474ffe1f)  
(Importante)  
Actualización de servidor DNS:  
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=040a1ba8-21b0-439e-bf21-1acd1c43b162)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Actualización de cliente DNS:  
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=facc80da-61d6-49c5-872d-a1980b66ae3e)  
(Importante)  
Actualización de servidor DNS:  
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c63e3ee6-6055-4313-b0f1-fec7408886bb)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-040**](http://technet.microsoft.com/security/bulletin/ms08-040)
</td>
<td style="border:1px solid black;">
[**MS08-038**](http://technet.microsoft.com/security/bulletin/ms08-038)
</td>
<td style="border:1px solid black;">
[**MS08-037**](http://technet.microsoft.com/security/bulletin/ms08-037)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Gravedad máxima del boletín**
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=06739ca6-7368-4acb-bb67-7e8146071a29)  
(Importante)
</td>
<td style="border:1px solid black;">
Ninguna actualización de cliente DNS aplicable  
Ninguna actualización de servidor DNS aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=74ea0893-7c2f-4fad-ad27-588ad953b046)  
(Importante)
</td>
<td style="border:1px solid black;">
Ninguna actualización de cliente DNS aplicable  
Ninguna actualización de servidor DNS aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-040**](http://technet.microsoft.com/security/bulletin/ms08-040)
</td>
<td style="border:1px solid black;">
[**MS08-038**](http://technet.microsoft.com/security/bulletin/ms08-038)
</td>
<td style="border:1px solid black;">
[**MS08-037**](http://technet.microsoft.com/security/bulletin/ms08-037)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Gravedad máxima del boletín**
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows Internal Database (WYukon) Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48f6aaa5-49fc-4a16-bc34-8514e214b8cf)\*  
(KB948109)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=189a4170-b495-4904-9cbd-209e7494d303)\*  
(Importante)
</td>
<td style="border:1px solid black;">
Ninguna actualización de cliente DNS aplicable  
Actualización de servidor DNS:  
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=1fcea8f4-b233-42e1-b913-c4fcae276c7b)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Internal Database (WYukon) x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48f6aaa5-49fc-4a16-bc34-8514e214b8cf)\*  
(KB948109)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=85d8701d-f8c7-4079-8a21-a3a9d5ba71ce)\*  
(Importante)
</td>
<td style="border:1px solid black;">
Ninguna actualización de cliente DNS aplicable  
Actualización de servidor DNS:  
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=afac5bbc-71fa-457b-8b0a-f5902d37bfd0)\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=b30ee4f0-850f-4ff3-86a4-663603a0a802)  
(Importante)
</td>
<td style="border:1px solid black;">
Ninguna actualización de cliente DNS aplicable  
Ninguna actualización de servidor DNS aplicable
</td>
</tr>
</table>
 
**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft SQL Server</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-040"><strong>MS08-040</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SQL Server 7.0 Service Pack 4</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c95b2cb3-51a4-44e4-b9f4-9416e9ce16a0">SQL Server 7.0 Service Pack 4</a><br />
(KB948113)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c95b2cb3-51a4-44e4-b9f4-9416e9ce16a0">SQL Server 7.0 Service Pack 4</a><br />
(KB948113)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQL Server 2000 Service Pack 4</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4fd1f86a-94a2-43d8-9b0a-774c81426d9e">SQL Server 2000 Service Pack 4</a><br />
(KB948110)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=8316bc5e-8c2d-4710-8acc-b815ccc81cd4">SQL Server 2000 Service Pack 4</a><br />
(KB948111)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SQL Server 2000 Edition Service Pack 4 basado en Itanium</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4fd1f86a-94a2-43d8-9b0a-774c81426d9e">SQL Server 2000 Edition Service Pack 4 basado en Itanium</a><br />
(KB948110)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=8316bc5e-8c2d-4710-8acc-b815ccc81cd4">SQL Server 2000 Edition Service Pack 4 basado en Itanium</a><br />
(KB948111)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQL Server 2005 Service Pack 2</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4c9851cc-2c4c-4190-872c-84993a7623b7">SQL Server 2005 Service Pack 2</a><br />
(KB948109)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a60bb7e7-ef4e-4cbd-b63a-0ad7bd1402b3">SQL Server 2005 Service Pack 2</a><br />
(KB948108)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SQL Server 2005 x64 Edition Service Pack 2</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4c9851cc-2c4c-4190-872c-84993a7623b7">SQL Server 2005 x64 Edition Service Pack 2</a><br />
(KB948109)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a60bb7e7-ef4e-4cbd-b63a-0ad7bd1402b3">SQL Server 2005 x64 Edition Service Pack 2</a><br />
(KB948108)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQL Server 2005 con SP2 para sistemas con Itanium</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4c9851cc-2c4c-4190-872c-84993a7623b7">SQL Server 2005 con SP2 para sistemas con Itanium</a><br />
(KB948109)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a60bb7e7-ef4e-4cbd-b63a-0ad7bd1402b3">SQL Server 2005 con SP2 para sistemas con Itanium</a><br />
(KB948108)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Data Engine (MSDE) 1.0 Service Pack 4</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c95b2cb3-51a4-44e4-b9f4-9416e9ce16a0">Microsoft Data Engine (MSDE) 1.0 Service Pack 4</a><br />
(KB948113)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c95b2cb3-51a4-44e4-b9f4-9416e9ce16a0">Microsoft Data Engine (MSDE) 1.0 Service Pack 4</a><br />
(KB948113)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Service Pack 4</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4fd1f86a-94a2-43d8-9b0a-774c81426d9e">Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Service Pack 4</a><br />
(KB948110)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=8316bc5e-8c2d-4710-8acc-b815ccc81cd4">Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Service Pack 4</a><br />
(KB948111)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft SQL Server 2005 Express Edition Service Pack 2</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4c9851cc-2c4c-4190-872c-84993a7623b7">Microsoft SQL Server 2005 Express Edition Service Pack 2</a><br />
(KB948109)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a60bb7e7-ef4e-4cbd-b63a-0ad7bd1402b3">Microsoft SQL Server 2005 Express Edition Service Pack 2</a><br />
(KB948108)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 2</td>
<td style="border:1px solid black;">Actualización de RDA:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4c9851cc-2c4c-4190-872c-84993a7623b7">Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 2</a><br />
(KB948109)<br />
(Importante)<br />
<br />
Actualización de QFE:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a60bb7e7-ef4e-4cbd-b63a-0ad7bd1402b3">Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 2</a><br />
(KB948108)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Exchange Server</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-039"><strong>MS08-039</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Exchange Server 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e099c1d1-5af6-4d6c-b735-9599412b3131">Microsoft Exchange Server 2003 Service Pack 2</a><br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Exchange Server 2007</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=086a2a13-a1de-4b1d-bd12-b148bfd2dafa">Microsoft Exchange Server 2007</a><br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Exchange Server 2007 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=63e7f26c-92a8-4264-882d-f96b348c96ab">Microsoft Exchange Server 2007 Service Pack 1</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como “MS07-036”), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, consulte:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Cambios de contenido de Software Update Services y Windows Server Update Services para 2008. Incluye todo el contenido de Windows.
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

-   Dan Kaminsky, [IOActive](http://www.ioactive.com/), por informar de un problema descrito en MS08-037.
-   Michael Jordan, de [Context Information Security](http://www.contextis.co.uk/), por informar de dos problemas descritos en MS08-039.
-   Un investigador anónimo, por informar de un problema descrito en MS08-040.
-   Un investigador anónimo, por informar de un problema descrito en MS08-040.
-   Brett Moore, de [Insomnia Security](http://www.insomniasec.com/), en colaboración con [iDefense VCP](http://labs.idefense.com/), por informar de un problema descrito en MS08-040.
-   Un investigador anónimo, por informar de un problema descrito en MS08-040.

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de julio de 2008): Publicación del resumen del boletín.
-   V1.1 (11 de febrero de 2009): Se ha quitado la referencia errónea a Microsoft SQL Server 2000 Desktop Engine (WMSDE) en Microsoft Windows 2000 Service Pack 4 de la tabla Software afectado y Ubicaciones de descarga para el sistema operativo Windows, en MS08-040.

*Built at 2014-04-18T01:50:00Z-07:00*
