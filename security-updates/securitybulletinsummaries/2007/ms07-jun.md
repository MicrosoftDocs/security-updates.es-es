---
TOCTitle: 'MS07-JUN'
Title: Resumen del boletín de seguridad de Microsoft de junio 2007
ms:assetid: 'ms07-jun'
ms:contentKeyID: 61225378
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms07-jun(v=Security.10)'
--- 

Summary

Resumen del boletín de seguridad de Microsoft de junio 2007
===========================================================

Publicado: martes, 12 de junio de 2007

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2007.

Con la publicación de los boletines de junio de 2007, este resumen de boletín reemplaza la notificación de avance de boletines publicada originalmente el 7 de junio de 2007. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para recibir notificaciones automáticas por correo electrónico siempre que se publiquen boletines de seguridad de Microsoft, suscríbase [Microsoft Technical Security Notifications](http://www.microsoft.com/spain/technet/seguridad/boletines/notificacion.mspx) (en inglés).

Microsoft realizará un webcast para atender las consultas de los clientes sobre estos boletines el miércoles 13 de junio de 2007, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032327013&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Crítica (4)
-----------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-031                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el paquete de seguridad de Windows Schannel podría permitir la ejecución remota de código (935840)**](http://technet.microsoft.com/security/bulletin/ms07-031)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en el paquete de seguridad de canal seguro (Schannel) en Windows. El paquete de seguridad Schannel implementa los protocolos de autenticación estándar SSL (capa de sockets seguros) y TLS (seguridad de la capa de transporte) de Internet. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante un explorador web de Internet o usa una aplicación que emplea SSL/TLS. Sin embargo, lo más probable es que los intentos para aprovechar esta vulnerabilidad tengan como consecuencia que se cierre el explorador web de Internet o la aplicación. El sistema no se podría conectar a sitios web ni a recursos mediante SSL o TLS hasta que se reiniciara el sistema. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Software afectado**                 | **Windows**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-033                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Actualización de seguridad acumulativa para Internet Explorer (933566)**](http://technet.microsoft.com/security/bulletin/ms07-033)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve cinco vulnerabilidades de las que se ha informado de forma privada y otra vulnerabilidad de la que se ha informado de forma pública. Todas estas vulnerabilidades menos una podrían permitir la ejecución remota de código si un usuario consulta una página web especialmente diseñada mediante Internet Explorer. Una vulnerabilidad podría permitir la suplantación e implica también una página web especialmente diseñada. En todos los casos de ejecución remota de código, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Para el caso de suplantación, es necesaria la interacción del usuario para aprovechar la vulnerabilidad. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Software afectado**                 | **Windows, Internet Explorer**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-034                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Actualización de seguridad acumulativa para Outlook Express y Windows Mail (929123)**](http://technet.microsoft.com/security/bulletin/ms07-034)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve dos vulnerabilidades de las que se ha informado de forma privada y dos vulnerabilidades de las que se ha informado de forma pública. Una de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario consulta un correo electrónico especialmente diseñado que use Windows Mail en Windows Vista. Las otras vulnerabilidades podrían permitir la divulgación de información si un usuario visita una página web especialmente diseñada mediante Internet Explorer y no se pueden aprovechar directamente en Outlook Express. En el caso de las vulnerabilidades de divulgación de información, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Detección**                         | Microsoft Baseline Security Analyzer y la herramienta Enterprise Scan Tool pueden detectar si el sistema necesita esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Software afectado**                 | **Windows, Outlook Express, Windows Mail**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-035                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en la API Win 32 podría permitir la ejecución remota de código (935839)**](http://technet.microsoft.com/security/bulletin/ms07-035)                                                                                                                                                                                                                                                                                                                                                                                              |
| **Resumen ejecutivo**                 | Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en una API Win32. Esta vulnerabilidad podría permitir la ejecución remota de código o la elevación de privilegios si una aplicación especialmente diseñada usa la API afectada de forma local. Por lo tanto las aplicaciones que usan este componente de la API Win32 se pueden usar para aprovechar esta vulnerabilidad. Por ejemplo, Internet Explorer usa esta función de API Win32 al analizar páginas web especialmente diseñadas. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                |
| **Software afectado**                 | **Windows**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                          |

Importante (1)
--------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-030                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Microsoft Visio podrían permitir la ejecución remota de código (927051)**](http://technet.microsoft.com/security/bulletin/ms07-030)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Resumen ejecutivo**                 | Esta importante actualización de seguridad resuelve dos vulnerabilidades detectadas de forma privada y de las que se ha informado de forma responsable, además de otros problemas de seguridad detectados durante la investigación. Las vulnerabilidades de las que se ha informado de forma privada podrían permitir la ejecución remota de código si un usuario abre un archivo de Visio especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Es necesaria la intervención del usuario para aprovechar estas vulnerabilidades. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Software afectado**                 | **Office, Visio**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

Moderada (1)
------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS07-032                                                                                                                                                                                                                                                                                                       |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Windows Vista podría permitir la divulgación de información (931213)**](http://technet.microsoft.com/security/bulletin/ms07-032)                                                                                                                                                                                        |
| **Resumen ejecutivo**                 | Esta actualización de seguridad moderada resuelve una vulnerabilidad de la que se ha informado de forma privada. Esta vulnerabilidad podría permitir que usuarios sin privilegios tuvieran acceso a almacenes de datos de información de usuario locales, incluidas las contraseñas administrativas del Registro y el sistema de archivos local. |
| **Gravedad máxima**                   | [Moderada](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                |
| **Consecuencia de la vulnerabilidad** | Divulgación de información                                                                                                                                                                                                                                                                                                                       |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                          |
| **Software afectado**                 | **Windows**. Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                    |

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
[**MS07-030**](http://technet.microsoft.com/security/bulletin/ms07-030)
</td>
<td style="border:1px solid black;">
[**MS07-031**](http://technet.microsoft.com/security/bulletin/ms07-031)
</td>
<td style="border:1px solid black;">
[**MS07-032**](http://technet.microsoft.com/security/bulletin/ms07-032)
</td>
<td style="border:1px solid black;">
[**MS07-033**](http://technet.microsoft.com/security/bulletin/ms07-033)
</td>
<td style="border:1px solid black;">
[**MS07-034**](http://technet.microsoft.com/security/bulletin/ms07-034)
</td>
<td style="border:1px solid black;">
[**MS07-035**](http://technet.microsoft.com/security/bulletin/ms07-035)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Software de Windows afectado
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=5b8e728c-cb9f-4176-93a0-bf42d6387f93)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=3918ac76-ebb6-4886-9a9e-808eafb96b1b)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=8615e6f3-415b-4c23-ba52-7eef70a11d77)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=27c7f1b9-2d1d-40cb-ad7e-bfedb6156a9c)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7e994340-c616-4f66-845b-7eaf095e968a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=0ba12191-1e6f-443b-9150-7ab8b2deb7c2)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7e994340-c616-4f66-845b-7eaf095e968a)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=0ba12191-1e6f-443b-9150-7ab8b2deb7c2)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=39e6c6d2-7e6f-4992-a731-36f44fe2d87f)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=d554dff4-bcfb-4bbc-8fa0-af2f939d2610)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=39e6c6d2-7e6f-4992-a731-36f44fe2d87f)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=d554dff4-bcfb-4bbc-8fa0-af2f939d2610)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=da424772-079c-4351-9759-8886e0f1ba79)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=170473d8-6bb1-4fbd-8494-a059dbfdf182)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=da424772-079c-4351-9759-8886e0f1ba79)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=170473d8-6bb1-4fbd-8494-a059dbfdf182)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=028592ff-2b69-472e-b186-bd2cc76bdfa4)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=f5e45e3c-4cac-41a5-99f7-42c2c2c73e99)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=028592ff-2b69-472e-b186-bd2cc76bdfa4)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=f5e45e3c-4cac-41a5-99f7-42c2c2c73e99)
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=cdf79d00-6f34-404b-8ad5-a2801ff35443)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=89dde3f4-4123-4c97-86d8-00a83462c34b)
</td>
<td style="border:1px solid black;">
**<sup>[1]</sup>**
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=3b49f1ed-abe3-4dbd-a91d-973415658f6b)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Internet Explorer 6 Service Pack 1 en Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=5c958650-28d2-4dd0-96a8-dbfe79ce3f68)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=60fb294e-a8e1-405e-a289-2d2723edf7ee)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=086d6d6e-4703-4c6c-a7af-b6dafeeede5d)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=7ed19127-5c2d-48e4-a8d1-090dc69fd68b)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=1449eb5d-6e4c-4332-8cb6-ab9ee59c9a95)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=b628a3cc-a70c-478a-a10c-eee254ee34ab)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=c2191703-8cbd-4959-9f84-e13f21173926)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=69c526b8-8b07-42bc-9bed-e18deae21c8e)
</td>
<td style="border:1px solid black;">
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=a074d9c0-1fed-4753-845e-073cfce99f45)
</td>
<td style="border:1px solid black;">
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=744acb43-64da-48cc-ae69-9386b597eabc)
</td>
<td style="border:1px solid black;">
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=069c1560-b5e5-4dfe-a18d-e0507d406028)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=77287386-48eb-4aa9-9537-626a3093aaf7)
</td>
<td style="border:1px solid black;">
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=77287386-48eb-4aa9-9537-626a3093aaf7)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Outlook Express 6 para Windows XP Service Pack 2
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
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=27cca556-0872-4803-b610-4c895ceb99aa)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Outlook Express 6 para Windows XP Professional x64 Edition
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
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=1ea813bf-bddb-40f0-8960-b9debc8413e7)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Outlook Express 6 para Windows XP Professional x64 Edition Service Pack 2
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
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=1ea813bf-bddb-40f0-8960-b9debc8413e7)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Outlook Express 6 en Windows Server 2003 Service Pack 1
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
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=93808a74-035c-4ab7-9283-c693d7bd82be)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Outlook Express 6 en Windows Server 2003 Service Pack 2
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
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=93808a74-035c-4ab7-9283-c693d7bd82be)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Outlook Express 6 para Windows Server 2003 x64 Edition
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=f63323a9-e285-45e5-84bd-71ae9da126e3)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Outlook Express 6 para Windows Server 2003 x64 Edition Service Pack 2
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
[Moderada](http://www.microsoft.com/downloads/details.aspx?familyid=f63323a9-e285-45e5-84bd-71ae9da126e3)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Outlook Express 6 para Windows Server 2003 con SP1 para sistemas con Itanium
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
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=2e62e96e-6571-437d-a612-99175ac39025)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Outlook Express 6 para Windows Server 2003 con SP2 para sistemas con Itanium
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
[Baja](http://www.microsoft.com/downloads/details.aspx?familyid=2e62e96e-6571-437d-a612-99175ac39025)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Mail en Windows Vista
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=ee57de19-44ea-48f2-ae28-e76fd2018633)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Mail en Windows Vista x64 Edition
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
[Crítica](http://www.microsoft.com/downloads/details.aspx?familyid=343db20f-7794-4423-b11d-885329fbdf78)
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Software de Office afectado
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Visio 2002 Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=fc1d0483-27e8-4541-b81d-4a47973bea30)
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
Visio 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Importante](http://www.microsoft.com/downloads/details.aspx?familyid=c47f432e-8538-42fd-92c9-7e0f1d643e8e)
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
</table>
 
**Notas**

**<sup>[1]</sup>** Hay una actualización de seguridad disponible para este sistema operativo. Para obtener información, consulte el software o el componente afectado en la tabla y el boletín de seguridad apropiado.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://www.microsoft.com/spain/seguridad/content/pc/protect.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “revisión de seguridad” podrá encontrarlas fácilmente. Finalmente, las actualizaciones de seguridad se pueden descargar del Catálogo de actualizaciones de Windows. Para obtener más información sobre el Catálogo de actualizaciones de Windows, consulte el [artículo 323166 de Microsoft Knowledge Base](http://support.microsoft.com/kb/323166).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS), Extended Security Update Inventory Tool y Enterprise Update Scan Tool (EST). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer y herramienta** **Enterprise** **Update Scan Tool**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx).

Cuando MBSA 1.2.1 no puede realizar la detección de una actualización de seguridad especifica, Microsoft publica una versión de la herramienta Enterprise Update Scan Tool (EST) para dicha actualización de seguridad específica. Para obtener más información acerca de EST, visite [Enterprise Update Scan Tool](http://support.microsoft.com/default.aspx?id=894193).

**Nota** Después del 9 de octubre de 2007, el archivo MSSecure.XML que usa MBSA 1.2.1 ya no se actualizará. Después de esa fecha, no se agregará ninguna actualización de seguridad nueva al archivo MSSecure.XML que usa MBSA 1.2.1 y no se publicará ninguna versión nueva de la herramienta Enterprise Scan Tool. Para obtener más información, visite [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx).

**Software Update Services**

Software Update Services (SUS) permite a los administradores implementar con rapidez y confiabilidad las actualizaciones críticas y de seguridad más recientes en servidores basados en Windows 2000 y Windows Server 2003, y en sistemas de escritorio donde se ejecute Windows 2000 Professional o Windows XP Professional.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Software Update Services, visite [Software Update Services](http://go.microsoft.com/fwlink/?linkid=21133).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. Para obtener más información acerca de cómo pueden utilizar SMS 2003 los administradores para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

Tenga en cuenta que esta herramienta **no** se distribuye mediante Software Update Services (SUS).

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU, WSUS y SUS

Para este mes:

-   Microsoft ha publicado siete actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update (MU) y Windows Server Update Services (WSUS).
-   Microsoft no ha publicado ninguna actualización **no relacionada con la seguridad** de alta prioridad para Windows en Windows Update (WU) y Software Update Services (SUS).

Tenga en cuenta que esta información **sólo** pertenece a actualizaciones **no relacionadas con la seguridad** de alta prioridad en Microsoft Update, Windows Update, Windows Server Update Services y Software Update Services publicadas el mismo día que el resumen del boletín de seguridad. **No** se proporcionará información sobre las actualizaciones **no relacionadas con la seguridad** publicadas en otros días.

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de revisiones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de las prácticas recomendadas de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “revisión de seguridad” (security patch) podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de la zona de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Un investigador anónimo, en colaboración con [iDefense VCP](http://idefense.com/), por informar de un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   Tom Cross, de [ISS](http://www.iss.net/), por colaborar con Microsoft en un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   Un investigador anónimo, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   Sam Thomas, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   Will Dorman, de [CERT/CC](http://www.cert.org/certcc.html), por informar de un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   cocoruder, de [Fortinet Security Research](http://www.fortinet.com/), por colaborar con Microsoft en un problema descrito en [MS07-033](http://technet.microsoft.com/security/bulletin/ms07-033).
-   Billy Rios, por informar de un problema descrito en [MS07-035](http://technet.microsoft.com/security/bulletin/ms07-035).
-   Thomas Lim, de [COSEINC](http://www.coseinc.com/), por informar de un problema descrito en [MS07-031](http://technet.microsoft.com/security/bulletin/ms07-031).
-   [SANS ISC](http://isc.sans.org/), por colaborar con nosotros en un problema descrito en [MS07-034](http://technet.microsoft.com/security/bulletin/ms07-034).
-   Yosuke Hasegawa, de [WebAppSec.JP](https://www.webappsec.jp/), por informar de un problema descrito en [MS07-034](http://technet.microsoft.com/security/bulletin/ms07-034).
-   Robbie Sohlman, por informar de un problema descrito en [MS07-032](http://technet.microsoft.com/security/bulletin/ms07-032).

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida del soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico de los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) en 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (12 de junio de 2007): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
