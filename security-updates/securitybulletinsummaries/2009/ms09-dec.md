---
TOCTitle: 'MS09-DEC'
Title: Resumen del boletín de seguridad de Microsoft de diciembre 2009
ms:assetid: 'ms09-dec'
ms:contentKeyID: 61225398
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-dec(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de diciembre 2009
===============================================================

Publicado: martes, 8 de diciembre de 2009 | Actualizado: miércoles, 13 de enero de 2010

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para diciembre de 2009.

Con la publicación de los boletines de diciembre de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de diciembre de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 9 de diciembre de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de diciembre](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032407802&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-071">MS09-071</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el servicio de autenticación podría permitir la ejecución remota de código (974318)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si los mensajes que recibe el servidor del Servicio de autenticación de Internet se copian incorrectamente en la memoria al procesar los intentos de autenticación PEAP. En Windows Server 2008, Servicio de autenticación de Internet se reemplaza por Servidor de directiva de red (NPS). Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado. Los servidores que usan Servicio de autenticación de Internet o Servidor de directiva de red sólo están afectados cuando usan PEAP con la autenticación MS-CHAP v2.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-074">MS09-074</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office Project podría permitir la ejecución remota de código (967183)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office Project. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Project especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-072">MS09-072</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (976325)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Un control ActiveX compilado con encabezados de Microsoft Active Template Library (ATL) también podría permitir la ejecución remota de código. Esta vulnerabilidad se ha descrito en el documento informativo sobre seguridad de Microsoft 973882 y el boletín de seguridad MS09-035.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-069">MS09-069</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio del subsistema de autoridad de seguridad local podría permitir la denegación de servicio (974392)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante remoto autenticado, durante la comunicación mediante la Seguridad del protocolo de Internet (IPsec), envía un mensaje ISAKMP especialmente diseñado al servicio de subsistema de la autoridad de seguridad local (LSASS) en un sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-070">MS09-070</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Servicios de federación de Active Directory podrían permitir la ejecución remota de código (971726)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante envía una solicitud HTTP especialmente diseñada a un servidor web habilitado para ADFS. El atacante debe ser un usuario autenticado para aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-073">MS09-073</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los convertidores de texto de WordPad y Office podría permitir la ejecución remota de código (975539)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft WordPad y Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si se abre un archivo de Word 97 especialmente diseñado en WordPad o Microsoft Office Word. Un atacante que aprovechara con éxito esta vulnerabilidad podría obtener los mismos privilegios que el usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos privilegios en el sistema correrían un riesgo menor que aquellos que cuenten con privilegios administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft Office</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título de vulnerabilidad                                                                               | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                                                                                                                                                                                     |  
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-069](http://technet.microsoft.com/security/bulletin/ms09-069) | Vulnerabilidad de agotamiento de recursos en el servicio de subsistema de autoridad de seguridad local | [CVE-2009-3675](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3675) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | La vulnerabilidad no permite la ejecución remota de código, sólo la denegación de servicio si un atacante remoto autenticado aprovecha la vulnerabilidad.                                                                                                                                                                       |  
| [MS09-070](http://technet.microsoft.com/security/bulletin/ms09-070) | Vulnerabilidad de suplantación de identidad del inicio de sesión único en ADFS                         | [CVE-2009-2508](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2508) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | La vulnerabilidad no permite la ejecución remota de código, sólo la suplantación de identidad.                                                                                                                                                                                                                                  |  
| [MS09-070](http://technet.microsoft.com/security/bulletin/ms09-070) | Vulnerabilidad de ejecución remota de código en ADFS                                                   | [CVE-2009-2509](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2509) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Sólo un atacante autenticado puede aprovechar la vulnerabilidad.                                                                                                                                                                                                                                                                |  
| [MS09-071](http://technet.microsoft.com/security/bulletin/ms09-071) | Vulnerabilidad de daños en la memoria relacionada con el Servicio de autenticación de Internet         | [CVE-2009-2505](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2505) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Posibilidad limitada de ejecución remota de código. El resultado más probable es la denegación de servicio.                                                                                                                                                                                                                     |  
| [MS09-071](http://technet.microsoft.com/security/bulletin/ms09-071) | Vulnerabilidad de omisión de autenticación de MS-CHAP                                                  | [CVE-2009-3677](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3677) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | La vulnerabilidad no permite la ejecución remota de código, sólo la elevación de privilegios debido a que se elude la autenticación de red.                                                                                                                                                                                     |  
| [MS09-072](http://technet.microsoft.com/security/bulletin/ms09-072) | Vulnerabilidad de inicialización COM de ATL                                                            | [CVE-2009-2493](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2493) | Ninguna                                                                                                                               | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul). Esto se debe a que la vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035).) |  
| [MS09-072](http://technet.microsoft.com/security/bulletin/ms09-072) | Vulnerabilidad de daños en la memoria sin inicializar                                                  | [CVE-2009-3671](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3671) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                       |  
| [MS09-072](http://technet.microsoft.com/security/bulletin/ms09-072) | Vulnerabilidad de daños en la memoria relacionada con los objetos                                      | [CVE-2009-3672](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3672) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                       |  
| [MS09-072](http://technet.microsoft.com/security/bulletin/ms09-072) | Vulnerabilidad de daños en la memoria sin inicializar                                                  | [CVE-2009-3673](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3673) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                       |  
| [MS09-072](http://technet.microsoft.com/security/bulletin/ms09-072) | Vulnerabilidad de daños en la memoria sin inicializar                                                  | [CVE-2009-3674](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3674) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                       |  
| [MS09-073](http://technet.microsoft.com/security/bulletin/ms09-073) | Vulnerabilidad de daños en la memoria de los convertidores de texto de WordPad y Office                | [CVE-2009-2506](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2506) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                       |  
| [MS09-074](http://technet.microsoft.com/security/bulletin/ms09-074) | Vulnerabilidad de validación de la memoria en Project                                                  | [CVE-2009-0102](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0102) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                       |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
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
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
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
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=5b02d10d-1abd-4d68-826b-71dad543657a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=0cf37247-505a-4dc2-aad7-c8cb1a63b57a)  
(Crítica)  
[Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7fb6261c-6895-4f79-be2c-bb110874a19c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=560e01db-5f59-4ef1-9406-f5d7e0fd4128)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=50936f51-b0a9-4e94-85bf-93f9ad74fdd1)  
(KB973904)  
(Importante)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
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
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4d294be6-19d1-43b5-9c75-f9d30699a2e7)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=facab13f-ea31-4c71-be4c-24e44ded174f)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=def2c038-3b03-4162-a563-a6ebec756f37)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=6c003629-77bf-4735-bd4a-c37c4386f869)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=5448b168-6bf7-4bae-9627-b88d76c4d5c5)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c090c4c2-c277-4d8c-91e1-28286bc5443e)  
(KB973904)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=17b5206d-61e9-4663-afc7-80e98bf4d618)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=a253c19a-c808-4115-8bd0-cf312d396abd)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=98a56425-4f88-4f0f-963b-dada8dc0d8f8)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=0c9af3b5-d015-4025-bbb4-1a5113e9113f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c2bbf515-f81a-436b-947b-cbf2db85fdd9)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4b9bf156-cd34-460f-b4ad-571e37f54659)  
(KB973904)  
(Importante)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3d49b386-133a-4d51-b6f0-cec0c70ef93e)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=6659fc40-71ee-44a9-9656-8d3ee02b5bc0)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7bdba030-e2c6-44ac-bb5f-24ae8ec372a2)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=0dd50357-64f2-4286-86ba-c512e65eed2a)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a779aae1-7724-4458-94fb-a2343356ecae)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=31351b9e-b5bb-4618-990b-1089ea5a3bc2)<sup>[1]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b9678229-2473-4aae-a814-eca9ea556d17)  
(KB973904)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5a273b47-8a18-4778-9b60-8b560a1ce089)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=287e7921-8aab-42a6-b647-551d0a9adc15)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4de4bbcd-b1b8-4482-8ef7-0d9b4a730e0c)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e62aba15-5eeb-46a2-a142-bfca94016c55)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a8a9bf12-4ad6-49fd-b2b7-f379dc3309d2)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b6eb9d9b-1a43-4b30-a033-19a1db786244)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=257facf3-20a1-49e2-ab4c-c1ae67fe05a0)  
(KB973904)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=498f5eeb-d03e-42ee-ad6a-9d6f98c66acb)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=9ce1a721-0c6a-4775-9407-9633d817d716)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=72d44de7-dfc5-4667-a59f-2ee73d0e3708)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=f5b003ad-af25-488a-91fb-98835a0bfeac)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=1a7784ef-5d25-4de1-a293-f742b5a3473d)  
(KB973904)  
(Importante)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3e4ae4d0-1060-4867-82c5-7e20ea93c2c6)  
(Moderada)  
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3e4ae4d0-1060-4867-82c5-7e20ea93c2c6)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=40d26d40-4203-4013-b3f9-912a5b209fbd)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=47d5ada1-1d60-4233-bdd3-64918b5e1245)  
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2ca62ea8-67cb-40da-8a65-db6f3607bbab)  
(Moderada)  
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2ca62ea8-67cb-40da-8a65-db6f3607bbab)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3140527a-aa33-462b-b3a6-bfcd78b5aa0c)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=1e466b48-422f-4c80-8fdf-ba61111942b1)  
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
<th colspan="6" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=582a1b15-214e-4f5e-bb5b-95677f4d5968)\*  
(Importante)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=582a1b15-214e-4f5e-bb5b-95677f4d5968)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d0570536-756e-4fda-883d-f2a3c4ac5bbd)\*  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=43660133-43e1-41f3-8a82-98c4a739914f)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f6715abb-fd93-44ba-9854-2ecc672622da)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=77e774b4-ec0c-481c-9e93-eee9f44ec71b)\*  
(Importante)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=77e774b4-ec0c-481c-9e93-eee9f44ec71b)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0e72d0f1-2ce7-4650-b72c-bb303351aafc)\*  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=22972970-740f-4c50-93ec-f6d49dd1b360)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d1f5e9e-a7de-4f96-89c8-510fd51f16e7)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=89defe77-7e82-4bfa-9693-66c93b930da1)  
(Moderada)  
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=89defe77-7e82-4bfa-9693-66c93b930da1)  
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2c7765a2-3117-4dd8-94b4-0060ca16871b)  
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
<th colspan="6" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5af3be0b-2dd2-4039-90e1-2278e9c5aee5)  
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
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9d9a04c8-a019-4943-8e93-c6bfd77c8960)  
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
<th colspan="6" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-071**](http://technet.microsoft.com/security/bulletin/ms09-071)
</td>
<td style="border:1px solid black;">
[**MS09-072**](http://technet.microsoft.com/security/bulletin/ms09-072)
</td>
<td style="border:1px solid black;">
[**MS09-069**](http://technet.microsoft.com/security/bulletin/ms09-069)
</td>
<td style="border:1px solid black;">
[**MS09-070**](http://technet.microsoft.com/security/bulletin/ms09-070)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=bcb38127-787f-49b0-b3fb-62f6a8628d89)\*  
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
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2c1b96f2-b3c3-4711-a9ad-b2133ea7bf81)  
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
</table>
 
**Nota para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS09-070**

<sup>[1]</sup> Sólo está afectado cuando se ha actualizado con Windows Server 2003 R2, que implementa Servicios de federación de Active Directory.

<sup>[2]</sup> Sólo está afectado cuando se ha actualizado con Windows Server 2003 R2 x64 Edition, que implementa Servicios de federación de Active Directory.

**Nota para MS09-073**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-074**](http://technet.microsoft.com/security/bulletin/ms09-074)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office XP
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=bc3ec3ba-2cec-43ab-b184-c222794231f2)  
(KB975008)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b4a4126c-b0b3-4db2-b6f5-0e67519c2a5f)  
(KB975051)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-074**](http://technet.microsoft.com/security/bulletin/ms09-074)
</td>
<td style="border:1px solid black;">
[**MS09-073**](http://technet.microsoft.com/security/bulletin/ms09-073)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Project 2000
</td>
<td style="border:1px solid black;">
[Microsoft Project 2000 Service Release 1](http://www.microsoft.com/downloads/details.aspx?familyid=135c010a-55f4-4385-b67d-96ea06ef881a)  
(KB961083)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Project 2002
</td>
<td style="border:1px solid black;">
[Microsoft Project 2002 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c55ef8fe-8f66-42fc-a298-de6f8886b3e4)  
(KB961079)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Project 2003
</td>
<td style="border:1px solid black;">
[Microsoft Office Project 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2ea8ca39-f130-439a-92d5-77e9ef050105)  
(KB961082)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Works 8.5
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 8.5](http://www.microsoft.com/downloads/details.aspx?familyid=807426a1-8b78-4681-a606-dc39f4d7b64a)  
(KB977304)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de convertidores de Microsoft Office
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete de convertidores de Microsoft Office](http://www.microsoft.com/downloads/details.aspx?familyid=f3ff8bb6-d047-42f1-9331-b6df85fff9fd)  
(KB974882)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS09-073**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Ryan Smith, de [Verisign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-072
-   Sam Thomas, de eshu.co.uk, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-072
-   [team509](http://www.team509.com/), en colaboración con [Verisign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-072
-   Un investigador anónimo, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-072
-   Un investigador anónimo, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de otro problema descrito en MS09-072
-   Sean Larsson y Jun Mao, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-073
-   Bing Liu, de [FortiGuard Labs de Fortinet](http://www.fortiguard.com/), por informar de un problema descrito en MS09-074

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de diciembre de 2009): Publicación del resumen del boletín.
-   V1.1 (9 de diciembre de 2009): Se ha actualizado la descripción para MS09-071 en la tabla Resúmenes ejecutivos. Se ha corregido el requisito de reinicio para MS09-073.
-   V2.0 (13 de enero de 2010): Para MS09-073, se ha cambiado el nombre de los paquetes de actualización que anteriormente se enumeraban como **Microsoft Office Word 2002 Service Pack 3 (KB975008)** y **Microsoft Office Word 2003 Service Pack 3 (KB975051)** por **Microsoft Office XP Service Pack 3 (KB975008)** y **Microsoft Office 2003 Service Pack 3 (KB975051)**, respectivamente.

*Built at 2014-04-18T01:50:00Z-07:00*
