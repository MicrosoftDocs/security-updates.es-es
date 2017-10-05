---
TOCTitle: 'Apéndice A: Instrucciones adicionales para Windows XP Service Pack 2'
Title: 'Apéndice A: Instrucciones adicionales para Windows XP Service Pack 2'
ms:assetid: 'e0db3e64-90ab-4850-9732-70e0873421ee'
ms:contentKeyID: 20112565
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458743(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Apéndice A: Instrucciones adicionales para Windows XP Service Pack 2

Actualizado: 16/08/2004

En este apéndice se describen los cambios en las orientaciones de seguridad a partir del lanzamiento de Microsoft Windows XP Service Pack 2 (SP2) para Windows XP.

Debe estar ya familiarizado con las secciones anteriores de la *Guía de seguridad de Windows XP* antes de leer este apéndice. Se ha diseñado para complementar esas secciones y describe sólo los cambios de configuración específicos para SP2. Este apéndice no debe considerarse como un documento independiente.

##### En esta página

[](#efaa)[Información general de Windows XP SP2](#efaa)
[](#eeaa)[Cambios en la configuración de seguridad](#eeaa)
[](#edaa)[Cambios en Plantillas administrativas](#edaa)
[](#ecaa)[Parámetros de Configuración del equipo](#ecaa)
[](#ebaa)[Parámetros de Configuración de usuario](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general de Windows XP SP2

Windows XP SP2 contiene la recopilación más reciente de actualizaciones para Windows XP. Estas actualizaciones ayudan a mejorar la seguridad, la confiabilidad y la compatibilidad del sistema operativo al introducir un conjunto de tecnologías de seguridad que contribuirán a mejorar la capacidad de los equipos en los que se ejecuta Windows XP para resistir ataques malintencionados de virus y gusanos. Entre estas tecnologías se incluyen:

-   Protección de redes

-   Protección de memoria

-   Seguridad de correo electrónico mejorada

-   Exploración más segura

-   Mantenimiento mejorado del equipo

SP2 incluye numerosas mejoras relacionadas con la capacidad de administración de los servicios de seguridad. Estas mejoras permiten a los administradores implementar configuraciones de seguridad más específicas para usuarios y equipos.

Un cambio importante en SP2 es el mayor nivel de seguridad predeterminado. La mayoría de los cambios de seguridad se implementan de forma predeterminada y no requieren cambios de configuración. Aunque muchas de estas mejoras puedan dar lugar a dificultades de compatibilidad, la mejora general en la seguridad del sistema operativo suele compensarlas.

Para obtener más información acerca de los importantes cambios realizados en SP2, consulte la guía "Changes to Functionality in Microsoft Windows XP Service Pack 2" en [http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/sp2chngs.mspx.](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/sp2chngs.mspx)

[](#mainsection)[Principio de la página](#mainsection)

### Cambios en la configuración de seguridad

Los importantes cambios de configuración y directivas de Windows XP SP2 se limitan principalmente a las Plantillas administrativas de Directiva de grupo. Como consecuencia de esto, en este apéndice no se incluyen cambios recomendados para la Configuración de seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Cambios en Plantillas administrativas

Se han realizado importantes cambios en las Plantillas administrativas en Windows XP SP 2. Centenares de nuevas opciones de configuración permiten implementar un control más preciso de la experiencia de los usuarios y del entorno de seguridad. La mayor parte de este apéndice proporciona detalles acerca de las nuevas opciones de configuración en Plantillas administrativas, que le ayudarán a proporcionar un mayor nivel de seguridad en su entorno.

**Nota**: en el momento de redactar esta guía, las opciones de configuración descritas en este apéndice no tienen efecto en ningún sistema operativo distinto de Windows XP SP2. La configuración no afecta a Windows XP Service Pack 1 ni a versiones anteriores del sistema operativo.

#### Nuevas plantillas administrativas

También se ofrecen parámetros de configuración de la seguridad adicionales en archivos basados en Unicode denominados plantillas administrativas. Estos archivos contienen opciones de configuración del Registro que afectan a Windows XP y sus componentes. En Windows XP SP2 se incluyen nuevas plantillas administrativas. Estas plantillas nuevas requieren el uso de un equipo en el que se ejecute Windows XP SP2 al administrar GPO.

Las versiones más antiguas del Editor de objetos de directiva de grupo (Gpedit.exe) no son compatibles con las nuevas Plantillas administrativas. Las modificaciones de GPO nuevos o existentes deben realizarse desde un equipo en el que se ejecute Windows XP SP2. Para obtener información acerca del uso de otros sistemas operativos para administrar GPO, consulte el artículo 842933 de Microsoft Knowledge Base en [http://support.microsoft.com/?kbid=842933.](http://support.microsoft.com/?kbid=842933)

Las opciones de configuración en las nuevas Plantillas administrativas sólo afectan a equipos en los que se ejecuta Windows XP SP2; Windows XP SP1 y las versiones de sistema operativo anteriores pasarán por alto la configuración nueva. Este enfoque le permite implementar objetos GPO con la misma estructura de unidades organizativas descrita en el Capítulo 2 de la *Guía de seguridad de Windows XP* para mejorar la seguridad de todos los equipos de su entorno en los que se ejecuta Windows XP.

[](#mainsection)[Principio de la página](#mainsection)

### Parámetros de Configuración del equipo

Las siguientes secciones tratan los parámetros recomendados en Configuración del equipo del Editor de objetos de directiva de grupo. Para configurarlos, diríjase a la siguiente ubicación:

Configuración del equipo\\Plantillas administrativas

Aplique estos parámetros a través de un GPO vinculado a una unidad organizativa que contenga las cuentas del equipo en el entorno. Vincule los parámetros del equipo portátil del GPO a la unidad organizativa del mismo y los parámetros del equipo de escritorio en el GPO a la unidad organizativa, tal como se describe en el Capítulo 2 de la *Guía de seguridad de Windows XP*.

#### Internet Explorer

Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:

Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer

##### Desactivar la detección de bloqueos

**Tabla A.1: Configuración de detecciones de bloqueos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **Desactivar la detección de bloqueos** le permite administrar la característica de detección de la administración de complementos en Internet Explorer. Si habilita esta configuración de directiva, un bloqueo en Internet Explorer será similar al de un equipo en el que se ejecuta Windows XP Professional Service Pack 1 y versiones anteriores: se invocará el Informe de errores de Windows. Si deshabilita esta configuración de directiva, funcionará la característica de detección de bloqueos en la administración de complementos.
  
Dado que la información de informe de bloqueos de Internet Explorer podría contener datos confidenciales de la memoria del equipo, en este apéndice se recomienda que configure esta directiva como **Habilitada**, a menos que experimente bloqueos y deba informar de éstos para la solución de problemas en fase de seguimiento. En esos casos podría establecer temporalmente la configuración como **Deshabilitada.**
  
##### No permitir que usuarios habiliten ni deshabiliten complementos
  
**Tabla A.2: Configuración de habilitación o deshabilitación de la configuración de complementos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **No permitir que usuarios habiliten ni deshabiliten complementos** le permite administrar si los usuarios pueden permitir o denegar complementos a través de Administrar complementos. Si se establece esta configuración de directiva como **Habilitada**, los usuarios no podrán habilitar ni deshabilitar los complementos a través de la característica Administrar complementos. La única excepción se produce si un complemento se ha introducido específicamente en la configuración de directiva **Lista de complementos** de manera que los usuarios puedan seguir administrando el complemento. En tal caso, el usuario aún puede administrar el complemento a través de Administrar complementos. Si establece esta configuración de directiva como **Deshabilitada**, el usuario podrá habilitar o deshabilitar complementos.
  
**Nota**: para obtener más información acerca de cómo administrar complementos de Internet Explorer en Windows XP SP2, vea el artículo 883256 de Microsoft Knowledge Base acerca de cómo administrar complementos de Internet Explorer en Windows XP Service Pack 2, en [http://support.microsoft.com/?kbid=883256.](http://support.microsoft.com/?kbid=883256)
  
Es habitual que los usuarios decidan instalar complementos no permitidos por una directiva de seguridad de la organización. Dichos complementos pueden suponer un riesgo considerable para la seguridad y la privacidad en la red. Por eso, en este apéndice se recomienda que configure esta directiva como **Habilitada.**
  
**Nota**: debe revisar la configuración de GPO en Internet Explorer\\Características de seguridad\\Administración de complementos para asegurarse de que en su entorno aún se pueden ejecutar los complementos autorizados que corresponda.
  
##### Panel de control Internet\\Página Seguridad
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
\\Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Página Seguridad
  
SP2 introduce varias configuraciones de directiva nuevas que le ayudan a proteger la configuración de zonas de Internet Explorer en su entorno. SP2 establece para los equipos valores predeterminados de estas configuraciones que aumentan el nivel de seguridad. Sin embargo, quizá desee revisar estos parámetros y configurar estas directivas para que sean requeridas en mayor o menor medida en su entorno a fin de facilitar el uso o la compatibilidad con aplicaciones.
  
Por ejemplo, SP2 configura Internet Explorer para que se bloqueen de forma predeterminada los elementos emergentes en todas las zonas de Internet. Quizá desee asegurarse de que esta configuración se aplica en todos los equipos de su entorno para eliminar la aparición continua de ventanas emergentes y reducir la posibilidad de instalaciones de software espía y malintencionado que a menudo se inician desde sitios web de Internet. Por otra parte, existe la posibilidad de que su entorno contenga aplicaciones que requieren el uso de elementos emergentes para funcionar. Si así fuera, podría configurar esta directiva para permitir elementos emergentes de sitios web de la intranet.
  
##### Panel de control Internet\\Página Opciones avanzadas
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
\\Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas
  
###### Permitir que el software se ejecute o instale incluso si la firma no es válida
  
**Tabla A.3: Configuración de permiso para ejecutar software**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
Los controles Microsoft ActiveX y los archivos que se descargan suelen tener adjuntas firmas digitales que garantizan la integridad del archivo y la identidad del firmante (creador) del software. Estas firmas ayudan a asegurar que se descarga software no modificado y que el usuario pueda identificar al firmante para determinar si confía en éste lo suficiente como para ejecutar su software.
  
La configuración de directiva **Permitir que el software se ejecute o instale incluso si la firma no es válida** le permite administrar si el software descargado puede ser instalado o ejecutado por los usuarios aunque la firma no sea válida. Una firma no válida podría indicar que alguien ha manipulado el archivo. Si habilita esta configuración de directiva, se preguntará a los usuarios si desean instalar o ejecutar los archivos cuya firma no es válida. Si deshabilita esta configuración de directiva, los usuarios no podrán ejecutar ni instalar archivos cuya firma no sea válida.
  
Puesto que el software sin firmar puede crear una vulnerabilidad de seguridad, en este apéndice se recomienda bloquear ese software estableciendo la configuración como **Deshabilitada**.
  
**Nota**: puede haber software y controles legítimos que tengan firma no válida, aunque sean correctos. Deberá probar cuidadosamente ese software en un entorno aislado antes de permitir su uso en la red de la organización.
  
##### Características de seguridad\\Restricción de seguridad del protocolo MK
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Restricción de seguridad del protocolo MK
  
###### Procesos de Internet Explorer (Protocolo MK)
  
**Tabla A.4: Configuración del protocolo MK**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **Restricción de seguridad del protocolo MK** reduce área de superficie de ataque al bloquear el protocolo MK, que raramente se utiliza. Algunas aplicaciones web más antiguas utilizan el protocolo MK para recuperar información de archivos comprimidos. Si se establece esta directiva como **Habilitada**, se bloqueará el protocolo MK para el Explorador de Windows e Internet Explorer, lo que provocará errores de los recursos que utilizan el protocolo MK. Al deshabilitar este parámetro se permite a las aplicaciones que utilicen la API del protocolo MK.
  
Dado que el protocolo de MK no se utiliza de forma generalizada, debe bloquearse siempre que no se necesite. En este apéndice se recomienda establecer esta configuración como **Habilitada** para bloquear el protocolo MK, a menos que lo necesite específicamente en su entorno.
  
**Nota**: dado que se producirá un error en los recursos que utilizan el protocolo MK cuando implemente esta configuración, debe asegurarse de que ninguna de sus aplicaciones utiliza el protocolo MK.
  
##### Características de seguridad\\Administración de MIME consistente
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Administración de MIME consistente
  
###### Procesos de Internet Explorer (Administración de MIME consistente)
  
**Tabla A.5: Configuración de administración de MIME consistente**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Internet Explorer utiliza datos MIME (Extensiones seguras multipropósito de correo de Internet) para determinar los procedimientos de administración de archivos recibidos a través de un servidor web. La configuración de directiva **Administración de MIME consistente\\Procesos de Internet Explorer** determina si Internet Explorer debe requerir que toda la información de tipo de archivo proporcionada por los servidores web sea coherente. Por ejemplo, si el tipo MIME de un archivo es texto/sin formato pero los datos MIME indican que el archivo es realmente un archivo ejecutable, Internet Explorer cambia su extensión para reflejar el estado ejecutable. Esta capacidad ayuda a asegurar que ese código ejecutable no se haga pasar por otros tipos de datos en los que se puede confiar.
  
Si habilita esta configuración de directiva, Internet Explorer examina todos los archivos recibidos y exige que tengan datos MIME coherentes. Si deshabilita o no configura este parámetro de directiva, Internet Explorer no requerirá que los datos MIME sean coherentes en todos los archivos recibidos y utilizará los datos MIME proporcionados por el archivo.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Asegurarse de que estos archivos son coherentes y están debidamente etiquetados ayuda a evitar descargas de archivos malintencionados que podrían infectar su red. Por eso, en este apéndice se recomienda que configure esta directiva como **Habilitada** para todos los entornos especificados en la guía.
  
**Nota:** esta configuración funciona conjuntamente con los parámetros de las **Características de seguridad de examen de MIME**, pero no los reemplaza.
  
##### Características de seguridad\\Características de seguridad de examen de MIME
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Características de seguridad de examen de MIME
  
###### Procesos de Internet Explorer (Examen de MIME)
  
**Tabla A.6: Configuración de examen de MIME**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
El examen de MIME es el proceso que consiste en la evaluación del contenido de un archivo MIME para determinar su contexto (si se trata de un archivo de datos, de un archivo ejecutable o de algún otro tipo del archivo). Esta configuración de directiva determina si el examen de MIME de Internet Explorer evitará la conversión de un archivo de un tipo determinado a otro tipo más peligroso. Cuando se establece como **Habilitada**, la función de examen de MIME nunca convertirá un archivo de un tipo a otro tipo de archivo más peligroso. Al deshabilitar el examen de MIME se configuran los procesos de Internet Explorer de modo que permitan una evaluación de MIME que convierta un archivo de un tipo determinado a otro tipo de archivo más peligroso. Por ejemplo, la conversión de un archivo de texto en un archivo ejecutable es peligrosa porque se ejecutaría cualquier código del supuesto archivo de texto.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Asegurarse de que estos archivos se tratan de forma coherente ayuda a evitar descargas de archivos malintencionados que podrían infectar su red. Por eso, en este apéndice se recomienda que configure esta directiva como **Habilitada** para todos los entornos especificados en la guía.
  
**Nota:** esta configuración funciona conjuntamente con los parámetros de **Administración de MIME consistente**, pero no los reemplaza.
  
##### Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos
  
###### Procesos de Internet Explorer (Restricciones de seguridad de ventanas con secuencias de comandos)
  
**Tabla A.7: Configuración de restricciones de seguridad de ventanas con secuencias de comandos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Internet Explorer permite que mediante secuencias de comandos se abran distintos tipos de ventanas, así como que se cambie su tamaño y posición. Hay sitios web de mala reputación que cambian el tamaño de las ventanas para ocultar otras o que obligan al visitante a interaccionar con una ventana que contiene código malintencionado.
  
La característica de seguridad **Restricciones de seguridad de ventanas con secuencias de comandos** restringe las ventanas emergentes e impide que a través de secuencias de comandos se muestren ventanas en las que las barras de título y estado no sean visibles para el usuario o que se oculten las barras de título y estado de otras ventanas. Si habilita la configuración de directiva **Restricciones de seguridad de ventanas con secuencias de comandos\\Procesos de Internet Explorer**, las restricciones de ventanas emergentes y otros elementos se aplican al Explorador de Windows y a los procesos de Internet Explorer. Si deshabilita o no establece esta configuración de directiva, las secuencias de comandos pueden seguir creando ventanas emergentes y ventanas que oculten a otras.
  
En este apéndice se recomienda establecer esta directiva como **Habilitada** para contribuir a evitar que desde sitios web malintencionados se controlen sus ventanas de Internet Explorer o se engañe a los usuarios para que hagan clic en una ventana indebidamente.
  
##### Características de seguridad\\Protección contra elevación de zona
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Protección contra elevación de zona
  
###### Procesos de Internet Explorer (Protección contra elevación de zona)
  
**Tabla A.8: Configuración de protección contra elevación de zona**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Internet Explorer establece restricciones para cada página web que abre, las cuales dependen de la ubicación de ésta (zona Internet, zona de intranet o zona Máquina local). Las páginas web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Máquina local, lo que convierte a la zona de seguridad Máquina local en un objetivo prioritario para los atacantes malintencionados.
  
Si habilita esta configuración de directiva, se puede proteger cualquier zona de modo que los procesos de Internet Explorer no puedan llevar a cabo una elevación de zona. Con este método se impide que se apliquen privilegios elevados de una zona al contenido de otra zona. Si deshabilita esta configuración de directiva, ninguna zona recibirá ese tipo de protección en los procesos de Internet Explorer.
  
A causa de la gravedad y relativa frecuencia de los ataques de elevación de zona, en este apéndice se recomienda establecer esta configuración como **Habilitada** en todos los entornos.
  
##### Características de seguridad\\Limitar la instalación de ActiveX
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Limitar la instalación de ActiveX
  
###### Procesos de Internet Explorer (Limitar la instalación de ActiveX)
  
**Tabla A.9: Configuración de limitación de la instalación de ActiveX**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **Limitar la instalación de ActiveX\\Procesos de Internet Explorer** habilita el bloqueo de mensajes de instalación de controles ActiveX para procesos de Internet Explorer.
  
Si habilita esta configuración de directiva, se bloquearán los mensajes de instalación de controles de ActiveX en procesos de Internet Explorer. Si deshabilita esta configuración de directiva, no se bloquearán los mensajes de instalación de controles ActiveX.
  
A menudo, los usuarios deciden instalar software (como, por ejemplo, controles de ActiveX) que no permite la directiva de seguridad de la compañía. Ese tipo de software puede entrañar riesgos considerables para la seguridad y la privacidad en la red. Por eso, en este apéndice se recomienda que configure esta directiva como **Habilitada.**
  
**Nota**: esta configuración impide también que los usuarios instalen controles legítimos de ActiveX que interfieran en el funcionamiento de componentes importantes del sistema, como Windows Update. Si habilita esta configuración, asegúrese de implementar Servicios de actualización de software (SUS) o algún método alternativo de implementación de actualizaciones de seguridad.
  
Para obtener más información acerca de SUS, vea la página de Servicios de actualización de software (que incluye también información acerca de Windows Update, sucesor a SUS) en [http://www.microsoft.com/windowsserversystem/sus/default.mspx.](http://www.microsoft.com/windowsserversystem/sus/default.mspx)
  
##### Características de seguridad\\Limitar la descarga de archivos
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Limitar la descarga de archivos
  
###### Procesos de Internet Explorer (Limitar la descarga de archivos)
  
**Tabla A.10: Configuración de limitación de descarga de archivos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
En determinadas circunstancias los sitios web pueden iniciar diálogos de descarga de archivos sin la interacción de los usuarios. Esta técnica puede permitir a un sitio web colocar archivos no autorizados en el disco duro de un usuario si éste hace clic en el botón equivocado y acepta la descarga.
  
Si establece la configuración de directiva **Limitar la descarga de archivos\\Procesos de Internet Explorer** como **Habilitada**, se bloquean los mensajes de descarga de archivos que no inician los usuarios para los procesos de Internet Explorer. Si establece esta configuración de directiva como **Deshabilitada**, se mostrarán mensajes para descargas de archivos que no inicien los usuarios en los procesos de Internet Explorer.
  
**Nota**: esta configuración se establece como **Habilitada** en todos los entornos especificados en esta guía para contribuir a evitar que un atacante coloque código arbitrario en equipos de usuarios.
  
##### Características de seguridad\\Administración de complementos
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Administración de complementos
  
###### Denegar complementos a menos que se permitan específicamente en la Lista de complementos
  
**Tabla A.11: Configuración de denegación de complementos a menos que se permitan específicamente en la Lista de complementos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Esta configuración de directiva, junto con la directiva **Lista de complementos**, le permite controlar complementos de Internet Explorer. De forma predeterminada, la configuración de directiva **Lista de complementos** define una relación de complementos que se deben permitir o denegar a través de Directiva de grupo. La configuración de directiva **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** supone que todos los complementos se deniegan a menos que aparezcan enumerados específicamente en la configuración de directiva **Lista de complementos.**
  
Si habilita esta configuración de directiva, Internet Explorer sólo permite complementos que se enumeran (y permiten) específicamente a través de la configuración de directiva **Lista de complementos.** Si deshabilita esta configuración de directiva, los usuarios pueden utilizar el Administrador de complementos para permitir o denegar cualquier complemento.
  
Considere la posibilidad de utilizar tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en su entorno. Este método ayudará a garantizar que sólo se utilicen complementos autorizados.
  
###### Lista de complementos
  
**Tabla A.12: Configuración de Lista de complementos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Esta configuración de directiva, junto con la directiva **Denegar complementos a menos que se permitan específicamente en la Lista de complementos**, le permite controlar los complementos de Internet Explorer. De forma predeterminada, la configuración de directiva **Lista de complementos** define una relación de complementos que se deben permitir o denegar a través de Directiva de grupo. La configuración de directiva **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** supone que todos los complementos se deniegan a menos que aparezcan enumerados específicamente en la configuración de directiva **Lista de complementos.**
  
Si se habilita esta configuración de directiva, deberá especificar una lista de complementos que deben ser permitidos o denegados por Internet Explorer. Para cada entrada que agregue a la lista debe proporcionar la información siguiente:
  
-   **Nombre del valor.** El CLSID (identificación de clase) del componente que desea agregar a la lista. El CLSID debe escribirse entre llaves; por ejemplo, {000000000-0000-0000-0000-0000000000000}. El CLSID de un complemento se puede obtener si se lee la etiqueta OBJECT de una página web que haga referencia al complemento.
  
-   **Valor**. Un número que indica si Internet Explorer debe denegar o permitir que se cargue el complemento. Los valores siguientes son válidos:
  
    **Tabla A.13: Valores de configuración de la Lista de complementos**

 
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Valor</th>
    <th style="border:1px solid black;" >Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">0</td>
    <td style="border:1px solid black;">Denegar este complemento</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">1</td>
    <td style="border:1px solid black;">Permitir este complemento</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">2</td>
    <td style="border:1px solid black;">Permitir este complemento y que el usuario lo administre a través de Administrar complementos</td>
    </tr>
    </tbody>
    </table>
  
Si deshabilita esta configuración de directiva, se elimina la lista.
  
Considere la posibilidad de utilizar tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en su entorno. Este método ayudará a garantizar que sólo se utilicen complementos autorizados.
  
#### Servicios de Terminal Server\\Cliente
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\componentes de Windows\\Servicios de Terminal Server\\Cliente
  
##### No permitir que se guarden las contraseñas
  
**Tabla A.14: Configuración de no autorización de almacenamiento de contraseñas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **No permitir que se guarden las contraseñas** evita que los clientes de Servicios de Terminal Server guarden contraseñas en un equipo. Cuando se habilita esta configuración, se deshabilita la casilla de verificación de almacenamiento en los clientes de Servicios de Terminal Server, de modo que los usuarios no puedan seguir guardando sus contraseñas. Dado que la práctica de guardar la contraseña puede suponer un riesgo adicional, esta configuración se establece como **Habilitada** para los entornos definidos en esta guía.
  
**Nota**: si esta configuración se estableció previamente como **Deshabilitada** o como parámetro **No configurado**, todas las contraseñas guardadas se eliminarán la primera vez que un cliente de Servicios de Terminal Server se desconecte de cualquier servidor.
  
#### Windows Update
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\Componentes de Windows\\Windows Update
  
##### No mostrar la opción 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar
  
**Tabla A.15: Configuración de no visualización de opciones de Apagar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **No mostrar la opción 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar** le permite administrar si se debe mostrar la opción **Instalar actualizaciones y Apagar** en el cuadro de diálogo **Salir de Windows.**
  
En caso de deshabilitarse esta configuración de directiva, la opción **Instalar actualizaciones y cerrar** estará disponible en el cuadro de diálogo **Salir de Windows** si hay actualizaciones disponibles cuando el usuario selecciona **Apagar equipo** en el menú **Inicio** o hace clic en **Apagar** en la ventana que se muestra después de presionar Ctrl + Alt + Supr. Dado que la instalación de actualizaciones es importante para la seguridad de los equipos en general, la configuración se establece como **Deshabilitada** para todos los entornos definidos en esta guía. Esta configuración funciona conjuntamente con la configuración de directiva **No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar**, que se trata a continuación.
  
##### No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar
  
**Tabla A.16: Configuración de no autorización de ajuste de opciones de Apagar predeterminadas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar** permite administrar si se posibilita que la opción **Instalar actualizaciones y Apagar** sea la predeterminada en el cuadro de diálogo **Salir de Windows**. Si se deshabilita esta configuración de directiva, la opción **Instalar actualizaciones y Apagar** será la predeterminada en el cuadro de diálogo **Salir de Windows** en caso de que haya actualizaciones disponibles para la instalación en el momento en que el usuario seleccione la opción **Apagar equipo** en el menú **Inicio**.
  
Dado que la instalación de actualizaciones es importante para la seguridad de los equipos en general, la configuración se establece como **Deshabilitada** para todos los entornos definidos en esta guía.
  
**Nota**: esta configuración de directiva no tiene ningún efecto si está habilitada la configuración de directiva **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Update\\No mostrar la opción 'Instalar actualizaciones y Apagar'** en el **cuadro de diálogo Salir de Windows**.
  
#### Sistema
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración del equipo\\Plantillas administrativas\\Sistema
  
##### Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update
  
**Tabla A.17: Configuración de la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update** controla si se le pide al administrador que busque controladores de dispositivo a través de Windows Update en Internet. Si esta configuración está habilitada, no se solicitará a los administradores que busquen con Windows Update. Si esta configuración está deshabilita o el parámetro no está configurado y **Desactivar la búsqueda de controladores de dispositivo en Windows Update** se deshabilita o no se configura, se pedirá al administrador su consentimiento antes de iniciar la búsqueda de controladores de dispositivo a través de Windows Update.
  
Dado que existe un cierto grado de riesgo al descargar controladores de dispositivo de Internet, en este apéndice se recomienda establecer la configuración como **Habilitada** para entornos de alta seguridad y como **Deshabilitada** para entornos de empresa. El motivo de esta recomendación es que, normalmente, los tipos de ataques que pueden aprovechar descargas de controladores se reducirán mediante una administración apropiada de los recursos de la empresa.
  
**Nota**: esta configuración sólo es efectiva si se ha deshabilitado o no se ha configurado **Desactivar la búsqueda de controladores de dispositivo en Windows Update** en **Plantillas administrativas/Sistema/Administración de comunicaciones de Internet/Configuración de comunicaciones de Internet**.
  
##### Sistema\\Informe de errores
  
En el capítulo 4 de la *Guía de seguridad de Windows XP* se recomiendan diversas configuraciones para los informes de errores. Estas configuraciones son las mismas para los equipos en los que se ejecuta Windows XP SP2, aunque ha cambiado el nombre de una de ellas. La configuración de **Informar de errores** que se describe en la Tabla 4.42 se muestra ahora como **Configurar Informe de errores.** Los parámetros de configuración recomendados son los mismos que los descritos en el Capítulo 4.
  
##### Sistema\\Llamada a procedimiento remoto
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\Sistema\\Llamada a procedimiento remoto
  
###### Restricciones para clientes RPC no autenticados
  
**Tabla A.18: Configuración de clientes RPC no autenticados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Si se habilita la configuración **Restricciones para clientes RPC no autenticados** se establece el Tiempo de ejecución de RPC en un servidor RPC para limitar la conexión de clientes RPC no autenticados a servidores RPC que se ejecutan en un equipo. Se considerará que un cliente se ha autenticado si utiliza una canalización con nombre para comunicarse con el servidor o si utiliza seguridad RPC. Las interfaces de RPC que han pedido específicamente ofrecer acceso a clientes no autenticados pueden quedar exentas de esta restricción, con arreglo al valor seleccionado para esta directiva. Si se habilita esta configuración estarán disponibles los siguientes valores:
  
-   **Ninguno**. Este valor permite a todos los clientes RPC conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva.
  
-   **Autenticado**. Este valor permite únicamente a los clientes RPC conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva. A las interfaces que han solicitado quedar exentas de esta restricción se les otorgará una exención.
  
-   **Autenticado sin excepciones.** Este valor permite únicamente a los clientes RPC conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva. No se permiten excepciones.
  
Dado que la comunicación RPC sin autenticación puede crear una vulnerabilidad de seguridad, en este apéndice se recomienda establecer esta configuración como **Habilitada** y el valor de **Restricción de clientes sin autenticar del tiempo de ejecución RPC que desea aplicar** como **Autenticado** para todos los entornos definidos en esta guía.
  
**Nota**: las aplicaciones RPC que no autentican solicitudes de conexión de entrada no solicitadas pueden no funcionar correctamente cuando se aplica esta configuración. Asegúrese de probar las aplicaciones antes de generalizar la implementación de esta configuración. Aunque el valor **Autenticado** para este parámetro no sea completamente seguro, puede resultar útil por lo que respecta a la compatibilidad de aplicaciones en su entorno.
  
###### Autenticación de clientes del Asignador de puntos finales de RPC
  
**Tabla A.19: Configuración de autenticación de cliente**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Si se habilita la configuración **Autenticación de clientes del Asignador de puntos finales de RPC**, los clientes que se comunican con este equipo deberán proporcionar autenticación antes de que se establezca la comunicación RPC.
  
##### Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet
  
Existen varias opciones de configuración disponibles en el grupo Configuración de comunicaciones de Internet. En este apéndice se recomienda que muchas de estas configuraciones sean restringidas, principalmente para ayudar a aumentar el nivel de confidencialidad de los datos en los sistemas informáticos. Si esta configuración no es restringida, la información podría ser interceptada y utilizada por atacantes. Aunque las probabilidades de que se produzca hoy este tipo de ataque son escasas, si configura ahora correctamente estos parámetros ayudará a proteger su entorno contra futuros ataques.
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet
  
###### Desactivar la tarea Publicar en Web para archivos y carpetas
  
**Tabla A.20: Configuración de la desactivación de las tareas de publicación en Web**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Esta configuración especifica si las tareas **Publicar este archivo en Web**, **Publicar esta carpeta en Web** y **Publicar los elementos seleccionados en Web** están disponibles en las Tareas de archivo y carpeta en las carpetas de Windows. El Asistente para la publicación en Web se usa para descargar una lista de proveedores y permite que los usuarios publiquen contenido en Web. Si se establece esta configuración como **Habilitada** se quitan estas opciones de Tareas de archivo y carpeta en las carpetas de Windows.
  
###### Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea
  
**Tabla A.21: Configuración de la desactivación de descargas de Internet**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración de **Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea** controla si Windows descargará una lista de proveedores de los asistentes para la publicación en Web y para pedidos en línea. Si se habilita esta configuración se evitará que Windows descargue proveedores; sólo se mostrarán los proveedores de servicios que se encuentren almacenados en caché en el Registro local.
  
###### Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger
  
**Tabla A.22: Configuración de la desactivación del programa para el cliente de Messenger**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger** especifica si Windows Messenger debe recopilar información anónima acerca del uso del servicio y del software Windows Messenger. Si establece esta configuración como **Habilitada**, se asegurará de que Windows Messenger no recopilará información de uso, y que no se mostrará la configuración de usuario que permite habilitar la recopilación de información de uso.
  
###### Desactivar la actualización de archivos de contenido del Asistente para búsqueda
  
**Tabla A.23: Configuración de desactivación de la actualización del Asistente para búsqueda**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Desactivar la actualización de archivos de contenido del Asistente para búsqueda** especifica si el Asistente para búsqueda debe descargar automáticamente actualizaciones de contenido durante búsquedas en Internet y locales. Si se establece esta configuración como **Habilitada**, evitará que el Asistente para búsqueda descargue actualizaciones de contenido durante las búsquedas.
  
**Nota**: las búsquedas de Internet seguirán enviando el texto de la búsqueda e información acerca de la búsqueda a Microsoft y al proveedor de búsqueda elegido. Si se selecciona la búsqueda clásica se desactivará completamente la característica Asistente para búsqueda. Puede seleccionar la búsqueda clásica si hace clic en **Inicio**, **Buscar**, **Cambiar preferencias** y, a continuación, en **Cambiar el comportamiento de búsqueda en Internet**.
  
###### Desactivar impresión a través de HTTP
  
**Tabla A.24: Configuración de desactivación de la impresión a través de HTTP**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Esta configuración le permite deshabilitar la impresión a través de HTTP desde este cliente. La impresión a través de HTTP permite a un cliente imprimir con impresoras de la intranet así como de Internet. Si se habilita esta configuración, el cliente no podrá utilizar impresoras de Internet a través de HTTP.
  
La información transmitida al imprimir a través de HTTP no es protegida y puede ser interceptada por usuarios malintencionados. Por eso se utiliza pocas veces en empresas o entornos de alta seguridad. La desactivación de esta característica ayuda a asegurar que no se utilice accidentalmente, ya que podría ponerse en peligro la seguridad con un trabajo de impresión no protegido.
  
**Nota**: este parámetro afecta únicamente a los clientes de impresión de Internet. No impide que el equipo actúe como un servidor de impresión de Internet ni que sus impresoras compartidas estén disponibles a través de HTTP.
  
###### Desactivar la descarga de controladores de impresión a través de HTTP
  
**Tabla A.25: Configuración de desactivación de la descarga de controladores de impresión a través de HTTP**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Desactivar la descarga de controladores de impresión a través de HTTP** controla si el equipo puede descargar paquetes de controladores de impresión a través de HTTP. Para configurar la impresión a través de HTTP, quizá sea necesario descargar a través de HTTP los controladores de impresión no disponibles en la instalación del sistema operativo estándar. En este apéndice se recomienda establecer la configuración como **Habilitada** para evitar que se descarguen controladores de impresión a través de HTTP.
  
**Nota**: esta configuración no impide que el cliente utilice impresoras de la intranet o de Internet a través HTTP. Sólo desautoriza la descarga de controladores no instalados ya localmente.
  
###### Desactivar la búsqueda de controladores de dispositivo en Windows Update
  
**Tabla A.26: Configuración de la desactivación de la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La directiva **Desactivar la búsqueda de controladores de dispositivo en Windows Update** especifica si Windows debe buscar mediante Windows Update controladores de dispositivo cuando no se encuentran localmente.
  
Dado que existe un cierto grado de riesgo al descargar controladores de dispositivo de Internet, en este apéndice se recomienda establecer la configuración como **Habilitada** para entornos de alta seguridad y como **Deshabilitada** para entornos de empresa. El motivo de esta recomendación es que, normalmente, los tipos de ataques que pueden aprovechar descargas de controladores se reducirán mediante una administración apropiada de los recursos de la empresa y las configuraciones.
  
**Nota**: vea también **Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update** en **Plantillas administrativas/Sistema**, que permite establecer si se pregunta al administrador antes de buscar a través de Windows Update controladores de dispositivo que no se encuentren localmente.
  
#### Firewall de Windows\\Perfil de dominio
  
Las opciones de esta sección configuran el Perfil de dominio de Firewall de Windows. Firewall de Windows puede determinar dinámicamente si el equipo se encuentra en un entorno de dominio y aplicar una configuración específica de servidor de seguridad en consecuencia. Esta capacidad le permite implementar opciones de configuración de servidor de seguridad independientes basadas en la ubicación de equipo.
  
Siempre que se detecta un entorno de dominio, se utiliza el Perfil de dominio. Puede configurar este perfil de modo que sea menos restrictivo que el Perfil estándar, ya que un entorno de dominio suele proporcionar capas de protección adicionales. La información de configuración de Perfil estándar figura más adelante en este apéndice.
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\Red\\Conexiones de red\\Firewall de Windows\\Perfil de dominio
  
##### Firewall de Windows: proteger todas las conexiones de red (Perfil de dominio)
  
**Tabla A.27: Configuración de protección de todas las conexiones de red con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: proteger todas las conexiones de red** activa el Firewall de Windows, que reemplaza al Servidor de seguridad de conexión a Internet en todos los equipos en los que se ejecuta Windows XP SP2. En este apéndice se recomienda establecer la configuración como **Habilitada** para proteger todas las conexiones de red para equipos de todos los entornos.
  
Si esta configuración se establece como **Deshabilitada**, se desactiva el Firewall de Windows y se omiten todos los demás parámetros de configuración del Firewall de Windows.
  
**Nota**: si habilita esta configuración de directiva, se ejecuta el Firewall de Windows y se omite la configuración de directiva **Configuración del equipo\\Plantillas administrativas\\Red\\Conexiones de red\\Prohibir el uso de Servidor de seguridad de conexión a Internet en su red de dominio DNS**.
  
##### Firewall de Windows: no permitir excepciones (Perfil de dominio)
  
**Tabla A.28: Configuración de no autorización de excepciones con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
Mediante la configuración **Firewall de Windows: no permitir excepciones** se especifica que el Firewall de Windows debe bloquear todos los mensajes entrantes no solicitados. Esta configuración de directiva anula todos los demás parámetros de directiva de Firewall de Windows que permitan ese tipo de mensajes. Si habilita esta configuración de directiva en el componente Firewall de Windows del Panel de control, se activa la casilla de verificación **No permitir excepciones**, que no podrán desactivar los administradores.
  
Muchos entornos contienen aplicaciones y servicios a los que para su funcionamiento normal se debe permitir la recepción de comunicaciones entrantes no solicitadas. En esos casos, quizá deba considerar la posibilidad de establecer esta configuración como **Deshabilitada** para permitir que esas aplicaciones y servicios se ejecuten debidamente. Sin embargo, antes de realizar cualquier cambio en esta directiva, debe probar el entorno para determinar exactamente lo que puede permitirse y rechazarse.
  
**Nota**: esta configuración proporciona una sólida defensa frente a atacantes externos y debe establecerse como **Habilitada** en situaciones en las que se necesite una completa protección frente a ataques externos tales como un gusano nuevo en la red. La configuración de esta directiva como **Deshabilitada** permite a Firewall de Windows aplicar otra configuración de directiva que autoriza los mensajes entrantes no solicitados.
  
##### Firewall de Windows: definir excepciones de programa (Perfil de dominio)
  
**Tabla A.29: Configuración de definición de excepciones de programa con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Es posible que algunas aplicaciones necesiten abrir y utilizar puertos de red que no suele permitir el Firewall de Windows. La configuración **Firewall de Windows: definir excepciones de programa** le permite ver y cambiar la lista de excepciones de programa definidas por Directiva de grupo.
  
Si se configura esta directiva como **Habilitada** podrá ver y cambiar la lista de excepciones de programa. Si agrega un programa a esta lista y establece su estado como **Habilitado**, ese programa podrá recibir mensajes entrantes no solicitados en cualquier puerto que pida a Firewall de Windows que se abra, aunque dicho puerto esté bloqueado por otra configuración de directiva.
  
Si establece esta configuración de directiva como **Deshabilitada**, se elimina la lista de excepciones de programa definida por Directiva de grupo.
  
**Nota**: si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores. Dado que no se comprueba la entrada, puede agregar programas que aún no se han instalado. También es posible crear accidentalmente varias excepciones para el mismo programa y que entren en conflicto los valores de Ámbito o Estado.
  
##### Firewall de Windows: permitir excepciones de programa local (Perfil de dominio)
  
**Tabla A.30: Configuración de autorización de excepciones de programa local con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones de programa local** permite a los administradores utilizar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de programa local. El hecho de deshabilitar esta configuración de directiva no autoriza a los administradores a definir una lista local de excepciones de programa, y garantiza que esas excepciones de programa sólo procedan de la Directiva de grupo. Si se configura esta directiva como **Habilitada**, los administradores locales podrán utilizar el Panel de control para definir excepciones de programa localmente.
  
Para equipos de cliente de empresa, es posible que existan condiciones que justifiquen que el cliente pueda definir excepciones de programa de ámbito local. Estas condiciones pueden incluir aplicaciones que no se analizaron al crear la directiva de servidor de seguridad de la organización o aplicaciones nuevas que requieren una configuración de puertos no estándar. En esos casos, tiene la posibilidad de habilitar esta configuración, teniendo presente que se amplía la superficie de ataque de los equipos afectados.
  
##### Firewall de Windows: permitir excepción de administración remota (Perfil de dominio)
  
**Tabla A.31: Configuración de autorización de excepciones de administración remota con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
Muchas organizaciones aprovechan la administración de equipos remotos en sus operaciones diarias. Sin embargo, se han producido ataques en los que se aprovechaban puertos que suelen utilizar los programas de administración remota; Firewall de Windows puede bloquear estos puertos. Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de administración remota**.
  
Si se establece esta configuración como **Habilitada**, el equipo podrá recibir mensajes entrantes no solicitados que están asociados a la administración remota en los puertos TCP 135 y 445. Esta configuración de directiva permite también que SVCHOST.EXE y LSASS.EXE reciban mensajes entrantes no solicitados y que los servicios alojados abran puertos adicionales asignados dinámicamente, por lo general en el intervalo que va de 1024 a 1034, aunque puede ser cualquiera de los comprendidos entre el 1024 y el 65535. Si habilita esta configuración, también deberá especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows no aplica ninguna de las excepciones descritas.
  
En este apéndice se recomienda habilitar esta configuración para equipos de empresa si es necesario, y que deshabilite siempre la configuración para equipos de alta seguridad. Los equipos de su entorno deben aceptar las solicitudes de administración remota del menor número de equipos posible. Para maximizar la protección que ofrece Firewall de Windows, asegúrese de especificar sólo las direcciones IP y las subredes de equipos que se necesitan para la administración remota.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir la excepción compartir impresoras y archivos (Perfil del dominio)
  
**Tabla A.32: Configuración de autorización de la excepción de compartir impresoras y archivos con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
Esta configuración permite compartir archivos e impresoras al establecer que Firewall de Windows abra los puertos UDP 137 y 138 y los puertos TCP 139 y 445. Si habilita esta configuración de directiva, Firewall de Windows abre estos puertos para que el equipo pueda recibir trabajos de impresión y solicitudes de acceso a archivos compartidos. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo comparta archivos e impresoras.
  
Dado que, por lo general, los equipos del entorno en los que se ejecuta Windows XP no compartirán archivos e impresoras, en este apéndice se recomienda que establezca esta configuración como **Deshabilitada** en todos los entornos.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepciones ICMP (Perfil de dominio)
  
**Tabla A.33: Configuración de autorización de excepciones ICMP con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones ICMP** define el conjunto de tipos de mensajes ICMP (Protocolo de mensajes de control de Internet) que permitirá Firewall de Windows. Las utilidades pueden usar los mensajes ICMP para determinar el estado de otros equipos. Por ejemplo, Ping utiliza el mensaje de solicitud de eco.
  
Si establece esta configuración de directiva como **Habilitada**, deberá especificar qué tipos de mensajes ICMP permitirá Firewall de Windows que envíe o reciba el equipo. Cuando establece esta directiva como **Deshabilitada**, Firewall de Windows bloquea todos los tipos de mensajes ICMP entrantes no solicitados y los tipos de mensajes ICMP salientes enumerados. Como consecuencia de ello, las utilidades que usan mensajes ICMP bloqueados no podrán enviarlos al equipo o desde éste.
  
Muchas herramientas de atacantes aprovechan la posibilidad que ofrecen los equipos que aceptan tipos de mensajes ICMP y utilizan éstos para preparar distintos ataques. Sin embargo, algunas aplicaciones precisan mensajes ICMP para funcionar correctamente. Por eso, en este apéndice se recomienda que establezca esta configuración como **Deshabilitada** siempre que sea posible. Si en su entorno es necesario que algunos mensajes ICMP atraviesen el Firewall de Windows, establezca la configuración con los tipos de mensajes adecuados.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepción de Escritorio remoto (Perfil de dominio)
  
**Tabla A.34: Configuración de autorización de excepciones de Escritorio remoto con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Muchas organizaciones utilizan conexiones de Escritorio remoto en sus operaciones o procedimientos habituales de solución de problemas. Sin embargo, se han producido ataques en los que se aprovechaban los puertos que suele utilizar Escritorio remoto. Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de Escritorio remoto**.
  
Cuando se habilita esta configuración, se establece Firewall de Windows de modo que abra el puerto TCP 3389 para las conexiones de entrada. También debe especificar las direcciones IP o las subredes de las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloqueará este puerto e impedirá que el equipo reciba solicitudes de Escritorio remoto. Si un administrador intenta abrir este puerto agregándolo a una lista de excepciones de puerto local, Firewall de Windows no abre el puerto.
  
En algunos ataques se puede aprovechar un puerto 3389 abierto. Para mantener las capacidades de administración mejorada que proporciona Escritorio remoto, debe establecer esta configuración como **Habilitada** y especificar las direcciones IP y las subredes de los equipos utilizados para la administración remota. Los equipos de su entorno deben aceptar las solicitudes de Escritorio remoto del menor número de equipos posible.
  
##### Firewall de Windows: permitir excepción de entorno UPnP (Perfil de dominio)
  
**Tabla A.35: Configuración de autorización de excepción de entorno UPnP con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepción de entorno UPnP** permite a un equipo recibir mensajes Plug and Play no solicitados procedentes de dispositivos de red, tales como enrutadores con servidores de seguridad integrados. Para recibir estos mensajes, Firewall de Windows abre el puerto TCP 2869 y el puerto UDP 1900.
  
Si habilita esta configuración de directiva, Firewall de Windows abre estos puertos para que el equipo pueda recibir los mensajes Plug and Play. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes. Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo reciba mensajes Plug and Play.
  
Con el bloqueo del tráfico de red UPnP se reduce en la práctica la superficie susceptible de ataque en los equipos del entorno. En este apéndice se recomienda establecer esta configuración como **Deshabilitada** a menos que utilice dispositivos UPnP en la red.
  
##### Firewall de Windows: no permitir notificaciones (Perfil de dominio)
  
**Tabla A.36: Configuración de prohibición de notificaciones con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
Firewall de Windows puede mostrar notificaciones a los usuarios cuando un programa solicita que Firewall de Windows agregue el programa a la lista de excepciones de programa. Esta situación se produce cuando los programas intentan abrir un puerto y no se les permite, con arreglo a las reglas actuales de Firewall de Windows. La configuración **Firewall de Windows: no permitir notificaciones** establece si se muestran estos parámetros a los usuarios.
  
Si establece esta directiva como **Habilitada**, Firewall de Windows impide que se muestren estas notificaciones. Si se establece como **Deshabilitada**, Firewall de Windows permite que se muestren estas notificaciones.
  
A menudo, a los usuarios no se les permitirá agregar aplicaciones y puertos en respuesta a estos mensajes en entornos de empresa o de alta seguridad. En tales casos, este mensaje informará al usuario de que ocurre algo sobre lo que no tienen control. En esas situaciones debe establecer esta opción como **Habilitada**. En otros entornos en los que la configuración del usuario permite excepciones, deberá establecer esta opción como **Deshabilitada**.
  
##### Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión (Perfil de dominio)
  
**Tabla A.37: Configuración de prohibición de respuesta de monodifusión con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión** impide que un equipo reciba respuestas de monodifusión a sus mensajes salientes de difusión o multidifusión. Cuando esta configuración de directiva está habilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows bloquea las respuestas de monodifusión enviadas por esos otros equipos. Cuando la configuración está deshabilitada y este equipo envía un mensaje de difusión o multidifusión a otros equipos, Firewall de Windows espera hasta tres segundos respuestas de monodifusión de los otros equipos y después bloquea todas las respuestas posteriores.
  
Normalmente, no deseará recibir respuestas de monodifusión a mensajes de difusión o multidifusión. Tales respuestas pueden indicar un ataque de denegación de servicio (DoS) o que un atacante intenta sondear un equipo activo conocido. En este apéndice se recomienda que establezca esta configuración de directiva como **Habilitada** como ayuda para prevenir este tipo de ataques.
  
**Nota** : esta configuración de directiva no surte efecto si el mensaje de monodifusión es una respuesta a un mensaje de difusión de Protocolo de configuración dinámica de host (DHCP) enviado por el equipo. Firewall de Windows permite siempre esas respuestas de monodifusión DHCP. Sin embargo, esta configuración de directiva puede interferir en los mensajes NetBIOS que detectan conflictos de nombres.
  
##### Firewall de Windows: definir excepciones de puerto (Perfil de dominio)
  
**Tabla A.38: Configuración de definición de excepciones de puerto con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
La lista de excepciones de puerto de Firewall de Windows debe ser definida por Directiva de grupo, de modo que pueda administrar e implementar de forma centralizada las excepciones de puerto, y asegurarse de que los administradores locales no crean configuraciones menos seguras. La configuración de directiva **Firewall de Windows: definir excepciones de puerto** le permite administrar de forma centralizada estas configuraciones.
  
Si habilita esta configuración de directiva, puede ver y cambiar la lista de excepciones de puerto definida por Directiva de grupo. Para ver y modificar la lista de excepciones de puerto, establezca la configuración de directiva como **Habilitada** y haga clic en el botón **Mostrar**. Tenga en cuenta que si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores, lo que significa que puede crear accidentalmente varias entradas para el mismo puerto y que entren en conflicto los valores de Ámbito o Estado.
  
Si deshabilita esta configuración de directiva, la lista de excepciones de puerto definida por Directiva de grupo se elimina, pero otras configuraciones de directiva pueden seguir abriendo o bloqueando puertos. Asimismo, si existe una lista de excepciones de puerto local, se pasa por alto a menos que habilite la configuración de directiva **Firewall de Windows: permitir excepciones de puerto local**.
  
Para los entornos con aplicaciones no estándar que requieren que se abran determinados puertos debe considerarse la posibilidad de implementar excepciones de programa. En este apéndice se recomienda habilitar esta configuración y especificar una lista de excepciones de puerto sólo cuando no se pueden definir excepciones de programa. Las excepciones de programa permiten que Firewall de Windows acepte tráfico de red no solicitado únicamente mientras se ejecuta el programa especificado, y que a través de las excepciones de puerto se mantengan abiertos en todo momento los puertos especificados.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepciones de puerto local (Perfil de dominio)
  
**Tabla A.39: Configuración de autorización de excepciones de puerto local con Perfil de dominio**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones de puerto local** permite a los administradores utilizar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de puerto local. Firewall de Windows puede utilizar dos listas de excepciones de puerto; la otra se define mediante la configuración de directiva **Firewall de Windows: definir excepciones de puerto**.
  
Si habilita esta configuración de directiva, el componente del Panel de control Firewall de Windows permite a los administradores definir una lista de excepciones de puerto local. Si deshabilita esta configuración de directiva, el componente del Panel de control Firewall de Windows no permite a los administradores definir esa lista.
  
Normalmente, los administradores locales no están autorizados a anular las directivas organizativas y establecer sus propia listas de excepciones de puertos en los entornos de empresa o de alta seguridad. Por eso, en este apéndice se recomienda configurar esta opción como **Deshabilitada**.
  
#### Firewall de Windows\\Perfil estándar
  
La configuración de esta sección determina el Perfil estándar de Firewall de Windows. Firewall de Windows puede determinar dinámicamente si el equipo se encuentra en un entorno de dominio y aplicar una configuración específica de servidor de seguridad en consecuencia. Esta capacidad le permite implementar opciones de configuración de servidor de seguridad independientes basadas en la ubicación de equipo.
  
Siempre que se detecte un entorno que no es de dominio se utiliza el Perfil estándar. Este perfil es a menudo más restrictivo que el Perfil de dominio, que asume que un entorno de dominio proporciona un nivel de seguridad básico. Se espera que se utilice el Perfil estándar cuando un equipo se encuentra en una red que no es de confianza, en una red de hotel o en un punto de inalámbrico público. Ese tipo de entornos implican riesgos desconocidos y requieren precauciones de seguridad adicionales.
  
Para obtener más información acerca de cómo se usa el servicio Network Location Awareness (NLA) en Windows XP para determinar a qué clase de red está conectado el sistema, vea el artículo (en inglés) sobre la configuración del comportamiento en la determinación de la red para la directiva de grupo relacionada con la red en el sitio web de Microsoft, en [http://www.microsoft.com/spain/technet/recursos/articulos/cg0504.mspx.](http://www.microsoft.com/spain/technet/recursos/articulos/cg0504.mspx)
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Plantillas administrativas\\Red\\Conexiones de red\\Firewall de Windows\\Perfil estándar
  
##### Firewall de Windows: proteger todas las conexiones de red (Perfil estándar)
  
**Tabla A.40: Configuración de protección de todas las conexiones de red con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: proteger todas las conexiones de red** activa el Firewall de Windows, que reemplaza al Servidor de seguridad de conexión a Internet en todos los equipos en los que se ejecuta Windows XP SP2. Dado que las conexiones de red deben estar protegidas por un servidor de seguridad en todos los entornos, esta configuración se establece como **Habilitada.**
  
Si esta configuración se establece como **Deshabilitada**, se desactiva el Firewall de Windows y se omiten todos los demás parámetros de configuración del Firewall de Windows.
  
**Nota**: si habilita esta configuración de directiva, se ejecuta el Firewall de Windows y se omite la configuración de directiva **Configuración del equipo\\Plantillas administrativas\\Red\\Conexiones de red\\Prohibir el uso de Servidor de seguridad de conexión a Internet en su red de dominio DNS**.
  
##### Firewall de Windows: no permitir excepciones (Perfil estándar)
  
**Tabla A.41: Configuración de no autorización de excepciones con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Mediante la configuración **Firewall de Windows: no permitir excepciones** se especifica que el Firewall de Windows debe bloquear todos los mensajes entrantes no solicitados. Esta configuración de directiva anula todos los demás parámetros de directiva de Firewall de Windows que permitan ese tipo de mensajes. Si habilita esta configuración de directiva en el componente Firewall de Windows del Panel de control, se activa la casilla de verificación **No permitir excepciones**, que no podrán desactivar los administradores.
  
**Nota**: esta configuración proporciona una sólida defensa frente a atacantes externos y debe establecerse como **Habilitada** a menos que establezca excepciones en otras configuraciones de directiva. La configuración de esta directiva como **Deshabilitada** permite a Firewall de Windows aplicar otra configuración de directiva que autoriza los mensajes entrantes no solicitados.
  
##### Firewall de Windows: definir excepciones de programa (Perfil estándar)
  
**Tabla A.42: Configuración de definición de excepciones de programa con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
Es posible que algunas aplicaciones necesiten abrir y utilizar puertos de red que no suele permitir el Firewall de Windows. La configuración **Firewall de Windows: definir excepciones de programa** le permite ver y cambiar la lista de excepciones de programa definidas por Directiva de grupo.
  
Si se configura esta directiva como **Habilitada** podrá ver y cambiar la lista de excepciones de programa. Si agrega un programa a esta lista y establece su estado como **Habilitado**, ese programa podrá recibir mensajes entrantes no solicitados en cualquier puerto que pida a Firewall de Windows que se abra, aunque dicho puerto esté bloqueado por otra configuración de directiva.
  
Si establece esta configuración de directiva como **Deshabilitada**, se elimina la lista de excepciones de programa definida por Directiva de grupo.
  
**Nota**: si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores. Esta capacidad le permite agregar programas que no ha instalado todavía, pero debe tener en cuenta que puede crear accidentalmente varias entradas del mismo programa y que entren en conflicto los valores de Ámbito o Estado.
  
##### Firewall de Windows: permitir excepciones de programa local (Perfil estándar)
  
**Tabla A.43: Configuración de autorización de excepciones de programa local con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones de programa local** permite a los administradores utilizar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de programa local. Al deshabilitar esta configuración de directiva se asegura que el componente del Panel de control Firewall de Windows no permita a los administradores definir esa lista, y que esas excepciones de programa sólo procedan de la Directiva de grupo. Si se configura la directiva como **Habilitada**, los administradores locales podrán utilizar el Panel de control para definir excepciones de programa localmente.
  
##### Firewall de Windows: permitir excepción de administración remota (Perfil estándar)
  
**Tabla A.44: Configuración de autorización de excepciones de administración remota con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
Muchas organizaciones aprovechan la administración de equipos remotos en sus operaciones diarias. Sin embargo, a través de algunos ataques se han aprovechado puertos que suelen utilizar los programas de administración remota. En respuesta, Firewall de Windows puede bloquear estos puertos. Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de administración remota**.
  
Si se establece esta configuración como **Habilitada**, el equipo podrá recibir mensajes entrantes no solicitados que están asociados a la administración remota en los puertos TCP 135 y 445. Esta configuración de directiva permite también que SVCHOST.EXE y LSASS.EXE reciban mensajes entrantes no solicitados y que los servicios alojados abran puertos adicionales asignados dinámicamente, por lo general en el intervalo que va de 1024 a 1034, aunque puede ser cualquiera de los comprendidos entre el 1024 y el 65535. Si habilita esta configuración, también deberá especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows no aplica ninguna de las excepciones descritas.
  
En este apéndice se recomienda que deshabilite esta configuración para todos los equipos de Perfil estándar con objeto de evitar ataques conocidos que aprovechen específicamente los puertos TCP 135 y 445.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir la excepción compartir impresoras y archivos (Perfil estándar)
  
**Tabla A.45: Configuración de autorización de la excepción de compartir impresoras y archivos con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
Esta configuración permite compartir archivos e impresoras al establecer que Firewall de Windows abra los puertos UDP 137 y 138 y los puertos TCP 139 y 445. Si habilita esta configuración de directiva, Firewall de Windows abre estos puertos para que el equipo pueda recibir trabajos de impresión y solicitudes de acceso a archivos compartidos. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo comparta archivos e impresoras.
  
Dado que, por lo general, los equipos del entorno en los que se ejecuta Windows XP no compartirán archivos e impresoras, en este apéndice se recomienda que establezca esta configuración como **Deshabilitada** en todos los entornos.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepciones ICMP (Perfil estándar)
  
**Tabla A.46: Configuración de autorización de excepciones ICMP con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones ICMP** define el conjunto de tipos de mensajes ICMP (Protocolo de mensajes de control de Internet) que permitirá Firewall de Windows. Las utilidades pueden usar los mensajes ICMP para determinar el estado de otros equipos. Por ejemplo, la utilidad Ping utiliza el mensaje de solicitud de eco.
  
Si establece esta configuración de directiva como **Habilitada**, deberá especificar qué tipos de mensajes ICMP permitirá Firewall de Windows que envíe o reciba el equipo. Cuando establece esta directiva como **Deshabilitada**, Firewall de Windows bloquea todos los tipos de mensajes ICMP entrantes no solicitados y los tipos de mensajes ICMP salientes enumerados. Como consecuencia de ello, las utilidades que usan mensajes ICMP bloqueados no podrán enviarlos al equipo o desde éste.
  
Muchas herramientas de atacantes aprovechan la posibilidad que ofrecen los equipos que aceptan tipos de mensajes ICMP y utilizan éstos para preparar distintos ataques. Sin embargo, algunas aplicaciones precisan mensajes ICMP para funcionar correctamente. Por eso, en este apéndice se recomienda que establezca esta configuración como **Deshabilitada** siempre que sea posible. Siempre que el equipo se encuentra en una red que no es de confianza, esta configuración debe estar **Deshabilitada.**
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepción de Escritorio remoto (Perfil estándar)
  
**Tabla A.47: Configuración de autorización de excepciones de Escritorio remoto con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Muchas organizaciones utilizan conexiones de Escritorio remoto en sus operaciones o procedimientos habituales de solución de problemas. Sin embargo, se han producido ataques en los que se aprovechaban los puertos que suele utilizar Escritorio remoto. Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de Escritorio remoto**.
  
Cuando se habilita esta configuración, se establece Firewall de Windows de modo que abra el puerto TCP 3389 para las conexiones de entrada. También debe especificar las direcciones IP o las subredes de las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloqueará este puerto e impedirá que el equipo reciba solicitudes de Escritorio remoto. Si un administrador intenta abrir este puerto agregándolo a una lista de excepciones de puerto local, Firewall de Windows no abre el puerto.
  
En algunos ataques se puede aprovechar un puerto 3389 abierto. Para mantener las capacidades de administración mejorada que proporciona Escritorio remoto, debe establecer esta configuración como **Habilitada** y especificar las direcciones IP y las subredes de los equipos utilizados para la administración remota. Los equipos de su entorno deben aceptar las solicitudes de Escritorio remoto del menor número de equipos posible.
  
##### Firewall de Windows: permitir excepción de entorno UPnP (Perfil estándar)
  
**Tabla A.48: Configuración de autorización de excepción de entorno UPnP con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepción de entorno UPnP** permite a un equipo recibir mensajes Plug and Play no solicitados procedentes de dispositivos de red, tales como enrutadores con servidores de seguridad integrados. Para recibir estos mensajes, Firewall de Windows abre el puerto TCP 2869 y el puerto UDP 1900.
  
Si habilita esta configuración de directiva, Firewall de Windows abre estos puertos para que el equipo pueda recibir los mensajes Plug and Play. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes. Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo reciba mensajes Plug and Play.
  
El bloqueo del tráfico de red UPnP reduce de forma eficaz la superficie de ataque de un equipo. Esta configuración siempre debe estar **Deshabilitada** en redes que no son de confianza.
  
##### Firewall de Windows: no permitir notificaciones (Perfil estándar)
  
**Tabla A.49: Configuración de prohibición de notificaciones con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
Firewall de Windows puede mostrar notificaciones a los usuarios cuando un programa solicita que Firewall de Windows agregue el programa a la lista de excepciones de programa. Esta situación se produce cuando los programas intentan abrir un puerto y no se les permite, con arreglo a las reglas actuales de Firewall de Windows. La configuración **Firewall de Windows: no permitir notificaciones** establece si se muestran estos parámetros a los usuarios.
  
Si establece esta directiva como **Habilitada**, Firewall de Windows impide que se muestren estas notificaciones. Si se establece como **Deshabilitada**, Firewall de Windows permite que se muestren estas notificaciones.
  
A menudo, a los usuarios no se les permitirá agregar aplicaciones y puertos en respuesta a estos mensajes en entornos de empresa o de alta seguridad. En tales casos, este mensaje informará al usuario de que ocurre algo sobre lo que no tienen control. En esas situaciones debe establecer esta opción como **Habilitada**. En otros entornos en los que la configuración del usuario permite excepciones, deberá establecer esta opción como **Deshabilitada**.
  
##### Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión (Perfil estándar)
  
**Tabla A.50: Configuración de prohibición de respuesta de monodifusión con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión** impide que un equipo reciba respuestas de monodifusión a sus mensajes salientes de difusión o multidifusión. Cuando esta configuración de directiva está habilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows bloquea las respuestas de monodifusión enviadas por esos otros equipos. Cuando la configuración está deshabilitada y este equipo envía un mensaje de difusión o multidifusión a otros equipos, Firewall de Windows espera hasta tres segundos respuestas de monodifusión de los otros equipos y después bloquea todas las respuestas posteriores.
  
Normalmente, no deseará respuestas de monodifusión a mensajes de difusión o multidifusión. Tales respuestas pueden indicar un ataque de denegación de servicio (DoS) o que un atacante intenta sondear un equipo activo conocido. En este apéndice se recomienda que establezca esta configuración de directiva como **Habilitada** como ayuda para prevenir este tipo de ataques.
  
**Nota** : esta configuración de directiva no surte efecto si el mensaje de monodifusión es una respuesta a un mensaje de difusión de Protocolo de configuración dinámica de host (DHCP) enviado por el equipo. Firewall de Windows permite siempre esas respuestas de monodifusión DHCP. Sin embargo, esta configuración de directiva puede interferir en los mensajes NetBIOS que detectan conflictos de nombres.
  
##### Firewall de Windows: definir excepciones de puerto (Perfil estándar)
  
**Tabla A.51: Configuración de definición de excepciones de puerto con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
</tbody>
</table>
  
La lista de excepciones de puerto de Firewall de Windows debe ser definida por Directiva de grupo, de modo que pueda administrar e implementar de forma centralizada las excepciones de puerto, y asegurarse de que los administradores locales no crean configuraciones menos seguras. La configuración de directiva **Firewall de Windows: definir excepciones de puerto** le permite administrar de forma centralizada estas configuraciones.
  
Si habilita esta configuración de directiva, puede ver y cambiar la lista de excepciones de puerto definida por Directiva de grupo. Para ver y modificar la lista de excepciones de puerto, establezca la configuración de directiva como **Habilitada** y haga clic en el botón **Mostrar**. Tenga en cuenta que si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores, lo que significa que puede crear accidentalmente varias entradas para el mismo puerto y que entren en conflicto los valores de Ámbito o Estado.
  
Si deshabilita esta configuración de directiva, la lista de excepciones de puerto definida por Directiva de grupo se elimina, pero otras configuraciones de directiva pueden seguir abriendo o bloqueando puertos. Asimismo, si existe una lista de excepciones de puerto local, se pasa por alto a menos que habilite la configuración de directiva **Firewall de Windows: permitir excepciones de puerto local**.
  
Para los entornos con aplicaciones no estándar que requieren que se abran determinados puertos debe considerarse la posibilidad de implementar excepciones de programa. En este apéndice se recomienda habilitar esta configuración y especificar una lista de excepciones de puerto sólo cuando no se pueden definir excepciones de programa. Las excepciones de programa permiten que Firewall de Windows acepte tráfico de red no solicitado únicamente mientras se ejecuta el programa especificado, y que a través de las excepciones de puerto se mantengan abiertos en todo momento los puertos especificados.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
##### Firewall de Windows: permitir excepciones de puerto local (Perfil estándar)
  
**Tabla A.52: Configuración de autorización de excepciones de puerto local con Perfil estándar**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa: Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa: Portátil</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Escritorio</th>
<th style="border:1px solid black;" >Nivel de seguridad alto: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **Firewall de Windows: permitir excepciones de puerto local** permite a los administradores utilizar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de puerto local. Firewall de Windows puede utilizar dos listas de excepciones de puerto; la otra se define mediante la configuración de directiva **Firewall de Windows: definir excepciones de puerto**.
  
Si habilita esta configuración de directiva, el componente del Panel de control Firewall de Windows permite a los administradores definir una lista de excepciones de puerto local. Si deshabilita esta configuración de directiva, el componente del Panel de control Firewall de Windows no permite a los administradores definir esa lista.
  
Normalmente, los administradores locales no tienen autoridad para anular las directivas organizativas y establecer sus propia listas de excepciones de puertos en los entornos de empresa o de alta seguridad. Por eso, en este apéndice se recomienda configurar esta opción como **Deshabilitada**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Parámetros de Configuración de usuario
  
En las restantes secciones de este apéndice se tratan las opciones de configuración de usuario. Aplique las opciones de configuración a través de un GPO (objeto de directiva de grupo) vinculado a una unidad organizativa que contenga cuentas de usuario.
  
**Nota**: las opciones de configuración de usuario se aplican a cualquier cliente en que un usuario inicia sesión en un dominio de servicio de directorio de Microsoft Active Directory. Las opciones de configuración de equipo se aplican a todos los clientes controlados por un GPO en Active Directory, independientemente del usuario que inicie sesión en el cliente. Por este motivo, las tablas de esta sección sólo contienen la configuración recomendada para los entornos de cliente de empresa y de alta seguridad definidos en esta guía. No existen recomendaciones de equipo de escritorio o portátil para estas configuraciones.
  
#### Administrador de datos adjuntos
  
Utilice el Editor de objetos de directiva de grupo para configurar la Plantilla administrativa apropiada. La configuración recomendada se encuentra en la ubicación siguiente:
  
Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Administrador de datos adjuntos
  
##### No conservar la información de zona en los datos adjuntos de archivos
  
**Tabla A.53: Configuración de no conservación de información de zona**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Nivel de seguridad alto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
La configuración **No conservar la información de zona en los datos adjuntos de archivos** le permite administrar si Windows debe marcar archivos adjuntos de Internet Explorer o de Outlook Express con información acerca de su zona de origen (restringida, Internet, intranet o local). Esta configuración requiere que los archivos sean descargados en particiones de disco NTFS para funcionar correctamente. Si no se conserva la información de zona, Windows no puede realizar apropiadamente evaluaciones de riesgo basadas en la zona de procedencia del archivo adjunto.
  
Si se establece esta configuración como **Habilitada**, no se marcarán los archivos adjuntos con información de zona. Si se establece la configuración como **Deshabilitada**, Windows deberá almacenar los archivos adjuntos con la información de zona correspondiente. Dado que los archivos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza, como la zona Internet, en este apéndice se recomienda establecer la configuración como **Deshabilitada** para asegurarse de que se conserva la máxima cantidad de información de seguridad posible con cada archivo.
  
##### Ocultar mecanismos para eliminar la información de zona
  
**Tabla A.54: Configuración de mecanismos para quitar la información de zona**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Nivel de seguridad alto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
La configuración de directiva **Ocultar mecanismos para eliminar la información de zona** le permite administrar si los usuarios pueden quitar manualmente la información de zona de los archivos adjuntos guardados haciendo clic en el botón **Desbloquear** en la hoja de **Propiedades** del archivo o activando una casilla de verificación en el cuadro de diálogo **Advertencia de seguridad**. Al quitar la información de la zona, los usuarios pueden abrir archivos adjuntos potencialmente peligrosos que Windows ha impedido que se abran.
  
Windows oculta la casilla de verificación y el botón **Desbloquear** cuando esta configuración de directiva está **Habilitada.** Cuando la configuración se establece como **Deshabilitada**, Windows muestra la casilla de verificación y el botón **Desbloquear**. Dado que los archivos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza, como la zona Internet, en este apéndice se recomienda establecer la configuración como **Habilitada** para asegurarse de que se conserva la máxima cantidad de información de seguridad posible con cada archivo.
  
**Nota**: para configurar si los archivos deben guardarse con información de zona, vea la configuración de directiva anterior **No conservar la información de zona en los datos adjuntos de archivos.**
  
##### Notificar a los programas antivirus cuando se abren datos adjuntos
  
**Tabla A.55: Configuración de notificación a los programas antivirus**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Nivel de seguridad alto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Los programas antivirus empiezan a ser obligatorios en la mayoría de los entornos y constituyen una sólida línea defensiva contra los ataques actuales. La configuración de directiva **Notificar a los programas antivirus cuando se abren datos adjuntos** le permite administrar el comportamiento con respecto a la notificación de programas antivirus registrados.
  
Cuando está establecida como **Habilitada**, esta configuración de directiva determina que Windows llame al programa antivirus registrado para que analice los archivos adjuntos cuando los abren los usuarios. Si el análisis del antivirus no se lleva a cabo satisfactoriamente, se impide que se puedan abrir los archivos adjuntos. Si esta configuración de directiva está establecida como **Deshabilitada**, Windows no llama al programa antivirus registrado cuando se abren archivos adjuntos.
  
Para procurar que los programas de detección de virus examinen todos los archivos antes de que sean abiertos, en este apéndice se recomienda establecer esta directiva como **Habilitada** en todos los entornos.
  
**Nota**: debe haber instalado un programa antivirus actualizado para que esta configuración funcione correctamente. Muchos programas antivirus actualizados utilizan nuevas API que se incluyen con SP2.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Las numerosas mejoras relacionadas con la capacidad de administración de los servicios de seguridad en Windows XP SP2 permiten a los administradores implementar parámetros de configuración de seguridad más específicos para usuarios y equipos. En este apéndice se ilustran las configuraciones más importantes que deben utilizarse para aumentar el nivel de seguridad en un entorno SP2. Aunque en el apéndice no se describan todas las configuraciones posibles, las especificadas son las que pueden tener repercusiones directas y de gran alcance en su entorno.
  
Recuerde que SP2 representa un cambio considerable con respecto a versiones anteriores de Windows, y es probable que surjan problemas de compatibilidad de aplicaciones en su entorno. Debe probar cuidadosamente todas las configuraciones recomendadas antes de implementarlas. Aunque estas configuraciones se hayan probado exhaustivamente para asegurarse de que funcionan en los entornos especificados, el mejor método consiste en probarlas en su entorno en particular.
  
[](#mainsection)[Principio de la página](#mainsection)
