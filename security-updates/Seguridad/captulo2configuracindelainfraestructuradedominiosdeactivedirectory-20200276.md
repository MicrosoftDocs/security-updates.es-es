---
TOCTitle: 'Capítulo 2: Configuración de la infraestructura de dominios de Active Directory'
Title: 'Capítulo 2: Configuración de la infraestructura de dominios de Active Directory'
ms:assetid: '620c0004-41a8-4d13-9a61-e6d879f9cc65'
ms:contentKeyID: 20200276
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163071(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 2: Configuración de la infraestructura de dominios de Active Directory

Actualizado: 20/10/05

### En esta página

[](#elaa)[Información general](#elaa)
[](#ekaa)[Diseño de unidades organizativas compatibles con la administración de la seguridad](#ekaa)
[](#ejaa)[Diseño de objetos de directiva de grupo compatibles con la administración de la seguridad](#ejaa)
[](#eiaa)[Directiva de grupo del nivel de dominio](#eiaa)
[](#ehaa)[Configuración de la directiva de contraseñas](#ehaa)
[](#egaa)[Configuración de directiva de bloqueo de cuentas](#egaa)
[](#efaa)[Configuración de Asignación de derechos de usuario](#efaa)
[](#eeaa)[Configuración de Opciones de seguridad](#eeaa)
[](#edaa)[Directiva Kerberos](#edaa)
[](#ecaa)[Directiva de grupo del nivel de unidad organizativa](#ecaa)
[](#ebaa)[Herramientas de directivas de grupos](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Directiva de grupo es una característica del servicio de directorio Active Directory® que facilita la administración de cambios y configuraciones en dominios Microsoft® Windows Server™ 2003 y Microsoft Windows® 2000 Server. Sin embargo, debe seguir ciertos pasos preliminares en su dominio antes de aplicar Directiva de grupo en su entorno a equipos cliente Microsoft Windows XP Professional con Service Pack 2 (SP2).

La configuración de Directiva de grupo se almacena en objetos de directiva de grupo (GPO) en la base de datos de Active Directory. Los GPO están vinculados a los contenedores, entre los que se incluyen unidades organizativas (UO), dominios y sitios de Active Directory. Debido a que Directiva de grupo está estrechamente integrada con Active Directory, es importante tener conocimientos básicos de la estructura de Active Directory y conocer las implicaciones de seguridad que supone configurar distintas opciones de diseño dentro de la misma antes de implementarla. Para obtener más información sobre el diseño de Active Directory, consulte el capítulo 3, "Directiva de dominio", de la *Guía de seguridad* de *Windows* Server 2003.

Esta directiva constituye una herramienta esencial para garantizar la seguridad de Windows XP. En este capítulo se proporcionan detalles sobre cómo utilizar Directiva de grupo para aplicar y mantener una directiva de seguridad coherente en la red desde una ubicación central.

Esta guía presenta opciones tanto para el entorno de Cliente de empresa (EC) como para el de Seguridad especializada: Funcionalidad limitada (SSLF). Las configuraciones que se recomiendan en este capítulo son idénticas para los equipos de escritorio y portátiles y, dado que se trata de casos especiales, se aplican en el nivel de raíz de dominio, en lugar de aplicarse en el nivel de unidad organizativa. Por ejemplo, las directivas de contraseñas y bloqueo de cuentas para Windows Server 2003 y Windows 2000 Server deben configurarse a través de un GPO que esté vinculado a la raíz del dominio. Los nombres de los archivos de plantilla de seguridad de línea base para los distintos entornos son los siguientes:

-   EC-Domain.inf

-   SSLF-Domain.inf

[](#mainsection)[Principio de la página](#mainsection)

### Diseño de unidades organizativas compatibles con la administración de la seguridad

Una unidad organizativa (UO) es un contenedor dentro de un dominio Active Directory. Una UO puede contener usuarios, grupos, equipos y otras UO, que se conocen como UO secundarias. Puede vincular un GPO a una unidad organizativa; la configuración del GPO se aplicará a los usuarios y equipos que se encuentran en esa UO y sus unidades organizativas secundarias. Para facilitar la administración, puede delegar la autoridad administrativa en cada UO. Las unidades organizativas ofrecen un mecanismo sencillo para agrupar usuarios, equipos y otras entidades de seguridad principales, además de proporcionar un medio eficaz de segmentar los límites administrativos. Microsoft recomienda que las organizaciones asignen usuarios y equipos a unidades organizativas distintas, puesto que ciertos parámetros de configuración sólo se aplican a los usuarios y otros parámetros sólo se aplican a los equipos.

Puede delegar el control sobre un grupo o una UO individual mediante el Asistente de delegación que se incluye en la herramienta del complemento Usuarios y equipos de Microsoft Management Console (MMC) de Active Directory. Consulte la sección "Información adicional" al final de este capítulo, para ver vínculos a documentación sobre el proceso de delegación de autoridad.

Uno de los objetivos principales del diseño de la estructura de unidades organizativas de cualquier entorno es sentar las bases para una implementación sin problemas de Directiva de grupo que se aplique a todas las estaciones de trabajo de Active Directory y que garantice que se cumplen los estándares de seguridad de la organización. De la misma forma, la estructura de unidades organizativas se debe diseñar de forma que ofrezca la configuración de seguridad adecuada a los tipos específicos de usuarios dentro de la misma. Por ejemplo, es probable que los desarrolladores puedan realizar tareas en sus estaciones de trabajo que no estén autorizadas a usuarios con menos privilegios. Los usuarios de equipos portátiles también pueden tener requisitos de seguridad distintos a los usuarios de equipos de escritorio. En la siguiente figura se muestra una estructura sencilla de unidades organizativas que resulta suficiente para el contenido relacionado con Directiva de grupo que se trata en este capítulo. Esta estructura puede diferir significativamente de los requisitos organizativos de su entorno.

![](images/Cc163071.XPSG0201(es-es,TechNet.10).gif)

**Figura 2.1 Estructura de unidades organizativas para equipos Windows XP**

### UO Departamento

Dado que los requisitos de seguridad suelen cambiar dentro de una organización, puede resultar lógico crear unidades organizativas de departamento en el entorno. La configuración de seguridad del departamento se puede aplicar a través de un GPO a los equipos y usuarios en sus respectivas unidades organizativas de departamento.

### UO Usuarios de XP seguros

Esta UO contiene las cuentas para los usuarios tanto en el entorno EC como SSLF. La configuración que se aplica a esta unidad organizativa se describe en la sección "Configuración de usuario" en el capítulo 4, "Plantillas administrativas para Windows XP".

### UO Windows XP

Esta unidad organizativa contiene unidades organizativas secundarias para cada tipo de equipos cliente Windows XP del entorno. En esta guía se incluyen instrucciones para equipos de escritorio y portátiles. Por esta razón se han creado una unidad organizativa Escritorio y una unidad organizativa Equipo portátil.

-   **UO Escritorio**. Incluye los equipos de escritorio que permanecen conectados constantemente a la red. La configuración que se aplica a esta unidad se describe con mayor detalle en el capítulo 3, "Configuración de seguridad para clientes Windows XP" y en el capítulo 4, "Plantillas administrativas para Windows XP".

-   **UO Equipo portátil**. Incluye los equipos portátiles de los usuarios móviles que no siempre están conectados a la red. En el capítulo 3, "Configuración de seguridad para clientes Windows XP" y en el capítulo 4, "Plantillas administrativas para Windows XP" se proporciona información detallada acerca de la configuración que se aplica a esta UO.

[](#mainsection)[Principio de la página](#mainsection)

### Diseño de objetos de directiva de grupo compatibles con la administración de la seguridad

Utilice objetos GPO para asegurarse de que se aplican a todas las estaciones de trabajo o usuarios de una unidad organizativa las configuraciones de directiva, los derechos de usuario y los comportamiento específicos. El uso de Directiva de grupo en vez de la configuración manual simplifica la actualización de varias estaciones de trabajo o usuarios en el futuro cuando se producen cambios adicionales. La configuración manual no es eficaz, porque requiere que un técnico se desplace personalmente a cada equipo cliente. Asimismo, si las configuraciones de directiva en objetos GPO basados en dominio son distintas de las que se aplican localmente, sobrescribirán a éstas últimas.

[![](images/Cc163071.XPSG0202(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163071.xpsg0202_big(es-es,technet.10).gif)

**Figura 2.2 Orden de aplicación de GPO**

En esta figura se muestra el orden en que se aplican los GPO a un equipo miembro de la UO secundaria, de menor (1) a mayor (5). Las directivas de grupo se aplican primero desde la directiva local de cada estación de trabajo Windows XP. Una vez se han aplicado las directivas locales, se aplican los GPO a nivel de sitio y después a nivel de dominio.

Cuando los equipos cliente Windows XP están anidados en varias capas de unidades organizativas, los GPO se aplican en orden descendente, de mayor a menor nivel de unidad organizativa en la jerarquía. El último GPO se aplica desde la unidad organizativa que contiene el equipo cliente. Este orden de procesamiento de los GPO (directiva local, de sitio, de dominio, de UO primaria y de UO secundaria) es muy significativo, ya que los GPO que se apliquen posteriormente en el proceso sobrescribirán a los que se aplicaron previamente. Los GPO de usuario se aplican de la misma manera.

Las siguientes consideraciones hacen referencia al diseño de directivas de grupo.

-   Un administrador debe establecer el orden en el que se vinculan los distintos GPO a una UO, o las directivas se aplicarán de forma predeterminada en el orden en el que se vincularon a la unidad. Si se especifica la misma configuración en varias directivas, la más alta en la lista de directivas del contenedor será la que tendrá prioridad.

-   Puede configurar un GPO con la opción **Forzado**. Si selecciona esta opción, otros GPO no pueden anular los parámetros configurados en este GPO.

    **Nota**: en Windows 2000 se hace referencia a la opción **Forzado** como **No reemplazar**.

-   Puede configurar una unidad organizativa, un dominio o un sitio de Active Directory con la opción **Bloquear la herencia de directivas**. Esta opción bloquea la configuración de los GPO más altos en la jerarquía de Active Directory, a menos que se haya seleccionado la opción **Forzado**. Es decir, la opción **Forzado** tiene prioridad sobre la opción **Bloquear la herencia de directivas**.

-   La configuración de Directiva de grupo se aplica a los usuarios y equipos, y está basada en la ubicación en Active Directory del objeto de usuario o equipo. En algunos casos los objetos de usuario pueden precisar que se les aplique una directiva teniendo en cuenta la ubicación del objeto de equipo y no la del objeto de usuario. La característica Modo de procesamiento de bucle invertido de Directiva de grupo permite al administrador aplicar la configuración de Directiva de grupo en función del equipo en el que ha iniciado sesión el usuario. Para obtener más información sobre la compatibilidad de bucle, consulte las notas del producto sobre Directiva de grupo, que se enumeran en la sección “Más información”, al final de este capítulo.

En la siguiente figura se amplía la estructura de unidades organizativas preliminar y se muestra cómo se pueden aplicar los GPO a los equipos cliente Windows XP que pertenecen a las unidades organizativas Escritorio y Equipo portátil.

[![](images/Cc163071.XPSG0203(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163071.xpsg0203_big(es-es,technet.10).gif)

**Figura 2.3 Estructura de unidades organizativas ampliada para equipos Windows XP de escritorio y portátiles**

En el ejemplo anterior, los equipos portátiles son miembros de la unidad organizativa Equipo portátil. La primera directiva aplicada a los equipos portátiles es la de seguridad local. Puesto que sólo hay un sitio en este ejemplo, no se aplica ningún GPO a nivel de sitio, por lo que se deja el GPO Dominio como la siguiente directiva que se debe aplicar. Por último se aplica el GPO Equipo portátil.

**Nota**:** **la directiva de escritorio no se aplica a los equipos portátiles puesto que no está vinculada a ninguna unidad organizativa de la jerarquía que contiene la UO Equipo portátil. Asimismo, la UO Usuarios de XP seguros no dispone de la plantilla de seguridad correspondiente (archivo .inf), ya que sólo incluye la configuración de Plantillas administrativas.

Para ilustrar cómo se establecen las prioridades, podemos imaginar una situación en la que la configuración de directiva de la UO Windows XP para **Permitir inicio de sesión a través de Servicios de Terminal Server** se establece en el grupo **Administradores** y el parámetro de GPO Equipo portátil para **Permitir inicio de sesión a través de Servicios de Terminal Server** se establece en los grupos **Usuarios avanzados** y **Administradores**. En este ejemplo, un usuario cuya cuenta se encuentre en el grupo **Usuarios avanzados** puede iniciar sesión en un equipo portátil a través de Servicios de Terminal Server porque la UO Equipo portátil es una unidad organizativa secundaria de la UO Windows XP. Si está habilitada la opción de directiva **No reemplazar** en el GPO Windows XP, sólo las cuentas del grupo **Administradores** podrán iniciar sesión en el equipo cliente a través de Servicios de Terminal Server.

### Plantillas de seguridad

Las plantillas de seguridad son archivos de texto que contienen valores de configuración de seguridad. Son subcomponentes de los GPO. Las configuraciones de directiva contenidas en las plantillas de seguridad se pueden modificar en el complemento de MMC Editor de objetos de directiva de grupo, y están ubicadas en la carpeta **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**. También puede modificar estos archivos con el complemento de MMC Plantillas de seguridad o con un editor de texto, como Bloc de notas. Microsoft recomienda utilizar el complemento de Editor de objetos de directiva de grupo para administrar configuraciones de directiva en plantillas de seguridad que se encuentren en GPO, y el complemento Plantillas de seguridad para administrar configuraciones de directiva en plantillas de seguridad independientes.

Algunas secciones de los archivos de plantilla contienen listas de control de acceso (ACL) específicas, que se definen por medio de un lenguaje de definición de descriptores de seguridad (SDDL). Para obtener información detallada acerca de cómo editar plantillas de seguridad y SDDL, consulte la sección “Más información”, al final de este capítulo.

### Administración de plantillas de seguridad

Es muy importante almacenar plantillas de seguridad del entorno de producción en una ubicación segura en la infraestructura. El acceso a las plantillas de seguridad sólo debería asignarse a los administradores responsables de la implementación de Directiva de grupo. Las plantillas de seguridad que se incluyen con Windows XP, Windows 2000 y Windows Server 2003 están almacenadas en la carpeta **%SystemRoot%\\security\\templates** de forma predeterminada. Tal como se explica en el capítulo 1, las plantillas de seguridad incluidas con esta guía se copian en la carpeta **\\Windows XP Security Guide Tools and Templates\\Security Templates** cuando ejecuta el archivo .msi incluido con el archivo WinZip que contiene esta guía. (La versión de descarga de la guía está disponible en http://go.microsoft.com/fwlink/?LinkId=14840). Puede copiar o mover las plantillas de seguridad de esta carpeta a una ubicación nueva en los equipos de prueba mientras evalúa y perfecciona la configuración con arreglo a los requisitos empresariales de la organización. Después de realizar las pruebas, debe mover las versiones finales de las plantillas de seguridad a una ubicación centralizada, como la ubicación predeterminada de las plantillas de seguridad integradas.

La carpeta **%SystemRoot%\\security\\templates** no se replica entre controladores de dominio. Por tanto, será preciso seleccionar un controlador que almacene la copia maestra de las plantillas de seguridad para evitar que se produzcan problemas de control de la versión. Con ello se asegurará de que siempre se modifica la misma copia de las plantillas.

### Importación de una plantilla de seguridad

Siga los pasos del procedimiento que se indica a continuación para importar una plantilla de seguridad.

**Para importar una plantilla a un GPO**

1.  Vaya hasta la carpeta **Configuración de Windows** en el Editor de objetos de directiva de grupo.

2.  Expanda la carpeta **Configuración de Windows** y seleccione **Configuración de seguridad**.

3.  Haga clic con el botón secundario en la carpeta **Configuración de seguridad** y, a continuación, haga clic en **Importar directiva...**

4.  Seleccione la plantilla de seguridad que desee importar y haga clic enAbrir. Se importará la configuración del archivo al GPO.

### Plantillas administrativas

También se ofrecen parámetros de configuración de seguridad adicionales en archivos basados en Unicode que se denominan plantillas administrativas. Estos archivos contienen parámetros del Registro que afectan a Windows XP y a sus componentes, así como a otras aplicaciones, como Microsoft Office 2003. Las plantillas administrativas pueden incluir configuración del equipo y del usuario. La configuración del equipo se almacena en el subárbol del Registro HKEY\_LOCAL\_MACHINE. La configuración del usuario se almacena en HKEY\_CURRENT\_USER.

### Administración de plantillas administrativas

Es importante almacenar las plantillas administrativas que se utilizan en un entorno de producción en una ubicación segura de la infraestructura, del mismo modo que lo es almacenar de manera segura las plantillas de seguridad. El acceso a esta ubicación sólo debería permitirse a los administradores responsables de la implementación de Directiva de grupo. Las plantillas administrativas que se proporcionan con Windows XP y Windows Server 2003 se almacenan en el directorio **%systemroot%\\inf**. El resto de plantillas de Office 2003 se incluyen en el *Kit de recursos de Office 2003*. Las plantillas administrativas que proporciona Microsoft no deben editarse porque pueden cambiar cuando se publican Service Packs.

### Incorporación de una plantilla administrativa a una directiva

Además de las plantillas administrativas que se proporcionan con Windows XP, puede aplicar las plantillas de Office 2003 a aquellos GPO en los que desee configurar los parámetros de Office 2003. O puede haber creado plantillas administrativas personalizadas exclusivas para su organización. Siga el procedimiento que se indica a continuación para agregar una plantilla administrativa a un GPO.

**Para agregar una plantilla administrativa a un GPO**

1.  Vaya hasta la carpeta Plantillas administrativas de Editor de objetos de directiva de grupo.

2.  Haga clic con el botón secundario en la carpeta **Plantillas administrativas** y, a continuación, haga clic en **Agregar o quitar plantillas**.

3.  En el cuadro de diálogo **Agregar o quitar plantillas**, haga clic en **Agregar**.

4.  Vaya hasta la carpeta que contiene los archivos de plantillas administrativas.

5.  Seleccione la plantilla que desee agregar, haga clic en **Abrir** y, a continuación, en **Cerrar**.

[](#mainsection)[Principio de la página](#mainsection)

### Directiva de grupo del nivel de dominio

La directiva de grupo del nivel de dominio incluye parámetros que se aplican a todos los equipos del dominio. En esta guía se sugiere que configure parámetros de nivel de dominio en un GPO nuevo en lugar de hacerlo en la Directiva de dominio predeterminada integrada. El motivo de esta sugerencia es que facilitará la posibilidad de restaurar la configuración predeterminada si los cambios que se introducen en esta guía causan problemas. Debe tener en cuenta que algunas aplicaciones configuran automáticamente la Directiva de dominio predeterminada, y que las configuraciones de directiva que esas aplicaciones cambian pueden entrar en conflicto con parámetros definidos en el GPO de directiva de dominio que se describe en esta guía. Sin embargo, el riesgo de que eso ocurra es reducido, dado que hay muy pocos parámetros que se configuren en el nivel de dominio. La seguridad en el nivel de dominio se trata en detalle en el capítulo 3, "Directiva de dominio", en la [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845), que está disponible en http://go.microsoft.com/fwlink/?LinkId=14845.

[](#mainsection)[Principio de la página](#mainsection)

### Configuración de la directiva de contraseñas

Las contraseñas complejas que se pueden modificar regularmente reducen los riesgos de que se produzcan ataques a las mismas. La configuración de la directiva de contraseñas permite controlar la complejidad y la vigencia de las contraseñas y sólo se puede establecer mediante Directiva de grupo en el nivel de dominio. Para obtener información sobre cómo establecer directivas de contraseñas directamente en el administrador de cuentas de seguridad (SAM) en equipos independientes, consulte el capítulo 5, "Seguridad de clientes Windows XP independientes".

En esta sección se describe cada uno de los parámetros de directiva de contraseñas para los entornos EC y SSLF.

Puede establecer la configuración de directiva de contraseñas en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directivas de contraseñas**

En la siguiente tabla se resumen las recomendaciones acerca de la configuración de la directiva de contraseñas para los dos tipos de entornos seguros definidos en esta guía. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.

**Tabla 2.1 Recomendaciones sobre la configuración de la directiva de contraseñas**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Configuración predeterminada del controlador de dominio</p></th>
<th><p>EC</p></th>
<th><p>SSLF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Forzar el historial de contraseñas</p></td>
<td style="border:1px solid black;"><p>24 contraseñas</p></td>
<td style="border:1px solid black;"><p>24 contraseñas</p></td>
<td style="border:1px solid black;"><p>24 contraseñas</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Vigencia máxima de la contraseña</p></td>
<td style="border:1px solid black;"><p>42 días</p></td>
<td style="border:1px solid black;"><p>90 días</p></td>
<td style="border:1px solid black;"><p>90 días</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Vigencia mínima de la contraseña</p></td>
<td style="border:1px solid black;"><p>1 día</p></td>
<td style="border:1px solid black;"><p>1 día</p></td>
<td style="border:1px solid black;"><p>1 día</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Longitud mínima de la contraseña</p></td>
<td style="border:1px solid black;"><p>7 caracteres</p></td>
<td style="border:1px solid black;"><p>8 caracteres</p></td>
<td style="border:1px solid black;"><p>12 caracteres</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Las contraseñas deben cumplir los requerimientos de complejidad</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
### Forzar el historial de contraseñas
  
Esta configuración determina el número de nuevas contraseñas únicas que se deben asociar a una cuenta de usuario antes de que sea posible volver a utilizar una contraseña anterior. El valor de esta configuración de directiva debe estar comprendido entre 0 y 24 contraseñas. El valor predeterminado para Windows XP es de 0 contraseñas, pero en el caso de un dominio es de 24. Para mantener la eficacia de esta configuración de directiva, utilice el parámetro **Vigencia mínima de la contraseña** con objeto de evitar que los usuarios cambien repetidamente sus contraseñas.
  
Establezca la configuración **Forzar el historial de contraseñas** en **24 contraseñas** para los dos entornos de seguridad definidos en esta guía.
  
### Vigencia máxima de la contraseña
  
Los valores de esta configuración de directiva están comprendidos entre 1 y 999 días. (También puede establecer el valor en 0 para especificar que las contraseñas no caducan). Esta configuración de directiva define durante cuánto tiempo puede utilizar un usuario su contraseña antes de que caduque. El valor predeterminado de esta configuración de directiva es de 42 días. La mayoría de las contraseñas se pueden descifrar; por tanto, cuanto mayor sea la frecuencia con la que se cambian, menores serán las posibilidades de que el atacante pueda utilizarlas. No obstante, cuanto menor sea el valor de la configuración, mayor será, con mucha probabilidad, el número de llamadas al servicio de asistencia que realice el usuario.
  
Establezca la configuración **Vigencia máxima de la contraseña** en un valor de **90 días** para los dos entornos de seguridad definidos en esta guía.
  
### Vigencia mínima de la contraseña
  
Esta configuración de directiva determina el número de días que se debe utilizar una contraseña antes de que un usuario la pueda cambiar. Los valores para esta configuración están comprendidos entre 1 y 998 días. (También puede establecer el valor en 0 para permitir cambios de contraseña inmediatos). El valor predeterminado para esta configuración de directiva es de 0 días.
  
El valor de la configuración **Vigencia mínima de la contraseña** debe ser inferior al especificado para **Vigencia máxima de la contraseña**, a menos que el valor deesta última opción se configure como 0, lo que hace que la contraseña nunca caduque. Si el valor de **Vigencia máxima de la contraseña** se establece en 0, el valor de esta configuración de directiva se puede establecer en cualquier valor comprendido entre 0 y 999.
  
Si desea que la configuración **Forzar el historial de contraseñas** sea efectiva, seleccione un valor mayor que 0. Si el parámetro de **Vigencia mínima de la contraseña** es 0, los usuarios pueden pasar de una contraseña a otra repetidamente hasta volver a su contraseña favorita utilizada con anterioridad.
  
Establezca la configuración **Vigencia mínima de la contraseña** en un valor de 1 día para los dos entornos de seguridad definidos en esta guía. Este valor impide que los usuarios reutilicen la misma contraseña, ya que debe esperarse un día entero antes de poder cambiar la contraseña. También les anima a recordar las nuevas contraseñas, ya que deben utilizarlas durante al menos un día antes del restablecimiento. Por último, evita que los usuarios burlen la restricción de la configuración **Forzar el historial de contraseñas**.
  
### Longitud mínima de la contraseña
  
Esta configuración de directiva determina el número mínimo de caracteres que componen una contraseña para una cuenta de usuario. Hay muchas teorías diferentes acerca de cómo determinar la longitud más adecuada para las contraseñas en una organización, pero quizás "frase cifrada" sea un término que se ajuste más a las circunstancias que el de "contraseña". En Microsoft Windows 2000 y versiones posteriores, las frases cifradas pueden ser bastante largas e incluir espacios. Así, “Quiero beberme un batido de 5 €” es una frase cifrada válida bastante más segura que una cadena compuesta de 8 o 10 caracteres que incluya números y letras aleatorios. Además, es más fácil de recordar. Recuerde que es necesario instruir a los usuarios acerca de la selección y el mantenimiento adecuados de las contraseñas, sobre todo en lo referente a su longitud.
  
En el entorno EC, asegúrese de que el valor para el parámetro **Longitud mínima de la contraseña** se configure en **8 caracteres**. Esta configuración de directiva exige una contraseña lo suficientemente larga como para proporcionar la seguridad adecuada y, al mismo tiempo, lo bastante corta como para que los usuarios la recuerden con facilidad. En el entorno SSLF, configure el valor en **12 caracteres.**
  
### Las contraseñas deben cumplir los requerimientos de complejidad
  
Esta configuración de directiva comprueba todas las contraseñas nuevas para garantizar que se cumplen los requisitos básicos de una contraseña segura. De forma predeterminada, el valor de esta configuración de directiva en Windows XP se establece en **Deshabilitado**, pero aparece como **Habilitado** en el dominio Windows Server 2003.
  
Cada carácter adicional de una contraseña aumenta su complejidad de forma exponencial. Por ejemplo, una contraseña con siete caracteres alfabéticos en minúsculas tendría 267 (aproximadamente 8 x 109 u 8.000 millones) combinaciones posibles. A razón de 1.000.000 de intentos por segundo (capacidad que ofrecen muchas utilidades de descifrado de contraseñas), sólo se necesitarían 133 minutos para descifrarla. Una contraseña alfabética de 7 caracteres en la que se distingan mayúsculas y minúsculas tiene 527 combinaciones. Una contraseña alfanumérica de 7 caracteres en la que se distingan mayúsculas y minúsculas sin puntuación tiene 627 combinaciones. Una contraseña de 8 caracteres tiene 268, o 2 x 1011, combinaciones posibles. Aunque pueda parecer un número inconcebible, a razón de 1.000.000 de intentos por segundo sólo se necesitarían 59 horas para probar todas las contraseñas posibles. Recuerde que estos tiempos se incrementarán considerablemente en el caso de las contraseñas con caracteres ALT y otros caracteres especiales del teclado, tales como ! o @.
  
El uso apropiado de configuraciones de contraseñas puede hacer muy difícil, si no imposible, un ataque de fuerza bruta.
  
### Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio
  
Esta configuración de directiva determina si el sistema operativo almacena las contraseñas de una manera en que se utilice el cifrado reversible; admite protocolos de aplicación que requieren el conocimiento de la contraseña del usuario para la autenticación. Las contraseñas almacenadas con cifrado reversible coinciden básicamente con las versiones de texto sin formato de las contraseñas. Por esta razón, esta configuración de directiva nunca se debe habilitar a menos que los requisitos de la aplicación tengan más peso que la necesidad de proteger la contraseña. El valor predeterminado de esta configuración de directiva es **Deshabilitado**.
  
Esta configuración de directiva debe estar habilitada cuando se utiliza el protocolo de autenticación por desafío mutuo (CHAP) a través del acceso remoto o el servicio de autenticación de Internet (IAS). También se requiere al utilizar la autenticación de texto implícita en los Servicios de Internet Information Server (IIS) de Microsoft.
  
Asegúrese de que la configuración **Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio** se establece como **Deshabilitada**, que es como se configura en el GPO predeterminado de dominio de Windows Server 2003 y en la directiva de seguridad local para estaciones de trabajo y servidores. Esta configuración de directiva también está **Deshabilitada** en los dos entornos que se definen en esta guía.
  
### Mecanismos para impedir que los usuarios cambien las contraseñas excepto cuando se les solicite
  
Además de las directivas de contraseñas descritas anteriormente en este capítulo, el control centralizado de todos los usuarios es un requisito para algunas organizaciones. En esta sección se describen los mecanismos para impedir que los usuarios puedan cambiar sus contraseñas excepto cuando se les requiera específicamente que lo hagan.
  
El control centralizado de las contraseñas de los usuarios es la piedra angular de cualquier esquema de seguridad de un sistema Windows XP bien diseñado. Puede emplear Directiva de grupo para establecer la vigencia mínima y máxima de las contraseñas, como se analizó anteriormente. Sin embargo, el hecho de que sea necesario cambiar frecuentemente las contraseñas puede dar lugar a que a los usuarios burlen la configuración **Forzar el historial de contraseñas** del entorno. El requisito de que las contraseñas sean demasiado largas también puede provocar más llamadas al servicio de asistencia por parte de usuarios que olviden sus contraseñas.
  
Los usuarios pueden cambiar sus contraseñas en el período entre la vigencia mínima y máxima de la contraseña. Sin embargo, el diseño para el entorno Seguridad especializada: Funcionalidad limitada requiere que los usuarios cambien sus contraseñas únicamente cuando el sistema operativo así lo solicite, después de que sus contraseñas hayan llegado a la vigencia máxima de 42 días. Para lograr este nivel de control, los administradores pueden deshabilitar el botón **Cambiar contraseña...** en el cuadro de diálogo **Seguridad de Windows** que aparece al presionar Ctrl+Alt+Supr.
  
Esta configuración se puede implementar en todo el dominio a través de Directiva de grupo o para uno o varios usuarios específicos mediante la edición del Registro. Para obtener información más detallada acerca de esta configuración, consulte el artículo 324744 de Microsoft Knowledge Base, "[Impedir que los usuarios cambien una contraseña excepto cuando se les pida en Windows Server 2003](http://support.microsoft.com/default.aspx?scid=324744)”, que está disponible en http://support.microsoft.com/default.aspx?scid=324744. Si tiene un dominio Windows 2000, consulte el artículo 309799 de Microsoft Knowledge Base, "[Impedir que los usuarios cambien una contraseña excepto cuando se les pida](http://support.microsoft.com/default.aspx?scid=309799)", en http://support.microsoft.com/default.aspx?scid=309799.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de bloqueo de cuentas
  
La directiva de bloqueo de cuentas es una característica de seguridad de Active Directory que bloquea las cuentas de usuario e impide el inicio de sesión después de un número determinado de intentos de inicio de sesión sin éxito dentro de un período especificado. Los controladores de dominio realizan un seguimiento de los intentos de inicio de sesión. El número de intentos permitidos y el período de tiempo se basan en los valores establecidos en la configuración del bloqueo de cuentas. La duración del bloqueo también se puede especificar.
  
Estas configuraciones de directiva ayudan a evitar que los atacantes puedan averiguar las contraseñas de los usuarios y reducen las probabilidades de ataques con éxito en el entorno de red. Sin embargo, es probable que la habilitación de una directiva de bloqueo de cuentas provoque más problemas de soporte para los usuarios de red. Antes de habilitar la configuración siguiente, asegúrese de que su organización desea aceptar esta carga de administración adicional. Para muchas organizaciones, una solución mejorada y menos costosa consiste en analizar los registros de eventos de seguridad para los controladores de dominio y generar alarmas administrativas cuando parezca que alguien intenta adivinar las contraseñas de cuentas de usuario.
  
Puede establecer la configuración de directiva de bloqueo de cuentas en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directiva de bloqueo de cuentas**
  
La tabla siguiente incluye las recomendaciones sobre la configuración de la directiva de bloqueo de cuentas para los dos entornos de seguridad que se definen en esta guía. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
**Tabla 2.2 Recomendaciones sobre la configuración de la directiva de bloqueo de cuentas**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Configuración</p></th>  
<th><p>Configuración predeterminada del controlador de dominio</p></th>  
<th><p>EC</p></th>  
<th><p>SSLF</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Duración del bloqueo de cuenta</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Umbral de bloqueos de la cuenta</p></td>
<td style="border:1px solid black;"><p>0 intentos de inicio de sesión incorrectos</p></td>
<td style="border:1px solid black;"><p>50 intentos de inicio de sesión no válidos</p></td>
<td style="border:1px solid black;"><p>10 intentos de inicio de sesión no válidos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Restablecer la cuenta de bloqueos después de</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
<td style="border:1px solid black;"><p>15 minutos</p></td>
</tr>  
</tbody>  
</table>
  
### Duración del bloqueo de cuenta
  
Esta configuración de directiva determina el tiempo que debe transcurrir antes de que una cuenta se bloquee y de que un usuario pueda volver a intentar iniciar sesión. Funciona especificando el número de minutos que permanece no disponible una cuenta bloqueada. Si el valor de esta configuración de directiva está establecido en 0, las cuentas permanecerán bloqueadas hasta que el administrador las desbloquee. El valor predeterminado de Windows XP para esta configuración de directiva es **No está definido**.
  
Para reducir el número de llamadas al servicio de asistencia y proporcionar una infraestructura segura, configure el valor de la configuración **Duración del bloqueo de cuenta** en **15** minutos para los entornos EC y SSLF que se definen en esta guía.
  
Aunque quizás parezca una buena idea configurar el valor de esta configuración de directiva de modo que nunca se desbloqueen las cuentas automáticamente, es probable que en ese caso se incremente el número de llamadas al servicio de asistencia para desbloquear cuentas bloqueadas por error. El valor de configuración recomendado de 15 minutos se consideró un tiempo razonable de espera de los usuarios antes de intentar iniciar sesión nuevamente en caso de bloqueo de la cuenta. Los usuarios también deben ser informados de cómo se configura esta directiva para que sepan que sólo tienen que llamar al personal de asistencia si necesitan recuperar urgentemente el acceso a su equipo.
  
### Umbral de bloqueos de la cuenta
  
Esta configuración de directiva determina el número de intentos de inicio de sesión que un usuario puede llevar a cabo antes de que se bloquee una cuenta. Los usuarios autorizados pueden bloquear sus propias cuentas en caso de no recordar su contraseña, escribirla incorrectamente o cambiarla en un equipo mientras han iniciado sesión en otro. El equipo con la contraseña incorrecta intentará repetidamente autenticar al usuario y, puesto que la contraseña utilizada es incorrecta, la cuenta del usuario terminará bloqueándose. Para evitar el bloqueo accidental de usuarios autorizados, establezca el umbral de bloqueos de la cuenta en un número alto. El valor predeterminado para esta configuración de directiva es de 0 intentos de inicio de sesión no válidos, con lo que se deshabilita la característica del bloqueo de cuentas.
  
Establezca el valor para la configuración del **Umbral de bloqueos de la cuenta** en **50** intentos de inicio de sesión no válidos para entornos EC y **10** para entornos SSLF.
  
Dado que un atacante puede utilizar este estado de bloqueo como una denegación de servicio (DoS) desencadenando un bloqueo que afecte a un gran número de cuentas, es aconsejable que la organización determine si debe utilizarse esta configuración de directiva, en función de las amenazas identificadas y de los riesgos que se desea evitar. Son dos las opciones que se deben considerar en el caso de esta configuración de directiva.
  
-   Establezca el valor de **Umbral de bloqueos de la cuenta** en **0** para asegurarse de que las cuentas no se bloquean. Este valor evitará los ataques DoS que intenten bloquear las cuentas de su organización. Se reducirán también las llamadas al servicio de asistencia, ya que los usuarios no podrán bloquear sus cuentas accidentalmente. Sin embargo, este valor de configuración no evitará un ataque de fuerza bruta. También deben considerarse las siguientes defensas:
  
    -   Una directiva de contraseñas que obligue a los usuarios a tener contraseñas complejas compuestas de 8 o más caracteres.
  
    -   Un mecanismo de auditoría eficaz para avisar a los administradores cuando se produzca una serie de bloqueos de cuentas en el entorno. Por ejemplo, la solución de auditoría debería supervisar el suceso de seguridad 539, que es un error de inicio de sesión. Este suceso significa que la cuenta se bloqueó en el momento en el que se intentó el inicio de sesión.
  
La segunda opción es la siguiente:
  
-   Configure el **Umbral de bloqueos de la cuenta** con un valor que proporcione a los usuarios la posibilidad de escribir incorrectamente su contraseña varias veces de forma accidental, pero que bloquee la cuenta si se produce un ataque de fuerza bruta. Un valor de configuración de 50 inicios de sesión no válidos para entornos EC y 10 para entornos de tipo SSLF podrían garantizar un nivel de seguridad adecuado y una capacidad de uso aceptable. Esta configuración evitará bloqueos accidentales y reducirá el número de llamadas al servicio de asistencia, pero no impedirá los ataques DoS, como se describía en la opción anterior.
  
### Restablecer la cuenta de bloqueos después de
  
Esta configuración de directiva determina el plazo de tiempo antes de que el **Umbral de bloqueos de la cuenta** se restablezca a cero. El valor predeterminado de esta configuración de directiva es **No está definido**. Si se define **Umbral de bloqueos de la cuenta**, este tiempo de restablecimiento debe ser inferior o igual al valor de **Duración del bloqueo de cuenta**.
  
Establezca el valor de la configuración **Restablecer la cuenta de bloqueos después de** en **15** minutos para los entornos EC y SSLF que se definen en esta guía.
  
Si deja el valor predeterminado para esta configuración de directiva o configura el valor con un intervalo demasiado largo, su entorno podría ser vulnerable a un ataque de DoS. Un atacante podría realizar una serie de intentos de inicio de sesión malintencionados en todas las cuentas de usuario de la organización y bloquearlas, como se describió anteriormente en este capítulo. Si no se determina ninguna directiva para restablecer el bloqueo, los administrados deberían desbloquear manualmente todas las cuentas. Por el contrario, si se establece un valor de tiempo razonable para esta configuración de directiva, los usuarios no tendrán acceso durante un período de tiempo establecido hasta que todas las cuentas se desbloqueen automáticamente. El valor de configuración recomendado de 15 minutos se consideró un tiempo razonable que es probable que acepten los usuarios y que ayudará a reducir al mínimo el número de llamadas al servicio de asistencia técnica. Los usuarios también deben ser informados de cómo se configura esta directiva para que sepan que sólo tienen que llamar al personal de asistencia si necesitan recuperar urgentemente el acceso a su equipo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Asignación de derechos de usuario
  
Los derechos de usuario se describen en detalle en el capítulo 3, "Configuración de seguridad para clientes Windows XP". Sin embargo, el derecho de usuario **Agregar estaciones de trabajo al dominio** debe asignarse a todos controladores de dominio, por lo que se trata en este capítulo. Puede encontrar información adicional acerca de las configuraciones de servidores miembros y controladores de dominio en los capítulos 4 y 5 de la *Guía de seguridad* de *Windows* *Server 2003*.
  
### Agregar estaciones de trabajo al dominio
  
Esta configuración de directiva permite al usuario agregar un equipo a un dominio específico.
  
**Tabla 2.3 Recomendaciones sobre la configuración de asignaciones de derechos de usuario**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Configuración</p></th>  
<th><p>Configuración predeterminada del controlador de dominio</p></th>  
<th><p>EC</p></th>  
<th><p>SSLF</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Agregar estaciones de trabajo al dominio</p></td>
<td style="border:1px solid black;"><p>Usuarios autenticados</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Administradores</p></td>
</tr>  
</tbody>  
</table>
  
Para que la configuración **Agregar estaciones de trabajo al dominio** surta efecto, debe asignarse al usuario en un GPO que se aplique a todos los controladores del dominio. Un usuario al que se haya asignado este derecho puede agregar hasta 10 estaciones de trabajo al dominio. Los usuarios a los que se asigna el permiso **Crear objetos de equipo** para una UO o el contenedor Equipos en Active Directory también pueden unir un equipo a un dominio y agregar un número ilimitado de equipos a éste, independientemente de si se les ha asignado o no el derecho de usuario **Agregar estaciones de trabajo al dominio**.
  
De forma predeterminada, todos los usuarios del grupo **Usuarios autenticados** pueden agregar hasta 10 cuentas de equipo a un dominio Active Directory. Estas nuevas cuentas de equipo se crean en el contenedor Equipos.
  
En un dominio Active Directory, cada cuenta de equipo es una entidad de seguridad principal con capacidad para autenticar y obtener acceso a los recursos. Algunas organizaciones optan por limitar el número de equipos en el entorno de Active Directory para poder realizar un seguimiento de los mismos, crearlos y administrarlos de forma coherente. Estas tareas de administración pueden verse dificultadas si se permite a los usuarios agregar estaciones de trabajo al dominio. Asimismo, este derecho de usuario proporciona a los usuarios un medio de llevar a cabo actividades cuyo seguimiento es más difícil, porque pueden crearse en el dominio equipos adicionales no autorizados.
  
Por todas estas razones, el derecho de usuario **Agregar estaciones de trabajo al dominio** sólo se debe asignar al grupo **Administradores** en los dos entornos que se definen en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Opciones de seguridad
  
Debe definirse una directiva de cuentas en un GPO que se vincule en el nivel de dominio, como en el caso de las configuraciones de directiva en la Directiva de dominio predeterminada. Los controladores de dominio siempre obtienen la directiva de cuentas de los GPO del nivel de dominio, incluso si hay una directiva de cuentas establecida en un GPO que se aplique a la UO que contiene el controlador de dominio.
  
En el nivel de dominio deben considerarse tres configuraciones de opciones de seguridad similares a directivas de cuentas. Puede establecer estas configuraciones de opciones de seguridad en la siguiente ubicación en el Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Seguridad\\Opciones**
  
En la siguiente tabla se resumen las recomendaciones acerca de la configuración de las opciones de seguridad para los dos tipos de entornos seguros que se definen en esta guía. En las siguientes subsecciones se proporciona información más detallada acerca de cada una de las configuraciones.
  
**Tabla 2.4 Recomendaciones sobre la configuración de las opciones de seguridad**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Configuración</p></th>  
<th><p>Predeterminada de miembro de dominio</p></th>  
<th><p>EC</p></th>  
<th><p>SSLF</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso de red: permitir traducción SID/nombre anónima</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
### Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión
  
Esta configuración de directiva determina si se desconectará a los usuarios que están conectados a la red local fuera de las horas de inicio de sesión válidas para sus cuentas de usuario. Esta configuración de directiva afecta al componente Bloques de mensajes de servidor (SMB). Cuando esta configuración de directiva está habilitada, las sesiones del equipo cliente con el servicio SMB se desconectan una vez transcurrido el tiempo de sesión válido del cliente. Cuando está deshabilitada, se permite que continúe la sesión del equipo cliente establecida después de transcurrido el tiempo de sesión. Al habilitar esta configuración de directiva, asegúrese de que también está habilitado el parámetro **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión**.
  
**Nota:  **el bloque de mensajes del servidor es la base para los recursos compartidos en las redes Windows. Por lo tanto, las configuraciones que afectan a SMB también afectan a los recursos compartidos, como carpetas e impresoras.
  
Si en su organización se han configurado horas de inicio de sesión para los usuarios, es razonable habilitar la configuración **Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión**. De lo contrario, los usuarios que se supone que no pueden tener acceso a los recursos de la red fuera de las horas de sesión que les corresponden podrían continuar utilizando los recursos en sesiones iniciadas durante las horas permitidas.
  
Si no se utilizan horas de inicio de sesión en la organización, esta configuración de directiva no surtirá efecto aunque esté habilitada. Si, por el contrario, sí que se utilizan horas de inicio de sesión, las sesiones de los usuarios se darán por terminadas en cuanto transcurra el tiempo de sesión correspondiente.
  
### Acceso de red: permitir traducción SID/nombre anónima
  
La configuración **Acceso de red: permitir traducción SID/nombre anónima** determina si un usuario anónimo puede solicitar el SID de otro. Si se habilita esta configuración de directiva en un controlador de dominio, un usuario que conozca los atributos de SID de un administrador podría ponerse en contacto con un equipo que también tuviera esta configuración de directiva habilitada y utilizar dicho SID para obtener la información de la cuenta del administrador. Esa persona podría entonces utilizar la cuenta para iniciar un ataque de contraseña. La configuración predeterminada en *equipos miembros* es **Deshabilitada**. Sin embargo, la configuración predeterminada para los *controladores de dominio* es **Habilitada**. Si esta configuración de directiva está deshabilitada, los sistemas siguientes pueden no ser capaces de comunicarse con dominios basados en Windows Server 2003:
  
-   Servidores de servicio de acceso remoto (RAS) basados en Microsoft Windows NT® 4.0.
  
-   Equipos basados en servidores de servicio de acceso remoto Windows 2000 ubicados en dominios Windows NT 3.*x* o Windows NT 4.0.
  
-   Microsoft SQL Server en equipos Windows NT 3.*X*o Windows NT 4.0.
  
-   SQL Server en equipos Windows 2000 ubicados en dominios Windows NT 3.*x* o en dominios Windows NT 4.0.
  
-   Usuarios del recurso de dominios Windows NT 4.0 que desean asignar permisos para el acceso a archivos, carpetas compartidas y objetos del Registro a cuentas de usuario de dominios de cuentas que contienen controladores de dominio Windows Server 2003.
  
### Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión
  
El uso del valor **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión** determina si se desconecta a los usuarios conectados a la red local fuera de las horas válidas de inicio de sesión de la cuenta del usuario. Esta configuración de directiva afecta al componente SMB.
  
Si habilita esta configuración de directiva, se desconectarán las sesiones de equipo cliente con el servidor SMB cuando hayan transcurrido las horas de inicio de sesión. Los usuarios no podrán iniciar sesión en el sistema hasta la siguiente hora de acceso permitido. Si deshabilita esta configuración de directiva, las sesiones de equipo cliente establecidas se mantendrán después de que transcurran las horas de inicio de sesión del usuario. Para que afecte a las cuentas de dominio, esta configuración de directiva debe definirse en un GPO que esté vinculado a la raíz del dominio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva Kerberos
  
La directiva del protocolo de autenticación de la versión 5 de Kerberos se configura en los controladores de dominio, no en los equipos miembros del dominio. Esta directiva determina la configuración relacionada con el protocolo Kerberos, la obligatoriedad y la vigencia máxima de los vales de servicio. La configuración Kerberos no existe en la directiva de equipo local. En la mayoría de los entornos, los valores predeterminados de esta configuración no se deben cambiar. Tampoco se proporcionan cambios para la directiva predeterminada Kerberos. Para obtener más información acerca de estos parámetros, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de grupo del nivel de unidad organizativa
  
La configuración de seguridad incluida en la directiva de grupo de nivel de unidad organizativa debe ser específica de la unidad. Esta configuración incluye tanto parámetros de equipo como de usuario. Para facilitar la administración y mejorar la seguridad, la sección que trata sobre la directiva de restricción de software (SRP) se presenta de forma separada del resto de configuraciones de seguridad en esta guía. El capítulo 6, "Directiva de restricción de software para clientes Windows XP", proporciona información detallada acerca de SRP.
  
### Configuración de seguridad de Directiva de grupo
  
Deberá crear un GPO para cada categoría de equipos Windows XP del entorno. Los equipos portátiles y de escritorio se dividen en unidades organizativas independientes en esta guía para aplicar GPO personalizados a cada una de las categorías de equipos.
  
### Configuración de la directiva de restricción de software
  
Cree GPO dedicados para establecer la configuración de SRP en el entorno. Existen razones de peso para mantener la configuración de SRP separada de los restantes parámetros de Directiva de grupo. Una de las razones es que SRP es conceptualmente diferente de otras configuraciones de Directiva de grupo. Las opciones no se habilitan ni deshabilitan, y no se configuran valores. En cambio, SRP requiere que los administradores identifiquen el conjunto de aplicaciones compatibles, las restricciones que se aplicarán y cómo se tratarán las excepciones. Otra razón es facilitar una recuperación rápida si se produce un error catastrófico cuando se implementan directivas de SRP en el entorno de producción: los administradores pueden deshabilitar temporalmente los GPO en los que se define la configuración de SRP sin que se vean afectados los restantes parámetros de seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Herramientas de directivas de grupos
  
Hay varias herramientas incluidas con Windows XP que facilitan el trabajo con los GPO. En esta sección se ofrece una breve descripción de esas herramientas. Para obtener más información sobre las mismas, consulte la Ayuda en pantalla de Windows XP.
  
### Obligatoriedad de la actualización de Directiva de grupo
  
Aunque Active Directory actualiza Directiva de grupo de forma periódica, puede forzar a que la versión de su equipo cliente se actualice mediante Gpupdate, una herramienta de línea de comandos que se facilita con Windows XP Professional. Esta herramienta se debe ejecutar de forma local en los equipos cliente.
  
Para actualizar un equipo local con esta herramienta, ejecute lo siguiente en el símbolo del sistema:
  
```  
gpupdate /force  
```  
Después de ejecutar Gpupdate, se mostrará la siguiente información de confirmación:
  
```  
C:\\Documents and Settings\\administrator.MSSLAB&gt;gpupdate /force Refreshing Policy... User Policy Refresh has completed. Computer Policy Refresh has completed. To check for errors in policy processing, review the event log. C:\\Documents and Settings\\administrator.MSSLAB&gt;  
```  
En caso de que la directiva de grupo esté basada en usuarios, deberá cerrar sesión y volver a iniciarla en el equipo que utiliza para probar las directivas. Las directivas de equipo se deberían actualizar inmediatamente.
  
Para ver opciones adicionales de Gpupdate, ejecute lo siguiente en el símbolo del sistema:
  
```  
gpupdate /?  
```  
### Visualización del conjunto resultante de directivas
  
Existen dos herramientas que se proporcionan con Windows XP y que permiten determinar qué directivas se han aplicado a los equipos del entorno, cuándo se han aplicado y en qué orden.
  
-   **Complemento RSoP**. RSoP.msc es una herramienta de complemento de MMC que muestra la configuración adicional que se ha aplicado a un equipo. Esta herramienta se puede ejecutar de forma local o remota desde otro equipo. En cada configuración de directiva, la herramienta RSoP muestra la configuración del equipo y el GPO de origen.
  
-   **Gpresult**. Es una herramienta de línea de comandos que ofrece estadísticas sobre cuándo se aplicó más recientemente Directiva de grupo a un equipo, qué GPO se aplicaron al mismo y en qué orden. Esta herramienta también proporciona información acerca de cualquier GPO que se haya aplicado mediante filtrado. Gpresult se puede utilizar de forma remota o local en los equipos cliente.
  
### Consola de administración de directivas de grupo
  
La Consola de administración de directivas de grupo (GPMC) es un complemento de MMC que está disponible como componente opcional con Windows Server 2003 Service Pack 1. Se utiliza para administrar todas las tareas relacionadas con Directiva de grupo. GPMC ayuda a planear, preparar, implementar, generar informes, crear secuencias de comandos y solucionar problemas en relación con la aplicación de GPO. Si desea más información, visite el sitio de [GPMC](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx) en www.microsoft.com/windowsserver2003/gpmc/default.msp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Directiva de grupo es una característica basada en Active Directory que permite controlar los entornos informáticos de usuarios y equipos en dominios Windows Server 2003 y Windows 2000. Antes de aplicarla a equipos de escritorio Windows XP es preciso seguir ciertos pasos previos en el dominio.
  
La configuración de Directiva de grupo almacenada en los objetos de directiva de grupo (GPO) de los controladores de dominio del entorno se vinculan a sitios, dominios y unidades organizativas que residen en la estructura de Active Directory. Es importante conocer la estructura de Active Directory y las implicaciones de seguridad que supone configurar distintas opciones de diseño dentro de la misma antes de implementar Directiva de grupo.
  
Esta directiva constituye una herramienta esencial para garantizar la seguridad de Windows XP. En este capítulo se incluían detalles acerca de cómo utilizar Directiva de grupo para aplicar y mantener una directiva de seguridad coherente en la red desde una ubicación central.
  
También proporciona información acerca de los distintos niveles de Directiva de grupo y las herramientas especiales que se pueden emplear para actualizarla en su entorno.
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.
  
-   Para obtener más información acerca del diseño y la administración de Active Directory, consulte las notas del producto "[Design Considerations for Delegation of Administration in Active Directory](http://technet.microsoft.com/en-us/library/bb727032.aspx)" en www.microsoft.com/technet/prodtechnol/ad/windows2000/plan/addeladm.asp.
  
-   Para obtener más información acerca del diseño de Active Directory, consulte las notas del producto "[Best Practice Active Directory Design for Managing Windows Networks](http://technet.microsoft.com/en-us/library/bb727032.aspx)" en www.microsoft.com/technet/prodtechnol/ad/windows2000/plan/bpaddsgn.asp.
  
-   Para obtener más información acerca de Directiva de grupo, consulte las notas del producto "[Step-by-Step Guide to Understanding the Group Policy Feature Set](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/stepbystep/gpfeat.mspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/  
    /stepbystep/gpfeat. mspx.  
    Consulte también la página principal de [Directiva de grupo](http://www.microsoft.com/windowsserver2003/technologies/management/grouppolicy/default.mspx) de Windows Server 2003 en www.microsoft.com/windowsserver2003/technologies/management/grouppolicy/default.mspx
  
-   Para obtener más información acerca de la seguridad de Windows XP, consulte la [documentación del kit de recursos de Microsoft Windows XP Professional](http://www.microsoft.com/windowsxp/pro/techinfo/productdoc/resourcekit.asp) en www.microsoft.com/WindowsXP/pro/techinfo/productdoc/resourcekit.asp.
  
-   Si desea obtener información general acerca de las características de seguridad para Windows XP, consulte las notas del producto "[What's New in Security for Windows XP Professional and Windows XP Home Edition](http://www.microsoft.com/technet/prodtechnol/winxppro/evaluate/xpsec.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/evaluate/xpsec.asp.
  
-   Para obtener más información acerca de las plantillas administrativas, consulte las notas del producto "[Implementing Registry-Based Group Policy](http://www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp)" en www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp.
  
-   Para obtener más información acerca de la Consola de administración de directivas de grupo (GPMC), consulte el sitio de [GPMC](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx) en http://www.microsoft.com/windowsserver2003/gpmc/default.mspx.
  
-   Para obtener información adicional acerca de la herramienta de actualización de Directiva de grupo ([Gpupdate](http://www.microsoft.com/technet/prodtechnol/winxppro/proddocs/refrgp.mspx)), consulte www.microsoft.com/technet/prodtechnol/winxppro/proddocs/refrGP.asp.
  
-   Para obtener información adicional acerca de la herramienta [Conjunto resultante de directivas](http://www.microsoft.com/technet/prodtechnol/winxppro/proddocs/rspintro.mspx) (RSoP), consulte www.microsoft.com/technet/prodtechnol/winxppro/proddocs/RSPintro.asp.
  
-   Para obtener más información acerca de la herramienta Resultados de directiva de grupo ([Gpupdate](http://www.microsoft.com/technet/prodtechnol/winxppro/proddocs/gpresult.mspx)), consulte www.microsoft.com/technet/prodtechnol/winxppro/proddocs/refrGP.asp.
  
-   Para obtener más información acerca de cómo delegar la autoridad en Active Directory, consulte la sección de los *kits de recursos de Windows 2000* relativa al planeamiento de la [Seguridad distribuida](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/distrib/dsca_pt3_stbp.asp) en www.microsoft.com/resources/documentation/Windows/2000/server/reskit/en-us/distrib/  
    dsca\_pt3\_stbp.asp.
  
### Descargar
  
![](images/Cc163071.icon_exe(es-es,TechNet.10).gif)[Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
  
[](#mainsection)[Principio de la página](#mainsection)
