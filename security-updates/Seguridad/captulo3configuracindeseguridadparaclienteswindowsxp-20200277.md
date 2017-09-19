---
TOCTitle: 'Capítulo 3: Configuración de seguridad para clientes Windows XP'
Title: 'Capítulo 3: Configuración de seguridad para clientes Windows XP'
ms:assetid: 'bca34b8d-a1ca-42e4-b743-aa3ca12fd8f9'
ms:contentKeyID: 20200277
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163074(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 3: Configuración de seguridad para clientes Windows XP

Actualizado: 20/10/05

##### En esta página

[](#enaa)[Información general](#enaa)
[](#emaa)[Configuración de directiva de cuentas](#emaa)
[](#elaa)[Configuración de Directiva local](#elaa)
[](#ekaa)[Configuración de directiva de auditoría](#ekaa)
[](#ejaa)[Configuración de Asignación de derechos de usuario](#ejaa)
[](#eiaa)[Configuración de Opciones de seguridad](#eiaa)
[](#ehaa)[Configuración de seguridad del registro de eventos](#ehaa)
[](#egaa)[Grupos restringidos](#egaa)
[](#efaa)[Servicios del sistema](#efaa)
[](#eeaa)[Parámetros adicionales del registro](#eeaa)
[](#edaa)[Modificación de la interfaz de usuario del Editor de configuración de seguridad](#edaa)
[](#ecaa)[Configuración de seguridad adicional](#ecaa)
[](#ebaa)[Seguridad del sistema de archivos](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

En este capítulo se describen los parámetros principales que se configuran a través de Directiva de grupo en un dominio de servicio de directorio Microsoft® Windows® 2000 o Windows Server™ 2003 Active Directory®. Implemente las configuraciones de directiva recomendadas para que los equipos de escritorio y portátiles de su organización en los que se ejecuta Microsoft Windows XP Professional con Service Pack 2 (SP2) queden configurados de un modo seguro. No se proporciona orientación para todas las configuraciones de directiva disponibles en Windows XP, sólo para las que pueden tener una relación directa en la seguridad del equipo.

Tal como se describía en el capítulo 1, "Introducción a la Guía de seguridad de Windows XP", la orientación que se presenta en este capítulo es específica para los entornos Cliente de empresa (EC), Seguridad especializada: Funcionalidad limitada (SSLF) que se definen en esta guía. En algunos casos, en este capítulo se recomiendan configuraciones de directiva para equipos portátiles distintas a las que se aplican a los equipos de escritorio, debido a que los primeros cuentan con movilidad y no siempre se encuentran conectados a controladores de dominio en el entorno a través de la red de la organización. También se da por sentado que los usuarios de equipos portátiles trabajan a horas distintas cuando no disponen de soporte técnico inmediato. Por esos motivos, las configuraciones de directiva que requieren conectividad a un controlador de dominio o que determinan las horas de inicio de sesión son distintos para los equipos portátiles cliente.

Las configuraciones de directiva que no se especifican para entornos determinados se definen a veces en el nivel de dominio, tal como se describe en el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory". Otras configuraciones de directiva que se enumeran en este capítulo como **No está definido** se tratan de ese modo porque el valor predeterminado es suficientemente seguro para ese entorno en particular. Asimismo, las configuraciones de directiva no definidas en estos objetos de directiva de grupo (GPO) facilitan la implementación de aplicaciones que necesitan modificar parámetros durante la instalación. Por ejemplo, puede haber herramientas de administración que necesiten asignar derechos de usuario específicos a las cuentas del servicio local en equipos administrados. La orientación en este capítulo consiste en recomendaciones. Siempre deberá considerar detenidamente las necesidades de su organización antes de realizar cambios en el entorno.

En la siguiente tabla se definen los archivos de infraestructura (.inf) disponibles con esta guía. Dichos archivos incluyen todas las instrucciones de configuración de seguridad de línea de base para los dos entornos que se tratan en este capítulo.

**Tabla 3.1. Plantillas de seguridad de línea de base**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Descripción</p></th>
<th><p>EC</p></th>
<th><p>SSLF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Plantillas de seguridad de línea de base para equipos de escritorio</p></td>
<td style="border:1px solid black;"><p>EC-Desktop.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Desktop.inf</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Plantillas de seguridad de línea de base para equipos portátiles</p></td>
<td style="border:1px solid black;"><p>EC-Laptop.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Laptop.inf</p></td>
</tr>  
</tbody>  
</table>
  
Para obtener información más detallada acerca de las configuraciones de directiva que se tratan en este capítulo, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que se puede descargar en http://go.microsoft.com/fwlink/?LinkId=15159.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de cuentas
  
En este capítulo no se proporciona información acerca de parámetros de configuración de directiva de cuentas. Este tipo de configuración se trata en el capítulo 2 de esta guía, "Configuración de la infraestructura de dominios de Active Directory".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Directiva local
  
La configuración de la directiva local se puede establecer en cualquier equipo en el que se ejecute Windows XP Professional a través de o la consola de directivas de seguridad local o de GPO basados en dominio de Active Directory. Entre los parámetros de directiva local se incluyen los de directiva de auditoría, asignaciones de derechos de usuario y opciones de seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
Las directivas de auditoría determinan los eventos de seguridad que se enviarán a los administradores, de modo que se registre la actividad del sistema o del usuario en categorías de eventos específicas. El administrador puede supervisar la actividad relacionada con la seguridad como, por ejemplo, quién tiene acceso a un objeto, el momento en que los usuarios inician o cierran sesión en sus equipos o si se realizan cambios en una configuración de directiva de auditoría. Por todo ello, Microsoft recomienda que se cree una directiva de auditoría para un administrador con el fin de implementarla en el entorno.
  
Sin embargo, antes de implementar una directiva de auditoría tendrá que decidir qué categorías de eventos deben ser auditadas en su entorno. La configuración de auditoría que se seleccione en las categorías de eventos definirá la directiva de auditoría. Cuando defina una configuración de auditoría para categorías de eventos específicas, un administrador podrá crear una directiva de auditoría que responda a las necesidades de su organización en materia de seguridad.
  
Si no se establece ninguna configuración de auditoría, resultará difícil o imposible determinar lo que sucedió durante un incidente de seguridad. No obstante, si se configura la auditoría de manera que generen eventos demasiadas actividades autorizadas, el registro de eventos de seguridad se llenará de datos poco útiles. La información de las secciones siguientes está diseñada para ayudarle a decidir qué debe supervisar y cómo recopilar datos de auditoría pertinentes para su organización.
  
Puede establecer la configuración de directiva de auditoría en Windows XP en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Directiva de auditoría**
  
La tabla siguiente resume las recomendaciones sobre la configuración de directiva de auditoría para equipos cliente de escritorio y portátiles en los dos tipos de entornos seguros que se tratan en este capítulo. Se hace referencia al entorno de Cliente de empresa como EC, y al de Seguridad especializada: Funcionalidad limitada, como SSLF. Debe revisar estas recomendaciones y ajustarlas según corresponda para su organización. No obstante, es importante tener especial precaución con los parámetros de auditoría que puedan generar un gran volumen de tráfico. Por ejemplo, si habilita la auditoría de errores y aciertos para el **uso de privilegios de auditoría**, se generarán tantos eventos de auditoría que quizá no sea posible encontrar otros tipos de entradas en el registro de eventos de seguridad. Ese tipo de configuración podría tener también una repercusión significativa en el rendimiento. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
**Tabla 3.2 Recomendaciones para la configuración de la directiva de auditoría**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión de cuenta</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar la administración de cuentas</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar el acceso del servicio de directorio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
<td style="border:1px solid black;"><p>Correcto, Erróneo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar el acceso a objetos</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar el cambio de directivas</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar el uso de privilegios</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditar el seguimiento de procesos</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditar eventos del sistema</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar eventos de inicio de sesión de cuenta
  
Si esta configuración de directiva se habilita, se generan eventos para la validación de credenciales. Estos eventos se producen en el equipo con autorización para las credenciales. Para las cuentas de dominio, el controlador de dominio tiene autorización, mientras que para las cuentas locales es el equipo local el que la tiene. En los entornos de dominio, la mayoría de los eventos de Inicio de sesión de cuenta se producen en el registro de seguridad de los controladores de dominio que tienen autorización para las cuentas de dominio. Sin embargo, estos eventos pueden producirse en otros equipos de la organización, en función de las cuentas que se utilizan para iniciar sesión.
  
En esta guía, el parámetro de **Auditar sucesos de inicio de sesión de cuenta** se establece como **Correcto** sólo para el entorno EC y como **Correcto** y **Erróneo** para el entorno SSLF.
  
#### Auditar la administración de cuentas
  
Esta configuración de directiva se emplea para realizar un seguimiento de los intentos de creación de usuarios o grupos y del cambio del nombre de éstos, activación o desactivación de cuentas de usuario, cambio de contraseñas de cuentas y habilitación de la auditoría para los eventos de administración de cuentas. Si habilita esta configuración de directiva de auditoría, los administradores podrán realizar un seguimiento de los eventos con el fin de detectar la creación autorizada, accidental o malintencionada de cuentas de grupos y usuarios.
  
El parámetro **Auditar la administración de cuestas** se configura como **Correcto** para el entorno EC y como **Correcto** y **Erróneo** para el entorno SSLF.
  
#### Auditar el acceso del servicio de directorio
  
Esta configuración de directiva sólo se puede habilitar para realizar tareas de auditoría en controladores de dominio. Por ello, no se define en el nivel de estación de trabajo. Esta configuración de directiva no se aplica a equipos en los que se ejecuta Windows XP Professional. Así pues, asegúrese de que el parámetro **Auditar el acceso del servicio de directorio** está configurado como **No está definido** para los dos entornos que se tratan en este capítulo.
  
#### Auditar eventos de inicio de sesión
  
Esta configuración de directiva genera eventos que registran la creación y la destrucción de sesiones de inicio. Estos eventos se producen en el equipo al que se tiene acceso. Para inicios de sesión interactivos, estos eventos se generarían en el equipo en el que se inició sesión. Si se llevó a cabo un inicio de sesión de red para tener acceso a un recurso compartido, estos eventos se generarían en el equipo que aloja el recurso al que se tuvo acceso.
  
Si configura el parámetro **Auditar eventos de inicio de sesión** como **Sin auditoría**, resultará difícil o imposible determinar qué usuario ha tenido o intentado tener acceso a equipos de la organización.
  
El parámetro **Auditar eventos de inicio de sesión** se configura para registrar eventos de tipo **Correcto** para el entorno EC. Esta configuración de directiva está establecida como eventos de tipo **Correcto** y **Erróneo** para el entorno SSLF.
  
#### Auditar el acceso a objetos
  
Por sí misma, esta configuración de directiva no provocará que se audite ningún evento. Determina si debe auditarse el evento de un usuario que tiene acceso a un objeto (por ejemplo, un archivo, una carpeta, una clave de Registro o una impresora) con una lista de control de acceso al sistema especificada (SACL).
  
Una lista de control de acceso al sistema se compone de entradas de control de acceso (ACE), cada una de las cuales contiene tres datos:
  
-   La entidad de seguridad principal (el usuario, equipo o grupo) que se va a auditar.
  
-   El tipo de acceso específico que se va a auditar, denominado máscara de acceso.
  
-   Un indicador que señala si se deben auditar eventos de acceso erróneos, eventos de acceso correctos o ambos.
  
Si configura el parámetro **Auditar el acceso a objetos** como **Correcto**, se genera una entrada de auditoría cada vez que un usuario tiene acceso a un objeto con una SACL especificada. Si establece esta configuración de directiva como **Erróneo**, se genera una entrada de auditoría cada vez que un usuario intenta sin éxito tener acceso a un objeto con una SACL especificada.
  
Al configurar las listas de acceso al sistema, las organizaciones deben definir sólo las acciones que desean habilitar. Por ejemplo, quizá desee habilitar la configuración de auditoría **Escribir datos y Anexar datos** para los archivos ejecutables, con el fin de realizar un seguimiento de cuándo se cambian o reemplazan, ya que los virus, los gusanos y los troyanos suelen dirigirse a los archivos ejecutables. Asimismo, quizá desee realizar un seguimiento de cuándo se tiene acceso o se cambian documentos confidenciales.
  
La configuración de **Auditar el acceso a objetos** se establece como **Sin auditoría** para el entorno EC y como **Erróneo** para el entorno SSLF. Debe habilitar este parámetro para que surtan efecto los siguientes procedimientos.
  
En los siguientes procedimientos se analiza la forma de configurar manualmente las reglas de auditoría para un archivo o carpeta y de comprobar dichas reglas con cada objeto de la carpeta o archivo que se haya especificado. El procedimiento de prueba se puede automatizar por medio de un archivo de secuencia de comandos.
  
**Para definir una regla de auditoría para el archivo o carpeta:**
  
1.  Localice la carpeta o archivo en cuestión con el Explorador de Windows y selecciónelo.
  
2.  Haga clic en el menú **Archivo** y seleccione **Propiedades**.
  
3.  Haga clic en la ficha **Seguridad** y, a continuación, en el botón **Opciones avanzadas**.
  
4.  Haga clic en la ficha **Auditoría**.
  
5.  Haga clic en el botón **Agregar** y se mostrará el cuadro de diálogo **Seleccione los usuarios, equipos o grupos**.
  
6.  Haga clic en el botón **Tipos de objetos...** y, a continuación, en el cuadro de diálogo **Tipos de objetos**, seleccione los tipos de objetos que desee buscar.
  
    **Nota**: los tipos de objeto Usuario, Grupo y Ppio. de seguridad incorporado se encuentran seleccionados de forma predeterminada.
  
7.  Haga clic en el botón **Ubicaciones...** y, en el cuadro de diálogo **Ubicación:** seleccione su dominio o equipo local.
  
8.  En el cuadro de diálogo **Seleccionar usuarios o grupos**, escriba el nombre del grupo o usuario que desee auditar. A continuación, en **Escriba los nombres de objeto que desea seleccionar**, escriba **Usuarios autenticados** (para poder auditar el acceso de todos los usuarios autenticados) y haga clic en **Aceptar**. Se mostrará el cuadro de diálogo **Entrada de auditoría**.
  
9.  Determine el tipo de acceso que desea auditar en el archivo o carpeta utilizando el cuadro de diálogo **Entrada de auditoría**.
  
    **Nota**: recuerde que cada acceso puede generar varios eventos en el registro de eventos y provocar un rápido crecimiento del registro.
  
10. En el cuadro de diálogo **Entrada de auditoría**, situado junto a **Listar carpeta / Leer datos**, seleccione **Correcto y Erróneo** y después haga clic en **Aceptar**.
  
11. Las entradas de auditoría habilitadas se mostrarán en la ficha **Auditoría** del cuadro de diálogo **Configuración de seguridad avanzada**.
  
12. Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Propiedades**.
  
**Para comprobar una regla de auditoría para el archivo o carpeta:**
  
1.  Abra el archivo o carpeta.
  
2.  Cierre el archivo o carpeta.
  
3.  Inicie el Visor de eventos. En el Registro de eventos de seguridad aparecerán varios eventos de acceso a objetos con el **Id. de evento 560**.
  
4.  Haga doble clic en los eventos según sea necesario para ver información sobre los mismos.
  
#### Auditar el cambio de directivas
  
Esta configuración de directiva determina si debe auditarse cada incidente de un cambio de directivas de asignación de derechos de usuario, de directivas de Firewall de Windows, de directivas de confianza, o de cambios en la propia directiva de auditoría. Los parámetros recomendados le permitirán ver los privilegios de una cuenta que un atacante intente elevar, por ejemplo, mediante la incorporación del privilegio **Depurar programas** o del privilegio **Realizar copias de seguridad de archivos y directorios**.
  
El parámetro **Auditar el cambio de directivas** se configura como **Correcto** en los dos entornos que se tratan en este capítulo. El valor del parámetro para **Erróneo** no se incluye porque no proporcionará información significativa de acceso en el registro de eventos de seguridad.
  
#### Auditar el uso de privilegios
  
Esta configuración de directiva determina si se debe auditar cada caso en el que un usuario ejecute un derecho de usuario. Si configura este valor como **Correcto**, se genera una entrada de auditoría cada vez que un derecho de usuario se ejerce correctamente. Si configura este valor como **Erróneo**, se genera una entrada de auditoría cada vez que un derecho de usuario se ejerce sin éxito. Esta configuración de directiva puede generar un gran número de registros de eventos.
  
El parámetro **Auditar el uso de privilegios** se configura como **Sin auditoría** para equipos en el entorno EC y como **Erróneo** para el entorno SSLF para auditar todos los intentos fallidos de utilizar privilegios.
  
#### Auditar el seguimiento de procesos
  
Esta configuración de directiva determina si se debe auditar información detallada de seguimiento de eventos tales como la activación de programas, la salida de procesos, la duplicación de identificadores y el acceso indirecto a objetos. La habilitación del parámetro **Auditar el seguimiento de procesos** generará una cantidad considerable de eventos, por lo que generalmente se establece en **Sin auditoría**. Sin embargo, esta configuración puede resultar muy útil durante la respuesta a un incidente a partir del registro detallado de los procesos iniciados y la hora de inicio de los mismos.
  
El parámetro **Auditar el seguimiento de procesos** está configurado como **Sin auditoría** en los dos entornos que se tratan en este capítulo.
  
#### Auditar eventos del sistema
  
Esta configuración de directiva resulta muy importante, ya que permite supervisar eventos del sistema correctos y erróneos. Asimismo, proporciona un registro de estos eventos, que puede ayudar a determinar las instancias de acceso no autorizado al sistema. Entre los eventos del sistema se incluyen el inicio y el apagado de los equipos del entorno, los registros de eventos completos u otros eventos relacionados con la seguridad que afectan a todo el sistema.
  
El parámetro **Auditar eventos del sistema** está configurado como **Correcto** en los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Asignación de derechos de usuario
  
Además de los numerosos grupos con privilegios de Windows XP Professional, es posible asignar una serie de derechos a usuarios o grupos que normalmente no los tienen.
  
Para establecer el valor de un derecho de usuario en **Ninguno**, habilite este parámetro, pero no agregue ningún usuario o grupo. Para establecer el valor en **No está definido**, no lo habilite.
  
Puede establecer la configuración de asignación de derechos de usuario en la ubicación que se indica a continuación en el Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario**
  
La tabla siguiente resume las recomendaciones sobre asignaciones de derechos de usuario, para derechos que empiezan por las letras A hasta la E. Se proporcionan recomendaciones tanto para equipos cliente de escritorio como portátiles en los dos tipos de entornos seguros que se tratan en este capítulo. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
Las recomendaciones sobre derechos de usuario que empiezan por cualquiera de las restantes letras del alfabeto se resumen en la Tabla 3.4, y se proporciona información adicional detallada acerca de esos derechos de usuario en las subsecciones que siguen a esa tabla.
  
**Nota**: muchas características de Internet Information Server (IIS) requieren que ciertas cuentas, como IIS\_WPG, IIS IUSR\_*&lt;NombreEquipo&gt;* e* *IWAM\_*&lt;NombreEquipo&gt;*, cuenten con privilegios específicos. Para obtener más información acerca de qué derechos de usuario requieren las cuentas relacionadas con IIS, consulte el artículo sobre [IIS y cuentas integradas (IIS 6.0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx) en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/  
IIS/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx.
  
#### Derechos de usuario A – E
  
**Tabla 3.3 Recomendaciones para la configuración de asignaciones de derechos de usuario: Primera parte**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tener acceso a este equipo desde la red</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Actuar como parte del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ajustar las cuotas de memoria para un proceso</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Administradores, Servicio local, Servicio de red</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Permitir el inicio de sesión local</p></td>
<td style="border:1px solid black;"><p>Usuarios, Administradores</p></td>
<td style="border:1px solid black;"><p>Usuarios, Administradores</p></td>
<td style="border:1px solid black;"><p>Usuarios, Administradores</p></td>
<td style="border:1px solid black;"><p>Usuarios, Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Permitir inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Realizar copias de seguridad de archivos y directorios</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Omitir la comprobación de recorrido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cambiar la hora del sistema</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear un archivo de paginación</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Crear objetos compartidos permanentes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear un objeto Token</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Depurar programas</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el acceso desde la red a este equipo</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión como trabajo por lotes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el inicio de sesión localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0,<br />
Invitado, cualquier cuenta de servicio</p></td>
<td style="border:1px solid black;"><p>Support_<br />
388945a0, Invitado, cualquier cuenta de servicio</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Denegar inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Todos</p></td>
<td style="border:1px solid black;"><p>Todos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
</tbody>  
</table>
  
##### Tener acceso a este equipo desde la red
  
Esta configuración de directiva permite a otros usuarios de la red conectarse al equipo y constituye un requisito de diversos protocolos de red entre los que se incluyen los protocolos basados en bloques de mensajes de servidor (SMB), NetBIOS, el sistema común de archivos de Internet (CIFS) y el modelo de objetos componentes Plus (COM+).
  
El parámetro **Tener acceso a este equipo desde la red** se establece como **No está definido** para el entorno EC y como **Administradores** para el entorno SSLF.
  
##### Actuar como parte del sistema operativo
  
Esta configuración de directiva permite a un proceso asumir la identidad de cualquier usuario y obtener acceso de ese modo a los recursos autorizados al usuario.
  
Por eso, el parámetro **Actuar como parte del sistema operativo** queda restringido a **Ninguno** para los dos entornos que se tratan en este capítulo.
  
##### Ajustar las cuotas de memoria para un proceso
  
Esta configuración de directiva permite a un usuario ajustar la cantidad máxima de memoria disponible para un proceso. La posibilidad de ajustar cuotas de memoria resulta útil para optimizar el sistema, pero es susceptible de ser utilizada indebidamente. Si no está en buenas manos, podría utilizarse para iniciar un ataque de denegación de servicio.
  
Por ese motivo, el parámetro **Ajustar las cuotas de memoria para un proceso** queda restringido a **Administradores**, al **Servicio local** y al **Servicio de red** para los dos tipos de equipos en el entorno SSLF, y se configura como **No está definido** para los equipos del entorno EC.
  
##### Permitir el inicio de sesión local
  
Esta configuración de directiva determina qué usuarios pueden iniciar sesión interactivamente en los equipos de su entorno. Para los inicios de sesión con la secuencia del teclado Ctrl+Alt+Supr en el equipo del cliente se requiere este derecho de usuario. Este derecho también es necesario para los usuarios que intenten iniciar la sesión mediante los Servicios de Terminal Server o los Servicios de Internet Information Server (IIS) de Microsoft.
  
A la cuenta **Invitado** se le asigna este derecho de usuario de forma predeterminada. Aunque esta cuenta está deshabilitada de forma predeterminada, Microsoft recomienda habilitar este parámetro a través de Directiva de grupo. No obstante, por lo general se debe restringir este derecho de usuario a los grupos **Administradores** y **Usuarios**. Asigne este derecho de usuario a los **Operadores de copia de seguridad** si su organización requiere que tengan esta capacidad.
  
El parámetro **Permitir el inicio de sesión local** queda restringido a los grupos **Usuarios** y **Administradores** para los dos entornos que se tratan en este capítulo.
  
##### Permitir inicio de sesión a través de Servicios de Terminal Server
  
Esta configuración de directiva determina qué usuarios o grupos tienen derecho a iniciar sesión como cliente de Servicios de Terminal Server. Los usuarios de escritorio remoto requieren este derecho de usuario. Si su organización utiliza Asistencia remota como parte de su estrategia de soporte técnico, cree un grupo y asígnele este derecho de usuario a través de Directiva de grupo. Si el personal de asistencia de su organización no utiliza Asistencia remota, asigne este derecho de usuario sólo al grupo **Administradores** o utilice la característica de grupos restringidos para asegurarse de que ninguna cuenta de usuario forma parte del grupo **Usuarios de escritorio remoto.**
  
Restrinja este derecho de usuario al grupo **Administradores** y, si es posible, al grupo **Usuarios de escritorio remoto**, para evitar que usuarios no deseados obtengan acceso a equipos de la red por medio de la nueva característica Asistencia Remota en Windows XP Professional.
  
El parámetro **Permitir inicio de sesión a través de Servicios de Terminal Server** está configurado como **No está definido** para el entorno EC. Para mayor seguridad, esta configuración de directiva se establece como **Ninguno** en el entorno SSLF.
  
##### Realizar copias de seguridad de archivos y directorios
  
Esta configuración de directiva permite a los usuarios eludir los permisos de archivo y directorio para realizar una copia de seguridad del sistema. Este derecho de usuario se habilita sólo cuando una aplicación (como NTBACKUP) intenta tener acceso a un archivo o a un directorio a través de la interfaz de programación aplicaciones (API) de copia de seguridad del sistema de archivos NTFS. De lo contrario, se aplican los permisos asignados con respecto a los archivos y directorios.
  
El parámetro **Realizar copias de seguridad de archivos y directorios** se configura como **No está definido** para equipos en el entorno EC. Este parámetro de configuración de directiva se establece para el grupo **Administradores** en el entorno SSLF.
  
##### Omitir la comprobación de recorrido
  
Esta configuración de directiva permite a los usuarios que no tienen el permiso de acceso especial “Recorrer carpeta” pasar por las carpetas cuando se desplazan por una ruta de objetos en el sistema de archivos NTFS o en el Registro. Este derecho de usuario no permite a los usuarios enumerar el contenido de una carpeta; sólo atravesar los directorios.
  
El parámetro **Omitir la comprobación de recorrido** se configura como **No está definido** para equipos en el entorno EC. Se configura para los grupos **Administradores** y **Usuarios** en el entorno SSLF.
  
##### Cambiar la hora del sistema
  
Esta configuración de directiva determina qué usuarios y grupos pueden cambiar la hora y la fecha en el reloj interno de los equipos en su entorno. Los usuarios a los que se asigna este derecho pueden influir en el aspecto de los registros de eventos. Cuando se cambia la configuración de la hora en un equipo, los eventos registrados registran la nueva hora, no la hora real en que se produjeron.
  
El parámetro **Cambiar la hora del sistema** se configura para el grupo **Administradores** en los dos entornos que se tratan en este capítulo.
  
**Nota**: las discrepancias entre la hora del equipo local y la de los controladores de dominio en el entorno pueden acarrear problemas para el protocolo de autenticación Kerberos, lo cual puede imposibilitar que los usuarios inicien sesión en el dominio u obtengan autorización de acceso a los recursos del dominio tras iniciar sesión. Asimismo, surgirán problemas cuando se aplique Directiva de grupo a los equipos cliente si la hora del sistema no está sincronizada con los controladores de dominio.
  
##### Crear un archivo de paginación
  
Esta configuración de directiva permite a los usuarios cambiar el tamaño del archivo de paginación. Un atacante podría deteriorar el rendimiento de un equipo expuesto si modifica el tamaño de un archivo de paginación de modo que resulte extremadamente grande o pequeño.
  
El parámetro **Crear un archivo de paginación** se configura para **Administradores** en todos equipos del entorno EC y del entorno SSLF.
  
##### Crear objetos compartidos permanentes
  
Esta configuración de directiva permite a los usuarios crear objetos de directorio en el administrador de objetos. Este derecho de usuario resulta útil para componentes de modo de núcleo que amplían el espacio de nombres de objetos. Sin embargo, los componentes que se ejecutan en el modo de núcleo tienen intrínsecamente este derecho de usuario. Así pues, no suele ser necesario asignar este derecho de usuario de forma específica.
  
El parámetro **Crear objetos compartidos permanentes** se configura como **No está definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
##### Crear un objeto Token
  
Esta configuración de directiva permite a un proceso crear un símbolo (token) de acceso, que puede proporcionar derechos elevados para el acceso a datos confidenciales. En los entornos donde la seguridad es prioritaria, este derecho no debe ser asignado a ningún usuario. Cualquier proceso que requiera esta capacidad deberá utilizar la cuenta Sistema local, a la que se asigna este derecho de usuario de forma predeterminada.
  
El parámetro **Crear un objeto Token** se configura como **No está definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
##### Depurar programas
  
Esta configuración de directiva determina qué usuarios pueden adjuntar un depurador a cualquier proceso o al núcleo, lo que proporciona un acceso completo a componentes sensibles y críticos del sistema operativo. Este derecho de usuario es necesario cuando los administradores desean aprovechar la características de aplicación de revisiones en memoria. Para obtener más información acerca de las últimas características del instalador de paquetes de Microsoft, consulte el artículo sobre [el instalador de paquetes (antes Update.exe) para sistemas operativos Microsoft Windows y componentes de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/deployment/winupdte.mspx), en www.microsoft.com/technet/prodtechnol/windowsserver2003/deployment/winupdte.mspx. Dado que un atacante podría aprovechar este derecho de usuario, sólo se asigna al grupo **Administradores** de forma predeterminada.
  
**Nota**: Microsoft publicó en octubre de 2003 varias revisiones de seguridad en las que se utilizaba una versión de Update.exe que requería que el administrador dispusiera del derecho de usuario **Depurar programas.** Los administradores que no tenían este derecho de usuario no pudieron instalar estas revisiones hasta que reconfiguraron sus derechos de usuario. Para obtener más información, consulte el artículo de Microsoft Knowledge Base sobre [las actualizaciones de productos de Windows que pueden dejar de responder o que podrían utilizar la mayor parte de los recursos de la CPU](http://support.microsoft.com/default.aspx?kbid=830846), en http://support.microsoft.com/default.aspx?kbid=830846.
  
El derecho de usuario **Depurar programas** confiere una gran capacidad. Por lo tanto, esta configuración de directiva está establecida para **Administradores** en el entorno EC y se mantiene en la opción predeterminada **Ninguno** en el entorno SSLF.
  
##### Denegar el acceso desde la red a este equipo
  
Esta configuración de directiva prohíbe a los usuarios conectarse a un equipo a través de la red, una posibilidad que les permitiría obtener acceso a datos de forma remota y, en algunos casos, de modificarlos. En un entorno de alta seguridad no debe existir la necesidad de que los usuarios remotos tengan acceso a los datos de un equipo. En vez de eso, el uso compartido de archivos debería tener lugar a través de los servidores de la red.
  
El parámetro **Denegar el acceso desde la red a este equipo** se configura para las cuentas **Support\_388945a0** e **Invitado** en los equipos de los dos entornos que se tratan en este capítulo.
  
##### Denegar el inicio de sesión como trabajo por lotes
  
Esta configuración de directiva prohíbe el inicio de sesión a los usuarios a través de un servicio de cola por lotes, una característica de Windows Server 2003 que se utiliza para programar trabajos de modo que se ejecuten automáticamente una o varias veces con posterioridad.
  
El parámetro **Denegar el inicio de sesión como trabajo por lotes** se configura como **No está definido** para el entorno EC y como **Support\_388945a0** e **Invitado** para el entorno SSLF.
  
##### Denegar el inicio de sesión localmente
  
Esta configuración de directiva prohíbe a los usuarios un inicio de sesión local en la consola del equipo. Si un usuario no autorizado pudiera iniciar sesión localmente en un equipo, tendría la ocasión de descargar código malintencionado o de elevar sus privilegios en el equipo. (Si algún atacante tiene acceso físico a la consola, deben considerarse otros riesgos). Este derecho de usuario no debe asignarse a los usuarios que necesitan acceso físico a la consola del equipo.
  
El parámetro **Denegar el inicio de sesión localmente** se configura como **No está definido** para el entorno EC y como **Support\_388945a0** e **Invitado** para el entorno SSLF. Asimismo, a cualquier cuenta de servicio para el entorno SSLF que se agregue al equipo se le debe asignar este derecho de usuario para evitar su uso indebido.
  
##### Denegar inicio de sesión a través de Servicios de Terminal Server
  
Esta configuración de directiva prohíbe a los usuarios iniciar sesión en equipos de su entorno a través de conexiones de Escritorio remoto. Si asigna este derecho de usuario al grupo **Todos**, también impedirá a los miembros del grupo **Administradores** predeterminado que utilice Servicios de Terminal Server para iniciar sesión en equipos de su entorno.
  
El parámetro **Denegar inicio de sesión a través de Servicios de Terminal Server** se configura como **No está definido** en el entorno EC y para el grupo **Todos** en el entorno SSLF.
  
##### Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo
  
Esta configuración de directiva permite a los usuarios cambiar el parámetro **De confianza para la delegación** en un objeto de equipo en Active Directory. El uso indebido de este privilegio podría permitir a usuarios no autorizados suplantar a otros usuarios en la red.
  
Por ese motivo, el parámetro **Habilitar la opción De confianza para la delegación en las cuentas de equipo de usuario** se configura como **No está definido** en el entorno EC y como **Ninguno** en el entorno SSLF.
  
#### Derechos de usuario F –T
  
**Tabla 3.4 Recomendaciones para la configuración de asignaciones de derechos de usuario: Segunda parte**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Forzar el apagado de un sistema remoto</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Generar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Aumentar la prioridad de programación</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cargar y descargar controladores de dispositivo</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Bloquear páginas en la memoria</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Iniciar sesión como proceso por lotes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
<td style="border:1px solid black;"><p>Ninguno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Iniciar sesión como servicio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Servicio de red, Servicio local</p></td>
<td style="border:1px solid black;"><p>Servicio de red, Servicio local</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Administrar registros de auditoría y de seguridad</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Modificar variables de entorno del firmware</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Realizar tareas de mantenimiento de volúmenes</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Hacer perfil de un solo proceso</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Perfilar el rendimiento del sistema</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Quitar el equipo de la estación de acoplamiento</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Reemplazar un token a nivel de proceso</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
<td style="border:1px solid black;"><p>Servicio local, Servicio de red</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Restaurar archivos y directorios</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cerrar el sistema</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
<td style="border:1px solid black;"><p>Administradores, Usuarios</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tomar posesión de archivos u otros objetos</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
</tbody>  
</table>
  
Esta tabla resume las recomendaciones sobre asignaciones de derechos de usuario, para derechos que empiezan por las letras F hasta la T. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
##### Forzar el apagado de un sistema remoto
  
Esta configuración de directiva permite a los usuarios apagar equipos Windows XP desde ubicaciones remotas de la red. Cualquier usuario al que se le haya asignado este derecho puede provocar una situación de denegación del servicio (DoS), con lo que el equipo dejaría de estar disponible para las solicitudes del usuario del servicio. Por lo tanto, Microsoft recomienda que sólo se asigne este derecho de usuario a los administradores de máxima confianza.
  
El parámetro **Forzar el apagado desde un sistema remoto** se configura para el grupo **Administradores** en los dos entornos que se tratan en este capítulo.
  
##### Generar auditorías de seguridad
  
Esta configuración de directiva determina qué usuarios o procesos pueden generar registros de auditoría en el registro de seguridad. Un atacante podría utilizar esta capacidad para crear un gran número de eventos auditados, lo que dificultaría a un administrador de sistema la localización de una actividad ilícita. Asimismo, si el registro de eventos se configura para sobrescribir eventos según sea necesario, cualquier evidencia de actividades no autorizadas podría ser sobrescrita por una gran cantidad de eventos no relacionados.
  
Por ese motivo, el parámetro **Generar auditorías de seguridad** se configura para los grupos de **Servicio local** y **Servicio de red** en los dos entornos que se tratan en este capítulo.
  
##### Aumentar la prioridad de programación
  
Esta configuración de directiva permite a los usuarios cambiar la cantidad de tiempo de procesador que utiliza un proceso. Un atacante podría utilizar esta capacidad para aumentar la prioridad de un proceso a tiempo real y crear una situación de denegación de servicio para un equipo.
  
Por ese motivo, el parámetro **Aumentar la prioridad de programación** se configura para el grupo **Administradores** en los dos entornos que se tratan en este capítulo.
  
##### Cargar y descargar controladores de dispositivo
  
Esta configuración de directiva permite a los usuarios cargar dinámicamente un nuevo controlador de dispositivo en un sistema. Un atacante podría utilizar esta capacidad para instalar código malintencionado con la apariencia de un controlador de dispositivo. Este derecho de usuario y la pertenencia al grupo **Usuarios avanzados** o al grupo **Administradores** son necesarios para que los usuarios puedan agregar controladores de impresora o impresoras locales en Windows XP.
  
Dado que este derecho de usuario podría ser utilizado por un atacante, el parámetro **Cargar y descargar controladores de dispositivo** se configura para el grupo **Administradores** en los dos entornos que se tratan en este capítulo.
  
##### Bloquear páginas en la memoria
  
Esta configuración de directiva permite que un proceso mantenga datos en la memoria física. Esto evita que el sistema pagine los datos en la memoria virtual del disco. Si asigna este derecho al usuario, podría afectar de manera significativa al rendimiento del sistema.
  
Por ese motivo, el parámetro **Bloquear páginas en la memoria** se configura como **Ninguno** para los dos entornos que se tratan en este capítulo.
  
##### Iniciar sesión como proceso por lotes
  
Esta configuración de directiva permite que las cuentas inicien sesión mediante el servicio del programador de tareas. Dado que el programador de tareas se utiliza a menudo con fines administrativos, puede que se necesite en el entorno EC. Sin embargo, su uso debe ser restringido en el entorno SSLF para evitar la utilización indebida de recursos de sistema o para evitar que algún atacante utilice el derecho con el objetivo de iniciar código malintencionado tras obtener acceso de nivel de usuario a un equipo.
  
Por lo tanto, el parámetro **Iniciar sesión como proceso por lotes** se configura como **No está definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
##### Iniciar sesión como servicio
  
Esta configuración de directiva permite a las cuentas iniciar servicios de red o registrar un proceso como un servicio que se ejecuta en el sistema. Este derecho de usuario debe ser restringido en cualquier equipo de un entorno SSLF, pero dado que muchas aplicaciones pueden requerir este privilegio, se debe evaluar y probar detenidamente antes de configurarlo en un entorno EC.
  
El parámetro **Iniciar sesión como servicio** se configura como **No está definido** para el entorno EC y como **Servicio de red** y **Servicio local** para el entorno SSLF.
  
##### Administrar registros de auditoría y de seguridad
  
Esta configuración de directiva determina qué usuarios pueden cambiar las opciones de auditoría de archivos y directorios y borrar el registro de seguridad.
  
Dado que esta capacidad representa una amenaza relativamente moderada, el parámetro **Administrar registros de auditoría y seguridad** aplica el valor predeterminado del grupo **Administradores** a los dos entornos que se tratan en este capítulo.
  
##### Modificar variables de entorno del firmware
  
Esta configuración de directiva permite a los usuarios configurar las variables de entorno del sistema que afectan a la configuración de hardware. Esta información suele almacenarse en la última configuración válida conocida. La modificación de estos valores podría llevar a un error de hardware que provocaría una denegación de servicio.
  
Dado que esta capacidad representa una amenaza relativamente moderada, el parámetro **Modificar variables de entorno del firmware** aplica el valor predeterminado del grupo **Administradores** a los dos entornos que se tratan en este capítulo.
  
##### Realizar tareas de mantenimiento de volúmenes
  
Esta configuración de directiva permite a los usuarios administrar la configuración de volúmenes o discos del sistema, lo que podría permitir a un usuario eliminar un volumen y provocar una pérdida de datos, así como una denegación de servicio.
  
El parámetro **Realizar tareas de mantenimiento de volúmenes** aplica el valor predeterminado del grupo **Administradores** en los dos entornos que se tratan en este capítulo.
  
##### Hacer perfil de un solo proceso
  
Esta configuración de directiva determina qué usuarios pueden utilizar herramientas para supervisar el rendimiento de procesos que no son del sistema. Por lo general no es necesario configurar este derecho de usuario para utilizar el complemento Rendimiento de la Consola de Administración de Microsoft (MMC). Sin embargo, sí necesita este derecho de usuario si el monitor de sistema se configura para reunir datos con el Instrumental de administración de Windows (WMI). Con la restricción del derecho de usuario **Hacer perfil de un solo proceso**, se evita que los intrusos obtengan información adicional que puede utilizarse para llevar a cabo un ataque al sistema.
  
El parámetro **Hacer perfil de un solo proceso** se configura como **No está definido** para equipos del entorno EC y para el grupo **Administradores** en el entorno SSLF.
  
##### Perfilar el rendimiento del sistema
  
Esta configuración de directiva permite a los usuarios utilizar herramientas para ver el rendimiento de distintos procesos del sistema, posibilidad que se podría utilizar indebidamente para que un atacante determinara los procesos activos de un sistema y conociera mejor la superficie vulnerable a ataques en el equipo.
  
El parámetro **Perfilar el rendimiento del sistema** aplica la configuración predeterminada del grupo **Administradores** a los dos entornos que se tratan en este capítulo.
  
##### Quitar el equipo de la estación de acoplamiento
  
Esta configuración de directiva permite al usuario de un equipo portátil hacer clic en **Retirar equipo** en el menú **Inicio** para quitar el equipo de la estación de acoplamiento.
  
El parámetro **Quitar el equipo de la estación de acoplamiento** se configura para los grupos de **Administradores** y **Usuarios** en los dos entornos que se tratan en este capítulo.
  
##### Reemplazar un token a nivel de proceso
  
Esta configuración de directiva permite a un proceso o servicio iniciar otro servicio o proceso con un símbolo (token) de acceso de seguridad distinto, lo que se puede utilizar para modificar el símbolo de acceso de seguridad de ese subproceso y dar lugar a un incremento de privilegios.
  
El parámetro **Reemplazar un token a nivel de proceso** se configura con los valores predeterminados de **Servicio local** y **Servicio de red** para los dos entornos que se tratan en este capítulo.
  
##### Restaurar archivos y directorios
  
Esta configuración de directiva determina qué usuarios pueden evitar los permisos de archivo, directorio, registro y otros objetos persistentes al restaurar copias de seguridad de archivos y directorios en equipos con Windows XP del entorno. Este derecho de usuario determina también qué usuarios pueden establecer entidades principales de seguridad válidas como propietarios de objetos; es similar al derecho de usuario **Realizar copias de seguridad de archivos y directorios**.
  
El parámetro **Restaurar archivos y directorios** se configura como **No está definido** en equipos del entorno EC y para el grupo **Administradores** en el entorno SSLF.
  
##### Cerrar el sistema
  
Esta configuración de directiva determina qué usuarios que han iniciado sesión localmente en los equipos del entorno pueden cerrar el sistema operativo con el comando Apagar. El uso incorrecto de este derecho puede dar lugar a un situación de denegación de servicio. En entornos de alta seguridad, Microsoft recomienda que este derecho sólo sea asignado a los grupos **Administradores** y **Usuarios.**
  
El parámetro **Apagar el sistema** se configura para los grupos **Administradores** y **Usuarios** en los dos entornos que se tratan en este capítulo.
  
##### Tomar posesión de archivos u otros objetos
  
Esta configuración de directiva permite a los usuarios tomar posesión de archivos, carpetas, claves del Registro, procesos o subprocesos. Este derecho de usuario pasa por alto cualquier permiso diseñado para proteger objetos y proporcionar la posesión al usuario especificado.
  
El parámetro **Tomar posesión de archivos u otros objetos** está configurado con el valor predeterminado del grupo **Administradores** para los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Opciones de seguridad
  
La configuración de las opciones de seguridad que se aplican a través de Directiva de grupo en equipos de su entorno en los que se ejecuta Windows XP se utiliza para habilitar o deshabilitar capacidades y características tales como el acceso a unidades de disquete, el acceso a unidades de CD-ROM y los mensajes de inicio de sesión. Esta configuración se utiliza también para configurar otros parámetros, como los de firma digital de datos, nombres de cuenta de administrador e invitado, y el funcionamiento de la instalación de controladores.
  
Puede configurar las opciones de seguridad en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Seguridad\\Opciones**
  
No todas las configuraciones que se incluyen en esta sección existen en todos los tipos de sistemas. Por lo tanto, puede que los parámetros que incluyen la parte de Opciones de seguridad de Directiva de grupo que se definen en esta sección se deban modificar manualmente en los sistemas en los que se presentan para funcionar sin impedimentos. Asimismo, las plantillas de Directiva de grupo se pueden editar por separado para incluir las opciones de configuración adecuadas, de modo que las opciones de configuración recomendadas puedan aplicarse en su totalidad.
  
En las siguientes secciones se proporcionan recomendaciones para la configuración de opciones de seguridad, que se agrupan por tipo de objeto. Cada sección incluye una tabla en la que se resumen los parámetros de configuración, y en las subsecciones que siguen a cada tabla se proporciona información detallada. Las recomendaciones se proporcionan tanto para equipos cliente de escritorio como portátiles en los dos tipos de entornos seguros que se tratan en este capítulo: el de Cliente de empresa (EC) y el de Seguridad especializada: Funcionalidad limitada (SSLF).
  
#### Cuentas
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para las cuentas. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.5 Recomendaciones para la configuración de opciones de seguridad: Cuentas**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cuentas: estado de la cuenta de administrador</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cuentas: estado de la cuenta de invitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cuentas: cambiar el nombre de la cuenta del administrador</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cuentas: cambiar el nombre de la cuenta de invitado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
<td style="border:1px solid black;"><p>Recomendado</p></td>
</tr>  
</tbody>  
</table>
  
##### Cuentas: estado de la cuenta de administrador
  
Esta configuración de directiva habilita o deshabilita la cuenta del administrador durante el funcionamiento normal. Cuando un equipo se inicia en el modo a prueba de fallos, la cuenta del administrador siempre está habilitada, independientemente de la configuración de este parámetro.
  
El parámetro **Cuentas: estado de la cuenta de administrador** se configura como **No está definido** para el entorno EC y como **Habilitado** para el entorno SSLF.
  
##### Cuentas: estado de la cuenta de invitado
  
Esta configuración de directiva determina si la cuenta de invitado se habilita o se deshabilita. La cuenta de invitado permite a usuarios de red no autenticados obtener acceso al sistema.
  
El parámetro **Cuentas: estado de la cuenta de invitado** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola
  
Esta configuración de directiva determina si las cuentas locales que no están protegidas con contraseña se pueden utilizar para iniciar sesión desde ubicaciones distintas a la consola física del equipo. Si habilita esta configuración de directiva, las cuentas locales con contraseñas en blanco no podrán iniciar sesión en la red desde equipos cliente remotos. Dichas cuentas sólo podrán iniciar sesión a través del teclado del equipo.
  
El parámetro **Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Cuentas: cambiar el nombre de la cuenta del administrador
  
El nombre de la cuenta de administrador local integrada es bien conocido y constituye uno de los principales objetivos de los atacantes. Microsoft recomienda que elija otro nombre para esta cuenta y que evite los nombres que denotan cuentas administrativas o de acceso elevado. Asegúrese también de cambiar la descripción predeterminada del administrador local (a través de la consola de administración de equipos).
  
La recomendación de utilizar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** se aplica a los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva no se establece en las plantillas de seguridad, ni se sugiere un nuevo nombre de usuario para la cuenta en esta guía. Los nombres de usuario sugeridos se omiten para asegurar que las organizaciones que implementen esta guía no utilizarán el mismo nombre de usuario nuevo en sus entornos.
  
##### Cuentas: cambiar el nombre de la cuenta de invitado
  
La cuenta integrada de invitado local es otro de los nombres bien conocidos por los piratas informáticos. Microsoft también recomienda que cambie el nombre de esta cuenta para no revelar su propósito. Incluso si deshabilita esta cuenta de invitado (lo cual se recomienda), asegúrese de cambiar el nombre como medida de seguridad adicional.
  
La recomendación de utilizar el parámetro **Cuentas: cambiar el nombre de la cuenta de invitado** se aplica a los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva no se establece en las plantillas de seguridad, ni se sugiere un nuevo nombre de usuario para la cuenta en este documento. Los nombres de usuario sugeridos se omiten para asegurar que las organizaciones que implementen esta guía no utilizarán el mismo nombre de usuario nuevo en sus entornos.
  
#### Auditoría
  
La tabla siguiente resume la configuración de auditoría recomendada. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.6 Recomendaciones para la configuración de opciones de seguridad: Auditoría**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditoría: auditar el acceso de objetos globales del sistema</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditoría: auditar el uso del privilegio de copia de seguridad y restauración</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
</tr>  
</tbody>  
</table>
  
##### Auditoría: auditar el acceso de objetos globales del sistema
  
Esta configuración de directiva crea una Lista de control de acceso predeterminada del sistema (SACL) para objetos del sistema tales como exclusiones mutuas, eventos, semáforos, y dispositivos MS-DOS®, y provoca que se auditen estos objetos del sistema.
  
Si está habilitado el parámetro **Auditoría: Audita el acceso de objetos globales de sistema**, un gran número de eventos de seguridad podría llenar rápidamente el registro de eventos de seguridad. Por lo tanto, este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Deshabilitada** para el entorno SSLF.
  
##### Auditoría: auditar el uso del privilegio de copia de seguridad y restauración
  
Esta configuración de directiva determina si se debe auditar el uso de todos los privilegios de usuario, incluido el de copia de seguridad y restauración, cuando se habilita el parámetro **Auditar el uso de privilegios**. Si habilita ambas directivas, se generará un evento de auditoría para cada archivo del que se realiza una copia de seguridad o que se restaura.
  
Si está habilitado el parámetro **Auditoría: auditar el uso del privilegio de copia de seguridad y restauración**, un gran número de eventos de seguridad podría llenar rápidamente el registro de eventos de seguridad. Por lo tanto, este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Deshabilitada** para el entorno SSLF.
  
##### Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad
  
Esta configuración de directiva determina si el sistema se debe cerrar en caso de que no pueda registrar eventos de seguridad. Constituye un requisito para que las certificaciones Trusted Computer System Evaluation Criteria (TCSEC)-C2 y Common Criteria impidan que se produzcan eventos susceptibles de ser auditados si el sistema de auditoría no puede registrarlos. Microsoft ha decidido cumplir este requisito de forma que el sistema se detenga y muestre un mensaje de parada cuando se produce un error del sistema de auditoría. Cuando esta configuración de directiva esté habilitada, el sistema se cerrará si no se puede registrar una auditoría de seguridad por algún motivo.
  
Si está habilitado el parámetro **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad**, existe la posibilidad de que se produzcan errores inesperados en el sistema. Por lo tanto, esta configuración de directiva se establece como **No está definido** para los dos entornos que se tratan en este capítulo.
  
#### Dispositivos
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los dispositivos. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.7 Recomendaciones para la configuración de opciones de seguridad: Dispositivos**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Dispositivos: permitir el desbloqueo sin tener que iniciar sesión</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Dispositivos: permitir formatear y expulsar medios extraíbles</p></td>
<td style="border:1px solid black;"><p>Administradores, Interactive Users</p></td>
<td style="border:1px solid black;"><p>Administradores, Interactive Users</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Dispositivos: impedir que los usuarios instalen controladores de impresora</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Dispositivos: comportamiento de instalación de controlador no firmado</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
<td style="border:1px solid black;"><p>Avisar pero permitir la instalación</p></td>
</tr>  
</tbody>  
</table>
  
##### Dispositivos: permitir el desbloqueo sin tener que iniciar sesión
  
Esta configuración de directiva determina si un equipo portátil puede retirarse de la estación de acoplamiento en caso de que el usuario no haya iniciado sesión en el sistema. Habilite esta configuración de directiva para eliminar el requisito de inicio de sesión y permitir el uso de un botón de hardware externo para retirar el equipo. Si deshabilita esta configuración de directiva, a un usuario que no haya iniciado sesión se le debe haber asignado el derecho de usuario **Quitar el equipo de la estación de acoplamiento** (no definido en esta guía).
  
El parámetro **Dispositivos**: **permitir el desbloqueo sin tener que iniciar sesión** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
##### Dispositivos: permitir formatear y expulsar medios extraíbles
  
Esta configuración de directiva determina a quién se permite formatear y expulsar medios extraíbles. Puede utilizar esta configuración de directiva para evitar que usuarios no autorizados extraigan datos de un equipo para tener acceso a esa información en otro equipo para el que tienen privilegios de administrador local.
  
El parámetro **Dispositivos**: **permitir formatear y expulsar medios extraíbles** está restringido a los grupos **Administradores** y **Usuarios interactivos** en el entorno EC, y exclusivamente al grupo **Administradores** en el entorno SSLF para mayor seguridad.
  
##### Dispositivos: impedir que los usuarios instalen controladores de impresora
  
Los intrusos pueden conseguir que un programa troyano parezca un controlador de impresora. Este programa hace creer a los usuarios que deben utilizarlo para imprimir, pero en realidad puede introducir código malintencionado en la red del equipo. Para reducir las posibilidades de que ocurra algo así, la instalación de controladores de impresora sólo se debe permitir a los administradores. Sin embargo, dado que los equipos portátiles son dispositivos móviles, es probable que de vez en cuando sea necesario que los usuarios de estos equipos instalen un controlador de impresora desde un origen remoto, a fin de continuar su trabajo. Por tanto, esta configuración de directiva se debe deshabilitar para ese tipo de usuarios, aunque debe estar siempre habilitada para los usuarios de equipos de escritorio.
  
El parámetro **Dispositivos**: **impedir que los usuarios instalen controladores de impresora** se configura como **Habilitado** para los equipos de escritorio en los dos entornos que se tratan en este capítulo, y como **Deshabilitado** para usuarios de equipos portátiles en ambos entornos.
  
##### Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente
  
Esta configuración de directiva determina si pueden tener acceso simultáneamente a la unidad de CD-ROM los usuarios locales y remotos. Si habilita esta configuración de directiva, sólo los usuarios que han iniciado sesión interactivamente podrán obtener acceso a medios de la unidad de CD-ROM. Cuando está habilitada esta configuración de directiva y nadie ha iniciado sesión, el contenido de la unidad de CD-ROM estará disponible a través de la red. Si habilita esta configuración, la utilidad de copia de seguridad de Windows generará un error en caso de que se especificaran instantáneas de volumen para el trabajo de copia de seguridad. También se generará un error con cualquier producto de terceros cuando se deseen realizar copias de seguridad en las que se utilicen instantáneas de volumen.
  
El parámetro **Dispositivos**: **restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente** se configura como **No está definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
##### Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente
  
Esta configuración de directiva determina si pueden tener acceso simultáneamente a la unidad de disquete los usuarios locales y remotos. Si habilita esta configuración de directiva, sólo los usuarios que han iniciado sesión interactivamente podrán obtener acceso a medios de la unidad de disquete. Si esta configuración de directiva está habilitada y nadie ha iniciado sesión, el contenido de la unidad de disquete estará disponible a través de la red. Si habilita esta configuración, la utilidad de copia de seguridad de Windows generará un error en caso de que se especificaran instantáneas de volumen para el trabajo de copia de seguridad. También se generará un error con cualquier producto de terceros cuando se deseen realizar copias de seguridad en las que se utilicen instantáneas de volumen.
  
El parámetro **Dispositivos**: **restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente** se configura como **No está definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
##### Dispositivos: comportamiento de instalación de controlador no firmado
  
Esta configuración de directiva determina lo que sucede cuando se intenta instalar un controlador de dispositivo (mediante la API del programa de instalación) no aprobado o firmado por el Laboratorio de calidad de hardware de Windows \[Windows Hardware Quality Lab (WHQL)\]. Esta opción impide la instalación de controladores sin firmar o advierte al administrador de que un controlador sin firmar está a punto de ser instalado, con lo que se puede evitar la instalación de controladores que no están certificados para la ejecución en Windows XP. Si establece esta configuración de directiva con el valor **Avisar pero permitir la instalación**, un posible problema es que las secuencias de comandos de instalación desatendidas generen errores cuando intenten instalar controladores sin firmar.
  
Por ese motivo, el parámetro **Dispositivos**: **comportamiento de instalación de controlador no firmado** se configura como **Avisar pero permitir la instalación** para los dos entornos que se tratan en este capítulo.
  
**Nota**: si implementa esta configuración de directiva, los equipos cliente deben estar completamente configurados con todas las aplicaciones de software estándar antes de que se aplique la directiva de grupo para mitigar el riesgo de errores de instalación originados por el parámetro.
  
#### Miembro de dominio
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los miembros de dominio. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.8 Recomendaciones para la configuración de opciones de seguridad: Miembro de dominio**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Miembro de dominio: duración máxima de contraseña de cuenta de equipo</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
<td style="border:1px solid black;"><p>30 días</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)
  
Esta configuración de directiva determina si todo el tráfico de canal seguro iniciado por el miembro de dominio se debe firmar o cifrar. Si un sistema se ha configurado para cifrar o firmar datos de canal seguro siempre, no podrá establecer un canal seguro con un controlador de dominio que no sea capaz de firmar o cifrar todo el tráfico de canal seguro, ya que dichos datos estarán firmados y cifrados.
  
El parámetro **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)
  
Esta configuración de directiva determina si un miembro de dominio puede intentar negociar cifrado para todo el tráfico de canal seguro que inicia. Si habilita esta configuración de directiva, el miembro de dominio solicitará cifrado de todo el tráfico de canal seguro. Si deshabilita esta configuración de directiva, se impedirá que el miembro de dominio negocie cifrado de canal seguro.
  
El parámetro **Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)
  
Esta configuración de directiva determina si un miembro de dominio puede intentar negociar si debe cifrarse digitalmente todo el tráfico de canal seguro que inicia. Las firmas digitales protegen el tráfico frente a la posibilidad de que sea modificado por alguien que capture los datos cuando atraviesan la red.
  
El parámetro **Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo
  
Esta configuración de directiva determina si un miembro de dominio puede cambiar periódicamente su contraseña de cuenta en el equipo. Si habilita esta configuración de directiva, se impedirá al miembro de dominio cambiar su contraseña de cuenta en el equipo. Si deshabilita esta configuración de directiva, el miembro de dominio puede cambiar su contraseña de cuenta en el equipo según se especifica en el parámetro **Miembro de dominio: duración máxima de contraseña de cuenta de equipo**, que de forma predeterminada suele ser cada 30 días. Los equipos que no pueden cambiar automáticamente las contraseñas de sus cuentas son potencialmente vulnerables, dado que un atacante puede ser capaz de determinar la contraseña de la cuenta de dominio de sistema.
  
Por lo tanto, el parámetro **Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Miembro de dominio: duración máxima de contraseña de cuenta de equipo
  
Esta configuración de directiva determina la duración máxima admisible para una contraseña de cuenta de equipo. De forma predeterminada, los miembros de dominio cambian automáticamente sus contraseñas cada 30 días. Si aumenta este intervalo de forma significativa o se establece en 0 para que no se cambien las contraseñas de los equipos, se da más tiempo al atacante para emprender un ataque de fuerza bruta contra una de las cuentas de equipo.
  
Por lo tanto, el parámetro **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** se configura en **30 días** para los dos entornos que se tratan en este capítulo.
  
##### Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)
  
Cuando esta configuración de directiva está habilitada, sólo se puede establecer un canal seguro con controladores de dominio capaces de cifrar datos de canal seguro con una clave de sesión protegida (de 128 bits).
  
Para habilitar esta configuración de directiva, todos los controladores del dominio deben ser capaces de cifrar datos de canal seguro con una clave protegida, lo que significa que en todos los controladores de dominio debe estar ejecutándose Microsoft Windows 2000 o posterior. Si se requiere comunicación con dominios que no sean Windows 2000, Microsoft recomienda deshabilitar esta configuración de directiva.
  
El parámetro **Miembro de dominio: requerir clave de sesión protegida (Windows** **2000 o más reciente**) se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
#### Inicio de sesión interactivo
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el inicio de sesión interactivo. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.9 Recomendaciones para la configuración de opciones de seguridad: Inicio de sesión interactivo**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: no mostrar el último nombre de usuario</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión</p></td>
<td style="border:1px solid black;"><p>El acceso a este sistema está restringido a usuarios autorizados. Individuals attempting unauthorized access will be prosecuted.</p></td>
<td style="border:1px solid black;"><p>El acceso a este sistema está restringido a usuarios autorizados. Individuals attempting unauthorized access will be prosecuted.</p></td>
<td style="border:1px solid black;"><p>El acceso a este sistema está restringido a usuarios autorizados. Individuals attempting unauthorized access will be prosecuted.</p></td>
<td style="border:1px solid black;"><p>El acceso a este sistema está restringido a usuarios autorizados. Individuals attempting unauthorized access will be prosecuted.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión</p></td>
<td style="border:1px solid black;"><p>CONTINUAR SIN LA AUTORIZACIÓN PERTINENTE CONSTITUYE UN<br />
DELITO.</p></td>
<td style="border:1px solid black;"><p>CONTINUAR SIN LA AUTORIZACIÓN PERTINENTE CONSTITUYE UN<br />
DELITO.</p></td>
<td style="border:1px solid black;"><p>CONTINUAR SIN LA AUTORIZACIÓN PERTINENTE CONSTITUYE UN<br />
DELITO.</p></td>
<td style="border:1px solid black;"><p>CONTINUAR SIN LA AUTORIZACIÓN PERTINENTE CONSTITUYE UN<br />
DELITO.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>2</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
<td style="border:1px solid black;"><p>14 días</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
<td style="border:1px solid black;"><p>Bloquear estación de trabajo</p></td>
</tr>  
</tbody>  
</table>
  
##### Inicio de sesión interactivo: no mostrar el último nombre de usuario
  
Esta configuración de directiva determina si el nombre de la cuenta del último usuario que ha iniciado sesión en los equipos cliente de la organización aparecerá en la pantalla de inicio de sesión de Windows de cada equipo. Habilite esta configuración de directiva para impedir que algún intruso pueda ver los nombres de cuenta de las pantallas de equipos de escritorio o portátiles de la organización.
  
El parámetro **Inicio de sesión interactivo: no mostrar el último nombre de usuario** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr
  
La combinación de teclas Ctrl+Alt+Supr establece una ruta de confianza hacia el sistema operativo cuando un usuario determinado escribe un nombre de usuario y una contraseña. Cuando está habilitada esta configuración de directiva, no es necesario que los usuarios utilicen esta combinación de teclas para iniciar sesión en la red. Sin embargo, esta configuración conlleva un riesgo para la seguridad, ya que ofrece a los usuarios la oportunidad de iniciar sesión con credenciales no seguras.
  
El parámetro **Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión
  
Esta configuración de directiva especifica un mensaje de texto que se muestra a los usuarios cuando inician sesión. A menudo, este texto se utiliza por motivos legales; por ejemplo, para advertir a los usuarios acerca de las consecuencias del uso indebido de información empresarial o acerca de las acciones que se pueden auditar. El texto del mensaje que se especifica en la tabla anterior es un ejemplo recomendado para los entornos EC y SSLF.
  
El parámetro **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** está habilitado e incluye texto apropiado para los dos entornos que se tratan en este capítulo.
  
**Nota**: las advertencias que decida mostrar deben recibir la aprobación de los representantes de asuntos jurídicos y recursos humanos de su organización. Asimismo, las configuraciones **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** e **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar habilitadas para que una u otra funcione correctamente.
  
##### Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión
  
Esta configuración de directiva permite especificar texto en la barra de título de la ventana que ven los usuarios cuando inician sesión en el sistema. El razonamiento para utilizar esta configuración de directiva es el mismo que para el anterior parámetro de texto de mensaje. Las organizaciones que no utilizan esta configuración de directiva son más vulnerables legalmente ante los intrusos que ataquen el sistema.
  
Por lo tanto, el parámetro **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** está habilitado e incluye texto apropiado en los dos entornos que se tratan en este capítulo.
  
**Nota**: las advertencias que decida mostrar deben recibir la aprobación de los representantes de asuntos jurídicos y recursos humanos de su organización. Asimismo, las configuraciones **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** e **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar habilitadas para que una u otra funcione correctamente.
  
##### Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)
  
Esta configuración de directiva determina si un usuario puede iniciar sesión en un dominio de Windows utilizando la información de cuenta almacenada en caché. La información de inicio de sesión para cuentas de dominio se puede guardar localmente en caché para que los usuarios puedan iniciar sesión incluso si no es posible la comunicación con un controlador de dominio. Esta configuración de directiva determina el número de usuarios únicos cuya información de inicio de sesión se almacenará localmente en caché. El valor predeterminado de esta configuración de directiva es 10. Si este valor se establece en 0, la característica de caché de inicio de sesión se deshabilita. de forma que un atacante que tiene acceso al sistema de archivos del servidor podría localizar esta información almacenada en caché y realizar un ataque de fuerza bruta para determinar las contraseñas de usuario.
  
El parámetro **Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** se configura en **2** tanto para los equipos de escritorio como portátiles en el entorno EC y para los equipos portátiles en el entorno SSLF. Sin embargo, esta configuración de directiva se establece en **0** para los equipos de escritorio en el entorno SSLF porque estos equipos siempre debe estar conectados de forma segura a la red de la organización.
  
##### Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque
  
Esta configuración de directiva determina con cuánta antelación se advertirá a los usuarios de la fecha de caducidad de las contraseñas. Microsoft recomienda establecer esta configuración de directiva en 14 días para advertir con suficiente antelación a los usuarios de la fecha de caducidad de sus contraseñas.
  
El parámetro **Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque** se configura en **14 días** para los dos entornos que se tratan en este capítulo.
  
##### Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo
  
Cuando esta configuración de directiva está habilitada, un controlador de dominio debe autenticar la cuenta de dominio utilizada para desbloquear el equipo. Si esta configuración de directiva está deshabilitada, se pueden utilizar las credenciales en caché para desbloquear el equipo. Microsoft recomienda que esta configuración de directiva esté deshabilitada para los usuarios de equipos portátiles en ambos entornos, ya que éstos no disponen de acceso de red a controladores de dominio.
  
El parámetro **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo** se configura como **Habilitado** para los equipos de escritorio tanto en el entorno EC como SSLF. Sin embargo, esta configuración de directiva se establece como **Deshabilitada** para los equipos portátiles en los dos entornos, lo que permite a estos usuarios trabajar cuando no se encuentran en la propia oficina.
  
##### Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente
  
Esta configuración de directiva determina lo que ocurre cuando la tarjeta inteligente de un usuario que ha iniciado sesión se retira del lector de tarjetas inteligentes. Cuando se establece como **Bloquear estación de trabajo**, esta configuración de directiva bloquea la estación de trabajo en el momento en que se retira la tarjeta inteligente, lo que permite a los usuarios salir del área, llevarse sus tarjetas inteligentes y que sus estaciones de trabajo queden automáticamente bloqueadas. Si establece esta configuración de directiva como **Forzar cierre de sesión**, se cerrará automáticamente la sesión de los usuarios cuando se retire la tarjeta inteligente.
  
El parámetro **Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente** se configura con la opción **Bloquear estación de trabajo** para los dos entornos que se tratan en este capítulo.
  
#### Cliente de redes de Microsoft
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los equipos cliente de redes de Microsoft. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.10 Recomendaciones para la configuración de opciones de seguridad: Cliente de redes de Microsoft**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)
  
Esta configuración de directiva determina si el componente de cliente SMB requiere la firma de paquetes. Si habilita esta configuración de directiva, el equipo cliente de redes de Microsoft no puede comunicarse con un servidor de red Microsoft salvo que dicho servidor acepte la firma de paquetes SMB. En entornos combinados con equipos cliente heredados, esta opción se debe establecer como **Deshabilitado**, ya que dichos equipos no se podrán autenticar u obtener acceso a controladores de dominio. No obstante, puede utilizar esta configuración de directiva en entornos con Windows 2000 o versiones posteriores.
  
El parámetro **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Habilitado** para los equipos de los dos entornos que se tratan en este capítulo.
  
**Nota**: cuando los equipos con Windows XP tienen esta configuración de directiva habilitada y se conectan a recursos compartidos de archivos o impresión de servidores remotos, es importante que para dichos servidores el parámetro se sincronice con una opción complementaria, **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)**. Para obtener información más detallada acerca de esta configuración, vea la sección "Servidor y cliente de red de Microsoft: firmar digitalmente las comunicaciones (cuatro valores relacionados)" en el capítulo 5 de la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que se puede descargar en http://go.microsoft.com/fwlink/?LinkId=15159.
  
##### Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)
  
Esta configuración de directiva determina si el cliente SMB intentará negociar la firma de paquetes SMB. La implementación de firma digital en redes de Windows ayuda a evitar el secuestro de sesiones. Si habilita esta configuración de directiva, el cliente de redes de Microsoft utilizará la firma sólo si el servidor con el que se comunica acepta comunicación firmada digitalmente.
  
El parámetro **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: habilite esta configuración de directiva en los clientes SMB de la red para que puedan firmar paquetes con todos los equipos cliente y servidores del entorno.
  
##### Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes
  
Deshabilite esta configuración de directiva para evitar que durante la autenticación el redirector SMB envíe contraseñas de texto sin formato a servidores SMB que no son Microsoft ni admiten el cifrado de contraseñas. Microsoft recomienda deshabilitar esta configuración de directiva a no ser que exista una razón empresarial de peso para habilitarlo. Si esta configuración de directiva está habilitada, se permitirán contraseñas no cifradas en la red.
  
El parámetro **Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
#### Servidor de red Microsoft
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los servidores de red Microsoft. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.11 Recomendaciones para la configuración de opciones de seguridad: Servidores de red Microsoft**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión
  
Esta configuración de directiva le permite especificar el tiempo de inactividad que debe transcurrir de forma ininterrumpida en una sesión SMB antes de que la sesión se suspenda por inactividad. Los administradores pueden utilizar esta configuración de directiva para controlar el momento en que un equipo suspende una sesión SMB inactiva. Si se reanuda la actividad del cliente, la sesión se restablece automáticamente.
  
El parámetro **Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión** se configura como **Habilitado** por un período de **15 minutos** en los dos entornos que se tratan en este capítulo.
  
##### Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)
  
Esta configuración de directiva determina si el servicio SMB de servidor es necesario para la firma de paquetes SMB. Habilite esta configuración de directiva en un entorno mixto para evitar que los clientes indirectos utilicen la estación de trabajo como un servidor de red.
  
El parámetro **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)
  
Esta configuración de directiva determina si el servicio SMB de servidor puede firmar paquetes SMB cuando lo solicite un cliente que intenta establecer una conexión. Si no hay ninguna solicitud de firma procedente del cliente, se permitirá una conexión sin firma en caso de que no esté habilitado el parámetro **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)**.
  
El parámetro **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: habilite esta configuración de directiva en los clientes SMB de la red para que puedan firmar paquetes con todos los equipos cliente y servidores del entorno.
  
#### Acceso de red
  
En la tabla siguiente se resume la configuración recomendada de las opciones de seguridad para el acceso de red. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.12 Recomendaciones para la configuración de opciones de seguridad: Acceso de red**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso de red: permitir traducción SID/nombre anónima</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso de red: canalizaciones con nombre accesibles anónimamente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>* Consulte la siguiente descripción de configuración para ver la lista completa de canalizaciones con nombre</p></td>
<td style="border:1px solid black;"><p>* Consulte la siguiente descripción de configuración para ver la lista completa de canalizaciones con nombre</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso de red: rutas de Registro accesibles remotamente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>* Consulte la siguiente descripción de configuración para ver la lista completa de rutas de acceso</p></td>
<td style="border:1px solid black;"><p>* Consulte la siguiente descripción de configuración para ver la lista completa de rutas de acceso</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso de red: recursos compartidos accesibles anónimamente</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>comcfg, dfs$</p></td>
<td style="border:1px solid black;"><p>comcfg, dfs$</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso de red: modelo de seguridad y para compartir para cuentas locales</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
<td style="border:1px solid black;"><p>Clásico: usuarios locales autenticados como ellos mismos</p></td>
</tr>  
</tbody>  
</table>
  
##### Acceso de red: permitir traducción SID/nombre anónima
  
Esta configuración de directiva determina si un usuario anónimo puede solicitar atributos del identificador de seguridad (SID) para otro usuario, o utilizar un SID para obtener el nombre de usuario correspondiente. Deshabilite esta opción de directiva para evitar que usuarios no autenticados puedan obtener nombres de usuario que estén asociados a sus respectivos SID.
  
La opción **Acceso de red: permitir traducción SID/nombre anónima** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM
  
Esta configuración de directiva controla la capacidad de los usuarios anónimos para enumerar las cuentas en el Administrador de cuentas de seguridad (SAM). Si habilita esta configuración de directiva, los usuarios con conexiones anónimas no podrán enumerar nombres de usuario de cuentas de dominio en las estaciones de trabajo de su entorno. Esta configuración de directiva también permite restricciones adicionales en conexiones anónimas.
  
El parámetro **Acceso de red: no permitir enumeraciones anónimas de cuentas SAM** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM
  
Esta configuración de directiva controla la capacidad de los usuarios anónimos para enumerar cuentas SAM y recursos compartidos. Si habilita esta configuración de directiva, los usuarios anónimos no podrán enumerar nombres de usuario de cuentas de dominio ni nombres de recursos compartidos de red en las estaciones de trabajo de su entorno.
  
El parámetro **Acceso de red: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio
  
Esta configuración de directiva controla el almacenamiento de credenciales y contraseñas de autenticación en el sistema local.
  
El parámetro **Acceso de red: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos
  
Esta configuración de directiva determina qué permisos adicionales se asignan para conexiones anónimas al equipo. Si habilita esta configuración de directiva, se permite que los usuarios anónimos de Windows realicen ciertas actividades, tal como enumerar los nombres de cuentas de dominio y de recursos compartidos de red. Un usuario no autorizado podría obtener de forma anónima una lista de los nombres de las cuentas y los recursos compartidos y utilizar dicha información para intentar adivinar contraseñas o realizar ataques de ingeniería social.
  
Por lo tanto, el parámetro de configuración **Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Acceso de red: canalizaciones con nombre accesibles anónimamente
  
Esta configuración de directiva determina qué sesiones de comunicación, o canalizaciones, tendrán atributos y permisos que permitan el acceso anónimo.
  
Para el entorno EC, el parámetro **Acceso de red: canalizaciones con nombre accesibles anónimamente** se configura como **No está definido.** Sin embargo, se aplican los siguientes valores predeterminados para el entorno SSLF:
  
-   COMNAP
  
-   COMNODE
  
-   SQL\\QUERY
  
-   SPOOLSS
  
-   LLSRPC
  
-   Examinador
  
##### Acceso de red: rutas de Registro accesibles remotamente
  
Esta configuración de directiva determina qué rutas del Registro serán accesibles después de hacer referencia a la clave WinReg para determinar permisos de acceso a las rutas de acceso.
  
Para el entorno EC, el parámetro **Acceso de red: rutas de Registro accesibles remotamente** se configura como **No está definido.** Sin embargo, para el entorno SSLF se aplican los siguientes valores predeterminados:
  
-   System\\CurrentControlSet\\Control\\ProductOptions
  
-   System\\CurrentControlSet\\Control\\Print\\Printers
  
-   System\\CurrentControlSet\\Control\\Server Applications
  
-   System\\CurrentControlSet\\Control\\ContentIndex
  
-   System\\CurrentControlSet\\Control\\Terminal Server
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\UserConfig
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\DefaultUserConfiguration
  
-   System\\CurrentControlSet\\Services\\Eventlog
  
-   Software\\Microsoft\\OLAP Server
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion
  
##### Acceso de red: recursos compartidos accesibles anónimamente
  
Esta configuración de directiva determina a qué recursos compartidos de red pueden tener acceso los usuarios anónimos. El parámetro predeterminado de esta configuración de directiva tiene pocas repercusiones, ya que todos los usuarios se deben autenticar para poder obtener acceso a los recursos compartidos del servidor.
  
El parámetro **Acceso de red: recursos compartidos accesibles anónimamente** se configura como **No está definido** para el entorno EC. Sin embargo, debe asegurarse de que este parámetro se configure como **comcfg, dfs$** para el entorno SSLF.
  
**Nota**: puede ser muy peligroso agregar otros recursos compartidos a este parámetro de Directiva de grupo. Cualquier usuario de la red puede tener acceso a cualquier recurso compartido enumerado, lo que podría dar lugar a que datos confidenciales quedaran expuestos o resultaran dañados.
  
##### Acceso de red: modelo de seguridad y para compartir para cuentas locales
  
Esta configuración de directiva determina el modo en que se autentican los inicios de sesión de red que utilizan cuentas locales. La opción **Clásico** permite un control preciso del acceso a los recursos, incluida la capacidad de asignar distintos tipos de acceso a usuarios diferentes para el mismo recurso. La opción **Sólo invitado** le permite tratar a todos los usuarios del mismo modo. En este contexto, todos los usuarios se autentican como **Sólo invitado** para recibir el mismo nivel de acceso a un recurso determinado.
  
Por lo tanto, el parámetro **Modelo de seguridad y recursos compartidos para cuentas locales** utiliza la opción **Clásico** predeterminada para los dos entornos que se tratan en este capítulo.
  
#### Seguridad de red
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la seguridad de red. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.13 Recomendaciones para la configuración de opciones de seguridad: Seguridad de red**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Seguridad de red: nivel de autenticación de LAN Manager</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NTLMv2\rechazar LM</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NTLMv2\rechazar LM</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NT Lan Manager versión 2\rechazar Lan Manager y NT Lan Manager</p></td>
<td style="border:1px solid black;"><p>Enviar sólo respuesta NT Lan Manager versión 2\rechazar Lan Manager y NT Lan Manager</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad de red: requisitos de firma de cliente LDAP</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
<td style="border:1px solid black;"><p>Negociar firma</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
<td style="border:1px solid black;"><p>Necesita confidencialidad de mensaje, Necesita integridad de mensaje, Necesita seguridad<br />
de sesión NTLMv2, Necesita codificación de 128 bits</p></td>
</tr>
</tbody>
</table>
<p> </p>

##### Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña

Esta configuración de directiva determina si el valor de hash de LAN Manager (LM) para la contraseña nueva se almacena al cambiar la contraseña. El hash de LM es relativamente débil y propenso a ataques en comparación con el hash de Windows NT®, más seguro desde el punto de vista criptográfico.

Por este motivo, el parámetro **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.

**Nota**: puede que los sistemas operativos muy antiguos y algunas aplicaciones de terceros no funcionen correctamente cuando está habilitado este parámetro. Asimismo, será necesario cambiar la contraseña de todas las cuentas tras habilitarlo.

##### Seguridad de red: nivel de autenticación de LAN Manager

Esta configuración de directiva especifica el tipo de autenticación de desafío/respuesta para los inicios de sesión de red con clientes que no son Windows 2000 ni Windows XP Professional. La autenticación de LAN Manager (LM) es el método menos seguro; da ocasión a que se descifren las contraseñas cifradas porque pueden ser interceptadas fácilmente en la red. NT LAN Manager (NTLM) es un tanto más seguro. NTLMv2 es la versión más completa de NTLM disponible en Windows XP Professional, Windows 2000 y Windows NT 4.0 Service Pack 4 (SP4) o posteriores. NTLMv2 también se encuentra disponible para Windows 95 y Windows 98 con el cliente de servicios de directorio opcional.

Microsoft recomienda que establezca esta configuración de directiva en el nivel de autenticación más seguro que sea posible para su entorno. En entornos en los que las estaciones de trabajo ejecutan sólo Windows 2000 Server o Windows Server 2003 con Windows XP Professional, establezca esta configuración de directiva con la opción **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM** para contar con el máximo nivel de seguridad.

El parámetro **Seguridad de red: nivel de autenticación de LAN Manager** se configura como **Enviar sólo respuesta NTLMv2\\rechazar LM** para el entorno EC. Sin embargo, esta configuración de directiva se configura con el parámetro más restrictivo **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM** en el entorno SSLF.

##### Seguridad de red: requisitos de firma de cliente LDAP

Esta configuración de directiva determina el nivel de firma de datos que se solicita en nombre de clientes que emiten peticiones LDAP BIND. Dado que el tráfico de red sin firmar es susceptible de sufrir ataques de intermediario, un atacante podría provocar que un servidor LDAP tome decisiones basadas en consultas falsas del cliente LDAP.

Por consiguiente, el valor del parámetro **Seguridad de red: requisitos de firma de cliente LDAP** se configura como **Negociar firma** para los dos entornos que se tratan en este capítulo.

##### Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)

Esta configuración de directiva determina los estándares de seguridad mínimos en las comunicaciones de aplicación a aplicación para clientes. Las opciones para esta configuración de directiva son:

-   Necesita integridad de mensaje

-   Necesita confidencialidad de mensaje

-   Necesita seguridad de sesión NTLMv2

-   Necesita codificación de 128 bits

Si todos los equipos de su red pueden admitir NTLMv2 y cifrado de 128 bits (por ejemplo, Windows XP Professional SP2 y Windows Server 2003 SP1), se pueden seleccionar las cuatro opciones de configuración para contar con el máximo nivel de seguridad.

Las cuatro opciones se habilitan para el parámetro **Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)** en los dos entornos que se tratan en este capítulo.

##### Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)

Esta configuración de directiva es semejante al parámetro anterior, pero afecta al lado del servidor de la comunicación con las aplicaciones. Las opciones para el parámetro son las mismas:

-   Necesita integridad de mensaje

-   Necesita confidencialidad de mensaje

-   Necesita seguridad de sesión NTLMv2

-   Necesita codificación de 128 bits

Si todos los equipos de su red pueden admitir NTLMv2 y cifrado de 128 bits (por ejemplo, Windows XP Professional SP2 y Windows Server 2003 SP1), es posible seleccionar las cuatro opciones para contar con el máximo nivel de seguridad.

Las cuatro opciones se habilitan para el parámetro **Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)** en los dos entornos que se tratan en este capítulo.

#### Consola de recuperación

En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la consola de recuperación. Se proporciona información adicional en las subsecciones que siguen a la tabla.

**Tabla 3.14 Recomendaciones para la configuración de opciones de seguridad: Consola de recuperación**

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
<th><p>Configuración</p></th>
<th><p>EC: Escritorio</p></th>
<th><p>EC: Portátil</p></th>
<th><p>SSLF: Escritorio</p></th>
<th><p>SSLF: Portátil</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Consola de recuperación: permitir el inicio de sesión administrativo automático</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Consola de recuperación: permitir el inicio de sesión administrativo automático
  
La consola de recuperación es un entorno de línea de comandos que se utiliza para solucionar problemas en el sistema. Si habilita esta configuración de directiva, se iniciará automáticamente una sesión con la cuenta de administrador en la consola de recuperación al invocarla durante el inicio. Microsoft recomienda que deshabilite este parámetro de configuración de directiva, lo cual requerirá que los administradores introduzcan una contraseña para obtener acceso a la consola de recuperación.
  
El parámetro **Consola de recuperación: permitir el inicio de sesión administrativo automático** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
##### Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas
  
Mediante esta configuración de directiva estará disponible el comando SET de la consola de recuperación, lo que permitirá establecer las siguientes variables de entorno de consola de recuperación:
  
-   **AllowWildCards**. habilita la compatibilidad con comodines para algunos comandos (como el comando DEL).
  
-   **AllowAllPaths**. permite el acceso a todos los archivos y carpetas del equipo.
  
-   **AllowRemovableMedia**. permite la copia de archivos en medios extraíbles, como un disquete.
  
-   **NoCopyPrompt**. No solicita confirmación al sobrescribir un archivo existente.
  
El parámetro **Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas** se configura como **No está definido** para el entorno EC. Sin embargo, para contar con un máximo nivel de seguridad, este parámetro se configura como **Deshabilitado** para el entorno SSLF.
  
#### Apagado
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el apagado. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.15 Recomendaciones para la configuración de opciones de seguridad: Apagado**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Apagado: permitir apagar el sistema sin tener que iniciar sesión</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Apagado: borrar el archivo de paginación de la memoria virtual</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Apagado: permitir apagar el sistema sin tener que iniciar sesión
  
Esta configuración de directiva determina si un equipo se puede apagar cuando un usuario no ha iniciado sesión en él. Si se habilita esta configuración de directiva, el comando de apagado estará disponible en la pantalla de inicio de sesión de Windows. Microsoft recomienda que deshabilite esta configuración de directiva para restringir la capacidad de apagar el equipo a sólo aquellos usuarios con credenciales en el sistema.
  
El parámetro **Apagado: permitir apagar el sistema sin tener que iniciar sesión** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
##### Apagado: borrar el archivo de paginación de la memoria virtual
  
Esta configuración de directiva determina si el archivo de paginación de la memoria virtual se borra cuando se apaga el sistema. Con esta configuración de directiva habilitada, el archivo de paginación del sistema se borra cada vez que el sistema se apaga debidamente. Si se habilita esta opción de seguridad, el archivo de hibernación (Hiberfil.sys) se borra también cuando se deshabilita la hibernación en un equipo portátil. Aumentará el tiempo empleado en apagar y reiniciar el servidor, y será especialmente evidente en servidores con grandes archivos de paginación.
  
Por esos motivos, el parámetro **Apagado: borrar el archivo de paginación de la memoria virtual** se configura como **Deshabilitado** para todos los tipos de equipos en los dos entornos que se tratan en este capítulo.
  
#### Criptografía de sistema
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la criptografía de sistema. Se proporciona información adicional después de la tabla.
  
**Tabla 3.16 Recomendaciones para la configuración de opciones de seguridad: Criptografía de sistema**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash
  
Esta configuración de directiva determina si el proveedor de seguridad de Transport Layer Security/Secure Sockets Layer (TL/SS) es compatible sólo con el conjunto cifrado TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA. Aunque esta configuración de directiva aumenta la seguridad, la mayoría de los sitios web públicos que están protegidos con TLS o SSL no admiten estos algoritmos. Los equipos cliente que tienen habilitado este parámetro de configuración de directiva tampoco podrán conectarse a Servicios de Terminal Server en servidores que no estén configurados para utilizar los algoritmos compatibles con FIPS.
  
El parámetro **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
**Nota**: si habilita este parámetro de configuración de directiva, el rendimiento del equipo será más lento porque el proceso 3DES se realiza en cada bloque de datos del archivo tres veces. Únicamente se debe habilitar esta configuración de directiva en el caso de que la empresa deba cumplir la norma FIPS.
  
#### Objetos de sistema
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los objetos de sistema. Se proporciona información adicional en las subsecciones que siguen a la tabla.
  
**Tabla 3.17 Recomendaciones para la configuración de opciones de seguridad: Objetos de sistema**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
<td style="border:1px solid black;"><p>Creador de objetos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
##### Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores
  
Este parámetro de configuración de directiva determina si el grupo **Administradores** o el grupo **Creador de objetos** es el propietario predeterminado de los nuevos objetos de sistema.
  
Para proporcionar un mayor control, el parámetro **Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores** se configura como grupo **Creador de objetos** para los dos entornos que se tratan en este capítulo.
  
##### Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows
  
Esta configuración de directiva determina si no se requerirá la distinción entre mayúsculas y minúsculas en todos los subsistemas. El subsistema Microsoft Win32® hace distinción de mayúsculas y minúsculas. No obstante, el núcleo admite la distinción de mayúsculas y minúsculas para otros subsistemas, como la Interfaz de sistema operativo portátil de UNIX (POSIX). Dado que Windows no hace distinción de mayúsculas y minúsculas (pero el subsistema POSIX sí), si no se exige esta configuración un usuario del subsistema POSIX podrá crear un archivo con el mismo nombre que otro archivo utilizando mayúsculas y minúsculas en el nombre. Tal situación puede bloquear el acceso a esos archivos de otro usuario que utilice herramientas Win32 típicas, porque sólo uno de los archivos estará disponible.
  
Para asegurar la coherencia de nombres de archivo, el parámetro **Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows** se configura como **No está definido** para el entorno EC y como **Habilitado** para el entorno SSLF.
  
##### Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema
  
Esta configuración de directiva determina la fuerza de la lista de control de acceso discrecional (DACL) predeterminada de los objetos. El uso del parámetro ayuda a proteger objetos que pueden ser localizados y compartidos entre procesos, y su configuración predeterminada refuerza DACL, ya que permite a los usuarios que no son administradores leer objetos compartidos pero no les permite modificar los que no hayan creado.
  
Por lo tanto, el parámetro **Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema** (p. ej. vínculos simbólicos) se configura utilizando el valor predeterminado **Habilitado** para los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad del registro de eventos
  
El registro de eventos registra eventos en el sistema, y el registro de seguridad registra eventos de auditoría. El contenedor de registro de eventos de directiva de grupo se utiliza para definir atributos relacionados con la aplicación, la seguridad y los registros de eventos del sistema como, por ejemplo, el tamaño máximo del registro, los derechos de acceso para los registros, así como la configuración y los métodos de retención. Las configuraciones para los registros de eventos del sistema, seguridad y aplicación se establecen en la directiva de línea de base de servidores miembro (MSBP) y se aplican a todos los servidores miembro del dominio.
  
Puede establecer la configuración del registro de eventos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Registro de eventos**
  
En esta sección se proporcionan detalles acerca de la configuración recomendada para los entornos que se tratan en este capítulo. Para ver un resumen de la configuración recomendada en esta sección, consulte el libro de Microsoft Excel® sobre la configuración de la guía de seguridad denominado "Windows XP Security Guide Settings." Si desea información acerca de la configuración predeterminada y una explicación detallada de cada uno de los parámetros descritos en esta sección, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159. La guía complementaria incluye también información detallada acerca de la posibilidad de perder datos del registro de eventos cuando los tamaño del registro se establecen en valores muy elevados.
  
En la tabla siguiente se resume la configuración de seguridad recomendada para el registro de eventos, tanto para clientes de equipos de escritorio como de equipos portátiles en los dos tipos de entorno que se tratan en este capítulo, el entorno Cliente de empresa (EC) y el entorno Seguridad especializada: Funcionalidad limitada (SSLF). En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
**Tabla 3.18 Recomendaciones para la configuración de seguridad del registro de eventos**

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
<th><p>Configuración</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tamaño máximo del registro de la aplicación</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Tamaño máximo del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
<td style="border:1px solid black;"><p>81.920 KB</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tamaño máximo del registro del sistema</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
<td style="border:1px solid black;"><p>16.384 KB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro del sistema</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Método de retención del registro de la aplicación</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Método de retención del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Método de retención del registro del sistema</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
<td style="border:1px solid black;"><p>Según se necesite</p></td>
</tr>  
</tbody>  
</table>
  
#### Tamaño máximo del registro de la aplicación
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de la aplicación, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de aplicación varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
El parámetro **Tamaño máximo del registro de la aplicación** se establece en **16.384 KB** para todos los equipos en los dos entornos que se tratan en este capítulo.
  
#### Tamaño máximo del registro de seguridad
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de seguridad, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de seguridad varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
El parámetro **Tamaño máximo del registro de seguridad** se establece en **81.920 KB** para todos los equipos en los dos entornos que se tratan en este capítulo.
  
#### Tamaño máximo del registro del sistema
  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos del sistema, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de aplicación varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
El parámetro **Tamaño máximo del registro del sistema** se establece en **16.384 KB** para todos los equipos en los dos entornos que se tratan en este capítulo.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones
  
Esta configuración de directiva determina si se impide que los invitados tengan acceso al registro de eventos de la aplicación. De forma predeterminada, en Windows Server 2003 los invitados tienen prohibido el acceso a todos los sistemas. Por lo tanto, este parámetro de directiva no tiene una repercusión real en las configuraciones de sistema predeterminadas. No obstante, se considera una opción de seguridad extrema que no tiene efectos secundarios.
  
El parámetro **Evitar que el grupo de invitados locales tenga acceso al registro de aplicaciones** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro de seguridad
  
Esta configuración de directiva determina si se impide que los invitados tengan acceso al registro de eventos de seguridad. A un usuario se le debe asignar el derecho de usuario **Administrar registros de auditoría y seguridad** (que no se define en esta guía) para obtener acceso al registro de seguridad. Por lo tanto, este parámetro de directiva no tiene una repercusión real en las configuraciones de sistema predeterminadas. No obstante, se considera una opción de seguridad extrema que no tiene efectos secundarios.
  
El parámetro **Evitar que el grupo de invitados locales tenga acceso al registro de seguridad** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
#### Evitar que el grupo de invitados locales tenga acceso al registro del sistema
  
Esta configuración de directiva determina si se impide que los invitados tengan acceso al registro de eventos del sistema. De forma predeterminada, en Windows Server 2003 los invitados tienen prohibido el acceso a todos los sistemas. Por lo tanto, este parámetro de directiva no tiene una repercusión real en las configuraciones de sistema predeterminadas. No obstante, se considera una opción de seguridad extrema que no tiene efectos secundarios.
  
El parámetro **Evitar que el grupo de invitados locales tenga acceso al registro del sistema** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
#### Método de retención del registro de la aplicación
  
Esta configuración de directiva determina el método de "ajuste" del registro de la aplicación. Es de gran importancia que el registro de aplicaciones se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
La opción **Método de retención del registro de la aplicación** se configura como **Según se necesite** para los dos entornos que se tratan en este capítulo.
  
#### Método de retención del registro de seguridad
  
Esta configuración de directiva determina el método de "ajuste" del registro de seguridad. Es de gran importancia que el registro de seguridad se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
La opción **Método de retención del registro de seguridad** se configura como **Según se necesite** para los dos entornos que se tratan en este capítulo.
  
#### Método de retención del registro del sistema
  
Esta configuración de directiva determina el método de "ajuste" del registro del sistema. Es de gran importancia que el registro del sistema se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
La opción **Método de retención del registro del sistema** se configura como **Según se necesite** para los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Grupos restringidos
  
El parámetro Grupos restringidos permite administrar la pertenencia a los grupos de Windows XP Professional a través de la directiva de grupo de Active Directory. Primero, revise las necesidades de su organización para determinar los grupos que desea restringir. En esta guía, los grupos **Operadores de copia de seguridad** y **Usuarios avanzados** están restringidos en los dos entornos pero sólo el grupo **Usuarios de escritorio remoto** está restringido para el entorno SSLF. Los miembros de los grupos **Operadores de copia de seguridad** y **Usuarios avanzados** poseen un menor acceso al sistema que los miembros del grupo **Administradores**, si bien disponen de medios eficaces para hacerlo.
  
**Nota :** si su organización utiliza cualquiera de estos grupos, controle con cuidado su asociación y no implemente la guía para la configuración de Grupos restringidos. Si su organización agrega usuarios al grupo Usuarios avanzados, es posible que desee implementar los permisos opcionales de sistema de archivos que se describen posteriormente en la sección “Seguridad del sistema de archivos” de este capítulo.
  
**Tabla 3.19 Recomendaciones sobre grupos restringidos**

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
<th><p>Grupo local</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Operadores de copia de seguridad</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Usuarios avanzados</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Usuarios de Escritorio remoto</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
</tr>  
</tbody>  
</table>
  
Puede establecer la configuración Grupos restringidos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Grupos restringidos**
  
Los administradores pueden configurar grupos restringidos para un GPO mediante la adición del grupo que se desee directamente en el nodo **Grupos restringidos** del espacio de nombres de GPO.
  
Cuando un grupo está restringido, se pueden definir sus miembros así como otros grupos a los que pertenezca. Si no especifica esos miembros, el grupo queda totalmente restringido. Los grupos se pueden restringir únicamente mediante la utilización de las plantillas de seguridad.
  
**Para visualizar o modificar el parámetro Grupos restringidos**
  
1.  Abra Plantillas de seguridad de Microsoft Management Console (MMC).
  
    **Nota**: Plantillas de seguridad de Microsoft Management Console (MMC) no se incluye de forma predeterminada en el menú Herramientas administrativas. Para agregarlo, inicie Microsoft Management Console (mmc.exe) y agregue el complemento Plantillas de seguridad.
  
2.  Haga doble clic en el directorio del archivo de configuración y, a continuación, en el archivo.
  
3.  Haga doble clic en el elemento **Grupos restringidos**.
  
4.  Haga clic con el botón secundario en **Grupos restringidos** y seleccione **Agregar grupo**.
  
5.  Haga clic en los botones **Examinar** y **Ubicaciones**, seleccione las ubicaciones que desea examinar y después haga clic en **Aceptar**.
  
    **Nota**: normalmente, aparecerá un equipo local en el primer lugar de la lista.
  
6.  Escriba el nombre del grupo en el cuadro de texto **Escriba los nombres de objeto que desea seleccionar** y haga clic en el botón **Comprobar nombres**.
  
    - O bien -
  
    Haga clic en el botón **Avanzadas** y, a continuación, en **Buscar ahora** para que se muestre una lista de todos los grupos disponibles.
  
7.  Seleccione los grupos que desea restringir y, a continuación, haga clic en **Aceptar**.
  
8.  Haga clic en **Aceptar** en el cuadro de diálogo **Agregar grupos** para cerrarlo.
  
En esta guía se eliminó la configuración para todos los miembros (usuarios y grupos) de los grupos Usuarios avanzados y Operadores de copia de seguridad con objeto de restringirlos totalmente en ambos entornos. Además, en el entorno SSLF se eliminaron todos los miembros del grupo Usuarios de escritorio remoto. Microsoft recomienda que restrinja todos los grupos integrados que no prevea utilizar en su organización.
  
**Nota**: la configuración de Grupos restringidos que se describe en esta sección es muy sencilla. Las versiones de Windows XP SP1 o posteriores, así como Windows Server 2003, admiten diseños más complejos. Para más información, consulte el artículo de Microsoft Knowledge Base sobre [actualizaciones del comportamiento de grupos restringidos ("miembro de") de grupos locales definidos por el usuario](http://support.microsoft.com/default.aspx?kbid=810076), en http://support.microsoft.com/default.aspx?kbid=810076.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Servicios del sistema
  
Al instalar Windows XP Professional, los servicios del sistema predeterminados se crean y configuran para ejecutarse cuando se inicia el sistema. Muchos de estos servicios del sistema no necesitan ejecutarse en los entornos descritos en este capítulo.
  
Existen otros servicios opcionales disponibles con Windows XP Professional como, por ejemplo, los servicios de Internet Information Server (IIS), que no se incluyen durante la instalación predeterminada del sistema operativo. Puede agregar esos servicios opcionales a un sistema existente a través de Agregar o quitar programas, en el Panel de control, o bien crear una instalación automática personalizada de Windows XP Professional.
  
**Importante**: recuerde que cualquier servicio o aplicación supone un posible punto de ataque. Por tanto, conviene deshabilitar o quitar del entorno todos aquellos servicios o archivos ejecutables que no sean necesarios.
  
Puede establecer la configuración de los servicios del sistema en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Servicios del sistema**
  
Los administradores pueden establecer el modo de inicio de los servicios del sistema y cambiar la configuración de seguridad de todos ellos.
  
**Importante**: las versiones de las herramientas gráficas que se pueden utilizar para editar los servicios que se incluyeron con versiones anteriores a Windows 2003 del sistema operativo Windows aplican automáticamente los permisos a cada servicio al configurar cualquiera de las propiedades de un servicio. Las herramientas como el Editor de objetos de directiva de grupo y el complemento Plantillas de seguridad de MMC utilizan el DLL Editor de configuración de seguridad para aplicar esos permisos. Si los permisos predeterminados se cambian, se producirán varios problemas para muchos servicios. Microsoft recomienda que no altere los permisos en los servicios que se incluyen con Windows XP o Windows Server 2003, porque los permisos predeterminados son ya bastante restrictivos.  
La versión de Windows Server 2003 del DLL Editor de configuración de seguridad no le exige que configure los permisos cuando edita las propiedades de un servicio. Para obtener más información, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159)*,* que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
En la tabla siguiente se resume la configuración recomendada de servicios del sistema tanto para clientes de escritorio como portátiles en los dos tipos de entornos que se tratan en este capítulo: el entorno Cliente de empresa (EC) y el entorno Seguridad especializada: Funcionalidad limitada (SSLF). En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
**Tabla 3.20 Recomendaciones para la configuración de seguridad de los servicios del sistema**
  
<table style="width:100%;">  
<colgroup>  
<col width="16%" />  
<col width="16%" />  
<col width="16%" />  
<col width="16%" />  
<col width="16%" />  
<col width="16%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Nombre del servicio</p></th>  
<th><p>Nombre para mostrar</p></th>  
<th><p>EC: Escritorio</p></th>  
<th><p>EC: Portátil</p></th>  
<th><p>SSLF: Escritorio</p></th>  
<th><p>SSLF: Portátil</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servicio de alerta</p></td>
<td style="border:1px solid black;"><p>Servicio de alerta</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>ClipSrv</p></td>
<td style="border:1px solid black;"><p>Portafolios</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Examinador</p></td>
<td style="border:1px solid black;"><p>Examinador de equipos</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Fax</p></td>
<td style="border:1px solid black;"><p>Fax</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSFtpsvr</p></td>
<td style="border:1px solid black;"><p>Publicación FTP</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>IISADMIN</p></td>
<td style="border:1px solid black;"><p>Administración IIS</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>cisvc</p></td>
<td style="border:1px solid black;"><p>Servicio de Index Server</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Messenger</p></td>
<td style="border:1px solid black;"><p>Messenger</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>mnmsrvc</p></td>
<td style="border:1px solid black;"><p>Escritorio remoto compartido de NetMeeting®</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>RDSessMgr</p></td>
<td style="border:1px solid black;"><p>Administrador de sesión de Ayuda de escritorio remoto</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>RemoteAccess</p></td>
<td style="border:1px solid black;"><p>Enrutamiento y acceso remoto</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SNMP</p></td>
<td style="border:1px solid black;"><p>Servicio SNMP</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SNMPTRAP</p></td>
<td style="border:1px solid black;"><p>Servicio de captura SNMP</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SSDPSrv</p></td>
<td style="border:1px solid black;"><p>Servicio de descubrimientos SSDP</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Programación</p></td>
<td style="border:1px solid black;"><p>Programador de tareas</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TlntSvr</p></td>
<td style="border:1px solid black;"><p>Telnet</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TermService</p></td>
<td style="border:1px solid black;"><p>Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Upnphost</p></td>
<td style="border:1px solid black;"><p>Host de dispositivo Plug and Play universal</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>W3SVC</p></td>
<td style="border:1px solid black;"><p>Publicación de World Wide Web</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
#### Servicio de alerta
  
Este servicio notifica las alertas administrativas a los usuarios y equipos seleccionados. Puede utilizarlo para enviar mensajes de alerta a usuarios especificados que estén conectados a la red.
  
El **Servicio de alerta** se configura como **Deshabilitado** para evitar que se envíe información a través de la red. Esta configuración garantiza un mayor nivel de seguridad para los dos entornos que se tratan en este capítulo.
  
**Nota**: la funcionalidad de los sistemas de mensajes de alerta del sistema de alimentación ininterrumpida (UPS) puede verse afectada si deshabilita este servicio.
  
#### Portafolios
  
Este servicio permite que el Visor del Portafolios cree y comparta “páginas” de datos que se pueden visualizar en equipos remotos. El servicio depende del servicio DDE de red (NetDDE) para crear los recursos compartidos de archivo a los que otros equipos se pueden conectar, mientras que el servicio y la aplicación **Portafolios** permiten crear las páginas de datos que se compartirán. Todos los servicios que dependen directamente de éste darán error. Sin embargo, Clipbrd.exe se puede utilizar para visualizar el Portapapeles local, en el que se almacenan los datos cuando un usuario selecciona texto y, a continuación, hace clic en **Copiar** del menú **Edición** o presiona CTRL+C.
  
El servicio **Portafolios** se configura como **Deshabilitado** para garantizar un mayor nivel de seguridad en los dos entornos que se tratan en este capítulo.
  
#### Examinador de equipos
  
Este servicio mantiene una lista actualizada de los equipos de la red y la proporciona a los programas que la solicitan. El servicio es utilizado por equipos basados en Windows que necesitan visualizar recursos y dominios de red.
  
Para un mayor nivel de seguridad, el servicio **Examinador de equipos** se establece en **No está definido** para el entorno EC y en **Deshabilitado** para el entorno SSLF.
  
#### Fax
  
Este servicio, compatible con la API de telefonía (TAPI), proporciona capacidades de fax para los clientes del entorno. El servicio permite a los usuarios enviar y recibir faxes desde las aplicaciones del escritorio, a través de un dispositivo de fax local o compartido en la red.
  
El **Servicio de fax** se configura como **No está definido** para los equipos del entorno EC. Sin embargo, se configura como **Deshabilitado** para el entorno SSLF con el fin de garantizar un máximo nivel de seguridad.
  
#### Publicación FTP
  
Este servicio proporciona conectividad y administración a través del complemento IIS de MMC. Microsoft recomienda que no se instale este servicio en clientes Windows XP de su entorno a menos que exista una necesidad empresarial.
  
El servicio **Publicación FTP** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
#### Administración IIS
  
Este servicio permite administrar los componentes de IIS, como por ejemplo ftp, grupos de aplicaciones, sitios web y extensiones de servicios web. Deshabilite este servicio para impedir que los usuarios ejecuten en sus equipos sitios web o FTP, que no se necesitan en la mayoría de los equipos cliente Windows XP.
  
El servicio **Administración de IIS** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
#### Servicio de Index Server
  
Este servicio genera un índice del contenido y las propiedades de archivos en equipos locales y remotos, y ofrece acceso inmediato a archivos a través de un lenguaje de consulta flexible. El servicio también permite la “búsqueda rápida” de documentos en equipos locales y remotos, y proporciona un índice de búsqueda para el contenido que se comparte en la Web.
  
Los **servicios de Index Server** se configuran como **No está definido** para los equipos en el entorno EC. Sin embargo, se configura como **Deshabilitado** para el entorno SSLF con el fin de garantizar un máximo nivel de seguridad.
  
#### Messenger
  
Este servicio transmite y envía mensajes del **Servicio de alerta** entre clientes y servidores. Este servicio no está relacionado con Windows Messenger ni con MSN Messenger, y no es un requisito para los equipos clientes Windows XP.
  
Por este motivo, el servicio de **Mensajería** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Escritorio remoto compartido de NetMeeting
  
Este servicio permite que un usuario autorizado tenga acceso de forma remota a un cliente con Microsoft NetMeeting a través de una intranet de la organización. Este servicio se debe habilitar explícitamente en NetMeeting. Puede deshabilitar también esta característica en NetMeeting, cerrar el servicio por medio de un icono de la bandeja de Windows o deshabilitar esta característica en Directiva de grupo configurando el parámetro **Desactivar el uso compartido de escritorio remoto**, descrito en el capítulo 4, "Plantillas administrativas para Windows XP". Microsoft recomienda que deshabilite este servicio para impedir el acceso a sus clientes desde ubicaciones remotas.
  
El servicio **Escritorio remoto compartido de NetMeeting** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Administrador de sesión de Ayuda de escritorio remoto
  
Este servicio administra y controla la característica Asistencia remota en la aplicación Centro de ayuda y soporte técnico (Helpctr.exe).
  
El servicio **Administrador de sesión de Ayuda de escritorio remoto** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
#### Enrutamiento y acceso remoto
  
Este servicio proporciona los servicios de enrutamiento de varios protocolos: LAN a LAN, LAN a WAN, VPN y NAT. Este servicio también proporciona servicios de acceso telefónico y acceso remoto VPN.
  
El servicio **Enrutamiento y acceso remoto** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
#### Servicio SNMP
  
Este servicio permite al equipo local atender las solicitudes de entrada del protocolo simple de administración de redes (SNMP). El **servicio SNMP** incluye agentes que supervisan la actividad de los dispositivos de la red e informan a la estación de trabajo de la consola de red.
  
El **servicio SNMP** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Servicio de captura SNMP
  
Este servicio intercepta mensajes generados por agentes SNMP locales o remotos y los reenvía a programas de administración SNMP que se ejecutan en el equipo. El **Servicio SNMP**, cuando se ha configurado para un agente, genera mensajes de captura si se produce algún evento específico. Estos mensajes se envían a un destino de capturas.
  
El **servicio de captura SNMP** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Servicio de descubrimientos SSDP
  
Este servicio proporciona el Host de Plug and Play universal con la capacidad de localizar e identificar dispositivos de red UPnP. Si deshabilita el **Servicio de descubrimientos SSDP**, impedirá que el sistema busque dispositivos UPnP en la red y el servicio Host de Plug and Play universal no podrá encontrar dispositivos UPnP e interactuar con ellos.
  
El **servicio de descubrimientos SSDP** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Programador de tareas
  
Este servicio permite configurar y programar tareas automatizadas en el equipo. El servicio supervisa los criterios seleccionados y realiza las tareas si se cumplen estos.
  
El servicio **Programador de tareas** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
#### Telnet
  
Este servicio para Windows proporciona sesiones de terminal ASCII a los clientes Telnet. El servicio admite dos tipos de autenticación y los cuatro tipos de terminales siguientes: ANSI, VT-100, VT-52 y VTNT. No obstante, no supone un requisito para la mayor parte de los clientes Windows XP.
  
El servicio **Telnet** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
#### Servicios de Terminal Server
  
Este servicio proporciona un entorno con varias sesiones que permite a los dispositivos cliente obtener acceso a una sesión del escritorio de Windows virtual y a programas basados en Windows que se ejecutan en el servidor. En Windows XP, este servicio permite que los usuarios remotos estén conectados de forma interactiva a un equipo, además de mostrar escritorios y aplicaciones en equipos remotos.
  
El servicio **Servicios de Terminal Server** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
#### Host de Plug and Play universal
  
Este servicio admite la funcionalidad Plug and Play de igual a igual para dispositivos de red. La especificación UPnP está diseñada para simplificar la instalación y administración del servicio de red y dispositivos. UPnP lleva a cabo la detección y el control de dispositivos y servicios a través de mecanismos basados en protocolos estándar sin controladores. Los dispositivos Plug and Play universales pueden configurar automáticamente el direccionamiento de red, anunciar su presencia en una subred de la red y habilitar el intercambio de descripciones de dispositivos y servicios. Un equipo con Windows XP puede actuar como punto de control UPnP para detectar y controlar los dispositivos a través de una interfaz web o de aplicación.
  
El servicio **Plug and Play universal** se configura como **No está definido** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
#### Publicación de World Wide Web
  
Este servicio proporciona conectividad y administración web a través del complemento IIS de MMC. Proporciona servicios HTTP para aplicaciones sobre la plataforma Windows y contiene un administrador de procesos y un administrador de configuraciones. No obstante, no supone un requisito para la mayor parte de los clientes Windows XP.
  
El servicio **Publicación de World Wide Web** se establece en **Deshabilitado** en los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Parámetros adicionales del registro
  
Se han creado entradas de valores del Registro adicionales para los archivos de plantilla de seguridad de línea de base que no se han definido en el archivo de plantilla administrativa (.adm) para los dos entornos de seguridad que se tratan en este capítulo.
  
Esta configuración se incrusta en las plantillas de seguridad (en la sección "Opciones de seguridad") para automatizar su implementación. La eliminación de la directiva no supondrá la eliminación automática de dichos valores de configuración; éstos se deberán cambiar manualmente con una herramienta de edición del Registro como Regedt32.exe.
  
En esta guía se incluyen parámetros de configuración adicionales que se agregan al Editor de configuración de seguridad (SCE); para ello, se modifica el archivo Sceregvl.inf (ubicado en la carpeta **%windir%\\inf**) y se vuelve a registrar el archivo Scecli.dll. Los parámetros originales de la configuración de seguridad y los adicionales aparecen bajo **Directivas Locales\\Opciones de seguridad** en los complementos y las herramientas enumerados anteriormente en este capítulo. Es necesario actualizar el archivo Sceregvl.inf y volver a registrar Scecli.dll como se describe en la siguiente subsección, “Modificación de la interfaz de usuario del Editor de configuración de seguridad”, en todos los equipos que requieran la edición de las plantillas de seguridad y las directivas de grupo que se proporcionan con esta guía.
  
En la tabla siguiente se resumen las recomendaciones de los parámetros de Registro adicionales, tanto para equipos cliente de escritorio como portátiles en los dos tipos de entorno que se tratan en este capítulo: el entorno Cliente de empresa (EC) y el entorno Seguridad especializada: Funcionalidad limitada (SSLF).
  
La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla. Para obtener información acerca de la configuración predeterminada y una explicación detallada de cada uno de los parámetros, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
**Tabla 3.21 Parámetros adicionales del Registro**

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
<th><p>Nombre de la configuración</p></th>  
<th><p>Escritorio EC<br />  
</p></th>  
<th><p>Equipo portátil EC<br />  
</p></th>  
<th><p>Escritorio SSLF<br />  
</p></th>  
<th><p>Equipo portátil SSLF<br />  
</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Highest Protection, source routing is completely disabled.</p></td>
<td style="border:1px solid black;"><p>Highest Protection, source routing is completely disabled.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (KeepAliveTime)How often keep-alive packets are sent in milliseconds</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>30000 or 5 minutes (recommended)</p></td>
<td style="border:1px solid black;"><p>30000 or 5 minutes (recommended)</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering (recommended)</p></td>
<td style="border:1px solid black;"><p>El tráfico de multidifusión, difusión e ISAKMP está exento (mejor para Windows XP)</p></td>
<td style="border:1px solid black;"><p>El tráfico de multidifusión, difusión e ISAKMP está exento (mejor para Windows XP)</p></td>
<td style="border:1px solid black;"><p>El tráfico de multidifusión, difusión e ISAKMP está exento (mejor para Windows XP)</p></td>
<td style="border:1px solid black;"><p>El tráfico de multidifusión, difusión e ISAKMP está exento (mejor para Windows XP)</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)</p></td>
<td style="border:1px solid black;"><p>255, disable autorun for all drives</p></td>
<td style="border:1px solid black;"><p>255, disable autorun for all drives</p></td>
<td style="border:1px solid black;"><p>255, disable autorun for all drives</p></td>
<td style="border:1px solid black;"><p>255, disable autorun for all drives</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Connections timeout sooner if attack is detected</p></td>
<td style="border:1px solid black;"><p>Connections timeout sooner if attack is detected</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (TCPMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>3 &amp; 6 seconds, half-open connections dropped after 21 seconds</p></td>
<td style="border:1px solid black;"><p>3 &amp; 6 seconds, half-open connections dropped after 21 seconds</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (TCPMaxDataRetransmissions) How many times unacknowledged data is retransmitted (3 recommended, 5 is default)</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>3</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>90</p></td>
<td style="border:1px solid black;"><p>90</p></td>
</tr>  
</tbody>  
</table>
  
#### (AutoAdminLogon) Enable Automatic Logon
  
Se agregó la entrada de valor del Registro **AutoAdminLogon** al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\**. La entrada aparece como **MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)** en el SCE.
  
Este parámetro es independiente de la característica **pantalla de bienvenida** en Windows XP; si esa característica se deshabilita, el parámetro no se deshabilita. Si configura un equipo para inicio de sesión automático, cualquier persona que pueda obtener acceso físicamente al equipo puede obtener acceso también a sus recursos, incluida cualquier red a la que se conecte el equipo. Además, si habilita el inicio de sesión automático, la contraseña se almacena en el Registro como texto sin formato y la clave de Registro específica que almacena este valor será legible de forma remota para el grupo **Usuarios autenticados**. Por dichos motivos el parámetro se configura como **No está definido** para el entorno EC, y el valor predeterminado **Deshabilitado** se implanta explícitamente para el entorno SSLF.
  
Para obtener información adicional, consulte el artículo de Microsoft Knowledge Base "[Habilitar el inicio de sesión automático en Windows XP](http://support.microsoft.com/default.aspx?scid=315231)", que está disponible en línea en http://support.microsoft.com/default.aspx?scid=315231.
  
#### (DisableIPSourceRouting) IP source routing protection level
  
La entrada de valor de Registro **DisableIPSourceRouting** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)** en el SCE.
  
El enrutamiento de origen IP es un mecanismo que permite al remitente determinar la ruta IP que un datagrama debe tomar a través de la red. Este parámetro se configura como **No está definido** para el entorno EC y como **Highest Protection, source routing is completely disabled** para el entorno SSLF.
  
#### (EnableDeadGWDetect) Allow automatic detection of dead network gateways
  
La entrada de valor de Registro **EnableDeadGWDetect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)** en el SCE.
  
Cuando se habilita la detección de puertas de enlace inactivas, la IP puede cambiar a una puerta de enlace de reserva si varias conexiones experimentan dificultades. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Deshabilitada** para el entorno SSLF.
  
#### (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes
  
La entrada de valor de Registro **EnableICMPRedirect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes** en el SCE.
  
Las redirecciones del protocolo ICMP (Protocolo de mensajes de control de Internet) hacen que la pila instale rutas de host. Estas rutas reemplazan a las rutas generadas con OSPF (Abrir primero la ruta de acceso más corta). Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Deshabilitada** para el entorno SSLF.
  
#### (Hidden) Hide the Computer from Network Neighborhood Browse Lists
  
La entrada de valor de Registro **Hidden** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Lanmanserver\\Parameters\\**. La entrada aparece como **MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)** en el SCE.
  
Puede configurar un equipo para que no envíe anuncios a exploradores en el dominio. Si lo hace, ocultará el equipo de la lista de búsqueda, lo que significa el equipo dejará de anunciarse a otros equipos de la misma red. Un atacante que sabe el nombre de un equipo puede recopilar con más facilidad información adicional acerca del sistema. Puede habilitar este parámetro para eliminar uno de los métodos que podría utilizar cualquier atacante para recopilar información acerca de los equipos de la red. Este parámetro también puede ayudar a reducir tráfico de red cuando está habilitado. Sin embargo, no son muchas las ventajas que aporta este parámetro desde el punto de vista de la seguridad, porque los atacantes pueden utilizar métodos alternativos para identificar y localizar los destinos potenciales. Por este motivo, Microsoft recomienda que habilite este parámetro sólo en entornos de alta seguridad.
  
Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Habilitada** para el entorno SSLF.
  
Para obtener información adicional, consulte el artículo de Microsoft Knowledge Base acerca del [procedimiento de ocultación de un equipo Windows 2000 de la lista del examinador](http://support.microsoft.com/default.aspx?scid=321710), que está disponible en línea en http://support.microsoft.com/default.aspx?scid=321710.
  
#### (KeepAliveTime) How often keep-alive packets are sent in milliseconds
  
La entrada de valor de Registro **KeepAliveTime** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds (300,000 is recommended)** en el SCE.
  
Este valor controla con qué frecuencia TCP intenta comprobar que una conexión inactiva sigue intacta, enviando un paquete de mantenimiento de conexión. Si todavía se puede tener acceso al equipo remoto, confirma el paquete de mantenimiento de conexión. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **30000 o 5 minutos** para el entorno SSLF.
  
#### (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering
  
La entrada de valor del Registro **NoDefaultExempt** se agregó a esta pantalla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\IPSEC\\**. La entrada aparece como **MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering (recommended)** en el SCE.
  
Las exenciones predeterminadas para filtros de la directiva IPsec se documentan en la ayuda en pantalla de Microsoft Windows 2000 y Windows XP. Estos filtros permiten que funcione el intercambio de claves de Internet (IKE) y el protocolo de autenticación Kerberos. Los filtros también permiten que la calidad de servicio de red (QoS) se señalice (RSVP) cuando el tráfico de datos está protegido por IPsec, y para el tráfico que IPsec no pueda proteger como tráfico de multidifusión y de difusión.
  
IPsec se utiliza cada vez más para el filtrado básico de paquetes de servidor de seguridad de host, especialmente en situaciones expuestas de Internet y la repercusión de esas exenciones predeterminadas no se conoce completamente. Por lo tanto, algunos administradores de IPsec pueden crear directivas IPsec que consideran seguras, pero no lo son realmente contra los ataques entrantes que utilizan las exenciones predeterminadas. Microsoft recomienda que se aplique la configuración predeterminada en Windows XP con SP 2, **El tráfico de multidifusión, difusión e ISAKMP está exento**, para los dos entornos que se tratan en este capítulo.
  
Para obtener información adicional, consulte el artículo de Microsoft Knowledge Base sobre [la posibilidad de utilizar las exenciones predeterminadas de IPsec para pasar por alto la protección IPsec en algunas situaciones](http://support.microsoft.com/default.aspx?scid=811832), disponible en línea en http://support.microsoft.com/default.aspx?scid=811832.
  
#### (NoDriveTypeAutoRun) Disable Autorun for all drives
  
Se ha agregado la entrada de valor del Registro **NoDriveTypeAutoRun** al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\**  
**Policies\\Explorer\\**. La entrada aparece como **MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)** en el SCE.
  
La ejecución automática inicia la lectura de una unidad del equipo tan pronto como se insertan los medios en la misma. Como resultado, el archivo de configuración de programas y el sonido en medios de audio se inicia inmediatamente. Este parámetro se configura como **255, disable autorun for all drives** para los dos entornos que se tratan en este capítulo.
  
#### (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers
  
La entrada de valor de Registro **NoNameReleaseOnDemand** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Netbt\\Parameters\\**. La entrada aparece como **MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers** en el SCE.
  
NetBIOS sobre TCP/IP es un protocolo de red que, entre otras cosas, proporciona una manera de resolver fácilmente los nombres NetBIOS registrados en sistemas basados en Windows para las direcciones IP que se configuran en esos sistemas. Esta configuración determina si el equipo libera su nombre NetBIOS al recibir una solicitud de liberación de nombre. Se estable en **No está definido** para el entorno EC y en **Habilitado** para el entorno SSLF.
  
#### (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames
  
La entrada de valor de Registro **NtfsDisable8dot3NameCreation** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\FileSystem\\**. La entrada aparece como **MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)** en el SCE.
  
Windows Server 2003 admite formatos de nombre de archivo 8.3 para la compatibilidad con aplicaciones de 16 bits anteriores. La convención del nombre de archivo 8.3 es un formato de nombre que permite nombres de archivo con una longitud máxima de ocho caracteres. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Habilitada** para el entorno SSLF.
  
#### (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses
  
La entrada de valor de Registro **PerformRouterDiscovery** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)** en el SCE.
  
Este parámetro se utiliza para habilitar o deshabilitar el protocolo IRDP (Internet Router Discovery Protocol), que permite al sistema detectar y configurar automáticamente las direcciones predeterminadas de puerta de enlace, como se describe en RFC 1256 en función de la interfaz. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y se establece la configuración **Habilitada** para el entorno SSLF.
  
#### (SafeDllSearchMode) Enable Safe DLL Search Order
  
La entrada de valor de Registro **SafeDllSearchMode** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Control\\Session Manager\\**. La entrada aparece como **MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)** en el SCE.
  
La orden de búsqueda de DLL se puede configurar para que busque los archivos DLL que han solicitado los procesos en curso de una de estas dos formas:
  
-   Buscar primero en las carpetas especificadas en la ruta de acceso del sistema para, a continuación, buscar en la carpeta de trabajo actual.
  
-   Buscar primero en la carpeta de trabajo actual para, a continuación, buscar en las carpetas especificadas en la ruta de acceso del sistema.
  
Cuándo se habilita, el valor de Registro se establece en **1**. Con un valor **1**, el sistema busca primero las carpetas que se especifican en la ruta de acceso del sistema y después busca la carpeta de trabajo actual. Cuando se deshabilita, el valor de Registro se establece en **0** y el sistema busca primero la carpeta de trabajo actual y después busca las carpetas que se especifican en la ruta de acceso del sistema. Esta configuración se establece como **Habilitada** para los dos entornos que se tratan en este capítulo.
  
#### (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires
  
Se ha agregado la entrada de valor del Registro **ScreenSaverGracePeriod** al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\SYSTEM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\**  
**Winlogon\\**. La entrada aparece como **MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)** en el SCE.
  
Windows incluye un período de gracia que abarca desde que se inicia el protector de pantalla hasta el momento en el que se bloquea la consola de forma automática y se habilita el bloqueo del protector de pantalla. Esta configuración se establece en **0** segundos para los dos entornos que se tratan en este capítulo.
  
#### (SynAttackProtect) Syn attack protection level
  
La entrada de valor de Registro **SynAttackProtect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)** en el SCE.
  
Esta configuración hace que TCP ajuste la retransmisión de SYN-ACK. Al configurar este valor, las respuestas de conexión exceden el tiempo de espera más rápidamente en caso de que se detecte un ataque de solicitud de conexión (SYN). Este parámetro se configura como **No está definido** para el entorno EC y como **Connections timeout sooner if attack is detected** (Agotar antes el tiempo de espera de las conexiones si se detecta un ataque) para el entorno SSLF.
  
#### (TCPMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged
  
La entrada de valor de Registro **TCPMaxConnectResponseRetransmissions** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (TcpMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged** en el SCE.
  
Este parámetro determina el número de veces que TCP retransmite un SYN antes de que el intento de conexión se anule. El tiempo de espera de retransmisión se dobla con cada retransmisión sucesiva en un intento de conexión concreto. El valor de tiempo de espera inicial es de tres segundos. Este parámetro se configura como **No está definido** para el entorno EC y como **3 & 6 seconds, half-open connections dropped after 21 seconds** para el entorno SSLF.
  
#### (TCPMaxDataRetransmissions) How many times unacknowledged data is retransmitted
  
La entrada de valor de Registro **TCPMaxDataRetransmissions** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (TcpMaxDataRetransmissions) How many times unacknowledged data is retransmitted (3 recommended, 5 is default)** en el SCE.
  
Esta configuración controla el número de veces que TCP retransmite un segmento de datos individual (segmento sin conexión) antes de que se anule la conexión. El tiempo de espera de retransmisión se duplicará con cada retransmisión sucesiva en una conexión. Se restablece cuando se reanudan las respuestas. El valor base de tiempo de espera está determinado de forma dinámica por el tiempo de recorrido completo medido en la conexión. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y en **3** para el entorno SSLF.
  
#### (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning
  
La entrada de valor de Registro **WarningLevel** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Services\\Eventlog\\Security\\**. La entrada aparece como **MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning** en el SCE.
  
Este parámetro está disponible con SP3 para Windows 2000 y es una característica nueva que puede generar una auditoría de seguridad en el registro de eventos de seguridad cuando el registro alcanza un umbral definido por el usuario. Este parámetro de configuración de directiva se establece como **No está definido** para el entorno EC y en **90** para el entorno SSLF.
  
**Nota**: si la configuración del registro se define como **Sobrescribir eventos cuando sea necesario** como **Sobrescribir eventos que tengan más de x días**, no se generará este evento.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Modificación de la interfaz de usuario del Editor de configuración de seguridad
  
El conjunto de herramientas del Editor de configuración de seguridad (SCE) se utiliza para definir plantillas de directiva de seguridad que se pueden aplicar a equipos individuales o a cualquier número de equipos a través de Directiva de grupo. Las plantillas de seguridad pueden contener directivas de contraseña, directivas de bloqueo, directivas de protocolo de autenticación Kerberos, directivas de auditoría, valores de configuración del registro de eventos, valores de registro, modos de inicio del servicio, permisos del servicio, derechos de usuario, restricciones de pertenencia a grupos, permisos de registro y permisos de sistema de archivos. El SCE aparece en varios complementos de MMC y herramientas de administrador. Lo utiliza el complemento Plantillas de seguridad y el complemento Configuración y análisis de seguridad. El complemento Editor de objetos de directiva de grupo lo utiliza para la parte de configuración de seguridad del árbol de configuración del equipo, y también lo utiliza para la configuración de seguridad local, para la Directiva de seguridad del controlador de dominio y para las herramientas de Directiva de seguridad de dominio.
  
En esta guía se incluyen los parámetros de configuración adicionales que se agregaron al SCE. Para agregar esos parámetros, debe modificar el archivo Sceregvl.inf, que se encuentra en la carpeta **%systemroot%\\inf**, y volver a registrar el archivo Scecli.dll.
  
**Importante**: la versión personalizada del archivo Sceregvl.inf que se crea a partir de los procedimientos siguientes utiliza características que están sólo disponibles en Windows XP Professional con SP 2 y Windows Server 2003. No trate de instalar el archivo personalizado en versiones más antiguas de Windows.
  
Después de modificar y registrar el archivo Sceregvl.inf, los valores de Registro personalizados se exponen en las interfaces de usuario del SCE del equipo en cuestión. Verá la configuración nueva en la parte inferior de la lista de elementos del SCE (todos están precedidos por el texto "MSS:"). MSS significa Microsoft Solutions for Security, nombre del grupo que creó esta guía. Podrá crear plantillas de seguridad o directivas que definan esos nuevos valores de Registro y que se puedan aplicar a cualquier equipo, independientemente de si el archivo Sceregvl.inf se modificó en el equipo de destino o no. Los lanzamientos posteriores del SCE expondrán su valores de Registro personalizados.
  
Algunos parámetros que aparecerán en el SCE no se documentan en esta guía porque normalmente no se configuran para sistemas de usuario final. Para obtener más información acerca de esos parámetros nuevos, puede consultar la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que se puede descargar en http://go.microsoft.com/fwlink/?LinkId=15159.
  
Las instrucciones acerca de cómo modificar la interfaz de usuario de SCE se proporcionan en los procedimientos siguientes. Hay instrucciones manuales que debe seguir si ya ha realizado otras personalizaciones en SCE. Se proporciona una secuencia de comandos para agregar los parámetros de configuración con poca intervención del usuario y, aunque la secuencia de comandos integra funciones de detección de errores y recuperación, puede fallar. Si falla, debería determinar la causa del error y corregir el problema o seguir las instrucciones manuales. Se proporciona otra secuencia de comandos que puede utilizar para restaurar la interfaz de usuario de SCE a su estado predeterminado. Esta secuencia de comandos quitará todos los parámetros personalizados y devolverá el SCE a la forma en que aparece en una instalación predeterminada de Windows XP con SP2 o Windows Server 2003 con SP1.
  
**Para actualizar manualmente Sceregvl.inf**
  
1.  Utilice un editor de texto, como Bloc de notas, para abrir el archivo **Values-sceregvl.txt** de la carpeta **SCE Update** de la descarga de esta guía.
  
2.  Abra otra ventana en el editor de texto y después abra el archivo **%systemroot%\\inf\\sceregvl.inf.**
  
3.  Desplácese hasta el final de la sección “\[Register Registry Values\]” en el archivo **sceregvl.inf.** Copie y pegue el texto del archivo **Values-sceregvl.txt**, sin saltos de página, en esa sección del archivo **sceregvl.inf.**
  
4.  Cierre el archivo **Values-sceregvl.txt** y abra el archivo **Strings-sceregvl.txt** en la carpeta **SCE Update** de la descarga.
  
5.  Desplácese hasta el final de la sección “\[Strings\]” en el archivo **sceregvl.inf**. Copie y pegue el texto del archivo **Strings-sceregvl.txt**, sin saltos de página, en esa sección del archivo **sceregvl.inf**.
  
6.  Guarde el archivo **sceregvl.inf** y cierre el editor de texto.
  
7.  Abra un símbolo del sistema y ejecute el comando **regsvr32 scecli.dll** para registrar de nuevo el archivo DLL.
  
Los lanzamientos posteriores del SCE mostrarán estos valores de registro personalizados.
  
**Para actualizar automáticamente sceregvl.inf**
  
1.  Los archivos **Values-sceregvl.txt, Strings-sceregvl.txt** y **Update\_SCE\_with\_MSS\_Regkeys.vbs** que hay en la carpeta **SCE Update** de la descarga de esta guía deben encontrarse en la misma ubicación para que funcione la secuencia de comandos.
  
2.  Ejecute la secuencia de comandos **Update\_SCE\_with\_MSS\_Regkeys.vbs** en el equipo que desea actualizar.
  
3.  Siga los cuadros de diálogo que aparecen en pantalla.
  
Con este procedimiento se quitarán sólo las entradas personalizadas que se hicieron con la secuencia de comandos descrita en el procedimiento anterior, **Update\_SCE\_with\_MSS\_Regkeys.vbs.**
  
**Para deshacer los cambios realizados por la secuencia de comandos Update\_SCE\_with\_MSS\_Regkeys.vbs**
  
1.  Ejecute la secuencia de comandos **Rollback\_SCE\_for\_MSS\_Regkeys.vbs** en el equipo que desea actualizar.
  
2.  Siga los cuadros de diálogo que aparecen en pantalla.
  
Este procedimiento quitará *todas* las entradas personalizadas que haya podido agregar a la interfaz de usuario de SCE, incluidas las de esta guía y otras que se pueden haber proporcionado en versiones anteriores de esta guía o en otras guías de seguridad.
  
**Para restaurar el SCE a su estado predeterminado para Windows XP con SP2 o Windows Server 2003 con SP1**
  
1.  Los archivos **sceregvl\_W2K3\_SP1.inf.txt, sceregvl\_XPSP2.inf.txt** y **Restore\_SCE\_to\_Default.vbs** que se encuentran en la carpeta **SCE Update** de la descarga de esta guía deben estar en la misma ubicación para que funcione la secuencia de comandos.
  
2.  Ejecute la secuencia de comandos **Restore\_SCE\_to\_Default.vbs** en el equipo que desea actualizar.
  
3.  Siga los cuadros de diálogo que aparecen en pantalla.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
Aunque la mayor parte de las contramedidas utilizadas para reforzar los sistemas cliente en los dos entornos que se tratan en este capítulo se aplicaron a través de Directiva de grupo, hay parámetros adicionales cuya aplicación es difícil o imposible con Directiva de grupo. Para ver una explicación detallada de cada una de las contramedidas tratadas en esta sección, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
#### Procedimientos de consolidación manual
  
En esta sección se describe cómo se implementaron manualmente algunas contramedidas adicionales para proteger a los clientes Windows XP en cada uno de los entornos de seguridad que se definen en esta guía.
  
##### Deshabilitar Dr. Watson: deshabilitar la ejecución automática del depurador de sistema Dr. Watson
  
Algunas organizaciones pueden considerar que los depuradores de sistema, como la herramienta Dr. Watson incluida con Windows, podrían ser aprovechados por atacantes expertos. Para obtener instrucciones acerca de cómo deshabilitar el depurador del sistema Dr. Watson, consulte el artículo de Microsoft Knowledge Base "[Cómo deshabilitar Dr. Watson para Windows"](http://support.microsoft.com/default.aspx?scid=188296), que está disponible en línea en http://support.microsoft.com/default.aspx?scid=188296.
  
##### Deshabilitar SSDP/UPNP: Deshabilitar SSDP/UPNP
  
Algunas organizaciones pueden considerar que las características de Plug and Play universal que se incluyen con subcomponentes de Windows XP se deben deshabilitar completamente. Aunque el servicio **Plug and Play universal** está deshabilitado en esta guía, otras aplicaciones como Windows Messenger utilizarán el proceso del **servicio de detección SSDP (Simple Service Discovery Protocol)** para identificar puertas de enlace de red u otros dispositivos de red. Puede asegurarse de que ninguna aplicación utilice las funciones SSDP y UPnP incluidas en Windows XP si agrega un valor de Registro REG\_DWORD llamado **UPnPMode** a la clave de Registro **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DirectPlayNATHelp\\DPNHUPnP\\** y estableciendo su valor en **2**.
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base donde se describe [cómo se envía el tráfico tras desactivar el servicio de detección SSDP y Host de dispositivo Plug and Play universal](http://support.microsoft.com/default.aspx?scid=317843), y que está disponible en línea en http://support.microsoft.com/default.aspx?scid=317843.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Seguridad del sistema de archivos
  
El sistema de archivos NTFS se ha mejorado en cada nueva versión de Microsoft Windows. Los permisos predeterminados para NTFS resultan suficientes para la mayor parte de las organizaciones. Los parámetros de configuración que se tratan en esta sección son para las organizaciones que utilizan equipos portátiles y de escritorio en el entorno Seguridad especializada: Funcionalidad limitada (SSLF) que se define en esta guía.
  
La configuración del sistema de archivos se puede modificar a través de la directiva de grupo. Puede establecer la configuración del sistema de archivos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Sistema de archivos**
  
**Nota**: los cambios realizados a la configuración de seguridad predeterminada del sistema de archivos se deben probar minuciosamente en un entorno de laboratorio antes de que se implementen en una organización de gran tamaño. Han existido casos en los que se han alterado los permisos de archivo hasta tal punto que fue necesario reconstruir por completo los equipos afectados.
  
Los permisos de archivo predeterminados en Windows XP son suficientes para la mayoría de las situaciones. Sin embargo, si no va a bloquear la pertenencia del grupo **Usuarios avanzados** con la característica Grupos restringidos o si va a habilitar la opción **Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos**, tal vez desee aplicar los permisos opcionales que se describen en el párrafo siguiente. Esos permisos opcionales son muy específicos y aplican restricciones adicionales a ciertas herramientas ejecutables que un usuario malintencionado con privilegios elevados puede utilizar para comprometer más el sistema o la red.
  
Tenga en cuenta que esos cambios de permisos no afectan a varias carpetas ni a la raíz del volumen del sistema. Puede ser muy arriesgado cambiar los permisos de esa manera, y hacerlo puede causar en muchos casos inestabilidad en el sistema. Todos los archivos se encuentran en la carpeta **%SystemRoot%\\System32\\** y se les aplican los permisos siguientes: **Administradores: Control total, Sistema: Control total.**
  
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
  
Para su comodidad, esos permisos opcionales ya están configurados en la plantilla de seguridad denominada Optional-File-Permissions.inf, que se incluye con la versión para la descarga de esta guía.
  
#### Permisos avanzados
  
Puede configurar en el cuadro de diálogo **Permisos** los permisos de archivos con un mayor control del que parecen ofrecer inicialmente. Para ello, haga clic en el botón **Opciones avanzadas.** En la tabla siguiente se describen esos permisos avanzados.
  
**Tabla 3.22 Permisos de archivo avanzados y descripciones**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Nombre de permiso avanzado</p></th>  
<th><p>Descripción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Recorrer carpeta/Ejecutar archivo</p></td>
<td style="border:1px solid black;"><p>Permite o rechaza las peticiones de usuarios para desplazarse de unas carpetas a otras con el fin de llegar a otros archivos o carpetas, incluso si el usuario no posee permiso para recorrer las carpetas (se aplica únicamente a las carpetas).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Listar carpeta/Leer datos</p></td>
<td style="border:1px solid black;"><p>Permite o rechaza las peticiones de usuarios para visualizar nombres de archivos y subcarpetas que se encuentren dentro de la carpeta especificada. Sólo afecta al contenido de esa carpeta y no influye en si la carpeta en la que establece el permiso se va a enumerar (se aplica sólo a carpetas).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Atributos de lectura</p></td>
<td style="border:1px solid black;"><p>Permite o deniega la capacidad de ver datos en archivos (se aplica sólo a archivos).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Atributos extendidos de lectura</p></td>
<td style="border:1px solid black;"><p>Permite o rechaza las peticiones de usuarios para visualizar los atributos de un archivo o carpeta como, por ejemplo, los de sólo lectura y los ocultos. Los atributos vienen definidos por NTFS.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear archivos/Escribir datos</p></td>
<td style="border:1px solid black;"><p>Crear archivos permite o deniega la creación de archivos en la carpeta (se aplica sólo a carpetas). Escribir datos permite o deniega la posibilidad de realizar cambios en el archivo y sobrescribir el contenido existente (se aplica sólo a archivos).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Crear carpetas/Anexar datos</p></td>
<td style="border:1px solid black;"><p>Crear carpetas permite o deniega solicitudes de usuario para crear carpetas en una carpeta especificada (se aplica sólo a carpetas). Anexar datos permite o deniega la posibilidad de realizar cambios al final del archivo pero no de cambiar, eliminar o sobrescribir los datos existentes (se aplica sólo a archivos).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Atributos de escritura</p></td>
<td style="border:1px solid black;"><p>Permite o deniega solicitudes de usuario para realizar cambios al final del archivo, pero no cambiar, eliminar o sobrescribir los datos existentes (se aplica sólo a archivos).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Atributos extendidos de escritura</p></td>
<td style="border:1px solid black;"><p>Permite o rechaza las peticiones de usuarios para cambiar los atributos de un archivo o carpeta como, por ejemplo, de sólo lectura u ocultos. Los atributos vienen definidos por NTFS.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Eliminar subcarpetas y archivos</p></td>
<td style="border:1px solid black;"><p>Permite o deniega la capacidad de eliminar subcarpetas y archivos, incluso si no se ha asignado el permiso Eliminar en la subcarpeta o el archivo (se aplica a carpetas).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Eliminar</p></td>
<td style="border:1px solid black;"><p>Permite o deniega solicitudes de usuario para eliminar subcarpetas y archivos, incluso si no se ha asignado el permiso Eliminar para la subcarpeta o el archivo (se aplica a carpetas).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Leer permisos</p></td>
<td style="border:1px solid black;"><p>Se permiten o rechazan las peticiones de usuarios para leer los permisos de los archivos o carpetas, como por ejemplo los de control total, lectura y escritura.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cambiar permisos</p></td>
<td style="border:1px solid black;"><p>Se permiten o rechazan las peticiones de usuarios para cambiar los permisos de los archivos o carpetas, como por ejemplo los de control total, lectura y escritura.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tomar posesión</p></td>
<td style="border:1px solid black;"><p>Permite o deniega la toma de posesión del archivo o la carpeta. El propietario de un archivo o carpeta puede en cualquier momento cambiar los permisos para éstos, a pesar de que exista alguno que protege el archivo o carpeta.</p></td>
</tr>  
</tbody>  
</table>
  
Los tres términos adicionales siguientes se utilizan para describir la herencia de los permisos que se aplican a los archivos y las carpetas:
  
-   **Propagar** se refiere a la propagación de permisos heredables a todas las subcarpetas y archivos. Todos los objetos secundarios heredan la configuración de seguridad del objeto principal, siempre y cuando el objeto secundario no esté protegido contra la aceptación de la herencia de permisos. Si se produce un conflicto, los permisos explícitos del objeto secundario predominarán sobre los permisos que se heredan del objeto principal.
  
-   **Reemplazar** se refiere al reemplazo de permisos en todos los archivos y subcarpetas con permisos heredables. Las entradas del permiso del objeto principal predominarán sobre todas las configuraciones de seguridad que existan para el objeto secundario, independientemente de cuál sea la configuración de este último. El objeto secundario tendrá las mismas entradas de control de acceso que el objeto principal.
  
-   **Omitir** se refiere a no permitir permisos para sustituir un archivo o carpeta (o clave). Se puede utilizar esta opción de configuración si no se desea configurar o analizar la seguridad de este objeto ni de ninguno de sus objetos secundarios.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han descrito detalladamente los parámetros de seguridad principales y las configuraciones recomendadas de cada parámetro para proteger equipos que ejecutan Windows XP Professional con SP2 en los dos entornos que se tratan en este capítulo. Cuando considere las directivas de seguridad para su organización, recuerde el equilibrio entre seguridad y productividad del usuario. Aunque los usuarios necesitan protección frente a código y atacantes malintencionados, también necesitan realizar su trabajo sin directivas de seguridad excesivamente restrictivas que frustren sus esfuerzos.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.
  
-   Para obtener más información acerca de cómo mantener la seguridad para Windows XP Professional, consulte la herramienta de Ayuda y soporte técnico que se incluye con Windows XP y el sitio web de [Seguridad y privacidad de Microsoft Windows XP](http://www.microsoft.com/spain/windowsxp/using/security/default.mspx), en www.microsoft.com/windowsxp/security/.
  
-   Para obtener más información acerca de las características de seguridad de Windows XP SP2, consulte el documento de [información de seguridad para Windows XP Service Pack 2](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/xpsp2sec.mspx), en www.microsoft.com/technet/prodtechnol/winxppro/maintain/xpsp2sec.mspx.
  
-   Para obtener más información acerca de los parámetros de seguridad disponibles en Windows XP SP2, consulte el artículo de Microsoft TechNet sobre [descripciones de parámetros de seguridad](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/dd980ca3-f686-4ffc-a617-50c6240f5582.mspx), en www.microsoft.com/technet/prodtechnol  
    /windowsserver2003/library/ServerHelp/dd980ca3-f686-4ffc-a617-50c6240f5582.mspx.
  
-   Para obtener más información acerca de la seguridad para el sistema operativo Windows, consulte el [Kit de recursos de seguridad de Microsoft Windows](http://www.microsoft.com/mspress/books/authors/auth6418.aspx), en www.microsoft.com/MSPress/books/6418.asp.
  
-   Para obtener más información acerca de la característica Sistema de cifrado de archivos de Windows XP y Windows Server 2003, consulte "[Encrypting File System in Windows XP and Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/deploy/cryptfs.mspx)", en www.microsoft.com/technet/prodtechnol/winxppro/deploy/cryptfs.mspx.
  
##### Descargar
  
[![](images/Cc163074.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
  
[](#mainsection)[Principio de la página](#mainsection)
