---
TOCTitle: 'MS09-JAN'
Title: Resumen del boletín de seguridad de Microsoft de enero 2009
ms:assetid: 'ms09-jan'
ms:contentKeyID: 61225400
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-jan(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de enero 2009
===========================================================

Publicado: martes, 13 de enero de 2009

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para enero de 2009.

Con la publicación de los boletines de enero de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 8 de enero de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 14 de enero de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de enero](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032395120). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-001">MS09-001</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en SMB podrían permitir la ejecución remota de código (958687)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades en el protocolo del bloque de mensajes del servidor (SMB) de Microsoft de las que se ha informado de forma privada y una de forma pública. Las vulnerabilidades podrían permitir la ejecución remota de código en los sistemas afectados. Un atacante que aprovechara con éxito estas vulnerabilidades podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Si se siguen las prácticas recomendadas relativas al uso de servidores de seguridad y se implementan las configuraciones de servidores de seguridad predeterminadas estándar, puede contribuirse a proteger una red de los ataques que se originen fuera del ámbito de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                              | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                                                                                                                                                                                                                                                                                        |  
|---------------------------------------------------------------------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-001](http://technet.microsoft.com/security/bulletin/ms09-001) | Vulnerabilidades en SMB podrían permitir la ejecución remota de código (958687) | [CVE-2008-4114](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4114) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad no permite la ejecución remota de código. Existe una prueba pública de código que permite ejecutar la negación de servicio remoto.                                                                                                                                                                                                                                                                             |  
| [MS09-001](http://technet.microsoft.com/security/bulletin/ms09-001) | Vulnerabilidades en SMB podrían permitir la ejecución remota de código (958687) | [CVE-2008-4834](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4834) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Aunque se trata de una vulnerabilidad de ejecución remota de código, es improbable que haya código funcional que la aproveche. Para obtener más información, consulte el blog de investigación y defensa de vulnerabilidades de seguridad de Microsoft, [Asignar prioridad a la implementación del boletín de SMB](http://blogs.technet.com/swi/archive/2009/01/09/ms09-001-prioritizing-the-deployment-of-the-smb-bulletin.aspx). |  
| [MS09-001](http://technet.microsoft.com/security/bulletin/ms09-001) | Vulnerabilidades en SMB podrían permitir la ejecución remota de código (958687) | [CVE-2008-4835](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4835) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Aunque se trata de una vulnerabilidad de ejecución remota de código, es improbable que haya código funcional que la aproveche. Para obtener más información, consulte el blog de investigación y defensa de vulnerabilidades de seguridad de Microsoft, [Asignar prioridad a la implementación del boletín de SMB](http://blogs.technet.com/swi/archive/2009/01/09/ms09-001-prioritizing-the-deployment-of-the-smb-bulletin.aspx). |
  
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
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-001**](http://technet.microsoft.com/security/bulletin/ms09-001)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=e0678d14-c1b5-457a-8222-8e7682760ed4)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-001**](http://technet.microsoft.com/security/bulletin/ms09-001)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=eeafcdc5-df39-4b29-b6f1-7d32b64761e1)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=26898401-f669-4542-ad93-199ed1fe9a2a)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-001**](http://technet.microsoft.com/security/bulletin/ms09-001)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=588ca8e8-38a9-47ed-9c41-09aaf1022e49)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ee59441c-1e8f-4425-ae8d-dec14e7f13fb)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=caec9321-fa5b-42f0-9f26-61f673fe6eef)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-001**](http://technet.microsoft.com/security/bulletin/ms09-001)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9179c463-c10a-452a-990f-b7e37cdd889b)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6b26952e-b59d-4b0f-a52d-025e45ecd233)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-001**](http://technet.microsoft.com/security/bulletin/ms09-001)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=7245b411-7c9e-41e5-9841-4c586336086c)\*  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=a241eaad-95a0-442b-978f-f21a6f0c7db4)\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ab7c7015-20bb-4a0c-977a-969f4e2a5189)  
(Moderada)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

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

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/bb466214.aspx).

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

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

-   Un investigador anónimo, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-001
-   Un investigador anónimo, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de otro problema descrito en MS09-001

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (13 de enero de 2009): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
