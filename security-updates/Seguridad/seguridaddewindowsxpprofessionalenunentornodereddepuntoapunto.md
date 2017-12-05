---
TOCTitle: Seguridad de Windows XP Professional en un entorno de red de punto a punto
Title: Seguridad de Windows XP Professional en un entorno de red de punto a punto
ms:assetid: '8dbc5935-ec3e-4b06-bc4e-4edf8aace9e2'
ms:contentKeyID: 20200263
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875837(v=TechNet.10)'
---

Seguridad de Windows XP Professional en un entorno de red de punto a punto
==========================================================================

Actualizado: julio 21, 2006

##### En esta página

[](#efaa)[Introducción](#efaa)  
[](#eeaa)[Antes de comenzar](#eeaa)  
[](#edaa)[Seguridad del sistema de archivos](#edaa)  
[](#ecaa)[Firewall de Windows](#ecaa)  
[](#ebaa)[Actualización de las revisiones de seguridad](#ebaa)  
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

Las redes de punto a punto pueden aumentar la productividad, ya que facilitan el uso compartido de información y recursos en la red. No obstante, la posibilidad de los usuarios de controlar el acceso a los equipos puede dejar indefensos a éstos frente a la pérdida o apropiación de información, así como al uso compartido involuntario de archivos. Por ello, además de imponer una directiva de informática corporativa, se debe garantizar que todo el personal comprende los aspectos básicos de la seguridad y de la red de punto a punto de Windows.

Con la amenaza del código malicioso, como, por ejemplo, gusanos, virus, troyanos y spyware, y también de los piratas informáticos, resulta crucial adoptar con rapidez las medidas necesarias para bloquear los equipos portátiles y de escritorio. En este documento se explica cómo implementar medidas de seguridad en entornos de pequeñas y medianas empresas en los que se utilizan redes de punto a punto. Estas recomendaciones permiten asegurar que los equipos con Microsoft® Windows® XP Professional con Service Pack 2 (SP2) estarán más protegidos, al mismo tiempo que garantizan a los usuarios la eficacia y la productividad de dichos equipos.

#### Objetivo de este documento

Una vez que se haya familiarizado con la información de este documento, podrá aumentar la seguridad de un grupo de trabajo de punto a punto.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

Al igual que las demás recomendaciones de seguridad, esta guía pretende encontrar el equilibrio adecuado entre una seguridad mejorada y una capacidad de uso aceptable. Las recomendaciones facilitadas en este documento se podrán aplicar sin problemas en implementaciones de Windows XP Professional SP2 en una gran variedad de entornos. No obstante, antes de implementarlas, tenga en cuenta que este documento no trata la extensa gama de necesidades y configuraciones que pueden resultar necesarias en una organización de gran tamaño. Asimismo, puede que la guía no cubra las necesidades de seguridad específicas de algunas organizaciones.

#### Cumplimiento con el requisito del Service Pack

Las recomendaciones de este documento se aplican únicamente a los equipos con Windows XP Professional con SP2 que son miembros de un grupo de trabajo, no de un dominio. Si el SP2 no está instalado en un equipo determinado, o si no sabe si está instalado, puede ir a la página [Microsoft Update](http://windowsupdate.microsoft.com/) del sitio Web de Microsoft en http://windowsupdate.microsoft.com, y se analizará su equipo para encontrar las actualizaciones disponibles. Si aparece el SP2 como actualización disponible, instálelo antes de iniciar los procedimientos contenidos en este documento.

**Nota**   Para instalar el SP2, es necesario reiniciar el equipo.

#### Requisitos administrativos

Debe haber iniciado la sesión como administrador o miembro del grupo de administradores para finalizar los procedimientos siguientes. Si el equipo está conectado a una red, puede que la configuración de la directiva de red también impida que finalice dichos procedimientos.

[](#mainsection)[Principio de la página](#mainsection)

### Seguridad del sistema de archivos

Un sistema de archivos determina el modo en que se organizan en el equipo los diferentes directorios y archivos. Existen varias formas de proteger el sistema de archivos contra la eliminación, alteración o acceso no autorizado. Esta sección proporciona instrucciones paso a paso para completar las siguientes tareas, que le ayudarán a mantener seguro el sistema de archivos:

-   Conversión de sistemas de archivos a NTFS

-   Utilización del software antivirus

-   Utilización de Windows Defender (Beta 2)

-   Protección de recursos compartidos de archivo

-   Seguridad de carpetas compartidas

-   Deshabilitación de servicios innecesarios

-   Deshabilitación o eliminación de cuentas innecesarias

#### Conversión de los sistemas de archivos a NTFS

Durante el proceso de instalación de Windows XP, los equipos se pueden configurar para que utilicen el sistema de archivos FAT32 o NTFS.

FAT32 es una tecnología más antigua que se utiliza en las versiones anteriores de Windows. El sistema de archivos NTFS es más rápido y más seguro que FAT32 y que muchos otros sistemas anteriores. Para garantizar un rendimiento óptimo del sistema operativo, se recomienda proteger todas las particiones del sistema de archivos del equipo con NTFS. Siga los dos procedimientos siguientes para comprobar, en primer lugar, el tipo de sistema de archivos del equipo y, si resulta necesario, convertirlo a continuación a NTFS.

**Importante**   Tenga en cuenta las limitaciones siguientes antes de convertir una partición FAT a NTFS:

-   La conversión es un proceso unidireccional. Tras converitir una partición a NTFS, no es posible volver a convertirla a FAT. Para restaurar la partición como FAT, es necesario volver a formatearla como FAT, proceso que elimina todos los datos de la partición. En este caso, sería necesario restaurar los datos a partir de la copia de seguridad.

-   Tras convertir cualquier unidad del equipo a NTFS, no será posible eliminar Windows XP para restituir de nuevo Windows 98 o Windows Millennium Edition (Me).

-   Convert.exe precisa de una determinada cantidad de espacio libre en la unidad para poder convertir el sistema de archivos. Para obtener más información acerca de la cantidad de espacio libre necesaria para la conversión, consulte el artículo de Microsoft Knowledge Base
    [Espacio libre necesario para convertir FAT a NTFS](http://support.microsoft.com/kb/156560) en http://support.microsoft.com/kb/156560.

**Para comprobar el tipo de sistema de archivos del equipo**

1.  En el menú **Inicio**, haga clic en **Mi PC**.

2.  Haga clic con el botón secundario del mouse en la letra de unidad que desea comprobar y haga clic en **Propiedades**.

3.  El tipo de sistema de archivos debería ser NTFS, como se muestra en la siguiente captura de pantalla. Si no lo es, puede utilizar la utilidad Convert.exe para convertir de FAT16 o FAT32 a NTFS.

    ![](images/Cc875837.XPP2P01(es-es,TechNet.10).gif)

Repita este procedimiento con todas las particiones ubicadas en los discos duros del equipo. Aunque el sistema de archivos se configurara como FAT32 cuando se instaló el sistema operativo, se puede convertir fácilmente a NTFS para incrementar la seguridad.

Para hacerlo, apunte el nombre del disco, también conocido como la etiqueta del volumen (en la ilustración anterior sería Unidad C). A continuación, realice los siguientes pasos para convertir el sistema de archivos a NTFS y obtener así un mayor nivel de seguridad en el equipo.

**Para convertir el sistema de archivos a NTFS**

1.  Haga clic en **Inicio**, **Ejecutar**, escriba **cmd** y, a continuación, haga clic en **Aceptar**.

2.  En el símbolo del sistema, escriba lo siguiente, donde *&lt;drive\_letter&gt;* hace referencia a la unidad que quiere convertirse, y, después, presione Entrar:

    **convert** ***&lt;drive\_letter&gt;*: /fs:ntfs**

3.  Se le pedirá que especifique la etiqueta de volumen correspondiente a la unidad. Especifique la etiqueta de volumen anotada anteriormente y presione Entrar.

4.  Una vez finalizada la conversión, escriba **exit** y, a continuación, presione Entrar para cerrar el símbolo del sistema.

    **Nota**   Si trata de realizar este procedimiento en la unidad en la que se encuentra instalado el sistema operativo, puede que se le pregunte si desea programar la conversión para que se produzca la próxima vez que se reinicie el sistema. De ser así, escriba **s** y presione Entrar para reiniciar el equipo.

#### Utilización del software antivirus

Los virus informáticos son programas que se cargan en el equipo sin el conocimiento o la aprobación del usuario. Tanto los virus como otros tipos de software malicioso llevan existiendo durante años. Los virus actuales pueden replicarse de forma automática y utilizar Internet y las aplicaciones de correo electrónico para propagarse por todo el mundo en menos de una hora.

Un programa de software antivirus le ayudará a proteger el equipo contra gran cantidad de virus, gusanos, troyanos y demás códigos maliciosos. Un software antivirus examina continuamente el equipo en busca de virus y permite eliminarlos una vez detectados. Sin embargo, hay que tener en cuenta que la instalación de un antivirus sólo soluciona parte del problema. Para proteger los equipos portátiles y de escritorio, también resulta esencial mantener actualizados los archivos de firma.

Gran cantidad de equipos incorporan este tipo de software. No obstante, los programas antivirus necesitan una suscripción para que sea posible actualizarlos. Si no dispone de una suscripción actual para dichas actualizaciones, es muy probable que el equipo se quede indefenso ante nuevas amenazas.

Otra medida fundamental a la hora de impedir los ataques de virus consiste en fomentar la educación del usuario en lo que respecta a las prácticas de correo electrónico seguras. Los usuarios no deberían abrir mensajes de correo electrónico ni manipular los archivos adjuntos a no ser que los estén esperando. Asimismo, se recomienda examinar todos los archivos adjuntos con un software antivirus antes de ejecutarlos.

Microsoft ha elaborado Windows Live OneCare, un servicio de protección de actualización automática para equipos que se ejecuta en segundo plano. Dicho servicio proporciona una protección constante contra virus, piratas informáticos y otras amenazas, y ayuda a mantener el equipo a punto y a realizar copias de seguridad de documentos importantes. Para obtener más información, consulte [Windows Live OneCare](http://www.microsoft.com/spain/athome/security/update/onecare_live.mspx) en www.microsoft.com/spain/athome/security/update/onecare\_live.mspx.

Para obtener más información sobre los proveedores de software que proporcionan software antivirus compatible con Windows XP, consulte la página [Lista de proveedores de software antivirus](http://support.microsoft.com/kb/49500) en el sitio Web de Microsoft en http://support.microsoft.com/kb/49500.

#### Utilización de Microsoft Defender

Windows Defender (Beta2) es una tecnología de seguridad que ayuda a proteger a los usuarios de Windows del spyware y de otros tipos de software potencialmente no deseados. El spyware identificado en el equipo puede detectarse y eliminarse, lo que contribuye a reducir sus efectos negativos, incluida la ralentización del equipo, la aparición de anuncios emergentes molestos, los cambios no deseados de la configuración de Internet y el uso no autorizado de la información privada. La protección continua mejora la seguridad de la exploración de Internet mediante la protección de más de 50 vías por las que el spyware puede introducirse en el equipo. Los integrantes de la comunidad de ámbito mundial SpyNet™ desempeñan una labor clave a la hora de determinar qué programas sospechosos pueden clasificarse como spyware. En consecuencia, los investigadores de Microsoft desarrollan rápidamente métodos para contrarrestar dichas amenazas y las actualizaciones resultantes se descargan automáticamente en los equipos para que estén totalmente al día.

Puede descargar [Windows Defender](http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx) en http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx. La versión actual es la Beta 2. El nombre del archivo es WindowsDefender.msi y ocupa unos 5,5 MB. (El nombre y el tamaño del archivo pueden modificarse tras el lanzamiento completo.)

#### Protección de recursos compartidos de archivos

Los recursos compartidos de archivos de Windows XP Professional son una forma de compartir archivos de la unidad de disco duro local con usuarios de otros sistemas basados en Windows. Puede darse un nombre compartido y permisos a todo un directorio o carpeta para que el recurso compartido pueda asignarse a otros usuarios o grupos de usuarios. Los recursos compartidos de archivos funcionan de la misma manera, tanto si la estación de trabajo es miembro de un dominio como si lo es de un grupo de trabajo. En ambas configuraciones, puede crearse un recurso compartido para permitir que usuarios de otras estaciones de trabajo puedan obtener acceso a un directorio de una unidad de disco duro local. Un usuario de la estación de trabajo Windows XP Professional puede asignar permisos para estos recursos compartidos a cuentas locales y grupos en ambas configuraciones, pero sólo podrá asignar accesos para las cuentas de servicio y los grupos del directorio de Active Directory® si la estación de trabajo es miembro de Active Directory.

Los recursos compartidos se crean de forma predeterminada con la opción Todos y control total. Deberán modificarse estos permisos de forma que sólo se permita el acceso al recurso compartido a aquellos que lo necesiten. Además, pueden limitarse las cuentas de usuario y los grupos de cuentas de usuario a lo que pueden hacer en un recurso compartido según los permisos asignados; esto es, pueden limitarse a un acceso de sólo lectura o pueden asignárseles permisos para crear, cambiar e, incluso, eliminar archivos.

Los recursos compartidos de archivos están diseñados para su uso en redes domésticas o redes de negocios protegidas por un servidor de seguridad, como Firewall de Windows (proporcionado con Windows XP SP2). Si está conectado a Internet y no trabaja detrás con un servidor de seguridad, recuerde que cualquier uso compartido de archivo que cree estará accesible a cualquier usuario de Internet.

#### Seguridad de carpetas compartidas

Las redes de punto a punto de Windows le permiten compartir el contenido del sistema de archivos con otros equipos de la red. En el siguiente conjunto de pasos se asume que ya ha compartido una o varias carpetas del sistema de archivos. Si se cambia parte de la configuración predeterminada del sistema de archivos, puede restringirse el acceso no autorizado a los recursos compartidos.

-   Todos los usuarios que necesiten obtener acceso a los recursos compartidos desde sus equipos necesitarán, además, una cuenta de usuario en la estación de trabajo que contenga los recursos compartidos. Este requisito constituye una limitación de la configuración de red de un grupo de trabajo de punto a punto. Se recomienda mantener al mínimo el número de equipos con directorios compartidos. Si posee recursos compartidos en todas las estaciones de trabajo, deberá tener cuentas de usuario en todas ellas, lo que puede provocar que la configuración pase a ser excesivamente compleja en un corto período de tiempo.

-   Puede establecer permisos únicamente en las unidades que cuenten con el formato para utilizar el sistema de archivos NTFS.

-   En los siguientes pasos, se proporcionan las instrucciones para eliminar el grupo especial **Todos**, que proporciona un acceso anónimo. A continuación, deberá asignar permisos para **Leer** o **Cambiar** la carpeta de recursos compartidos a todas las cuentas de usuario locales.

    -   **Leer** proporciona a una cuenta de usuario los permisos pertinentes para enumerar, abrir y copiar archivos del recurso compartido a otra ubicación.

    -   **Cambiar** proporciona a una cuenta de usuario la capacidad de enumerar, agregar, modificar y eliminar archivos.

    Deberá seleccionar tanto **Cambiar** como **Leer** para asignar los permisos para **Cambiar**. Limite el número de usuarios a los que vaya a asignar permisos para **Cambiar**. No se recomienda la asignación de **Control total** de los recursos compartidos a otras cuentas de usuario. **Control total** proporciona a los usuarios los mismos permisos que **Cambiar**, además de la capacidad de adoptar la propiedad de archivos y directorios y de cambiar permisos.

**Para asegurar una carpeta compartida:**

1.  Haga clic con el botón secundario del mouse en una carpeta que ya se haya compartido y, a continuación, seleccione **Compartir y Seguridad**.

2.  En la ficha **Compartir**, haga clic en **Permisos**. Aparecerá una pantalla parecida a la siguiente.

    ![](images/Cc875837.XPP2P02(es-es,TechNet.10).gif)

3.  Seleccione el grupo **Todos** y, a continuación, haga clic en **Quitar**.

4.  Haga clic en **Agregar** para seleccionar los usuarios que pueden tener acceso a la carpeta.

5.  En el cuadro de diálogo **Seleccionar usuarios,** **o Grupos**, haga clic en **Tipos de objetos**.

6.  Desactive las casillas de verificación **Ppios. seguridad integrados** y **Grupos** y, a continuación haga clic en **Aceptar**.

7.  Haga clic en **Avanzadas**.

8.  Haga clic en **Buscar ahora**.

9.  Haga clic para resaltar los usuarios a los que desea autorizar el acceso a la carpeta. Una vez seleccionados los usuarios, haga clic en **Aceptar**.

10. A partir de ahora, cada usuario de la lista de permisos necesitará obtener el tipo correcto de acceso. Haga doble clic en un usuario y, a continuación, desactive la casilla de verificación **Permitir**, situada junto a **Control total**. Tras esto, seleccione si desea que el usuario tenga permiso para**Cambiar** y **Leer**, o sólo para **Leer**.

11. Haga clic en **Aceptar**.

12. Vuelva a hacer clic en **Aceptar** para cerrar el cuadro de diálogo **Permisos de la carpeta**.

    **Nota**   Si las casillas de verificación del cuadro de diálogo Permisos no están disponibles, los permisos se heredan de la carpeta principal.

#### Deshabilitación de servicios innecesarios

Mediante la deshabilitación de servicios innecesarios, podrá reducir las posibilidades de que se produzcan vulnerabilidades conocidas o desconocidas. Utilice Agregar o quitar programas del Panel de control para deshabilitar dichos servicios.

Para obtener una lista de los servicios y sus configuraciones, consulte la página Default settings for services en el sitio Web de [Microsoft Windows XP Professional Documentation](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/sys_srv_default_settings.mspx?mfr=true) en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/
en-us/sys\_srv\_default\_settings.mspx?mfr=true.

#### Deshabilitación o eliminación de cuentas innecesarias

Deshabilite o elimine todas las cuentas de usuario que no necesite. Mediante la deshabilitación o eliminación de cuentas innecesarias, podrá reducir las posibilidades de que se produzca un acceso no autorizado a su equipo.

**Para deshabilitar una cuenta**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**.

2.  Haga doble clic en **Cuentas de usuario**.

3.  Haga clic en la ficha **Avanzadas** y, a continuación, haga clic en el botón **Avanzadas**.

4.  Haga clic en **Usuarios**.

5.  Haga doble clic en una cuenta de usuario para visualizar el cuadro de diálogo de propiedades.

6.  Active la casilla de verificación **Cuenta deshabilitada**.

**Nota**   La cuenta deshabilitada seguirá existiendo aunque el usuario no esté autorizado a iniciar sesión. El icono aparece en el panel de detalles de **Usuarios**, pero con una X encima.

**Para eliminar una cuenta**

1.  Repita los pasos del 1 al 4 del procedimiento anterior.

2.  En lugar de hacer doble clic sobre la cuenta, haga clic en ella con el botón secundario del mouse y seleccione **Eliminar**.

    -   Antes de eliminar las cuentas de usuario, deshabilítelas. Una vez que se haya asegurado de que la deshabilitación de la cuenta no ha causado ningún problema, podrá eliminarla con seguridad.

    -   Una cuenta de usuario eliminada no se puede restaurar.

    -   Las cuentas integradas Administrador e Invitado no se pueden eliminar.

#### Seguridad de las cuentas de usuario

Mediante el uso de contraseñas y la configuración de bloqueos de cuentas, podrá reducir las posibilidades de que se produzca un acceso no autorizado a su equipo.

##### Utilización de contraseñas

Es importante que todas las cuentas de usuario de las estaciones de trabajo tengan contraseña. Si se dejan las contraseñas en blanco, otras personas podrán obtener acceso a los equipos con identidades ajenas.

-   No utilice una cuenta de invitado en las estaciones de trabajo. De hecho, debería estar deshabilitada.

-   Todos los usuarios deberán tener sus propias cuentas de usuario. No deberán compartirse ni las cuentas de usuario ni las contraseñas.

Suelen confundirse dos conceptos en relación con las contraseñas. Las cuentas de usuario pueden quedar bloqueadas, lo que suele ocurrir cuando se intenta iniciar sesión con una contraseña incorrecta demasiadas veces. Si esto sucede, bastará con desbloquear la cuenta; no hará falta restablecer la contraseña a no ser que el usuario la haya olvidado. Un buen ejemplo de esto, y, probablemente, el más común, es el bloqueo que se produce al tener activada la tecla Bloq Mayús cuando se está escribiendo la contraseña.

El restablecimiento de la contraseña proporciona una nueva contraseña a la cuenta de usuario, que, normalmente, es temporal. A continuación, podrá proporcionarse esta contraseña temporal al usuario para que pueda iniciar sesión. Se recomienda configurar estas contraseñas para que caduquen al utilizarlas por primera vez si el usuario olvida cambiarlas después de iniciar sesión. Obligar al usuario a crear una nueva contraseña inmediatamente después de iniciar sesión es un método eficaz para asegurar que sólo el usuario conozca su contraseña.

**Para desbloquear una cuenta de usuario bloqueada**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**.

2.  Haga doble clic en **Cuentas de usuario**.

3.  Haga clic en la ficha **Avanzadas** y, a continuación, haga clic en el botón **Avanzadas**.

4.  Haga clic en **Usuarios**.

5.  Encuentre la cuenta de usuario afectada y haga doble clic sobre ella.

6.  Desactive la casilla de verificación **La cuenta está bloqueada** y, a continuación, haga clic en **Aceptar**.

**Para establecer o restablecer una contraseña para una cuenta de usuario existente**

1.  Repita los pasos del 1 al 5 del procedimiento anterior.

2.  Coloque una marca de verificación en la opción **El usuario debe cambiar la contraseña en el siguiente inicio de sesión**. A continuación, haga clic en **Aceptar**.

3.  Haga clic con el botón secundario del mouse en la cuenta pertinente y, después, haga clic en **Establecer contraseña**. A continuación, aparecerá un mensaje de advertencia. Tenga en cuenta las repercusiones posibles antes de continuar.

4.  Si ha hecho clic en el botón **Continuar**, escriba la contraseña temporal en los dos campos de la contraseña.

5.  A continuación, haga clic en **Aceptar** y comunique la contraseña temporal al usuario.

[](#mainsection)[Principio de la página](#mainsection)

### Firewall de Windows

Firewall de Windows es un servidor de seguridad basado en hosts que se incluye como parte integrante de Windows XP Professional SP2 y que tiene múltiples opciones de configuración. Se habilita de forma predeterminada y ayuda a proteger el equipo contra los ataques a la red. Asimismo, Windows Live OneCare también se encarga de la supervisión de Firewall de Windows y proporciona una única consola para la comprobación del estado de seguridad global del equipo.

Firewall de Windows no está diseñado para sustituir la funcionalidad del servidor de seguridad de la red. Firewall de Windows habilita los puertos de red de Windows de manera que los grupos de trabajo de punto a punto puedan comunicarse y compartir recursos. No obstante, se necesita un servidor de seguridad de la red para que proteja la red mientras Firewall de Windows hace lo propio con todas las estaciones de trabajo para las que se ha instalado y habilitado. Varios fabricantes proporcionan servidores de seguridad de la red asequibles diseñados para redes de pequeño a mediano tamaño.

**Para comprobar que Firewall de Windows no esté deshabilitado**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**.

2.  Haga doble clic en el icono **Firewall de Windows**.

3.  Asegúrese de que **Activado (se recomienda)** esté seleccionado.

[](#mainsection)[Principio de la página](#mainsection)

### Actualización de las revisiones de seguridad

Para estar al día con las revisiones de seguridad, se recomienda la suscripción a los boletines de seguridad de Microsoft, que se envían por correo electrónico. Puede registrarse en el sitio Web de [Seguridad de Microsoft](http://www.microsoft.com/spain/seguridad/default.mspx), en http://www.microsoft.com/spain/seguridad/default.mspx. Además de estar siempre informado a través de los boletines, existen otras tecnologías que le servirán para automatizar las revisiones de seguridad.

#### Actualizaciones automáticas

La característica Actualizaciones automáticas de Windows XP puede detectar y descargar automáticamente las últimas revisiones de seguridad de Microsoft. Se puede configurar para que la descarga se realice automáticamente en segundo plano y que, una vez finalizada ésta, se solicite al usuario que instale las revisiones.

**Para configurar el equipo para las actualizaciones automáticas**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**.

2.  Haga doble clic en el icono **Actualizaciones automáticas**.

3.  Configure todas las estaciones de trabajo de Windows XP como **Automáticas**. Tenga en cuenta que podrá configurar la frecuencia de actualización y la hora del día en la que quiera que se realice dicha actualización.

4.  Haga clic en **Aceptar**.

**Nota**   Además, Microsoft emite boletines de seguridad a través de su Servicio de notificación de seguridad. Estos boletines se emiten con respecto a cualquier producto Microsoft del que se detecten problemas de seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Información relacionada

Para obtener más información sobre la seguridad de Windows XP, consulte lo siguiente:

-   La guía [*Windows XP Security Guide*](http://www.microsoft.com/spain/technet/recursos/articulos/secmod60.mspx), disponible para su visualización y descarga en el sitio Web de Microsoft TechNet en www.microsoft.com/spain/technet/recursos/articulos/secmod60.mspx.

Para obtener más información sobre temas relacionados con la seguridad de Windows XP, consulte lo siguiente:

-   La guía de [*Threats and Countermeasures*](http://www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx), disponible para su visualización y descarga en el sitio Web de Microsoft TechNet Web en www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Consiga Seguridad de Windows XP Professional en un entorno de red de punto a punto](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc)

[](#mainsection)[Principio de la página](#mainsection)
