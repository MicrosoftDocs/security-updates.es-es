---
TOCTitle: Kit de herramientas de cifrado de datos para equipos móviles
Title: Kit de herramientas de cifrado de datos para equipos móviles
ms:assetid: '54de4f8c-d962-4744-b2da-99f7ad7953df'
ms:contentKeyID: 20200206
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162806(v=TechNet.10)'
---

Kit de herramientas de cifrado de datos para equipos móviles: guía de implementación y planeación
=================================================================================================

### Capítulo 1: elementos importantes para la planeación

Publicado: 29-05-2007

La implementación de herramientas para cifrar datos con objeto de proteger los datos de la organización requiere que comprenda perfectamente las tecnologías incluidas en los sistemas operativos de Microsoft, así como los problemas de seguridad del entorno concreto. También debe estar preparado para identificar y resolver posibles problemas de implementación relacionados con la elección de hardware de cliente y su configuración, la directiva de seguridad de la organización y las complejas cuestiones del cumplimiento normativo y la realización de auditorías.

En este capítulo de la *Guía de implementación y planeación*, se tratan los elementos importantes de planeación para la implementación de Windows Vista™ con Cifrado de unidad BitLocker™ de Microsoft® (BitLocker) y el Sistema de cifrado de archivos (EFS), componente integrado en Windows Vista y Microsoft Windows® XP.

Los elementos importantes para la planeación de BitLocker y EFS que se analizan en este capítulo incluyen los requisitos de hardware y software, con lo que se determinan los equipos y los datos que necesitan protección, y se eligen las configuraciones adecuadas. Otros elementos incluyen el servicio de directorio de Active Directory® y las cuestiones de implementación de la directiva de grupo, la capacidad de administración, las posibilidades de uso y la planeación de una recuperación de datos eficaz.

Para EFS, otros elementos incluyen la integración de EFS con una infraestructura de claves públicas (PKI) existente, la implementación del Asistente para sistemas de cifrado de archivos (Asistente para EFS) de Microsoft y la planeación de una recuperación de claves eficaz.

##### En esta página

[](#edae)[Plan para el Cifrado de unidad BitLocker](#edae)
[](#ecae)[Plan para el Sistema de cifrado de archivos](#ecae)
[](#ebae)[Más información](#ebae)

### Plan para el Cifrado de unidad BitLocker

Para completar un plan de implementación de BitLocker, se deben realizar las siguientes acciones:

1.  Comprender las opciones de implementación de BitLocker

2.  Evaluar el grado de preparación para implementar BitLocker

3.  Determinar el ámbito de implementación de BitLocker

4.  Elegir la configuración de BitLocker

5.  Planear la recuperación de datos

6.  Planear la capacidad de administración

7.  Planear las posibilidades de uso

8.  Planear la implementación de Active Directory y la directiva de grupo

En las siguientes subsecciones, se analizan más detalladamente las cuestiones relacionadas con la planeación de BitLocker.

#### Descripción de las opciones de implementación de BitLocker

BitLocker mitiga eficazmente distintas amenazas contra la seguridad. Para conocer las amenazas que mitiga BitLocker, así como otras amenazas que puede mitigar junto con EFS, es necesario que comprenda el modelo de seguridad de BitLocker y las opciones de implementación compatibles. En el documento *Análisis de seguridad* incluido en el Kit de herramientas, se enumeran varios riesgos y el modo en que BitLocker los mitiga. Se debe familiarizar por completo con su contenido antes de continuar con el proceso de planeación.

#### Evaluación del grado de preparación para implementar BitLocker

Para usar BitLocker, un equipo requiere los siguientes componentes:

-   Edición Enterprise o Ultimate de Windows Vista™

-   Si desea usar BitLocker con un TPM, una placa base compatible con TPM (BIOS y chip TPM con la versión 1.2 o superior de la especificación de TPM de Trusted Computing Group).

-   Unidad de disco duro con dos particiones con formato NTFS. La partición en la que se almacena la información de los componentes de arranque de BitLocker debe estar vacía y tener un mínimo de 1,5 GB de espacio disponible. Esta debe ser la partición activa.

Puede confirmar manualmente estos requisitos mediante un script de Instrumental de administración de Windows (WMI) o PowerShell para consultar los equipos cliente y reunir información acerca de sus funciones. La mayoría de las organizaciones prefiere usar una herramienta de administración como Microsoft Systems Management Server (SMS) o una herramienta equivalente de terceros, ya que ofrecen opciones de inventario automatizado y de generación de informes.

##### Requisitos de hardware para BitLocker

BitLocker es compatible con cualquier equipo que cumpla los requisitos de sistema de Windows Vista. Para obtener más información acerca de requisitos específicos de CPU, memoria y disco, consulte la [Guía de planeación de hardware de Windows Vista Enterprise](http://go.microsoft.com/fwlink/?linkid=79962). Aunque Microsoft ha establecido las categorías independientes “PC apto para Windows Vista” y “Equipo preparado para Windows Vista Premium” para el hardware que es compatible con distintas características de Windows Vista, BitLocker funcionará en cualquier equipo compatible con Windows Vista.

Para obtener ventajas de la compatibilidad de BitLocker con el hardware de TPM, los equipos deben incluir la versión 1.2 o superior del hardware de TPM. Muchos fabricantes incluyen la compatibilidad con TPM como parte de sus productos estándar; otros la ofrecen en subconjuntos limitados de sus líneas de equipos portátiles, o no la proporcionan en ningún grado. No existe forma de agregar la compatibilidad con TPM a los equipos que no la tienen. Sin embargo, puede usar una llave USB para almacenar las claves de cifrado de BitLocker en los equipos que no incluyen hardware de TPM.

Los equipos que incluyen hardware de TPM deben incluir también una versión del BIOS que permita a Windows Vista usar el conjunto completo de funciones de TPM. Algunos equipos que poseen la versión 1.2 del hardware de TPM pueden requerir actualizaciones del BIOS si se enviaron antes de enero de 2007. Si desea usar BitLocker con una llave USB, el BIOS debe poder leer dicha llave durante el proceso de arranque.

![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**

Algunas implementaciones del BIOS son compatibles con el arranque del equipo desde USB, pero esta capacidad se deshabilita si el equipo se arranca desde un disco duro u otro dispositivo. Estas implementaciones no son compatibles con BitLocker porque lee la llave USB en una fase posterior del proceso de arranque.

Los equipos protegidos con BitLocker deben tener dos particiones de disco: una para el sistema operativo y los datos, y otra más pequeña que se usará solo cuando se arranque el equipo o durante las actualizaciones del sistema operativo. No debe usar esta partición de inicio para el almacenamiento de otros datos. Microsoft recomienda que la partición de inicio tenga al menos 1,5 GB de espacio disponible. Ambas particiones deben estar formateadas con el sistema de archivos NTFS (NTFS).

Los usuarios de Windows Vista Ultimate pueden usar la Herramienta de preparación de unidad BitLocker de Windows para crear la partición de utilidades de forma dinámica con objeto de usar BitLocker. Los usuarios de la edición Enterprise pueden obtener la Herramienta de preparación de unidad como se describe en el artículo 930063 de Microsoft Knowledge Base, [Descripción de la Herramienta de preparación de unidad BitLocker](http://support.microsoft.com/kb/930063). La obtención de la herramienta precisa llamar a los servicios de soporte al cliente de Microsoft, aunque tanto la llamada como la herramienta son gratuitas. Microsoft no ofrece compatibilidad con la creación o el traslado manual de las particiones para crear la configuración de partición necesaria para BitLocker. Debe realizar una instalación limpia de Windows Vista (con la creación de particiones como parte del proceso de instalación) o bien usar la Herramienta de preparación de unidad.

Si tiene la intención de usar unidades flash USB como parte de la implementación de BitLocker, los modelos que usa deben implementar la especificación de [Transporte "bulk-only" clase almacenamiento masivo USB](http://www.usb.org/developers/devclass_docs/usbmassbulk_10.pdf), en el sitio web de bus serie universal.

###### Descripción del TPM

La mayoría de las organizaciones que implementa BitLocker querrán las ventajas de seguridad que ofrecen los equipos que incluyen hardware de TPM. El conocimiento de este hardware y lo que puede ofrecer es parte importante de la selección de la configuración de BitLocker adecuada para su organización. El análisis detallado del TPM queda fuera del ámbito de esta guía. Para obtener información más concreta acerca de TPM y Trusted Computing Group, consulte la página [Especificaciones del Módulo de plataforma segura (TPM)](https://www.trustedcomputinggroup.org/specs/tpm) en el sitio web de Trusted Computing Group.

Es importante comprender la naturaleza del TPM, que es básicamente un microprocesador con un propósito concreto, con su propio sistema de E/S y almacenamiento integrado. El TPM presenta una clave de aprobación (EK) que se usa para firmar y cifrar datos que proceden directamente del TPM o que se pasan al TPM para que se firmen o cifren. El fabricante del equipo debe cargar la EK en el TPM, o bien se debe cargar automáticamente como parte del proceso de inicialización de BitLocker.

También debe entender que el TPM puede presentar uno de estos estados en un momento determinado:

-   **Habilitado o deshabilitado:** el TPM se puede habilitar o deshabilitar varias veces durante un proceso de inicio. Cuando se habilita el TPM, todas sus características están disponibles. Cuando el TPM está deshabilitado, restringe todas las operaciones, salvo la capacidad de notificar las funciones de TPM y de aceptar las actualizaciones.

-   **Activado o desactivado:** cuando el TPM está activado, todas sus características están disponibles. El estado de desactivado es similar al de deshabilitado, pero aquí es posible cambiar el estado operativo (por ejemplo, se puede cambiar el propietario o la activación por presencia física).

-   **Con o sin propietario:** cuando el sistema operativo toma posesión del TPM, este genera una clave raíz de almacenamiento (SRK), que es un par de claves que se usa para las operaciones de sellado en los volúmenes protegidos. El propietario de un TPM puede realizar todas las operaciones, incluidos los cambios en el estado operativo. BitLocker no puede usar el TPM hasta que esté en estado “con propietario”.

Los estados mencionados se pueden combinar. Por ejemplo, algunos proveedores distribuyen equipos habilitados con TPM y en el estado predeterminado “deshabilitado”, “desactivado” y “sin propietario”. Para usar BitLocker en estos equipos, se debe definir la propiedad del TPM, activarlo y habilitarlo. Estas operaciones se realizan de forma automática al usar la interfaz de usuario estándar de BitLocker. Cuando BitLocker está activado, habilitará, activará y tomará posesión del TPM, si procede.

También deberá comprender el requisito de presencia física para algunas operaciones con el TPM. Las especificaciones de TPM de Trusted Computing Group requieren que una persona interactúe directamente con el equipo físico para ejecutar algunos comandos; además, esta persona no se puede reemplazar ni imitar mediante un script. La presencia física indica que un usuario reivindica la propiedad y está físicamente presente en el equipo para realizar las tareas básicas de administración del TPM, por ejemplo:

-   Habilitar el TPM sin información de propietario.

-   Activar el TPM.

-   Borrar un propietario existente del TPM.

-   Desactivar o deshabilitar temporalmente el TPM.

##### Requisitos de software de BitLocker

Windows Vista está disponible en distintas ediciones, pero solo las ediciones Enterprise y Ultimate son compatibles con BitLocker. Microsoft incluye la característica Windows Anytime Upgrade (descrita en la ayuda en pantalla de Windows Vista), que puede usar para actualizar los equipos individuales. Por ejemplo, puede actualizar Business Edition a Ultimate Edition mediante la característica Windows Anytime Upgrade. Algunos tipos de actualización pueden requerir la reinstalación. Por ejemplo, las actualizaciones de 32 a 64 bits requieren una reinstalación de la versión de 64 bits de Windows Vista.

![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**

La orientación y las herramientas del Kit de herramientas de cifrado de datos para equipos móviles son aplicables a EFS (disponible en Windows XP Professional SP 2 y en todas las versiones de Windows Vista) y a BitLocker (disponible en Windows Vista Enterprise y Windows Vista Ultimate). Sin embargo, en Windows Vista Ultimate no se ha probado rigurosamente la compatibilidad con todas las características de la orientación ni de las herramientas. En principio, el Kit de herramientas está pensado para Windows XP Professional SP 2 y las ediciones Enterprise y Business de Windows Vista.

###### Implementación de Windows Vista

El [Acelerador de solución para Business Desktop Deployment](http://go.microsoft.com/fwlink/?linkid=91187) proporciona orientación y herramientas completas para la implementación de Windows Vista en los equipos cliente de la organización. A medida que planea la estrategia de implementación de Windows Vista, recuerde que, para habilitar BitLocker, será probablemente necesario que intervenga físicamente en cada equipo, ya que el TPM solo se puede inicializar o volver a programar desde la consola del equipo afectado. Asimismo, puede que necesite actualizar el BIOS de los equipos para sacar partido de todas las ventajas de BitLocker.

Una decisión de implementación importante es la actualización de los equipos existentes con Windows XP a Windows Vista, o la realización de una instalación limpia del nuevo sistema operativo. BitLocker no se puede habilitar hasta que no haya instalado Windows Vista. No obstante, debe ser consciente de que BitLocker requiere una configuración de partición de disco especial (como se describe en la [Guía paso a paso para el Cifrado de la unidad BitLocker de Windows](http://go.microsoft.com/fwlink/?linkid=83223). Si debe actualizar los equipos existentes que ejecutan Windows XP, el plan de implementación debe contar con la creación de la estructura de partición necesaria con el fin de activar BitLocker en estos equipos.

El kit de herramientas Business Desktop Deployment (BDD) Toolkit de Windows Vista es compatible con la habilitación automática de BitLocker en algunas circunstancias. Consulte la [Guía de instalación de Lite Touch](http://go.microsoft.com/fwlink/?linkid=78607) para obtener detalles acerca de la forma de usar las herramientas de BDD para habilitar BitLocker como parte del proceso de implementación del sistema operativo.

#### Determinación del ámbito de implementación de BitLocker

Después de evaluar las partes de una organización que tienen hardware y software compatibles con uno o más modos de BitLocker, el siguiente paso es determinar dónde se debe implementar exactamente BitLocker. Para realizar este paso, se deben responder las siguientes preguntas y se debe determinar el ámbito final de la implementación de BitLocker:

-   ¿Qué equipos de la organización necesitan protección? Puede decidirse por proteger algunos o todos los equipos móviles y de escritorio en función de las necesidades de seguridad y del ciclo de implementación.

-   ¿Qué datos de la organización necesitan protección? Es posible que algunas organizaciones deseen proteger todos los datos disponibles, mientras que otras pueden tener requisitos más específicos.

##### ¿Qué equipos requieren protección?

Las decisiones de seguridad suelen implicar una relación protección-costo; la implementación de BitLocker no es una excepción. En principio, puede parecer que la mejor estrategia de seguridad es implementar Windows Vista en todos los equipos cliente de la organización y habilitar BitLocker en ellos. Sin embargo, la mayoría de las organizaciones deberán sincronizar la implementación generalizada de Windows Vista y, por tanto, de BitLocker, con el plan global de implementación de TI. Aun así, todas las organizaciones se pueden beneficiar de la implementación selectiva de Windows Vista y BitLocker en los equipos que presentan un mayor riesgo potencial. Entre estos equipos, se incluyen los siguientes:

-   Equipos de ejecutivos, abogados u otros empleados que trabajan normalmente con datos financieros, legales o estratégicos confidenciales.

-   Equipos de desarrolladores de software, evaluadores, diseñadores de sitios web u otros usuarios que puedan tener acceso a datos personales o financieros de clientes, empleados o asociados comerciales.

-   Equipos de personal de recursos humanos, responsables de seguros, personal médico u otro personal que deba tratar normalmente con información personal confidencial de clientes y empleados.

-   Equipos usados en áreas donde se puedan producir ataques físicos (incluidos el robo de unidades de disco o de todo el equipo).

-   Equipos portátiles que usan los empleados para tener acceso a la información de la compañía o para trabajar con ella mientras están fuera de la oficina.

-   Equipos domésticos o personales de empleados importantes, si estos se usan para trabajar con información de la compañía o para tener acceso a la red de la organización.

Para determinar los equipos de su entorno que precisan protección, emplee un inventario automatizado de los activos (si es posible) para identificar los equipos que pertenecen a los grupos recién mencionados. Puede ser buena idea complementar un inventario automatizado con una comprobación manual de los empleados que trabajan con información confidencial y los equipos de la organización con que normalmente usan. Si su organización usa un conjunto de equipos móviles asignados a ubicaciones concretas, o que los empleados pueden utilizar fuera de la empresa, considere crear con ellos una categoría aparte de equipos que necesitan protección.

##### ¿Qué datos requieren protección?

Una de las principales ventajas de BitLocker es que protege todo el contenido de un volumen del sistema. Esta funcionalidad anula la incertidumbre acerca de los datos que se deben o no se deben cifrar. Todos los archivos que el usuario cree o toque se cifrarán si están almacenados en el volumen del sistema operativo.

No obstante, es importante identificar categorías o clases de datos concretas que puedan necesitar la protección de BitLocker para que pueda identificar mejor los usuarios y los equipos que tienen permiso para procesar dichos tipos de datos. Entre los tipos de datos que pueden beneficiarse de la protección, se incluyen los siguientes:

-   Información empresarial confidencial, incluidos los datos financieros, los planes de productos, la información bancaria o crediticia, y los planes y comunicaciones estratégicos.

-   Información y registros relacionados con pleitos pendientes, pasados o futuros, especialmente si se trata de asuntos confidenciales entre cliente y abogado.

-   Datos personales acerca de empleados, antiguos empleados, jubilados o clientes.

-   Código fuente, bases de datos, información de diseño de autor, material comercial confidencial y otros tipos de información de propiedad intelectual.

-   Material con licencia o propiedad de los socios comerciales u otros otorgantes de licencias que pudieran exigirle que mantenga la confidencialidad de dicha información.

#### Elección de la configuración de BitLocker

En esta fase de la planeación, se determinarán los parámetros apropiados para la organización y se explicará el proceso de implementación y configuración.

La guía *Análisis de seguridad* de este Acelerador de solución contiene una descripción detallada de los métodos de seguridad que se pueden usar con BitLocker para proteger las claves de cifrado de volúmenes. Use la información de la guía *Análisis de seguridad* para elegir los modos de BitLocker apropiados para la organización. La elección de los modos de BitLocker puede depender de la disponibilidad de hardware y software que se ha analizado anteriormente o de los distintos requisitos de seguridad que tienen las distintas partes de la organización. Los modos disponibles son:

-   BitLocker con TPM

-   BitLocker con TPM y NIP

-   BitLocker con dispositivo USB

-   BitLocker con TPM y dispositivo USB

La siguiente ilustración muestra un diagrama para tomar decisiones que puede usar para evaluar las opciones de configuración de BitLocker en su entorno.

![](images/Cc162806.ca97aaca-c63e-43bb-948c-67d3ae965c2e(es-es,TechNet.10).gif)

**Figura 1.1. Diagrama para decidir las opciones de configuración de BitLocker**

El resultado del proceso de decisión se puede parecer al que se muestra en la siguiente tabla. En la información, se deben incluir funciones de hardware, tipos de hardware compatible, y directiva y configuración de BitLocker asociada.

**Tabla 1.1. Directiva y directrices de configuración de BitLocker**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de sistema</th>
<th style="border:1px solid black;" >Directiva y configuración de BitLocker</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Escritorio estándar</td>
<td style="border:1px solid black;">Los equipos usarán el cifrado de BitLocker con un TPM o una llave de inicio USB, según la funcionalidad del hardware. Esta configuración se usará para controlar la exposición de datos y para administrar la retirada de activos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Equipo portátil estándar</td>
<td style="border:1px solid black;">Todos los equipos nuevos usarán un TPM y un NIP. Los equipos sin TPM usarán llaves de inicio en las unidades USB, pero todos los equipos nuevos se comprarán con dispositivos TPM. Esta configuración se usará para controlar la exposición de datos y para administrar la retirada de activos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Equipos portátiles de ejecutivos</td>
<td style="border:1px solid black;">Todos los equipos usarán un TPM con un NIP. Se reemplazarán los equipos existentes que no sean compatibles con TPM.</td>
</tr>
</tbody>
</table>
  
##### Elementos importantes para BitLocker con TPM
  
El modo BitLocker con TPM ofrece protección sin necesidad de que el usuario intervenga; el cifrado de volúmenes, el arranque y el funcionamiento son fáciles de comprender para el usuario. Este modo de BitLocker *no* es normalmente adecuado para la implementación básica de BitLocker y solo se debe considerar en las siguientes situaciones:
  
-   Cuando no se requiere la autenticación multifactor de BitLocker.
  
-   Cuando el valor de los datos no justifica el gasto adicional y/o la complejidad de la autenticación multifactor de BitLocker.
  
##### Plan para BitLocker con TPM
  
Los pasos de planeación para el modo BitLocker con TPM incluyen lo siguiente:
  
-   Un inventario de los equipos de la organización que disponen de hardware de TPM.
  
-   Su ciclo de actualización y sustitución de hardware.
  
-   El modo de funcionamiento de los procesos existentes de actualización de software y administración de revisiones.
  
-   Si tiene razones empresariales u operativas que permitan o denieguen el inicio desatendido de los equipos. BitLocker con TPM permite el inicio desatendido, pero los modos de BitLocker que usan un NIP o una llave USB requieren que se facilite este NIP o esta llave USB durante el proceso de inicio.
  
-   El funcionamiento que presentarán los procesos de soporte técnico (por ejemplo, la reparación de hardware, la sustitución y el retiro) con los sistemas protegidos con BitLocker, ya que es posible que un disco protegido con BitLocker no se pueda usar directamente en un equipo de sustitución.
  
##### Elementos importantes para BitLocker con TPM y NIP
  
BitLocker con TPM y NIP agrega la capacidad de evitar que los usuarios de dominio que no conocen el NIP lean los datos de un equipo protegido. Protege de ataques al equipo que podrían tener éxito si el equipo se arrancara con una pantalla de inicio de sesión.
  
En la fase de planeación, se debe determinar si los usuarios se resistirían a aprender y recordar un NIP adicional y se deben tomar medidas para superar esta dificultad. La seguridad adicional que supone requerir un paso de autenticación adicional hace de esta una buena solución para proteger los activos de valor.
  
##### Plan para BitLocker con TPM y NIP
  
A modo de preparación para usar BitLocker con TPM y NIP, debe seguir todos los pasos de planeación para el modo BitLocker con TPM. También debe crear un plan para:
  
1.  crear documentación para instruir a los usuarios acerca de la forma de crear un NIP correcto que cumpla los requisitos de seguridad de la organización e indique lo que se debe hacer en caso de olvidar el NIP.
  
2.  crear documentación que instruya al personal de soporte técnico acerca de los procedimientos de restablecimiento del NIP.
  
##### Elementos importantes para BitLocker con USB
  
BitLocker con un dispositivo USB ofrece protección a los equipos que no contienen TPM. Este modo proporciona una funcionalidad básica, pero no ofrece la comprobación de integridad durante el arranque, ni tampoco evita que los usuarios de dominio inicien sesión en el equipo y lean los datos después de arrancar el sistema con el dispositivo USB.
  
##### Plan para BitLocker con USB
  
Si tiene pensado usar BitLocker con una llave de inicio USB, deberá realizar las siguientes acciones de planeación:
  
1.  Probar los equipos para garantizar que pueden reconocer el modelo preferido de llave USB en el arranque. Las pruebas de Microsoft indican que algunas marcas de llaves USB presentan tasas de error que superan el 50%, de modo que las pruebas realizadas deben incluir una prueba de confiabilidad. También debe considerar la estandarización a una sola marca de llave para garantizar el acceso seguro a las contraseñas de inicio y de recuperación.
  
2.  Planear la forma en que los usuarios que solo usan BitLocker con una llave USB migrarán al modo BitLocker con TPM y NIP. El plan debe incluir la forma de migración de datos y aplicaciones a los equipos compatibles con TPM o, si los equipos existentes ya son compatibles con TPM, habilitar TPM y volver a habilitar BitLocker.
  
##### Elementos importantes para BitLocker con TPM y USB
  
En este modo, BitLocker proporciona la comprobación de integridad y el cifrado durante el arranque, y el símbolo (token) USB debe estar presente durante el arranque para permitir el arranque del equipo. Los elementos importantes para la planeación en este modo mezclan lo necesario para los modos de solo TPM y solo USB, ya que se debe asegurar de que los equipos pueden usar BitLocker con un TPM, así como prepararse para ser compatibles con el almacenamiento en llaves USB.
  
##### Plan para BitLocker con TPM y USB
  
Si desea usar este modo, debe realizar los mismos pasos de planeación descritos en la sección anterior de este capítulo “Plan para BitLocker con TPM”, así como los pasos de la sección “Plan para BitLocker con USB”.
  
#### Plan para la recuperación de datos
  
BitLocker proporciona un cifrado eficaz de los datos. No existen puertas traseras u otra forma de recuperar los datos de un disco protegido con BitLocker si no dispone de la contraseña de recuperación correcta. Esto aumenta la importancia de la planeación de recuperación, ya que, sin una copia adecuada de la contraseña de recuperación, no podrá recuperar *ningún* dato de un volumen protegido.
  
Durante el inicio del equipo, BitLocker puede detectar condiciones que evitan el desbloqueo de la unidad en la que Windows está instalado. Estas condiciones pueden incluir errores de disco o cambios en los archivos de inicio del equipo, por ejemplo. Si se produce una de estas condiciones, no podrá iniciar la sesión ni tener acceso a los archivos protegidos hasta que desbloquee el volumen mediante el uso de la contraseña de recuperación de BitLocker. Si intenta instalar el disco duro en otro equipo, seguirá necesitando la contraseña de recuperación de BitLocker.
  
Existen cuatro estrategias básicas de almacenamiento de contraseñas de recuperación:
  
-   Imprimir la contraseña.
  
-   Almacenar la contraseña en un medio extraíble.
  
-   Almacenar la contraseña en una ubicación de almacenamiento de red.
  
-   Almacenar la contraseña en Active Directory.
  
Microsoft recomienda que elija una combinación de los métodos de recuperación para su entorno. Puesto que no es posible recuperar volúmenes de BitLocker sin la contraseña, el almacenamiento de las contraseñas de recuperación mediante un único método supone un punto débil en el proceso de recuperación de datos. Todos los métodos presentan ventajas y desventajas; debe asegurarse de haber comprendido estas cuestiones cuando elija un método.
  
##### 
  
###### Active Directory
  
Microsoft recomienda encarecidamente que planee e implemente el almacenamiento de Active Directory de contraseñas de recuperación para los equipos protegidos con BitLocker. Mediante este método, la información de recuperación se almacena como atributo en el objeto de equipo de Active Directory. La información de recuperación incluye una contraseña de recuperación para cada volumen habilitado con BitLocker, la contraseña de propietario de TPM y la información necesaria para identificar los equipos y los volúmenes a los que se aplica la información de recuperación. De forma opcional, también puede guardar un paquete que contenga las claves reales usadas para cifrar los datos, así como la contraseña de recuperación necesaria para tener acceso a estas claves. Este método de almacenamiento de contraseñas de recuperación presenta las siguientes ventajas en comparación con otros métodos de almacenamiento:
  
-   El proceso de almacenamiento se automatiza y no requiere la intervención del usuario.
  
-   El usuario no puede perder ni dañar la información de recuperación.
  
-   Active Directory proporciona auditoría y control centralizados para el almacenamiento y el uso de la información de recuperación.
  
-   Se crean copias de seguridad de la información de recuperación y se protege junto con otros datos valiosos de Active Directory.
  
-   Se puede tener acceso a la información de recuperación de forma remota, con lo que la recuperación se puede realizar en otro lugar y con ayuda del personal de soporte técnico.
  
El uso de Active Directory para almacenar contraseñas de recuperación de BitLocker introduce los siguientes requisitos:
  
-   La organización debe contar con una infraestructura de Active Directory sólida y bien administrada.
  
-   Se debe extender el esquema de Active Directory de Windows Server® 2003 con objeto de incluir atributos y objetos de BitLocker. La planeación de la extensión del esquema de Active Directory es una tarea de gran envergadura. Para obtener más información acerca de la extensión del esquema de Active Directory, consulte [Extensión del esquema de Active Directory en Windows Server 2003 R2](http://technet.microsoft.com/es-es/library/cc664691.aspx).
  
-   El administrador debe habilitar la configuración de la directiva de grupo para habilitar la copia de seguridad de la contraseña de recuperación de BitLocker.
  
-   Debe existir una directiva lo suficientemente amplia y suficientes medidas de seguridad para el personal con objeto de ofrecer un almacenamiento seguro y un acceso controlado al material de recuperación almacenado en Active Directory.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Los equipos en los que el modo de recuperación se inicia de forma inesperada pueden haber sufrido un ataque de malware. Debe asegurarse de que el personal de soporte técnico examina los equipos en los que el modo de recuperación se inicia sin causa conocida antes de que el usuario ejecute la recuperación.
  
###### Método de impresión o almacenamiento en archivo
  
La impresión de la contraseña de recuperación o su almacenamiento en un archivo son procesos sencillos que presentan algunas ventajas importantes:
  
-   Facilidad de uso.
  
-   Se requiere una infraestructura mínima.
  
-   Administración sencilla para los usuarios sin conocimientos técnicos.
  
Sin embargo, también presentan grandes desventajas:
  
-   Confían en el usuario para administrar la contraseña de recuperación y evitar su pérdida y el compromiso de su seguridad.
  
-   El almacenamiento de las contraseñas mediante estos métodos no ofrece control ni auditoría centralizados.
  
-   No existe una protección eficaz para evitar que el archivo guardado o la copia impresa se pierdan o dañen.
  
###### Método de almacenamiento en dispositivo USB
  
El almacenamiento de la contraseña de recuperación en un dispositivo USB ofrece las siguientes ventajas:
  
-   Puede almacenar varias contraseñas de recuperación en un único dispositivo USB porque se trata de simples archivos de texto.
  
-   Es más fácil aplicar medidas y barreras de seguridad físicas para proteger las contraseñas.
  
-   La separación de la llave USB del equipo proporciona una forma de mantener las obligaciones separadas.
  
Sin embargo, este método también presenta algunas desventajas:
  
-   No todos los equipos son compatibles con la instalación de dispositivos USB durante los procesos anterior al arranque y de arranque.
  
-   La recopilación y el almacenamiento de contraseñas de recuperación constituyen un proceso manual que debe realizar cada sujeto en su equipo.
  
-   No existe control ni auditoría centralizados para este método.
  
-   El dispositivo USB se puede perder o dañar, o puede dar error.
  
###### Definición de una directiva de recuperación
  
Es importante definir una directiva que indique quién puede recuperar los datos de un equipo protegido con BitLocker. La recuperación de BitLocker requiere el acceso físico al equipo para poder escribir la contraseña de recuperación. Este requisito influye significativamente en el proceso de definición de una directiva de recuperación, ya que es posible que necesite habilitar escenarios en los que un usuario remoto o móvil precise acceso a un volumen protegido con BitLocker cuando este está fuera de la oficina.
  
De manera predeterminada, todos los administradores de dominio pueden leer las contraseñas de recuperación de BitLocker que están almacenadas en los Servicios de dominio de Active Directory (AD DS). Estos administradores pueden delegar esta capacidad en otros usuarios si les asignan los permisos “controlar acceso” y “propiedad de lectura”. De igual modo, los administradores pueden delegar la capacidad de lectura de la información de propietario de TPM almacenada. Por ejemplo, puede otorgar al soporte técnico o al personal de soporté técnico por teléfono la capacidad de tener acceso a las contraseñas de recuperación de los usuarios. Sin embargo, antes de hacerlo, debe asegurarse de que permitir este acceso no infringe las directivas de seguridad de su organización, ya que cualquier usuario que tiene acceso a la contraseña de recuperación de un volumen puede leer los datos del volumen sin limitaciones.
  
Antes de indicar un método de recuperación obligatorio, asegúrese de que cumple los requisitos previos necesarios para el método concreto. Estos requisitos previos son:
  
-   Para llaves USB, asegúrese de que el sistema implicado puede leer dispositivos USB durante el arranque. Asimismo, pruebe en un equipo simbólico para estar seguro que la marca estándar de llave USB funciona correctamente con BitLocker antes de la implementación generalizada. Asegúrese de tener la llave USB a mano cuando habilite BitLocker por primera vez.
  
-   Para otras ubicaciones de almacenamiento, asegúrese de que la contraseña de recuperación está a disposición de los usuarios cuando necesiten ejecutar una recuperación. No use una ubicación de almacenamiento alternativa en el mismo equipo, ya que no se podrá obtener acceso al mismo durante el proceso de recuperación. Evite el uso de recursos compartidos de red que no se puedan asegurar adecuadamente contra el acceso de usuarios malintencionados o sospechosos.
  
-   Si desea imprimir la contraseña de recuperación, asegúrese de que haya conectada una impresora local o de red cuando vaya a habilitar BitLocker. Asegúrese también de planear lo que se debe hacer con la contraseña impresa (los registros en papel están sujetos a riesgos y amenazas).
  
-   El almacenamiento de las contraseñas de recuperación de Active Directory requiere su propio conjunto de pasos preparatorios (que se describen en el próximo capítulo).
  
#### Plan para la capacidad de administración
  
Un paso importante en el proceso de planeación de BitLocker es decidir la forma en que BitLocker afectará a los procesos de administración de TI de la organización. BitLocker afecta a los siguientes procesos en curso que tienen lugar en cualquier organización:
  
-   Administración de las actualizaciones de software
  
-   Actualizaciones y sustituciones de hardware
  
-   Integración con software de creación de imágenes, copias de seguridad y antimalware
  
-   Administración de la configuración de BitLocker
  
-   Retiro de equipos
  
##### Administración de las actualizaciones de software
  
Tres escenarios principales de administración de actualización de software afectan a la planeación para la implementación de BitLocker.
  
En el primer escenario, están implicadas las actualizaciones del BIOS. BitLocker controla los cambios que se producen en una serie de componentes, incluidos algunos aspectos de la configuración del BIOS. Si alguno de estos parámetros cambia inesperadamente, BitLocker aplicará obligatoriamente una recuperación en cada nuevo arranque. Para evitar este problema, debe deshabilitar BitLocker antes de actualizar el BIOS del sistema, actualizar el BIOS y, a continuación, volver a habilitar BitLocker.
  
En el segundo escenario, están implicadas las actualizaciones o las revisiones de Windows Vista. Si BitLocker está habilitado con un TPM, existen otros dos escenarios secundarios:
  
-   Las actualizaciones que afectan a la administración de arranque, al cargador de arranque del sistema operativo, a la aplicación que se usa para reanudar las operaciones desde una hibernación o a la aplicación de diagnóstico de memoria. Cuando BitLocker detecta que Windows Update ha modificado uno o más de estos componentes, actualiza la información de configuración para reflejar las nuevas versiones.
  
-   Las actualizaciones que afectan a otros componentes de Windows se aplican en función de los mecanismos de actualización habituales de Windows, que no afectan a los parámetros que mide BitLocker.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Si BitLocker está habilitado pero no se usa el TPM, no existe una ruta de acceso segura para la integridad durante el arranque y las actualizaciones de sistema no pueden aplicar obligatoriamente una recuperación o una actualización de la configuración.
  
En el tercer escenario, están implicadas las actualizaciones de versión o edición (por ejemplo, de Windows Vista Enterprise a Windows Vista Ultimate). En un escenario así, deberá descifrar la unidad y deshabilitar BitLocker antes de aplicar la actualización. Una vez completada la actualización, puede habilitar BitLocker y volver a cifrar la unidad.
  
##### Actualizaciones y sustituciones de hardware
  
Un volumen de disco cifrado con BitLocker no se puede montar ni leer en otro equipo, a menos que tenga acceso a la contraseña de recuperación. Al arrancar Windows Vista, puede recuperar el volumen escribiendo la contraseña de recuperación para que el proceso de arranque pueda continuar. Esta funcionalidad puede requerir cambios en la directiva de reparación y actualización de hardware. Los cambios específicos pueden variar en función de la forma y el momento en que reemplace los equipos, de si usa software de creación de imágenes de disco o de copias de seguridad para pasar los datos de un equipo a otro y de la forma de otorgar acceso a los datos de recuperación de BitLocker.
  
##### Integración con software de creación de imágenes, copias de seguridad y antimalware
  
BitLocker cifra los datos del volumen de disco. Los programas o las utilidades que obtienen acceso al disco directamente mientras Windows no se está ejecutando podrán leer datos del disco, pero los datos estarán cifrados. Por ejemplo, las herramientas de creación de imágenes pueden capturar el contenido cifrado de un disco protegido con BitLocker, pero no el contenido de texto sin formato.
  
La mayoría de las herramientas de copias de seguridad, restauración y antimalware que se aplican durante la ejecución de Windows funcionarán de la forma prevista en un equipo que usa BitLocker.
  
Además, las herramientas que cambian los archivos de sistema de Windows o modifican los parámetros de configuración pueden hacer que BitLocker solicite una contraseña de recuperación en el siguiente arranque. Los cambios de directiva, como cambiar del modo de solo TPM a TPM con NIP, también pueden activar el proceso de recuperación. Para obtener más información acerca del efecto que tiene el cifrado de BitLocker en la administración de las actualizaciones de software, consulte el [Capítulo 3: operaciones y escenarios de recuperación](https://technet.microsoft.com/es-es/library/01754723-3e94-4bec-8284-02e2a4e91593(v=TechNet.10)) de esta guía.
  
##### Administración de la configuración de BitLocker
  
Junto con la directiva de grupo, BitLocker es compatible con el uso de scripting para controlar y administrar el comportamiento básico de la tecnología. Para obtener más información acerca de interfaces de scripting como ProtectKeyWithTPM, consulte el documento [Introducción técnica al Cifrado de unidad BitLocker](http://go.microsoft.com/fwlink/?linkid=77977). Algunas organizaciones pueden decidirse por emplear scripting para aplicar la directiva de BitLocker, mientras que otras elegirán la directiva de grupo. Esta decisión se debe tomar relativamente pronto en el proceso de planeación.
  
Las opciones de control de BitLocker disponibles en la Consola de administración de directivas de grupo de Windows Vista (o en otros equipos que tengan instaladas las plantillas administrativas de Windows Vista) permiten controlar lo siguiente:
  
-   Si se realizan automáticamente copias de seguridad de las claves de BitLocker en Active Directory.
  
-   La ubicación predeterminada usada para almacenar las claves de recuperación.
  
-   Si los usuarios pueden cambiar las opciones de recuperación e inicio.
  
-   El método de cifrado que usa BitLocker.
  
-   La forma en que se realiza la validación de plataforma de TPM.
  
En lo que queda de sección, se describen todos los parámetros de la plantilla. Puede obtener acceso a estos parámetros en **\\Configuración del equipo\\Configuración administrativa\\Cifrado de unidad BitLocker**.
  
###### Activar copia de seguridad de BitLocker en los Servicios de directorio de Active Directory
  
Esta configuración de directiva permite administrar la copia de seguridad de los Servicios de dominio de Active Directory (AD DS) de la información de recuperación del Cifrado de unidad BitLocker. De manera predeterminada, este parámetro aparece como **No configurado**. Si habilita esta configuración de directiva, se realizará una copia de seguridad automática y silenciosa de la información de recuperación de BitLocker en AD DS cuando BitLocker se active en un equipo.
  
La información de recuperación de BitLocker incluye la contraseña de recuperación y algunos datos de identificación únicos. También puede especificar que Windows debe realizar una copia de seguridad de un paquete de claves de recuperación, que contiene la clave de cifrado del volumen protegido con BitLocker y la contraseña de recuperación. Este paquete de claves viene asegurado por la contraseña de recuperación y puede ayudar a realizar una recuperación especializada cuando el disco está dañado.
  
Si selecciona la opción **Requerir copia de seguridad de BitLocker en AD** **DS**, BitLocker no se podrá activar, a menos que el equipo esté conectado al dominio y la copia de seguridad en AD DS se realice correctamente. Esta opción está seleccionada de manera predeterminada para asegurar que se puede realizar la recuperación de BitLocker. Si desactiva esta opción, BitLocker seguirá intentando registrar las claves de recuperación en Active Directory pero, si el registro no se realiza correctamente, la instalación de BitLocker puede proseguir. La copia de seguridad no se volverá a intentar de forma automática, y es posible que la contraseña de recuperación no se haya almacenado en AD DS durante la instalación de BitLocker.
  
![](images/Cc162806.important(es-es,TechNet.10).gif)**Importante:**
  
Para evitar la pérdida de datos, debe disponer de una forma de recuperar BitLocker. Si deshabilita o no configura esta configuración de directiva, no se realizará una copia de seguridad de la información de recuperación de BitLocker en AD DS.
  
###### Configuración del Panel de control: configurar carpeta de recuperación
  
Esta configuración de directiva permite especificar la ruta de acceso predeterminada que se mostrará cuando el Asistente para la instalación del Cifrado de unidad BitLocker solicite al usuario la ubicación de una carpeta en la que guardar la contraseña de recuperación.
  
Si habilita esta configuración de directiva, puede especificar la ruta de acceso que se usará como ubicación de carpeta predeterminada cuando el usuario elija la opción de guardar la contraseña de recuperación en una carpeta. Puede especificar una ruta de acceso completa o incluir las variables de entorno del equipo de destino en la ruta de acceso. Si la ruta de acceso no es válida, el Asistente para la instalación de BitLocker mostrará la vista de carpetas del equipo desde el nivel superior.
  
Si deshabilita o no configura esta configuración de directiva, el Asistente para la instalación de BitLocker mostrará la vista de carpetas del equipo desde el nivel superior cuando el usuario elija la opción de guardar la contraseña de recuperación en una carpeta.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
El usuario siempre podrá seleccionar otras carpetas para guardar la contraseña de recuperación.
  
###### Configuración del Panel de control: configurar opciones de recuperación
  
Esta configuración de directiva permite configurar si el Asistente para la instalación del Cifrado de unidad BitLocker solicita al usuario guardar las opciones de recuperación de BitLocker.
  
Los usuarios tienen dos opciones de recuperación para desbloquear el acceso a los datos cifrados con BitLocker:
  
-   Escribir una contraseña de recuperación numérica de 48 dígitos generada al azar.
  
-   Insertar una unidad flash USB que contenga una clave de recuperación de 256 bits generada al azar.
  
Las claves o las contraseñas de recuperación se generan durante la instalación de BitLocker. Si habilita esta configuración de directiva, podrá configurar las opciones que el Asistente para la instalación muestra a los usuarios a la hora de recuperar BitLocker. Por ejemplo, al denegar la contraseña de recuperación de 48 dígitos se evita que los usuarios puedan imprimir o guardar información de recuperación en una carpeta.
  
Si deshabilita o no configura esta configuración de directiva, el Asistente para la instalación de BitLocker ofrece a los usuarios varias formas de almacenar las opciones de recuperación. Si se utiliza una unidad flash USB, la contraseña de recuperación de 48 dígitos se almacena como archivo de texto, y la clave de recuperación de 256 bits se guarda como archivo oculto. Si se utiliza una carpeta, la contraseña de recuperación de 48 dígitos se almacena como archivo de texto. La opción de impresión proporcionará la contraseña de recuperación de 48 dígitos.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Si la inicialización del TPM es necesaria durante la instalación de BitLocker, la información de propietario de TPM se guardará o imprimirá con la información de recuperación de BitLocker.
  
###### Configuración del Panel de control: habilitar opciones de inicio avanzadas
  
Esta configuración de directiva permite configurar si el Asistente para la instalación del Cifrado de unidad BitLocker solicita al usuario configurar una autenticación adicional que se solicitará siempre que se inicie el equipo. Mediante esta configuración de directiva, puede controlar los siguientes aspectos del inicio de BitLocker:
  
-   La configuración **Permitir BitLocker sin un TPM compatible** controla si se puede usar BitLocker en equipos que no tienen un TPM compatible. En los equipos sin TPM, debe usar un dispositivo USB para conservar la clave de inicio, lo que significa que el equipo debe ser capaz de leer un dispositivo USB durante el arranque. Sin un TPM, los datos cifrados con BitLocker están protegidos únicamente por el material de clave de esta unidad flash USB.
  
-   En un equipo con un TPM compatible, puede seleccionar los métodos de inicio que estarán disponibles para los usuarios. Cuando el equipo se inicia, puede requerir al usuario que inserte una unidad flash USB que contenga la clave de inicio. También puede requerir que se escriba un NIP de inicio de 4 a 20 dígitos.
  
Si habilita esta configuración de directiva, el asistente mostrará una página que permite al usuario configurar opciones avanzadas de inicio para BitLocker. También puede configurar opciones de configuración para equipos con o sin TPM.
  
Si deshabilita o no configura esta configuración de directiva, el Asistente para la instalación de BitLocker mostrará los pasos básicos que permiten a los usuarios habilitar BitLocker en equipos con un TPM. En este asistente básico, no se pueden configurar claves o NIP de inicio adicionales.
  
Si desea usar BitLocker sin TPM, o con TPM más un NIP o una clave de inicio, asegúrese de que la directiva del equipo local (o la directiva de grupo en vigor acumulativa) está configurada para las opciones de inicio avanzadas (consulte la siguiente ilustración). Esta configuración se debe establecer antes de habilitar BitLocker y se puede encontrar en **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Cifrado de unidad BitLocker\\Configuración del Panel de Control: habilitar opciones de inicio avanzadas**.
  
![](images/Cc162806.01e06e8d-fc15-49cd-a09c-ed805d2c1655(es-es,TechNet.10).gif)
  
**Figura 1.2. Habilitar opciones de inicio avanzadas**
  
###### Configurar método de cifrado
  
Esta configuración de directiva permite configurar el algoritmo y el tamaño de clave que usa BitLocker. Esta configuración de directiva se aplica a discos completamente descifrados. El cambio del método de cifrado no tiene efecto alguno si el disco ya está cifrado o si el cifrado está en curso. La configuración de directiva tiene cuatro opciones:
  
-   Los estándares AES 128 bits y AES 256 bits usan el algoritmo del Estándar de cifrado avanzado (AES) de la norma FIPS con la seguridad de clave especificada.
  
-   Los estándares AES 128 bits con difusor y AES 256 bits con difusor agregan el algoritmo Difusor descrito en la guía *Análisis de seguridad*. El nivel del difusor agrega algunas propiedades de seguridad adecuadas para la configuración de cifrado de disco pero el modo de encadenamiento de bloques de cifrado (CBC) de AES no las proporciona directamente.
  
Si habilita esta configuración de directiva, puede configurar el método de cifrado que se usa para cifrar un volumen sin cifrar. Si deshabilita o no configura esta configuración de directiva, BitLocker usará el método de cifrado predeterminado AES 128 bits con difusor o el método de cifrado especificado por un script de instalación del administrador local.
  
###### Impedir la sobrescritura de memoria al reiniciar
  
Esta configuración de directiva controla el rendimiento de reinicio del equipo con el riesgo de exponer datos confidenciales de BitLocker. Estos datos incluyen el material de clave que se usa para cifrar información. Esta configuración de directiva se aplica solo cuando la protección de BitLocker está habilitada.
  
Si habilita esta configuración de directiva, Microsoft Windows no exige al equipo la sobrescritura de memoria durante el reinicio. Esto puede mejorar el rendimiento de reinicio, pero aumenta el riesgo de exposición de datos confidenciales de BitLocker.
  
Si deshabilita o no configura esta configuración de directiva, Windows ayuda a garantizar que los datos confidenciales de BitLocker se quitan de la memoria al reiniciar el equipo. De manera predeterminada, está directiva no está configurada.
  
###### Configurar perfil de validación de plataforma de TPM
  
Esta configuración de directiva permite configurar la forma en que el hardware de seguridad de TPM del equipo protege la clave de cifrado de BitLocker. Esta configuración de directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya se ha activado con protección de TPM.
  
Si habilita esta configuración de directiva antes de activar BitLocker, puede configurar los componentes de arranque que el TPM valida antes de desbloquear el acceso al volumen del sistema operativo cifrado por BitLocker. Si algunos de estos componentes cambian mientras la protección de BitLocker está activada, el TPM no revelará la clave de cifrado para desbloquear el volumen y el equipo pasará a modo de recuperación durante el arranque.
  
Si deshabilita o no establece esta configuración de directiva, el TPM usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de instalación de un administrador local. El perfil de validación de plataforma predeterminado protege la clave de cifrado de los cambios en CRTM (Core Root of Trust of Measurement), BIOS y extensiones de la plataforma (PCR 0), Código ROM de opción (PCR 2), Código de registro de arranque maestro (MBR) (PCR 4), Sector de arranque de NTFS (PCR 8), Bloque de arranque de NTFS (PCR 9), Administrador de arranque (PCR 10) y Control de acceso de BitLocker (PCR 11).
  
![](images/Cc162806.important(es-es,TechNet.10).gif)**Importante:**
  
El cambio del perfil predeterminado afecta a la seguridad y capacidad de administración del equipo. La sensibilidad de BitLocker a las modificaciones de plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión de los PCR, respectivamente.
  
##### Retiro de equipos
  
Debe incluir el retiro de equipos como parte de la planeación. Por ejemplo, ¿qué hará cuando sea necesario volver a asignar, sacar de la organización o desechar un equipo protegido con BitLocker por un error de hardware? Gracias al nivel de seguridad del algoritmo AES que usa BitLocker, borrar la contraseña de recuperación evita de forma eficaz el acceso a un volumen protegido. Considere directivas y procedimientos que le ayuden a asegurarse de que todos los protectores se quitan de Active Directory y de otras ubicaciones al retirar un equipo. Para obtener más información acerca de la forma de quitar los protectores para el retiro, consulte [Cifrado de unidad BitLocker y sanitización de discos](http://go.microsoft.com/fwlink/?linkid=80648).
  
#### Plan para las posibilidades de uso
  
BitLocker está diseñado para ofrecer un alto nivel de seguridad, al tiempo que permanece transparente para los usuarios durante las operaciones habituales. Sin embargo, los usuarios deben conocer una serie de cosas para usar BitLocker de forma eficaz y segura. Debe desarrollar una directiva de cifrado escrita que describa el uso, los requisitos y las cuestiones operativas en relación al cifrado. Los usuarios y el personal de soporte técnico deben ser instruidos acerca del uso correcto del cifrado antes de su implementación.
  
Una directiva de cifrado debe tratar las cuestiones relacionadas con el uso del cifrado para la protección de información confidencial, por ejemplo:
  
-   El tipo de información que se debe cifrar.
  
-   Los tipos de equipos que deben usar cifrado (por ejemplo, equipos de escritorio y portátiles).
  
-   Las soluciones de cifrado de datos compatibles (por ejemplo, EFS y BitLocker).
  
-   Los problemas que el cifrado puede y no puede solucionar.
  
-   La forma en que las claves y las contraseñas de recuperación se deben y no se deben almacenar.
  
-   La persona que tiene la custodia de las claves y las contraseñas de recuperación y el acceso a las mismas.
  
-   Los usuarios que pueden y deben asegurar el uso apropiado del cifrado.
  
-   Las responsabilidades de los usuarios relacionadas con la conservación de las contraseñas de recuperación de sus equipos.
  
-   Los posibles problemas relacionados con el cifrado, como la pérdida de datos.
  
-   Los pasos que los usuarios deben realizar para cifrar archivos.
  
-   La persona responsable de la recuperación de los datos cifrados y la forma en que los usuarios pueden iniciar una recuperación.
  
-   La forma en que los usuarios pueden obtener soporte técnico para los problemas de cifrado.
  
Use los canales de aprendizaje habituales para compartir información acerca del cifrado con los usuarios, incluidas fuentes en línea y en papel, con lecciones prácticas y clases teóricas, si fuera necesario. Esta tarea se puede desarrollar de forma paralela con el resto del proceso de implementación.
  
#### Plan para la implementación de Active Directory y la directiva de grupo
  
El resultado de los pasos de planeación anteriores describe la medida en que se usará Active Directory para ayudar a administrar el entorno de BitLocker. Entre las posibilidades, se incluyen las siguientes:
  
-   Uso de Active Directory para almacenar el TPM y las contraseñas de recuperación.
  
-   Administración de los parámetros y las configuraciones de BitLocker mediante la directiva de grupo.
  
##### Plan para el almacenamiento de las contraseñas de recuperación en Active Directory
  
Como se ha analizado anteriormente en la sección “Plan para la recuperación de datos”, el uso de Active Directory para almacenar contraseñas de recuperación requiere una extensión del esquema de Active Directory. La implementación de esta extensión es una tarea de gran envergadura y se debe planear adecuadamente antes de la implementación de BitLocker para asegurarse de que la extensión del esquema se realiza correctamente y de que el entorno es estable.
  
El proceso de planeación para las acciones de Active Directory en BitLocker debe incluir también análisis y decisiones acerca de las personas que se designarán como operadores para la recuperación de claves y datos. Un punto clave es considerar si la función del operador para la recuperación se separará de las funciones de administrador de dominio y administrador de empresa. Algunas organizaciones con requisitos exigentes de segregación de obligaciones deben separar estas funciones, y otras (probablemente las más pequeñas) permitirán que los administradores de dominio realicen la recuperación de claves y datos por el simple hecho de que estas personas ya tienen formación acerca de complejas tareas técnicas de administración con Active Directory.
  
##### Control del cifrado de datos de BitLocker con directivas de grupo
  
Los pasos de planeación anteriores determinan las opciones de directiva de grupo relacionadas con BitLocker que se usarán. Las opciones de directiva de grupo que se deben planear son:
  
-   La forma en que Active Directory almacena el TPM y las contraseñas de recuperación.
  
-   Los mecanismos de recuperación que se habilitan o deshabilitan.
  
-   La configuración predeterminada de BitLocker para la longitud y el nivel de seguridad del cifrado.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Plan para el Sistema de cifrado de archivos
  
Para completar un plan de implementación de EFS, se deben realizar las siguientes acciones:
  
1.  Comprender las opciones de implementación de EFS.
  
2.  Evaluar el grado de preparación para implementar EFS.
  
3.  Determinar el ámbito de implementación de EFS.
  
4.  Elegir la configuración de EFS.
  
5.  Planear la recuperación de claves y datos.
  
6.  Planear la capacidad de administración.
  
7.  Planear las posibilidades de uso.
  
8.  Planear la implementación de Active Directory y la directiva de grupo.
  
#### Descripción de las opciones de implementación de EFS
  
EFS mitiga eficazmente distintas amenazas contra la seguridad. Para conocer las amenazas que EFS puede mitigar y otras amenazas que EFS puede mitigar junto con BitLocker, es necesario que comprenda el modelo de seguridad de EFS y las opciones de implementación compatibles. En el documento de *Análisis de seguridad* incluido en el Kit de herramientas, se enumeran una serie de riesgos y el modo en que EFS los mitiga. Se debe familiarizar por completo con su contenido antes de continuar con el proceso de planeación.
  
#### Evaluación del grado de preparación para implementar EFS
  
Antes de que pueda crear un plan para implementar EFS, debe evaluar lo preparada que está la organización para implementar y usar EFS.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Puede simplificar mucho los planes de implementación de EFS si usa la característica de credenciales móviles de Active Directory. Para obtener más información, consulte la página [Descripción de las credenciales móviles](http://technet.microsoft.com/es-es/library/cc783542.aspx) de Microsoft TechNet.
  
##### Requisitos de hardware y software
  
EFS no necesita hardware especial aparte de un equipo que pueda ejecutar una versión del sistema operativo Windows que sea compatible con EFS. Esta guía no ofrece información detallada acerca del uso de EFS en un sistema operativo que no sea Windows XP Professional o las versiones Business, Enterprise o Ultimate de Windows Vista.
  
##### Requisitos adicionales
  
Además de los requisitos de hardware y software enumerados anteriormente, EFS necesita lo siguiente:
  
-   Todos los equipos participantes deben ejecutar Windows XP o Windows Vista.
  
-   Los archivos y las carpetas que desea cifrar deben estar almacenados en volúmenes con formato NTFS.
  
-   Los usuarios que cifren archivos deben tener permisos de modificación de NTFS sobre el archivo o la carpeta que vayan a cifrar.
  
-   Se debe comprobar que las aplicaciones que abran y modifiquen archivos protegidos con EFS son compatibles con EFS. Por lo general, todas las aplicaciones Win32® de Microsoft son compatibles con EFS. La mayoría de los problemas de compatibilidad se producen con aplicaciones heredadas de 16 bits, aunque se debe prestar especial atención a las aplicaciones que tienen acceso al sistema de archivos de alguna forma especial (incluidos los paquetes antivirus, las aplicaciones de copia de seguridad y los desfragmentadores).
  
#### Determinación del ámbito de implementación de EFS
  
La planeación de la implementación de EFS implica decisiones con respecto a la designación de los equipos y los usuarios que usarán EFS, y sobre los datos de cada equipo que se deben proteger con EFS. EFS se puede usar en la mayoría de equipos basados en Windows, por lo que un proceso analítico que comienza con la selección de los datos que se deben proteger y que, a continuación, identifica los usuarios que tienen copias de estos datos y los equipos que los contienen, puede definir íntegramente el ámbito de una implementación de EFS.
  
Reflexione acerca de las siguientes cuestiones, que le ayudarán a identificar los datos que debe proteger:
  
-   Si los datos se dañan o modifican, ya sea con mala intención o por accidente, ¿cuánto trabajo habría que invertir en recuperarlos o volver a crearlos?
  
-   Si los datos no se pueden recuperar ni volver a crear, ¿cuál es la repercusión financiera para su organización?
  
-   Si los datos se exponen o revelan de forma indebida, ¿quedaría su organización en mal lugar?
  
-   ¿Cuál sería el costo de la exposición pública de estos datos?
  
-   ¿Sería el hecho de que se produjera la exposición igual de perjudicial que la exposición del contenido mismo?
  
-   Si un intruso con malas intenciones obtiene estos datos sin que se perciba, ¿de qué forma se podrían usar estos datos para perturbar el desarrollo de la compañía, dejarla en mal lugar, timarla, estafarla o incomodarla de cualquier otro modo?
  
-   ¿Cuánto le costaría a la organización cada uno de estos escenarios?
  
Estos son algunos ejemplos de datos que se deben cifrar:
  
-   Contratos, negociaciones, RFP, solicitudes de presupuesto y presupuestos generados por clientes o proveedores
  
-   Listas de precios, programas de descuentos y otros tipos de información relacionada con los precios
  
-   Información de contacto de empleados, clientes y clientes potenciales
  
-   Notas de reuniones y presentaciones
  
-   Manuales y memorandos de directivas
  
-   Diseños y configuraciones
  
-   Investigaciones y análisis competitivos
  
-   Datos protegidos legalmente (por ejemplo, información de identificación personal de clientes)
  
El propósito de esta lista es estimular hábitos de pensamiento con conciencia acerca de la seguridad; no se trata de una lista completa.
  
##### Archivos y carpetas que no se pueden cifrar con EFS
  
Hay muchos archivos y carpetas que no se pueden cifrar con EFS, independientemente de los permisos que tenga el usuario. Para proteger al usuario de un estado no operativo, Windows evita de forma específica el cifrado de elementos críticos que no se deben cifrar. Entre estos archivos y carpetas, se incluyen:
  
-   Los archivos de arranque críticos para el sistema de la carpeta raíz
  
-   %Windir% y todos los objetos secundarios
  
-   Archivos relacionados con los perfiles de usuario (es decir, Ntuser.\*)
  
-   %APPDATA%
  
-   \\Boot (en Windows Vista)
  
-   \\$Recycle.Bin
  
-   Todos los archivos y las carpetas marcados con el atributo de sistema
  
-   Archivos de hibernación
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Algunas de estas carpetas permiten que se cifren algunos de los archivos que contienen, se excluyen simplemente los archivos críticos.
  
Se deniega de forma explícita el cifrado de la mayoría de los archivos y las carpetas que no se pueden cifrar con EFS para proteger al usuario y al equipo participante. Por ejemplo, las claves de descifrado de EFS privadas del usuario se almacenan en el perfil del usuario. Si el usuario pudiera cifrar su perfil de usuario, no habría forma de que Windows obtuviera la clave de descifrado para descifrar el perfil de usuario. Por lo tanto, Windows bloquea el cifrado de estos archivos por parte de los usuarios.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Puede usar BitLocker para cifrar archivos de sistema críticos de forma previa al arranque.
  
Windows Vista permite cifrar algunos archivos y carpetas críticos que no se podían cifrar en versiones anteriores de Windows, incluido el archivo de paginación del sistema (**pagefile.sys**).
  
##### Archivos y carpetas que no debe cifrar
  
Hay otros tipos de archivos y carpetas que los usuarios, por norma general, no deben cifrar, incluso si el sistema operativo lo permite. Algunos ejemplos son:
  
-   Archivos que se vayan a compartir (a menos que esté habilitado el uso compartido de EFS)
  
-   La carpeta \\Archivos de programa y sus subcarpetas
  
-   Bases de datos compartidas, incluidas las bases de datos de Microsoft Exchange Server
  
-   Archivos generados en un equipo para su consumo o procesamiento en otro (a menos que esté habilitado el uso compartido de EFS)
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Los archivos de bases de datos compartidas no se deben cifrar porque se debe cifrar el archivo de modo que todos los usuarios, así como el programa de base de datos, puedan tener acceso al mismo. Los archivos de base de datos están mejor protegidos con el cifrado específico de campo/atributo.
  
##### Identificación de datos y ubicaciones de datos
  
Un escenario de EFS común es la protección de texto, gráficos, hojas de cálculo y documentos de presentación creados por productos como Microsoft Office. Se debe realizar una encuesta para averiguar si todos los usuarios de la organización usan la ubicación predeterminada de estos documentos. Si es así, planee el cifrado de esta carpeta completa en cada equipo para protegerla.
  
Además, la carpeta %TEMP% se debe cifrar para proteger todos los archivos de aplicación temporales que se puedan crear en esta carpeta.
  
Se deben examinar otras aplicaciones que interactúan con información confidencial para determinar dónde se almacenan los datos que crean.
  
Una vez identificadas las ubicaciones de la información confidencial y de los datos de aplicaciones, se debe redactar un borrador de directiva para informar a los usuarios de la forma de habilitar el cifrado en estas carpetas. También se debe desarrollar un plan para configurar e implementar la automatización de directivas con el fin de habilitar el cifrado de forma automática.
  
##### Estructuras comunes de directorios cifrados
  
Probablemente se sorprenda al averiguar dónde guardan los usuarios los archivos con información confidencial. La función principal de esta tarea no es especificar, por ejemplo, que los usuarios deben guardar documentos en Mis documentos\\Confidencial, sino asegurarse de que no los almacenan en directorios que no se deben o pueden cifrar, como C:\\ o C:\\WINDOWS.
  
La creación de una estructura de directorios común para todos los equipos portátiles protegidos simplificará el mantenimiento. El enfoque más sencillo, por supuesto, es el establecimiento de una directiva para conservar todos los documentos en Mis documentos y el cifrado de todo el árbol de Mis documentos. Aunque este enfoque pueda ser suficiente para muchas organizaciones, algunas lo considerarán demasiado restrictivo y definirán directivas más complejas y flexibles.
  
Algunas aplicaciones crean archivos temporales o de almacenamiento en caché que pueden contener información confidencial. Es posible que pueda usar EFS y la herramienta Asistente para EFS que acompaña a esta guía para proteger los directorios que contienen estos archivos. No obstante, deberá probar las aplicaciones para asegurarse de que funcionan correctamente cuando se cifran sus directorios temporales o de almacenamiento en caché.
  
#### Elección de las opciones de configuración de EFS
  
Una vez determinado el ámbito de la implementación de EFS, el siguiente paso del proceso de planeación es la elección de las opciones y la configuración de EFS para los equipos de la organización. Algunas de las opciones que se deben considerar y planear son:
  
-   Decidir si se van a usar certificados emitidos por la CA o certificados autofirmados.
  
-   Decidir si se van a usar tarjetas inteligentes para el almacenamiento de certificados y claves de EFS.
  
-   Elegir el tamaño de algoritmos y claves de cifrado.
  
-   La capacidad de evitar que EFS use certificados autofirmados cuando no hay ninguna entidad de certificación (CA).
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Esta característica está incluida en Windows Vista. Para usarla en Windows XP, consulte el artículo 912761 de Microsoft Knowledge Base, [Sistema de archivos cifrados genera un certificado con firma automática cuando intenta cifrar un archivo EFS en un equipo con Windows XP](http://support.microsoft.com/kb/912761).
  
Los equipos con Windows Vista ofrecen varias opciones adicionales, incluidas las siguientes funciones:
  
-   Cifrado del contenido de la carpeta Documentos del usuario
  
-   Uso obligado de una tarjeta inteligente para EFS
  
-   Uso directo de la tarjeta inteligente para todas las operaciones de cifrado
  
-   Habilitación del cifrado del archivo de paginación
  
-   Visualización de notificaciones de copia de seguridad de claves cuando se crea o cambia una clave de usuario
  
Algunas de las opciones de configuración son solo posibles en Windows Vista, por lo que es posible que deba planear una actualización del sistema operativo en determinados equipos de acuerdo con los requisitos de seguridad para parte de la organización.
  
##### Elección de una estrategia de certificados digitales
  
Los certificados digitales EFS se pueden autofirmar o emitir desde una CA de confianza. La primera vez que un usuario intenta cifrar un archivo o una carpeta con EFS, Windows realiza una comprobación para ver si cuenta con un certificado y una clave que pueda usar. Si no es así, Windows intenta ponerse en contacto con una entidad de certificación para obtener un certificado y una clave. Si no se pudiera, Windows generaría un certificado autofirmado para el usuario. Un certificado autofirmado es aquel en el que el certificado digital no tiene una entidad de firmas de confianza de mayor nivel que certifique su autenticidad. De forma general, los terceros no deben confiar de forma externa en los certificados digitales autofirmados. No obstante, los certificados digitales autofirmados suelen ser adecuados para aplicaciones internas como EFS.
  
En general, los certificados digitales EFS autofirmados son más fáciles de implementar en un principio y más difíciles de administrar desde un punto de vista operativo. Se deben elegir certificados generados por entidades de certificación si ya se han implementado los servicios PKI adecuados.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Se recomienda encarecidamente que las empresas sin plataforma PKI consideren la implementación de los Servicios de Certificate Server antes de habilitar y usar EFS. Los Servicios de Certificate Server están disponibles en Microsoft Windows 2000 Server y en productos de servidor posteriores. Los beneficios en la administración del ciclo de vida de los certificados digitales EFS y la automatización de una solución de recuperación disminuirán el esfuerzo y los costos totales.
  
Se puede usar una directiva de grupo o una directiva de equipo local para permitir o deshabilitar la capacidad que tiene un equipo de generar un certificado EFS autofirmado cuando no hay presente una CA participante. En la sección siguiente, se comenta esta opción.
  
Los administradores deben estudiar las ventajas y las desventajas de todos los métodos de emisión de certificados digitales y tomar una decisión fundamentada acerca del uso de una u otra solución. La tarea de cambiar el método de cadena de confianza de los certificados digitales EFS después de haber implementado EFS inicialmente podría ser muy pesada.
  
###### Ventajas y desventajas de los certificados EFS autofirmados
  
Los certificados autofirmados son la forma más fácil de establecer una infraestructura funcional para EFS. Los certificados autofirmados se emiten automáticamente para los clientes de EFS si no se detecta ninguna CA de PKI participante y compatible. La generación y la instalación de certificados digitales autofirmados son procesos rápidos y transparentes para el usuario participante. De manera predeterminada, los certificados autofirmados tienen un período de validez de 100 años.
  
No obstante, los certificados digitales autofirmados tienen desventajas significativas, entre las que se incluyen las siguientes:
  
-   El largo período de validez de los certificados digitales autofirmados aumenta las probabilidades de que se comprometa su seguridad.
  
-   La revocación de los certificados digitales autofirmados implica mayor trabajo, ya que es necesario revocarlos en cada uno de los equipos individuales, en vez de hacerlo en una CA central.
  
-   El uso compartido de archivos cifrados es más difícil. Dado que los certificados autofirmados no se publican en Active Directory, no son accesibles en otros equipos a menos que se trasladen de forma manual.
  
-   Es más complicado automatizar el archivado de claves, ya que no existe una ubicación centralizada para realizar esta operación.
  
###### Ventajas y desventajas de los certificados EFS emitidos desde una entidad de certificación
  
La emisión de certificados EFS desde una CA centralizada tiene algunos beneficios convincentes. Este método ofrece una administración centralizada de los certificados digitales y disminuye el riesgo de seguridad porque los certificados digitales generados tienen un período de vida útil más corto. Las tareas de renovación, revocación, cambio de claves y archivado son más fáciles de automatizar gracias a que el material de claves y certificados sigue siendo accesible a través de la CA. También puede ajustar varios parámetros de certificado mediante la modificación de la plantilla de certificado. Además, puede publicar los certificados en Active Directory para facilitar que los usuarios localicen los certificados de otros usuarios con el fin de realizar un uso compartido de archivos cifrados con EFS.
  
No obstante, los certificados EFS emitidos desde una CA tienen sus propias desventajas. En primer lugar, debe implementar una CA participante compatible con EFS antes de implementar EFS. En segundo lugar, al ser más corto el período de validez de los certificados emitidos desde una CA, es necesario cambiar las claves de los certificados con mayor frecuencia. Y, lo que es más importante, los equipos con Windows emiten sus propios certificados EFS autofirmados si no logran ponerse en contacto con una CA participante. Esta capacidad podría derivar en un entorno en el que se mezclan los certificados autofirmados y los firmados por una CA, lo que complicaría la administración de los certificados digitales EFS. Puede resolver este posible problema mediante la configuración de una directiva de grupo para deshabilitar el uso de certificados autofirmados para EFS o mediante la deshabilitación completa de EFS hasta que implemente los servicios de CA necesarios.
  
Si planea usar la inscripción automática con objeto de emitir certificados de cliente para su uso con EFS, lea atentamente la sección “Plan para la implementación de Active Directory y la directiva de grupo” más adelante en este mismo capítulo. Debe asegurarse de que la infraestructura de Active Directory que tiene será compatible con la inscripción automática (para la que necesitará al menos un controlador de dominio de Windows Server 2003 en su bosque).
  
##### EFS y las tarjetas inteligentes
  
Tanto Windows XP como Windows Vista son compatibles con el uso de tarjetas inteligentes con EFS. Como se describe en *Análisis de seguridad*, el uso de tarjetas inteligentes con EFS ayuda a reducir el riesgo de que un atacante obtenga la contraseña de un usuario y la use para iniciar sesión en un equipo y recuperar archivos protegidos con EFS, uno de los principales factores de riesgo de EFS. El uso obligado de tarjetas inteligentes con EFS ayuda de forma eficaz a aportar un mayor grado de protección, aunque las formas de obligar a hacer uso de las tarjetas inteligentes con EFS son diferentes en Windows XP y Windows Vista.
  
En Windows XP, se puede pedir la tarjeta inteligente para iniciar sesión. También se puede pedir para desbloquear un escritorio inactivo o bloqueado. En este escenario, la protección adicional de las claves de EFS la aporta la presencia obligada de la tarjeta inteligente, que es la única forma de desbloquear las claves de EFS y usarlas en los archivos.
  
En Windows Vista, se puede pedir la tarjeta inteligente para iniciar sesión y para el desbloqueo. No obstante, es posible obligar a que la tarjeta esté presente cada vez que se cifre o descifre un archivo protegido con EFS. De manera predeterminada, Windows Vista deriva una clave criptográfica y la almacena en caché para su uso en operaciones con EFS. Para mayor seguridad, en lugar de esto, Windows Vista puede usar la tarjeta inteligente directamente en cada operación de cifrado. No obstante, este enfoque es menos apropiado para los usuarios y es más lento que el modo de clave almacenada en caché, por lo que es posible que no sea conveniente en algunos entornos.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Para obtener más información acerca de los modos de EFS compatibles con Windows Vista y Windows XP, consulte el “Capítulo 3: Sistema de cifrado de archivos” en *Análisis de seguridad*.
  
###### Ventajas de las tarjetas inteligentes
  
Las tarjetas inteligentes están diseñadas para ofrecer un alto nivel de seguridad de cifrado en un paquete portátil y físicamente seguro. Aumentan la seguridad gracias a que transfieren las operaciones de firma, comprobación, cifrado y descifrado del equipo host a la propia tarjeta inteligente. Las claves criptográficas se almacenan de forma segura en la tarjeta inteligente y, por lo general, se las considera a salvo de todos los atacantes, a excepción de los más sofisticados y acaudalados. Los certificados asociados a una tarjeta inteligente se pueden usar para un gran número de mejoras de seguridad, incluida la protección S/MIME para el correo electrónico, la autenticación basada en certificados para las aplicaciones web y el acceso remoto, así como un inicio de sesión de escritorio más seguro. El hecho de exigir el uso de tarjetas inteligentes obliga principalmente al uso de una autenticación de dos factores, ya que cualquier usuario que desee autenticarse debe poseer la tarjeta y la frase de contraseña o el NIP. Además, no hace falta configurar sistemas de credenciales móviles, ya que las credenciales de cada usuario se almacenan en la tarjeta.
  
###### Desventajas de las tarjetas inteligentes
  
Las tarjetas inteligentes tienen algunos inconvenientes destacables. En primer lugar, es necesaria la implementación de las propias tarjetas junto con los lectores, que pueden resultar demasiado caros para algunas organizaciones. El mecanismo de control y emisión de certificados de las tarjetas se debe integrar con una PKI, lo que puede aumentar el costo y la complejidad de las implementaciones de las tarjetas inteligentes. Las organizaciones que usan tarjetas inteligentes también deben implementar procedimientos para emitir las tarjetas y realizar un seguimiento de las mismas, una actividad relacionada con la seguridad que se debe administrar con cuidado para evitar la introducción de vulnerabilidades. Se puede implementar [Identity Lifecycle Manager 2007](http://www.microsoft.com/windowsserver/ilm2007) (ILM 2007) de Microsoft para ayudar a que se realice el proceso de implementación de tarjetas inteligentes sin problemas.
  
##### Elección de un algoritmo de cifrado
  
Se puede implementar EFS con varios cifrados y claves de diferentes niveles de seguridad. Es importante comprender que el tipo de cifrado y el nivel de seguridad de las claves se pueden elegir en dos objetos de EFS *diferentes*: la clave asimétrica de EFS personal del usuario y la clave de cifrado de archivos (FEK) simétrica compartida de los archivos. Todos los archivos protegidos con EFS tienen una única FEK simétrica. Los datos de archivo de cada archivo protegido con EFS se cifran con la FEK del archivo.
  
A cada usuario autorizado (o agente de recuperación) se le asigna una copia de la FEK del archivo, que se cifra con la clave pública contenida en el certificado EFS del usuario (y solo se puede descifrar con la clave privada correspondiente del usuario). Cuando el usuario necesita acceso a un archivo protegido con EFS, la clave de cifrado de EFS asimétrica, privada y personal del usuario se usa para descifrar la copia cifrada del usuario de la FEK del archivo. La FEK simétrica, que ahora está sin cifrar, se usa para descifrar el archivo protegido con EFS. Es importante comprender la diferencia entre los dos tipos de claves de EFS a la hora de decidir el tipo de cifrado y el nivel de seguridad de la clave.
  
###### Cifrados compatibles
  
Los algoritmos de cifrado para FEK incluyen, en orden ascendente de seguridad:
  
-   Estándar de cifrado de datos (DES)
  
-   Estándar de cifrado de datos ampliado (DESX)
  
-   Estándar de cifrado de datos triple (3DES)
  
-   Estándar de cifrado avanzado (AES)
  
Windows Vista, Windows XP Professional (SP1 y superior) y Windows Server 2003 usan el cifrado AES de alta seguridad de manera predeterminada. Las versiones anteriores de Windows XP Professional usan DESX de manera predeterminada, aunque se puede cambiar al cifrado 3DES de mayor seguridad. Para ello, se debe habilitar la opción de directiva de seguridad **Usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** en la directiva de grupo, la directiva de equipo local o mediante la edición directa del Registro. Windows 2000 usa los cifrados DES o DESX para EFS. DESX se usa de manera automática en cualquier versión de Windows 2000 SP1 o posterior.
  
Si se habilita la opción de la norma FIPS en Windows XP Professional SP1 (o en versiones posteriores) o en Windows Server 2003, la protección de cifrado cambia de AES a 3DES. Sin embargo, si se habilita la opción de la norma FIPS, los servidores de Internet Information Service (IIS) y los clientes de Internet Explorer® de Microsoft deben usar la Seguridad de la capa de transporte (TLS) en vez de la Capa de sockets seguros (SSL) de menor seguridad para las transacciones web seguras. También se puede exigir el uso de TLS de mayor seguridad en el servidor, sin habilitar el nivel de seguridad de la norma FIPS ni disminuir la seguridad de la clave simétrica en los clientes con Windows XP heredado.
  
El algoritmo de cifrado asimétrico predeterminado usado para cifrar las claves FEK es RSA, tanto para las claves autofirmadas como para las claves emitidas por una entidad de certificación basada en Microsoft.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
El algoritmo predeterminado usado es siempre el cifrado más seguro disponible en el momento concreto. Cada versión de Windows es capaz de administrar todos los cifrados compatibles con las versiones anteriores. Microsoft recomienda que no cambie la configuración de cifrado para EFS, excepto por razones normativas o de cumplimiento.
  
###### Tamaños de las claves de EFS
  
Windows XP y Windows Vista ofrecen flexibilidad en cuanto al tamaño de la clave de cifrado FEK del archivo y de la clave asimétrica del usuario, aunque hay menos flexibilidad en cuanto al tamaño de la clave FEK. La elección del algoritmo de cifrado de FEK determina el nivel de seguridad de la clave simétrica de FEK. El uso de claves de mayor tamaño puede dar lugar a una mayor protección de EFS, pero también podría tener como consecuencia un mayor detrimento del rendimiento, según el algoritmo que se use.
  
**Tamaños de la clave asimétrica de usuario**
  
En general, el tamaño de la clave asimétrica de EFS puede oscilar entre los 1024 y los 16384 bits. Los tamaños de clave comunes son: 1024, 2048, 4096, 8192 y 16384 bits. En Windows Vista, el tamaño de clave predeterminado es de 2048 bits, lo que ofrece la suficiente seguridad para casi todas las aplicaciones de EFS. Microsoft recomienda encarecidamente que mantenga el tamaño de clave predeterminado para las nuevas implementaciones de EFS. Las versiones anteriores de Windows usaban un tamaño de clave predeterminado de 1024 bits.
  
**Tamaños de FEK simétrica**
  
Los cifrados de la clave FEK simétrica de EFS suelen oscilar entre los 56 bits en las versiones anteriores de Windows y los cifrados AES de 256 bits en Windows Vista. Windows 2000 usa claves DESX de 128 bits cuando está instalado High Encryption Pack o SP1 (o posterior); en otros casos, se usa una clave de 56 bits. Windows XP SP1 (o posterior) y Windows Server 2003 usan AES de 256 bits de manera predeterminada. Antes de SP1, Windows XP usaba DESX, pero se podía configurar para usar 3DES de 168 bits.
  
En general, a la mayoría de los usuarios les suele bastar con permitir que se usen los cifrados de la clave FEK de EFS. No obstante, algunas organizaciones necesitan algoritmos de cifrado anteriores o tamaños de clave personalizados.
  
##### EFS y Windows Vista
  
Windows Vista ofrece algunas mejoras significativas para EFS. Debe tener en cuenta dónde y cómo implementa Windows Vista para usar correctamente estas mejoras, entre las que se incluyen:
  
-   La capacidad de exigir el uso de una tarjeta inteligente para EFS. Esta funcionalidad ofrece un grado de seguridad significativo y beneficios de facilidad de uso, dado que EFS se puede administrar con el proceso existente usado para administrar tarjetas inteligentes.
  
-   La capacidad de hacer un uso directo de la tarjeta inteligente para todas las operaciones de cifrado (modo sin intercambio en caché) o permitir que Windows almacene una clave criptográfica derivada (modo de intercambio en caché). Estos modos, que se describen con detalle en el “Capítulo 3: Sistema de cifrado de archivos” en *Análisis de seguridad*, permiten mantener el equilibrio entre la seguridad, el rendimiento y la comodidad del usuario.
  
-   La capacidad de cifrar el archivo de paginación del sistema. Esta funcionalidad ayuda a proteger de la revelación accidental de información confidencial mediante métodos al evitar que un atacante pueda inspeccionar el archivo de paginación mientras Windows no se está ejecutando.
  
-   La capacidad de recordar a los usuarios que realicen copias de seguridad de las claves cuando actualicen las claves existentes o creen otras nuevas.
  
-   La capacidad de evitar que los usuarios creen certificados autofirmados propios para su uso con EFS cuando no hay una CA disponible. Esta funcionalidad permite limitar el uso de EFS fuera de la infraestructura de claves públicas.
  
Si estas características son importantes para su organización, debe reflexionar acerca de la forma de coordinar la implementación de EFS y la implementación de Windows Vista. El Asistente para implementar Windows permite habilitar BitLocker como parte de la implementación de Lite Touch. El equivalente en EFS es habilitar la inscripción automática para los certificados de usuario y, a continuación, instalar el Asistente para EFS (ya sea como parte de la imagen de Windows Vista o a través de otros medios) para que los archivos confidenciales se puedan proteger automáticamente.
  
##### Uso compartido de archivos y EFS
  
A partir de Windows XP Professional, los archivos y las carpetas con protección EFS se pueden compartir con otros usuarios. El primer usuario (o Agente de recuperación de datos de EFS) que cifra un archivo o una carpeta debe agregar a los demás usuarios al archivo o a la carpeta. Los demás usuarios deben contar con certificados digitales EFS válidos.
  
Es posible que otros usuarios que tienen permisos de escritura, eliminación o modificación puedan modificar o eliminar archivos y carpetas protegidos con EFS, incluso si no tienen la capacidad de cifrar o descifrar estos mismos archivos o carpetas. EFS protege la confidencialidad (es decir, los usuarios no autorizados no pueden leer, ver ni imprimir archivos protegidos), pero es posible que sí puedan manipular de algún otro modo el archivo sin ver o leer su contenido. Si la capacidad de compartir archivos entre varios usuarios es importante, debe asegurarse de que las directivas corporativas sean claras acerca de las personas que son responsables de cifrar archivos, a las que se les permite leerlos y las que tienen autoridad para agregar o quitar usuarios compartidos de los archivos cifrados.
  
#### Plan para la recuperación de claves y datos
  
Las organizaciones que decidan implementar EFS deberán planear cuidadosamente la forma de recuperar datos en determinadas situaciones, como los casos en que un usuario se marcha de la organización o tiene bloqueado el acceso a su estación de trabajo, y cuando las claves y el certificado EFS están dañados. Las tareas de planeación más importantes para la recuperación de datos de EFS están documentadas en la sección “Protección y recuperación de datos en Windows XP/[Información general acerca de la recuperación de datos](http://www.microsoft.com/technet/prodtechnol/winxppro/support/dataprot.mspx)” de la documentación de Windows XP. Esta sección ofrece orientación adicional acerca de las cuestiones que debe tener en cuenta durante la planeación.
  
EFS es una solución de cifrado de archivos segura. Si las claves de cifrado usadas para descifrar los archivos protegidos dejan de estar disponibles, es posible que los archivos protegidos también dejen de estar disponibles. Si no hay ninguna copia de seguridad de los datos en forma no cifrada o, si no se ha implementado ningún método de recuperación de cifrado, los archivos protegidos podrían dejar de estar disponibles de forma permanente.
  
Como se ha comentado anteriormente en esta guía, EFS usa una combinación de algoritmos de claves simétricas y asimétricas (públicas y privadas) para proteger los datos. En el escenario predeterminado, se genera una clave de cifrado de archivos (FEK) simétrica que, a continuación, se cifra usando la clave pública de un certificado X.509. Hay dos enfoques diferentes para aplicar una estrategia de copia de seguridad de los datos cifrados con EFS:
  
-   La creación de copias de seguridad de las claves privadas asociadas al certificado X.509. Se suele hacer referencia a este enfoque como recuperación de claves porque hace hincapié en la protección del material de clave como forma de conservar el acceso a los archivos protegidos.
  
-   La creación de copias cifradas adicionales de la clave FEK copiada con diferentes certificados. Se suele hacer referencia a este enfoque como recuperación de datos porque permite recuperar datos incluso si se pierde la clave o el certificado originales.
  
##### Recuperación de claves
  
La recuperación de claves implica que la parte de clave privada de un par de claves pública y privada se puede archivar y recuperar si es necesario. Si la copia de la clave privada del usuario se pierde o daña, independientemente de si está almacenada en una tarjeta inteligente o en un equipo local, se puede recuperar la clave a partir de la ubicación de la copia de seguridad. Después de recuperar una clave privada, se pueden descifrar todos los datos (o, para ser más precisos, todas las claves simétricas cifradas, como la clave FEK). En Windows, se puede realizar esta función de dos formas: a través de agentes Key Recovery Agent o del archivado manual de las claves.
  
###### Mediante Key Recovery Agent
  
Si se usan los Servicios de Certificate Server u otra CA compatible, se puede usar un Key Recovery Agent (KRA) para que recupere los archivos. La entidad de certificación puede archivar automáticamente certificados digitales EFS a medida que los emite, y se puede usar el KRA para recuperar las claves de EFS perdidas de este archivo. La principal diferencia operativa entre un DRA de EFS y un KRA es que los agentes DRA de EFS tienen acceso explícito a todos los archivos protegidos con EFS participantes, mientras que los agentes KRA solo pueden recuperar copias almacenadas de las claves de otras personas. Los agentes KRA también participan en los eventos de recuperación de claves de certificados digitales más allá del ámbito de EFS.
  
El archivado de claves automático se realiza como parte del proceso de inscripción de certificados si las plantillas de certificado se configuran para exigir el archivado de claves. Cuando se configura de esta manera, la clave privada se envía a la CA como parte de la solicitud de certificado y la CA archiva automáticamente la clave privada.
  
Para obtener más información acerca de la planeación e implementación de un mecanismo de archivado y recuperación de claves, consulte [Archivado y administración de claves en Windows Server 2003](http://technet.microsoft.com/es-es/library/cc755395.aspx).
  
###### Archivado manual de claves
  
Si la implementación de EFS está basada en certificados autofirmados, el archivado manual de claves constituye la única forma de realizar copias de seguridad de la clave privada que se necesita para descifrar la FEK. De manera predeterminada, todos los usuarios de EFS pueden realizar una copia de seguridad de su certificado digital EFS y de la clave de descifrado de EFS privada. Windows Vista pide a los usuarios que realicen copias de seguridad de sus claves cuando las crean o las cambian. Todas las versiones de Windows posteriores a Windows 2000 permiten que los usuarios realicen manualmente copias de seguridad de sus claves de EFS usando dos o más métodos. Si se lo permite la directiva de seguridad, los usuarios deben realizar copias de seguridad de sus claves de EFS y almacenarlas en dos o más ubicaciones seguras e independientes usando medios de almacenamiento de confianza.
  
Con el archivado manual de claves, los usuarios exportan manualmente las claves privadas y las envían a un administrador de CA que, después, las importa a la base de datos protegida de la CA.
  
Este enfoque permite que los usuarios sean los responsables de sus propias claves de recuperación. No obstante, esto es difícil de controlar y regular en las organizaciones grandes, y no existe ninguna forma segura de determinar si un usuario ha archivado o no una clave de EFS, y tanto un hecho como el otro puede ser importante para el cumplimiento de la directiva.
  
##### Recuperación de datos
  
La recuperación de datos es un proceso algo diferente del que no forma parte el archivado de las claves asociadas a un certificado X.509 concreto. Por el contrario, este proceso crea rutas redundantes para obtener acceso a un archivo cifrado mediante la creación de claves FEK cifradas adicionales, cada una de ellas cifrada con la clave pública de un certificado X.509 diferente. Las claves adicionales creadas por este proceso se conocen como agentes de recuperación de datos.
  
Cuando se cifra un archivo, Windows realiza automáticamente una copia de la clave FEK del archivo y la cifra con la clave de EFS pública del DRA. Esta funcionalidad implica que un DRA puede descifrar cualquier archivo protegido con EFS.
  
La principal ventaja de un DRA es que todos los archivos protegidos con EFS tienen automáticamente una copia de la clave FEK del archivo creada de manera predeterminada. No es necesario que el usuario realice manualmente copias de seguridad de las claves. La mayor desventaja es que, si se compromete la seguridad de la cuenta de usuario del DRA, el intruso puede tener acceso a los archivos protegidos con EFS.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
Se deben usar métodos que aumenten la seguridad para proteger las cuentas de usuario de los agentes DRA. Además, se puede exportar y almacenar externamente la clave de recuperación de EFS del agente de recuperación para evitar que la seguridad de EFS quede comprometida, si así sucede con la cuenta del agente. La clave de recuperación de EFS se puede importar en el futuro en caso necesario.
  
Mediante la implementación de la recuperación de datos y de agentes de recuperación de datos, se cifra la clave de cifrado de todos los archivos cifrados mediante la clave pública del DRA junto con la clave pública del usuario. Con la clave privada asociada, un DRA designado puede descifrar cualquier archivo cifrado en el ámbito de la directiva de recuperación de EFS.
  
##### Definición de una directiva de recuperación
  
La directiva de recuperación indica la persona a la que se le permite recuperar datos y las circunstancias en las que se pueden realizar las recuperaciones, y es una parte fundamental de la planeación de EFS. La directiva debe definir:
  
-   los usuarios o las funciones que pueden recuperar datos para sí mismos.
  
-   los usuarios o las funciones que pueden recuperar datos de otros usuarios.
  
-   los controles empresariales o normativos que se aplican a la recuperación de datos.
  
-   la forma de auditar el uso de las herramientas de recuperación de datos para asegurarse de que no se les da el uso incorrecto.
  
-   la forma de reunir, almacenar y proteger los materiales de contraseña de recuperación.
  
-   las estaciones de trabajo o los recursos que se pueden usar para realizar operaciones de recuperación.
  
Siempre que sea posible, Microsoft recomienda que elija uno de los dos procedimientos recomendados para su directiva de recuperación. El método preferido de recuperación es la emisión de un certificado de DRA en una tarjeta inteligente y, a continuación, la protección independiente de la tarjeta inteligente y de su NIP. Un equipo con Windows Vista puede usar esta tarjeta inteligente y el certificado asociado para recuperar datos de un cliente en el dominio. Esta combinación ofrece un alto nivel de protección de dos factores para las credenciales de DRA y puede aplicar un acceso independiente a la tarjeta inteligente y al NIP para garantizar la separación de las tareas de recuperación.
  
En entornos en los que esto no sea posible, Microsoft recomienda que defina y configure equipos independientes que se usen solo para la recuperación de datos. Estas estaciones de recuperación deben estar protegidas físicamente y se les debe aplicar medidas adicionales de auditoría y seguridad, de acuerdo con el valor de los datos que se pudieran recuperar.
  
###### Plan para la expiración de los agentes DRA
  
Los agentes de recuperación de datos de EFS usan certificados que, como cualquier otro certificado, tienen fecha de expiración. No obstante, los certificados convencionales se usan normalmente para ofrecer confidencialidad directa: protegen el material que debe permanecer cifrado durante un período de tiempo. Para preservar la confidencialidad directa, es necesario que la clave asociada al certificado expire en el futuro de forma que se pueda cambiar.
  
Los agentes DRA proporcionan la acción contraria a la confidencialidad directa: permiten que se puedan recuperar los datos antiguos. Esta funcionalidad implica que un certificado de DRA expirado sigue siendo útil para la recuperación de los datos que se cifraron durante el período de validez del certificado de DRA. Para conservar la capacidad de recuperar datos independientemente de su antigüedad, debe planear el archivo de los certificados de DRA en un medio de almacenamiento seguro para que se puedan usar cuando sea necesario.
  
Cuando un certificado de DRA expira, puede volver a emitirlo o cambiar la clave. Después, el DRA se puede usar para recuperar los datos recién cifrados. Sin embargo, debe mantener una copia del certificado de DRA anterior para recuperar los datos protegidos con el DRA anterior. Al desarrollar procedimientos y directivas para el control (o prevención) de la expiración de DRA, considere lo siguiente:
  
-   Si se ha producido la expiración de algún certificado de DRA activo, aunque sea uno solo (incluso si el cliente ha configurado varios certificados de DRA), Windows denegará el cifrado de nuevos archivos. Esta funcionalidad implica que una organización debe asegurarse de que emite nuevos certificados de DRA y reemplaza los certificados que vayan a expirar pronto con la suficiente antelación para que la latencia de la directiva de grupo no permita que ningún cliente tenga un certificado de DRA expirado.
  
-   La sustitución de los certificados de DRA (y los pasos posteriores, aunque opcionales, necesarios para actualizar los archivos de cliente) es un proceso sencillo, aunque compuesto por varios pasos.
  
-   Los objetos de directiva de grupo (GPO) que configuran agentes DRA deben contener más de un DRA. Este enfoque ofrece protección redundante ante la pérdida de datos causada por la pérdida de acceso a una única clave privada de DRA.
  
###### Determinación del nivel de directiva de recuperación de datos
  
Una directiva de recuperación predeterminada se aplica automáticamente en el dominio cuando el administrador inicia sesión en el controlador de dominio por primera vez, lo que convierte al administrador en el agente de recuperación del dominio. Windows XP, Windows Vista y Windows Server 2003 ya no necesitan que se aplique ninguna directiva de recuperación para cifrar archivos.
  
La directiva de recuperación predeterminada está configurada de forma local en los equipos independientes. En los equipos que son parte de un dominio de Active Directory, la directiva de recuperación está configurada en el sitio, el dominio, la unidad organizativa o el equipo individual, y se aplica a todos los equipos basados en Windows 2000, Windows Server 2003, Windows XP y Windows Vista en el ámbito de influencia definido. Una CA puede emitir certificados de recuperación y se pueden administrar mediante el complemento Certificados de Microsoft Management Console.
  
En un entorno de red, el administrador de dominio controla la forma en que se implementa EFS en la directiva de recuperación para todos los usuarios y los equipos del ámbito de influencia. En una instalación de Active Directory predeterminada, cuando se configura el primer controlador de dominio, el administrador del dominio es el agente de recuperación específico del dominio. La forma en que el administrador de dominio configura la directiva de recuperación determina la forma en que se implementa EFS para los usuarios de los equipos locales. Para cambiar la directiva de recuperación del dominio, el administrador de dominio usa el editor de la directiva de grupo desde cualquier servidor o equipo cliente conectado al dominio. En los equipos independientes (no unidos a un dominio), el período de expiración de un certificado de DRA autoemitido de la cuenta de administrador es de 100 años. En los equipos unidos a un dominio, el certificado de DRA predeterminado emitido para el administrador del dominio tiene un período de expiración de tres años.
  
Los administradores pueden definir uno de estos tres tipos de directiva:
  
-   **Directiva de agente de recuperación:** cuando un administrador agrega uno o más agentes de recuperación, se activa una directiva de agente de recuperación. Estos agentes son responsables de la recuperación de los datos cifrados en el ámbito de administración. Las directivas de agente de recuperación constituyen la clase más común de directiva de recuperación. Las directivas de agente de recuperación se pueden usar para distribuir la carga de trabajo administrativo en la organización y pueden designar cuentas de recuperación de EFS alternativas para las categorías de equipos agrupados por unidades organizativas. También puede configurar parámetros de agentes de recuperación de datos cifrados para los equipos portátiles de modo que usen los mismos certificados de agente de recuperación cuando se conecten al dominio que cuando operan como equipos independientes.
  
-   **Directiva de recuperación vacía:** cuando un administrador elimina todos los agentes de recuperación y sus certificados de clave pública, se activa una directiva de recuperación vacía. La directiva de recuperación vacía implica que no existe ningún agente de recuperación y, si el sistema operativo cliente es Windows 2000, EFS se deshabilita en esta configuración. El cliente de Windows XP permite que EFS funcione con una directiva de DRA vacía.
  
-   **Directiva de recuperación nula:** cuando un administrador elimina las claves privadas asociadas a una directiva de recuperación dada, entra en vigor una directiva de recuperación nula. No hay disponible ninguna clave privada, por lo que no hay ninguna forma de usar un agente de recuperación, con lo cual la recuperación no es posible. Este tipo de directiva puede ser útil para aquellas organizaciones con un entorno en el que se combinan clientes de Windows 2000 y de Windows XP que no necesitan recuperar datos.
  
Aunque el administrador de dominio es el DRA predeterminado en un entorno de Active Directory, esta función debe ser delegada o asignada a uno o más usuarios.
  
##### Elección del mecanismo adecuado
  
Se pueden usar estrategias de recuperación de claves y de recuperación de datos de forma separada o conjunta. Hay muchas cuestiones operativas y de seguridad en las que hay que pensar. Se puede encontrar información adicional en [Archivado y administración de claves en Windows Server 2003](http://technet.microsoft.com/es-es/library/cc755395.aspx). Se recomienda encarecidamente que examine esta información antes de decidir la estrategia o la combinación de estrategias que va a usar.
  
#### Plan para la capacidad de administración
  
Un paso importante en el proceso de planeación de EFS es la decisión acerca de la forma en que EFS afecta a los procesos de administración de TI de la organización. EFS afecta a los siguientes procesos continuos que se encuentran en una organización:
  
-   Integración con software de creación de imágenes, copias de seguridad y antimalware
  
-   Plan para el uso compartido de archivos y EFS
  
-   Retiro de equipos
  
##### Integración con software de creación de imágenes, copias de seguridad y antimalware
  
La mayoría de las aplicaciones de creación de imágenes, copias de seguridad y antimalware de terceros están diseñadas y probadas para su uso con EFS. El conocimiento de los diferentes tipos de herramientas que usa la organización y su posterior prueba junto con EFS es un paso de la planeación necesario para garantizar que se cumplen los acuerdos de servicio de TI. Entre los criterios de prueba, se debe incluir si las aplicaciones funcionan correctamente con los datos cifrados, así como si las herramientas conservan o no el estado de cifrado, según los requisitos de la organización.
  
###### Copia y traslado de archivos
  
La copia o el traslado de archivos protegidos con EFS pueden producir cambios en el estado de cifrado del archivo. Las reglas generales del impacto de la copia y el traslado de archivos en el cifrado son:
  
-   Si copia un archivo o una carpeta *en el mismo equipo* de una partición NTFS a otra, el archivo se cifrará en la ubicación de destino.
  
-   Si copia un archivo o una carpeta de una partición NTFS de un equipo a otro tipo de partición, independientemente de que las particiones estén o no en el mismo equipo, la copia no se cifra porque el sistema de archivos de destino no es compatible con el cifrado.
  
-   Si copia un archivo o una carpeta entre particiones NTFS en dos equipos, el archivo de destino se cifrará si el equipo remoto permite que el usuario cifre archivos; si no es así, no se cifrará. Tenga en cuenta que se debe confiar en el equipo remoto para la delegación. En un entorno de dominio, el cifrado remoto no está habilitado de manera predeterminada.
  
Las utilidades de mantenimiento que copian archivos enteros sin leer los datos de archivo deberían funcionar como se espera. Por ejemplo, la utilidad de copia de seguridad de Windows (y la mayoría de programas de copia de seguridad) leen el conjunto completo de todos los datos de secuencia NTFS de los archivos de los cuales realizan copias de seguridad, por lo que la copia de seguridad puede continuar sin tener acceso al material de clave del usuario. Los archivos de los que se realicen copias de seguridad con este método seguirán cifrados en el medio de copia de seguridad.
  
![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
La utilidad de copia de seguridad incluida en Windows Vista no puede realizar copias de seguridad de archivos cifrados con EFS. Si no va a usar una herramienta de copia de seguridad de terceros, puede seguir usando la herramienta Robocopy con el parámetro /efsraw para automatizar la creación de copias de seguridad de archivos protegidos con EFS en equipos que ejecutan Windows Vista.
  
###### Herramientas de creación de imagen de disco
  
Igualmente, las herramientas de creación de imagen de disco que capturan el contenido del sistema de archivos completo conservarán el estado de EFS de los archivos protegidos porque leen bloques individuales del disco. La creación de la imagen de un equipo que contiene datos protegidos con EFS incluye los datos cifrados con EFS como parte de la imagen. Algunas herramientas de creación de imagen permiten abrir una imagen y ver o modificar archivos individuales de la imagen sin restaurarla en un equipo de destino. Estas herramientas no suelen funcionar correctamente con archivos cifrados con EFS, y no podrá abrir o modificar archivos cifrados capturados en una imagen a menos que el equipo en el que abra los archivos contenga el material de clave correcto.
  
###### Herramientas antimalware
  
Los programas antimalware (incluido el software antivirus y antispyware) suelen funcionar de dos formas:
  
-   Interceptan solicitudes para abrir archivos y examinarlos en busca de malware antes de que el usuario pueda tener acceso al archivo. Los programas que usan este mecanismo suelen funcionar con EFS porque los archivos se examinan después de que la aplicación solicite datos de un archivo y la solicitud se realiza en el contexto de seguridad del usuario.
  
-   Usan una cuenta de sistema (como LOCAL SYSTEM o NETWORK SERVICE) para examinar archivos en un equipo, independientemente de quién los posea. Por lo general, las herramientas que usan este mecanismo no pueden inspeccionar archivos protegidos con EFS porque, cuando intentan abrir el archivo, se genera un error de acceso denegado.
  
Los programas antimalware individuales pueden combinar estos dos enfoques. Revise la documentación de las soluciones antimalware que tenga y pruébelas para asegurarse de que funcionan correctamente con archivos protegidos con EFS en su entorno.
  
##### Plan para el uso compartido de archivos y EFS
  
Si su organización debe permitir el uso compartido de información confidencial entre varios usuarios, hay dos posibilidades para hacerlo: su almacenamiento en carpetas compartidas típicas en servidores de archivos o el uso de carpetas web. En ambos métodos, es necesaria la configuración para ofrecer compatibilidad con EFS, y debe comprender los problemas, ventajas y riesgos, por ejemplo:
  
-   Si se almacenan archivos cifrados en un servidor de archivos remoto, puede decidir si desea permitir que el servidor mantenga copias de los archivos de texto sin formato o si deben seguir cifrados en el servidor. Si desea proporcionar acceso compartido a los archivos cifrados mientras sigue protegiendo su contenido en equipos móviles, puede conservar copias de archivo de texto sin formato en el servidor. Si es obligatorio que los archivos protegidos permanezcan cifrados independientemente del lugar en el que estén almacenados, deberá configurar el servidor adecuadamente (se debe confiar en el servidor para la delegación en Active Directory).
  
-   Puede almacenar archivos cifrados en carpetas web si usa Windows XP o Windows Server 2003. Este enfoque hace que estén disponibles los archivos a través de aplicaciones que pueden usar DAV para tener acceso a las carpetas web (incluso Microsoft Office 2000 y posterior), y también permite tenerlos a disposición de los usuarios a través de aplicaciones basadas en Web.
  
##### Plan para el retiro
  
EFS solo cifra archivos seleccionados, y el material de clave se puede conservar en el volumen de sistema en algunos modos de funcionamiento. Cuando se retira un equipo con contenido protegido por EFS, debe seguir los procedimientos habituales de retiro para asegurarse de que se quitan todos los archivos confidenciales.
  
#### Plan para las posibilidades de uso
  
EFS es un método seguro para el cifrado de archivos y carpetas en volúmenes NTFS. Se debe crear y distribuir una directiva de cifrado escrita que describa el uso, los requisitos y las cuestiones operativas relacionadas con el cifrado. Los usuarios y el personal de soporte técnico deben ser instruidos acerca del uso correcto del cifrado antes de su implementación.
  
Una directiva de cifrado debe describir las cuestiones relacionadas con el cifrado de información confidencial, entre las que se incluyen:
  
-   El tipo de información que se debe cifrar.
  
-   Los tipos de equipos que deben usar cifrado (por ejemplo, equipos de escritorio y portátiles).
  
-   Las soluciones de cifrado de datos compatibles (por ejemplo, EFS y BitLocker).
  
-   Los problemas que el cifrado soluciona y no soluciona.
  
-   Los algoritmos de cifrado y el tamaño mínimo de las claves que son aceptables para la protección de la información corporativa.
  
-   Los usuarios que pueden y deben asegurar el uso apropiado del cifrado.
  
-   Los posibles problemas relacionados con el cifrado, como la pérdida de datos.
  
-   Los pasos que los usuarios deben realizar para cifrar archivos.
  
-   La forma en que los usuarios pueden confirmar el cifrado de archivos (por ejemplo, archivo resaltado con una fuente verde en el Explorador de Windows y Cipher.exe).
  
-   La persona responsable de la recuperación de los datos cifrados y la forma en que los usuarios deben iniciar una recuperación.
  
-   La forma en que los usuarios pueden obtener soporte técnico para los problemas de cifrado.
  
Use los canales de aprendizaje habituales para compartir información acerca del cifrado con los usuarios, incluidas fuentes en línea y en papel, con lecciones prácticas y clases teóricas si fuera necesario. Esta tarea se puede desarrollar de forma paralela con el resto del proceso de implementación.
  
#### Plan para Active Directory y la directiva de grupo
  
Active Directory y la directiva de grupo ofrecen la forma más eficaz de administrar la configuración y la directiva de EFS. Los siguientes parámetros de GPO pueden afectar al comportamiento de EFS.
  
-   En **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad**
  
    -   **Apagado: borrar el archivo de paginación de la memoria virtual.** Este parámetro da instrucciones al sistema operativo para que borre el contenido del archivo de paginación del sistema cuando se apague el sistema operativo. Esta configuración reduce el riesgo de que se pierdan datos de texto sin formato a través del archivo de paginación.
  
    -   **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash.** De manera predeterminada, EFS usa el algoritmo Estándar de cifrado avanzado (AES) con una clave de 256 bits en equipos con Windows XP Service Pack 1 (SP1) y Windows Server 2003. No obstante, si habilita el parámetro **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** en estos equipos, el sistema operativo usará 3DES con una clave de 168 bits. En los equipos con Windows Vista, esta configuración hace que EFS use AES.
  
    ![](images/Cc162806.note(es-es,TechNet.10).gif)**Nota:**
  
    El uso de la directiva FIPS no es la forma recomendada de manipular los algoritmos de cifrado usados por EFS, a menos que el cumplimiento de la norma FIPS sea obligatorio. La forma recomendada de cambiar los algoritmos usados por EFS es mediante el establecimiento del valor adecuado en **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\EFS.**
  
-   En **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas**
  
    -   **Sistema de cifrado de archivos.** Habilita EFS en equipos en el ámbito de la directiva.
  
    -   **Sistema de cifrado de archivos.** Agregue o quite agentes de recuperación de datos para modificar la directiva de recuperación de su organización. El proceso de administración de los agentes de recuperación de datos se describe con detalle en el [Capítulo 2: tareas de configuración e implementación](https://technet.microsoft.com/es-es/library/a69e5f04-8f25-43a6-86b9-e8279021d108(v=TechNet.10)) de esta guía.
  
##### Plan para la migración a cuentas de dominio
  
Por los motivos explicados en la guía *Análisis de seguridad* de este Acelerador de solución, EFS ofrece seguridad óptima solo para usuarios con cuentas de dominio de Active Directory. Es posible usar Syskey para conseguir niveles similares de seguridad, pero el efecto de unos niveles de Syskey avanzados es algo negativo para el usuario. Por este motivo, los usuarios de EFS deben ser usuarios de dominio. Parte de la planeación de EFS debe incluir una encuesta a los posibles usuarios para asegurarse de que tienen cuentas de dominio y de que solo usan estas cuentas cuando inician la sesión en un equipo para obtener acceso a la información confidencial protegida con EFS.
  
##### Plan para la directiva de contraseñas de Active Directory
  
A menos que se usen tarjetas inteligentes con EFS, las claves de cifrado de archivos de EFS están protegidas con la contraseña del usuario. Cualquiera que pueda obtener un identificador de usuario y una contraseña puede iniciar la sesión como dicho usuario y descifrar sus archivos. Por lo tanto, una directiva de contraseñas seguras junto con una educación sólida de los usuarios debe formar parte de los procedimientos de seguridad de cada organización para garantizar la protección de los archivos cifrados con EFS.
  
##### Plan para la migración de certificados autofirmados a certificados emitidos por CA
  
Algunos usuarios pueden haber comenzado a usar EFS antes de la implementación oficial de EFS. Si un usuario intenta cifrar un archivo en un equipo que no tenga certificados EFS, el subsistema de EFS generará un nuevo certificado autofirmado. Cuando implemente EFS en los equipos de la organización, debe planear la sustitución de estos certificados autofirmados por certificados emitidos por la entidad de certificación. El proceso de sustitución estandariza la vigencia y el nivel de seguridad de las claves de los certificados usados para EFS en equipos con certificados autofirmados y en otros equipos en los que se haya implementado EFS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
-   [Orientación acerca de la planeación del hardware para Windows Vista Enterprise](http://go.microsoft.com/fwlink/?linkid=79962)
  
-   Especificación de [Transporte "bulk-only" clase almacenamiento masivo USB](http://www.usb.org/developers/devclass_docs/usbmassbulk_10.pdf) en el sitio web de bus serie universal
  
-   La página de [Especificaciones del Módulo de plataforma segura (TPM)](https://www.trustedcomputinggroup.org/specs/tpm) en el sitio web de Trusted Computing Group
  
-   [Acelerador de solución para Business Desktop Deployment](http://go.microsoft.com/fwlink/?linkid=91187)
  
-   [Guía de instalación de Lite Touch](http://go.microsoft.com/fwlink/?linkid=78607) para Business Desktop Deployment
  
-   [Introducción técnica al Cifrado de unidad BitLocker](http://go.microsoft.com/fwlink/?linkid=77977)
  
-   [Cifrado de unidad BitLocker y sanitización de discos](http://go.microsoft.com/fwlink/?linkid=80648)
  
-   [Descripción de las credenciales móviles](http://technet.microsoft.com/es-es/library/cc783542.aspx)
  
-   [El Sistema de archivos cifrados (EFS) genera un certificado con firma automática cuando intenta cifrar un archivo EFS en un equipo con Windows XP](http://support.microsoft.com/kb/912761)
  
-   [Identity Lifecycle Manager 2007](http://www.microsoft.com/windowsserver/ilm2007) (ILM 2007) de Microsoft
  
-   La sección [Protección y recuperación de datos en Windows XP/Información general acerca de la recuperación de datos](http://www.microsoft.com/technet/prodtechnol/winxppro/support/dataprot.mspx) de la documentación de Windows XP
  
-   [Guía paso a paso sobre el Cifrado de unidad BitLocker de Windows](http://go.microsoft.com/fwlink/?linkid=83223)
  
-   [Archivado y administración de claves en Windows Server 2003](http://technet.microsoft.com/es-es/library/cc755395.aspx)
  
-   [Descripción de la Herramienta de preparación de unidad BitLocker](http://support.microsoft.com/kb/930063)
  
-   [Extensión del esquema de Active Directory en Windows Server 2003 R2](http://technet.microsoft.com/es-es/library/cc664691.aspx)
  
**Descargar**
  
[Consiga el Kit de herramientas de cifrado de datos para equipos móviles](http://go.microsoft.com/fwlink/?linkid=81666)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=kit%20de%20herramientas%20de%20cifrado%20de%20datos%20para%20equipos%20móviles,%20guía%20de%20implementación%20y%20planeación%20para%20el%20kit%20de%20herramientas%20de%20cifrado%20de%20datos)
  
[](#mainsection)[Principio de la página](#mainsection)
