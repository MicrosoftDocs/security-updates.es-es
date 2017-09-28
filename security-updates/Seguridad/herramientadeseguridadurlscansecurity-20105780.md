---
TOCTitle: Herramienta de seguridad URLScan Security
Title: Herramienta de seguridad URLScan Security
ms:assetid: 'fdd63bcd-1d08-4cb6-b017-c2bf43b46775'
ms:contentKeyID: 20105780
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc242650(v=MSDN.10)'
---

Herramienta de seguridad URLScan Security
=========================================

UrlScan V2.5 es una herramienta de seguridad que restringe los tipos de peticiones HTTP que puede procesar Internet Information Services. Al bloquear peticiones HTTP concretas, la herramienta de seguridad UrlScan previene la posibilidad de que peticiones potencialmente dañinas puedan alcanzar el servidor. UrlScan 2.5 se puede instalar directamente sobre servidores con IIS4.0 o versión superior.

##### En esta página

[](#eeaa)[Nuevas funcionalidades en UrlScan 2.5](#eeaa)
[](#edaa)[Determinar si se debe emplear UrlScan 2.5 con IIS 6.0](#edaa)
[](#ecaa)[Instalación de UrlScan 2.5](#ecaa)
[](#ebaa)[Preguntas más frecuentes](#ebaa)

### Nuevas funcionalidades en UrlScan 2.5

Microsoft ha vuelto a lanzar la versión 2.5 de UrlScan con un nuevo proceso de instalación que efectúa una instalación limpia de UrlScan 2.5 en sistemas con IIS4.0 o versión posterior.

**Importante:** Aunque la herramienta de seguridad UrlScan 2.5 ayuda a proteger a los servidores frente a ataques, es necesario evaluar e instalar las últimas actualizaciones de seguridad proporcionadas por Microsoft. Según se van descubriendo nuevas vilnerabilidades de seguridad, Microsoft publica actualizaciones en forma de Service Packs, parches y hotfixes.Para contribuir a reducir los riesgos que esas vulnerabilidades pudieran representar, es necesario que se apliquen estas actualizaciones de seguridad tan pronto como estén disponibles.

La herramienta de seguridad UrlScan consta de dos archivos: UrlScan.dll y UrlScan.ini, juntos componen el paquete UrlScan.exe. La última actualización de UrlScan 2.5 ofrece a los administradores mayor control sobre la configuración de UrlScan y proporciona funcionalidades que ayudan a reforzar la seguridad del servidor.

UrlScan 2.5 introduce las siguientes funcionalidades que no estaban disponibles en versiones anteriores:

-   [Cambio del directorio del archivo de log](http://www.microsoft.com/spain/technet/security/tools/urlscan.mspx?)

-   [Log de URLs largas](http://www.microsoft.com/spain/technet/security/tools/urlscan.mspx?)

-   [Restricción del tamaño de las peticiones](http://www.microsoft.com/spain/technet/security/tools/urlscan.mspx?)

**Cambio del directorio del archivo de Log**

La opción **LoggingDirectory** se emplea para especificar la carpeta en la cual se va a guardar el archivo de log. Este valor debe ser el path absoluto (por ejemplo, c:\\logs) del archivo de log. Si no se especifica ninguna carpeta, UrlScan creará el archivo de log en la misma carpeta donde se localiza UrlScan.dll.

**Log de URLs largas**

La opción **LogLongUrls** se ha incorporado para incrementar la longitud de URLs que se van a almacenar en el archivo de Log. En versiones anteriores, UrlScan truncaba las líneas más largas a 1024 bytes. Esta nueva opción permite un log avanzado al incrementar este tamaño máximo a 128 Kilobytes (KB). Valores admitidos de esta opción son 0 y 1, y el valor por defecto es 0. Si **LogLongUrls** está como 1, el log se amplía a URLs de hasta 128 KB por petición. Si el valor se deja en 0, las entradas del log solamente contendrán los primeros 1024 bytes.

**Restricción del tamaño de las peticiones**

Se ha añadido la sección **RequestLimits** de modo que UrlScan puede forzar límites de tamaño, en bytes, de partes independientes de las peticiones que llegan al servidor. La sección **RequestLimits** incluye las siguientes tres entradas:

-   **MaxAllowedContentLength:** fuerza un valor máximo a la variable contentlength. En esta versión no impide que el servidor lea más datos que los que especifica este valor. Por ejemplo, si un cliente realiza una petición POST en un fragmento codificado, esta opción de UrlScan no es efectiva a la hora de comprobar el tamaño de la entidad solicitada. El valor por defecto es ~2 GB (2,000,000,000 bytes).

-   **MaxUrl:** Restringe la longitud de la URL peticionaria, en bytes, pero no restringe la longitud de la cadena de consulta (query string). Al actualizar UrlScan con el proceso de instalación, este valor se establece en 16 KB.

    **Nota:** Si se extrae manualmente UrlScan.dll del archivo UrlScan.exe y no se actualiza UrlScan.ini, el valor por defecto será de 260 bytes. En este caso, habrá que añadir una línea en UrlScan.ini con el texto MaxUrl = 16384 para sobreescribir el valor por defecto.

-   **MaxQueryString:** Restringe la longitud de la cadena de consulta (query string), en bytes. El valor por defecto es 4 KB.

Se puede imponer una limitación de tamaño a una cabecera de petición si se antepone **Max-** al nombre de cualquier cabecera. Por ejemplo, la siguiente entrada impone un límite de 100 bytes en la cabecera "Content-Type": Max-Content-Type=100. Para visualizar una cabecera sin especificar valor máximo, utilice 0. Por ejemplo, Max-User-Agent=0. Asimismo, cualquier cabecera no se descrita en la sección **RequestLimits** no se examina para limitar su tamaño.

[](#mainsection)[Principio de la página](#mainsection)

### Determinar si se debe emplear UrlScan 2.5 con IIS 6.0

Windows Server 2003 incorpora muchas características de seguridad que permiten proteger los servidores IIS6.0. UrlScan aporta algunas funcionalidades adicionales, como el control de verbos, más allá de lo que ofrece IIS6.0. También sucede que algunas organizaciones han integrado ciertas funcionalidades de UrlScan en sus prácticas de administración de IIS y para otros servidores de Microsoft. Si desea utilizar las funcionalidades y características adicionales de UrlScan 2.5 o simplemente mantener su administración de seguridad actual, entonces puede considerar la posibilidad de instalar y utilizar UrlScan con IIS6.0.

UrlScan 2.5 no se incluye con IIS6.0 porque IIS6.0 ya incorpora ciertas funcionalidades que ofrecen un nivel de seguridad igual o mejor que muchas de las que aporta UrlScan 2.5. La Tabla 1 compara la forma en que IIS 6.0y UrlScan manejan ciertos aspectos de la seguridad. Esta comparativa le ayudará a decidir si ha de instalar UrlScan 2.5 en sus servidores con IIS 6.0.

**Tabla 1: Comparativa de funcionalidades de UrlScan 2.5 y características incorporadas en IIS 6.0**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Funcionalidad de UrlScan 2.5</strong></td>
<td style="border:1px solid black;"><strong>Característica incluida en IIS 6.0</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>DenyExtensions:</strong> esta característica se incorporó a UrlScan para limitar la superficie de ataque del servidor al prevenir que se ejecutasen ciertas peticiones concretas en el servidor mediante código ISAPI o CGI en base a la extensión de los nombres de archivos.</td>
<td style="border:1px solid black;">IIS 6.0 limita la superficie de ataque del servidor al permitir a los administradores especificar qué codigo ISAPI o CGI puede ejecutarse en el servidor. Puesto que IIS 6.0 especifica el código directamente, no es necesario conocer qué extensiones de nombre de archivo en la URL son capaces de invocar esa ejecución.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>DenyVerbs:</strong> El código WebDAV puede invocarse en un servidor web basándose en el uso de ciertos verbos HTTP. Esta funcionalidad se incorpora a UrlScan para limitar la superficie de ataque del servidor al impedir la ejecución de peticiones que pueden invocar WebDAV.</td>
<td style="border:1px solid black;">IIS 6.0 permite a los administradores activar o desactivar de forma explícita WebDAV. Puesto que esta acción afecta al código ejecutable WebDAV directamente, no es necesario revisar cada verbo HTTP asociado con cada petición.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>DenyHeaders:</strong> El código WebDAV puede ser invocado en un servidor web en base a la presencia de ciertas cabeceras HTTP. Esta funcionalidad se incluye en UrlScan para limitar el área de ataque del servidor al impedir que ciertas peticiones puedan invocar WebDAV.</td>
<td style="border:1px solid black;">IIS 6.0 permite a los administradores activar o desactivar de forma explícita WebDAV. Puesto que esta acción afecta al código ejecutable WebDAV directamente, no es necesario revisar cada cabecera HTTP asociada con cada petición.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>NormalizeUrlBeforeScan:</strong> Esta funcionalidad permite a los administradores especificar si IIS puede procesar la URL en bruto, tal y como se la envía el cliente, o la URL normalizada (canónica) que se procesa en el servidor.<br />
<strong>Nota:</strong> No resulta práctico poner el valor a cero en un servidor en producción. Cuando este valor se deja en 0, todas las extensiones de nombre de archivo y otras verificaciones de URL en el archivo UrlScan.ini deben contener todas las posibles variantes de codificación de cada carácter. El número de combinaciones resultante hace prácticamente imposible asumir esta actividad en un servidor en producción.</td>
<td style="border:1px solid black;">El mecanismo de bloqueo incorporado a IIS 6.0 se basa en que el código que se puede ejecutar no depende de la URL de la petición del cliente. Por este motivo, la directiva <strong>NormalizeUrlBeforeScan</strong> no es necesaria en IIS 6.0.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>VerifyNormalization:</strong> UrlScan fue diseñado para correr sobre diversas verisones de IIS. El código que controla la normalización de URL ha sido mejorada en versiones posteriores de IIS y Service Packs. Esta funcionalidad permite a UrlScan detectar riesgos potenciales con la normalización de URL en sistemas no actualizados.</td>
<td style="border:1px solid black;">El compontente HTTP.SYS usado en IIS 6.0 mejora sensiblemente el código de normalización, el cual ha sido específicamente diseñado para proteger al servidor de ataques basados en la normalización de URL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>DenyUrlSequences:</strong> Esta característica se incorpora a UrlScan para detectar secuencias utilizadas en ataques a servidores basados en URL.</td>
<td style="border:1px solid black;">En IIS 6.0 no es necesario denegar secuencias URL. Por diseño, IIS 6.0 no es sensible a ataques basados en URL que utilicen ninguna secuencia de caracteres indicada en la sección <strong>DenyUrlSequences</strong> del archivo UrlScan.ini proporcionado por Microsoft.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>AllowDotInPath:</strong> El mecanismo de bloqueo de UrlScan depende de una notificación de filtrado que tiene lugar muy al comienzo del procesado de una petición web. En ese momento UrlScan no puede saber con seguridad cómo va a interpretar IIS la cadena URL para extraer el valor PATH_INFO. Podría suceder que PATH_INFO pueda verse influida por la presencia de una extensión de nombre de archivo contenida en el URL. Poniendo el valor <strong>AllowDotInPath</strong> a 0 se obliga a UrlScan a rechazar cualquier petición donde la extensión del nombre de archivo sea ambigua debido a la existencia de un punto en el path.</td>
<td style="border:1px solid black;">La función <strong>AllowDotInPath</strong> no es necesaria en IIS 6.0 porque IIS 6.0 no depende de notificaciones de filtro para activar su mecanismo de bloqueo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>RemoveServerHeader:</strong> Esta funcionalidad permite a UrlScan a eliminar o alterar la identidad del servidor desde la cabecera &quot;Server&quot; de la respuesta al cliente.</td>
<td style="border:1px solid black;">IIS 6.0 no incluye la funcionalidad <strong>RemoveServerHeader</strong> porque no ofrece una protección real. Muchos ataques a servidores no se dirigen específicamente a un sistema operativo. Asimismo, es posible detectar la identidad de un servidor y la información acerca de su sistema operativo mediante procedimientos ajenos al contenido de la cabecera Server.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>EnableLogging</strong>, <strong>PerProcessLogging</strong> y <strong>PerDayLogging:</strong> UrlScan no forma parte del núcleo de IIS; más bien es una utilidad add-on que produce sus propios archivos de log. Estos parámetros controlan la manera en que UrlScan produce y nombra sus propios archivos de log.</td>
<td style="border:1px solid black;">IIS 6.0 registra toda su actividad de bloqueo en los logs W3SVC. Las peticiones rechazadas por bloqueo o código ejecutable se identifican como errores 404 con nivel de sub-error 2 (404.2) en los logs. Las peticiones de archivos que se bloquean por no identificados se registran como error 404 con subnivel de error 3 (404.3).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>AllowLateScanning:</strong> esta funcionalidad permite a los administradores especificar si UrlScan debe examinar URLs antes o después de otros filtros. Existen unos cuantos filtros que modifican las cadenas URL, y lo deseable sería que UrlScan examine lso URL después de ser modificados. Un ejemplo de filtros de este tipo es FrontPage Server Extensions.</td>
<td style="border:1px solid black;">The <strong>AllowLateScanning</strong> no es necesario en IIS 6.0 debido a que IIS 6.0 no depende de notificaciones de filtros para activar sus mecanismos de bloqueo. El mecanismo de bloqueo incluido en IIS 6.0 se basa en el código ejecutable que se puede ejecutar, y no en el URL de la petición del cliente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>RejectResponseUrl:</strong> esta funcionalildad opera conjuntamente con <strong>UseFastPathReject</strong>. Si <strong>UseFastPathReject</strong> se pone a 0, las peticiones rechazadas se re-mapean al URL especificado en <strong>RejectResponseUrl</strong>. Si este URL no existe, el cliente recibirá un mensaje de error 404, igual que si hubiese solicitado una página inexistente. Si el URL especificado no existe, el servidor puede adaptar la respuesta a enviar al cliente.</td>
<td style="border:1px solid black;">En IIS 6.0, una petición rechazada debido a un bloqueo sobre código ejecutable, genera un mensaje de error 404.2. Un archivo estático rechazado debido a un tipo desconocido MIME, genera un error 404.3. Los administradores pueden utilizar el mecanismo de particularización de errores de IIS para controlar estas respuestas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>UseFastPathReject:</strong> El mecanismo de bloqueo de UrlScan depende de una notificación de filtrado que tiene lugar muy al comienzo del procesado de una petición web. Por ello, si UrlScan rechaza la petición directamente desde esta notificación, el mensaje de respuesta 404 habitual no puede generarse. En lugar de ello, el cliente recibirá una respuesta escueta 404 en vez del mensaje de explicación más amplio que normalmente se devuelve. Si <strong>UseFastPathReject</strong> se pone en 0, UrlScan re-mapea la petición al URL especificado por <strong>RejectResponseUrl</strong>.</td>
<td style="border:1px solid black;">En IIS 6.0, una petición rechazada debido a un bloqueo sobre código ejecutable, genera un mensaje de error 404.2. Un archivo estático rechazado debido a un tipo desconocido MIME, genera un error 404.3. Los administradores pueden utilizar el mecanismo de particularización de errores de IIS para controlar estas respuestas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>AllowHighBitCharacters:</strong> Esta funcionalidad permite la detección de caracteres no ASCII en los URLs.</td>
<td style="border:1px solid black;">El rango de caracteres permitidos está controlado por HTTP.SYS. Este valor puede cambiarse modificando las siguientes claves del registro: HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\HTTP\Parameters\EnableNonUTF8<br />
<strong>Aviso:</strong> Modificar de forma incorrecta el registro puede dañar seriamente su sistema. Antes de modificar cualquier clave del registro, se debe realizar una copia de seguridad del mismo y de los datos importantes almacenados en la máquina.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>MaxAllowedContentLength:</strong> Esta característica permite a UrlScan poner límites al tamaño de las peticiones enviadas al servidor.</td>
<td style="border:1px solid black;">IIS 6.0 incluye la posibilidad de limitar el tamaño de las peticiones; este valor es configurable modificando las propiedades <strong>MaxRequestEntityAllowed</strong> y <strong>ASPMaxRequestEntityAllowed</strong> de la metabase.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>MaxUrl</strong>, <strong>MaxQueryString</strong> y <strong>MaxHeader:</strong> Estos valores permiten a UrlScan limitar los tamaños de los URLs, cadenas de consulta y cabeceras específicas que se envían al servidor.</td>
<td style="border:1px solid black;">El componente HTTP.SYS de IIS 6.0 permite establecer límites en varias partes de las peticiones. Los valores pueden cambiarse modificando los valores <strong>AllowRestrictedChars</strong>, <strong>MaxFieldLength</strong>, <strong>UrlSegmentMaxLength</strong> y <strong>UrlSegmentMaxCount</strong> dentro de las siguientes claves del registro:
<ul>
<li>HKEY_LOCAL_MACHINE\System\CurrentControlSet\ Services\HTTP\Parameters\AllowRestrictedChars</li>
<li>HKEY_LOCAL_MACHINE\System\CurrentControlSet\ Services\HTTP\Parameters\MaxFieldLength</li>
<li>HKEY_LOCAL_MACHINE\System\CurrentControlSet\ Services\HTTP\Parameters\UrlSegmentMaxLength</li>
<li>HKEY_LOCAL_MACHINE\System\CurrentControlSet\ Services\HTTP\Parameters\UrlSegmentMaxCount</li>
</ul>
<strong>Aviso:</strong> Modificar de forma incorrecta el registro puede dañar seriamente su sistema. Antes de modificar cualquier clave del registro, se debe realizar una copia de seguridad del mismo y de los datos importantes almacenados en la máquina.</td>
</tr>
</tbody>
</table>
 

¿Por qué se hace UrlScan disponible para IIS 6.0? UrlScan proporciona un pequeño nivel adicional de seguridad sobre el que ofrece IIS 6.0. UrlScan es una herramienta flexible que algunos usuarios emplean para propósitos que no se cubren en este artículo. Algunas organizaciones han integrado características de UrlScan en sus prácticas de administración de servidores IIS y otros servidores de Microsoft. Por algunas de estas razones, algunos clientes pueden instalar UrlScan 2.5 y usarlo con IIS 6.0.

Para conocer más sobre UrlScan 2.5, puede leer el artículo 307608 de la Knowledge Base de Microsoft, [Utilizar URLScan en IIS](http://support.microsoft.com/default.aspx?scid=kb;%5Bln%5D;307608).

[](#mainsection)[Principio de la página](#mainsection)

### Instalación de UrlScan 2.5

UrlScan 2.5 se instala desde cero en un ordenador con IIS 4.0 o posterior. Se admiten también escenarios de actualización.

**Para instalar UrlScan 2.5**

1.  [Descargue el archivo Setup.exe](http://www.microsoft.com/downloads/details.aspx?familyid=23d18937-dd7e-4613-9928-7f94ef1c902a&displaylang=en) para UrlScan 2.5.

2.  Haga doble click en el icono Setup.exe.

3.  Lea el texto de Acuerdo de Licencia de Usuario Final presentado por el paquete de instalación y pulse **Yes** para aceptar las condiciones y continuar. Si pulsa **No**, el instalador cerrará el proceso.

4.  Cuando el instalador terminar, se muestra el siguiente mensaje: "UrlScan ha sido instalado con éxito". Pulse **OK** para cerrar el instalador.

**Para desinstalar UrlScan**

1.  En el Panel de Control, haga doble click en **Añadir o Quitar Programas**.

2.  Seleccione UrlScan 2.5 y pulse el botón **Cambiar/Eliminar**.

3.  Cuando UrlScan 2.5 ya ha sido eliminado del servidor, aparece el mensaje: "UrlScan ha sido desinstalado con éxito" Pulse **OK** para terminar el proceso de desinstalación.

**Pasos realizados por UrlScan 2.5 Installer**

En el proceso de instalación de UrlScan 2.5 el instalador hace lo siguiente:

-   Instala los archivos UrlScan.dll y UrlScan.ini en el directorio %windir%\\system32\\inetsrv\\UrlScan. Si UrlScan estaba ya instalado en el ordenador, el archivo UrlScan.ini se actualiza con los nuevos valores que no existían en el anterior archivo de configuración.

-   Añade UrlScan como filtro global de IIS.

Cuando UrlScan se instala en un servidor con IIS 6.0, el instalador realiza algunos cambios adicionales que permiten a UrlScan 2.5 ejecutarse bajo el nuevo modelo de proceso de IIS 6.0. Estos cambios son los siguientes:

-   **PerProcessLogging** se pone a 1 en el archivo UrlScan.ini. Esto garantiza que dos procesos UrlScan no escriben sobre el archivo de log simultáneamente.

-   UrlScan queda marcado como "cache-aware" en la metabase. Con ello se garantiza que dos o más procesos de usuario que ejecutan UrlScan no escriben sobre el archivo de log simultáneamente.

-   Se crea un nuevo directorio de log, que es un subdirectorio debajo de la carpeta \\inetsrv\\UrlScan directory. Con ello se evita que el tamaño del directorio de UrlScan se desborde excesivamente con el contenido de los archivos de log que va a producir la opción **PerProcessLogging**.

Al instalar UrlScan 2.5 sobre IIS, el instalador asigna permisos para UrlScan.dll, UrlScan.ini y el archivo de log. En la instalación sobre IIS 6.0, el proceso de instalación asigna permisos sobre los mismos archivos para permitirle a UrlScan 2.5 trabajar con los procesos de usuario de IIS 6.0 en modo aislado. La tabla 2 muestra la lista de permisos asignados por el instalador de UrlScan 2.5.

**Tabla 2: Permisos asignados por UrlScan 2.5 con IIS 6.0**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Archivo/Directorio</strong></td>
<td style="border:1px solid black;"><strong>Permisos</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">..\inetsrv\urlscan\urlscan.dll</td>
<td style="border:1px solid black;">Read y Execute (sólo en IIS 6.0): LocalService, IIS_WPG, y NetworkService<br />
Full: Administradores y LocalSystem</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">..\inetsrv\urlscan\urlscan.ini</td>
<td style="border:1px solid black;">Read (sólo en IIS 6.0): IIS_WPG, LocalService y NetworkService<br />
Full: Administradores y LocalSystem</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">..\inetsrv\urlscan\logs</td>
<td style="border:1px solid black;">Read y Write (sólo en IIS 6.0): IIS_WPG, LocalService y NetworkService<br />
Full: Administradores y LocalSystem</td>
</tr>
</tbody>
</table>
 

Si se detecta una versión anterior de UrlScan instalada en el ordenador, la instalación se considera una actualización. En el escenario de actualización, los cambios que realiza el proceso instalador serán los mismos que en la instalación limpia salvo que se haya configurado un directorio de log diferente. Si se ha indicado una ubicación distinta para los logs de UrlScan, el nuevo directorio de logs no se creará.

[](#mainsection)[Principio de la página](#mainsection)

### Preguntas más frecuentes

Haga clic sobre cualquiera de las siguientes preguntas:

-   ¿Qué es UrlScan?

-   ¿Funciona UrlScan 2.5 sobre IIS 6.0?

-   Ya estoy utilizando UrlScan 2.0. ¿Por qué tengo que instalar esta actualización?

-   Ya he configurado UrlScan para mi sitio web. Va a sobreescribir UrlScan 2.5 mis parámetros actuales?

-   Si UrlScan 2.5 ayuda a proteger el servidor frente a ciertas vulnerabilidades, ¿sigue siendo necesario aplicar actualizaciones de seguridad

-   No estoy seguro de si alguna de mis aplicaciones utiliza transferencia en fragmentos. ¿En qué consiste?

**Pregunta: ¿Qué es UrlScan?**

**Respuesta:** UrlScan es una herramienta de seguridad que examina todas las peticiones entrantes en el servidor filtrando las peticiones en base a reglas establecidas por el administrador. El filtrado de peticiones ayuda a proteger el sistema asegurando que solamente se procesan las peticiones válidas. UrlScan ayuda a proteger los servidores Web en la medida en que muchos de los ataques externos comparten características comunes que incluyen el uso de peticiones en formas poco usuales. Por ejemplo, la cadena de petición puede ser extremadamente larga, puede solicitarse alguna acción poco habitual, puede incluir juegos de caracteres alternativos o secuencias de caracteres que rara vez se ven en las peticiones legítimas. Al filtrar estas peticiones inusuales, UrlScan previene al servidor de la ejecución de acciones en respuesta, las cuales pueden causar daños potenciales.

**Pregunta: ¿Funciona UrlScan 2.5 sobre IIS 6.0?**

**Respuesta:** Sí, UrlScan 2.5 es la única versión de UrlScan que Microsoft soporta para su uso con IIS 6.0.

**Pregunta: Ya estoy utilizando UrlScan 2.0. ¿Por qué tengo que instalar esta actualización?**

**Respuesta:** UrlScan 2.5 incorpora nuevas funcionalidades que mejoran la seguridad de los servidores con IIS. Estas nuevas funcionalidades son:

-   Cambio del directorio de log

-   Registro (logging) de URLs largas

-   Restricción del tamaño de las peticiones

**Pregunta: Ya he configurado UrlScan para mi sitio web. Va a sobreescribir UrlScan 2.5 mis parámetros actuales?**

**Respuesta:** No, el instalador únicamente añade nuevas entradas a las existentes en su archivo de configuración. UrlScan soporta todos los parámetros de configuración de las versiones anteriores.

**Pregunta: Si UrlScan 2.5 ayuda a proteger el servidor frente a ciertas vulnerabilidades, ¿sigue siendo necesario aplicar actualizaciones de seguridad?**

**Respuesta:** Sí. Para proteger su servidor de vulnerabilidades actuales o futuras, Microsoft recomienda encarecidamente que obtenga e instale las últimas actualizaciones de seguridad tan pronto como estén disponibles.

**Pregunta: No estoy seguro de si alguna de mis aplicaciones utiliza transferencia en fragmentos. ¿En qué consiste?**

**Respuesta:** la codificación de transferencia por fragmentos (Chunked-transfer encoding) es una característica de HTTP/1.1 que posibilita la transmisión del cuerpo del mensaje en una petición o respuesta por trozos, en los que se indica su tamaño. HTTP 1.1 permite a los clientes enviar peticiones POST utilizando esta técnica de troceado. En muchos casos, IIS decodifica automáticamente estas peticiones antes de ser procesadas, Si el tamaño de la petición sobrepasa un umbral determinado (por defecto 48 Kb), el código ISAPI o CGI al cual se dirige la petición necesita recomponer correctamente los fragmentos antes de pasar a su procesado. Si está ejecutando programas en un servidor que recibe peticiones POST y no está seguro de si soporta la transferencia por fragmentos, puede emplear UrlScan para prohibir la s peticiones que incluyan la cabecera "Transfer-Encodig". Para más información sobre la técnica de codificación de transferencia por fragmentos puede leer la sección 3.6.1 de la [RFC 2616](http://www.cis.ohio-state.edu/cgi-bin/rfc/rfc2616.html), "Hypertext Transfer Protocol ? HTTP/1.1."

[](#mainsection)[Principio de la página](#mainsection)
