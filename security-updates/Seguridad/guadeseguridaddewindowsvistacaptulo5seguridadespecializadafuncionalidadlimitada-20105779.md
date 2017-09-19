---
TOCTitle: 'Guía de seguridad de Windows Vista. Capítulo 5: Seguridad especializada: Funcionalidad limitada'
Title: 'Guía de seguridad de Windows Vista. Capítulo 5: Seguridad especializada: Funcionalidad limitada'
ms:assetid: 'e28d5030-e662-4c7c-ae4f-358f9120d1dc'
ms:contentKeyID: 20105779
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb629464(v=MSDN.10)'
---

Guía de seguridad de Windows Vista
==================================

### Capítulo 5: Seguridad especializada: Funcionalidad limitada

Publicado: noviembre 8, 2006

La línea de base de Seguridad especializada: Funcionalidad limitada (SSLF) que se trata en esta guía va dirigida a ayudar en la creación de entornos muy seguros para equipos en los que se ejecuta Windows Vista™. La preocupación general en asuntos de seguridad es tan grande en estos entornos que puede aceptarse una pérdida significativa de funcionalidad y capacidad de administración. La línea de base de seguridad de cliente de empresa (EC) ayuda a garantizar un sistema de seguridad mejorado que permite disfrutar de una funcionalidad suficiente en el sistema operativo y en las aplicaciones de la mayoría de las organizaciones.

**Advertencia:**

La configuración de seguridad SSLF no está diseñada para la mayoría de las organizaciones empresariales. La configuración de estos parámetros ha sido desarrollada para organizaciones en las que la seguridad prima sobre la funcionalidad.

Si opta por probar e implementar los parámetros de configuración SSLF en los equipos cliente de su entorno, los recursos TI de su organización pueden experimentar un aumento de llamadas solicitando ayuda acerca de los problemas de funcionalidad limitada que estos parámetros imponen. Aunque la configuración para este entorno proporciona un nivel superior de seguridad de los datos y de la red, también hace que algunos servicios necesarios para la organización dejen de funcionar. Ejemplos de ello son los Servicios de Terminal Server, los cuales permiten a varios usuarios conectarse interactivamente a escritorios y aplicaciones ubicados en equipos remotos, así como el Servicio de fax, que permite a los usuarios enviar y recibir faxes con sus equipos a través de la red. Para obtener una lista completa de los servicios cuyo funcionamiento se bloquea en entornos SSLF, consulte la sección "Servicios limitados" dentro de este capítulo.

Es importante tener en cuenta que la línea de base SSLF no es una mera adición a la línea de base EC: la línea de base SSLF proporciona un nivel de seguridad significativamente diferente. Por esta razón, no debe intentar aplicar la línea de base SSLF y la línea de base EC a los mismos equipos que ejecuten Windows Vista. Más bien, y en lo que respecta al propósito de esta guía, es indispensable identificar primero el nivel de seguridad que requiere el entorno y después decidir aplicar una de las dos líneas de base, la EC o la SSLF. Para comparar las diferencias entre los valores de configuración de la línea de base EC y la línea de base SSLF, consulte el Apéndice A, "Configuración de directivas de grupo de seguridad". El archivo Windows Vista Security Guide Settings.xls (en inglés) que acompaña a la guía es otro recurso útil para comparar los valores de configuración.

**Importante**   Si va a utilizar la línea de base SSLF en su entorno, deberá estar preparado para probar los equipos del entorno de forma exhaustiva una vez aplique los valores de configuración SSLF. De esta manera se podrá asegurar de que no se impide disponer de aquellas funciones necesarias en los equipos del entorno.

##### En esta página

[](#edaa)[Entorno de seguridad especializado](#edaa)
[](#ecaa)[Entorno de seguridad limitada](#ecaa)
[](#ebaa)[GPOAccelerator Tool](#ebaa)
[](#eaaa)[Más información](#eaaa)

### Entorno de seguridad especializado

Las organizaciones que utilizan equipos y redes, especialmente si están conectados a recursos externos como Internet, deben abordar los problemas de seguridad en el diseño, tanto del sistema como de la red, así como la manera en la que están configurados e implementados los equipos. Las capacidades de automatización de procesos, administración remota, acceso remoto, disponibilidad 24 horas al día, acceso a nivel mundial e independencia entre software y dispositivo, permiten a las empresas funcionar de manera más racionalizada y ser más productivos en un mercado competitivo. No obstante, estas capacidades también exponen a los equipos de estas organizaciones a posibles puntos vulnerables.

En general, los administradores prestan mucha atención a evitar que se produzcan accesos no autorizados a los datos, interrupciones de servicios y usos incorrectos de los equipos. Algunas organizaciones especializadas, como las del sector militar, las de los gobiernos locales y estatales y las del sector financiero, necesitan proteger todos sus servicios o algunos de ellos, así como los sistemas y datos que utilizan con un nivel de seguridad especializado. La línea de base SSLF se diseñó para proporcionar este nivel de seguridad a este tipo de organizaciones. Para consultar los valores de configuración SSLF, consulte el Apéndice A, "Configuración de directivas de grupo de seguridad".

[](#mainsection)[Principio de la página](#mainsection)

### Entorno de seguridad limitada

La seguridad especializada que la línea de base SSLF implementa puede disminuir la funcionalidad del entorno. Esto se debe a que se limita a los usuarios a utilizar sólo las funciones específicas que necesitan para realizar las tareas que tienen que llevar a cabo. El acceso queda limitado a las aplicaciones, los servicios y los entornos de infraestructura que se hayan aprobado previamente. La funcionalidad de configuración se ve reducida porque la línea de base deshabilita muchas páginas de propiedades con las que el usuario puede estar familiarizado.

Las secciones que siguen en este capítulo describen las áreas de mayor seguridad y funcionalidad limitada que aplica la línea de base SSLF:

-   Servicios y acceso a datos restringidos

-   Acceso restringido a la red

-   Protección segura de redes

-   Servicios limitados

#### Servicios y acceso a datos restringidos

La línea de base SSLF presenta valores de configuración específicos que pueden evitar que usuarios válidos obtengan acceso a servicios y datos en caso de olvidar sus contraseñas o de escribirlas mal. Además, estos valores pueden hacer que aumente el número de llamadas al personal de asistencia. No obstante, las ventajas en materia de seguridad que ofrecen estos valores de configuración hacen que resulte más difícil que los usuarios malintencionados puedan atacar los equipos con Windows Vista en el entorno. Las opciones de configuración en la línea de base SSLF que podrían evitar potencialmente que los usuarios obtuvieran acceso a servicios y datos incluyen aquellas que:

-   Deshabilitan las cuentas de administrador.

-   Implantan requisitos de contraseña más rigurosos.

-   Imponen directivas de desbloqueo de cuentas más estrictas.

-   Requieren directivas más restrictivas para los siguientes valores de configuración de **Asignaciones de derechos de usuario**:
    **Iniciar sesión como servicio** e **Iniciar sesión como proceso por lotes**.

**Nota**   Los detalles de configuración de las líneas de base EC y SSLF se pueden consultar en el Apéndice A, "Configuración de directivas de grupo de seguridad". El archivo Windows Vista Security Guide Settings.xls (en inglés) que acompaña a la guía es otro recurso útil para comparar los valores de configuración.

#### Acceso restringido a la red

Contar con una red de confianza y una buena conectividad del sistema resulta fundamental para que una empresa funcione. Los sistemas operativos de Microsoft proporcionan capacidades de trabajo en red avanzadas que le ayudan a conectar sistemas, mantener en buen funcionamiento esta conectividad y reparar conexiones con problemas. Aunque esta capacidad resulta beneficiosa para mantener en buen estado la conectividad de la red, los posibles atacantes la pueden aprovechar para dañar los equipos en esta red.

Los administradores generalmente acogen con alegría aquellas funciones que contribuyen al buen funcionamiento de las comunicaciones de red. No obstante, en algunos casos especiales, la primera preocupación es la seguridad de los datos y los servicios. En este tipo de entornos especializados, se tolera cierta pérdida de conectividad en beneficio de una mejor protección de los datos. Entre las opciones de configuración de la línea de base SSLF que aumentan la seguridad de la red, pero que podrían potencialmente impedir a los usuarios obtener acceso a la red, se incluyen aquellas que:

-   Limitan el acceso a los sistemas cliente de la red.

-   Ocultan los sistemas de las listas de búsqueda.

-   Controlan excepciones de Firewall de Windows.

-   Implementan seguridad en la conexión, como la firma de paquetes.

#### Protección segura de redes

Una estrategia habitual para atacar los servicios de red es realizar ataques de denegación de servicios (DoS). Este tipo de ataques impide conectarse a los datos y los servicios o extralimita la capacidad de los recursos del sistema y degrada el rendimiento. La línea de base SSLF protege el acceso a los objetos del sistema y la asignación de recursos frente a este tipo de ataque. Las opciones de configuración en la línea de base SSLF que ayudan a evitar ataques DoS incluyen aquellas que:

-   Controlan las asignaciones de cuota de memoria de procesos.

-   Controlan la creación de objetos.

-   Controlan la capacidad de depuración de programas.

-   Controlan la creación de perfiles de procesos.

Todos estos aspectos de seguridad contribuyen a que la configuración de seguridad de la línea de base SSLF pueda evitar que se ejecuten aplicaciones del entorno o que los usuarios puedan obtener acceso a los servicios y los datos que de otra manera sí obtendrían. Por este motivo, es importante probar en profundidad la línea de base SSLF después y *antes* de implementarla en el entorno de producción.

#### Servicios limitados

Además, la línea de base SSLF evita que cierto número de aplicaciones y utilidades se ejecuten automáticamente. También hace que no se procesen las áreas Ejecutar y Ejecutar una vez del registro. La línea de base SSLF deshabilita igualmente la reproducción automática de CDs.

En concreto, la línea de base SSLF deshabilita los siguientes servicios:

-   **Examinador de equipos** (**Browser**). Este servicio mantiene al día una lista con los equipos de la red, la cual proporciona a los equipos designados como examinadores. Si se deshabilita este servicio, no se podrá actualizar o mantener al día la lista. No se puede iniciar cualquier servicio que dependa explícitamente del servicio.

-   **Servicio de fax** (**Fax**). Este servicio permite a los usuarios enviar y recibir faxes a través de recursos de fax en sus equipos o en la red.

-   **Servicio de publicación FTP** (**MSFtpsvc**). Este servicio proporciona conectividad y administración FTP a través del complemento Servicios de Internet Information Server (IIS).

-   **Servicio de Index Server** (**CiSvc**). Este servicio genera un índice del contenido de los archivos y las propiedades en los equipos locales y remotos. También proporciona un sistema de acceso rápido a los archivos a través de un lenguaje de consulta flexible.

-   **Servicio de administración de IIS** (**IISADMIN**). Este servicio permite administrar servicios FTP y Web a través del complemento IIS.

-   **Servicio Administrador de sesión de Ayuda de escritorio remoto** (**RDSessMgr**). Este servicio administra y controla la asistencia remota. Si este servicio está deshabilitado, no podrá utilizarse la asistencia remota.

-   **Servicio de enrutamiento y acceso remoto** (**RemoteAccess**). Este servicio ofrece un servicio de enrutamiento a las empresas dentro de un entorno de red de área local (LAN) y de red de área extensa (WAN).

-   **Servicio de captura SNMP** (**SNMPTRAP**). Este servicio intercepta mensajes generados por agentes SNMP locales o remotos y los reenvía a programas de administración SNMP que se ejecutan en equipos cliente.

-   **Servicio SNMP** (**SNMP**). Este servicio incluye agentes que supervisan la actividad de los dispositivos de la red e informan a la consola de administración de la red.

-   **Servicio de descubrimientos SSDP** (**SSDPSRV**). Este servicio habilita la detección de dispositivos UPnP en las redes domésticas.

-   **Servicio Programador de tareas** (**Schedule**). Este servicio permite a los usuarios configurar y programar tareas automatizadas en sus equipos. Si se deshabilita este servicio, no se podrán ejecutar las tareas programadas. No se puede iniciar cualquier servicio que dependa explícitamente del servicio.

-   **Servicio Telnet** (**TlntSvr**). Este servicio permite a los usuarios remotos conectarse a otro equipo y ejecutar programas. El servicio admite varios clientes Telnet TCP/IP, incluidos equipos basados en UNIX y Windows. Si este servicio está deshabilitado, es posible que los usuarios remotos no puedan obtener acceso a los programas. No se puede iniciar cualquier servicio que dependa explícitamente del servicio.

-   **Servicios de Terminal Server** (**TermService**). Este servicio permite que varios usuarios se conecten de forma interactiva a las pantallas de los escritorios y a las aplicaciones de equipos remotos. El servicio proporciona el software en segundo plano para las funciones de escritorio remoto (incluido el escritorio remoto para administradores), conmutación rápida de usuarios, asistencia remota y Terminal Server.

-   **Servicio Host de dispositivo Plug and Play universal** (**Upnphost**). Este servicio proporciona compatibilidad para alojar dispositivos Plug and Play universales.

-   **Servicio de publicación World Wide Web** (**W3SVC**). Este servicio proporciona conectividad y administración Web a través del complemento IIS.

La funcionalidad de Windows Vista en equipos cliente se controla a través de la línea de base SSLF hasta el punto de deshabilitar toda la funcionalidad no específicamente necesaria. Esto representa un cambio significativo con respecto a las directivas de seguridad anteriores: En lugar de identificar específicamente aquello que los usuarios necesitan, y después deshabilitar el resto, este método se centra en deshabilitar todos los servicios y todas las utilidades que pueden dañar el sistema operativo en concreto.

#### Implementación de directivas de seguridad

La solución SSLF descrita en esta guía utiliza la Consola de administración de directivas de grupo (GPMC) y secuencias de comandos basadas en GPMC. La consola GPMC está integrada en el sistema operativo Windows Vista, por lo que no tendrá que descargarla e instalarla cada vez que tenga que administrar los GPO de un equipo diferente.

**Importante**   Es necesario que realice cada uno de los procedimientos descritos en esta guía en un equipo cliente con Windows Vista unido a un dominio que utilice el servicio de directorio Active Directory®. Además, el usuario que realice los procedimientos debe disponer de privilegios de administrador del dominio. Si utiliza un sistema operativo Microsoft Windows® XP o Windows Server® 2003, la configuración de seguridad específica de Windows Vista no aparecerá visible en la consola GPMC.

Para implementar el diseño de seguridad debe llevar a cabo tres tareas fundamentales:

1.  Crear el entorno SSLF.

2.  Utilizar la consola GPMC para vincular la directiva de dominio SSLF de VSG (Guía de seguridad de Windows Vista) al dominio.

3.  Utilizar la consola GPMC para comprobar resultados.

Esta sección del capítulo describe cuáles son estas tareas y procedimientos, así como la funcionalidad de la secuencia de comandos GPOAccelerator.wsf, la cual crea automáticamente los GPO recomendados.

##### La secuencia de comandos GPOAccelerator.wsf

La secuencia de comandos **GPOAccelerator.wsf** que acompaña a esta guía creará los GPO que necesita. Ya no es necesario que dedique tanto tiempo a editar manualmente la configuración de las directivas o a aplicar plantillas. Para establecer el entorno SSLF, la secuencia de comandos crea los cuatro GPO siguientes:

-   **Directiva de dominio SSLF de VSG** para el dominio.

-   **Directiva de usuarios SSLF de VSG** para usuarios.

-   **Directiva de escritorio SSLF de VSG** para equipos de escritorio.

-   **Directiva de equipo portátil SSLF de VSG** para equipos portátiles.

**Importante**   Para implementar correctamente el diseño de seguridad para el entorno SSLF, asegúrese de probar en profundidad el diseño antes de implementarlo en el entorno de producción.

Utilice la secuencia de comandos GPOAccelerator.wsf para:

-   **Probar el diseño en un entorno de laboratorio**. En el entorno de laboratorio, utilice la secuencia de comandos GPOAccelerator.wsf para crear una estructura de unidad organizativa, crear los GPO y después vincular automáticamente estos GPO a las unidades organizativas. Cuando haya terminado con la fase de prueba de la implementación, podrá utilizar la secuencia de comandos dentro del entorno de producción.

-   **Implementar el diseño en un entorno de producción**. Cuando empiece a trabajar en el entorno de producción para implementar la solución, primero debe crear una estructura UO adecuada o modificar el conjunto de unidades organizativas existente. Puede servirse de la secuencia de comandos GPOAccelerator.wsf para crear los GPO y después vincular los GPO recién creados a las unidades organizativas del entorno.

##### Probar el diseño en un entorno de laboratorio.

Los GPO que se proporcionan en esta guía han sido sometidos a pruebas exhaustivas. No obstante, es importante que realice sus propias pruebas dentro de su entorno. Para ahorrar tiempo, puede utilizar la secuencia de comandos GPOAccelerator.wsf para crear los GPO recomendados y la estructura UO de muestra y, después, vincular automáticamente los GPO a las UO.

###### Tarea 1: Crear el entorno SSLF

La secuencia de comandos GPOAccelerator.wsf se encuentra en la carpeta Windows Vista Security Guide\\GPOAccelerator Tool que crea el archivo de Microsoft Windows Installer (.msi).

**Nota   **La carpeta GPOAccelerator Tool y sus subcarpetas deben estar presentes en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en el siguiente procedimiento.

**Para crear los GPO y vincularlos a las UO adecuadas en el entorno de laboratorio**

1.  Inicie sesión como administrador del dominio en un equipo con Windows Vista unido al dominio mediante Active Directory y en el cual desee crear los GPO.

2.  En el escritorio, elija el botón **Inicio** de Windows Vista, elija **Todos los programas** y haga clic en **Windows Vista Security Guide**.

3.  Abra la carpeta **GPOAccelerator Tool\\Security Group Policy Objects**.

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir el símbolo del sistema con todos los privilegios de administración de dominio.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /SSLF /LAB** y presione después ENTRAR.

6.  En el cuadro de mensaje **Click Yes to continue** (Haga clic en Sí para continuar)**,o No to exit the script** (No para cerrar la secuencia de comandos), haga clic en **Yes** (SÍ).

    **Nota**   Este paso podría tardar varios minutos.

7.  En el cuadro de mensaje **The** **SSLF Lab Environment is created** (El Entorno de laboratorio SSLF se ha creado correctamente), haga clic en **OK** (Aceptar).

8.  En el cuadro de mensaje **Make sure to link the SSLF Domain GPO to your domain** (Asegúrese de que vincula el GPO del dominio SSLF a su dominio), haga clic en **OK** (Aceptar)y después complete la siguiente tarea para vincular la directiva de dominio SSLF de VSG.

    **Nota**   La directiva de grupo de nivel de dominio incluye valores de configuración aplicables a todos los equipos y usuarios incluidos en el dominio. Es importante poder decidir cuándo vincular el GPO de dominio, ya que este GPO se aplicará a *todos* los usuarios y a todos los equipos. Por ello, la secuencia de comandos GPOAccelerator.wsf no vincula automáticamente el GPO de dominio al dominio.

###### Tarea 2: Utilizar la consola GPMC para vincular la directiva de dominio SSLF de VSG al dominio

Es el momento de vincular el GPO de dominio al dominio. Las instrucciones que siguen describen cómo utilizar la consola GPMC en un equipo cliente con Windows Vista para vincular la directiva de dominio SSLF de VSG al dominio.

**Para vincular la directiva de dominio SSLF de VSG**

1.  Haga clic en el botón **Inicio** de Windows Vista, elija **Todos los programas**, a continuación, **Accesorios** y haga clic en **Ejecutar**. (O presione la tecla del logotipo de Windows y la tecla R.)

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y después haga clic en **Aceptar**.

3.  En el árbol Dominios, haga clic con el botón secundario en el dominio y después elija **Vincular un GPO existente**.

4.  En el cuadro de diálogo **Seleccionar GPO**, elija el GPO de **directiva de dominio SSLF de VSG** y después haga clic en **Sí**.

5.  En el panel de detalles, seleccione la **directiva de dominio SSLF de VSG** y haga clic en el botón **Mover vínculo hasta arriba**.

**Importante**   Asegúrese de que la **directiva de dominio SSLF de VSG** tiene **Orden de vínculos** establecido en **1**. Si no es así, el resto de los GPO vinculados al dominio, como el GPO de directiva de dominio predeterminada, sobrescribirá los valores de configuración de la *Guía de Seguridad de Windows Vista*.

###### Tarea 3: Utilizar la consola GPMC para comprobar los resultados

Puede utilizar la consola GPMC para comprobar los resultados de la secuencia de comandos. El procedimiento que sigue describe cómo utilizar la consola GPMC en un equipo cliente con Windows Vista para comprobar la estructura de UO y los GPO que crea la secuencia de comandos GPOAccelerator.wsf.

**Para comprobar los resultados de la secuencia de comandos GPOAccelerator.wsf**

1.  Haga clic en el botón **Inicio** de Windows Vista, elija **Todos los programas**, a continuación, **Accesorios** y haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y después haga clic en **Aceptar**.

3.  Haga clic en el bosque adecuado, luego en **Dominios** y después en su dominio.

4.  Haga clic en la **UO de Cliente SSLF de la Guía de seguridad de Windows Vista** para expandirla y, después, haga clic en cada una de las cinco UO inferiores para abrirlas.

5.  Compruebe que la estructura UO y los vínculos de los GPO coincidan con los de la siguiente figura.

    ![](images/Bb629464.VSGF0501(es-es,MSDN.10).gif)

    **Figura 5.1 Vista en la consola GPMC de la estructura UO y los vínculos de los GPO que crea la secuencia de comandos GPOAccelerator.wsf**

Todos los GPO que crea la secuencia de comandos GPOAccelerator.wsf se rellenan con los valores de configuración recomendados en esta guía. Ahora puede utilizar la herramienta Usuarios y equipos de Active Directory para probar el diseño desplazando a los usuarios y los equipos a sus respectivas UO. Para obtener información detallada acerca de los valores de configuración que hay en cada GPO, consulte el Apéndice A, "Configuración de directivas de grupo de seguridad".

##### Implementar el diseño en un entorno de producción.

Para ahorrar tiempo, puede servirse de la secuencia de comandos GPOAccelerator.wsf para crear los GPO del entorno SSLF. Después podrá vincular los GPO a las UO adecuadas dentro de la estructura existente. En dominios de mayor tamaño con un número elevado de UO, será necesario determinar cómo se utilizará la estructura UO existente para implementar los GPO.

En dominios de mayor tamaño con un número elevado de UO, será necesario determinar cómo se utilizará la estructura UO existente para implementar los GPO. De ser posible, deberá mantener aparte las UO de los equipos de las UO de los usuarios. Los equipos de escritorio y portátiles también se deberán organizar en sus propias UO. Si no es posible establecer este tipo de infraestructura en su entorno, puede que tenga que modificar los GPO. También puede utilizar la referencia de valores de configuración del Apéndice A, "Configuración de directivas de grupo de seguridad" para determinar qué modificaciones puede ser necesario aplicar.

**Nota**   Tal y como se indicó en la sección anterior, también puede utilizar la secuencia de comandos GPOAccelerator.wsf con la
opción **/LAB** en un entorno de prueba para crear la estructura UO de muestra. No obstante, los entornos con estructura UO flexible también podrán utilizar esta opción en el entorno de producción para crear una estructura UO básica y vincular automáticamente los GPO. A continuación, podrá modificar manualmente la estructura UO de acuerdo con los requisitos del entorno.

###### Tarea 1: Crear los GPO

Los GPO de SSLF que se describen en esta guía se crean mediante la secuencia de comandos GPOAccelerator.wsf. La secuencia de comandos GPOAccelerator.wsf se encuentra en la carpeta Windows Vista Security Guide\\GPOAccelerator Tool que crea el archivo Microsoft Windows Installer (.msi).

**Nota**   También puede optar por copiar simplemente el directorio GPOAccelerator Tool desde un equipo donde esté instalado a otro equipo que desee usar para ejecutar la secuencia de comandos. La carpeta GPOAccelerator Tool y sus subcarpetas deben estar presentes en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en el siguiente procedimiento.

**Para crear los GPO en un entorno de producción**

1.  Inicie sesión como administrador del dominio en un equipo con Windows Vista unido al dominio mediante Active Directory y en el cual desee crear los GPO.

2.  En el escritorio, elija el botón **Inicio** de Windows Vista, elija **Todos los programas** y haga clic en **Windows Vista Security Guide**.

3.  Abra la carpeta **GPOAccelerator Tool\\Security Group Policy Objects**.

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir el símbolo del sistema con todos los privilegios de administración de dominio.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

5.  Cambie a la carpeta **GPOAccelerator Tool\\Security Group Policy Objects**.

6.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /SSLF** y presione después ENTRAR.

7.  En el cuadro de mensaje **Click Yes to continue** **(Haga clic en Sí para continuar)** **o No to exit the script** (No para cerrar la secuencia de comandos), haga clic en **Yes** (Sí).

    **Nota**   Este paso podría tardar varios minutos.

8.  En el cuadro de mensaje **The SSLF GPOs are created** (Los GPO de SSLF se crearon correctamente), haga clic en **OK** (Aceptar).

9.  En el cuadro de texto **Make sure to link the SSLF GPOs to the appropriate OUs** (Asegúrese de vincular los GPO de SSLF a las UO adecuadas), haga clic en **OK** (Aceptar).

###### Tarea 2: Utilizar la consola GPMC para comprobar los resultados

Si lo desea, podrá utilizar la consola GPMC para asegurarse de que la secuencia de comandos haya creado correctamente todos los GPO. El procedimiento que sigue describe cómo utilizar la consola GPMC en un equipo cliente con Windows Vista para comprobar los GPO que crea la secuencia de comandos GPOAccelerator.wsf.

**Para comprobar los resultados de la secuencia de comandos GPOAccelerator.wsf**

1.  Haga clic en el botón **Inicio** de Windows Vista, elija **Todos los programas**, a continuación, **Accesorios** y haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y después haga clic en **Aceptar**.

3.  Haga clic en el bosque adecuado, luego en **Dominios** y después en su dominio.

4.  Haga clic en los **Objetos de directiva de grupo** para expandirlos y, a continuación, compruebe que los cuatro GPO de SSLF de VSG coincidan con los de la figura siguiente.

    ![](images/Bb629464.VSGF0502(es-es,MSDN.10).gif)

    **Figura 5.2 Vista en la consola GPMC de los GPO de SSLF que crea la secuencia de comandos GPOAccelerator.wsf**

En este punto podrá utilizar la consola GPMC para vincular cada GPO a la UO correspondiente. La tarea final de este proceso explica cómo hacerlo.

###### Tarea 3: Utilizar la consola GPMC para vincular los GPO a las UO

El procedimiento que sigue describe cómo utilizar la consola GPMC en un equipo cliente con Windows Vista para realizar esta tarea.

**Para vincular los GPO en un entorno de producción**

1.  Haga clic en el botón **Inicio** de Windows Vista, elija **Todos los programas**, a continuación, **Accesorios** y haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y después haga clic en **Aceptar**.

3.  En el árbol Dominios, haga clic con el botón secundario en el dominio y después elija **Vincular un GPO existente**.

4.  En el cuadro de diálogo **Seleccionar GPO**, elija el GPO de **directiva de dominio SSLF de VSG** y después haga clic en **Aceptar**.

5.  En el panel de detalles, seleccione la **directiva de dominio SSLF de VSG** y haga clic en el botón **Mover vínculo hasta arriba**.

    **Importante**   Asegúrese de que la **directiva de dominio SSLF de VSG** tiene **Orden de vínculos** establecido en **1**. Si no es así, el resto de los GPO vinculados al dominio, como el GPO de directiva de dominio predeterminada, sobrescribirá los valores de configuración de la *Guía de Seguridad de Windows Vista*.

6.  Haga clic con el botón secundario en el nodo de **UO de usuarios de Windows Vista** y, a continuación, haga clic en **Vincular un GPO existente**.

7.  En el cuadro de diálogo **Seleccionar GPO**, elija el GPO de **directiva de usuarios SSLF de VSG** y después haga clic en **Aceptar**.

8.  Haga clic con el botón secundario del mouse en el nodo de **OU de escritorio** y, a continuación, haga clic en **Vincular un GPO existente**.

9.  En el cuadro de diálogo **Seleccionar GPO**, elija el GPO de **directiva de escritorio SSLF de VSG** y después haga clic en **Aceptar**.

10. Haga clic con el botón secundario en el nodo de **UO de equipo portátil** y, a continuación, haga clic en **Vincular un GPO existente**.

11. En el cuadro de diálogo **Seleccionar GPO**, elija el GPO de **directiva de equipo portátil SSLF de VSG** y después haga clic en **Aceptar**.

12. Repita estos pasos con cada UO de usuario o equipo adicional creada para vincular estas UO adicionales a los GPO correspondientes.

**Nota**   También puede arrastrar un GPO desde debajo del nodo de objetos de directiva de grupo hasta la UO adecuada. No obstante, sólo podrá realizar esta operación de arrastrar y colocar dentro del mismo dominio.

**Para confirmar los vínculos de GPO a través de la consola GPMC**

-   Expanda el nodo de **objetos de directiva de grupo**, seleccione el GPO y, a continuación, en el panel de detalles, haga clic en la ficha **Ámbito** y consulte la información en las columna **Vínculo habilitado** y **Ruta de acceso**.

- O bien -

-   Seleccione la UO y, después, en el panel de detalles, haga clic en la ficha **Objetos de directivas de grupos vinculados** y consulte la información de las columnas **Vínculo habilitado** y **GPO**.

**Nota**   Puede utilizar la consola GPMC para desvincular los GPO y, opcionalmente, eliminarlos. A continuación, sírvase de la consola GPMC o de la consola Usuarios y equipos de Active Directory para eliminar las UO que ya no necesite. Para deshacer por completo todas las modificaciones de Active Directory que haya realizado la secuencia de comandos GPOAccelerator.wsf, deberá eliminar manualmente los archivos SSLF-VSGAuditPolicy.cmd, SSLF-ApplyAuditPolicy.cmd y SSLF-AuditPolicy.txt del recurso compartido NETLOGON de uno de los controladores del dominio. Para obtener información adicional acerca de estos archivos, consulte la sección de directiva de auditoría en el Apéndice A, "Configuración de directivas de grupo de seguridad".

Todos los GPO que crea la secuencia de comandos GPOAccelerator.wsf se rellenan con los valores de configuración recomendados en esta guía. Ahora puede utilizar la herramienta Usuarios y equipos de Active Directory para probar el diseño desplazando a los usuarios y los equipos a sus respectivas UO. Para obtener información detallada acerca de los valores de configuración que hay en cada GPO, consulte el Apéndice A, "Configuración de directivas de grupo de seguridad".

##### Migración de GPO a dominios diferentes (opcional)

Si se modificaron los GPO de esta solución, o si se crearon GPO propios que se desean utilizar en más de un dominio, será necesario migrarlos. Migrar un GPO que funciona en un dominio a otro dominio requiere cierta planificación, si bien el procedimiento básico es bastante simple. Hay dos aspectos de especial importancia con respecto a los GPO que se han de tener en cuenta durante la fase de planificación:

-   **La complejidad de los datos**. Los datos que configuran los GPO son complejos y se almacenan en varias ubicaciones. Al utilizar la consola GPMC para migrar los GPO se garantiza que todos los datos relevantes se migren correctamente.

-   **Los datos específicos del dominio**. Algunos datos de los GPO pueden ser específicos de un dominio en cuestión y pueden no resultar válidos si se copian directamente en otro dominio. Para solucionar este problema, la consola GPMC usa tablas de migración que permiten actualizar los datos específicos de dominio de un GPO a valores nuevos dentro del proceso de migración en sí. Sólo es necesario realizar esta operación si el GPO contiene un identificador de seguridad (SID), o rutas de acceso UNC (Convención de nomenclatura universal) específicas de un dominio.

Podrá consultar más información acerca del proceso de migración de los GPO en la Ayuda de la consola GPMC. Las notas de producto "[Migración de GPO a través de dominios con GPMC](http://www.microsoft.com/windowsserver2003/gpmc/migrgpo.mspx)" (en inglés) proporcionan también más información acerca de cómo migrar objetos GPO de un dominio a otro.

[](#mainsection)[Principio de la página](#mainsection)

### GPOAccelerator Tool

Las herramientas y plantillas en esta guía incluyen secuencias de comandos y plantillas de seguridad. Esta sección proporciona información acerca de tales recursos. La herramienta clave que ejecuta la secuencia de comandos central de esta guía de seguridad es GPOAccelerator.wsf, la cual se encuentra en la carpeta Windows Vista Security Guide\\GPOAccelerator Tool\\Security Group Policy Objects. Esta sección incluye información acerca de cómo modificar la consola GPMC para ver los valores de configuración de los GPO, así como la estructura de subdirectorios y los tipos de archivos que acompañan a esta guía. El archivo Windows Vista Security Guide Settings.xls (en inglés) que acompaña a la guía es otro recurso útil para comparar los valores de configuración.

#### Extensión de GPMC y SCE

La solución que esta guía presenta utiliza valores de configuración de GPO que aparecen en la interfaz de usuario estándar de la consola GPMC de Windows Vista o la herramienta Editor de configuración de seguridad (SCE). El grupo Microsoft Solutions for Security desarrolló estas configuraciones (a las cuales se antepone siempre el prefijo **MSS**:) para la anterior guía de seguridad.

**Importante**   La extensiones de SCE y la secuencia de comandos GPOAccelerator.wsf se diseñaron para que se pudieran ejecutar desde un equipo basado en Windows Vista. Estas herramientas no funcionarán correctamente si se intentan ejecutar desde un equipo con Windows XP o Windows Server 2003.

Por este motivo, será necesario que extienda estas herramientas para que pueda ver los valores de configuración de seguridad y editarlos según sea oportuno. Para hacerlo, la secuencia de comandos GPOAccelerator.wsf actualiza automáticamente el equipo al crear los GPO. Si desea administrar los GPO de la *Guía de seguridad deWindows Vista* desde otro equipo con Windows Vista, siga este procedimiento para actualizar la herramienta SCE en ese equipo.

**Para modificar la herramienta SCE con el objeto de mostrar la configuración MSS**

1.  Asegúrese de que cumple con los siguiente requisitos previos:

    -   El equipo que esté utilizando debe estar unido al dominio con Active Directory en los casos donde se hayan creado GPO.

    -   El directorio *Windows* *Vista Security Guide* **GPOAccelerator** **Tool** debe estar presente.

    **Nota**   También puede optar por copiar simplemente el directorio GPOAccelerator Tool desde un equipo donde esté instalado a otro equipo que desee usar para ejecutar la secuencia de comandos. La carpeta GPOAccelerator Tool y sus subcarpetas deben estar presentes en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en el siguiente procedimiento.

2.  Inicie sesión en el equipo como administrador.

3.  En el escritorio, elija el botón **Inicio** de Windows Vista, elija **Todos los programas** y haga clic en **Windows Vista Security Guide**.

4.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects.

5.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir el símbolo del sistema con todos los privilegios de administración.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

6.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /ConfigSCE** y presione después ENTRAR.

7.  En el cuadro de mensaje **Click Yes to continue** (Haga clic en Sí para continuar)**,o No to exit the script** (No para cerrar la secuencia de comandos), haga clic en **Yes** (SÍ).

8.  En el cuadro de mensaje **The Security Configuration Editor is updated** (el Editor de configuración de seguridad se ha actualizado), haga clic en **OK** (Aceptar).

**Importante**   Esta secuencia de comandos sólo modifica la herramienta SCE para mostrar los valores de configuración MSS, no crea ni GPO ni UO.

El procedimiento que sigue quita los valores de configuración de seguridad MSS adicionales y después restablece la herramienta SCE a los valores predeterminados en Windows Vista.

**Para restablecer la herramienta SCE a los valores predeterminados en Windows Vista**

1.  Inicie sesión en el equipo como administrador.

2.  En el escritorio, elija el botón **Inicio** de Windows Vista, elija **Todos los programas** y haga clic en **Windows Vista Security Guide**.

3.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects.

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir el símbolo del sistema con todos los privilegios de administración.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /ResetSCE** y presione después ENTRAR.

6.  En el cuadro de mensaje **Click Yes to continue** (Haga clic en Sí para continuar)**,o No to exit the script** (No para cerrar la secuencia de comandos), haga clic en **Yes** (SÍ).

    **Nota**   Al finalizarse este procedimiento, el Editor de configuración de seguridad en el equipo volverá a los valores de configuración predeterminados en Windows Vista. Los valores agregados al Editor de configuración de seguridad predeterminado serán eliminados. Esto sólo afectará a la capacidad de ver los valores de configuración con el Editor de configuración de seguridad. Los valores de la directiva de grupo configurados permanecerán intactos.

7.  En el cuadro de mensaje **The Security Configuration Editor is updated** (el Editor de configuración de seguridad se ha actualizado), haga clic en **OK** (Aceptar).

#### Valores de configuración de seguridad anteriores

Dispone de plantillas de seguridad para que, si desea crear sus propias directivas en lugar de utilizar o modificar las directivas proporcionadas en esta guía, pueda importar los valores de configuración de seguridad relevantes. Las plantillas de seguridad son archivos de texto que contienen valores de configuración de seguridad y son componentes secundarios de los GPO. Podrá modificar los valores de configuración de directiva incluidos en las plantillas de seguridad en el complemento Editor de objetos de directiva de grupo de MMC. Al contrario que en las versiones anteriores del sistema operativo Windows, Windows Vista no incluye plantillas de seguridad predefinidas, si bien, de ser necesario, se pueden seguir utilizando las plantillas de seguridad existentes.

Las plantillas de seguridad están en el archivo de Windows Installer (.msi) que acompaña a esta guía. Las plantillas siguientes para entornos CE se encuentran en la carpeta GPOAccelerator Tool\\Security Templates:

-   VSG SSLF Desktop.inf

-   VSG SSLF Domain.inf

-   VSG SSLF Laptop.inf

**Importante**   No es necesario que emplee las plantillas de seguridad para implementar la solución que se describe en esta guía. Las plantillas son una alternativa a la solución basada en la consola GPMC y sólo cubren los valores de configuración de seguridad del equipo que aparecen bajo **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**. Por ejemplo, no es posible administrar los valores de configuración de Internet Explorer o de Firewall de Windows en los GPO mediante una plantilla de seguridad y los valores de configuración de usuario no están incluidos.

##### Uso de plantillas de seguridad

Si desea utilizar las plantillas de seguridad, en primer lugar debe extender la herramienta SCE para que la configuración de seguridad MSS personalizada se pueda ver en la interfaz de usuario. Consulte el procedimiento descrito en la sección anterior "Extensión de GPMC y SCE" en este capítulo para ver información detallada. Cuando ya pueda ver las plantillas, podrá utilizar el siguiente procedimiento para importarlas en los GPO que haya creado según sus necesidades.

**Para importar una plantilla de seguridad a un GPO**

1.  Abra el Editor de objetos de directiva de grupo para el GPO que quiera modificar; para hacerlo en la consola GPMC, haga clic con el botón secundario en el GPO y después haga clic en **Editar**.

2.  En el Editor de objetos de directiva de grupo, busque la carpeta **Configuración de Windows**.

3.  Expanda la carpeta **Configuración de Windows** y seleccione **Configuración de seguridad**.

4.  Haga clic con el botón secundario en la carpeta **Configuración de seguridad** y, a continuación, haga clic en **Importar directiva.**

5.  Vaya a la carpeta **Plantillas de seguridad** de la carpeta **Windows Vista Security Guide**.

6.  Seleccione la plantilla de seguridad que desee importar y haga clic en **Abrir**.

    El resultado del último paso de este procedimiento importa los valores de configuración del archivo en el GPO.

También puede utilizar las plantillas de seguridad que acompañan a esta guía para modificar la directiva de seguridad local en equipos cliente independientes con Windows Vista. La secuencia de comandos GPOAccelerator.wsf simplifica el proceso de aplicación de plantillas.

**Para aplicar las plantillas de seguridad con el objeto de crear la directiva de grupo local en un equipo cliente independiente con Windows Vista**

1.  Inicie sesión como administrador en un equipo con Windows Vista.

2.  En el escritorio, elija el botón **Inicio** de Windows Vista, elija **Todos los programas** y haga clic en **Windows Vista Security Guide**.

3.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects.

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir el símbolo del sistema con todos los privilegios de administración.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /SSLF /Desktop** o **cscript GPOAccelerator.wsf /SSLF /Laptop** y después presione ENTRAR.

    Cuando finalice este procedimiento, se modificarán los valores de configuración de la directiva de seguridad con los valores de las plantillas de seguridad para el entorno CE.

**Para restablecer la directiva de grupo local a los valores predeterminados en Windows Vista**

1.  Inicie sesión como administrador en un equipo cliente con Windows Vista.

2.  En el escritorio, elija el botón Inicio de Windows Vista, elija **Todos los programas**, a continuación, **Accesorios**, haga clic con el botón secundario en **Símbolo del sistema** y, después, elija **Ejecutar como administrador**.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba su nombre de usuario y su contraseña y presione ENTRAR.

3.  Cambie a la carpeta **GPOAccelerator Tool\\Security Group Policy Objects**.

4.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /Restore** y presione después ENTRAR.

    Al finalizar este procedimiento se restaurarán los valores de configuración de directiva de seguridad local con los valores predeterminados de Windows Vista.

[](#mainsection)[Principio de la página](#mainsection)

### Más información

Los vínculos que siguen proporcionan información adicional acerca de temas relacionados con la seguridad de Windows Vista.

-   [Administración de directivas de grupo con la consola GPMC](http://go.microsoft.com/fwlink/?linkid=14320) en Microsoft.com.

-   [Administración empresarial con la consola de administración de directivas de grupo](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx) en Microsoft.com.

-   [Migración de objetos GPO de un dominio a otro con la consola GPMC](http://www.microsoft.com/windowsserver2003/gpmc/migrgpo.mspx) en Microsoft.com.

-   [*Guía detallada para comprender el conjunto de funciones de directivas de grupo*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/stepbystep/gpfeat.mspx) en Microsoft TechNet®.

-   [*Guía detallada para usar el Asistente para delegación de control*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/stepbystep/ctrlwiz.mspx) en TechNet.

-   [Resumen de valores de configuración de directiva de grupo nuevos o extendidos](http://www.microsoft.com/technet/windowsvista/library/gpol/2b8dc2fd-eafe-4c74-914c-ec101133feb4.mspx?mfr=true) en TechNet.

-   [Ayuda y soporte técnico para Windows Vista](http://go.microsoft.com/fwlink/?linkid=51089)en Microsoft.com.

-   Las notas del producto [Avances de seguridad de Windows Vista](http://www.microsoft.com/presspass/newsroom/security/vistasecurity.mspx) (en inglés) y el vídeo a petición con esta información en Microsoft.com.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Consiga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)

**Notificaciones de actualizaciones**

[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)

[](#mainsection)[Principio de la página](#mainsection)
