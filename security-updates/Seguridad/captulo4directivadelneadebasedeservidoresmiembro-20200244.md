---
TOCTitle: 'Capítulo 4: Directiva de línea de base de servidores miembro'
Title: 'Capítulo 4: Directiva de línea de base de servidores miembro'
ms:assetid: 'd28caa21-4ec2-4556-a92a-5aa8410df6da'
ms:contentKeyID: 20200244
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163121(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 4: Directiva de línea de base de servidores miembro

Actualizado: 27/12/05

##### En esta página

[](#ekaa)[Información general](#ekaa)
[](#ejaa)[Directiva de línea de base de Windows Server 2003](#ejaa)
[](#eiaa)[Directiva de auditoría](#eiaa)
[](#ehaa)[Asignaciones de derechos de usuario](#ehaa)
[](#egaa)[Opciones de seguridad](#egaa)
[](#efaa)[Registro de eventos](#efaa)
[](#eeaa)[Entradas de registro adicionales](#eeaa)
[](#edaa)[Grupos restringidos](#edaa)
[](#ecaa)[Seguridad del sistema de archivos](#ecaa)
[](#ebaa)[Configuración de seguridad adicional](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

En este capítulo se documentan los requisitos de configuración para administrar una plantilla de seguridad de línea de base para todos los servidores que ejecutan Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1). También se proporciona una orientación administrativa para instalar y configurar un sistema seguro basado en Windows Server 2003 con SP1 en tres entornos distintos. Los requisitos de configuración de este capítulo constituyen la línea de base para todos los procedimientos descritos en los capítulos posteriores de esta guía. Estos capítulos describen cómo reforzar la seguridad de funciones específicas de servidor.

Las recomendaciones de configuración de este capítulo permitirán instaurar seguridad en la base de los servidores de aplicaciones empresariales de un entorno de empresa. Sin embargo, es necesario probar exhaustivamente la interacción de estas configuraciones de seguridad con las aplicaciones empresariales de su organización antes de implementarlas en los entornos de producción.

Las recomendaciones de este capítulo son adecuadas para la mayoría de las organizaciones y se pueden implementar en equipos nuevos o existentes que ejecuten Windows Server 2003 con SP1. El equipo que ha elaborado esta guía ha investigado, revisado y probado las configuraciones de seguridad predeterminadas dentro de Windows Server 2003 con SP1. Para obtener información acerca de todas las configuraciones predeterminadas y una explicación detallada sobre las que se describen en este capítulo, consulte la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en [http://go.microsoft.com/fwlink/?LinkId=15159](http://go.microsoft.com/fwlink/?linkid=15159). Normalmente, la mayoría de las siguientes recomendaciones de configuración ofrecen una mayor seguridad que las configuraciones predeterminadas.

Las configuraciones de seguridad que se analizan en este capítulo están relacionadas con los tres entornos siguientes:

-   **Cliente heredado (LC).** Este entorno incluye equipos que ejecutan Windows NT® 4.0 y Microsoft Windows® 98, a los que a veces se les denomina sistemas operativos *heredados*. Aunque este entorno proporciona una seguridad adecuada, es el menos seguro de los tres que se definen en esta guía. Para contar con una mayor seguridad, las organizaciones pueden decidir migrar al entorno Cliente de empresa, que es más seguro. Además de los sistemas operativos heredados a los que se ha hecho referencia, el entorno LC incluye estaciones de trabajo con Windows 2000 Professional y Windows XP Professional. Este entorno sólo contiene controladores de dominio con Windows 2000 o Windows Server 2003. No existen controladores de dominio con Windows NT 4.0 en este entorno, pero es posible que existan servidores miembro con Windows NT.

-   **Cliente de empresa (EC)**. Este entorno proporciona una seguridad sólida y está diseñado para las versiones más recientes del sistema operativo Windows. Incluye equipos cliente que ejecutan Windows 2000 Professional y Windows XP Professional. La mayoría del trabajo que es necesario realizar para migrar del entorno LC al entorno EC está relacionado con las actualizaciones de los clientes heredados; por ejemplo, de Windows 98 y Windows NT 4.0 Workstation a Windows 2000 o Windows XP. Todos los controladores de dominio y servidores miembro de este entorno ejecutan Windows 2000 Server o Windows Server 2003.

-   **Seguridad especializada: Funcionalidad limitada (SSLF)**. Este entorno ofrece una seguridad más sólida que el entorno EC. La migración del entorno EC al entorno SSLF requiere el cumplimiento de estrictas directivas de seguridad en los equipos cliente y en los servidores. Este entorno incluye equipos cliente que ejecutan Windows 2000 Professional y Windows XP Professional, así como controladores de dominio con Windows 2000 Server o Windows Server 2003. En el entorno SSLF, la preocupación por la seguridad es tan importante que se considera aceptable una pérdida significativa de funcionalidad y de capacidad de administración de los clientes a cambio de lograr el máximo nivel de seguridad. Los servidores miembro de este entorno ejecutan Windows 2000 Server o Windows Server 2003.

Advertirá que en muchos casos el entorno SSLF establece de forma explícita el valor predeterminado. Debe tener en cuenta que esta configuración afectará a la compatibilidad, ya que es posible que se produzcan errores en las aplicaciones que intenten ajustar localmente algunos valores de configuración. Por ejemplo, algunas aplicaciones necesitan ajustar las asignaciones de derechos de usuario para conceder privilegios adicionales a las cuentas de servicios. Como las directivas de grupo tienen prioridad sobre la directiva del equipo local, se pueden generar errores en estas operaciones. Antes de implementar las configuraciones recomendadas en los equipos de producción, especialmente las relativas al entorno SSLF, debe probar minuciosamente todas las aplicaciones.

La figura siguiente muestra los tres entornos de seguridad y los clientes compatibles en cada uno de ellos.

[![](images/Cc163121.sgfg0401(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163121.sgfg0401_big(es-es,technet.10).gif)

**Figura 4.1 Entornos de seguridad existentes y planeados**

Las organizaciones que deseen garantizar la seguridad de sus entornos mediante un enfoque por fases pueden optar por empezar por el nivel del entorno Cliente heredado y después ir migrando gradualmente a entornos más seguros a medida que vayan actualizando y probando las aplicaciones y los equipos cliente con configuraciones de seguridad más estrictas.

La siguiente figura muestra cómo las plantillas de seguridad del archivo .inf se utilizan como base para la directiva de línea de base de servidores miembro (MSBP) del entorno Cliente de empresa. En la figura también se indica una manera posible de vincular y aplicar esta directiva a todos los servidores de una organización.

Windows Server 2003 con SP1 se proporciona con los valores predeterminados para crear un entorno seguro. En muchos casos, en este capítulo se recomiendan configuraciones que difieren de los valores predeterminados. En el capítulo también se aplican valores predeterminados específicos para los tres entornos. Para obtener más información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.

[![](images/Cc163121.sgfg0402(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163121.sgfg0402_big(es-es,technet.10).gif)

**Figura 4.2 La plantilla de seguridad EC-Member Server Baseline.inf se importa en la directiva MSBP, que se vincula a continuación a la unidad organizativa (UO) Servidores miembro**

En el resto de los capítulos de la guía se definen los procedimientos para reforzar la seguridad de funciones específicas de servidor. Las principales funciones de servidor que se describen en esta guía son las siguientes:

-   Controladores de dominio que incluyen servicios DNS

-   Servidores de infraestructura que incluyen servicios WINS y DHCP

-   Servidores de archivos

-   Servidores de impresión

-   Servidores web que ejecutan Servicios de Internet Information Server (IIS)

-   Servidores de autenticación de Internet de Microsoft (IAS)

-   Servidores de Servicios de Certificate Server (CA)

-   Hosts de baluarte

Muchas de las siguientes configuraciones que aparecen en la directiva MSBP del entorno Cliente de empresa se aplican también a estas funciones de servidor en los tres entornos definidos en esta guía. Las plantillas de seguridad están diseñadas de manera única para satisfacer las necesidades de cada entorno particular. En la siguiente tabla se muestran los nombres de las plantillas de seguridad de línea de base para los tres entornos.

**Tabla 4.1 Plantillas de seguridad de línea de base para los tres entornos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Cliente heredado</p></th>
<th><p>Cliente de empresa</p></th>
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>LC-Member Server Baseline.inf</p></td>
<td style="border:1px solid black;"><p>EC-Member Server Baseline.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Member Server Baseline.inf</p></td>
</tr>  
</tbody>  
</table>
  
En el resto del capítulo se describen las configuraciones de seguridad que son comunes a los tres entornos y, por tanto, todas las plantillas de seguridad de **línea de base de servidores miembro**.
  
Las plantillas de seguridad de línea de base constituyen también la base para las plantillas de seguridad de controladores de dominio que se definen en el capítulo 5, "Directiva de línea de base de controladores de dominio". Las plantillas de seguridad de la **función de controladores de dominio** incluyen la configuración de línea de base del GPO Directiva de grupo de controladores de dominio, que está vinculado a la UO Controladores de dominio en los tres entornos. En el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", se proporcionan instrucciones paso a paso para crear las UO y las directivas de grupo y, a continuación, importar la plantilla de seguridad adecuada en cada GPO.
  
**Nota**: algunos de los procedimientos utilizados para reforzar la seguridad de los servidores no se pueden automatizar mediante la directiva de grupo. Estos procedimientos se describen en la sección "Configuración de seguridad adicional" de este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de línea de base de Windows Server 2003
  
La configuración en el nivel de la UO Servidor miembro define los valores comunes a todas funciones de servidores miembro que se tratan en esta guía. Para aplicar esta configuración, puede crear un objeto GPO que esté vinculado a la UO Servidor miembro, a la que se le conoce como una directiva de línea de base. El GPO automatizará la configuración de los valores de seguridad específicos en cada servidor. Deberá mover las cuentas de servidor a las UO secundarias correspondientes de la UO Servidor miembro según la función de cada servidor.
  
Las siguientes configuraciones se describen según el orden en que aparecen en la interfaz de usuario (UI) del complemento Editor de configuración de seguridad (SCE) de Microsoft Management Console (MMC).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de auditoría
  
Los administradores deben crear una directiva de auditoría que defina los eventos que se identificarán y que registre las actividades de los usuarios o equipos en las categorías de eventos especificadas. Asimismo, pueden controlar la actividad relacionada con la seguridad como, por ejemplo, los usuarios que tienen acceso a un objeto, si un usuario inicia o cierra sesión en un equipo o si se realizan cambios en una configuración de la directiva de auditoría.
  
Antes de implementar una directiva de auditoría, debe decidir las categorías de eventos que se van a auditar para el entorno. La configuración de auditoría seleccionada por un administrador para las categorías de eventos definirá la directiva de auditoría de la organización. Al definir la configuración de auditoría para las categorías de eventos específicas, los administradores pueden crear una directiva de auditoría que se ajuste a las necesidades de seguridad de la organización.
  
Si no existe ninguna directiva de auditoría, será complicado o imposible determinar lo que sucedió durante un incidente de seguridad. No obstante, si la configuración de auditoría se establece de modo que demasiadas actividades autorizadas generen eventos, el registro de seguridad se llenará de datos poco útiles. El objetivo de las siguientes recomendaciones y descripciones de configuración es ayudarle a determinar lo que se va a supervisar para que los datos recopilados sean relevantes.
  
A menudo, los registros de errores son mucho más informativos que los registros de aciertos, ya que los errores suelen indicar problemas. Por ejemplo, el inicio de sesión correcto en un equipo por parte de un usuario se consideraría normal. Sin embargo, si alguien intenta iniciar sesión en un equipo varias veces y no lo consigue, esto puede indicar un intento de obtener acceso al equipo con las credenciales de la cuenta de otro usuario. Los registros de eventos registran los eventos del equipo. En los sistemas operativos Microsoft Windows, hay registros de eventos independientes para las aplicaciones, las eventos de seguridad y los eventos de sistema. El registro de seguridad registra eventos de auditoría. El contenedor del registro de eventos de la directiva de grupo se utiliza para definir los atributos relacionados con los registros de eventos de aplicación, seguridad y sistema; por ejemplo, el tamaño máximo del registro, los derechos de acceso para cada registro, y la configuración y los métodos de retención.
  
Antes de implementar una directiva de auditoría, las organizaciones deben determinar cómo recopilarán, organizarán y analizarán los datos. Los volúmenes grandes de datos de auditoría no tienen mucho valor si no hay un plan para aprovecharlos. Además, el rendimiento se puede ver afectado cuando se auditan redes de equipos. La repercusión de una determinada combinación de valores de configuración puede ser insignificante en el equipo de un usuario final, pero muy notable en un servidor con mucha actividad. Por lo tanto, debe probar si el rendimiento se verá afectado antes de implementar la nueva configuración de auditoría en el entorno de producción.
  
La tabla siguiente incluye recomendaciones de configuración de la directiva de auditoría para los tres entornos definidos en esta guía. Es posible que observe que la configuración de la mayoría de los valores es similar en los tres entornos. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
Puede configurar los valores de configuración de la directiva de auditoría en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales**  
**\\Directiva de auditoría**
  
Para obtener un resumen de la configuración recomendada en esta sección, consulte el libro de Microsoft Excel® "Windows Server 2003 Security Guide Settings" que se incluye con la versión descargable de esta guía. Para obtener más información acerca de la configuración predeterminada y una explicación detallada de las configuraciones descritas en esta sección, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en [http://go.microsoft.com/fwlink/?LinkId=15159](http://go.microsoft.com/fwlink/?linkid=15159).
  
**Tabla 4.2 Configuraciones de la directiva de auditoría**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión de cuenta</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar la administración de cuentas</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar el acceso a objetos</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar el cambio de directivas</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar el uso de privilegios</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar el seguimiento de procesos</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar eventos del sistema</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar eventos de inicio de sesión de cuenta
  
Esta configuración de directiva determina si se deben auditar los inicios o cierres de sesión de un usuario desde otro equipo que valide la cuenta. Cuando una cuenta de usuario de dominio se autentica en un controlador de dominio, se genera y se registra un evento de inicio de sesión de cuenta en el registro de seguridad del controlador de dominio. Cuando un usuario local se autentica en un equipo local, se genera y se registra un evento de inicio de sesión en el registro de seguridad local. Los eventos de cierre de sesión de cuenta no se registran nunca.
  
**Auditar eventos de inicio de sesión de cuenta** se configura para registrar los valores **Correcto** para las directivas de línea de base de los entornos LC y EC, y para registrar los eventos de tipo **Correcto** y **Erróneo** para la directiva de línea de base del entorno SSLF.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración de directiva registra en el registro de seguridad. Estos Id. de evento pueden ser útiles si desean crear alertas personalizadas para supervisar un conjunto de programas de software, como Microsoft Operations Manager (MOM).
  
**Tabla 4.3 Eventos de inicio de sesión de cuenta**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>672</p></td>
<td style="border:1px solid black;"><p>Se ha emitido y validado con éxito un vale del servicio de autenticación (AS). En Windows Server 2003 con SP1, este evento será de tipo Auditoría de aciertos para las solicitudes correctas o de tipo Auditoría de errores para las solicitudes con errores.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>673</p></td>
<td style="border:1px solid black;"><p>Se ha otorgado un vale del servicio de otorgamiento de vales (TGS). Un TGS es un vale emitido por el servicio TGS de Kerberos versión 5 que permite a un usuario autenticarse en un servicio específico del dominio. Windows Server 2003 con SP1 registrará los aciertos y errores de este tipo de evento.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>674</p></td>
<td style="border:1px solid black;"><p>Una entidad principal de seguridad ha renovado un vale AS o TGS.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>675</p></td>
<td style="border:1px solid black;"><p>Error en la autenticación previa. Este evento se genera en un Centro de distribución de claves (KDC) cuando un usuario escribe una contraseña incorrecta.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>676</p></td>
<td style="border:1px solid black;"><p>Error de la petición del vale de autenticación. Windows Server 2003 con SP1 no genera este evento. Este evento se utiliza en otras versiones de Windows para indicar un error en la autenticación que no se debe al uso de credenciales incorrectas.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>677</p></td>
<td style="border:1px solid black;"><p>No se ha otorgado un vale TGS. Windows Server 2003 con SP1 no genera este evento. Para este caso, Windows Server 2003 con SP1 utiliza un evento de tipo Auditoría de errores con el Id. 672.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>678</p></td>
<td style="border:1px solid black;"><p>Se ha asignado con éxito una cuenta a una cuenta de dominio.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>681</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Se ha intentado un inicio de sesión de cuenta de dominio. Este evento sólo lo generan los controladores de dominio.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>682</p></td>
<td style="border:1px solid black;"><p>Un usuario se ha vuelto a conectar a una sesión de Servicios de Terminal Server desconectada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>683</p></td>
<td style="border:1px solid black;"><p>Un usuario ha desconectado una sesión de Servicios de Terminal Server, pero no la ha cerrado.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar la administración de cuentas
  
Esta configuración de directiva determina si se deben auditar todos los eventos de administración de cuentas de un equipo. Algunos ejemplos de eventos de administración de cuentas:
  
-   Se crea, cambia o elimina una cuenta de usuario o grupo.
  
-   Cambia el nombre de una cuenta de usuario, o bien, se desactiva o se activa una.
  
-   Se establece o cambia una contraseña.
  
Las organizaciones deben ser capaces de determinar quién crea, modifica o elimina tanto las cuentas locales como las de dominio. Los cambios no autorizados podrían indicar cambios erróneos realizados por un administrador que no comprende cómo seguir las directivas de la organización, pero también un ataque deliberado.
  
Por ejemplo, los eventos de error de administración de cuentas suelen indicar intentos por parte de un administrador de nivel inferior (o de un atacante que ha comprometido la cuenta de un administrador de nivel inferior) de elevar sus privilegios. Los registros pueden ser útiles para determinar las cuentas que un atacante ha modificado y creado.
  
**Auditar la administración de cuentas** se configura para registrar los valores **Correcto** para las directivas de línea de base de los entornos LC y EC, y para registrar los valores de tipo **Correcto** y **Erróneo** para la directiva de línea de base del entorno SSLF.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración de directiva registra en el registro de seguridad. Estos Id. de evento pueden ser útiles cuando se desean crear alertas personalizadas para supervisar un conjunto de programas de software, como MOM. La mayoría del software de administración de operaciones se puede personalizar con secuencias de comandos para capturar o marcar eventos que se basan en estos Id. de evento.
  
**Tabla 4.4 Eventos de administración de cuentas**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>624</p></td>
<td style="border:1px solid black;"><p>Se ha creado una cuenta de usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>627</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una contraseña de usuario.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>628</p></td>
<td style="border:1px solid black;"><p>Se ha configurado una contraseña de usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>630</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado una cuenta de usuario.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>631</p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo global.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>632</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo global.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>633</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo global.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>634</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un grupo global.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>635</p></td>
<td style="border:1px solid black;"><p>Se ha creado un nuevo grupo local.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>636</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo local.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>637</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo local.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>638</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un grupo local.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>639</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una cuenta de grupo local.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>641</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una cuenta de grupo global.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>642</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una cuenta de usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>643</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una directiva de dominio.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>644</p></td>
<td style="border:1px solid black;"><p>Se ha bloqueado automáticamente una cuenta de usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>645</p></td>
<td style="border:1px solid black;"><p>Se ha creado una cuenta de equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>646</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una cuenta de equipo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>647</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado una cuenta de equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>648    </p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo de seguridad local con la seguridad deshabilitada.</p>
<p><strong>Nota</strong>: SECURITY_DISABLED formalmente significa que este grupo no puede usarse para conceder permisos en las comprobaciones de acceso.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>649</p></td>
<td style="border:1px solid black;"><p>Se ha modificado un grupo de seguridad local con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>650</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo de seguridad local con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>651</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo de seguridad local con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>652</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un grupo local con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>653</p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo global con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>654</p></td>
<td style="border:1px solid black;"><p>Se ha modificado un grupo global con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>655</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo global con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>656</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo global con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>657</p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo global con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>658</p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo universal con la seguridad habilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>659</p></td>
<td style="border:1px solid black;"><p>Se ha modificado un grupo universal con la seguridad habilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>660</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo universal con la seguridad habilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>661</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo universal con la seguridad habilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>662</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un grupo universal con la seguridad habilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>663</p></td>
<td style="border:1px solid black;"><p>Se ha creado un grupo universal con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>664</p></td>
<td style="border:1px solid black;"><p>Se ha modificado un grupo universal con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>665</p></td>
<td style="border:1px solid black;"><p>Se ha agregado un miembro a un grupo universal con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>666</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un miembro de un grupo universal con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>667</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un grupo universal con la seguridad deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>668</p></td>
<td style="border:1px solid black;"><p>Se ha modificado un tipo de grupo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>684    </p></td>
<td style="border:1px solid black;"><p>Se ha establecido el descriptor de seguridad de los miembros del grupo administrativo.</p>
<p><strong>Nota</strong>: en un controlador de dominio, cada 60 minutos, un subproceso en segundo plano busca todos los miembros de los grupos administrativos (como los administradores de dominio, empresariales y del esquema) y les aplica un descriptor fijo de seguridad. Este evento queda registrado.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>685</p></td>
<td style="border:1px solid black;"><p>Se ha modificado el nombre de una cuenta.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar eventos de inicio de sesión
  
Esta configuración de directiva determina si se debe auditar cada inicio y cierre de sesión de usuario en un equipo. **Auditar eventos de inicio de sesión** genera registros en los controladores de dominio y en los equipos locales para supervisar la actividad de las cuentas de dominio y de las cuentas locales, respectivamente.
  
Si se configura **Auditar eventos de inicio de sesión** como **Sin auditoría**, será difícil o imposible determinar qué usuario ha iniciado o intentado iniciar una sesión en los equipos de la organización. Si se habilita el valor **Correcto** para **Auditar eventos de inicio de sesión** en un miembro de dominio, se generará un evento cada vez que un usuario inicie sesión en la red, independientemente del lugar de la red en el que residan las cuentas. Si el usuario inicia una sesión en una cuenta local y **Auditar eventos de inicio de sesión de cuenta** está configurado como **Habilitado**, el inicio de sesión del usuario generará dos eventos.
  
Aunque no modifique los valores predeterminados de esta configuración de directiva, no habrá disponible ningún registro de auditoría que pueda analizar después de un incidente de seguridad. **Auditar eventos de inicio de sesión** se configura para registrar los valores **Correcto** en las directivas de línea de base de los entornos LC y EC, y para registrar los valores de tipo **Correcto** y **Erróneo** para la directiva SSLF.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración de directiva registra en el registro de seguridad.
  
**Tabla 4.5 Auditar eventos de inicio de sesión    **

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>528</p></td>
<td style="border:1px solid black;"><p>Un usuario ha iniciado una sesión con éxito en un equipo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>529</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El intento de inicio de sesión se ha realizado con un nombre de usuario desconocido o con un nombre de usuario conocido y una contraseña incorrecta.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>530</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El intento de inicio de sesión se ha realizado fuera del tiempo permitido.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>531</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Se ha intentado iniciar una sesión con una cuenta deshabilitada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>532</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Se ha intentado iniciar una sesión con una cuenta caducada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>533</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El usuario que ha intentado el inicio de sesión no cuenta con permiso para iniciar la sesión en este equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>534</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El usuario ha intentado iniciar la sesión con un tipo de contraseña no permitido.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>535</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Ha caducado la contraseña correspondiente a la cuenta especificada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>536</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El servicio de inicio de cuenta de red no se encuentra activo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>537    </p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Error en el intento de inicio de sesión por otras razones.</p>
<p><strong>Nota</strong>: en algunos casos, el motivo del error de inicio de sesión puede ser desconocido.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>538</p></td>
<td style="border:1px solid black;"><p>Un usuario ha cerrado la sesión.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>539</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. La cuenta se ha bloqueado en el momento en el que se ha intentado iniciar la sesión.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>540</p></td>
<td style="border:1px solid black;"><p>Un usuario ha iniciado la sesión correctamente en la red.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>541</p></td>
<td style="border:1px solid black;"><p>Se ha completado la autenticación IKE (Internal Key Exchange) en modo principal entre el equipo local y la identidad recíproca (estableciendo una asociación de seguridad), o el modo rápido ha establecido un canal de datos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>542</p></td>
<td style="border:1px solid black;"><p>Se ha finalizado el canal de datos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>543    </p></td>
<td style="border:1px solid black;"><p>Se ha finalizado el modo principal.</p>
<p><strong>Nota</strong>: esto puede ocurrir porque ha caducado el límite de tiempo de la asociación de seguridad (el valor predeterminado es de ocho horas), hay cambios en la directiva o se ha producido una finalización recíproca.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>544</p></td>
<td style="border:1px solid black;"><p>Se ha producido un error en la autenticación en modo principal porque la otra parte no ha proporcionado un certificado válido o no se ha validado la firma.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>545</p></td>
<td style="border:1px solid black;"><p>Se ha producido un error en la autenticación de modo principal debido a un error del protocolo de autenticación Kerberos o a una contraseña no válida.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>546</p></td>
<td style="border:1px solid black;"><p>Se ha producido un error en el establecimiento de la asociación de seguridad IKE porque la otra parte ha enviado una propuesta no válida. Se ha recibido un paquete que contenía datos no válidos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>547</p></td>
<td style="border:1px solid black;"><p>Error durante una negociación IKE.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>548</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. El identificador de seguridad (SID) de un dominio de confianza no coincide con el SID del dominio de la cuenta del cliente.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>549</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión. Se han filtrado todos los SID correspondientes a los espacios de nombres que no son de confianza durante una autenticación a través de bosques.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>550</p></td>
<td style="border:1px solid black;"><p>Mensaje de notificación que podría indicar un posible ataque de negación de servicio (DoS).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>551</p></td>
<td style="border:1px solid black;"><p>Un usuario ha iniciado el proceso de cierre de sesión.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>552</p></td>
<td style="border:1px solid black;"><p>Un usuario ha iniciado correctamente una sesión en un equipo mediante credenciales explícitas mientras todavía mantenía abierta una sesión como un usuario diferente.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>682</p></td>
<td style="border:1px solid black;"><p>Un usuario se ha conectado de nuevo a una sesión de servidor de terminal desconectada.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>683    </p></td>
<td style="border:1px solid black;"><p>Un usuario ha desconectado una sesión de Servicios de Terminal Server, pero no la ha cerrado.</p>
<p><strong>Nota</strong>: este evento se genera cuando un usuario está conectado a una sesión de Servicios de Terminal Server en la red. Aparece en el servidor de la terminal.</p></td>
</tr>
</tbody>
</table>
<p> </p>

#### Auditar el acceso a objetos

Esta configuración de directiva no provocará por sí misma la auditoría de ningún evento. **Auditar el acceso a objetos** determina si se debe auditar el acceso de un usuario a un objeto (por ejemplo, un archivo, una carpeta, una clave del Registro o una impresora) si hay especificada una lista de control de acceso del sistema (SACL).

Una lista de control de acceso del sistema se compone de entradas de control de acceso (ACE), cada una de las cuales contiene tres datos:

-   La entidad de seguridad principal (el usuario, equipo o grupo) que se va a auditar.

-   El tipo de acceso específico que se va a auditar, denominado máscara de acceso.

-   Un indicador que señala si se deben auditar eventos de acceso erróneos, eventos de acceso correctos o ambos.

Si se configura **Auditar el acceso a objetos** para registrar los valores **Correcto**, se generará una entrada de auditoría cada vez que un usuario obtenga acceso a un objeto con una SACL especificada. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría cada vez que un usuario intente obtener acceso a un objeto con una SACL especificada y no lo consiga.

Al configurar las SACL, las organizaciones deben definir sólo las acciones que desean que se habiliten. Por ejemplo, es posible que desee habilitar las configuraciones de auditoría **Escribir datos y Anexar datos** en los archivos ejecutables para realizar un seguimiento del cambio o reemplazo de dichos archivos, ya que los virus informáticos, gusanos y caballos de Troya atacarán normalmente los archivos ejecutables. De forma similar, puede estar interesado en el seguimiento del acceso o cambio de los documentos confidenciales.

**Auditar el acceso a objetos** se configura en el valor predeterminado **Sin auditoría** en la directiva de línea de base para los entornos LC y EC. Sin embargo, esta configuración de directiva se establece para registrar los valores **Erróneos** en la directiva de línea de base del entorno SSLF.

La tabla siguiente incluye los eventos de seguridad importantes que esta configuración de directiva registra en el registro de seguridad.

**Tabla 4.6 Eventos de acceso a objetos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Descripción del evento</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>560</p></td>
<td style="border:1px solid black;"><p>Se ha otorgado acceso a un objeto existente.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>562</p></td>
<td style="border:1px solid black;"><p>Se ha cerrado un identificador para un objeto.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>563    </p></td>
<td style="border:1px solid black;"><p>Se ha intentado abrir un objeto con la intención de eliminarlo.</p>
<p><strong>Nota</strong>: los sistemas de archivos utilizan este evento cuando se especifica el indicador FILE_DELETE_ON_CLOSE en Createfile().</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>564</p></td>
<td style="border:1px solid black;"><p>Se ha eliminado un objeto protegido.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>565</p></td>
<td style="border:1px solid black;"><p>Se ha otorgado acceso a un tipo de objeto existente.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>567    </p></td>
<td style="border:1px solid black;"><p>Se ha utilizado un permiso asociado a un identificador.</p>
<p><strong>Nota</strong>: se crea un identificador con determinados permisos concedidos, como de lectura y escritura. Cuando se utiliza el identificador, se genera un máximo de una auditoría para cada uno de los permisos utilizados.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>568</p></td>
<td style="border:1px solid black;"><p>Se ha intentado crear un vínculo físico a un archivo que se está auditando.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>569</p></td>
<td style="border:1px solid black;"><p>El administrador de recursos de la aplicación Administrador de autorización ha intentado crear un contexto cliente.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>570    </p></td>
<td style="border:1px solid black;"><p>Un cliente ha intentado obtener acceso a un objeto.</p>
<p><strong>Nota</strong>: se generará un evento por cada operación que se intente realizar en el objeto.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>571</p></td>
<td style="border:1px solid black;"><p>La aplicación Administrador de autorización ha eliminado el contexto cliente.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>572</p></td>
<td style="border:1px solid black;"><p>El Administrador de autorización ha inicializado la aplicación.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>772</p></td>
<td style="border:1px solid black;"><p>El Administrador de certificados ha denegado una petición pendiente de certificado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>773</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server recibieron una solicitud de certificado reenviada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>774</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server revocaron un certificado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>775</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server recibieron una solicitud de publicación de la lista de revocación de certificados (CRL).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>776</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server han publicado la CRL.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>777</p></td>
<td style="border:1px solid black;"><p>Se ha realizado una extensión de petición de certificado.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>778</p></td>
<td style="border:1px solid black;"><p>Cambio en uno o más de los atributos de solicitudes de certificados.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>779</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server recibieron una solicitud de cierre.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>780</p></td>
<td style="border:1px solid black;"><p>Se inició la copia de seguridad de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>781</p></td>
<td style="border:1px solid black;"><p>Se completó la copia de seguridad de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>782</p></td>
<td style="border:1px solid black;"><p>Se inició la restauración de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>783</p></td>
<td style="border:1px solid black;"><p>Se completó la restauración de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>784</p></td>
<td style="border:1px solid black;"><p>Se iniciaron los Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>785</p></td>
<td style="border:1px solid black;"><p>Se detuvieron los Servicios de Certificate Server</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>786</p></td>
<td style="border:1px solid black;"><p>Cambio en los permisos de seguridad de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>787</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server recuperaron una clave archivada.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>788</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server importaron un certificado a su correspondiente base de datos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>789</p></td>
<td style="border:1px solid black;"><p>Cambio en el filtro de auditoría de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>790</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server recibieron una solicitud de certificado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>791</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server aprobaron una solicitud de certificado y emitieron un certificado.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>792</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server denegaron una solicitud de certificado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>793</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server han establecido el estado de una solicitud de certificado en Pendiente.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>794</p></td>
<td style="border:1px solid black;"><p>Cambio en la configuración del administrador de certificados correspondiente a Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>795</p></td>
<td style="border:1px solid black;"><p>Cambio en una entrada de configuración de Servicios de Certificate Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>796</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una propiedad de los Servicios de Certificate Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>797</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server archivaron una clave.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>798</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server importaron y archivaron una clave.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>799</p></td>
<td style="border:1px solid black;"><p>Los Servicios de Certificate Server publicaron el certificado de la entidad de certificación (CA) en Active Directory.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>800</p></td>
<td style="border:1px solid black;"><p>Se han eliminado una o varias filas de la base de datos de certificados.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>801</p></td>
<td style="border:1px solid black;"><p>Separación de funciones activada.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar el cambio de directivas
  
Esta configuración de directiva determina si se debe auditar cada caso en que se produzca un cambio en las directivas de asignación de derechos de usuario, auditoría o confianza.
  
Si se configura **Auditar el cambio de directivas** para registrar los valores **Correcto**, se generará una entrada de auditoría para cada cambio que se realice en las directivas de asignación de derechos de usuario, auditoría o confianza. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría con cada intento de cambiar las directivas de asignación de derechos de usuario, auditoría o confianza que no se consiga.
  
La configuración recomendada le permitirá ver los privilegios de cuenta que un atacante intente elevar; por ejemplo, si intenta agregar el privilegio **Depurar programas** o **Realizar copias de seguridad de archivos y directorios**.
  
**Auditar el cambio de directivas** se configura para registrar los valores **Correcto** en la directiva de línea de base para los tres entornos definidos en esta guía. Actualmente, el valor de configuración **Erróneo** no captura eventos relevantes.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración de directiva registra en el registro de seguridad.
  
**Tabla 4.7 Eventos de Auditar el cambio de directivas**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>608</p></td>
<td style="border:1px solid black;"><p>Se ha asignado un derecho de usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>609</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un derecho de usuario.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>610</p></td>
<td style="border:1px solid black;"><p>Se ha creado una relación de confianza con otro dominio.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>611</p></td>
<td style="border:1px solid black;"><p>Se ha quitado una relación de confianza con otro dominio.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>612</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una directiva de auditoría.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>613</p></td>
<td style="border:1px solid black;"><p>Se ha iniciado un agente de directiva IPSec (protocolo de seguridad de Internet).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>614</p></td>
<td style="border:1px solid black;"><p>Se ha deshabilitado un agente de directiva IPSec.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>615</p></td>
<td style="border:1px solid black;"><p>Un agente de directiva IPSec ha cambiado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>616</p></td>
<td style="border:1px solid black;"><p>Un agente de directiva IPSec ha detectado un error potencialmente grave.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>617</p></td>
<td style="border:1px solid black;"><p>Una directiva de Kerberos versión 5 ha cambiado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>618</p></td>
<td style="border:1px solid black;"><p>Una directiva de recuperación de datos cifrados ha cambiado.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>620</p></td>
<td style="border:1px solid black;"><p>Se ha modificado una relación de confianza con otro dominio.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>621</p></td>
<td style="border:1px solid black;"><p>Se ha otorgado a una cuenta acceso al sistema.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>622</p></td>
<td style="border:1px solid black;"><p>Se ha quitado el acceso al sistema desde una cuenta.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>623</p></td>
<td style="border:1px solid black;"><p>La directiva de auditoría se ha establecido de forma individual para cada usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>625</p></td>
<td style="border:1px solid black;"><p>La directiva de auditoría se ha actualizado de forma individual para cada usuario.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>768    </p></td>
<td style="border:1px solid black;"><p>Se ha detectado una colisión entre un elemento de espacio de nombres de un bosque y un elemento de espacio de nombres de otro bosque.</p>
<p><strong>Nota</strong>: cuando un elemento de espacio de nombres de un bosque se superpone a un elemento de otro bosque, se puede producir ambigüedad en la resolución de nombres de los elementos de espacio de nombres. Esta coincidencia también se conoce como colisión. No todos los parámetros son válidos para todos los tipos de entrada. Por ejemplo, los campos como el nombre DNS, el nombre NetBIOS y el SID no son válidos para una entrada del tipo 'TopLevelName'.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>769    </p></td>
<td style="border:1px solid black;"><p>Se ha agregado información de confianza del bosque.</p>
<p><strong>Nota</strong>: este mensaje de evento se genera cuando la información de confianza del bosque se actualiza y se agregan una o varias entradas. Se genera un mensaje de evento por cada entrada agregada, eliminada o modificada. Si se agregan, eliminan o modifican varias entradas en una actualización individual de la información de confianza del bosque, se asigna a todos los mensajes de evento generados un identificador único exclusivo denominado Id. de operación. Esta funcionalidad le permite saber que los diversos mensajes de evento generados son el resultado de una sola operación. No todos los parámetros son válidos para todos los tipos de entrada. Por ejemplo, los parámetros como el nombre DNS, el nombre NetBIOS y el SID no son válidos para una entrada del tipo &quot;TopLevelName&quot;.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>770    </p></td>
<td style="border:1px solid black;"><p>Se ha eliminado información de confianza del bosque.</p>
<p><strong>Nota</strong>: consulte la descripción del evento 769.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>771    </p></td>
<td style="border:1px solid black;"><p>Se ha modificado información de confianza del bosque.</p>
<p><strong>Nota</strong>: consulte la descripción del evento 769.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>805</p></td>
<td style="border:1px solid black;"><p>El servicio de registro de eventos ha leído la configuración del registro de seguridad de una sesión.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar el uso de privilegios
  
Esta configuración de directiva determina si se debe auditar cada caso en el que un usuario ejecute un derecho de usuario. Si se configura **Auditar el uso de privilegios** para registrar los valores **Correcto**, se generará una entrada de auditoría cada vez que un usuario ejerza correctamente un derecho de usuario. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría cada vez que no se consiga ejercer un derecho de usuario.
  
Aunque se configure **Auditar el uso de privilegios**, no se generarán auditorías cuando se ejerzan los siguientes derechos de usuario, ya que estos derechos generan muchos eventos en el registro de seguridad. El rendimiento de los equipos probablemente se verá afectado si se auditan estos derechos de usuario:
  
-   Omitir la comprobación de recorrido
  
-   Depurar programas
  
-   Crear un objeto Token
  
-   Reemplazar un token de nivel de proceso
  
-   Generar auditorías de seguridad
  
-   Realizar copias de seguridad de archivos y directorios
  
-   Restaurar archivos y directorios
  
    **Nota**: si desea auditar estos derechos de usuario, debe habilitar la opción de seguridad **Auditoría: auditar el uso del privilegio de copia de seguridad y restauración** en la directiva de grupo.
  
**Auditar el uso de privilegios** se encuentra a la izquierda del valor predeterminado **Sin auditoría** de la directiva de línea de base de los entornos LC y EC. Sin embargo, esta configuración de directiva se establece para registrar los valores **Erróneos** en la directiva de línea de base del entorno SSLF. El uso con errores de un derecho de usuario es un indicador de un problema de red general y, frecuentemente, puede señalar un intento de infracción de seguridad. Las organizaciones deben configurar **Auditar el uso de privilegios** en **Habilitar** sólo si hay un motivo empresarial específico que lo justifique.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración registra en el registro de seguridad.
  
**Tabla 4.8 Eventos de uso de privilegios**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>576    </p></td>
<td style="border:1px solid black;"><p>Se han agregado los privilegios especificados al testigo de acceso de un usuario.</p>
<p><strong>Nota</strong>: este evento se genera cuando el usuario inicia sesión.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>577</p></td>
<td style="border:1px solid black;"><p>Un usuario ha intentado realizar una operación privilegiada de servicio del sistema.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>578</p></td>
<td style="border:1px solid black;"><p>Se han utilizado privilegios en un identificador ya abierto de un objeto protegido.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar el seguimiento de procesos
  
Esta configuración de directiva determina si se debe auditar información de seguimiento detallada de eventos como la activación de programas, la salida de procesos, la duplicación de identificadores y el acceso indirecto a objetos. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría cada vez que se consiga realizar un seguimiento del proceso. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría cada vez que no se consiga realizar un seguimiento del proceso.
  
**Auditar el seguimiento de procesos** genera un elevado número de eventos; por ello, se configura normalmente en **Sin auditoría**, ya que está en la directiva de línea de base de los tres entornos definidos en esta guía. Sin embargo, esta configuración de directiva puede ser muy útil durante la respuesta a un incidente porque proporciona un registro detallado de los procesos que se iniciaron y del momento de inicio de cada uno de ellos.
  
La tabla siguiente incluye los eventos de seguridad importantes que esta configuración registra en el registro de seguridad.
  
**Tabla 4.9 Eventos de seguimiento de procesos**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>592</p></td>
<td style="border:1px solid black;"><p>Se ha creado un nuevo proceso.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>593</p></td>
<td style="border:1px solid black;"><p>Se ha salido de un proceso.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>594</p></td>
<td style="border:1px solid black;"><p>Se ha duplicado un identificador para un objeto.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>595</p></td>
<td style="border:1px solid black;"><p>Se ha obtenido acceso indirecto a un objeto.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>596    </p></td>
<td style="border:1px solid black;"><p>Se ha realizado una copia de seguridad de una clave de sesión de protección de datos.</p>
<p><strong>Nota</strong>: las rutinas CryptProtectData y CryptUnprotectData y el sistema de cifrado de archivos (EFS) utilizan la clave de sesión de protección. Se realiza una copia de seguridad de la clave de sesión de protección cada vez que se crea una nueva (la configuración predeterminada es de 90 días). Generalmente, es un controlador de dominio el que realiza la copia de la clave.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>597</p></td>
<td style="border:1px solid black;"><p>Se ha recuperado una clave de sesión de protección de datos desde un servidor de recuperación.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>598</p></td>
<td style="border:1px solid black;"><p>Se han protegido los datos auditables.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>599</p></td>
<td style="border:1px solid black;"><p>Se han desprotegido los datos auditables.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>600</p></td>
<td style="border:1px solid black;"><p>Se ha asignado un testigo principal a un proceso.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>601</p></td>
<td style="border:1px solid black;"><p>Un usuario ha intentado instalar un servicio.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>602</p></td>
<td style="border:1px solid black;"><p>Se ha creado una tarea del programador.</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar eventos del sistema
  
Esta configuración de directiva determina si se debe auditar el reinicio o cierre de un equipo realizado por un usuario o si se produce un evento que afecta a la seguridad del equipo o al registro de seguridad. Si se configura para registrar los valores **Correcto**, se generará una entrada de auditoría cuando se ejecute correctamente un evento del sistema. Si se configura para registrar los valores **Erróneo**, se generará una entrada de auditoría cuando se intente ejecutar un evento del sistema sin conseguirlo.
  
La tabla siguiente incluye los eventos de tipo Correcto más útiles para esta configuración.
  
**Tabla 4.10 Mensajes de eventos del sistema para Auditar eventos del sistema**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Id. de evento</p></th>  
<th><p>Descripción del evento</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>512</p></td>
<td style="border:1px solid black;"><p>Se está iniciando Windows.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>513</p></td>
<td style="border:1px solid black;"><p>Se está apagando Windows.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>514</p></td>
<td style="border:1px solid black;"><p>La autoridad de seguridad local ha cargado un paquete de autenticación.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>515</p></td>
<td style="border:1px solid black;"><p>Se ha registrado un proceso de inicio de sesión confiable en la autoridad de seguridad local.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>516</p></td>
<td style="border:1px solid black;"><p>Se han agotado los recursos internos asignados para poner en cola de espera los mensajes de eventos de seguridad, lo cual produce la pérdida de algunos mensajes de eventos de seguridad.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>517</p></td>
<td style="border:1px solid black;"><p>Se ha limpiado el registro de auditoría.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>518</p></td>
<td style="border:1px solid black;"><p>El administrador de cuentas de seguridad ha cargado un paquete de notificación.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>519</p></td>
<td style="border:1px solid black;"><p>Un proceso utiliza un puerto LPC (llamada a procedimiento local) no válido para hacerse pasar por un cliente y responder, leer o escribir en un espacio de dirección de cliente.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>520    </p></td>
<td style="border:1px solid black;"><p>Se ha modificado la hora del sistema.</p>
<p><strong>Nota</strong>: esta auditoría aparece normalmente dos veces.</p></td>
</tr>
</tbody>
</table>
<p> </p>

[](#mainsection)[Principio de la página](#mainsection)

### Asignaciones de derechos de usuario

Las asignaciones de derechos de usuario proporcionan a los usuarios y grupos derechos o privilegios de inicio de sesión en los equipos de la organización. Un ejemplo de derecho de inicio de sesión es el derecho de iniciar sesión en un equipo de forma interactiva. Un ejemplo de privilegio consistiría en el derecho de apagar el sistema. Tanto uno como otro tipo los asigna el administrador a los usuarios individuales o grupos como parte de la configuración de seguridad del equipo.

**Nota**: en esta sección, se utiliza "No está definido" para referirse únicamente a los usuarios; los administradores siguen teniendo el derecho de usuario. Los administradores locales pueden realizar cambios, pero cualquier parámetro de Directiva de grupo basado en el dominio los anulará la próxima vez que las directivas de grupo se actualicen o se vuelvan a aplicar.

Puede establecer los valores de configuración de las asignaciones de derechos de usuario en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales**
**\\Asignación de derechos de usuario**

Las asignaciones de derechos de usuario predeterminadas difieren según los diversos tipos de servidores de la organización. Por ejemplo, Windows Server 2003 asigna derechos diferentes a los grupos integrados de los servidores miembro y de los controladores de dominio. (En la siguiente lista no se detallan las similitudes existentes entre los grupos integrados de los distintos tipos de servidor.)

-   **Servidores miembro**

    -   **Usuarios avanzados**. Poseen la mayoría de las capacidades administrativas con algunas restricciones. Pueden ejecutar aplicaciones heredadas además de aplicaciones certificadas para Windows Server 2003 con SP1 o Windows XP.

    -   **HelpServicesGroup**. Es el grupo del Centro de ayuda y soporte técnico. Support\_388945a0 es miembro de este grupo de forma predeterminada.

    -   **TelnetClients**. Los miembros de este grupo tienen acceso al servidor Telnet de la red.

-   **Controladores de dominio**

    -   **Operadores de servidores**. Los miembros de este grupo pueden administrar servidores de dominio.

    -   **Servicios de licencias de Terminal Server**. Los miembros de este grupo tienen acceso a los servidores de licencias de Terminal Server de la red.

    -   **Grupo de acceso de autorización de Windows**.** **Los miembros de este grupo tienen acceso al atributo informático tokenGroupsGlobalAndUniversal en objetos de usuario.

El grupo **Invitados** y las cuentas de usuario Invitado y Support\_388945a0 tienen SID únicos entre diferentes dominios. Por lo tanto, quizás sea necesario modificar esta directiva de grupo para las asignaciones de derechos de usuario en los equipos donde sólo exista el grupo de destino específico. Asimismo, las plantillas de directivas se pueden editar individualmente a fin de incluir los grupos adecuados dentro de los archivos .inf. Por ejemplo, se puede crear una directiva de grupo del controlador de dominio en un controlador de dominio que se encuentre en un entorno de prueba.

**Nota**: a causa de que existen SID únicos entre los miembros del grupo **Invitados**, Support\_388945a0 e Invitado, algunas configuraciones utilizadas para reforzar la seguridad de los servidores no se puede automatizar mediante las plantillas de seguridad incluidas en esta guía. Estas configuraciones se describen en la sección "Configuración de seguridad adicional" de este capítulo.

En esta sección se proporcionan detalles sobre la configuración recomendada de asignaciones de derechos de usuario de la directiva MSBP para los tres entornos definidos en esta guía. Para obtener un resumen de las configuraciones recomendadas en esta sección, consulte el libro de Microsoft Excel "Windows Server 2003 Security Guide Settings" que se incluye con la versión descargable de esta guía. Para obtener más información acerca de la configuración predeterminada y una explicación detallada de las configuraciones descritas en esta sección, consulte la guía complementaria, *Amenazas y contramedidas: configuración de seguridad en Windows* *Server* *2003 y Windows* *XP*.

La tabla siguiente incluye recomendaciones de configuración de las asignaciones de derechos de usuario para los tres entornos definidos en esta guía. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.

**Tabla 4.11 Recomendaciones de configuración de las asignaciones de derechos de usuario**

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
<th><p>Configuración</p></th>
<th><p>Cliente heredado</p></th>
<th><p>Cliente de empresa</p></th>
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Tener acceso a este equipo desde la red</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios autenticados, CONTROLADORES DE DOMINIO DE EMPRESA</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Actuar como parte del sistema operativo</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ajustar las cuotas de memoria para un proceso</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, SERVICIO DE RED, SERVICIO LOCAL</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Permitir el inicio de sesión local</p></td>
<td style="border:1px solid black;"><p>Administradores, Operadores de copia de seguridad, Usuarios avanzados</p></td>
<td style="border:1px solid black;"><p>Administradores, Operadores de copia de seguridad, Usuarios avanzados</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Permitir inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>Administradores y usuarios de equipos de escritorio remotos</p></td>
<td style="border:1px solid black;"><p>Administradores y usuarios de equipos de escritorio remotos</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Realizar copias de seguridad de archivos y directorios</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Omitir la comprobación de recorrido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Usuarios autenticados</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cambiar la hora del sistema</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear un archivo de paginación</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Crear un objeto Token</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear objetos globales</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, SERVICIO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Crear objetos compartidos permanentes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Depurar programas</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Denegar el acceso desde la red a este equipo</p></td>
<td style="border:1px solid black;"><p>INICIO DE SESIÓN ANÓNIMO; Invitados; Support_388945a0;</p>
<p>todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>INICIO DE SESIÓN ANÓNIMO; Invitados; Support_388945a0;</p>
<p>todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>INICIO DE SESIÓN ANÓNIMO; Invitados; Support_388945a0;</p>
<p>todas las cuentas de servicios que NO sean del sistema operativo</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión como trabajo por lotes</p></td>
<td style="border:1px solid black;"><p>Invitados; Support_388945a0</p></td>
<td style="border:1px solid black;"><p>Invitados; Support_388945a0</p></td>
<td style="border:1px solid black;"><p>Invitados; Support_388945a0;</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión como servicio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Invitados; Support_388945a0;</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Denegar inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>Invitados</p></td>
<td style="border:1px solid black;"><p>Invitados</p></td>
<td style="border:1px solid black;"><p>Invitados</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Forzar el apagado de un sistema remoto</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Generar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>SERVICIO DE RED, SERVICIO LOCAL</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Suplantar a un cliente después de la autenticación</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, SERVICIO</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Aumentar la prioridad de programación</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cargar y descargar controladores de dispositivo</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Bloquear páginas en la memoria</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Iniciar sesión como proceso por lotes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Iniciar sesión como servicio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>SERVICIO DE RED</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Administrar registros de auditoría y de seguridad</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Modificar valores de entorno del firmware</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Realizar tareas de mantenimiento de volúmenes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Hacer perfil de un solo proceso</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Perfilar el rendimiento del sistema</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Quitar el equipo de la estación de acoplamiento</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Reemplazar un token a nivel de proceso</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>SERVICIO LOCAL, SERVICIO DE RED</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Restaurar archivos y directorios</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cerrar el sistema</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Sincronizar los datos del servicio de directorio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Tomar posesión de archivos u otros objetos</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
</tbody>  
</table>
  
#### Tener acceso a este equipo desde la red
  
Esta configuración de directiva determina los usuarios y grupos con autorización para conectarse al equipo a través de la red. Es necesaria para una serie de protocolos de red, entre los que se encuentran los protocolos basados en bloques de mensajes de servidor (SMB), NetBIOS, el sistema común de archivos de Internet (CIFS) y el modelo de objetos componentes Plus (COM+).
  
**Tener acceso a este equipo desde la red** se configura como **No está definido** para los entornos LC y EC. Sin embargo, aunque los permisos asignados al grupo de seguridad **Todos** de Windows Server 2003 con SP1 ya no otorgan acceso a los usuarios anónimos, los grupos y las cuentas de invitados todavía pueden tener asignado acceso mediante el grupo de seguridad **Todos**. Por esta razón, en el entorno SSLF se deniega el derecho de usuario **Tener acceso a este equipo desde la red** al grupo de seguridad **Todos**, lo que permite ofrecer una protección frente a los ataques que pretenden tener acceso al dominio como invitado. Sólo los grupos **Administradores**, **Usuarios autenticados** y **ENTERPRISE DOMAIN CONTROLLERS** tienen asignado este derecho de usuario en el entorno SSLF.
  
#### Actuar como parte del sistema operativo
  
Esta configuración de directiva determina si un proceso puede asumir la identidad de cualquier usuario y así tener acceso a los recursos para los que el usuario tiene autorización de acceso. Generalmente, sólo los servicios de autenticación de bajo nivel requieren este derecho de usuario.
  
El derecho de usuario **Actuar como parte del sistema operativo** se configura como **No está definido** para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se establece en un valor nulo o en blanco, que deniega este derecho de usuario a todos los grupos de seguridad y cuentas.
  
#### Ajustar las cuotas de memoria para un proceso
  
Esta configuración de directiva determina si usuarios pueden ajustar la cantidad máxima de memoria disponible para un proceso. Resulta útil para el ajuste de equipos, si bien se puede llegar a abusar de ella. Un atacante podría aprovechar la vulnerabilidad de este derecho de usuario para iniciar un ataque DoS.
  
**Ajustar las cuotas de memoria para un proceso** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna al grupo **Administradores**, SERVICIO DE RED y SERVICIO LOCAL para el entorno SSLF.
  
#### Permitir el inicio de sesión local
  
Esta configuración de directiva determina los usuarios que pueden iniciar sesión de forma interactiva en el equipo especificado. Para que se puedan iniciar sesiones con la combinación de teclas Ctrl+Alt+Supr, el usuario debe disponer de este derecho. Una cuenta con este derecho de usuario se podría utilizar para iniciar una sesión en la consola local del equipo.
  
El derecho de usuario **Permitir el inicio de sesión local** está restringido a los grupos **Administradores**, **Operadores de copia de seguridad** y **Usuarios avanzados** para los entornos LC y EC, lo que permite impedir el inicio de sesión por parte de usuarios no autorizados que deseen elevar sus privilegios o introducir virus en el entorno. Este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Permitir inicio de sesión a través de Servicios de Terminal Server
  
Esta configuración de directiva determina los usuarios o grupos que tienen permiso para iniciar sesión como un cliente de Servicios de Terminal Server.
  
Para los entornos LC y EC, el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** está restringido a los grupos **Administradores** y **Usuarios de escritorio remoto**. Para el entorno SSLF, sólo los miembros del grupo **Administradores** tienen asignado este derecho de usuario.
  
#### Realizar copias de seguridad de archivos y directorios
  
Esta configuración de directiva determina si los usuarios pueden evadir los permisos de archivo y directorio al hacer una copia de seguridad del equipo. Sólo se utiliza cuando una aplicación intenta tener acceso a través de la interfaz de programación de aplicaciones (API) de copia de seguridad NTFS mediante una utilidad de copia de seguridad como NTBACKUP.EXE. De lo contrario, se aplican los permisos normales de directorios y archivos.
  
**Realizar copias de seguridad de archivos y directorios** se configura como **No está definido** para los entornos LC y EC. Este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Omitir la comprobación de recorrido
  
Esta configuración de directiva determina si los usuarios pueden pasar a través de carpetas sin que se compruebe el permiso de acceso especial "Recorrer la carpeta" cuando navegan por una ruta de objeto en el sistema de archivos NTFS o en el Registro. Este derecho de usuario no permite al usuario mostrar el contenido de una carpeta, sólo recorrer los directorios.
  
**Omitir la comprobación de recorrido** se configura como **No está definido** para los entornos LC y EC. Este derecho de usuario se asigna sólo al grupo **Usuarios autenticados** del entorno SSLF.
  
#### Cambiar la hora del sistema
  
Esta configuración de directiva determina los usuarios que pueden cambiar la fecha y hora del reloj interno del equipo. Los usuarios que tienen asignado este derecho de usuario pueden influir en la apariencia de los registros de eventos, que tienen una marca de tiempo según el reloj interno del equipo. Si se cambia la hora del equipo, los registros no reflejarán la hora real en la que se produjeron dichos eventos.
  
**Cambiar la hora del sistema** se configura como **No está definido** para los entornos LC y EC. Este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
**Nota**: las discrepancias entre la hora del equipo local y la de los controladores de dominio pueden acarrear problemas para el protocolo de autenticación Kerberos, que pueden impedir que los usuarios inicien sesión en el dominio u obtengan autorización de acceso a los recursos del dominio tras iniciar una sesión.
  
#### Crear un archivo de paginación
  
Esta configuración de directiva determina si los usuarios pueden crear y cambiar el tamaño de un archivo de paginación. Para realizar esta tarea, el usuario especifica un tamaño de archivo de paginación para una unidad concreta en el cuadro **Opciones de rendimiento** situado en la ficha **Avanzadas** del cuadro de diálogo **Propiedades del sistema**.
  
**Crear un archivo de paginación** se configura como **No definido** para los entornos LC y EC. Este derecho de usuario se asigna sólo al grupo **Administradores** del entorno SSLF.
  
#### Crear un objeto Token
  
Esta configuración de directiva determina si un proceso puede crear un token, que podrá utilizar posteriormente el proceso para obtener acceso a cualquier recurso local cuando use NtCreateToken() u otra API de creación de token.
  
**Crear un objeto Token** se configura como **No está definido** para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
#### Crear objetos globales
  
Esta configuración de directiva permite a los usuarios crear objetos globales que estén disponibles para todas las sesiones. Los usuarios pueden seguir creando objetos específicos para su propia sesión sin tener asignado este derecho de usuario.
  
**Crear objetos globales** se configura como **No está definido** para los entornos LC y EC. Para el entorno SSLF, este derecho de usuario sólo se asigna a los grupos **SERVICIO** y **Administradores**.
  
#### Crear objetos compartidos permanentes
  
Esta configuración de directiva determina si los usuarios pueden crear objetos de directorio en el administrador de objetos, lo que significa que pueden crear carpetas, impresoras y otros objetos compartidos. Es útil para los componentes de modo kernel que amplían el espacio de nombres de objetos y para los componentes que tienen este derecho de usuario intrínsecamente. Por tanto, generalmente no es necesario asignar este derecho de forma específica a los usuarios.
  
**Crear objetos compartidos permanentes** se configura como **No está definido** para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
#### Depurar programas
  
Esta configuración de directiva determina los usuarios que pueden adjuntar un depurador a cualquier proceso o al kernel. Proporciona acceso a componentes críticos y confidenciales del sistema operativo. La depuración de programas no se debe llevar a cabo en entornos de producción, excepto en circunstancias extremas, como cuando es necesario solucionar un problema de una aplicación fundamental para la empresa que no se puede evaluar de forma eficaz en un entorno de prueba.
  
**Depurar programas** se configura como **No está definido** para el entorno LC. Para el entorno EC, este derecho de usuario sólo se asigna al grupo **Administradores**. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
**Nota**: si en Windows Server 2003 con SP1 se quita el derecho de usuario **Depurar programas**, es posible que no se pueda utilizar el servicio Windows Update. Sin embargo, las revisiones se pueden descargar manualmente e instalarse o aplicarse por otros medios. Quitar este derecho de usuario también puede afectar al Servicio de clúster. Para obtener más información, consulte el artículo de Microsoft Knowledge Base sobre [cómo aplicar una configuración de seguridad más restrictiva a un servidor de clúster basado en Windows Server 2003](http://support.microsoft.com/?kbid=891597) en <http://support.microsoft.com/?kbid=891597> (en inglés).
  
#### Denegar el acceso desde la red a este equipo
  
**Nota**: INICIO DE SESIÓN ANÓNIMO, Administrador integrado, Support\_388945a0; Invitado; y todas las cuentas de servicios que NO se incluyan en la plantilla de seguridad .inf. Estas cuentas y grupos tienen identificadores de seguridad (SID) únicos para cada dominio de la organización. Por lo tanto, se deben agregar manualmente. Para más información, consulte la sección "Procedimientos de seguridad manuales" al final de este capítulo.
  
Esta configuración de directiva determina los usuarios que no podrán tener acceso a un equipo a través de la red. Deniega una serie de protocolos de red, entre los que se incluyen los protocolos basados en SMB, NetBIOS, CIFS, HTTP y COM+. Esta configuración de directiva anula el derecho de usuario **Tener acceso a este equipo desde la red** cuando una cuenta de usuario tiene asignada ambas configuraciones.
  
Para los tres entornos definidos en esta guía, se asigna el derecho de usuario **Denegar el acceso desde la red a este equipo** al grupo **Invitados**, INICIO DE SESIÓN ANÓNIMO, Support\_388945a0, así como a todas las cuentas de servicios que no son parte del sistema operativo.
  
La configuración de este parámetro de directiva para otros grupos podría limitar las capacidades de los usuarios asignados a funciones administrativas específicas del entorno. Debe verificar que las tareas delegadas no se vean afectadas de forma negativa.
  
#### Denegar el inicio de sesión como trabajo por lotes
  
**Nota**: INICIO DE SESIÓN ANÓNIMO, Administrador integrado, Support\_388945a0; Invitado; y todas las cuentas de servicios que NO se incluyan en la plantilla de seguridad .inf. Estas cuentas y grupos tienen identificadores de seguridad (SID) únicos para cada dominio de la organización. Por lo tanto, se deben agregar manualmente. Para más información, consulte la sección "Procedimientos de seguridad manuales" al final de este capítulo.
  
Esta configuración de directiva determina las cuentas que no podrán registrarse en el equipo como un trabajo por lotes. Un trabajo por lotes no es un archivo por lotes (.bat), sino más bien un servicio de cola de proceso por lotes. Las cuentas que utilizan el Programador de Tareas para programar los trabajos necesitan este derecho de usuario.
  
El derecho de usuario **Denegar el inicio de sesión como trabajo por lotes** invalida el derecho de usuario **Iniciar sesión como proceso por lotes**, que se podría utilizar para permitir a las cuentas programar trabajos que consumen recursos excesivos del sistema. Esto podría causar una condición DoS. Por esta razón, el derecho de usuario **Denegar el inicio de sesión como trabajo por lotes** se asigna al grupo **Invitados** y a la cuenta de usuario Support\_388945a0 en la directiva de línea de base para los tres entornos definidos en esta guía. Si no se asigna este derecho de usuario a las cuentas recomendadas puede producirse un riesgo de seguridad.
  
#### Denegar el inicio de sesión como servicio
  
Esta configuración de directiva determina si los servicios se pueden iniciar en el contexto de la cuenta especificada.
  
**Denegar el inicio de sesión como servicio** se configura como **No está definido** para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
#### Denegar el inicio de sesión localmente
  
Esta configuración de directiva determina si los usuarios pueden iniciar sesión directamente en el teclado de equipo.
  
**Denegar el inicio de sesión localmente** se configura como **No está definido** para los entornos EC y LC. Sin embargo, este derecho de usuario se asigna sólo al grupo **Invitados** y a la cuenta de usuario Support\_388945a0 para el entorno SSLF. Si no se asigna este derecho de usuario a las cuentas recomendadas puede producirse un riesgo de seguridad.
  
#### Denegar inicio de sesión a través de Servicios de Terminal Server
  
**Nota**: INICIO DE SESIÓN ANÓNIMO, Administrador integrado, Support\_388945a0; Invitado; y todas las cuentas de servicios que NO se incluyan en la plantilla de seguridad .inf. Estas cuentas y grupos tienen identificadores de seguridad (SID) únicos para cada dominio de la organización. Por lo tanto, se deben agregar manualmente. Para más información, consulte la sección "Procedimientos de seguridad manuales" al final de este capítulo.
  
Esta configuración de directiva determina si los usuarios pueden iniciar sesión como clientes de Servicios de Terminal Server. Después de que el servidor miembro de línea de base se una a un entorno de dominio, no es necesario utilizar cuentas locales para tener acceso al servidor desde la red. Las cuentas de dominio pueden tener acceso al servidor con fines de procesamientos administrativos y de usuarios finales.
  
Para los tres entornos definidos en esta guía, el grupo **Invitados** tiene asignado el derecho de usuario **Denegar inicio de sesión a través de Servicios de Terminal Server** de modo que sus miembros no puedan iniciar sesión a través de Servicios de Terminal Server.
  
#### Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo
  
Esta configuración de directiva determina si los usuarios pueden cambiar la configuración **De confianza para la delegación** en un objeto de usuario o equipo en Active Directory. Los usuarios o equipos a los que se asigna este derecho de usuario también deben disponer de acceso de escritura a los indicadores de control de cuenta en el objeto. Un abuso de este derecho de usuario podría causar la suplantación no autorizada de otros usuarios en la red.
  
**Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Forzar el apagado de un sistema remoto
  
Esta configuración de directiva determina si los usuarios pueden apagar los equipos desde ubicaciones remotas de la red. Cualquier usuario que pueda apagar un equipo puede provocar una condición DoS. Por lo tanto, este derecho de usuario debe restringirse al máximo.
  
**Forzar el apagado de un sistema remoto** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo **Administradores** del entorno SSLF.
  
#### Generar auditorías de seguridad
  
Esta configuración de directiva determina si un proceso puede generar registros de auditoría en el registro de seguridad. Como el registro de seguridad se puede utilizar para hacer un seguimiento del acceso no autorizado, un atacante puede utilizar las cuentas que pueden escribir en dicho registro para llenarlo con eventos que carecen de sentido. Si configura el equipo de modo que se sobrescriban los eventos cuando sea necesario, el atacante podría usar esta capacidad para eliminar la evidencia de las actividades no autorizadas que realiza. Si configura el equipo para apagarse cuando no se pueda escribir en el registro de seguridad, un atacante podría utilizar esta capacidad para crear una condición DoS.
  
**Generar auditorías de seguridad** se configura como **No está definido** para los entornos LC y EC. Este derecho de usuario sólo se asigna a las cuentas SERVICIO DE RED y SERVICIO LOCAL para el entorno SSLF.  
  
#### Suplantar a un cliente después de la autenticación
  
Esta configuración de directiva determina si las aplicaciones que se ejecutan en nombre de un usuario autenticado pueden suplantar a clientes. Si este derecho de usuario se requiere para este tipo de suplantación, un usuario no autorizado no podrá convencer a un cliente de que se conecte (por ejemplo, mediante una llamada a procedimiento remoto (RPC) o canalizaciones con nombre) a un servicio creado para suplantar a ese cliente. El usuario no autorizado podría utilizar esta capacidad para elevar sus permisos a niveles administrativos o del sistema.
  
**Suplantar a un cliente después de la autenticación** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo **Administradores** y SERVICIO del entorno SSLF.
  
#### Aumentar la prioridad de programación
  
Esta configuración de directiva determina si los usuarios pueden aumentar la clase de prioridad base de un proceso. El aumento en la prioridad relativa dentro de una clase de prioridad no es una operación de privilegio. Las herramientas administrativas incluidas en el sistema operativo no necesitan este derecho de usuario, aunque sí lo pueden precisar las herramientas de desarrollo de software. Un usuario que tenga asignado este derecho puede aumentar la prioridad de programación de un proceso a tiempo real y dejar poco tiempo de procesamiento para los demás procesos, lo que puede provocar una condición DoS.
  
**Aumentar la prioridad de programación** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Cargar y descargar controladores de dispositivo
  
Esta configuración de directiva determina los usuarios que pueden cargar y descargar dinámicamente controladores de dispositivos. Este derecho de usuario no es necesario si ya existe un controlador firmado para el nuevo hardware en el archivo Driver.cab del equipo. Los controladores de dispositivos se ejecutan como un código con privilegios elevados. Un usuario con el derecho de usuario **Cargar y descargar controladores de dispositivo** puede instalar código malintencionado que se haga pasar por un controlador de dispositivo (bien de forma involuntaria o de otro modo). (Los administradores deben tener más cuidado e instalar sólo aquellos controladores con firmas digitales comprobadas.)
  
**Cargar y descargar controladores de dispositivo** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Bloquear páginas en la memoria
  
Esta configuración de directiva determina si un proceso puede mantener los datos en la memoria física, lo que impide al equipo la paginación de los datos en la memoria virtual del disco. Esto podría degradar en gran medida el rendimiento. Los usuarios que tienen asignado este derecho pueden asignar memoria física a varios procesos y dejar poca o ninguna memoria de acceso aleatorio (RAM) para otros procesos, lo que podría provocar una condición DoS.
  
**Bloquear páginas en la memoria** se configura como **No está definido** para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
#### Iniciar sesión como servicio
  
Esta configuración de directiva determina si una entidad principal de seguridad puede iniciar sesión como un servicio. Los servicios se pueden configurar para ejecutarse con las cuentas Sistema local, Servicio local o Servicio de red, que tienen derechos integrados para iniciar sesión como un servicio. Todo servicio que se ejecute en una cuenta de usuario diferente debe tener asignado este derecho de usuario.
  
**Iniciar sesión como servicio** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna sólo a la cuenta Servicio de red del entorno SSLF.
  
#### Administrar registros de auditoría y de seguridad
  
Esta configuración de directiva** **determina si los usuarios pueden especificar opciones de auditoría de acceso a objetos para recursos individuales, como archivos, objetos de Active Directory y claves del Registro. Este derecho de usuario proporciona muchas capacidades y es necesario vigilarlo de cerca. Cualquier usuario con este derecho puede borrar el registro de seguridad, así como posiblemente evidencias importantes sobre las actividades no autorizadas.
  
**Administrar registros de auditoría y de seguridad** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo **Administradores** del entorno SSLF.
  
**Importante**: Microsoft Exchange Server 2003 modifica este derecho de usuario en la directiva predeterminada de controladores de dominio durante el proceso de instalación. Para obtener más detalles, consulte la información disponible en línea sobre la [implementación de Exchange Server 2003](http://www.microsoft.com/technet/prodtechnol/exchange/guides/e2k3adperm/110e37bf-a68c-47bb-b4d5-1cfd539d9cba.mspx) en [http://www.microsoft.com/technet/prodtechnol/exchange/guides/E2k3ADPerm/110e37bf-a68c-47bb-b4d5-1cfd539d9cba.mspx](http://www.microsoft.com/technet/prodtechnol/exchange/guides/e2k3adperm/110e37bf-a68c-47bb-b4d5-1cfd539d9cba.mspx) (en inglés). Si este derecho de usuario está restringido al grupo del administrador, Exchange registrará con frecuencia mensajes de error en el registro de eventos de aplicación. Si usa Exchange Server 2003, deberá ajustar el valor de esta configuración para los controladores de dominio. Al igual que con el resto de las configuraciones recomendadas en esta guía, es posible que deba realizar algunos ajustes para que las aplicaciones de la organización funcionen con normalidad.
  
#### Modificar valores de entorno del firmware
  
Esta configuración de directiva determina si las variables de entorno del equipo las puede modificar un proceso a través de una API o un usuario a través de **Propiedades del sistema**. Cualquiera que tenga asignado este derecho puede configurar los parámetros de un componente de hardware para que genere errores, lo que puede provocar una corrupción de datos o condición DoS.
  
**Modificar valores de entorno del firmware** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Realizar tareas de mantenimiento de volúmenes
  
Esta configuración de directiva determina si un usuario no administrativo o remoto puede administrar los volúmenes o discos. Un usuario que tenga asignado este derecho puede eliminar un volumen, lo que provocaría una pérdida de datos o condición DoS.
  
**Realizar tareas de mantenimiento de volúmenes** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho del usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Hacer perfil de un solo proceso
  
Esta configuración de directiva determina los usuarios que pueden utilizar herramientas de supervisión de rendimiento para controlar el rendimiento de procesos que no son del sistema. Este derecho de usuario supone una vulnerabilidad moderada puesto que un atacante con esta capacidad podría supervisar el rendimiento de un equipo para identificar los procesos fundamentales que desea atacar directamente. El atacante también puede determinar cuáles son los procesos que se ejecutan en el equipo para poder identificar las contramedidas que deberá evitar, como un software antivirus, un sistema de detección de intrusiones u otros usuarios que tengan iniciada una sesión en el equipo.
  
**Hacer perfil de un solo proceso** se configura como **No está definido** para los entornos LC y EC. Para obtener una mayor seguridad, asegúrese de que el grupo **Usuarios avanzados** no tiene asignado este derecho de usuario en el entorno SSLF; sólo los miembros del grupo **Administradores** deben tener esta capacidad en este tipo de entornos.
  
#### Perfilar el rendimiento del sistema
  
Esta configuración de directiva es semejante a la anterior. Determina si los usuarios pueden supervisar el rendimiento de los procesos del sistema. Este derecho de usuario supone una vulnerabilidad moderada puesto que un atacante con este privilegio podría supervisar el rendimiento de un equipo para identificar los procesos fundamentales que desea atacar directamente. El atacante también podría determinar cuáles son los procesos que se ejecutan en el equipo para poder identificar contramedidas que deberá evitar, como un software antivirus o un sistema de detección de intrusiones.
  
**Perfilar el rendimiento del sistema** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Quitar el equipo de la estación de acoplamiento
  
Esta configuración de directiva determina si los usuarios de equipos portátiles pueden hacer clic en **Retirar equipo** en el menú **Inicio** para desacoplar los equipos. Cualquier usuario que tenga asignado este derecho puede quitar un equipo portátil de la estación de acoplamiento.
  
**Quitar el equipo de la estación de acoplamiento** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario se asigna sólo al grupo de **administradores** del entorno SSLF.
  
#### Reemplazar un token a nivel de proceso
  
Esta configuración de directiva determina si un proceso principal puede reemplazar el token de acceso asociado a un proceso secundario.
  
**Reemplazar un token a nivel de proceso** se configura como **No está definido** para los entornos LC y EC. Sin embargo, este derecho de usuario sólo se asigna a las cuentas SERVICIO LOCAL y SERVICIO DE RED para el entorno SSLF.
  
#### Restaurar archivos y directorios
  
Esta configuración de directiva determina los usuarios que pueden omitir los permisos de archivos, directorios, Registro y otros objetos persistentes cuando restauran copias de seguridad de archivos y directorios. También determina qué usuarios pueden establecer cualquier entidad de seguridad válida principal como propietaria de un objeto.
  
**Restaurar archivos y directorios** se configura como **No está definido** para los entornos LC y EC. Sin embargo, sólo el grupo **Administradores** tiene asignado este derecho de usuario para el entorno SSLF. Las tareas de restauración de archivos generalmente las llevan a cabo los administradores o los miembros de otro grupo de seguridad específicamente delegado, especialmente cuando se trata de servidores o controladores de dominio extremadamente importantes.
  
#### Cerrar el sistema
  
Esta configuración de directiva determina los usuarios que tienen iniciada una sesión local que pueden cerrar el sistema operativo con el comando **Apagar**. Debido a que un uso incorrecto de esta capacidad puede provocar una condición DoS, la capacidad de cerrar los controladores de dominio se debería limitar a un número reducido de administradores que sean de confianza. A pesar de que es necesario iniciar sesión en el servidor para poder cerrar el sistema, es importante tener cuidado con las cuentas y grupos a los que se concede permiso para apagar un controlador de dominio.
  
**Cerrar el sistema** se configura como **No está definido** para los entornos LC y EC. Sin embargo, sólo el grupo **Administradores** tiene asignado este derecho de usuario para el entorno SSLF.
  
#### Sincronizar los datos del servicio de directorio
  
Esta configuración de directiva determina si un proceso puede leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y las propiedades. Este derecho de usuario es necesario para poder usar los servicios de sincronización (Dirsync) de directorios LDAP.
  
La configuración predeterminada de **Sincronizar los datos del servicio de directorio** es **No está definido**, que es un valor suficiente para los entornos LC y EC. Sin embargo, para el entorno SSLF, esta configuración de directiva se configura en un valor nulo o en blanco, lo que significa que ningún grupo de seguridad o cuenta tendrá este derecho de usuario.
  
#### Tomar posesión de archivos u otros objetos
  
Esta configuración de directiva determina si los usuarios puede tomar posesión de cualquier objeto que se pueda asegurar en la red, como los objetos de Active Directory, los archivos y carpetas del sistema de archivos NTFS, las impresoras, las claves del Registro, los servicios, los procesos y los subprocesos.
  
**Tomar posesión de archivos u otros objetos** se configura como **No está definido** para los entornos LC y EC. Sin embargo, debe asignar este derecho de usuario sólo al grupo **Administradores** para el entorno SSLF.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
Las configuraciones de directiva de la sección Opciones de seguridad de la directiva de grupo se utilizan para habilitar o deshabilitar capacidades y características, como el acceso a una unidad de disco o una unidad de CD-ROM y los mensajes de inicio de sesión. También sirven para configurar otras opciones, como las relacionadas con la firma digital de datos, los nombres de cuentas de administrador e invitado y el funcionamiento de la instalación de un controlador.
  
Puede configurar los valores de configuración de las opciones de seguridad en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\**  
**Seguridad\\Opciones**
  
No todas las configuraciones incluidas en esta sección existen en todos los tipos de equipos. Por lo tanto, puede que las configuraciones de la parte Opciones de seguridad de la directiva de grupo que se definen en esta sección se deban modificar manualmente en los equipos en los que estén presentes para que puedan funcionar por completo.
  
En las siguientes secciones se proporcionan detalles sobre la configuración recomendada de las opciones de seguridad de la directiva MSBP para los tres entornos definidos en esta guía. Para obtener un resumen de la configuración recomendada, consulte el libro de Microsoft Excel "Windows Server 2003 Security Guide Settings" que se incluye con la versión descargable de esta guía. Para obtener información acerca de la configuración predeterminada y una explicación detallada de cada una de las configuraciones, consulte la guía complementaria, *Amenazas y contramedidas: configuración de seguridad en Windows* *Server* *2003 y Windows* *XP*.
  
En las tablas de las siguientes secciones se resume la configuración recomendada para los distintos tipos de opciones de seguridad. Las subsecciones a continuación de cada tabla proporcionan información detallada sobre las configuraciones.
  
#### Configuración de cuentas
  
**Tabla 4.12 Opciones de seguridad: recomendaciones de configuración de cuentas**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>estado de la cuenta de administrador</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>estado de la cuenta de invitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Cuentas: estado de la cuenta de administrador
  
Esta configuración de directiva habilita o deshabilita la cuenta de administrador durante el funcionamiento normal. Al iniciar un equipo en modo seguro, la cuenta de administrador siempre está habilitada, independientemente del valor de esta configuración.
  
**Cuentas: estado de la cuenta de administrador** se configura como **No está definido** para los entornos LC y EC y como **Habilitado** para el entorno SSLF.
  
##### Cuentas: estado de la cuenta de invitado
  
Esta configuración de directiva determina si la cuenta de invitado se habilita o deshabilita. Esta cuenta permite que los usuarios de red no autenticados inicien sesión como invitados y obtengan acceso al equipo.
  
**Cuentas: estado de la cuenta de invitado** se configura como **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola
  
Esta configuración de directiva determina si las cuentas locales que no están protegidas por contraseñas se pueden utilizar para iniciar sesión desde ubicaciones distintas a la consola del equipo físico. Si se habilita, las cuentas locales con una contraseña que no esté en blanco no podrán iniciar sesión en la red desde un cliente remoto y las cuentas locales que no estén protegidas por contraseñas sólo podrán iniciar sesión físicamente a través del teclado de un equipo.
  
**Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola** se configura en el valor predeterminado **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Configuración de auditoría
  
**Tabla 4.13 Opciones de seguridad: recomendaciones de configuración de auditoría**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>auditar el acceso de objetos globales del sistema</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>auditar el uso del privilegio de copia de seguridad y restauración</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>apagar el sistema de inmediato si no puede registrar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Auditoría: auditar el acceso de objetos globales del sistema
  
Esta configuración de directiva audita el acceso de los objetos globales del sistema cuando se aplica. Si las configuraciones **Auditoría: auditar el acceso de objetos globales del sistema** y **Auditar acceso a objetos** están habilitadas, se generará un gran número de eventos de auditoría.
  
**Auditoría: auditar el acceso de objetos globales del sistema** se configura en el valor predeterminado **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: los cambios en la configuración de este parámetro de seguridad no tendrán efecto hasta que se reinicie Windows Server 2003.
  
##### Auditoría: auditar el uso del privilegio de copia de seguridad y restauración
  
Esta configuración de directiva determina si se debe auditar el uso de todos privilegios de usuario, incluidos los de copia de seguridad y restauración, cuando la configuración de directiva **Auditar el uso de privilegios** está activa. Si se habilita, se podrían generar un gran número de eventos de seguridad, lo que causaría una respuesta lenta en los servidores y un registro de numerosos eventos no relevantes en el registro de seguridad.
  
Por tanto, **Auditoría: auditar el uso del privilegio de copia de seguridad y restauración** se configura en el valor predeterminado **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: los cambios en la configuración de este parámetro de seguridad no tendrán efecto hasta que se reinicie Windows Server 2003.
  
##### Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad
  
Esta configuración de directiva determina si el equipo se apaga inmediatamente si no puede registrar eventos de seguridad.
  
Se ha determinado que la cantidad de carga administrativa necesaria para habilitar **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad** en los entornos LC y EC es demasiado grande. Por lo tanto, esta configuración de directiva se establece en **Deshabilitado** en la directiva de línea de base para esos entornos. Sin embargo, se configura como **Habilitado** en la directiva de línea de base para el entorno SSLF, porque la carga administrativa adicional se consideró aceptable para impedir la eliminación de eventos del registro de seguridad, salvo que un administrador decida específicamente hacerlo así.
  
#### Configuración de dispositivos
  
**Tabla 4.14 Opciones de seguridad: recomendaciones de configuración de dispositivos**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>permitir el desbloqueo sin tener que iniciar sesión</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>permitir formatear y expulsar medios extraíbles</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>impedir que los usuarios instalen controladores de impresora</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>comportamiento de instalación de controlador no firmado</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
</tr>  
</tbody>  
</table>
  
##### Dispositivos: permitir el desbloqueo sin tener que iniciar sesión
  
Esta configuración de directiva determina si un equipo portátil se puede desacoplar sin que el usuario tenga que iniciar sesión en el equipo. Puede habilitar esta configuración de directiva para que no sea necesario iniciar sesión y permitir el uso de un botón de expulsión en el hardware externo para desacoplar el equipo. Si se deshabilita, los usuarios que no tengan iniciada sesión deberán tener asignado el derecho de usuario **Quitar el equipo de la estación de acoplamiento**.
  
**Dispositivos: permitir el desbloqueo sin tener que iniciar sesión** se configura como **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Dispositivos: permitir formatear y expulsar medios extraíbles
  
Esta configuración de directiva determina qué usuarios pueden dar formato y expulsar medios extraíbles. Los administradores deberían ser los únicos habilitados para expulsar medios extraíbles en los servidores.
  
Por tanto, se recomienda usar el valor predeterminado **Administradores** para **Dispositivos: permitir formatear y expulsar medios extraíbles** en la directiva de línea de base de los tres entornos definidos en esta guía.
  
##### Dispositivos: impedir que los usuarios instalen controladores de impresora
  
Para que un equipo pueda imprimir en una impresora de red, debe tener instalado el controlador para esa impresora. Si se habilita **Dispositivos: impedir que los usuarios instalen controladores de impresora**, sólo los usuarios de los grupos **Administradores** o **Usuarios avanzados** o que tengan privilegios de operador de servidor podrán instalar un controlador de impresora para agregar una impresora de red. Si se deshabilita, cualquier usuario podrá instalar un controlador de impresora.
  
**Dispositivos: impedir que los usuarios instalen controladores de impresora** se configura en el valor predeterminado **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente
  
Esta configuración de directiva determina si los usuarios locales y remotos pueden obtener acceso a un CD-ROM simultáneamente. Si se habilita, sólo el usuario que haya iniciado sesión de forma interactiva podrá tener acceso a medios de CD-ROM extraíbles. Si se habilita y ningún usuario ha iniciado sesión de forma interactiva, se podrá tener acceso al CD-ROM a través de la red.
  
**Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente** se configura como **No está definido** en la directiva de línea de base para los entornos LC y EC. En la directiva de línea de base del entorno SSLF, este parámetro de configuración de directiva se establece como **Deshabilitado.**
  
##### Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente
  
Esta configuración de directiva determina si los usuarios locales y remotos pueden obtener acceso a un medio de disquete extraíble simultáneamente. Si se habilita, sólo el usuario que haya iniciado sesión de forma interactiva podrá tener acceso a medios de disquete extraíbles. Si se habilita y ningún usuario ha iniciado sesión de forma interactiva, se podrá tener acceso a los medios de disquete a través de la red.
  
**Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente** se configura como **No está definido** en la directiva de línea de base para los entornos LC y EC. En la directiva de línea de base del entorno SSLF, este parámetro de configuración de directiva se establece como **Deshabilitado.**
  
##### Dispositivos: comportamiento de instalación de controlador no firmado
  
Esta configuración de directiva determina lo que ocurre ante un intento de instalar un controlador de dispositivo (mediante una API de instalación) no aprobado y firmado por el laboratorio de calidad de hardware de Windows (WHQL). En función de cómo se configure, se impedirá la instalación de controladores no firmados o se advertirá al administrador de que está a punto de instalar un controlador no firmado.
  
**Dispositivos: comportamiento de instalación de controlador no firmado** se puede utilizar para impedir la instalación de controladores que no estén certificados para ejecutarse en Windows Server 2003 con SP1. Sin embargo, esta configuración de directiva se establece en **Avisar pero permitir la instalación** en la directiva de línea de base para los tres entornos definidos en esta guía. Uno de los problemas potenciales de esta configuración es que las secuencias de comandos de instalación desatendida generarán errores cuando se intenten instalar controladores no firmados.
  
#### Configuración de miembros de dominio
  
**Tabla 4.15 Opciones de seguridad: recomendaciones de configuración de miembros de dominio**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>cifrar o firmar datos de canal seguro digitalmente (siempre)</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>cifrar datos de canal seguro digitalmente (cuando sea posible)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Firmar datos de canal seguro digitalmente (cuando sea posible)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>deshabilitar los cambios de contraseña de cuentas de equipo</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>duración máxima de contraseña de cuenta de equipo</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>requerir clave de sesión protegida (Windows 2000, Windows XP o Windows Server 2003)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)
  
Esta configuración de directiva determina si todo el tráfico de canal seguro iniciado por el miembro de dominio se debe firmar o cifrar. Si un equipo se ha configurado para cifrar o firmar siempre los datos de canal seguro, no podrá establecer un canal seguro con un controlador de dominio que no pueda firmar o cifrar todo el tráfico de canal seguro.
  
**Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)** se configura como **Deshabilitado** en la directiva de línea de base para el entorno LC y como **Habilitado** para los entornos EC y SSLF.
  
**Nota**: con el objetivo de aprovechar las ventajas de esta configuración en las estaciones de trabajo y los servidores miembro, todos los controladores de dominio que formen parte del dominio del miembro deben ejecutar Windows NT 4.0 con Service Pack 6a o la versión más reciente de Windows. Además, esta configuración de directiva no es compatible con Windows 98 Second Edition, salvo que esté instalado Dsclient.
  
##### Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)
  
Esta configuración de directiva determina si un miembro de dominio puede intentar negociar el cifrado de todo el tráfico de canal seguro que inicie. Si se habilita, el miembro de dominio solicitará el cifrado de todo el tráfico de canal seguro. Si se deshabilita, el miembro de dominio no podrá negociar el cifrado de canal seguro.
  
Por lo tanto, **Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)
  
Esta configuración de directiva determina si un miembro de dominio puede intentar negociar una firma para todo el tráfico de canal seguro que inicie. El requisito de utilizar una firma protege el tráfico e impide que una persona que eventualmente capture sus datos pueda modificarlo.
  
**Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo
  
Esta configuración de directiva determina si un miembro de dominio puede cambiar periódicamente la contraseña de la cuenta de equipo. Si se habilita, el miembro de dominio no podrá cambiar la contraseña de la cuenta de equipo. Si se deshabilita, el miembro de dominio podrá cambiar la contraseña de la cuenta de equipo tal y como especifique la configuración **Miembro de dominio: duración máxima de contraseña de cuenta de equipo**, cuyo valor predeterminado es cada 30 días.
  
Los equipos que no pueden cambiar automáticamente sus contraseñas de cuenta están expuestos a sufrir un ataque por parte de un usuario que haya averiguado la contraseña de la cuenta de dominio del equipo. Por lo tanto, **Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo** se configura como **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Miembro de dominio: duración máxima de contraseña de cuenta de equipo
  
Esta configuración de directiva determina la antigüedad máxima permitida para la contraseña de una cuenta de equipo. También se aplica a los equipos con Windows 2000, pero no está disponible a través de las herramientas de Administrador de configuración de seguridad de los mismos. De forma predeterminada, los miembros de dominio cambian automáticamente sus contraseñas cada 30 días. Si se aumenta este intervalo de forma significativa o se establece en 0 para que los equipos no cambien las contraseñas, un atacante dispondrá de más tiempo para realizar un ataque de fuerza bruta y averiguar la contraseña de una o más cuentas del equipo.
  
Por lo tanto, **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** se configura como **30 días** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)
  
Esta configuración de directiva determina si la seguridad de clave de 128 bits se requiere para los datos cifrados de canal seguro. Si se habilita, se podrá establecer un canal seguro sin cifrado de 128 bits. Si se deshabilita, el miembro de dominio deberá negociar la seguridad de clave con el controlador de dominio. Las claves de sesión utilizadas para establecer comunicaciones de canal seguro entre controladores de dominio y equipos miembro son mucho más seguras en Windows 2000 que en los sistemas operativos anteriores de Microsoft.
  
Por lo tanto, debido a que los tres entornos de seguridad descritos en esta guía contienen controladores de dominio con Windows 2000 o versiones superiores, **Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)** se configura como **Habilitado** en la directiva de línea de base para los tres entornos.
  
**Nota**: si habilita esta configuración de directiva, no podrá unir equipos que ejecuten Windows 2000 a dominios con Windows NT 4.0.
  
#### Configuración de inicio de sesión interactivo
  
**Tabla 4.16 Opciones de seguridad: recomendaciones de configuración de inicio de sesión interactivo**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>mostrar información de usuario cuando se bloquee la sesión</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Nombre para mostrar del usuario, dominio y nombres de usuario</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>no mostrar el último nombre de usuario</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>no requerir Ctrl+Alt+Supr</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>texto del mensaje para los usuarios que intentan iniciar una sesión</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>título del mensaje para los usuarios que intentan iniciar una sesión</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
<td style="border:1px solid black;"><p>(Consulte con las personas pertinentes en su organización.)</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>pedir al usuario cambiar la contraseña antes de que caduque</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>requerir la autenticación del controlador de dominio para desbloquear el equipo</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>necesita una tarjeta inteligente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>comportamiento de extracción de tarjeta inteligente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
</tr>  
</tbody>  
</table>
  
##### Inicio de sesión interactivo: mostrar información de usuario cuando se bloquee la sesión
  
Esta configuración de directiva determina si el nombre de cuenta del último usuario que inicia sesión en los equipos cliente de la organización se mostrará en la pantalla de inicio de sesión de Windows correspondiente de cada equipo. Si se habilita, los intrusos no podrán ver los nombres de cuenta en las pantallas de los equipos de escritorio o portátiles de la organización.
  
**Inicio de sesión interactivo: mostrar información de usuario cuando se bloquee la sesión** se configura como **No está definido** para los entornos LC y EC, y como **Nombre para mostrar del usuario,** **dominio y nombres de usuario** en la directiva de servidor de línea de base para el entorno SSLF.
  
##### Inicio de sesión interactivo: no mostrar el último nombre de usuario
  
Esta configuración de directiva determina si se mostrará en la pantalla de inicio de sesión de Windows el nombre del último usuario que inició una sesión en el equipo. Si se habilita, no se mostrará el nombre del último usuario que inició una sesión en el cuadro de diálogo **Iniciar sesión en Windows**.
  
**Inicio de sesión interactivo: no mostrar el último nombre de usuario** se configura como **Habilitado** en la directiva de servidor de línea de base para los tres entornos definidos en esta guía.
  
##### Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr
  
Esta configuración de directiva determina si un usuario debe presionar Ctrl+Alt+Supr para poder iniciar sesión. Si se deshabilita, todos los usuarios deberán presionar Ctrl+Alt+Supr para poder iniciar sesión en Windows (a menos que utilicen una tarjeta inteligente para el inicio de sesión de Windows).
  
**Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr** se configura como **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía con el fin de reducir las probabilidades de que un atacante pueda interceptar las contraseñas de los usuarios mediante un programa de caballo de Troya.
  
##### Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión
  
Esta configuración de directiva especifica un mensaje de texto que le aparece a los usuarios cuando inician sesión. Normalmente, este texto se utiliza con fines legales; por ejemplo, para advertir a los usuarios acerca de las ramificaciones del acceso no autorizado, el uso incorrecto de información empresarial o que es posible que se vayan a auditar las acciones que realicen.
  
Se recomienda utilizar la configuración de la opción de seguridad **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión**. Consulte a las personas pertinentes de su organización para decidir el contenido de este texto.
  
**Nota**: tanto **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** como **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar habilitadas para que una u otra funcionen correctamente.
  
##### Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión
  
Esta configuración de directiva permite especificar un título en la barra de título del cuadro de diálogo de inicio de sesión interactivo que aparece cuando los usuarios inician sesión en el equipo. La razón de ser de esta configuración de directiva es la misma que la de **Texto del mensaje para los usuarios que intentan iniciar una sesión**.
  
Por tanto, se recomienda usar la configuración **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión**. Consulte a las personas pertinentes de su organización para decidir el contenido de este texto.
  
**Nota**: tanto **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** como **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar habilitadas para que una u otra funcione correctamente.
  
##### Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)
  
Esta configuración de directiva determina si un usuario puede iniciar sesión en un dominio de Windows con información de cuenta almacenada en caché. La información de inicio de sesión de las cuentas de dominio se puede almacenar localmente en caché de modo que si no es posible ponerse en contacto con un controlador de dominio en los inicios de sesión siguientes, el usuario pueda iniciar sesión. Esta capacidad puede permitir a los usuarios iniciar sesión después de que su cuenta se haya deshabilitado o eliminado, ya que la estación de trabajo no se pone en contacto con el controlador de dominio. Esta configuración de directiva determina el número de usuarios únicos cuya información de inicio de sesión se almacena localmente en caché. Si se configura como 0, se deshabilita la caché de inicio de sesión.
  
**Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** se configura como **0** en la directiva de línea de base para los entornos EC y SSLF. En el entorno LC, se configura como **1** para permitir el acceso a los clientes legítimos que no puedan ponerse en contacto con el controlador de dominio.
  
##### Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque
  
Esta configuración de directiva determina con cuántos días de antelación se advierte a los usuarios de que sus contraseñas están a punto de caducar. En la sección "Directivas de cuentas" del capítulo 3 se recomienda configurar las contraseñas de usuario para que caduquen periódicamente. Si no se notifica a los usuarios cuando sus contraseñas están a punto de caducar, es posible que no se den cuenta de ello hasta que hayan caducado, lo que podría alterar el funcionamiento normal y dificultar a los usuarios locales el cambio de las contraseñas. Cuando las contraseñas caducan sin que el usuario lo espere, los usuarios remotos tampoco pueden iniciar sesión a través de conexiones de redes privadas virtuales (VPN) o de acceso telefónico.
  
Por lo tanto, **Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque** se configura en el valor predeterminado de 14 días en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo
  
Para las cuentas de dominio, esta configuración de directiva determina si es necesario ponerse en contacto con un controlador de dominio para desbloquear un equipo. Esta configuración de directiva aborda una vulnerabilidad potencial similar a la de **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo**. Un usuario podría desconectar el cable de red del servidor y desbloquear el servidor con una contraseña antigua y sin autenticación.
  
Para impedir que esto ocurra, **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Importante**: esta configuración de directiva es aplicable a los equipos que ejecutan Windows 2000, Windows XP y Windows Server 2003, pero no está disponible mediante las herramientas del Administrador de configuración de seguridad de los equipos que ejecutan Windows 2000.
  
##### Inicio de sesión interactivo: necesita una tarjeta inteligente
  
Esta configuración de directiva requiere que los usuarios inicien sesión en un equipo con una tarjeta inteligente. La seguridad mejora cuando los usuarios están obligados a usar contraseñas largas y complejas para autenticarse, sobre todo si deben cambiar sus contraseñas periódicamente. Este enfoque reduce la posibilidad de que un atacante pueda averiguar la contraseña de un usuario a través de un ataque de fuerza bruta. Sin embargo, es difícil conseguir que los usuarios elijan una contraseña segura; además, incluso las contraseñas seguras son vulnerables a los ataques de fuerza bruta.
  
El uso de tarjetas inteligentes en lugar de contraseñas para la autenticación aumenta la seguridad de forma muy notable, ya que, con la tecnología actual, es prácticamente imposible que un atacante suplante a otro usuario. Las tarjetas inteligentes que precisan números de identificación personal (NIP) proporcionan una autenticación de dos factores: el usuario debe, por un lado, poseer la tarjeta inteligente y, por otro, conocer el NIP correspondiente. Un atacante que capturara el tráfico de autenticación entre el equipo del usuario y el controlador de dominio se encontraría con verdaderas dificultades para descifrar el tráfico y, aun consiguiéndolo, la próxima vez que el usuario iniciara sesión en la red, se generaría una clave de sesión nueva para cifrar el tráfico entre el usuario y el controlador de dominio.
  
Microsoft recomienda a las organizaciones migrar a tarjetas inteligentes o a otras tecnologías de autenticación firme. Sin embargo, sólo es necesario habilitar **Inicio de sesión interactivo: necesita una tarjeta inteligente** si ya hay implementadas tarjetas inteligentes. Por este motivo, esta configuración de directiva se establece en **No está definido** en la directiva de línea de base para los entornos LC y EC. Este parámetro de configuración de directiva se establece como **Deshabilitado** en la directiva de línea de base del entorno SSLF.
  
##### Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente
  
Esta configuración de directiva determina lo que ocurre cuando se quita la tarjeta inteligente del lector de tarjetas inteligentes de un usuario que ha iniciado sesión. Si se configura como **Bloquear estación de trabajo**, la estación de trabajo se bloquea cuando se quita la tarjeta inteligente, lo que permite a los usuarios salir de la zona y llevarse las tarjetas inteligentes consigo. Si se configura como **Forzar cierre de sesión**, la sesión del usuario se cerrará automáticamente cuando se quite la tarjeta inteligente.
  
**Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente** se configura como **No está definido** en la directiva de línea de base para el entorno LC y como **Bloquear estación de trabajo** para los entornos EC y SSLF.
  
#### Configuración de cliente de redes de Microsoft
  
**Tabla 4.17 Opciones de seguridad: recomendaciones de configuración de cliente de redes de Microsoft**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>firmar digitalmente las comunicaciones (siempre)</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>firmar digitalmente las comunicaciones (si el servidor lo permite)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>enviar contraseña no cifrada para conectar SMB de otros fabricantes</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)
  
Esta configuración de directiva determina si el componente de cliente SMB requiere la firma de paquetes. Si se habilita, los clientes de redes de Microsoft no podrán comunicarse con un servidor de red de Microsoft salvo que dicho servidor acepte realizar la firma de paquetes SMB. En entornos mixtos con clientes heredados, esta opción se debe establecer en **Deshabilitado**, ya que estos clientes no podrán autenticarse en los controladores de dominio ni obtener acceso a dichos controladores. Sin embargo, se puede usar esta opción en entornos que ejecuten Windows 2000, Windows XP y Windows Server 2003. Los entornos EC y SSLF definidos en esta guía sólo contienen equipos que ejecutan estos sistemas operativos y todos ellos son compatibles con firmas digitales.
  
Por tanto, para aumentar la seguridad de las comunicaciones entre los equipos de este entorno, **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Habilitado** en la directiva de línea de base para los entornos EC y SSLF.
  
##### Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)
  
Esta configuración de directiva determina si el cliente SMB intentará negociar las firmas de paquetes SMB. La implementación de firmas digitales en redes Windows ayuda a impedir el secuestro de las sesiones. Si se habilita, el cliente de redes de Microsoft de los servidores miembro solicitará firmas sólo si los servidores con los que se comunica aceptan la comunicación firmada digitalmente.
  
**Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes
  
Si se habilita, se permitirá al redirector SMB enviar contraseñas de texto sin formato a los servidores SMB que no sean de Microsoft y que no sean compatibles con el cifrado de contraseñas durante la autenticación.
  
**Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes** se configura en el valor predeterminado **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía, salvo que los requisitos de la aplicación anulen la necesidad de mantener secretas las contraseñas.
  
#### Configuración de servidor de red Microsoft
  
**Tabla 4.18 Opciones de seguridad: recomendaciones de configuración de servidor de red Microsoft**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>tiempo de inactividad requerido antes de suspender la sesión</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>firmar digitalmente las comunicaciones (siempre)</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>firmar digitalmente las comunicaciones (si el cliente lo permite)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>desconectar a los clientes cuando termine el tiempo de sesión</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión
  
Esta configuración de directiva determina el tiempo de inactividad continuado que debe transcurrir en una sesión SMB antes de que la sesión se suspenda por inactividad. Los administradores pueden utilizar esta configuración de directiva para controlar el momento en el que un equipo suspende una sesión SMB inactiva. Si se reanuda la actividad del cliente, la sesión se restablece automáticamente.
  
**Servidor de red Microsoft: tiempo de inactividad requerido antes de suspender la sesión** se configura como **15 minutos** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)
  
Esta configuración de directiva determina si el componente de servidor SMB requiere la firma de paquetes antes de permitir cualquier comunicación con un cliente SMB. Windows 2000 Server, Windows 2000 Professional, Windows Server 2003 y Windows XP Professional incluyen versiones de SMB compatibles con la autenticación mutua, que impiden los intentos de secuestrar sesiones y es compatible con la autenticación de mensajes para evitar los ataques de tipo "hombre en el medio". La firma SMB proporciona esta autenticación colocando una firma digital en cada paquete SMB, que posteriormente comprueban el cliente y el servidor. Si los equipos se configuran para ignorar todas las comunicaciones SMB sin firmar, las aplicaciones y los sistemas operativos heredados no se podrán conectar entre sí. Si las firmas SMB se deshabilitan completamente, los equipos son vulnerables a ataques que intenten secuestrar sus sesiones de comunicación.
  
**Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Deshabilitado** en la directiva de línea de base para el entorno LC y como **Habilitado** para los entornos EC y SSLF.
  
##### Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)
  
Esta configuración de directiva determina si el servidor SMB negociará la firma de paquetes SMB con los clientes que lo soliciten. Windows 2000 Server, Windows 2000 Professional, Windows Server 2003 y Windows XP Professional incluyen versiones de SMB compatibles con la autenticación mutua, que bloquea los intentos de secuestro de sesiones y es compatible con la autenticación de mensajes para evitar los ataques de tipo "hombre en el medio". La firma SMB proporciona esta autenticación colocando una firma digital en cada paquete SMB, que posteriormente comprueban el cliente y el servidor. Si los equipos se configuran para ignorar todas las comunicaciones SMB sin firmar, las aplicaciones y los sistemas operativos heredados no se podrán conectar entre sí. Si las firmas SMB se deshabilitan completamente, los equipos son vulnerables a ataques que intenten secuestrar sus sesiones de comunicación.
  
**Servidor de red Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión
  
Esta configuración de directiva determina si se desconectará a los usuarios que se conectan a un equipo de red fuera de las horas de inicio de sesión válidas asignadas a las cuentas de usuario correspondientes. Esta configuración de directiva afecta al componente SMB. Si su organización ha configurado las horas de inicio de sesión de los usuarios, resulta buena idea habilitar esta configuración de directiva. De lo contrario, los usuarios no podrán tener acceso a los recursos de la red fuera de las horas de inicio de sesión que les corresponden o es posible que sigan utilizando los recursos con sesiones iniciadas durante las horas permitidas.
  
**Servidor de red Microsoft: desconectar a los clientes cuando termine el tiempo de sesión** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Configuración de acceso de red
  
**Tabla 4.19 Opciones de seguridad: recomendaciones de configuración de acceso de red**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>permitir traducción SID/nombre anónima</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>no permitir enumeraciones anónimas de cuentas SAM</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>deja los permisos de Todos para aplicarse a usuarios anónimos</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>canalizaciones con nombre accesibles anónimamente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>COMNAP, COMNODE, SQL\QUERY, SPOOLSS, LLSRPC, netlogon, lsarpc, samr, explorador</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>rutas de registro accesibles remotamente</p></td>
<td style="border:1px solid black;"><p>System\CurrentControlSet\Control\Product Options;</p>
<p>System\CurrentControlSet\Control\</p>  
<p>Server Applications;</p>  
<p>Software\Microsoft\</p>  
<p>Windows NT\Current</p>
<p>Versión</p></td>
<td style="border:1px solid black;"><p>System\CurrentControlSet\Control\Product Options;</p>
<p>System\CurrentControlSet\Control\</p>  
<p>Server Applications;</p>  
<p>Software\Microsoft\</p>  
<p>Windows NT\Current</p>
<p>Versión</p></td>
<td style="border:1px solid black;"><p>System\CurrentControlSet\Control\Product Options;</p>
<p>System\CurrentControlSet\Control\</p>  
<p>Server Applications;</p>  
<p>Software\Microsoft\</p>  
<p>Windows NT\Current</p>
<p>Versión</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>rutas y subrutas de registro accesibles remotamente</p></td>
<td style="border:1px solid black;"><p>(consulte la siguiente subsección para ver la información de configuración)</p></td>
<td style="border:1px solid black;"><p>(consulte la siguiente subsección para ver la información de configuración)</p></td>
<td style="border:1px solid black;"><p>(consulte la siguiente subsección para ver la información de configuración)</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>restringir acceso anónimo a canalizaciones con nombre y recursos compartidos</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>recursos compartidos accesibles anónimamente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>modelo de seguridad y para compartir para cuentas locales</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
</tr>  
</tbody>  
</table>
  
##### Acceso de red: permitir traducción SID/nombre anónima
  
Esta configuración de directiva determina si un usuario anónimo puede solicitar atributos SID para otro usuario. Si está habilitada, un usuario con acceso local podrá utilizar el SID conocido de los administradores para obtener el nombre real de la cuenta de administrador integrada, incluso si se ha cambiado su nombre. Esa persona podría entonces utilizar la cuenta para iniciar un ataque de contraseña.
  
**Acceso de red: permitir traducción SID/nombre anónima** se configura como **No está definido** en la directiva de línea de base para los entornos LC y EC. Este parámetro de configuración de directiva se establece como **Deshabilitado** en la directiva de línea de base del entorno SSLF.
  
##### Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM
  
Esta configuración de directiva determina los permisos adicionales que se otorgarán para las conexiones anónimas al equipo. Windows permite a los usuarios anónimos realizar determinadas actividades, como la enumeración de los nombres de las cuentas de dominio. Esta opción resulta útil, por ejemplo, cuando un administrador desea conceder acceso a usuarios en un dominio de confianza que no mantiene una confianza recíproca. Sin embargo, aunque esta configuración esté habilitada, los usuarios anónimos tendrán acceso a cualquier recurso que tenga permisos que incluyan de forma explícita el grupo integrado especial **INICIO DE SESIÓN ANÓNIMO**.
  
**Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM
  
Esta configuración de directiva determina si se permite la enumeración anónima de las cuentas y recursos compartidos SAM.
  
**Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio
  
Esta configuración de directiva determina si las opciones de configuración de **Nombres de usuarios y contraseñas almacenados** guardarán las contraseñas, credenciales o datos de Microsoft .NET Passport para su uso posterior una vez lograda la autenticación en el dominio.
  
**Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: los cambios en la configuración de este parámetro de directiva no tendrán efecto hasta que se reinicie Windows.
  
##### Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos
  
Esta configuración de directiva determina los permisos adicionales que se otorgan para las conexiones anónimas al equipo. Si se habilita, los usuarios anónimos de Windows pueden realizar determinadas actividades, como la enumeración de nombres de cuentas de dominio y recursos compartidos de red. Un usuario no autorizado podría obtener de forma anónima una lista de los nombres de las cuentas y los recursos compartidos y utilizar dicha información para intentar adivinar contraseñas o realizar ataques de ingeniería social.
  
Por lo tanto, **Acceso de red: deja que los permisos de Todos se apliquen a los usuarios anónimos** se configura como **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: los dominios con esta configuración de directiva no podrán establecer o mantener confianzas con dominios o controladores de dominio con Windows NT 4.0.
  
##### Acceso de red: canalizaciones con nombre accesibles anónimamente
  
Esta configuración de directiva determina qué sesiones de comunicación (canalizaciones con nombre) tendrán atributos y permisos que les permitan el acceso anónimo.
  
Debe aplicar los valores predeterminados de la configuración **Acceso de red: canalizaciones con nombre accesibles anónimamente** en el entorno SSLF. Los valores predeterminados constan de las siguientes canalizaciones con nombre:
  
-   COMNAP: acceso de sesión de SNA
  
-   COMNODE: acceso de sesión de SNA
  
-   SQL\\QUERY: acceso de instancia de SQL
  
-   SPOOLSS: servicio de cola de impresión
  
-   LLSRPC: servicio de registro de licencias
  
-   Netlogon: servicio de inicio de sesión de red
  
-   Lsarpc: acceso de LSA
  
-   Samr: acceso de SAM
  
-   explorador: servicio del explorador del equipo
  
    **Importante**: si necesita habilitar esta configuración de directiva, asegúrese de agregar solamente las canalizaciones con nombre que sean necesarias para las aplicaciones de su entorno. Al igual que sucede con todas las configuraciones recomendadas en esta guía, esta configuración de directiva se debe probar detenidamente con antelación en el entorno de producción.
  
##### Acceso de red: rutas de Registro accesibles remotamente
  
Esta configuración de directiva determina las rutas de Registro a las que se podrá obtener acceso a través de la red.
  
**Acceso de red: rutas de Registro accesibles remotamente** se configura en el valor predeterminado en las plantillas de seguridad de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: aunque se establezca esta configuración de directiva, se debe iniciar también el servicio del sistema Registro remoto si los usuarios autorizados deben tener acceso al Registro a través de la red.
  
##### Acceso de red: rutas y subrutas de Registro accesibles remotamente
  
Esta configuración de directiva determina las rutas y subrutas de Registro a las que se podrá obtener acceso a través de la red.
  
Los valores predeterminados de la configuración **Acceso de red: rutas y subrutas de Registro accesibles remotamente** se aplican mediante las plantillas de seguridad de línea de base para los tres entornos definidos en esta guía. Los valores predeterminados constan de las siguientes rutas y subrutas:
  
-   System\\CurrentControlSet\\Control\\Print\\Printers
  
-   System\\CurrentControlSet\\Services\\Eventlog
  
-   Software\\Microsoft\\OLAP Server
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\Print
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows
  
-   System\\CurrentControlSet\\Control\\ContentIndex
  
-   System\\CurrentControlSet\\Control\\Terminal Server
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\UserConfig
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\DefaultUserConfiguration
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\Perflib
  
-   System\\CurrentControlSet\\Services\\SysmonLog
  
##### Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos
  
Esta configuración de directiva se puede utilizar para restringir el acceso anónimo a recursos compartidos y canalizaciones con nombre en las configuraciones siguientes:
  
-   **Acceso de red: canalizaciones con nombre accesibles anónimamente**
  
-   **Acceso de red: recursos compartidos accesibles anónimamente**
  
**Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos** se configura en el valor predeterminado **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Acceso de red: recursos compartidos accesibles anónimamente
  
Esta configuración de directiva determina los recursos compartidos de red a los que podrán obtener acceso los usuarios anónimos. La configuración predeterminada de esta opción tiene pocas repercusiones, ya que todos los usuarios se deben autenticar antes de poder obtener acceso a los recursos compartidos del servidor.
  
**Acceso de red: recursos compartidos accesibles anónimamente** se configura como **No está definido** para los entornos LC y EC y como **Ninguno** para el entorno SSLF.
  
**Nota**: esta configuración de directiva puede ser muy peligrosa, porque cualquier usuario de la red puede tener acceso a los recursos compartidos que se enumeran. Los datos confidenciales podrían verse expuestos o dañados si se habilita esta configuración de directiva.
  
##### Acceso de red: modelo de seguridad y para compartir para cuentas locales
  
Esta configuración de directiva determina cómo se autentican los inicios de sesión de red que utilizan cuentas locales. La configuración **Clásico** ofrece un mejor control sobre el acceso a los recursos y permite otorgar tipos de acceso diferentes a distintos usuarios para el mismo recurso. La configuración **Sólo invitado** permite tratar a todos los usuarios del mismo modo. En este contexto, todos los usuarios se autentican como **Sólo invitado** para que tengan el mismo nivel de acceso a un recurso determinado.
  
**Acceso de red: modelo de seguridad y recursos compartidos para cuentas locales** se configura en el valor predeterminado **Clásico** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Configuración de seguridad de red
  
**Tabla 4.20 Opciones de seguridad: recomendaciones de configuración de seguridad de red**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>nivel de autenticación de LAN Manager</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NTLMv2</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NTLMv2\rechazar LM</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NT Lan Manager versión 2\rechazar Lan Manager y NT Lan Manager</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>requisitos de firma de cliente LDAP</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)</p></td>
<td style="border:1px solid black;"><p>Sin mínimo</p></td>
<td style="border:1px solid black;"><p>Habilitado todas las opciones</p></td>
<td style="border:1px solid black;"><p>Habilitado todas las opciones</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)</p></td>
<td style="border:1px solid black;"><p>Sin mínimo</p></td>
<td style="border:1px solid black;"><p>Habilitado todas las opciones</p></td>
<td style="border:1px solid black;"><p>Habilitado todas las opciones</p></td>
</tr>  
</tbody>  
</table>
  
##### Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña
  
Esta configuración de directiva determina si el valor de hash de LAN Manager (LM) para la contraseña nueva se almacena al cambiar la contraseña. El hash de LM es relativamente débil y propenso a ataques en comparación con el hash de Windows NT, más seguro desde el punto de vista criptográfico.
  
Por este motivo, **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** se configura como **Habilitado** en la directiva de línea de base para los tres entornos de seguridad definidos en esta guía.
  
**Nota**: puede que los sistemas operativos heredados muy antiguos y algunas aplicaciones no funcionen correctamente al habilitar esta configuración de directiva. Asimismo, será necesario cambiar la contraseña de todas las cuentas tras habilitarla.
  
##### Seguridad de red: nivel de autenticación de LAN Manager
  
Esta configuración de directiva determina qué protocolo de autenticación desafío/respuesta se utiliza para los inicios de sesión de red. Esta opción afecta al nivel de protocolo de autenticación utilizado por los equipos cliente, al nivel de seguridad negociado y al nivel de autenticación aceptado por los servidores, tal y como se detalla a continuación. Los números de la siguiente tabla son los valores reales del valor del Registro **LMCompatibilityLevel**.
  
**Tabla 4.21 Configuración del valor del Registro LMCompatibilityLevel**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Valor</p></th>  
<th><p>Protocolo</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan la autenticación Lan Manager y NTLM, y nunca usan la seguridad de sesión NTLMv2.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan la autenticación Lan Manager y NTLM, así como la seguridad de sesión NTLMv2 si el servidor la admite.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan sólo la autenticación NTLM y la seguridad de sesión NTLMv2 si el servidor la admite.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan sólo la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>4</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan sólo la autenticación NTLM y la seguridad de sesión NTLMv2 si el servidor la admite. El controlador de dominio rechaza la autenticación Lan Manager.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>Los clientes utilizan sólo la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. El controlador de dominio rechaza la autenticación Lan Manager y NTLM y únicamente acepta NTLMv2.</p></td>
</tr>  
</tbody>  
</table>
  
Esta configuración de directiva se debe establecer con el nivel más alto que permita el entorno según las siguientes instrucciones:
  
En un entorno que sólo incluya Windows NT 4.0 SP4, Windows 2000 y Windows XP Professional, establezca esta configuración de directiva como **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM** en todos los clientes y, a continuación, como **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM** en todos los servidores una vez configurados todos los clientes. La excepción a esta recomendación son los servidores de enrutamiento y acceso remoto de Windows Server 2003, que no funcionarán correctamente si se configura esta opción de directiva con un valor superior a **Enviar sólo respuesta NTLMv2\\rechazar LM**.
  
Es posible que el entorno EC deba ser compatible con servidores de enrutamiento y acceso remoto; por ello, para este entorno, **Seguridad de red: nivel de autenticación de LAN Manager** se configura como **Enviar sólo respuesta NTLMv2\\rechazar LM** en la directiva de línea de base. Los servidores de enrutamiento y acceso remoto no son compatibles con el entorno SSLF, por lo que esta configuración de directiva se configura como **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM**.
  
Si existen clientes con Windows 9x en los que se puede instalar DSClient, se debe configurar como **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM** en los equipos que ejecuten Windows NT (Windows NT, Windows 2000 y Windows XP Professional). En caso contrario, se debe dejar configurada en un valor no superior a **Enviar sólo respuesta NTLMv2** en la directiva de línea de base para los equipos que no ejecuten Windows 9x, que es la configuración para el entorno LC.
  
Si detecta que hay aplicaciones que dan error cuando se habilita esta configuración de directiva, deshaga el procedimiento realizado paso a paso para descubrir dónde está el error. Como mínimo, esta configuración de directiva se debe establecer en **Enviar Lan Manager y NT Lan Manager: usar la seguridad de sesión NT Lan Manager versión 2 si se negocia** en la directiva de línea de base en todos los equipos. Normalmente, se puede configurar como **Enviar sólo respuesta NTLMv2** en todos los equipos del entorno.
  
##### Seguridad de red: requisitos de firma de cliente LDAP
  
Esta configuración de directiva determina el nivel de firma de datos que se solicita en nombre de los clientes que emiten solicitudes BIND de LDAP. El tráfico de red sin firmar es susceptible de sufrir ataques de tipo "hombre en el medio". En el caso de un servidor LDAP, un atacante podría hacer que un cliente tomara decisiones en función de consultas falsas del cliente LDAP.
  
Por lo tanto, **Seguridad de red: requisitos de firma de cliente LDAP** se configura como **Negociar firma** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)
  
Esta configuración de directiva permite a un cliente solicitar la negociación de confidencialidad de mensaje (cifrado), firma de mensaje, cifrado de 128 bits o seguridad de sesión NTLM versión 2 (NTLMv2). Establezca esta configuración de directiva en un nivel de seguridad tan alto como sea posible, pero recuerde que todavía necesitará permitir el funcionamiento de las aplicaciones en la red. Una configuración apropiada en esta opción de directiva ayudará a asegurar que el tráfico de red desde los servidores basados en SSP de NTLM esté protegido de los ataques de tipo "hombre en el medio" y de la exposición de los datos.
  
**Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)** se configura como **Sin mínimo** en la directiva de línea de base para el entorno LC. Toda configuración se habilita para los entornos EC y SSLF.
  
##### Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)
  
Esta configuración de directiva permite a un servidor solicitar la negociación de confidencialidad de mensaje (cifrado), integridad de mensaje, cifrado de 128 bits o seguridad de sesión NTLMv2. Establezca esta configuración de directiva en un nivel de seguridad tan alto como sea posible, pero recuerde que todavía necesitará permitir el funcionamiento de las aplicaciones en la red. Al igual que en el caso de la configuración de directiva anterior, una configuración apropiada de esta opción de directiva ayudará a asegurar que el tráfico de red desde los clientes basados en SSP de NTLM esté protegido de los ataques de tipo "hombre en el medio" y de la exposición de los datos.
  
**Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)** se configura como **Sin mínimo** en la directiva de línea de base para el entorno LC. Toda configuración se habilita para los entornos EC y SSLF.
  
#### Configuración de Consola de recuperación
  
**Tabla 4.22 Opciones de seguridad: recomendaciones de configuración de Consola de recuperación**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>permitir el inicio de sesión administrativo automático</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>permitir la copia de disquetes y el acceso a todas las unidades y carpetas</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Consola de recuperación: permitir el inicio de sesión administrativo automático
  
Esta configuración de directiva determina si la contraseña de la cuenta de administrador se debe proporcionar antes de que se conceda el acceso al equipo. Si se habilita, la Consola de recuperación no requiere que se especifique una contraseña e inicia automáticamente la sesión en el equipo. La Consola de recuperación puede ser muy útil cuando es necesario trabajar con equipos que tienen problemas de inicio. No obstante, habilitar esta configuración puede ser perjudicial porque cualquier persona puede acercarse al servidor, desconectarlo de la alimentación eléctrica para apagarlo, reiniciarlo, seleccionar **Consola de recuperación** en el menú **Reiniciar** y asumir pleno control del servidor.
  
Por lo tanto, **Consola de recuperación: permitir el inicio de sesión administrativo automático** se configura en el valor predeterminado **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía. Para utilizar la Consola de recuperación cuando esta opción esté deshabilitada, el usuario deberá introducir un nombre de usuario y una contraseña para obtener acceso a la cuenta de la Consola de recuperación.
  
##### Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas
  
Puede habilitar esta configuración de directiva para que esté disponible el comando **SET** de la Consola de recuperación, que permite establecer las siguientes variables de entorno de la Consola de recuperación:
  
-   **AllowWildCards**: habilita la compatibilidad con comodines para algunos comandos (como el comando DEL).
  
-   **AllowAllPaths**: permite el acceso a todos los archivos y carpetas del equipo.
  
-   **AllowRemovableMedia**: permite la copia de archivos en medios extraíbles, como un disquete.
  
-   **NoCopyPrompt**: no se solicita confirmación al sobrescribir un archivo existente.
  
Para una seguridad máxima, **Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas** se configura como **Deshabilitado** en la directiva de línea de base para el entorno SSLF. Sin embargo, esta configuración de directiva se establece como **Habilitada** para los entornos LC y EC.
  
#### Configuración de apagado
  
**Tabla 4.23 Opciones de seguridad: recomendaciones de configuración de apagado**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>permitir apagar el sistema sin tener que iniciar sesión</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>borrar el archivo de páginas de la memoria virtual</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Apagado: permitir apagar el sistema sin tener que iniciar sesión
  
Esta configuración de directiva determina si un usuario que no es necesario que inicie sesión en el sistema operativo Windows puede apagar un equipo. Los usuarios que pueden obtener acceso a la consola pueden apagar el sistema. Un atacante o usuario con malas intenciones podría conectarse al servidor mediante Servicios de Terminal Server y apagarlo o reiniciarlo sin necesidad de identificarse.
  
Por lo tanto, **Apagado: permitir apagar el sistema sin tener que iniciar sesión** se configura en el valor predeterminado **Deshabilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Apagado: borrar el archivo de paginación de la memoria virtual
  
Esta configuración de directiva determina si el archivo de paginación de memoria virtual se borra cuando se apaga el equipo. Si está habilitada, el archivo de paginación del sistema se borra cada vez que el equipo se apaga debidamente. Si se habilita esta configuración de directiva, el archivo de hibernación (Hiberfil.sys) se borra también cuando se deshabilita la hibernación en un equipo portátil. Apagar y reiniciar el servidor llevará más tiempo y se notará especialmente en los servidores que tengan archivos de paginación más grandes.
  
Por estas razones, **Apagado: borrar el archivo de paginación de la memoria virtual** se configura como **Habilitado** en los tres entornos definidos en esta guía.
  
**Nota**: un atacante que tenga acceso físico al servidor podría simplemente desconectar el servidor de la fuente de alimentación para pasar por alto esta contramedida.
  
#### Configuración de la criptografía de sistema
  
**Tabla 4.24 Opciones de seguridad: recomendaciones de configuración de criptografía de sistema**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>forzar la protección de clave segura para las claves de usuario almacenadas en el equipo</p></td>
<td style="border:1px solid black;"><p>Se preguntará al usuario cuando se use la clave por primera vez</p></td>
<td style="border:1px solid black;"><p>Se preguntará al usuario cuando se use la clave por primera vez</p></td>
<td style="border:1px solid black;"><p>El usuario debe introducir una contraseña cada vez que use una clave</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Criptografía de sistema: establece una protección fuerte de clave para las aquellas claves del usuario en el equipo
  
Esta configuración de directiva determina si las claves privadas de los usuarios, como las claves S-MIME, requieren una contraseña para poder utilizarse. Si se configura para que los usuarios deban proporcionar una contraseña (distinta de su contraseña de dominio) cada vez que utilicen una clave, será más difícil que un atacante tenga acceso a las claves de usuario almacenadas localmente, incluso si éste descubre las contraseñas de inicio de sesión.
  
Para satisfacer los requisitos de funcionalidad de los entornos LC y EC, **Criptografía de sistema: establece una protección fuerte de clave para las aquellas claves del usuario en el equipo** se configura como **Se preguntará al usuario cuando se use la clave por primera vez** en la directiva de línea de base. Para proporcionar una seguridad adicional, esta configuración de directiva se establece en **El usuario debe introducir una contraseña cada vez que use una clave** para el entorno SSLF.
  
##### Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash
  
Esta configuración de directiva determina si el proveedor de seguridad de Transport Layer Security/Secure Sockets Layer (TLS/SSL) es compatible sólo con el conjunto cifrado TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA. Aunque esta configuración de directiva aumente la seguridad, la mayoría de los sitios web públicos protegidos con TLS o SSL no son compatibles con estos algoritmos. Muchos equipos cliente tampoco están configurados para ofrecer compatibilidad con estos algoritmos.
  
Por estas razones, **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** se configura como **Deshabilitado** en la directiva de línea de base para los entornos LC y EC. Esta configuración de directiva se establece como **Habilitado** para el entorno SSLF.
  
#### Configuración de objetos de sistema
  
**Tabla 4.25 Opciones de seguridad: recomendaciones de configuración de objetos de sistema**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>propietario predeterminado para objetos creados por miembros del grupo de administradores</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>reforzar los permisos predeterminados de los objetos internos del sistema (p. ej., vínculos simbólicos)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores
  
Esta configuración de directiva determina si el grupo **Administradores** o un creador de objetos es el propietario predeterminado de cualquier objeto de sistema que se haya creado. Cuando se crean objetos de sistema, la propiedad de éstos indicará qué cuenta los ha creado, en lugar del grupo **Administradores**, que es más genérico.
  
**Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores** se configura como **Creador de objetos** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows
  
Esta configuración de directiva determina si no se aplica diferenciación de mayúsculas y minúsculas en todos los subsistemas. El subsistema Microsoft Win32® no distingue mayúsculas de minúsculas. No obstante, el núcleo admite la distinción de mayúsculas y minúsculas para otros subsistemas, como la Interfaz de sistema operativo portátil de UNIX (POSIX). Dado que Windows no distingue mayúsculas de minúsculas y que el subsistema POSIX es compatible con esta característica, si no se aplica esta configuración es posible que un usuario del subsistema POSIX cree un archivo con el mismo nombre que otro si utiliza mayúsculas y minúsculas en el nombre. Esto podría bloquear el acceso de otro usuario a estos archivos con herramientas normales de Win32, porque sólo estaría disponible uno de esos archivos.
  
Para garantizar la coherencia de los nombres de archivo, **Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema (p. ej. vínculos simbólicos)
  
Esta configuración de directiva determina la seguridad de la lista de control de acceso discrecional (DACL) predeterminada para los objetos y ayuda a proteger los objetos que pueden ser localizados y compartidos entre procesos. Para reforzar la seguridad de la lista DACL, se puede usar el valor predeterminado **Habilitado**, que permite a los usuarios que no son administradores leer objetos compartidos, pero no modificar ninguno que no hayan creado.
  
**Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema (p. ej. vínculos simbólicos)** se configura en el valor predeterminado **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Configuración del sistema
  
**Tabla 4.26 Opciones de seguridad: recomendaciones de configuración del sistema**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Configuración del sistema: Subsistemas opcionales</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Configuración del sistema: Subsistemas opcionales
  
Esta configuración de directiva determina los subsistemas que se utilizarán para ofrecer compatibilidad con las aplicaciones del entorno. El valor predeterminado de esta configuración de directiva en Windows Server 2003 es **POSIX**.
  
Para deshabilitar el subsistema POSIX, **Configuración del sistema: Subsistemas opcionales** se configura como **Ninguno** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
##### Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software
  
Esta configuración de directiva determina si se procesan los certificados digitales cuando se habilitan las directivas de restricción de software y un usuario o proceso intenta ejecutar software con una extensión de nombre de archivo .exe. Habilita o deshabilita las reglas de certificado (un tipo de regla de directivas de restricción de software). Con las directivas de restricción de software, se puede crear una regla de certificado que permita o impida la ejecución de software firmado con Authenticode®, según el certificado digital asociado al software. Para que las reglas de certificado surtan efecto en las directivas de restricción de software, se debe habilitar esta configuración de directiva.
  
**Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software** se configura como **Habilitado** en el entorno SSLF. Sin embargo, se configura como **Deshabilitado** en el entorno EC y como **No está definido** en el entorno LC debido a la posible repercusión sobre el rendimiento.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Registro de eventos
  
El registro de eventos registra los eventos del equipo, y el registro de seguridad, los eventos de auditoría. El contenedor del registro de eventos de la directiva de grupo se utiliza para definir los atributos de los registros de eventos de aplicación, seguridad y sistema; por ejemplo, el tamaño máximo del registro, los derechos de acceso para cada registro, y la configuración y los métodos de retención. Las configuraciones de los registros de eventos de aplicación, seguridad y sistema se establecen en la directiva MSBP y se aplican a todos los servidores miembro del dominio.
  
Puede establecer la configuración del registro de eventos en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Registro de eventos**
  
En esta sección se proporcionan detalles sobre la configuración recomendada para los registros de eventos en la directiva MSBP para los tres entornos definidos en esta guía. Para obtener un resumen de las configuraciones recomendadas en esta sección, consulte el libro de Microsoft Excel "Windows Server 2003 Security Guide Settings", que está disponible en la versión descargable de esta guía. Para obtener información acerca de la configuración predeterminada y una explicación detallada sobre cada una de las configuraciones descritas en este capítulo, consulte la guía complementaria *Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows* *XP*, que está disponible en [http://go.microsoft.com/fwlink/?LinkId=15159](http://go.microsoft.com/fwlink/?linkid=15159).
  
La tabla siguiente incluye recomendaciones de configuración del registro de eventos para los tres entornos definidos en esta guía. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.27 Recomendaciones de configuración del registro de eventos**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tamaño máximo del registro de la aplicación</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Tamaño máximo del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tamaño máximo del registro del sistema</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro del sistema</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Método de retención del registro de la aplicación</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Método de retención del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Método de retención del registro del sistema</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
</tbody>  
</table>
  
#### Tamaño máximo del registro de la aplicación
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de aplicación, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos de tamaño del registro de aplicación varían en función de la plataforma y la necesidad de disponer de registros históricos de eventos relacionados con aplicaciones.
  
**Tamaño máximo del registro de la aplicación** se configura en el valor predeterminado **16.384 KB** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Tamaño máximo del registro de seguridad
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de seguridad, que tiene una capacidad máxima de 4 GB. Debe configurar el registro de seguridad con un mínimo de 80 MB en los controladores de dominio y servidores independientes, capacidad que debería ser suficiente para almacenar la información para realizar auditorías. El modo de establecer esta configuración de directiva para otros equipos dependerá de factores como la frecuencia con que se revisará el registro, el espacio disponible en el disco, etc.
  
**Tamaño máximo del registro de seguridad** se configura como **81.920 KB** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Tamaño máximo del registro del sistema
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos del sistema, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos de tamaño del registro de sistema varían en función de la plataforma y la necesidad de disponer de registros históricos.
  
**Tamaño máximo del registro del sistema** se configura en el valor predeterminado **16.384 KB** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones
  
Esta configuración de directiva determina si a los invitados se les deniega el acceso al registro de eventos de aplicación. De forma predeterminada, en Windows Server 2003 con SP1 los invitados tienen prohibido el acceso a todos los equipos. Por lo tanto, esta configuración de directiva no tiene efecto real en equipos con configuraciones predeterminadas.
  
Sin embargo, como esta configuración se considera una medida de defensa exhaustiva que no tiene efectos secundarios, **Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: esta configuración no aparece en el objeto Directiva de equipo local.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro de seguridad
  
Esta configuración de directiva determina si a los invitados se les deniega el acceso al registro de eventos de seguridad. Un usuario debe tener asignado el derecho de usuario **Administrar registros de auditoría y de seguridad** (no se define en esta guía) para obtener acceso al registro de seguridad. Por lo tanto, esta configuración de directiva no tiene efecto real en equipos con configuraciones predeterminadas.
  
Sin embargo, como esta configuración se considera una medida de defensa exhaustiva que no tiene efectos secundarios, **Evitar que el grupo de invitados locales tenga acceso al registro de seguridad** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: esta configuración no aparece en el objeto Directiva de equipo local.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro del sistema
  
Esta configuración de directiva determina si a los invitados se les deniega el acceso al registro de eventos del sistema. De forma predeterminada, en Windows Server 2003 con SP1 los invitados tienen prohibido el acceso a todos los equipos. Por lo tanto, esta configuración de directiva no tiene efecto real en equipos con configuraciones predeterminadas.
  
Sin embargo, como esta configuración se considera una medida de defensa exhaustiva que no tiene efectos secundarios, **Evitar que el grupo de invitados locales tenga acceso al registro del sistema** se configura como **Habilitado** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
**Nota**: esta configuración no aparece en el objeto Directiva de equipo local.
  
#### Método de retención del registro de la aplicación
  
Esta configuración de directiva determina el método de "ajuste" del registro de aplicación. Es de gran importancia que el registro de aplicación se archive regularmente si se necesita disponer de eventos históricos con fines de argumentación y solución de problemas. Si se sobrescriben los eventos según se necesiten, el registro siempre almacenará los eventos más recientes, aunque esta configuración pueda tener como resultado una pérdida de datos históricos.
  
**Método de retención del registro de la aplicación** se configura como **Según se necesite** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Método de retención del registro de seguridad
  
Esta configuración de directiva determina el método de "ajuste" del registro de seguridad. Es de gran importancia que el registro de seguridad se archive regularmente si se necesita disponer de eventos históricos con fines de argumentación y solución de problemas. Si se sobrescriben los eventos según se necesiten, el registro siempre almacenará los eventos más recientes, aunque esta configuración pueda tener como resultado una pérdida de datos históricos.
  
**Método de retención del registro de seguridad** se configura como **Según se necesite** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
#### Método de retención del registro del sistema
  
Esta configuración de directiva determina el método de "ajuste" del registro del sistema. Es de gran importancia que los registros se archiven regularmente si se necesita disponer de eventos históricos con fines de argumentación y solución de problemas. Si se sobrescriben los eventos según se necesiten, el registro siempre almacenará los eventos más recientes, aunque esta configuración pueda tener como resultado una pérdida de datos históricos.
  
**Método de retención del registro del sistema** se configura como **Según se necesite** en la directiva de línea de base para los tres entornos definidos en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas de registro adicionales
  
Se han creado entradas del Registro (también conocidas como *valores del Registro*) adicionales para los archivos de plantilla de seguridad de línea de base que no se definen en el archivo de la plantilla administrativa (.adm) predeterminada para los tres entornos de seguridad definidos en esta guía. En los archivos .adm se definen las directivas y restricciones del escritorio, del shell y de la seguridad para Windows Server 2003.
  
Estas entradas del Registro se incluyen en las plantillas de seguridad (en la sección "Opciones de seguridad") para automatizar las modificaciones. Si se quita la directiva, no se quitarán automáticamente estas entradas del Registro; éstas se deben modificar manualmente mediante una herramienta de edición del Registro como Regedt32.exe. Se aplican las mismas entradas del Registro a los tres entornos.
  
En esta guía se incluyen entradas del Registro adicionales que se agregan al Editor de configuración de seguridad (SCE). Para agregar estas entradas del Registro, es necesario modificar el archivo Sceregvl.Inf (disponible en la carpeta **%windir%\\inf**) y volver a registrar el archivo Scecli.dll. Las entradas de seguridad originales, así como las adicionales, se encuentran en **Directivas locales\\Seguridad** en los complementos y las herramientas que se han indicado previamente en este capítulo. Es necesario actualizar el archivo Sceregvl.inf y registrar el archivoScecli.dll de nuevo en los equipos en los que se vayan a editar las plantillas de seguridad y las directivas de grupo que se facilitan con esta guía. Hay disponible más información acerca de cómo actualizar estos archivos en la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en [http://go.microsoft.com/fwlink/?LinkId=15159](http://go.microsoft.com/fwlink/?linkid=15159).
  
Esta sección sólo constituye un resumen de las entradas adicionales del Registro que se describen más detalladamente en la guía complementaria. Para obtener más información acerca de la configuración predeterminada y una explicación detallada de las configuraciones descritas en esta sección, consulte la guía complementaria *Amenazas y contramedidas: configuración de seguridad en Windows* *Server* *2003 y Windows* *XP*.
  
#### Consideración de seguridad sobre los ataques en red
  
Los ataques por denegación de servicio (DoS) son ataques de red que intentan hacer que un equipo o servicio determinado de un equipo no se encuentre disponible para los usuarios de la red. Los ataques de denegación de servicio (DoS) son difíciles de combatir.
  
Para prevenirlos, sería recomendable mantener el equipo actualizado con las últimas correcciones de seguridad y reforzar la seguridad de la pila del protocolo TCP/IP en aquellos equipos en los que se ejecute Windows Server 2003 con SP1 y que estén expuestos a posibles atacantes. La configuración predeterminada de la pila TCP/IP se optimiza para el control del tráfico de la intranet estándar. En el caso de que se conecte un equipo directamente a Internet, Microsoft recomienda la consolidación de la pila TCP/IP frente a los ataques por servicio denegado (DoS).
  
Puede agregar los valores del Registro de la siguiente tabla al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**
  
subclave.
  
**Tabla 4.28 Recomendaciones sobre las entradas del Registro de TCP/IP**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Entrada del Registro</p></th>  
<th><p>Formato</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>EnableICMPRedirect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SynAttackProtect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>EnableDeadGWDetect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>KeepAliveTime</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>300.000</p></td>
<td style="border:1px solid black;"><p>300.000</p></td>
<td style="border:1px solid black;"><p>300.000</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>DisableIPSourceRouting</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TcpMaxConnectResponseRetransmissions</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TcpMaxDataRetransmissions</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>3</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>PerformRouterDiscovery</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
</tbody>  
</table>
  
#### Otras entradas del Registro
  
La siguiente tabla incluye otras entradas del Registro recomendadas que no son específicas de TCP/IP. La información adicional sobre cada entrada se proporciona en las subsecciones que se incluyen después de la tabla.
  
**Tabla 4.29 Recomendaciones sobre otras entradas del Registro**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Entrada del Registro</p></th>  
<th><p>Formato</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0xFF</p></td>
<td style="border:1px solid black;"><p>0xFF</p></td>
<td style="border:1px solid black;"><p>0xFF</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)</p></td>
<td style="border:1px solid black;"><p>Cadena</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>90</p></td>
<td style="border:1px solid black;"><p>90</p></td>
<td style="border:1px solid black;"><p>90</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (AutoReboot) Allow Windows to automatically restart after a system crash (recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (AutoShareWks) Enable Administrative Shares (recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (DisableSavePassword) Prevent the dial-up password from being saved (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>3</p></td>
</tr>  
</tbody>  
</table>
  
##### Configure NetBIOS Name Release Security: Allow the computer to ignore NetBIOS name release requests except from WINS servers
  
Esta entrada aparece como **MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers** en SCE.
  
NetBIOS sobre TCP/IP es un protocolo de red que, entre otras cosas, proporciona una forma de resolver fácilmente los nombres NetBIOS registrados en equipos basados en Windows en las direcciones IP configuradas en los mismos. Este valor determina si el equipo libera su nombre NetBIOS al recibir una solicitud de liberación de nombre.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Netbt\\Parameters\\**
  
subclave.
  
##### Disable Auto Generation of 8.3 File Names: Enable the computer to stop generating 8.3 style filenames
  
Esta entrada aparece como **MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)** en SCE.
  
Windows Server 2003 con SP1 es compatible con los formatos de nombre de archivo 8.3 para la compatibilidad con aplicaciones de 16 bits anteriores. La convención del nombre de archivo 8.3 es un formato de nombre que sólo permite nombres de archivo con una longitud máxima de ocho caracteres.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\FileSystem\\**
  
subclave.
  
##### Disable Autorun: Disable Autorun for all drives
  
Esta entrada del Registro aparece como **MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)** en SCE.
  
La ejecución automática empieza a leer la información de una unidad del equipo tan pronto como se insertan los medios. Como resultado, elementos como el archivo de instalación (en el caso de programas) o el sonido (en el caso de contenido de audio) se inician inmediatamente.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\Explorer\\**
  
subclave.
  
##### Make Screensaver Password Protection Immediate: The time in seconds before the screen saver grace period expires (0 recommended)
  
Esta entrada aparece como **MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)** en SCE.
  
Windows incluye un período de gracia que abarca desde que se inicia el protector de pantalla hasta el momento en el que se bloquea la consola de forma automática y se habilita el bloqueo del protector de pantalla.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\**  
**Winlogon\\**
  
subclave.
  
##### Security Log Near Capacity Warning: Percentage threshold for the security event log at which the system will generate a warning
  
Esta entrada aparece como **MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning** en SCE.
  
Esta opción está disponible con el SP3 de Windows 2000. Genera una auditoría de seguridad en el registro de seguridad cuando el tamaño del mismo alcanza un umbral definido por el usuario. Por ejemplo, si se configura el valor de esta entrada del Registro en 90 y el registro de seguridad alcanza un 90% de capacidad, el registro mostrará la siguiente entrada con el Id. de evento 523: "The security event log is 90 percent full."
  
**Nota**: si la configuración del registro se establece para **Sobrescribir eventos cuando sea necesario** o **Sobrescribir eventos que tengan más de x días**, no se generará este evento.
  
Puede agregar este valor del Registro al archivo de plantilla de seguridad en la
  
**HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Services\\Eventlog\\Security\\**
  
subclave.
  
##### Enable Safe DLL Search Order: Enable Safe DLL search mode (recommended)
  
Esta entrada aparece como **MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)** en SCE.
  
El orden de búsqueda de DLL se puede configurar para que los archivos DLL solicitados por los procesos en ejecución se busquen de una de estas dos formas:
  
-   Buscar primero en las carpetas especificadas en la ruta de acceso del sistema y, a continuación, buscar en la carpeta de trabajo actual.
  
-   Buscar primero en la carpeta de trabajo actual y, a continuación, buscar en las carpetas especificadas en la ruta de acceso del sistema.
  
El valor del Registro se configura como 1, lo que hace que el equipo busque primero en las carpetas especificadas en la ruta de acceso del sistema y, a continuación, en la carpeta de trabajo actual. Si esta entrada se configura como 0, el sistema busca primero en la carpeta de trabajo actual y, a continuación, en las carpetas especificadas en la ruta de acceso del sistema.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Control\\Session Manager\\**
  
subclave.
  
##### Automatic Reboot: Allow Windows to automatically restart after a system crash
  
Esta entrada aparece como **MSS: (AutoReboot) Allow Windows to automatically restart after a system crash** **(recommended except for highly secure environments)** en SCE.
  
Cuando esta entrada está habilitada, un servidor puede reiniciarse automáticamente tras un bloqueo grave. Está habilitada de forma predeterminada, lo que no es recomendable para los servidores altamente seguros.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\CrashControl\\**
  
subclave.
  
##### Automatic Logon: Enable Automatic Logon
  
Esta entrada aparece como **MSS: (AutoAdminLogon) Enable Automatic Logon** **(not recommended)** en SCE. Esta entrada no está habilitada de forma predeterminada y no debe usarse nunca en un servidor, prácticamente en ninguna circunstancia imaginable.
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[Habilitar el inicio de sesión automático en Windows X](http://support.microsoft.com/default.aspx?kbid=315231)" en [http://support.microsoft.com/?kbid=315231](http://support.microsoft.com/default.aspx?kbid=315231).
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\**  
**Winlogon\\**
  
subclave.    
  
##### Administrative Shares: Enable Administrative Shares
  
Esta entrada aparece como **MSS: (AutoShareWks) Enable Administrative Shares** **(recommended except for highly secure environments)** en SCE. De forma predeterminada, cuando las funciones de red de Windows están activadas en un servidor, Windows crea recursos compartidos administrativos ocultos, lo que no es recomendable en servidores altamente seguros.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\RasMan\\Parameters\\**
  
subclave.
  
##### Disable Saved Passwords: Prevent the dial-up password from being saved
  
Esta entrada aparece como **MSS: (DisableSavePassword) Prevent the dial-up password from being saved** **(recommended)** en SCE. De forma predeterminada, Windows ofrecerá la opción de guardar las contraseñas para las conexiones de acceso telefónico y VPN, lo que no es recomendable en un servidor.
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\LanmanServer\\**  
**Parameters\\**
  
subclave.
  
##### Enable IPSec to protect Kerberos RSVP Traffic: Enable NoDefaultExempt for IPSec Filtering
  
Esta entrada aparece como **MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering** **(recommended)** en SCE. En la ayuda en pantalla de Microsoft Windows Server 2003 se detallan las exenciones predeterminadas a los filtros de la directiva IPSec. Estos filtros permiten el funcionamiento de Intercambio de claves de Internet (IKE) y del protocolo de autenticación Kerberos. Los filtros también permiten que se señale (RSVP) la calidad de servicio (QoS) de la red cuando el tráfico de datos está protegido mediante IPSec, así como el tráfico que IPSec no puede proteger (como el tráfico de multidifusión o difusión).
  
Puede agregar este valor del Registro al archivo de plantilla en la
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\IPSEC\\**
  
subclave.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Grupos restringidos
  
La función Grupos restringidos permite administrar la pertenencia a grupos a través de mecanismos de directiva, así como impedir la explotación deliberada o inadvertida de los grupos que tienen derechos de usuario potentes. Analice en primer lugar las necesidades de su organización para determinar los grupos que desea restringir.
  
Los grupos **Operadores de copia de seguridad** y **Usuarios avanzados** se han restringido en los tres entornos definidos en esta guía. Aunque los miembros de los grupos **Operadores de copia de seguridad** y **Usuarios avanzados** tengan menos derechos de acceso que los miembros del grupo **Administradores**, siguen contando con eficaces capacidades.
  
**Nota :** si su organización utiliza cualquiera de estos grupos, controle con cuidado su asociación y no implemente la guía para la configuración de Grupos restringidos. Si su organización agrega usuarios al grupo Usuarios avanzados, es probable que desee implementar los permisos opcionales del sistema de archivos que se describen en la siguiente sección, “Seguridad del sistema de archivos”.
  
Puede establecer la configuración de Grupos restringidos en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Grupos restringidos**
  
Los administradores pueden configurar grupos restringidos si agregan el grupo que desean directamente a la directiva MSBP. Cuando un grupo está restringido, se pueden definir sus miembros así como otros grupos a los que pertenezca. Si no se especifican estos miembros de grupo, el grupo estará totalmente restringido.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Seguridad del sistema de archivos
  
El sistema de archivos NTFS se ha mejorado con cada nueva versión de Microsoft Windows y los permisos predeterminados para NTFS son adecuados para la mayoría de las organizaciones. Las configuraciones tratadas en esta sección se proporcionan como opciones de uso opcional para las organizaciones que no utilizan grupos restringidos pero que desean tener un nivel adicional de seguridad en los servidores.
  
Puede establecer la configuración de seguridad del sistema de archivos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Sistema de archivos**
  
**Nota**: es necesario probar exhaustivamente todos los cambios realizados en la configuración de seguridad predeterminada del sistema de archivos en un entorno de laboratorio antes de implementarlos en una organización de gran tamaño. Se han dado casos en que los permisos de archivos se han modificado hasta tal punto que los equipos afectados por ello se han tenido que reconstruir completamente.
  
Los permisos predeterminados de archivos en Windows Server 2003 con SP1 son suficientes para la mayoría de las situaciones. Sin embargo, si no prevé bloquear los miembros que forman parte del grupo **Usuarios avanzados** con la característica Grupos restringidos o si planea habilitar la configuración **Acceso de red: deja que los permisos de Todos se apliquen a los usuarios anónimos**, es posible que desee aplicar los permisos opcionales que se describen a continuación. Son muy específicos y aplican restricciones adicionales a determinadas herramientas ejecutables que un usuario malintencionado con privilegios elevados podría usar para comprometer el equipo o la red.
  
Observe cómo estos cambios no afectan a varias carpetas ni a la raíz del volumen del sistema. Puede resultar muy arriesgado cambiar los permisos de esa manera, además de que a menudo conlleva la inestabilidad del equipo. Todos los archivos siguientes se encuentran en la carpeta **%SystemRoot%\\System32\\** y a todos ellos se les han concedido los siguientes permisos: **Administradores: Control total,** **Sistema: Control total**.
  
-   regedit.exe
  
-   arp.exe
  
-   at.exe
  
-   attrib.exe
  
-   cacls.exe
  
-   debug.exe
  
-   edlin.exe
  
-   eventcreate.exe
  
-   eventtriggers.exe
  
-   ftp.exe
  
-   nbtstat.exe
  
-   net.exe
  
-   net1.exe
  
-   netsh.exe
  
-   netstat.exe
  
-   nslookup.exe
  
-   ntbackup.exe
  
-   rcp.exe
  
-   reg.exe
  
-   regedt32.exe
  
-   regini.exe
  
-   regsvr32.exe
  
-   rexec.exe
  
-   route.exe
  
-   rsh.exe
  
-   sc.exe
  
-   secedit.exe
  
-   subst.exe
  
-   systeminfo.exe
  
-   telnet.exe
  
-   tftp.exe
  
-   tlntsvr.exe
  
Para su comodidad, estos permisos opcionales ya están configurados en la plantilla de seguridad denominada **Optional-File-Permissions.inf**, que se incluye con la versión descargable de esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
Aunque la mayoría de las contramedidas utilizadas en esta guía para reforzar la seguridad de los servidores de línea de base se han aplicado mediante la directiva de grupo, existen configuraciones adicionales que son bastante difíciles o casi imposibles de aplicar con la directiva de grupo. Para obtener una explicación detallada de las contramedidas descritas en esta sección, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en [http://go.microsoft.com/fwlink/?LinkId=15159](http://go.microsoft.com/fwlink/?linkid=15159).
  
#### Procedimientos de consolidación manual
  
En esta sección se describe cómo se implementaron manualmente algunas contramedidas adicionales (como la seguridad de las cuentas) para los distintos entornos de seguridad definidos en esta guía.
  
##### Adición manual de grupos de seguridad únicos a las asignaciones de derechos de usuario
  
La mayoría de los grupos de seguridad recomendados para las asignaciones de derechos de usuario se configuraron en las plantillas de seguridad que acompañan a esta guía. No obstante, existen algunos derechos que no se pueden incluir en las plantillas de seguridad, porque los identificadores de seguridad (SID) de determinados grupos de seguridad son únicos entre los distintos dominios de Windows Server 2003. El problema radica en que el RID (identificador relativo), que forma parte del SID (identificador de seguridad), es único. Estos derechos se incluyen en la tabla siguiente.
  
**Advertencia**: en la siguiente tabla se incluyen valores para el administrador integrado. El administrador integrado es la cuenta de usuario integrada y *no* el grupo de seguridad **Administradores**. Si se agrega el grupo de seguridad **Administradores** a cualquiera de los derechos de usuario de denegación de acceso siguientes, deberá iniciar sesión localmente para corregir el error.
  
Además, la cuenta de administrador integrada puede tener un nombre nuevo si ha seguido la recomendación anteriormente indicada en esta guía de cambiarle el nombre. Al agregar esta cuenta a cualquier derecho de usuario de denegación de acceso, asegúrese de seleccionar la cuenta de administrador a la que ha cambiado el nombre.
  
**Tabla 4.30 Asignaciones de derechos de usuario agregadas manualmente**

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
<th><p>Nombre del parámetro en IU</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el acceso desde la red a este equipo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión como trabajo por lotes</p></td>
<td style="border:1px solid black;"><p>Support_388945a0 e Invitado</p></td>
<td style="border:1px solid black;"><p>Support_388945a0 e Invitado</p></td>
<td style="border:1px solid black;"><p>Support_388945a0 e Invitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Invitados; Support_388945a0; Invitado y todas las cuentas de servicio que NO sean del sistema operativo.</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Invitados; Support_388945a0; Invitado y todas las cuentas de servicio que NO sean del sistema operativo.</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Invitados; Support_388945a0; Invitado y todas las cuentas de servicio que NO sean del sistema operativo.</p></td>
</tr>  
</tbody>  
</table>
  
**Importante**: todas las cuentas de servicio que NO sean del sistema operativo son cuentas de servicio de aplicaciones específicas de la empresa. Estas cuentas no incluyen las cuentas SISTEMA LOCAL, SERVICIO LOCAL o SERVICIO DE RED que son cuentas integradas del sistema operativo.
  
Para agregar manualmente los grupos de seguridad indicados a la directiva de línea de base de servidores miembros para el entorno Cliente de empresa, siga los pasos siguientes.
  
**Para agregar grupos de seguridad a las asignaciones de derechos de usuario**
  
1.  En Usuarios y equipos de Active Directory, haga clic con el botón secundario en la UO Servidores miembro y, a continuación, seleccione **Propiedades**.
  
2.  En la ficha **Directiva de grupo**, seleccione **Enterprise Client Member Server Baseline Policy** (directiva de línea de base de servidores miembros de Cliente de empresa) para editar el GPO vinculado.
  
3.  Seleccione **Enterprise Client – Member Server Baseline Policy** y, a continuación, haga clic en **Editar**.
  
4.  En la ventana **Directiva de grupo**, haga clic en **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario** para agregar los grupos de seguridad únicos de la tabla anterior para cada derecho.
  
5.  Cierre la directiva de grupo que ha modificado.
  
6.  Cierre la ventana **Propiedades** de la UO Servidores miembro.
  
7.  Fuerce la replicación entre los controladores de dominio para que la directiva se aplique a todos; para ello, proceda del siguiente modo:
  
    1.  Abra una ventana del símbolo del sistema, escriba **gpupdate /Force** y presione ENTRAR para forzar al servidor a actualizar la directiva.
  
    2.  Reinicie el servidor.
  
8.  Compruebe en el registro de eventos que la directiva de grupo se ha descargado correctamente y que el servidor puede comunicarse con los otros controladores de dominio en el dominio.
  
##### Seguridad de las cuentas conocidas
  
Windows Server 2003 con SP 1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, se cambia el nombre de la cuenta de administrador integrada y se modifica su descripción para impedir que los atacantes que intenten usar esta cuenta conocida comprometan un servidor remoto.
  
El valor de este cambio de configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta de administrador integrada para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de administrador si cambia su nombre por uno único.
  
Realice los pasos siguientes para proteger las cuentas conocidas en los servidores y dominios:
  
-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.
  
-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás con el mismo nombre de cuenta y contraseña.
  
-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.
  
-   Registre cualquier cambio que haga en una ubicación segura.
  
    **Nota**: se puede cambiar el nombre de la cuenta integrada Administrador desde Directiva de grupo. Esta configuración no se implementó en la directiva de línea de base porque cada organización debe elegir un nombre único para esta cuenta. Sin embargo, puede configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de las cuentas de administrador en los tres entornos que se definen en esta guía. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.
  
##### Seguridad de las cuentas de servicios
  
A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en [www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) (en inglés).
  
##### NTFS
  
Las particiones NTFS admiten las ACL en los niveles de archivo y carpeta. Esta compatibilidad no se encuentra disponible con la tabla de asignación de archivos (FAT) o los sistemas de archivos FAT32. FAT32 es una versión actualizada del sistema de archivos FAT que permite tamaños predeterminados de clúster significativamente más pequeños y admite discos duros con un tamaño máximo de dos terabytes. FAT32 se incluye en Windows 95 OSR2, Windows 98, Microsoft Windows Me, Windows 2000, Windows XP Professional y Windows Server 2003.
  
Formatee todas las particiones en cada servidor con NTFS. Emplee la utilidad de conversión para convertir con cuidado particiones FAT a NTFS, pero no olvide que dicha utilidad configurará las listas ACL de la unidad convertida en **Todos: Control total**.
  
En el caso de equipos que ejecuten Windows 2003 Server con SP1, aplique localmente las dos plantillas de seguridad siguientes para configurar las ACL predeterminadas de sistema de archivos en los servidores miembro y los controladores de dominio, respectivamente:
  
-   **%windir%\\inf\\defltsv.inf**
  
-   **%windir%\\inf\\defltdc.inf**
  
    **Nota**: la configuración de seguridad predeterminada del controlador de dominio se aplica durante la promoción de un servidor a un controlador de dominio.
  
Se ha dado formato a todas las particiones de los servidores de los tres entornos definidos en esta guía con particiones NTFS, con el fin de ofrecer los medios necesarios para una administración de seguridad de los archivos y directorios mediante las ACL.
  
##### Configuraciones de los Servicios de Terminal Server
  
La configuración **Establecer nivel de cifrado de conexión de cliente** determina el nivel de cifrado para las conexiones de clientes de los Servicios de Terminal Server en el entorno. La opción de configuración **Nivel alto** que utiliza cifrado de 128 bits impide que los atacantes intercepten las sesiones de los Servicios de Terminal Server con un analizador de paquetes. Algunas versiones más antiguas del cliente de Servicios de Terminal Server no son compatibles con este nivel de cifrado alto. Si su red dispone de dichos clientes, configure el nivel de cifrado de la conexión para que envíe y reciba datos en el nivel de cifrado más alto permitido por el cliente.
  
Puede establecer esta configuración en la siguiente ubicación de la directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Terminal Server\\Cifrado y seguridad.**
  
**Tabla 4.31 Recomendación de configuración del nivel de cifrado de las conexiones de cliente**

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
<th><p>Nombre del parámetro en IU</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Establecer el nivel de cifrado de conexión de cliente</p></td>
<td style="border:1px solid black;"><p>Alta</p></td>
<td style="border:1px solid black;"><p>Alta</p></td>
<td style="border:1px solid black;"><p>Alta</p></td>
</tr>  
</tbody>  
</table>
  
Los tres niveles disponibles de cifrado se describen en la tabla siguiente:
  
**Tabla 4.32 Niveles de cifrado de Servicios de Terminal Server**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Nivel de cifrado</p></th>  
<th><p>Descripción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nivel alto</p></td>
<td style="border:1px solid black;"><p>Cifra los datos que se envían desde el cliente al servidor y desde el servidor al cliente con cifrado de 128 bits. Utilice este nivel siempre que Terminal Server se ejecute en un entorno que sólo incluya clientes de 128 bits, como los clientes de Conexión a Escritorio remoto. Los clientes que no admitan este nivel de cifrado no se podrán conectar.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cliente compatible</p></td>
<td style="border:1px solid black;"><p>Cifra los datos enviados entre el cliente y el servidor con la fuerza máxima de la clave admitida por el cliente. Emplee este nivel cuando Terminal Server se ejecute en un entorno con clientes mixtos o heredados.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nivel bajo</p></td>
<td style="border:1px solid black;"><p>Cifra los datos que se envían del cliente al servidor con cifrado de 56 bits.</p>
<p><strong>Importante</strong>: los datos enviados del servidor al cliente no están cifrados.</p></td>
</tr>
</tbody>
</table>
<p> </p>

#### Informe de errores

**Tabla 4.33 Configuración recomendada de los informes de errores**

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
<th><p>Configuración</p></th>
<th><p>Cliente heredado</p></th>
<th><p>Cliente de empresa</p></th>
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Desactivar Informe de errores de Windows</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
Este servicio ayuda a Microsoft a realizar un seguimiento de los errores así como a solucionarlos. Puede configurar este servicio para generar informes para los errores del sistema operativo, componentes de Windows o de programa. Sólo está disponible en Windows XP Professional y Windows Server 2003.
  
El servicio **Informe de errores** puede informar de dichos errores a Microsoft a través de Internet o a un recurso compartido de archivos internos. Aunque los informes de error puedan incluir datos corporativos de contenido delicado o incluso confidenciales, la directiva de privacidad de Microsoft con respecto a la notificación de errores asegura que Microsoft no utilizará dichos datos de forma incorrecta. No obstante, los datos se transmiten en HTTP de texto sin formato y podrían ser interceptados en Internet y visualizados por terceros.
  
La configuración **Desactivar Informe** **de errores de Windows** permite controlar si el servicio Informe de errores transmite algún dato.
  
Puede configurar esta configuración de directiva en Windows Server 2003 en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet**
  
Establezca el parámetro **Desactivar Informe** **de errores de Windows** como **Habilitado** en la DCBP para los tres entornos que se definen en esta guía.
  
##### Habilitación de volcados de memoria manuales
  
Windows Server 2003 con SP1 incluye una característica que sirve para detener el equipo y generar un archivo de volcado de memoria Memory.dmp. Esta característica se debe habilitar de forma explícita y puede que no sea apropiada para todos los servidores de la organización. Si determina que sería valioso capturar volcados de memoria en algunos servidores, puede seguir las instrucciones proporcionadas en el artículo [Las características de Windows permiten generar un archivo Memory.dmp mediante el teclado](http://support.microsoft.com/default.aspx?kbid=244139) en <http://support.microsoft.com/default.aspx?kbid=244139>.
  
**Importante**: cuando la memoria se copia a un disco como se describe en dicho artículo, la información confidencial podría incluirse en el archivo Memory.dmp. Lo ideal es que todos los servidores estén protegidos del acceso físico no autorizado. Si genera un archivo de volcado de memoria en un servidor que tiene riesgos de resultar comprometido físicamente, asegúrese de eliminar el archivo de volcado antes de concluir la solución de problemas.
  
#### Creación de la directiva de línea de base con SCW
  
Para implementar la configuración de seguridad necesaria, primero debe crear una directiva de línea de base de servidores miembro (MSBP). Para ello, debe utilizar el Asistente para configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
Es probable que durante la creación de la directiva MSBP quite la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.
  
**Para crear la directiva de línea de base de servidores miembro (MSBP)**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el equipo al dominio.
  
4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor en su entorno. Los ejemplos incluyen su software y los agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
6.  Elimine la función de servidor de archivos de las funciones detectadas que se enumeran.
  
7.  Compruebe que las funciones de servidor detectadas son adecuadas para su entorno.
  
8.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
9.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
10. Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
11. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
12. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.
  
13. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
14. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
15. Incluya la plantilla de seguridad apropiada (por ejemplo, EC-Member Server Baseline.inf).
  
16. Guarde la directiva con un nombre apropiado (por ejemplo, Member Server Baseline.xml).
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método nativo de implementación ofrece la ventaja de poder deshacer fácilmente las directivas implementadas desde SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.
  
La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.
  
Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.
  
Para obtener más información acerca de cómo probar las directivas de SCW, consulte la [Guía de implementación del Asistente para configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en [www.microsoft.com/technet/prodtechnol/windowsserver2003/library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx](http://technet.microsoft.com/es-es/library/cc776871.aspx) (en inglés) y la [documentación del Asistente para configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en <http://go.microsoft.com/fwlink/?linkid=43450> (en inglés).
  
#### Conversión e implementación de la directiva
  
Después de probar completamente la directiva, complete los pasos siguientes para convertirla en un GPO e implementarla:
  
1.  En el símbolo de sistema, escriba el siguiente comando:
  
    ```  
scwcmd transform /p:&lt;PathToPolicy.xml&gt; /g:&lt;GPODisplayName&gt;  
```
  
    y, a continuación, pulse Entrar. Por ejemplo:
  
    ```  
 scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Member Server Baseline.xml" /g:"Member Server Baseline Policy"   
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han explicado los procedimientos para reforzar la seguridad de los servidores que se aplicaron inicialmente a todos los servidores que ejecutaban Windows Server 2003 con SP1 en los tres entornos de seguridad definidos en esta guía. Una gran parte de estos procedimientos consistieron en la creación de una única plantilla de seguridad para cada uno de los entornos de seguridad y su posterior importación a un objeto de directiva de grupo (GPO) vinculado a la OU principal para que el servidor miembro obtuviese el nivel de seguridad objetivo.
  
No obstante, existen algunos procedimientos de consolidación que no se pueden aplicar mediante la directiva de grupo. Se ha proporcionado además orientación acerca de cómo establecer esta configuración manualmente. Se han adoptado pasos adicionales en el caso de determinadas funciones de servidor con el fin de permitir su funcionamiento de la forma más segura posible.
  
Entre las medidas específicas para las funciones de servidor se incluyen procedimientos adicionales para reforzar la seguridad y para reducir la configuración de seguridad en la directiva de seguridad de línea de base. Estas modificaciones se analizan en detalle en los capítulos siguientes de esta guía.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores que ejecutan Windows Server 2003 con SP1.
  
-   Para obtener más información acerca de la configuración de seguridad de Windows Server 2003, consulte la página de [descripciones sobre las configuraciones de seguridad](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/dd980ca3-f686-4ffc-a617-50c6240f5582.mspx) en[http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/dd980ca3-f686-4ffc-a617-50c6240f5582.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/dd980ca3-f686-4ffc-a617-50c6240f5582.mspx) (en inglés).
  
-   Para obtener más información acerca de la seguridad en Windows Server 2003, visite el [Centro de seguridad de Windows Server 2003](http://www.microsoft.com/technet/security/prodtech/windowsserver2003.mspx) en <http://www.microsoft.com/technet/security/prodtech/windowsserver2003.mspx>.
  
-   Para obtener más información acerca de la directiva de auditoría de Windows Server 2003, consulte la página sobre la [directiva de auditoría](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx) en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx) (en inglés).
  
-   Para obtener más información acerca de Microsoft Operations Manager (MOM), consulte la página de [Microsoft Operations Manager](http://www.microsoft.com/mom/) en <http://www.microsoft.com/mom/>.
  
-   Para obtener más información acerca de los derechos de usuario en Windows Server 2003, consulte la página de [derechos de usuario](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/589980fb-1a83-490e-a745-357750ced3d9.mspx) en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/589980fb-1a83-490e-a745-357750ced3d9.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/589980fb-1a83-490e-a745-357750ced3d9.mspx) (en inglés).
  
-   Para obtener más información acerca de la configuración predeterminada de seguridad para Windows Server 2003, consulte las [diferencias de la configuración predeterminada de seguridad](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/1494bf2c-b596-4785-93bb-bc86f8e548d5.mspx) en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/1494bf2c-b596-4785-93bb-bc86f8e548d5.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/1494bf2c-b596-4785-93bb-bc86f8e548d5.mspx) (en inglés).
  
-   Para obtener más información acerca de cómo garantizar la seguridad de Servicios de Terminal Server de Windows 2000, consulte los detalles sobre la [seguridad de los Servicios de Terminal Server de Windows 2000](http://www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.mspx) en <http://www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.mspx> (en inglés).
  
-   Para obtener más información acerca de cómo garantizar la seguridad de la pila TCP/IP de Windows Server 2003, consulte el artículo de Microsoft Knowledge Base "[Cómo proteger la pila TCP/IP frente a ataques por denegación de servicio en la familia Windows Server 2003](http://support.microsoft.com/?kbid=324270)" en [http://support.microsoft.com/?scid=324270](http://support.microsoft.com/?kbid=324270).
  
-   Para obtener más detalles acerca de cómo reforzar la configuración de las aplicaciones Windows Sockets, consulte el artículo de Microsoft Knowledge Base sobre la [no disponibilidad de los servidores de Internet debido a ataques SYN malintencionados](http://support.microsoft.com/?kbid=142641) en <http://support.microsoft.com/?kbid=142641> (en inglés).
  
-   Para obtener más información acerca de la ubicación de los archivos .adm, consulte el artículo de Microsoft Knowledge Base "[Ubicación de archivos ADM (plantilla administrativa) en Windows](http://support.microsoft.com/?kbid=228460)" en <http://support.microsoft.com/?kbid=228460>.
  
-   Para obtener más información acerca de cómo personalizar la interfaz de usuario del Editor de configuración de seguridad, consulte el artículo de Microsoft Knowledge Base "[Cómo agregar configuraciones personalizadas del Registro al Editor de configuración de seguridad](http://support.microsoft.com/?kbid=214752)" en [http://support.microsoft.com/?scid=214752](http://support.microsoft.com/?kbid=214752).
  
-   Para obtener más información acerca de cómo crear archivos de plantillas administrativas personalizadas en Windows, consulte el artículo de Microsoft Knowledge Base "[Cómo crear plantillas administrativas personalizadas en Windows 2000](http://support.microsoft.com/?kbid=323639)" en [http://support.microsoft.com/?scid=323639](http://support.microsoft.com/?kbid=323639). Revise también las notas del producto relativas a la [implementación de la directiva de grupo basada en el Registro](http://www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp) en [http://www.microsoft.com/WINDOWS2000/techinfo/howitworks/management/rbppaper.asp](http://www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp) (en inglés).
  
-   Para obtener más información acerca de cómo garantizar que las configuraciones del nivel de autenticación de LAN Manager más seguras funcionen en redes con una combinación de equipos con Windows 2000 y Windows NT 4.0, consulte el artículo de Microsoft Knowledge Base "[Problemas de autenticación en Windows 2000 con niveles de NTLM 2 superiores a 2 en un dominio de Windows NT 4.0](http://support.microsoft.com/?kbid=305379)" en [http://support.microsoft.com/?scid=305379](http://support.microsoft.com/?kbid=305379).
  
-   Para obtener más información acerca de la autenticación NTLMv2, consulte el artículo de Microsoft Knowledge Base "[Cómo habilitar la autenticación NTLM 2](http://support.microsoft.com/?kbid=239869)" en [http://support.microsoft.com/?scid=239869](http://support.microsoft.com/?kbid=239869).
  
-   Para obtener más información acerca de la configuración predeterminada de los servicios en Windows Server 2003, consulte la página sobre la [configuración predeterminada de servicios](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/2b1dc6cf-2e34-4681-9aa6-8d0ffba2d3e3.mspx) en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/2b1dc6cf-2e34-4681-9aa6-8d0ffba2d3e3.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/2b1dc6cf-2e34-4681-9aa6-8d0ffba2d3e3.mspx) (en inglés).
  
-   Para obtener más información acerca de la implementación de tarjetas inteligentes, consulte la página sobre cómo [fomentar la calidad de la información de la red con tarjetas inteligentes](http://www.microsoft.com/technet/technetmag/issues/2005/01/smartcards/) en [http://www.microsoft.com/technet/technetmag/issues/2005/01/SmartCards/default.aspx](http://www.microsoft.com/technet/technetmag/issues/2005/01/smartcards/) (en inglés).
  
-   Para obtener más información sobre el valor del Registro "Restrict Anonymous" y Windows 2000, consulte el artículo de Microsoft Knowledge Base sobre la [posibilidad de que el valor del Registro "RestrictAnonymous" afecte a la confianza de un dominio Windows 2000](http://support.microsoft.com/?kbid=296405) en <http://support.microsoft.com/?kbid=296405> (en inglés).
  
-   Para obtener más información sobre los informes de errores, consulte la página sobre [informes de errores corporativos](http://www.microsoft.com/spain/licencias/sa/cer.mspx) en [http://www.microsoft.com/resources/satech/cer/](http://www.microsoft.com/spain/licencias/sa/cer.mspx) (en inglés).
  
-   Para obtener información acerca de los puertos de red utilizados por las aplicaciones de Microsoft, consulte el artículo de Microsoft Knowledge Base "[Introducción al servicio y requisitos del puerto de red para el sistema Windows Server](http://support.microsoft.com/kb/832017)" en <http://support.microsoft.com/kb/832017>.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
