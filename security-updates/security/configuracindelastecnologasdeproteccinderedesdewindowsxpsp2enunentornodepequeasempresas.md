---
TOCTitle: Configuración de las tecnologías de protección de redes de Windows XP SP2 en un entorno de pequeñas empresas
Title: Configuración de las tecnologías de protección de redes de Windows XP SP2 en un entorno de pequeñas empresas
ms:assetid: 'c74175c6-46bd-4fd2-976f-9b89daf37348'
ms:contentKeyID: 20200230
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875819(v=TechNet.10)'
---

Cómo configurar las tecnologías de protección de redes de Windows XP SP2 en un entorno de pequeñas empresas
===========================================================================================================

Publicado: diciembre 10, 2004 | Actualizado: julio 21, 2006

### En esta página

[](#ehaa)[Introducción](#ehaa)  
[](#egaa)[Antes de comenzar](#egaa)  
[](#efaa)[Aplicación de las revisiones de seguridad](#efaa)  
[](#eeaa)[Actualización de objetos de directiva de grupo existentes](#eeaa)  
[](#edaa)[Configuración de objetos de directiva de grupo](#edaa)  
[](#ecaa)[Acerca de la configuración de seguridad de Internet Explorer](#ecaa)  
[](#ebaa)[Aplicación de nuevas configuraciones con GPUpdate](#ebaa)  
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

El servicio de directorio Active Directory® proporciona una forma de administrar la configuración de seguridad de las estaciones de trabajo y los servidores de las pequeñas empresas de manera centralizada. Este servicio proporciona un entorno de estación de trabajo más seguro y fácil de administrar.

Este artículo trata sobre la administración central de las estaciones de trabajo que ejecutan Microsoft® Windows® XP con Service Pack 2 (SP2). Depende únicamente de Active Directory para aplicar objetos de directiva de grupo (GPO) en las estaciones de trabajo para administrar la configuración de seguridad.

#### Objetivo de este documento

Las organizaciones distintas tienen distintas necesidades de seguridad. Independientemente del nivel de seguridad que requieran los clientes, deberían utilizar los conceptos que aparecen en este artículo para facilitar la administración de la seguridad de la estación de trabajo.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

Debe haber iniciado sesión como miembro del grupo Adminis. del dominio para finalizar los procedimientos siguientes.

**Nota**   Si no puede realizar cambios en una estación de trabajo o en un servidor, puede que se deba a Directiva de grupo. En tal caso, tendrá que realizar los cambios en el nivel de directiva de grupo.

Complete las tareas que se describen en este documento para configurar las tecnologías de protección de redes de Windows XP SP2 con Directiva de grupo:

-   Aplicación de las revisiones de seguridad

-   Actualización de objetos de directiva de grupo (GPO) existentes

-   Configuración de los parámetros de Centro de seguridad

-   Configuración de los parámetros de Firewall de Windows

-   Configuración de los parámetros de Internet Explorer

-   Configuración de los parámetros de Administración de comunicaciones de Internet

-   Aplicación de la configuración con GPUpdate

[](#mainsection)[Principio de la página](#mainsection)

### Aplicación de las revisiones de seguridad

Microsoft recomienda que aplique las revisiones de seguridad y los Service Packs más actualizados en todas las estaciones de trabajo y servidores de Windows. Es aconsejable hacer copias de seguridad del equipo o de archivos importantes antes de aplicar las revisiones.

**Nota**   Algunas de las funcionalidades que aparecen en este artículo y algunas características de seguridad fundamentales dependen de las revisiones más recientes. Si los controladores de dominio no están actualizados, pueden no disponer de las plantillas administrativas que se necesitan para la estación de trabajo de Windows XP SP2 con GPO. Sin las plantillas administrativas, las nuevas características de seguridad de SP2 no estarán disponibles.

[](#mainsection)[Principio de la página](#mainsection)

### Actualización de objetos de directiva de grupo existentes

La mejor forma de administrar GPO en Active Directory es mediante la [Consola de administración de directivas de grupo de Microsoft (GPMC)](http://technet.microsoft.com/es-es/library/cc721918.aspx), que puede descargarse del sitio Web de Microsoft en www.microsoft.com/spain/servidores/windowsserver2003/technologies/management/grouppolicy/gpmc.aspx. Se trata de una opción alternativa al uso de Microsoft Management Console (MMC) con el complemento Editor de objetos de directiva de grupo (GPOE).

La GPMC también utiliza el Editor de objetos de directiva de grupo para editar GPO.

1.  Dentro de la GPMC, haga doble clic en el GPO que desee actualizar con la plantilla administrativa nueva. El GPO se abrirá en el GPOE.

2.  Haga clic en **Aceptar** y después en **Finalizar**. Con esta acción se aplica la plantilla nueva.

3.  Repita los pasos con cada GPO.

[](#mainsection)[Principio de la página](#mainsection)

### Configuración de objetos de directiva de grupo

Realice los procedimientos siguientes para configurar los GPO en su entorno.

#### Configuración de los parámetros de Centro de seguridad

Es posible habilitar Centro de seguridad en cada una de las estaciones de trabajo en el control de la Directiva de grupo. En el caso de que se encuentre instalado, Centro de seguridad puede informar a cada uno de los usuarios de las estaciones de trabajo acerca del estado de su Firewall de Windows, del antivirus y de la configuración de las Actualizaciones automáticas. De forma predeterminada, Directiva de grupo no habilita esta característica.

1.  Abra la GPMC y haga doble clic en el GPO que desee utilizar para aplicar Centro de seguridad en cada estación de trabajo.

2.  Dentro del GPO seleccionado, abra **Configuración de equipo**, **Plantillas administrativas**, **Componentes de Windows** y, a continuación, **Centro de seguridad**.

3.  Haga doble clic en **Activar el Centro de seguridad (sólo equipos de dominio)**.

4.  Habilite este parámetro.

5.  Haga clic en **Aceptar**.

#### Configuración de los parámetros de Firewall de Windows

Esta sección describe la configuración de Firewall de Windows en un GPO y la configuración que se recomienda para un entorno de pequeñas empresas.

1.  Dentro del GPO seleccionado, abra **Configuración del equipo**, **Plantillas administrativas**, **Red**, **Conexiones de red**, **Firewall de Windows** y, a continuación, **Perfil de dominio**.

2.  Haga doble clic en cada parámetro de configuración y defínalo de acuerdo con la información de la tabla siguiente.

    **Nota**   Tras habilitar **Definir excepciones de programas** en el perfil de dominio, debe especificar todos los programas a los que se les permitirá establecer conexiones con sus equipos antes de hacer clic en **Aceptar**.

**Tabla 1. Configuración recomendada de Firewall de Windows para pequeñas empresas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Perfil de dominio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Protección de todas las conexiones de red</td>
<td style="border:1px solid black;">Especifica que todas las conexiones de red tienen habilitado Firewall de Windows.</td>
<td style="border:1px solid black;">Habilitado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir excepciones</td>
<td style="border:1px solid black;">Especifica que todo el tráfico no solicitado se descarta, incluido el tráfico permitido.</td>
<td style="border:1px solid black;">No configurado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Definir excepciones de programas</td>
<td style="border:1px solid black;">Define el tráfico permitido en términos de nombres de archivos de programas.</td>
<td style="border:1px solid black;">Habilitado y configurado con los programas (aplicaciones y servicios) utilizados por los equipos basados en Windows XP SP2 de su red.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepciones de programas locales</td>
<td style="border:1px solid black;">Habilita la configuración local de excepciones de programa.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción de administración remota</td>
<td style="border:1px solid black;">Permite efectuar la configuración remota mediante el uso de herramientas.</td>
<td style="border:1px solid black;">Deshabilitado, a menos que quiera administrar sus equipos con complementos MMC de forma remota.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepción de impresión y archivos compartidos</td>
<td style="border:1px solid black;">Especifica si se permite el tráfico generado al compartir impresoras y archivos.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepciones ICMP</td>
<td style="border:1px solid black;">Especifica los tipos de mensajes ICMP que se permiten.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepción de escritorio remoto</td>
<td style="border:1px solid black;">Especifica si el equipo puede aceptar una solicitud de conexión basada en escritorio remoto.</td>
<td style="border:1px solid black;">Habilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir excepción del marco UPnP</td>
<td style="border:1px solid black;">Especifica si el equipo puede recibir mensajes UPnP no solicitados.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Prohibir notificaciones</td>
<td style="border:1px solid black;">Deshabilita las notificaciones.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir registro</td>
<td style="border:1px solid black;">Habilita el registro del tráfico y configura los parámetros de los archivos de registro.</td>
<td style="border:1px solid black;">No configurado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Prohibir respuesta de unidifusión para solicitudes de difusión o multidifusión</td>
<td style="border:1px solid black;">Descarta los paquetes de unidifusión recibidos como respuesta a un mensaje de solicitud de difusión o multidifusión.</td>
<td style="border:1px solid black;">Habilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Definir excepciones de puerto</td>
<td style="border:1px solid black;">Especifica el tráfico permitido en términos de TCP y UDP.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir excepciones de puerto local</td>
<td style="border:1px solid black;">Permite la configuración local de excepciones de puerto.</td>
<td style="border:1px solid black;">Deshabilitado.</td>
</tr>
</tbody>
</table>
  
Para obtener más detalles, consulte "[Cómo configurar Firewall de Windows en un entorno de pequeñas empresas mediante Directiva de grupo](http://www.microsoft.com/spain/empresas/seguridad/articulos/fwgrppol.mspx)" en www.microsoft.com/spain/empresas/seguridad/articulos/fwgrppol.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Acerca de la configuración de seguridad de Internet Explorer
  
La configuración de directiva de seguridad permite administrar determinados escenarios que pueden afectar a la seguridad de Internet Explorer. En la mayoría de los casos, se prefiere evitar un comportamiento determinado y, para ello, se debe comprobar que las características de seguridad están habilitadas. Microsoft recomienda utilizar Internet Explorer 6, ya que sus características nuevas aumentan la seguridad del explorador.
  
#### Zonas de seguridad
  
Internet Explorer clasifica los sitios Web en cuatro zonas de seguridad, cada una de las cuales proporciona niveles distintos de seguridad. Estas zonas son Internet, Intranet local, Sitios de confianza y Sitios restringidos. Cada zona se puede configurar de forma independiente con niveles de seguridad establecidos previamente de Bajo a Alto. Internet Explorer también ofrece la posibilidad de definir un conjunto personalizado de opciones de seguridad para cada una de las zonas. Microsoft ha definido la configuración de seguridad predeterminada para cada zona. La tabla siguiente proporciona una descripción de cada zona de seguridad, así como la configuración de seguridad predeterminada de Microsoft para cada una de ellas.
  
**Tabla 2. Descripciones de las zonas de seguridad y configuración de seguridad predeterminada**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Zona de seguridad</th>
<th style="border:1px solid black;" >Nivel de seguridad predeterminado</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet</td>
<td style="border:1px solid black;">Medio</td>
<td style="border:1px solid black;">La zona de Internet se compone de todos los sitios Web que no se incluyen en otras zonas.<br />
<br />
<strong>Nota</strong>   Las amenazas de Internet son una realidad. Como consecuencia de la gran preocupación de Microsoft por proteger a los usuarios frente a las amenazas de Internet no es posible configurar el nivel de seguridad como Bajo, ni siquiera con el botón avanzado <strong>Nivel personalizado</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Intranet local</td>
<td style="border:1px solid black;">Medio-bajo</td>
<td style="border:1px solid black;">Todos los sitios de esta zona están dentro del servidor de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Sitios de confianza</td>
<td style="border:1px solid black;">Bajo</td>
<td style="border:1px solid black;">Los sitios de la zona Sitios de confianza pueden llevar a cabo una gran cantidad de operaciones y desde ellos se les pedirá a los usuarios que tomen menos decisiones relacionadas con la seguridad. Los sitios sólo deberían agregarse a esta zona si se tiene la certeza de que ninguno de sus contenidos emprenderá acciones maliciosas en los equipos.<br />
Para esta zona, Microsoft recomienda que utilice el protocolo HTTPS o que se asegure de que todas las conexiones al sitio son completamente seguras.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Sitios restringidos</td>
<td style="border:1px solid black;">Alto</td>
<td style="border:1px solid black;">Esta zona está diseñada para permitir la adición de sitios que no se consideren de confianza. Controla y restringe las características Web, pero no bloquea el acceso al sitio. El usuario puede agregar sitios o venir determinados por Directiva de grupo. Para bloquear el acceso a los sitios Web, debe utilizar un servidor proxy que admita esa característica.</td>
</tr>
</tbody>
</table>
  
#### Aumento de la seguridad
  
Cada zona de seguridad contiene más de 30 parámetros de configuración que se pueden modificar de forma independiente para aumentar áreas determinadas de funcionalidad. La mayoría de los parámetros ofrecen la posibilidad de estar habilitados, deshabilitados o de solicitar una respuesta al usuario. Microsoft recomienda a los clientes limitar el número de opciones configuradas para solicitar una respuesta al usuario en todas las zonas de seguridad. Las directivas estrictas de seguridad de información limitan los permisos de usuario y evitan que éstos realicen acciones que puedan comprometer la seguridad. La configuración de las zonas de seguridad debe definirse y establecerse para zonas; no se recomienda, en ningún caso, el uso de un sólo conjunto de definiciones para todas las zonas. La tabla siguiente ofrece un “muestreo” de algunos parámetros de configuración predeterminados entre las zonas de seguridad. Éstos y otros parámetros pueden modificarse para ajustarse a las necesidades de la organización.
  
**Tabla 3. Parámetros de configuración de la directiva de zonas de seguridad**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Zona de seguridad</th>
<th style="border:1px solid black;" >Configuración de directiva</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet</td>
<td style="border:1px solid black;">Usar el bloqueador de elementos emergentes = Habilitado<br />
Pedir intervención del usuario automática para controles ActiveX = Deshabilitado<br />
Descarga de controles ActiveX firmados = Pedir datos<br />
Descarga de archivos = Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Intranet local</td>
<td style="border:1px solid black;">Usar el bloqueador de elementos emergentes = Deshabilitado<br />
Pedir intervención del usuario automática para controles ActiveX = Habilitado<br />
Descarga de controles ActiveX firmados = Pedir datos<br />
Descarga de archivos = Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Sitios de confianza</td>
<td style="border:1px solid black;">Usar el bloqueador de elementos emergentes = Deshabilitado<br />
Pedir intervención del usuario automática para controles ActiveX = Habilitado<br />
Descarga de controles ActiveX firmados = Habilitado<br />
Descarga de archivos = Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Sitios restringidos</td>
<td style="border:1px solid black;">Usar el bloqueador de elementos emergentes = Habilitado<br />
Pedir intervención del usuario automática para controles ActiveX = Deshabilitado<br />
Descarga de controles ActiveX firmados = Deshabilitado<br />
Descarga de archivos = Deshabilitado</td>
</tr>
</tbody>
</table>
 

ActiveX® es una plataforma de desarrollo Web de gran extensibilidad que propicia al usuario una experiencia en línea más completa. Muchos clientes empresariales utilizan controles ActiveX para aplicaciones de línea de negocios internas y, por lo tanto, ActiveX debe estar habilitado dentro de Internet Explorer. Sus estándares de seguridad y sus directivas de uso aceptables pueden requerir que se deshabilite ActiveX para la zona Internet. Desactivar los controles ActiveX, bien mediante Directiva de grupo, bien mediante el parámetro de configuración del conrol de la zona de seguridad a Alto, puede provocar un mal funcionamiento de los sitios Web. Microsoft recomienda a las organizaciones definir directivas para resolver este problema y preparar una estrategia para permitir el acceso basado en la justificación empresarial.

ActiveX es un objetivo de seguridad debido a su capacidad para ejecutar comandos dentro de la consola del explorador. Es aconsejable que ActiveX solo pueda ejecutarse desde sitios Web de confianza.

Existe una explicación más detallada de las zonas de seguridad y las opciones de configuración en "[Setting Up Security Zones](http://www.microsoft.com/spain/windows/ie/using/howto/security/settings.mspx)" en www.microsoft.com/spain/windows/ie/using/howto/security/settings.mspx.

#### Privacidad y cookies

En un intento por ofrecer mejores experiencias en línea personalizadas, algunos sitios Web almacenan información en pequeños archivos de texto en su equipo. Estos archivos se llaman cookies. Internet Explorer 6 dispone de diversos mecanismos para controlar la utilización de cookies.

Existen diferentes tipos. Las cookies de origen sólo pueden ser leídas por los sitios Web que las emiten. Otro tipo de cookies son las denominadas cookies de terceros, que son las que utilizan entidades Web para registrar información acerca de los visitantes. Las cookies de terceros pueden ser utilizadas por diversos sitios Web. La información que contienen varía desde las contraseñas e Id. de usuarios hasta códigos postales.

-   **Cookies de origen**. Sólo los sitios emisores pueden leerlas.

-   **Cookies de terceros**. Diversos sitios Web pueden leerlas y escribir en ellas.

Puede que los usuarios no sepan que tienen la capacidad de controlar la información que se almacena en las cookies. Con sólo hacer clic en una casilla de verificación para recordar una dirección de facturación, se puede dejar información no deseada en una cookie de origen o de terceros.

Cada organización debe determinar sus propias directivas con respecto a las cookies. Microsoft recomienda configurar el parámetro como mínimo en **Medio**. Este parámetro bloquea las cookies de terceros que no tienen una directiva de privacidad compacta, las cookies de terceros que utilizan información personal de identificación sin consentimiento implícito, y, además, restringe las cookies de origen que utilizan información personal de identificación sin consentimiento implícito. El parámetro **Alto** limita todas las cookies, mientras que los otros parámetros las permiten bajo ciertas circunstancias. El parámetro **Bajo** permite todas las cookies sin condición alguna.

Pueden añadirse sitios que omitan la configuración general. Las opciones para agregar un sitio son **Bloquear siempre** o **Permitir siempre**. Independientemente de lo restrictivo que decida ser, podrá agregar sitios. Se puede utilizar Directiva de grupo para aplicar tanto la configuración de las cookies como la de los sitios.

**Nota**   No se pueden controlar las cookies en cada zona. La configuración se generaliza en las cuatro zonas de seguridad.

#### Bloqueador de elementos emergentes

Sirve para bloquear la mayoría de las ventanas emergentes no deseadas. Las ventanas emergentes que se abren cuando el usuario hace clic en un vínculo no se bloquean. Se puede establecer su configuración por zonas, con lo que se permite que ciertos sitios estén bloqueados en una zona pero no en las otras. Se pueden utilizar Directiva de grupo para aplicar el bloqueador de elementos emergentes en cada zona y añadir una lista de sitios permitidos.

Los elementos emergentes pueden resultar incómodos, y tan numerosos y persistentes que el explorador resulta prácticamente inutilizable. Cada vez que se bloquea un elemento emergente, éste se anota en la barra de herramientas de Internet Explorer.

**Nota**   El bloqueador de elementos emergentes puede controlarse en cada zona, pero los sitios se agregan en las cuatro zonas.

#### Programas de Internet

Internet Explorer puede configurarse para iniciar otros programas para enviar correos electrónicos, administrar contactos o ver el código fuente de la página. Por ejemplo, cuando un usuario hace clic en una dirección de correo electrónico en una página Web, Internet Explorer abre el programa de correo electrónico definido, con un nuevo mensaje de correo electrónico saliente en el que aparece escrita la dirección. Esta funcionalidad proporciona una forma eficaz de enviar mensajes de correo electrónico sin la necesidad de abrir otro programa e introducir manualmente la dirección de correo electrónico. No obstante, junto a esta funcionalidad añadida, existen algunos riesgos potenciales. Los usuarios pueden experimentar un comportamiento o funcionamiento inesperado si alguno de los programas asociados se modifica desde las aplicaciones estándar de la organización. Directiva de grupo puede utilizarse para aplicar la configuración de esta lista de programas, con lo que se garantiza que no se iniciará ningún programa no deseado.

#### Complementos

Los complementos son pequeños programas diseñados para realizar funciones específicas, que una página Web puede cargar a petición. Las barras de herramientas y los objetos del ayudante del explorador (BHO) son otros tipos de programas que instalan botones y características adicionales para ampliar la funcionalidad del explorador. Microsoft recomienda a las organizaciones definir una lista de barras de herramientas de BHO aceptables, y que utilicen Directiva de grupo para aplicar dicha configuración.

Muchos desarrolladores utilizan la plataforma ActiveX para generar herramientas que aumenten la productividad o mejoren la funcionalidad. Microsoft anima a la comunidad de desarrollo a continuar ofreciendo estos complementos, pero reconoce la necesidad de implementar complementos de orígenes confiables. Internet Explorer 6 ofrece Authenticode para validar la autenticidad de un complemento a través de firmas digitales. Microsoft recomienda que las organizaciones sólo permitan complementos con firma en la zona Internet. Puede que los sitios de la zona Intranet local no requieran firmas Authenticode, ya que es probable que sean los desarrolladores internos de confianza quienes hayan diseño esos complementos.

#### Configuración de Directiva de grupo para Internet Explorer 6

Todas las características de seguridad de Explorer 6 pueden configurarse y protegerse mediante Directiva de grupo. Existe un gran número de parámetros de seguridad basados en objetos de directiva de grupo para administrar varios componentes de IE; en consecuencia, este documento se centra en las cuatro ramas primarias (a, b, c y d del siguiente procedimiento). El Editor de objetos de directiva de grupo proporciona detalles acerca de las ramificaciones de todos los parámetros de las cuatro ramas. Lea minuciosamente cada descripción y compruebe la eficacia de los parámetros deseados antes de su implementación.

1.  Abra la Consola de administración de directivas de grupo.

2.  Cree un nuevo objeto de directiva de grupo (GPO); por ejemplo, Internet Explorer 6.

3.  Las directivas de Internet Explorer se encuentran dentro de las siguientes cuatro ramas del árbol de directivas en el Editor de objetos de directiva de grupo. Configure cada objeto de directiva en las cuatro ramas para cumplir los requisitos de su organización.

    1.  **Configuración del equipo**, **Plantillas administrativas**, **Componentes de Windows**, **Internet Explorer**

        Dentro de esta rama, existen directivas de seguridad adicionales para bloquear la configuración de seguridad más allá de lo que permite el explorador. Una de las directivas más útiles es **Zonas de seguridad: no permitir a los usuarios cambiar las directivas**. Esta directiva está deshabilitada de forma predeterminada en el objeto de directiva de grupo. Al habilitarse, impide que el usuario pueda cambiar cualquiera de los parámetros de seguridad de la configuración del explorador. Microsoft recomienda configurarlo como **Habilitado**. Ni siquiera los administradores locales pueden cambiar dichos parámetros una vez configurados mediante Directiva de grupo. Existen muchas otras directivas que pueden habilitarse, algunas referentes a la seguridad y otras no. Lea las descripciones cuidadosamente antes de habilitarlas.

    2.  **Configuración del equipo**, **Plantillas administrativas**, **Sistema**, **Configuración de comunicaciones de Internet**

        Esta rama es específica para Windows XP SP2. Contiene 20 nuevas directivas que varían desde características de publicación Web hasta soporte multimedia. Una directiva, **Desactivar el servicio de Asociación de archivos de Internet**, evita que el explorador abra aplicaciones asociadas con extensiones de archivo cuando el contenido se descarga desde un sitio Web. Esta función es similar a la de apertura automática de Notepad.exe por parte del sistema operativo para archivos con la extensión .txt. Otra de las directivas, **Desactivar impresión a través de HTTP**, está diseñada para restringir la posibilidad de los usuarios de utilizar la impresora mediante HTTP a través de Intranet o de la intranet. Esta directiva no afecta a su capacidad de alojar una impresora HTTP propia. Lea las descripciones cuidadosamente antes de proceder a la habilitación.

    3.  **Configuración de usuario**, **Configuración de Windows**, **Mantenimiento de Internet Explorer**, **Seguridad**, **Programas**

        Estas dos secciones contienen parámetros y directivas que afectan a la seguridad del explorador. Ambas secciones contienen parámetros de usuario que se encuentran en la configuración de seguridad y privacidad de cada explorador particular. Se recomienda utilizar los parámetros predeterminados mínimos de Microsoft, pero las configuraciones deberían establecerse para cumplir los requisitos de la organización.
  
        **Nota**   Pueden agregarse sitios a todas las zonas excepto a la de Internet. Elija los sitios para añadirlos a Intranet local, Zonas restringidas y Zonas de confianza, ya que se aplican a todas las estaciones de trabajo y servidores vinculados al GPO.

    4.  **Configuración del usuario**, **Plantillas administrativas**, **Componentes de Windows**, **Internet Explorer**

        Esta rama contiene parámetros de configuración detallados para restringir los cambios de la configuración del explorador, en lugar de restringir completamente la posibilidad de los usuarios de efectuar cambios. Estos parámetros se aplican a cambios de elementos como los controles de archivos temporales de Internet y el cambio de la página principal. Esta rama contiene diversas opciones de configuración. Microsoft recomienda a los administradores leer y comprobar sus efectos antes de utilizarlas en un entorno de producción.

4.  Cuando acabe con el editor de directivas, vincule el nuevo GPO a todos los dominios con los servidores y estaciones de trabajo de Windows.

5.  Configure **Filtrado de seguridad** para el GPO en función de los grupos, usuarios y equipos a los que debería afectar. Algunas directivas están diseñadas para equipos y otras sólo se aplican a los usuarios.

[](#mainsection)[Principio de la página](#mainsection)

### Aplicación de nuevas configuraciones con GPUpdate

La utilidad GPUpdate actualiza la configuración de Directiva de grupo basada en Active Directory. Después de configurar Directiva de grupo, puede esperar a que se aplique la configuración a los equipos cliente mediante los ciclos de actualización estándar. De forma predeterminada, estos ciclos de actualización tienen una periodicidad de 90 minutos, con una variación aleatoria de +/- 30 minutos. Este procedimiento puede hacer que la directiva de prueba pase a la estación de trabajo más rápidamente.

Para actualizar Directiva de grupo entre ciclos estándar, sírvase de la utilidad GPUpdate como sigue:

1.  Desde el escritorio de Windows XP SP2, haga clic en **Inicio** y después haga clic en **Ejecutar**.

2.  En el cuadro **Abrir**, escriba **cmd** y después haga clic en **Aceptar**. Se mostrará una ventana del símbolo del sistema.

3.  En el símbolo del sistema, escriba **GPUpdate** y haga clic en **OK**. Deberá ver el mensaje que se muestra en la siguiente captura de pantalla:

    [![](images/Cc875819.XPNPT01(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875819.netprt03(es-es,technet.10).gif)

    Para cerrar el símbolo del sistema, escriba **exit** y después presione la tecla Entrar.

[](#mainsection)[Principio de la página](#mainsection)

### Información relacionada

Para obtener definiciones de términos relacionados con la seguridad, consulte:

-   El [Glosario de seguridad de Microsoft](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx), disponible en el sitio Web de Microsoft, http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx.

Para obtener más información acerca de la protección de redes de Windows XP SP2, consulte:

-   "[Cambios de funcionalidad en Service Pack 2 de Microsoft Windows XP - Parte 2: Tecnologías para la protección de redes](http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx)", en el sitio Web de Microsoft TechNet en http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx.

-   "[Using Windows XP Professional with Service Pack 2 in a Managed Environment: Controlling Communication with the Internet](http://www.microsoft.com/spain/technet/recursos/articulos/mngintro.mspx)", en el sitio Web de Microsoft TechNet en http://www.microsoft.com/spain/technet/recursos/articulos/mngintro.mspx.

-   [Deploying Windows Firewall Settings for Microsoft Windows XP with Service Pack 2](http://www.microsoft.com/spain/technet/recursos/articulos/adprtect.mspx), en el sitio Web del Centro de descarga de Microsoft, en http://www.microsoft.com/spain/technet/recursos/articulos/adprtect.mspx.

Para obtener más información acerca de la seguridad de Windows XP SP2, consulte:

-   [*Guía de seguridad de Windows XP*](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc), en el sitio Web del centro de descarga de Microsoft, en http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/GuideforWinXPProSP2inSMB.doc.

-   [*Windows XP Security Guide Appendix A: Key Settings to Consider*](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc), en el sitio Web de Microsoft TechNet, en http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/GuideforWinXPProSP2inSMB.doc.

Para obtener más información acerca de Directiva de grupo, consulte:

-   "[Troubleshooting Group Policy in Microsoft Windows Server](http://go.microsoft.com/fwlink/?linkid=35481)", en el sitio Web del Centro de descarga de Microsoft, en http://go.microsoft.com/fwlink/?linkid=35481.

-   [Enterprise Management with the Group Policy Management Console](http://technet.microsoft.com/es-es/library/cc721918.aspx), en el sitio Web de Microsoft Windows Server System, en http://www.microsoft.com/spain/servidores/windowsserver2003/technologies/management/grouppolicy/gpmc.aspx.

[](#mainsection)[Principio de la página](#mainsection)

**Descarga**

[Obtener Cómo configurar las tecnologías de protección de redes de Windows XP SP2 en un entorno de pequeñas empresas](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc)

[](#mainsection)[Principio de la página](#mainsection)
