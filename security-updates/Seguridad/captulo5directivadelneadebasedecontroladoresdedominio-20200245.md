---
TOCTitle: 'Capítulo 5: Directiva de línea de base de controladores de dominio'
Title: 'Capítulo 5: Directiva de línea de base de controladores de dominio'
ms:assetid: '4247b4ee-4805-4ac4-8962-9f73c91bb80f'
ms:contentKeyID: 20200245
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163123(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 5: Directiva de línea de base de controladores de dominio

Actualizado: 27/12/05

##### En esta página

[](#eiaa)[Información general](#eiaa)
[](#ehaa)[Configuración de directiva de auditoría](#ehaa)
[](#egaa)[Configuración de Asignación de derechos de usuario](#egaa)
[](#efaa)[Opciones de seguridad](#efaa)
[](#eeaa)[Configuración del registro de eventos](#eeaa)
[](#edaa)[Grupos restringidos](#edaa)
[](#ecaa)[Configuración de seguridad adicional](#ecaa)
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

La seguridad de la función de servidor de controladores de dominio es uno de los aspectos más importantes que se debe abordar para cualquier entorno con equipos que ejecuten Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1) y el servicio de directorio de Active Directory®. Cualquier problema en la seguridad de un controlador de dominio podría afectar enormemente a los equipos cliente, servidores y aplicaciones que dependan de controladores de dominio para la autenticación, de la directiva de grupo y de un directorio LDPA (Protocolo ligero de acceso a directorios) central.

Dada su importancia, los controladores de dominio siempre se deben almacenar en ubicaciones físicas seguras a las que sólo pueda tener acceso personal administrativo autorizado. En caso de que se deban almacenar en ubicaciones no seguras, como sucursales, se pueden ajustar varias configuraciones de seguridad para limitar el daño potencial de las amenazas físicas.

#### Directiva de línea de base de controladores de dominio

A diferencia de otras directivas de función de servidor que se han descrito anteriormente en esta guía, la directiva de grupo de la función de servidor de controladores de dominio es una directiva de línea de base como la directiva de línea de base de servidores miembro (MSBP) definida en el capítulo 4, "Directiva de línea de base de servidores miembro". La directiva de línea de base de controladores de dominio (DSBP) está vinculada a la unidad organizativa (UO) Controladores de dominio y tiene prioridad sobre la directiva predeterminada de controladores de dominio. La configuración de directiva incluida en la DCBP fortalecerá la seguridad general de todos los controladores de dominio de cualquier entorno.

La mayor parte de la DCBP se copia de la MSBP. Por lo tanto, debe revisar minuciosamente el capítulo 4, "Directiva de línea de base de servidores miembro", para comprender completamente las distintas configuraciones de directiva que se incluyen también en la DCBP. Este capítulo sólo incluye las configuraciones de la DCBP que difieren de las de la MSBP.

Las plantillas de controladores de dominio están diseñadas exclusivamente para tratar las necesidades de seguridad de los tres entornos definidos en esta guía. En la tabla siguiente se muestran los archivos .inf de controlador de dominio que se incluyen con esta guía para los entornos Cliente heredado (LC), Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF). Por ejemplo, el archivo EC-Domain Controller.inf es la plantilla de seguridad para el entorno Cliente de empresa.

**Tabla 5.1 Plantillas de seguridad de línea de base de controladores de dominio**

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
<td style="border:1px solid black;"><p>LC-Domain Controller.inf</p></td>
<td style="border:1px solid black;"><p>EC-Domain Controller.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Domain Controller.inf</p></td>
</tr>  
</tbody>  
</table>
  
**Nota**: las operaciones del dominio se podrían ver enormemente afectadas si un objeto de directiva de grupo (GPO) configurado de forma incorrecta se vincula a la UO Controladores de Dominio. Sea extremadamente precavido al importar estas plantillas de seguridad y compruebe que toda la configuración de directiva importada sea correcta antes de vincular un GPO a la UO Controladores de dominio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
La configuración de la directiva de auditoría para los controladores de dominio es casi la misma que la especificada en MSBP. Para obtener más información, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de directiva de MSBP garantiza que toda la información de auditoría de seguridad pertinente se registre en los controladores de dominio.
  
**Tabla 5.2 Configuración recomendada para la directiva de auditoría**

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
<td style="border:1px solid black;"><p>Auditar el acceso del servicio de directorio</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Sin auditoría</p></td>
<td style="border:1px solid black;"><p>Erróneo</p></td>
</tr>  
</tbody>  
</table>
  
#### Auditar el acceso del servicio de directorio
  
Esta configuración de directiva determina si se debe auditar el acceso de los usuarios a un objeto de Active Directory que tiene especificada una lista de control de acceso al sistema (SACL) propia. Si configura **Auditar el acceso del servicio de directorio**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un usuario obtiene acceso correctamente a un objeto de Active Directory que tiene una SACL especificada. Las auditorías de errores generan una entrada de auditoría cuando un usuario no consigue obtener acceso a un objeto de Active Directory que tiene una SACL especificada.
  
Si habilita **Auditar el acceso del servicio de directorio** en la DCBP y configura listas SACL en objetos del directorio, se puede generar un elevado número de entradas en los registros de seguridad de los controladores de dominio. Sólo debe habilitar esta configuración si realmente va a utilizar la información creada.
  
**Auditar el acceso del servicio de directorio** se configura en **Sin auditoría** en los entornos LC y EC, y para que se registren eventos de **error** en el entorno SSLF.
  
La tabla siguiente incluye eventos de seguridad importantes que la configuración **Auditar el acceso del servicio de directorio** inserta en el registro de seguridad.
  
**Tabla 5.3 Eventos de acceso del servicio de directorio**

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
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>Descripción</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>566</p></td>
<td style="border:1px solid black;"><p>Ha tenido lugar una operación genérica de objeto.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Asignación de derechos de usuario
  
La DCBP especifica una serie de asignaciones de derechos de usuario para los controladores de dominio. Además de la configuración predeterminada, se modificaron otras configuraciones de derechos de usuario para reforzar la seguridad de los controladores de dominio en los tres entornos definidos en esta guía.
  
En esta sección se proporcionan detalles sobre la configuración recomendada de derechos de usuario para la DCBP que difiere de la configuración de MSBP. Para obtener un resumen de la configuración recomendada en esta sección, consulte el libro de Microsoft Excel® "Windows Server 2003 Security Guide Settings" que se incluye con la versión descargable de esta guía.
  
La tabla siguiente resume la configuración recomendada de asignaciones de derechos de usuario para DCBP. En las secciones siguientes a esta tabla se proporciona información adicional sobre cada configuración.
  
**Tabla 5.4 Configuración recomendada de asignaciones de derechos de usuario**

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
<td style="border:1px solid black;"><p>Agregar estaciones de trabajo al dominio</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Permitir el inicio de sesión local</p></td>
<td style="border:1px solid black;"><p>Administradores, operadores de servidor, operadores de copia de seguridad</p></td>
<td style="border:1px solid black;"><p>Administradores, operadores de servidor, operadores de copia de seguridad</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Permitir inicio de sesión a través de Servicios de Terminal Server</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cambiar la hora del sistema</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cargar y descargar controladores de dispositivo</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Restaurar archivos y directorios</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Apagar el sistema</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
</tbody>  
</table>
  
#### Tener acceso a este equipo desde la red
  
Esta configuración de directiva determina los usuarios y grupos con autorización para conectarse al controlador de dominio a través de la red. Se necesita para varias operaciones de red, como la réplica de Active Directory entre controladores de dominio y las solicitudes de autenticación de usuarios y equipos en controladores de dominio, así como para el acceso a carpetas e impresoras compartidas.
  
Aunque los permisos asignados al grupo de seguridad **Todos** ya no otorgan acceso a usuarios anónimos en Windows Server 2003 con SP1, los grupos y las cuentas de invitados todavía pueden obtener acceso mediante el grupo de seguridad **Todos**.
  
Por este motivo, al grupo de seguridad **Todos** se le ha quitado el derecho de usuario **Tener acceso a este equipo desde la red** en la DCBP para el entorno SSLF. La eliminación de este grupo proporciona una medida de seguridad adicional frente a los ataques cuyo objetivo es tener acceso como invitado al dominio. Esta configuración de directiva se ha establecido como **No definida** para los entornos LC y EC.
  
#### Agregar estaciones de trabajo al dominio
  
Esta configuración de directiva especifica los usuarios que pueden agregar estaciones de trabajo a un dominio específico. Para que esta configuración de directiva tenga efecto, se debe asignar al usuario como parte de la directiva predeterminada de controladores de dominio del dominio específico. Un usuario al que se le asigna este derecho puede agregar hasta 10 estaciones de trabajo al dominio. Los usuarios a los que se le asigna el permiso **Crear objetos de equipo** para una UO o el contenedor Equipos en Active Directory también pueden agregar un número ilimitado de equipos al dominio, independientemente de si se les ha asignado o no el derecho de usuario **Agregar estaciones de trabajo al dominio**.
  
De forma predeterminada, todos los usuarios del grupo **Usuarios autenticados** pueden agregar hasta 10 cuentas de equipo a un dominio Active Directory. Estas nuevas cuentas de equipo se crean en el contenedor Equipos.
  
En las redes basadas en Windows, por el término *entidad principal de seguridad* se entiende un usuario, grupo o equipo al que se le asigna automáticamente un identificador de seguridad para controlar el acceso a los recursos. En un dominio Active Directory, cada cuenta de equipo es una entidad de seguridad principal con capacidad para autenticar y obtener acceso a los recursos. Sin embargo, es posible que algunas organizaciones deseen limitar el número de equipos de un entorno de Active Directory para poder realizar un seguimiento de los mismos, crearlos y administrarlos de forma coherente. Si los usuarios tienen permiso para agregar equipos al dominio, los esfuerzos de seguimiento y administración pueden verse dificultados. Además, los usuarios podrían realizar actividades cuyo seguimiento resulte más complicado, ya que pueden crear equipos de dominio adicionales no autorizados.
  
Por estos motivos, el derecho de usuario **Agregar estaciones de trabajo al dominio** sólo se debe asignar al grupo **Administradores** en la DCBP para el entorno SSLF. Esta configuración de directiva se ha establecido como **No definida** para los entornos LC y EC.
  
#### Permitir el inicio de sesión local
  
Esta configuración de directiva especifica los usuarios que pueden iniciar sesiones interactivas en el controlador de dominio. Los usuarios que no tengan este derecho aún pueden iniciar una sesión interactiva remota en el controlador de dominio si se les ha asignado el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server**.
  
Debe restringir el número de cuentas que pueden iniciar sesión en las consolas de controlador de dominio para evitar el acceso no autorizado a los sistemas de archivos y servicios del sistema de los controladores de dominio. Un usuario que pueda iniciar una sesión en la consola de un controlador de dominio podría aprovecharse malintencionadamente del equipo y poner probablemente en peligro la seguridad de todo el dominio o bosque.
  
De forma predeterminada, se asigna el derecho de usuario **Permitir el inicio de sesión local** a los grupos **Opers. de cuentas**, **Operadores de copia de seguridad**, **Opers. de impresión** y **Opers. de servidores** en los controladores de dominio. Los usuarios de estos grupos no deben necesitar iniciar sesión en un controlador de dominio para realizar las tareas de administración y deben poder efectuar sus tareas desde otras estaciones de trabajo. Sólo los usuarios del grupo **Administradores** deben realizar tareas de mantenimiento en los controladores de dominio.
  
Si asigna el derecho de usuario **Permitir el inicio de sesión local** sólo al grupo **Administradores**, el acceso físico e interactivo al controlador de dominio está limitado únicamente a los usuarios en los que se tiene mucha confianza, lo que aumenta la seguridad. Por este motivo, el derecho de usuario **Permitir el inicio de sesión local** sólo se asigna al grupo **Administradores** en la DCBP para el entorno SSLF. Esta configuración de directiva se establece para incluir los grupos **Opers. de servidores** y **Operadores de copia de seguridad** para los entornos LC y EC.
  
#### Permitir inicio de sesión a través de Servicios de Terminal Server
  
Esta configuración de directiva especifica los usuarios que pueden iniciar sesión en el controlador de dominio mediante una conexión a Escritorio remoto.
  
Debe restringir el número de cuentas que pueden iniciar sesión en las consolas de controlador de dominio a través de Servicios de Terminal Server para evitar el acceso no autorizado a los sistemas de archivos y servicios del sistema de los controladores de dominio. Un usuario que pueda iniciar una sesión en la consola de un controlador de dominio a través de los Servicios de Terminal Server puede aprovecharse del sistema y poner probablemente en peligro la seguridad de todo el dominio o bosque.
  
Si asigna el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** sólo al grupo **Administradores**, el acceso interactivo al controlador de dominio está limitado únicamente a los usuarios en los que se tiene mucha confianza, lo que aumenta la seguridad. Por esta razón, sólo se asigna el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** al grupo **Administradores** en la DCBP para los tres entornos definidos en esta guía. Aunque para iniciar una sesión en un controlador de dominio a través de los Servicios de Terminal Server es necesario disponer de forma predeterminada de acceso administrativo, la configuración de directiva ayuda a proteger la red de acciones malintencionadas o que pueden pasar inadvertidas y que podrían ponerla en peligro.
  
Como medida de seguridad adicional, la DCBP deniega a la cuenta predeterminada de administrador el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server**. Esta configuración evita que usuarios malintencionados intenten obtener acceso a un controlador de dominio mediante la cuenta Administrador predeterminada. Para obtener más detalles acerca de esta configuración de directiva, consulte el capítulo 4, "Directiva de línea de base de servidores miembro".
  
#### Cambiar la hora del sistema
  
Esta configuración de directiva especifica los usuarios que pueden ajustar la hora del reloj interno de un equipo. Sin embargo, no es necesaria para cambiar la zona horaria ni otras características de presentación de la hora del sistema.
  
Sincronizar la hora del sistema resulta esencial para el funcionamiento de Active Directory. Tanto una réplica adecuada de Active Directory como los procesos de generación de vales de autenticación que utiliza el protocolo de autenticación Kerberos dependen de la sincronización horaria de todo el entorno.
  
Un controlador de dominio cuyo reloj no esté sincronizado con la hora del sistema de otros controladores de dominio del entorno podría interferir en el funcionamiento de los servicios de dominio. Si solamente los administradores pueden modificar la hora del sistema, se reduce al mínimo la posibilidad de que la hora del sistema de un controlador de dominio sea inexacta.
  
De forma predeterminada, el grupo **Opers. de servidores** puede modificar la hora del sistema de los controladores de dominio. A causa de los problemas que podrían producirse si los miembros de este grupo modifican de forma incorrecta el reloj de un controlador de dominio, únicamente se asigna en la DCBP el derecho de usuario **Cambiar la hora del sistema** al grupo **Administradores** para los tres entornos definidos en esta guía.
  
Para obtener más información sobre el servicio de hora de Microsoft Windows®, consulte la página que contiene [información técnica de consulta sobre el servicio de hora de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/a0fcd250-e5f7-41b3-b0e8-240f8236e210.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/TechRef/  
a0fcd250-e5f7-41b3-b0e8-240f8236e210.mspx (en inglés).
  
#### Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo
  
Esta configuración de directiva especifica los usuarios que pueden cambiar la configuración **De confianza para la delegación** para un usuario u objeto de equipo en Active Directory. La delegación de autenticación es una capacidad que las aplicaciones cliente/servidor de varios niveles emplean y que permite que un servicio de cliente, como una aplicación, utilice las credenciales de un cliente para la autenticación en un servicio de servidor, como una base de datos. Para que esta autenticación sea posible, el cliente y el servidor deben ejecutarse con cuentas de confianza para delegación.
  
Un uso incorrecto de este derecho de usuario podría permitir que usuarios no autorizados suplantasen a otros usuarios de la red. Un atacante podría aprovechar este derecho de usuario para obtener acceso a recursos de red como si fuese otro usuario, lo que podría dificultar la determinación de lo que ha ocurrido tras un incidente de seguridad.
  
El derecho de usuario **Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo** sólo se asigna al grupo **Administradores** de los controladores de dominio del entorno SSLF. Esta configuración de directiva se ha establecido como **No definida** para los entornos LC y EC.
  
**Nota**: aunque la directiva predeterminada de controladores de dominio asigna este derecho de usuario al grupo **Administradores**, la DCBP implementa solamente este derecho en el entorno SSLF porque se basa originalmente en la MSBP. La MSBP asigna a este derecho un valor nulo.
  
#### Cargar y descargar controladores de dispositivo
  
Esta configuración de directiva especifica los usuarios que pueden cargar y descargar controladores de dispositivos y, si es necesario, cargar y descargar dispositivos Plug and Play.
  
Una administración descuidada de los controladores de dispositivos de los controladores de dominio aumenta las posibilidades de que errores o código malintencionado afecten de forma negativa al funcionamiento de los controladores de dominio. Si en la DCBP se restringen las cuentas que pueden cargar y descargar controladores de dispositivos a solamente los usuarios en los que más se confía, se reduce al mínimo el potencial de que los controladores de dispositivos se utilicen para poner en peligro los controladores de dominio.
  
De forma predeterminada, se asigna el derecho de usuario **Cargar y descargar controladores de dispositivo** al grupo **Opers. de impresión.** Como se ha indicado antes, no se recomienda crear recursos compartidos de impresoras en los controladores de dominio, lo que elimina la necesidad de que el grupo **Opers. de impresión** deba tener capacidad para cargar y descargar controladores de dispositivos. Por lo tanto, sólo se asigna el derecho de usuario **Cargar y descargar controladores de dispositivo** al grupo **Administradores** en la DCBP para los tres entornos definidos en esta guía.
  
#### Restaurar archivos y directorios
  
Esta configuración de directiva especifica los usuarios que pueden evadir los permisos de archivo y directorio durante un proceso de restauración. Se puede establecer cualquier entidad de seguridad válida principal como propietaria de un objeto.
  
Una cuenta con capacidad para restaurar archivos y directorios del sistema de archivos de un controlador de dominio puede modificar fácilmente los archivos ejecutables. Los usuarios malintencionados pueden explotar esta capacidad para inutilizar un controlador de dominio, además de para poner en peligro la seguridad de un dominio o de todo un bosque.
  
De forma predeterminada, el derecho de usuario **Restaurar archivos y directorios** se asigna a los grupos **Opers. de servidores** y **Operadores de copia de seguridad.** Si este derecho de usuario se quita de estos grupos y sólo se asigna al grupo **Administradores**, se reduce la probabilidad de que se ponga en peligro un controlador de dominio debido a modificaciones inadecuadas del sistema de archivos. Por lo tanto, sólo se asigna el derecho de usuario **Restaurar archivos y directorios** al grupo **Administradores** en la DCBP para los tres entornos definidos en esta guía.
  
#### Apagar el sistema
  
Esta configuración de directiva especifica los usuarios que pueden apagar el equipo local.
  
Cualquier usuario malintencionado con capacidad para apagar los controladores de dominio puede iniciar fácilmente un ataque por denegación de servicio (DoS) con un grave impacto sobre todo el dominio o bosque. Un atacante podría aprovechar este derecho de usuario para iniciar una elevación del ataque de privilegios en una cuenta de controlador de dominio cuando se reinicien los servicios. El éxito de un ataque de elevación de privilegios contra un controlador de dominio pone en peligro la seguridad de un dominio o de todo el bosque.
  
De forma predeterminada, el derecho de usuario **Apagar el sistema** se asigna a los grupos **Administradores**, **Opers. de servidores**, **Opers. de impresión** y **Operadores de copia de seguridad**. En entornos seguros, ninguno de estos grupos, salvo **Administradores**, requiere este derecho para realizar tareas de administración. Por esta razón, sólo se asigna el derecho de usuario **Apagar el sistema** al grupo **Administradores** en la DCBP para los tres entornos definidos en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
La mayor parte de la configuración de las opciones de seguridad para controladores de dominio es la misma que la especificada para la MSBP. Para obtener más información, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". Las diferencias entre la configuración de las directivas MSBP y DCBP se describen en las secciones siguientes.
  
#### Configuración del controlador de dominio
  
**Tabla 5.5 Opciones de seguridad: recomendaciones sobre la configuración de controladores de dominio**

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
<td style="border:1px solid black;"><p>permitir que los operadores de servidor programen tareas</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>requisitos de firma de servidor LDAP</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Requiere firma</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>rechazar cambios automatizados de contraseñas de cuentas</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
##### Controlador de dominio: permitir a los operadores de servidor programar tareas
  
Esta configuración de directiva determina si los miembros del grupo **Opers. de servidores** pueden enviar trabajos mediante la herramienta de programación AT.
  
La configuración **Controlador de dominio: permitir a los operadores de servidor programar tareas** está establecida como **Deshabilitado** en la DCBP para los tres entornos definidos en esta guía. La repercusión de esta configuración de directiva es pequeña para la mayoría de las organizaciones. Los usuarios, incluidos los del grupo **Opers. de servidores**, podrán crear trabajos con el Asistente del programador de tareas, pero esos trabajos se ejecutarán en el contexto de la cuenta con la que se autentica el usuario al configurar el trabajo.
  
**Nota**: la cuenta de servicios AT se puede modificar para seleccionar otra cuenta que no sea la cuenta del SISTEMA LOCAL. Para cambiar la cuenta, abra Herramientas del sistema y haga clic en **Tareas programadas** y, a continuación, en la carpeta **Accesorios**. A continuación, seleccione **Cuenta de servicios AT** en el menú **Opciones avanzadas**.
  
##### Controlador de dominio: requisitos de firma de servidor LDAP
  
Esta configuración de directiva determina si el servidor LDAP requiere una firma antes de negociar con los clientes LDAP. El tráfico de red no firmado ni cifrado es susceptible de sufrir ataques con intervención humana en los que un intruso captura paquetes entre el servidor y el cliente y los modifica antes de reenviarlos al cliente. En el caso de un servidor LDAP, un atacante podría hacer que un cliente tomara decisiones en función de registros falsos del directorio LDAP.
  
Si todos los controladores de dominio ejecutan Windows 2000 o Windows Server 2003, configure la opción **Controlador de dominio: requisitos de firma de servidor LDAP** como **Requiere firma.** En caso contrario, deje esta configuración de directiva como **No está definido**, que es la configuración de la directiva DCBP para los entornos LC y EC. Esta configuración de directiva se establece como **Requiere firma** en la DCBP para el entorno SSLF, porque todos los equipos de este entorno ejecutan Windows 2000 o Windows Server 2003.
  
##### Controlador de dominio: no permitir los cambios de contraseña de cuenta de equipo
  
Esta configuración de directiva determina si los controladores de dominio rechazarán las solicitudes de los equipos miembro de cambiar las contraseñas de las cuentas de equipos. Si se habilita esta configuración de directiva en todos los controladores de dominio de un dominio, las contraseñas de las cuentas de los equipos de los miembros del dominio no podrán cambiarse y serán más susceptibles a los ataques.
  
La configuración **Controlador de dominio: no permitir los cambios de contraseña de cuenta de equipo** está establecida como **Deshabilitado** en la DCBP para los tres entornos definidos en esta guía.
  
#### Configuración de seguridad de red
  
**Tabla 5.6 Opciones de seguridad: recomendaciones sobre la configuración de seguridad de red**

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
</tbody>  
</table>
  
#### Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña
  
Esta configuración de directiva determina si el valor de hash de LAN Manager (LM) para la contraseña nueva se almacena al cambiar la contraseña. El hash de LM es relativamente débil y propenso a ataques en comparación con el hash de Windows NT®, más seguro desde el punto de vista criptográfico.
  
Por este motivo, la DCBP habilita la configuración **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** en los tres entornos definidos en esta guía.
  
**Nota**: puede que los sistemas operativos antiguos y algunas aplicaciones de terceros no permitan habilitar esta configuración de directiva. Por ejemplo, se producirán errores en Windows 95 y Windows 98 si no está instalada la extensión de cliente de Active Directory. Asimismo, será necesario cambiar la contraseña de todas las cuentas si se habilita esta configuración de directiva.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
La configuración del registro de eventos para controladores de dominio es la misma que la especificada en la MSBP. Para obtener más información, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de línea de base de DCBP garantiza que toda la información de auditoría de seguridad pertinente se registre en los controladores de dominio, incluido el acceso del servicio de directorio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Grupos restringidos
  
Como se ha descrito en el capítulo anterior, la configuración **Grupos restringidos** le permite administrar la pertenencia a los grupos de Windows Server 2003 con SP1 mediante la directiva de grupo de Active Directory. En primer lugar, analice las necesidades de su organización para determinar los grupos que desea restringir. Para los controladores de dominio, los grupos **Opers. de servidores** y **Operadores de copia de seguridad** se han restringido en los tres entornos definidos en esta guía. Aunque los miembros de los grupos **Opers. de servidores** y **Operadores de copia de seguridad** tengan menos derechos de acceso que los miembros del grupo **Administradores**, siguen contando con eficaces capacidades.
  
**Nota:** si su organización utiliza cualquiera de estos grupos, controle con cuidado su asociación y no implemente la guía para la configuración de **Grupos restringidos**. Si su organización agrega usuarios al grupo de usuarios de servidores, es probable que desee implementar los permisos opcionales del sistema de archivos que se describen en la sección “Seguridad del sistema de archivos” del capítulo anterior.
  
**Tabla 5.7 Recomendaciones sobre los grupos restringidos**

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
<th><p>Grupo local</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Operadores de copia de seguridad</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Operadores de servidores</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
<td style="border:1px solid black;"><p>Ningún miembro</p></td>
</tr>  
</tbody>  
</table>
  
La configuración **Grupos restringidos** se puede establecer en Windows Server 2003 con SP1 en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Grupos restringidos**
  
Para configurar grupos restringidos para un GPO, los administradores pueden agregar el grupo que deseen directamente al nodo **Grupos restringidos** del espacio de nombres de GPO.
  
Cuando un grupo está restringido, se pueden definir sus miembros así como otros grupos a los que pertenezca. Si no especifica estos miembros de grupo, el grupo estará totalmente restringido. Los grupos se pueden restringir únicamente mediante plantillas de seguridad.
  
**Para visualizar o modificar el parámetro Grupos restringidos**
  
1.  Abra Plantillas de seguridad de Microsoft Management Console (MMC).
  
    **Nota**: Plantillas de seguridad de Microsoft Management Console (MMC) no se incluye de forma predeterminada en el menú Herramientas administrativas. Para agregarlo, inicie Microsoft Management Console (mmc.exe) y agregue el complemento Plantillas de seguridad.
  
2.  Haga doble clic en el directorio del archivo de configuración y, a continuación, en el archivo.
  
3.  Haga doble clic en el elemento **Grupos restringidos**.
  
4.  Haga clic con el botón secundario del mouse en **Grupos restringidos**.
  
5.  Seleccione **Agregar grupo**.
  
6.  Haga clic en el botón **Examinar** y, a continuación en **Ubicaciones**; después, seleccione las ubicaciones que desea examinar y luego haga clic en **Aceptar**.
  
    **Nota**: normalmente, esta acción hará que un equipo local se muestre al principio de la lista.
  
7.  Escriba el nombre del grupo en el cuadro de texto **Escriba los nombres de objeto que desea seleccionar** y haga clic en el botón **Comprobar nombres**.
  
    - O bien -
  
    Haga clic en el botón **Avanzadas** y, a continuación, en el botón **Buscar ahora** para mostrar una lista de todos los grupos disponibles.
  
8.  Seleccione los grupos que desea restringir y, a continuación, haga clic en **Aceptar**.
  
9.  Haga clic en **Aceptar** en el cuadro de diálogo **Agregar grupos** para cerrarlo.
  
En esta guía, todos los miembros, tanto usuarios como grupos, de los grupos **Opers. de servidores** y **Operadores de copia de seguridad** se quitaron para que estuviesen totalmente restringidos en ambos entornos. Además, para el entorno SSLF, se quitaron todos los miembros del grupo **Usuarios de escritorio remoto**. Microsoft recomienda restringir todos los grupos integrados que no se prevea utilizar en la organización.
  
**Nota**: la configuración de Grupos Restringidos descrita en esta sección es muy sencilla. Las versiones de Windows XP con SP1 y SP2, así como Windows Server 2003, son compatibles con diseños más complejos. Para obtener más información, consulte el artículo de Microsoft Knowledge Base sobre [actualizaciones del comportamiento de Grupos restringidos ("miembro de") de los grupos locales definidos por el usuario](http://support.microsoft.com/default.aspx?kbid=810076) en http://support.microsoft.com/default.aspx?kbid=810076 (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
En esta sección se describen modificaciones que se deben realizar manualmente en la DCBP, así como configuraciones adicionales y contramedidas que no se pueden implementar a través de la directiva de grupo.
  
#### Adición manual de grupos de seguridad únicos a las asignaciones de derechos de usuario
  
La mayor parte de las asignaciones de derechos de usuario aplicadas a través de la directiva DCBP están correctamente especificadas en las plantillas de seguridad que acompañan a esta guía. Sin embargo, existen algunas cuentas y grupos de seguridad que no se pueden incluir en las plantillas debido a que sus identificadores de seguridad (SID) son específicos de dominios individuales de Windows Server 2003. Las tareas de derechos de usuario que se deben configurar se especifican manualmente en la tabla siguiente.
  
**Advertencia**: en la siguiente tabla se incluyen valores para la cuenta integrada Administrador. No hay que confundir esta cuenta con el grupo de seguridad **Administradores** integrado. Si se agrega el grupo de seguridad **Administradores** a cualquiera de los siguientes derechos de usuario de denegación de acceso, deberá iniciar la sesión localmente para corregir el error.
  
Además, si ha cambiado el nombre de la cuenta integrada del administrador según lo recomendado en el capítulo 4, "Directiva de línea de base de servidores miembro", asegúrese de seleccionar la cuenta de administrador que acaba de cambiar al agregar la cuenta a cualquier derecho de usuario de denegación de acceso.
  
**Tabla 5.8 Asignaciones de derechos de usuario agregadas manualmente**

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
<td style="border:1px solid black;"><p>Administrador integrado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
</tr>  
</tbody>  
</table>
  
**Importante**: “Todas las cuentas de servicio del sistema que NO sean del sistema operativo” incluye cuentas de servicio que se utilizan para aplicaciones específicas en una empresa, pero NO incluye las cuentas de SISTEMA LOCAL, SERVICIO LOCAL ni de SERVICIO DE RED (las cuentas incorporadas que el sistema operativo utiliza).
  
#### Servicios de directorio
  
Los controladores de dominio que ejecutan Windows Server 2003 con SP1 almacenan los datos del directorio y administran las interacciones entre el usuario y el dominio, incluidos los procesos de inicio de sesión del usuario, la autenticación y las búsquedas del directorio.
  
##### Reubicación de datos: archivos de registro y base de datos de Active Directory
  
Para mantener la integridad y confiabilidad del directorio, es esencial proteger la base de datos de Active Directory y sus archivos de registro.
  
Puede mover los archivos Ntds.dit, Edb.log y Temp.edb de su ubicación predeterminada, lo que ayudará a ocultarlos de un atacante si un controlador de dominio se encuentra en peligro. Si mueve los archivos a otro disco físico fuera del volumen del sistema actual, obtendrá la ventaja adicional de contar con un rendimiento mejorado del controlador de dominio.
  
Por estos motivos, en esta guía se recomienda mover los archivos de base de datos y de registro de Active Directory de los controladores de dominio a un volumen de disco seccionado o seccionado/reflejado que no contenga el sistema operativo. Estos archivos se deben mover para los tres entornos definidos en esta guía.
  
##### Cambio de tamaño de los archivos de registro de Active Directory
  
Es necesario que se registre una cantidad adecuada de información para poder supervisar y mantener de forma eficaz la integridad, confiabilidad y disponibilidad de Active Directory. Se necesita información de todos los controladores de dominio en el entorno.
  
Puede aumentar el tamaño máximo de los archivos de registro para admitir este esfuerzo. Si existe más información del registro, los administradores podrán realizar las auditorías relevantes en caso de ataques de intrusos.
  
En esta guía se recomienda aumentar el tamaño máximo de los archivos de registro del Servicio de directorio y del Servicio de replicación de archivos de los 512 KB predeterminados a 16 MB en los controladores de dominio de los tres entornos aquí definidos.
  
##### Uso de Syskey
  
En los controladores de dominio, la información de contraseña se almacena en Active Directory. No es extraño que el software de averiguación de contraseñas tenga como principal objetivo la base de datos del Administrador de cuentas de seguridad (SAM) o los servicios de directorio para obtener acceso a las contraseñas de las cuentas de los usuarios.
  
La utilidad System Key (Syskey) proporciona una línea de defensa adicional frente al software de averiguación de contraseñas sin conexión. Syskey utiliza técnicas de cifrado de alta seguridad para garantizar la seguridad de la información de contraseñas de cuentas almacenada en SAM en el controlador de dominio.
  
**Tabla 5.9 Modos de Syskey**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Opción Clave del sistema</p></th>  
<th><p>Nivel de seguridad</p></th>  
<th><p>Descripción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Modo 1: Contraseña generada por el sistema y almacenamiento de la clave de inicio localmente</p></td>
<td style="border:1px solid black;"><p>Seguro</p></td>
<td style="border:1px solid black;"><p>Utiliza una clave aleatoria generada por el equipo como clave del sistema y almacena una versión cifrada de la misma en el equipo local. Esta opción proporciona un cifrado de alta seguridad de la información sobre las contraseñas en el Registro y permite al usuario reiniciar el equipo sin necesidad de que un administrador escriba la contraseña o inserte un disco.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Modo 2: Contraseña generada por el administrador e inicio con contraseña</p></td>
<td style="border:1px solid black;"><p>Más seguro</p></td>
<td style="border:1px solid black;"><p>Utiliza una clave aleatoria generada por el equipo como clave del sistema y almacena una versión cifrada de la misma en el equipo local. La clave también está protegida por una contraseña elegida por el administrador. Cuando el equipo se encuentra en la secuencia de inicio se solicita a los usuarios la contraseña para la clave del sistema. Esta contraseña no está almacenada en ningún otro sector del equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Modo 3: Contraseña generada por el sistema y almacenamiento de la clave de inicio en un disco</p></td>
<td style="border:1px solid black;"><p>Absolutamente seguro</p></td>
<td style="border:1px solid black;"><p>Utiliza una clave aleatoria generada por el equipo y almacena la clave en un disco. El disco que contiene la clave del sistema es necesario para el inicio del equipo y debe insertarse cuando se solicite durante la secuencia de inicio. La clave del sistema no está almacenada en ningún otro sector del equipo.</p></td>
</tr>  
</tbody>  
</table>
  
Syskey se encuentra habilitado en todos los servidores que ejecutan Windows Server 2003 con SP1 en el Modo 1 (clave ofuscada). Desde un punto de vista de la seguridad, esta configuración parece sensata en un primer momento. Sin embargo, Syskey en el Modo 1 permite a un atacante leer y alterar el contenido del directorio, lo que convertiría al controlador de dominio en fácilmente vulnerable ante un atacante que tenga acceso físico.
  
Existen muchas razones para recomendar el uso de Syskey en Modo 2 (contraseña de la consola) o en Modo 3 (almacenamiento de la contraseña de Syskey en un disco) para cualquier controlador de dominio expuesto a amenazas contra su seguridad física. Sin embargo, la necesidad operativa de reiniciar los controladores de dominio suele complicar el uso de Syskey en Modo 2 ó 3. Para aprovechar la protección adicional que proporcionan estos modos de Syskey, se deben implementar los procesos operativos adecuados en el entorno para cumplir con los requisitos de disponibilidad específicos de los controladores de dominio.
  
La logística de la administración de las contraseñas o los discos de Syskey puede resultar bastante compleja, especialmente en las sucursales. Por ejemplo, puede resultar muy caro exigir al director de una sucursal o al personal administrativo local que vaya a la oficina a las 3 a.m. para escribir las contraseñas o insertar un disco para habilitar el acceso de los usuarios. Este tipo de requisitos caros pueden hacer que conseguir contratos de nivel de servicio (SLA) de gran disponibilidad sea un reto muy importante.
  
Como alternativa, si decide permitir que el personal de operaciones de TI centralizado proporcione contraseñas Syskey de forma remota, necesitará disponer de hardware adicional. Algunos proveedores de hardware tienen soluciones en forma de complementos que permiten tener acceso remoto a las consolas de servidor.
  
Por último, la pérdida de la contraseña o del disco Syskey imposibilita el reinicio del controlador de dominio. No existe ningún método de recuperación de un controlador de dominio en caso de pérdida de la contraseña o el disco Syskey. Si esto sucede, el controlador de dominio debe ser reconstruido.
  
Con los procedimientos operativos adecuados, Syskey puede proporcionar un alto nivel de seguridad para proteger la importante información de directorio de los controladores de dominio. Por estas razones, se recomienda Syskey en Modo 2 ó 3 para los controladores de dominio en ubicaciones carentes de fuertes medidas de seguridad de almacenamiento físico. Esta configuración se aplica a los controladores de dominio de los tres entornos descritos en esta guía.
  
**Para crear o actualizar una clave de sistema**
  
1.  Haga clic en **Inicio**, seleccione **Ejecutar**, escriba **syskey** y, a continuación, haga clic en **Aceptar**.
  
2.  Haga clic en **Cifrado habilitado** y, a continuación, haga clic en **Actualizar**.
  
3.  Haga clic en la opción que desea y, a continuación, haga clic en **Aceptar**.
  
#### Active Directory integrado con DNS
  
Microsoft recomienda el uso de Active Directory integrado con DNS en los tres entornos definidos en esta guía. Parte del motivo para hacer esta recomendación se basa en que la integración de la zona de Active Directory hace que sea más sencillo garantizar la seguridad de la infraestructura DNS en un entorno que utiliza Active Directory integrado con DNS que en un entorno que no lo utiliza.
  
##### Protección de los servidores DNS
  
Es esencial proteger los servidores DNS de cualquier entorno con Active Directory. Las siguientes secciones proporcionan recomendaciones y explicaciones acerca de cómo proteger los servidores DNS.
  
Cuando un servidor DNS sufre un ataque, un posible objetivo del atacante es controlar la información DNS devuelta como respuesta a las consultas del cliente DNS. Si un atacante controla esta información, los clientes pueden ser redirigidos sin saberlo a equipos no autorizados. La suplantación de IP y la infección de caché son ejemplos de este tipo de ataque.
  
En el caso de la suplantación de IP, una transmisión recibe la dirección IP de un usuario autorizado para obtener acceso a un equipo o a una red. La infección de caché es un ataque en el que un host no autorizado transmite información falsa sobre otro host a la caché de un servidor DNS. El ataque provoca un redireccionamiento de los clientes a equipos no autorizados.
  
Si se permite que los equipos cliente se comuniquen con equipos no autorizados, estos últimos pueden intentar obtener acceso a la información de los equipos cliente.
  
No todos los ataques tienen como objetivo la suplantación de los servidores DNS. Algunos ataques por servicio denegado pueden alterar los registros DNS en servidores DNS legítimos para proporcionar direcciones no válidas en respuesta a las consultas de los clientes. Si un servidor DNS responde con direcciones no válidas, ni los clientes ni los servidores podrán localizar los recursos que necesitan, tales como controladores de dominio, servidores web o recursos compartidos de archivos.
  
Por estas razones, los enrutadores utilizados en los tres entornos definidos en esta guía están configurados de modo que se eliminen los paquetes IP suplantados, lo que garantiza que otros equipos no puedan suplantar las direcciones IP de los servidores DNS.
  
##### Configuración de las actualizaciones dinámicas seguras
  
El servicio de **cliente DNS** de Windows Server 2003 con SP1 es compatible con las actualizaciones DNS dinámicas, lo que permite a los equipos cliente agregar registros DNS directamente a la base de datos. Si un servidor DNS dinámico está configurado para aceptar actualizaciones no seguras, un atacante podría transmitir actualizaciones malintencionadas o no autorizadas de un equipo cliente compatible con el protocolo de actualizaciones dinámicas DNS.
  
Un atacante podría, como mínimo, agregar entradas falsas a la base de datos DNS y, en el peor de los casos, sobrescribir o delegar entradas legítimas de la base de datos DNS. Dicho atacante podría realizar alguna de las siguientes acciones:
  
-   **Direccionamiento de los clientes a controladores de dominio no autorizados:** cuando un cliente envía una consulta DNS para buscar la dirección de un controlador de dominio, un servidor DNS comprometido puede recibir instrucciones para devolver la dirección de un servidor no autorizado. A continuación, mediante otros ataques no relacionados con DNS, se puede engañar al cliente y convencerle para que transmita información segura al servidor no autorizado.
  
-   **Respuesta a consultas DNS con direcciones no válidas:** los clientes y los servidores no podrán localizarse mutuamente. Si los clientes no pueden localizar los servidores, no podrán obtener acceso al directorio. Cuando los controladores de dominio no encuentran a otros controladores de dominio, se detiene la réplica del directorio, lo que crea una condición DoS que puede afectar a los usuarios de todo un bosque.
  
-   **Creación de una condición DoS:** el espacio en disco de un servidor puede agotarse debido a un archivo de zona lleno de registros ficticios o a una gran cantidad de entradas que disminuyen la velocidad de la réplica.
  
El uso de actualizaciones DNS dinámicas seguras garantiza que las solicitudes de registro sólo se procesen si éstas se envían desde clientes válidos de un bosque de Active Directory. Este método limita en gran medida la posibilidad de que un atacante comprometa la integridad de un servidor DNS.
  
Por estas razones, los servidores DNS de Active Directory de los tres entornos definidos en esta guía están configurados para aceptar únicamente actualizaciones dinámicas seguras.
  
##### Limitación de las transferencias de zona a sistemas autorizados
  
Debido a la importante función que desempeñan las zonas en DNS, éstas deben estar disponibles en más de un servidor DNS de la red para proporcionar niveles adecuados de disponibilidad y tolerancia a errores en las consultas de resolución de nombres. Cuando una zona se aloja en servidores adicionales, es necesario que las transferencias de zona repliquen y sincronicen todas las copias de la zona en todos los servidores configurados como host de la zona.
  
Además, un servidor DNS sin limitaciones que pueda realizar solicitudes de transferencia de zona puede transferir toda la zona DNS a cualquiera que la solicite. Esta transferencia se puede realizar fácilmente con herramientas como Nslookup.exe. Estas herramientas pueden exponer todo el conjunto de datos DNS del dominio, incluidos los host que actúan como controladores de dominio, los servidores web integrados en el directorio o las bases de datos de Microsoft SQL Server™.
  
Por estas razones, los servidores DNS integrados en Active Directory en los tres entornos aquí definidos están configurados para permitir las transferencias de zonas, pero con una limitación respecto a los equipos que pueden realizar solicitudes de transferencias.
  
##### Cambio de tamaño del registro de eventos y del registro del servicio DNS
  
Es necesario que se registre una cantidad adecuada de información para poder supervisar y mantener de forma eficaz el servicio DNS. Se necesita información de todos los controladores de dominio en el entorno.
  
Puede aumentar el tamaño máximo del archivo de registro del servicio DNS, lo que permitirá a los administradores realizar las auditorías relevantes ante un ataque.
  
En esta guía se recomienda aumentar el tamaño máximo del archivo de registro del servicio DNS a como mínimo 16 MB en los controladores de dominio de los tres entornos aquí definidos. Además, asegúrese de que está seleccionada la opción **Sobrescribir eventos cuando sea necesario** del servicio DNS para aumentar la cantidad de entradas de registro que se conservan.
  
#### Seguridad de las cuentas conocidas
  
Windows Server 2003 con SP 1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.
  
El valor de este cambio de configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.
  
Realice los pasos siguientes para proteger las cuentas conocidas en los servidores y dominios:
  
-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.
  
-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás con el mismo nombre de cuenta y contraseña.
  
-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.
  
-   Registre cualquier cambio que haga en una ubicación segura.
  
    **Nota**: se puede cambiar el nombre de la cuenta integrada Administrador desde la directiva de grupo. Esta configuración de directiva no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque cada organización debe escoger un nombre único para esta cuenta. Sin embargo, puede configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de las cuentas de administrador en los tres entornos que se definen en esta guía. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.
  
#### Seguridad de las cuentas de servicios
  
A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.
  
#### Configuraciones de los Servicios de Terminal Server
  
**Tabla 5.10 Configuración recomendada para los Servicios de Terminal Server**

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
<th><p>Predeterminado</p></th>  
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
  
La configuración **Establecer nivel de cifrado de conexión de cliente** determina el nivel de cifrado para las conexiones de clientes de los Servicios de Terminal Server en el entorno. La opción **Nivel alto** que utiliza cifrado de 128 bits impide que los atacantes intercepten las sesiones de los Servicios de Terminal Server con un analizador de paquetes. Algunas versiones más antiguas del cliente de Servicios de Terminal Server no son compatibles con este nivel de cifrado alto. Si su red dispone de dichos clientes, configure el nivel de cifrado de la conexión para que envíe y reciba datos en el nivel de cifrado más alto permitido por el cliente.
  
**Establecer el nivel de cifrado de conexión de cliente** está configurada como **Habilitado**, y la opción de cifrado de **Nivel alto** está seleccionada en la DCBP en los tres entornos de seguridad definidos en esta guía.
  
Puede configurar esta configuración de directiva en Windows Server 2003 en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Terminal Server\\Cifrado y seguridad.**
  
Los tres niveles disponibles de cifrado se describen en la tabla siguiente:
  
**Tabla 5.11 Niveles de cifrado de Servicios de Terminal Server**

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
<td style="border:1px solid black;"><p>Cifra los datos que se envían desde el cliente al servidor y desde el servidor al cliente con cifrado de 128 bits. Utilice siempre este nivel cuando Terminal Server se ejecute en un entorno que sólo incluya clientes de 128 bits, como los clientes de Conexión a Escritorio remoto. Los clientes que no admitan este nivel de cifrado no se podrán conectar.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cliente compatible</p></td>
<td style="border:1px solid black;"><p>Cifra los datos enviados entre el cliente y el servidor con la fuerza máxima de la clave admitida por el cliente. Emplee este nivel cuando Terminal Server se ejecute en un entorno que incluya clientes mixtos o heredados.</p></td>
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

**Tabla 5.12 Configuración recomendada para los informes de errores**

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
  
La configuración **Desactivar Informe** **de errores de Windows** controla si el servicio **Informe de errores** transmite datos.
  
Puede configurar esta configuración de directiva en Windows Server 2003 en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet**
  
Establezca el parámetro **Desactivar Informe** **de errores de Windows** como **Habilitado** en la DCBP para los tres entornos que se definen en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de la directiva utilizando SCW
  
Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía con el fin de crear una directiva de línea de base de controladores de dominio.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración de directiva para el entorno escogido. Este enfoque es necesario para garantizar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, instale el sistema operativo en un hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
**Para crear la directiva de línea de base de controladores de dominio**
  
Debe usar un equipo configurado como controlador de dominio para crear la directiva de línea de base de controladores de dominio. Puede utilizar un controlador de dominio existente o crear un equipo de referencia y utilizar la herramienta Dcpromo para crear un controlador de dominio para el equipo. Sin embargo, la mayoría de las organizaciones no quieren agregar un controlador de dominio a su entorno de producción porque puede violar su directiva de seguridad. Si utiliza un controlador de dominio existente, asegúrese de que no aplica ningún parámetro con SCW ni modifica su configuración.
  
1.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
2.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
3.  Compruebe que las funciones de servidor detectadas son adecuadas para su entorno. No quite la función de servidor de archivos, ya que es necesaria para que los controladores de dominio funcionen correctamente.
  
4.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
5.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
    **Nota**: si el entorno contiene controladores de dominio en múltiples sitios, asegúrese de que está seleccionada la opción **Replicación de Active Directory basada en correo**.
  
6.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
7.  Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
8.  Compruebe que la casilla de verificación **Omitir esta sección** está desactivada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.
  
    **Nota**: asegúrese de que la opción **Puertos para aplicaciones RPC del sistema** está seleccionada.
  
9.  En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
10. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
11. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-Domain Controller.inf).
  
12. Guarde la directiva con un nombre apropiado (por ejemplo, Domain Controller.xml**)**.
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método nativo de implementación ofrece la ventaja de poder deshacer fácilmente las directivas implementadas desde SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.
  
La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.
  
Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.
  
Para obtener más información acerca de cómo probar las directivas del SCW, consulte la [Guía de implementación para el Asistente para la configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx* *y la [documentación del Asistente para la configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.
  
#### Conversión e implementación de la directiva
  
Después de probar completamente la directiva, complete los pasos siguientes para convertirla en un GPO e implementarla:
  
1.  En el símbolo de sistema, escriba el siguiente comando:
  
    ```  
scwcmd transform /p:&lt;PathToPolicy.xml&gt; /g:&lt;GPODisplayName&gt;  
```
  
    y, a continuación, pulse Entrar. Por ejemplo:
  
    ```  
scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Domain Controller.xml" /g:"Domain Controller Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular el objeto GPO creado recientemente a la UO Controladores de dominio y asegúrese de moverlo a un nivel superior del de la directiva predeterminada de controladores de dominio para que tenga la máxima prioridad.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Recuerde que el GPO creado recientemente puede tardar algún tiempo en replicarse a todos los controladores de dominio, especialmente en entornos con controladores de dominio en múltiples sitios. Una vez comprobado que el GPO se ha replicado correctamente, debe realizar una última prueba para asegurarse de que el GPO aplica la configuración de directiva deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se ha explicado cómo reforzar la seguridad de los servidores de controladores de dominio que ejecutan Windows Server 2003 con SP1 en los tres entornos definidos en esta guía. La mayor parte de los parámetros de configuración de directiva descritos se configuraron y aplicaron mediante la directiva de grupo. La directiva de línea de base de controladores de dominio (DCBP) que complementa a la directiva predeterminada de controladores de dominio se vinculó a la UO Controladores de dominio.
  
La configuración de la directiva DCBP mejorará la seguridad general de los controladores de dominio de cualquier entorno. El uso de dos objetos GPO para garantizar la seguridad de los controladores de dominio permite conservar el entorno predeterminado y simplifica la solución de problemas.
  
Varias de las configuraciones descritas no se pueden aplicar a través de la directiva de grupo. Para esta configuración, se proporcionan detalles sobre la configuración manual.
  
Una vez configurada la seguridad de los controladores de dominio, se pueden hacer más seguras otras funciones de servidor. Los capítulos siguientes de esta guía se centran en cómo garantizar la seguridad de otras funciones específicas de servidor.
  
#### Información adicional
  
Los vínculos siguientes proporcionan información adicional acerca de temas relacionados con reforzar la seguridad de los controladores de dominio en los que se ejecuta Windows Server 2003 con SP1.
  
-   Para obtener información sobre guías recomendadas de arquitectura de sistemas Microsoft y Enterprise Data Center, consulte la página que contiene la [guía sobre la arquitectura recomendada de MSA EDC](http://www.microsoft.com/resources/documentation/msa/edc/all/solution/en-us/pak/pag/default.mspx) en www.microsoft.com/resources/documentation/msa/edc/all/solution/  
    en-us/pak/pag/default.mspx (en inglés).
  
-   Para obtener información sobre cómo habilitar el acceso anónimo a Active Directory, consulte el artículo de Microsoft Knowledge Base que contiene una [descripción de las opciones de permiso de Dcpromo](http://support.microsoft.com/?kbid=257988) en http://support.microsoft.com/?kbid=257988 (en inglés).
  
-   Para obtener información sobre DNS en Windows 2000 DNS, consulte el documento "[Windows 2000 DNS White Paper](http://www.microsoft.com/windows2000/techinfo/howitworks/communications/nameadrmgmt/w2kdns.asp)" en www.microsoft.com/windows2000/techinfo/howitworks/communications/  
    nameadrmgmt/w2kdns.asp (en inglés).
  
-   Para obtener información sobre DNS en Windows 2000, consulte el capítulo 6 de la versión en línea de la guía "[TCP/IP Core Networking Guide](http://www.microsoft.com/windows2000/techinfo/reskit/en-us/default.asp)" del kit de recursos de Windows 2000 en www.microsoft.com/windows2000/techinfo/reskit/en-us/default.asp (en inglés).
  
-   Para obtener información acerca de DNS en Windows 2003, consulte la página que contiene información sobre los [cambios en DNS en Windows Server 2003](http://www.microsoft.com/windows2000/technologies/communications/dns/dns2003.asp) en www.microsoft.com/windows2000/technologies/communications/dns/dns2003.asp (en inglés).
  
-   Para obtener más información acerca de la restricción de Active Directory, consulte el artículo de Microsoft Knowledge Base sobre la [restricción del tráfico de replicación de Active Directory en un puerto específico](http://support.microsoft.com/?kbid=224196) en http://support.microsoft.com/?kbid=224196 (en inglés).
  
-   Para obtener más información acerca de la restricción del tráfico de replicación de FRS, consulte el artículo de Microsoft Knowledge Base sobre [cómo restringir el tráfico de replicación de FRS en un puerto estático específico](http://support.microsoft.com/?kbid=319553) en http://support.microsoft.com/?kbid=319553.
  
-   Para obtener más información acerca del servicio de hora de Windows, consulte la página de [referencia técnica del servicio de hora de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/a0fcd250-e5f7-41b3-b0e8-240f8236e210.mspx) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    library/TechRef/a0fcd250-e5f7-41b3-b0e8-240f8236e210.mspx (en inglés).
  
-   Para obtener más información acerca de la imitación de IP, consulte el artículo que contiene una [introducción a la imitación IP](http://www.giac.org/practical/gsec/victor_velasco_gsec.pdf) en www.giac.org/practical/gsec/Victor\_Velasco\_GSEC.pdf (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
