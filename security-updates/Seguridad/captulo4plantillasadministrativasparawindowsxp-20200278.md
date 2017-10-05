---
TOCTitle: 'Capítulo 4: Plantillas administrativas para Windows XP'
Title: 'Capítulo 4: Plantillas administrativas para Windows XP'
ms:assetid: 'adb79ec2-691f-4a9f-b940-36d2d9807fd7'
ms:contentKeyID: 20200278
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163076(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 4: Plantillas administrativas para Windows XP

Actualizado: 20/10/05

##### En esta página

[](#edaa)[Información general](#edaa)
[](#ecaa)[Parámetros de Configuración del equipo](#ecaa)
[](#ebaa)[Parámetros de Configuración de usuario](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

En este capítulo se describe en detalle cómo configurar y aplicar parámetros de seguridad adicionales a Microsoft® Windows® XP Professional con Service Pack 2 (SP2) mediante plantillas administrativas. Los archivos de plantilla administrativa (.adm) se utilizan para establecer la configuración en el Registro de Windows XP, que rige el comportamiento de un gran cantidad de servicios, aplicaciones y componentes de este sistema operativo.

Cinco de las plantillas administrativas que se suministran con Windows XP SP2 incluyen centenares de parámetros adicionales que puede utilizar para mejorar la seguridad de Windows XP Professional. Existen varios parámetros en las plantillas administrativas de Microsoft Windows Server™ 2003 que no funcionan con Windows XP. Para obtener una lista completa de todos los parámetros de las plantillas administrativas disponibles en Windows XP, consulte el libro en Microsoft Excel Excel® "Policy Settings" que se menciona en la sección “Información adicional” al final de este módulo.

En la siguiente tabla se enumeran los archivos .adm, además de mostrarse las aplicaciones y los servicios que se ven afectados.

**Tabla 4.1. Archivos de plantilla administrativa**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de archivo</th>
<th style="border:1px solid black;" >Sistema operativo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">System.adm</td>
<td style="border:1px solid black;">Windows XP Professional</td>
<td style="border:1px solid black;">Contiene un gran número de parámetros para personalizar el entorno operativo del usuario.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inetres.adm</td>
<td style="border:1px solid black;">Windows XP Professional</td>
<td style="border:1px solid black;">Contiene parámetros de configuración para Internet Explorer 6.0.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Conf.adm</td>
<td style="border:1px solid black;">Windows XP Professional</td>
<td style="border:1px solid black;">Contiene parámetros para configurar Microsoft NetMeeting®.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Wmplayer.adm</td>
<td style="border:1px solid black;">Windows XP Professional</td>
<td style="border:1px solid black;">Contiene parámetros para configurar el Reproductor de Windows Media.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Wuau.adm</td>
<td style="border:1px solid black;">Windows XP Professional</td>
<td style="border:1px solid black;">Contiene parámetros para configurar Windows Update.</td>
</tr>
</tbody>
</table>
  
**Nota**: debe configurar manualmente los parámetros de plantillas administrativas en el objeto de directiva de grupo (GPO) para aplicarlos a los equipos y usuarios del entorno.
  
Hay dos grupos principales de parámetros de configuración en las plantillas administrativas:
  
-   Parámetros de Configuración del equipo (almacenados en el subárbol del registro **HKEY\_Local\_Machine**).
  
-   Parámetros de Configuración de usuario (almacenados en el subárbol del registro **HKEY\_Current\_User**).
  
Al igual que en el capítulo 3, "Configuración de seguridad para clientes Windows XP", se incluyen recomendaciones de configuración para los entornos Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF) que se definen en esta guía.
  
**Nota**: los parámetros de usuario se aplican a una unidad organizativa (UO), que contiene usuarios, a través de un GPO vinculado. Consulte el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory" para obtener detalles adicionales acerca de esta unidad organizativa.
  
Algunos parámetros se encuentran disponibles en Configuración del equipo y Configuración de usuario en el Editor de objetos de directiva de grupo. Si se aplica un parámetro a un usuario que inicia sesión en un equipo al que se ha aplicado la misma configuración de equipo anteriormente a través de Directiva de grupo, el parámetro de Configuración de equipo tiene prioridad sobre el parámetro de Configuración de usuario.
  
En versiones anteriores de esta guía figuraba información para la configuración de Office XP. Sin embargo, estos parámetros de configuración se han actualizado para Office 2003 y están disponibles en el sitio web de Microsoft. Consulte la sección "Información adicional" al final de este capítulo, donde encontrará vínculos a esta información.
  
En este capítulo no se describen todos los parámetros disponibles en las plantillas administrativas facilitadas por Microsoft; muchos pertenecen a la interfaz de usuario (IU) y no están específicamente asociados a la seguridad. Tenga en cuenta qué configuraciones de parámetros recomendadas en estas instrucciones son aplicables a su entorno en función de los objetivos de seguridad de su organización.
  
Si desea aplicar parámetros adicionales a través de Directiva de grupo en Windows XP Professional, podrá desarrollar plantillas personalizadas. Consulte las notas del producto que se enumeran en la sección “Información adicional”, al final de este capítulo, para obtener información detallada acerca de cómo desarrollar sus propias plantillas administrativas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Parámetros de Configuración del equipo
  
Las siguientes secciones tratan los parámetros que se recomienda en Configuración del equipo, en el Editor de objetos de directiva de grupo. Para configurarlos, diríjase a la siguiente ubicación:
  
**Configuración del equipo\\Plantillas administrativas**
  
Esta ubicación se muestra en contexto en la figura siguiente:
  
[![](images/Cc163076.SGFG0401(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0401_big(es-es,technet.10).gif)
  
**Figura 4.1 Estructura de Directiva de grupo para Configuración del equipo**
  
La estructura de este capítulo se basa en la de contenedores de Directiva de grupo. En las tablas de las siguientes secciones se resumen las recomendaciones de parámetros para diversas opciones de Configuración del equipo. Además, se proporcionan recomendaciones tanto para equipos de escritorio como portátiles en dos tipos de entornos seguros: el de Cliente de empresa (EC) y el de Seguridad especializada: Funcionalidad limitada (SSLF). En las subsecciones que siguen a cada tabla se proporciona información más detallada acerca de cada una de las configuraciones.
  
Aplique estos parámetros a través de un GPO vinculado a una unidad organizativa que contenga las cuentas de equipo del entorno. Incluya los parámetros del equipo portátil en el GPO vinculado a la unidad organizativa de equipos portátiles y los parámetros del equipo de escritorio en el GPO vinculado a la unidad organizativa equipos de escritorio.
  
#### Componentes de Windows
  
En la figura siguiente se ilustran las secciones de Directiva de grupo que se verán afectadas por los cambios de configuración en este apartado:
  
[![](images/Cc163076.SGFG0402(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0402_big(es-es,technet.10).gif)
  
**Figura 4.2 Estructura de Directiva de grupo para Componentes de Windows en Configuración del equipo**
  
##### NetMeeting
  
Microsoft NetMeeting permite que los usuarios mantengan reuniones virtuales en la red de la organización. Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**NetMeeting**
  
**Tabla 4.2 Configuración recomendada para NetMeeting**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar el uso compartido de escritorio remoto</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Desactivar el uso compartido de escritorio remoto
  
Esta configuración de directiva deshabilita la característica de uso compartido de escritorio remoto que ofrece NetMeeting. Si habilita esta configuración de directiva, los usuarios no podrán configurar NetMeeting para permitir el control remoto del escritorio local.
  
El parámetro **Desactivar el uso compartido de escritorio remoto** se establece como **No configurado** para el entorno EC. Sin embargo, se configura como **Habilitado** para el entorno SSLF con objeto de evitar que los usuarios compartan escritorios de forma remota a través de NetMeeting.
  
##### Internet Explorer
  
Las directivas de grupo de Microsoft Internet Explorer le ayudan a cumplir los requisitos de seguridad de las estaciones de trabajo Windows XP, así como a evitar el intercambio de contenido no deseado a través de Internet Explorer. Utilice los siguientes criterios para proteger Internet Explorer en las estaciones de trabajo del entorno:
  
-   Asegúrese de que las peticiones a Internet sólo se producen como respuesta directa a acciones del usuario.
  
-   Asegúrese de que la información enviada a sitios web específicos sólo llega a los mismos, a menos que se produzcan acciones concretas del usuario que permiten la transmisión de información a otros destinos.
  
-   Asegúrese de que los canales de confianza a servidores o sitios están identificados con toda claridad junto con el propietario de los mismos en cada canal.
  
-   Asegúrese de que cualquier secuencia de comandos o programa que funcione con Internet Explorer se ejecuta en un entorno restringido. Puede ser que los programas enviados a través de canales de confianza estén habilitados para funcionar fuera del entorno restringido.
  
Puede establecer la siguiente configuración de equipo recomendada para Internet Explorer en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**
  
En la tabla siguiente se resumen muchas de las recomendaciones sobre la configuración de Internet Explorer. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.3 Configuración recomendada de Internet Explorer**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la instalación automática de componentes de Internet Explorer</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir que usuarios habiliten ni deshabiliten complementos</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configuración de proxy por equipo y no por usuario</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zonas de seguridad: no permitir que los usuarios cambien las directivas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zonas de seguridad: usar sólo la configuración del equipo</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la detección de bloqueos</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Deshabilitar la instalación automática de componentes de Internet Explorer
  
Si habilita esta configuración de directiva, Internet Explorer no podrá descargar componentes cuando los usuarios exploren sitios web que requieran los componentes para funcionar completamente. Si esta configuración de directiva se deshabilita o no está configurada, se preguntará a los usuarios si desean descargar e instalar los componentes cada vez que visiten sitios web que los utilicen.
  
El parámetro **Deshabilitar la instalación automática de componentes de Internet Explorer** se configura como **Habilitado** para los dos entornos que se tratan en el capítulo.
  
**Nota**: antes de habilitar esta configuración de directiva, Microsoft recomienda que configure una estrategia alternativa para actualizar Internet Explorer a través de Microsoft Update o un servicio semejante.
  
###### Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer
  
Si habilita esta configuración de directiva, Internet Explorer no podrá determinar si hay disponible una versión posterior del explorador y avisar a los usuarios en ese caso. Si esta configuración de directiva se deshabilita o no está configurada, Internet Explorer buscará actualizaciones cada 30 días (su configuración predeterminada) y avisará a los usuarios si hay una versión nueva disponible.
  
El parámetro **Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: antes de habilitar esta configuración de directiva, Microsoft le recomienda que configure una estrategia alternativa para los administradores de su organización con el fin de asegurar que acepten periódicamente nuevas actualizaciones para Internet Explorer en los equipos cliente del entorno.
  
###### Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa
  
Esta configuración de directiva especifica que los programas que utilizan los canales de distribución de software de Microsoft no avisarán a los usuarios cuando instalen nuevos componentes. Los canales de distribución de software se utilizan para actualizar el software dinámicamente en los equipos de los usuarios; esta funcionalidad se basa en tecnologías de distribución abierta de software (OSD).
  
El parámetro **Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
###### No permitir que usuarios habiliten ni deshabiliten complementos
  
Esta configuración de directiva le permite administrar si los usuarios tienen la capacidad de permitir o denegar complementos a través de Administrar complementos. Si se establece esta configuración de directiva como **Habilitada**, los usuarios no podrán habilitar ni deshabilitar los complementos a través de la característica Administrar complementos. La única excepción se produce si un complemento se ha introducido específicamente en la configuración de directiva **Lista de complementos** de manera que los usuarios puedan seguir administrando el complemento. En tal caso, el usuario aún puede administrar el complemento a través de Administrar complementos. Si establece esta configuración de directiva como **Deshabilitada**, el usuario podrá habilitar o deshabilitar complementos.
  
**Nota**: para obtener más información acerca de cómo administrar complementos de Internet Explorer en Windows XP SP2, vea el artículo 883256 de Microsoft Knowledge Base acerca de [cómo administrar complementos de Internet Explorer en Windows XP Service Pack 2](http://support.microsoft.com/?kbid=883256), en http://support.microsoft.com/?kbid=883256.
  
Es habitual que los usuarios decidan instalar complementos no permitidos por una directiva de seguridad de la organización. Dichos complementos pueden suponer un riesgo considerable para la seguridad y la privacidad en la red. Por lo tanto, esta configuración de directiva se establece como **Habilitada** para los dos entornos que se tratan en esta guía.
  
**Nota**: debe revisar la configuración de GPO en Internet Explorer\\Características de seguridad\\Administración de complementos para asegurarse de que en su entorno aún se pueden ejecutar los complementos autorizados que corresponda. Por ejemplo, quizá le interese leer el artículo de Microsoft Knowledge Base en el que se describe que [Outlook Web Access y Lugar de trabajo remoto en Web de Small Business Server no funcionan si el bloqueo de complementos de XP Service Pack 2 se habilita a través de directiva de grupo](http://support.microsoft.com/default.aspx?kbid=555235), en http://support.microsoft.com/default.aspx?kbid=555235.
  
###### Configuración de proxy por equipo y no por usuario
  
Si habilita esta configuración de directiva, no se permitirá a los usuarios alterar parámetros de configuración de proxy específicos del usuario. Deben utilizar las zonas que se crean para todos los usuarios de los equipos a los que tienen acceso.
  
El parámetro **Configuración de proxy por equipo y no por usuario** se establece como **Habilitado** para equipos cliente de escritorio en los dos entornos que se tratan en este capítulo. Sin embargo, la configuración de directiva está configurada como **Deshabilitada** para equipos cliente portátiles porque los usuarios móviles quizá tengan que cambiar su configuración de proxy cuando viajan.
  
###### Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios
  
Habilite esta configuración de directiva para deshabilitar los parámetros de administración de sitios para zonas de seguridad. (Para ver la configuración de la administración de sitios para las zonas de seguridad, abra Internet Explorer, seleccione **Herramientas** y después **Opciones de Internet**, haga clic en la etiqueta **Seguridad** y, a continuación, en **Sitios**). Si esta configuración de directiva se deshabilita o no se establece, los usuarios podrán agregar o quitar sitios web en las zonas de **Sitios de confianza** y **Sitios restringidos** , así como alterar la configuración en la zona de **Intranet local.**
  
El parámetro **Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: si habilita el parámetro **Deshabilitar la página Seguridad** (que se ubica en Configuración de usuario  
\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet), la etiqueta **Seguridad** se quita de la interfaz y el parámetro **Deshabilitar** tiene prioridad sobre este parámetro de **Zonas de seguridad**.
  
###### Zonas de seguridad: no permitir que los usuarios cambien las directivas
  
Si habilita esta configuración de directiva, se deshabilita el botón **Nivel personalizado** y el control deslizante de **Nivel de seguridad de la zona** en la etiqueta **Seguridad** en el cuadro de diálogo **Opciones de Internet**. Si esta configuración de directiva se deshabilita o no está configurada, los usuarios podrán cambiar la configuración de las zonas de seguridad. Evita que los usuarios cambien la configuración de la zona de seguridad establecida por el administrador.
  
El parámetro **Zonas de seguridad: no permitir que los usuarios cambien las directivas** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: Si habilita el parámetro **Deshabilitar la página Seguridad** (que se ubica en Configuración de usuario  
\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet), la etiqueta **Seguridad** se quita de Internet Explorer en el Panel de control y el parámetro **Deshabilitar** tiene prioridad sobre este parámetro de **Zonas de seguridad**.
  
###### Zonas de seguridad: usar sólo la configuración del equipo
  
Esta configuración de directiva afecta a la forma en que se aplican los cambios de zona de seguridad a diferentes usuarios. Se pretende asegurar que la configuración de la zona de seguridad está presente de modo uniforme en el mismo equipo y que no varía de usuario a usuario. Si habilita esta configuración de directiva, los cambios que realice un usuario en una zona de seguridad se aplicarán a todos los usuarios de ese equipo. Si esta configuración de directiva se deshabilita o no se establece, los usuarios del mismo equipo podrán establecer su propia configuración de zona de seguridad.
  
El parámetro **Zonas de seguridad: usar sólo la configuración del equipo** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
###### Desactivar la detección de bloqueos
  
Esta configuración de directiva le permite administrar la característica de detección de bloqueos en la administración de complementos de Internet Explorer. Si habilita esta configuración de directiva, un bloqueo en Internet Explorer será similar al de un equipo en el que se ejecuta Windows XP Professional con Service Pack 1 (SP1) o versiones anteriores: se invocará el Informe de errores de Windows. Si deshabilita esta configuración de directiva, funcionará la característica de detección de bloqueos en la administración de complementos.
  
Dado que los informes de bloqueos de Internet Explorer podrían contener información confidencial de la memoria del equipo, el parámetro **Desactivar la detección de bloqueos** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo. Si experimenta bloqueos frecuentes y necesita informar de éstos para la solución de problemas en fase de seguimiento, podría establecer temporalmente la configuración de directiva como **Deshabilitada.**
  
##### Internet Explorer\\Panel de control Internet\\Página Seguridad
  
Puede establecer esta configuración del equipo en la siguiente ubicación en el Editor de objetos de directiva de grupo:
  
**\\Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Página Seguridad**
  
SP2 introdujo varias configuraciones de directiva nuevas para ayudarle a proteger la configuración de zonas de Internet Explorer en su entorno. Los valores predeterminados de estas configuraciones proporcionan mecanismos de seguridad mejorados con respecto a versiones anteriores de Windows. Sin embargo, quizá desee revisar estas configuraciones para determinar si desea que sean requeridas en mayor o menor medida en su entorno a fin de facilitar el uso o la compatibilidad con aplicaciones.
  
Por ejemplo, SP2 configura Internet Explorer para que se bloqueen de forma predeterminada los elementos emergentes en todas las zonas de Internet. Quizá desee asegurarse de que esta configuración de directiva se aplica en todos los equipos de su entorno para evitar la aparición de ventanas emergentes y reducir la posibilidad de instalaciones de software espía y malintencionado que a menudo se inician desde sitios web de Internet. Por otra parte, existe la posibilidad de que su entorno contenga aplicaciones que requieren el uso de elementos emergentes para funcionar. En ese caso, podría configurar esta directiva para permitir elementos emergentes de sitios web de la intranet.
  
##### Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**\\Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas**
  
**Tabla 4.4 Configuración recomendada de permiso para ejecutar software**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir que el software se ejecute o instale incluso si la firma no es válida</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
###### Permitir que el software se ejecute o instale incluso si la firma no es válida
  
Los controles Microsoft ActiveX® y los archivos que se descargan suelen tener adjuntas firmas digitales que garantizan tanto la integridad del archivo como la identidad del firmante (creador) del software. Estas firmas ayudan a asegurar que se descarga software no modificado y que el usuario pueda identificar al firmante para determinar si confía en éste lo suficiente como para ejecutar su software.
  
El parámetro **Permitir que el software se ejecute o instale incluso si la firma no es válida** le permite controlar si el software descargado puede ser instalado o ejecutado por los usuarios aunque la firma no sea válida. Una firma no válida podría indicar que alguien ha manipulado el archivo. Si habilita esta configuración de directiva, se preguntará a los usuarios si desean instalar o ejecutar los archivos cuya firma no es válida. Si deshabilita esta configuración de directiva, los usuarios no podrán ejecutar ni instalar archivos cuya firma no sea válida.
  
Puesto que el software sin firmar puede crear una vulnerabilidad de seguridad, esta configuración de directiva se establece como **Deshabilitada** para los dos entornos que se tratan en este capítulo.
  
**Nota**: puede haber software y controles legítimos con firma no válida, aunque sean correctos. Deberá probar cuidadosamente ese software en un entorno aislado antes de permitir su uso en la red de la organización.
  
##### Internet Explorer\\Características de seguridad\\Restricción de seguridad del protocolo MK
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Restricción de seguridad del protocolo MK**
  
**Tabla 4.5 Configuración recomendada del protocolo MK**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Protocolo MK)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Protocolo MK)
  
Esta configuración de directiva reduce el área de superficie de ataque al bloquear el protocolo MK, que raramente se utiliza. Algunas aplicaciones web más antiguas utilizan el protocolo MK para recuperar información de archivos comprimidos. Si establece esta configuración de directiva como **Habilitada**, se bloqueará el protocolo MK para el Explorador de Windows e Internet Explorer, lo que provocará errores de los recursos que utilizan el protocolo MK. Si deshabilita esta configuración de directiva, permitirá a otras aplicaciones que utilicen la API del protocolo MK.
  
Dado que el protocolo de MK no se utiliza de forma generalizada, debe bloquearse siempre que no se necesite. Esta configuración de directiva se establece como **Habilitada** para los dos entornos que se tratan en este capítulo. Microsoft recomienda bloquear el protocolo MK, a menos que lo necesite específicamente en su entorno.
  
**Nota**: dado que se producirá un error en los recursos que utilizan el protocolo MK cuando implemente esta configuración de directiva, debe asegurarse de que ninguna de sus aplicaciones utiliza el protocolo.
  
##### Internet Explorer\\Características de seguridad\\Administración de MIME consistente
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Administración de MIME consistente**
  
**Tabla 4.6 Configuración recomendada para Administración de MIME consistente**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Administración de MIME consistente)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Administración de MIME consistente)
  
Internet Explorer utiliza datos MIME (Extensiones seguras multipropósito de correo de Internet) para determinar los procedimientos de administración de archivos que se reciben a través de un servidor web. El parámetro **Administración de MIME consistente** determina si Internet Explorer debe requerir que toda la información de tipo de archivo proporcionada por los servidores web sea coherente. Por ejemplo, si el tipo MIME de un archivo es texto/sin formato pero los datos MIME indican que el archivo es realmente un archivo ejecutable, Internet Explorer cambia su extensión para reflejar el estado ejecutable. Esta capacidad ayuda a asegurar que ese código ejecutable no se haga pasar por otros tipos de datos en los que se puede confiar.
  
Si habilita esta configuración de directiva, Internet Explorer examina todos los archivos recibidos y exige que tengan datos MIME coherentes. Si deshabilita o no establece esta configuración de directiva, Internet Explorer no requerirá que los datos MIME sean coherentes en todos los archivos recibidos y utilizará los datos MIME que proporciona el archivo.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Debe asegurarse de que estos archivos son coherentes y están debidamente etiquetados como medida para evitar descargas de archivos malintencionados que pueden infectar su red. Esta configuración de directiva se establece como **Habilitada** para los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva funciona conjuntamente con los parámetros de las **Características de seguridad de examen de MIME**, pero no los reemplaza.
  
##### Internet Explorer\\Características de seguridad\\Características de seguridad de examen de MIME
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Características de seguridad de examen de MIME**
  
**Tabla 4.7 Configuración recomendada para Examen de MIME**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Examen de MIME)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Examen de MIME)
  
El examen de MIME es un proceso en el que se evalúa el contenido de un archivo MIME para determinar su contexto (si se trata de un archivo de datos, de un archivo ejecutable o de algún otro tipo de archivo). Esta configuración de directiva determina si el examen de MIME de Internet Explorer evitará la conversión de un archivo de un tipo determinado a otro tipo más peligroso. Cuando se establece como **Habilitada**, la función de examen de MIME nunca convertirá un archivo de un tipo a otro tipo de archivo más peligroso. Si deshabilita esta configuración de directiva, el examen de MIME configura los procesos de Internet Explorer de modo que permitan la conversión de un archivo de un tipo determinado a otro tipo de archivo más peligroso. Por ejemplo, un archivo de texto podría ser convertido en un archivo ejecutable, lo cual resulta peligroso porque se ejecutaría cualquier código que hubiera en el supuesto archivo de texto.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Microsoft recomienda asegurarse de que estos archivos se tratan de un modo coherente como medida para evitar descargas de archivos malintencionados que pueden infectar su red.
  
El parámetro **Procesos de Internet Explorer (Examen de MIME)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva funciona conjuntamente con los parámetros de **Administración de MIME consistente**, pero no los reemplaza.
  
##### Internet Explorer\\Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos**
  
**Tabla 4.8 Configuración recomendada de restricciones de seguridad de ventanas con secuencias de comandos**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Restricciones de seguridad de ventanas con secuencias de comandos)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Restricciones de seguridad de ventanas con secuencias de comandos)
  
Internet Explorer permite que mediante secuencias de comandos se abran distintos tipos de ventanas, así como que se cambie su tamaño y posición. Hay sitios web de mala reputación que cambian el tamaño de las ventanas para ocultar otras o que obligan al visitante a interaccionar con una ventana que contiene código malintencionado.
  
El parámetro **Procesos de Internet Explorer** (**Restricciones de seguridad de ventanas con secuencias de comandos**) restringe las ventanas emergentes e impide que a través de secuencias de comandos se muestren ventanas en las que las barras de título y estado no son visibles para el usuario o que se oculten las barras de título y estado de otras ventanas. Si habilita esta configuración de directiva, no se mostrarán ventanas emergentes en el Explorador de Windows ni en los procesos de Internet Explorer. Si deshabilita o no establece esta configuración de directiva, las secuencias de comandos aún podrán crear ventanas emergentes y ventanas que oculten a otras.
  
El parámetro **Procesos de Internet Explorer** **(Restricciones de seguridad de ventanas con secuencias de comandos)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo. Cuando está habilitada, esta configuración de directiva dificulta que desde sitios web malintencionados se controlen sus ventanas de Internet Explorer o se engañe a los usuarios para que hagan clic en una ventana indebidamente.
  
##### Internet Explorer\\Características de seguridad\\Protección contra elevación de zona
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Protección contra elevación de zona**
  
**Tabla 4.9 Configuración recomendada para la protección contra elevación de zona**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Protección contra elevación de zona)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Protección contra elevación de zona)
  
Internet Explorer establece restricciones para cada página web que abre. Estas restricciones dependen de la ubicación de la página web (zona Internet, zona de intranet o zona Máquina local). Las páginas web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Máquina local, lo que convierte a la zona de seguridad Máquina local en un objetivo prioritario para los atacantes malintencionados.
  
Si habilita el parámetro **Procesos de Internet Explorer (Protección contra elevación de zona)**, se puede proteger cualquier zona de modo que los procesos de Internet Explorer no puedan llevar a cabo una elevación de zona. Con este método se impide que se apliquen privilegios elevados de una zona al contenido de otra. Si deshabilita esta configuración de directiva, ninguna zona recibirá ese tipo de protección en los procesos de Internet Explorer.
  
A causa de la gravedad y relativa frecuencia de los ataques de elevación de zona, el parámetro **Procesos de Internet Explorer (Protección contra elevación de zona)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Internet Explorer\\Características de seguridad\\Limitar la instalación de ActiveX
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Limitar la instalación de ActiveX**
  
**Tabla 4.10 Configuración de limitación de la instalación de ActiveX**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Limitar la instalación de ActiveX)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Limitar la instalación de ActiveX)
  
Esta configuración de directiva proporciona la capacidad de bloquear mensajes de instalación de controles ActiveX para procesos de Internet Explorer. Si habilita esta configuración de directiva, se bloquearán los mensajes de instalación de controles de ActiveX en procesos de Internet Explorer. Si deshabilita esta configuración de directiva, no se bloquearán los mensajes de instalación de controles de ActiveX, de modo que los usuarios verán esos mensajes.
  
A menudo, los usuarios deciden instalar software (como, por ejemplo, controles de ActiveX) que no permite la directiva de seguridad de su organización. Ese tipo de software puede entrañar riesgos considerables para la seguridad y la privacidad en las redes. Por lo tanto, el parámetro **Procesos de Internet Explorer (Limitar la instalación de ActiveX)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva impide también que los usuarios instalen controles legítimos de ActiveX que interfieran en el funcionamiento de componentes importantes del sistema, como Windows Update. Si habilita esta configuración de directiva, aplique algún método alternativo para implementar actualizaciones de seguridad, como Windows Server Update Services (WSUS).  
Para obtener más información acerca de WSUS, consulte la página de [información general del producto Windows Server Update Services](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx), en www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx.  
Para obtener más información acerca de Windows Update, vea la página de [Windows Update](http://update.microsoft.com/windowsupdate/v6/default.aspx?ln=es) en http://windowsupdate.microsoft.com.
  
##### Internet Explorer\\Características de seguridad\\Limitar la descarga de archivos
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Limitar la descarga de archivos**
  
**Tabla 4.11 Configuración recomendada para la limitación de la descarga de archivos**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (Limitar la descarga de archivos)</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesos de Internet Explorer (Limitar la descarga de archivos)
  
En determinadas circunstancias los sitios web pueden iniciar diálogos de descarga de archivos sin la interacción de los usuarios. Esta técnica puede permitir a un sitio web colocar archivos no autorizados en el disco duro de un usuario si éste hace clic en el botón equivocado y acepta la descarga.
  
Si establece el parámetro **Procesos de Internet Explorer (Limitar la descarga de archivos)** como **Habilitado**, se bloquean los mensajes de descarga de archivos que no inician los usuarios en los procesos de Internet Explorer. Si establece esta configuración de directiva como **Deshabilitada**, se mostrarán mensajes para descargas de archivos que no inicien los usuarios en los procesos de Internet Explorer.
  
El parámetro **Procesos de Internet Explorer (Limitar la descarga de archivos)** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo, como medida para evitar que un atacante introduzca código arbitrario en equipos de usuarios.
  
##### Internet Explorer\\Características de seguridad\\Administración de complementos
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad\\Administración de complementos**
  
**Tabla 4.12 Configuración de Administración de complementos**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Denegar complementos a menos que se permitan específicamente en la Lista de complementos</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Lista de complementos</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
###### Denegar complementos a menos que se permitan específicamente en la Lista de complementos
  
Esta configuración de directiva, junto con el parámetro **Lista de complementos**, le permite controlar complementos de Internet Explorer. De forma predeterminada, la configuración **Lista de complementos** define una lista de complementos que se deben permitir o denegar a través de Directiva de grupo. La configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** supone que todos los complementos se deniegan a menos que aparezcan enumerados específicamente en la configuración **Lista de complementos.**
  
Si habilita esta configuración de directiva, Internet Explorer sólo permite complementos que se enumeran (y permiten) específicamente a través de la **Lista de complementos.** Si deshabilita esta configuración de directiva, los usuarios pueden utilizar el Administrador de complementos para permitir o denegar cualquier complemento.
  
Considere la posibilidad de utilizar tanto el parámetro **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como el parámetro **Lista de complementos** para controlar los complementos que se pueden utilizar en su entorno. Este método ayudará a garantizar que sólo se utilicen complementos autorizados.
  
###### Lista de complementos
  
Esta configuración de directiva, junto con el parámetro **Denegar complementos a menos que se permitan específicamente en la Lista de complementos**, le permite controlar los complementos de Internet Explorer. De forma predeterminada, la configuración **Lista de complementos** define una lista de complementos que se deben permitir o denegar a través de Directiva de grupo. La configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** supone que todos los complementos se deniegan a menos que aparezcan enumerados específicamente en la configuración **Lista de complementos.**
  
Si habilita el parámetro **Lista de complementos**, deberá enumerar los complementos que deben ser permitidos o denegados por Internet Explorer. La relación específica de complementos que se deben incluir en esta lista variará según la organización, por lo que en esta guía no se proporciona una relación detallada. Para cada entrada que agregue a la lista debe proporcionar la información siguiente:
  
-   **Nombre del valor**. El CLSID (identificación de clase) del componente que desea agregar a la lista. El CLSID debe escribirse entre llaves; por ejemplo, {000000000-0000-0000-0000-0000000000000}. El CLSID de un complemento se puede obtener si se lee la etiqueta OBJECT de una página web que haga referencia al complemento.
  
-   **Valor**. Un número que indica si Internet Explorer debe denegar o permitir que se cargue el complemento. Los valores siguientes son válidos:
  
    -   **0**    Denegar este complemento
  
    -   **1**    Permitir este complemento
  
    -   **2**    Permitir este complemento y que el usuario lo administre a través de Administrar complementos
  
Si deshabilita el parámetro **Lista de complementos**, la lista se elimina. Considere la posibilidad de utilizar tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en su entorno. Este método ayudará a garantizar que sólo se utilicen complementos autorizados.
  
##### Servicios de Terminal Server\\Redirección de datos cliente&\#150;servidor
  
La configuración de Servicios de Terminal Server ofrecen opciones para redireccionar los recursos del equipo cliente a servidores a los que otorguen acceso. El siguiente parámetro es específico de los Servicios de Terminal Server.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Servicios de Terminal Server\\Redirección de datos cliente&\#150;servidor**
  
**Tabla 4.13 Configuración recomendada para No permitir redirección de unidad**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir redirección de unidad</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No permitir redirección de unidad
  
Esta configuración de directiva impide que los usuarios compartan las unidades locales de los equipos cliente que utilizan para obtener acceso a servicios de Terminal Server. Las unidades asignadas aparecen en el árbol de carpeta de sesión en el Explorador de Windows o en Mi PC con el formato:
  
\\\\TSClient\\*&lt;letraunidad&gt;$*
  
Si las unidades locales se comparten serán vulnerables a los intrusos que deseen aprovechar los datos que almacenan.
  
Por ese motivo, el parámetro **No permitir redirección de unidad** se configura como **Habilitado** para el entorno SSLF. Sin embargo, esta configuración de directiva es **No configurada** para el entorno de EC.
  
##### Servicios de Terminal Server\\Cifrado y seguridad
  
Puede establecer la siguiente configuración recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Servicios de Terminal Server\\Cifrado y seguridad.**
  
**Tabla 4.14 Configuración recomendada de cifrado y seguridad de Servicios de Terminal Server**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Pedir siempre al cliente la contraseña al conectarse</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Establecer el nivel de cifrado de conexión de cliente</td>
<td style="border:1px solid black;">Alto nivel</td>
<td style="border:1px solid black;">Alto nivel</td>
<td style="border:1px solid black;">Alto nivel</td>
<td style="border:1px solid black;">Alto nivel</td>
</tr>
</tbody>
</table>
  
###### Pedir siempre al cliente la contraseña al conectarse
  
Esta configuración de directiva especifica si los servicios de Terminal Server deben solicitar siempre una contraseña al cliente al realizar la conexión. Puede utilizarla para forzar la petición de una contraseña a los usuarios que inicien sesión en los Servicios de Terminal Server, aunque ya se haya proporcionado una en el cliente de Conexión a Escritorio remoto. De forma predeterminada, los Servicios de Terminal Server permiten a los usuarios iniciar sesión de forma automática si escriben una contraseña en el cliente de Conexión a Escritorio remoto.
  
El parámetro **Pedir siempre al cliente la contraseña al conectarse** se configura como **Habilitado** en el entorno SSLF. Sin embargo, esta configuración de directiva es **No configurada** para el entorno de EC.
  
**Nota**: si no establece esta configuración de directiva, el administrador del equipo local podrá utilizar la herramienta de configuración de Servicios de Terminal Server para permitir o impedir que se envíen automáticamente las contraseñas.
  
###### Establecer el nivel de cifrado de conexión de cliente
  
Esta configuración de directiva especifica si el equipo que está a punto de alojar la conexión remota exigirá que se aplique un nivel de cifrado para todos los datos que intercambie con el equipo cliente para la sesión remota.
  
El cifrado se establece en **Nivel alto** para que se aplique un cifrado de 128 bits para los dos entornos que se tratan en este capítulo.
  
##### Servicios de Terminal Server\\Cliente
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\componentes de Windows\\Servicios de Terminal Server\\Cliente**
  
**Tabla 4.15: Configuración recomendada de no autorización de almacenamiento de contraseñas**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir que se guarden las contraseñas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No permitir que se guarden las contraseñas
  
Esta configuración de directiva impide que los clientes de Servicios de Terminal Server guarden contraseñas en un equipo. Si habilita esta configuración de directiva, se deshabilita la casilla de verificación de almacenamiento en los clientes de Servicios de Terminal Server, de modo que los usuarios no podrán guardar contraseñas.
  
Dado que las contraseñas guardadas pueden suponer un riesgo adicional, el parámetro **No permitir que se guarden las contraseñas** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: si esta configuración de directiva se estableció previamente como **Deshabilitada** o como parámetro **No configurado**, todas las contraseñas guardadas se eliminarán la primera vez que un cliente de Servicios de Terminal Server se desconecte de cualquier servidor.
  
##### Windows Messenger
  
Windows Messenger sirve para enviar mensajes instantáneos a otros usuarios en una red de equipos. Estos mensajes podrán incluir archivos y otros datos adjuntos.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Messenger**
  
**Tabla 4.16 Configuración recomendada de Windows Messenger**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir que se ejecute Windows Messenger</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No permitir que se ejecute Windows Messenger
  
Puede habilitar el parámetro **No permitir que se ejecute Windows Messenger** para deshabilitar Windows Messenger y evitar que se ejecute el programa. Dado que esta aplicación se ha utilizado con fines malintencionados tales como el envío de correo no deseado, la distribución de software malintencionado y la divulgación de datos confidenciales, Microsoft recomienda configurar el parámetro **No permitir que se ejecute Windows Messenger** como **Habilitado** para los entornos EC y SSLF.
  
**Nota**: si establece esta configuración de directiva como **Habilitado**, se impide que Asistencia remota utilice Windows Messenger y que los usuarios empleen MSN® Messenger.
  
##### Windows Update
  
Los administradores utilizan los parámetros de Windows Update para administrar la forma en que se aplican las revisiones en las estaciones de trabajo Windows XP. Las actualizaciones se encuentran disponibles en el sitio web de Microsoft Windows Update. Asimismo, se puede configurar un sitio web en la intranet para distribuir las revisiones de forma parecida y con mayor control administrativo. La plantilla administrativa de Windows Update (WUAU.adm) se introdujo con Windows XP Service Pack 1 (SP1).
  
Windows Server Update Services (WSUS) es un servicio de infraestructuras que aumenta la eficacia de las tecnología de Microsoft Windows Update y Software Update Services (SUS). WSUS administra y distribuye revisiones críticas de Windows que resuelven vulnerabilidades conocidas en la seguridad, así como otros problemas de estabilidad en los sistemas operativos Microsoft Windows.
  
WSUS elimina los pasos de actualización manual gracias a un sistema dinámico de notificación de actualizaciones críticas disponibles para los equipos cliente Windows a través del servidor de intranet. Para utilizar este servicio no se necesita acceso a Internet desde los equipos cliente. Esta tecnología ofrece además una forma sencilla y automática de distribuir actualizaciones a los servidores y estaciones de trabajo Windows propios.
  
Windows Server Update Services también proporciona las siguientes características:
  
-   **Control del administrador sobre la sincronización de contenido en la intranet**. Este servicio de sincronización es un componente en el servidor que recupera las actualizaciones críticas más recientes de Windows Update. A medida que se agregan actualizaciones en Windows Update, el servidor que ejecuta WSUS las descarga y las almacena de acuerdo a una programación definida por el administrador.
  
-   **Un servidor de Windows Update alojado en la intranet**. Este servidor de uso sencillo actúa como el servidor virtual de Windows Update para los equipos cliente. Contiene herramientas administrativas y un servicio de sincronización para administrar las actualizaciones. Atiende solicitudes de actualizaciones aprobadas desde los equipos cliente conectados a través del protocolo HTTP. Este servidor también puede alojar actualizaciones críticas que se descargan del servicio de sincronización y, posteriormente, informar a los equipos cliente de las mismas.
  
-   **Control del administrador sobre las actualizaciones**. El administrador puede probar y aprobar las actualizaciones desde el sitio público de Windows Update antes de distribuirlas en la intranet de su organización. La distribución tiene lugar según una programación que crea el administrador. Si WSUS se ejecuta en varios servidores, el administrador controla qué equipos obtienen acceso a determinados servidores que ejecuten este servicio. Los administradores habilitan este nivel de control con Directiva de grupo en un entorno de servicio de directorio de Active Directory® o a través de claves del Registro.
  
-   **Actualizaciones automáticas en equipos (estaciones de trabajo o servidores)**. Actualizaciones automáticas es una característica de Windows que se puede configurar para la búsqueda de actualizaciones que se publiquen en Windows Update. WSUS utiliza esta característica de Windows para notificar al administrador la existencia de actualizaciones aprobadas en una intranet.
  
    **Nota**: si decide distribuir revisiones a través de otro método, como Microsoft Systems Management Server (SMS), en esta guía se recomienda que deshabilite el parámetro **Configurar actualizaciones automáticas.**
  
Hay varias opciones de configuración de Windows Update. Se requieren como mínimo tres opciones de configuración para que Windows Update funcione: **Configurar actualizaciones automáticas**, **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** y **Volver a programar la instalación programada de actualizaciones automáticas**. La configuración del cuarto parámetro es opcional y depende de los requisitos de su organización: **Especificar la ubicación del servicio Windows Update de la intranet**.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Update**
  
Los parámetros que se tratan en esta sección no solucionan por separado ninguna amenaza para la seguridad en particular, sino que más bien guardan relación con las preferencias del administrador. No obstante, la configuración de Windows Update resulta fundamental para la seguridad del entorno, ya que asegura que los equipos cliente reciben las revisiones desde Microsoft tan pronto como están disponibles.
  
**Nota**: Windows Update depende de varios servicios, incluidos el Registro remoto y el Servicio de transferencia inteligente en segundo plano. En el capítulo 3, "Configuración de seguridad para clientes Windows XP", estos servicios están deshabilitados para el entorno SSLF. Por tanto, si se encuentran deshabilitados, Windows Update no funcionará y las cuatro recomendaciones de configuración siguientes se pueden descartar para el entorno SSLF.
  
La tabla siguiente resume la configuración recomendada de Windows Update. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.17 Configuración recomendada de Windows Update**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No mostrar la opción 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configurar actualizaciones automáticas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No reiniciar automáticamente para instalaciones de actualizaciones automáticas</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Volver a programar la instalación programada de actualizaciones automáticas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Especificar la ubicación del servicio Windows Update de la intranet</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No mostrar la opción 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar
  
Esta configuración de directiva le permite administrar si la opción **Instalar actualizaciones y Apagar** se muestra en el cuadro de diálogo **Apagar**. Si deshabilita esta configuración de directiva, la opción **Instalar actualizaciones y Apagar** se mostrará en el cuadro de diálogo **Salir de Windows** en caso de que haya actualizaciones disponibles cuando el usuario selecciona **Apagar equipo** en el menú **Inicio** o hace clic en **Apagar** después de presionar Ctrl+Alt+Supr.
  
Dado que las actualizaciones son importantes para la seguridad de los equipos en general, el parámetro **No mostrar la opción 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo. Esta configuración de directiva funciona conjuntamente con la configuración de directiva **No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar**, que se trata a continuación.
  
###### No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar
  
Esta configuración de directiva le permite administrar si se posibilita que la opción **Instalar actualizaciones y Apagar** sea la predeterminada en el cuadro de diálogo **Salir de Windows**. Si deshabilita esta configuración de directiva, la opción **Instalar actualizaciones y Apagar** será la predeterminada en el cuadro de diálogo **Salir de Windows** en caso de que haya actualizaciones disponibles para la instalación cuando el usuario seleccione la opción **Apagar equipo** en el menú **Inicio**.
  
Dado que las actualizaciones son importantes para la seguridad de los equipos en general, el parámetro **No ajustar la opción predeterminada a 'Instalar actualizaciones y Apagar' en el cuadro de diálogo Apagar** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de directiva no tiene ningún efecto si la opción **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Update\\No mostrar la opción 'Instalar actualizaciones y Apagar'** en el cuadro de diálogo **Salir de Windows** está **Habilitada**.
  
###### Configurar actualizaciones automáticas
  
Esta configuración de directiva especifica si los equipos del entorno recibirán actualizaciones de seguridad desde Windows Update o WSUS. Si establece esta configuración de directiva como **Habilitada**, el sistema operativo reconocerá cuándo una conexión en red se encuentra disponible para buscar el sitio web de Windows Update o el sitio designado en la intranet para las actualizaciones correspondientes.
  
Una vez establecida la configuración de directiva como **Habilitada**, seleccione una de las tres opciones siguientes en el cuadro de diálogo **Propiedades de Configurar actualizaciones automáticas** para especificar cómo funcionará este servicio:
  
1.  **Notificar antes de descargar las actualizaciones y notificar de nuevo antes de instalarlas.**
  
2.  **Descargar las actualizaciones automáticamente y enviar una notificación cuando se puedan instalar. (Configuración predeterminada)**
  
3.  **Descargar las actualizaciones automáticamente e instalarlas en la programación especificada debajo.**
  
Si deshabilita esta configuración de directiva, necesitará descargar e instalar manualmente cualquier actualización disponible del sitio web de [Windows Update](http://update.microsoft.com/windowsupdate/v6/default.aspx?ln=es), en http://windowsupdate.microsoft.com.
  
El parámetro **Configurar actualizaciones automáticas** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
###### No reiniciar automáticamente para instalaciones de actualizaciones automáticas
  
Si esta configuración de directiva se habilita, el equipo esperará a que un usuario que haya iniciado la sesión reinicie para finalizar una instalación programada; de otro modo, el equipo se reiniciará automáticamente. Cuando está habilitada, esta configuración de directiva también evitará que Actualizaciones automáticas reinicie los equipos durante una instalación programada. Si un usuario inicia una sesión en el equipo y Actualizaciones automáticas necesita reiniciar para finalizar una instalación, el usuario recibirá una notificación y podrá retardar el reinicio del sistema. Actualizaciones automáticas no detectará actualizaciones posteriores mientras no se reinicie el equipo.
  
Si el parámetro **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** se configura como **Deshabilitado** o **No configurado**, Actualizaciones automáticas notificará al usuario que el equipo se reiniciará automáticamente al cabo de 5 minutos para completar la instalación. Si los reinicios automáticos constituyen un motivo de preocupación, puede configurar el parámetro **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** como **Habilitado.** Si habilita esta configuración de directiva, programe los equipos cliente para que se reinicien transcurrido el horario laboral habitual, a fin de asegurar que la instalación se completa.
  
El parámetro **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: esta configuración de seguridad sólo funciona si Actualizaciones automáticas se ha configurado para realizar instalaciones de actualizaciones programadas. Si el parámetro **Configurar actualizaciones automáticas** se ha establecido como **Deshabilitado**, no funcionará. Normalmente, es necesario reiniciar para finalizar una instalación de actualización.
  
###### Volver a programar la instalación programada de actualizaciones automáticas
  
Esta configuración de directiva determina el período de tiempo que transcurrirá antes de que las instalaciones programadas de Actualizaciones automáticas se lleven a cabo tras el inicio del sistema. Si establece esta configuración de directiva como **Habilitada**, cuando el equipo se inicie de nuevo comenzará una instalación anteriormente programada cuando haya transcurrido un tiempo especificado en minutos. Si establece esta configuración de directiva como parámetro **Deshabilitado** o **No configurado**, tendrá lugar una instalación programada con anterioridad durante el siguiente tiempo de instalación de la programación regular.
  
El parámetro **Volver a programar la instalación programada de actualizaciones automáticas** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo. Después que habilite esta configuración de directiva, podrá cambiar el período de espera predeterminado a otro más adecuado para el entorno.
  
**Nota**: esta configuración de seguridad sólo funciona si Actualizaciones automáticas se ha configurado para realizar instalaciones de actualizaciones programadas. Si el parámetro **Configurar actualizaciones automáticas** se establece como **Deshabilitado**, el parámetro **Volver a programar la instalación programada de actualizaciones automáticas** no tendrá efecto. Puede habilitar los dos parámetros anteriores para asegurarse de que las instalaciones que falten se programarán para realizarse cada vez que se reinicie el equipo.
  
###### Especificar la ubicación del servicio Windows Update de la intranet
  
Esta configuración de directiva especifica un servidor en la intranet para alojar actualizaciones de los sitios web de Microsoft Update. A continuación, podrá utilizar este servicio para actualizar automáticamente los equipos en la red. Esta configuración de directiva le permite determinar un servidor WSUS en la red que funcione a modo de servicio de actualizaciones internas. El cliente con Actualizaciones automáticas trabajará con el servidor WSUS para buscar las actualizaciones aplicables a los equipos de la red.
  
El parámetro **Especificar la ubicación del servicio Windows Update de la intranet** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: la habilitación del parámetro **Especificar la ubicación del servicio Windows Update de la intranet** no produce efecto alguno si el parámetro **Configurar actualizaciones automáticas** se encuentra deshabilitado.
  
#### Sistema
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema**
  
En la figura siguiente se ilustran las secciones de Directiva de grupo que se verán afectadas por los cambios de configuración en este apartado:
  
[![](images/Cc163076.SGFG0403(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0403_big(es-es,technet.10).gif)
  
**Figura 4.3 Estructura de Directiva de grupo para el Sistema en Configuración del equipo**
  
La tabla siguiente resume la configuración de sistema recomendada. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.18 Configuración de sistema recomendada**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar reproducción automática</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitado:<br />
Todas las unidades</td>
<td style="border:1px solid black;">Habilitado:<br />
Todas las unidades</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
##### Desactivar reproducción automática
  
Reproducción automática inicia la lectura desde una unidad en cuanto inserte el medio en la misma, lo que provoca el inicio inmediato del archivo de configuración de programas y medios de audio. Un atacante podría utilizar esta característica para iniciar un programa capaz de dañar el equipo o los datos que contiene. Puede habilitar el parámetro **Desactivar reproducción automática** para deshabilitar la característica de reproducción automática. La característica Reproducción automática está deshabilitada de forma predeterminada en algunos tipos de unidades extraíbles, como la unidad de disquete y de red, pero no en las unidades de CD-ROM.
  
El parámetro **Desactivar reproducción automática** se configura como **Habilitado: Todas las unidades** para el entorno SSLF únicamente. Sin embargo, esta configuración de directiva es **No configurada** para el entorno de EC.
  
**Nota**: no puede utilizar esta configuración de directiva para habilitar Reproducción automática en las unidades del equipo en las que está deshabilitada de forma predeterminada, como las unidades de disquete y de red.
  
##### Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update
  
Esta configuración de directiva controla si se le pide al administrador que busque controladores de dispositivo a través de Windows Update en Internet. Si esta configuración de directiva se establece como **Habilitada**, no se solicitará a los administradores que busquen con Windows Update. Si tanto esta configuración de directiva como **Desactivar la búsqueda de controladores de dispositivo en Windows Update** se establecen como **Deshabilitada** o **No configurada**, se pedirá al administrador su consentimiento antes de iniciar la búsqueda de controladores de dispositivo a través de Windows Update.
  
Dado que existe un cierto grado de riesgo al descargar controladores de dispositivo de Internet, el parámetro **Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update** se configura como **Habilitado** para el entorno SSLF y como **Deshabilitado** para el entorno EC. El motivo de esta recomendación es que, normalmente, los tipos de ataques que pueden aprovechar descargas de controladores se reducirán mediante una administración apropiada de los recursos de la empresa.
  
**Nota**: esta configuración de directiva sólo es efectiva si el parámetro **Desactivar la búsqueda de controladores de dispositivo en Windows Update** en **Plantillas administrativas/Sistema/Administración de comunicaciones de Internet/Configuración de comunicaciones de Internet** se establece como **Deshabilitado** o **No configurado**.
  
##### Inicio de sesión
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Inicio de sesión**
  
La tabla siguiente resume la configuración recomendada de inicio de sesión. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.19 Configuración recomendada de inicio de sesión**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No procesar la lista de ejecución heredada</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No procesar la lista de una sola ejecución</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No procesar la lista de ejecución heredada
  
Esta configuración de directiva hace que se pase por alto la lista de ejecución, que es la lista de programas que Windows XP ejecuta automáticamente cuando se inicia. Las listas de ejecución personalizadas de Windows XP se almacenan en el Registro en las siguientes ubicaciones:
  
-   **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**
  
-   **HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**
  
Puede habilitar el parámetro **No procesar la lista de ejecución heredada** para impedir que, cada vez que Windows XP se inicie, un usuario malintencionado ejecute un programa que comprometa los datos del equipo o cause otros daños. Cuando esta configuración de directiva se habilita, evita que determinados programas de sistema se ejecuten, como el software antivirus, así como la distribución de software y el software de supervisión. Microsoft le recomienda que evalúe el nivel de amenaza en el entorno antes de determinar si se debe usar esta configuración de directiva en su organización.
  
El parámetro **No procesar la lista de ejecución heredada** es **No configurado** para el entorno EC y **Habilitado** para el entorno SSLF.
  
###### No procesar la lista de una sola ejecución
  
Esta configuración de directiva hace que se pase por alto la lista de una sola ejecución, que es la lista de programas que Windows XP ejecuta automáticamente cuando se inicia. Esta configuración de directiva difiere de **No procesar la lista de ejecución heredada** en que los programas de la lista se ejecutarán una sola vez cuando se reinicie el equipo cliente. A veces se agregan a esta lista programas de configuración e instalación para finalizar las instalaciones después de que un equipo cliente se reinicie. Si habilita esta configuración de directiva, los atacantes no podrán utilizar la lista de una sola ejecución para iniciar aplicaciones falsas, un método común de ataque en el pasado. Un usuario malintencionado puede aprovechar la lista de una sola ejecución para instalar un programa que comprometa la seguridad de los equipos cliente Windows XP.
  
**Nota**: las listas de una sola ejecución personalizadas se almacenan en el Registro en la siguiente ubicación: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce.**
  
El parámetro **No procesar la lista de una sola ejecución** debe causar una pérdida mínima de funcionalidad a los usuarios de su entorno, especialmente si los equipos cliente se han configurado con todo el software estándar de la organización antes de que esta configuración de directiva se aplique a través de Directiva de grupo.
  
El parámetro **No procesar la lista de una sola ejecución** es **No configurado** para el entorno EC y **Habilitado** para el entorno SSLF.
  
##### Directiva de grupo.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Directiva de grupo**
  
**Tabla 4.20 Configuración recomendada de Directiva de grupo**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesamiento de directivas de Registro</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Procesamiento de directivas de Registro
  
Esta configuración de directiva determina cuándo se actualizan las directivas de Registro. Afecta a todas las directivas de la carpeta Plantillas administrativas y a cualquier otra directiva que almacene valores en el Registro. Si esta configuración de directiva se habilita, están disponibles las opciones siguientes:
  
-   **No aplicar durante el procesamiento periódico en segundo plano.**
  
-   **Procesar incluso si los objetos de directiva de grupo no han cambiado.**
  
Algunas configuraciones que se establecen mediante las plantillas administrativas se realizan en áreas del Registro accesibles para los usuarios. Los cambios realizados en estos parámetros por los usuarios se sobrescribirán si se habilita esta configuración de directiva.
  
El parámetro **Procesamiento de directivas de Registro** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Asistencia remota
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Asistencia remota**
  
La tabla siguiente resume la configuración recomendada de Asistencia remota. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.21 Configuración recomendada de Asistencia remota**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Ofrecer asistencia remota</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Solicit Remote Assistance</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
###### Ofrecer asistencia remota
  
Esta configuración de directiva determina si un ayudante de soporte técnico o un administrador de TI "experto" pueden ofrecer asistencia remota a los equipos del entorno sin que un usuario lo solicite explícitamente a través de un canal, correo electrónico o mensajería instantánea.
  
**Nota**: el experto no puede conectarse al equipo sin avisar o controlarlo sin permiso del usuario. Cuando el experto intente conectarse, el usuario podrá optar por rechazar la conexión o proporcionar al experto privilegios de sólo vista. El usuario debe hacer clic explícitamente en el botón **Sí** para permitir que el experto controle remotamente la estación de trabajo, después de establecer el parámetro **Ofrecer asistencia remota** como **Habilitado**.
  
Si esta configuración de directiva se habilita, están disponibles las opciones siguientes:
  
-   **Dar permiso a los servicios de ayuda para que sólo vean el equipo**
  
-   **Dar permiso a los servicios de ayuda para que controlen el equipo remotamente**
  
Al establecer esta configuración de directiva también puede especificar una lista de usuarios o grupos de usuarios conocidos como "servicios de ayuda" que pueden ofrecer asistencia remota.
  
**Para configurar la lista de servicios de ayuda**
  
1.  En la ventana de configuración del parámetro **Ofrecer asistencia remota**, haga clic en **Mostrar**. Aparecerá una ventana nueva en la que puede introducir los nombres de los servicios de ayuda.
  
2.  Agregue cada usuario o grupo a la lista de **servicios de ayuda** en uno de los siguientes formatos:
  
    -   *&lt;Nombre de dominio&gt;*\\*&lt;Nombre de usuario&gt;*
  
    -   *&lt;Nombre de dominio&gt;*\\*&lt;Nombre de grupo&gt;*
  
Si esta configuración de directiva se deshabilita o no está configurada, los usuarios y los grupos no podrán ofrecer asistencia remota no solicitada a los usuarios del entorno.
  
El parámetro **Ofrecer asistencia remota** se establece como **No configurado** para el entorno EC. Sin embargo, esta configuración de directiva se establece como **Deshabilitada** para el entorno SSLF con el fin de evitar el acceso a equipos cliente Windows XP a través de la red.
  
###### Solicit Remote Assistance
  
Esta configuración de directiva determina si se puede solicitar asistencia remota desde los equipos Windows XP del entorno. Tiene la posibilidad de habilitar esta configuración de directiva para que los usuarios puedan solicitar asistencia remota a administradores de TI "expertos".
  
**Nota**: los expertos no pueden conectarse al equipo sin avisar, ni controlarlo sin permiso del usuario. Cuando el experto intente conectarse, el usuario podrá optar por rechazar la conexión o proporcionar al experto privilegios de sólo vista. El usuario debe hacer clic en el botón **Sí** para permitir que el experto controle de forma remota la estación de trabajo.
  
Si se hablita el parámetro **Solicit Remote Assistance**, estarán disponibles las opciones siguientes:
  
-   **Dar permiso a los servicios de ayuda para que controlen el equipo remotamente**
  
-   **Dar permiso a los servicios de ayuda para que sólo vean el equipo**
  
Asimismo, las siguientes opciones están disponibles para configurar cuánto tiempo se mantiene la validez de una solicitud de ayuda de un usuario:
  
-   **Validez máxima del vale (valores):**
  
-   **Validez máxima del vale (unidades): horas, minutos o días**
  
Cuando un vale (solicitud de ayuda) caduca, el usuario debe enviar otra solicitud para que un experto pueda conectarse al equipo. Si deshabilita el parámetro **Solicit Remote Assistance**, los usuarios no podrán enviar solicitudes de ayuda y el experto no se podrá conectar a los equipos.
  
Si no se configura **Solicit Remote Assistance**, los usuarios podrán configurar la asistencia remota solicitada a través del Panel de control. La configuración siguiente se habilita de forma predeterminada en el Panel de control: **Asistencia remota solicitada**, **Buddy support** y **Control remoto**. El valor de **Validez máxima del vale** se establece en **30 días**. Si esta configuración de directiva se deshabilita, nadie podrá tener acceso a los equipos cliente Windows XP a través de la red.
  
El parámetro **Solicit Remote Assistance** se establece como **No configurado** para el entorno EC y como **Deshabilitado** para el entorno SSLF.
  
##### Informe de errores
  
Estos parámetros controlan cómo se informa de los errores de aplicación y de sistema. En la configuración predeterminada, cuando se produce un error se pregunta al usuario mediante un cuadro de diálogo emergente si desea enviar un informe de errores a Microsoft. Microsoft sigue directivas estrictas con respecto a la protección de los datos recibidos en estos informes. Sin embargo, los datos se transmiten en texto sin formato, lo que constituye un riesgo potencial para la seguridad.
  
Microsoft proporciona la herramienta Informe de errores corporativos para que las organizaciones recopilen los informes de forma local y no los envíen a Microsoft a través de Internet. Microsoft recomienda el uso de la herramienta Informe de errores corporativos en el entorno de SSLF para evitar la exposición en Internet de información confidencial. Se proporciona más información acerca de esta herramienta en la sección "Información adicional" que aparece al final de este capítulo.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Informe de errores**
  
La tabla siguiente resume la configuración recomendada de Informe de errores. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.22 Configuración recomendada de Informe de errores**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Mostrar notificación de errores</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configurar Informe de errores</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Mostrar notificación de errores
  
Esta configuración de directiva controla si los mensajes de error se muestran a los usuarios en las pantallas de los equipos. Si habilita esta configuración de directiva, se enviarán notificaciones de mensajes de error cuando se produzcan errores y los usuarios tendrán acceso a detalles acerca de los errores. Si deshabilita esta configuración de directiva, se impedirá que los usuarios vean las notificaciones de error.
  
Cuando se produce un error, resulta importante que el usuario sea consciente del problema. Los usuarios no serán informados de la existencia de problemas si se deshabilita el parámetro **Mostrar notificación de errores.** Por ese motivo, el parámetro **Mostrar notificación de errores** se establece en **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Configurar Informe de errores
  
Esta configuración de directiva controla si se informa de los errores. Cuando esta configuración de directiva se habilita, los usuarios pueden elegir si informan de los errores cuando se producen. Se puede informar de los errores a Microsoft (a través de Internet) o a un recurso compartido local. Si habilita esta configuración de directiva, también están disponibles las siguientes opciones:
  
-   **No mostrar vínculos a ningún sitio web de "más información" proporcionado por Microsoft**
  
-   **No recopilar archivos adicionales**
  
-   **No recopilar información de equipos adicionales**
  
-   **Forzar el modo de cola para errores de aplicación**
  
-   **Ruta de acceso al archivo de carga corporativa**
  
-   **Remplazar todos los casos de la palabra "Microsoft" con**
  
Si se deshabilita el parámetro **Configurar Informe de errores**, los usuarios no pueden informar de los errores. Si se habilita el parámetro **Mostrar notificación de errores**, los usuarios recibirán notificaciones de errores, pero no podrán informar sobre ellos. El parámetro **Configurar Informe de errores** le permite personalizar una estrategia de generación de informes de errores para su organización y recopilar informes para un análisis local.
  
El parámetro **Configurar Informe de errores** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo. Además, se seleccionaron las opciones siguientes para el entorno SSLF:
  
-   **No recopilar archivos adicionales**
  
-   **No recopilar información de equipos adicionales**
  
-   **Forzar el modo de cola para errores de aplicación**
  
También puede seleccionar la opción **Ruta de acceso al archivo de carga corporativa** e incluir la ruta de acceso al servidor en el que ha instalado la herramienta Informe de errores corporativos. Debe evaluar las necesidades de su organización para determinar qué opciones puede utilizar.
  
##### Llamada a procedimiento remoto
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Sistema\\Llamada a procedimiento remoto**
  
La tabla siguiente resume la configuración recomendada de Llamada a procedimiento remoto. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.23 Configuración recomendada de Llamada a procedimiento remoto**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Restricciones para clientes RPC no autenticados</td>
<td style="border:1px solid black;">Habilitado: Autenticados</td>
<td style="border:1px solid black;">Habilitado: Autenticados</td>
<td style="border:1px solid black;">Habilitado: Autenticados</td>
<td style="border:1px solid black;">Habilitado: Autenticados</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Autenticación de clientes del Asignador de puntos finales de RPC</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Restricciones para clientes RPC no autenticados
  
Esta configuración de directiva establece el Tiempo de ejecución de RPC en un servidor RPC para limitar la conexión de clientes RPC no autenticados al servidor RPC. Se considerará que un cliente se ha autenticado si utiliza una canalización con nombre para comunicarse con el servidor o si utiliza seguridad RPC. Las interfaces de RPC que han pedido específicamente ofrecer acceso a clientes no autenticados pueden quedar exentas de esta restricción, con arreglo al valor seleccionado para esta directiva. Si habilita esta configuración de directiva, están disponibles los siguientes valores:
  
-   **Ninguno**. Permite a todos los clientes RPC conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva.
  
-   **Autenticado**. Permite únicamente a los clientes RPC autenticados conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva. A las interfaces que han solicitado quedar exentas de esta restricción se les otorgará una exención.
  
-   **Autenticado sin excepciones**. Permite únicamente a los clientes RPC autenticados conectarse a servidores RPC que se ejecutan en el equipo en que se aplica la directiva. No se permiten excepciones.
  
Dado que la comunicación RPC sin autenticación puede crear una vulnerabilidad de seguridad, el parámetro **Restricciones para clientes RPC no autenticados** se configura como **Habilitado**, y el valor **Restricción de clientes sin autenticar del tiempo de ejecución RPC que desea aplicar** se establece como **Autenticado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: las aplicaciones RPC que no autentican solicitudes de conexión de entrada no solicitadas pueden no funcionar correctamente cuando se aplica esta configuración. Asegúrese de probar las aplicaciones antes de implementar esta configuración de directiva en el entorno. Aunque el valor Autenticado para esta configuración de directiva no sea completamente seguro, puede resultar útil por lo que respecta a la compatibilidad de las aplicaciones en su entorno.
  
###### Autenticación de clientes del Asignador de puntos finales de RPC
  
Si habilita esta configuración de directiva, se exigirá a los equipos cliente que se comunican con este equipo que proporcionen autenticación antes de que se establezca una comunicación RPC. De forma predeterminada, los clientes RPC no utilizarán la autenticación para comunicarse con el Servicio de asignador de extremos cuando solicitan el extremo de un servidor. Sin embargo, esta configuración predeterminada se cambió para el entorno SSLF a fin de requerir la autenticación de los equipos cliente antes de que se permita una comunicación RPC.
  
##### Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet
  
Existen varias opciones de configuración disponibles en el grupo Configuración de comunicaciones de Internet. En esta guía se recomienda la restricción de muchas de estas configuraciones, sobre todo para ayudar a aumentar el nivel de confidencialidad de los datos en los sistemas informáticos. Si esta configuración no es restringida, la información podría ser interceptada y utilizada por atacantes. Aunque las probabilidades de que se produzca hoy este tipo de ataque son escasas, una configuración adecuada de estos parámetros ayudará a proteger su entorno contra futuros ataques.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet**
  
La tabla siguiente resume la configuración recomendada de las comunicaciones de Internet. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.3 Configuración recomendada de comunicaciones de Internet**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la tarea Publicar en Web para archivos y carpetas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar la actualización de archivos de contenido del Asistente para búsqueda</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar impresión a través de HTTP</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar la descarga de controladores de impresión a través de HTTP</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la búsqueda de controladores de dispositivo en Windows Update</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Desactivar la tarea Publicar en Web para archivos y carpetas
  
Esta configuración de directiva especifica si las tareas **Publicar este archivo en Web**, **Publicar esta carpeta en Web** y **Publicar los elementos seleccionados en Web** están disponibles en las Tareas de archivo y carpeta en las carpetas de Windows. El Asistente para la publicación en Web se usa para descargar una lista de proveedores y permite que los usuarios publiquen contenido en Web.
  
Si configura el parámetro **Desactivar la tarea Publicar en Web para archivos y carpetas** como **Habilitado**, estas opciones se quitan de las Tareas de archivo y carpeta en las carpetas de Windows. De forma predeterminada, la opción de publicar en Web está disponible. Dado que esta capacidad se podría utilizar para exponer contenido protegido ante un equipo cliente web no autenticado, esta configuración de directiva se configura como **Habilitada** para los entornos EC y SSLF.
  
###### Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea
  
Esta configuración de directiva controla si Windows descargará una lista de proveedores de los asistentes para la publicación en Web y para pedidos en línea. Si esta configuración de directiva se habilita, se evitará que Windows descargue proveedores; sólo se mostrarán los proveedores de servicios que se encuentren almacenados en caché en el Registro local.
  
Dado que el parámetro **Desactivar** **la tarea Publicar en Web para archivos y carpetas** se habilitó para los entornos EC y SSLF (consulte el parámetro anterior), esta opción no se necesita. Sin embargo, el parámetro **Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea** se configura como **Habilitado** para minimizar la superficie de ataque de los equipos cliente y para asegurar que esta capacidad no se pueda aprovechar de otras maneras.
  
###### Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger
  
Esta configuración de directiva especifica si Windows Messenger puede recopilar información anónima acerca del uso del servicio y del software Windows Messenger. Puede habilitar esta configuración de directiva para asegurarse de que Windows Messenger no recopila información de uso y para evitar que se muestren parámetros de configuración de usuario que posibiliten la recopilación de información de uso.
  
En entornos de gran empresa quizá no sea deseable la recopilación de información de los equipos cliente administrados. El parámetro **Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo, a fin de evitar que se recopile información.
  
###### Desactivar la actualización de archivos de contenido del Asistente para búsqueda
  
Esta configuración de directiva especifica si el Asistente para búsqueda debe descargar automáticamente actualizaciones de contenido durante las búsquedas en Internet y locales. Si establece esta configuración de directiva como **Habilitada**, evitará que el Asistente para búsqueda descargue actualizaciones de contenido durante las búsquedas.
  
El parámetro **Desactivar la actualización de archivos de contenido del Asistente para búsqueda** se configura como **Habilitado** para los entornos EC y SSLF con objeto de controlar comunicaciones de red innecesarias desde cada equipo cliente administrado.
  
**Nota**: las búsquedas de Internet seguirán enviando el texto de la búsqueda e información acerca de la búsqueda a Microsoft y al proveedor de búsqueda elegido. Si selecciona Búsqueda clásica, la característica de Asistente para búsqueda no estará disponible. Puede seleccionar la búsqueda clásica si hace clic en **Inicio**, **Buscar**, **Cambiar preferencias** y, a continuación, en **Cambiar el comportamiento de búsqueda en Internet**.
  
###### Desactivar impresión a través de HTTP
  
Mediante esta configuración de directiva es posible deshabilitar la capacidad del equipo cliente de imprimir a través de HTTP, que permite al equipo imprimir con impresoras de la intranet y de Internet. Si habilita esta configuración de directiva, el equipo cliente no podrá imprimir con impresoras de Internet a través de HTTP.
  
La información que se transmite a través de HTTP mediante esta capacidad no se protege y puede ser interceptada por usuarios malintencionados. Por eso se utiliza pocas veces en entornos de empresa. El parámetro **Desactivar impresión a través de HTTP** se configura como **Habilitado** para los entornos EC y SSLF como medida para evitar una posible infracción de la seguridad a través de un trabajo de impresión inseguro.
  
**Nota**: esta configuración de directiva afecta únicamente a los clientes de impresión de Internet. Independientemente de cómo se configura, un equipo podría actuar como servidor de impresión de Internet y hacer que sus impresoras compartidas estén disponibles a través de HTTP.
  
###### Desactivar la descarga de controladores de impresión a través de HTTP
  
Esta configuración de directiva controla si el equipo puede descargar paquetes de controladores de impresión a través de HTTP. Para configurar la impresión HTTP, quizá sea necesario descargar a través de HTTP los controladores de impresión que no están disponibles en la instalación del sistema operativo estándar.
  
El parámetro **Desactivar la descarga de controladores de impresión a través de HTTP** se configura como **Habilitado** para evitar que se descarguen controladores de impresión a través de HTTP.
  
**Nota**: esta configuración de directiva no impide que el equipo cliente utilice impresoras de la intranet o de Internet a través de HTTP. Sólo desautoriza la descarga de controladores que no se encuentran ya instalados localmente.
  
###### Desactivar la búsqueda de controladores de dispositivo en Windows Update
  
Esta configuración de directiva especifica si Windows deberá buscar mediante Windows Update controladores de dispositivo cuando no se encuentren localmente.
  
Dado que existe un cierto grado de riesgo al descargar controladores de dispositivo de Internet, el parámetro **Desactivar la búsqueda de controladores de dispositivo en Windows Update** se configura como **Habilitado** para el entorno SSLF y como **Deshabilitado** para el entorno EC. El motivo de esta configuración es que, normalmente, los tipos de ataques que pueden aprovechar descargas de controladores se reducirán mediante una administración apropiada de los recursos de la empresa y las configuraciones.
  
**Nota**: vea también **Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update** en **Plantillas administrativas/Sistema**, que permite establecer si se pregunta al administrador antes de buscar a través de Windows Update controladores de dispositivo que no se encuentren localmente.
  
#### Red
  
No hay configuraciones específicas relacionadas con la seguridad en el contenedor de Red de Directiva de grupo. Sin embargo, hay varias opciones de configuración muy importantes en el contenedor **Conexiones de red\\Firewall de Windows** que se explican en las secciones siguientes.
  
En la figura siguiente se ilustran las secciones de Directiva de grupo que se verán afectadas por los cambios de configuración en este apartado:
  
[![](images/Cc163076.SGFG0404(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0404_big(es-es,technet.10).gif)
  
**Figura 4.4 Estructura de Directiva de grupo para Conexiones de red en Configuración del equipo**
  
#### Conexiones de red\\Firewall de Windows
  
La configuración de Firewall de Windows se realiza en dos perfiles: Perfil de dominio y Perfil estándar. Siempre que se detecta un entorno de dominio, se utiliza el Perfil de dominio; si se detecta un entorno que no es de dominio, se utiliza el Perfil estándar.
  
Cuando una opción de configuración de Firewall de Windows aparece **Recomendada** en una de los dos tablas siguientes, el valor específico que se debe utilizar variará según la organización. Por ejemplo, cada organización tendrá una lista única de aplicaciones que requerirán las excepciones definidas para el Firewall de Windows. Por lo tanto, en esta guía no se puede definir una lista que tenga una utilidad general.
  
Cuando necesita determinar qué aplicaciones o puertos pueden necesitar excepciones, quizá sea útil habilitar el registro de Firewall de Windows, la auditoría de Firewall de Windows y el seguimiento de red. Para obtener más información, consulte el artículo sobre la [configuración de un equipo para solucionar problemas de Windows Firewall](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/operations/bfdeda55-46fc-4b53-b4cd-c71838ef4b41.mspx), disponible en línea en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
library/Operations/bfdeda55-46fc-4b53-b4cd-c71838ef4b41.mspx.
  
Para obtener más información acerca de cómo se usa el servicio Network Location Awareness (NLA) en Windows XP para determinar a qué clase de red está conectado el sistema, vea el artículo (en inglés) sobre la [configuración del comportamiento en la determinación de la red para la directiva de grupo relacionada con la red](http://www.microsoft.com/spain/technet/recursos/articulos/cg0504.mspx) en el sitio web de Microsoft, en http://www.microsoft.com/spain/technet/recursos/articulos/cg0504.mspx.
  
Normalmente, el Perfil de dominio se configura de modo que sea menos restrictivo que el Perfil estándar, ya que un entorno de dominio suele proporcionar capas de protección adicionales.
  
Los nombres de configuración de directiva son idénticos en ambos perfiles. En las dos tablas siguientes se resumen las configuraciones de directiva para los distintos perfiles, y se proporcionan explicaciones más detalladas en las subsecciones que siguen a las tablas.
  
##### Conexiones de red\\Firewall de Windows\\Perfil de dominio
  
Las opciones de esta sección configuran el Perfil de dominio de Firewall de Windows.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Red\\Conexiones de red\\Firewall de Windows\\Perfil de dominio**
  
**Tabla 4.25 Configuración recomendada de Perfil de dominio de Firewall de Windows**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Proteja todas las conexiones de red</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir excepciones</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Definir excepciones de programa</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepciones de programa local</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción de administración remota</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir la excepción compartir impresoras y archivos</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepciones ICMP</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepción de Escritorio remoto</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción de entorno UPnP</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir notificaciones</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">No permitir respuesta de monodifusión a peticiones de difusión o multidifusión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Definir excepciones de puerto</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepciones de puerto local</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Nota**: cuando una opción de configuración de Firewall de Windows aparece **Recomendada** en esta tabla, el valor específico que se debe utilizar variará según la organización. Por ejemplo, cada organización tendrá una lista única de aplicaciones que requerirán las excepciones definidas para el Firewall de Windows. Por lo tanto, en esta guía no se puede definir una lista que tenga una utilidad general.
  
##### Conexiones de red\\Firewall de Windows\\Perfil estándar
  
La configuración de esta sección determina el Perfil estándar de Firewall de Windows. Este perfil es a menudo más restrictivo que el Perfil de dominio, que asume que un entorno de dominio proporciona un nivel de seguridad básico. Se espera que se utilice el Perfil estándar cuando un equipo se encuentra en una red que no es de confianza, en una red de hotel o en un punto de inalámbrico público. Ese tipo de entornos implican riesgos desconocidos y requieren precauciones de seguridad adicionales.
  
Puede establecer la siguiente configuración de equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Red\\Conexiones de red\\Firewall de Windows\\Perfil estándar**
  
**Tabla 4.26 Configuración recomendada de Perfil estándar de Firewall de Windows**

 
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
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >EC: Escritorio</th>
<th style="border:1px solid black;" >EC: Portátil</th>
<th style="border:1px solid black;" >SSLF: Escritorio</th>
<th style="border:1px solid black;" >SSLF: Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Proteja todas las conexiones de red</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir excepciones</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Definir excepciones de programa</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepciones de programa local</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción de administración remota</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir la excepción compartir impresoras y archivos</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepciones ICMP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepción de Escritorio remoto</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción de entorno UPnP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir notificaciones</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">No permitir respuesta de monodifusión a peticiones de difusión o multidifusión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Definir excepciones de puerto</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepciones de puerto local</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Nota**: cuando una opción de configuración de Firewall de Windows aparece **Recomendada** en esta tabla, el valor específico que se debe utilizar variará según la organización. Por ejemplo, cada organización tendrá una lista única de aplicaciones que requerirán las excepciones definidas para el Firewall de Windows. Por lo tanto, en esta guía no se puede definir una lista que tenga una utilidad general.
  
###### Firewall de Windows: proteger todas las conexiones de red
  
Esta configuración de directiva habilita Firewall de Windows, que reemplaza a Servidor de seguridad de conexión a Internet en todos los equipos en los que se ejecuta Windows XP con SP2. En esta guía se recomienda que establezca esta configuración de directiva como **Habilitada** con el fin de proteger las conexiones de red de los equipos en todos los entornos que se tratan en esta guía.
  
Si el parámetro **Firewall de Windows: proteger todas las conexiones de red** se configura como **Deshabilitado**, se desactiva el Firewall de Windows y se omiten todos los demás parámetros de configuración de Firewall de Windows.
  
**Nota**: si habilita esta configuración de directiva, se ejecuta el Firewall de Windows y se omite el parámetro **Configuración del equipo\\Plantillas administrativas\\Red\\Conexiones de red\\Prohibir el uso de Servidor de seguridad de conexión a Internet en su red de dominio DNS**.
  
###### Firewall de Windows: no permitir excepciones
  
Esta configuración de directiva provocó que Firewall de Windows bloqueara todos los mensajes entrantes no solicitados. Anula todos los demás parámetros de Firewall de Windows que permitan dichos mensajes. Si habilita esta configuración de directiva en el componente Firewall de Windows del Panel de control, se activa la casilla de verificación **No permitir excepciones**, que no podrán desactivar los administradores.
  
Muchos entornos contienen aplicaciones y servicios a los que para su funcionamiento normal se debe permitir la recepción de comunicaciones entrantes no solicitadas. Puede que en esos entornos sea necesario configurar el parámetro **Firewall de Windows: no permitir excepciones** como **Deshabilitado** para permitir que esas aplicaciones y servicios se ejecuten correctamente. Sin embargo, antes de establecer esta configuración de directiva tendrá que probar el entorno para determinar exactamente qué comunicaciones deben permitirse.
  
**Nota**: esta configuración de directiva proporciona una sólida defensa frente a atacantes externos y debe establecerse como **Habilitada** en situaciones en las que se necesite una completa protección frente a ataques desde el exterior, tales como un gusano nuevo en la red. Si establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows podrá aplicar otros parámetros de configuración de directiva que permitan mensajes entrantes no solicitados.
  
###### Firewall de Windows: definir excepciones de programa
  
Es posible que algunas aplicaciones necesiten abrir y utilizar puertos de red que no suele permitir Firewall de Windows. La configuración **Firewall de Windows: definir excepciones de programa** le permite ver y cambiar la lista de excepciones de programa que define Directiva de grupo.
  
Si esta configuración de directiva está **Habilitada**, puede ver y cambiar la lista de excepciones de programa. Si agrega un programa a esta lista y establece su estado como **Habilitado**, ese programa podrá recibir mensajes entrantes no solicitados en cualquier puerto que solicite a Firewall de Windows que se abra, aunque dicho puerto esté bloqueado por otro parámetro. Si establece esta configuración de directiva como **Deshabilitada**, se elimina la lista de excepciones de programa que ha definido Directiva de grupo.
  
**Nota**: si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores. Dado que no se comprueba la entrada, puede agregar programas que aún no se han instalado. También es posible crear accidentalmente varias excepciones para el mismo programa y que entren en conflicto los valores de Ámbito o Estado.
  
###### Firewall de Windows: permitir excepciones de programa local
  
Esta configuración de directiva controla si los administradores pueden usar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de programa local. Si deshabilita esta configuración de directiva, los administradores no podrán definir una lista de excepciones de programa local; asimismo, esta configuración garantiza que esas excepciones de programa sólo procedan de la Directiva de grupo. Si se habilita esta configuración de directiva, los administradores locales podrán utilizar el Panel de control para definir excepciones de programa localmente.
  
Para equipos cliente de empresa, es posible que existan condiciones que justifiquen excepciones de programa de ámbito local. Estas condiciones pueden incluir aplicaciones que no se analizaron cuando se creó la directiva de firewall de la organización o aplicaciones nuevas que requieren una configuración de puertos no estándar. Si opta por habilitar el parámetro **Firewall de Windows: permitir excepciones de programa local** para esas situaciones, recuerde que la superficie de ataque de los equipos afectados se incrementa.
  
###### Firewall de Windows: permitir excepción de administración remota
  
Muchas organizaciones aprovechan la administración de equipos remotos en sus operaciones diarias. Sin embargo, se han producido ataques en los que se aprovechaban puertos que suelen utilizar los programas de administración remota; Firewall de Windows puede bloquear estos puertos.
  
Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de administración remota**. Si se habilita esta configuración de directiva, el equipo podrá recibir mensajes entrantes no solicitados que están asociados a la administración remota en los puertos TCP 135 y 445. Esta configuración de directiva permite también que Svchost.exe y Lsass.exe reciban mensajes entrantes no solicitados y que los servicios alojados abran puertos adicionales asignados dinámicamente, por lo general en el intervalo que va de 1024 a 1034, aunque puede ser cualquiera de los comprendidos entre el 1024 y el 65535. Si habilita esta configuración de directiva, también deberá especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si configura el parámetro **Firewall de Windows: permitir excepción de administración remota** como **Deshabilitado**, Firewall de Windows no aplica ninguna de las excepciones descritas. La repercusión de establecer esta configuración de directiva como **Deshabilitada** puede ser inaceptable para un gran número de organizaciones, ya que no permite que funcionen muchas herramientas de administración remota ni de detección de vulnerabilidades. Así pues, Microsoft recomienda que sólo las organizaciones más sensibles desde el punto de vista de la seguridad habiliten esta configuración de directiva.
  
Para el Perfil de dominio, Microsoft recomienda que el parámetro **Firewall de Windows: permitir excepción de administración remota** se establezca como **Habilitado** para equipos del entorno EC (si es posible) y como **Deshabilitado** para equipos del entorno SSLF. Los equipos de su entorno deben aceptar las solicitudes de administración remota del menor número de equipos posible. Para maximizar la protección que ofrece Firewall de Windows, asegúrese de especificar sólo las direcciones IP y las subredes de equipos que se utilizan en la administración remota.
  
Microsoft recomienda que el parámetro **Firewall de Windows: permitir excepción de administración remota** se establezca como **Deshabilitado** para todos los equipos de Perfil estándar con objeto de evitar ataques conocidos que aprovechen específicamente los puertos TCP 135 y 445.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
###### Firewall de Windows: permitir la excepción compartir impresoras y archivos
  
Esta configuración de directiva crea una excepción que permite el uso compartido de archivos e impresoras. Configura Firewall de Windows para que se abran los puertos UDP 137 y 138 y los puertos TCP 139 y 445. Si habilita esta configuración de directiva, Firewall de Windows abre estos puertos para que el equipo pueda recibir trabajos de impresión y solicitudes de acceso a archivos compartidos. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes.
  
Si deshabilita el parámetro **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, Firewall de Windows bloquea estos puertos y evita que el equipo comparta archivos e impresoras.
  
Dado que, por lo general, los equipos del entorno en los que se ejecuta Windows XP no compartirán archivos e impresoras, Microsoft recomienda configurar el parámetro **Firewall de Windows: permitir la excepción compartir impresoras y archivos** como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
###### Firewall de Windows: permitir excepciones ICMP
  
Esta configuración de directiva define el conjunto de tipos de mensajes ICMP (Protocolo de mensajes de control de Internet) que permitirá Firewall de Windows. Las utilidades pueden usar los mensajes ICMP para determinar el estado de otros equipos. Por ejemplo, Ping utiliza el mensaje de solicitud de eco.
  
Si configura el parámetro **Firewall de Windows: permitir excepciones ICMP** como **Habilitado**, deberá especificar qué tipos de mensajes ICMP permitirá Firewall de Windows que envíe o reciba el equipo. Cuando se establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows bloquea todos los tipos de mensajes ICMP entrantes no solicitados y los tipos de mensajes ICMP salientes enumerados. Como consecuencia de ello, las utilidades que dependen de ICMP pueden no funcionar.
  
Muchas herramientas de atacantes aprovechan la posibilidad que ofrecen los equipos que aceptan tipos de mensajes ICMP y utilizan éstos para preparar distintos ataques. Sin embargo, algunas aplicaciones precisan mensajes ICMP para funcionar correctamente. Asimismo, los mensajes ICMP se utilizan para calcular el rendimiento de la red cuando se descarga y se procesa Directiva de grupo; si los mensajes ICMP se bloquean, no se puede aplicar Directiva de grupo a los sistemas afectados. Por eso, Microsoft recomienda configurar el parámetro **Firewall de Windows: permitir excepciones ICMP** como **Deshabilitado** siempre que sea posible. Si en su entorno es necesario que algunos mensajes ICMP atraviesen Firewall de Windows, establezca esta configuración de directiva con los tipos de mensajes adecuados.
  
Siempre que el equipo se encuentra en una red que no es de confianza, el parámetro **Firewall de Windows: permitir excepciones ICMP** debe configurarse como **Deshabilitado.**
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
###### Firewall de Windows: permitir excepción de Escritorio remoto
  
Muchas organizaciones utilizan conexiones de Escritorio remoto en sus operaciones o procedimientos habituales de solución de problemas. Sin embargo, en algunos ataques se han aprovechado los puertos que suele utilizar Escritorio remoto.
  
Para una mayor flexibilidad en la administración remota, se encuentra disponible la configuración **Firewall de Windows: permitir excepción de Escritorio remoto**. Si habilita esta configuración de directiva, Firewall de Windows abre el puerto TCP 3389 para las conexiones entrantes. También debe especificar las direcciones IP o las subredes de las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloqueará este puerto e impedirá que el equipo reciba solicitudes de Escritorio remoto. Si un administrador agrega este puerto a una lista de excepciones de puerto local para intentar abrirlo, Firewall de Windows no abre el puerto.
  
En algunos ataques se puede aprovechar un puerto 3389 abierto, por lo que Microsoft recomienda configurar el parámetro **Firewall de Windows: permitir excepción de Escritorio remoto** como **Deshabilitado** para el entorno SSLF. Para mantener las capacidades de administración mejorada que proporciona Escritorio remoto, debe establecer esta configuración de directiva como **Habilitada** para el entorno EC. Tiene que especificar las direcciones IP y las subredes de los equipos que se utilizan para la administración remota. Los equipos de su entorno deben aceptar las solicitudes de Escritorio remoto del menor número de equipos posible.
  
###### Firewall de Windows: permitir excepción de entorno UPnP
  
Esta configuración de directiva permite a un equipo recibir mensajes Plug and Play no solicitados que envían dispositivos de red tales como enrutadores con servidores de seguridad integrados. Para recibir estos mensajes, Firewall de Windows abre el puerto TCP 2869 y el puerto UDP 1900.
  
Si habilita el parámetro **Firewall de Windows: permitir excepción de entorno UPnP**, Firewall de Windows abre estos puertos para que el equipo pueda recibir mensajes Plug and Play. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes. Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo reciba mensajes Plug and Play.
  
Con el bloqueo del tráfico de red UPnP se reduce en la práctica la superficie susceptible de ataque en los equipos del entorno. En redes de confianza, Microsoft recomienda configurar el parámetro **Firewall de Windows: permitir excepción de entorno UPnP** como **Deshabilitado** a menos que utilice dispositivos UPnP en la red. Esta configuración de directiva siempre debe estar **Deshabilitada** para redes que no son de confianza.
  
###### Firewall de Windows: no permitir notificaciones
  
Firewall de Windows puede mostrar notificaciones a los usuarios cuando un programa solicita que Firewall de Windows agregue el programa a la lista de excepciones de programa. Esta situación se produce cuando los programas intentan abrir un puerto y no se les permite debido a las reglas actuales de Firewall de Windows.
  
El parámetro **Firewall de Windows: no permitir notificaciones** determina si se muestra esta configuración a los usuarios. Si establece esta configuración de directiva como **Habilitada**, Firewall de Windows impide que se muestren estas notificaciones. Si se establece como **Deshabilitada**, Firewall de Windows permite que se muestren estas notificaciones.
  
Normalmente, a los usuarios no se les permitirá agregar aplicaciones y puertos en respuesta a estos mensajes en entornos EC o SSLF. En esos casos, este mensaje informará al usuario de que ocurre algo sobre lo que no tienen control y debe configurarse el parámetro **Firewall de Windows: no permitir notificaciones** como **Habilitado.** En otros entornos en los que se permiten excepciones para algunos usuarios, debe establecer esta configuración de directiva como **Deshabilitado.**
  
###### Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión
  
Esta configuración de directiva impide que un equipo reciba respuestas de monodifusión a sus mensajes salientes de difusión o multidifusión. Cuando esta configuración de directiva está habilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows bloquea las respuestas de monodifusión que envían esos otros equipos. Cuando esta configuración de directiva está deshabilitada y el equipo envía un mensaje de difusión o multidifusión a otros equipos, Firewall de Windows espera hasta tres segundos respuestas de monodifusión de los demás equipos y después bloquea todas las respuestas posteriores.
  
Normalmente, no deseará recibir respuestas de monodifusión a mensajes de difusión o multidifusión. Tales respuestas pueden indicar un ataque de denegación de servicio (DoS) o un intento de sondear un equipo activo conocido. Microsoft recomienda configurar el parámetro **Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión** como **Habilitado** para ayudar a prevenir este tipo de ataques.
  
**Nota**: esta configuración de directiva no surte efecto si el mensaje de monodifusión es una respuesta a un mensaje de difusión DHCP que envía el equipo. Firewall de Windows permite siempre esas respuestas de monodifusión DHCP. Sin embargo, esta configuración de directiva puede interferir en los mensajes NetBIOS que detectan conflictos de nombres.
  
###### Firewall de Windows: definir excepciones de puerto
  
La lista de excepciones de puerto de Firewall de Windows debe ser definida por Directiva de grupo, de modo que pueda administrar e implementar de forma centralizada las excepciones de puerto, y asegurarse de que los administradores locales no crean configuraciones menos seguras.
  
Si habilita el parámetro **Firewall de Windows: definir excepciones de puerto**, puede ver y cambiar la lista de excepciones de programa que define Directiva de grupo. Para ver y modificar la lista de excepciones de puerto, configure el parámetro como **Habilitado** y haga clic en el botón **Mostrar**. Tenga en cuenta que si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores, lo que significa que puede crear accidentalmente varias entradas para el mismo puerto y que entren en conflicto los valores de Ámbito o Estado.
  
Si deshabilita el parámetro **Firewall de Windows: definir excepciones de puerto**, la lista de excepciones de puerto que define Directiva de grupo se elimina, pero otros parámetros de configuración pueden seguir abriendo o bloqueando puertos. Asimismo, si existe una lista de excepciones de puerto local, se pasa por alto a menos que habilite el parámetro **Firewall de Windows: permitir excepciones de puerto local**.
  
Para los entornos con aplicaciones no estándar que requieren que se abran determinados puertos debe considerarse la posibilidad de implementar excepciones de programa, en lugar de excepciones de puerto. Microsoft recomienda configurar el parámetro **Firewall de Windows: definir excepciones de puerto** como **Habilitado** y especificar una lista de excepciones de puerto sólo cuando no se pueden definir excepciones de programa. Las excepciones de programa permiten que Firewall de Windows acepte tráfico de red no solicitado únicamente mientras se ejecuta el programa especificado, y que a través de las excepciones de puerto se mantengan abiertos en todo momento los puertos especificados.
  
**Nota**: si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite mensajes de solicitud de eco entrante ICMP (como los enviados por la utilidad Ping), incluso si fuera a bloquearlos la configuración de directiva **Firewall de Windows: permitir excepciones ICMP**. Entre las configuraciones de directiva que pueden abrir el puerto TCP 445 se encuentran **Firewall de Windows: permitir la excepción compartir impresoras y archivos**, **Firewall de Windows: permitir excepción de administración remota** y **Firewall de Windows: definir excepciones de puerto**.
  
###### Firewall de Windows: permitir excepciones de puerto local
  
Esta configuración de directiva permite a los administradores usar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de puerto local. Firewall de Windows puede utilizar dos listas de excepciones de puerto; la otra se define mediante el parámetro **Firewall de Windows: definir excepciones de puerto**.
  
Si habilita el parámetro **Firewall de Windows: permitir excepciones de puerto local**, el componente Firewall de Windows del Panel de control permite a los administradores definir una lista de excepciones de puerto local. Si deshabilita esta configuración de directiva, el componente del Panel de control Firewall de Windows no permite a los administradores definir esa lista.
  
Normalmente, los administradores locales no están autorizados a anular las directivas organizativas y establecer sus propia listas de excepciones de puertos en los entornos EC o SSLF. Por eso, Microsoft recomienda configurar el parámetro **Firewall de Windows: permitir excepciones de puerto local** como **Deshabilitado.**
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Parámetros de Configuración de usuario
  
En las restantes secciones de este capítulo se incluyen recomendaciones sobre las opciones de Configuración de usuario. Recuerde que estos parámetros deben aplicarse a los usuarios, no a los equipos. Deben implementarse en una Directiva de grupo que esté vinculada a la unidad organizativa que contiene los usuarios que desea configurar. Como recordatorio puede consultar en el capítulo 2 la Figura 2.3, “Estructura de unidades organizativas ampliada para equipos Windows XP de escritorio y portátiles”. Estos parámetros se configuran en el Editor de objetos de directiva de grupo en la ubicación siguiente:
  
**Configuración de usuario\\Plantillas administrativas**
  
Esta ubicación se muestra en contexto en la figura siguiente:
  
[![](images/Cc163076.SGFG0405(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0405_big(es-es,technet.10).gif)
  
**Figura 4.5 Estructura de Directiva de grupo para Configuración de usuario**
  
Aplique estas opciones de configuración a través de un GPO (objeto de directiva de grupo) vinculado a una unidad organizativa que contenga cuentas de usuario.
  
**Nota**: los parámetros de Configuración de usuario se aplican a cualquier equipo Windows XP en el que inicie sesión un usuario en un dominio Active Directory. Sin embargo, los parámetros de configuración del equipo se aplican a todos los equipos cliente controlados por un GPO en Active Directory, independientemente del usuario que inicie sesión en el equipo. Por ese motivo, las tablas de esta sección contienen únicamente la configuración recomendada para los entornos EC y SSLF que se tratan en este capítulo. No existen recomendaciones de equipo de escritorio o portátil para estas configuraciones.
  
#### Componentes de Windows
  
En la figura siguiente se ilustran las secciones de Directiva de grupo que se verán afectadas por los cambios de configuración realizados en la sección Componentes de Windows:
  
[![](images/Cc163076.SGFG0406(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0406_big(es-es,technet.10).gif)
  
**Figura 4.6 Estructura de Directiva de grupo para Componentes de Windows en Configuración de usuario**
  
##### Internet Explorer
  
Puede establecer la siguiente configuración de usuario recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.27 Configuración de usuario recomendada para Internet Explorer**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Menús del explorador\Deshabilitar la opción Guardar este programa en disco</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Panel de control de Internet\Deshabilitar la página Opciones avanzadas</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Panel de control de Internet\Deshabilitar la página Seguridad</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la posibilidad de agregar canales</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar todas las páginas sin conexión programadas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar totalmente la interfaz de usuario del canal</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilita la descarga del contenido de las suscripciones a sitios</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la edición y creación de grupos de programaciones</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la edición de programaciones para páginas sin conexión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la cuenta de visitas a la página sin conexión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la posibilidad de quitar canales</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Páginas sin conexión\Deshabilitar la eliminación de programaciones para páginas sin conexión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configurar Outlook Express</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la configuración de página de Opciones avanzadas</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar cambio de valores de Configuración auto.</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar cambio de config. de certificados</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar cambio de configuración de conexión</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar el cambio de configuración de proxy</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir que Autocompletar guarde las contraseñas</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Menús del explorador\\Deshabilitar la opción Guardar este programa en disco
  
Esta configuración de directiva impide que los usuarios guarden en el disco duro un programa o un archivo que haya descargado Internet Explorer. Si habilita esta configuración de directiva, los usuarios no pueden guardar los programas en el disco mediante la opción **Guardar este programa en disco**. El archivo de programa no se descargará y se informará al usuario de que el comando no está disponible. Esta configuración de directiva ayuda a proteger los entornos de alta seguridad, ya que los usuarios no pueden descargar y guardar en disco a través de Internet Explorer programas potencialmente nocivos.
  
El parámetro **Menús del explorador\\Deshabilitar la opción Guardar este programa en disco** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
###### Panel de control de Internet\\Deshabilitar la página Opciones avanzadas
  
Esta configuración de directiva funciona conjuntamente con otros parámetros para que los usuarios no puedan cambiar los valores de la ficha **Opciones avanzadas** de la interfaz de usuario de Internet Explorer.
  
El parámetro **Panel de control de Internet\\Deshabilitar la página Opciones avanzadas** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
###### Panel de control de Internet\\Deshabilitar la página Seguridad
  
Esta configuración de directiva funciona conjuntamente con otros parámetros para que los usuarios no puedan cambiar los valores que se configuran a través de Directiva de grupo. Con esta configuración de directiva se quita la ficha **Seguridad** del cuadro de diálogo **Opciones de Internet**. Si habilita esta configuración de directiva, los usuarios no pueden ver ni cambiar parámetros de las zonas de seguridad tales como las secuencias de comandos, las descargas y la autenticación de usuarios. Microsoft recomienda habilitar esta configuración de directiva para que los usuarios no puedan cambiar parámetros y debilitar otras opciones de configuración de seguridad de Internet Explorer.
  
El parámetro **Panel de control de Internet\\Deshabilitar la página Seguridad** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
###### Páginas sin conexión\\Deshabilitar la posibilidad de agregar canales
  
Esta configuración de directiva impide a los usuarios agregar canales a Internet Explorer. Los canales son sitios web que se actualizan automáticamente en los equipos en los que se ejecuta Internet Explorer, según una programación de actualizaciones especificada por el proveedor de canal. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente. Es aconsejable permitir únicamente a un equipo descargar páginas de Internet siempre que un usuario realice solicitudes directamente desde el equipo.
  
Por esos motivos, el parámetro **Páginas sin conexión\\Deshabilitar la posibilidad de agregar canales** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión
  
Esta configuración de directiva impide a los usuarios especificar que las páginas web se pueden descargar y ver sin conexión. Esa capacidad permitiría a los usuarios ver páginas web cuando sus equipos no están conectados a Internet.
  
El parámetro **Páginas sin conexión\\Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar todas las páginas sin conexión programadas
  
Esta configuración de directiva deshabilita las programaciones que se hayan configurado para descargar páginas web destinadas a la visualización sin conexión. Si habilita esta directiva, se desactivarán las casillas de verificación correspondientes a las programaciones en la ficha **Programación** del cuadro de diálogo de **propiedades de la página web** para impedir que los usuarios las seleccionen. Para que se muestre esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas**, **Sincronizar**, seleccionar una página web y hacer clic en el botón **Propiedades** y en la ficha **Programación**. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilitar todas las páginas sin conexión programadas** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar totalmente la interfaz de usuario del canal
  
Esta configuración de directiva impide que los usuarios vean la interfaz de la Barra de canales. Los canales son sitios web que se actualizan automáticamente en los equipos, con una programación especificada por el proveedor de canal. Si habilita esta configuración de directiva, los usuarios no podrán tener acceso a la interfaz de la Barra de canales y activar la casilla de verificación **Barra de canales de Internet Explorer** en la ficha **web** del cuadro de diálogo **Propiedades de Pantalla**. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilitar totalmente la interfaz de usuario del canal** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilita la descarga del contenido de las suscripciones a sitios
  
Esta configuración de directiva impide a los usuarios descargar contenido de suscripciones de los sitios web. Sin embargo, la sincronización del contenido de la página web se sigue produciendo cuando el usuario vuelve a una página a la que tuvo acceso anteriormente para determinar si se ha actualizado algún contenido. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilita la descarga del contenido de las suscripciones a sitios** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la edición y creación de grupos de programaciones
  
Esta configuración de directiva impide a los usuarios agregar, editar o quitar programaciones para la revisión sin conexión de páginas web y grupos de páginas web a los que se suscriban. Un grupo de suscripción es una página web favorita que incluye las páginas web a las que está vinculada. Si habilita esta directiva, se atenúan los botones **Agregar**, **Quitar** y **Editar** de la ficha **Programación** del cuadro de diálogo **Propiedades de la página web**. Para que se muestre esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas** y después **Sincronizar** en Internet Explorer, seleccionar una página web, hacer clic en el botón **Propiedades** y después hacer clic en la ficha **Programación.** Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
Por esos motivos, el parámetro **Páginas sin conexión\\Deshabilitar la edición y creación de grupos de programaciones** se configura como **Habilitado** en los dos entornos definidos en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la edición de programaciones para páginas sin conexión
  
Esta configuración de directiva impide a los usuarios editar las programaciones que se hayan configurado para descargar páginas web a fin de revisarlas sin conexión. Si habilita esta directiva, los usuarios no podrán hacer que se muestren las propiedades de programación de las páginas que han configurado para la revisión sin conexión. No se mostrará ninguna propiedad cuando los usuarios hagan clic en **Herramientas**, **Sincronizar** en Internet Explorer, seleccionen una página web y después hacen clic en el botón **Propiedades.** Los usuarios no reciben ningún mensaje que indique que el comando no está disponible. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilitar la edición de programaciones para páginas sin conexión** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la cuenta de visitas a la página sin conexión
  
Esta configuración de directiva impide que los proveedores de canal puedan registrar la frecuencia con que los usuarios ven sus páginas de canal cuando están sin conexión. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilitar la cuenta de visitas a la página sin conexión** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la posibilidad de quitar canales
  
Esta configuración de directiva impide que los usuarios deshabiliten la sincronización de canales en Internet Explorer. Es aconsejable permitir únicamente a un equipo descargar páginas de Internet siempre que un usuario realice solicitudes directamente desde el equipo.
  
Por ese motivo, el parámetro **Páginas sin conexión\\Deshabilitar la posibilidad de agregar canales** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Páginas sin conexión\\Deshabilitar la eliminación de programaciones para páginas sin conexión
  
Esta configuración de directiva impide a los usuarios que desactiven la configuración previa de las páginas web con el fin de descargarlas para verlas sin conexión. Si habilita esta configuración de directiva, la configuración previa de las páginas web se protege. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
El parámetro **Páginas sin conexión\\Deshabilitar la eliminación de programaciones para páginas sin conexión** se configura como **Habilitado** en los dos entornos que se tratan en este capítulo.
  
###### Configurar Outlook Express
  
Esta configuración de directiva permite a los administradores habilitar y deshabilitar la capacidad de los usuarios de Microsoft Outlook Express® de guardar o abrir datos adjuntos que pueden contener un virus. Los usuarios no pueden deshabilitar el parámetro **Configurar Outlook Express** para que deje de bloquear datos adjuntos. Para exigir que se aplique esta configuración de directiva, haga clic en **Habilitar** y seleccione **Bloquear datos adjuntos que puedan contener virus**.
  
El parámetro **Configurar Outlook Express** se establece como **Habilitado** con la opción **Bloquear datos adjuntos que puedan contener virus** para los dos entornos que se tratan en este capítulo.
  
###### Deshabilitar la configuración de página de Opciones avanzadas
  
Esta configuración de directiva impide que los usuarios puedan cambiar la configuración en la ficha **Opciones avanzadas**, en el cuadro de diálogo **Opciones de Internet** de Internet Explorer. Si habilita esta configuración de directiva, los usuarios no podrán cambiar los parámetros de configuración avanzada que están relacionados con las características de seguridad, multimedia e impresión en el explorador. Tampoco podrán activar ni desactivar las casillas de verificación para estas opciones en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet.** Esta configuración de directiva impide también a los usuarios cambiar los parámetros que se configuran a través de Directiva de grupo.
  
El parámetro **Deshabilitar la configuración de página de Opciones avanzadas** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
**Nota**: si establece el parámetro **Deshabilitar la página Opciones avanzadas** (ubicado en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet), no necesita establecer esta configuración de directiva, ya que el parámetro **Deshabilitar la página Opciones avanzadas** quita la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet**.
  
###### Deshabilitar cambio de valores de Configuración auto.
  
Esta configuración de directiva impide a los usuarios cambiar los parámetros configurados automáticamente. Los administradores utilizan la configuración automática para actualizar los parámetros del explorador periódicamente. Si habilita esta configuración de directiva, se atenúan las propiedades de configuración de Internet Explorer. (Estos parámetros están ubicados en el área **Configuración automática** del cuadro de diálogo **Configuración LAN**). Esta configuración de directiva impide también a los usuarios cambiar los parámetros que se configuran a través de Directiva de grupo.
  
**Para ver el cuadro de diálogo Configuración LAN**
  
1.  Abra el cuadro de diálogo **Opciones de Internet** y haga clic en la ficha **Conexiones**.
  
2.  Haga clic en el botón **Configuración LAN** para ver los parámetros.
  
El parámetro **Deshabilitar cambio de valores de Configuración auto** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
**Nota**: el parámetro **Deshabilitar la página Conexiones** (ubicado en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet) quita la ficha **Conexiones** de Internet Explorer en el Panel de control y tiene prioridad con respecto a esta opción de configuración **Deshabilitar cambio de valores de Configuración auto**. Si se habilita el parámetro anterior, el último se pasa por alto.
  
###### Deshabilitar cambio de config. de certificados
  
Esta configuración de directiva impide que los usuarios puedan cambiar la configuración de certificados en Internet Explorer. Los certificados se utilizan para comprobar la identidad de los fabricantes de software. Si habilita esta configuración de directiva, se atenúan los parámetros de certificado en el área **Certificados** de la ficha **Contenido**, en el cuadro de diálogo **Opciones de Internet**. Esta configuración de directiva impide también a los usuarios cambiar los parámetros que se configuran a través de Directiva de grupo.
  
El parámetro **Deshabilitar cambio de config. de certificados** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
**Nota**: cuando esta configuración de directiva se habilita, los usuarios aún pueden hacer doble clic en el archivo de certificados de publicación de software (.spc) con el fin de ejecutar el Asistente para importación de Administrador de certificados. Este asistente permite a los usuarios importar y configurar propiedades para los certificados de los fabricantes de software que aún no se han configurado en Internet Explorer.
  
**Nota**: el parámetro **Deshabilitar la página Contenido** (ubicado en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet) quita la ficha **Contenido** de Internet Explorer en el Panel de control y tiene prioridad con respecto a esta opción de configuración **Deshabilitar cambio de valores de Configuración auto**. Si se habilita el parámetro anterior, el último se pasa por alto.
  
###### Deshabilitar cambio de configuración de conexión
  
Esta configuración de directiva impide a los usuarios cambiar los parámetros de conexión de acceso telefónico. Si habilita esta configuración de directiva, se atenuará el botón **Configuración** de la ficha **Conexiones** en el cuadro de diálogo **Opciones de Internet**. Esta configuración de directiva impide también a los usuarios cambiar los parámetros que se configuran a través de Directiva de grupo. Puede que desee deshabilitar esta directiva para los usuarios de equipos portátiles, en caso de que necesiten cambiar la configuración de conexión con motivo de sus viajes.
  
El parámetro **Deshabilitar cambio de configuración de conexión** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
**Nota**: si establece la configuración **Deshabilitar la página Conexiones** (que se encuentra en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet), no tiene que configurar esta configuración de directiva. Con la configuración **Deshabilitar la página Conexiones** se quita de la interfaz la ficha **Conexiones**.
  
###### Deshabilitar el cambio de configuración de proxy
  
Esta configuración de directiva impide a los usuarios cambiar los parámetros de proxy. Si habilita esta configuración de directiva, se atenúan las opciones de proxy. (La configuración de proxy está ubicada en el área **Servidor Proxy** del cuadro de diálogo **Configuración LAN**, que aparece cuando el usuario hace clic en la ficha **Conexiones** y, a continuación, en el botón **Configuración LAN** del cuadro de diálogo **Opciones de Internet**). Esta configuración de directiva también impide a los usuarios cambiar los parámetros que se configuran a través de Directiva de grupo. Puede que desee deshabilitar esta directiva para los usuarios de equipos portátiles, en caso de que necesiten cambiar la configuración de conexión con motivo de sus viajes.
  
El parámetro **Deshabilitar el cambio de configuración de proxy** se configura como **Habilitado** sólo para el entorno SSLF. Esta configuración de directiva no se configura para el entorno EC.
  
**Nota**: si establece la configuración **Deshabilitar la página Conexiones** (que se encuentra en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet), no tiene que configurar esta configuración de directiva. Con la configuración **Deshabilitar la página Conexiones** se quita de la interfaz la ficha **Conexiones**.
  
###### No permitir que Autocompletar guarde las contraseñas
  
Esta configuración de directiva deshabilita el autocompletado de los nombres de usuario y las contraseñas en formularios de páginas web e impide que se le pregunte al usuario si desea guardar las contraseñas Si habilita esta configuración de directiva, se atenúan las casillas de verificación **Nombres de usuario y contraseñas en formularios** y **Preguntar si se guardan las contraseñas**. Además, se impide que los usuarios guarden las contraseñas en una ubicación local. Para que se muestren estas casillas, los usuarios pueden abrir el cuadro de diálogo **Opciones de Internet**, hacer clic en la ficha **Contenido** y, a continuación, en el botón **Autocompletar**.
  
El parámetro **No permitir que Autocompletar guarde las contraseñas** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
##### Administrador de datos adjuntos
  
Puede establecer la siguiente configuración de usuario recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Administrador de datos adjuntos**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Administrador de datos adjuntos. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.28 Configuración de usuario recomendada para Administrador de datos adjuntos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No conservar la información de zona en los datos adjuntos de archivos</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ocultar mecanismos para eliminar la información de zona</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Notificar a los programas antivirus cuando se abren datos adjuntos</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### No conservar la información de zona en los datos adjuntos de archivos
  
Esta configuración de directiva le permite decidir si Windows debe marcar archivos adjuntos de Internet Explorer o de Outlook Express con información acerca de su zona de origen (restringida, Internet, intranet o local). Esta configuración de directiva requiere que los archivos sean descargados en particiones de disco NTFS para funcionar correctamente. Si no se conserva la información de zona, Windows no puede realizar apropiadamente evaluaciones de riesgo basadas en la zona de procedencia del archivo adjunto.
  
Si se habilita el parámetro **No conservar la información de zona en los datos adjuntos de archivos**, no se marcarán los archivos adjuntos con información de zona. Si esta configuración de directiva se deshabilita, Windows deberá almacenar los archivos adjuntos con la información de zona correspondiente. Dado que los archivos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza, como la zona Internet, Microsoft recomienda establecer esta configuración de directiva como **Deshabilitada** para asegurarse de que se conserva la máxima cantidad de información de seguridad posible con cada archivo.
  
El parámetro **No conservar la información de zona en los datos adjuntos de archivos** se configura como **Deshabilitado** para los dos entornos que se tratan en este capítulo.
  
###### Ocultar mecanismos para eliminar la información de zona
  
Esta configuración de directiva le permite administrar si los usuarios pueden quitar manualmente la información de zona de los archivos adjuntos guardados. Normalmente, los usuarios pueden hacer clic en el botón **Desbloquear** en la hoja de **Propiedades** del archivo o activar una casilla de verificación en el cuadro de diálogo **Advertencia de seguridad**. Si se quita la información de la zona, los usuarios pueden abrir archivos adjuntos potencialmente peligrosos que Windows ha impedido que abran.
  
Cuando se habilita el parámetro **Ocultar mecanismos para eliminar la información de zona**, Windows oculta la casilla de verificación y el botón **Desbloquear**. Cuando se deshabilita esta configuración de directiva, Windows muestra la casilla de verificación y el botón **Desbloquear**. Dado que los archivos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza, como la zona Internet, Microsoft recomienda establecer esta configuración de directiva como **Habilitada** para asegurarse de que se conserva la máxima cantidad de información de seguridad posible con cada archivo.
  
El parámetro **Ocultar mecanismos para eliminar la información de zona** se configura como **Habilitado** los dos entornos que se tratan en este capítulo.
  
**Nota**: para configurar si los archivos deben guardarse con información de zona, vea el parámetro anterior **No conservar la información de zona en los datos adjuntos de archivos.**
  
###### Notificar a los programas antivirus cuando se abren datos adjuntos
  
Los programas antivirus son obligatorios en muchos entornos y constituyen una sólida línea defensiva contra los ataques.
  
El parámetro **Notificar a los programas antivirus cuando se abren datos adjuntos** le permite administrar cómo se notifica a los programas antivirus registrados. Cuando se habilita, esta configuración de directiva determina que Windows llame al programa antivirus registrado para que analice los archivos adjuntos cuando los abren los usuarios. Si el análisis del antivirus no se lleva a cabo satisfactoriamente, se impide que se puedan abrir los archivos adjuntos. Si esta configuración de directiva se deshabilita, Windows no llama al programa antivirus registrado cuando se abren archivos adjuntos. Para procurar que los programas de detección de virus examinen todos los archivos antes de que sean abiertos, Microsoft recomienda establecer esta configuración de directiva como **Habilitada** en todos los entornos.
  
El parámetro **Notificar a los programas antivirus cuando se abren datos adjuntos** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
**Nota**: debe haberse instalado un programa antivirus actualizado para que esta configuración de directiva funcione correctamente. Muchos programas antivirus actualizados utilizan nuevas API que se incluyen con SP2.
  
##### Explorador de Windows
  
El Explorador de Windows se utiliza para explorar el sistema de archivos en equipos cliente en los que se ejecuta Windows XP Professional.
  
Puede establecer la siguiente configuración de usuario recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Explorador de Windows**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para el Explorador de Windows. La información adicional de cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 4.29 Configuración de usuario recomendada para el Explorador de Windows**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Quitar las características de grabación de CD</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Quitar la ficha Seguridad</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
###### Quitar las características de grabación de CD
  
Esta configuración de directiva quita las características integradas de Windows XP que permiten a los usuarios grabar CD a través del Explorador de Windows. Windows XP le permite crear y modificar CD regrabables si tiene una unidad de CD de lectura/escritura conectada al equipo. Esta característica se puede utilizar para copiar grandes cantidades de datos de un disco duro en un CD, que se puede extraer del equipo.
  
El parámetro **Quitar las características de grabación de CD** se establece como **No configurado** para el entorno EC. Sin embargo, esta configuración de directiva se establece como **Habilitada** para el entorno SSLF.
  
**Nota**: esta configuración de directiva no impide que aplicaciones de terceros que utilizan una grabadora de CD creen o modifiquen CD. En esta guía se recomienda el uso de directivas de restricción de software para bloquear la creación o la modificación de CD desde aplicaciones de terceros. Si desea más información, consulte el capítulo 6, "Directiva de restricción de software para clientes Windows XP".
  
Otra forma de impedir que los usuarios graben CD consiste en quitar las grabadoras de CD de los equipos cliente del entorno o reemplazarlas por unidades de CD de sólo lectura.
  
###### Quitar la ficha Seguridad
  
Esta configuración de directiva deshabilita la ficha **Seguridad** en los cuadros de diálogo de propiedades de carpeta y de archivo en el Explorador de Windows. Si habilita esta configuración de directiva, los usuarios no podrán obtener acceso a la ficha **Seguridad** después de abrir el cuadro de diálogo **Propiedades** para todos los objetos de sistema de archivos, lo que incluye carpetas, archivos, accesos directos y unidades. Dado que la ficha **Seguridad** es inaccesible, los usuarios no pueden cambiar la configuración ni ver la lista de usuarios.
  
Por esos motivos, el parámetro **Quitar la ficha Seguridad** es **No configurado** para el entorno EC. Sin embargo, esta configuración de directiva se establece como **Habilitada** para el entorno SSLF.
  
#### Sistema
  
En la figura siguiente se ilustran las secciones de Directiva de grupo que se verán afectadas por los cambios de configuración realizados en la sección Sistema:
  
[![](images/Cc163076.SGFG0407(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163076.sgfg0407_big(es-es,technet.10).gif)
  
**Figura 4.7 Estructura de Directiva de grupo para el Sistema en Configuración de usuario**
  
Puede establecer la siguiente configuración recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema**
  
##### Impedir el acceso a herramientas de edición del Registro
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para el Editor del Registro.
  
**Tabla 4.30 Configuración de usuario recomendada para el Editor del Registro**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Impedir el acceso a herramientas de edición del Registro</td>
<td style="border:1px solid black;">No configurado</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Esta configuración de directiva deshabilita los editores del Registro de Windows Regedit.exe y Regedt32.exe. Si habilita esta configuración de directiva, se mostrará un mensaje cuando los usuarios traten de utilizar un editor de Registro en el que se les informa de que no pueden utilizar ninguno de estos editores. Esta configuración de directiva impide a usuarios e intrusos la posibilidad de tener acceso al Registro mediante estas herramientas, pero no el acceso al Registro.
  
El parámetro **Impedir el acceso a herramientas de edición del Registro** es **No configurado** para el entorno EC. Sin embargo, esta configuración de directiva se establece como **Habilitada** para el entorno SSLF.
  
##### Sistema\\Administración de energía
  
Puede establecer la siguiente configuración recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema\\Administración de energía**
  
###### Solicitar contraseña al reanudar tras hibernación o suspensión
  
La tabla siguiente resume los parámetros de configuración recomendados para **Solicitar contraseña al reanudar tras hibernación o suspensión**.
  
**Tabla 4.31 Configuración de usuario recomendada para Sistema\\Administración de energía**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Solicitar contraseña al reanudar tras hibernación o suspensión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Esta configuración de directiva controla si los equipos cliente del entorno están bloqueados cuando reanudan el funcionamiento normal tras un estado de hibernación o suspensión. Si habilita esta configuración de directiva, los equipos cliente se bloquean cuando reanudan el funcionamiento normal y los usuarios deben escribir sus contraseñas para desbloquearlos. Pueden producirse infracciones de seguridad graves si esta configuración de directiva se deshabilita o no se establece, ya que cualquier persona puede tener acceso a los equipos cliente.
  
Por ese motivo, el parámetro **Solicitar contraseña al reanudar tras hibernación o suspensión** se configura como **Habilitado** para los dos entornos que se tratan en este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han descrito muchas de las configuraciones de seguridad importantes que se encuentran disponibles en las plantillas administrativas incluidas con Windows XP. Puede utilizar estas plantillas para proteger los equipos de escritorio y portátiles con Windows XP de su organización. Al analizar las directivas de configuración de seguridad de la organización, es importante tener presente el equilibrio entre seguridad y productividad del usuario. El objetivo consiste en proteger a los usuarios contra virus y programas malintencionados a través de un empleo seguro de los equipos que les permita realizar su trabajo plenamente sin sufrir las frustraciones que puedan provocar configuraciones de seguridad excesivamente restrictivas.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.
  
-   Para ver una lista completa de todas las configuraciones de Directiva de grupo de Plantillas administrativas disponibles en Windows XP y Windows Server 2003, descargue el libro [Group Policy Settings Reference for Windows Server 2003 with Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7821c32f-da15-438d-8e48-45915cd2bc14&displaylang=en), en www.microsoft.com/downloads/details.aspx?FamilyId=  
    7821C32F-DA15-438D-8E48-45915CD2BC14.
  
-   Para obtener información acerca de cómo crear sus propias plantillas administrativas, consulte el artículo técnico sobre la [implementación de la directiva de grupo basada en el Registro](http://www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp), en  
    www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp.
  
-   Para obtener información acerca de los informes de errores, consulte el sitio web de Windows sobre [informes de errores corporativos](http://www.microsoft.com/spain/licencias/sa/cer.mspx) en www.microsoft.com/resources/satech/cer/.
  
-   Para obtener información general acerca de Windows Server Update Services (WSUS), consulte la [información general del producto Windows Server Update Services](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx), en  
    www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx.
  
-   Para obtener información acerca de cómo implementar WSUS, consulte el artículo sobre [implementación de Microsoft Windows Server Update Services](http://technet.microsoft.com/en-us/library/cc708532.aspx), en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    /WSUS/WSUSDeploymentGuideTC/.
  
-   Para obtener más información acerca de la administración de directivas de grupo, consulte el artículo sobre [administración empresarial con la consola de administración de directivas de grupo](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx), en www.microsoft.com/windowsserver2003/gpmc/.
  
-   El sitio principal de [Seguridad](http://office.microsoft.com/en-us/assistance/ha011403061033.aspx) de Office 2003 incluye vínculos a artículos en los que se explica cómo utilizar las características y la configuración de seguridad de Office 2003 en  
    http://office.microsoft.com/en-us/assistance/HA011403061033.aspx.
  
-   En [los archivos de plantilla de directiva y herramientas de planeamiento para la implementación de Office 2003](http://technet.microsoft.com/es-es/library/cc179155.aspx) se incluyen los archivos de Plantilla administrativa de Directiva de grupo de Office y hojas de cálculo que resumen todos los parámetros de configuración disponibles. Estas herramientas están disponibles en  
    http://download.microsoft.com/download/9/5/f/95f7e000-d7ab-4b86-8a5d-804b124c7a69/Office-2003-SP1-ADMs-OPAs-and-Explain-Text.exe.
  
-   El [conjunto de herramientas del Kit de recursos de Office 2003](http://download.microsoft.com/download/0/e/d/0eda9ae6-f5c9-44be-98c7-ccc3016a296a/ork.exe) incluye archivos de plantilla de directiva y herramientas de planeamiento para la implementación de Office 2003, así como otras herramientas de utilidad para implementar y administrar Office 2003, en http://download.microsoft.com/download/0/e/  
    d/0eda9ae6-f5c9-44be-98c7-ccc3016a296a/ork.exe.
  
-   Para obtener más información acerca del [*Kit de administración de Internet Explorer*](http://www.microsoft.com/technet/prodtechnol/ie/ieak/), consulte www.microsoft.com/technet/prodtechnol/ie/ieak/.
  
##### Descargar
  
[![](images/Cc163076.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
  
[](#mainsection)[Principio de la página](#mainsection)
