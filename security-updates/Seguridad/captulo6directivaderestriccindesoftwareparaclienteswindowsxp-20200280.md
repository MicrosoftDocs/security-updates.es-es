---
TOCTitle: 'Capítulo 6: Directiva de restricción de software para clientes Windows XP'
Title: 'Capítulo 6: Directiva de restricción de software para clientes Windows XP'
ms:assetid: '548c007a-7c26-44fd-8723-563a1f72f21e'
ms:contentKeyID: 20200280
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163080(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 6: Directiva de restricción de software para clientes Windows XP

Actualizado: 20/10/05

### En esta página

[](#eeaa)[Información general](#eeaa)
[](#edaa)[Arquitectura de la directiva de restricción de software](#edaa)
[](#ecaa)[Opciones de las directivas de restricción de software](#ecaa)
[](#ebaa)[Diseño e implementación de directivas de restricción de software](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

La directiva de restricción de software proporciona a los administradores un mecanismo para identificar software y controlar su capacidad de ejecutarse en los equipos locales. Esta herramienta puede ser útil para proteger los equipos que ejecutan Microsoft® Windows® XP Profesional de conflictos conocidos y de software malintencionado, como virus y caballos de Troya. La directiva de restricción de software se integra totalmente con el servicio de directorio de Active Directory® y la directiva de grupo. Asimismo, se puede utilizar en equipos independientes.

La estructura de este capítulo es distinta de la de los capítulos anteriores debido a cómo funciona la directiva de restricción de software. En los capítulos anteriores se han proporcionado recomendaciones sobre cómo configurar las opciones de configuración de la directiva de grupo. La directiva de restricción de software requiere que un administrador defina las aplicaciones que pueden ejecutarse en los equipos cliente del entorno y que posteriormente determine las restricciones que aplicará la directiva a los clientes.

La primera decisión que deberá tomar cuando implemente la directiva de restricción de software es si el nivel de seguridad predeterminado será **Irrestricto** o **No permitido**. Si el nivel de seguridad predeterminado es **Irrestricto**, todo el software podrá ejecutarse y tendrá que configurar reglas adicionales para bloquear aplicaciones específicas. El enfoque más seguro es configurar el nivel en **No permitido**, que significa que no se podrá ejecutar ningún software y que se tendrán que configurar posteriormente reglas adicionales para permitir la ejecución de aplicaciones específicas. Puede aplicar la directiva de restricción de software a varios equipos mediante directivas de grupo basadas en el dominio o a equipos individuales a través de la directiva de grupo local.

**Importante**: es importante que pruebe minuciosamente todas las configuraciones de directiva descritas en esta guía antes de implementarlas en los sistemas de producción, especialmente la configuración de la directiva de restricción de software. Los errores en el diseño o la implementación de esta característica pueden causar importante frustración en los usuarios.

La directiva de restricción de software ofrece una serie de mecanismos para identificar el software, así como una infraestructura basada en directivas para aplicar reglas acerca de cómo se puede ejecutar el software identificado. Los usuarios deben cumplir las instrucciones que el administrador haya establecido en la directiva de restricción de software para el entorno.

Puede utilizar la directiva de restricción de software para realizar lo siguiente:

-   Controlar el software que se puede ejecutar en los equipos cliente del entorno.

-   Restringir el acceso de los usuarios a archivos específicos de equipos multiusuario.

-   Decidir qué usuarios pueden agregar editores de confianza a los equipos cliente.

-   Definir si las directivas afectan a todos los usuarios o a un subconjunto de usuarios de los equipos cliente.

-   Impedir la ejecución de archivos ejecutables en los equipos locales según las directivas establecidas en el nivel de equipo, unidad organizativa, sitio o dominio.

[](#mainsection)[Principio de la página](#mainsection)

### Arquitectura de la directiva de restricción de software

La directiva de restricción de software ofrece estas eficaces características:

-   **Obligatoriedad de la directiva, que puede ser para todo el dominio o para un equipo local**. Los administradores crean la directiva y, a continuación, definen las aplicaciones que son de confianza y las que no. La directiva se aplica en el tiempo de ejecución y los usuarios no reciben mensajes en los que se les permite elegir si ejecutar los archivos ejecutables.

-   **Directiva aplicable a mucho más que a sólo archivos binarios ejecutables**. La definición de lo que constituye software es ambigua. La directiva de restricción de software proporciona control sobre Microsoft Visual Basic® Scripting Edition (VBScript), JScript® y otros lenguajes de secuencias de comandos. También se integra con la característica Windows Installer para aportar control sobre los paquetes que se pueden instalar en los equipos cliente. Esta característica incluye una interfaz de programación de aplicaciones (API) que puede utilizar para coordinar el tiempo de ejecución de la directiva con otros tiempos de ejecución.

-   **Directiva que es escalable**. La directiva de restricción de software, al implementarse mediante la directiva de grupo, puede implementarse y administrarse de una forma eficaz en dominios que constan de decenas de miles de equipos.

-   **Directiva que es flexible**. Los administradores cuentan con flexibilidad para prohibir la ejecución de secuencias de comandos no autorizadas, regular los controles Microsoft ActiveX® o bloquear estrictamente equipos cliente.

-   **Directiva que permite una criptografía segura para identificar software**. La directiva de restricción de software puede identificar software mediante código hash o firmas digitales.

La implementación de la directiva de restricción de software incluye tres fases:

1.  El administrador o una autoridad delegada crea la directiva con el complemento Directiva de grupo de Microsoft Management Console (MMC) para el sitio contenedor, dominio o unidad organizativa de Active Directory. Microsoft recomienda crear un objeto de directiva de grupo (GPO) independiente para la directiva de restricción de software.

    **Nota**: para crear una nueva directiva de restricción de software destinada a un equipo independiente local, deberá ser miembro del grupo **Administradores** en el equipo local. Para configurar estos parámetros de directiva, haga clic en **Configuración de Windows**, **Configuración de seguridad** y, a continuación, en **Software Restriction Policy**.

2.  La directiva de nivel de equipo se descarga y se aplica después de iniciar el equipo. Las directivas de usuario tienen efecto cuando el usuario inicia sesión en el sistema o dominio. Para actualizar la directiva, ejecute el comando **gpupdate.exe /force.**

3.  Cuando un usuario inicia un archivo ejecutable, como una aplicación o secuencia de comandos, la directiva determina si puede ejecutarse según sus reglas de prioridad.

### Configuraciones Irrestricto y No permitido

La directiva de restricción de software consta de dos partes:

-   Una regla predeterminada que especifica los programas que pueden ejecutarse.

-   Un inventario de excepciones a la regla predeterminada.

Puede establecer la regla predeterminada usada para identificar el software en **Irrestricto** o **No permitido**, que permitirá ejecutar o no todo el software, respectivamente.

Si la regla predeterminada se establece en **Irrestricto**, el administrador puede definir excepciones o un conjunto de programas que no tienen permiso de ejecución. Utilice la configuración predeterminada **Irrestricto** en un entorno con equipos cliente escasamente administrados. Por ejemplo, para impedir que los usuarios instalen un programa que ocasionará conflictos con los programas existentes puede crear una regla para bloquearlo.

Un enfoque más seguro consiste en establecer la regla predeterminada en **No permitido** y, a continuación, permitir que sólo se pueda ejecutar un conjunto de programas determinado. Con la configuración predeterminada **No permitido**, el administrador tiene que definir todas las reglas para cada aplicación y asegurarse de que los usuarios tienen la configuración de directiva de seguridad correcta en sus equipos para poder tener acceso a las aplicaciones que pueden ejecutar. La configuración predeterminada **No permitido** es el enfoque más seguro para las organizaciones que desean proteger los equipos cliente Windows XP.

### Cuatro reglas para identificar el software

Las reglas en una directiva de restricción de software identifican una o varias aplicaciones y especifican si tienen o no permiso para ejecutarse. El motor de aplicación de Windows XP consulta las reglas de la directiva antes de permitir la ejecución de aplicaciones. Para crear una regla, debe identificar las aplicaciones y luego clasificarlas como excepciones con la configuración predeterminada **No permitido.** Cada regla puede incluir comentarios que describan su finalidad.

La directiva de restricción de software sigue estas cuatro reglas para identificar el software:

-   **Regla hash:** utiliza una huella digital cifrada del archivo ejecutable.

-   **Regla de certificado:** emplea un certificado firmado digitalmente de un editor de software para el archivo .exe.

-   **Regla de ruta:** utiliza la convención de nomenclatura universal (UNC) local o ruta del Registro de la ubicación del archivo .exe.

-   **Regla de zona:** usa la zona de Internet en la que se originó el archivo ejecutable (si se descargó con Microsoft Internet Explorer).

### La regla hash

El hash es una huella digital que identifica de forma exclusiva un programa de software o un archivo ejecutable, incluso cuando se ha movido o cambiado de nombre. Los administradores pueden utilizar un hash para realizar el seguimiento de una versión específica de un archivo ejecutable o programa que puede que no deseen que ejecuten los usuarios.

Con una regla hash, los programas de software permanecen identificados de forma exclusiva, ya que la coincidencia de esta regla se basa en un cálculo cifrado del contenido del archivo. Los únicos tipos de archivo que se ven afectados por las reglas hash son aquellos que aparecen enumerados en la sección **Tipos de archivo designados** del panel de detalles de **Directivas de restricción de software**.

Las reglas hash funcionan de forma eficaz en un entorno estático. Si el software del entorno se actualiza, el hash se tiene que volver a calcular para cada archivo ejecutable actualizado. Las reglas hash funcionan muy bien en entornos en los que se realizan cambios o actualizaciones de software con poca frecuencia.

Una regla hash se compone de los siguientes tres datos, separados por dos puntos:

-   El valor hash MD5 o SHA-1

-   La longitud del archivo

-   El número de Id. del algoritmo hash

Los archivos firmados digitalmente utilizan el valor hash contenido en la firma, que puede ser MD5 o SHA -1. Los archivos ejecutables que no tienen firma digital utilizan un valor hash MD5.

El formato de las reglas hash es el siguiente:

\[valor hash MD5 o SHA1\]:\[longitud del archivo\]:\[Id. del algoritmo hash\]

El siguiente ejemplo de regla hash es para un archivo de 126 bytes con un contenido que corresponde al valor hash MD5 (7bc04acc0d6480af862d22d724c3b049) y al algoritmo hash (indicado por el identificador de algoritmo hash 32771):

7bc04acc0d6480af862d22d724c3b049:126:32771

Cada archivo que el administrador desea restringir o permitir necesita contener una regla hash. Cuando se actualiza el software, el administrador debe crear una nueva regla hash para cada aplicación, ya que los valores hash de los archivos ejecutables originales no coincidirán con los de los archivos nuevos.

Realice los pasos del siguiente procedimiento para crear una regla hash para un archivo ejecutable.

**Para crear una regla hash para un archivo ejecutable existente**

1.  En la barra de herramientas de Editor de objetos de directiva de grupo, haga clic en **Configuración de Windows**, **Configuración de seguridad**, **Software Restriction Policy** y, a continuación, haga clic con el botón secundario del mouse en **Reglas adicionales**.

2.  Haga clic en **Regla de nuevo hash** en el menú contextual.

    [![](images/Cc163080.XPSG0601(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163080.xpsg0601_big(es-es,technet.10).gif)

    **Figure 6.1 Cuadro de diálogo Regla de nuevo hash**

3.  Haga clic en **Examinar** para seleccionar el archivo para el que desea crear una regla hash. En este ejemplo, el archivo ejecutable es **Excel.exe**. El nuevo valor hash del archivo aparece en el cuadro **Hash de archivo**, y la versión de la aplicación se muestra en el cuadro **Información del archivo**.

4.  Seleccione la configuración predeterminada del nivel de seguridad que desea para esta regla. Las opciones son:

    -   **No permitido**

    -   **Irrestricto**

### La regla de certificado

Una regla de certificado especifica que debe existir un certificado del editor de software (usado para la firma con código) para que se permita la ejecución de un programa. Por ejemplo, el administrador puede exigir certificados firmados para todas las secuencias de comandos y controles ActiveX. Entre las fuentes permitidas que cumplen con la regla de certificado se incluyen:

-   Una entidad emisora de certificados (CA) comercial, como VeriSign.

-   Una infraestructura de claves públicas (PKI) de Microsoft Windows 2000 o Windows Server™ 2003.

-   Un certificado con firma automática.

Una regla de certificado constituye un método seguro de identificación de software, ya que utiliza valores hash firmados incluidos en la firma del archivo para hacer coincidir los archivos sin tener en cuenta el nombre o la ubicación. Desgraciadamente, son muy pocos los proveedores de software que usan la tecnología de firma con código y, aquellos que lo hacen, normalmente firman un reducido porcentaje de los archivos ejecutables que distribuyen. Por estos motivos, las reglas de certificado se usan normalmente para algunos tipos de aplicaciones específicas, como los controles ActiveX o las aplicaciones desarrolladas internamente. Por ejemplo, en esta guía se recomienda que las organizaciones firmen digitalmente las secuencias de comandos utilizadas para administrar los equipos y usuarios con el fin de poder bloquear todas aquellas sin firmar. Una regla hash se puede utilizar para identificar las excepciones a una regla de certificado.

### Habilitación de reglas de certificado

Las reglas de certificado no se habilitan de forma predeterminada. Siga los pasos del siguiente procedimiento para habilitar las reglas de certificado.

**Para habilitar las reglas de certificado**

1.  Abra el GPO en Editor de objetos de directiva de grupo.

2.  En el árbol de consola, haga clic en **Opciones de seguridad**.

3.  En el panel de detalles, haga doble clic en **Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software**.

4.  Haga clic en **Habilitado** para que estén disponibles las reglas de certificado.

Para obtener instrucciones detalladas acerca de cómo firmar digitalmente archivos, consulte la sección “Step-by-Step Guide to Digitally Signing Files with Test Certificates” de "[Using Software Restriction Policies to Protect Against Unauthorized Software](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx (en inglés).

Muchos de los sitios web comerciales cuentan con su propio software firmado con código por una entidad de certificación (CA) comercial. Normalmente, la validez de estos certificados es de uno a varios años. Al utilizar reglas de certificado, tenga en cuenta que los certificados tienen una fecha de caducidad. Puede ponerse en contacto con el editor del software para obtener más información sobre el período de caducidad del certificado publicado. Cuando reciba un certificado de una entidad de certificación comercial, puede exportarlo a un archivo para crear una regla de certificado. Siga los pasos del siguiente procedimiento para exportar un certificado.

**Para exportar un certificado**

1.  Seleccione el editor de confianza que emitirá el certificado. En este ejemplo, el editor del certificado es Microsoft MSN®.

    [![](images/Cc163080.XPSG0602(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0602_big(es-es,technet.10).jpg)

    **Figura 6.2 Cuadro de diálogo Advertencia de seguridad que muestra el editor de confianza**

2.  Haga clic en la ficha **Detalles** y, a continuación, en **Copiar en archivo...** para copiar el certificado en un archivo y utilizarlo para crear una regla de certificado.

    [![](images/Cc163080.XPSG0603(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0603_big(es-es,technet.10).jpg)

    **Figura 6.3 Ficha Detalles del cuadro de diálogo Certificado**

3.  Aparece la página de presentación del **Asistente para exportación de certificados**. Haga clic en **Siguiente** para continuar.

    [![](images/Cc163080.XPSG0604(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0604_big(es-es,technet.10).jpg)

    **Figura 6.4 Página de presentación del Asistente para exportación de certificados**

4.  En la página **Formato de archivo de exportación**, seleccione **DER binario codificado X.509 (.CER)** y haga clic en **Siguiente** para crear el archivo del certificado con la extensión (.cer).

    [![](images/Cc163080.XPSG0605(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0605_big(es-es,technet.10).jpg)

    **Figure 6.5 Página Formato de archivo de exportación del Asistente para exportación de certificados que muestra el método de codificación seleccionado**

5.  En la página **Archivo para exportar**, indique un nombre descriptivo para el archivo de la regla de certificado. El certificado se guardará en cualquier ubicación que seleccione con el nombre de archivo elegido.

    [![](images/Cc163080.XPSG0606(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0606_big(es-es,technet.10).jpg)

    **Figure 6.6 Página Archivo para exportar del Asistente para exportación de certificados que muestra un ejemplo de nombre de archivo**

6.  La página **Finalización del Asistente para exportación de certificados** mostrará la configuración especificada del archivo de certificado. Revise la configuración y haga clic en **Finalizar** para exportar el archivo.

    [![](images/Cc163080.XPSG0607(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0607_big(es-es,technet.10).jpg)

    **Figure 6.5 Página Finalización del Asistente para exportación de certificados que muestra la configuración especificada**

### La regla de ruta

Esta regla especifica una carpeta o una ruta de acceso completa a un programa. Cuando la regla de ruta especifica una carpeta, hace coincidir cualquier programa contenido en dicha carpeta y todos los programas incluidos en subcarpetas de esa carpeta. Las reglas de ruta admiten tanto rutas locales como UNC.

El administrador debe definir todos los directorios desde los que se iniciará una aplicación determinada en la regla de ruta. Por ejemplo, si un acceso directo del escritorio se utiliza para iniciar una aplicación, la regla de ruta debe especificar las rutas del archivo ejecutable y del acceso directo para ejecutar la aplicación. Si un usuario intenta ejecutar una aplicación con sólo una regla de ruta parcial, aparecerá la advertencia de **software restringido**.

Un gran número de aplicaciones utilizan la variable %*ProgramFiles*% para instalar los archivos en el disco duro de los equipos basados en Windows XP. Desafortunadamente, algunas aplicaciones están codificadas de forma rígida para copiar los archivos en el subdirectorio **C:\\Archivos de programa** y lo harán aquí aunque esta variable se establezca en otro directorio de una unidad distinta. Recuerde esta limitación al crear y probar las reglas de ruta.

### Uso de variables de entorno en las reglas de ruta

Se puede definir una regla de ruta de modo que utilice variables de entorno. Puesto que las reglas de ruta se evalúan en el entorno del cliente, las variables de entorno permiten al administrador adaptar una regla al entorno de un usuario determinado.

Los siguientes dos ejemplos muestran formas de cómo aplicar las variables de entorno a una regla de ruta.

-   “%UserProfile%” corresponde a **C:\\Documents and Settings\\*&lt;Usuario&gt;**** *y todas las subcarpetas de este directorio.

-   “%ProgramFiles%\\*&lt;Aplicación&gt;*”* *corresponde a **C:\\Program Files\\*&lt;Aplicación&gt;*** y todas las subcarpetas de este directorio.

    **Nota:** las variables de entorno no están protegidas mediante listas de control de acceso (ACL). Existen dos tipos de variables de entorno, **User** y **System**. Los usuarios que pueden iniciar el símbolo del sistema tienen la posibilidad de volver a definir la variable de entorno **Users** en una ruta distinta. Sin embargo, sólo los usuarios del grupo **Administradores** pueden modificar la variable de entorno **System**.

Aunque los dos ejemplos anteriores son muy útiles, es posible que desee considerar otras variables de entorno disponibles. Para ver una lista completa, consulte la página de [introducción al shell de comandos](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/ntcmds_shelloverview.mspx) en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/
en-us/ntcmds\_shelloverview.mspx (en inglés).

#### Uso de comodines en las reglas de ruta

Las reglas de ruta pueden incorporar los comodines "?" y "\*". En los siguientes ejemplos se muestran los comodines aplicados a distintas reglas de ruta:

-   **\\\\DC – ??\\login$** indica **\\\\DC – 01\\login$**, **\\\\DC – 02\\login$**, etc.

-   **\*\\Windows** indica **C:\\Windows**, **D:\\Windows**, **E:\\Windows** y todas las subcarpetas de cada directorio.

-   **C:\\win\*** indica **C:\\winnt**, **C:\\windows**, **C:\\windir** y todas las subcarpetas de cada directorio.

-   **\*.vbs** indica cualquier aplicación que tenga esta extensión en Windows XP Professional.

-   **C:\\Archivos de aplicación\\\*.\*** indica todos los archivos de aplicaciones del subdirectorio específico.

#### Reglas de ruta del Registro

Un gran número de aplicaciones almacenan las rutas a sus carpetas de instalación o directorios de aplicaciones en el Registro de Microsoft Windows. Algunas aplicaciones se pueden instalar en cualquier parte del sistema de archivos. Para localizarlas, puede crear una regla de ruta que busque estas claves del Registro.

Puede que estas ubicaciones no se identifiquen fácilmente con rutas de carpeta específicas, como **C:\\Archivos de programa\\Microsoft Platform SDK**, o variables de entorno, como **%ProgramFiles%\\Microsoft Platform SDK**. Sin embargo, si el programa almacena sus directorios de aplicaciones en el Registro, podrá crear una regla de ruta que utilice el valor almacenado en el mismo, como por ejemplo:

**%HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\PlatformSDK\\Directories\\**
**Install Dir%**

Este tipo de regla de ruta, denominado regla de ruta del Registro, presenta el formato siguiente:

%*&lt;Subárbol del Registro&gt;*\\*&lt;Nombre de la clave del Registro&gt;*\\*&lt;Nombre de valor&gt;*%

**Nota:** cualquier sufijo de la regla de ruta del Registro no debe contener un carácter \\ inmediatamente después del último signo % en la regla. El nombre del subárbol del Registro debe escribirse completo; las abreviaturas no sirven.

Cuando la regla predeterminada se establece como **No permitido**, se configuran cuatro reglas de ruta de acceso al Registro de forma que el sistema operativo tenga acceso a los archivos del sistema. Estas reglas de ruta del Registro se crean como salvaguarda para evitar que uno mismo o los demás usuarios puedan bloquear el sistema y se establecen como **Irrestricto**. Estas reglas sólo las deben modificar o eliminar usuarios expertos. Las configuraciones de las reglas de ruta del Registro son:

-   %HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\
    CurrentVersion\\SystemRoot%

-   %HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\
    CurrentVersion\\SystemRoot%\\\*.exe

-   %HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\
    CurrentVersion\\SystemRoot%\\System32\\\*.exe

-   %HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\
    CurrentVersion\\ProgramFilesDir%

#### Prioridad en las reglas de ruta

Cuando hay varias reglas de ruta que coinciden, la regla que sea más específica tendrá prioridad sobre las demás. El siguiente conjunto de rutas se ha ordenado de mayor (coincidencia más específica) a menor prioridad (coincidencia más general):

-   Unidad:\\Carpeta1\\Carpeta2\\NombreArchivo.Extensión

-   Unidad:\\Carpeta1\\Carpeta2\\\*.Extensión

-   \*.Extensión

-   Unidad:\\Carpeta1\\Carpeta2\\

-   Unidad:\\Carpeta1\\

### La regla de zona

La regla de zona se puede utilizar para identificar software descargado desde cualquiera de las zonas siguientes definidas en Internet Explorer:

-   Internet

-   Intranet

-   Sitios restringidos

-   Sitios de confianza

-   Mi PC

La versión actual de la regla de zona de Internet se aplica sólo a los paquetes de Windows Installer (\*.msi). Además, no se aplica a software descargado a través de Internet Explorer. Los demás tipos de archivo afectados por reglas de zona se muestran en la tabla de tipos de archivos designados que aparece más adelante en este capítulo. Una lista de tipos de archivos designados se comparte entre todas las reglas de zona.

### Recomendaciones sobre las reglas

Utilice la información de la siguiente tabla para determinar el tipo de regla que mejor se adapta al entorno y a los usuarios de una aplicación.

**Tabla 6.1 Determinación de la mejor regla para una aplicación específica**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tarea</th>
<th style="border:1px solid black;" >Regla recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir o no permitir una versión de programa específica.</td>
<td style="border:1px solid black;"><strong>Regla hash</strong><br />
Buscar el archivo para crear una regla hash.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Identificar un programa instalado siempre en el mismo lugar.</td>
<td style="border:1px solid black;"><strong>Regla de ruta con variables de entorno</strong><br />
%ProgramFiles%\Internet Explorer\iexplore.exe</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Identificar un programa que se puede instalar en cualquier lugar de los equipos cliente.</td>
<td style="border:1px solid black;"><strong>Regla de ruta del Registro</strong><br />
%HKEY_LOCAL_MACHINE\SOFTWARE\ ComputerAssociates\InoculateIT\6.0\Path\HOME%</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Identificar un conjunto de secuencias de comandos en un servidor central.</td>
<td style="border:1px solid black;"><strong>Regla de ruta</strong><br />
\\SERVER_NAME\Share</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Identificar un conjunto de secuencias de comandos en un conjunto de servidores. Por ejemplo, DC01, DC02 y DC03.</td>
<td style="border:1px solid black;"><strong>Regla de ruta con comodín</strong><br />
\\DC??\Share</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir ningún archivo .vbs, excepto aquellos que estén en un directorio de secuencias de comandos de inicio.</td>
<td style="border:1px solid black;"><strong>Regla de ruta con comodín</strong>
*.VBS establecido como <strong>No permitido</strong>
\\LOGIN_SRV\Share\*.VBS establecido como <strong>Irrestricto</strong></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">No permitir un archivo instalado por un virus que se llama siempre Flcss.exe.</td>
<td style="border:1px solid black;"><strong>Regla de ruta</strong>
Flcss.exe establecido como <strong>No permitido</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Identificar un conjunto de secuencias de comandos que se pueden ejecutar en cualquier lugar.</td>
<td style="border:1px solid black;"><strong>Regla de certificado</strong>
Utilizar un certificado para firmar digitalmente las secuencias de comandos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir que se instale software desde cualquier sito de la zona de Internet de confianza.</td>
<td style="border:1px solid black;"><strong>Regla de zona</strong>
Establecer <strong>Sitios de confianza</strong> como <strong>Irrestricto</strong>.</td>
</tr>
</tbody>
</table>
 

#### Reglas de prioridad para las directivas de restricción de software

Las reglas se evalúan siguiendo un orden concreto. Las reglas que coinciden más específicamente con un programa tienen prioridad sobre aquellas que coinciden de forma más general con dicho programa. Si se establecen dos reglas idénticas con distintos niveles de seguridad para el mismo software, tendrá prioridad la regla con el nivel de seguridad más alto. Por ejemplo, si dos reglas hash, una con el nivel de seguridad **No permitido** y otra con el nivel **Irrestricto**, se aplican al mismo programa de software, tendrá prioridad la regla con el nivel de seguridad **No permitido** y el programa no se ejecutará. La siguiente lista define el orden de prioridad de las reglas desde la más a la menos específica:

1.  Regla hash

2.  Regla de certificado

3.  Regla de ruta

4.  Regla de zona

5.  Regla predeterminada

[](#mainsection)[Principio de la página](#mainsection)

### Opciones de las directivas de restricción de software

En esta sección se explican las distintas opciones de obligatoriedad que influyen en cómo funciona una directiva de restricción de software. Estas opciones alteran la forma en que se aplica la configuración de confianza de Microsoft Authenticode® para los archivos firmados digitalmente. Existen dos opciones de obligatoriedad: la comprobación de bibliotecas de vínculos dinámicos (DLL) y la omisión de administradores.

### Comprobación de DLL

La mayoría de los programas están formados por un archivo ejecutable y un gran número de DLL compatibles. De forma predeterminada, las reglas de la directiva de restricción de software no se aplican a las DLL. Ésta es la configuración predeterminada recomendada para la mayoría de los clientes por estas tres razones:

-   Si no se permite la ejecución del archivo ejecutable principal, el programa no se ejecuta y, por tanto, no es necesario no permitir las DLL que lo constituyen.

-   La comprobación de DLL disminuye el rendimiento del sistema debido a que es preciso comprobar todas las bibliotecas vinculadas a la aplicación. Por ejemplo, si un usuario ejecuta 10 programas durante una sesión de inicio, la directiva de restricción de software evalúa cada uno de los programas. Si se tiene activada la comprobación de DLL, la directiva de restricción de software evalúa cada DLL cargada dentro de cada programa. Si cada programa utiliza 20 DLL, esta configuración exigirá realizar 10 comprobaciones de programas ejecutables más 200 comprobaciones de DLL, con lo cual, la directiva de restricción de software deberá realizar 210 evaluaciones.

    Un programa como Internet Explorer está formado por un archivo ejecutable (iexplore.exe) y muchas DLL compatibles.

-   Si se establece el nivel de seguridad predeterminado como **No permitido**, el sistema no sólo se ve obligado a identificar el archivo ejecutable principal antes de que se permita su ejecución, sino también todas las DLL constituyentes del archivo .exe, lo que supone una carga adicional para el sistema.

Aunque los virus atacan principalmente a los archivos ejecutables, algunos lo hacen específicamente a las DLL. Por tanto, la comprobación de DLL es la opción recomendada si desea el máximo grado de seguridad posible para los programas que se ejecutan en su entorno.

Para asegurarse de que un programa no contiene virus, puede utilizar un conjunto de reglas hash que identifiquen el archivo ejecutable y todas sus DLL constituyentes.

**Para desactivar la opción de comprobación de DLL:**

-   Al editar un directiva de restricción de software, en el cuadro de diálogo **Propiedades de Obligatoriedad**, seleccione **Todos los archivos de software excepto bibliotecas (tales como DLLs)** como se muestra en la siguiente figura:

    [![](images/Cc163080.XPSG0608(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0608_big(es-es,technet.10).jpg)

    **Figura 6.8 Cuadro de diálogo Propiedades de Obligatoriedad que muestra las opciones de obligatoriedad de archivos y usuarios**

#### Omisión de administradores

Es posible que desee prohibir la ejecución de programas para la mayoría de los usuarios, pero permitir a los administradores que los ejecuten todos. Por ejemplo, existe la posibilidad de que un administrador tenga un equipo compartido al que se conecten varios usuarios con Terminal Server. El administrador podría querer que los usuarios sólo ejecutaran determinadas aplicaciones en el equipo, pero que los miembros del grupo **Administradores** local tuviesen la posibilidad de ejecutar todo. Para ello, deberá utilizar la opción de obligatoriedad de **omisión de administradores**.

Si la directiva de restricción de software se crea en un GPO vinculado a un objeto en Active Directory, Microsoft recomienda denegar el permiso **Aplicar directiva de grupos** en el GPO para el grupo **Administradores** y no usar la opción de **omisión de administradores**. Con este método se consume menos ancho de banda de red, ya que no se descargará la configuración de GPO no aplicable a los administradores.

**Nota**: la directiva de restricción de software definida en objetos de directiva de seguridad local no puede filtrar los grupos de usuarios y, por tanto, requerirá que se utilice la opción de **omisión de administradores**.

**Para activar la opción de omisión de administradores**

-   En el cuadro de diálogo **Propiedades de Obligatoriedad** (mostrado en la figura 6.8), seleccione **Todos los usuarios excepto los administradores locales**.

### Definición de ejecutables

El cuadro de diálogo **Propiedades de Tipos de archivo designados** de la siguiente figura muestra los tipos de archivo que se rigen por la directiva de restricción de software. Estos tipos de archivo se consideran archivos ejecutables. Por ejemplo, un archivo protector de pantalla (.scr), se considera un archivo ejecutable porque se carga como un programa cuando se hace doble clic en él desde el Explorador de Windows.

Las reglas de la directiva de restricción de software sólo se aplican a los tipos de archivo que aparecen en el cuadro de diálogo **Propiedades de Tipos de archivo designados**. Si en su entorno hay un tipo de archivo al que desea aplicar reglas, agréguelo a la lista. Por ejemplo, para archivos de secuencias de comandos Perl, puede elegir agregar .pl y otros tipos de archivo asociados con el motor Perl a la lista **Tipos de archivo designados** de la ficha **General** del cuadro de diálogo **Propiedades de Tipos de archivo designados**.

[![](images/Cc163080.XPSG0609(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0609_big(es-es,technet.10).jpg)

**Figura 6.9 Cuadro de diálogo Propiedades de Tipos de archivo designados**

Para el diseño de GPO que se define en esta guía, se quitan los tipos de archivo .mdb y .lnk y se agrega el tipo de archivo .ocx. En la tabla siguiente se muestran los tipos de archivo designados.

**Tabla 6.2 Tipos de archivo designados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Extensión del archivo</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Extensión del archivo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">.ade</td>
<td style="border:1px solid black;">Extensión de proyectos de Microsoft Access</td>
<td style="border:1px solid black;">.msc</td>
<td style="border:1px solid black;">Documento de la consola común de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.adp</td>
<td style="border:1px solid black;">Proyecto de Microsoft Access</td>
<td style="border:1px solid black;">.msi</td>
<td style="border:1px solid black;">Paquete de Windows Installer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.bas</td>
<td style="border:1px solid black;">Módulo de clase de Visual Basic</td>
<td style="border:1px solid black;">.msp</td>
<td style="border:1px solid black;">Revisión de Windows Installer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.bat</td>
<td style="border:1px solid black;">Archivo por lotes</td>
<td style="border:1px solid black;">.mst</td>
<td style="border:1px solid black;">Archivo de origen de prueba de Microsoft Visual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.chm</td>
<td style="border:1px solid black;">Archivo de ayuda HTML compilado</td>
<td style="border:1px solid black;">.ocx</td>
<td style="border:1px solid black;">Control ActiveX</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos de Windows NT</td>
<td style="border:1px solid black;">.pcd</td>
<td style="border:1px solid black;">Imagen de CD de fotografías</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.com</td>
<td style="border:1px solid black;">Aplicación MS-DOS</td>
<td style="border:1px solid black;">.pif</td>
<td style="border:1px solid black;">Acceso directo al programa MS-DOS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.cpl</td>
<td style="border:1px solid black;">Extensión del Panel de control</td>
<td style="border:1px solid black;">.reg</td>
<td style="border:1px solid black;">Entrada de registro</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.crt</td>
<td style="border:1px solid black;">Certificado de seguridad</td>
<td style="border:1px solid black;">.scr</td>
<td style="border:1px solid black;">Protector de pantalla</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.exe</td>
<td style="border:1px solid black;">Aplicación</td>
<td style="border:1px solid black;">.sct</td>
<td style="border:1px solid black;">Componente de secuencia de comandos de Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.hlp</td>
<td style="border:1px solid black;">Archivo de ayuda de Windows</td>
<td style="border:1px solid black;">.shs</td>
<td style="border:1px solid black;">Objeto de recorte de Shell</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.hta</td>
<td style="border:1px solid black;">Aplicación HTML</td>
<td style="border:1px solid black;">.url</td>
<td style="border:1px solid black;">Acceso directo a Internet (Uniform Resource Locator)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.inf</td>
<td style="border:1px solid black;">Archivo de información de instalación</td>
<td style="border:1px solid black;">.vb</td>
<td style="border:1px solid black;">Archivo de Visual Basic</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.ins</td>
<td style="border:1px solid black;">Configuración de comunicaciones de Internet</td>
<td style="border:1px solid black;">.vbe</td>
<td style="border:1px solid black;">Archivo de secuencia de comandos codificado de VBScript</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.isp</td>
<td style="border:1px solid black;">Configuración de comunicaciones de Internet</td>
<td style="border:1px solid black;">.vbs</td>
<td style="border:1px solid black;">Archivo de secuencia de comandos de VBScript</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.js</td>
<td style="border:1px solid black;">Archivo JScript</td>
<td style="border:1px solid black;">.wsc</td>
<td style="border:1px solid black;">Componente de secuencia de comandos de Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">.jse</td>
<td style="border:1px solid black;">Archivo de secuencia de comandos codificado de JScript</td>
<td style="border:1px solid black;">.wsf</td>
<td style="border:1px solid black;">Archivo de secuencia de comandos de Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">.mde</td>
<td style="border:1px solid black;">Base de datos MDE de Microsoft Access</td>
<td style="border:1px solid black;">.wsh</td>
<td style="border:1px solid black;">Archivo de configuración de Windows Scripting Host</td>
</tr>
</tbody>
</table>
  
### Editores de confianza
  
Puede utilizar el cuadro de diálogo **Propiedades de Editores de confianza** para configurar qué usuarios pueden seleccionar editores de confianza. También puede determinar qué comprobaciones de revocación de certificado, si las hubiese, se deben realizar antes de confiar en un editor. Con las reglas de certificado habilitadas, la directiva de restricción de software comprobará una lista de revocación de certificados (CRL) para asegurarse de que el certificado y la firma del software son válidos. Sin embargo, este proceso puede disminuir el rendimiento al iniciar programas firmados.
  
Las opciones de la ficha **General** del cuadro de diálogo **Propiedades de Editores de confianza** que se muestran en la siguiente figura permiten configurar los parámetros relacionados con los controles ActiveX y otro contenido firmado.
  
[![](images/Cc163080.XPSG0610(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163080.xpsg0610_big(es-es,technet.10).jpg)
  
**Figure 6.1 Cuadro de diálogo Propiedades de Editores de confianza**
  
La siguiente tabla muestra las opciones de editores de confianza relacionadas con controles ActiveX y otro contenido firmado.
  
**Tabla 6.3 Configuración y tareas de los editores de confianza**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la configuración</th>
<th style="border:1px solid black;" >Tarea</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administradores de organización</td>
<td style="border:1px solid black;">Utilizar para permitir que sólo los administradores de organización tomen decisiones sobre el contenido activo firmado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administradores de equipo local</td>
<td style="border:1px solid black;">Utilizar para permitir que los administradores de equipos locales tomen todas las decisiones sobre el contenido activo firmado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Usuarios finales</td>
<td style="border:1px solid black;">Utilizar para permitir que los usuarios tomen decisiones sobre el contenido activo firmado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Editor</td>
<td style="border:1px solid black;">Utilizar para asegurar que el certificado que utiliza el editor de software no se ha revocado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Marca de hora</td>
<td style="border:1px solid black;">Utilizar para asegurar que el certificado que utiliza la organización para marcar la hora en el contenido activo no se ha revocado.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Diseño e implementación de directivas de restricción de software
  
En esta sección se describe el proceso de administración de la directiva de restricción de software con el complemento Directiva de grupo, lo que se debe tener en cuenta al editar una directiva por primera vez y la forma de aplicar una directiva de restricción de software a un grupo de usuarios. Asimismo, se tratan distintos aspectos relacionados con la implementación de una directiva de restricción de software.
  
#### Integración con Directiva de grupo
  
Puede administrar la directiva de restricción de software utilizando el complemento Directiva de grupo tanto en un conjunto de equipos cliente, como en todos los usuarios que inician sesión en los equipos. La directiva se aplica a las unidades organizativas Equipo portátil y Escritorio definidas en esta guía.
  
#### Dominio
  
El administrador debería crear un objeto de directiva de grupo independiente para la directiva de restricción de software. Este método proporciona una forma de deshabilitar la directiva de grupo sin interrumpir las demás directivas aplicadas al objeto en caso de que surjan problemas.
  
#### Local
  
Se debe configurar una directiva local para los equipos cliente independientes del entorno como se describe en el capítulo 5, "Seguridad de clientes Windows XP independientes", de esta guía.
  
#### Diseño de una directiva
  
En esta sección se describen los pasos que deben seguirse al diseñar e implementar una directiva de restricción de software. El diseño de la directiva conlleva tomar varias decisiones, todas ellas descritas en la siguiente tabla.
  
**Tabla 6.4 Consideraciones importantes sobre el diseño de directivas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Decisión</th>
<th style="border:1px solid black;" >Factores que deben considerarse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Equipos portátiles o estaciones de trabajo</td>
<td style="border:1px solid black;">Investigar las necesidades de los usuarios móviles de su entorno para averiguar si los equipos portátiles precisan una directiva distinta a la del resto. Los equipos portátiles tienden a necesitar más flexibilidad que los de escritorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Recursos compartidos del servidor, secuencias de comandos de inicio de sesión y unidades principales</td>
<td style="border:1px solid black;">Necesitará definir una regla de ruta para todas las aplicaciones que se inicien desde un recurso compartido del servidor o un directorio principal. Puede agregar archivos de comandos de inicio de sesión a la regla de ruta. Si una secuencia de comandos llama a otra, agregue también a la regla de ruta las ubicaciones de los ejecutables.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPO o directiva de seguridad local</td>
<td style="border:1px solid black;">En esta guía se utiliza un GPO para el diseño. Sin embargo, debe considerar las repercusiones que tendrá la directiva local sobre el diseño.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Directiva de usuario o equipo</td>
<td style="border:1px solid black;">Este diseño se aplica a todas las configuraciones en el nivel de equipo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nivel de seguridad predeterminado</td>
<td style="border:1px solid black;">Se recomienda configurar el parámetro predeterminado como <strong>No permitido</strong> y después configurar el resto de la directiva de acuerdo al parámetro. La configuración predeterminada <strong>Irrestricto</strong> también está disponible.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reglas adicionales</td>
<td style="border:1px solid black;">Necesitará aplicar reglas de ruta de sistema operativo adicionales según sea necesario cuando utilice la directiva predeterminada <strong>No permitido</strong>. En la configuración <strong>No permitido</strong>, se crean automáticamente las cuatro reglas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Opciones de directiva</td>
<td style="border:1px solid black;">Si utiliza una directiva de seguridad local y no desea que la directiva se aplique a los administradores en los equipos cliente de su entorno, seleccione la opción de obligatoriedad de directiva de <strong>omisión de administradores</strong>.
Si desea comprobar las DLL además de los archivos ejecutables y las secuencias de comandos, seleccione la opción de obligatoriedad de directiva de <strong>comprobación de DLL</strong>.
Si desea establecer reglas para tipos de archivo que no se encuentran en la lista predeterminada de tipos de archivo designados, utilice la opción para agregarlas según sea necesario en el cuadro de diálogo <strong>Propiedades de Tipos de archivo designados</strong>.
Si desea cambiar el responsable que puede tomar decisiones sobre la descarga de controles ActiveX y otro contenido firmado, active la casilla de verificación <strong>Editor</strong> en la ficha <strong>General</strong> del cuadro de diálogo <strong>Propiedades de Editores de confianza</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Aplicar la directiva a un sitio, dominio o unidad organizativa (UO)</td>
<td style="border:1px solid black;">La directiva residirá en la UO donde se ubican los equipos portátiles y de escritorio.</td>
</tr>
</tbody>
</table>
  
**Nota**: aunque en esta guía se recomienda aplicar la directiva de restricción de software en el nivel de equipo, hay muchos casos en los que tendrá sentido aplicarla en el nivel de usuario. Por ejemplo, es posible que una organización con equipos compartidos, como los servidores de aplicación de Servicios de Terminal Server o las estaciones de trabajo de un centro de llamadas, desee permitir a determinados usuarios la ejecución de un conjunto de aplicaciones, pero bloquear el acceso de otros usuarios.
  
#### Prácticas recomendables
  
Microsoft recomienda crear un GPO independiente para la directiva de restricción de software, para que si necesita deshabilitar la directiva en un caso de emergencia, no influya en el resto de la directiva local o de dominio.
  
Asimismo, si accidentalmente bloquea una estación de trabajo con la directiva de restricción de software durante la fase de diseño de la unidad organizativa, reinicie el equipo en **Modo a prueba de errores**, inicie la sesión como administrador local y, a continuación, modifique la directiva. La directiva de restricción de software no se aplica cuando Windows se inicia en **Modo a prueba de errores**. Una vez iniciado el equipo en **Modo a prueba de errores**, ejecute Gpupdate.exe y reinícielo.
  
Para lograr una seguridad óptima, utilice listas de control de acceso (ACL) junto con la directiva de restricción de software y no conceda a los usuarios privilegios administrativos. Los usuarios pueden intentar cambiar el nombre o mover archivos no permitidos o sobrescribir archivos no restringidos para omitir la directiva de restricción de software. Utilice listas ACL para denegar a los usuarios acceso para realizar alguna de estas acciones. Los usuarios que son miembros del grupo **Administradores** local podrán omitir la implementación de la directiva de restricción de software; por tanto, Microsoft recomienda no conceder privilegios administrativos a los usuarios cuando sea posible.
  
Las secuencias de comandos de inicio de sesión se ubican en SYSVOL en el controlador de dominio o en un servidor centralizado. El controlador de dominio a menudo cambia con cada inicio de sesión. Si la regla predeterminada está establecida como **No permitido**, asegúrese de crear reglas que identifiquen las ubicaciones de las secuencias de comandos de inicio de sesión. Si los servidores de inicio de sesión tienen nombres similares, considere utilizar comodines para localizarlos, o bien, incluya el nombre de la secuencia de comandos de inicio de sesión con la configuración Irrestricto.
  
**Nota**: compruebe minuciosamente la configuración de la nueva directiva de restricción de software en los entornos de prueba antes de aplicarla a su dominio. La configuración de la nueva directiva puede actuar de forma distinta a la esperada originalmente. La realización de pruebas completas reducirá la posibilidad de encontrar problemas al implementar la configuración de la directiva de restricción de software en la red.
  
#### Pasos a través del proceso
  
Utilice la información que se muestra a continuación como guía en el proceso de diseño de la directiva de restricción de software y de aplicación del diseño como un GPO a los equipos portátiles y de escritorio de su entorno.
  
#### Paso 1. Crear un objeto de directiva de grupo para la unidad organizativa
  
Localice la unidad organizativa que se ha creado para los equipos portátiles y de escritorio en su entorno. Si trabaja en un equipo cliente independiente, la configuración de directiva se ubica en la directiva de equipo local. En esta directiva, haga clic en **Propiedades** y, a continuación, cree un nuevo GPO. Asigne un nombre a la directiva de acuerdo con la convención de nomenclatura de su organización. Recuerde, esta directiva sólo se utilizará para aplicar las restricciones de software.
  
#### Paso 2. Establecer la directiva de restricción de software
  
Resalte el GPO y haga clic en **Modificar**. Recorra el árbol hasta que encuentre **Configuración de Windows\\Software Restriction Policy**. La primera vez que modifique la directiva, se le presentará el siguiente mensaje:
  
No se han definido directivas de restricción de software.
  
Este mensaje le avisa de que al crear una directiva, se definirán los valores predeterminados. Estos valores predeterminados pueden invalidar la configuración de directiva de otras directivas de restricción de software. Puesto que aún no se ha establecido ninguna configuración de la directiva de restricción de software, utilice la configuración predeterminada para empezar. Haga clic con el botón secundario en el menú **Acciones** y seleccione **Nuevas directivas de restricción de software**.
  
#### Paso 3. Configurar las reglas de ruta
  
Una vez que haya decidido las aplicaciones y secuencias de comandos que utilizarán las estaciones de trabajo, puede configurar las reglas de ruta. Algunos programas inician otros programas para realizar tareas y es posible que las aplicaciones de software de su entorno dependan de uno o más programas para otros. Para el seguimiento de las reglas de ruta resulta de gran utilidad la documentación sobre la instalación y el inventario del software actualmente instalado. Un ejemplo de diseño de estación de trabajo podría incluir las siguientes instrucciones:
  
-   Aplicaciones = \*\\Archivos de programa
  
-   Aplicaciones de grupo compartidas= g:\\Group Applications
  
-   Secuencia de comandos de inicio de sesión = Logon.bat
  
-   Accesos directos de escritorio = \*.lnk
  
-   Secuencias de comandos de VBS Script aprobadas =\*.vbs
  
#### Paso 4. Establecer las opciones de la directiva
  
Las opciones siguientes incluyen la configuración de directiva recomendada para el diseño definido en esta guía. Estas opciones alteran el ámbito del comportamiento de obligatoriedad de la configuración de confianza de Authenticode para los archivos firmados digitalmente.
  
-   **Obligatoriedad:** si el equipo forma parte del dominio, asegúrese de que el grupo **Admins. del dominio** se agrega automáticamente al grupo **Administradores**.
  
-   **Aplicar a Usuarios:** esta opción incluye a todos los usuarios, excepto a los administradores locales. Si se utiliza esta opción, se retrasará el inicio de las aplicaciones. Para compensar esta demora, el diseño configura la directiva de modo que no compruebe las DLL.
  
-   **Aplicar a Archivos:** esta opción incluye todos los archivos de software, excepto las bibliotecas (como las DLL). Si se utiliza esta opción, se retrasará el inicio de las aplicaciones. Para compensar esta demora, el diseño configura la directiva de modo que no compruebe las DLL.
  
-   **Tipos de archivo designados:** para el diseño de GPO que se define en esta guía, se quitaron los tipos de archivo .mdb y .lnk y se agregó el tipo de archivo .ocx. Puede agregar extensiones de tipo de archivo de aplicaciones personalizadas, según sea necesario, para que se sometan a las mismas reglas.
  
-   **Editores de confianza:** para el diseño de GPO definido en esta guía, se habilitó el grupo **Administradores** y se seleccionó la opción **Propiedades de Editores de confianza: Administradores de equipo local**.
  
Antes de confiar en un editor, seleccione la opción **Comprobar: Editor** cuando diseñe el GPO para asegurarse de que la directiva validará los certificados.
  
#### Paso 5. Aplicar la configuración predeterminada
  
Se recomienda configurar la directiva en el valor predeterminado **Irrestricto**. Este método garantiza que la directiva se inicializa adecuadamente antes de que se apliquen las restricciones de software. Después de revisar la configuración de la directiva, restablezca el valor predeterminado, es decir, **No permitido**.
  
#### Paso 6. Probar la directiva
  
Si el equipo forma parte de un dominio, traslade el equipo a un contenedor de la unidad organizativa en la que se aplique la directiva. Reinicie el equipo de prueba e inicie sesión en él. Los planes de prueba deberían tener instrucciones sobre la forma en que deben funcionar las aplicaciones cuando se aplique la directiva. Ejecute las aplicaciones para comprobar que su funcionalidad es completa y que puede obtener acceso a todas sus características. Una vez haya validado la funcionalidad de las aplicaciones, simule un ataque contra ellas para asegurarse de que la directiva no cuenta con puntos vulnerables en la seguridad.
  
Si el equipo es un cliente independiente, inicie sesión para probarlo y siga el plan de prueba. Una vez que haya validado las aplicaciones, vuelva a iniciar el ataque simulado para asegurarse de que la directiva no tiene puntos vulnerables en la seguridad.
  
#### Implementación de la directiva de restricción de software
  
Una vez probada a fondo la directiva, aplíquela a la unidad organizativa Equipo portátil o Escritorio de su entorno. En un equipo cliente independiente, aplíquela a la configuración de equipo local del cliente. Abra el complemento Usuarios y equipos de MMC y recorra el directorio hasta encontrar el contenedor de la unidad organizativa de los equipos portátiles y de escritorio. A continuación, cree el nuevo GPO con el Editor de objetos de directiva de grupo. Modifique las propiedades y aplique la configuración de directiva adecuada según la información de las tablas siguientes a **Software Restriction Policy** en **Configuración de Windows\\Configuración de seguridad**.
  
**Tabla 6.5 Niveles de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Regla predeterminada en la UI</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitido</td>
<td style="border:1px solid black;">No se ejecutará el software, independientemente de los derechos de acceso del usuario.</td>
<td style="border:1px solid black;">Utilizar esta regla predeterminada</td>
</tr>
</tbody>
</table>
  
**Tabla 6.6 Reglas adicionales**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Regla de ruta</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">%HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\SystemRoot%</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">%HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\SystemRoot%\*.exe</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">%HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\SystemRoot%\System32\*.exe</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">%HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\ProgramFilesDir%</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">*.vbs</td>
<td style="border:1px solid black;">No permitido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">G:\Group Applications</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Logon.bat o secuencia de comandos de inicio de sesión</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">*\Archivos de programa</td>
<td style="border:1px solid black;">Irrestricto</td>
</tr>
</tbody>
</table>
  
**Tabla 6.7 Obligatoriedad para los archivos y usuarios**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Opciones de obligatoriedad</th>
<th style="border:1px solid black;" >Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Aplicar directivas de restricción de software a:</td>
<td style="border:1px solid black;">Todos los archivos de software excepto bibliotecas (tales como DLLs).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Aplicar directivas de restricción de software a los siguientes usuarios:</td>
<td style="border:1px solid black;">Todos los usuarios excepto los administradores locales.</td>
</tr>
</tbody>
</table>
  
**Tabla 6.8 Tipos de archivo designados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipos de archivo</th>
<th style="border:1px solid black;" >Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Propiedades de Tipos de archivo designados</td>
<td style="border:1px solid black;">Quitar los tipos de archivo .mdb y .lnk, y agregar el tipo de archivo .ocx.</td>
</tr>
</tbody>
</table>
  
**Tabla 6.9 Editores de confianza**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Editores de confianza</th>
<th style="border:1px solid black;" >Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir a los siguientes usuarios seleccionar editores de confianza:</td>
<td style="border:1px solid black;"><strong>Administradores de equipo local</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Determinar si el certificado se ha revocado.</td>
<td style="border:1px solid black;">Seleccionar la opción <strong>Editor</strong>.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
La directiva de restricción de software proporciona a los administradores una forma eficaz de identificar y controlar el software de los equipos que ejecutan Windows XP Professional. Puede crear directivas para bloquear archivos de comandos malintencionados o equipos de su entorno de distintas maneras, así como para impedir la ejecución de aplicaciones. En un entorno empresarial resulta una práctica recomendable administrar la directiva de restricción de software mediante GPO y personalizar cada directiva de forma que se ajuste a las necesidades de los distintos grupos de usuarios y equipos. Microsoft recomienda no intentar administrar grupos de usuarios en un entorno independiente.
  
Si se aplica correctamente, la directiva de restricción de software mejorará la integridad y capacidad de administración de los equipos de la organización y, en última instancia, reducirá los costos de propiedad y mantenimiento de los sistemas operativos de esos equipos.
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.
  
-   Para obtener más información sobre la directiva de restricción de software, consulte el artículo sobre el [uso de directivas de restricción de software para proteger contra software no autorizado](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx) en www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx (en inglés).
  
-   Para obtener más información acerca de la directiva de grupo, consulte la página que contiene detalles sobre la [directiva de grupo de Windows 2000](http://www.microsoft.com/windows2000/techinfo/howitworks/management/grouppolwp.asp) en www.microsoft.com/windows2000/techinfo/howitworks/management/grouppolwp.asp (en inglés).
  
### Descargar
  
![](images/Cc163080.icon_exe(es-es,TechNet.10).gif)[Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
  
[](#mainsection)[Principio de la página](#mainsection)
