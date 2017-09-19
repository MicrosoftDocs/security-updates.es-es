---
TOCTitle: 'Capítulo 11: Función de servidor de Servicios de Certificate Server'
Title: 'Capítulo 11: Función de servidor de Servicios de Certificate Server'
ms:assetid: 'a4238f44-28fc-4931-b1d5-a37d2a173284'
ms:contentKeyID: 20200251
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163135(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 11: Función de servidor de Servicios de Certificate Server

Actualizado: 27/12/05

##### En esta página

[](#eiaa)[Información general](#eiaa)
[](#ehaa)[Configuración de directiva de auditoría](#ehaa)
[](#egaa)[Asignaciones de derechos de usuario](#egaa)
[](#efaa)[Opciones de seguridad](#efaa)
[](#eeaa)[Configuración del registro de eventos](#eeaa)
[](#edaa)[Entradas de registro adicionales](#edaa)
[](#ecaa)[Configuración de seguridad adicional](#ecaa)
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Este capítulo proporciona orientación que le ayudará a consolidar servidores en los que se ejecuta Microsoft® Windows Server™* *2003 con Service Pack 1 (SP1) y Servicios de Certificate Server de Microsoft en su entorno. Aunque se incluye toda la información que necesita para proteger estos tipos de servidores, en este capítulo no se proporcionan detalles acerca de cómo crear una infraestructura segura de Servicios de Certificate Server en su entorno ni cómo implementar una entidad emisora de certificados. Estos temas se tratan con detalle en la documentación del producto Windows* *Server* *2003. También se tratan en el *Kit de recursos de Windows* Server 2003 y en notas del producto disponibles en el sitio web de Microsoft. Encontrará información adicional en una guía complementaria: [*Seguridad en LAN inalámbricas con Servicios de Certificate Server*](http://go.microsoft.com/fwlink/?linkid=14843), en http://go.microsoft.com/fwlink/?LinkId=14843.

La configuración que se muestra en este capítulo se realiza y aplica mediante Directiva de grupo. Un objeto de directiva de grupo (GPO) que complementa la Directiva de línea de base de servidores miembro (MSBP) puede vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores de entidad emisora con el fin de proporcionar los cambios de configuración de seguridad necesarios para esta función de servidor. Este capítulo sólo trata aquellas configuraciones de la directiva que varían del MSBP.

Siempre que sea posible, estas configuraciones se reunirán en una plantilla incremental de Directiva de grupo que se aplicará a la unidad organizativa de servidores de entidad emisora. Parte de los ajustes que se muestran en este capítulo no se pueden aplicar mediante Directiva de grupo. Se proporciona información detallada acerca de cómo configurar estos ajustes manualmente.

El nombre de la plantilla de seguridad de servidores de entidad emisora para el entorno de cliente de empresa es EC-CA Server.inf. Ésta es la plantilla incremental de servidores de entidad emisora, la cual sirve para crear un GPO nuevo que se vincula a la unidad organizativa de servidores de entidad emisora en el entorno apropiado. Se proporcionan instrucciones detalladas en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", para ayudarle a crear las UO y las directivas de grupo, así como para importar la plantilla de seguridad apropiada en cada GPO.

Para obtener más información acerca de la configuración en el MSBP, consulte el capítulo 4, “Directiva de línea de base de servidores miembro”. Para obtener más información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159)*, *que está disponible en* *http://go.microsoft.com/fwlink/?LinkId=15159.

**Nota**: las recomendaciones de configuración de directiva para la función de servidor de Servicios de Certificate Server se probaron únicamente para el entorno de cliente de empresa. Por este motivo, en este capítulo no se incluye la información de denegación de servicio (DoS) que se especificó para la mayoría de las restantes funciones de servidor definidas en esta guía.

Podría instalar Microsoft Internet Information Server (IIS) en algunos de los servidores de Servicios de Certificate Server de su entorno para que puedan distribuir certificados de entidad emisora de certificados (CA) y listas de revocación de certificados (CRL). IIS se utiliza también para alojar las páginas de inscripción web del servidor de Servicios de Certificate Server, que permiten que los clientes que no utilizan Microsoft Windows® puedan inscribir certificados. Antes de utilizar la información de este capítulo, averigüe cómo instalar IIS de forma segura, tal como se describe en el capítulo 9 de esta guía, "Función de servidor web". Si instala IIS en sus entidades emisoras, la plantilla de configuración de seguridad que se desarrolló para el capítulo 9 deberá aplicarse a los servidores de Servicios de Certificate Server antes de configurar los parámetros recomendados que se describen en este capítulo.

**Nota**: en entornos simplificados se puede utilizar el servidor CA emisor para alojar el servidor web, el certificado de la entidad emisora y los puntos de descarga de listas CRL. No obstante, considere la posibilidad de usar un servidor web independiente en su propio entorno para aumentar la seguridad de las entidades emisoras de certificados.

IIS se utiliza para alojar páginas de inscripción del servidor de certificados, así como para distribuir puntos de descarga de listas CRL y certificados de entidad emisora para clientes que no utilizan Windows. Microsoft recomienda no instalar IIS en el servidor de la entidad emisora raíz. Si es posible, se debe evitar ejecutar IIS en las entidades emisoras de certificados y en las entidades intermedias de su entorno. Resulta más seguro alojar los puntos de descarga web para los certificados de CA y las listas CRL en un servidor distinto al de la entidad emisora de certificados. Muchos usuarios de certificados (internos y externos) que necesiten recuperar información de las listas CRL o de la cadena de CA no dispondrán necesariamente de permiso de acceso a la entidad. Sin embargo, no puede aislar usuarios de la entidad emisora si aloja allí los puntos de descarga.

[](#mainsection)[Principio de la página](#mainsection)

### Configuración de directiva de auditoría

La configuración de directiva de auditoría para servidores de Servicios de Certificate Server en la guía del entorno de cliente de empresa se configura a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que en todos los servidores de Servicios de Certificate Server se registre la información de auditoría de seguridad pertinente.

[](#mainsection)[Principio de la página](#mainsection)

### Asignaciones de derechos de usuario

La configuración de la asignación de derechos de usuario para servidores de Servicios de Certificate Server en el entorno de cliente de empresa se establece también a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, “Configuración de la directiva de línea de base de servidores miembro". La configuración de MSBP permite garantizar que en una organización se configura de forma uniforme el acceso adecuado a los servidores de Servicios de Certificate Server.

[](#mainsection)[Principio de la página](#mainsection)

### Opciones de seguridad

La sección Opciones de seguridad de Directiva de grupo se emplea para habilitar o deshabilitar parámetros de configuración de seguridad de los equipos; por ejemplo, la firma digital de datos, los nombres de cuenta de administrador e invitado, el acceso a la unidad de disquete y de CD-ROM, el comportamiento de la instalación de controladores y los mensajes de inicio de sesión.

Los parámetros de las opciones de seguridad se pueden establecer en Windows Server 2003 en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\**
**Seguridad\\Opciones**

En la tabla siguiente se incluye la configuración de opciones de seguridad recomendadas para la función de servidor de Servicios de Certificate Server en el entorno de cliente de empresa. En el texto que sigue a la tabla se proporciona información detallada acerca de la configuración.

**Tabla 11.1 Configuración recomendada de opciones de seguridad**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Cliente de empresa</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
#### Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash
  
Esta configuración de directiva determina si el proveedor de seguridad de Transport Layer Security/Secure Sockets Layer (TLS/SSL) es compatible sólo con el conjunto cifrado TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA. En realidad, la compatibilidad con este conjunto de cifrado significa que el proveedor sólo admite el protocolo TLS como cliente y servidor (si procede).
  
El proveedor de seguridad de TLS/SSL utiliza los siguientes algoritmos:
  
-   El algoritmo de cifrado Triple Data Encryption Standard (3DES) para el cifrado del tráfico de TLS.
  
-   El algoritmo de clave pública Rivest, Shamir y Adelman (RSA) para el intercambio de claves y la autenticación de TLS. (RSA es una tecnología de cifrado de claves públicas desarrollada por RSA Data Security, Inc.)
  
-   El algoritmo hash SHA-1 para los requisitos de operaciones hash de TLS.
  
Para el Sistema de archivos de cifrado (EFS), el proveedor de seguridad TLS/SSL admite sólo el algoritmo de cifrado Triple DES para cifrar los datos de archivo almacenados en el sistema de archivos NTFS de Windows. De forma predeterminada, EFS utiliza el algoritmo DESX para cifrar los datos de archivo.
  
Si habilita esta configuración de directiva, los equipos que cumplen esta función de servidor en su entorno utilizarán los algoritmos más eficaces disponibles para las operaciones de cifrado digital, hash y firma. El uso de estos algoritmos minimiza el riesgo porque limitan la capacidad de un usuario no autorizado a poner en peligro los datos cifrados o firmados digitalmente.
  
Por esos motivos, el parámetro **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado,** **firmay operaciones hash** se configura como **Habilitado** para el entorno de cliente de empresa.
  
**Nota**: los equipos cliente que tienen esta configuración de directiva habilitada no podrán comunicarse a través de protocolos cifrados o firmados digitalmente con servidores que no admiten estos algoritmos. Los equipos cliente de red que no admiten estos algoritmos no podrán utilizar los servidores que los requieran para las comunicaciones de red. Por ejemplo, muchos servidores web basados en Apache no están configurados para admitir TLS.
  
Si habilita esta configuración, también deberá configurar Internet Explorer para que utilice TLS. Para ello, abra el cuadro de diálogo **Opciones de Internet** del menú **Herramientas** de Internet Explorer, haga clic en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet**, desplácese hasta la parte inferior de la lista **Configuración** y después haga clic en la casilla de verificación **Usar TLS 1.0**. También se puede configurar esta funcionalidad a través de Directiva de grupo o con el Kit de administración de Internet Explorer.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
La configuración del registro de eventos para servidores de Servicios de Certificate Server en el entorno de cliente de empresa se configura a través de MSBP. Para obtener más información sobre MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas de registro adicionales
  
Se crearon entradas de Registro adicionales para el archivo de plantilla EC-CA Server.inf. Estas entradas no se definen dentro de los archivos de plantilla administrativa (.adm) para el entorno de cliente de empresa según se define en esta guía. En los archivos .adm se definen las directivas del sistema y las restricciones para la configuración del escritorio, del núcleo y de seguridad para Windows* *Server* *2003 con SP1.
  
Las entradas de Registro adicionales se configuran dentro de la plantilla de seguridad para automatizar su implementación. Si se quita la Directiva de grupo incremental de Servicios de Certificate Server para este entorno, su configuración no se quita automáticamente y debe cambiarse manualmente con una herramienta de edición del Registro, como Regedt32.exe.
  
Puede configurar las entradas del Registro en Windows Server 2003 en la siguiente ubicación del Editor de objetos de Directiva de grupo:
  
**MACHINE\\SYSTEM\\CurrentControlSet\\Services\\CertSvc\\Configuration**
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
Se sugieren las listas ACL que se indican a continuación. Es posible asignarlas a través de Directiva de grupo. No obstante, estas ACL no se incluyen en las plantillas de seguridad que se proporcionan con esta guía porque la ruta de acceso para la base de datos y los registros variará según el servidor. Por ejemplo, su servidor de Servicios de Certificate Server podría tener una unidad C:\\, D:\\ y E:\\. En la siguiente sección se describe detalladamente el modo de implementar manualmente estas configuraciones de directiva.
  
#### ACL del sistema de archivos
  
Un usuario no autorizado puede obtener acceso localmente o a través de la red a aquellos archivos que no se protegen mediante listas de control de acceso (ACL) para verlos, cambiarlos o eliminarlos fácilmente. Aunque las listas ACL pueden contribuir a proteger los archivos, el cifrado brinda una protección muy superior y resulta una opción viable para los archivos a los que sólo necesita tener acceso un usuario.
  
La tabla siguiente incluye las ACL de sistema de archivos para servidores de Servicios de Certificate Server de *Windows Server 2003* en el entorno de cliente de empresa. En este entorno, los servidores de Servicios de Certificate Server utilizan **D: \\CertSrv** como directorio de base de datos de certificados y los registros de base de datos se almacenan en la carpeta predeterminada **%SystemRoot%\\system32\\CertLog**. También es posible mover los registros de la unidad del sistema a una unidad reflejada independiente físicamente, como **E: \\CertLog.** Atendiendo a consideraciones de seguridad no es imprescindible la separación de la base de datos y los registros en distintas unidades de disco físicas, pero se recomienda como medida de protección adicional en caso de error de disco y para mejorar el rendimiento. Las carpetas de instalación predeterminada de Servicios de Certificate Server **%SystemRoot%\\system32\\CertLog** y **%SystemRoot%\\system32\\CertSrv** tienen las listas ACL correctas de forma predeterminada, tal como se muestra en la tabla siguiente.
  
**Tabla 11.2 Listas ACL de sistema de archivos**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Ruta de ACL en la IU</p></th>  
<th><p>Cliente de empresa</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>%SystemRoot%\system32\CertLog (se propaga a todas las subcarpetas)</p></td>
<td style="border:1px solid black;"><p>Administradores (control total)</p>
<p>SISTEMA (control total)</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>%SystemRoot%\system32\CertSrv (se propaga a todas las subcarpetas)</p></td>
<td style="border:1px solid black;"><p>Administradores (control total)</p>
<p>SISTEMA (control total)</p>
<p>Usuarios (Leer y ejecutar, Listar el contenido de la carpeta y Leer)</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>D:\CertLog</p></td>
<td style="border:1px solid black;"><p>Administradores (control total)</p>
<p>SISTEMA (control total)</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>D:\CertSrv</p></td>
<td style="border:1px solid black;"><p>Administradores (control total)</p>
<p>SISTEMA (control total)</p>
<p>Usuarios (Leer y ejecutar, Listar el contenido de la carpeta y Leer)</p></td>
</tr>
</tbody>
</table>
<p> </p>

Debido a que las entidades emisoras de certificados contienen información confidencial, se habilita la auditoría de archivos en las carpetas de Servicios de Certificate Server enumeradas en la tabla anterior. Las entradas de auditoría se configuran tal como se muestra en la siguiente tabla:

**Tabla 11.3 Configuración de auditoría de archivos de Servicios de Certificate Server y Registro**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ruta del archivo o del Registro</p></th>
<th><p>Tipo de auditoría</p></th>
<th><p>Configuración de auditoría</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>%SystemRoot%\system32\CertLog</p></td>
<td style="border:1px solid black;"><p>Error</p></td>
<td style="border:1px solid black;"><p>Todos (Control total)</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>%SystemRoot%\system32\CertSrv</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Todos (Modificar)</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>D:\CertSrv</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Todos (Modificar)</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>D:\CertLog</p></td>
<td style="border:1px solid black;"><p>Correcto</p></td>
<td style="border:1px solid black;"><p>Todos (Modificar)</p></td>
</tr>  
</tbody>  
</table>
  
Con estas configuraciones de directiva se auditarán tanto los accesos fallidos (de lectura o modificación) como las modificaciones realizadas por cualquier usuario.
  
#### Seguridad de las cuentas conocidas
  
Windows* *Server* *2003 con SP1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son *Invitado* y *Administrador*.
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.
  
El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.
  
**Para proteger las cuentas conocidas en los servidores de entidad emisora**
  
-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.
  
-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás.
  
-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.
  
-   Registre estos cambios en una ubicación segura.
  
    **Nota**: el nombre de la cuenta integrada de Administrador puede cambiarse mediante la utilización de la directiva de grupo. Esta configuración de directiva no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque cada organización debe escoger un nombre único para esta cuenta. Sin embargo, puede configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** si desea realizar ese tipo de modificación en el entorno EC. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.
  
#### Seguridad de las cuentas de servicios
  
A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de la directiva utilizando SCW
  
Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
Durante los pasos de creación de la directiva de servidor probablemente elimine la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.
  
**Para crear la directiva de servidores de Servicios de Certificate Server**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el equipo al dominio, que aplicará toda la configuración de seguridad de las UO principales.
  
4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor que comparte esta función. Los ejemplos incluyen servicios específicos de la función, software y agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
6.  Asegúrese de que las funciones de servidor detectadas sean apropiadas para su entorno; por ejemplo, la función de Servicios de Certificate Server.
  
7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
9.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
11. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.
  
12. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
13. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
14. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-CA Server.inf).
  
15. Guarde la directiva con un nombre apropiado (por ejemplo, Certificate Services.xml).
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método original de implementación le permite deshacer fácilmente las directivas implementadas desde el SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.
  
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
scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\ Certificate Services.xml" /g:"Certificate Services Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han explicado las configuraciones de directiva que se pueden utilizar para consolidar los servidores de Servicios de Certificate Server en los que se ejecuta Windows Server 2003 con SP1 en el entorno de Cliente de empresa que se define en esta guía. La configuración se establece y se aplica a través de un objeto de directiva de grupo (GPO) que complementa a MSBP. Los GPO pueden vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores de Servicios de Certificate Server para proporcionar seguridad adicional.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores que ejecutan Windows Server 2003 con SP1 y Servicios de Certificate Server.
  
-   Como introducción a los conceptos de infraestructura de claves públicas (PKI) y las características de Servicios de Certificate Server de Windows* *2000, consulte [An Introduction to the Windows 2000 Public-Key Infrastructure](http://www.microsoft.com/technet/archive/windows2000serv/evaluate/featfunc/pkiintro.mspx) en http://www.microsoft.com/technet/archive/windows2000serv/evaluate/featfunc/pkiintro.mspx.
  
-   Para obtener información más detallada acerca de la funcionalidad mejorada de la infraestructura de claves públicas en Windows* *Server* *2003 y Windows* *XP, consulte "[PKI Enhancements in Windows XP Professional and Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx)", en http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx.
  
-   Para obtener más información acerca de los principales conceptos relacionados con las infraestructuras de claves públicas, consulte la página de [Infraestructura de claves públicas](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/32aacfe8-83af-4676-a45c-75483545a978.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/  
    ServerHelp/32aacfe8-83af-4676-a45c-75483545a978.mspx.
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
