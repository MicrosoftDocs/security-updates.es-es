---
TOCTitle: Supervisión de la seguridad y detección de ataques
Title: Supervisión de la seguridad y detección de ataques
ms:assetid: 'a30af90e-ce18-47fc-a947-11f332ee4731'
ms:contentKeyID: 20200218
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875806(v=TechNet.10)'
---

Supervisión de la seguridad y detección de ataques
==================================================

Publicado: 29/08/2006

##### En esta página

[](#egaa)[Introducción](#egaa)
[](#efaa)[Definición](#efaa)
[](#eeaa)[El desafío de las medianas empresas](#eeaa)
[](#edaa)[Soluciones](#edaa)
[](#ecaa)[Resumen](#ecaa)
[](#ebaa)[Apéndice A: Exclusión de eventos innecesarios](#ebaa)
[](#eaaa)[Apéndice B: Implementación de la configuración de la directiva de grupo](#eaaa)

### Introducción

Bienvenido a este documento de la colección Guías de seguridad para medianas empresas. Microsoft espera que esta información le ayude a crear un entorno informático más seguro y productivo.

#### Resumen ejecutivo

El número de casos importantes de amenazas e incidentes relacionados con software malintencionado que llevan años escuchándose en los medios de comunicación ha servido para aumentar la concienciación sobre este problema y alentar a muchas empresas a invertir tiempo y recursos en defenderse contra este frecuente problema de seguridad. Sin embargo, es posible que la mayor amenaza para la infraestructura de las empresas no provenga de los ataques del exterior (por ejemplo, un virus), sino que resida en la propia red interna.

El daño potencial que pueden producir los ataques realizados desde el interior de la red de la empresa es muy elevado, especialmente si los autores son empleados con puestos de confianza y tienen acceso a todos los recursos de la red de la empresa. Tras examinar minuciosamente los riesgos que plantean las amenazas tanto externas como internas, muchas empresas deciden buscar sistemas que puedan supervisar las redes y detectar ataques allí donde se originen.

Las prácticas de supervisión de la seguridad no son una opción para las empresas que se rigen por restricciones normativas: son un requisito. Esas mismas normativas pueden controlar incluso durante cuánto tiempo y de qué manera se deben guardar y archivar los registros de supervisión de la seguridad. Los continuos cambios del entorno normativo y el continuo aumento de las demandas a los que se ven sometidos las empresas reguladas para proteger sus redes, realizar un seguimiento de la identidad de las personas que tienen acceso a los recursos y proteger la información privada, obligan a las empresas de todo el mundo a utilizar soluciones de supervisión de la seguridad efectivas.

Existen muchas razones por las que la supervisión de la seguridad y la detección de ataques también debería ser un tema importante para las medianas empresas que no necesitan atenerse a ningún requisito normativo. Entre ellas, se incluyen las consecuencias a las que podría enfrentarse cualquier empresa si alguien consiguiera atacar su infraestructura. No sólo se podrían interrumpir las operaciones de la empresa, lo que derivaría en pérdidas de la productividad e incluso económicas, sino que la empresa podría sufrir también una pérdida de reputación, lo cual suele ser más difícil de recuperar que cualquier otra pérdida derivada de un ataque.

Las utilidades del registro de seguridad de Microsoft® Windows® pueden servir como punto de partida de una solución de supervisión de la seguridad. Sin embargo, los registros de seguridad por sí solos no proporcionan información suficiente para planear respuestas a los incidentes. Estos registros de seguridad se pueden combinar con otras tecnologías que recopilan y consultan esa información para crear la parte central de una solución de supervisión de la seguridad y detección de ataques completa.

El principal objetivo de un sistema de supervisión de la seguridad y detección de ataques es ayudar a identificar eventos sospechosos en la red que puedan indicar que se está produciendo una actividad malintencionada o errores de procedimientos. En este artículo, se describe cómo elaborar un plan para ayudar a satisfacer la necesidad de un sistema de este tipo en las redes basadas en Windows. También se incluyen instrucciones acerca de cómo implementar, administrar y validar ese sistema.

#### Descripción general

Este artículo consta de cuatro secciones principales que se concentran en los conceptos y temas esenciales para diseñar e implementar una solución de supervisión de la seguridad y detección de ataques efectiva. La primera sección es la "Introducción", que es la que está leyendo en este momento. Las demás secciones son:

##### Definición

En esta sección, se ofrece información útil para conocer los procesos relacionados con la generación y la aplicación de la solución que se presenta en este artículo.

##### El desafío de las medianas empresas

En esta sección, se describen muchos de los desafíos más comunes a los que se enfrentan las medianas empresas en relación con los sistemas de supervisión de la seguridad y detección de ataques.

##### Soluciones

Esta sección ofrece información detallada acerca de cómo desarrollar, implementar, administrar y validar la solución que se presenta en este artículo. Se divide, a su vez, en dos subsecciones. "Desarrollo de la solución" trata de los requisitos previos y elabora los pasos del planeamiento. "Implementación y administración de la solución" ofrece información que ayuda a implementar, administrar y validar un sistema de supervisión de la seguridad y detección de ataques.

#### Quién debería leer este artículo

En este artículo, se tratan los problemas de privacidad y seguridad de las medianas empresas, especialmente de aquellas que necesitan proteger la identidad y controlar el acceso a los datos debido a restricciones normativas. En consecuencia, el público al que se destina este artículo abarca desde directores técnicos y personas que toman las decisiones, a profesionales de TI e implementadores de tecnología que son responsables del planeamiento, la implementación, el funcionamiento o, especialmente, la seguridad de la red de la empresa.

Aunque algunas partes del artículo deberían ser útiles para la mayoría de los técnicos encargados de tomar las decisiones, los lectores deberían estar familiarizados con los problemas de seguridad y los riesgos de su entorno de red, y conocer los conceptos de los servicios de registro de sucesos de Windows para aplicar todas las materias que se incluyen en él.

[](#mainsection)[Principio de la página](#mainsection)

### Definición

En este artículo, se utiliza el modelo de procesos Microsoft Operations Framework (MOF), además de las funciones de administración de servicio (SMF) de administración de seguridad y de incidentes de MOF.

En particular, la solución que se presenta en este artículo recomienda el uso de un proceso continuo, en lugar de una implementación lineal de la supervisión de la seguridad y la detección de ataques. Concretamente, la solución debería incluir los pasos que se muestran en la siguiente:

![](images/Cc875806.SMAAD1(es-es,TechNet.10).gif)

**Figura 1. Aplicación de MOF**

Una solución de supervisión de la seguridad es, en realidad, un proceso continuo de planeamiento, implementación, administración y realización de pruebas, porque esa es la naturaleza misma de la supervisión de la seguridad. Dado que las amenazas para las redes empresariales siempre están cambiando, el sistema que supervisa la seguridad de la red empresarial también debe cambiar.

La aplicación de este proceso a la supervisión de la seguridad se adapta a la función SMF de administración de la seguridad, que pretende lograr lo siguiente:

-   Evaluar la exposición de la empresa e identificar los activos que se deben proteger.

-   Identificar formas de reducir el riesgo hasta niveles aceptables.

-   Diseñar un plan para mitigar los riesgos para la seguridad.

-   Supervisar la eficiencia de los mecanismos de seguridad.

-   Volver a evaluar la efectividad y los requisitos de seguridad regularmente.

Para obtener más información acerca de MOF, consulte el sitio web de [Microsoft Operations Framework](http://www.microsoft.com/mof) en www.microsoft.com/mof. Encontrará más información acerca de la función [SMF de administración de la seguridad](http://www.microsoft.com/technet/itsolutions/cits/mo/smf/mofsmsmf.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/smf/mofsmsmf.mspx.

La administración de riesgos es el proceso mediante el cual se determina el nivel de riesgo aceptable de una organización, se evalúan los riesgos actuales, se buscan formas de alcanzar ese nivel de riesgo aceptable y se administra el riesgo. Aunque en este artículo se tratan algunos conceptos de la administración de riesgos y algunos pasos que le ayudarán a evaluarlos, la administración de riesgos es un tema diferente que merece un estudio en profundidad. Para obtener más información acerca del análisis y las evaluaciones de riesgos, consulte la [*Guía de administración de riesgos de seguridad*](http://go.microsoft.com/fwlink/?linkid=30794) en http://go.microsoft.com/fwlink/?linkid=30794 (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### El desafío de las medianas empresas

Las medianas empresas tienen que enfrentarse a numerosos desafíos a la hora de construir un sistema de supervisión de la seguridad efectivo y establecer directrices que apoyen esa labor. Esos desafíos incluyen:

-   Comprender la necesidad y las ventajas de proteger todo el entorno de red de amenazas internas y externas.

-   Diseñar un sistema de supervisión de la seguridad y detección de ataques efectivo que incluya métodos para detectar y evitar los intentos de burlar las directivas establecidas.

-   Implementar directivas de supervisión completas y efectivas que no sólo detecten ataques, sino que además ofrezcan una visión general del nivel de seguridad del entorno para solucionar cualquier problema.

-   Mantener directivas y procesos que establezcan una correlación entre los informes de seguridad y las directivas establecidas para facilitar el trabajo administrativo a la hora de detectar actividades sospechosas.

-   Implementar y aplicar directivas y prácticas empresariales eficientes que ayuden a supervisar la seguridad a la vez que equilibran las necesidades de la empresa.

-   Determinar umbrales de riesgo aceptables para equilibrar la funcionalidad y la mitigación de riesgos.

[](#mainsection)[Principio de la página](#mainsection)

### Soluciones

Tal y como se ha explicado anteriormente, un proceso de supervisión de la seguridad completo no sólo ayuda a satisfacer la necesidad de realizar análisis de investigación, sino que también puede ser una medida de seguridad proactiva capaz de suministrar información antes, durante y después de un ataque. Al disponer de un repositorio centralizado para los informes de seguridad, los ataques se pueden detectar durante la fase de sondeo, mientras se producen o inmediatamente después, para que las personas que responden a ellos tengan la información que necesitan para reaccionar de manera efectiva, lo que puede reducir el impacto de los intentos de intrusión.

Es importante comprender durante la fase de conceptualización del desarrollo todas las ventajas que se pueden obtener implementando la supervisión de la seguridad para que el diseño y las directivas puedan beneficiarse de ellas. Algunas de las ventajas de la supervisión de la seguridad son:

-   Identificación y solución de problemas de los sistemas que no cumplen las directivas de seguridad o de actualizaciones para reducir el perfil de vulnerabilidad de una mediana empresa.

-   Producción de información que pueda alertar al personal de los intentos de intrusión antes de que se produzca el ataque propiamente dicho mediante la identificación de actividades inusuales.

-   Creación de información de auditoría de seguridad y protección de la misma para mejorar los análisis de investigación, lo que no sólo cumple los requisitos normativos, sino que además reduce el impacto de cualquier ataque que se pueda producir.

-   Ayuda al análisis del nivel de seguridad para mejorar la seguridad general.

-   Detección de actividades que se producen al margen de los procesos empresariales establecidos, ya sean ocasionales o accidentales.

-   Ayuda a la identificación de sistemas no administrados en una red o a la solución de la vulnerabilidad de dispositivos.

#### Desarrollo de la solución

La seguridad es un tema importante para muchas empresas. Aunque la mayoría dedica una cantidad de recursos razonable a la seguridad física con métodos que abarcan desde las cerraduras de las puertas hasta complejos controles de acceso basados en tarjetas, muchas de las empresas aún no son capaces de garantizar la seguridad de los datos de los que cada vez dependen más.

Cuando las empresas centran su atención en la seguridad de los datos y la supervisión, normalmente concentran sus esfuerzos en el perímetro con firewalls. Sin embargo, este método deja vulnerables otros puntos de ataque. De acuerdo con el [Estudio de delitos electrónicos de 2004](http://www.cert.org/archive/pdf/2004ecrimewatchsummary.pdf) publicado por el Servicio Secreto de Estados Unidos y el Centro de Coordinación de CERT en www.cert.org/archive/pdf/2004eCrimeWatchSummary.pdf, el 29% de los atacantes identificados eran internos, es decir, empleados actuales, contratistas y antiguos empleados. Teniendo en cuenta esta información, queda claro que hay que crear un método de seguridad multinivel para salvaguardar la empresa de amenazas internas, además de las que se originan en el exterior.

Un método que sirve para enfrentarse a las amenazas internas y externas desde un punto de vista de seguridad reactivo consiste en implementar un proceso de registro de auditoría de seguridad. Todas las versiones de Microsoft Windows, desde Microsoft Windows NT® 3.1 hasta las actuales, utilizan un archivo de registro de seguridad integrado para registrar los eventos de seguridad. Sin embargo, aunque esta funcionalidad por sí sola puede resultar útil para realizar una investigación en respuesta a una intrusión que ya se ha producido, sería difícil utilizarla de una manera proactiva para identificar con antelación un ataque o alertar al personal adecuado de los intentos de intrusión mientras se están produciendo.

Como ya se ha mencionado, los registros de seguridad se suelen utilizar de manera reactiva durante los análisis de investigación de un incidente de seguridad después de que se haya producido. Sin embargo, en el [Estudio sobre amenazas internas de 2005](http://www.cert.org/archive/pdf/insidercross051105.pdf) publicado por el Servicio Secreto de EE.UU. y CERT en www.cert.org/archive/pdf/insidercross051105.pdf, tras analizar los descubrimientos clave, se llegó a la conclusión de que la supervisión y el registro de seguridad se pueden utilizar para la detección proactiva, en lugar de exclusivamente para el análisis de investigación reactivo. Asimismo, la mayoría de los atacantes, ya sean internos o externos, intentan borrar sus huellas modificando los registros; por lo tanto, hay que tomar medidas para proteger los registros del sistema. Los registros de seguridad y otros métodos que se utilizan para supervisar y detectar ataques pueden ser una herramienta esencial del arsenal de seguridad de la red si se utilizan y protegen correctamente.

Aunque este documento se concentra en los registros de seguridad del sistema, tan sólo son el núcleo de la metodología de supervisión de la seguridad y detección de ataques. Entre otros aspectos que se deberían tener en cuenta, se incluye la forma de identificar y solucionar los problemas de los sistemas que no cumplen las directivas de seguridad establecidas o que no han implementado las revisiones de seguridad para vulnerabilidades recomendadas. También se debería supervisar la infraestructura interna de la red, incluidos los informes de seguridad de puertos de conmutación (para evitar que los sistemas no administrados obtengan acceso a la red) y la supervisión de la seguridad inalámbrica (para evitar las conexiones no autorizadas o el robo de paquetes). Muchos de estos temas sobre supervisión están fuera del ámbito de este documento, pero merecen que se les preste atención en cualquier solución de supervisión de la seguridad bien equilibrada.

##### Implementación de la supervisión de la seguridad

En las subsecciones siguientes, se ofrece información acerca de diversos aspectos de la implementación de un sistema de supervisión de la seguridad.

**Registro de sucesos de seguridad de Windows**
Todas las versiones de Microsoft Windows, desde Microsoft Windows NT 3.1 en adelante, son capaces de registrar los eventos de seguridad mediante una funcionalidad de archivos de registro integrada. En un entorno basado en Microsoft Windows, esta funcionalidad es la base de la supervisión de la seguridad. Sin embargo, sin utilidades ni herramientas adicionales para establecer una correlación entre esta información, resulta difícil utilizarla de manera proactiva, ya que está dispersa.

[![](images/Cc875806.SMAAD2(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875806.smaad2_big(es-es,technet.10).gif)

**Figura 2. Registro de seguridad del Visor de sucesos**

El registro de sucesos de seguridad (que se muestra en la figura anterior) utiliza un formato de archivo personalizado para registrar los datos de supervisión de la seguridad. Aunque es posible leer partes de estos registros con un editor de texto, es necesario utilizar un programa adecuado, como el Visor de sucesos, para ver toda la información registrada en ellos. El archivo de registro de sucesos de seguridad (SecEvent.evt) reside en el directorio %systemroot%\\System32\\config. El acceso a los registros de sucesos siempre se rige por medio del servicio Registro de sucesos, y este servicio aplica controles de acceso a cada registro.  Los permisos predeterminados del registro de seguridad son muy estrictos comparados con los de otros registros del sistema. Sólo los administradores tienen acceso al registro de seguridad de manera predeterminada.

Hay dos tipos de evento que se incluyen en el registro de sucesos de seguridad: las auditorías de aciertos y las auditorías de errores. Los eventos Auditoría de aciertos indican las operaciones que los usuarios, los servicios o los programas han realizado correctamente. Los eventos Auditoría de errores detallan las operaciones que no se han completado correctamente. Por ejemplo, los errores en los intentos de inicio de sesión de los usuarios serían ejemplos de eventos Auditoría de errores que se incluyen en el registro de sucesos de seguridad si se han habilitado las auditorías de inicio de sesión.

La configuración de directiva de grupo de la directiva de auditoría, que se encuentra en Configuración del equipo\\Configuración de Windows\\Directivas locales, controla qué eventos crean entradas en los registros de seguridad. La directiva de auditoría se puede configurar a través de la consola Configuración de seguridad local, o en el ámbito del sitio, dominio o unidad organizativa (OU) a través de la directiva de grupo con Active Directory.

**Interpretación de eventos de auditoría**
A lo largo de este artículo, vamos a describir los eventos de auditoría con todo detalle, por lo que es importante disponer de conocimientos básicos de la estructura de los eventos de auditoría y la información que contienen.

![](images/Cc875806.SMAAD3(es-es,TechNet.10).gif)

**Figura 3. Ventana Propiedades del evento**

Los eventos constan de tres partes básicas: el encabezado del evento, la descripción del evento y una sección de datos binarios.

Los encabezados de los eventos se componen de los campos siguientes:

**Tabla 1. El encabezado del evento**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Campo</p></th>
<th><p>Definición</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Fecha</p></td>
<td style="border:1px solid black;"><p>Fecha en la que se ha producido el evento.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Hora</p></td>
<td style="border:1px solid black;"><p>Hora local en la que se ha producido el evento.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Tipo</p></td>
<td style="border:1px solid black;"><p>Clasificación del tipo o gravedad del evento. Los eventos de auditorías de seguridad pertenecen a los tipos Auditoría de aciertos o Auditoría de errores.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Origen</p></td>
<td style="border:1px solid black;"><p>Aplicación que registró el evento. Puede ser un programa propiamente dicho, como SQL Server, un nombre de controlador o un componente del sistema como, por ejemplo, Seguridad.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Categoría</p></td>
<td style="border:1px solid black;"><p>Clasificación del origen del evento. Esta clasificación se aplica a los registros de auditoría de seguridad, ya que se corresponden con un tipo de evento que se puede configurar en la directiva de grupo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Id. de evento</p></td>
<td style="border:1px solid black;"><p>Este código identifica el tipo de evento específico. En la figura anterior, el Id. de evento es 680. Este Id. de evento indica que se ha pasado un conjunto de credenciales al sistema de autenticación por medio de un proceso local, un proceso remoto o un usuario.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Usuario</p></td>
<td style="border:1px solid black;"><p>Usuario en cuyo nombre se ha producido el evento. Este nombre es el Id. de cliente si el evento lo produjo un proceso o el Id. principal si no se está produciendo una suplantación. En los eventos de seguridad, se muestra la información principal y de suplantación, si es posible y existe.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Equipo</p></td>
<td style="border:1px solid black;"><p>Nombre del equipo en el que se produjo el evento.</p></td>
</tr>
</tbody>
</table>
  
De hecho, el campo de descripción del evento contiene una gran variedad de información que puede ser distinta en cada evento. Por ejemplo, en el ejemplo del evento 680 que se muestra en la figura anterior, el campo **Código de error:** especifica **0xC000006A**, lo que significa que se ha proporcionado una contraseña incorrecta. Cada tipo de evento muestra información específica del evento en este campo.
  
Los eventos del registro de sucesos de seguridad de Windows no utilizan la sección de datos binarios del registro del evento.
  
**Aspectos técnicos**  
Para implementar un sistema de supervisión de la seguridad y detección de ataques basado en el registro de sucesos de seguridad de Windows, se deben tener en cuenta los aspectos siguientes:
  
-   **Gestionar grandes volúmenes de eventos de seguridad**. Para asimilar el gran volumen de eventos de seguridad que se generan, habrá que pensar bien de qué eventos de auditoría de seguridad específicos se debería realizar un seguimiento. Esto es especialmente importante en las auditorías de acceso a archivos y objetos, porque ambas pueden generar grandes cantidades de datos.
  
-   **Almacenar y administrar la información de los eventos en un repositorio central**. La información de los eventos puede ocupar terabytes, dependiendo de la configuración del sistema de supervisión. Esto es especialmente importante para los análisis de investigación y se explica con detenimiento en la sección correspondiente.
  
-   **Identificar y responder a firmas de ataques**. Para poder identificar patrones de actividad que puedan indicar un ataque, un revisor o una consulta personalizada debe poder distinguir los eventos asociados a dicha actividad que están incrustados en la información proporcionada. Si se identifica ahí alguna actividad sospechosa, debería haber un mecanismo para responder de la manera oportuna y adecuada.
  
-   **Restringir la posibilidad de que el personal burle los controles de la auditoría de seguridad**. El personal que dispone de privilegios elevados en una red, sobre todo los administradores, se debe compartimentar con el fin de restringir el acceso a la información de auditoría, de forma que los especialistas en seguridad sean los únicos responsables de la administración de los sistemas de auditoría.
  
**Planeamiento de la solución**  
Se deben realizar las actividades siguientes antes de implementar un sistema de supervisión de la seguridad y detección de ataques:
  
-   Revisar la configuración de la auditoría de seguridad actual.
  
-   Evaluar las funciones de administrador y las tareas de los usuarios normales.
  
-   Revisar los procedimientos y las directivas empresariales.
  
-   Identificar los sistemas vulnerables.
  
-   Enumerar los activos de gran valor.
  
-   Identificar cuentas confidenciales o sospechosas.
  
-   Enumerar los programas autorizados.
  
Para obtener más información acerca de los requisitos de almacenamiento, consulte la sección "Implementación de análisis de investigación", más adelante en este artículo.
  
**Revisar la configuración de la auditoría de seguridad actual**  
Las empresas deberían revisar la configuración del archivo de registro de seguridad y de auditoría de seguridad actual para tener una base para realizar los cambios que se recomiendan en este artículo. Esa revisión se debería realizar regularmente después de implementar una solución. Habría que obtener la información siguiente:
  
-   Configuración de la auditoría de seguridad efectiva actual.
  
-   Nivel al que se aplica esta configuración (equipo local, sitio, dominio o unidad organizativa).
  
-   Configuración del archivo de registro actual (límites de tamaño y comportamiento cuando se alcanza el tamaño máximo).
  
-   Configuración de auditoría de seguridad adicional que pueda aplicarse (por ejemplo, auditoría del uso de los privilegios de copias de seguridad y restauración).
  
Puede utilizar la información del "Apéndice B: Implementación de la configuración de la directiva de grupo", al final de este artículo, para ayudarle a identificar qué configuración se debe registrar. Para obtener más información acerca de la configuración de la auditoría de seguridad, consulte la [*Guía de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?LinkId=14845 (puede estar en inglés).
  
**Evaluar las funciones de administrador y las tareas de los usuarios normales.**  
Un elemento clave de la implementación de una solución de supervisión de la seguridad efectiva es garantizar que se conocen los propietarios de las cuentas de administrador y se comprenden sus funciones y responsabilidades. Por ejemplo, la mayoría de las empresas incluyen a los administradores en el grupo Administradores de dominio para que puedan crear nuevas cuentas de usuario en el dominio. Sin embargo, es posible que en las directivas de la empresa se especifique que sólo se permite crear cuentas nuevas a un sistema de aprovisionamiento instalado. En dicha situación, un evento de creación de cuenta iniciado por una cuenta de administrador requeriría una investigación inmediata.
  
Normalmente, es mucho más sencillo realizar una evaluación de las tareas de las cuentas de usuario, porque esas cuentas suelen tener menos acceso a los recursos de red que las cuentas de administrador. Por ejemplo, los usuarios normales no suelen necesitar obtener acceso al sistema de archivos en equipos que residen en el perímetro de una red, por lo que no es necesario supervisar la actividad de los usuarios normales en esos servidores.
  
**Revisar los procedimientos y las directivas empresariales**  
La revisión de los procedimientos y procesos empresariales se corresponde estrechamente con una evaluación de las funciones y responsabilidades de los administradores, aunque no se limita a ella. Entre los componentes más importantes de esa revisión, se incluye el examen del proceso de creación de usuarios y del proceso de control de cambios, entre otros. Es esencial realizar un examen de los mecanismos que proporcionan un proceso de aprobación y una pista de auditoría de todos los eventos que se producen en una red para poder establecer una correlación entre lo que serían eventos de auditoría autorizados y un intento de intrusión.
  
**Identificar los sistemas vulnerables**  
Los sistemas vulnerables son los equipos y los dispositivos de una red que tienen más probabilidades de que un atacante externo los sondee e intente obtener acceso a ellos antes de probar otro método. Normalmente, estos equipos residen en el perímetro de una red, pero los dispositivos internos también pueden ser vulnerables a los ataques, por lo que no hay que olvidarse de ellos.
  
En una revisión completa de los sistemas vulnerables, hay que asegurarse de lo siguiente:
  
-   Se han aplicado todas las actualizaciones de seguridad y Service Pack correspondientes.
  
-   Se han deshabilitado los servicios y las cuentas de usuario innecesarias.
  
-   Los servicios están configurados para ejecutarse en las cuentas Servicio local o Servicio de red siempre que sea posible.
  
-   Se han comprobado los servicios que requieren credenciales de usuario para garantizar que requieren ese nivel de acceso, especialmente si dichas cuentas tienen privilegios de administrador.
  
-   Se han aplicado plantillas de directivas de alta seguridad.
  
**Nota**   Este proceso de revisión no se debería limitar a los equipos vulnerables que residen en el perímetro. Sería recomendable realizar estas comprobaciones en todos los equipos de una red.
  
Para obtener más información acerca de cómo configurar los servicios para que se ejecuten con seguridad, consulte [*La Guía de planeamiento de servicios y cuentas de servicio*](http://go.microsoft.com/fwlink/?linkid=41311) en http://go.microsoft.com/fwlink/?LinkId=41311 (puede estar en inglés).
  
**Enumerar los activos de gran valor**  
Es probable que la mayoría de las empresas haya identificado ya los activos de gran valor que residen en sus redes, pero es posible que no hayan formalizado esa información como parte de una directiva organizativa en la que se documenten y detallen las protecciones que se han aplicado para cada activo. Por ejemplo, una empresa podría utilizar listas de control de acceso (ACL) y un sistema de cifrado para almacenar con seguridad los registros financieros confidenciales en las particiones del sistema de archivos NTFS. Sin embargo, en la directiva organizativa se deberían identificar esos registros como archivos protegidos a los cuales no deberían tener acceso los usuarios y administradores no autorizados para que esos usuarios administradores conozcan esa restricción.
  
Se debería investigar cualquier cambio que se realice en una lista ACL que se utilice para proteger dichos archivos, especialmente si se trata de cambios de propietario, porque esos eventos pueden indicar que se están produciendo intentos ilícitos de obtener acceso a los archivos sin la autorización adecuada. Dado que los cambios de propietario de esta naturaleza son muy extraños, deberían ser fáciles de detectar después de identificar y documentar los activos de gran valor.
  
**Identificar cuentas confidenciales o sospechosas**  
Se deberían revisar todas las cuentas confidenciales para identificar cuáles necesitan un nivel de auditoría mayor. Esas cuentas incluyen la cuenta predeterminada del administrador, cualquier miembro de los grupos Empresa, Esquema o Administradores de dominio, y cualquier cuenta que utilicen los servicios.
  
Aparte de las cuentas confidenciales, también es importante ajustar los niveles de las auditorías de seguridad de las cuentas que son propiedad de individuos que se han identificado como un riesgo o que se cree que participan en actividades sospechosas. Para obtener más información acerca de cómo ajustar los niveles de las auditorías para cuentas de usuario individuales, consulte la sección “Infracciones de directivas y umbrales”, más adelante en este artículo.
  
**Enumerar los programas autorizados**  
Para descubrir información acerca de una red, un atacante debe ejecutar programas en los sistemas que residen en esa red. Si se limitan los programas que pueden ejecutarse en una red, la empresa puede reducir de manera significativa la amenaza de un ataque externo. Para crear una lista de programas autorizados, se debería realizar una auditoría en todos los programas que actualmente estén autorizados o identificados como necesarios en el entorno de red. Cualquier programa desconocido que se encuentre durante dicha auditoría se debería considerar sospechoso e investigar inmediatamente. Microsoft Systems Management Server 2003 puede ayudarle a realizar auditorías de software, aunque no es obligatorio.
  
**Nota**   Puede que sea necesario realizar algunas excepciones en algunos equipos como, por ejemplo, en las estaciones de trabajo de los desarrolladores, en las que puede que los archivos ejecutables en desarrollo no se encuentren en las listas de programas autorizados. Sin embargo, el método más seguro es hacer que sea obligatorio realizar las labores de desarrollo y prueba únicamente en un entorno de equipos virtual o en un dominio de una red de desarrollo aislada.
  
##### Detección de infracciones de directivas y umbrales
  
Las infracciones de directivas constituyen la categoría de problemas de seguridad más importante que deben tener en cuenta las empresas. Entre estos tipos de incidentes, se incluyen:
  
-   Creación de cuentas de usuario al margen del proceso establecido.
  
-   Uso inadecuado o no autorizado de los privilegios de administrador.
  
-   Uso de cuentas de servicio para inicios de sesión interactivos.
  
-   Intentos de acceso a archivos a través de cuentas de usuario no autorizadas.
  
-   Eliminación de archivos a los cuales tienen acceso las cuentas de usuario.
  
-   Instalación y ejecución de software no autorizado.
  
Aunque el tipo de infracción de directivas más común es el intento de acceso no intencionado de los usuarios (por ejemplo, el acceso a directorios restringidos), esas infracciones suelen ser las menos importantes, ya que el problema se soluciona con limitaciones de acceso y directivas de derechos bien diseñadas. El tipo de evento más importante son las infracciones de directivas administrativas, ya sean deliberadas o accidentales, por la propia naturaleza de los derechos administrativos.
  
Los privilegios de las cuentas administrativas proporcionan un nivel de acceso importante a los sistemas a los individuos que necesitan ese tipo de autoridad para realizar su trabajo. Sin embargo, esta autoridad no implica la autorización a utilizar esos derechos del sistema al margen del ámbito o proceso autorizado. La capacidad de las cuentas administrativas de habilitar la creación de cuentas de usuario, modificar cuentas de usuario, ver datos restringidos y modificar derechos de acceso a datos implica que hay que pensar bien las formas de mitigar los riesgos asociados a capacidades tan importantes.
  
**Modelado de amenazas**  
Como es evidente, algunos conjuntos de amenazas se pueden mitigar con auditorías, otros no y algunos se pueden mitigar con auditorías, pero el costo que implica no vale la pena. Lo más importante que hay que saber es que no todas las vulnerabilidades suponen una amenaza para la red. Para tomar decisiones sobre qué vulnerabilidades se pueden o se deben mitigar, puede que resulte útil aplicar principios de modelado de amenazas.
  
El modelado de amenazas es una técnica de ingeniería que sirve para identificar amenazas y vulnerabilidades con el fin de crear más eficientemente contramedidas en el contexto de un entorno específico. Generalmente, este proceso consta de tres pasos básicos:
  
-   Comprender la perspectiva del atacante.
  
-   Identificar el perfil de seguridad del sistema.
  
-   Determinar y clasificar las amenazas relevantes.
  
Más concretamente, el examen del entorno de red desde la perspectiva del atacante implica la determinación de los objetivos que serían más tentadores para una persona que intentara obtener acceso a una red y las condiciones que se deberían cumplir para lograr atacar esos objetivos. Una vez identificados los objetivos vulnerables más tentadores, se puede examinar el entorno para determinar cómo afectan las protecciones a las condiciones de ataque. Este proceso revela las amenazas importantes, que luego se pueden clasificar de acuerdo con el nivel de riesgo que presentan, qué actividades pueden ser la solución más valiosa para esa amenaza y si la mitigación de las mismas puede beneficiar o perjudicar a otras áreas, lo que, a su vez, puede afectar al valor de la solución.
  
Por consiguiente, un proceso de modelado de amenazas de la red efectivo consta de una serie de pasos específicos que se basan en estos requisitos:
  
1.  **Identificación de activos críticos.** Para determinar en qué lugar es mejor utilizar los recursos de seguridad, hay que elaborar una lista de los activos que son críticos para las operaciones de la empresa. En este proceso, deberían participar los propietarios de los procesos empresariales y los propietarios de la tecnología, puesto que cada uno tiene puntos de vista importantes acerca de qué activos dañarían la empresa si se ven comprometidos.
  
2.  **Identificación de posibles puntos de ataque**. Esta fase de identificación también conlleva dos perspectivas diferentes. En primer lugar, es necesario clasificar los tipos de límites dentro de los cuales pueden residir los datos de la red. Estos límites residen en áreas críticas, confidenciales y públicas, en función del daño que podrían causar si dichos datos quedaran expuestos. En segundo lugar, desde la perspectiva tecnológica, se examinan los puntos de ataque por medio de vectores y los puntos de vulnerabilidad potenciales que podrían dejar expuestos los activos críticos y confidenciales. Esta combinación de información puede ayudar a reducir el centro de atención a las vulnerabilidades que se encuentran en los puntos en los que se puede obtener acceso a información crítica.
  
3.  **Identificación de amenazas reales.** Una vez que se conocen los activos críticos y los posibles puntos de acceso, se puede crear una lista de lo que podrían hacer los atacantes para provocar daños. Con esa lista, es posible centrar los esfuerzos en amenazas específicas reales.
  
    Existen diferentes métodos para identificar las amenazas reales. STRIDE es un método que examina las amenazas basándose en los tipos de ataques que se pueden utilizar (suplantación, alteración, rechazo, divulgación de información, denegación de servicio y elevación de privilegios). También existen otras medidas iterativas como, por ejemplo, la clasificación de las amenazas en niveles lógicos (por ejemplo, red, host y aplicación). El método lo decide la organización en función de lo que resulte más adecuado en un entorno determinado.
  
4.  **Categorización y clasificación de amenazas**. En este paso, entran en juego la evaluación de riesgos comunes y los principios de administración. Las amenazas se clasifican según la probabilidad de uso y el impacto potencial en la empresa. La fórmula estándar que se utiliza es:
  
    Riesgo = probabilidad de aprovechamiento x impacto potencial en la empresa
  
    Ese proceso implica varios métodos, además de una serie de herramientas que ayudan a evaluar los riesgos que están fuera del ámbito de este artículo. Para obtener más información acerca de la administración de riesgos y estos métodos, consulte la [*Guía de administración de riesgos de seguridad*](http://go.microsoft.com/fwlink/?linkid=30794) en http://go.microsoft.com/fwlink/?linkid=30794 (puede estar en inglés).
  
5.  **Remedio y reevaluación**. Como resultado de los pasos anteriores, se obtiene una lista de amenazas reales que son capaces de afectar a la empresa, y que se clasifican de acuerdo con el riesgo que presentan para la empresa. Esta lista permite utilizar un remedio específico cuya relación costo-beneficio también se debería evaluar. Después de todo, podrían existir diferentes formas de mitigar riesgos específicos y algunas podrían solucionar otras vulnerabilidades que podrían hacer que las labores de seguridad fueran más efectivas.
  
Aun después de poner en marcha un plan de remedio, el método de modelado de amenazas es un proceso iterativo que se debería realizar de manera regular con una reevaluación constante para garantizar que la seguridad es tan efectiva y completa como sea posible.
  
**Investigaciones y revisiones de antecedentes**  
La mayoría de las empresas realiza algún tipo de comprobación de antecedentes de los futuros empleados antes de firmar el contrato de empleo, pero no realiza ninguna comprobación posteriormente. Las empresas deberían pensar en la posibilidad de realizar comprobaciones de antecedentes a intervalos regulares durante el contrato de empleo, sobre todo en los puestos críticos que tienen acceso a información restringida.
  
**Acuerdos de directivas de uso de equipos**  
Los acuerdos de uso de redes o equipos son importantes, no sólo para informar a los empleados acerca de cómo pueden utilizar los activos de la empresa, sino también para informarles acerca de las directivas para supervisar la actividad de la red y el uso de equipos, además de las posibles consecuencias derivadas de cualquier intento de infringirlas.
  
Las directivas de uso también sirven de documentos legales para definir estos temas en términos explícitos y se necesita la firma de los empleados para confirmar que están de acuerdo. Si no hay pruebas de que un empleado conoce las directivas de supervisión de la seguridad internas y de que se espera un uso aceptable de los activos de la empresa, es muy difícil denunciar a una persona en caso de que cometa un acto ilícito.
  
También es importante que haya una advertencia de acceso y uso no autorizado en cualquier punto de acceso a la red de la empresa que informe a la persona que se trata de una red privada cuyo acceso está prohibido y que, si entra, será denunciado. Por ejemplo, los sistemas operativos Windows poseen la capacidad de mostrar una advertencia durante los eventos de intentos de inicio de sesión que se puede utilizar para informar a los usuarios de que están a punto de obtener acceso a un recurso protegido de la empresa y que está prohibido el acceso sin autorización.
  
Aunque este artículo no trata de los aspectos legales relacionados con el texto exacto y el uso de dichos documentos, es importante mencionar que esos documentos y directivas deberían existir. En Internet, existen muchos ejemplos de esas cláusulas de uso y acceso, pero esos materiales sólo se deberían preparar con la ayuda y el asesoramiento de expertos legales cualificados, porque existen muchos aspectos legales internacionales y locales que hay que tener en cuenta.
  
**Separación de obligaciones**  
Al igual que las diferentes funcionalidades de los sistemas están segmentadas en la red por motivos de seguridad, rendimiento y disponibilidad, también es importante duplicar y separar las obligaciones a la hora de desarrollar los requisitos del personal de un departamento de seguridad de TI.
  
Las funciones importantes que implican el acceso o el control de datos y sistemas confidenciales deberían ser redundantes siempre que sea posible y razonable, no sólo para protegerse contra los problemas relacionados con la pérdida de conocimientos si se va un miembro del personal, sino también para disponer de una función de seguridad en casos de sabotaje interno. Por ejemplo, sería difícil recuperarse si el único miembro del personal que conoce las contraseñas de administrador se va sin proporcionarlas.
  
Además de la redundancia de funciones, también es importante separar funciones críticas, especialmente para supervisar la seguridad. Asimismo, las personas que administran la red no deberían ser responsables de revisar la información de auditoría de seguridad, y el personal de seguridad no debería tener los mismos derechos administrativos que los administradores. En ocasiones, también es necesario salvaguardar la información departamental del personal administrativo para aplicar en mayor grado la separación de obligaciones. Por ejemplo, algunas empresas tienen unidades organizativas con sus propios sistemas o cuentas administrativas para proteger la información confidencial (por ejemplo, financiera o de recursos humanos).
  
**Nota**   Aunque puede que no sea posible evitar que los propietarios de las cuentas de administradores encuentren la forma de burlar las separaciones de obligaciones, es importante establecer al menos unas directrices sobre el uso de la autoridad administrativa en las que se recoja el principio de separación de obligaciones.
  
**Validación de la funcionalidad de supervisión de la seguridad**  
Se debería planear cuidadosamente la realización de pruebas regulares de la solución de supervisión de la seguridad antes de implementar el programa. Aunque es importante realizar pruebas iniciales para validar la solución de supervisión de la seguridad, también lo es programar pruebas regulares, ya que el entorno de seguridad cambia continuamente.
  
Las pruebas pueden incluir intentos de intrusión y el uso de privilegios administrativos para determinar si la solución es efectiva a la hora de localizar dichas actividades. Sin embargo, también es importante investigar los últimos avances en técnicas de seguridad y perfiles de ataque para determinar si hay que realizar cambios. Las amenazas a las redes empresariales cambian constantemente a medida que los atacantes se ajustan a las implementaciones de seguridad, por lo que las defensas y las técnicas de supervisión deberían evolucionar constantemente para ser efectivas.
  
**Establecimiento de procesos**  
Para separar los eventos autorizados de los no autorizados, es necesario crear un plan para los procesos obligatorios establecidos de control de cambios y administración de problemas. Dicho plan podría proporcionar un rastro en papel detallado con el que se podría establecer una correlación cruzada con la información del registro de seguridad. Aunque la mayoría de las empresas realiza un seguimiento de problemas por medio de vales del departamento de soporte u otros procesos, el control de cambios se suele relegar al olvido. El control de cambios es un mecanismo necesario, y se puede utilizar no sólo para realizar un seguimiento de tendencias con el fin de detectar sistemas o aplicaciones problemáticas, sino que también es un mecanismo de seguridad vital.
  
Los procesos de control de cambios deberían ser procedimientos proactivos, y los cambios reactivos se deberían limitar para utilizar un proceso de administración de problemas. El proceso de control de cambios debería requerir la aprobación antes de realizar algún cambio, e incluye los detalles siguientes:
  
-   Nombre de persona que lo aprueba
  
-   Nombre de la persona que lo implementa
  
-   Calendario del cambio
  
-   Razones del cambio
  
-   Cambios que se deben realizar
  
-   Sistemas afectados por el cambio
  
-   Impacto en la empresa
  
-   Resultados reales del cambio
  
También se debería establecer un proceso de aprovisionamiento de usuarios por medio de un procedimiento para agregar/cambiar/eliminar usuarios que también crea una pista de auditoría para protegerse contra cambios de cuentas no autorizados. Antes de establecer un proceso de esta naturaleza, es importante realizar una auditoría de seguridad de las cuentas de usuario actuales para comprobar la validez de de las mismas y validar periódicamente esa lista a medida que cambia.
  
Podría resultar de ayuda utilizar soluciones de administración de identidades y aprovisionamiento de usuarios automático \[por ejemplo, Microsoft Identity Integration Server (MIIS) 2003\], además de automatizar los cambios de cuentas y los procesos que hay detrás de esas actividades. Al utilizar soluciones de ese tipo, es importante recordar que las cuentas de administrador aún conservan la capacidad de crear nuevas cuentas, pero no es necesario, porque las cuentas se crearían por medio de procesos establecidos. Por tanto, los eventos asociados con la creación de cuentas, como el evento 624, sólo se deberían correlacionar con la cuenta de MIIS 2003 u otra cuenta de servicio establecida que se utilice para el aprovisionamiento automático.
  
Aunque en los medios de comunicación no se deja de hablar de amenazas externas para las redes empresariales, la experiencia demuestra que las redes y los datos de las empresas son mucho más vulnerables a sufrir pérdidas a causa de configuraciones incorrectas o errores de procedimientos. Es importante protegerse contra todas las amenazas, ya sean externas o internas. Muchos fabricantes se dedican exclusivamente a ayudar a las empresas a protegerse de las amenazas externas, pero no existe ningún paquete que las proteja de los errores que cometen las personas responsables de la red y la seguridad. La mejor forma de mitigar esos riesgos es implementar y aplicar procesos y procedimientos correctos relacionados con los cambios que se producen en la red.
  
**Definición de respuestas de seguridad**  
Para limitar el daño que puede causar una infracción de seguridad, es importante desarrollar un plan de respuesta adecuado y establecer procesos para responder a los incidentes. Los informes de incidentes, la formación de un equipo de respuesta rápido y un protocolo de respuesta de emergencia son buenos ejemplos. La velocidad y la efectividad de las respuestas a los incidentes mejorarán el perfil de seguridad de la organización y limitarán el daño percibido y real que puede causar un intento de intrusión.
  
La formación de un proceso de respuesta de seguridad establecido no sólo ayuda a limitar el daño que puede producir un incidente real, sino que también actúa como un sistema disuasorio, ya que notifica al personal y a otros individuos que cualquier incidente desencadenará una respuesta inmediata y coordinada a cualquier infracción de la seguridad.
  
**Recursos humanos**  
Según los estudios realizados por CERT y el Servicio Secreto de EE.UU., muchos ataques de origen interno se podrían evitar si las empresas tuvieran más información y tomaran medidas en respuesta a las amenazas o los cambios de comportamiento de un empleado. Probablemente, los recursos de seguridad más valiosos de una empresa son los propios empleados, porque ellos saben si un miembro del personal está descontento o alertan al personal adecuado cuando un visitante se comporta de forma sospechosa. De hecho, una de las primeras medidas que tomaría un grupo de auditoría externo sería darse un "paseo" para encontrar las contraseñas escritas en papel, localizar dispositivos no protegidos o intentar realizar intrusiones conectándose directamente a la red interna.
  
El personal de la empresa puede representar un importante nivel de protección contra amenazas internas y externas. Si se fomentan políticas de puertas abiertas para discutir cualquier comportamiento preocupante de los compañeros y se forma al personal de soporte técnico para recoger informes de actividades inusuales en los equipos, se puede ayudar a mitigar los intentos de intrusión o los incidentes de malware. La formación interna también es un método importante para enseñar a los empleados a localizar tipos de comportamientos en los equipos de los que se debería informar. La formación también sirve como medida preventiva para evitar ataques de ingeniería social.
  
##### Correlación de infracciones de la directiva de seguridad con eventos de auditoría
  
Para correlacionar la información de eventos de seguridad, es necesario recopilar eventos de seguridad de múltiples sistemas y colocar esos datos en una ubicación central protegida. Cuando ya se ha correlacionado la información de seguridad, el personal adecuado puede analizar este repositorio central para identificar infracciones o ataques externos. Este repositorio no sólo es importante para el análisis de investigación, sino también como herramienta para detectar ataques y solucionar vulnerabilidades. Aunque existen muchas soluciones de terceros que tienen esta finalidad, los productos y herramientas de Microsoft siguientes pueden ayudar a satisfacer esta necesidad al correlacionar los registros de sucesos de seguridad y otra información de supervisión de la seguridad en un repositorio central.
  
**EventCombMT**  
EventCombMT (multiproceso) es un componente de la [*Guía de seguridad de Windows 2003*](http://go.microsoft.com/fwlink/?linkid=14845), que está disponible en http://go.microsoft.com/fwlink/?LinkId=14845 (puede estar en inglés). Esta herramienta puede analizar y recopilar eventos de los registros de sucesos en varios equipos. Funciona como una aplicación multiproceso que permite al usuario especificar cualquier número de parámetros al examinar los registros de sucesos. Por ejemplo:
  
-   Id. de evento (individuales o múltiples)
  
-   Intervalos de Id. de evento
  
-   Orígenes de evento
  
-   Texto de eventos específicos
  
-   Duración del evento en minutos, horas o días
  
[![](images/Cc875806.SMAAD4(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875806.smaad4_big(es-es,technet.10).gif)
  
**Figura 4. EventCombMT**
  
En EventCombMT, se incluyen determinadas categorías de búsqueda, como los bloqueos de cuentas (que se muestran en la figura anterior), que proporcionan una funcionalidad de búsqueda de los eventos siguientes:
  
-   **529**. Error de inicio de sesión (nombre de usuario o contraseña incorrectos).
  
-   **644**. Una cuenta de usuario se ha bloqueado automáticamente.
  
-   **675**. La autenticación previa ha producido un error en un controlador de dominio (contraseña incorrecta).
  
-   **676**. Error de solicitud de vale de autenticación
  
-   **681**. Error de inicio de sesión
  
Otro de los eventos relacionados con la seguridad que no reside en el archivo de registro de seguridad es el evento 12294, que pertenece al archivo de registro del sistema. Es importante agregar este evento a cualquier búsqueda, porque se puede utilizar para detectar intentos de ataque a la cuenta del administrador, que no tiene ningún umbral de bloqueo y, por tanto, es un objetivo vulnerable y tentador para cualquier posible atacante.
  
**Nota**   El evento 12294 aparece como un evento del Administrador de cuentas de seguridad (SAM) en el registro del sistema, no en el registro de seguridad.
  
EventCombMT puede guardar eventos en una tabla de base de datos de Microsoft SQL Server™, por lo que resulta útil para el almacenamiento y el análisis a largo plazo. Después de almacenar la información de los registros de sucesos en una base de datos de SQL Server, se puede obtener acceso a ella mediante varios programas diferentes como, por ejemplo, Analizador de consultas SQL, Microsoft Visual Studio® .NET o numerosas utilidades de terceros.
  
**Log Parser 2.2**  
Log Parser es una herramienta gratuita de Microsoft que se puede utilizar para buscar datos en un registro, cargar registros en una base de datos de SQL o un archivo CSV, y generar informes a partir de registros de sucesos, archivos CSV u otros formatos de registro (incluidos registros de IIS, para los cuales se diseñó originalmente).
  
Esta herramienta de scripting de la línea de comandos se puede utilizar como recurso para correlacionar la información de registro de sucesos en una ubicación central, analizar los eventos que resultan de interés e incluso generar informes. Sin embargo, la interfaz de línea de comandos y scripting requiere un nivel de detalle que está fuera del ámbito de este artículo. Hay disponible más información acerca de Log Parser, sus usos y los recursos de script en la página de [Log Parser 2.2](http://www.microsoft.com/technet/scriptcenter/tools/logparser/default.mspx), en www.microsoft.com/technet/scriptcenter/tools/logparser/default.mspx, y en el artículo "[Cómo funciona Log Parser 2.2](http://www.microsoft.com/technet/community/columns/profwin/pw0505.mspx)", en www.microsoft.com/technet/community/columns/profwin/pw0505.mspx (pueden estar en inglés).
  
**EventQuery.vbs**  
EventQuery.vbs es una herramienta que se incluye en Windows XP. Se puede utilizar para elaborar una lista de eventos y propiedades de eventos a partir de uno o varios registros de sucesos. Para utilizar este script, se debe estar ejecutando el host de script basado en comandos (CScript.exe). Si no se ha establecido el valor predeterminado de Windows Script Host en CScript, puede hacerlo con el comando siguiente:
  
```  
Cscript //h:cscript //s //nologo  
```  
Esta utilidad de script de la línea de comandos es muy flexible y puede aceptar muchos parámetros diferentes para ajustar el filtrado y el formato que se aplican a su resultado. Para obtener más información acerca del uso de esta herramienta y los parámetros disponibles, consulte el tema [Administración de registros de sucesos desde la línea de comandos](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/event_commandline.mspx?mfr=true), en la documentación de Windows XP Professional en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/event\_commandline.mspx?mfr=true (puede estar en inglés).
  
**Registro de Internet Information Services**  
La funcionalidad de registro adicional disponible con Internet Information Services (IIS) permite informar de la identidad de los visitantes del sitio, a qué han tenido acceso los visitantes y cuándo lo han tenido. Los registros de IIS indican los intentos correctos e incorrectos de obtener acceso a los sitios, carpetas virtuales y archivos, y se pueden configurar para auditar de manera selectiva esa información con el fin de reducir al mínimo los requisitos de almacenamiento y limitar el registro de información innecesaria.
  
Estos registros se pueden almacenar en formato nativo como archivos, que luego se pueden filtrar con una de las herramientas de análisis e intercalación que se han mencionado anteriormente, o directamente en una ubicación central mediante el registro de bases de datos de ODBC, que se puede utilizar para almacenar la información en una base de datos de SQL o en cualquier otra base de datos compatible con ODBC.
  
Hay ciertas actividades y secuencias de eventos que se deberían supervisar atentamente como, por ejemplo:
  
-   Varios comandos incorrectos que intentan ejecutar archivos ejecutables o scripts.
  
-   Número excesivo de intentos frustrados de inicio de sesión desde una sola dirección IP o intervalo de direcciones IP, lo que puede indicar un intento de denegación de servicio o de elevación de privilegios.
  
-   Intentos frustrados de obtener acceso o modificar archivos .bat o .cmd.
  
-   Intentos no autorizados de cargar archivos en una carpeta que contiene archivos ejecutables.
  
A partir de Windows Server 2003, se han incorporado en IIS nuevas capacidades de auditoría, que se pueden utilizar con las nuevas capacidades de registro de IIS, que están integradas directamente en el Visor de sucesos, o se puede tener acceso a ellas con páginas ASP para utilizar soluciones personalizadas. Para obtener más información acerca de estas capacidades y cómo implementarlas, consulte la documentación de IIS.
  
**Microsoft Internet Security and Acceleration Server**  
Microsoft Internet Security and Acceleration (ISA) Server es un paquete avanzado con estado y un firewall de nivel de aplicación que también ofrece funcionalidades adicionales, que incluyen capacidades de almacenamiento en caché de proxy y VPN.
  
Además de la utilidad de defensa activa que proporciona ISA Server, también puede servir como una función de supervisión de la seguridad gracias a su capacidad de actuar como una herramienta de registro centralizada que puede supervisar toda la actividad que se produce en el perímetro de la red. Las capacidades de registro de ISA Server incluyen la posibilidad de capturar el tráfico del firewall, la actividad del proxy web y los registros de filtrado de mensajes SMTP. Estos registros se pueden filtrar, consultar o supervisar en tiempo real con el Visor de registros en tiempo real integrado (que se muestra en la pantalla siguiente) o con el escritorio de supervisión.
  
[![](images/Cc875806.SMAAD5(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875806.smaad5_big(es-es,technet.10).gif)
  
**Figura 5. Visor de registros en tiempo real de Microsoft ISA Server 2004**
  
Además de la funcionalidad de registro integrada, ISA Server tiene una función de alerta que puede enviar alertas a través del correo electrónico y entradas de registro de sucesos, o incluso iniciar o detener servicios. La capacidad de registrar las actividades sospechosas en entradas de registros de sucesos es especialmente útil para los temas que nos ocupan. Esta capacidad permite registrar y almacenar posible información de ataques en una ubicación centralizada con otros datos de registro de sucesos de auditoría.
  
Además de esta funcionalidad de registro y alerta, también hay herramientas de detección de intrusiones integradas que se pueden habilitar en ISA Server. Estos servicios de detección de intrusiones (IDS) básicos tienen la licencia de Internet Security Systems e incluyen varios filtros de paquetes IP, filtros de aplicaciones DNS y un filtro de aplicaciones POP. Estos servicios son capaces de detectar numerosas vulnerabilidades comunes.
  
La funcionalidad de detección de intrusiones de ISA Server es capaz de registrar eventos y generar alertas cuando se detectan ataques potenciales. También puede finalizar servicios o conexiones sospechosas. Entre algunos de los perfiles de ataques que se pueden detectar, se incluyen:
  
-   WinNuke (ataques de tipo "Windows out-of-band")
  
-   Ataques de tipo "Land"
  
-   Ataques de tipo "IP half scan"
  
-   Ataques de tipo "UDP bomb"
  
-   Ataques de tipo "Port scan"
  
-   Ataques de desbordamiento de longitud de nombre de host DNS
  
-   Transferencias de zonas DNS desde puertos TCP/IP altos o con privilegios
  
En cualquier caso, con independencia de si se utiliza ISA Server u otro tipo de solución IDS o de firewall, es importante tener en cuenta la red perimetral (también conocida como DMZ, o zona desmilitarizada, y subred apantallada) a la hora de diseñar un sistema de supervisión de la seguridad y detección de ataques.
  
**Microsoft Operations Manager 2005**  
Microsoft Operations Manager (MOM) supervisa múltiples servidores de un entorno empresarial desde una ubicación central. El agente MOM recopila eventos de los registros de sucesos y se los reenvía al servidor de administración MOM que, a continuación, los coloca en la base de datos MOM. MOM 2005 y las versiones posteriores son capaces de recopilar eventos de equipos que no ejecutan agentes MOM.
  
MOM utiliza las reglas de su Management Pack para identificar problemas que afectan a la efectividad operativa de los servidores. Se pueden crear reglas adicionales para supervisar eventos específicos y, cuando se produzcan esos eventos, enviar notificaciones de alerta a través del correo electrónico, mensajes emergentes o directamente a localizadores (pagers).
  
Aunque MOM dispone de numerosas funciones que son útiles para supervisar la seguridad y detectar ataques, no fue diseñado con ese propósito. Las versiones futuras de MOM incluirán más funcionalidades para la recopilación de registros de seguridad.
  
**Microsoft Systems Management Server 2003**  
Microsoft Systems Management Server (SMS) 2003 puede supervisar y administrar servidores y estaciones de trabajo de una red desde una ubicación central. Aunque se concentra en las tareas de administración, también puede ser útil en funciones esenciales relacionadas con la seguridad de una solución de supervisión al administrar la distribución de las actualizaciones de seguridad y al informar acerca de las instalaciones de software no autorizadas.
  
La funcionalidad de inventario SMS puede ayudar a satisfacer una necesidad vital de las soluciones de supervisión de la seguridad al actuar como una solución de administración de inventarios centralizada en tiempo real, lo cual es imprescindible para cualquier proceso de supervisión y auditoría de seguridad.
  
##### Implementación de análisis de investigación
  
Los análisis de investigación son un tema muy amplio en el que este artículo no puede profundizar. En concreto, este artículo no se ocupa de los requisitos del tratamiento de pruebas de los análisis de investigación ni describe datos de investigación aparte de la información suministrada por los registros de sucesos de seguridad.
  
Los análisis de investigación permiten determinar el momento, la gravedad y los resultados de las infracciones de seguridad, e identificar los sistemas afectados por los atacantes. Para que sea efectiva, la información recopilada en estos análisis debe contener lo siguiente:
  
-   Hora del ataque
  
-   Duración del ataque
  
-   Sistemas afectados por el ataque
  
-   Cambios realizados durante el ataque
  
Una vez más, dado el enorme número de detalles relacionado con las leyes que rigen los procedimientos de presentación de pruebas, los tipos de datos clave relacionados con las investigaciones, las herramientas necesarias para los análisis, la recopilación de pruebas, la conservación de las mismas y las metodologías de investigación, es imposible tratar este tema en profundidad en este artículo. Sin embargo, existen algunos recursos excelentes como, por ejemplo, la [Guía básica de la investigación informática](http://www.cert.org/archive/pdf/frgcf_v1.3.pdf) de CERT en www.cert.org/archive/pdf/FRGCF\_v1.3.pdf (puede estar en inglés), que también está disponible en sitios dedicados a los estudios de la seguridad.
  
**Aspectos de la empresa**  
El planeamiento del uso de los análisis de investigación se diferencia de los métodos que se emplean en otras soluciones en que implica la investigación de incidentes después de que se hayan producido, en lugar de ser un análisis de los incidentes en tiempo real. Por tanto, se debe mantener un historial detallado de eventos de varios sistemas durante un período de tiempo más largo. A causa de esta necesidad adicional, un sistema de análisis de investigación efectivo debería estar centralizado y disponer de una capacidad de almacenamiento importante para almacenar un gran número de registros en una estructura de base de datos adecuada.
  
Una de las decisiones que deben tomar las empresas es el tiempo que se deben guardar dichos registros para los análisis de investigación, y también qué tipo de ciclo de conservación se debería utilizar. Esos factores pueden afectar enormemente a los requisitos de almacenamiento y equipamiento de un plan de análisis de investigación. En la tabla siguiente, se ilustran los tiempos de conservación normales que se suelen utilizar en las empresas que tienen establecidos planes de análisis de investigación.
  
**Tabla 2. Límites de almacenamiento para análisis de investigación**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Factores de almacenamiento</p></th>
<th><p>Límites de almacenamiento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Almacenamiento en línea (base de datos)</p></td>
<td style="border:1px solid black;"><p>21 días</p></td>
<td style="border:1px solid black;"><p>Proporciona acceso rápido a los detalles del evento</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Almacenamiento sin conexión (copia de seguridad)</p></td>
<td style="border:1px solid black;"><p>180 días</p></td>
<td style="border:1px solid black;"><p>Límite de archivado razonable para la mayoría de las organizaciones</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Entorno regulado</p></td>
<td style="border:1px solid black;"><p>7 años</p></td>
<td style="border:1px solid black;"><p>Requisito de archivado para empresas reguladas</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Agencias de inteligencia</p></td>
<td style="border:1px solid black;"><p>Permanente</p></td>
<td style="border:1px solid black;"><p>Requisitos organizativos de defensa e inteligencia</p></td>
</tr>
</tbody>
</table>
  
**Nota**   En las prácticas reguladas de algunos sectores (por ejemplo, en los que se manejan registros médicos), se utilizan especificaciones de límites temporales (en términos de "no conservar más de") en lugar de un tiempo de conservación fijo.
  
Una de las opciones que se debería tener en cuenta es el uso de bases de datos en línea para conservar los datos de los análisis de investigación en línea y archivar los eventos más antiguos en un formato que se comprima mejor como, por ejemplo, en texto delimitado por comas (también conocido como valores separados por comas o CSV) para el almacenamiento sin conexión. Si es necesario, los archivos CSV se pueden volver a importar a la base de datos en línea para analizarlos.
  
Asegúrese de que, sea cual sea la solución que se elija, satisfaga las necesidades de la empresa en caso de que haya que investigar rápidamente los eventos recientes, con la capacidad añadida de recuperar los eventos más antiguos cuando sea necesario. Debería haber un historial de incidentes de seguridad de la empresa, además de una lista de recursos disponibles, para guiar el desarrollo de un plan que proporcione la mejor combinación de tiempos de conservación de datos para el almacenamiento en línea y sin conexión.. Si es posible, pruebe el sistema de recopilación de eventos en una base de datos razonablemente grande con los informes que desee ejecutar y compruebe que se ejecutan en un tiempo razonable y proporcionan información útil.
  
También hay que pensar en la seguridad de los datos de los análisis de investigación, porque el acceso a esta información no es necesario normalmente. Si se necesita obtener acceso a ella, sólo se debería proporcionar este permiso a unos cuantos miembros seleccionados del personal de seguridad de confianza. El acceso del administrador a esta información debería estar regulado estrictamente en un proceso de control de cambios establecido que disponga de funciones de supervisión adicionales. Nadie más debería tener acceso a esta información, interrumpir su recopilación o modificarla.
  
**Aspectos técnicos**  
El planeamiento de una solución de supervisión de la seguridad para análisis de investigación requiere un aprovisionamiento muy cuidadoso para recopilar de forma segura y fiable, y almacenar, un gran número de eventos. Los requisitos de supervisión de la seguridad son similares a los que se detallan en los escenarios de otras soluciones, pero necesitan muchos más recursos para el almacenamiento en la base de datos y una administración de los datos enormemente eficiente.
  
Entre algunos de los desafíos técnicos que hay que tener en cuenta, se incluyen:
  
-   Almacenamiento fiable y seguro de los datos en línea.
  
-   Aprovisionamiento de grandes cantidades de espacio en disco de alto rendimiento para el almacenamiento en línea.
  
-   Sistemas de copia de seguridad fiables para almacenar los eventos más antiguos en medios de archivado.
  
-   Procesos seguros de administración del almacenamiento de los archivos.
  
-   Procesos de restauración probados para recuperar información del almacenamiento de copia de seguridad.
  
Puede que estos desafíos no sean específicos de la supervisión de la seguridad, ya que los administradores de bases de datos tienen que enfrentarse a problemas similares en el caso de otras aplicaciones como, por ejemplo, las bases de datos de procesamiento de transacciones en línea (OLTP). Sin embargo, a diferencia de otras aplicaciones de base de datos tradicionales, como OLTP, la base de datos de análisis de investigación debe ocuparse de un volumen mucho mayor de escrituras que de lecturas.
  
**Requisitos**  
Para planear un programa de análisis de investigación efectivo, se deben cumplir los requisitos siguientes:
  
-   Configuración adecuada de las opciones de registro de la seguridad.
  
-   Establecimiento de procesos seguros de comprobación de la entrada de registros.
  
-   Un punto y un proceso de recopilación seguros y centralizados para los registros de seguridad.
  
-   Almacenamiento fiable de la información de supervisión de la seguridad.
  
-   Desarrollo de planes y programas de archivado efectivos.
  
Los requisitos, las capacidades y las restricciones normativas de un entorno empresarial se deberían tener en cuenta en todas las soluciones de análisis de investigación, porque cada organización es diferente en este respecto.
  
#### Implementación y administración de la solución
  
La capacidad de identificar, perfilar y responder a un ataque es el objetivo básico de cualquier solución de supervisión de la seguridad y detección de ataques. Por lo tanto, la mayor parte de esta sección está dedicada a explicar con detenimiento los eventos pertinentes que se encuentran en los registros de sucesos que pueden indicar que se está produciendo un ataque. Teniendo esto en cuenta, el plan de supervisión de la seguridad y detección de ataques debería cumplir los requisitos siguientes:
  
-   Detectar infracciones de directivas internas
  
-   Identificar ataques de orígenes externos
  
-   Permitir análisis de investigación eficientes y precisos
  
La solución que se detalla en este artículo utiliza componentes similares para cada uno de los tres requisitos. La implementación de capacidades de análisis de investigación tiene otros requisitos que se explicarán más adelante.
  
##### Supervisión de la seguridad y detección de ataques
  
La solución de supervisión de la seguridad y detección de ataques requiere que se planeen los niveles adecuados de auditorías de seguridad en las áreas siguientes:
  
-   Administración de cuentas
  
-   Acceso a archivos protegido
  
-   Cambios de directivas de seguridad
  
-   Creación y eliminación de confianzas
  
-   Uso de derechos de usuario
  
-   Reinicios del sistema y cambios de hora
  
-   Modificaciones del Registro
  
-   Ejecución de programas desconocidos
  
El sistema de supervisión de la seguridad y detección de ataques recopila información de los registros de sucesos de seguridad y la coloca en una ubicación central. A continuación, los auditores de seguridad pueden analizar los datos en busca de actividades sospechosas. Además, esta información también se puede almacenar y archivar para poder realizar posteriormente un análisis de investigación si surge la necesidad.
  
Uno de los componentes principales de esta solución es la capacidad de configurar una función de Microsoft Windows 2003 con Service Pack 1 (SP1) y Microsoft Windows XP con Service Pack 2 (SP2) denominada auditoría por usuario. Las auditorías por usuario permiten especificar diferentes niveles de auditoría para cuentas de usuario específicas, por lo que se permite un nivel de detalle de auditoría mayor en cuentas confidenciales o sospechosas.
  
**Requisitos previos de la solución**  
Para configurar esta solución de supervisión de la seguridad y detección de ataques, hay que cumplir los requisitos previos siguientes:
  
-   Los servidores deben ejecutar Windows Server 2003 SP1 o posterior en un dominio de Active Directory.
  
-   Los equipos cliente deben ejecutar Windows XP SP2 o posterior como miembros de un dominio de Active Directory.
  
**Nota**   Si los equipos del perímetro de una empresa no residen en un dominio, no se pueden configurar con las opciones de directiva de grupo de Active Directory. Sin embargo, se pueden utilizar plantillas y directivas locales para configurar esos sistemas.
  
Este artículo se concentra en la identificación de las firmas características de los ataques y no recomienda utilizar ninguna tecnología específica para la intercalación de eventos de seguridad, aunque sí enumera algunas posibles soluciones. Después de elegir un mecanismo de intercalación adecuado, se pueden utilizar los eventos y secuencias de eventos que se incluyen en este artículo para diseñar consultas y alertas para identificar comportamientos sospechosos.
  
##### Infracciones de directivas y umbrales
  
Las nuevas funciones de Microsoft Windows Server 2003 y Microsoft Windows XP con SP2 permiten niveles de auditoría selectivos en cuentas de usuario individuales. Por ejemplo, se pueden establecer niveles de auditoría para informar únicamente de las actividades de inicio y cierre de sesión de todos los usuarios y, al mismo tiempo, auditar todas las actividades de un usuario específico. También se puede utilizar la auditoría selectiva por usuario para reducir el volumen de eventos del registro de seguridad, al permitir excluir determinadas cuentas de la generación de auditorías relacionadas con ciertas actividades. Las cuentas de usuario son las únicas que se pueden auditar con esta funcionalidad; los grupos de seguridad y distribución no se pueden auditar de esta forma. Las cuentas que pertenecen al grupo local de administradores no se pueden excluir de la auditoría por medio del mecanismo de auditoría selectiva por usuario.
  
La utilidad de línea de comandos que se utiliza para establecer la directiva de auditoría por usuario con el fin de realizar auditorías selectivas en Windows Server 2003 y Windows XP SP2 es Auditusr.exe. Las categorías de auditoría selectiva válidas son:
  
-   Evento del sistema
  
-   Inicio o cierre de sesión
  
-   Acceso a objetos
  
-   Uso de privilegios
  
-   Seguimiento detallado
  
-   Cambio de directiva
  
-   Administración de cuentas
  
-   Acceso del servicio de directorio
  
-   Inicio de sesión de la cuenta
  
Cuando se ejecuta Aauditusr.exe desde la línea de comandos sin ningún parámetro, aparece la configuración de auditoría selectiva actual, que al principio estará en blanco. Existen dos formas de rellenar los parámetros de la auditoría selectiva: especificar cada usuario manualmente como parámetros de la línea de comandos o introducir varios parámetros importando un archivo de configuración de auditoría por usuario.
  
Audituser.exe se utiliza del siguiente modo:
  
```  
Audituser.exe /parámetro cuentaDeUsuario:”categoría”  
```  
(o una lista de categorías delimitadas por comas).
  
Por ejemplo, para habilitar la auditoría de errores de los eventos del sistema y los eventos de inicio o cierre de sesión en una cuenta denominada LocalUser, se utilizaría la siguiente entrada en la línea de comandos:
  
```  
Audituser /if LocalUser:”System Event”,”Logon/Logoff”  
```  
En la línea de comandos, se pueden utilizar los comandos siguientes:
  
-   **/is** – agrega o cambia una entrada incluida correctamente
  
-   **/if** – agrega o cambia una entrada no incluida correctamente
  
-   **/es** – agrega o cambia una entrada excluida correctamente
  
-   **/ef** – agrega o cambia una entrada no excluida correctamente
  
-   **/r** – elimina todas las entradas de auditorías por usuario de una cuenta de usuario específica
  
-   **/ra** – elimina todas las entradas de auditorías por usuario de todas las cuentas de usuario
  
-   **/e** – exporta configuraciones al nombre de archivo especificado
  
-   **/i** – importa configuraciones desde un nombre de archivo especificado
  
Los archivos de configuración de auditorías por usuario son archivos de texto sin formato, que se utilizan de la forma que se muestra en la figura siguiente.
  
![](images/Cc875806.SMAAD6(es-es,TechNet.10).gif)
  
**Figura 6. Archivo de importación Auditusr.exe de ejemplo**
  
**Nota**   El archivo de importación debe comenzar con la línea “Auditusr 1.0”, tal y como se muestra, para que la importación se realice correctamente.
  
Por tanto, para importar el archivo de configuración de auditoría de la figura anterior, se utilizaría el comando siguiente:
  
```  
 Audituser /i path\\audit.txt  
```  
Utilice esta utilidad para establecer umbrales para la información de registro de auditoría, lo que puede reducir los requisitos de almacenamiento y aumentar la probabilidad de detectar los intentos de intrusión.
  
##### Infracciones de directivas de seguridad y correlación de eventos de auditoría
  
Aunque en esta sección no se realiza ninguna distinción entre infracciones de directivas de orígenes internos y externos, es importante saber que las infracciones de directivas internas pueden ser tan devastadoras para una empresa como los ataques que se originan en el exterior. Tal y como se ha mencionado ya en este artículo, un porcentaje importante de los ataques malintencionados es de origen interno, y este porcentaje no incluye los daños accidentales provocados por el uso inadecuado de privilegios elevados al margen de los procedimientos establecidos.
  
Dado el riesgo que implica el abuso accidental o intencionado de privilegios elevados de origen interno, es importante establecer directivas y procedimientos que rijan el uso adecuado de esos privilegios, y establecer pistas de auditoría para establecer correlaciones cruzadas. Después de crear un proceso de administración de cambios y una directiva de documentación, se puede establecer una correlación para que la información de auditoría coincida con los eventos aprobados y no aprobados, y así facilitar la detección de comportamientos inusuales en la empresa. Esta sección le ayudará a establecer esa correlación mediante una descripción de los diferentes tipos de evento de los que se puede realizar un seguimiento y cómo se pueden aplicar a directivas y procesos.
  
**Acceso a equipos no autorizados**  
El personal de soporte técnico y administración cada vez utiliza más las instalaciones de administración remota (por ejemplo, Terminal Services) para conectarse a los sistemas remotos y administrarlos. Se debería supervisar estos sistemas para detectar intentos de inicio de sesión interactivos y se debería comprobar la validez de cada intento de conexión. Esas comprobaciones deberían realizar las acciones siguientes:
  
-   Identificar inicios de sesión de cuentas de servicio.
  
-   Registrar intentos de acceso por cuentas no autorizadas.
  
-   Investigar intentos procedentes de áreas geográficas inusuales.
  
-   Elaborar una lista de intentos procedentes de intervalos de direcciones IP externas.
  
Se debería prestar especial atención a la supervisión de los activos de gran valor. Esos recursos críticos deberían residir en servidores específicos configurados con opciones de supervisión de auditorías y control de acceso estrictas.
  
En la siguiente tabla, se incluyen los eventos de auditorías de inicio de sesión que se deberían comparar con listas de cuentas autorizadas si aparecen en sistemas de activos de gran valor.
  
**Tabla 3. Eventos de uso de equipos no autorizados**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>528</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión realizado</p></td>
<td style="border:1px solid black;"><p>Compruebe el nombre de la estación de trabajo y el nombre de la cuenta de usuario. Asegúrese de que la dirección de red de origen reside en una red.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>529</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: nombre de usuario desconocido o contraseña incorrecta</p></td>
<td style="border:1px solid black;"><p>Compruebe los intentos en los que el nombre de la cuenta de destino sea igual al administrador o la cuenta de administrador predeterminada con un nuevo nombre. Compruebe también si se han producido muchos errores de inicio de sesión que estén por debajo del umbral de bloqueo de la cuenta.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>530</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: restricciones de tiempo</p></td>
<td style="border:1px solid black;"><p>Indica un intento de inicio de sesión fuera del intervalo de tiempo permitido. Compruebe el nombre de la cuenta de usuario y el nombre de la estación de trabajo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>531</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: la cuenta está desactivada.</p></td>
<td style="border:1px solid black;"><p>Compruebe el nombre de la cuenta de destino y el nombre de la estación de trabajo. Este evento puede indicar intentos de intrusión de antiguos usuarios y debería dar lugar a una investigación.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>532</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: la cuenta de usuario especificada ha caducado</p></td>
<td style="border:1px solid black;"><p>Compruebe el nombre de la cuenta de destino y el nombre de la estación de trabajo. Este evento puede indicar intentos de intrusión de empleados contratados o temporales y debería dar lugar a una investigación.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>533</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: el usuario no tiene permiso para iniciar una sesión en este equipo</p></td>
<td style="border:1px solid black;"><p>Indica que es posible que un usuario esté intentando iniciar sesión en estaciones de trabajo restringidas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>534</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: tipo de inicio de sesión no permitido</p></td>
<td style="border:1px solid black;"><p>Compruebe el nombre de la cuenta de destino, el nombre de la estación de trabajo y el tipo de inicio de sesión. Este evento indica un error en el intento de iniciar sesión de manera interactiva con credenciales de cuenta de servicio cuando la configuración de la directiva de grupo impide los inicios de sesión interactivos en esas cuentas.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>535</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: la contraseña ha caducado</p></td>
<td style="border:1px solid black;"><p>Indica que un usuario está intentando iniciar sesión con una cuenta que posee una contraseña expirada. Debería iniciarse una investigación si se repite sin que haya un cambio de contraseña correspondiente o una llamada al servicio de soporte técnico.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>536</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: el componente de inicio de sesión de red no está activado</p></td>
<td style="border:1px solid black;"><p>Compruebe que el servicio de inicio de sesión de red funciona. De lo contrario, el evento debería dar lugar a una investigación.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>540</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión realizado</p></td>
<td style="border:1px solid black;"><p>Este evento es el equivalente al evento 528, pero en la red.</p></td>
</tr>
</tbody>
</table>
  
**Troyanos, rootkits y malware**  
El Id. de evento 592 es especialmente útil para detectar casos de troyanos, rootkits y otro software malintencionado, porque se crea siempre que se inicia un nuevo proceso. Este evento debería dar lugar a una investigación inmediata siempre que el nombre de archivo de imagen no se corresponda con un proceso que esté incluido en una lista de programas autorizados.
  
Aunque los troyanos y los registradores de claves son relativamente fáciles de identificar, los rootkits son especialmente sigilosos. Para detectarlos, hay que localizar programas desconocidos que se inician y detienen en rápida sucesión. Sin embargo, cuando se inicia un rootkit, el sistema operativo no tiene ninguna forma de detectarlo y, por tanto, no genera ningún evento.
  
Otro malware puede adoptar la forma de archivos adjuntos de correo electrónico o sitios web infectados, y podrían intentar elevar los privilegios si la cuenta de ejecución no tiene derechos para iniciar nuevos programas. En tales casos, el software no autorizado debería crear un evento de error que se debería investigar, sobre todo si se producen los eventos siguientes:
  
-   **Procesos que se generan como LocalSystem**. Los procesos que se ejecutan como LocalSystem se deberían definir bien en una lista de programas autorizados, que podría incluir procesos como Services.exe.
  
-   **Procesos que se generan en momentos inesperados**. Si el sistema supervisado no utiliza ningún proceso por lotes programado, se deberían investigar ciertas actividades (por ejemplo, copias de seguridad, CGI o scripts) después de que se produzcan. En otros casos, se debería realizar una investigación cuando dichos eventos se produzcan fuera de los períodos de tiempo por lotes programados regularmente.
  
**Tabla 4. Evento 592**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>592</p></td>
<td style="border:1px solid black;"><p>Creación de un proceso nuevo</p></td>
<td style="border:1px solid black;"><p>Compruebe las entradas del nombre de archivo de imagen y el nombre de usuario para buscar procesos no autorizados, momentos de inicio inesperados o saber si hay programas que se inician y se detienen en rápida sucesión.</p></td>
</tr>
</tbody>
</table>
  
**Acceso a recursos mediante el cambio de los permisos de archivo**  
Es posible utilizar privilegios administrativos para tener acceso a archivos cuyo acceso normalmente se denegaría si se cambia la propiedad de los datos y luego se agregan las cuentas a la lista de permisos de lectura de esos datos. También es posible camuflar esas actividades en Windows Server 2003 cambiando la propiedad y los permisos a su configuración original.
  
A este respecto, es importante identificar los activos y los datos de gran valor, ya que sería contraproducente implementar una auditoría de acceso a objetos para cada archivo de una red empresarial de tamaño medio, debido al gran volumen de eventos de acceso que se producen todos los días. Se debería habilitar la auditoría de acceso a objetos para archivos y carpetas confidenciales; las entradas de ACL no son una defensa adecuada contra los intentos de acceso no autorizados.
  
Para detectar eficientemente las actividades ilegales, debería ser fácil identificar los siguientes factores para todos los archivos de gran valor:
  
-   ¿Qué objeto ha sido el objetivo de un intento de acceso?
  
-   ¿Qué cuenta se ha utilizado para solicitar el acceso?
  
-   ¿Qué cuenta autorizó el acceso?
  
-   ¿Qué tipo de acceso se ha intentado?
  
-   ¿El evento se realizó correctamente o produjo un error?
  
-   ¿Qué sistema se utilizó para iniciar el intento?
  
El Visor de sucesos integrado no tiene suficientes opciones de filtrado para identificar esta información. Por tanto, se debe utilizar EventCombMT o algún otro mecanismo para realizar este análisis.
  
Los eventos de auditoría de acceso a objetos de la tabla siguiente se encargan de los intentos de esta naturaleza.
  
**Tabla 5. Eventos de cambio de permisos de archivos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>560</p></td>
<td style="border:1px solid black;"><p>Acceso concedido a objeto existente</p></td>
<td style="border:1px solid black;"><p>Indica que se ha concedido la solicitud de acceso a un objeto. Compruebe el Id. de inicio de sesión principal, el nombre de usuario de cliente y el nombre de usuario principal para detectar un acceso no autorizado. Compruebe el campo de accesos para determinar el tipo de operación. Este evento sólo detecta solicitudes de acceso, no si se ha producido un acceso propiamente dicho.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>567</p></td>
<td style="border:1px solid black;"><p>Se ha utilizado un permiso asociado a un identificador</p></td>
<td style="border:1px solid black;"><p>Indica la primera instancia de un tipo de acceso a un objeto y que los permisos se han cambiado si el campo Acceso incluye “WRITE_DAC.” Compare los campos de identificador para establecer una correlación con el evento 560.</p></td>
</tr>
</tbody>
</table>
  
**Acceso a recursos mediante el restablecimiento de la contraseña**  
Los cambios de contraseñas sólo se deberían producir en un marco de procedimientos establecidos. Si los niveles de auditoría están configurados correctamente, se deberían registrar los eventos de administración de cuentas que se muestran en la tabla siguiente y establecer una correlación entre esos eventos y los procesos registrados para identificar actividades que no cumplan ese procedimiento.
  
**Tabla 6. Eventos de restablecimiento de contraseñas**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>627</p></td>
<td style="border:1px solid black;"><p>Intento de cambio de contraseña</p></td>
<td style="border:1px solid black;"><p>Indica una solicitud de cambio de contraseña en la cual el solicitante ha suministrado la contraseña original. Compare el nombre de cuenta principal con el nombre de cuenta de destino para determinar si la cuenta solicitante es la cuenta cambiada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>628</p></td>
<td style="border:1px solid black;"><p>Contraseña de cuenta de usuario establecida o restablecida</p></td>
<td style="border:1px solid black;"><p>Indica que se ha restablecido una contraseña desde una interfaz administrativa, en lugar de utilizar un proceso de cambio de contraseña. El solicitante debería ser una cuenta autorizada como, por ejemplo, una cuenta del departamento de soporte o una cuenta de restablecimiento de contraseñas del servicio automático.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>698</p></td>
<td style="border:1px solid black;"><p>Cambio de la contraseña del modo de restauración de servicios de directorio</p></td>
<td style="border:1px solid black;"><p>Indica un intento de cambiar la contraseña del modo de restauración de servicios de directorio en un controlador de dominio. Compruebe la IP de la estación de trabajo y el nombre de la cuenta. Este evento garantiza una investigación inmediata.</p></td>
</tr>
</tbody>
</table>
  
**Modificación de cuentas de usuario**  
Cualquier modificación de una cuenta, ya sea para agregarla, eliminarla o cambiarla, debería corresponderse con un proceso establecido que implique un proceso de lógica de negocio de varios pasos iniciado por una solicitud oficial de un empleado del nivel administrativo. Todos los eventos de la tabla siguiente deberían corresponderse con una solicitud oficial de modificación de cuenta o se debería iniciar una investigación inmediata.
  
**Tabla 7. Eventos de cambio de cuentas de usuario**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>624</p></td>
<td style="border:1px solid black;"><p>Creación de una cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Indica que se ha creado una cuenta de red.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>630</p></td>
<td style="border:1px solid black;"><p>Eliminación de una cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Indica que se ha eliminado de una cuenta de red.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>642</p></td>
<td style="border:1px solid black;"><p>Cambio de una cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Indica cambios de cuentas de usuario relacionados con la seguridad que no cubren los eventos 627 a 630.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>685</p></td>
<td style="border:1px solid black;"><p>Cambio del nombre de una cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Indica un cambio de nombre de cuenta de usuario.</p></td>
</tr>
</tbody>
</table>
  
Para identificar de forma efectiva problemas de administración de cuentas, se deberían configurar consultas para lograr lo siguiente:
  
-   Encontrar actividades de cuentas irregulares o inusuales.
  
-   Identificar cuentas de nivel de administrador que abusen de privilegios para crear o modificar cuentas.
  
-   Detectar patrones de actividades de cuentas que se produzcan al margen de la directiva de seguridad de la organización.
  
También es importante confirmar el intervalo entre la creación de la cuenta y el cambio inicial de contraseña e información de inicio de sesión. Si la nueva cuenta no se utiliza en un período de tiempo predeterminado (normalmente, en el proceso de creación de la cuenta se registra la fecha de inicio prevista de un usuario nuevo), la cuenta se deshabilita y se inicia una investigación para determinar la razón del retraso.
  
**Cambios de pertenencia a grupos**  
Es recomendable utilizar el principio del menor privilegio, lo que significa que a las cuentas se les otorga el nivel mínimo de acceso necesario para realizar sus funciones adecuadamente. Si se aplica este principio, la mayoría de las cuentas pertenecerán al grupo de usuarios de dominio predeterminado y algunas a grupos de seguridad específicos de la empresa.
  
Sólo se deberían producir cambios de pertenencia a grupos de acuerdo con las directrices de las directivas establecidas, sobre todo cuando tienen que ver con cuentas con privilegios elevados. Esos cambios de pertenencia a grupos sólo deberían realizarlos cuentas establecidas que se utilizan para la administración de cuentas, y dichos eventos se deberían correlacionar con un proceso establecido para dichos cambios. Cualquier cambio que se realice al margen de este proceso debería dar lugar a una investigación inmediata.
  
Los eventos de auditoría de administración de cuentas de la tabla siguiente detallan los cambios de pertenencia a grupos.
  
**Tabla 8. Eventos de cambios de pertenencia a grupos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>631, 632,<br />
633, 634</p></td>
<td style="border:1px solid black;"><p>Cambio del grupo global con seguridad habilitada</p></td>
<td style="border:1px solid black;"><p>Examine el campo del nombre de cuenta de destino para determinar si el grupo cambiado era global o tenía amplios privilegios de acceso.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>635, 636,<br />
637, 638</p></td>
<td style="border:1px solid black;"><p>Cambio del grupo local con seguridad habilitada</p></td>
<td style="border:1px solid black;"><p>Examine el campo del nombre de cuenta de destino para determinar si el grupo cambiado era de administradores, operadores de servidores u operadores de copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>639, 641,<br />
668</p></td>
<td style="border:1px solid black;"><p>Cambio de grupo con seguridad habilitada</p></td>
<td style="border:1px solid black;"><p>Indica un cambio en un grupo que no es una eliminación, una creación ni un cambio de pertenencia. Examine el nombre de cuenta de destino para asegurarse de que no se ha modificado un grupo con grandes privilegios.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>659, 660, 661, 662</p></td>
<td style="border:1px solid black;"><p>Cambio de grupo universal con seguridad habilitada</p></td>
<td style="border:1px solid black;"><p>Examine el campo del nombre de cuenta de destino para asegurarse de que no se ha modificado un grupo con grandes privilegios como, por ejemplo, el de administradores de la organización.</p></td>
</tr>
</tbody>
</table>
  
**Nota**   La pertenencia a un grupo de distribución no da derecho de acceso a recursos de la red, porque los grupos de distribución no son principios de seguridad. Sin embargo, la pertenencia a ciertos grupos de distribución puede crear problemas de seguridad, dependiendo del grupo. Por ejemplo, si se colocan cuentas de usuario en un grupo de distribución ejecutivo o de administración, un usuario podría recibir mensajes de correo electrónico no adecuados para su puesto.
  
**Intentos de uso de cuentas no autorizadas**  
La promoción del primer controlador de dominio de Active Directory de un bosque crea una cuenta de administrador que es miembro de los grupos Administradores de dominio y Administradores de organización. Esta cuenta requiere una protección especial, porque es la única a la que no le afecta la configuración de bloqueo de cuentas. Por tanto, aunque haya una directiva de bloqueo de cuentas, esta cuenta es especialmente vulnerable a ataques por diccionario.
  
Con una supervisión de la seguridad efectiva, se deberían poder identificar todos los intentos de inicio de sesión con esta cuenta de administrador, aunque se le haya cambiado el nombre. Para obtener más información acerca de cómo aumentar la seguridad en las cuentas administrativas, consulte la [*Guía de planeamiento de la seguridad de las cuentas de administrador*](http://go.microsoft.com/fwlink/?linkid=41315) en http://go.microsoft.com/fwlink/?LinkId=41315 (puede estar en inglés).
  
Asimismo, los intentos de iniciar sesión con cuentas deshabilitadas o expiradas puede indicar que un empleado antiguo, un empleado temporal o un contratista ha intentado obtener acceso a la red sin las credenciales actuales. Esos eventos deberían dar lugar a investigaciones inmediatas.
  
En la tabla siguiente se incluyen los eventos que identifican el uso de cuentas no autorizadas que pertenecen a las categorías de auditoría de inicio de sesión y de inicio de sesión de cuenta.
  
**Tabla 9. Eventos de inicio de sesión no autorizados**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>528</p>
<p>540</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión realizado</p></td>
<td style="border:1px solid black;"><p>El evento 528 es un evento común. Sin embargo, el evento 540 debería dar lugar a un examen del nombre de cuenta de destino para determinar si ha sido provocado por la cuenta de administrador predeterminada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>529</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: nombre de usuario o contraseña desconocidos</p></td>
<td style="border:1px solid black;"><p>Investigue siempre si el nombre de cuenta de destino pertenece al administrador o es la cuenta de administrador predeterminada con otro nombre. Investigue también si los errores de inicio de sesión están por debajo del umbral de bloqueo. Asimismo, compruebe si hay algún intento en el que el nombre de cuenta de destino sea el administrador o raíz, y si el nombre de dominio es desconocido.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>531</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: cuenta deshabilitada</p></td>
<td style="border:1px solid black;"><p>Examine el nombre de cuenta de destino y el nombre de estación de trabajo para determinar el origen. Este evento debería dar lugar a una investigación, ya que es posible que se haya producido un intento de intrusión por parte de antiguos usuarios de cuentas.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>532</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: cuenta caducada</p></td>
<td style="border:1px solid black;"><p>Examine el nombre de cuenta de destino y el nombre de estación de trabajo para determinar el origen. Este evento debería dar lugar a una investigación, ya que es posible que se haya producido un intento de intrusión por parte de antiguos usuarios de cuentas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>576</p></td>
<td style="border:1px solid black;"><p>Privilegios especiales asignados al nuevo inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Indica una asignación de privilegios que puede otorgar un nuevo privilegio administrativo de cuenta o la capacidad de modificar la pista de auditoría. Compare el campo de Id. de inicio de sesión con los eventos 528 o 540 para determinar fácilmente si una cuenta ha obtenido el nivel de administrador.</p></td>
</tr>
</tbody>
</table>
  
Otro de los problemas de seguridad que tiene que ver con el uso no autorizado de credenciales de cuentas se deriva del uso de directivas de contraseñas efectivas como, por ejemplo, directivas de contraseñas muy estrictas y tiempos de expiración de contraseñas más cortos. En ocasiones, los usuarios tienen que anotar o registrar de alguna forma sus contraseñas para poder recordarlas. Este problema es especialmente evidente en entornos que tienen varios almacenes de identidades sin servicios de administración de identidades, lo que exige el uso de muchas contraseñas y cuentas.
  
**Nota**   Para obtener información acerca de la administración de contraseñas en entornos heterogéneos, consulte la [Serie de administración de acceso e identidades de Microsoft](http://go.microsoft.com/fwlink/?linkid=14841) en http://go.Microsoft.com/fwlink/?LinkId=14841 (puede estar en inglés).
  
Las organizaciones deben evitar que los usuarios guarden sus contraseñas, sobre todo a plena vista, porque individuos no autorizados podrían encontrarlas y utilizarlas para realizar un ataque. Es posible supervisar este tipo de intrusiones con la información de la tabla anterior, pero hay que establecer una correlación cruzada entre esta información y un historial de inicios de sesión correctos de la cuenta de usuario en cuestión para poder crear una lista de estaciones de trabajo comunes a los que obtiene acceso esa cuenta con el fin de compararlas.
  
**Nota**   Es posible restringir las cuentas de usuario a estaciones de trabajo específicas con la funcionalidad de Active Directory integrada. Sin embargo, para utilizar esta funcionalidad, la red debe admitir los nombres de sistemas de entrada/salida básicos de red (NetBIOS), que suministra el Servicio de nombres Internet de Windows (WINS), por ejemplo.
  
**Inicio de sesión interactivo con credenciales de cuenta de servicio**  
Al iniciarse, los servicios deben presentar credenciales de inicio de sesión. En ocasiones, algunos servicios podrían requerir el uso de una cuenta de dominio para ejecutar servicios o conectarse a equipos remotos. Puede que algunos servicios necesiten incluso credenciales de administrador, o que deban interactuar también con el escritorio.
  
En Windows Server 2003 y versiones posteriores, algunas cuentas de servicio (por ejemplo, el servicio de alerta) se pueden iniciar con el modificador **–LocalService**. Además, los servicios que necesitan conectividad de red pueden utilizar la cuenta de servicio de red NT AUTHORITY\\Network Service. Se deberían comprobar todos los servicios que necesitan cuentas de usuario para asegurarse de que las cuentas utilizadas están protegidas con contraseñas estrictas. La supervisión de la seguridad debería confirmar que los eventos de inicio de sesión de esas cuentas sólo se producen cuando se inician servicios asociados. Para obtener más información acerca de cómo aumentar la seguridad de las cuentas de servicio, consulte la [*Guía de planeamiento de la seguridad de cuentas de servicio y servicios*](http://go.microsoft.com/fwlink/?linkid=41311) en http://go.Microsoft.com/fwlink/?LinkId=41311 (puede estar en inglés).
  
El principal problema de seguridad de las cuentas de servicio se produce cuando dichas cuentas inician sesión de manera interactiva en lugar de como un servicio. Esos eventos sólo se producen cuando un intruso ha comprometido una cuenta de servicio e inicia sesión con ella. Si la cuenta de servicio comprometida tiene privilegios de administrador, el intruso obtiene acceso a importantes capacidades y puede interrumpir los servicios de red normales.
  
Se deberían identificar todos los recursos a los que tienen acceso las cuentas de servicio y no debería haber permisos no explicados que impliquen el acceso a datos de gran valor. Por ejemplo, puede que una cuenta de servicio necesite acceso de escritura ocasional a un directorio de archivos de registro, pero no es lo normal. Las cuentas de servicio que pueden interactuar con el escritorio también merecen especial atención, porque dichas cuentas ofrecen mayores oportunidades a los atacantes.
  
En la tabla siguiente, se incluyen los eventos de auditoría de inicio de sesión e inicio de sesión de cuentas que identifican el uso no autorizado de credenciales de cuentas de servicio.
  
**Tabla 10. Eventos de inicio de sesión con credenciales de cuentas de servicio**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>528</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión realizado: ataque a consola o Terminal Services</p></td>
<td style="border:1px solid black;"><p>Indica que se está produciendo un ataque si el tipo de inicio de sesión 10, una cuenta de servicio o la cuenta local del sistema están asociados a este evento. Este evento debería dar lugar a una investigación inmediata.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>534</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: tipo de inicio de sesión no permitido</p></td>
<td style="border:1px solid black;"><p>Indica un error en el intento de iniciar sesión de manera interactiva con credenciales de cuentas de servicio cuando lo prohíbe la configuración de directiva de grupo. Compruebe el nombre de cuenta de destino, el nombre de estación de trabajo y el tipo de inicio de sesión cuando se produzca este evento.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>600</p></td>
<td style="border:1px solid black;"><p>Se asignó un símbolo (token) principal a un proceso</p></td>
<td style="border:1px solid black;"><p>Indica que un servicio está utilizando una cuenta con nombre para iniciar sesión en un sistema que ejecuta Windows XP o posterior. Establezca una correlación con la información de los eventos 672, 673, 528 y 592 para investigarlo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>601</p></td>
<td style="border:1px solid black;"><p>Intento de un usuario de instalar un servicio</p></td>
<td style="border:1px solid black;"><p>Este evento no se debería producir con frecuencia en un entorno empresarial que tenga una directiva de aplicaciones y un proceso de estandarización del sistema aceptables y bien definidos. Este evento debería dar lugar a una investigación si los procesos de control de cambios no se correlacionan en dichos entornos.</p></td>
</tr>
</tbody>
</table>
  
**Ejecución de programas no autorizados**  
Las cuentas de nivel de administrador pueden instalar y ejecutar programas y, por tanto, sólo se delegan a personal de confianza que necesita tener esas capacidades. Dados los riesgos asociados al software no probado, es importante diseñar una lista de software autorizado y con licencia, además de un proceso para solicitar, probar y autorizar nuevas aplicaciones. Las aplicaciones no autorizadas se deberían limitar a un entorno de prueba aislado, y no se deberían instalar en un entorno de red de producción al margen del proceso de control de cambios establecido. Incluso en ese caso, sólo se deberían permitir después de agregarlas a una lista de software autorizado.
  
La siguiente tabla incluye los eventos de seguimiento de procesos que pueden identificar el uso de programas no autorizados.
  
**Tabla 11. Eventos de ejecución de programas no autorizados**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>592</p></td>
<td style="border:1px solid black;"><p>Creación de un proceso nuevo</p></td>
<td style="border:1px solid black;"><p>Indica que se ha creado un proceso nuevo. Examine los campos del nombre de archivo de imagen y de nombre de usuario, y compárelos con la lista de programas autorizados si hay una directiva de programas permisible establecida en la empresa. Busque también instancias en las que se haya utilizado LocalSystem para abrir un símbolo del sistema, ya que éste es un método común de evadir una pista de auditoría.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>602</p></td>
<td style="border:1px solid black;"><p>Creación de un trabajo programado</p></td>
<td style="border:1px solid black;"><p>Examine el campo del nombre de destino y el tiempo de la tarea si esos eventos se producen en momentos inesperados.</p></td>
</tr>
</tbody>
</table>
  
**Nota**   Las auditorías de seguridad de seguimiento de procesos son capaces de identificar programas no autorizados. Sin embargo, el seguimiento de procesos genera muchas entradas en el registro de seguridad, así que hay que procurar que el número de eventos no sature los mecanismos de detección de seguridad.
  
**Acceso a recursos no autorizados**  
La tabla siguiente de eventos de auditoría de acceso a objetos indica intentos de acceso a recursos a los que un usuario no está autorizado.
  
**Tabla 12. Eventos de intentos de acceso a recursos no autorizados**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>560</p></td>
<td style="border:1px solid black;"><p>Acceso denegado a objeto existente</p></td>
<td style="border:1px solid black;"><p>Examine el campo del nombre de objeto para determinar el recurso al que se ha tenido acceso y establezca una correlación entre los campos del nombre de usuario principal y de dominio principal o los campos de nombre de usuario de cliente y dominio de cliente para determinar el origen.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>568</p></td>
<td style="border:1px solid black;"><p>Intento de crear un vínculo físico a un archivo auditado</p></td>
<td style="border:1px solid black;"><p>Indica que un usuario o programa ha intentado crear un vínculo físico a un archivo u objeto. Un vínculo físico establecido permite que una cuenta manipule un archivo sin crear una pista de auditoría si esa cuenta tiene derechos sobre el objeto.</p></td>
</tr>
</tbody>
</table>
  
**Uso de sistemas operativos no autorizados**  
El uso de sistemas operativos no autorizados puede producir problemas importantes, ya sea una reducción de la protección frente al aprovechamiento malintencionado de vulnerabilidades o un aumento de la probabilidad de que se dañen los datos en los sistemas de archivos. Los administradores y los usuarios pueden introducir sistemas operativos no autorizados en la red mediante los mecanismos siguientes:
  
-   Equipos personales conectados a la red de manera local o remota.
  
-   Uso de sistemas operativos que se arrancan desde un CD.
  
-   Reinstalación de un sistema operativo Windows.
  
-   Uso de imágenes de PC virtuales.
  
Las directivas de la organización pueden especificar cómo se deben conectar a la red los usuarios desde ubicaciones remotas por medio de una red privada virtual o un servicio de acceso remoto, e incluir requisitos para conectar sistemas como, por ejemplo, el tipo de sistema operativo, el nivel de actualización y la instalación de medidas de protección, como firewall personales y software antivirus. Para obtener más información acerca de cómo asegurarse de que los sistemas remotos cumplen las directivas de seguridad de la empresa, consulte [*Implementación de servicios de cuarentena con la Guía de planeamiento de la red privada virtual de Microsoft*](http://go.microsoft.com/fwlink/?linkid=41307) en http://go.microsoft.com/fwlink/?LinkId=41307 (puede estar en inglés).
  
Los usuarios también pueden utilizar los CD de instalación de Windows XP y reiniciar sus equipos para instalar un sistema operativo no administrado. En tales casos, puede que sea posible detectar este tipo de actividad localizando los intentos de inicio de sesión con una cuenta de usuario de administrador desde un nombre de grupo de trabajo no identificado o desde el nombre de grupo de trabajo predeterminado.
  
**Nota**   Existen algunas distribuciones de código abierto en formato de CD de arranque que permiten utilizar sistemas operativos sin necesidad de instalarlos en un sistema local. Puesto que el sistema operativo no está instalado en el equipo local, es difícil localizar esa actividad. Sin embargo, los intentos de inicio de sesión de las cuentas de usuario denominadas "raíz" en un entorno de red homogéneo o desde nombres de equipos inesperados pueden indicar la presencia de un sistema operativo no autorizado. Para evitar este tipo de actividad, deshabilite la función de arranque desde CD en la configuración de BIOS del equipo y, a continuación, proteja mediante contraseña la configuración de la BIOS, aunque este método podría no resultar práctico en algunos entornos.
  
Las imágenes de PC virtuales ofrecen la emulación completa de un entorno de equipos en un equipo host. Esta emulación se ejecuta en su propio sistema operativo con su propio nombre de equipo, cuentas de usuario, estructura de servicios de directorio y programas en un entorno virtual. Una instancia de PC virtual también es capaz de iniciarse, ejecutarse y detenerse de manera independiente a un sistema host y, por tanto, en ese equipo host es probable que no se creen eventos de auditoría. Esta capacidad, combinada con la posibilidad de que un equipo virtual se conecte a la red del host, obtenga direcciones IP e incluso se asigne a unidades compartidas, representa una serie de riesgos para la seguridad que abarcan desde la reducción de la protección mediante contraseñas hasta un aumento de las vulnerabilidades, porque es probable que no se rija por ningún proceso de actualización establecido en la red. Dados los riesgos que representan los equipos virtuales, es importante restringir el uso de software de PC virtual al personal autorizado y establecer procesos documentados relativos a la creación y uso de instancias de PC virtuales.
  
Para detectar el uso de sistemas operativos no autorizados, la solución de supervisión de la seguridad debe poder detectar lo siguiente:
  
-   Cuentas de usuario, nombres de equipo, grupos de trabajo o nombres de dominio no reconocidos.
  
-   Duplicar o poner fuera de rango direcciones IP.
  
-   Intentos de inicio de sesión con la cuenta de administrador predeterminada.
  
Los eventos de seguimiento de procesos que se incluyen en la tabla siguiente se pueden utilizar para detectar el uso de sistemas operativos no autorizados.
  
**Tabla 13. Eventos de uso de plataformas no autorizadas**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>529</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: nombre de usuario o contraseña desconocidos</p></td>
<td style="border:1px solid black;"><p>Compruebe los intentos en los que el campo del nombre de cuenta de destino sea igual al administrador o raíz, o en los que el nombre de dominio sea desconocido.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>533</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: el usuario no está autorizado a iniciar una sesión en este equipo</p></td>
<td style="border:1px solid black;"><p>Indica que es posible que un usuario esté intentando iniciar sesión en estaciones de trabajo restringidas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>592</p></td>
<td style="border:1px solid black;"><p>Creación de un proceso nuevo</p></td>
<td style="border:1px solid black;"><p>Compruebe los campos de nombre de archivo de imagen y nombre de usuario para asegurarse de que el programa está autorizado para ese uso por esa cuenta.</p></td>
</tr>
</tbody>
</table>
  
**Creación o ruptura de relaciones de confianza**  
Las relaciones de confianza permiten a las cuentas de un dominio tener acceso a recursos que residen en otro dominio. Es evidente que la creación de relaciones de confianza no es una operación rutinaria y sólo se debería realizar en el ámbito de un proceso de control de cambios establecido. La ruptura de relaciones de confianza también es una actividad que sólo se debería realizar después de ser autorizada en un proceso de control de cambios y después de pensar bien en los efectos que puede tener esta acción en la red.
  
Los eventos de auditoría de cambios de directiva de la tabla siguiente identifican las actividades de relaciones de confianza.
  
**Tabla 14. Eventos de cambio de relaciones de confianza**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>610<br />
611<br />
620</p></td>
<td style="border:1px solid black;"><p>Se han creado, eliminado o modificado relaciones de confianza con otro dominio</p></td>
<td style="border:1px solid black;"><p>Estos eventos se generan en el controlador de dominio que ha establecido la relación de confianza. Este evento debería dar lugar a una investigación inmediata si no se correlaciona con un proceso de solicitud de control de cambios establecido. Examine el campo de nombre de usuario para determinar la cuenta solicitante.</p></td>
</tr>
</tbody>
</table>
  
**Cambios de directivas de seguridad no autorizados**  
Los cambios en la configuración de las directivas de seguridad aprobadas sólo se deberían realizar en el marco de un proceso de control de cambios establecido. Cualquier cambio que se produzca al margen de este proceso debería dar lugar a una investigación inmediata.
  
Este tipo de cambios de las directivas de seguridad incluye:
  
-   Configuración de la directiva de grupo
  
    -   Directiva de contraseñas de cuentas de usuario
  
    -   Directiva de bloqueo de cuentas de usuario
  
    -   Directiva de auditoría
  
    -   Configuración de registros de sucesos que se aplican al registro de sucesos de seguridad
  
    -   Directiva IPsec
  
    -   Directivas de red inalámbrica (IEEE 802.1x)
  
    -   Directivas del sistema de archivos de cifrado (EFS) y claves públicas
  
    -   Directivas de restricción de software
  
-   Configuración de seguridad
  
    -   Configuración de derechos de usuario
  
    -   Directiva de contraseñas de cuentas de usuario
  
    -   Opciones de seguridad
  
La lista anterior sólo incluye los requisitos mínimos, porque es probable que la mayoría de las empresas agreguen más configuraciones de la directiva de grupo a su entorno. Las auditorías de seguridad tienen que identificar los intentos correctos e incorrectos de cambio de estas configuraciones, porque los intentos correctos deberían corresponderse con las cuentas que tienen autoridad para realizar estos cambios en un proceso establecido para ese fin.
  
En la tabla siguiente, se incluyen los eventos de auditoría de cambio de directivas que identifican cambios de directivas del sistema local y de la directiva de grupo.
  
**Tabla 15. Eventos de cambio de directivas**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>612</p></td>
<td style="border:1px solid black;"><p>Cambio de directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Indica un cambio en una directiva de auditoría. Estos eventos se deberían correlacionar con una directiva de control de cambios establecida para determinar si estaban autorizados.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>613<br />
614<br />
615</p></td>
<td style="border:1px solid black;"><p>Cambio de directiva IPsec</p></td>
<td style="border:1px solid black;"><p>Indica un cambio en la directiva IPsec. Se debería investigar si el cambio se realiza fuera del inicio de un sistema.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>618</p></td>
<td style="border:1px solid black;"><p>Directiva de recuperación de datos cifrados</p></td>
<td style="border:1px solid black;"><p>Estos eventos se producen cuando se está utilizando una directiva de recuperación de datos cifrados. Si se produce alguno al margen de las directivas especificadas, se debería realizar una investigación.</p></td>
</tr>
</tbody>
</table>
  
**Nota**   Para obtener más información acerca de la configuración de directivas de grupo, consulte la sección "[Configuración de directivas de seguridad](http://technet2.microsoft.com/windowsserver/en/library/bcd7ea4c-f989-4cee-969a-920f62f555111033.mspx?mfr=true)" en http://technet2.microsoft.com/WindowsServer/en/library/bcd7ea4c-f989-4cee-969a-920f62f555111033.mspx?mfr=true (puede estar en inglés).
  
**Intento de comprometer las credenciales**  
Los atacantes pueden utilizar muchos métodos, ya sean ataques por diccionario o ataques de ingeniería social, para obtener las credenciales de las cuentas de usuario. Aunque el método más conocido es el ataque por diccionario contra una sola cuenta, otro método común consiste en utilizar un conjunto de contraseñas en todas las cuentas de una base de datos de servicios de directorio. En el segundo caso, es probable que el atacante tenga acceso a la base de datos de directorios de la organización, o haya averiguado la nomenclatura de nombres de usuario y disponga de una lista de empleados. Para detectar este tipo de ataque, es necesario tener la capacidad de detectar múltiples errores de inicio de sesión en múltiples cuentas, aunque no se activen los umbrales de bloqueo de cuentas.
  
El restablecimiento de contraseñas es otro método para obtener el control de la información de credenciales de una cuenta. Las operaciones de restablecimiento o cambio de contraseñas generan el mismo evento, hayan sido correctas o incorrectas, por lo que un atacante puede evitar ser detectado si burla la directiva de bloqueo de cuentas. Para frustrar estos intentos, la solución de supervisión de la seguridad debe poder identificar múltiples intentos de cambio o restablecimiento de las contraseñas, sobre todo los que se producen al margen de las directivas establecidas y los marcos de procesos empresariales.
  
Aunque los ciclos de contraseñas no son un ataque (se producen cuando los usuarios intentan burlar las directivas de reutilización de contraseñas mediante el uso de scripts que realizan ciclos con numerosas contraseñas con el fin de volver a utilizar la original), suponen una amenaza para la seguridad. Durante esas operaciones, el número de contraseñas restablecidas es prácticamente igual al umbral de reutilización de contraseñas y, por tanto, aparecerá como una serie rápida de eventos 627. La implementación de directivas sobre la duración mínima de las contraseñas ayuda a frustrar esos intentos.
  
En la tabla siguiente, se incluyen los eventos que se pueden producir a causa de intentos de ataque a las credenciales de autenticación, pero esos eventos también pueden ocurrir como consecuencia de las operaciones normales de la red como, por ejemplo, cuando los usuarios legítimos olvidan sus contraseñas.
  
**Tabla 16. Eventos de ataque a las credenciales de autenticación**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>529</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: nombre de usuario o contraseña desconocidos</p></td>
<td style="border:1px solid black;"><p>Compruebe los intentos en los que el nombre de cuenta de destino sea igual a la cuenta de nivel de administrador o de algún otro nivel administrativo que no tenga autorización para cambiar las contraseñas. Compruebe si se han producido muchos errores de inicio de sesión que estén por debajo del umbral de bloqueo. Establezca una correlación entre el evento 529 y el evento 539 para identificar patrones de bloqueos de cuentas continuos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>534</p></td>
<td style="border:1px solid black;"><p>Error de inicio de sesión: tipo de inicio de sesión no permitido</p></td>
<td style="border:1px solid black;"><p>Indica que un usuario ha intentado iniciar sesión con un tipo de cuenta que no está permitido (por ejemplo, de red, interactivo, por lotes o de servicio). Compruebe los campos de nombre de cuenta de destino, nombre de la estación de trabajo y tipo de inicio de sesión.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>539</p></td>
<td style="border:1px solid black;"><p>Cuenta bloqueada</p></td>
<td style="border:1px solid black;"><p>Indica un intento de iniciar sesión con una cuenta que se ha bloqueado. Establezca una correlación con el evento 529 para detectar patrones de bloqueos continuados.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>553</p></td>
<td style="border:1px solid black;"><p>Ataque de reproducción detectado</p></td>
<td style="border:1px solid black;"><p>Indica que un paquete de autenticación, normalmente Kerberos, ha detectado un intento de inicio de sesión mediante la reproducción de las credenciales de un usuario. Aunque este evento podría ser una señal de que la configuración de la red es incorrecta, debería dar lugar a una investigación inmediata.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>627</p></td>
<td style="border:1px solid black;"><p>Intento de cambio de contraseña</p></td>
<td style="border:1px solid black;"><p>Indica que alguien que no es el propietario de la cuenta ha intentado cambiar una contraseña cuando el campo de nombre de cuenta principal no coincide con el campo de nombre de cuenta de destino.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>628</p></td>
<td style="border:1px solid black;"><p>Contraseña de cuenta de usuario establecida o restablecida</p></td>
<td style="border:1px solid black;"><p>Esta actividad se debería restringir a cuentas autorizadas como, por ejemplo, una cuenta del departamento de soporte o una cuenta de restablecimiento de contraseñas de autoservicio.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>644</p></td>
<td style="border:1px solid black;"><p>Cuenta de usuario bloqueada automáticamente</p></td>
<td style="border:1px solid black;"><p>Indica un bloqueo de cuenta debido a que el número de errores secuenciales en los intentos de inicio de sesión es mayor que el límite de bloqueo de la cuenta. Establezca una correlación con los eventos 529, 675, 681 y 676 (sólo Windows 2000 Server). Consulte también la entrada del evento 12294 en esta tabla.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>675</p></td>
<td style="border:1px solid black;"><p>Error de preautenticación</p></td>
<td style="border:1px solid black;"><p>Indica un posible problema de sincronización temporal o que hay cuentas de equipos que no se han unido correctamente al dominio. Establezca una correlación con el evento 529 para determinar la razón exacta del error de inicio de sesión.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>12294</p></td>
<td style="border:1px solid black;"><p>Intento de bloqueo de cuenta</p></td>
<td style="border:1px solid black;"><p>Indica un posible ataque de fuerza bruta contra la cuenta de administrador predeterminada. Dado que en esta cuenta no se aplican las directivas de bloqueo de cuentas, se registra como un evento 12294 de SAM en el registro de sucesos del sistema. Si se produce este evento, se debería realizar una investigación, porque puede indicar el uso de un sistema operativo no autorizado. Compruebe si en el campo de nombre de dominio hay dominios desconocidos.</p></td>
</tr>
</tbody>
</table>
  
**Vulnerabilidades**  
En los intentos de intrusión, las vulnerabilidades son el primer objetivo de los atacantes, porque pueden estar en cualquier equipo, y requieren tiempo y esfuerzo para solucionarlas. El período de tiempo comprendido entre el momento que se descubren vulnerabilidades y el desarrollo de métodos para aprovecharlas, lo que normalmente se llama ventana de vulnerabilidad para aprovechar, cada vez es más corto, lo que significa que hay menos tiempo para desarrollar, probar y distribuir revisiones de seguridad para esas vulnerabilidades.
  
La mejor defensa contra el aprovechamiento de vulnerabilidades sigue siendo disponer de un proceso de administración de revisiones de seguridad efectivo que pruebe e implemente rápidamente actualizaciones de seguridad en el entorno. Algunos servicios que ayudan en este proceso son Microsoft Systems Management Server (SMS) 2003 o Windows Software Update Service (WSUS).
  
La supervisión de la seguridad en la red perimetral también es especialmente importante a este respecto, porque los equipos que residen allí están a disposición de los atacantes. Si no se implementan mecanismos para detectar ataques cuando se producen, puede que la organización no se dé cuenta de que algo va mal hasta que la red ya esté comprometida. Por tanto, es extremadamente importante supervisar atentamente los equipos que residen en la red perimetral para buscar una amplia variedad de eventos de auditoría.
  
Además de los eventos que ya se han mencionado, entre los eventos más importantes que se detallan en la sección “Intento de comprometer las credenciales", se incluyen los intentos de acceso no autorizado y el uso de identidades con privilegios. En la tabla siguiente, se incluyen algunos eventos que pueden identificar esos ataques.
  
**Tabla 17. Eventos causados por vulnerabilidades de elevación de privilegios**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>528</p>
<p>538</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión y cierre de sesión local</p></td>
<td style="border:1px solid black;"><p>Correlacione el campo de Id. de inicio de sesión cuando se produzcan esos eventos en los equipos perimetrales. Se debería realizar una investigación inmediata si los campos de nombre de cuenta de usuario, hora o nombre de estación de trabajo contienen valores inesperados.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>551</p></td>
<td style="border:1px solid black;"><p>El usuario inicia el cierre de sesión</p></td>
<td style="border:1px solid black;"><p>Este evento se puede considerar equivalente al evento 538, porque una pérdida de símbolos (tokens) puede producir un error en el evento de auditoría 538, pero en su lugar hace que se produzca el evento 551.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>576</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión con privilegios</p></td>
<td style="border:1px solid black;"><p>Indica un inicio de sesión de una cuenta de administrador, es decir, un inicio de sesión de una cuenta con privilegios suficientes para alterar la base informática de confianza (TCP, del inglés Trusted Computing Base), o con privilegios suficientes para hacerse con el control de un equipo que ejecuta Windows Server 2003 con SP1 o posterior. En versiones anteriores de Windows, este evento sólo era interesante si estaba asociado a privilegios confidenciales como, por ejemplo, SeSecurityPrivilege o SeDebugPrivilege.</p></td>
</tr>
</tbody>
</table>
  
**Nota**   En versiones de Windows anteriores a Windows Server 2003, el evento 576 se incluye en la categoría de uso privilegiado. En Windows Server 2003 y posteriores, este evento también se incluye en la categoría de inicio de sesión. Por tanto, la configuración de las opciones de auditoría de cualquiera de las categorías hace que se produzca este evento.
  
**Intentos de burlar la auditoría**  
Al igual que existen diversos métodos para atacar la red de una empresa, también existen técnicas para ocultar esos intentos y evitar ser descubiertos. Por ejemplo, un atacante puede cambiar la directiva de seguridad de un sistema o dominio comprometido para evitar que se registren actividades sospechosas en los registros de sucesos, o puede borrar deliberadamente un registro de seguridad para que se pierda la información auditada.
  
Es posible detectar intentos de eludir una solución de supervisión de la seguridad con esas técnicas, pero es difícil hacerlo debido a que los eventos que se producen durante un intento de cubrir las huellas de una intrusión son los eventos que se producen regularmente en una red empresarial típica.
  
En la tabla siguiente, se incluyen varios tipos de evento que ayudan a identificar los intentos de burla de las auditorías por parte de atacantes que intentan ocultar las pruebas de una infracción de seguridad.
  
**Tabla 18. Eventos de burla de auditorías de eventos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>512</p></td>
<td style="border:1px solid black;"><p>Inicio de Windows</p></td>
<td style="border:1px solid black;"><p>Normalmente se produce después del evento 513. Se deberían investigar los reinicios inesperados.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>513</p></td>
<td style="border:1px solid black;"><p>Cierre de Windows</p></td>
<td style="border:1px solid black;"><p>Normalmente se produce antes del evento 512. Los equipos de gran valor sólo debería reiniciarlos el personal autorizado e, incluso entonces, únicamente de acuerdo con un control de cambios establecido u otro procedimiento. Si este evento se produce en algún servidor, se debería realizar una investigación inmediata.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>516</p></td>
<td style="border:1px solid black;"><p>Error de auditoría</p></td>
<td style="border:1px solid black;"><p>Este evento se puede producir cuando hay demasiados eventos que están desbordando el búfer de registros de auditoría o cuando el registro de seguridad no está configurado para sobrescribirse. Aunque estos problemas se pueden evitar limitando los tipos de evento que se supervisan en la mayoría de los equipos, los equipos de gran valor o vulnerables necesitan una supervisión más detallada para protegerlos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>517</p></td>
<td style="border:1px solid black;"><p>Limpieza del registro de sucesos de seguridad</p></td>
<td style="border:1px solid black;"><p>Los registros de sucesos de seguridad no se deberían limpiar nunca sin autorización. Compruebe los campos de nombre de usuario del cliente y dominio del cliente para establecer una correlación cruzada con los registros de aprobación de procedimientos y personal autorizado.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>520</p></td>
<td style="border:1px solid black;"><p>Cambio de la hora del sistema</p></td>
<td style="border:1px solid black;"><p>Esta actividad puede servir para desorientar las investigaciones o dar a los atacantes una coartada falsa. Compruebe los campos de nombre de usuario del cliente y dominio del cliente para establecer una correlación cruzada con el personal autorizado, además de comprobar el nombre del proceso para asegurarse de que es %windir%\system32\svchost.exe.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>521</p></td>
<td style="border:1px solid black;"><p>No se pueden registrar eventos</p></td>
<td style="border:1px solid black;"><p>Se produce cuando Windows no puede escribir eventos en el registro de sucesos. Este evento se debería investigar siempre que se produzca en sistemas de gran valor.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>608</p></td>
<td style="border:1px solid black;"><p>Se ha asignado un privilegio de cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Se produce cuando se asigna un privilegio nuevo a una cuenta de usuario. El registro de sucesos registra esta acción junto con el identificador de seguridad (SID) de la cuenta de usuario, no junto al nombre de cuenta de usuario.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>609</p></td>
<td style="border:1px solid black;"><p>Se ha quitado un privilegio de cuenta de usuario</p></td>
<td style="border:1px solid black;"><p>Se produce cuando se quita un privilegio de una cuenta de usuario. El registro de sucesos registra esta acción junto con el SID de la cuenta de usuario, no junto al nombre de la cuenta de usuario.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>612</p></td>
<td style="border:1px solid black;"><p>Cambio de directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Aunque este evento no indica necesariamente que haya un problema, un atacante puede modificar las directivas de auditoría. Este evento se debería supervisar en controladores de dominio y equipos de gran valor.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>621</p></td>
<td style="border:1px solid black;"><p>Se ha concedido acceso al sistema a una cuenta</p></td>
<td style="border:1px solid black;"><p>Se produce cuando se concede acceso al sistema a un usuario. Hay que comprobar los campos de nombre de usuario y cuenta modificada si el permiso de acceso es interactivo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>622</p></td>
<td style="border:1px solid black;"><p>Se ha quitado el acceso al sistema de un sistema</p></td>
<td style="border:1px solid black;"><p>Este evento puede indicar que un atacante ha intentado quitar pruebas relacionadas con el evento 621 o está intentando denegar el servicio a alguna otra cuenta o cuentas.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>643</p></td>
<td style="border:1px solid black;"><p>Cambio de la directiva de seguridad de dominio</p></td>
<td style="border:1px solid black;"><p>Se produce cuando se realiza un intento de modificar la directiva de contraseñas u otras configuraciones de directivas de seguridad del dominio. Compruebe el nombre de usuario y establezca una correlación con cualquier registro de autorización.</p></td>
</tr>
</tbody>
</table>
  
##### Análisis de investigación
  
Aunque los análisis de investigación utilizan muchos de los elementos que se explican en este artículo, siguen siendo fundamentalmente diferentes a otras soluciones de supervisión y detección de ataques que hemos visto, porque se centran en el almacenamiento y el análisis de la información de seguridad y se utilizan en respuesta a un ataque después de haberse producido. La mayoría de las investigaciones comienzan siendo una lista de eventos asociados a un sistema o usuario específicos.
  
La supervisión de la seguridad para los análisis de investigación requiere:
  
-   Archivado de determinados tipos de evento.
  
-   Un cálculo del número de eventos previstos al día.
  
-   Definición de límites de tiempo para el almacenamiento en línea, sin conexión y en archivos.
  
-   Ampliación de bases de datos para hacer frente al número de eventos previstos.
  
-   Sistema de copia de seguridad capaz de gestionar la carga de eventos diaria prevista.
  
-   Establecimiento de directivas relativas a la administración del sistema de archivado.
  
Existen tres factores principales que determinan los requisitos de almacenamiento de un programa de análisis de investigación:
  
-   El número de eventos que se deben registrar.
  
-   La velocidad a la que los equipos de destino generan estos eventos.
  
-   Duración del almacenamiento en línea para determinar la disponibilidad.
  
El conocimiento de las necesidades de la empresa y de la información proporcionada en las secciones anteriores debería ayudarle a tomar decisiones acerca de estos tres factores con el fin de obtener un requisito de almacenamiento razonable.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Es evidente que, en los entornos de red de hoy en día, las soluciones de supervisión de la seguridad y detección de ataques efectivas y completas no son una opción, sino una necesidad para todas las medianas empresas. Las amenazas y los riesgos a los que se enfrentan las redes empresariales son numerosos y no sólo se originan en el exterior del perímetro, sino que también incluyen amenazas internas, ya sean intencionadas o accidentales. Los sistemas de supervisión de la seguridad bien pensados tienen en cuenta todos los riesgos y requieren un conocimiento profundo de los mismos, además de la arquitectura actual de una red empresarial y de los indicios de actividades y amenazas potenciales que podrían poner en peligro los datos que residen en los sistemas de la red.
  
Es evidente que Microsoft se toma la seguridad muy en serio y, por tanto, dispone de muchas herramientas que pueden servir para crear un sistema de supervisión de la seguridad y de detección de ataques efectivo. Windows Server 2003 y otras versiones del sistema operativo Windows ayudan a proporcionar la base de esta solución de supervisión de la seguridad gracias a su funcionalidad de registro de auditorías de seguridad integrada. Si se combina con otros componentes como, por ejemplo, Microsoft Operations Manager y EventCombMT, y los procesos y directivas empresariales necesarias, se puede desarrollar un sistema de supervisión completo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice A: Exclusión de eventos innecesarios
  
Los eventos de la tabla siguiente suelen excluirse de las consultas de supervisión de la seguridad por su frecuencia y porque no suelen dar resultados útiles cuando se incluyen en las soluciones de supervisión de la seguridad.
  
**Tabla A1. Eventos innecesarios**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de evento</p></th>
<th><p>Evento</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>538</p></td>
<td style="border:1px solid black;"><p>Cierre de sesión de usuario</p></td>
<td style="border:1px solid black;"><p>Este evento no indica necesariamente la hora a la que un usuario ha dejado de utilizar un sistema. Por ejemplo, si el equipo se cierra o pierde la conexión de red, puede que no registre ningún evento de cierre de sesión.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>562</p></td>
<td style="border:1px solid black;"><p>Se ha cerrado un identificador de objeto</p></td>
<td style="border:1px solid black;"><p>Siempre se registra como realizado correctamente.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>571</p></td>
<td style="border:1px solid black;"><p>Contexto de cliente eliminado por el Administrador de autorización</p></td>
<td style="border:1px solid black;"><p>Se espera que se produzca cuando se utiliza el Administrador de autorización.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>573</p></td>
<td style="border:1px solid black;"><p>Un proceso genera eventos de auditoría que no son del sistema con la interfaz de programación de aplicaciones de autorización (API AuthZ)</p></td>
<td style="border:1px solid black;"><p>Actividad esperada.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>577<br />
578</p></td>
<td style="border:1px solid black;"><p>Se ha llamado a un servicio de privilegios, operación de objeto con privilegios</p></td>
<td style="border:1px solid black;"><p>Se trata de eventos de gran volumen, que normalmente no contienen información suficiente para tomar medidas, ya que no describen qué operación se ha producido.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>594</p></td>
<td style="border:1px solid black;"><p>Se ha duplicado un identificador de objeto</p></td>
<td style="border:1px solid black;"><p>Actividad esperada.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>595</p></td>
<td style="border:1px solid black;"><p>Se ha obtenido acceso indirecto a un objeto</p></td>
<td style="border:1px solid black;"><p>Actividad esperada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>596</p></td>
<td style="border:1px solid black;"><p>Copia de seguridad de clave maestra de protección de datos</p></td>
<td style="border:1px solid black;"><p>Actividad esperada. Se produce cada 90 días de acuerdo con la configuración predeterminada.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>597</p></td>
<td style="border:1px solid black;"><p>Recuperación de la clave maestra de protección de datos</p></td>
<td style="border:1px solid black;"><p>Actividad esperada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>672</p></td>
<td style="border:1px solid black;"><p>Solicitud de vale Kerberos AS</p></td>
<td style="border:1px solid black;"><p>No contiene información adicional si ya se están recopilando datos de auditoría de los eventos de inicio de sesión 528 y 540. Este evento registra que se ha concedido un TGT Kerberos. El acceso no se produce hasta que se concede un vale de servicio, lo que se audita por medio del evento 673. Si PATYPE es PKINIT, se trata de un inicio de sesión de tarjeta inteligente.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>680</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión de la cuenta</p></td>
<td style="border:1px solid black;"><p>Actividad ya registrada por otros eventos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>697</p></td>
<td style="border:1px solid black;"><p>Se ha llamado a la API de comprobación de directivas de contraseñas</p></td>
<td style="border:1px solid black;"><p>Actividad esperada.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>768</p></td>
<td style="border:1px solid black;"><p>Colisión de espacios de nombres del bosque</p></td>
<td style="border:1px solid black;"><p>Este evento no está relacionado con la seguridad.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>769<br />
770<br />
771</p></td>
<td style="border:1px solid black;"><p>Información de bosque de confianza agregada, eliminada o modificada</p></td>
<td style="border:1px solid black;"><p>Actividad esperada. Estos eventos no se deben confundir con la adición, modificación o eliminación de la propia confianza.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>832<br />
833<br />
834<br />
835<br />
836<br />
837<br />
838<br />
839<br />
840<br />
841</p></td>
<td style="border:1px solid black;"><p>Varios eventos de replicación de Active Directory</p></td>
<td style="border:1px solid black;"><p>Estos eventos no están relacionados con la seguridad.</p></td>
</tr>
</tbody>
</table>
  
**Nota**   Existen algunos riesgos asociados a la exclusión de información de una auditoría, pero ese nivel de riesgo se debería comparar con las ventajas de la reducción de la carga en un agente de análisis.
  
Los sucesos que se enumeran en la tabla siguiente a menudo se excluyen de las consultas de supervisión de la seguridad dada su frecuencia y la falta de utilidad de la información que proporcionan.
  
**Nota: **Aunque existe cierto riesgo al excluir información de una auditoría, debe evaluarlo en función de la frecuencia de los sucesos y la carga resultante del agente de análisis.
  
**Tabla A.2: Reducción de la carga de almacenamiento mediante la eliminación de sucesos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Id. de suceso</p></th>
<th><p>Incidencia</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>538</p></td>
<td style="border:1px solid black;"><p>Cierre de sesión del usuario</p></td>
<td style="border:1px solid black;"><p>Este suceso no indica necesariamente la hora en que el usuario dejó de utilizar el equipo. Por ejemplo, si el usuario apaga el equipo sin antes cerrar la sesión o si se interrumpe la conexión de red a un recurso compartido, puede que el equipo no registre el cierre de sesión o que lo haga sólo cuando detecte la interrupción de la conexión.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>551</p></td>
<td style="border:1px solid black;"><p>El usuario inicia el cierre de sesión</p></td>
<td style="border:1px solid black;"><p>Utiliza el suceso 538, que confirma el cierre de sesión.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>562</p></td>
<td style="border:1px solid black;"><p>Identificador para un objeto cerrado</p></td>
<td style="border:1px solid black;"><p>Siempre registra una operación correcta.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>571</p></td>
<td style="border:1px solid black;"><p>El Administrador de autorización ha eliminado el contexto cliente.</p></td>
<td style="border:1px solid black;"><p>Normal cuando el Administrador de autorización está en uso.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>573</p></td>
<td style="border:1px solid black;"><p>Proceso que genera un suceso de auditoría que no es del sistema con la interfaz de programación de aplicaciones de autorización (API AuthZ)</p></td>
<td style="border:1px solid black;"><p>Comportamiento típico.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>577</p>
<p>578</p></td>
<td style="border:1px solid black;"><p>Se ha llamado al servicio de privilegio, operación de objeto privilegiado</p></td>
<td style="border:1px solid black;"><p>Estos sucesos de gran volumen no suelen contener información que permita comprender lo ocurrido ni actuar en los sucesos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>594</p></td>
<td style="border:1px solid black;"><p>Se ha duplicado un identificador para un objeto</p></td>
<td style="border:1px solid black;"><p>Comportamiento típico.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>595</p></td>
<td style="border:1px solid black;"><p>Se ha obtenido acceso indirecto a un objeto</p></td>
<td style="border:1px solid black;"><p>Comportamiento típico.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>596</p></td>
<td style="border:1px solid black;"><p>Copia de seguridad de clave de sesión de protección de datos</p></td>
<td style="border:1px solid black;"><p>Tiene lugar automáticamente cada 90 días con la configuración predeterminada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>597</p></td>
<td style="border:1px solid black;"><p>Recuperación de clave de sesión de protección de datos</p></td>
<td style="border:1px solid black;"><p>Comportamiento típico.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>624</p>
<p>642</p></td>
<td style="border:1px solid black;"><p>Suceso 624 cuando <strong>Usuario</strong> es igual a <em>Sistema</em>, seguido de 642 cuando <strong>Nombre de cuenta de destino</strong> es igual a <em>IUSR_nombreEquipo</em> o <em>IWAM_nombreEquipo</em>, y <strong>Nombre de usuario que llama</strong> es igual a <em>nombreEquipo$</em></p></td>
<td style="border:1px solid black;"><p>Esta secuencia de sucesos indica que un administrador tiene instalado IIS en el equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>624</p>
<p>630</p>
<p>642</p></td>
<td style="border:1px solid black;"><p><strong>Usuario</strong> es igual a <em>Sistema</em> y los tres sucesos presentan la misma marca de hora, <strong>Nombre de cuenta de destino/nueva</strong> es igual a <em>Asistente de ayuda</em> y <strong>Nombre de usuario que llama</strong> es igual a <em>nombreCD$</em>.</p></td>
<td style="border:1px solid black;"><p>Esta secuencia se genera cuando un administrador instala Active Directory en un equipo que ejecuta Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>624 o</p>
<p>642</p></td>
<td style="border:1px solid black;"><p><strong>Usuario</strong> es igual a <em>nombreExchangeServer$</em> y <strong>Nombre de cuenta de destino</strong> es un identificador único global (GUID)</p></td>
<td style="border:1px solid black;"><p>Este suceso tiene lugar cuando Exchange Server se conecta y genera automáticamente buzones de sistema.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>624</p></td>
<td style="border:1px solid black;"><p><strong>Nombre de usuario que llama</strong> es cualquier usuario y <strong>Nombre de cuenta nueva</strong> es <em>nombreEquipo$</em>.</p></td>
<td style="border:1px solid black;"><p>Un usuario del dominio ha creado o conectado un equipo nuevo en el dominio. Este suceso se acepta si los usuarios tienen derecho a unir equipos a un dominio; de lo contrario, el suceso no se debe investigar.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>627</p></td>
<td style="border:1px solid black;"><p><strong>Usuario</strong> es igual a <strong>Sistema</strong> y <strong>Nombre de cuenta de destino</strong> es igual a <strong>TsInternetUser</strong>. <strong>Nombre de usuario que llama</strong> suele ser <strong>nombreCD$</strong>.</p></td>
<td style="border:1px solid black;"><p>Estos sucesos se producen como resultado del comportamiento normal de un equipo que ejecuta Servicios de Terminal Server.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>672</p></td>
<td style="border:1px solid black;"><p>Solicitud de vale AS Kerberos</p></td>
<td style="border:1px solid black;"><p>Si recopila sucesos 528 y 540 procedentes de todos los equipos, puede que el suceso 672 no contenga información útil adicional, ya que sólo registra la concesión de un vale TGT Kerberos. Se debe producir la concesión de un vale de servicio (suceso 673) para que pueda tener lugar cualquier acceso.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>680</p></td>
<td style="border:1px solid black;"><p>Inicio de sesión de cuenta</p></td>
<td style="border:1px solid black;"><p>Si recopila sucesos 528 y 540 procedentes de todos los equipos, puede que el suceso 680 no contenga información útil adicional, ya que sólo registra la validación de las credenciales de la cuenta. Un suceso de inicio de sesión independiente registra el contenido al que el usuario obtuvo acceso.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>697</p></td>
<td style="border:1px solid black;"><p>API de comprobación de directiva de contraseña llamada</p></td>
<td style="border:1px solid black;"><p>Comportamiento típico.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>768</p></td>
<td style="border:1px solid black;"><p>Colisión de espacio de nombres de bosque</p></td>
<td style="border:1px solid black;"><p>La seguridad no se ve afectada.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>769</p>
<p>770</p>
<p>771</p></td>
<td style="border:1px solid black;"><p>Se ha agregado, eliminado o modificado información de confianza del bosque</p></td>
<td style="border:1px solid black;"><p>Estos sucesos indican el funcionamiento normal de las confianzas entre bosques. No se deben confundir con la adición, eliminación o modificación de la confianza en sí.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>De 832 a 841</p></td>
<td style="border:1px solid black;"><p>Varios problemas de replicación de Active Directory</p></td>
<td style="border:1px solid black;"><p>La seguridad no se ve afectada.</p></td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice B: Implementación de la configuración de la directiva de grupo
  
Este apéndice se debería utilizar para comprobar la configuración actual del entorno, e incluye configuraciones adicionales que afectan a la supervisión de la seguridad y la detección de ataques. Para configurar correctamente eventos de auditorías de seguridad de la directiva de grupo, hay que aplicar la configuración de la tabla siguiente.
  
**Tabla B1. Configuración de auditorías de seguridad de la directiva de grupo**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ruta de acceso de directiva</p></th>
<th><p>Directiva</p></th>
<th><p>Configuración de directiva y comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión de cuenta</p></td>
<td style="border:1px solid black;"><p>Habilite con cuidado la auditoría de aciertos en todos los equipos, porque este evento registra quién ha tenido acceso al equipo. Habilite con cuidado la auditoría de errores, porque un atacante con acceso de red sin credenciales podría iniciar un ataque de denegación de servicio (DoS), lo que obligaría al equipo a consumir recursos mientras registra estos eventos. Habilite la auditoría de aciertos también con cuidado, porque esta configuración podría provocar ataques DoS si los equipos están configurados para cerrarse cuando los registros de auditoría están llenos. Establezca una correlación entre los inicios de sesión del administrador y cualquier otra entrada sospechosa.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar la administración de cuentas</p></td>
<td style="border:1px solid black;"><p>Habilite los eventos correctos e incorrectos. Compare todas las entradas de auditoría de aciertos con las autorizaciones del administrador. Todos los errores se deberían considerar sospechosos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar el acceso del servicio de directorio</p></td>
<td style="border:1px solid black;"><p>La directiva de grupo de los controladores de dominio predeterminados habilita esta opción de manera predeterminada. Configure las opciones de auditoría en objetos de directorio confidenciales por medio de listas de control de acceso del sistema (SACL) en Usuarios y equipos de Active Directory o en el editor de interfaces de servicios de Active Directory (Editor ADSI). Debería planear la implementación de listas SACL y debería probarlas en un entorno de laboratorio realista antes de implementarlas en un entorno de producción. Este método impide la sobrecarga de los registros de seguridad por haber demasiados datos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar eventos de inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Habilite con cuidado la auditoría de aciertos en todos los equipos, porque este evento registra quién ha tenido acceso al equipo. Habilite con cuidado la auditoría de errores, porque un atacante con acceso de red sin credenciales podría realizar un ataque DoS para generar muchísimos errores.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar el acceso a objetos</p></td>
<td style="border:1px solid black;"><p>Tenga cuidado al habilitar esta opción, porque podría producir un volumen muy alto de auditorías. Configure las opciones de auditoría únicamente para carpetas de gran valor a través de SACL y sólo audite los tipos de acceso específicos que sean de interés. Si es posible, sólo audite los eventos de escritura de auditoría y no los de acceso de lectura.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar el cambio de directivas</p></td>
<td style="border:1px solid black;"><p>Habilite las auditorías de aciertos y de errores. Establezca una correlación cruzada entre los eventos correctos y las autorizaciones administrativas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar el uso de privilegios</p></td>
<td style="border:1px solid black;"><p>No habilite las auditorías para el uso de privilegios por el gran volumen de eventos que generaría esta configuración.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar el seguimiento de procesos</p></td>
<td style="border:1px solid black;"><p>Habilite esta opción en equipos vulnerables e investigue inmediatamente las actividades inesperadas de aplicaciones mediante el aislamiento del sistema si es necesario. No habilite esta opción en servidores web CGI (Common Gateway Interface), sistemas de prueba, servidores que ejecutan procesos por lotes ni estaciones de trabajo de desarrollo, porque los registros de sucesos podrían llenarse.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p>Auditar eventos del sistema</p></td>
<td style="border:1px solid black;"><p>Habilite las auditorías de aciertos y de errores.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Asignación de derechos de usuario</p></td>
<td style="border:1px solid black;"><p>Generar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>Esta opción se asigna de manera predeterminada al sistema local, el servidor local y el servicio de red. Este derecho no se debería aplicar a ninguna cuenta que no sea una cuenta de servicio. Un atacante podría utilizar esta opción para generar eventos falsos o imprecisos en el registro de seguridad.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Asignación de derechos de usuario</p></td>
<td style="border:1px solid black;"><p>Administrar registro de seguridad y auditoría</p></td>
<td style="border:1px solid black;"><p>Utilice esta opción para evitar que los administradores realicen cambios en las configuraciones de auditoría de los archivos, las carpetas y el Registro. Piense en la posibilidad de crear un grupo de seguridad para los administradores que tienen permiso para cambiar la configuración de auditoría y quitar el grupo de administradores de la configuración de la directiva de seguridad local. Sólo los miembros de un grupo de seguridad deberían ser capaces de configurar la auditoría.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p>Auditoría: auditar el acceso de objetos globales del sistema</p></td>
<td style="border:1px solid black;"><p>Esta opción agrega listas SACL a objetos del sistema con nombre como, por ejemplo, exclusiones mutuas, semáforos y dispositivos de MS-DOS. La configuración predeterminada de Windows Server 2003 no tiene habilitada esta opción. No la habilite, porque produce un gran volumen de eventos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p>Auditoría: auditar el uso del privilegio de copias de seguridad y restauración</p></td>
<td style="border:1px solid black;"><p>Las operaciones de copia de seguridad y restauración ofrecen la oportunidad de robar datos al burlar las listas ACL. No habilite esta opción, porque produce un gran volumen de eventos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p>Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad</p></td>
<td style="border:1px solid black;"><p>Habilite esta opción únicamente después de pensarlo mucho y sólo en equipos de gran valor, porque los atacantes podrían utilizarla para realizar ataques DoS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p>Tamaño máximo del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Opción recomendada dependiendo de los volúmenes de eventos previsto y de las opciones de conservación de los registros de seguridad. Esta opción sólo puede utilizar incrementos de 64 KB y el tamaño medio de los eventos es 0,5 KB. En entornos de gran volumen, se puede configurar hasta en 250 MB, pero el tamaño total combinado de todos los registros de sucesos no puede superar 300 MB.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p>Evitar que el grupo de invitados locales tenga acceso al registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Windows Server 2003 habilita esta opción de manera predeterminada. No hay que cambiarla.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p>Conservar el registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Habilite únicamente esta opción si el método de conservación seleccionado es “Sobrescribir sucesos por días”. Si se utiliza un sistema de correlación de eventos que sondea los eventos, asegúrese de que el número de días es al menos tres veces la frecuencia de sondeo para permitir errores del ciclo de sondeo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p>Método de retención del registro de seguridad</p></td>
<td style="border:1px solid black;"><p>Habilite la opción No sobrescribir sucesos en entornos de alta seguridad. Si es así, establezca procesos para vaciar y archivar los registros regularmente, especialmente si está habilitada la opción Apagar el sistema de inmediato si no puede registrar auditorías de seguridad.</p></td>
</tr>
</tbody>
</table>
  
Para configurar correctamente los valores de auditoría de seguridad de Directiva de grupo, aplique la configuración que se enumera en la tabla siguiente. En la tabla también se incluyen configuraciones adicionales que repercuten en la supervisión de la seguridad y la detección de ataques. Utilice esta tabla para comprobar la configuración actual del entorno.
  
**Tabla B.2: Configuración de la auditoría de seguridad de Directiva de grupo**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ruta de directiva</p></th>
<th><p>Directiva</p></th>
<th><p>Configuración de la directiva y comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar sucesos de inicio de sesión de cuenta</strong></p></td>
<td style="border:1px solid black;"><p>Habilite la operación de auditoría correcta en todos los equipos, ya que este suceso registra a la persona que tuvo acceso al equipo. Habilite el error de auditoría con precaución. Un atacante con acceso a la red, aunque sin credenciales, podría iniciar un ataque de denegación del servicio (DoS), a medida que el equipo consume recursos para generar estos sucesos. Habilite la operación de auditoría correcta con precaución, porque este valor puede dar lugar a ataques DoS si los equipos se apagan cuando los registros de auditoría están llenos. Establezca la correlación de los inicios de sesión de administrador con las entradas sospechosas.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar la administración de cuentas</strong></p></td>
<td style="border:1px solid black;"><p>Habilite las operaciones correcta e incorrecta. Establezca la correlación de las entradas de auditoría correctas con autorizaciones de administrador. Considere todos los errores sospechosos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar el acceso del servicio de directorio</strong></p></td>
<td style="border:1px solid black;"><p>La Directiva de grupo predeterminada de controladores de dominio habilita este valor de forma predeterminada. Configure los valores de auditoría en objetos de directorio confidenciales a través de listas de control de acceso al sistema (SACL) en Usuarios y equipos de Active Directory o en el editor de la Interfaz de servicios de Active Directory (Edición de ADSI). Debe planear la implementación de SACL y probarlas en un entorno de laboratorio real antes de implementarlas en un entorno de producción. De este modo, evitará la sobrecarga de datos en los registros de seguridad.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar sucesos de inicio de sesión</strong></p></td>
<td style="border:1px solid black;"><p>Habilite la operación de auditoría correcta en todos los equipos, ya que este suceso registra a la persona que tuvo acceso al equipo. Habilite el error de auditoría con precaución, porque un atacante con acceso a la red, aunque sin credenciales, podría ocasionar que el equipo consumiera recursos para generar estos sucesos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar el acceso a objetos</strong></p></td>
<td style="border:1px solid black;"><p>Preste atención al habilitar este valor, ya que podría dar lugar a un gran volumen de auditoría. Configure los valores de auditoría sólo en las carpetas más valiosas a través de SACL y audite sólo el número mínimo de tipos de acceso en los que esté interesado. Audite sólo accesos de escritura (y no de lectura) si el modelo de amenaza lo permite.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar el cambio de directivas</strong></p></td>
<td style="border:1px solid black;"><p>Habilite la auditoría de sucesos correctos e incorrectos. Establezca referencias cruzadas de las operaciones correctas con autorizaciones de administrador. Considere todos los errores sospechosos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar el uso de privilegios</strong></p></td>
<td style="border:1px solid black;"><p>No habilite la auditoría del uso de privilegios, ya que esta acción genera un alto volumen de sucesos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar el seguimiento de procesos</strong></p></td>
<td style="border:1px solid black;"><p>No habilite este valor en servidores Web CGI (Common Gateway Interface), equipos de prueba, servidores que ejecutan procesos por lotes o estaciones de trabajo de desarrolladores. Habilite este valor en equipos vulnerables y actúe inmediatamente en los casos de actividad de aplicaciones inesperada. Para ello, aísle físicamente el equipo si es necesario. Este valor puede ocasionar que los registros de sucesos se llenen.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/</p>
<p>Directiva de auditoría</p></td>
<td style="border:1px solid black;"><p><strong>Auditar sucesos del sistema</strong></p></td>
<td style="border:1px solid black;"><p>Habilite la auditoría de sucesos correctos e incorrectos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/ Asignación de derechos de usuario</p></td>
<td style="border:1px solid black;"><p><strong>Generar auditorías de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>Este valor se asigna de forma predeterminada al sistema local, al servicio local y al servicio de red. Este derecho no se debe aplicar a cuentas distintas a las de servicio. Un atacante puede utilizar este valor para generar sucesos falsos o imprecisos en el registro de seguridad.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/ Asignación de derechos de usuario</p></td>
<td style="border:1px solid black;"><p><strong>Administrar los registros de auditoría y seguridad</strong></p></td>
<td style="border:1px solid black;"><p>Utilice este valor para determinar qué administradores pueden modificar la configuración de auditoría de archivos, carpetas y registro. Considere la creación de un grupo de seguridad para los administradores que pueden cambiar la configuración de auditoría y eliminar el grupo de administradores de la configuración de Directiva de seguridad local. Sólo los miembros del nuevo grupo de seguridad podrán configurar la auditoría.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/ Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p><strong>Auditoría: auditar el acceso de objetos globales del sistema</strong></p></td>
<td style="border:1px solid black;"><p>Este valor agrega SACL a objetos con nombre del sistema, como exclusiones mutuas (sucesos exclusivos mutuos), semáforos y dispositivos de MS-DOS. La configuración predeterminada de Windows Server 2003 no habilita esta opción. No habilite este valor, ya que genera un volumen de sucesos muy elevado.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Directivas locales/ Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p><strong>Auditoría: auditar el uso del privilegio de copia de seguridad y restauración</strong></p></td>
<td style="border:1px solid black;"><p>Las operaciones de copia de seguridad y restauración permiten obtener datos protegidos por las ACL. No habilite este valor, ya que genera un volumen de sucesos muy elevado.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Directivas locales/ Opciones de seguridad</p></td>
<td style="border:1px solid black;"><p><strong>Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>Tras considerarlo cuidadosamente, habilite este valor sólo en equipos muy valiosos, ya que un atacante puede utilizar esta característica para realizar ataques DoS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p><strong>Tamaño máximo del registro de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>El tamaño máximo del registro de seguridad debe ser múltiplo de 64 kB. El tamaño medio de un suceso es de 0,5 kB. La configuración recomendada depende de los volúmenes de los sucesos proyectados y de la configuración de retención de los registros de seguridad. En el caso de los entornos con un gran volumen de sucesos, establezca el tamaño del archivo de registro en el mayor valor posible, incluso hasta 250 MB. El tamaño total de todos los registros de sucesos no puede ser superior a 300 MB. No intente superar este valor.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p><strong>Evitar que el grupo de invitados locales tenga acceso al registro de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>Windows Server 2003 habilita este valor de forma predeterminada. No lo cambie.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p><strong>Conservar el registro de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>Habilite este valor sólo si selecciona el método de retención &quot;Sobrescribir sucesos por días&quot;. Si utiliza un sistema de correlación de sucesos que sondea sucesos, asegúrese de que el número de días es, al menos, tres veces la frecuencia de sondeo, con el fin de permitir ciclos de sondeo de error.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Registro de sucesos</p></td>
<td style="border:1px solid black;"><p><strong>Método de retención del registro de seguridad</strong></p></td>
<td style="border:1px solid black;"><p>En los entornos con nivel de seguridad alto, habilite el valor No sobrescribir sucesos. En este caso, establezca procedimientos para vaciar y archivar los registros con regularidad, sobre todo si el equipo se apaga cuando el registro de seguridad está lleno.</p></td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener el artículo Supervisión de la seguridad y detección de ataques](http://go.microsoft.com/fwlink/?linkid=71717)
  
[](#mainsection)[Principio de la página](#mainsection)
