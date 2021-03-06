---
TOCTitle: 'MS14-NOV'
Title: Resumen de los boletines de seguridad de Microsoft de noviembre de 2014
ms:assetid: 'ms14-nov'
ms:contentKeyID: 63355195
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-nov(v=Security.10)'
---

MSRC. ppDocument Template

Resumen de los boletines de seguridad de Microsoft de noviembre de 2014
=======================================================================

Publicado: 11 de noviembre de 2014 | Actualizado: 18 de diciembre de 2014

**Versión:** 2.1

Este resumen enumera los boletines de seguridad publicados en noviembre de 2014.

Con la publicación de los boletines de seguridad de noviembre de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 6 de noviembre de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/gg309152.aspx).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite las [Notificaciones técnicas de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/dd252948.aspx).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Consulte la sección **Información adicional**.

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Software afectado**.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><strong>Título de boletín y resumen ejecutivo</strong></td>
<td style="border:1px solid black;"><strong>Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</strong></td>
<td style="border:1px solid black;"><strong>Requisito de reinicio</strong></td>
<td style="border:1px solid black;"><strong>Software afectado</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-064">MS14-064</a></td>
<td style="border:1px solid black;"><strong>Unas vulnerabilidades en Windows OLE podrían permitir la ejecución remota de código (3011443)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en la vinculación e incrustación de objetos (OLE) de Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara las vulnerabilidades podría ejecutar código arbitrario en el contexto del usuario actual. Si el usuario actual inicia sesión con derechos de administrador, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Crítico</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-065">MS14-065</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (3003057)<br />
<br />
</strong>Esta actualización de seguridad resuelve diecisiete vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Crítico</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-066">MS14-066</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en SChannel podría permitir la ejecución remota de código (2992611)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad en el paquete de seguridad de canal seguro (SChannel) de Microsoft en Windows de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si un atacante envía paquetes especialmente diseñados a un servidor de Windows.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Crítico</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-067">MS14-067</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en XML Core Services podría permitir la ejecución remota de código (2993958)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario que ha iniciado sesión visita un sitio web especialmente diseñado para invocar Microsoft XML Core Services (MSXML) a través de Internet Explorer. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos a un sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o una solicitud de mensajería instantánea que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Crítico</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-068">MS14-068</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad existente en Kerberos podría permitir la elevación de privilegios (3011780)<br />
</strong><br />
Esta actualización de seguridad soluciona una vulnerabilidad de la que se ha informado en privado del KDC de Microsoft Windows Kerberos que podría permitir que un atacante elevara los privilegios de una cuenta de usuario de dominio sin privilegios a los de la cuenta de administrador del dominio. Un atacante podría utilizar estos privilegios elevados para poner en peligro cualquier equipo del dominio, incluidos los controladores del dominio. Para aprovechar esta vulnerabilidad, el atacante debe tener unas credenciales de dominio válidas. El componente afectado está disponible de forma remota para los usuarios que tienen cuentas de usuario estándar con credenciales de dominio; no es el caso de los usuarios que tienen solo credenciales de cuenta local. Cuando se publicó este boletín de seguridad, Microsoft tenía constancia de ataques dirigidos y limitados que intentan aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Crítico</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-069">MS14-069</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office podrían permitir la ejecución remota de código (3009710)<br />
<br />
</strong>Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una edición afectada de Microsoft Office 2007. Un atacante que aprovechara esta vulnerabilidad podría obtener los mismos derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-070">MS14-070</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en TCP/IP podría permitir la elevación de privilegios (2989935)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad TCP/IP de la que se ha informado públicamente que se produce durante el procesamiento del control de entrada/salida (IOCTL). Esta vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Un atacante que consiguiera aprovechar esta vulnerabilidad podría ejecutar código arbitrario en el contexto de otro proceso. Si este proceso se ejecuta con privilegios de administrador, un atacante podría instalar programas; ver, cambiar o eliminar datos, o crear cuentas nuevas con todos los derechos de usuario.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-071">MS14-071</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio de audio de Windows podría permitir la elevación de privilegios (3005607)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si una aplicación utiliza el servicio de audio de Microsoft Windows. La vulnerabilidad en sí misma no permite la ejecución de código arbitrario. Se debe usar conjuntamente con otra vulnerabilidad que permitiera la ejecución remota de código.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-072">MS14-072</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la elevación de privilegios (3005210)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework. La vulnerabilidad podría permitir la elevación de privilegios si un usuario no autenticado envía datos especialmente diseñados a una estación de trabajo o a un servidor que estén afectados y usen .NET Remoting. Las aplicaciones personalizadas que se han diseñado específicamente para usar .NET Remoting son las únicas que expondrían un sistema a la vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-073">MS14-073</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft SharePoint Foundation podría permitir la elevación de privilegios (3000431)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft SharePoint Server. Un atacante autenticado que consiguiera aprovechar esta vulnerabilidad podría ejecutar script arbitrario en el contexto del usuario en el sitio actual de SharePoint. En un escenario de ataque web, el atacante podría hospedar un sitio web especialmente diseñado para aprovechar estas vulnerabilidades y convencer a un usuario de que visite el sitio web. El atacante también podría aprovechar sitios web vulnerables y sitios web que aceptan o reciben contenido o anuncios proporcionados por el usuario. Estos sitios web podrían incluir contenido malintencionado a través del cual se podrían aprovechar estas vulnerabilidades. No obstante, el atacante no podría en ningún caso obligar a los usuarios a ver el contenido controlado por el atacante. En su lugar, tendría que convencerlos para que realizaran alguna acción, normalmente incitándoles a que hagan clic en un vínculo de un mensaje de correo electrónico o de mensajería instantánea que los lleve al sitio web del atacante o a que abran datos adjuntos enviados por correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-074">MS14-074</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el Protocolo de escritorio remoto podría permitir la omisión de una característica de seguridad (3003743)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la omisión de una característica de seguridad cuando el Protocolo de escritorio remoto (RDP) no registra correctamente los eventos de auditoría. De forma predeterminada, RDP no está habilitado en ningún sistema operativo Windows. Los sistemas que no tienen RDP habilitado no están expuestos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-076">MS14-076</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Internet Information Services (IIS) podría permitir la omisión de una característica de seguridad (2982998)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Internet Information Services (IIS) que podría conducir a la omisión de la característica de seguridad &quot;restricciones de IP y de dominio&quot;. El aprovechamiento de esta vulnerabilidad podría dar lugar a que los clientes de dominios restringidos o bloqueados tengan acceso a recursos web restringidos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-077">MS14-077</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Servicios de federación de Active Directory podría permitir la divulgación de información (3003381)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Servicios de federación de Active Directory (AD FS). La vulnerabilidad podría permitir la revelación de información si un usuario deja el explorador abierto después de cerrar sesión en una aplicación y un atacante vuelve a abrir la aplicación en el explorador inmediatamente después de que el usuario haya cerrado sesión.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Importante</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-078">MS14-078</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad existente en IME (japonés) podría permitir la elevación de privilegios (2992719)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Editor de métodos de entrada (IME) (japonés) de Microsoft. La vulnerabilidad podría permitir la salida del espacio aislado basado en la directiva de espacio aislado de aplicación en un sistema donde esté instalada una versión afectada de Microsoft IME (japonés). Un atacante que aprovechara esta vulnerabilidad podría salir del espacio aislado de una aplicación vulnerable y obtener acceso al sistema afectado con los derechos de un usuario con la sesión iniciada. Si el sistema afectado ha iniciado sesión con derechos administrativos, un atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Moderado</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="https://technet.microsoft.com/es-es/library/security/ms14-079">MS14-079</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores modo kernel podría permitir la denegación de servicio (3002885)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante colocara una fuente TrueType especialmente creada para tal fin en un recurso compartido de red y un usuario posteriormente fuera hasta ahí con el Explorador de Windows. En el caso de un ataque basado en web, el intruso podría hospedar un sitio web que contuviera una página web para aprovechar esta vulnerabilidad. Además, los sitios web vulnerables y los sitios web que aceptan u hospedan contenido o anuncios proporcionados por el usuario podrían incluir contenido especialmente diseñado que permita aprovechar esta vulnerabilidad. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos a un sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de mensajería instantánea que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/gg309177.aspx">Moderado</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
 
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador del boletín y, a continuación, del identificador CVE. Solo se incluyen las vulnerabilidades que tienen un nivel de gravedad Crítico o Importante en los boletines.
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259).
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
**Título de vulnerabilidad**
</td>
<td style="border:1px solid black;">
**Identificador CVE**
</td>
<td style="border:1px solid black;" colspan="2">
**Evaluación de explotabilidad para la última versión de software**
</td>
<td style="border:1px solid black;" colspan="2">
**Evaluación de explotabilidad para la versión de software anterior**
</td>
<td style="border:1px solid black;">
**Evaluación de explotabilidad de denegación de servicio**
</td>
<td style="border:1px solid black;">
**Notas clave**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-064](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de matriz de automatización de Windows OLE
</td>
<td style="border:1px solid black;">
[CVE-2014-6332](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6332)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-064](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código en Windows OLE
</td>
<td style="border:1px solid black;">
[CVE-2014-6352](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6352)
</td>
<td style="border:1px solid black;" colspan="2">
0- Explotación detectada
</td>
<td style="border:1px solid black;" colspan="2">
0- Explotación detectada
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.  
Esta vulnerabilidad se describió por primera vez en el aviso de seguridad de Microsoft [3010060](https://technet.microsoft.com/es-es/library/security/3010060.aspx).
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-4143](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4143)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de divulgación de información de Portapapeles en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6323](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6323)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Esta vulnerabilidad afecta a la divulgación de información.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6337](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6337)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de omisión de ASLR en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6339](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6339)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Es una vulnerabilidad de omisión de característica de seguridad.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de divulgación de información entre dominios en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6340](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6340)
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Esta vulnerabilidad afecta a la divulgación de información.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6341](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6341)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6342](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6342)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6343](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6343)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6344](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6344)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de divulgación de información entre dominios en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6345](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6345)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Esta vulnerabilidad afecta a la divulgación de información.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de divulgación de información entre dominios en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6346](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6346)
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Esta vulnerabilidad afecta a la divulgación de información.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6347](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6347)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
No está afectada
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6348](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6348)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de elevación de privilegios en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6349](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6349)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de elevación de privilegios en Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6350](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6350)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6351](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6351)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-065](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de daños en la memoria de Internet Explorer
</td>
<td style="border:1px solid black;">
[CVE-2014-6353](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6353)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-066](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de Microsoft SChannel
</td>
<td style="border:1px solid black;">
[CVE-2014-6321](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6321)
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
Permanente
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-067](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de MSXML
</td>
<td style="border:1px solid black;">
[CVE-2014-4118](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4118)
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-068](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de suma de comprobación de Kerberos
</td>
<td style="border:1px solid black;" colspan="2">
[CVE-2014-6324](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6324)
</td>
<td style="border:1px solid black;">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
0- Explotación detectada
</td>
<td style="border:1px solid black;" colspan="2">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.  
Microsoft tiene constancia de los ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-069](https://technet.microsoft.com/es-es/library/security/ms14-069)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de doble eliminación de Microsoft Office
</td>
<td style="border:1px solid black;">
[CVE-2014-6333](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6333)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-069](https://technet.microsoft.com/es-es/library/security/ms14-069)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de índice incorrecto de Microsoft Office
</td>
<td style="border:1px solid black;">
[CVE-2014-6334](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6334)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-069](https://technet.microsoft.com/es-es/library/security/ms14-069)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de ejecución remota de código de puntero no válido de Microsoft Office
</td>
<td style="border:1px solid black;">
[CVE-2014-6335](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6335)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
1- Explotación más probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
(Ninguna)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-070](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de elevación de privilegios de TCP/IP
</td>
<td style="border:1px solid black;">
[CVE-2014-4076](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4076)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
Permanente
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-071](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
Vulnerabilidad del servicio de audio de Windows
</td>
<td style="border:1px solid black;">
[CVE-2014-6322](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6322)
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-072](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de TypeFilterLevel
</td>
<td style="border:1px solid black;">
[CVE-2014-4149](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4149)
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-073](https://technet.microsoft.com/es-es/library/security/ms14-073)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de elevación de privilegios de SharePoint
</td>
<td style="border:1px solid black;">
[CVE-2014-4116](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4116)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
2- Explotación menos probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-074](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
Error de Protocolo de escritorio remoto (RDP) para auditar la vulnerabilidad
</td>
<td style="border:1px solid black;">
[CVE-2014-6318](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6318)
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Es una vulnerabilidad de omisión de característica de seguridad.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-076](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de omisión de característica de seguridad en IIS
</td>
<td style="border:1px solid black;">
[CVE-2014-4078](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4078)
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Es una vulnerabilidad de omisión de característica de seguridad.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-077](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de divulgación de información de Servicios de federación de Active Directory
</td>
<td style="border:1px solid black;">
[CVE-2014-6331](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6331)
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Esta vulnerabilidad afecta a la divulgación de información.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-078](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
Vulnerabilidad de elevación de privilegios de IME (japonés) de Microsoft
</td>
<td style="border:1px solid black;">
[CVE-2014-4077](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4077)
</td>
<td style="border:1px solid black;" colspan="2">
No afectado
</td>
<td style="border:1px solid black;" colspan="2">
0- Explotación detectada
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de elevación de privilegios.
</td>
</tr>
<tr>
<td style="border:1px solid black;">
[MS14-079](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
<td style="border:1px solid black;">
Vulnerabilidad en controlador de modo Kernel de Windows de denegación de servicio
</td>
<td style="border:1px solid black;">
[CVE-2014-6317](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6317)
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;" colspan="2">
3- Explotación poco probable
</td>
<td style="border:1px solid black;">
Permanente
</td>
<td style="border:1px solid black;">
Se trata de una vulnerabilidad de denegación de servicio.
</td>
</tr>
</table>
 
 

Software afectado
-----------------

Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.

Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2 
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(3003057)  
(Moderado)  
Internet Explorer 7  
(3003057)  
(Moderado)  
Internet Explorer 8  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(2989935)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2978114)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2978124)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)
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
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2   
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(3003057)  
(Moderado)  
Internet Explorer 7  
(3003057)  
(Moderado)  
Internet Explorer 8  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2989935)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978124)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)
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
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(3003057)  
(Moderado)  
Internet Explorer 7  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2989935)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978124)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)
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
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3006226)  
(Crítico)  
Windows Vista Service Pack 2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(3003057)  
(Crítico)  
Internet Explorer 8  
(3003057)  
(Crítico)  
Internet Explorer 9  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978116)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3006226)  
(Crítico)  
Windows Vista x64 Edition Service Pack 2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(3003057)  
(Crítico)  
Internet Explorer 8  
(3003057)  
(Crítico)  
Internet Explorer 9  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978116)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3006226)  
(Crítico)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(3003057)  
(Moderado)  
Internet Explorer 8  
(3003057)  
(Moderado)  
Internet Explorer 9  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978116)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 2.0  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3006226)  
(Crítico)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(3003057)  
(Moderado)  
Internet Explorer 8  
(3003057)  
(Moderado)  
Internet Explorer 9  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978116)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 2.0  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3006226)  
(Crítico)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2978116)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows 7**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3006226)  
(Crítico)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(3003057)  
(Crítico)  
Internet Explorer 9  
(3003057)  
(Crítico)  
Internet Explorer 10  
(3003057)  
(Crítico)  
Internet Explorer 11  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2978120)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3006226)  
(Crítico)  
Windows 7 para sistemas x64 Service Pack 1  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(3003057)  
(Crítico)  
Internet Explorer 9  
(3003057)  
(Crítico)  
Internet Explorer 10  
(3003057)  
(Crítico)  
Internet Explorer 11  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2978120)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3006226)  
(Crítico)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(3003057)  
(Moderado)  
Internet Explorer 9  
(3003057)  
(Moderado)  
Internet Explorer 10  
(3003057)  
(Moderado)  
Internet Explorer 11  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2978120)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 2.0  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3006226)  
(Crítico)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2978120)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3006226)  
(Crítico)  
Windows 8 para sistemas de 32 bits  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978121)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978127)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.0  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3006226)  
(Crítico)  
Windows 8 para sistemas x64  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978121)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978127)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.0  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3006226)  
(Crítico)  
Windows 8.1 para sistemas de 32 bits  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978122)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978126)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.5  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3006226)  
(Crítico)  
Windows 8.1 para sistemas x64  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3011780)  
(Sin clasificación de gravedad)<sup>[1]</sup>
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978122)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978126)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.5  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(3006226)  
(Crítico)  
Windows Server 2012   
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978121)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978127)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.0  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 2.1  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012   
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3006226)  
(Crítico)  
Windows Server 2012 R2  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(3003057)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978122)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978126)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Internet Information Services 8.5  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 3.0  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Windows RT  
(3006226)  
(Crítico)  
Windows RT  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows RT  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows RT  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978127)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(3003743)  
(Importante)
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
<td style="border:1px solid black;">
Windows RT  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(3006226)  
(Crítico)  
Windows RT 8.1  
(3010788)  
(Importante)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(3003057)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2993958)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(3005607)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5.1/4.5.2  
(2978126)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(3003743)  
(Importante)
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
<td style="border:1px solid black;">
Windows RT 8.1  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="14">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-064**](https://technet.microsoft.com/es-es/library/security/ms14-064)
</td>
<td style="border:1px solid black;">
[**MS14-065**](https://technet.microsoft.com/es-es/library/security/ms14-065)
</td>
<td style="border:1px solid black;">
[**MS14-066**](https://technet.microsoft.com/es-es/library/security/ms14-066)
</td>
<td style="border:1px solid black;">
[**MS14-067**](https://technet.microsoft.com/es-es/library/security/ms14-067)
</td>
<td style="border:1px solid black;">
[**MS14-068**](https://technet.microsoft.com/es-es/library/security/ms14-068)
</td>
<td style="border:1px solid black;">
[**MS14-070**](https://technet.microsoft.com/es-es/library/security/ms14-070)
</td>
<td style="border:1px solid black;">
[**MS14-071**](https://technet.microsoft.com/es-es/library/security/ms14-071)
</td>
<td style="border:1px solid black;">
[**MS14-072**](https://technet.microsoft.com/es-es/library/security/ms14-072)
</td>
<td style="border:1px solid black;">
[**MS14-074**](https://technet.microsoft.com/es-es/library/security/ms14-074)
</td>
<td style="border:1px solid black;">
[**MS14-076**](https://technet.microsoft.com/es-es/library/security/ms14-076)
</td>
<td style="border:1px solid black;">
[**MS14-077**](https://technet.microsoft.com/es-es/library/security/ms14-077)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
<td style="border:1px solid black;">
[**MS14-079**](https://technet.microsoft.com/es-es/library/security/ms14-079)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Crítico**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(3011780)  
(Crítico)
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
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core) (2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core) (2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas basados en x64 Service Pack 2 (instalación Server Core)  
(3011780)  
(Crítico)
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
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas basados en x64 Service Pack 1 (instalación Server Core)  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2978120)  
(Importante)  
Microsoft .NET Framework 4  
(2978125)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978128)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2991963)  
(Moderado)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core) (2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978121)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978127)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core) (3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación de Server Core)  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core) (3002885)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(3006226)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2992611)  
(Crítico)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2993958)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(3011780)  
(Crítico)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2978122)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978126)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(3003743)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación de Server Core)  
(2982998)  
(Importante)
</td>
<td style="border:1px solid black;">
Servicios de federación de Active Directory 3.0  
(3003381)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(3002885)  
(Moderado)
</td>
</tr>
</table>
 
**Nota para MS14-064, MS14-065 y MS14-067**

Windows Technical Preview y Windows Server Technical Preview están afectados. Se anima a los usuarios que ejecutan estos sistemas operativos a que apliquen la actualización, disponible a través de [Windows Update](http://update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es). 

**Notas para MS14-068**

Windows Technical Preview y Windows Server Technical Preview están afectados. Se anima a los usuarios que ejecutan estos sistemas operativos a que apliquen la actualización, disponible a través de [Windows Update](http://update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es). 

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a este sistema operativo porque la vulnerabilidad tratada en este boletín no está presente. Esta actualización ofrece un refuerzo adicional de [defensa en profundidad](https://technet.microsoft.com/es-es/library/security/dn848375.aspx) que no corrigen ninguna vulnerabilidad conocida. 

**Nota para MS14-078**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-069**](https://technet.microsoft.com/es-es/library/security/ms14-069)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
[**Moderado**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Word 2007 Service Pack 3  
(2899527)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 IME (japonés)  
(2889913)  
(Moderado)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Otro software de Microsoft Office**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-069**](https://technet.microsoft.com/es-es/library/security/ms14-069)
</td>
<td style="border:1px solid black;">
[**MS14-078**](https://technet.microsoft.com/es-es/library/security/ms14-078)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
<td style="border:1px solid black;">
**Ninguno**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
Microsoft Word Viewer  
(2899553)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2899526)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS14-078**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-073**](https://technet.microsoft.com/es-es/library/security/ms14-073)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/es-es/security/gg309177.aspx)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 2  
(2889838)  
(Importante)
</td>
</tr>
</table>
 
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Hay disponibles varios recursos para ayudar a los administradores a implementar las actualizaciones de seguridad.

Microsoft Baseline Security Analyzer (MBSA) permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan y las configuraciones de seguridad incorrectas más comunes.

Windows Server Update Services (WSUS), Systems Management Server (SMS) y System Center Configuration Manager ayudan a los administradores a distribuir las actualizaciones de seguridad.

Los componentes del Evaluador de compatibilidad de aplicaciones incluidos con el kit de herramientas de compatibilidad de aplicaciones contribuyen a optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas.

Para obtener información acerca de estas y otras herramientas que hay disponibles, vea [Herramientas de seguridad para profesionales de TI](http://technet.microsoft.com/es-es/security/cc297183).

Agradecimientos
---------------

Microsoft reconoce el esfuerzo de aquellos de la comunidad de seguridad que nos ayudan a proteger a los usuarios mediante una revelación responsable de vulnerabilidades. Consulte [Agradecimientos](https://technet.microsoft.com/es-es/library/security/dn820091.aspx) para obtener más información.

Información adicional
---------------------

### Herramienta de eliminación de software malintencionado de Microsoft Windows

Para la publicación de boletines el segundo martes de cada mes, Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga. No hay disponible ninguna versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows para las publicaciones de boletín de seguridad fuera de ciclo.

### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](https://support.microsoft.com/kb/894199/es): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/es-es/windowsserver/bb332157.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumerados en [Asociados de Microsoft Active Protections Program (MAPP)](http://technet.microsoft.com/es-es/security/dn467918).

### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://technet.microsoft.com/es-es/library/bb466251.aspx) se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/es-es/download/search.aspx?q=security%20update) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave "actualización de seguridad" podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](https://support.microsoft.com/kb/913086/es).

**Comunidad de profesionales de TI de seguridad**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en la [Comunidad de profesionales de TI de seguridad](http://technet.microsoft.com/es-es/security/cc136632.aspx).

### Soporte técnico

El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).

Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/es-es/security/bb980617)

Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master?ln=es)

Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx?ln=es)

### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

### Revisiones

-   V1.0 (11 de noviembre de 2014): publicación del resumen del boletín.
-   V2.0 (18 de noviembre de 2014): Resumen de boletín revisado para documentar la publicación fuera de banda de MS14-068 y, en el caso de MS14-066, para anunciar la nueva oferta de la actualización 2992611 para los sistemas que ejecutan Windows Server 2008 R2 y Windows Server 2012.
-   V2.1 (19 de diciembre de 2014): Resumen del boletín revisado para incluir las instalaciones de Windows 2012 Server Core y Windows 2012 R2 Server Core en la tabla de software afectado para MS14-076.

*Página generada el 19/12/2014 13:20Z-08:00.*
