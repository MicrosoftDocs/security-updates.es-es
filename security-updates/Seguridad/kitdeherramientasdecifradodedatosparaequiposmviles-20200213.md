---
TOCTitle: Kit de herramientas de cifrado de datos para equipos móviles
Title: Kit de herramientas de cifrado de datos para equipos móviles
ms:assetid: 'a69e5f04-8f25-43a6-86b9-e8279021d108'
ms:contentKeyID: 20200213
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162812(v=TechNet.10)'
---

Kit de herramientas de cifrado de datos para equipos móviles: guía de implementación y planeación
=================================================================================================

### Capítulo 2: tareas de configuración e implementación

Publicado: 29-05-2007

Antes de empezar a implementar el Cifrado de unidad BitLocker™ de Microsoft® (BitLocker) y el Sistema de cifrado de archivos (EFS), debe realizar una serie de tareas preliminares de configuración para preparar el entorno. Las tareas que se describen en este capítulo le ayudarán a preparar el servicio de directorio de Active Directory® y su red, así como a implementar BitLocker y EFS en los equipos cliente.

EFS y BitLocker se benefician de Active Directory, que se puede usar para aplicar parámetros de configuración coherentes a varios equipos. Los parámetros disponibles para cada tecnología son algo diferentes entre sí. Sin embargo, puesto que los objetos de directiva de grupo (GPO) de Active Directory pueden controlar ambas tecnologías, debe considerar la forma de aprovechar el diseño de Active Directory para aplicar la protección apropiada a los equipos en función de la ubicación, la función o el usuario.

En este capítulo, se describen las siguientes tareas:

-   Selección de una configuración de BitLocker para proteger la información confidencial

-   Uso de los controles de directiva de grupo de Active Directory para controlar el funcionamiento en BitLocker de la copia de seguridad de claves, la instalación, el cifrado de discos y la interacción del Módulo de plataforma segura (TPM)

-   Uso de Active Directory para controlar el cifrado EFS y la administración de certificados

-   Preparación de los equipos cliente para usar BitLocker en la configuración seleccionada

-   Habilitación de BitLocker en equipos cliente

-   Configuración del Asistente para sistemas de cifrado de archivos (Asistente para EFS) de Microsoft para su uso con EFS en equipos vinculados a su dominio

-   Importación de plantillas administrativas para personalizar las herramientas de administración disponibles para EFS

-   Configuración de agentes de recuperación de datos para EFS

##### En esta página

[](#edae)[Tareas de preparación de infraestructura](#edae)
[](#ecae)[Tareas de configuración por equipo](#ecae)
[](#ebae)[Más información](#ebae)

### Tareas de preparación de infraestructura

BitLocker y EFS necesitan que se prepare la infraestructura antes de poder implementarlos en su entorno. Las tareas descritas en esta sección normalmente se deben realizar una vez antes de la primera implementación y no se suelen tener que repetir.

#### Preparación de infraestructura para BitLocker

La preparación de la infraestructura de BitLocker precisa dos pasos:

-   Configuración de las opciones de BitLocker a través de la directiva de grupo de Active Directory

-   Preparación de la infraestructura de Active Directory para permitir el almacenamiento de las claves de recuperación de BitLocker

##### Configuración de opciones de BitLocker mediante directivas de grupo

Windows Vista™ ofrece una serie de parámetros de control de BitLocker que puede usar para controlar la disponibilidad y el comportamiento de BitLocker en los equipos cliente. Puede controlar dichos parámetros mediante la creación de objetos de directiva de grupo de Active Directory con el conjunto de herramientas estándar para administración de GPO de Windows Server® y las plantillas de administración de Windows Vista. Para obtener más información acerca de estas herramientas, consulte la Ayuda en línea de Windows Server 2003.

Puesto que los objetos de directiva de grupo se pueden aplicar a equipos individuales o a sitios, dominios y unidades organizativas de Active Directory, cuenta con una gran flexibilidad a la hora de decidir la forma de asignar parámetros de BitLocker a los equipos de su organización. Puede:

-   asignar una configuración a equipos individuales mediante la modificación del GPO de los equipos locales.

-   agrupar equipos con funciones similares en una unidad organizativa y, a continuación, asignar una única configuración de BitLocker solo a dicha unidad. Por ejemplo, puede crear una unidad organizativa aparte para todos los equipos móviles o solo para los equipos móviles que pertenezcan a empleados de determinadas unidades de negocio o con determinadas funciones laborales.

-   aplicar de forma general las directivas de BitLocker a todos los equipos de un dominio o un bosque. Este enfoque facilita la implementación directa del cifrado en los equipos con Windows Vista de toda la compañía. Los equipos que ejecutan otras versiones de Windows prescindirán de la configuración específica de BitLocker.

##### Preparación para almacenamiento de claves de Active Directory

Para habilitar el almacenamiento de contraseñas de propietario de TPM y los datos de recuperación de volúmenes de BitLocker en Active Directory, debe realizar los pasos descritos a continuación. Para realizar estos pasos, es necesario que todos los controladores de dominio a los que tienen acceso los clientes de BitLocker ejecuten Windows Server 2003 Service Pack 1 (SP1) o posterior.

1.  Ampliar el esquema de Active Directory.

2.  Establecer los permisos en los objetos de esquema de información de recuperación de BitLocker y TPM.

3.  Configurar un GPO para habilitar la copia de seguridad de Active Directory con la información de claves de BitLocker.

4.  Configurar un GPO para habilitar la copia de seguridad de Active Directory con la información de contraseñas de propietario de TPM.

En la guía de [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=67438), se describe el procedimiento detallado para la ejecución de estos pasos.

Después de realizar los pasos anteriores, puede delegar el acceso de recuperación en otras personas de la organización.

**Para delegar el acceso de recuperación**

1.  Cree o identifique un grupo de seguridad de Active Directory que contenga las cuentas de usuario en las que desee delegar el acceso.

2.  Agregue una entrada de control de acceso (ACE) a la lista de control de acceso discrecional (DACL) para el dominio o la unidad organizativa que contiene los equipos en los que desea delegar el acceso. La ACE debe otorgar los permisos “control de acceso” y “propiedad de lectura” al objeto de información de recuperación de BitLocker, al paquete de claves y al objeto de equipo.

3.  Para habilitar la recuperación de la información de TPM, puede usar el mismo método para otorgar “control de acceso” y “propiedad de lectura” al objeto de información de propietario de TPM.

Como parte del proceso, es posible que desee otorgar acceso a la información de recuperación de TPM y de BitLocker a dos grupos de usuarios distintos. Este enfoque ayuda a mantener una separación de las obligaciones para obtener acceso a la información de recuperación.

#### Preparación de infraestructura para EFS

Para usar EFS eficazmente, debe realizar las siguientes tareas de preparación de infraestructura:

1.  Preparar Active Directory y crear objetos de directiva de grupo

2.  Administrar y configurar los agentes de recuperación de datos

3.  Administrar y configurar agentes Key Recovery Agent

##### Preparación de Active Directory y creación de objetos de directiva de grupo

En esta sección de la guía, se describen las tareas de configuración necesarias para preparar el entorno de Active Directory con objeto de ser compatible con EFS. Si no realiza estas tareas, es posible que los equipos cliente individuales que ejecutan Windows XP o Windows Vista puedan usar EFS, pero no podrán administrar de forma centralizada ni controlar la funcionalidad de EFS.

###### Control de la configuración de cifrado EFS

Windows Vista y Windows XP ofrecen una serie de parámetros que puede usar para controlar la disponibilidad y el comportamiento de EFS en los equipos cliente. Puede controlar estos parámetros mediante la creación de objetos de directiva de grupo de Active Directory con el conjunto de herramientas de administración estándar de GPO de Windows Server. Para obtener más información acerca de estas herramientas, consulte la Ayuda en línea de Windows Server 2003.

Puesto que los objetos de directiva de grupo se pueden aplicar a equipos individuales o a sitios, dominios y unidades organizativas de Active Directory, cuenta con una gran flexibilidad a la hora de decidir la forma de asignar parámetros de EFS a los equipos de su organización. Puede:

-   asignar una configuración a equipos individuales mediante la modificación del GPO de los equipos locales.

-   agrupar equipos con funciones similares en una unidad organizativa y, a continuación, asignar una única configuración de EFS solo a dicha unidad. Por ejemplo, puede crear una unidad organizativa aparte para todos los equipos móviles o solo para los equipos móviles que pertenezcan a empleados de determinadas unidades de negocio o con determinadas funciones laborales.

-   aplicar de forma general las directivas de EFS a todos los equipos de un dominio o un bosque. Este enfoque se puede aplicar junto con el Asistente para EFS con objeto de ofrecer una implementación directa del cifrado para toda la compañía en los equipos con Windows XP y Windows Vista.

###### Parámetros de EFS comunes de Windows Vista y Windows XP

La plantilla de GPO de Active Directory permite controlar una serie de parámetros relacionados con el sistema EFS, que se enumeran y describen en la siguiente tabla. Para obtener más información, consulte las guías de seguridad de Windows XP y Windows Vista.

**Tabla 2.1. Configuración relacionada con EFS de las plantillas de GPO de Active Directory**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de parámetro</p></th>
<th><p>Disponibilidad</p></th>
<th><p>Opción predeterminada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Habilitar EFS</p></td>
<td style="border:1px solid black;"><p>Windows XP, Windows Vista</p></td>
<td style="border:1px solid black;"><p>Permitir</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cifrar documentos</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Requerir tarjeta inteligente</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Crear claves de usuario con capacidad de almacenamiento en caché desde la tarjeta inteligente</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Habilitar cifrado de archivo de paginación</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inscripción automática de certificados</p></td>
<td style="border:1px solid black;"><p>Windows XP, Windows Vista</p></td>
<td style="border:1px solid black;"><p>Activado</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Tamaño de clave para certificados autofirmados</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>2048 bits</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Plantilla de EFS para solicitudes automáticas de certificados</p></td>
<td style="border:1px solid black;"><p>Windows Vista</p></td>
<td style="border:1px solid black;"><p>Ninguna</p></td>
</tr>  
</tbody>  
</table>
  
**Habilitación y deshabilitación de EFS**
  
Dado el alto riesgo de pérdida de claves (y, por tanto, de pérdida de acceso a los archivos cifrados) con un sistema EFS independiente, algunas organizaciones deciden deshabilitar EFS hasta que sea posible implementar una entidad de certificación (CA) de la empresa y un sistema EFS basado en dominios. Puede habilitar o deshabilitar el uso de EFS mediante el cambio de estado de la casilla **Permitir a usuarios cifrar archivos utilizando el Sistema de archivos cifrados (EFS)** situada en las propiedades del objeto del Sistema de cifrado de archivos de un GPO. El objeto del Sistema de cifrado de archivos está situado en la siguiente ruta de acceso: **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas**.
  
En caso de que su organización haya deshabilitado previamente EFS mediante un GPO, deberá modificar ahora el GPO para habilitar EFS. Si deshabilitó EFS mediante directivas locales o cambios en el Registro, ahora deberá quitar las directivas locales o usar el editor del Registro para habilitar EFS. Para habilitar EFS a través del Registro, busque un valor DWORD denominado **EfsConfiguration** en el Registro, dentro de la clave **HKLM\\SOFTWARE\\Microsoft\\WindowsNT\\CurrentVersion\\EFS**. Para deshabilitar EFS, cambie el valor a 1. Para habilitarlo, cambie el valor a 0. Tenga en cuenta que este cambio solo se aplica al equipo local, no a los demás equipos del dominio.
  
**Compatibilidad con algoritmos de cifrado adicionales**
  
Si durante la fase de planeación decide que la implementación de EFS cumpla la Norma federal de procesamiento de información (FIPS) 140-1, deberá habilitar la norma FIPS cambiando la opción **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** en la directiva local o de grupos de Active Directory. Esta opción se encuentra en la siguiente ruta de acceso: **Configuración de equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad**.
  
Si se debe usar otro algoritmo de cifrado (por una razón que no sea el cumplimiento de la norma FIPS), se deberá usar la directiva de grupo para modificar **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\EFS** en los equipos cliente necesarios.
  
###### Opciones de EFS específicas de Windows Vista
  
Windows Vista incluye varias opciones nuevas de directiva de grupo para ayudar a los administradores a definir e implementar directivas organizativas para EFS. Estas opciones, que se muestran en la siguiente figura, ofrecen la capacidad de exigir tarjetas inteligentes para EFS y cifrado de archivos de paginación, determinar la longitud mínima de claves para EFS y requerir el cifrado de la carpeta Documentos del usuario. Para tener acceso a estas opciones, debe editar el objeto del Sistema de cifrado de archivos de un GPO (situado en la siguiente ruta: **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas**).
  
![](images/Cc162812.1a71105c-d527-4302-a6e6-db91d08078a4(es-es,TechNet.10).gif)
  
**Figura 2.1. Opciones de las propiedades del Sistema de cifrado de archivos en Windows Vista**
  
###### Control de la inscripción automática de certificados
  
Windows XP Professional y Windows Vista permiten que los usuarios se inscriban automáticamente en los certificados de usuario al iniciar sesión. La inscripción automática para los certificados de usuario es rápida y sencilla, además de habilitar aplicaciones de infraestructura de claves públicas (PKI), como inicio de sesión de tarjeta inteligente, EFS, SSL, S/MIME, entre otras, dentro del entorno de Active Directory. La inscripción automática del usuario reduce el alto costo de las implementaciones típicas de PKI. Para habilitar la inscripción automática de certificados, debe crear una plantilla de certificados pertinente en Active Directory. Use el complemento Microsoft Management Console (MMC) Plantillas de certificado con objeto de agregar una plantilla de certificado apropiada. Para obtener más información, consulte el artículo [Inscripción automática de certificados en Windows XP](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/certenrl.mspx).
  
##### Administración y configuración de los agentes de recuperación de datos
  
Microsoft recomienda que su organización defina al menos un Agente de recuperación de datos (DRA) para su uso con EFS. Los agentes de recuperación de datos pueden ser cuentas de administradores de red normales, pero Microsoft recomienda el uso de cuentas dedicadas exclusivamente a actividades de recuperación. La directiva o los requisitos legales de la organización pueden definir requisitos adicionales, incluidos de auditoría o de separación de acceso. El cumplimiento de estos requisitos puede implicar la definición de distintos agentes de recuperación de datos para distintos grupos, organizaciones, funciones laborales u otras subdivisiones de la red corporativa.
  
La administración de DRA incluye las siguientes tareas, que se describen detalladamente en las siguientes subsecciones:
  
-   Crear las cuentas de usuario de DRA
  
-   Crear y rellenar grupos de seguridad para DRA
  
-   Configurar la CA para emitir certificados de DRA
  
-   Solicitar certificados de DRA
  
-   Aprobar las solicitudes de certificado de DRA para EFS
  
-   Definir una directiva de recuperación de datos (paso de planeación descrito en el primer capítulo)
  
-   Exportar certificados para su asignación a una directiva
  
-   Definir un agente de recuperación de datos
  
###### Creación de cuentas de usuario de DRA
  
El procedimiento recomendado para la administración de cuentas de usuario de DRA es la creación de cuentas de usuario independientes que solo se usen para la recuperación de datos, ya que este enfoque facilita la reducción del riesgo que supone que un usuario privilegiado recupere los datos de forma incorrecta. Las cuentas de usuario de DRA dedicadas comienzan como cuentas normales a las que asigna privilegios de recuperación.
  
**Para crear cuentas de usuario de DRA**
  
1.  Abra Usuarios y equipos de Active Directory.
  
2.  En el árbol de la consola, haga clic con el botón secundario en la carpeta en la que desea agregar una cuenta de usuario. (Usuarios y equipos de Active Directory/nodo de dominio/carpeta)
  
3.  Seleccione **Nueva** y, a continuación, haga clic en **Usuario**.
  
4.  Asigne un nombre a la cuenta. En lugar de usar un nombre de usuario individual, debe identificar la cuenta mediante la función (por ejemplo, DRA de RR. HH. o DRA de ingeniería).
  
5.  En **Nombre de inicio de sesión de usuario**, escriba dicho nombre, haga clic en el sufijo UPN de la lista desplegable y, a continuación, haga clic en **Siguiente**.
  
6.  En **Contraseña y Confirmar contraseña**, escriba la contraseña de usuario y, a continuación, seleccione las opciones de contraseña correspondientes.
  
7.  Haga clic en **Aceptar**.
  
8.  Repita los pasos 3-7 para cada DRA que desee crear.
  
###### Creación de grupos de seguridad para agentes de recuperación de datos
  
Microsoft aconseja la creación de un grupo de seguridad de Active Directory para cada grupo de agentes DRA que desee usar. Este enfoque permite controlar con eficacia los usuarios que tienen acceso a la recuperación de datos desde los distintos departamentos de la organización.
  
**Para crear grupos de seguridad para los agentes de recuperación de datos**
  
1.  Abra Usuarios y equipos de Active Directory.
  
2.  Haga clic con el botón secundario en **Usuarios**, haga clic en **Nuevo**, en **Grupo**, escriba **Agentes de recuperación de datos** (u otro nombre adecuado) y, a continuación, haga clic en **Aceptar**.
  
3.  Para agregar usuarios a dicho grupo, haga clic con el botón secundario en **Agentes de recuperación de datos** en la unidad organizativa **Usuarios**, haga clic en **Propiedades** y, a continuación, en la ficha **Miembros**. Seleccione los usuarios que desea agregar a este grupo y haga clic en **Aceptar**.
  
4.  Repita los pasos 2 y 3 para cada grupo de DRA adicional.
  
###### Configuración de la entidad de certificación para emitir certificados de DRA
  
Debe configurar la entidad de certificación para emitir certificados mediante una plantilla que incluya marcadores de uso de claves para la recuperación de EFS. En los siguientes pasos, se describe la forma de configurar los Servicios de Certificate Server de Microsoft para emitir certificados digitales de DRA para EFS. Puede usar otras entidades de certificación compatibles para emitir certificados de DRA para EFS, pero en esta guía no se proporcionan instrucciones para los servicios de CA de terceros.
  
**Para configurar los Servicios de Certificate Server con objeto de emitir certificados de recuperación de EFS**
  
1.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.
  
2.  Abra la consola Entidad de certificación centrándose en un servidor autorizado de los Servicios de Certificate Server. Para ello, haga clic en **Inicio**, **Todos los programas**, **Herramientas administrativas** y, a continuación, seleccione **Entidad de certificación**.
  
3.  Expanda el objeto del servidor Entidad de certificación para ver todos sus componentes.
  
4.  Haga clic con el botón secundario en el nodo **Plantillas de certificado** y seleccione **Administrar** para abrir la consola Plantilla de certificados, como se muestra en la siguiente figura.
  
    ![](images/Cc162812.5d9e236e-785e-454c-983f-216b50dcce52(es-es,TechNet.10).gif)
  
    **Figura 2.2. Plantillas de certificado de la consola Entidad de certificación**
  
5.  El certificado digital usado para emitir certificados de Agente de recuperación de EFS no permite cambiar el tamaño de clave predeterminado de 1024 bits. Se debe realizar una copia de la plantilla integrada y se debe configurar adecuadamente la copia resultante de la plantilla de certificado del Agente de recuperación de EFS.
  
    Haga clic con el botón secundario en la plantilla de certificado **Agente de recuperación de EFS** y seleccione **Plantilla duplicada**.
  
6.  Asigne un nuevo nombre a la plantilla de certificado nueva (por ejemplo, **Agente de recuperación de EFS actualizado**) para distinguirla de la plantilla estándar.
  
7.  Haga clic en la ficha **Tratamiento de la petición** y configure la opción de longitud de clave deseada en 2048 bits o más.
  
8.  Haga clic en la ficha **Seguridad** y asegúrese de que las cuentas de usuario que desea convertir en agentes de recuperación de EFS disponen de los permisos **Lectura** e **Inscripción**.
  
9.  Haga clic en **Aceptar**.
  
10. Abra el cuadro de diálogo de propiedades de la plantilla original de certificado de Agente de recuperación de EFS, haga clic en la ficha **Seguridad** y seleccione la opción de **denegar/inscribir permiso** para todos los usuarios. Haga clic en **Aceptar**.
  
11. Cambie a la consola Entidad de certificación, haga clic con el botón secundario en el objeto **Plantillas de certificado**, seleccione **Nueva** y, a continuación, **Plantilla de certificado que se va a emitir**.
  
12. Seleccione el certificado de Agente de recuperación de EFS nuevo y más seguro, y haga clic en **Aceptar**.
  
13. Cierre la consola Entidad de certificación.
  
14. Haga que todos los agentes de recuperación de EFS existentes soliciten nuevos certificados digitales mediante las plantillas de certificado del Agente de recuperación de EFS nuevo y más seguro.
  
15. Apruebe y emita los nuevos certificados de Agente de recuperación de datos de EFS.
  
16. Asegúrese de que se archivan las nuevas claves privadas del Agente de recuperación de EFS (como archivos con la extensión .PFX) o de que sus copias de seguridad se guardan en dos o más ubicaciones independientes y seguras y, a continuación, elimínelas del equipo local hasta que sean necesarias para una recuperación.
  
**Nota**   Todos los certificados de DRA y KRA para EFS se deben emitir a partir del certificado configurado recientemente; de lo contrario, presentarán la longitud de clave inicial.
  
Las organizaciones que pueden haber implementado anteriormente EFS y agentes de recuperación de EFS mediante la plantilla estándar, deberán cifrar con el certificado de Agente de recuperación de EFS nuevo y más seguro los archivos que ya se hayan cifrado con el Agente de recuperación de EFS menos seguro. Este proceso se realizará automáticamente, archivo por archivo, al modificar los archivos independientes.
  
Puede ordenar a EFS que actualice todos los archivos cifrados de las unidades locales de forma simultánea con tan solo abrir un símbolo del sistema, escribir **Cipher.exe /U** y presionar Entrar.
  
Después de volver a cifrar todos los archivos cifrados con el nuevo certificado de Agente de recuperación de EFS y, después de asegurarse de que ha creado una copia de seguridad de las copias de la clave original y menos segura del Agente de recuperación de EFS en dos o más ubicaciones seguras e independientes, puede eliminar la clave de recuperación original del objeto Plantillas de certificado de la consola Entidad de certificación.
  
###### Solicitud de certificados de DRA para un usuario independiente
  
En circunstancias para las que se requieren varios agentes de recuperación para el dominio o en las que es necesario que el agente de recuperación sea distinto del administrador de dominio por razones legales o por la directiva corporativa, puede que deba identificar a algunos usuarios como agentes de recuperación. Para estos usuarios se deben emitir certificados de recuperación de archivos.
  
La emisión de estos certificados requiere lo siguiente:
  
-   Una entidad de certificación de la empresa debe estar disponible.
  
-   La directiva de la entidad de certificación de la empresa debe permitir a los usuarios o los agentes designados solicitar y obtener un certificado de recuperación.
  
-   Cada usuario debe solicitar un certificado de recuperación de archivos.
  
Es posible automatizar este proceso mediante la habilitación de la inscripción automática de certificados, o bien, se puede realizar manualmente mediante la realización de los pasos de este procedimiento:
  
**Para crear un certificado de Agente de recuperación de EFS**
  
1.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, seleccione **Agregar o quitar complemento** y, a continuación, haga clic en **Agregar**.
  
3.  Haga doble clic en **Certificados**, seleccione **Mi cuenta de usuario** y, a continuación, haga clic en **Finalizar**. Haga clic en **Cerrar** y, a continuación, haga clic en **Aceptar**.
  
4.  Haga clic en el signo más (**+**) junto a **Certificados: usuario actual** para expandir la carpeta.
  
5.  Haga clic con el botón secundario en **Personal** en el panel izquierdo, haga clic en **Todas las tareas** y, a continuación, haga clic en **Solicitar un nuevo certificado** para iniciar el Asistente para solicitud de certificados.
  
6.  La primera página del asistente solo es informativa. Haga clic en **Siguiente** para continuar.
  
7.  Se mostrará una lista de plantillas de certificado. Seleccione **Agente de recuperación de EFS** y, a continuación, haga clic en **Siguiente**.
  
8.  Escriba un nombre descriptivo para distinguir este certificado de otros y agregue una descripción, si lo desea. Haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar** para solicitar el certificado.
  
9.  Haga clic en **Aceptar** para confirmar que se ha realizado una solicitud de certificado correcta.
  
Para crear una directiva de recuperación de EFS para todo el dominio, se deberá exportar con formato .CER el certificado de Agente de recuperación de EFS creado anteriormente.
  
###### Aprobación de las solicitudes de certificado de DRA para EFS
  
Por lo general, las solicitudes de certificado de DRA para EFS se deben aprobar manualmente en los Servicios de Certificate Server.
  
**Para revisar y aprobar las solicitudes de DRA enviadas al servidor de Servicios de Certificate Server**
  
1.  Inicie la sesión en Windows con una cuenta de usuario que permita aprobar solicitudes de certificado digital en Servicios de Certificate Server.
  
2.  Abra la consola Entidad de certificación centrándose en un servidor autorizado de los Servicios de Certificate Server. Para ello, haga clic en **Inicio**, **Todos los programas**, **Herramientas administrativas** y, a continuación, seleccione **Entidad de certificación**.
  
3.  Expanda el servidor Entidad de certificación para ver todos sus componentes.
  
4.  Haga clic en **Solicitudes pendientes**. El panel derecho mostrará una lista con las solicitudes de certificado pendientes en espera de aprobación.
  
5.  Busque las solicitudes de certificado de Agente de recuperación de EFS pendientes que correspondan, haga clic con el botón secundario en ellas y seleccione **Emitir**. Cierre la consola Entidad de certificación cuando termine.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
Si usa una plantilla de certificado que requiera la aprobación de un administrador y solicita manualmente un certificado mediante dicha plantilla, puede que la solicitud no se realice correctamente. De ser así, deberá editar la plantilla para quitar el requisito de aprobación de administrador, o bien, crear una nueva solicitud mediante otra plantilla.
  
###### Exportación de certificados para la asignación de directivas
  
Después de asignar un certificado de DRA a un usuario, deberá exportar dicho certificado para que se pueda adjuntar a un objeto de directiva de grupo para su asignación como directiva de recuperación.
  
**Para exportar un certificado para su asignación a un GPO**
  
1.  En la consola Certificados, expanda la carpeta **Personal**.
  
2.  En el panel derecho, haga clic con el botón secundario en el certificado que acaba de crear, haga clic en **Todas las tareas** y, a continuación, haga clic en **Exportar**. Haga clic en **Siguiente** para comenzar el proceso de exportación.
  
3.  Active la casilla **No exportar la clave privada** y, a continuación, haga clic en **Siguiente**.
  
4.  Mantenga el formato de archivo predeterminado .cer y haga clic en **Siguiente**.
  
5.  Proporcione una ruta de acceso y un nombre de archivo y, a continuación, haga clic en **Siguiente**.
  
6.  Para realizar la exportación, haga clic en **Finalizar** y, a continuación, haga clic en **Aceptar**.
  
7.  Cierre la consola Certificados.
  
###### Definición de un agente de recuperación de datos
  
Puede definir los agentes de recuperación de datos mediante la modificación del objeto de directivas de clave pública de un objeto de directiva de grupo, la adición de un DRA y la vinculación del certificado de DRA al DRA. Para ello, necesitará un certificado de DRA con formato .CER.
  
**Para definir un DRA**
  
1.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo** , haga clic en **Agregar o quitar complemento**.
  
3.  Haga clic en **Agregar**, desplácese hacia abajo y, a continuación, haga doble clic en **Directiva** de **grupo**.
  
4.  Seleccione el objeto de directiva de grupo que está usando para aplicar la directiva de DRA a los equipos implicados y, a continuación, haga clic en **Aceptar**.
  
5.  Haga clic en el signo más (**+**) junto al GPO de destino para expandir el árbol. Expanda **Configuración del equipo**, **Configuración de Windows**, **Configuración de seguridad** y **Directivas de claves públicas**. Haga clic en **Sistema de cifrado de archivos**.
  
6.  Haga clic con el botón secundario en **Sistema de cifrado de archivos** y, a continuación, haga clic en **Agregar Agente de recuperación de datos**.
  
7.  En la pantalla del Asistente para **agregar agente de recuperación**, haga clic en **Siguiente**, en **Examinar carpetas** y, a continuación, navegue a la carpeta **Documents and Settings** del administrador. Haga doble clic en el archivo **DRA.CER**, haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar**.
  
##### Administración y configuración de los agentes Key Recovery Agent
  
La próxima tarea de implementación necesaria para la implementación de EFS es la configuración de las cuentas e infraestructura de Key Recovery Agent (KRA).
  
###### Configuración de los Servicios de Certificate Server para almacenar claves
  
Si usa la solución Servicios de Certificate Server de Windows Server 2003, puede configurar la entidad de certificación para facilitar el almacenamiento automático de claves. El almacenamiento automático de claves solo es posible con Windows Server 2003 o posterior. Para configurar el almacenamiento automático de claves, debe realizar las siguientes tareas, que se describen detalladamente en las siguientes subsecciones:
  
-   Habilitar los certificados de Key Recovery Agent
  
-   Solicitar y emitir certificados de Key Recovery Agent
  
-   Aprobar solicitudes de certificado
  
-   Configurar agentes Key Recovery Agent en los Servicios de Certificate Server
  
-   Configurar la plantilla de certificado digital para incluir el marcador de capacidad de almacenamiento y poder archivar los certificados recién emitidos
  
**Habilitación de los certificados de Key Recovery Agent**
  
Para permitir las solicitudes de Key Recovery Agent, primero debe habilitarlas en Servicios de Certificate Server.
  
**Para permitir las solicitudes de certificado de KRA**
  
1.  Seleccione una o más cuentas de usuario para convertirlas en agentes Key Recovery Agent.
  
2.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.
  
3.  Abra la consola Entidad de certificación (**Inicio**, **Todos los programas**, **Herramientas administrativas**, **Entidad de certificación**) y agregue un servidor de Servicios de Certificate Server autorizado.
  
4.  Expanda el nodo **Entidad de certificación**, haga clic con el botón secundario en el objeto **Plantillas de certificado** y seleccione **Administrar** para abrir la consola Plantilla de certificados.
  
5.  Haga clic con el botón secundario en la plantilla de certificado **Key Recovery Agent** y seleccione **Propiedades**.
  
6.  Haga clic en la ficha **Seguridad** y asegúrese de que las cuentas de usuario que desea designar como KRA (las seleccionadas en el primer paso) disponen de los permisos **Lectura** e **Inscripción**.
  
7.  En la ficha **Tratamiento de la petición**, asegúrese de que la opción **Tamaño mínimo de clave** está definida en 2048 bits o más.
  
    ![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
    Microsoft recomienda ahora que todas las claves de recuperación DRA y KRA tengan 2048 bits o más.
  
8.  Haga clic en **Aceptar** .
  
9.  Si se siguen generando y usando claves de 1024 bits o menos, se deberán generar claves nuevas más largas para reemplazar las claves menos seguras. Haga clic con el botón secundario en la plantilla de certificado **Key Recovery Agent** y seleccione la opción **Volver a inscribir a todos los poseedores de certificados**.
  
10. Cambie a la consola Entidad de certificación, haga clic con el botón secundario en el objeto **Plantillas de certificado**, seleccione **Nueva** y, a continuación, **Plantilla de certificado que se va a emitir**.
  
11. Seleccione el **certificado de Key Recovery Agent** y haga clic en **Aceptar**.
  
12. Cierre las plantillas de certificado y las consolas Entidad de certificación.
  
**Solicitud y emisión de certificados de Key Recovery Agent**
  
Después de habilitar las cuentas seleccionadas para usarlas como KRA, deberá emitir los certificados habilitados como KRA a estos usuarios.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
Los certificados de Key Recovery Agent se pueden solicitar de diversas formas, incluidas a través de la consola Certificados, la inscripción web (si está habilitada) o mediante archivos de solicitud de certificado manual. En esta guía, se describe el método de la consola Certificados.
  
**Para emitir certificados habilitados como KRA**
  
1.  Inicie la sesión en Windows mediante el nombre de inicio de sesión y la contraseña de cuenta de usuario de KRA.
  
2.  Haga clic en **Inicio**, **Ejecutar**, escriba **MMC.EXE** y presione Entrar. Haga clic en **Continuar** si el Control de cuentas de usuario lo solicita.
  
3.  Haga clic en la opción de menú **Archivo** y, a continuación, seleccione **Agregar o quitar complemento**.
  
4.  Seleccione el complemento **Certificados** y, a continuación, haga clic en **Agregar**.
  
5.  Cuando se le solicite, seleccione **Mi cuenta de usuario**, haga clic en **Finalizar** y, a continuación, en **Aceptar**.
  
6.  Expanda el objeto **Certificados: usuario actual** y, a continuación, haga clic en **Personal**.
  
7.  Haga clic con el botón secundario en **Personal**, seleccione **Todas las tareas** y, a continuación, **Solicitar un nuevo certificado**.
  
8.  Haga clic en **Siguiente** en la pantalla del Asistente para solicitud de certificados.
  
9.  Seleccione **Key Recovery Agent** en el cuadro de diálogo **Tipo de certificado** y, a continuación, haga clic en **Siguiente**.
  
10. Escriba un nombre descriptivo (por ejemplo, **Mi certificado de Key Recovery Agent**) y una descripción, haga clic en **Siguiente** y, a continuación, en **Finalizar**.
  
11. Cierre la consola Certificados cuando ya no sea necesaria.
  
12. Cierre la sesión en Windows.
  
Repita los pasos 1-12 para todos los usuarios autorizados que vayan a recibir un certificado de Key Recovery Agent.
  
**Aprobación de solicitudes de certificado**
  
Por lo general, los certificados de KRA se deben aprobar manualmente en los Servicios de Certificate Server.
  
**Para aprobar solicitudes de certificado de KRA**
  
1.  Inicie la sesión en Windows con una cuenta de usuario que permita aprobar solicitudes de certificado digital en Servicios de Certificate Server.
  
2.  Abra la consola Entidad de certificación y agregue un servidor autorizado de Servicios de Certificate Server.
  
3.  Expanda el nodo **Entidad de certificación** y, a continuación, haga clic en **Solicitudes pendientes**. El panel derecho mostrará las solicitudes de certificado pendientes en espera de aprobación.
  
4.  Seleccione las solicitudes de certificado de KRA que desea aprobar.
  
5.  Haga clic con el botón secundario en cada solicitud de KRA y, a continuación, seleccione **Emitir**.
  
6.  Cierre la consola Entidad de certificación.
  
**Configuración de agentes Key Recovery Agent en los Servicios de Certificate Server**
  
Se debe agregar cada Key Recovery Agent a los Servicios de Certificate Server.
  
**Para agregar agentes KRA a Servicios de Certificate Server**
  
1.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.
  
2.  Abra la consola Entidad de certificación y agregue un servidor autorizado de Servicios de Certificate Server.
  
3.  Haga clic con el botón secundario en el objeto de servidor y seleccione **Propiedades**.
  
4.  Haga clic en la ficha **Agentes de recuperación** (mostrada en la siguiente captura de pantalla).
  
    ![](images/Cc162812.57b5ad90-e987-4a94-b282-f8ebe8ff066d(es-es,TechNet.10).gif)
  
    **Figura 2.3. Ficha Agentes de recuperación para un objeto de servidor en la consola Entidad de certificación**
  
5.  En el cuadro **Número de agentes de recuperación que se utilizarán**, escriba el número de agentes Key Recovery Agent que se van a usar para cifrar la clave archivada. Este valor debe ser igual o superior a 1. Sin embargo, si el valor supera el número de certificados de Agente de recuperación con estado “Válido”, las nuevas solicitudes de inscripción que requieran el almacenamiento de claves no se realizarán correctamente.
  
6.  Haga clic en **Agregar** y agregue uno o más agentes KRA que haya aprobado previamente. A continuación, haga clic en **Aceptar**.
  
7.  Seleccione **Sí** cuando se le solicite detener y reiniciar los Servicios de Certificate Server. No se cargarán nuevos agentes Key Recovery Agent hasta que los Servicios de Certificate Server no se hayan detenido y reiniciado.
  
8.  Cierre la consola Entidad de certificación cuando ya no sea necesaria.
  
**Creación de nueva plantilla de certificado EFS para permitir el almacenamiento de claves**
  
El certificado digital que se usa para emitir certificados digitales EFS a los usuarios se debe configurar para archivar claves de forma automática. Esta opción no se puede habilitar en la plantilla de certificado EFS básico integrada. Debe copiar la plantilla integrada y, a continuación, habilitar la copia de la plantilla de certificado EFS para automatizar el almacenamiento de claves.
  
**Para configurar un certificado digital con objeto de archivar claves de forma automática**
  
1.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.
  
2.  Abra la consola Entidad de certificación y agregue un servidor autorizado de Servicios de Certificate Server.
  
3.  Expanda el nodo **Entidad de certificación**, haga clic con el botón secundario en el nodo **Plantillas de** **certificado** y seleccione **Administrar** para abrir la consola Plantilla de certificados.
  
4.  Haga clic con el botón secundario en la plantilla de certificado **EFS básico** y seleccione **Plantilla duplicada**.
  
5.  Asigne un nuevo nombre a la plantilla de certificado nueva (por ejemplo, EFS básico actualizado) para distinguirla de la plantilla estándar.
  
6.  Haga clic en la ficha **Tratamiento de la petición** y active la casilla **Archivar clave privada de cifrado de sujeto** como se muestra en la siguiente captura de pantalla.
  
    ![](images/Cc162812.c10c48ea-8cdd-4057-8b41-760fa2df9665(es-es,TechNet.10).gif)
  
    **Figura 2.4. Cuadro de diálogo Propiedades de plantilla nueva en la consola Entidad de certificación**
  
7.  Establezca la longitud de clave deseada (por ejemplo, 2048 bits).
  
8.  Haga clic en la ficha **Seguridad** y asegúrese de que las cuentas de usuario que desea que funcionen como EFS disponen de los permisos **Lectura** e **Inscripción**.
  
9.  Establezca otras opciones de plantilla de certificado que desee, por ejemplo, la inscripción automática y la vida útil, entre otras.
  
10. En la plantilla de **certificado EFS básico**, haga clic en la ficha **Seguridad** y cree una entrada de control de acceso nueva que asigne la acción **Denegar** al **permiso de inscripción**.
  
    ![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
    Todos los certificados EFS emitidos se deben emitir a partir del certificado configurado recientemente o, de lo contrario, las claves no se archivarán automáticamente.
  
11. Haga clic en **Aceptar** y salga de la consola Entidad de certificación.
  
##### Creación y uso de un agente de recuperación sin conexión
  
Microsoft recomienda encarecidamente configurar los agentes KRA y DRA para su uso sin conexión, además de habilitarlos solo cuando se necesiten para escenarios de recuperación. Existen cuatro pasos generales necesarios para crear un agente de recuperación sin conexión:
  
1.  Crear una nueva cuenta de usuario con objeto de usarla exclusivamente para eventos de recuperación.
  
2.  Solicitar, generar y asignar un certificado digital de DRA o KRA para la nueva cuenta.
  
3.  Exportar el certificado y la clave privada, quitarlos de la red y almacenarlos de forma segura.
  
4.  Deshabilitar la cuenta de usuario de recuperación para que no se use hasta que sea necesaria.
  
Los pasos 1 y 2 se analizan en esta guía, y el paso 4 es una tarea de mantenimiento de cuentas habitual de Windows. Sin embargo, el paso 3 requiere una explicación más extensa.
  
###### Formas de exportar y eliminar certificados de recuperación
  
Con el fin de exportar y quitar un certificado de recuperación para su uso sin conexión, realice los siguientes pasos.
  
**Para exportar y quitar un certificado de recuperación**
  
1.  Inicie la sesión en Windows mediante la cuenta de usuario de recuperación para la que desea exportar las claves.
  
2.  Haga clic en **Inicio**, **Ejecutar**, escriba **MMC.EXE** y presione Entrar. Si lo solicita el Control de cuentas de usuario, haga clic en **Continuar**.
  
3.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**.
  
4.  Seleccione el complemento **Certificados** y, a continuación, haga clic en el botón **Agregar**.
  
5.  Cuando se le solicite, seleccione el botón de radio **Mi cuenta de usuario**, haga clic en el botón **Finalizar** y, a continuación, haga clic en **Aceptar**.
  
6.  Expanda el objeto **Certificados: usuario actual**, expanda **Personal** y, a continuación, haga clic en **Certificados**.
  
7.  Busque el certificado digital de recuperación adecuado. Si no está seguro del certificado que debe usar, consulte los certificados digitales con **Recuperación de archivos** o **Recuperación de clave** en el campo **Propósitos planteados**.
  
8.  Haga clic con el botón secundario en el certificado digital de recuperación, haga clic en **Todas las tareas** y, a continuación, haga clic en **Exportar** para iniciar el Asistente para exportación de certificados.
  
9.  Haga clic en el botón **Siguiente**.
  
10. Active la casilla **Exportar la clave privada** y, a continuación, haga clic en **Siguiente**.
  
11. Active la casilla **Eliminar la clave privada si la exportación es satisfactoria** y, a continuación, haga clic en **Siguiente**.
  
    ![](images/Cc162812.98313b0b-0b11-4d33-aaf6-0a5ac35dce84(es-es,TechNet.10).gif)
  
    **Figura 2.5. Solicitud de exportación de formato de archivo en el Asistente para exportación de certificados**
  
12. Escriba una contraseña de protección dos veces y, a continuación, haga clic en **Siguiente**.
  
13. Haga clic en **Examinar** y, a continuación, elija la ubicación en la que desea almacenar el certificado de recuperación exportado.
  
14. Escriba un nombre de archivo para las claves y el certificado de recuperación de los que se ha realizado una copia de seguridad. Deje la extensión del archivo como .PFX para facilitar la reimportación de la clave.
  
15. Haga clic en **Guardar**, en **Siguiente**, en **Finalizar** y, a continuación, haga clic en **Aceptar**.
  
16. Copie el archivo de copia de seguridad resultante en otra ubicación y elimínelo de la ubicación actual si no lo necesita. Asegúrese de vaciar la Papelera de reciclaje después de eliminar los archivos o los certificados digitales EFS.
  
17. Almacene las claves y el certificado digital de recuperación de los que se ha realizado una copia de seguridad en dos o más ubicaciones independientes y seguras.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
Cuando la clave privada del certificado de recuperación se haya exportado, se debe dejar la clave pública de recuperación (usada para el cifrado de FEK) en el equipo. Si la elimina, no podrá habilitar el agente de recuperación para cifrar o recuperar las claves o los archivos protegidos con EFS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas de configuración por equipo
  
Además de las tareas de configuración de la infraestructura descritas anteriormente, deberá realizar tareas de configuración en los equipos de forma individual.
  
#### Tareas de configuración por equipo en BitLocker
  
Para configurar BitLocker en un equipo, debe:
  
-   asegurarse de que el equipo puede ejecutar BitLocker.
  
-   habilitar e inicializar el TPM si ya hay uno.
  
-   habilitar BitLocker.
  
##### Actualización del BIOS para su compatibilidad con el TPM
  
En la fase de planeación, determinó los equipos que se usarían con BitLocker y los equipos que incluirían la versión 1.2 (o superior) del hardware de TPM y un BIOS compatible. El primer paso a la hora de realizar las tareas de configuración de cada equipo en BitLocker es la actualización del BIOS de los equipos que lo necesiten.
  
Los pasos específicos necesarios para la actualización del BIOS de un equipo varían según el fabricante. Las actualizaciones de firmware de BIOS suelen distribuirse en medios que acompañan a los nuevos equipos y estar disponibles en el sitio web del OEM o del proveedor de la placa base. En general, para los equipos móviles, deberá crear un CD de arranque o un disco USB con la imagen del BIOS suministrada por el fabricante y, a continuación, usarla para arrancar el equipo mientras está conectado a una salida eléctrica. Este proceso requiere obligatoriamente acceso físico a todos los equipos que se vayan a actualizar. Siga las instrucciones del proveedor para la actualización del firmware del BIOS y vuelva a arrancar el equipo después de aplicar la actualización.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
Es importante que todos los equipos participantes tengan las últimas actualizaciones del firmware del BIOS por muchas razones, incluidas actualizaciones de software y mejoras de rendimiento. Antes de habilitar un TPM o BitLocker en Windows Vista, asegúrese de que está instalada la última versión del firmware.
  
##### Confirmación de la ruta de acceso de arranque estable
  
BitLocker y TPM aseguran la integridad de la ruta de acceso de arranque desde que se inicia el equipo a lo largo del proceso de arranque de Windows Vista mediante la realización de una serie de comprobaciones conocidas conjuntamente como *perfil de validación de plataforma* (PVP) de TPM. Si el proceso de arranque cambia significativamente después de instalar BitLocker, los resultados del PVP serán diferentes y no se podrá notar ningún cambio de integridad. Si se produce un cambio de integridad, BitLocker podría denegar el desbloqueo del volumen del sistema operativo sin usar un método de recuperación adicional.
  
Por este motivo, asegúrese de que la ruta de arranque del hardware y el software esté completamente configurada y de que sea estable antes de habilitar BitLocker. En concreto, todos los equipos en los que vaya a habilitar BitLocker deben tener:
  
-   Una configuración del BIOS que refleje el dispositivo de arranque correcto
  
-   Todos los dispositivos opcionales con firmware ROM instalados
  
-   Eventos Wake-on-LAN configurados
  
-   Datos de la configuración de arranque (BCD) de Windows configurados
  
Puede usar la directiva de equipo local y la directiva de grupo de Active Directory para configurar los componentes de arranque (llamados *Registros de configuración de la plataforma* o PCR) que el TPM tendrá en cuenta durante el proceso de inicio. En la mayoría de las aplicaciones, el conjunto de PCR predeterminado ofrece un buen nivel de seguridad y Microsoft no recomienda que se cambie.
  
Después de instalar BitLocker, si se cambian componentes que tienen un PCR correspondiente, BitLocker solicitará una contraseña de recuperación. Entre los cambios de PCR, se incluyen la actualización del BIOS, la adición de un dispositivo de arranque ROM, la modificación del registro de arranque maestro (MBR), la tabla de particiones, los datos del sector de arranque de bajo nivel, los datos de configuración de arranque o la administración de arranque, o bien la instalación de otro sistema operativo en un nuevo escenario de arranque dual.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
El registro de arranque maestro, el código del sector de arranque y la administración de arranque de Windows Vista proporcionan una protección de la integridad crítica a BitLocker. Microsoft recomienda encarecidamente que no usen cargadores de arranque de terceros. La agregación de un nuevo cargador de arranque después de habilitar BitLocker activará la recuperación, mientras que el cambio de los cargadores de arranque antes de habilitar BitLocker impedirá que BitLocker mantenga un entorno de arranque seguro.
  
##### Habilitación de TPM
  
Si tiene intención de implementar BitLocker con el TPM, debe habilitar el TPM de cada equipo cliente. Los equipos certificados como compatibles con Windows Vista deben contener una versión del BIOS que permita que BitLocker habilite el TPM como parte del proceso de configuración de BitLocker. Si no es así, la habilitación del TPM suele precisar que use el programa de configuración del BIOS del equipo, que se suele invocar mediante una combinación de teclas concreta durante el proceso de arranque del hardware del equipo. La opción de TPM se suele encontrar en **Opciones avanzadas** o en las opciones de **configuración de periféricos** en las pantallas de configuración, aunque no existe una ubicación estándar. Si la opción está deshabilitada, seleccione **Habilitar**, guarde la nueva configuración del BIOS, salga y, a continuación, vuelva a arrancar el equipo si es necesario. Después de arrancar de nuevo, la mayoría de los equipos con TPM muestran una pantalla como la que aparece en la siguiente captura de pantalla en la que se solicita que confirme que desea habilitar el TPM.
  
![](images/Cc162812.e6903e71-09fe-424c-87de-d344db8d8e05(es-es,TechNet.10).gif)
  
**Figura 2.6. Ejemplo de cuadro de diálogo de confirmación de TPM**
  
##### Inicialización de TPM con Windows Vista
  
Si se va a usar un TPM con BitLocker, el chip TPM se debe inicializar, lo que permite que Windows Vista tome posesión del TPM. La información de propiedad del TPM se puede visualizar con el complemento TPM MMC (tpm.msc).
  
Se deberá inicializar el TPM una vez en cada equipo. Se deberá habilitar BitLocker una vez por sistema operativo (si el equipo está configurado para arrancar varios sistemas operativos). En otras palabras, si tiene un único equipo que tiene varias instalaciones de arranque de Windows Vista, deberá habilitar BitLocker en cada instalación de Windows Vista.
  
En condiciones normales, el Asistente para instalar BitLocker automatizará el proceso de inicialización del TPM. No obstante, también puede inicializar el TPM manualmente, si es necesario.
  
**Para inicializar el TPM en Windows Vista**
  
1.  Asegúrese de que el chip TPM está habilitado en el BIOS.
  
2.  Asegúrese de que el dispositivo de almacenamiento o impresión está disponible para la contraseña de administración del TPM.
  
3.  Inicie la sesión en Windows Vista con una cuenta que tenga privilegios de administrador local en el equipo.
  
4.  Inicie el complemento Módulo de plataforma segura de MMC. Para ello, escriba **TPM.MSC** en el cuadro **Buscar** y, a continuación, presione Entrar.
  
5.  Si lo solicita el Control de cuentas de usuario, haga clic en **Continuar** y aparecerá una consola TPM.
  
6.  Si Windows Vista no reconoce el chip TPM, deberá solucionar el problema, habilitarlo correctamente y, a continuación, volver a comenzar este procedimiento.
  
7.  En el panel **Acciones**, haga clic en la opción **Inicializar TPM**.
  
8.  En el cuadro de diálogo **Crear contraseña de propietario de TPM**, se le solicitará que cree una contraseña de propietario de TPM. Esta contraseña es necesaria solo para las tareas de administración de TPM fuera del dominio de BitLocker.
  
    Puede dejar que el asistente cree automáticamente la contraseña (acción recomendada) o puede crear la contraseña manualmente. Si decide crear la contraseña manualmente, deberá crear una que tenga al menos 8 caracteres. Después de establecer la contraseña de propietario de TPM, podrá cambiarla cuando lo desee (aunque necesitará saber la contraseña actual para cambiarla).
  
9.  Puede guardar la contraseña en un medio extraíble o en una ubicación de almacenamiento válida, incluidos un dispositivo de memoria flash USB, una ubicación de archivo, el escritorio o una ubicación de red. Si lo prefiere, puede imprimir la contraseña en una impresora de red o local adjunta. Si almacena la contraseña TPM, Windows Vista la guarda como archivo XML terminado en una extensión de archivo .TPM. De manera predeterminada, se asigna el nombre del equipo al archivo. Debe guardar o imprimir la contraseña de propietario de TPM en dos o más ubicaciones independientes y seguras.
  
10. Después de escribir y guardar o imprimir la contraseña, comenzará la inicialización del TPM. Windows Vista muestra un cuadro de diálogo de progreso en el que se indica el estado de la inicialización del TPM.
  
11. Una vez completada la inicialización, Windows Vista muestra un cuadro de diálogo de finalización. Haga clic en **Cerrar** para finalizar el proceso de inicialización.
  
También puede inicializar el TPM y tomar posesión del mismo desde Windows Vista mediante el uso del script **manage-bde.wsf** en un símbolo del sistema de la siguiente forma:
  
**cscript manage-bde.wsf -tpm -takeownership -***&lt;contraseña&gt;*
  
Al ejecutarse este comando, se tomará posesión del TPM y se establecerá como contraseña de propietario de TPM el valor especificado.
  
También puede crear un script que use las interfaces WMI proporcionadas para controlar el TPM.
  
##### Habilitación de BitLocker
  
Se puede habilitar BitLocker de dos formas: de forma manual, mediante el uso de los pasos del procedimiento siguiente, o bien, mediante el uso del Asistente para implementar Windows. Si desea obtener más información acerca del uso del Asistente para implementar Windows para habilitar BitLocker, consulte [Ejecución del Asistente para implementar Windows](http://go.microsoft.com/fwlink/?linkid=78820) de la sección “Guía de instalación de Lite Touch” de Business Desktop Deployment Toolkit.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota:**
  
Los parámetros de la directiva de grupo se pueden usar para controlar las características de BitLocker que pueden configurar los usuarios finales, por lo que puede variar la interfaz que aparece en las siguientes capturas de pantalla.
  
**Para habilitar BitLocker manualmente**
  
1.  Abra el Panel de control y, a continuación, haga doble clic en **Seguridad**.
  
2.  Haga doble clic en **Cifrado de unidad BitLocker**. Si lo solicita el Control de acceso de usuarios, haga clic en **Continuar**.
  
    ![](images/Cc162812.d98ec788-93f5-4dc5-813d-55a9f67c70ba(es-es,TechNet.10).gif)
  
    **Figura 2.7. Pantalla de Cifrado de unidad BitLocker en el Panel de control**
  
3.  Haga clic en la opción **Activar BitLocker**.
  
4.  Como muestra la siguiente figura, es posible que se le pida que elija una ubicación donde guardar o imprimir la contraseña de recuperación de BitLocker. Si decide guardar la contraseña de recuperación de BitLocker, la contraseña de recuperación de BitLocker de 48 caracteres se guardará en un archivo de texto con el nombre del identificador de la contraseña de BitLocker. Si guarda la contraseña de recuperación en una unidad de memoria flash USB, se guardará una clave de recuperación de 256 bits, así como un archivo oculto (con extensión .BEK). Puede elegir la ubicación de almacenamiento de archivos o la unidad de memoria flash USB que desee, o puede imprimir la contraseña de recuperación. La siguiente captura de pantalla muestra cómo se guarda la contraseña de recuperación en una carpeta o en una unidad de memoria flash USB.
  
    ![](images/Cc162812.f0c09b3f-eeee-479e-8aa3-12214ccb7249(es-es,TechNet.10).gif)
  
    **Figura 2.8. Opciones de contraseña de recuperación de BitLocker**
  
5.  Debe guardar la contraseña de recuperación en una o más ubicaciones independientes y seguras. Si pierde esta clave de recuperación de BitLocker, podría perder el acceso a los datos. No podrá pasar a habilitar BitLocker hasta que guarde correctamente la contraseña de recuperación de BitLocker.
  
    ![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota**
  
    La contraseña de recuperación se escribe en texto sin formato en el archivo de texto, por lo que se debe proteger contra el acceso no autorizado.
  
    Después de guardar la contraseña de recuperación de BitLocker una o más veces, haga clic en el botón **Siguiente**.
  
6.  En el cuadro de diálogo **Cifrar el volumen**, seleccione la opción **Ejecutar la comprobación del sistema de BitLocker** para comprobar que la ruta de acceso de arranque es de confianza y que se puede ubicar el protector de BitLocker antes de comenzar el cifrado. Este paso es opcional, aunque se recomienda encarecidamente que se realice. Si se produce un error, Windows Vista muestra una advertencia y el cifrado de BitLocker no se produce de forma automática.
  
7.  Haga clic en el botón **Continuar**. Si decide no realizar una comprobación del sistema, puede hacer clic en **Cifrar** para comenzar el cifrado del volumen.
  
8.  Si decide realizar una comprobación del sistema, se le pedirá que se asegure de que se ha insertado el medio de memoria flash USB (si es ahí donde decide almacenar la contraseña de recuperación de BitLocker) y, a continuación, que reinicie el equipo.
  
9.  Durante el reinicio, Windows Vista busca y comprueba la contraseña de recuperación de BitLocker almacenada en la clave USB y muestra un mensaje en un cuadro de diálogo de texto antes del arranque que indica que se ha realizado correctamente.
  
10. Cuando Windows Vista se reinicia, BitLocker comienza el cifrado del volumen de arranque y muestra un mensaje de progreso que indica el porcentaje completado, como muestra la siguiente captura de pantalla.
  
    ![](images/Cc162812.bdf7dbb8-4613-45fb-af4a-6c0180e4702b(es-es,TechNet.10).gif)
  
    **Figura 2.9. Mensaje de progreso de cifrado de BitLocker**
  
El primer cifrado activo del volumen del sistema operativo causará un ligero retraso en el rendimiento. Los usuarios pueden seguir trabajando en el equipo mientras se produce el cifrado.
  
##### Validación de la configuración y la instalación de BitLocker
  
Cuando BitLocker haya terminado de cifrar el volumen del sistema operativo, puede confirmar el estado mediante el uso de la consola de administración de discos, que aparece en la siguiente captura de pantalla. El volumen cifrado incluirá las palabras BitLocker cifrado.
  
![](images/Cc162812.7985cd63-82be-41ae-bf22-ef5b57f7f667(es-es,TechNet.10).gif)
  
**Figura 2.10. Consola de administración de discos**
  
Si usa Active Directory para el almacenamiento de claves de recuperación, debe comprobar que la información de recuperación está correctamente almacenada en Active Directory. Para ello, puede obtener BitLocker Recovery Password Viewer (disponible en el artículo 928202 de Microsoft Knowledge Base, acerca de [cómo usar BitLocker Recovery Password Viewer para la herramienta Usuarios y equipos de Active Directory y ver contraseñas de recuperación de Windows Vista](http://support.microsoft.com/kb/928202)), instalarlo y usarlo para comprobar que la información de recuperación esté disponible para uno o más equipos de prueba. BitLocker Recovery Password Viewer también simplifica el proceso por el que se permite que el personal de soporte o del departamento de soporte técnico autorizado obtenga la información de recuperación cuando es necesario. Para obtener más información acerca de temas de directiva con respecto a la recuperación de contraseñas, consulte la guía de [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=67438).
  
#### Tareas de configuración de cada equipo en EFS
  
EFS necesita un número relativamente pequeño de tareas de configuración por equipo. Si es la primera vez que implementa EFS, la única tarea que tiene que completar es la de cifrar los archivos o las carpetas que quiere proteger en el equipo de destino.
  
##### Cifrado de archivos y carpetas
  
Después de que EFS esté habilitado en los equipos de destino, los usuarios de la organización pueden empezar a cifrar archivos y carpetas en sus equipos. El Asistente para EFS que acompaña a este Kit de herramientas se puede usar para crear directivas de cifrado o se puede enseñar a los usuarios la forma de usar una de las dos interfaces suministradas con Windows para habilitar el cifrado EFS.
  
###### Mediante el Explorador de Windows
  
**Para cambiar el estado de cifrado de un archivo o de una carpeta mediante el Explorador de Windows**
  
1.  Haga clic con el botón secundario en el archivo o la carpeta y, después, haga clic en **Propiedades**.
  
2.  En la ficha **General**, haga clic en el botón **Opciones avanzadas** y, a continuación, seleccione la casilla **Cifrar contenido para proteger datos**.
  
3.  Haga clic dos veces en **Aceptar** para asegurarse de que se realiza el cifrado del archivo.
  
![](images/Cc162812.5c7c1e31-6246-4f2a-bdd2-dd1691effa61(es-es,TechNet.10).gif)
  
**Figura 2.11. Cuadro de diálogo Atributos avanzados en el Explorador de Windows**
  
La primera vez que se cifra un archivo individual en una carpeta, Windows pregunta si desea cifrar solo el archivo o toda la carpeta primaria, con lo que se habilita EFS para toda la carpeta y todos sus archivos y carpetas secundarios.
  
![](images/Cc162812.1adbaf44-740f-4eef-82d9-b9bbd0750f41(es-es,TechNet.10).gif)
  
**Figura 2.12. Cuadro de diálogo Advertencia de cifrado en el Explorador de Windows**
  
###### Mediante Cipher.exe
  
También se puede usar la herramienta de línea de comandos **Cipher.exe** para cifrar archivos y carpetas. Para ello, en el símbolo del sistema cambie al directorio que contiene los archivos o las carpetas que desea cifrar. Para cifrar todo el directorio y todos los archivos y las carpetas que contiene, escriba **Cipher.exe/e** y, a continuación, presione Entrar. De forma alternativa, puede especificar una lista de archivos y carpetas que desee cifrar, incluyendo los nombres tras el parámetro **/e**.
  
###### Cifrado de archivos compartidos
  
**Para agregar usuarios a un archivo compartido**
  
1.  Haga clic con el botón secundario en el archivo o la carpeta y, después, haga clic en **Propiedades**.
  
2.  En la ficha **General**, haga clic en el botón **Opciones avanzadas** y, a continuación, haga clic en el botón **Detalles**.
  
    Windows mostrará los otros usuarios disponibles con certificados digitales EFS.
  
3.  Seleccione uno o más usuarios adicionales y, a continuación, haga clic en **Aceptar**.
  
4.  Cuando finalice, haga clic en **Aceptar** dos veces para volver al Explorador de Windows.
  
![](images/Cc162812.note(es-es,TechNet.10).gif)**Nota**
  
En Windows Vista, también se puede usar el comando **Cipher.exe** con el parámetro **/adduser** para agregar usuarios adicionales a los archivos protegidos por EFS.
  
###### Comprobación del estado de cifrado de un archivo o una carpeta
  
Si no está seguro acerca de si un archivo o una carpeta en particular están cifrados o no, puede usar varios métodos para determinar el estado. Dos de estos métodos son prestar atención a las indicaciones visuales del Explorador de Windows y usar **Cipher.exe**.
  
**Explorador de Windows**
  
En el Explorador de Windows, los archivos y las carpetas con cifrado EFS se resaltan con una fuente verde (como se muestra en la siguiente captura de pantalla) o se muestra una E en atributos de archivo.
  
![](images/Cc162812.87097207-c6cf-446a-be68-c00201db89ee(es-es,TechNet.10).gif)
  
**Figura 2.13. Archivos cifrados mediante EFS en el Explorador de Windows**
  
La fuente en verde es una característica activada de manera predeterminada en Windows XP Professional y en versiones superiores de Windows. Para activar o desactivar esta característica en Windows XP, haga clic en **Opciones de carpeta** y, a continuación, active o desactive la casilla de atributos **Mostrar con otro color los archivos NTFS comprimidos o cifrados**.
  
Para tener acceso a esta configuración en Windows Vista, abra el Explorador de Windows y, en el menú **Organizar**, haga clic en la ficha **Opciones de carpeta y de búsqueda**, haga clic en la ficha **Ver**, y active o desactive la casilla **Mostrar con otro color los archivos NTFS comprimidos o cifrados**.
  
Para tener acceso a esta configuración en Windows XP Professional, abra el Explorador de Windows y, en el menú **Herramientas**, haga clic en **Opciones de carpeta**. A continuación, haga clic en la ficha **Ver**.
  
Es posible que los atributos de archivos y carpetas no sean visibles de inmediato en el Explorador de Windows en algunas versiones de Windows. Asegúrese de que está usando la vista **Detalles** para ver los archivos. Si aun así los atributos de archivos y carpetas siguieran sin verse, deberá agregarlos a la vista **Detalles**. Para ello, haga clic con el botón secundario en el encabezado de cualquier columna en la vista **Detalles**, haga clic en **Más**, y, a continuación, seleccione **Atributos**.
  
**Cipher.exe**
  
También puede usar la utilidad de línea de comandos **Cipher.exe** para ver, cifrar o descifrar archivos protegidos con EFS (entre otras opciones). Para comprobar el estado de cifrado EFS de cualquier archivo, abra un símbolo del sistema en Windows, cambie a la ubicación del archivo o la carpeta, escriba **Cipher.exe** sin ningún parámetro en la línea de comandos, y, a continuación, presione Entrar. La utilidad Cipher mostrará una **U** junto a cualquier archivo o carpeta descifrados y una **E** para un archivo o carpeta cifrados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
-   [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=67438)
  
-   [Inscripción automática de certificados en Windows XP](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/certenrl.mspx)
  
-   [Ejecución del Asistente para implementar Windows](http://go.microsoft.com/fwlink/?linkid=78820)
  
-   [Cómo usar BitLocker Recovery Password Viewer para la herramienta Usuarios y equipos de Active Directory y ver contraseñas de recuperación de Windows Vista](http://support.microsoft.com/kb/928202)
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Consiga el Kit de herramientas de cifrado de datos para equipos móviles](http://go.microsoft.com/fwlink/?linkid=81666)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=kit%20de%20herramientas%20de%20cifrado%20de%20datos%20para%20equipos%20móviles,%20guía%20de%20implementación%20y%20planeación%20para%20el%20kit%20de%20herramientas%20de%20cifrado%20de%20datos)
  
[](#mainsection)[Principio de la página](#mainsection)
