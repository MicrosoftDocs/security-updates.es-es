---
TOCTitle: 'Capítulo 9: Función de servidor web'
Title: 'Capítulo 9: Función de servidor web'
ms:assetid: 'ae41b3f3-b46f-4818-ae75-3aaf23075b56'
ms:contentKeyID: 20200249
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163131(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 9: Función de servidor web

Actualizado: 27/12/05

##### En esta página

[](#eiaa)[Información general](#eiaa)  
[](#ehaa)[Acceso anónimo y configuración de SSLF](#ehaa)  
[](#egaa)[Configuración de directiva de auditoría](#egaa)  
[](#efaa)[Asignaciones de derechos de usuario](#efaa)  
[](#eeaa)[Opciones de seguridad](#eeaa)  
[](#edaa)[Configuración del registro de eventos](#edaa)  
[](#ecaa)[Configuración de seguridad adicional](#ecaa)  
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)  
[](#eaaa)[Resumen](#eaaa)

### Información general

Este capítulo proporciona orientación que le ayudará a consolidar los servidores web de su entorno en los que se ejecute Microsoft® Windows Server™ 2003 con SP1. Con el fin de proporcionar una seguridad completa para los servidores y aplicaciones web de una organización, Microsoft recomienda proteger todos los servidores de Servicios de Internet Information Server (IIS) de Microsoft, así como los sitios web y las aplicaciones que se ejecutan en esos servidores desde los equipos cliente que pueden conectarse a ellos. También debe proteger estos sitios web y las aplicaciones que se ejecutan en otros servidores IIS de la organización de la intranet.

Como medida para protegerse contra atacantes y usuarios malintencionados, en la configuración predeterminada para miembros de la familia de Windows Server 2003 no se instala IIS. Cuando se instala, IIS se configura en un modo sumamente seguro y "bloqueado". Por ejemplo, en su estado predeterminado, IIS sólo sirve contenido estático. Dado que podrían ser aprovechadas por posibles intrusos, hay características como las páginas Active Server (ASP), la ASP.NET, Inclusión del servidor (SSI), WebDAV (Web Distributed Authoring and Versioning) y extensiones de servidor de Microsoft FrontPage® que no funcionarán hasta que un administrador las habilite. Estas características y servicios se pueden habilitar a través del nodo Extensiones del servicio web del Administrador de servicios de Internet Information Server (Administrador IIS). Administrador IIS presenta una interfaz gráfica de usuario (GUI) diseñada para facilitar la administración de IIS. Contiene recursos para la administración de archivos y directorios, la configuración de grupos de aplicaciones, así como características de seguridad, rendimiento y confiabilidad.

Debe considerar la implementación de la configuración que se describe en las secciones siguientes de este capítulo para mejorar la seguridad de los servidores web IIS que alojan contenido HTML dentro de la intranet de su organización. Como medida para proteger sus servidores, también debe implementar procedimientos de supervisión de seguridad, detección y respuesta frente a nuevas amenazas.

La mayor parte de los parámetros que se describen en este capítulo se configuran y aplican mediante Directiva de grupo. Un GPO incremental que complementa MSBP se vincula a las unidades organizativas apropiadas y proporciona seguridad adicional para los servidores web. A fin de aumentar la funcionalidad de este capítulo, sólo se tratan las configuraciones de directiva diferentes de MSBP.

Siempre que sea posible, estas configuraciones se reunirán en una plantilla incremental de Directiva de grupo que se aplicará a la unidad organizativa de servidores web. Parte de los ajustes que se muestran en este capítulo no se pueden aplicar mediante Directiva de grupo. Se proporciona información detallada acerca de cómo configurar estos ajustes manualmente.

En la siguiente tabla se muestran los nombres de las plantillas de seguridad de servidor web para los tres entornos que se definen en esta guía. Estas plantillas de seguridad de servidor web proporcionan las configuraciones de directiva para la plantilla incremental de servidores web. Puede utilizar esta plantilla para crear un nuevo GPO vinculado a la unidad organizativa Servidores web en el entorno apropiado. El capítulo 2, "Mecanismos de seguridad de Windows Server 2003" proporciona instrucciones paso a paso para ayudarle a crear las unidades organizativas y las directivas de grupo y después importar la plantilla de seguridad apropiada en cada GPO.

**Tabla 9.1 Plantillas de seguridad de servidor IIS**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente heredado</th>
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Seguridad especializada: Funcionalidad limitada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">LC-Web Server.inf</td>
<td style="border:1px solid black;">EC-Web Server.inf</td>
<td style="border:1px solid black;">SSLF-Web Server.inf</td>
</tr>
</tbody>
</table>
  
Para obtener información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
En esta guía se ilustra cómo proteger IIS con las características mínimas instaladas y habilitadas. Si planea utilizar características adicionales de IIS quizá deba ajustar algunos de los parámetros de seguridad. Si instala servicios adicionales, tales como SMTP, FTP o NNTP, tendrá que ajustar las plantillas y las directivas proporcionadas.
  
En el artículo en línea "[IIS y cuentas integradas (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx)" en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/  
3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx se explica qué cuentas se usan con las distintas características de IIS, así como los privilegios necesarios en cada caso. Para implementar parámetros de configuración más seguros en servidores web en los que se alojan aplicaciones complejas, puede repasar la [documentación de IIS 6.0](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/848968f3-baa0-46f9-b1e6-ef81dd09b015.mspx) en http://www.microsoft.com/technet/prodtechnol/WindowsServer2003/  
Library/IIS/848968f3-baa0-46f9-b1e6-ef81dd09b015.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Acceso anónimo y configuración de SSLF
  
Cuatro de los derechos de usuario que se definen explícitamente para el entorno SSLF en MSBP están diseñados para impedir el acceso anónimo a sitios web IIS. Sin embargo, si necesita permitir el acceso anónimo en un entorno de SSLF tendrá que hacer algunos cambios importantes en la estructura de unidades organizativas y GPO que se describe en los capítulos 2, 3 y 4 de esta guía. Deberá crear una unidad organizativa nueva que no forme parte de la jerarquía bajo la unidad organizativa de servidores miembro. Esta unidad organizativa podría vincularse directamente a la raíz de dominio, o bien ser una unidad organizativa secundaria de alguna otra jerarquía de unidades organizativas. Sin embargo, no debe asignar derechos de usuario en un GPO que afecte a los servidores IIS que se vayan a colocar en esta nueva unidad organizativa. Puede mover los servidores IIS a la nueva unidad organizativa, crear un GPO, aplicarle la configuración de MSBP y reconfigurar la asignación de derechos de usuario para que puedan controlarse por directiva local y no por GPO basado en dominio. Es decir, debe establecer la siguiente configuración de derechos de usuario como **No está definido** en este nuevo GPO.
  
-   Tener acceso a este equipo desde la red
  
-   Permitir el inicio de sesión local
  
-   Omitir la comprobación de recorrido
  
-   Iniciar sesión como proceso por lotes
  
Las características de IIS que necesita habilitar determinarán si también tendrá que reconfigurar otros parámetros de asignación de derechos de usuario con el valor **No está definido**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
La configuración de directiva de auditoría para los servidores IIS en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca del MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que toda la información de auditoría de seguridad pertinente se registre en todos los servidores IIS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Asignaciones de derechos de usuario
  
La configuración de asignaciones de derechos de usuario para los servidores IIS en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca del MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que toda la información de auditoría de seguridad pertinente se registre en todos los servidores IIS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
La configuración de opciones de seguridad para los servidores IIS en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que las opciones de seguridad pertinentes se configuren de manera uniforme en todos los servidores IIS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
La configuración del registro de eventos para los servidores IIS en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que en todos los servidores IIS de una organización se establecen los parámetros adecuados del registro de eventos de forma uniforme.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
Cuando IIS se instala en un equipo en el que se ejecuta Windows Server 2003 con SP1, su configuración predeterminada sólo permite la transmisión de contenido web estático. Cuando los sitios y aplicaciones web incluyen contenido dinámico o requieren uno o varios componentes de IIS adicionales, se deberán habilitar de forma individual características adicionales de IIS. Sin embargo, deberá tener cuidado para reducir al mínimo la superficie de ataque de los servidores IIS de su entorno. Si los sitios web de su organización sólo incluyen contenido estático y no requieren otros componentes de IIS, la configuración predeterminada bastará para reducir al mínimo la superficie de ataque de los servidores IIS.
  
La configuración de seguridad que se aplica mediante MSBP proporciona un nivel alto de protección para los servidores IIS. Sin embargo, hay algunos parámetros de configuración adicionales que deben tenerse en cuenta. Los parámetros de configuración de las siguientes secciones no se pueden implementar a través de Directiva de grupo y por lo tanto deben establecerse manualmente en todos los servidores IIS.
  
#### Instalación únicamente de los componentes de IIS necesarios
  
IIS 6.0 incluye otros componentes y servicios además del Servicio de publicación de World Wide Web; por ejemplo, los servicios que se requieren para FTP, NNTP y SMTP. Estos componentes y servicios se instalan y habilitan mediante el Asistente para componentes de Windows, que se puede iniciar a través de Agregar o quitar programas en el Panel de control. Después de instalar IIS, deberá habilitar todos los servicios y componentes de IIS que requieren sus aplicaciones y sitios web.
  
**Para instalar Servicios de Internet Information Server (IIS) 6.0**
  
1.  En el Panel de control, haga doble clic en **Agregar o quitar programas.**
  
2.  Haga clic en el botón **Agregar o quitar componentes de Windows** para iniciar el Asistente para componentes de Windows.
  
3.  En la lista **Componentes**, haga clic en **Servidor de aplicaciones** y después en **Detalles.**
  
4.  En el cuadro de diálogo **Servidor de aplicaciones**, bajo **Subcomponentes del servidor de aplicaciones**, haga clic en **Servicios de Internet Information Server (IIS)** y después en **Detalles**.
  
5.  En el cuadro de diálogo **Servicios de Internet Information Server (IIS**), en la lista **Subcomponentes de Servicios de Internet Information Server (IIS)** realice alguna de las siguientes operaciones:
  
    -   Para agregar componentes opcionales, active la casilla de verificación situada junto al componente que desee instalar.
  
    -   Para quitar componentes opcionales, desactive la casilla de verificación situada junto al componente que desee quitar.
  
6.  Haga clic en **Aceptar** hasta que regrese al Asistente para componentes de Windows.
  
7.  Haga clic en **Siguiente** y, a continuación, en **Finalizar**.
  
Sólo debe habilitar los componentes y servicios esenciales de IIS que requieran las aplicaciones y los sitios web. Si habilita componentes y servicios innecesarios, la superficie del servidor IIS susceptible a ataques se incrementará. En las siguientes tablas e ilustraciones se muestran la ubicación y la configuración sugerida para los componentes de IIS.
  
Los subcomponentes del cuadro de diálogo **Servidor de aplicaciones** se muestran en la figura siguiente:
  
[![](images/Cc163131.sgfg0901(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163131.sgfg0901_big(es-es,technet.10).gif)  
**Figura 9.1 Cuadro de diálogo Servidor de aplicaciones con lista de subcomponentes**
  
En la siguiente tabla se describen brevemente los subcomponentes del servidor de aplicaciones y se ofrecen recomendaciones para saber cuándo habilitarlos.
  
**Tabla 9.2 Configuración recomendada de subcomponentes del servidor de aplicaciones**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del componente en la IU</th>
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Lógica de la configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Consola del servidor de aplicaciones</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona un complemento de Microsoft Management Console (MMC) que se puede usar para administrar todos los componentes de servidor de aplicaciones web. Este componente no es necesario en un servidor IIS dedicado, ya que se puede utilizar el Administrador del servidor IIS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ASP.NET</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Ofrece compatibilidad para las aplicaciones ASP.NET. Habilite este componente cuando un servidor IIS ejecute aplicaciones ASP.NET.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitar el acceso de red COM+</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Permite que un servidor IIS albergue los componentes COM+ para las aplicaciones distribuidas. Es necesario para FTP, extensión de servidor de BITS, servicio World Wide Web y Administrador de IIS, entre otros.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Habilitar el acceso DTC de red</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Permite que un servidor IIS albergue las aplicaciones que participan en las transacciones de red a través del Coordinador de transacciones distribuidas (DTC). Deshabilite este componente a menos que lo requieran las aplicaciones que se ejecutan en el servidor IIS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicios de Internet Information Server (IIS)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Ofrece servicios web y FTP básicos. Este componente es necesario para los servidores IIS dedicados.

<strong>Nota</strong>: si no está habilitado este componente, se deshabilitan todos los subcomponentes.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicios de Message Queue Server</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Microsoft Message Queue Server (MSMQ) proporciona una capa de software intermedio de enrutamiento de mensajes, almacenamiento y reenvío para aplicaciones web de empresa.</td>
</tr>
</tbody>
</table>
  
Los subcomponentes del cuadro de diálogo **Servicios de Internet Information Server (IIS)** se muestran en la figura siguiente:
  
[![](images/Cc163131.sgfg0902(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163131.sgfg0902_big(es-es,technet.10).gif)  
**Figura 9.2 Cuadro de diálogo de IIS con lista de subcomponentes**
  
En la siguiente tabla se describen brevemente los subcomponentes de IIS y se ofrecen recomendaciones para saber cuándo habilitarlos.
  
**Tabla 9.3 Configuración recomendada para subcomponentes de IIS**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del componente en la IU</th>
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Lógica de la configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Extensión de servidor de Servicio de transferencia inteligente en segundo plano (BITS)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">La extensión de servidor BITS permite que el servicio BITS de los equipos cliente cargue en segundo plano archivos en este servidor. Si tiene una aplicación en los equipos cliente que utiliza el servicio BITS para cargar archivos en este servidor, habilite y configure la extensión de servidor BITS; si no es así, déjela deshabilitada. Observe que Windows Update, Microsoft Update, SUS, WSUS y Actualizaciones automáticas no requieren este componente para ejecutarse. Requieren el componente cliente BITS, que no forma parte de IIS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Archivos comunes</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">IIS requiere que estos archivos siempre estén habilitados en los servidores IIS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio del Protocolo de transferencia de archivos (FTP)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Permite a los servidores IIS suministrar los servicios FTP. Este servicio no es necesario para los servidores IIS dedicados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Extensiones de servidor de FrontPage 2002</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona compatibilidad con FrontPage para administrar y publicar sitios web. Deshabilite esta opción en los servidores IIS dedicados cuando ningún sitio web utilice las extensiones de FrontPage.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de servicios de Internet Information Server</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Interfaz administrativa para IIS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Impresión de Internet</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona una administración de impresión basada en Web y permite que las impresoras se compartan en HTTP. Este componente no es necesario en los servidores IIS dedicados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio NNTP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Distribuye, consulta, recupera y publica artículos de noticias Usenet en Internet. Este componente no es necesario en los servidores IIS dedicados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio SMTP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Admite la transferencia de correo electrónico. Este componente no es necesario en los servidores IIS dedicados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio World Wide Web</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Ofrece servicios web y contenido estático y dinámico a los clientes. Este componente es necesario en los servidores IIS dedicados.</td>
</tr>
</tbody>
</table>
  
Los subcomponentes del cuadro de diálogo **Servicios de Message Queue Server** se muestran en la figura siguiente:
  
[![](images/Cc163131.sgfg0903(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163131.sgfg0903_big(es-es,technet.10).gif)  
**Figura 9.3 Cuadro de diálogo Servicios de Message Queue Server con lista de subcomponentes**
  
En la siguiente tabla se describen brevemente los subcomponentes de Message Queue Server y se ofrecen recomendaciones para saber cuándo habilitarlos.
  
**Tabla 9.4 Configuración recomendada para subcomponentes de Message Queue Server**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del componente en la IU</th>
<th style="border:1px solid black;" >Opción de instalación</th>
<th style="border:1px solid black;" >Lógica de la configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Integración en Active Directory</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona integración con el servicio de directorio Active<em> </em>Directory® cuando un servidor IIS pertenece a un dominio. Este componente es necesario cuando los sitios y aplicaciones web que se ejecutan en los servidores IIS utilizan Microsoft Message Queue Server (MSMQ).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Común</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Este componente es necesario cuando los sitios y aplicaciones web que se ejecutan en los servidores IIS utilizan MSMQ.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compatibilidad con clientes de nivel inferior</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona acceso a Active<em> </em>Directory y reconocimiento de clientes indirectos. Este componente es necesario cuando los sitios y aplicaciones web de un servidor IIS utilizan MSMQ.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compatibilidad con HTTP en MSMQ</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona la posibilidad de enviar y recibir mensajes a través del transporte HTTP. Este componente es necesario cuando los sitios y aplicaciones web de un servidor IIS utilizan MSMQ.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compatibilidad de enrutamiento</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona mensajería de almacenamiento y reenvío, así como servicios de enrutamiento eficientes para MSMQ. Este componente es necesario cuando los sitios y aplicaciones web que se ejecutan en los servidores IIS utilizan MSMQ.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desencadenadores</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Se asocia la llegada de mensajes entrantes a una cola con la funcionalidad en un componente COM o un programa ejecutable independiente.</td>
</tr>
</tbody>
</table>
  
En la siguiente figura se muestran los subcomponentes del cuadro de diálogo **Extensiones de servidor de Servicio de transferencia inteligente en segundo plano (BITS)**:
  
[![](images/Cc163131.sgfg0904(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163131.sgfg0904_big(es-es,technet.10).gif)  
**Figura 9.4 Extensiones de servidor BITS con lista de subcomponentes**
  
En la siguiente tabla se describen brevemente los subcomponentes de Extensiones del servidor BITS y se ofrecen recomendaciones para saber cuándo habilitarlos.
  
**Tabla 9.5 Configuración recomendada de subcomponentes de Extensiones de servidor BITS**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del componente en la IU</th>
<th style="border:1px solid black;" >Opción de instalación</th>
<th style="border:1px solid black;" >Lógica de la configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Complemento de la consola de administración de BITS</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Instala un complemento de MMC para administrar el servicio BITS. Habilite este componente cuando la extensión de servidor de BITS para la Interfaz de programación de aplicaciones de servidores de Internet (ISAPI) esté habilitada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ISAPI de extensión de servidor de BITS</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Instala la ISAPI de BITS de manera que un servidor IIS pueda transferir datos mediante BITS. Las extensiones de servidor BITS permiten que el servicio BITS de los equipos cliente carguen en segundo plano archivos en este servidor. Si tiene una aplicación en los equipos cliente que utiliza el servicio BITS para cargar archivos en este servidor, habilite y configure la extensión de servidor BITS; si no es así, déjela deshabilitada. Observe que Windows Update, Microsoft Update, SUS, WSUS y Actualizaciones automáticas no requieren este componente para ejecutarse. Requieren el componente cliente BITS, que no forma parte de IIS.</td>
</tr>
</tbody>
</table>
  
Los subcomponentes del cuadro de diálogo **Servicio World Wide Web** se muestran en la figura siguiente:
  
[![](images/Cc163131.SGFG0905(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163131.sgfg0905_big(es-es,technet.10).gif)  
**Figura 9.5 Cuadro de diálogo Servicio World Wide Web con lista de subcomponentes**
  
En la tabla siguiente se describen brevemente los subcomponentes del Servicio World Wide Web y se ofrecen recomendaciones para saber cuándo habilitarlos.
  
**Tabla 9.6 Configuración recomendada de subcomponentes del Servicio World Wide Web**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del componente en la IU</th>
<th style="border:1px solid black;" >Opción de instalación</th>
<th style="border:1px solid black;" >Lógica de la configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Páginas de Active Server</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Ofrece compatibilidad para ASP. Deshabilite este componente si ninguno de los sitios ni aplicaciones web de los servidores IIS utiliza ASP. También puede deshabilitarlo mediante las extensiones del servicio web. Para obtener más información, consulte la sección “Habilitación únicamente de las extensiones de servicios web esenciales” de este capítulo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conector de datos de Internet</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Ofrece compatibilidad para el contenido dinámico que se proporciona a través de los archivos con extensiones .idc. Deshabilite este componente si ninguno de los sitios ni aplicaciones web que se ejecutan en los servidores IIS incluye archivos con extensiones .idc. También puede deshabilitarlo mediante las extensiones del servicio web. Para obtener más información, consulte la sección “Habilitación únicamente de las extensiones de servicios web esenciales” de este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administración remota (HTML)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Proporciona una interfaz HTML para administrar IIS. Utilice el Administrador de IIS para facilitar la administración y reducir la superficie de ataque de un servidor IIS. Esta función no es necesaria en los servidores IIS dedicados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conexión web a escritorio remoto</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Incluye el control ActiveX® de Microsoft y páginas de muestra para alojar conexiones de cliente de Servicios de Terminal Server. Utilice el Administrador de IIS para facilitar la administración y reducir la superficie de ataque de un servidor IIS. No es necesario en un servidor IIS dedicado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inclusión del servidor</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Ofrece compatibilidad para los archivos .shtm, .shtml y .stm. Deshabilite este componente si ninguno de los sitios ni aplicaciones web que se ejecutan en un servidor IIS incluye archivos con dichas extensiones.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WebDAV</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">WebDAV amplía el protocolo HTTP/1.1 para permitir a los clientes publicar, bloquear y administrar recursos en la Web. Deshabilite este componente en los servidores IIS dedicados. También puede deshabilitarlo mediante las extensiones del servicio web. Para obtener más información, consulte la sección “Habilitación únicamente de las extensiones de servicios web esenciales” de este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio World Wide Web</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Ofrece servicios web y contenido estático y dinámico a los clientes. Este componente es necesario en los servidores IIS dedicados.</td>
</tr>
</tbody>
</table>
  
#### Habilitación únicamente de las extensiones de servicios web esenciales
  
Un gran número de sitios y aplicaciones web que se ejecutan en servidores IIS incluyen funcionalidad extendida que, además de páginas estáticas, permite generar contenido dinámico. Cualquier contenido dinámico que se sirve o se extiende mediante las características que proporciona un servidor IIS se canaliza a través de extensiones de servicio web.
  
Las características de seguridad mejorada de IIS 6.0 permiten habilitar o deshabilitar extensiones de servicios web individuales. Como se ha indicado anteriormente, los servidores IIS transmitirán únicamente contenido estático tras una nueva instalación. Las capacidades de contenido dinámico se pueden habilitar a través del nodo de extensiones de servicios web en el Administrador IIS. Entre las extensiones se incluyen ASP.NET, SSI, WebDAV y extensiones de servidor FrontPage.
  
Una forma de asegurar la máxima compatibilidad posible con aplicaciones existentes consiste en habilitar todas las extensiones de servicio web, aunque el uso de este método también implica un riesgo para la seguridad porque aumenta la superficie de IIS susceptible de ser atacada. Sólo debe habilitar las extensiones de servicio web requeridas por las aplicaciones y sitios web que se ejecutan en servidores IIS en su entorno. De ese modo se reducirá al mínimo la funcionalidad del servidor y se reducirá la superficie de ataque de los servidores IIS.
  
Para reducir al mínimo la superficie de ataque de los servidores IIS, únicamente se deberán habilitar las extensiones de servicios web que resulten necesarias en los tres entornos que se definen en esta guía.
  
En la tabla siguiente se enumeran las extensiones de servicio web predefinidas y se proporcionan detalles sobre cuándo habilitar cada extensión.
  
**Tabla 9.7 Habilitación de extensiones de servicio web**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Extensión de servicio web</th>
<th style="border:1px solid black;" >Habilitar la extensión cuando</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Páginas de Active Server</td>
<td style="border:1px solid black;">Uno o varios de los sitios y aplicaciones web que se ejecutan en los servidores IIS tienen contenido ASP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ASP.NET v1.1.4322</td>
<td style="border:1px solid black;">Uno o varios de los sitios y aplicaciones web que se ejecutan en los servidores IIS tienen contenido ASP.NET.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Todas las extensiones CGI desconocidas</td>
<td style="border:1px solid black;">Uno o varios de los sitios y aplicaciones web que se ejecutan en los servidores IIS tienen contenido de extensiones CGI desconocidas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Todas las extensiones ISAPI desconocidas</td>
<td style="border:1px solid black;">Uno o varios de los sitios y aplicaciones web que se ejecutan en los servidores IIS tienen contenido de extensiones ISAPI desconocidas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Extensiones de servidor de FrontPage 2002</td>
<td style="border:1px solid black;">Uno o varios de los sitios web que se ejecutan en servidores IIS utilizan Extensiones de FrontPage.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conector de datos de Internet (IDC)</td>
<td style="border:1px solid black;">Uno o varios de los sitios y aplicaciones web que se ejecutan en los servidores IIS utilizan IDC para mostrar la información de la base de datos (este contenido incluye archivos .idc e .idx).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inclusión del servidor (SSI)</td>
<td style="border:1px solid black;">Uno o varios de los sitios web que se ejecutan en los servidores IIS utilizan las directrices SSI con el fin de instruir a los servidores IIS para que inserten contenido reutilizable (por ejemplo, una barra de exploración, un encabezado o pie de página, etc.) en diferentes páginas web.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WebDav (Web Distributed Authoring and Versioning)</td>
<td style="border:1px solid black;">Se requiere compatibilidad con WebDAV en los servidores IIS para que los clientes publiquen y administren con transparencia los recursos web.</td>
</tr>
</tbody>
</table>
  
#### Colocación de contenido en un volumen de disco dedicado
  
IIS almacena los archivos de su sitio web predeterminado en ***&lt;systemroot&gt;*\\inetpub\\wwwroot**, donde *&lt;systemroot&gt;* es la unidad en la que está instalado el sistema operativo Windows Server 2003.
  
En los tres entornos que se definen en esta guía, todos los archivos y carpetas que componen sitios web y aplicaciones se colocan en volúmenes de disco dedicados independientes del sistema operativo. Este enfoque ayuda a evitar los ataques transversales de directorio en los que un atacante envía solicitudes para un archivo ubicado fuera de la estructura de directorios de un servidor IIS.
  
Por ejemplo, el archivo Cmd.exe se encuentra en la carpeta ***&lt;systemroot&gt;*\\System32.** Un atacante podría realizar una solicitud a la siguiente ubicación:
  
..\\..\\Windows\\system\\cmd.exe
  
en un intento de invocar el símbolo del sistema.
  
Si el contenido del sitio web se encuentra en un volumen de disco independiente, este tipo de ataque no podría llevarse a cabo por dos motivos. En primer lugar, los permisos para cmd.exe se han restablecido como parte del núcleo de *Windows Server 2003* con SP1, de modo que el acceso se restringe a un grupo de usuarios mucho más reducido. En segundo lugar, el archivo Cmd.exe no se encontraría en el mismo volumen de disco que la raíz web y actualmente no se conoce ningún método para tener acceso a los comandos de una unidad diferente mediante este tipo de ataque.
  
Además de las ventajas relacionadas con la seguridad, las tareas de la administración tales como la copia de seguridad y la restauración resultan más fáciles cuando las carpetas y los archivos de las aplicaciones y los sitios web se colocan en un volumen de disco dedicado. Asimismo, el uso de una unidad física dedicada independiente puede ayudar a reducir los conflictos de disco en el volumen del sistema y mejorar el rendimiento general de acceso al disco.
  
#### Configuración de permisos de NTFS
  
Los equipos en los que se ejecuta Windows Server 2003 examinan los permisos del sistema de archivos NTFS a fin de determinar los tipos de acceso de los que dispone un usuario o un proceso a un archivo o carpeta específicos. Debe asignar permisos de NTFS para permitir o denegar el acceso a usuarios específicos a sitios web de servidores IIS en los tres entornos que se definen en esta guía.
  
Los permisos de NTFS afectan sólo a las cuentas en las que se ha permitido o denegado acceso al contenido de sitios y aplicaciones web. Debe utilizar los permisos de NTFS junto con los permisos web, no en lugar de éstos. Los permisos del sitio web afectan a todos los usuarios que tienen acceso al sitio o aplicación web. Si se produce un conflicto entre los permisos web y los de NTFS para un directorio o archivo, se aplicará la configuración más restrictiva.
  
Debe denegar explícitamente el acceso a cuentas anónimas en aplicaciones y sitios web para los que no se desea un acceso anónimo. En los accesos anónimos, un usuario que no dispone de credenciales autenticadas obtiene acceso a los recursos de red. Entre las cuentas anónimas se incluyen la cuenta integrada **Invitado**, el grupo Invitados y las cuentas IIS anónimo. Elimine también cualquier permiso de acceso de escritura para todos los usuarios menos los que sean administradores de IIS.
  
En la siguiente tabla se ofrecen algunas recomendaciones acerca de los permisos de NTFS que se deben aplicar a los diferentes tipos de archivos de un servidor IIS. Estos archivos se pueden agrupar en carpetas independientes con el fin de simplificar la aplicación de permisos de NTFS.
  
**Tabla 9.8 Configuración recomendada de permisos de NTFS**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de archivo</th>
<th style="border:1px solid black;" >Permisos de NTFS recomendados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Archivos CGI (.exe, .dll, .cmd, .pl)</td>
<td style="border:1px solid black;">Todos (ejecutar)
Administradores (control total)
Sistema (control total)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Archivos de secuencia de comandos (.asp)</td>
<td style="border:1px solid black;">Todos (ejecutar)
Administradores (control total)
Sistema (control total)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Archivos de inclusión (.inc, .shtm, .shtml)</td>
<td style="border:1px solid black;">Todos (ejecutar)
Administradores (control total)
Sistema (control total)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Contenido estático (.txt, .gif, .jpg, .htm, .html)</td>
<td style="border:1px solid black;">Todos (sólo lectura)
Administradores (control total)
Sistema (control total)</td>
</tr>
</tbody>
</table>
 

#### Configuración de permisos del sitio web de IIS

IIS examina los permisos del sitio web para determinar los tipos de acciones que se pueden realizar en el mismo; por ejemplo, el acceso al código fuente de las secuencias de comandos o la exploración de directorios. Debe asignar permisos de sitio web con objeto de proporcionar seguridad adicional para sitios web en los servidores IIS en los tres entornos que se definen en esta guía.

Los permisos de sitio web se pueden utilizar junto con permisos de NTFS configurarse para sitios específicos, directorios y archivos. A diferencia de los permisos de NTFS, los del sitio web afectan a todos los usuarios que intentan tener acceso a un sitio web que se ejecuta en un servidor IIS. Se pueden aplicar mediante el complemento de MMC Administrador IIS.

En la tabla siguiente se enumeran los permisos de sitio web que admite IIS 6.0 y se ofrecen breves explicaciones acerca de cuándo asignar un determinado permiso a un sitio web.

**Tabla 9.9 Permisos de sitio web de IIS 6.0**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Permiso de sitio web</th>
<th style="border:1px solid black;" >Permiso otorgado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Leer</td>
<td style="border:1px solid black;">Los usuarios pueden ver el contenido y las propiedades de los directorios o archivos. Este permiso está seleccionado de forma predeterminada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Escritura</td>
<td style="border:1px solid black;">Los usuarios pueden modificar el contenido y las propiedades de los directorios o archivos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso al código fuente de secuencias de comandos</td>
<td style="border:1px solid black;">Los usuarios pueden tener acceso a los archivos de origen. Si está habilitado el permiso de lectura, se podrá leer el código fuente de secuencias de comandos; si está habilitado el permiso de escritura, se podrá modificar dicho código. Este tipo de acceso incluye el código fuente para las secuencias de comandos. Si no están habilitados los permisos de lectura y escritura, esta opción no estará disponible.
<strong>Importante</strong>: cuando está habilitado el acceso al código fuente de secuencias de comandos, los usuarios pueden ver información relevante como, por ejemplo, el nombre de usuario y la contraseña. También pueden modificar el código fuente que se ejecuta en un servidor IIS, con lo que la seguridad y el rendimiento del servidor pueden verse gravemente afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Examen de directorios</td>
<td style="border:1px solid black;">Los usuarios puede ver listas y colecciones de archivos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registrar visitas</td>
<td style="border:1px solid black;">Por cada visita al sitio web se crea una entrada de registro.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Indizar este recurso</td>
<td style="border:1px solid black;">Permite que el <strong>Servicio de Index Server</strong> indice los recursos, de modo que se puedan realizar búsquedas de recursos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ejecución</td>
<td style="border:1px solid black;">Las opciones siguientes permiten determinar el nivel de ejecución de secuencias de comandos para los usuarios:
<ul>
<li><strong>Ninguno</strong>. No permite que se ejecuten secuencias de comandos en el servidor.</li>
<li><strong>Sólo secuencias de comandos</strong>. Permite que sólo se ejecuten secuencias de comandos en el servidor.</li>
<li><strong>Secuencias de comandos y ejecutables</strong>. Permite ejecutar secuencias de comandos y archivos ejecutables en el servidor.</li>
</ul></td>
</tr>
</tbody>
</table>
 

#### Configuración del registro IIS

Microsoft recomienda que se habilite el registro IIS en servidores IIS en los tres entornos que se definen en esta guía.

Se pueden crear registros independientes para cada sitio o aplicación web. IIS registra más información que los registros de eventos y las características de supervisión de rendimiento que proporciona el sistema operativo Windows. Los registros IIS pueden contener información sobre qué usuario ha visitado un sitio web, las páginas que ha consultado y cuándo fue la última vez que se visualizó la información. Los registros IIS se pueden utilizar para evaluar la frecuencia con la que se consulta el contenido o identificar cuellos de botella en la información, o bien, a modo de recursos, para ayudar a investigar ataques.

Se puede utilizar el complemento Administrador IIS de MMC para configurar el formato del archivo de registro, la programación de registro y la información exacta que se registrará. Para limitar el tamaño de los registros, debe seguir un proceso de diseño cuidadoso para determinar qué campos se deben registrar.

Cuando se habilita el registro IIS, éste utilizará el formato de archivo de registro extendido W3C para crear los registros de actividades diarias que se almacenan en el directorio especificado para el sitio web en Administrador IIS. Para mejorar el rendimiento del servidor, los registros se deben almacenar en un volumen de disco seccionado o seccionado/reflejado que no sea del sistema.

Los registros también se pueden escribir en un recurso compartido remoto de una red mediante una ruta completa de convención de nomenclatura universal (UNC). El registro remoto permite a los administradores configurar el almacenamiento y la copia de seguridad centralizados de los archivos de registro. Sin embargo, el rendimiento del servidor se podría ver afectado negativamente cuando los archivos de registro se escriben a través de la red.

El registro IIS se puede configurar para que utilice otros formatos de archivo de registro ASCII u Open Database Connectivity (ODBC). Los registros ODBC pueden almacenar información de actividad en una base de datos SQL. Sin embargo, tenga en cuenta que cuando está habilitado el registro ODBC, IIS deshabilita la caché del modo de núcleo, lo que puede afectar al rendimiento global del servidor.

Los servidores IIS que alojan centenares de sitios pueden habilitar un registro binario centralizado para mejorar el rendimiento de las operaciones de registro. Este tipo de registro permite que todos los sitios web de un servidor IIS escriban información de actividades en un único archivo de registro. Con este método es posible incrementar en gran medida la capacidad de administración y la escalabilidad del proceso de registro de IIS al reducir el número de registros que se deben almacenar y analizar individualmente. Para obtener más información acerca del registro binario centralizado, consulte la página [IIS Centralized Binary Logging](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/13a4c0b5-686b-4766-8729-a3402da835f1.mspx) en www.microsoft.com/technet/prodtechnol
/WindowsServer2003/Library/IIS/13a4c0b5-686b-4766-8729-a3402da835f1.mspx.

Cuando los registros de IIS se almacenan en los servidores IIS, únicamente los administradores de los servidores disponen de permiso de acceso de forma predeterminada. Si no se encuentra un directorio de archivo de registro o un propietario de archivo en el grupo **Administradores locales**, el archivo HTTP.sys (el controlador de modo de núcleo de IIS 6.0) publicará un error en el registro de eventos de NT. Este error indica que el propietario del directorio o archivo no está en el grupo de **Administradores locales** y que se ha suspendido el registro para ese sitio web hasta que se agregue el propietarioa dicho grupo o se elimine el directorio o archivo de registro existente.

#### Adición manual de grupos de seguridad únicos a las asignaciones de derechos de usuario

La mayor parte de las asignaciones de derechos de usuario que se aplican a través de MSBP contienen los grupos de seguridad adecuados especificados en las plantillas de seguridad que acompañan a esta guía. Sin embargo, existen algunas cuentas y grupos de seguridad que no se pueden incluir en las plantillas debido a que sus identificadores de seguridad (SID) son específicos de dominios individuales de Windows Server 2003. Las tareas de derechos de usuario que se deben configurar se especifican manualmente en la tabla siguiente.

**Advertencia**: en la siguiente tabla se incluyen valores para la cuenta integrada Administrador. No confunda la cuenta de Administrador con el grupo de seguridad integrado **Administradores.** Si agrega el grupo de seguridad **Administradores** a cualquiera de los derechos de usuario de denegación de acceso enumerados, deberá iniciar sesión localmente para corregir el error.

Asimismo, puede haber cambiado el nombre de la cuenta de Administrador integrada de acuerdo con la recomendación del capítulo 4, "Directiva de línea de base de servidores miembro". Cuando agrega la cuenta de Administrador a cualquier derecho de usuario, asegúrese de que se especifique la cuenta con el nombre cambiado.

**Tabla 9.10 Asignaciones de derechos de usuario agregadas manualmente**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Predeterminada del servidor miembro</th>
<th style="border:1px solid black;" >Cliente heredado</th>
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Seguridad especializada: Funcionalidad limitada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Denegar el acceso desde la red a este equipo</td>
<td style="border:1px solid black;">Administrador integrado; Support_388945a0;
Invitado; todas las cuentas de servicios que NO sean del sistema operativo</td>
<td style="border:1px solid black;">Administrador integrado; Support_388945a0;
Invitado; todas las cuentas de servicios que NO sean del sistema operativo</td>
<td style="border:1px solid black;">Administrador integrado; Support_388945a0;
Invitado; todas las cuentas de servicios que NO sean del sistema operativo</td>
</tr>
</tbody>
</table>
 

**Importante**: “Todas las cuentas de servicio del sistema que no sean del sistema operativo” incluye cuentas de servicio que se utilizan para aplicaciones específicas en una empresa, pero NO incluye las cuentas de SISTEMA LOCAL, SERVICIO LOCAL ni de SERVICIO DE RED (las cuentas incorporadas que el sistema operativo utiliza).

#### Seguridad de las cuentas conocidas

Windows Server 2003 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.

De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.

El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.

**Para proteger las cuentas conocidas en los servidores IIS**

-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.

-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás.

-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.

-   Registre en una ubicación segura cualquier cambio que realice.

    **Nota**: el nombre de la cuenta de administrador integrada puede cambiarse mediante Directiva de grupo. Esta configuración no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque cada organización debe escoger un nombre único para esta cuenta. Sin embargo, tiene la posibilidad de configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de las cuentas de administrador en los tres entornos que se definen en esta guía. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.

#### Seguridad de las cuentas de servicios

A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Creación de la directiva utilizando SCW

Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.

Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.

Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al de su implementación para garantizar la máxima compatibilidad posible. La instalación nueva se llama *equipo de referencia*.

**Para crear la directiva de servidor IIS**

1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.

2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.

3.  Una el equipo al dominio, que aplicará toda la configuración de seguridad de las UO principales.

4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor que comparte esta función. Los ejemplos incluyen servicios específicos de la función, software y agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.

5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.

6.  Asegúrese de que las funciones de servidor detectadas sean apropiadas para su entorno; por ejemplo, las funciones de servidor de aplicaciones y servidor web.

7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.

8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.

9.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.

10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.

11. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.

12. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.

13. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.

14. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-IIS Server.inf).

15. Guarde la directiva con un nombre apropiado (por ejemplo, IIS Server.xml).

    **Nota**: MSBP deshabilita otros servicios relacionados con IIS, como FTP, SMTP y NNTP. La directiva de servidor web se deberá modificar si se va a habilitar alguno de estos servicios en los servidores IIS de cualquiera de los tres entornos que se definen en esta guía.

#### Prueba de la directiva utilizando SCW

Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.

Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.

Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método original de implementación le permite deshacer fácilmente las directivas implementadas desde el SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.

La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.

Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.

Para obtener más información acerca de cómo probar las directivas del SCW, consulte la [Guía de implementación para el Asistente para la configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx y la [documentación del Asistente para la configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.

#### Conversión e implementación de la directiva

Después de probar exhaustivamente la directiva, siga los pasos que se indican a continuación para convertirla en un GPO y realizar la implementación:

1.  En el símbolo de sistema, escriba el siguiente comando:

    ```
    scwcmd transform /p:<PathToPolicy.xml> /g:<GPODisplayName>
    ```

    y, a continuación, pulse Entrar. Por ejemplo:

    ```
    scwcmd transform /p:"C:\Windows\Security\msscw\Policies\IIS
    Server.xml" /g:"IIS Policy"
    ```
    
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.

2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.

Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.

Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

En este capítulo se han explicado las configuraciones de directiva que se pueden utilizar para consolidar los servidores IIS en los que se ejecuta Windows Server 2003 con SP1 en los tres entornos que se definen en esta guía. La mayoría de las configuraciones se aplican mediante un objeto de directiva de grupo (GPO) que se diseñó como complemento de MSBP. Los GPO pueden vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores IIS para proporcionar seguridad adicional.

Algunas configuraciones que se han tratado no se pueden aplicar a través de Directiva de grupo. Para esta configuración, se proporcionan detalles sobre la configuración manual.

#### Información adicional

Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores web IIS en los que se ejecuta Windows Server 2003 con SP1.

-   Para obtener información acerca de cómo habilitar el registro en IIS, consulte el artículo de Microsoft Knowledge Base "[Cómo habilitar el registro en IIS](http://support.microsoft.com/?kbid=313437)", en http://support.microsoft.com/?kbid=313437.

-   Encontrará información adicional acerca del registro en la página [Enable Logging (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/d29207e8-5274-4f4b-9a00-9433b73252d6.mspx) en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/
    d29207e8-5274-4f4b-9a00-9433b73252d6.mspx.

-   Para obtener información acerca de cómo registrar la actividad del sitio, consulte la página [Logging Site Activity (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/ab7e4070-e185-4110-b2b1-1bcac4b168e0.mspx) página en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/
    IIS/ab7e4070-e185-4110-b2b1-1bcac4b168e0.mspx.

-   Para obtener información acerca del registro extendido, consulte la página [Customizing W3C Extended Logging (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/96af216b-e2c0-428e-9880-95cbd85d90a1.mspx) en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/
    IIS/96af216b-e2c0-428e-9880-95cbd85d90a1.mspx.

-   Para obtener información acerca del registro binario centralizado, consulte la página [Centralized Binary Logging in IIS 6.0 (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/b9cdc076-403d-463e-9a36-5a14811d34c7.mspx) en Microsoft.com, en www.microsoft.com/technet/prodtechnol
    /WindowsServer2003/Library/IIS/b9cdc076-403d-463e-9a36-5a14811d34c7.mspx.

-   Para obtener información acerca del registro remoto, consulte la página [Remote Logging (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/a6347ae3-39d1-4434-97c9-5756e5862c61.mspx) en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/
    a6347ae3-39d1-4434-97c9-5756e5862c61.mspx.

-   Para obtener información adicional acerca de IIS 6.0, consulte la página [Internet Information Services](http://www.microsoft.com/windowsserver2003/iis/default.mspx) en www.microsoft.com/WindowsServer2003/iis/default.mspx.

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
