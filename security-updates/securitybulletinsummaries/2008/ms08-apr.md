---
TOCTitle: 'MS08-APR'
Title: Resumen del boletín de seguridad de Microsoft de abril 2008
ms:assetid: 'ms08-apr'
ms:contentKeyID: 61225384
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms08-apr(v=Security.10)'
--- 

Summary

Resumen del boletín de seguridad de Microsoft de abril 2008
===========================================================

Publicado: martes, 8 de abril de 2008 | Actualizado: miércoles, 18 de febrero de 2009

**Versión:** 1.3

Este resumen del boletín enumera los boletines de seguridad publicados para abril de 2008.

Con la publicación de los boletines de abril de 2008, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de abril de 2008. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 9 de abril de 2008, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de abril](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032357219&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

Los boletines de seguridad de este mes son los siguientes, en orden de gravedad:

Crítica (5)
-----------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-018                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en Microsoft Project podría permitir la ejecución remota de código (950183)**](http://technet.microsoft.com/security/bulletin/ms08-018)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Project que podría permitir la ejecución remota de código si un usuario abre un archivo de Project especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Software afectado**                 | **Microsoft Office.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-021                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en GDI podría permitir la ejecución remota de código (948590)**](http://technet.microsoft.com/security/bulletin/ms08-021)                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en GDI. Si se aprovechan estas vulnerabilidades, se podría permitir la ejecución remota de código si un usuario abre un archivo de imagen EMF o WMF especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                                                                                                                                                                                          |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                         |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-022                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en los motores de secuencias de comandos de VBScript y JScript podría permitir la ejecución remota de código (944338)**](http://technet.microsoft.com/security/bulletin/ms08-022)                                                                                                                                                                                                                                   |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los motores de secuencias de comandos de VBScript y JScript en Windows. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                          |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                                                                                    |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                   |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-023                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Actualización de seguridad de bits de interrupción de ActiveX (948881)**](http://technet.microsoft.com/security/bulletin/ms08-023)                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada para un producto de Microsoft. Esta actualización también incluye un bit de interrupción para el producto Yahoo! Music Jukebox. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización podría requerir el reinicio del equipo.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Software afectado**                 | **Microsoft Windows, Internet Explorer.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-024                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Actualización de seguridad acumulativa para Internet Explorer (947864)**](http://technet.microsoft.com/security/bulletin/ms08-024)                                                                                                                                                                                                                                                                                                                           |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Crítica](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                                                                                                          |
| **Software afectado**                 | **Microsoft Windows, Internet Explorer.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                      |

Importante (3)
--------------


| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-020                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el cliente DNS podría permitir la suplantación (945553)**](http://technet.microsoft.com/security/bulletin/ms08-020)                                                                                                                                                                                                                            |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada. Existe una vulnerabilidad de suplantación en los clientes DNS de Windows y podría permitir a un atacante enviar respuestas especialmente diseñadas a solicitudes DNS, por lo que se suplanta o redirecciona el tráfico de Internet desde ubicaciones legítimas. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                     |
| **Consecuencia de la vulnerabilidad** | Suplantación                                                                                                                                                                                                                                                                                                                                                            |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                                  |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                 |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-025                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Una vulnerabilidad en el kernel de Windows podría permitir la elevación de privilegios (941693)**](http://technet.microsoft.com/security/bulletin/ms08-025)                                                                                                                                                                                               |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve una vulnerabilidad en el kernel de Windows de la que se ha informado de forma privada. Un atacante local que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                          |
| **Consecuencia de la vulnerabilidad** | Elevación de privilegios                                                                                                                                                                                                                                                                                                                                     |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. Esta actualización requiere que se reinicie el sistema.                                                                                                                                                                                                       |
| **Software afectado**                 | **Microsoft Windows.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                      |

| Identificador del boletín             | Boletín de seguridad de Microsoft MS08-019                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título del boletín**                | [**Vulnerabilidades en Microsoft Visio podrían permitir la ejecución remota de código (949032)**](http://technet.microsoft.com/security/bulletin/ms08-019)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Resumen ejecutivo**                 | Esta actualización de seguridad resuelve vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Visio que podrían permitir la ejecución remota de código si un usuario abre un archivo de Visio especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. |
| **Gravedad máxima**                   | [Importante](http://technet.microsoft.com/security/bulletin/rating)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Consecuencia de la vulnerabilidad** | Ejecución remota de código                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Detección**                         | Microsoft Baseline Security Analyzer puede detectar si su sistema requiere esta actualización. La actualización no requiere reinicio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Software afectado**                 | **Microsoft Office.** Para obtener más información, consulte la sección Ubicaciones de descarga y programas afectados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

Ubicaciones de descarga y software afectado
-------------------------------------------

**¿Cómo se usa esta tabla?**  

Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Windows 2000</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-021"><strong>MS08-021</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-022"><strong>MS08-022</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-023"><strong>MS08-023</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-024"><strong>MS08-024</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-020"><strong>MS08-020</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-025"><strong>MS08-025</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Windows 2000 Service Pack 4</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=caac000a-22b6-48cb-aa00-1a0bfe886de2">Microsoft Windows 2000 Service Pack 4</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8e3ff44f-145b-4a68-9ad4-4a55d74b216e">VBScript 5.1 y JScript 5.1</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=8e3ff44f-145b-4a68-9ad4-4a55d74b216e">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0395451f-b719-4f71-a7b4-403d0c7e8fcc">Microsoft Internet Explorer 5.01 Service Pack 4</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=ba6d3aeb-e35a-47cc-bace-7bd9d58a9d3f">Microsoft Internet Explorer 6 Service Pack 1</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b051ae04-fe81-440d-9136-d6b239ca954e">Microsoft Internet Explorer 5.01 Service Pack 4</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=75d2dc78-e3a4-4ff6-9e2d-bf1935003e8e">Microsoft Internet Explorer 6 Service Pack 1</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=41326ade-96b6-47ce-9291-d4e3039471c4">Microsoft Windows 2000 Service Pack 4</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8db9f328-da0e-4fb8-96c4-6d368b47c224">Microsoft Windows 2000 Service Pack 4</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows XP</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-021"><strong>MS08-021</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-022"><strong>MS08-022</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-023"><strong>MS08-023</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-024"><strong>MS08-024</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-020"><strong>MS08-020</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-025"><strong>MS08-025</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows XP Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=c2763dd8-a03e-4a48-aa86-a7ec00250a7a">Windows XP Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=c0124698-3b94-4474-9473-22a2f39a4a56">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=9dbf002f-fe53-4cc7-a430-35f45c520d10">Windows XP Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=36c641ad-953f-4b09-ba1c-9c383295e180">Microsoft Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=e771efe8-8881-4f23-b5b0-15651a390ba9">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=893f4cef-0395-4c44-ba28-7a10b6e7dd48">Windows XP Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0e937f65-abd0-46dd-8883-5bfd70ea1178">Windows XP Service Pack 2</a><br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=166f2ab5-913c-47a9-86fe-b814797b751e">Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=87b80ae3-e299-4d15-a135-3b1bcf943652">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=01400970-df68-4daf-aa39-2fc4f969974c">Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=85beacc0-8ca2-4ded-9c24-23348d05c735">Microsoft Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=9364bf81-6505-4788-958d-a4bd29dc98ad">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8fdd1207-6e93-4c43-bacc-fe3623a6ebe7">Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a29bbd13-761f-44fa-8948-e1a8c244bd7a">Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows Server 2003</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-021"><strong>MS08-021</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-022"><strong>MS08-022</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-023"><strong>MS08-023</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-024"><strong>MS08-024</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-020"><strong>MS08-020</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-025"><strong>MS08-025</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bee91d80-d49a-4d3d-82d6-d5aa63f54979">Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=88518aa6-e334-4529-aa63-0bf2ef417ce3">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=ad384fea-53be-4be3-8acb-1cd23a7f5405">Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0444b76e-93fa-43c2-b1bc-a5c054529eb5">Microsoft Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=9acd2a03-5530-49c8-9ea1-0bfaf259700d">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=214bd8f5-6eb2-414c-b013-c516a306d692">Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d3b855a6-4648-4771-826d-11a151828eac">Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2</a><br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e3dde449-e062-4ce0-a9f4-433bff23e224">Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=12cefefc-8553-4dca-9850-c653371de61e">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=ffc5c893-cb24-4875-b0a7-6d5c7aa4d642">Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5ebb5ef9-615f-4cab-bac5-6f45f1b94952">Microsoft Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=a9e406aa-33e2-49b8-ab54-4a7328e46147">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=fd123394-a5d6-4b55-be74-2938f52ce922">Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=320fd100-35e1-4345-9399-796393235cbc">Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7886a802-f2b5-489c-b14b-631f4c4c0742">Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=fe22a828-cca4-4b51-bbd5-995c65fead21">VBScript 5.6 y JScript 5.6</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=94cf78d3-b6c3-41bc-993e-3af3be0d70f1">Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=63da8040-fda2-42c7-8543-26ad6f9811f2">Microsoft Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=75a05d3a-92a0-4a00-95d4-e2b2f6755180">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e0e63f03-904d-47ee-94fc-51a8dea668eb">Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=126426a7-be38-4327-89db-02d99d76589d">Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows Vista</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-021"><strong>MS08-021</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-022"><strong>MS08-022</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-023"><strong>MS08-023</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-024"><strong>MS08-024</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-020"><strong>MS08-020</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-025"><strong>MS08-025</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Vista y Windows Vista Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=9b51deb8-3873-4146-977f-7e3d0840a4c5">Windows Vista y Windows Vista Service Pack 1</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d7f14001-7f42-4ca0-9193-cdf061179b59">Windows Vista y Windows Vista Service Pack 1</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d4e24966-6530-463a-9ee2-f6a9d000f998">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8203d303-c855-4579-9bbf-b06ddf5c1b87">Windows Vista</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=9640cd8b-d749-4ddd-8af9-b298cebed969">Windows Vista y Windows Vista Service Pack 1</a><br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4ad6dcd1-6ea5-43bf-8bee-a5f507beadc6">Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d33462b6-7391-482d-babe-fb4cd0beaa21">Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=295cf8f2-265e-4570-b708-21033337fe05">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=73f3a234-3973-4467-be7e-69efa7ee978c">Windows Vista x64 Edition</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d56bb4fe-304e-45e0-95f2-fde2f47b2a04">Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

 
<p> </p>
<table style="border:1px solid black;">
<caption>Windows Server 2008</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-021"><strong>MS08-021</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-022"><strong>MS08-022</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-023"><strong>MS08-023</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-024"><strong>MS08-024</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-020"><strong>MS08-020</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-025"><strong>MS08-025</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 para sistemas de 32 bits</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=006d5c47-53e6-4ee1-932c-497611804938">Windows Server 2008 para sistemas de 32 bits</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=95691924-2813-4a86-9e11-99d853f8e606">Windows Server 2008 para sistemas de 32 bits</a><br />
(Baja)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e57b4d94-19ad-4818-8311-a3f94be01a4b">Windows Internet Explorer 7</a>\*<br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4497333c-9418-4b91-83dc-0155735421c0">Windows Server 2008 para sistemas de 32 bits</a><br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2008 para sistemas x64</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8909f144-655b-4f07-916f-fd967f1efb2b">Windows Server 2008 para sistemas x64</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=920ae29b-19d0-4089-ac79-f2da824a2256">Windows Server 2008 para sistemas x64</a><br />
(Baja)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=93e9f52a-c7d0-4033-9c12-740665a219af">Windows Internet Explorer 7</a>\*<br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5aefc7a6-79a4-45a2-b534-35d0ec400dda">Windows Server 2008 para sistemas x64</a><br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 para sistemas con Itanium</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b7771a4a-4e4f-48d1-8551-bb8b778ca5a7">Windows Server 2008 para sistemas con Itanium</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=66df79ac-8364-4922-9688-ebc7ec76d89f">Windows Server 2008 para sistemas con Itanium</a><br />
(Baja)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=acf948e8-c4a9-40da-b282-f5e584e77b05">Windows Internet Explorer 7</a><br />
(Crítica)</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3080c26b-7456-41ef-8668-28f15bc7b8ce">Windows Server 2008 para sistemas con Itanium</a><br />
(Importante)</td>
</tr>
</tbody>
</table>
 

**\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por estas actualizaciones no afectan a las ediciones compatibles Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core, aun cuando los archivos afectados por estas vulnerabilidades puedan estar presentes en el sistema. No obstante, a los usuarios con los archivos afectados se les sigue ofreciendo esta actualización porque los archivos de actualización son más recientes (con números de versión más altos) que los que se encuentran actualmente en el sistema. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Project</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-018"><strong>MS08-018</strong></a></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Project 2000 Service Release 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=fbe46241-b9da-40c6-803d-42eb6234be77">Project 2000 Service Release 1</a><br />
(KB949043)<br />
(Crítica)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Project 2002 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=07a90718-6597-426d-9dca-a336d60c01b8">Project 2002 Service Pack 1</a><br />
(KB949005)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Project 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=aaba07d6-e972-4e85-bccd-406aa2c4a4f4">Project 2003 Service Pack 2</a><br />
(KB948962)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
</tbody>
</table>

 
<p> </p>
<table style="border:1px solid black;">
<caption>Microsoft Visio</caption>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-019"><strong>MS08-019</strong></a></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Gravedad máxima</strong></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Visio 2002 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0056a936-def5-40fa-bcfc-0ab0dd5c3964">Visio 2002 Service Pack 2</a><br />
(KB947896)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Visio 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=18af0ce6-99a0-4471-8d26-9700a8a8e631">Visio 2003 Service Pack 2</a><br />
(KB947650)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Visio 2003 Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=18af0ce6-99a0-4471-8d26-9700a8a8e631">Visio 2003 Service Pack 3</a><br />
(KB947650)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Visio 2007</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0510a1bb-b464-452c-900f-7f4e58ed9c7e">Visio 2007</a><br />
(KB947590)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Visio 2007 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0510a1bb-b464-452c-900f-7f4e58ed9c7e">Visio 2007 Service Pack 1</a><br />
(KB947590)<br />
(Importante)</td>
<td style="border:1px solid black;"></td>
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
  
-   [National Cyber Security Center](http://www.ncsc.go.kr/eng/), República de Corea, por informar de un problema descrito en MS08-018  
-   Un investigador anónimo, por informar de un problema descrito en MS08-019  
-   Un investigador anónimo, por informar de otro problema descrito en MS08-019  
-   Amit Klein, de [Trusteer](http://www.trusteer.com/), por informar de un problema descrito en MS08-020  
-   Alla Berzroutchko, de [Scanit](http://www.scanit.be/), por informar de un problema descrito en MS08-020  
-   Roy Arends, de [Nominet UK](http://www.nominet.org.uk/), por informar de un problema descrito en MS08-020  
-   Jun Mao, de [iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS08-021  
-   Sebastian Apelt, de [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-021  
-   Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/), por informar de un problema descrito en MS08-021  
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS08-021  
-   Peter Ferrie, de [Symantec](http://www.symantec.com/), por informar de un problema descrito en MS08-022  
-   Un investigador anónimo, en colaboración con [iDefense VCP](http://labs.idefense.com/vcp/), por informar de un problema descrito en MS08-023  
-   Carsten Eiram, de [Secunia](http://secunia.com/), por informar de un problema descrito en MS08-024  
-   Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/), por informar de un problema descrito en MS08-025
  
#### Soporte técnico
  
-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).  
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.  
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.
  
#### Renuncia
  
La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.
  
#### Revisiones
  
-   V1.0 (8 de abril de 2008): Publicación del resumen del boletín.  
-   V1.1 (9 de abril de 2008): Actualización del resumen ejecutivo para el boletín de seguridad de Microsoft MS08-018.  
-   V1.2 (16 de abril de 2008): Actualización de la información de investigador para MS08-021 y aclaración del software afectado para Conjuntos de programas y software de Microsoft Office.  
-   V1.3 (18 de febrero de 2009): Se ha agregado una anotación de Core Server no afectado para Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas x64 para MS08-024.
  
*Built at 2014-04-18T01:50:00Z-07:00*
