---
TOCTitle: Seguridad de clientes remotos y equipos portátiles
Title: Seguridad de clientes remotos y equipos portátiles
ms:assetid: 'bd780478-d723-4873-b19b-79d5377b993f'
ms:contentKeyID: 20200262
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875832(v=TechNet.10)'
---

Seguridad de clientes remotos y equipos portátiles
==================================================

Actualizado: julio 21, 2006

##### En esta página

[](#elaa)[Introducción](#elaa)
[](#ekaa)[Antes de comenzar](#ekaa)
[](#ejaa)[Service Packs y revisiones](#ejaa)
[](#eiaa)[Virus y gusanos](#eiaa)
[](#ehaa)[Adware y spyware](#ehaa)
[](#egaa)[Puntos de restauración](#egaa)
[](#efaa)[Servidores de seguridad personales](#efaa)
[](#eeaa)[Protección de archivos](#eeaa)
[](#edaa)[Contraseñas seguras](#edaa)
[](#ecaa)[Seguridad de la red inalámbrica](#ecaa)
[](#ebaa)[Conexiones VPN](#ebaa)
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

En este documento se describen las características de seguridad que pueden ayudar a proteger los equipos portátiles y remotos en los se que ejecuta el sistema operativo Microsoft® Windows® XP Professional.

Los usuarios de los equipos se pueden conectar a Internet desde una serie ubicaciones muy variadas en todo el mundo, como hoteles y residencias privadas. Se pueden conectar mediante los cables de red tradicionales o mediante las redes inalámbricas. Muchos aeropuertos, cafeterías e incluso áreas metropolitanas enteras ofrecen este servicio mediante redes inalámbricas. Los usuarios de equipos portátiles se pueden conectar a Internet, explorar sitios Web difíciles y conectarse a la red de sus organizaciones mediante una red privada virtual (VPN). Los posibles riesgos de códigos maliciosos (incluidos los virus, gusanos y caballos troyanos) constituyen una auténtica amenaza. Los equipos portátiles no son los únicos a los que afecta este riesgo, ya que cualquier equipo infectado o en peligro puede ser el origen de una infección que podría repercutir en los otros equipos de la red de una pequeña empresa.

Se deben tomar precauciones para reducir los riesgos de los equipos remotos y portátiles. Algunas de estas precauciones o características de seguridad son las mismas que las que debería habilitar en las estaciones de trabajo. Los usuarios de equipos portátiles tienen que hacer frente a más amenazas. Asimismo, existe una verdadera amenaza de pérdida, daño o robo de equipos portátiles.

En este documento se facilita información acerca de las características de seguridad que las pequeñas empresas pueden utilizar para reducir los riesgos a los que se enfrentan los usuarios de equipos remotos o portátiles. También se incluyen punteros a documentos relacionados que ofrecen instrucciones detalladas para asegurar estos equipos.

#### Objetivo de este documento

Este documento está destinado a familiarizarle con las herramientas y características descritas que proporcionan seguridad a los equipos portátiles y cliente remotos. Tras leer este documento podrá comprobar el nivel de seguridad que se proporciona.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

Se recomienda examinar la información siguiente antes de aplicar las recomendaciones que se describen en este documento.

#### Credenciales necesarias

Este documento exigirá que tenga una cuenta con privilegios para realizar tareas. Dicha cuenta deberá ser miembro del grupo de administradores local de la estación de trabajo. Las cuentas que tengan este nivel de permiso en la estación de trabajo serán las únicas que puedan conceder otro miembro de grupo al grupo de administradores local. Las cuentas que tengan menos privilegios recibirán avisos de "Acceso denegado".

#### Windows Live OneCare

Windows Live OneCare proporciona características de seguridad para proteger equipos cliente de los ataques de red. Cada una de estas características consta de componentes específicos en el Panel de control. El Centro de seguridad de Windows consolidó algunas de estas funciones, pero todavía depende de software de terceros.

El medidor de estado de Windows OneCare proporciona un seguimiento claro y continuo del nivel general de protección y rendimiento del equipo. Si Windows OneCare reconoce alguna acción que pueda realizar para mejorar el nivel de seguridad del equipo, el servicio se la indicará automáticamente para obtener una solución de un solo clic.

Los antivirus, el Firewall, la copia de seguridad de Windows OneCare y la optimización de inicio siempre están activos y supervisando. Estos servicios se configuran automáticamente para que se actualicen y ayuden a mantener el equipo protegido de las últimas amenazas. Microsoft recomienda que se instale y utilice Windows Live OneCare para reunir un grupo de herramientas en una única consola o interfaz de usuario.

El uso de Defender con Windows Live OneCare ofrece un gran conjunto de herramientas para administrar el estado y la seguridad del equipo.

Para obtener más información, consulte el sitio Web de [Windows Live OneCare](http://www.microsoft.com/spain/athome/security/update/onecare_live.mspx), en http://www.microsoft.com/spain/athome/security/update/onecare\_live.mspx.

#### Postura de seguridad

No se debería depender de una única característica de seguridad para proteger los equipos portátiles y remotos de los ataques. Aunque se pueden producir errores con el enfoque de seguridad por capas, éste proporciona siempre un nivel de seguridad. Los equipos portátiles son especialmente vulnerables a los robos y a las pérdidas. Con este artículo se proporcionan características de seguridad que ofrecen capas suplementarias de seguridad para los equipos con Windows XP Professional, pero se trata de capas adicionales que se incluyen para ayudarle a proteger los archivos en caso de que se sustraiga el equipo portátil para explotar la información que pueda contener.

[](#mainsection)[Principio de la página](#mainsection)

### Service Packs y revisiones

El Centro de seguridad de Microsoft proporciona una sencilla manera de administrar las actualizaciones de seguridad para su amplia familia de sistemas operativos y otras aplicaciones de Microsoft, tales como Microsoft Office.

Siga los pasos siguientes para configurar Centro de seguridad con el fin de descargar automáticamente las actualizaciones e instalarlas cuando sea necesario. Se trata de una forma de permitirle administrar las revisiones de seguridad sin la carga de aplicarlas de forma manual.

1.  Haga clic en **Inicio**, y luego en **Panel de control**.

2.  En el Panel de control, haga clic en **Centro de seguridad** (que se muestra en la siguiente captura de pantalla).

    [![](images/Cc875832.SRCPC01(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875832.cfgfwa01(es-es,technet.10).gif)

3.  Haga clic en **Actualizaciones automáticas** (que se muestra en la siguiente captura de pantalla).

    [![](images/Cc875832.SRCPC02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875832.cfgfwa02_big(es-es,technet.10).gif)

4.  Seleccione **Automático (Recomendado)** (que se muestra en la siguiente captura de pantalla) y determine una programación recurrente para que se descarguen e instalen las actualizaciones automáticas. Asegúrese de establecer la programación cuando el equipo se esté ejecutando.

    ![](images/Cc875832.SRCPC03(es-es,TechNet.10).gif)

5.  Tras determinar la programación, haga clic en **Aceptar**.

[](#mainsection)[Principio de la página](#mainsection)

### Virus y gusanos

Los virus informáticos son programas de software diseñados deliberadamente para interferir en el funcionamiento del equipo. Pueden registrar, dañar o eliminar datos y distribuirlos a otros equipos y a través de Internet, lo que normalmente ralentiza la realización de tareas y produce otros problemas en el proceso.

Al igual que los virus humanos, que tienen distintos grados de gravedad, desde el Ébola hasta la gripe de 24 horas, los virus informáticos varían desde los ligeramente molestos a los altamente destructivos. Además, adoptan nuevas y diferentes formas. La parte positiva es que, con un poco de prevención y unos conocimientos mínimos, tendrá menos probabilidades de ser víctima de los virus y podrá reducir su impacto.

Puede contribuir a proteger los datos y las aplicaciones del equipo mediante el uso del software antivirus y de su actualización. Existen muchos programas antivirus que se pueden instalar para proteger a los usuarios de Windows de los virus. Asegúrese de que se cumplen los requisitos del sistema para dicho programa antes de la instalación. Cuando considere adquirir un programa antivirus, elija uno con las características siguientes:

-   Un servicio en tiempo real que administre e impida los ataques de virus.

-   Actualizaciones automáticas que mantengan las firmas de los virus al día.

-   Limpieza y exploración a petición y programadas.

Puede obtener acceso a una lista de [socios proveedores de antivirus de Microsoft](http://www.microsoft.com/spain/partner/seguridad.mspx) en http://www.microsoft.com/spain/partner/seguridad.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Adware y spyware

El spyware suele asociarse con el software que muestra anuncios publicitarios (llamado adware) o con el software que hace seguimientos de la información personal o confidencial. No obstante, esto no quiere decir que todo el software que proporcione anuncios o realice seguimientos de las actividades en línea sea nocivo. Por ejemplo, es posible inscribirse para recibir servicios musicales gratuitos y "pagar" por esto aceptando la recepción de los anuncios pertinentes. Si el usuario entiende y acepta los términos del contrato, supondrá que éste considera que es un intercambio justo. Además, es posible que el usuario permita que la empresa en cuestión realice un seguimiento de sus actividades en línea para determinar qué tipo de anuncios debe mostrarle.

Otros tipos de software no deseado realizarán cambios en el equipo que pueden resultar molestos y provocar que éste se ralentice o se bloquee. Estos programas tienen la capacidad de cambiar la página de inicio o la de búsqueda del explorador Web o de añadir componentes adicionales al explorador que ni se necesitan ni se desean. Asimismo, suelen dificultar el restablecimiento de la configuración establecida previamente. Estos programas no deseados suelen llamarse también spyware.

Windows Defender (Beta2) es una tecnología de seguridad que ayuda a proteger a los usuarios de Windows del spyware y de otros tipos de software potencialmente no deseados. El spyware conocido del equipo puede detectarse y eliminarse, lo que contribuye a reducir sus efectos negativos, incluida la ralentización del equipo, la aparición de anuncios emergentes molestos, los cambios no deseados de la configuración de Internet y el uso no autorizado de la información privada. Una protección continua mejora la seguridad de la exploración de Internet mediante la protección de más de 50 vías por las que el spyware puede introducirse en el equipo. Los integrantes de la comunidad de ámbito mundial SpyNet™ desempeñan una labor clave a la hora de determinar qué programas sospechosos pueden clasificarse como spyware. En consecuencia, los investigadores de Microsoft desarrollan rápidamente métodos para contrarrestar dichas amenazas y las actualizaciones resultantes se descargan automáticamente en los equipos para que estén totalmente al día.

Puede descargar [Windows Defender](http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx) en www.microsoft.com/spain/athome/security/spyware/software/default.mspx. La versión actual es la Beta 2. El nombre del archivo es WindowsDefender.msi y ocupa unos 5,5 MB. (El nombre y el tamaño del archivo pueden modificarse tras el lanzamiento completo.)

Complete los pasos siguientes para instalar Windows Defender (Beta 2) una vez descargado.

1.  Al descargar Windows Defender (Beta 2), aparecerá el siguiente cuadro de diálogo. Haga clic en **Ejecutar**.

    ![](images/Cc875832.SRCPC04(es-es,TechNet.10).gif)

2.  A continuación, aparecerá la pantalla **Éste es el Asistente para instalación de Windows Defender**. Haga clic en **Siguiente**.

    ![](images/Cc875832.SRCPC05(es-es,TechNet.10).gif)

3.  Aparecerá el **Contrato de licencia de Windows Defender** (que se muestra en la siguiente captura de pantalla). Revise los términos del contrato.

    Para continuar con la instalación, seleccione **Acepto los términos del contrato de licencia** y haga clic en **Siguiente**.

    ![](images/Cc875832.SRCPC06(es-es,TechNet.10).gif)

4.  En la pantalla **Ayudar a proteger Windows** (que se muestra en la siguiente captura de pantalla), seleccione **Utilizar la configuración recomendada**. Haga clic en el botón **Declaración de privacidad** si desea leerla. Haga clic en **Siguiente**.

    ![](images/Cc875832.SRCPC07(es-es,TechNet.10).gif)

5.  En la pantalla **Tipo de instalación** (que se muestra en la siguiente captura de pantalla), seleccione **Completa** y haga clic en **Siguiente**.

    ![](images/Cc875832.SRCPC08(es-es,TechNet.10).gif)

6.  Cuando se muestre la pantalla **Preparado para instalar Windows Defender**, haga clic en el botón **Instalar** para comenzar la instalación.

    ![](images/Cc875832.SRCPC09(es-es,TechNet.10).gif)

7.  Una vez finalizado el proceso de instalación, debería aparecer la pantalla**Instalación finalizada de Windows Defender**.

    Asegúrese de que la opción **Buscar definiciones actualizadas y realizar una exploración** esté seleccionada y haga clic en **Finalizar**.

    **Nota**   Se requiere la conexión a Internet para este paso.

    ![](images/Cc875832.SRCPC10(es-es,TechNet.10).gif)

8.  Cuando aparezca la siguiente pantalla, haga clic en el botón **Buscar actualizaciones** para obtener las actualizaciones más recientes.

    [![](images/Cc875832.SRCPC11(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875832.srcpc11_big(es-es,technet.10).gif)

Para obtener más información sobre este tema y sobre las características avanzadas de Windows Defender (Beta 2), consulte el sitio Web de [Windows Defender (Beta 2)](http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx) en www.microsoft.com/spain/athome/security/spyware/software/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Puntos de restauración

Existen varios elementos que pueden dañar un sistema operativo y sus aplicaciones. Windows XP Professional le puede ayudar a restaurar un cliente remoto o portátil en un punto de restauración aceptable. En ocasiones, los sistemas operativos guardan automáticamente estos puntos de restauración antes de algunos sucesos.

Para obtener más información, consulte “[How to ‘undo’ a big mistake in Windows](http://www.microsoft.com/spain/empresas/temas/ventaja_competitiva/resolverproblemas.mspx)” en www.microsoft.com/spain/empresas/temas/ventaja\_competitiva/
resolverproblemas.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Servidores de seguridad personales

Un servidor de seguridad es un sistema de seguridad que actúa como frontera protectora entre una red y el mundo exterior. Windows XP SP2 incluye Firewall de Windows, un software de servidor de seguridad para cada equipo cliente individual.

Firewall de Windows viene instalado en Windows XP Professional SP2 y cuenta con múltiples opciones de configuración. Se habilita de forma predeterminada y ayuda a proteger el equipo contra los ataques a la red. Asimismo, Windows Live OneCare también se encarga de la supervisión de Firewall de Windows y proporciona una única consola para la comprobación del estado global de seguridad del equipo. A continuación, se muestra la manera de modificar la configuración de Firewall de Windows a través del Centro de seguridad de Windows, que se encuentra en el Panel de control.

**Nota**   Firewall de Windows no está diseñado para sustituir la funcionalidad del servidor de seguridad de la red. La red de Windows está habilitada y permite pasar Firewall de Windows, lo que implica que el usuario podrá seguir comunicándose con otros equipos de la red, imprimir y obtener acceso a elementos compartidos en la red. No obstante, se recomienda contar con un servidor de seguridad de la red para proteger los puertos que se abren con estas funciones.

Para obtener más información acerca de la solución de los servidores de seguridad en red de Microsoft, consulte la página [Microsoft Internet Security and Acceleration Server](http://www.microsoft.com/spain/isaserver/default.mspx) en www.microsoft.com/spain/servidores/isaserver/default.mspx.

#### Configuración de los parámetros generales de Firewall de Windows

Los parámetros generales de Firewall de Windows permiten configurar estas opciones:

-   **Activado** (recomendado).

-   **Desactivado** (no se recomienda). Si desactiva Firewall de Windows, su equipo será más vulnerable frente a ataques de virus, gusanos o intrusos.

1.  Para abrir el Centro de seguridad de Windows, haga clic en **Inicio**, **Panel de control**. Aparecerá la pantalla siguiente.

    [![](images/Cc875832.SRCPC12(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875832.prot_clients_net_attacks_01(es-es,technet.10).jpg)

2.  En la sección **Elija una categoría**, haga clic en **Centro de seguridad**. Aparecerá la pantalla **Centro de seguridad de Windows**, como se muestra en la captura de pantalla siguiente.

    [![](images/Cc875832.SRCPC13(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875832.cfgfwa02_big(es-es,technet.10).gif)

#### Notificaciones de configuración

Firewall de Windows muestra un cuadro de diálogo de notificación de forma predeterminada siempre que bloquee un programa que intente establecer una comunicación de su equipo a otro. El cuadro de diálogo es similar al que se muestra en la captura de pantalla siguiente:

![](images/Cc875832.SRCPC14(es-es,TechNet.10).gif)

Dicho cuadro de diálogo indica qué programa se ha bloqueado y permite seleccionar si se desea admitirlo o no. Las opciones disponibles son las siguientes:

-   **Mantener el bloqueo**. Utilice esta opción para que el programa no acepte las conexiones desde Internet o desde la red sin permiso.

-   **Desbloquear**. Utilice esta opción para incluir el programa en la lista de excepciones de Firewall de Windows.

-   **Preguntar más tarde**. Utilice esta opción si no sabe si bloquear el programa o no. Esta opción mantiene bloqueado el programa para obtener una mayor seguridad. La próxima vez que se bloquee el programa, volverá a aparecer este mensaje.

Para obtener más información acerca de las características avanzadas, consulte "[Understanding Windows Firewall](http://www.microsoft.com/spain/windowsxp/using/security/internet/sp2_wfintro.mspx)" en www.microsoft.com/spain/windowsxp/using/security/internet/sp2\_wfintro.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Protección de archivos

Windows XP Professional y otros sistemas operativos de Microsoft utilizan el sistema de archivos NTFS. Este sistema de archivos es más tolerante a los errores que los sistemas predecesores de tabla de asignación de archivos (FAT). NTFS también ofrece controles de acceso de nivel de archivo y el Sistema de archivos de cifrado (EFS). Cuando se prepara un equipo portátil con Windows XP Professional, Microsoft recomienda que sólo se utilice el sistema NTFS para formatear los discos duros.

#### NTFS

NTFS v5 es una sistema de archivos más avanzado que FAT8, FAT16, FAT32, e incluso que los sistemas de archivos NTFS v4. NTFS es más adecuado para tratar errores de disco menos importantes y, si se utiliza correctamente con EFS, resulta realmente adecuado para la informática portátil.

**Nota**   De forma predeterminada, un atacante experto que tenga acceso físico a un disco duro al que se haya dado formato con el sistema NTFS o con la familia de sistemas de archivo FAT puede obviar características de seguridad sin que EFS esté habilitado. Aunque EFS esté habilitado, un atacante puede averiguar el equipo portátil Windows XP Professional que falta.

Se puede convertir una partición FAT existente de Windows XP Professional en una partición NTFS para obtener el nivel de estabilidad y seguridad adicional. El procedimiento se explica en el artículo "[How to Convert FAT Disks to NTFS](http://www.microsoft.com/spain/technet/recursos/articulos/2201021.aspx)" en el sitio Web de Microsoft en www.microsoft.com/spain/technet/recursos/articulos/2201021.aspx. Sin embargo, puede que algunos programas antiguos no se ejecuten en un volumen NTFS, por lo que deberá comprobar los requisitos actuales de su software antes de realizar la conversión.

**Nota**   Realice siempre un copia de seguridad de los archivos importantes antes de convertir un sistema de archivos en otro.

#### EFS

EFS sólo está disponible en sistemas de archivos NTFS, no en los sistemas de archivos FAT. El cifrado es un proceso que consiste en codificar los archivos para evitar el acceso no autorizado. Tras cifrar un archivo o una carpeta, se trabaja con el archivo o carpeta cifrada de igual forma que con cualquier otra carpeta o archivo.

Aunque existen varias formas de implementar EFS, establecer las directivas de recuperación de forma local en un equipo portátil o en un escritorio remoto puede ser un error. La directiva de recuperación local permite que un técnico con la suficiente experiencia pueda obtener acceso a los directorios y archivos cifrados mediante EFS. Si se implementa una recuperación desde una perspectiva de dominio, se obtiene un sistema de archivos más seguro.

Para obtener más información acerca de las características avanzadas, consulte “[Protección de datos mediante EFS para cifrar discos duros](http://www.microsoft.com/spain/technet/recursos/articulos/efs.mspx)” en el sitio Web de Microsoft http://www.microsoft.com/spain/technet/recursos/articulos/
efs.mspx.

**Nota**   Los archivos no se pueden comprimir y cifrar a la misma vez.

#### Copia de seguridad de archivos

Efectuar copias de seguridad de archivos le ayuda a garantizar la disponibilidad de éstos si un usuario de un equipo remoto o portátil experimenta un problema. El problema podría ser tan sencillo como la eliminación accidental de archivos, o tan serio como el robo intencionado de un equipo portátil de una pequeña empresa. Realizar copias periódicas de seguridad de archivos es un método económico y proactivo de proteger los datos más valiosos.

Para obtener más información acerca del modo de realizar copias de seguridad y de recuperar archivos en Windows XP Professional, consulte el artículo de Microsoft Knowledge Base "[Cómo utilizar Copia de seguridad para hacer copias de seguridad de los archivos y carpetas de su equipo en Windows XP](http://support.microsoft.com/kb/308422)" en http://support.microsoft.com/kb/308422.

[](#mainsection)[Principio de la página](#mainsection)

### Contraseñas seguras

Uno de los puntos débiles de seguridad más habituales es una contraseña insegura. Una contraseña debería ser lo suficientemente segura para proteger los archivos y equipos en los que se utiliza. Una contraseña segura le puede ayudar a proteger cualquier equipo de riesgos. El software para averiguar contraseñas es común y sencillo de utilizar.

Para obtener información detallada sobre el establecimiento de contraseñas seguras, consulte la sección "[Contraseñas seguras](http://www.microsoft.com/spain/empresas/seguridad/articulos/select_sec_passwords.mspx)” en el sitio Web de Microsoft en http://www.microsoft.com/spain/empresas/seguridad/articulos/select\_sec\_passwords.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Seguridad de la red inalámbrica

Los equipos cliente portátiles y remotos pueden estar bajo riesgo de ataque en cualquier momento mientras esté habilitado el adaptador de red inalámbrica. Microsoft recomienda deshabilitar los adaptadores de redes inalámbricas cuando no se utilicen.

Se debe tener en cuenta una consideración especial antes de conectarse a una red inalámbrica nueva. Algunas redes inalámbricas que se anuncian son realmente inseguras. Las características descritas en este artículo le pueden ayudar a proteger los equipos portátiles y las estaciones de trabajo de Windows XP Professional de ataques mientras están conectados a estas redes. Sin embargo, la regla primordial de las redes inalámbricas consiste en conectarse únicamente a redes conocidas.

Para proteger redes inalámbricas remotas, como una red doméstica, consulte"[Configuring Windows XP IEEE 802.11 Wireless Networks for the Home and Small Business](http://www.microsoft.com/spain/technet/recursos/articulos/wifisoho.mspx)" en el sitio Web de Microsoft TechNet en www.microsoft.com/spain/technet/recursos/articulos/wifisoho.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Conexiones VPN

Una red privada virtual (VPN) es una forma de conectarse a un equipo portátil o remoto de forma segura de una red a otra, normalmente por Internet. Esta tecnología permite a los usuarios de Windows que tengan un equipo portátil conectarse a una red en un hotel o en una cafetería, y luego conectarse de forma segura a los equipos en red del trabajo.

Las pequeñas empresas pueden tener la tentación de proporcionar conexiones que no sean VPN en Internet para obtener conectividad en accesos remotos. Microsoft recomienda que se utilice una VPN en lugar de una conexión no segura a Internet. El uso de dichas conexiones no seguras expone a las redes domésticas y a las de las pequeñas empresas a riesgos indebidos.

Cuando se hace uso de conexiones VPN en Internet, es importante asegurarse de que la solución VPN inhiba la conexión simultánea a otra red. Esta característica elimina una ruta directa de una red a otra, lo que un software malicioso o un pirata informático podría explotar.

[](#mainsection)[Principio de la página](#mainsection)

### Información relacionada

Para obtener más información sobre servidores de seguridad, actualizaciones informáticas y software antivirus, consulte lo siguiente:

-   La página [Proteja su PC](http://www.microsoft.com/spain/athome/security/protect/windowsxpsp2/default.mspx) en el sitio Web de Microsoft en http://www.microsoft.com/spain/athome/security/protect/windowsxpsp2/Default.mspx.

-   El artículo  "[5-Minute Security Advisor - The Road Warrior's Guide to Laptop Protection](http://www.microsoft.com/spain/technet/recursos/articulos/10110301.aspx)" en el sitio Web de Microsoft TechNet Web en www.microsoft.com/spain/technet/
    /recursos/articulos/10110301.aspx

-   El artículo “Puertos de red clave utilizados por productos de servidor de Microsoft” del [Kit de orientaciones sobre seguridad](http://www.microsoft.com/downloads/details.aspx?familyid=c3260bd0-2ebb-4496-ad07-7e9d55d0ef1f&displaylang=en), que se encuentra en el sitio Web del Centro de descarga de Microsoft en www.microsoft.com/downloads/details.aspx?FamilyID=c3260bd0-2ebb-4496-ad07-7e9d55d0ef1f&displaylang=en.

-   El artículo "[Port numbers](http://www.iana.org/assignments/port-numbers)” del sitio Web de Internet Assigned Numbers Authority que puede encontrarse en www.iana.org/assignments/port-numbers.

-   "[Managing Windows XP Service Pack 2 Features Using Group Policy – Windows Firewall](http://www.microsoft.com/spain/technet/recursos/articulos/mngwfw.mspx)" en el sitio Web Microsoft TechNet en www.microsoft.com/spain/technet/
    recursos/articulos/mngwfw.mspx

Para obtener más información acerca de la seguridad de Windows XP SP2, consulte:

-   La [*Guía de seguridad de Windows XP*](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc) actualizada, que se encuentra en el sitio Web del Centro de descarga de Microsoft en http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/GuideforWinXPProSP2inSMB.doc.

-   "[Cambios de funcionalidad en Service Pack 2 de Microsoft Windows XP - Parte 2: Tecnologías para la protección de redes](http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx)" en el sitio Web Microsoft TechNet en http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx

Para obtener más información acerca del modo de determinar el estado de seguridad de la red, consulte:

-   La página [Microsoft Baseline Security Analyzer](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx) en el sitio Web de Microsoft TechNet en www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx.

Para obtener definiciones acerca de términos relacionados con la seguridad, consulte el documento siguiente:

-   El [Glosario de seguridad de Microsoft](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx), disponible en el sitio Web de Microsoft, en http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga el archivo Seguridad de clientes remotos y equipos portátiles](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc)

[](#mainsection)[Principio de la página](#mainsection)
