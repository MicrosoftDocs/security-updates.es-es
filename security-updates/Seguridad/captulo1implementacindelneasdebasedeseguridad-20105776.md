---
TOCTitle: 'Capítulo 1: Implementación de líneas de base de seguridad'
Title: 'Capítulo 1: Implementación de líneas de base de seguridad'
ms:assetid: '5cc77490-ee9c-41de-829f-e42a86ca088e'
ms:contentKeyID: 20105776
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb629421(v=MSDN.10)'
---

Guía de seguridad de Windows Vista
==================================

### Capítulo 1: Implementación de líneas de base de seguridad

Publicado: noviembre 8, 2006

Windows Vista™ es el sistema operativo más seguro que ha producido Microsoft hasta la fecha. No obstante, es posible que necesite realizar cambios de configuración específicos para cumplir los requisitos de red de su entorno. El objetivo de este capítulo es demostrar que la configuración de los parámetros de seguridad es relativamente fácil para reforzar los equipos cliente en los que se ejecute el sistema operativo predeterminado y que estén unidos a un dominio con el servicio de directorio Active Directory®.

Este capítulo ofrece un conjunto sencillo de procedimientos para implementar la configuración de seguridad recomendada con el fin de mejorar la seguridad predeterminada del sistema operativo. Los procedimientos simplificados de este capítulo ofrecen medios rápidos y eficaces de reforzar los equipos cliente del entorno basados en Windows Vista.

Ahora puede reforzar el sistema operativo predeterminado sólo con objetos de directiva de grupo (GPO). Las instrucciones anteriores de Microsoft exigían la importación de archivos .inf de plantilla de seguridad y la modificación manual de la parte de Plantillas administrativas de varios GPO. Ya no es necesario trabajar con estos archivos y plantillas. No obstante, los archivos .inf de plantilla de seguridad siguen acompañando a esta guía para que pueda usarlos con el fin de reforzar los equipos cliente independientes. Toda la configuración recomendada de directivas de grupo se incluye en el apéndice A "Configuración de directivas de grupo de seguridad".

Para implementar estas instrucciones, es necesario:

-   Crear una estructura de unidad organizativa (UO) para el entorno.

-   Ejecutar la secuencia de comandos GPOAccelerator.wsf que acompaña a la guía.

-   Usar la Consola de administración de directivas de grupo (GPMC) para vincular y administrar los GPO.

**Advertencia:**

Es fundamental probar de forma exhaustiva los diseños de UO y GPO antes de implementarlos en un entorno de producción. La sección "Implementación de directivas de seguridad" de este capítulo ofrece procedimientos que puede usar para crear e implementar la estructura de UO y los GPO de seguridad durante las fases de prueba y producción de la implementación.

Los GPO de línea de base que acompañan a esta guía ofrecen una combinación de configuraciones probadas que mejoran la seguridad de los equipos cliente en los que se ejecuta Windows Vista para los siguientes dos entornos independientes:

-   **Cliente de empresa (EC)**

-   **Seguridad especializada: Funcionalidad limitada (SSLF)**

Este capítulo hace referencia al entorno EC. Para obtener una explicación del entorno SSLF y del proceso al que aplicar la configuración de seguridad específica del mismo, consulte el capítulo 5 "Seguridad especializada: funcionalidad limitada".

##### En esta página

[](#edaa)[Entorno Cliente de empresa](#edaa)
[](#ecaa)[Diseño de seguridad e implementación](#ecaa)
[](#ebaa)[Herramienta GPOAccelerator](#ebaa)
[](#eaaa)[Más información](#eaaa)

### Entorno Cliente de empresa

El entorno Cliente de empresa (EC) al que se hace referencia en este capítulo consiste en un dominio en el que se usa el servicio de directorio Active Directory® en los equipos con Microsoft® Windows Server® 2003 R2 o Windows Server 2003 con Service Pack 1 (SP1) y Active Directory administra los equipos cliente en los que se puede ejecutar Windows Vista o Windows XP®. Los equipos cliente de este entorno se administran mediante la directiva de grupo, que se aplica a sitios, dominios y UO. La directiva de grupo ofrece una infraestructura centralizada en Active Directory que permite la administración de cambios y configuración basada en directorios con respecto a la configuración del usuario y del equipo, que incluye datos de seguridad y usuario.

[](#mainsection)[Principio de la página](#mainsection)

### Diseño de seguridad e implementación

El diseño de seguridad que se recomienda en este capítulo forma el punto de partida de los escenarios de esta guía, así como las sugerencias de mitigación de los escenarios. Las siguientes secciones de este capítulo ofrecen detalles del diseño de seguridad central de la guía y proporcionan procedimientos para probar e implementar el diseño en los equipos en los que se ejecute Windows Vista:

-   **Diseño de UO para directivas de seguridad**

-   **Diseño de GPO para directivas de seguridad**

-   **Implementación de directivas de seguridad**

#### Diseño de UO para directivas de seguridad

Una UO es un contenedor de un dominio que usa Active Directory. Puede contener usuarios, grupos, equipos y otras UO. Si una UO contiene otras UO, se trata de una UO primaria. Las UO incluidas en la UO primaria son UO secundarias.

Puede vincular un GPO a una UO, que posteriormente aplicará la configuración de GPO a los usuarios y equipos contenidos en la UO y en las UO secundarias. Asimismo, para facilitar la administración, puede delegar la autoridad administrativa en cada UO.

Las UO facilitan la agrupación de los usuarios y los equipos con el fin de proporcionar una manera eficaz de segmentar los límites administrativos. Microsoft recomienda que las organizaciones asignen usuarios y equipos a unidades organizativas distintas, puesto que ciertos parámetros de configuración sólo se aplican a los usuarios y otros parámetros sólo se aplican a los equipos.

Puede delegar el control sobre un grupo o una UO individual mediante el Asistente de delegación que se incluye en la herramienta del complemento Usuarios y equipos de Microsoft Management Console (MMC) de Active Directory. Consulte la sección "Información adicional" al final de este capítulo, para ver vínculos a documentación sobre el proceso de delegación de autoridad.

Uno de los principales objetivos de un diseño de UO para cualquier entorno es ofrecer una base para la implementación perfecta de directivas de grupo que se aplique a todos los equipos cliente de Active Directory. Esto garantiza que los equipos cliente cumplen los estándares de seguridad de la organización. El diseño de UO debe ofrecer además una estructura adecuada para alojar la configuración de seguridad de tipos específicos de usuarios de una organización. Por ejemplo, es posible que los desarrolladores necesiten tener un tipo de acceso a sus equipos distinto del de los usuarios medios. Los usuarios de equipos portátiles también pueden tener requisitos de seguridad distintos a los usuarios de equipos de escritorio. En la siguiente figura se muestra una estructura sencilla de unidades organizativas que resulta suficiente para el contenido relacionado con Directiva de grupo que se trata en este capítulo. La estructura de la UO puede diferir de los requisitos del entorno de la organización.

![](images/Bb629421.VSGF0101(es-es,MSDN.10).gif)

**Figura 1.1 Ejemplo de estructura de UO para equipos con Windows Vista**

##### UO de departamento

Dado que los requisitos de seguridad suelen cambiar dentro de una organización, puede resultar lógico crear unidades organizativas de departamento en el entorno. Puede usar esta UO para aplicar la configuración de seguridad a través de un GPO en equipos y usuarios en sus UO de departamento correspondientes.

##### UO de usuarios de Windows Vista

Esta UO contiene las cuentas de usuario del entorno EC. La configuración que se aplica a esta UO se describe en detalle en el apéndice A "Configuración de directivas de grupo de seguridad".

##### UO de equipos de Windows Vista

Esta UO contiene diversas UO secundarias para cada tipo de equipo cliente en el que se ejecuta Windows Vista del entorno EC. Esta guía se centra en las orientaciones de seguridad de equipos de escritorio y portátiles. Por este motivo, los ingenieros de la guía crearon las siguientes UO de equipos:

-   **UO de escritorio**. Incluye los equipos de escritorio que permanecen conectados constantemente a la red. La configuración que se aplica a esta UO se describe en detalle en el apéndice A "Configuración de directivas de grupo de seguridad".

-   **UO de equipo portátil**. Incluye los equipos portátiles de los usuarios móviles que no siempre están conectados a la red. El apéndice A también ofrece información detallada sobre la configuración que se aplica a esta UO.

#### Diseño de GPO para directivas de seguridad

Un GPO es una colección de configuraciones de directiva de grupo compuesta fundamentalmente por los archivos creados por el complemento de directiva de grupo. Las configuraciones se almacenan en el nivel de dominio y afectan a los usuarios y a los equipos contenidos en sitios, dominios y UO.

Puede usar los GPO para garantizar que la configuración de directiva específica, los derechos de usuario y el comportamiento de los equipos se aplican a todos los equipos cliente o usuarios de una UO. El uso de la directiva de grupo en lugar de un proceso de configuración manual simplifica la administración y la actualización de cambios en muchos equipos y usuarios. La configuración manual no sólo resulta ineficiente, por requerir la visita de un técnico a cada equipo cliente, sino porque también es potencialmente ineficaz. Ésta es la principal razón por la que si la configuración de directivas en los GPO basados en dominio es diferente a la que se aplica localmente, la configuración de directivas de GPO basados en dominio sobrescribirá la configuración de directivas aplicada de forma local.

![](images/Bb629421.VSGF0102(es-es,MSDN.10).gif)

**Figura 1.2 Orden de prioridad de GPO**

La ilustración anterior muestra el orden de prioridad en el que se aplican los GPO en un equipo que es miembro de la UO secundaria, desde el nivel inferior (1) al superior (5). La directiva de grupo se aplica primero desde la directiva de seguridad local de cada equipo cliente en el que se ejecute Windows Vista. Después de que se aplique la directiva de seguridad local, los GPO se aplican en el nivel de sitio y, a continuación, en el nivel de dominio.

Cuando los equipos cliente basados en Windows Vista están anidados en varias capas de unidades organizativas, los GPO se aplican en orden descendente, del nivel de la UO primaria de la jerarquía al nivel de la última UO secundaria. El último GPO se aplica desde la unidad organizativa que contiene el equipo cliente. Este orden de procesamiento de los GPO para la directiva de grupo (directiva de seguridad local, de sitio, de dominio, de UO primaria y de UO secundaria) es muy significativo, ya que los GPO que se apliquen posteriormente en el proceso sobrescribirán a los que se aplicaron previamente. Los GPO de usuario se aplican de la misma manera.

Las siguientes consideraciones hacen referencia al diseño de directivas de grupo:

-   Un administrador debe establecer el orden en el que se vinculan los distintos GPO a una UO, o la directiva de grupo se aplicará de forma predeterminada en el orden en el que se vinculó a la UO. Si se especifica la misma configuración en varias directivas, la más alta en la lista de directivas del contenedor será la que tendrá prioridad.

-   Puede configurar un GPO con la opción **Exigido**. Si selecciona esta opción, otros GPO no pueden anular los parámetros configurados en este GPO.

    **Nota   **En Windows 2000 se hace referencia a la opción **Exigido** como **No sobrescribir**.

-   Puede configurar una unidad organizativa, un dominio o un sitio de Active Directory con la opción **Bloquear la herencia de directivas**. Esta opción bloquea la configuración de los GPO más altos en la jerarquía de Active Directory, a menos que se haya seleccionado la opción **Exigido**. Es decir, la opción **Exigido** tiene prioridad sobre la opción **Bloquear la herencia de directivas**.

-   La configuración de Directiva de grupo se aplica a los usuarios y equipos, y está basada en la ubicación en Active Directory del objeto de usuario o equipo. En algunos casos los objetos de usuario pueden precisar que se les aplique una directiva teniendo en cuenta la ubicación del objeto de equipo y no la del objeto de usuario. La característica Modo de procesamiento de bucle invertido de Directiva de grupo permite al administrador aplicar la configuración de Directiva de grupo en función del equipo en el que ha iniciado sesión el usuario. El artículo "[Bucle invertido al procesar la directiva de grupo](http://support.microsoft.com/default.aspx?id=231287)" ofrece más información sobre esta opción.

##### GPO recomendados

Para implementar el diseño de UO descrito anteriormente, es necesario contar con cuatro GPO como mínimo:

-   Una directiva para el dominio

-   Una directiva para la UO de usuarios de Windows Vista

-   Una directiva para la UO de escritorio

-   Una directiva para la UO de equipo portátil

En la siguiente ilustración se expande la estructura de UO previa para mostrar la vinculación entre los GPO y el diseño de UO.

[![](images/Bb629421.VSGF0103(es-es,MSDN.10).gif)](https://technet.microsoft.com/es-es/bb629421.vsgf0103_big(es-es,msdn.10).gif)

**Figure 1.3 Ejemplo de estructura de UO y vínculos de GPO para los equipos con Windows Vista**

En el ejemplo de la figura 1.3, los equipos portátiles son miembros de la UO de equipo portátil. La primera directiva aplicada a los equipos portátiles es la de seguridad local. Puesto que sólo hay un sitio en este ejemplo, no se aplica ningún GPO a nivel de sitio, por lo que se deja el GPO de dominio como la siguiente directiva que se debe aplicar. Por último, se aplica el GPO de equipo portátil.

**Nota**   La **directiva de escritorio** no se aplica a los equipos portátiles puesto que no está vinculada a ninguna unidad organizativa de la jerarquía que contiene la UO de equipo portátil.

Como ejemplo de prioridad, imagine un escenario en el que la configuración de directiva de **Permitir inicio de sesión a través de Servicios de Terminal Server** esta establecida para aplicarse a las UO y grupos de usuarios siguientes:

-   UO de equipos de Windows Vista: grupo **Administradores**

-   UO de equipo portátil: grupos **Usuarios de escritorio remoto** y **Administradores**

En este ejemplo, un usuario cuyas cuentas estén en el grupo **Usuarios de escritorio remoto** puede iniciar sesión en un equipo portátil a través de Terminal Services, ya que la UO de equipo portátil es secundaria de la UO de equipos de Windows Vista y la directiva secundaria tiene prioridad.

Si habilita la opción de directiva **No sobrescribir** en el GPO de la UO de equipos de Windows Vista, sólo los usuarios con cuentas en el grupo **Administradores** pueden iniciar sesión en el equipo portátil a través de Terminal Services. Esto se debe a que la opción **No sobrescribir** impide que la directiva de UO secundaria sobrescriba la directiva aplicada previamente en el proceso.

#### Implementación de directivas de seguridad

La implementación del diseño de seguridad para los dos entornos descritos en esta guía requiere el uso de la Consola de administración de directivas de grupo (GPMC) y de las secuencias de comandos basados en ella. GPMC está integrada en el sistema operativo Windows Vista, por lo que no es necesario descargarla e instalarla cada vez que necesite administrar GPO en un equipo distinto. A diferencia de las orientaciones de seguridad de sistemas operativos Windows anteriores, las orientaciones indicadas en esta guía de Windows Vista automatizan en gran medida el proceso de prueba e implementación del diseño de seguridad para el entorno EC. Esta guía se ha desarrollado y probado con el fin de ofrecer el proceso más eficaz posible a la hora de reducir la sobrecarga asociada al proceso de implementación.

**Importante**   Debe realizar todos los procedimientos de esta guía en un equipo cliente en el que se ejecute Windows Vista, que esté unido a un dominio con Active Directory. Además, el usuario que realice los procedimientos debe contar con privilegios de administrador de dominio. Si usa los sistemas operativos Microsoft Windows® XP o Windows Server® 2003, la configuración de seguridad específica de Windows Vista no estará visible en GPMC.

Para implementar el diseño de seguridad, hay tres tareas clave que llevar a cabo:

1.  Crear el entorno EC.

2.  Usar GPMC para vincular la directiva de dominio EC de la guía de seguridad de Vista (VSG) al dominio.

3.  Usar GPMC para comprobar los resultados.

Esta sección del capítulo describe estas tareas y procedimientos, así como la funcionalidad de la secuencia de comandos GPOAccelerator.wsf, que crea automáticamente los GPO indicados.

##### Secuencia de comandos GPOAccelerator.wsf

La herramienta clave que instala el archivo Windows Vista Security Guide.msi es la secuencia de comandos GPOAccelerator.wsf. La característica principal de la secuencia de comandos es que crea automáticamente todos los GPO necesarios para aplicar estas instrucciones. No es necesario dedicar una gran cantidad de tiempo a editar manualmente la configuración de directivas y aplicar las plantillas. Para los equipos cliente del entorno EC, la secuencia de comandos crea los siguientes cuatro GPO:

-   **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) para el dominio.

-   **VSG EC Users Policy** (Directiva de usuarios de VSG para EC) para los usuarios.

-   **VSG EC Desktop Policy** (Directiva de escritorio de VSG para EC) para los equipos de escritorio.

-   **VSG EC Laptop Policy** (Directiva de equipo portátil de VSG para EC) para los equipos portátiles.

**Importante**   Para implementar correctamente el diseño de seguridad de la guía para el entorno EC, asegúrese de que prueba de forma exhaustiva el diseño antes de implementarlo en el entorno de producción.

Use la secuencia de comandos GPOAccelerator.wsf para:

-   **Probar el diseño en un entorno de laboratorio**. En el entorno de prueba, use la secuencia de comandos GPOAccelerator.wsf para crear una estructura de UO, crear los GPO y vincular automáticamente los GPO a las UO. Una vez que termine la fase de prueba de la implementación, puede usar la secuencia de comandos en el entorno de producción.

-   **Implementar el diseño en un entorno de producción**. Al comenzar a trabajar en un entorno de producción para implementar la solución, primero debe crear una estructura de UO adecuada o modificar un conjunto de UO existente. A continuación, puede usar la secuencia de comandos GPOAccelerator.wsf para crear los GPO y luego vincularlos a las UO correspondientes del entorno.

##### Probar el diseño en un entorno de laboratorio

Los GPO que se ofrecen con esta guían se han probado de forma exhaustiva. No obstante, es importante realizar una comprobación propia de su entorno. Para ahorrar tiempo, puede usar la secuencia de comandos GPOAccelerator.wsf con el fin de crear los GPO correspondientes y la estructura de UO recomendada, y, a continuación, vincular automáticamente los GPO a las UO.

###### Tarea 1: crear el entorno EC

La secuencia de comandos GPOAccelerator.wsf se encuentra en la carpeta Windows Vista Security Guide\\
GPOAccelerator Tool que crea el archivo de Microsoft Windows Installer (.msi).

**Nota   **La carpeta GPOAccelerator Tool y las subcarpetas correspondientes deben encontrarse en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en el siguiente procedimiento.

**Para crear los GPO y vincularlos a las UO correspondientes del entorno de laboratorio**

1.  Inicie sesión como administrador de dominio en un equipo en el que se ejecute Windows Vista, que esté unido al dominio con Active Directory y en el que vaya a crear los GPO.

2.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

3.  Abra la carpeta **GPOAccelerator Tool\\Security Group Policy Objects** (Objetos de directiva de grupo de seguridad).

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos de dominio.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /Enterprise /LAB** y presione ENTRAR.

6.  En el cuadro de mensaje **Click Yes to continue, or No to exit the script** (Haga clic en Sí para continuar, o en No para salir de la secuencia de comandos), haga clic en **Yes** (Sí).

    **Nota**   Este paso puede durar varios minutos.

7.  En el cuadro de mensaje **The** **Enterprise Lab Environment is created** (Se ha creado el entorno Laboratorio empresarial), haga clic en **OK** (Aceptar).

8.  En el cuadro de mensaje **Make sure to link the Enterprise Domain GPO to your domain** (Asegúrese de vincular el GPO de dominio empresarial al dominio), haga clic en **OK** (Aceptar) y, a continuación, realice los pasos de la siguiente tarea para vincular la directiva de dominio EC de VSG.

    **Nota**   La directiva de grupo de nivel de dominio incluye una configuración que se aplica a todos los equipos y usuarios del dominio. Es importante poder decidir cuándo vincular el GPO de dominio, ya que se aplica a *todos* los usuarios y equipos. Por este motivo, la secuencia de comandos GPOAccelerator.wsf no vincula automáticamente el GPO de dominio al dominio.

###### Tarea 2: usar GPMC para vincular la directiva de dominio EC de VSG al dominio.

Ahora puede vincular el GPO de dominio al dominio. Las siguientes instrucciones describen cómo usar GPMC en un equipo cliente en el que se ejecute Windows Vista para vincular la directiva de dominio EC de VSG al dominio.

**Para vincular la directiva de dominio EC de VSG**

1.  Haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas**, elija **Accesorios** y, a continuación, haga clic en **Ejecutar**. También puede presionar la tecla Windows+R.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y haga clic en **Aceptar**.

3.  En el árbol de dominios, haga clic con el botón secundario en el dominio y, a continuación, haga clic en **Vincular un GPO existente**.

4.  En el cuadro de diálogo **Seleccionar GPO**, haga clic en el GPO **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) y, a continuación, haga clic en **Aceptar**.

5.  En el panel de detalles, seleccione **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) y haga clic en el botón **Mover vínculo hasta arriba**.

**Importante**   Asegúrese de que **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) tiene establecido el valor de **Orden de vínculos** en **1**. En caso contrario, otros GPO vinculados al dominio, como el GPO de directiva de dominio predeterminada, sobrescribirán la configuración de la *Guía de seguridad de Windows Vista*.

###### Tarea 3: usar GPMC para comprobar los resultados

Puede usar GPMC para comprobar los resultados de la secuencia de comandos. El siguiente procedimiento describe el modo de uso de GPMC en un equipo cliente con Windows Vista para comprobar los GPO y la estructura de UO que crea la secuencia de comandos GPOAccelerator.wsf.

**Para comprobar los resultados de la secuencia de comandos GPOAccelerator.wsf**

1.  Haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas**, elija **Accesorios** y, a continuación, haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y haga clic en **Aceptar**.

3.  Haga clic en el bosque correspondiente, elija **Dominios** y, a continuación, haga clic en su dominio.

4.  Haga clic y expanda **UO de cliente EC de guía de seguridad de Vista** y, a continuación, haga clic en cada una de las cinco UO contenidas para abrirlas.

5.  Compruebe que la estructura de UO y los vínculos de GPO coinciden con la siguiente ilustración.

    ![](images/Bb629421.VSGF0104(es-es,MSDN.10).gif)

    **Figure 1.4 Vista de GPMC de la estructura de UO y los vínculos de GPO que crea la secuencia de comandos GPOAccelerator.wsf**

Todos los GPO que crea la secuencia de comandos GPOAccelerator.wsf contienen la configuración indicada en esta guía. Ahora puede usar la herramienta Usuarios y equipos de Active Directory para probar el diseño moviendo a los usuarios y equipos a sus UO respectivas. Para obtener información detallada sobre la configuración contenida en cada GPO, consulte el apéndice A "Configuración de directivas de grupo de seguridad".

##### Implementar el diseño en un entorno de producción

Para ahorrar tiempo, puede usar la secuencia de comandos GPOAccelerator.wsf con objeto de crear los GPO para el entorno EC. Así, puede vincular los GPO a las UO correspondientes de la estructura actual. En dominios de mayor tamaño con un gran número de UO, deberá considerar cómo usar la estructura de UO existente para implementar los GPO.

Si es posible, debe mantener las UO de equipo aparte de las UO de usuario. Asimismo, los equipos portátiles y de escritorio se deben organizar en sus UO respectivas. Si esta estructura no es posible en el entorno, es posible que tenga que modificar los GPO. Puede usar la referencia de configuración del apéndice A "Configuración de directivas de grupo de seguridad" que le ayudará a decidir qué modificaciones son necesarias.

**Nota**   Como se comenta en la sección anterior, puede usar la secuencia de comandos GPOAccelerator.wsf con
la opción **/LAB** en un entorno de prueba para crear la estructura de UO de muestra. No obstante, los entornos con una estructura de UO flexible pueden usar además la opción en un entorno de producción para crear una estructura de UO básica y vincular automáticamente los GPO. Así, podrá modificar manualmente la estructura de UO para cumplir los requisitos del entorno.

###### Tarea 1: crear los GPO

Puede crear los GPO de EC que se describen en esta guía con la secuencia de comandos GPOAccelerator.wsf. La secuencia de comandos GPOAccelerator.wsf se encuentra en la carpeta Windows Vista Security Guide\\GPOAccelerator Tool que crea el archivo de Microsoft Windows Installer (.msi).

**Nota**   Sólo tiene que copiar el directorio GPOAccelerator Tool de un equipo donde esté instalado a otro equipo que desee usar para ejecutar la secuencia de comandos. La carpeta GPOAccelerator Tool y las subcarpetas correspondientes deben encontrarse en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en el siguiente procedimiento.

**Para crear los GPO en un entorno de producción**

1.  Inicie sesión como administrador de dominio en un equipo en el que se ejecute Windows Vista, que esté unido al dominio con Active Directory y en el que vaya a crear los GPO.

2.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

3.  Abra la carpeta **GPOAccelerator Tool\\Security Group Policy Objects** (Objetos de directiva de grupo de seguridad).

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos de dominio.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /Enterprise** y presione ENTRAR.

6.  En el cuadro de mensaje **Click Yes to continue, or No to exit the script** (Haga clic en Sí para continuar, o en No para salir de la secuencia de comandos), haga clic en **Yes** (Sí).

    **Nota**   Este paso puede durar varios minutos.

7.  En el cuadro de mensaje **The Enterprise GPOs are created** (Se han creado los GPO empresariales), haga clic en **Aceptar**.

8.  En el cuadro de mensaje **Make sure to link the Enterprise GPOs to the appropriate OUs** (Asegúrese de vincular los GPO empresariales a las UO correspondientes) haga clic en **OK** (Aceptar).

###### Tarea 2: usar GPMC para comprobar los resultados

Puede usar GPMC para asegurarse de que la secuencia de comandos ha creado correctamente todos los GPO. El siguiente procedimiento describe el modo de uso de GPMC en un equipo cliente con Windows Vista para comprobar los GPO que crea la secuencia de comandos GPOAccelerator.wsf.

**Para comprobar los resultados de la secuencia de comandos GPOAccelerator.wsf**

1.  Haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas**, elija **Accesorios** y, a continuación, haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y haga clic en **Aceptar**.

3.  Haga clic en el bosque correspondiente, elija **Dominios** y, a continuación, haga clic en su dominio.

4.  Haga clic y expanda **Objetos de directiva de grupo**, y compruebe que los cuatro GPO de EC de VSG se han creado de acuerdo con lo que aparece en la siguiente ilustración.

    ![](images/Bb629421.VSGF0105(es-es,MSDN.10).gif)

    **Figura 1.5 Vista de GPMC de los GPO de EC que crea la secuencia de comandos GPOAccelerator.wsf**

Ahora puede usar GPMC para vincular cada GPO a la UO correspondiente. La última tarea de este proceso explica cómo llevar a cabo este procedimiento.

###### Tarea 3: usar GPMC para vincular los GPO a las UO

El siguiente procedimiento describe cómo usar GPMC en un equipo cliente con Windows Vista para llevar a cabo esta tarea.

**Para vincular los GPO en un entorno de producción**

1.  Haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas**, elija **Accesorios** y, a continuación, haga clic en **Ejecutar**.

2.  En el cuadro de texto **Abrir**, escriba **gpmc.msc** y haga clic en **Aceptar**.

3.  En el árbol de dominios, haga clic con el botón secundario en el dominio y, a continuación, haga clic en **Vincular un GPO existente**.

4.  En el cuadro de diálogo **Seleccionar GPO**, haga clic en el GPO **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) y, a continuación, haga clic en **Aceptar**.

5.  En el panel de detalles, seleccione **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) y haga clic en el botón **Mover vínculo hasta arriba**.

    **Importante**   Asegúrese de que **VSG EC Domain Policy** (Directiva de dominio de VSG para EC) tiene establecido el valor de **Orden de vínculos** en **1**. En caso contrario, otros GPO vinculados al dominio, como el GPO de directiva de dominio predeterminada, sobrescribirán la configuración de la *Guía de seguridad de Windows* *Vista*.

6.  Haga clic con el botón secundario en el nodo UO de usuarios de Windows Vista y seleccione la opción **Vincular un GPO existente**.

7.  En el cuadro de diálogo **Seleccionar GPO**, haga clic en el GPO **VSG EC Users Policy** (Directiva de usuarios de VSG para EC) y, a continuación, haga clic en **Aceptar**.

8.  Haga clic con el botón secundario en el nodo **UO de escritorio** y, a continuación, seleccione la opción **Vincular un GPO existente**.

9.  En el cuadro de diálogo **Seleccionar GPO**, haga clic en el GPO **VSG EC Desktop Policy** (Directiva de escritorio de VSG para EC) y, a continuación, haga clic en **Aceptar**.

10. Haga clic con el botón secundario en el nodo **UO de equipo portátil** y, a continuación, seleccione la opción **Vincular un GPO existente**.

11. En el cuadro de diálogo **Seleccionar GPO**, haga clic en el GPO **VSG EC Laptop Policy** (Directiva de equipo portátil de VSG para EC) y, a continuación, haga clic en **Aceptar**.

12. Repita estos pasos para cualquier UO de usuario o equipo adicional que haya creado con el fin de vincular dichas UO adicionales a los GPO correspondientes.

**Nota**   También puede arrastrar un GPO desde el nodo Objetos de directiva de grupo a una UO. No obstante, sólo puede realizar esta operación de arrastrar y colocar dentro del mismo dominio.

**Para confirmar los vínculos de GPO con GPMC**

-   Expanda el nodo **Objetos de directiva de grupo** y seleccione el GPO; a continuación, en el panel de detalles, haga clic en la ficha **Ámbito** y anote la información de las columnas **Vínculo habilitado** y **Ruta de acceso**.

- O bien -

-   Seleccione la UO y, en el panel de detalles, haga clic en la ficha **Objetos de directivas de grupo vinculados** y anote la información de las columnas **Vínculo habilitado** y **GPO**.

**Nota**   Puede usar GPMC para desvincular los GPO y, si lo desea, eliminarlos. Posteriormente, use GPMC o la consola de Usuarios y equipos de Active Directory para eliminar cualquier UO que ya no necesite. Para deshacer por completo todas las modificaciones de Active Directory efectuadas por la secuencia de comandos GPOAccelerator.wsf, debe eliminar manualmente los archivos EC-VSGAuditPolicy.cmd, EC-ApplyAuditPolicy.cmd y EC-AuditPolicy.txt del recurso compartido NETLOGON de uno de los controladores de dominio. Para obtener información detallada sobre cómo eliminar por completo la implementación de la directiva de auditoría, consulte la sección sobre esta directiva en el apéndice A "Configuración de directivas de grupo de seguridad".

Todos los GPO que crea la secuencia de comandos GPOAccelerator.wsf contienen la configuración indicada en esta guía. Ahora puede usar la herramienta Usuarios y equipos de Active Directory para probar el diseño moviendo a los usuarios y equipos a sus UO respectivas. Para obtener información detallada sobre la configuración contenida en cada GPO, consulte el apéndice A "Configuración de directivas de grupo de seguridad".

##### Migración de GPO a un dominio distinto (opcional)

Si ha modificado los GPO en esta solución o ha creado GPO propios y desea usarlos en más de un dominio, necesitará migrar los GPO. La migración de un GPO que funciona en un dominio a otro dominio requiere cierta planificación, aunque el procedimiento básico es bastante sencillo. Hay dos aspectos de datos importantes de GPO que se deben considerar durante el proceso de planificación:

-   **Datos complejos**. Los datos que constituyen un GPO son complejos y se almacenan en varias ubicaciones. El uso de GPMC para migrar un GPO garantiza que todos los datos relevantes se migren correctamente.

-   **Datos específicos de dominio**. Algunos datos del GPO pueden ser específicos de dominio y resultar no válidos si se copian directamente en otro dominio. Para resolver este problema, GPMC usa las tablas de migración que permiten actualizar datos específicos de dominio en un GPO a nuevos valores como parte del proceso de migración. Esto sólo es necesario si el GPO contiene identificadores de seguridad (SID) o rutas de acceso de convención de nomenclatura universal (UNC) específicos de un dominio.

La ayuda de GPMC incluye más información sobre la migración de GPO. Las notas del producto "[Migración de GPO entre dominios con GPMC](http://www.microsoft.com/windowsserver2003/gpmc/migrgpo.mspx)" (en inglés) también ofrece información adicional sobre la migración de GPO entre dominios.

[](#mainsection)[Principio de la página](#mainsection)

### Herramienta GPOAccelerator

Las herramientas y plantillas que acompañan a esta guía incluyen secuencias de comandos y plantillas de seguridad. Esta sección ofrece información general sobre estos recursos. La herramienta clave que ejecuta la secuencia de comandos central de esta guía de seguridad es GPOAccelerator.wsf, que se encuentra en la carpeta Windows Vista Security Guide\\GPOAccelerator Tool\\Security Group Policy Objects. Esta sección también incluye información sobre cómo modificar GPMC para ver la configuración de GPO, la estructura de subdirectorios y los tipos de archivos que acompañan a esta guía. El archivo Windows Vista Security Guide Settings.xls (en inglés) que también acompaña a la guía ofrece otro recurso que puede usar para comparar valores de configuración.

#### GPMC y extensiones de SCE

La solución que se presenta en esta guía usa la configuración de GPO que no aparece en la interfaz de usuario (UI) estándar de GPMC en Windows Vista o la herramienta Editor de configuración de seguridad (SCE). El grupo Microsoft Solutions for Security desarrolló estos parámetros, que van siempre precedidos de **MSS:**, para una guía de seguridad anterior.

**Importante**   Las extensiones de SCE y la secuencia de comandos **GPOAccelerator.wsf** están diseñados para ejecutarse en un equipo basado en Windows Vista. Estas herramientas no funcionarán correctamente si intenta ejecutarlas desde un equipo con Windows XP o Windows Server 2003.

Por este motivo, es necesario que amplíe estas herramientas de modo que pueda ver la configuración de seguridad y pueda editarla según sea necesario. Para ello, la secuencia de comandos GPOAccelerator.wsf actualiza automáticamente el equipo a la vez que crea los GPO. Si desea administrar los GPO de la *Guía de seguridad de Windows* *Vista* desde otro equipo en el que se ejecute Windows Vista, use el siguiente procedimiento para actualizar el SCE en dicho equipo.

**Para modificar el SCE con el fin de mostrar la configuración de MSS**

1.  Asegúrese de que ha cumplido los siguientes requisitos previos:

    -   El equipo está unido al dominio mediante Active Directory donde se crearon los GPO.

    -   El directorio **GPOAccelerator** **Tool** de la *Guía de seguridad de Windows* *Vista* está instalado.

    **Nota**   Sólo tiene que copiar el directorio GPOAccelerator Tool de un equipo en el que esté instalado a otro equipo que desee usar para ejecutar la secuencia de comandos. La carpeta GPOAccelerator Tool y las subcarpetas correspondientes deben encontrarse en el equipo local para que la secuencia de comandos se ejecute tal y como se describe en este procedimiento.

2.  Inicie sesión en el equipo como administrador.

3.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

4.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects (Objetos de directiva de grupo de seguridad).

5.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

6.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /ConfigSCE** y presione ENTRAR.

7.  En el cuadro de mensaje **Click Yes to continue, or No to exit the script** (Haga clic en Sí para continuar, o en No para salir de la secuencia de comandos), haga clic en **Yes** (Sí).

8.  En el cuadro de mensaje **The** **Security Configuration Editor is updated** (Editor de configuración de seguridad está actualizado), haga clic en **OK** (Aceptar).

**Important**e   Esta secuencia de comandos sólo modifica el SCE para mostrar la configuración de MSS; no crea ningún GPO ni UO.

El siguiente procedimiento elimina la configuración de seguridad de MSS adicional y, a continuación, restablece la herramienta SCE a su configuración predeterminada en Windows Vista.

**Para restablecer la herramienta SCE a la configuración predeterminada de Windows Vista**

1.  Inicie sesión en el equipo como administrador.

2.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

3.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects (Objetos de directiva de grupo de seguridad).

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /ResetSCE** y presione ENTRAR.

6.  En el cuadro de mensaje **Click Yes to continue, or No to exit the script** (Haga clic en Sí para continuar, o en No para salir de la secuencia de comandos), haga clic en **Yes** (Sí).

    **Nota**   La realización de este procedimiento revierte en el equipo la configuración predeterminada del Editor de configuración de seguridad en Windows Vista. Se eliminará cualquier configuración adicional del Editor de configuración de seguridad. Esto sólo afectará a la capacidad de ver la configuración con el Editor de configuración de seguridad. Los parámetros de directiva de grupo configurados se mantienen.

7.  En el cuadro de mensaje **The** **Security Configuration Editor is updated** (Editor de configuración de seguridad está actualizado), haga clic en **OK** (Aceptar).

#### Configuración de seguridad anterior

Las plantillas de seguridad se proporcionan con el fin de que pueda crear directivas propias, en lugar de usar o modificar las directivas proporcionadas con esta guía, importando la configuración de seguridad correspondiente. Las plantillas de seguridad son archivos de texto que contienen valores de configuración de seguridad y son subcomponentes de los GPO. Puede modificar la configuración de directivas contenida en las plantillas de seguridad en el complemento Editor de objetos de directiva de grupo de MMC. A diferencia de versiones anteriores del sistema operativo Windows, Windows Vista no incluye plantillas de seguridad predefinidas, aunque puede seguir usando las plantillas de seguridad existentes según sea necesario.

Las plantillas de seguridad se incluyen en el archivo de Windows Installer (.msi) que acompaña a esta guía. Las siguientes plantillas del entorno EC se encuentran en la carpeta GPOAccelerator Tool\\Security Templates:

-   VSG EC Desktop.inf

-   VSG EC Domain.inf

-   VSG EC Laptop.inf

**Importante**   No es necesario usar plantillas de seguridad para implementar la solución que se describe en esta guía. Las plantillas ofrecen una alternativa a la solución basada en GPMC y sólo cubren la configuración de seguridad del equipo que aparece en **Computer Configuration\\Windows Settings\\Security Settings**. Por ejemplo, no puede administrar la configuración de Internet Explorer o Firewall de Windows de los GPO con una plantilla de seguridad y la configuración de usuario no está incluida.

##### Uso de las plantillas de seguridad

Si desee usar las plantillas de seguridad, primero debe expandir el SCE para que la configuración de seguridad de MSS personalizada aparezca en la interfaz de usuario. Consulte el procedimiento de la sección anterior "GPMC y extensiones de SCE" de este capítulo para obtener información. Cuando pueda ver las plantillas, podrá usar el siguiente procedimiento para importarlas en los GPO creados según sea necesario.

**Para importar una plantilla de seguridad en un GPO**

1.  Abra el Editor de objetos de directiva de grupo para el GPO que desee modificar; para realizar este proceso en GPMC, haga clic con el botón secundario en el GPO y elija **Editar**.

2.  En el Editor de objetos de directiva de grupo, busque la carpeta **Configuración de Windows**.

3.  Expanda la carpeta **Configuración de Windows** y seleccione **Configuración de seguridad**.

4.  Haga clic con el botón secundario en la carpeta **Configuración de seguridad** y, a continuación, haga clic en **Importar directiva.**

5.  Busque la carpeta **Security Templates** en la carpeta **Windows Vista Security Guide**.

6.  Seleccione la plantilla de seguridad que desee importar y haga clic en **Abrir**.

    El resultado del último paso de este procedimiento importa la configuración del archivo en el GPO.

También puede usar las plantillas de seguridad proporcionadas con la guía para modificar la directiva de seguridad local en los equipos cliente independientes en los que se ejecuta Windows Vista. La secuencia de comandos GPOAccelerator.wsf simplifica el proceso de aplicación de las plantillas.

**Para aplicar las plantillas de seguridad con objeto de crear la directiva de grupo local en un equipo cliente independiente en el que se ejecute Windows Vista**

1.  Inicie sesión como administrador en un equipo con Windows Vista.

2.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

3.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects (Objetos de directiva de grupo de seguridad).

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /Enterprise /Desktop** o **cscript GPOAccelerator.wsf /Enterprise /Laptop** y presione ENTRAR.

    La realización de este procedimiento modifica la configuración de directiva de seguridad local con los valores de las plantillas de seguridad del entorno EC.

**Para restaurar la configuración predeterminada de la directiva de grupo local en Windows Vista**

1.  Inicie sesión como administrador en un equipo cliente con Windows Vista.

2.  En el escritorio, haga clic en el botón **Inicio** de Windows Vista, haga clic en **Todos los programas** y, a continuación, en **Windows Vista Security Guide** (Guía de seguridad de Windows Vista).

3.  Abra la carpeta GPOAccelerator Tool\\Security Group Policy Objects (Objetos de directiva de grupo de seguridad).

4.  Haga clic con el botón secundario en el archivo **Command-line Here.cmd** y, a continuación, haga clic en **Ejecutar como administrador** para abrir un símbolo del sistema con plenos privilegios administrativos.

    **Nota**   Si se le solicitan credenciales de inicio de sesión, escriba el nombre de usuario, la contraseña y presione ENTRAR.

5.  En el símbolo del sistema, escriba **cscript GPOAccelerator.wsf /Restore** y presione ENTRAR.

    La realización de este procedimiento restaura los valores predeterminados de configuración de directiva de seguridad local en Windows Vista.

#### Subdirectorios y archivos

Al ejecutar el archivo de Windows Installer (.msi), crea la carpeta **Windows Vista Security Guide\\GPOAccelerator Tool** de forma predeterminada en una ubicación del equipo que se especifique. El archivo .msi crea la siguiente estructura de subdirectorios en la carpeta **GPOAccelerator Tool**, así como los archivos que se describen en la siguiente tabla.

**Tabla 1.1 Subdirectorios, archivos y descripciones**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subdirectorio\archivo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">SCE Update<br />
\Restore_SCE_to_Default.vbs</td>
<td style="border:1px solid black;">Secuencia de comandos que restaura los valores predeterminados de SCE de Windows Vista.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SCE Update<br />
\Sceregvl_Vista.inf.txt</td>
<td style="border:1px solid black;">Archivo predeterminado SCEREGVL.INF de Windows Vista que revierte los valores originales de SCE.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SCE Update<br />
\Strings-sceregvl.txt</td>
<td style="border:1px solid black;">Archivo de texto que contiene los valores de cadena necesarios para agregar la configuración de MSS al SCE.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SCE Update<br />
\Update_SCE_with_MSS_Regkeys.vbs</td>
<td style="border:1px solid black;">Secuencia de comandos que modifica el SCE para incluir la configuración de MSS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SCE Update<br />
\Sce.reg</td>
<td style="border:1px solid black;">Archivo de registro que contiene los valores de registro de SCE.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SCE Update<br />
\Values-sceregvl.txt</td>
<td style="border:1px solid black;">Archivo de texto que contiene los valores de registro necesarios para ver la configuración de registro del SCE.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Group Policy Objects<br />
\Command-line here.cmd</td>
<td style="border:1px solid black;">Archivo por lotes que abre un símbolo del sistema en la ruta de acceso desde la que se inicia.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Group Policy Objects<br />
\GPOAccelerator.wsf</td>
<td style="border:1px solid black;">Herramienta principal que ejecuta una secuencia de comandos para implementar las instrucciones indicadas.<br />

<strong>Advertencia:</strong>
No use esta secuencia de comandos sin antes leer toda la información de este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\CreateEnvironmentFromXML.wsf</td>
<td style="border:1px solid black;">Secuencia de comandos que crea los GPO y la estructura de UO.<br />

<strong>Advertencia:</strong>
No modifique este archivo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GPMCFiles<br />
\EC-VSG-GPOs.xml</td>
<td style="border:1px solid black;">Archivo XML que usa GPMC para crear los GPO empresariales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\EC-VSG-GPOs-LAB.xml</td>
<td style="border:1px solid black;">Archivo XML que usa GPMC para crear los GPO empresariales y la estructura de UO de muestra.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GPMCFiles<br />
\SSLF-VSG-GPOs.xml</td>
<td style="border:1px solid black;">Archivo XML que usa GPMC para crear los GPO empresariales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\SSLF-VSG-GPOs-LAB.xml</td>
<td style="border:1px solid black;">Archivo XML que usa GPMC para crear los GPO de SSLF y la estructura de UO recomendada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GPMCFiles<br />
\EC-VSGAuditPolicy.txt</td>
<td style="border:1px solid black;">Archivo de texto que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\EC-VSGAuditPolicy.cmd</td>
<td style="border:1px solid black;">Archivo de comandos que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GPMCFiles<br />
\EC-VSGApplyAuditPolicy.cmd</td>
<td style="border:1px solid black;">Archivo de comandos que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\SSLF-VSGAuditPolicy.txt</td>
<td style="border:1px solid black;">Archivo de texto que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GPMCFiles<br />
\SSLF-VSGAuditPolicy.cmd</td>
<td style="border:1px solid black;">Archivo de comandos que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GPMCFiles<br />
\SSLF-VSGApplyAuditPolicy.cmd</td>
<td style="border:1px solid black;">Archivo de comandos que usa la implementación de directiva de auditoría detallada que se incluye en esta guía.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates</td>
<td style="border:1px solid black;">Carpeta que contiene los archivos .inf de plantillas de seguridad que puede usar para implementar algunos parámetros de seguridad que se indican en esta guía.
<strong>Nota</strong>   Microsoft recomienda usar la secuencia de comandos que se incluye con esta guía para crear los GPO indicados. No obstante, las plantillas de seguridad proporcionadas pueden ayudarle a proteger los equipos independientes.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Templates<br />
\EC-VSG Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de escritorio empresarial</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates<br />
\EC-VSG Domain.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de dominio empresarial</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Templates<br />
\EC-VSG Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de equipo portátil empresarial</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates<br />
\SSLF-VSG Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de escritorio de SSLF</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Templates<br />
\SSLF-VSG Domain.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de dominio SSLF</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates<br />
\SSLF-VSG Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad de equipo portátil de SSLF</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Templates<br />
\Vista Default Security.cmd</td>
<td style="border:1px solid black;">Archivo de comandos que se usa como parte de la restauración de la configuración predeterminada de directiva de seguridad local de Windows Vista.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates<br />
\Vista Default Security.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad que se usa como parte de la restauración de la configuración predeterminada de directiva de seguridad local de Windows Vista.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Security Templates<br />
\Vista Default Security.sdb</td>
<td style="border:1px solid black;">Archivo de base de datos de seguridad que se usa como parte de la restauración de la configuración predeterminada de directiva de seguridad local de Windows Vista.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Security Templates<br />
\Vista Local Security.sdb</td>
<td style="border:1px solid black;">Archivo de base de datos de seguridad que se usa al aplicar las plantillas de seguridad de VSG en un equipo.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
Los siguientes vínculos ofrecen información adicional sobre temas de seguridad de Windows Vista:
  
-   [Administración de directiva de grupo con GPMC](http://go.microsoft.com/fwlink/?linkid=14320) (en inglés) en Microsoft.com.
  
-   [Administración empresarial con la Consola de administración de directivas de grupo](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx) (en inglés) en Microsoft.com.
  
-   [Bucle invertido al procesar la directiva de grupo](http://support.microsoft.com/default.aspx?id=231287) en Microsoft.com.
  
-   [Migración de GPO entre dominios con GPMC](http://www.microsoft.com/windowsserver2003/gpmc/migrgpo.mspx) en Microsoft.com.
  
-   [*Guía detallada para comprender el conjunto de funciones de directivas de grupo*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/stepbystep/gpfeat.mspx) (en inglés) Microsoft TechNet®.
  
-   [*Guía detallada de uso del Asistente para delegación de control*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/stepbystep/ctrlwiz.mspx) (en inglés) en TechNet.
  
-   [Resumen de configuración nueva o ampliada de directiva de grupo](http://www.microsoft.com/technet/windowsvista/library/gpol/2b8dc2fd-eafe-4c74-914c-ec101133feb4.mspx?mfr=true) (en inglés) en TechNet.
  
-   [Ayuda y soporte técnico de Windows Vista](http://go.microsoft.com/fwlink/?linkid=51089) (en inglés) en Microsoft.com.
  
-   Notas del producto [Avances de seguridad de Windows Vista](http://www.microsoft.com/presspass/newsroom/security/vistasecurity.mspx) y vídeo a petición (en inglés) sobre esta información en Microsoft.com.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)
  
**Actualizar notificaciones**
  
[Suscríbase para obtener información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)
  
[](#mainsection)[Principio de la página](#mainsection)
