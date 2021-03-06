---
TOCTitle: 'MS09-JUN'
Title: Resumen del boletín de seguridad de Microsoft de junio 2009
ms:assetid: 'ms09-jun'
ms:contentKeyID: 61225402
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-jun(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de junio 2009
===========================================================

Publicado: martes, 9 de junio de 2009

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2009.

Con la publicación de los boletines de junio de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de junio de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 10 de junio de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?culture=en-us&eventid=1032395225). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-018">MS09-018</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Active Directory podrían permitir la ejecución remota de código (971055)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en implementaciones de Active Directory en Microsoft Windows 2000 Server y Windows Server 2003, y Active Directory Application Mode (ADAM) cuando se instala en Windows XP Professional y Windows Server 2003. La vulnerabilidad más grave podría permitir la ejecución remota de código. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado de forma remota. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Si se siguen las prácticas recomendadas relativas al uso de servidores de seguridad y se implementan las configuraciones de servidores de seguridad predeterminadas estándar, puede contribuirse a proteger una red de los ataques que se originen fuera del ámbito de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-022">MS09-022</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el administrador de trabajos en cola de Windows podrían permitir la ejecución remota de código (961501)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en el administrador de trabajos en cola de Windows. La vulnerabilidad más grave podría permitir la ejecución remota de código si un servidor afectado recibe una solicitud RPC especialmente diseñada. Si se siguen las prácticas recomendadas relativas al uso de servidores de seguridad y se implementan las configuraciones de servidores de seguridad predeterminadas estándar, puede contribuirse a proteger una red de los ataques que se originen fuera del ámbito de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-019">MS09-019</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet (969897)</strong><br />
<br />
Esta actualización de seguridad resuelve siete vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-027">MS09-027</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Word podrían permitir la ejecución remota de código (969514)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada que podrían permitir la ejecución remota de código si un usuario abre un archivo de Word especialmente diseñado. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-021">MS09-021</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada que podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado que incluya un objeto de registro con formato incorrecto. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-024">MS09-024</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los convertidores de Microsoft Works podría permitir la ejecución remota de código (957632)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los convertidores de Microsoft Works. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Works especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-026">MS09-026</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en RPC podría permitir la elevación de privilegios (970238)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en la función de llamada a procedimiento remoto (RPC) de Windows, donde el motor de cálculo de referencias de RPC no actualiza su estado interno de forma adecuada. La vulnerabilidad podría permitir a un atacante ejecutar código arbitrario y tomar el control completo de un sistema afectado. Las ediciones compatibles de Microsoft Windows no se proporcionan con servidores o clientes de RPC que estén expuestos a esta vulnerabilidad. En una configuración predeterminada, no se puede atacar a los usuarios mediante esta vulnerabilidad. No obstante, la vulnerabilidad se encuentra en el módulo de tiempo de ejecución de RPC de Microsoft Windows y podría afectar a aplicaciones RPC de terceros.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-025">MS09-025</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (968537)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el kernel de Windows que podrían permitir la elevación de privilegios. Un atacante que consiga aprovechar cualquiera de estas vulnerabilidades podría ejecutar código arbitrario y tomar el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de aprovechar estas vulnerabilidades. Los usuarios anónimos o los usuarios remotos no pueden aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-020">MS09-020</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Internet Information Services (IIS) podría permitir la elevación de privilegios (970483)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en Internet Information Services (IIS). Las vulnerabilidades podrían permitir la elevación de privilegios si atacante envía una solicitud HTTP especialmente diseñado a un sitio web que requiere autenticación. Estas vulnerabilidades permiten que un atacante omita la configuración de IIS que especifica el tipo de autenticación que está permitido, pero no la comprobación de la lista de control de acceso (ACL) basada en el sistema de archivos, que comprueba si un determinado usuario puede obtener acceso a un archivo. Aunque se aprovecharan estas vulnerabilidades, el atacante estaría restringido a los permisos concedidos a la cuenta de usuario anónimo por parte de las ACL del sistema de archivos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-023">MS09-023</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Búsqueda de Windows podría permitir la divulgación de información (963093)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en Búsqueda de Windows de la que se ha informado de forma privada. La vulnerabilidad podría permitir la divulgación de información si un usuario realiza una búsqueda que devuelve un archivo especialmente diseñado como el primer resultado o si el usuario obtiene la vista previa de un archivo especialmente diseñado de los resultados de búsqueda. De forma predeterminada, el componente Búsqueda de Windows no se preinstala en Microsoft Windows XP ni Windows Server 2003. Es un componente opcional disponible para descargarlo. Búsqueda de Windows instalado en las ediciones compatibles de Windows Vista y Windows Server 2008 no está afectado por esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Moderada</a><br />
Divulgación de información</td>
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
  
| Identificador del boletín                                           | Título del boletín                                                                                                          | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                                                                                                                                  |  
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-018](http://technet.microsoft.com/security/bulletin/ms09-018) | Vulnerabilidades en Active Directory podrían permitir la ejecución remota de código (971055)                                | [CVE-2009-1138](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1138) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Existe la posibilidad de ejecución remota de código en los servidores Windows 2000 que exponen el servicio LDAP (tcp predeterminado/389) en la red.                                                                                                                          |  
| [MS09-018](http://technet.microsoft.com/security/bulletin/ms09-018) | Vulnerabilidades en Active Directory podrían permitir la ejecución remota de código (971055)                                | [CVE-2009-1139](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1139) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | El efecto de seguridad de esta vulnerabilidad es una pérdida de memoria que finalmente conlleva la denegación de servicio. No es posible la ejecución de código.                                                                                                             |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2007-3091](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2007-3091) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1140](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1140) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de acceso a información entre dominios que puede provocar la divulgación de información pero no la ejecución remota de código.                                                                                                                |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1141](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1141) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1528](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1528) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1529](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1529) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1530](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1530) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1531](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1531) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-019](http://technet.microsoft.com/security/bulletin/ms09-019) | Actualización de seguridad acumulativa para Internet (969897)                                                               | [CVE-2009-1532](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1532) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-020](http://technet.microsoft.com/security/bulletin/ms09-020) | Vulnerabilidades en Internet Information Services (IIS) podría permitir la elevación de privilegios (970483)                | [CVE-2009-1122](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1122) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Probabilidad baja de ejecución de código pero probabilidad alta de divulgación de información debido a las condiciones de omisión de la autenticación.                                                                                                                       |  
| [MS09-020](http://technet.microsoft.com/security/bulletin/ms09-020) | Vulnerabilidades en Internet Information Services (IIS) podría permitir la elevación de privilegios (970483)                | [CVE-2009-1535](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1535) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Hay disponible código público para la divulgación de información.                                                                                                                                                                                                            |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0549](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0549) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0557](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0557) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0558](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0558) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0559](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0559) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | La amenaza de ejecución de código sólo existe para Office 2000. Es improbable que los ataques a versiones posteriores de Office produzcan la ejecución de código.                                                                                                            |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0560](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0560) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-0561](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0561) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-021](http://technet.microsoft.com/security/bulletin/ms09-021) | Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (969462)                          | [CVE-2009-1134](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1134) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-022](http://technet.microsoft.com/security/bulletin/ms09-022) | Vulnerabilidades en el administrador de trabajos en cola de Windows podrían permitir la ejecución remota de código (961501) | [CVE-2009-0228](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0228) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-022](http://technet.microsoft.com/security/bulletin/ms09-022) | Vulnerabilidades en el administrador de trabajos en cola de Windows podrían permitir la ejecución remota de código (961501) | [CVE-2009-0229](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0229) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de divulgación de información sin posibilidad de ejecución de código.                                                                                                                                                                         |  
| [MS09-022](http://technet.microsoft.com/security/bulletin/ms09-022) | Vulnerabilidades en el administrador de trabajos en cola de Windows podrían permitir la ejecución remota de código (961501) | [CVE-2009-0230](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0230) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-023](http://technet.microsoft.com/security/bulletin/ms09-023) | Una vulnerabilidad en Búsqueda de Windows podría permitir la divulgación de información (963093)                            | [CVE-2009-0239](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0239) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-024](http://technet.microsoft.com/security/bulletin/ms09-024) | Una vulnerabilidad en los convertidores de Microsoft Works podría permitir la ejecución remota de código (957632)           | [CVE-2009-1533](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1533) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-025](http://technet.microsoft.com/security/bulletin/ms09-025) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (968537)                                | [CVE-2009-1123](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1123) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-025](http://technet.microsoft.com/security/bulletin/ms09-025) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (968537)                                | [CVE-2009-1124](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1124) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-025](http://technet.microsoft.com/security/bulletin/ms09-025) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (968537)                                | [CVE-2009-1125](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1125) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-025](http://technet.microsoft.com/security/bulletin/ms09-025) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (968537)                                | [CVE-2009-1126](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1126) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Existe bastante probabilidad de código que aproveche la vulnerabilidad en Windows 2000. La probabilidad de ejecución de código por esta vulnerabilidad de desbordamiento de búfer de pila es reducida en Windows XP y Windows Server 2003 debido a la protección /GS.        |  
| [MS09-026](http://technet.microsoft.com/security/bulletin/ms09-026) | Una vulnerabilidad en RPC podría permitir la elevación de privilegios (970238)                                              | [CVE-2009-0568](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0568) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Esta vulnerabilidad no afecta directamente a ningún software de Microsoft. No obstante, las estaciones de trabajo en las que se hayan implementado servicios de RPC pueden estar expuestas a la ejecución remota de código si no se instala esta actualización de seguridad. |  
| [MS09-027](http://technet.microsoft.com/security/bulletin/ms09-027) | Vulnerabilidades en Microsoft Office Word podrían permitir la ejecución remota de código (969514)                           | [CVE-2009-0563](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0563) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                    |  
| [MS09-027](http://technet.microsoft.com/security/bulletin/ms09-027) | Vulnerabilidades en Microsoft Office Word podrían permitir la ejecución remota de código (969514)                           | [CVE-2009-0565](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0565) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                    |
  
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
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-018**](http://technet.microsoft.com/security/bulletin/ms09-018)
</td>
<td style="border:1px solid black;">
[**MS09-022**](http://technet.microsoft.com/security/bulletin/ms09-022)
</td>
<td style="border:1px solid black;">
[**MS09-019**](http://technet.microsoft.com/security/bulletin/ms09-019)
</td>
<td style="border:1px solid black;">
[**MS09-026**](http://technet.microsoft.com/security/bulletin/ms09-026)
</td>
<td style="border:1px solid black;">
[**MS09-025**](http://technet.microsoft.com/security/bulletin/ms09-025)
</td>
<td style="border:1px solid black;">
[**MS09-020**](http://technet.microsoft.com/security/bulletin/ms09-020)
</td>
<td style="border:1px solid black;">
[**MS09-023**](http://technet.microsoft.com/security/bulletin/ms09-023)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Active Directory en Microsoft Windows 2000 Server Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=bba6e20a-0345-46ae-a6f1-fd27fdee7c21&displaylang=es)  
(KB969805)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=bba6e20a-0345-46ae-a6f1-fd27fdee7c21&displaylang=es)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=d645ad82-13c3-4030-808b-834e86ed3298)  
(Crítica)  
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=fe8b3796-a407-4f41-89eb-35b4bcc24ff6)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=155a79c1-e5e4-4f62-b4b0-53aca59f20ac)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=79b0481d-a3d7-477b-928a-a98cc79374af)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 5.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=8515a294-4f25-4dc5-860a-e7ad9b6c1c01)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-018**](http://technet.microsoft.com/security/bulletin/ms09-018)
</td>
<td style="border:1px solid black;">
[**MS09-022**](http://technet.microsoft.com/security/bulletin/ms09-022)
</td>
<td style="border:1px solid black;">
[**MS09-019**](http://technet.microsoft.com/security/bulletin/ms09-019)
</td>
<td style="border:1px solid black;">
[**MS09-026**](http://technet.microsoft.com/security/bulletin/ms09-026)
</td>
<td style="border:1px solid black;">
[**MS09-025**](http://technet.microsoft.com/security/bulletin/ms09-025)
</td>
<td style="border:1px solid black;">
[**MS09-020**](http://technet.microsoft.com/security/bulletin/ms09-020)
</td>
<td style="border:1px solid black;">
[**MS09-023**](http://technet.microsoft.com/security/bulletin/ms09-023)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM) en Windows XP Professional Service Pack 2 y Windows XP Professional Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=cb2c9b76-0c65-4754-9941-d45a7c74a29a)  
(KB970437)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=f2119aca-a98e-4810-be52-f38241443baf)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=3d7f63ee-d7c3-48a5-902e-60625405e97d)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=827b735c-660b-4723-b688-3297e107153a)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=d9e27ce1-4e7c-437f-9477-e7805a33da08)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=f033fa78-c451-44f8-aa6c-a49622c37f40)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6349e046-a3f8-4ae5-b8c3-c9879cc99e8f&displaylang=en)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 5.1 en Windows XP Professional Service Pack 2 y Windows XP Professional Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=97da589f-4534-42f6-9f29-967b5a33c542)  
(Importante)
</td>
<td style="border:1px solid black;">
[Búsqueda de Windows 4.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=759f22cb-ea7f-49dd-a200-19cb83fffd8d)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?familyid=2ef3aaf0-a2a9-4c17-99ab-a0dc3d3f7e86)  
(KB970437)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=22699d09-1e68-456a-8733-bfad6667ebf5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=088f70eb-c5c5-426a-880a-18ed386d0b56)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e5d2c81e-ffab-4e3b-a59a-a55000597213)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=a24aedf0-7a31-4ee8-a9a6-998f1160c700)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20734b70-37f1-47dd-bc09-d56f93577a55)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3769800e-af93-4a44-8a1e-b30cc54b226f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=8982e6d2-e1f7-4208-88e3-80b159a8e21a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Búsqueda de Windows 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=50c56dd6-c34d-4632-a779-8bcf8fdb341b)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-018**](http://technet.microsoft.com/security/bulletin/ms09-018)
</td>
<td style="border:1px solid black;">
[**MS09-022**](http://technet.microsoft.com/security/bulletin/ms09-022)
</td>
<td style="border:1px solid black;">
[**MS09-019**](http://technet.microsoft.com/security/bulletin/ms09-019)
</td>
<td style="border:1px solid black;">
[**MS09-026**](http://technet.microsoft.com/security/bulletin/ms09-026)
</td>
<td style="border:1px solid black;">
[**MS09-025**](http://technet.microsoft.com/security/bulletin/ms09-025)
</td>
<td style="border:1px solid black;">
[**MS09-020**](http://technet.microsoft.com/security/bulletin/ms09-020)
</td>
<td style="border:1px solid black;">
[**MS09-023**](http://technet.microsoft.com/security/bulletin/ms09-023)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=d814ce65-a193-4027-a6cd-106d388830a6)   
(KB969805)  
(Importante)  
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=f6f99957-f74f-4446-8734-a468283eebae)   
(KB970437)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=865414f8-3f77-4fee-acc6-6684a3dc0aa4)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=72a23752-86fb-4cc9-ab8e-63ffdfae5bec)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=a980b867-c67f-4c61-b6db-e55c2ca68dc0)  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=298143f2-f37a-4a2c-86ac-9804d4ff1dad)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=62bb9e22-4f4b-4ffc-ba76-f626e94c79d5)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=9356404c-d89a-4de0-b9b4-f6e1bdadf745)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 6.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=2bd4e410-dbd8-431a-b316-e1e2f1825c3a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Búsqueda de Windows 4.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=e72ef31f-5161-4fe6-8ed3-6206e02cef31)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=0d1f23c8-06eb-4996-92eb-0eb635fd6a42)  
(KB969805)  
(Importante)  
[Active Directory Application Mode (ADAM)](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=1a2badc7-c0a5-4032-a009-73ebe9d76313)  
(KB970437)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=197a6cc7-4ba3-4d2e-b621-0ef3da645ef2)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=2a03d3c4-e39d-43a3-8d42-216e9551be96)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5e7d6372-9c8c-449d-88fd-afd4f92ad9e6)  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=4a5401d7-ca97-4734-a0e9-d7ffe0777e34)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=888b8dd8-d76c-42f5-a377-1f1750d3cf56)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5a3123af-173d-49eb-9997-14e82e764aee)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 6.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=ea363223-535d-4142-9aba-3890960c6259)  
(Importante)
</td>
<td style="border:1px solid black;">
[Búsqueda de Windows 4.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=7ffc3680-f9bf-423b-96a7-102f4cc9c240)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Active Directory](http://www.microsoft.com/downloads/details.aspx?familyid=92e7808b-92ff-449d-bb73-ee8638e9ccd1)  
(KB969805)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=719efd62-fb33-447d-b6dd-2aaafbbad881)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=58efde2c-e0b8-4259-b19e-80564b834882)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a2d2907e-67ae-44a4-a805-8670e659ea57)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3084f46e-02b9-4d99-a7a1-033817f9bd9f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=13b50993-410f-4e7a-a33a-6d9b48dbb4d1)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Information Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e6b806eb-e2c4-4436-8964-720db593055d)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-018**](http://technet.microsoft.com/security/bulletin/ms09-018)
</td>
<td style="border:1px solid black;">
[**MS09-022**](http://technet.microsoft.com/security/bulletin/ms09-022)
</td>
<td style="border:1px solid black;">
[**MS09-019**](http://technet.microsoft.com/security/bulletin/ms09-019)
</td>
<td style="border:1px solid black;">
[**MS09-026**](http://technet.microsoft.com/security/bulletin/ms09-026)
</td>
<td style="border:1px solid black;">
[**MS09-025**](http://technet.microsoft.com/security/bulletin/ms09-025)
</td>
<td style="border:1px solid black;">
[**MS09-020**](http://technet.microsoft.com/security/bulletin/ms09-020)
</td>
<td style="border:1px solid black;">
[**MS09-023**](http://technet.microsoft.com/security/bulletin/ms09-023)
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
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=3ad8f037-2434-4dea-bfc3-9d3b4008b828)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=e60215c3-b8b9-4e45-9d9f-b3fb0b47cce1)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=6f2730e9-b4fc-4f20-96cf-73f1be63f374)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5ca227c0-f2dd-429c-a542-e08e93527214)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=c31b36f8-330c-4a0c-9a3d-7cbe9a1ab8c8)  
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
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=85c317cd-2a14-4747-9f50-3af3ddd3ae1b)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=88185088-8c2c-4bc6-89b2-87f4d4849cf7)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5edb14f7-11ec-4180-9f0f-b2673f1c8d83)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=188adafe-1feb-46ad-b237-a88d35104dcd)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=7d70a65f-07ce-4992-8bec-28fefd7587bc)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-018**](http://technet.microsoft.com/security/bulletin/ms09-018)
</td>
<td style="border:1px solid black;">
[**MS09-022**](http://technet.microsoft.com/security/bulletin/ms09-022)
</td>
<td style="border:1px solid black;">
[**MS09-019**](http://technet.microsoft.com/security/bulletin/ms09-019)
</td>
<td style="border:1px solid black;">
[**MS09-026**](http://technet.microsoft.com/security/bulletin/ms09-026)
</td>
<td style="border:1px solid black;">
[**MS09-025**](http://technet.microsoft.com/security/bulletin/ms09-025)
</td>
<td style="border:1px solid black;">
[**MS09-020**](http://technet.microsoft.com/security/bulletin/ms09-020)
</td>
<td style="border:1px solid black;">
[**MS09-023**](http://technet.microsoft.com/security/bulletin/ms09-023)
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
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=0f18356d-9f09-4d24-8361-970c0d1ccac4)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=a0e3f975-57da-43fa-ac12-3d14fd6ce939)\*\*  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=aaad301c-d232-4733-a0df-8e5d41bbfde8)\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=eaa26c6c-5bf7-4099-bb21-1e03de3a25ca)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=98ba52b2-da1a-4939-a10e-d43b3a7e7ed4)\*  
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
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=7d0a6e8d-a31d-4f3d-a7d7-e61215bfebed)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=758edce7-2a82-4b2e-bd71-5b7075cc4b17)\*\*  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=faac92d4-4a2b-4bb5-8bd1-1519a9fa8147)\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=447aaa4f-946b-4f23-b151-dcf46ea9f80e)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=dbaa5a72-c267-4907-a207-525c2803d7b9)\*  
(Importante)
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
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bbac3deb-6c93-45aa-832c-02b915ac7f44)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=67d4c189-030d-42eb-98b9-7957ccd92592)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f33012b9-5d5b-4f72-8d49-a8e1c8bc1337)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e0e3ad56-a363-44ba-af4d-b7f551c88afd)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

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
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-027**](http://technet.microsoft.com/security/bulletin/ms09-027)
</td>
<td style="border:1px solid black;">
[**MS09-021**](http://technet.microsoft.com/security/bulletin/ms09-021)
</td>
<td style="border:1px solid black;">
[**MS09-024**](http://technet.microsoft.com/security/bulletin/ms09-024)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2000 Service Pack 3](http://technet.microsoft.com/security/bulletin/ms09-024)  
(KB969600)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=dd16e243-b8e2-4afb-86b6-4d60214598eb)  
(KB969683)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=4bf95806-3d32-411b-9779-a81aebad45e9)  
(KB957838)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=f1323be1-15f2-491b-abae-c03ba1394398)  
(KB969602)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=dd80ce95-0aec-4493-b9d1-c3dad95c3415)  
(KB969680)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=b0ba8c9e-75ee-46bd-9e92-d4e6599309ad)  
(KB957646)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=7cbc2587-2c8c-49b4-9f40-e4cdccb61ecd)  
(KB969603)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=10156044-a5a4-4312-98a7-1b1ced625ddb)  
(KB969681)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2003 Service Pack 3 con el convertidor de archivos de Microsoft Works 6–9](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=a7ba3ea7-d06a-4c14-9107-9b92ef68fcae)\*\*\*  
(KB968326)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2007 Service Pack 1 y Microsoft Office Word 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=7e205108-4c28-4cab-a4d0-4ed3fd696473)  
(KB969604)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office Excel 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=2bcd565a-6acb-407d-80da-0398526ddf99)\*  
(KB969682)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=bd47e1e5-cd2e-4c08-9864-471e97f38ca3)  
(KB969559)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-027**](http://technet.microsoft.com/security/bulletin/ms09-027)
</td>
<td style="border:1px solid black;">
[**MS09-021**](http://technet.microsoft.com/security/bulletin/ms09-021)
</td>
<td style="border:1px solid black;">
[**MS09-024**](http://technet.microsoft.com/security/bulletin/ms09-024)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5557bfb7-ebb4-4c42-8042-41e830c4e550)  
(KB969661)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=5557bfb7-ebb4-4c42-8042-41e830c4e550)  
(KB969661)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=58326da2-eb75-4b42-b1bc-e70319defb58)  
(KB971822)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=58326da2-eb75-4b42-b1bc-e70319defb58)  
(KB971822)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=9d6d9eaa-8442-4184-8886-faab2803bde6)  
(KB971824)  
(Importante)
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=9d6d9eaa-8442-4184-8886-faab2803bde6)  
(KB971824)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-027**](http://technet.microsoft.com/security/bulletin/ms09-027)
</td>
<td style="border:1px solid black;">
[**MS09-021**](http://technet.microsoft.com/security/bulletin/ms09-021)
</td>
<td style="border:1px solid black;">
[**MS09-024**](http://technet.microsoft.com/security/bulletin/ms09-024)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Excel Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel Viewer 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=20e6933d-85f8-4cec-9534-893789cd053e)  
(KB969685)  
(Importante)  
[Microsoft Office Excel Viewer](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=ac0530dc-7f63-4ad0-85c1-784ad28156cf)  
(KB969686)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Office Word Viewer 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=82980a40-f10c-4f02-b06c-3a12d4434a6b)  
(KB969614)  
(Importante)  
[Microsoft Office Word Viewer](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=82980a40-f10c-4f02-b06c-3a12d4434a6b)  
(KB969614)  
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
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=63bd8f14-e736-46ce-af66-d30f17461e5a)  
(KB969613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=a8be8457-b0b6-455e-907e-d13be883adf2)  
(KB969679)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Works 8.5
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 8.5](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=628280fe-e035-4274-85f2-393d9bad543c)  
(KB967043)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Works 9
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 9](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=f6fa110e-45c6-450f-ae47-c89a06e3f762)  
(KB967044)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 1 y Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=862e6ad1-8124-4060-93b1-2b882ef5ce3d)\*\*  
(KB969737)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 1 y Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=b7b6e611-2c5d-4639-add9-972055789ecd)\*\*  
(KB969737)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para MS09-021**

\*Para Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office PowerPoint 2007 Service Pack 2, además del paquete de actualización de seguridad KB969682, los clientes también deben instalar la actualización de seguridad para [Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=a8be8457-b0b6-455e-907e-d13be883adf2) (KB969679) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

\*\*Esta actualización se aplica a los servidores que tienen instalados Servicios de Excel, como la configuración predeterminada de Microsoft Office SharePoint Server 2007 Enterprise y Microsoft Office SharePoint Server 2007 para sitios de Internet. Microsoft Office SharePoint Server 2007 Standard no incluye Servicios de Excel.

**Nota para MS09-024**

\*\*\*Microsoft Office Word 2003 está afectado si hay instalado un convertidor de Works vulnerable. Los convertidores de Works están disponibles para Microsoft Office Word 2003 como descarga desde [Convertidor de archivos de Microsoft Works 6–9](http://www.microsoft.com/downloads/details.aspx?familyid=bf41401e-70fa-465d-ae2e-cf44dbf05297&displaylang=en).

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/protect/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://update.microsoft.com/windowsupdate/v6/vistadefault.aspx?ln=es-es) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/configurationmanager/default.aspx).

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
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/dd573344.aspx).

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

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://technet.microsoft.com/es-es/security/cc136632.aspx) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Joshua J. Drake, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-018
-   Justin Wyatt, de [Beaverton School District](http://www.beaverton.k12.or.us/home/), por informar de un problema descrito en MS09-018
-   David Bloom, de [Google Inc.](http://www.google.com/), por colaborar con nosotros en un problema descrito en MS09-019
-   Jorge Luis Alvarez Medina, [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS09-019
-   Haifei Li, de [Fortinet](http://www.fortinet.com/), por informar de un problema descrito en MS09-019
-   [Tippingpoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-019
-   Peter Vreugdenhil, en colaboración con [Tippingpoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-019
-   Wushi, en colaboración con [Tippingpoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-019
-   Nils, en colaboración con [Tippingpoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-019
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS09-020
-   Bing Liu, de [FortiGuard Global Security Research Team](http://www.fortiguardcenter.com/) de Fortinet, por informar de tres problemas descritos en MS09-021
-   Carsten H. Eiram, de [Secunia](http://secunia.com/), por informar de dos problemas descritos en MS09-021
-   [TELUS Security Labs Vulnerability Research Team](http://telussecuritylabs.com/), por informar de un problema descrito en MS09-021
-   Sean Larsson y Joshua Drake, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-021
-   [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-021
-   Jun Mao, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-022
-   Yair Amit, de [IBM Rational Application Security](http://blog.watchfire.com/), por informar de un problema descrito en MS09-023
-   Shaun Colley, de [NGS Software](http://www.ngssoftware.com/), por informar de un problema descrito en MS09-024
-   Thomas Garnier, por informar de dos problemas descritos en MS09-025
-   Wushi de [team509](http://www.team509.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-027
-   Nicolas Joly, de [VUPEN Security](http://www.vupen.com/), por informar de un problema descrito en MS09-027

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://www.microsoft.com/spain/protect/support/default.mspx) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de junio de 2009): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
