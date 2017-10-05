---
TOCTitle: 'Seguridad de Internet Information Services 6.0'
Title: 'Seguridad de Internet Information Services 6.0'
ms:assetid: 'b53beabd-912c-4f53-80fb-acff5d74df20'
ms:contentKeyID: 20200261
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875829(v=TechNet.10)'
---

Seguridad de Internet Information Services 6.0
==============================================

Actualizado: julio 21, 2006

##### En esta página

[](#ehaa)[Introducción](#ehaa)
[](#egaa)[Antes de comenzar](#egaa)
[](#efaa)[Reducción del ámbito de ataque en el servidor Web](#efaa)
[](#eeaa)[Configuración de cuentas](#eeaa)
[](#edaa)[Configuración de seguridad para archivos y directorios](#edaa)
[](#ecaa)[Seguridad en sitios Web y directorios virtuales](#ecaa)
[](#ebaa)[Configuración de Capa de sockets seguros (Secure Sockets Layer, SSL) en el servidor Web](#ebaa)
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

Los servidores Web son objetivo frecuente de distintos tipos de ataques de seguridad. Algunos de estos ataques son lo suficientemente graves como para causar daños importantes en factores como activos empresariales, productividad o relaciones con el cliente; todos ellos son inoportunos y resultan frustrantes. La seguridad de los servidores Web es fundamental para el éxito de su empresa.

En este documento se explica cómo comenzar el proceso de aumentar la seguridad de un servidor Web en el que se ejecuta Internet Information Services (IIS) 6.0 en el sistema operativo Microsoft® Windows Server™ 2003, Standard Edition. En primer lugar, en esta sección se describen algunas de las amenazas más frecuentes que afectan a la seguridad del servidor Web. Posteriormente, se proporcionan indicaciones de carácter prescriptivo sobre la adopción de medidas de seguridad para el servidor Web frente a esos ataques.

IIS 6.0 adopta una postura más proactiva frente a los usuarios y atacantes maliciosos con las siguientes modificaciones con respecto a versiones anteriores de IIS:

-   IIS 6.0 no se instala de forma predeterminada al instalar Windows Server 2003, Standard Edition.

-   Cuando IIS 6.0 se instala por primera vez, el servidor Web ofrece o muestra únicamente páginas Web estáticas (HTML), lo cual reduce el riesgo que plantea el proporcionar contenido dinámico o ejecutable.

-   El Servicio de publicación World Wide Web (servicio WWW) es el único que se habilita de forma predeterminada cuando IIS 6.0 se instala por primera vez. Se pueden habilitar los servicios específicos que sean necesarios en el momento oportuno.

-   De forma predeterminada, ASP y ASP.NET se deshabilitan cuando IIS 6.0 se instala por primera vez.

Para obtener protección adicional, todos los parámetros de configuración de seguridad predeterminados en IIS 6.0 cumplen o sobrepasan los parámetros de configuración creados por IIS Lockdown Tool. Esta herramienta, diseñada para reducir la superficie de ataque de los servidores Web deshabilitando características innecesarias, se ejecuta en las versiones anteriores de IIS. Para obtener más información sobre IIS Lockdown Tool, consulte "Securing Internet Information Services 5.0 and 5" en el [Security Guidance kit](http://www.microsoft.com/spain/technet/productos/iis/default.mspx), que está disponible en el sitio Web del Centro de descarga de Microsoft, en www.microsoft.com/spain/technet/productos/iis/default.mspx.

Debido a que la configuración predeterminada de IIS 6.0 deshabilita muchas de las características que utilizan frecuentemente los servicios Web, en este documento se explica el modo de configurar características adicionales del servidor Web, al mismo tiempo que se reduce el ámbito en el que el servidor se expone a posibles ataques.

Para aumentar la seguridad en el servidor Web se proporcionan las siguientes indicaciones:

-   Reducir el ámbito de ataque o de exposición del servidor frente a posibles atacantes del servidor Web.

-   Configurar cuentas de grupo y usuario para el acceso anónimo.

-   Proteger los archivos y directorios frente al acceso no autorizado.

-   Proteger los sitios Web y directorios virtuales frente al acceso no autorizado.

-   Configurar la capa de sockets seguros (Secure Sockets Layer, SSL) en el servidor Web.

**Importante**   Todas las instrucciones paso a paso incluidas en este documento se han elaborado utilizando el menú predeterminado que se muestra cuando se hace clic en el botón **Inicio**. Si ha modificado dicho menú, puede que los pasos varíen ligeramente.

Tras completar los procedimientos de este documento, el servidor Web podrá proporcionar contenido dinámico en forma de páginas .asp y aún dispondrá de protección importante frente a los siguientes tipos de ataques que, en ocasiones, suponen una amenaza para los servidores expuestos a Internet:

-   Ataques de perfil que recopilan información sobre el sitio Web. Se pueden reducir bloqueando puertos innecesarios y deshabilitando protocolos que no resultan imprescindibles.

-   Ataques de denegación de servicio que inundan el servidor Web con solicitudes. Se pueden minimizar aplicando revisiones de seguridad y actualizaciones de software.

-   Acceso no autorizado por parte de un usuario sin los permisos adecuados. Se puede eliminar configurando permisos Web y NTFS.

-   Ejecución arbitraria de código malicioso en el servidor Web. Se puede reducir impidiendo el acceso a las herramientas y comandos del sistema.

-   Aumento de privilegios que permiten a usuarios maliciosos utilizar una cuenta de elevado privilegio para ejecutar programas. Se puede reducir con un servicio y cuentas de usuario menos privilegiados.

-   Daños procedentes de virus, gusanos y troyanos. Para hacerles frente, se puede deshabilitar funcionalidad innecesaria, utilizar cuentas menos privilegiadas y aplicar de inmediato las revisiones de seguridad más recientes.

**Nota**   La seguridad de un servidor Web supone un proceso complejo y continuo, por lo que no se puede garantizar una seguridad total.

#### Objetivo de este documento

En este documento se proporciona información de introducción que puede servir de ayuda para adoptar los primeros pasos a la hora de configurar un servidor Web más seguro. No obstante, para que el servidor sea lo más seguro posible, debe comprender el funcionamiento de las aplicaciones que se ejecutan en él. Este documento no incluye información sobre la configuración de seguridad específica de las aplicaciones.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

En esta sección se explican los requisitos previos del sistema, así como las características del servidor Web descritas en este documento.

#### Requisitos del sistema

El servidor Web de ejemplo de este documento presenta los siguientes requisitos del sistema:

-   El servidor ejecuta Windows Server 2003, Standard Edition.

-   El sistema operativo se encuentra instalado en una partición NTFS. Para obtener más información sobre NTFS, consulte "NTFS" en el Centro de ayuda y soporte técnico de Windows Server 2003.

-   Todas las revisiones y actualizaciones necesarias para Windows Server 2003 se han aplicado al servidor. Para comprobar que las actualizaciones de seguridad más recientes se han instalado en el servidor Web, visite la página [Microsoft Update](http://windowsupdate.microsoft.com/) del sitio Web de Microsoft en http://windowsupdate.microsoft.com/ y haga que el servicio Windows Update explore el servidor para buscar las actualizaciones disponibles.

-   Las medidas de seguridad de Windows Server 2003 se han aplicado al servidor. Para obtener más información acerca de la protección de Windows Server 2003, consulte [*Windows Server 2003 Security Guide*](http://www.microsoft.com/spain/technet/seguridad/recursos/guias/guia_ws2003.mspx) en http://www.microsoft.com/spain/technet/seguridad/recursos/guias/guia\_ws2003.mspx.

#### Características del servidor Web

El servidor Web de ejemplo de este documento presenta las siguientes características:

-   Ejecuta IIS 6.0 en modo de aislamiento del proceso de trabajo.

-   Aloja un sitio Web expuesto a Internet.

-   Está tras un servidor de seguridad que permite el tráfico únicamente en los puertos HTTP 80 y HTTPS 443.

-   Es un servidor Web dedicado. Sólo se emplea como tal y no para otros propósitos como, por ejemplo, servidor de archivos, de impresión o de base de datos con Microsoft SQL Server en ejecución.

-   Se permite el acceso anónimo al sitio Web.

-   Muestra páginas HTML y ASP.

-   Las Extensiones de servidor de FrontPage 2002 de Microsoft no están configuradas en el servidor Web.

-   Las aplicaciones del servidor Web no requieren conectividad de base de datos.

-   No admite los protocolos FTP (carga y descarga de archivos), SMTP (correo electrónico) ni NNTP (grupos de noticias).

-   No utiliza Internet Security and Acceleration (ISA) Server.

-   Un administrador debe iniciar sesión localmente para administrar el servidor Web.

[](#mainsection)[Principio de la página](#mainsection)

### Reducción del ámbito de ataque en el servidor Web

Inicie el proceso de protección del servidor Web reduciendo el ámbito de ataque o el grado de exposición de éste a los posibles atacantes. Por ejemplo, habilite únicamente aquellos componentes, servicios y puertos que sean necesarios para el funcionamiento correcto del servidor Web.

#### Deshabilitación de SMB y NetBIOS

Los ataques de enumeración de host exploran la red para determinar la dirección IP de posibles objetivos. Para reducir la probabilidad de éxito de estos ataques contra los puertos expuestos a Internet del servidor Web, deshabilite todos los protocolos de red excepto el Protocolo de control de transporte (TCP). Los servidores Web no requieren Bloques de mensajes de servidor (SMB) ni NetBIOS en sus adaptadores de red expuestos a Internet.

En esta sección se proporcionan instrucciones paso a paso para las siguientes tareas, lo que reducirá la superficie de ataque del servidor Web:

-   Deshabilitar SMB en una conexión expuesta a Internet

-   Deshabilitar NetBIOS a través de TCP/IP

**Nota**   Al deshabilitar SMB y NetBIOS, el servidor no puede funcionar como servidor de archivos ni de impresión; tampoco es posible la exploración de red y el servidor no puede administrarse de forma remota. Si el servidor es un servidor Web dedicado y requiere que los administradores inicien la sesión localmente, estas restricciones no deberían afectar a su funcionamiento.

SMB utiliza los siguientes puertos:

-   Puerto TCP 139

-   Puerto TCP y UDP 445 (Host directo SMB)

NetBIOS hace uso de los siguientes puertos:

-   Puerto TCP y de Protocolo de datagramas de usuario (UDP) 137 (servicio de nombres de NetBIOS)

-   Puerto TCP y UDP 138 (servicio de datagramas de NetBIOS)

-   Puerto TCP y UDP 139 (servicio de sesiones de NetBIOS)

La deshabilitación de NetBIOS como medida única no impedirá la comunicación SMB, ya que SMB utiliza el puerto TCP 445 (denominado Host directo SMB) si no está disponible un puerto de NetBIOS estándar. NetBIOS y SMB se deben deshabilitar independientemente.

##### Requisitos

Necesitará lo siguiente para realizar estas tareas:

-   **Credenciales**. La sesión se debe iniciar como miembro del grupo de administradores en el servidor Web.

-   **Herramientas.** Mi PC, Herramientas del sistema y Administrador de dispositivos.

**Para deshabilitar SMB en una conexión expuesta a Internet**

1.  Haga clic en **Inicio**, en **Panel de control** y, a continuación, haga doble clic en **Conexiones de red**.

2.  Haga clic con el botón secundario del mouse en la conexión expuesta a Internet y, a continuación, seleccione **Propiedades**.

3.  Desactive la casilla de verificación **Cliente para redes Microsoft**.

4.  Desactive la casilla de verificación **Compartir impresoras y archivos para redes de Microsoft** y, a continuación, haga clic en **Aceptar**.

**Para deshabilitar NetBIOS a través de TCP/IP**

1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Administrar**.

2.  Haga doble clic en **Herramientas del sistema**, y seleccione **Administrador de dispositivos**.

3.  Haga clic con el botón secundario del mouse en **Administrador de dispositivos**, haga clic en **Ver** y a continuación en **Mostrar dispositivos ocultos**.

4.  Haga doble clic en **Controladores que no son Plug and Play**.

5.  Haga clic con el botón secundario del mouse en **NetBIOS sobre TCP/IP**, haga clic en **Deshabilitar** (que se muestra en la siguiente captura de pantalla) y a continuación haga clic en **Sí**.

    ![](images/Cc875829.SIIS601(es-es,TechNet.10).gif)

    **Nota**   Las capturas de pantalla que se muestran en este documento reflejan un entorno de prueba, por lo que la información puede ser distinta a la que aparezca en realidad en su pantalla.

Con el procedimiento anterior se desactiva el proceso de escucha de host directo SMB en los puertos TCP 445 y UDP 445. También se deshabilita el controlador Nbt.sys y es necesario reiniciar el equipo.

##### Comprobación de la nueva configuración

Realice los siguientes procedimientos para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.

**Para comprobar que SMB está deshabilitado**

1.  Haga clic en Inicio, Configuración y, a continuación, en Conexiones de red y de acceso telefónico.

2.  Haga clic con el botón secundario del mouse en la conexión de Internet y, a continuación, seleccione **Propiedades**.

3.  Compruebe que las casillas **Cliente para redes Microsoft** y **Compartir impresoras y archivos para redes de Microsoft** están desactivadas; a continuación, haga clic en **Aceptar**.

**Para comprobar que NetBIOS está deshabilitado**

1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Administrar**.

2.  Haga doble clic en **Herramientas del sistema**, y seleccione **Administrador de dispositivos**.

3.  Haga clic con el botón secundario del mouse en **Administrador de dispositivos**, haga clic en **Ver** y a continuación en **Mostrar dispositivos ocultos**.

4.  Haga doble clic en **Controladores que no son Plug and Play** y a continuación haga clic con el botón secundario en **NetBIOS a través de TCP/IP**. La opción **Habilitar** aparece ahora en el menú contextual, lo que significa que la opción NetBios sobre TCP/IP está deshabilitada.

5.  Haga clic en **Aceptar** para cerrar el Administrador de dispositivos.

#### Selección de componentes y servicios de IIS fundamentales

IIS 6.0 incluye subcomponentes y servicios además del servicio WWW como, por ejemplo, los servicios FTP y SMTP. Para reducir el riesgo de ataques cuyo objetivo son servicios y subcomponentes específicos, Microsoft recomienda seleccionar únicamente aquellos que los sitios y aplicaciones Web necesiten para funcionar correctamente.

En la siguiente tabla se muestra la configuración recomendada de Agregar o quitar programas para los subcomponentes y servicios de IIS en el servidor Web de ejemplo en este documento.

**Tabla 1. Configuración recomendada para subcomponentes y servicios IIS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Subcomponente o servicio</th>
<th style="border:1px solid black;" >Configuración predeterminada</th>
<th style="border:1px solid black;" >Configuración del servidor Web</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Extensión de servidor de Servicio de transferencia inteligente en segundo plano (BITS)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Archivos comunes</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio FTP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Extensiones de servidor de FrontPage 2002</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de Internet Information Services</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Impresión de Internet</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio NNTP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio SMTP</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio World Wide Web</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Extensión de servidor de Servicio de transferencia inteligente en segundo plano (BITS)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin cambios</td>
</tr>
</tbody>
</table>
  
##### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Agregar o quitar programas.
  
**Para configurar componentes y servicios de IIS**
  
1.  Haga clic en **Inicio**, **Panel de control** y a continuación en **Agregar o quitar programas**.
  
2.  Haga clic en **Agregar o quitar componentes de Windows**.
  
3.  En la pantalla **Asistente para componentes de Windows** en **Componentes**, haga clic en **Servidor de aplicaciones** y a continuación en **Detalles**.
  
4.  Haga clic en **Internet Information Services (IIS)** y a continuación en **Detalles**.
  
5.  Consulte la tabla anterior y seleccione o anule la selección de los componentes y servicios de IIS adecuados. Para ello, active o desactive la casilla de verificación del componente o servicio correspondiente.
  
6.  Siga las instrucciones que aparecen en pantalla para completar el Asistente para componentes de Windows.
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que los componentes y servicios de IIS se han seleccionado**
  
1.  Haga clic en **Inicio**, en **Panel de control** y a continuación en **Herramientas administrativas**.
  
2.  **Administrador de Internet Information Services (IIS)** aparecerá ahora en el menú de herramientas administrativas.
  
#### Habilitación únicamente de las extensiones de servicios Web esenciales
  
Un servidor Web que ofrece contenido dinámico necesita extensiones de servicio Web. Cada uno de los tipos de contenido dinámico corresponde a una extensión de servicio Web específica. Por razones de seguridad, IIS 6.0 permite habilitar y deshabilitar extensiones de servicio Web independientes, de modo que se habiliten únicamente las necesarias para el contenido.
  
**Precaución**   No active todas las extensiones de servicio Web. Aunque con ello se asegura la mayor compatibilidad posible con los sitios y aplicaciones Web existentes, el ámbito de ataque del servidor Web aumenta considerablemente. Puede que sea necesario probar los sitios y aplicaciones Web por separado, para asegurarse de que sólo se habilitan las extensiones necesarias.
  
Supongamos que el servidor Web se configura para proporcionar el archivo Default.asp como su página predeterminada. Aunque se configure la página predeterminada, debe habilitar la extensión de servicio Web Páginas Active Server para poder visualizar la página .asp.
  
##### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Administrador de Internet Information Services (iis.msc).
  
**Para habilitar la extensión de servicio Web Páginas Active Server**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga doble clic en el equipo local y, a continuación, en **Extensiones de servicio Web**.
  
3.  Haga clic en **Páginas Active Server** y a continuación en **Permitir** (se muestra en la siguiente captura de pantalla).
  
    ![](images/Cc875829.SIIS602(es-es,TechNet.10).gif)
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que la extensión de servicio Web Páginas Active Server está habilitada**
  
1.  Abra un editor de textos, escriba **Página de prueba ASP** y guarde el archivo como **Default.asp** en el directorio C:\\inetpub\\wwwroot.
  
2.  En el cuadro **Dirección** de Internet Explorer, escriba la siguiente URL:
  
    http://localhost
  
    A continuación, presione Entrar. La página de prueba de ASP de texto debería mostrarse en el explorador.
  
3.  Elimine el archivo C:\\inetpub\\wwwroot\\**Default.asp**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de cuentas
  
Microsoft recomienda quitar las cuentas no utilizadas, ya que un atacante podría descubrirlas y emplearlas para obtener acceso a los datos y aplicaciones Web del servidor. Solicite siempre contraseñas seguras, ya que, de lo contrario, aumentará la probabilidad de ataques de fuerza bruta o de diccionarios con los que el atacante intenta averiguar las contraseñas. Deberá utilizar cuentas de usuario que se ejecuten con privilegios mínimos. De no hacerlo así, un atacante puede obtener acceso a recursos no autorizados haciendo uso de una cuenta que se ejecute con un nivel elevado de privilegio.
  
En esta sección, se proporcionan instrucciones paso a paso para las siguientes tareas:
  
-   Deshabilitación de cuentas no utilizadas
  
-   Aislamiento de aplicaciones utilizando grupos de aplicaciones
  
#### Deshabilitación de cuentas no utilizadas
  
Los atacantes pueden hacer uso de cuentas que no se utilizan y sus privilegios, a fin de obtener acceso al servidor. Es necesario auditar de forma periódica las cuentas locales del servidor y deshabilitar las cuentas que no se empleen. Deshabilite las cuentas en un servidor de prueba antes de hacerlo en un servidor de producción; de este modo, se asegurará de que no se afecta negativamente el funcionamiento de la aplicación. Si la deshabilitación de la cuenta no causa ningún problema en el servidor de prueba, realice la misma operación en el servidor de producción.
  
**Nota**   Si decide eliminar una cuenta no utilizada en lugar de deshabilitarla, tenga en cuenta que no se podrá recuperar y que no se pueden eliminar las cuentas Administrador e Invitado. Asimismo, asegúrese de eliminar la cuenta en un servidor de prueba antes de hacerlo en uno de producción.
  
En esta sección se proporcionan instrucciones paso a paso para los siguientes procedimientos:
  
-   Deshabilitación de la cuenta Invitado
  
-   Cambio de nombre de la cuenta Administrador
  
-   Cambio de nombre de la cuenta IUSR\_NombreEquipo
  
##### Deshabilitación de la cuenta Invitado
  
La cuenta Invitado se utiliza cuando se realiza una conexión anónima al servidor Web. Durante la instalación predeterminada de Windows Server 2003, la cuenta Invitado está deshabilitada. Para restringir las conexiones anónimas al servidor, compruebe que la cuenta Invitado sigue deshabilitada.
  
###### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Administración de equipos
  
**Para deshabilitar la cuenta Invitado**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y a continuación haga clic en **Administrar**.
  
2.  Haga doble clic en **Usuarios locales y grupos** y, a continuación, haga clic en la carpeta **Usuarios**. La cuenta Invitado debe aparecer con un icono X de color rojo, con lo que se indica que está deshabilitada (se muestra en la siguiente captura de pantalla).
  
    Si no lo está, continúe con el paso 3 para hacerlo.
  
    ![](images/Cc875829.SIIS603(es-es,TechNet.10).gif)
  
3.  Haga clic con el botón secundario del mouse en cuenta **Invitado** y, a continuación, elija **Propiedades**.
  
4.  En la ficha **General**, active la casilla de verificación **Cuenta deshabilitada** y, a continuación, haga clic en **Aceptar**.
  
La cuenta Invitado debería aparecer con un icono X de color rojo.
  
##### Cambio de nombre de la cuenta Administrador
  
La cuenta Administrador local predeterminada es uno de los objetivos de los usuarios maliciosos debido a sus elevados privilegios en el equipo. Para mejorar la seguridad, se debe cambiar el nombre predeterminado y asignarle una contraseña segura.
  
###### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC.
  
**Para cambiar el nombre de la cuenta Administrador y asignarle una contraseña segura**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y a continuación haga clic en **Administrar**.
  
2.  Haga doble clic en **Usuarios locales y grupos**, y a continuación haga clic en la carpeta **Usuarios**.
  
3.  Haga clic con el botón secundario del mouse en la cuenta **Administrador** y, a continuación, seleccione **Cambiar nombre**.
  
4.  Indique un nombre en el cuadro y presione Entrar.
  
5.  En el escritorio, presione Ctrl+Alt+Supr y haga clic en **Cambiar contraseña**.
  
6.  Escriba el nuevo nombre para la cuenta Administrador en el cuadro **Nombre de usuario**.
  
7.  Escriba la contraseña actual en el cuadro **Contraseña anterior** y una nueva contraseña en el cuadro **Contraseña nueva**. Vuelva a escribir la nueva contraseña en el cuadro **Confirmar contraseña nueva** y a continuación, haga clic en **Aceptar**.
  
**Precaución**   No utilice el elemento de menú Establecer contraseña del menú contextual para cambiar la contraseña a no ser que la haya olvidado y no disponga de un disco para restablecer contraseña. Si utiliza este método para cambiar la contraseña de administrador, puede causar la pérdida irreversible de información que haya protegido mediante esta contraseña.
  
##### Cambio de nombre de la cuenta IUSR
  
La cuenta de usuario anónima predeterminada de Internet, IUSR\_*&lt;NombreEquipo&gt;*,* *se crea durante la instalación de IIS. El valor de *&lt;NombreEquipo&gt;* es el nombre de NetBIOS del servidor cuando se instale IIS. Al cambiar el nombre de esta cuenta, disminuirá la probabilidad de éxito de los ataques de fuerza bruta.
  
###### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC.
  
**Para cambiar el nombre de la cuenta IUSR**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Administrar**.
  
2.  Haga doble clic en **Usuarios locales y grupos** y, a continuación, haga clic en la carpeta **Usuarios**.
  
3.  Haga clic con el botón secundario del mouse en la cuenta **IUSR\_*&lt;NombreEquipo&gt;**** * y, a continuación, seleccione **Cambiar nombre**.
  
4.  Escriba el nuevo nombre y presione Entrar.
  
**Para cambiar el valor de la cuenta IUSR en la metabase de IIS**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en**Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en el equipo local y, a continuación, haga clic en **Propiedades**.
  
3.  Active la casilla de verificación **Habilitar la modificación directa de archivos de metabase** y, a continuación, haga clic en **Aceptar**.
  
4.  Vaya a la ubicación del archivo **MetaBase.xml**. De forma predeterminada, se encuentra en C:\\Windows\\system32\\inetsrv.
  
5.  Haga clic con el botón secundario del mouse en el archivo **MetaBase.xml** y, a continuación, seleccione **Modificar**.
  
6.  Busque la propiedad **AnonymousUserName** y escriba el nuevo nombre de la cuenta IUSR.
  
7.  En el menú **Archivo**, haga clic en **Salir** y, a continuación, en **Sí**.
  
###### Comprobación de la nueva configuración
  
Realice los siguientes procedimientos para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que una cuenta está deshabilitada**
  
1.  Presione Ctrl+Alt+Supr y, a continuación, haga clic en **Cerrar sesión** para cerrar la sesión del servidor Web.
  
2.  En el cuadro de diálogo **Iniciar sesión en Windows** indique el nombre de la cuenta deshabilitada en el cuadro **Nombre de usuario** escriba la contraseña de la misma y, a continuación, haga clic en **Aceptar**.
  
    Se mostrará el siguiente mensaje:
  
    **Su cuenta está desactivada. Póngase en contacto con el administrador de su sistema.**
  
**Para comprobar el cambio de nombre de una cuenta**
  
1.  Presione Ctrl+Alt+Supr y, a continuación, haga clic en **Cerrar sesión** para cerrar la sesión del servidor Web.
  
2.  En el cuadro de diálogo **Iniciar sesión en Windows**, indique el nombre anterior de la cuenta cuyo nombre se ha cambiado en el cuadro **Nombre de usuario**, escriba la contraseña de dicha cuenta y, a continuación, haga clic en **Aceptar**.
  
    Se mostrará el siguiente mensaje:
  
    **No se puede iniciar sesión para usted. Asegúrese de que su nombre de usuario y dominio sean correctos** **y vuelva a escribir su contraseña. Las letras de la contraseña se deben escribir usando mayúsculas y minúsculas correctamente.**
  
3.  Haga clic en **Aceptar** y, a continuación, escriba el nuevo nombre de la cuenta en el cuadro **Nombre de usuario**.
  
4.  Escriba la contraseña de la cuenta con nuevo nombre y, a continuación, haga clic en **Aceptar**.
  
Se debe poder iniciar la sesión en el equipo con la cuenta de nuevo nombre.
  
#### Aislamiento de aplicaciones con grupos de ellas
  
Con IIS 6.0, las aplicaciones se pueden aislar en grupos. Un grupo de aplicaciones es un grupo de una o varias direcciones URL que ofrece un proceso de trabajo o un conjunto de ellos. Estos grupos pueden ayudar a mejorar la confiabilidad del servidor Web, ya que cada aplicación funciona de forma independiente con respecto a las demás.
  
Todos los procesos en ejecución en un sistema operativo Windows disponen de una identidad, que determina el modo en que el proceso tiene acceso a los recursos del equipo. Cada grupo de aplicaciones cuenta además con una identidad de proceso, que es una cuenta ejecutada con los permisos mínimos que requiere la aplicación. Esta identidad de proceso se puede utilizar para permitir el acceso anónimo al sitio o a las aplicaciones Web.
  
##### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC.
  
**Para crear un grupo de aplicaciones**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga doble clic en el equipo local, haga clic con el botón secundario del mouse en **Grupo de aplicaciones**, haga clic en **Nuevo** y, a continuación, en **Grupo de aplicaciones**.
  
3.  En el cuadro **Id. de grupo de aplicaciones**, escriba un nuevo Id. para el grupo de aplicaciones (la siguiente captura de pantalla utiliza ContosoAppPool para el Id.).
  
    ![](images/Cc875829.SIIS604(es-es,TechNet.10).gif)
  
4.  En **Configuración del grupo de aplicaciones**, seleccione **Usar la configuración predeterminada para nuevos grupos de aplicaciones** y, a continuación, haga clic en **Aceptar**.
  
**Para asignar una aplicación o sitio Web a un grupo de aplicaciones**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en la aplicación o sitio Web que desee asignar a un grupo de aplicaciones y, a continuación, haga clic en **Propiedades**.
  
3.  Haga clic en la ficha **Directorio principal**, **Directorio virtual** o **Directorio**, dependiendo del tipo de aplicación que se haya seleccionado.
  
4.  Si desea asignar un directorio o un directorio virtual a un grupo de aplicaciones, compruebe que el cuadro **Nombre de la aplicación** incluye el nombre de la aplicación o de su sitio Web correcto.
  
    - O bien -
  
    Si no hay ningún nombre en el cuadro **Nombre de la aplicación**, haga clic en **Crear** y, a continuación, escriba el nombre de la aplicación o del sitio Web.
  
5.  En el cuadro de lista **Grupo de aplicaciones**, haga clic en el nombre del grupo de aplicaciones al que desea asignar la aplicación o sitio Web (se muestra en la siguiente captura de pantalla) y, a continuación, haga clic en **Aceptar**.
  
    ![](images/Cc875829.SIIS605(es-es,TechNet.10).gif)
  
##### Comprobación de la nueva configuración
  
Realice los siguientes procedimientos para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que se ha creado un grupo de aplicaciones**
  
1.  Inicie sesión en el servidor Web con la cuenta Administrador.
  
2.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
3.  Haga doble clic en el equipo local y en **Grupos de aplicaciones** y, a continuación, compruebe que el grupo creado aparece bajo el nodo **Grupos de aplicaciones**.
  
4.  Haga clic con el botón secundario del mouse en el grupo creado y, a continuación, seleccione **Propiedades**.
  
5.  Haga clic en la ficha **Identidad**, compruebe que la identidad del grupo de aplicaciones se establece en una cuenta de seguridad predefinida denominada Servicio de red y, a continuación, haga clic en **Aceptar**.
  
**Para comprobar que una aplicación o sitio Web se ha asignado a un grupo de aplicaciones específico**
  
1.  Inicie sesión en el servidor Web con la cuenta Administrador.
  
2.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
3.  Haga doble clic en el equipo local y en **Sitios Web**,haga clic con el botón secundario del mouse en el sitio para el que desea comprobar la configuración del grupo de aplicaciones y, a continuación, haga clic en **Propiedades**.
  
4.  Haga clic en la ficha **Directorio principal**, **Directorio virtual** o **Directorio**, dependiendo del tipo de aplicación que se haya seleccionado.
  
5.  En el cuadro de lista **Grupo de aplicaciones**, compruebe que se incluye el nombre del grupo de aplicaciones al que desea asignar el sitio Web y, a continuación, haga clic en **Cancelar**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad para archivos y directorios
  
Para proteger archivos y directorios importantes se deben emplear controles de acceso seguros. En la mayoría de las situaciones, permitir el acceso a determinadas cuentas resulta más eficaz que denegarlo. El acceso se debe configurar en el nivel de directorio, siempre que sea posible. A medida que los archivos se agregan a la carpeta, heredan permisos de la misma, por lo que no es necesario realizar ninguna acción adicional.
  
En esta sección se proporcionan instrucciones paso a paso para las siguientes tareas, para facilitar la configuración de seguridad de archivos y directorios:
  
-   Reubicar y establecer permisos para archivos de registro de IIS
  
-   Configurar permisos de metabase de IIS
  
-   Deshabilitar el componente FileSystemObject
  
#### Reubicación y definición de permisos para archivos de registro de IIS
  
Con el fin de aumentar la seguridad de los archivos de registro de IIS, es necesario reubicarlos en una unidad que no sea de sistema y con formato para utilizar el sistema de archivos NTFS. Esta ubicación no debe ser la misma que la del contenido del sitio Web. La reubicación de estos archivos evitará que ciertos tipos de ataques muestren el contenido de los archivos de registro. Los archivos de registro deberían protegerse también para proporcionar una pista de auditoría de posibles ataques contra el servidor. La colocación de los archivos de registro en un disco que no sea del sistema también mejorará el rendimiento del servidor.
  
##### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC y el Administrador de Internet Information Services (IIS) (Iis.msc).
  
**Para desplazar la ubicación de los archivos de registro de IIS a una partición que no sea de sistema**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en**Mi PC** y, a continuación, haga clic en **Explorar**.
  
2.  Vaya a la ubicación donde desee reubicar los archivos de registro de IIS.
  
3.  Haga clic con el botón secundario del mouse en el directorio de un nivel superior donde desee reubicar los archivos; haga clic en **Nuevo** y, a continuación, en **Carpeta**.
  
4.  Indique un nombre para la carpeta como, por ejemplo, ContosoIISLogs y presione Entrar.
  
5.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
6.  Haga clic con el botón secundario del mouse en el sitio Web y, a continuación, haga clic en **Propiedades**.
  
7.  Haga clic en la ficha **Sitio Web** y, a continuación, en **Propiedades** del marco **Habilitar registro**.
  
8.  En la ficha **Propiedades generales**, seleccione **Examinar** y vaya a la carpeta que se acaba de crear para almacenar los archivos de registro de IIS.
  
9.  Haga clic en **Aceptar** tres veces.
  
**Nota**   Si ya dispone de archivos de registro de IIS en la ubicación original en Windows\\System32\\Logfiles, debe moverlos a la nueva ubicación de forma manual. IIS no realizará la operación por sí mismo.
  
**Para establecer listas de control de acceso (ACL) en archivos de registro de IIS**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Explorar**.
  
2.  Vaya a la carpeta donde se encuentran los archivos de registro.
  
3.  Haga clic con el botón secundario del mouse en la carpeta, seleccione **Propiedades** y, a continuación, haga clic en la ficha **Seguridad**.
  
4.  En el panel superior, haga clic en **Administradores** y compruebe que los permisos del panel inferior se definen como **Control total**.
  
5.  En el panel superior, haga clic en **Sistema**, compruebe que los permisos del panel inferior se definen como **Control total** y, a continuación, haga clic en **Aceptar**.
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que los archivos de registro se desplazan y los permisos se definen**
  
1.  Haga clic en **Inicio**, **Buscar** y seleccione**Archivos o carpetas**.
  
2.  Escriba un nombre de archivo parcial o completo en el cuadro **Buscar archivos con el nombre**, por ejemplo, LogFiles. Seleccione una ubicación en el cuadro **Buscar en** y, a continuación, haga clic en **Buscar ahora**.
  
    La búsqueda devuelve la nueva ubicación de los archivos de registro.
  
3.  Presione Ctrl+Alt+Supr y, a continuación, haga clic en **Cerrar sesión**.
  
4.  Inicie sesión en el servidor Web utilizando una cuenta que no tenga permiso de acceso a los archivos de registro.
  
5.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC**, haga clic en **Explorar** y, a continuación, vaya al directorio LogFiles.
  
6.  Haga clic con el botón secundario del mouse en el directorio LogFiles y, a continuación, haga clic en, **Abrir**. Se mostrará el siguiente mensaje:
  
    **Acceso denegado**.
  
#### Configuración de permisos de metabase de IIS
  
La metabase de IIS es un archivo XML que incluye la mayor parte de la información de configuración de IIS.
  
##### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC y el archivo MetaBase.xml.
  
**Para restringir el acceso al archivo MetaBase.xml**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Explorar**.
  
2.  Vaya al archivo **Windows\\System32\\Inetsrv\\MetaBase.xml**, haga clic con el botón secundario del mouse en él y, a continuación, haga clic en **Propiedades**.
  
3.  Haga clic en la ficha **Seguridad**, confirme que sólo los miembros del grupo de administradores y la cuenta LocalSystem tienen acceso de control total a la metabase, elimine todos los demás permisos de archivo y haga clic en **Aceptar**.
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar el acceso restringido al archivo MetaBase.xml**
  
1.  Presione Ctrl+Alt+Supr y, a continuación, haga clic en **Cerrar sesión**.
  
2.  Inicie la sesión en el servidor Web utilizando una cuenta que no tenga permiso de acceso al archivo **MetaBase.xml**.
  
3.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC**, haga clic en **Explorar** y, a continuación, vaya a la ubicación del archivo **MetaBase.xml**.
  
4.  Haga clic con el botón secundario del mouse en el archivo **MetaBase.xml** y, a continuación, seleccione **Abrir**. Se mostrará el siguiente mensaje:
  
    **Acceso denegado**.
  
#### Deshabilitación del componente FileSystemObject
  
ASP, Windows Script Host y otras aplicaciones de secuencias de comandos utilizan el componente FileSystemObject (FSO) para crear, eliminar, obtener información y manipular unidades, carpetas y archivos. Considere la posibilidad de deshabilitar el componente FSO, aunque tenga en cuenta que con ello también se eliminará el objeto Dictionary. Asimismo, compruebe que ningún otro programa necesita este componente.
  
##### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Símbolo del sistema.
  
**Para deshabilitar el componente FileSystemObject**
  
1.  Haga clic en **Inicio**, **Ejecutar**, escriba**cmd** en el cuadro **Abrir** y, a continuación, haga clic en **Aceptar**.
  
2.  Escriba **cd c:\\Windows\\system32** y presione Entrar para cambiar al directorio C:\\Windows\\system32.
  
3.  En el símbolo del sistema, escriba **regsvr32 scrrun.dll /u** y, a continuación, presione Entrar. Se mostrará el siguiente mensaje:
  
    **DllUnregisterServer en scrrun.dll se realizó con éxito.**
  
4.  Haga clic en **Aceptar**.
  
5.  En el símbolo del sistema, escriba **exit** y presione Entrar para cerrar la ventana.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Seguridad en sitios Web y directorios virtuales
  
Los directorios raíz Web y los directorios virtuales se deben reubicar en una partición que no sea del sistema para ayudar a protegerse de los ataques transversales de directorio. Estos ataques permiten a los atacantes ejecutar herramientas y programas del sistema operativo. Debido a que no es posible atravesar unidades, la reubicación del contenido del sitio Web en otra unidad ofrece protección adicional frente a este tipo de ataques.
  
En esta sección se proporcionan instrucciones paso a paso para las siguientes tareas, para la proteger sitios Web y directorios virtuales:
  
-   Desplazamiento del contenido del sitio Web a una unidad que no es del sistema
  
-   Configuración de permisos del sitio Web
  
#### Desplazamiento del contenido del sitio Web a una unidad que no es del sistema
  
No utilice el directorio predeterminado \\Inetpub\\Wwwroot como ubicación para el contenido del sitio Web. Por ejemplo, si el sistema se instala en la unidad C:, considere la posibilidad de mover el directorio del contenido y sitio a la unidad D: para eliminar los riesgos asociados con los ataques transversales de directorio, en los que un atacante intenta examinar la estructura de directorio de un servidor Web. Asegúrese de comprobar que todos los directorios virtuales apuntan a la nueva unidad.
  
##### Requisitos
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Administrador de Internet Information Services (iis.msc) y un símbolo del sistema.
  
**Para desplazar el contenido del sitio Web a una unidad que no es del sistema**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en el sitio Web que incluye el contenido que desea mover y, a continuación, seleccione **Detener**.
  
3.  Haga clic en **Inicio**, **Ejecutar**, escriba**cmd** en el cuadro **Abrir** y, a continuación, haga clic en **Aceptar**.
  
4.  Escriba lo siguiente en el símbolo del sistema:
  
    **xcopy c:\\inetpub\\wwwroot\\*&lt;SiteName&gt; &lt;Drive&gt;*:\\wwwroot\\SiteName /s /i /o**
  
    donde
  
    -   *&lt;SiteName&gt;* es el nombre de su sitio Web.
  
    -   *&lt;Drive&gt;* es la letra de la nueva unidad (por ejemplo, D).
  
5.  Vuelva al complemento Administrador de Internet Information Services (IIS), haga clic con el botón secundario del mouse en el sitio Web y, a continuación, seleccione **Propiedades**.
  
6.  Haga clic en las fichas **Directorio principal**, **Directorio virtual** o **Directorio**, dependiendo del tipo de aplicación que haya seleccionado. Indique la nueva ubicación del directorio en el cuadro **Ruta local** y, a continuación, haga clic en **Aceptar**.
  
    - O bien -
  
    Vaya a la nueva ubicación del directorio en el que acaba de copiar los archivos y seleccione **Aceptar**.
  
7.  Haga clic con el botón secundario del mouse en el sitio Web y, a continuación, seleccione **Inicio**.
  
##### Comprobación de la nueva configuración
  
Realice los siguientes procedimientos para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que el contenido del sitio Web se ha movido a una unidad que no es del sistema**
  
1.  Haga clic en **Inicio**, en **Buscar** y luego en **Archivos o carpetas**.
  
2.  Indique un nombre de archivo parcial o completo en el cuadro **Buscar archivos con el nombre**, seleccione una ubicación en el cuadro **Buscar en** y, a continuación, haga clic en **Buscar ahora**.
  
    La búsqueda devuelve la lista de archivos desplazados a su nueva ubicación, así como la ubicación original.
  
**Para eliminar el contenido del sitio Web de la unidad del sistema**
  
-   Vaya hasta el directorio C:\\Inetpub\\Wwwroot\\SiteName y, a continuación, elimine los archivos desplazados a una unidad que no sea del sistema.
  
**Para comprobar que el contenido del sitio Web se ha eliminado de la unidad del sistema**
  
1.  Haga clic en **Inicio**, en **Buscar** y luego en **Archivos o carpetas**.
  
2.  Indique un nombre de archivo parcial o completo en el cuadro **Buscar archivos con el nombre**, seleccione una ubicación en el cuadro **Buscar en** y, a continuación, haga clic en **Buscar ahora**.
  
    La búsqueda sólo devuelve la lista de archivos desplazados a su nueva ubicación.
  
#### Configuración de permisos del sitio Web
  
Los permisos de acceso se pueden configurar para el servidor Web para directorios, archivos y sitios específicos. Estos permisos se aplican a todos los usuarios independientemente de sus derechos de acceso concretos.
  
##### Configuración de permisos en directorios del sistema de archivos
  
IIS 6.0 depende de los permisos NTFS para ayudar a proteger los archivos y directorios independientes de accesos no autorizados. A diferencia de los permisos del sitio Web, aplicados a los usuarios que intentan tener acceso al sitio, se pueden utilizar los permisos NTFS para definir qué usuarios pueden tener acceso al contenido y el modo en que se permite su manipulación. Para mejorar la seguridad, utilice los permisos de sitio Web y NTFS.
  
Las listas de control de acceso (ACL) indican qué usuarios o grupos tienen permisos para tener acceso o modificar un archivo concreto. En lugar de establecer listas ACL en cada archivo, cree nuevos directorios para cada tipo de archivo, establezca listas ACL en cada directorio y, posteriormente, permita que los archivos hereden permisos del directorio en el que residen.
  
###### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Mi PC y el Administrador de Internet Information Services (IIS) (Iis.msc).
  
**Para desplazar el contenido del sitio Web a una carpeta independiente**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Explorar**.
  
2.  Examine la carpeta que incluya el contenido y, a continuación, haga clic en la carpeta de nivel superior del contenido del sitio Web.
  
3.  En el menú **Archivo**, haga clic en **Nuevo** y, a continuación, en **Carpeta** para crear una nueva carpeta en el directorio de contenido del sitio Web.
  
4.  Indique el nombre de la carpeta y presione Entrar.
  
5.  Presione Ctrl y, a continuación, seleccione cada una de las páginas que desee proteger.
  
6.  Haga clic con el botón secundario del mouse en las páginas y, a continuación, seleccione **Copiar**.
  
7.  Haga clic con el botón secundario en la nueva carpeta y, a continuación, seleccione **Pegar**.
  
**Nota**   Si se han creado vínculos a estas páginas, éstos deben actualizarse para reflejar la nueva ubicación del contenido del sitio.
  
**Para establecer permisos para el contenido Web**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario en la carpeta Sitios Web, el sitio Web, directorio, directorio virtual o archivo que desee configurar y haga clic en **Propiedades**.
  
3.  Active o desactive cualquiera de las siguientes casillas de verificación (si están disponibles), dependiendo del tipo de acceso que desee conceder o denegar:
  
    -   **Acceso al código fuente de secuencias de comandos**. Los usuarios pueden tener acceso a los archivos de código fuente. Si se selecciona la opción **Leer**, se podrá leer el código fuente; si se selecciona **Escribir**, se podrá escribir en el código fuente. Este tipo de acceso incluye el código fuente para las secuencias de comandos. Esta opción no se encuentra disponible si ni **Leer** ni **Escribir** están activadas.
  
    -   **Leer (activada de forma predeterminada)**. Los usuarios pueden ver las propiedades y el contenido del archivo o directorio.
  
    -   **Escribir**. Los usuarios pueden cambiar el contenido y las propiedades de un archivo o directorio.
  
    -   **Examen de directorios**. Los usuarios puede ver listas y colecciones de archivos.
  
    -   **Registrar visitas**. Por cada visita al sitio Web se crea una entrada de registro.
  
    -   **Indizar este recurso**. Permite que Servicios de Index Server realice la indización de este recurso. Esto permite a los usuarios realizar búsquedas en el recurso.
  
4.  En el cuadro de lista **Permisos de ejecución**, seleccione el nivel adecuado de ejecución de secuencia de comandos:
  
    -   **Ninguna**. No se ejecutan secuencias de comandos ni archivos ejecutables (por ejemplo, archivos del tipo .exe) en el servidor.
  
    -   **Sólo secuencias de comandos**. Se ejecutan únicamente secuencias de comandos en el servidor.
  
    -   **Sec. comandos y ejecutables**. En el servidor se ejecutan tanto secuencias de comandos como archivos ejecutables.
  
5.  Haga clic en **Aceptar**. Si los nodos secundarios de un directorio disponen de permisos distintos de sitio Web configurados, aparecerá el cuadro **Omitir herencia**.
  
6.  Si aparece el cuadro **Omitir herencia**, seleccione los nodos secundarios de la lista **Nodos secundarios** a los que desea aplicar los permisos Web del directorio.
  
    - O bien -
  
    Haga clic en **Seleccionar todo** para establecer la propiedad que se aplicará a los permisos Web en todos los nodos secundarios.
  
7.  Si aparece más de un cuadro de la opción **Omitir herencia**, seleccione los nodos secundarios en la lista **Nodos secundarios** o haga clic en **Seleccionar todo** y, a continuación, en **Aceptar** para aplicar los permisos Web para esta propiedad a los nodos secundarios.
  
Si un nodo secundario que pertenece al directorio que dispone de permisos del sitio Web modificados también ha establecido los permisos para una opción en concreto, los permisos del nodo secundario anularán a los definidos para el directorio. Si desea que los permisos del sitio Web del nivel de directorio se apliquen a los nodos secundarios, debe seleccionar los nodos en el cuadro **Omitir herencia**.
  
###### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar que el acceso de escritura se deniega en los directorios de contenido del sitio Web**
  
1.  Presione Ctrl+Alt+Supr y, a continuación, haga clic en **Cerrar sesión**.
  
2.  Inicie la sesión en el servidor Web utilizando una cuenta con permisos de lectura y ejecución en el directorio físico o virtual.
  
3.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC**, seleccione **Explorar** y vaya a la ubicación del un archivo que desee copiar en el directorio físico o virtual.
  
4.  Haga clic con el botón secundario del mouse en el archivo y, a continuación, seleccione **Copiar**.
  
5.  Diríjase al directorio físico o virtual y, a continuación, haga clic con el botón secundario del mouse en él. La selección de **Pegar** no está disponible en el menú contextual, lo que significa que no se dispone de acceso de escritura en el directorio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Capa de sockets seguros (Secure Sockets Layer, SSL) en el servidor Web
  
Configure características de seguridad de Capa de sockets seguros (SSL) en el servidor Web para comprobar la integridad del contenido, la identidad de los usuarios y cifrar las transmisiones de red. Generalmente, SSL es un requisito si tiene previsto aceptar transacciones de tarjetas de crédito en un sitio Web. La seguridad de SSL depende de un certificado de servidor que permite a los usuarios autenticar el sitio Web antes de que se transmita información personal como, por ejemplo, un número de tarjeta de crédito. Cada sitio Web puede disponer solamente de un certificado de servidor.
  
#### Obtención e instalación de certificados de servidor
  
Los certificados los envían organizaciones que no pertenecen a Microsoft y que se denominan entidades emisoras de certificados (CA). El certificado del servidor suele asociarse con el servidor Web, concretamente con el sitio donde se ha configurado SSL. Se debe generar una solicitud de certificado, enviarla a CA y, posteriormente, instalar el certificado una vez recibido.
  
Para reforzar la seguridad, los certificados dependen de un par de claves de cifrado, una pública y otra privada. De hecho, al emitir la solicitud para un certificado de servidor, se está generando la clave privada. El certificado de servidor que se recibe de CA incluye la clave pública.
  
##### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Administrador de Internet Information Services (IIS) (Iis.msc) y el Asistente para certificados de servidor Web.
  
**Para generar una solicitud para un certificado de servidor**
  
1.  Haga clic en **Inicio**, haga clic con el botón secundario del mouse en **Mi PC** y, a continuación, haga clic en **Administrar**.
  
2.  Haga doble clic en la sección **Servicios y aplicaciones** y, a continuación, en **Internet Information Services**.
  
3.  Haga clic con el botón secundario del mouse en el sitio Web en el que desea instalar el certificado de servidor y, a continuación, haga clic en **Propiedades**.
  
4.  Haga clic en la ficha **Seguridad de directorios**. En la sección **Comunicaciones seguras**, haga clic en **Certificado de servidor** para iniciar el Asistente para certificados de servidor Web y, a continuación, haga clic en **Siguiente**.
  
5.  Haga clic en **Crear un certificado nuevo** y, a continuación, seleccione**Siguiente**.
  
6.  Haga clic en **Preparar la petición ahora** **pero enviarla más tarde** y, a continuación, en **Siguiente**.
  
7.  En el cuadro **Nombre**, escriba un nombre que sea fácil de recordar. (El nombre predeterminado es el del sitio Web para el que se va a generar la solicitud de certificado como, por ejemplo, http://www.contoso.com.)
  
8.  Especifique una longitud en bits y haga clic en **Siguiente**.
  
    La longitud en bits de la clave de cifrado determina la seguridad de éste. La mayor parte de las CA que no pertenecen a Microsoft prefieren que se seleccione un mínimo de 1.024 bits.
  
9.  En la sección **Organización**, indique la información de organización y unidad organizativa. Compruebe que la información es correcta y que los campos de Organización no incluyen comas y, a continuación, haga clic en **Siguiente**.
  
10. En la sección **Nombre común de su sitio Web**, escriba el nombre del equipo host con el nombre de dominio y, a continuación, haga clic en **Siguiente**.
  
11. Indique la información geográfica y, a continuación, haga clic en **Siguiente**.
  
12. Guarde el archivo como .txt. (La ubicación y el nombre de archivo predeterminado son **C:\\certreq.txt**.) En el siguiente ejemplo se muestra el aspecto de un archivo de solicitud de certificado.
  
    ```  
 -----BEGIN NEW CERTIFICATE REQUEST----- MIIDATCCAmoCAQAwbDEOMAwGA1UEAxMFcGxhbjgxDDAKBgNVBAsTA1BTUzESMB A1UEChMJTWljcm9zb2Z0MRIwEAYDVQQHEwlDaGFybG90dGUxFzAVBgNVBAgTDk cnRoIENhcm9saW5hMQswCQYDVQQGEwJVUzCBnzANBgkqhkiG9w0BAQEFAAOBjQ gYkCgYEAtW1koGfdt+EoJbKdxUZ+5vE7TF1ZuT+xaK9jEWHESfw11zoRKrHzHN IASnwg3vZ0ACteQy5SiWmFaJeJ4k7YaKUb6chZXG3GqL4YiSKFaLpJX+YRiKMt JzFzict5GVVGHsa1lY0BDYDO2XOAlstGlHCtENHOKpzdYdANRg0CAwEAAaCCAV GgYKKwYBBAGCNw0CAzEMFgo1LjAuMjE5NS4yMDUGCisGAQQBgjcCAQ4xJzAlMA A1UdDwEB/wQEAwIE8DATBgNVHSUEDDAKBggrBgEFBQcDATCB/QYKKwYBBAGCNw AjGB7jCB6wIBAR5aAE0AaQBjAHIAbwBzAG8AZgB0ACAAUgBTAEEAIABTAEMAaA AG4AbgBlAGwAIABDAHIAeQBwAHQAbwBnAHIAYQBwAGgAaQBjACAAUAByAG8Adg AGQAZQByA4GJAGKa0jzBn8fkxScrWsdnU2eUJOMUK5Ms87Q+fjP1/pWN3PJnH7 MBc5isFCjww6YnIjD8c3OfYfjkmWc048ZuGoH7ZoD6YNfv/SfAvQmr90eGmKOF TD+hl1hM08gu2oxFU7mCvfTQ/2IbXP7KYFGEqaJ6wn0Z5yLOByPqblQZAAAAAA MhfC7CIvR0McCQ+CBwuLzD+UJxl+kjgb+qwcOUkGX2PCZ7tOWzcXWNmn/4YHQl GEXu0w67sVc2R9DlsHDNzeXLIOmjUl935qy1uoIR4V5C48YNsF4ejlgjeCFsbC Jb9/2RM= -----END NEW CERTIFICATE REQUEST-----   
```
  
13. Confirme los detalles de la solicitud, haga clic en **Siguiente** y, a continuación, en **Finalizar**.
  
**Para enviar una solicitud para un certificado de servidor**
  
1.  Póngase en contacto con la entidad emisora para consultar los requisitos necesarios para enviar una solicitud.
  
2.  Copie el contenido del archivo .txt creado en el anterior procedimiento en el formato que requiera su CA.
  
3.  Envíe la solicitud a la CA correspondiente.
  
Cuando reciba el certificado de su CA, podrá instalarlo en el servidor Web.
  
**Para instalar un certificado de servidor**
  
1.  Copie el archivo de certificado (.cer) en la carpeta C:\\Windows\\System32\\CertLog.
  
2.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
3.  Haga clic con el botón secundario del mouse en el sitio Web en el que desea instalar el certificado de servidor y, a continuación, haga clic en **Propiedades**.
  
4.  Haga clic en la ficha **Seguridad de directorios**. En la sección **Comunicaciones seguras**, haga clic en **Certificado de servidor** para iniciar el Asistente para certificados de servidor Web y, a continuación, haga clic en **Siguiente**.
  
5.  Haga clic en **Procesar la petición pendiente e instalar el certificado** y, a continuación, en **Siguiente**.
  
6.  Desplácese al certificado recibido de la CA. Haga clic dos veces en **Siguiente** y, a continuación, haga clic en **Finalizar**.
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al equipo local.
  
**Para comprobar que un certificado se ha instalado en un servidor Web**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga clic en**Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en el sitio Web que incluye el certificado que desea ver y, a continuación, seleccione **Propiedades**.
  
3.  En la ficha **Seguridad de directorios** del área **Comunicaciones seguras**, haga clic en **Ver certificado**, revise el certificado y, a continuación, haga clic dos veces en **Aceptar**.
  
#### Aplicación y habilitación de conexiones SSL en el servidor Web
  
Tras instalar el certificado de servidor, deberá aplicar conexiones SSL en el servidor Web. A continuación, se deben habilitar las conexiones SSL.
  
**Nota**   Después de requerir conexiones SSL al servidor Web, cualquier vínculo al servidor necesitará actualizarse para utilizar https en lugar de http.
  
##### Requisitos
  
Necesitará lo siguiente para realizar estas tareas:
  
-   **Credenciales**. Debe haber iniciado sesión como miembro del grupo de administradores en el servidor Web.
  
-   **Herramientas**. Administrador de Internet Information Services (iis.msc).
  
**Para aplicar las conexiones SSL**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en el sitio Web en el que desee aplicar las conexiones SSL, y a continuación, seleccione **Propiedades**.
  
3.  Haga clic en la ficha **Seguridad de directorios**. En la sección **Comunicaciones seguras**, haga clic en **Modificar**.
  
4.  Haga clic en **Requerir canal seguro (SSL)**, seleccione la seguridad del cifrado y, a continuación, haga clic en **Aceptar**.
  
    **Nota**   Si se especifica un cifrado de 128 bits, los equipos cliente que utilicen exploraciones de 40 o 56 bits no se podrán comunicar con el sitio, a no ser que los exploradores se actualicen a versiones que admitan cifrado de 128 bits.
  
**Para habilitar conexiones SSL en el servidor Web**
  
1.  Haga clic en **Inicio**, **Panel de control**, **Herramientas administrativas** y, a continuación, haga doble clic en **Administrador de Internet Information Services (IIS)**.
  
2.  Haga clic con el botón secundario del mouse en el sitio Web en el que desee activar las conexiones SSL y, a continuación, seleccione **Propiedades**.
  
3.  Haga clic en la ficha **Sitio Web**. En la sección **Identificación del sitio Web**, compruebe que el cuadro **Puerto SSL** se rellena con el valor numérico **443**.
  
4.  Haga clic en **Opciones avanzadas**. Generalmente, aparecen dos cuadros, y la dirección IP y el puerto del sitio Web ya aparecen en el cuadro **Varias identidades para este sitio Web**. En el campo **Varias identidades SSL para este sitio Web**, haga clic en **Agregar** si no aparece el puerto 443. Seleccione la dirección IP del servidor, escriba el valor numérico **443** en el cuadro **Puerto SSL** y, a continuación, haga clic en **Aceptar**.
  
##### Comprobación de la nueva configuración
  
Realice el siguiente procedimiento para asegurarse de que se ha aplicado la configuración de seguridad adecuada al servidor Web.
  
**Para comprobar conexiones SSL en el servidor Web**
  
1.  Abra el explorador e intente conectarse al servidor Web utilizando el protocolo estándar http://. Por ejemplo, en el cuadro **Dirección**, escriba **http://localhost** y presione Entrar.
  
    Si se aplica SSL, aparecerá el siguiente mensaje de error:
  
    **La página debe visualizarse en un canal seguro. La página a la que intenta tener acceso está asegurada con nivel de sockets seguro (SSL).**
  
2.  Intente de nuevo conectarse a la página que desee ver escribiendo **https://localhost** y presionando Entrar.
  
    Generalmente, aparece la página predeterminada del servidor Web.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información relacionada
  
Para obtener más información sobre la seguridad de IIS 6.0, consulte los siguientes documentos:
  
-   "[Security Enhancements in Internet Information Services 6.0](http://www.microsoft.com/spain/technet/recursos/articulos/2706032.aspx)" en el sitio Web de Microsoft Windows Server 2003, en www.microsoft.com/spain/technet/recursos/articulos/2706032.aspx.
  
-   "[Configuring Application Isolation on Windows Server 2003 and Internet Information Services (IIS) 6.0](http://www.microsoft.com/spain/technet/productos/iis/default.mspx)" en el sitio Web de Microsoft Technet www.microsoft.com/spain/technet/productos/iis/  
    default.mspx.
  
-   El TechNet Webcast "Effectively Using IIS 6.0 Security" en la página Web de Microsoft [Internet Information Services Webcasts](http://www.microsoft.com/spain/technet/jornadas/default.mspx), en www.microsoft.com/spain/technet/jornadas/default.asp.
  
Para obtener más información sobre IIS 6.0, consulte los siguientes documentos:
  
-   El [Internet Information Services (IIS) 6.0 Resource Kit](http://www.microsoft.com/downloads/details.aspx?familyid=80a1b6e6-829e-49b7-8c02-333d9c148e69&displaylang=en), disponible en el Centro de descarga de Microsoft, en www.microsoft.com/downloads/details.aspx?familyid=80a1b6e6-829e-49b7-8c02-333d9c148e69&displaylang=en.
  
-   "[Technical Overview of Internet Information Services (IIS) 6.0](http://www.microsoft.com/spain/technet/productos/iis/default.mspx)", disponible en el sitio Web de Microsoft Windows Server 2003, en www.microsoft.com/spain/technet/productos/iis/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener Seguridad de Internet Information Services 6.0](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc)
  
[](#mainsection)[Principio de la página](#mainsection)
