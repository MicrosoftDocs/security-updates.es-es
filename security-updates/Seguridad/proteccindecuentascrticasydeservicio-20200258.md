---
TOCTitle: Protección de cuentas críticas y de servicio
Title: Protección de cuentas críticas y de servicio
ms:assetid: 'aed37382-e798-437b-8740-8a03412ed1ef'
ms:contentKeyID: 20200258
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875826(v=TechNet.10)'
---

Protección de cuentas críticas y de servicio
============================================

Publicado: septiembre 26, 2006

##### En esta página

[](#ehaa)[Introducción](#ehaa)
[](#egaa)[Definiciones](#egaa)
[](#efaa)[Retos](#efaa)
[](#eeaa)[Soluciones](#eeaa)
[](#edaa)[Resumen](#edaa)
[](#ecaa)[Apéndice A: Servicios habituales](#ecaa)

### Introducción

El primer paso para proteger la red de una media empresa consiste en comprender las vulnerabilidades que un atacante seguramente va a aprovechar. La principal tarea de un atacante que se infiltra en una red es iniciar una elevación de privilegios, método con el que intenta obtener un acceso más amplio desde el punto de partida del ataque. Cuando se produce una elevación de privilegios, poco se puede hacer para detener cualquier intento de ataque que pretenda realizar un intruso. Los atacantes pueden usar diferentes mecanismos para lograr la elevación de privilegios pero, prácticamente todos ellos, implican el poner en peligro las cuentas existentes, especialmente las que tienen privilegios equivalentes a un administrador.

Las redes de las medianas empresas suelen usar algún tipo de medida de control de seguridad sobre las cuentas de usuario estándar, pero no suelen ejercer mucho control sobre las cuentas de servicio, por lo que dichas cuentas pasan a ser vulnerables y, por tanto, el objetivo habitual de los atacantes. Cuando un atacante pone en peligro una red hasta el punto en que una cuenta crítica con elevados privilegios queda expuesta, la red ya no podrá volver a considerarse de confianza en su totalidad, a menos que se elimine y se vuelva a crear por completo. Por lo tanto, el nivel de seguridad para todos los tipos de cuentas es un aspecto muy importante que debe incluir cualquier iniciativa de seguridad para una red.

Aparte de los riesgos que suponen las amenazas externas para la red de una mediana empresa, las amenazas internas también pueden provocar muchos daños. Las amenazas internas encarnan no sólo a los usuarios malintencionados sino también a aquellos que pueden causar un daño no intencional. Los intentos aparentemente inocuos de infringir las medidas de seguridad realizados por los usuarios que desean tener acceso a recursos son sólo uno de estos ejemplos. En demasiadas ocasiones, a los usuarios y a los servicios se les otorga acceso a más privilegios de los que necesitan por motivos de comodidad. Si bien este método garantiza que los usuarios tienen acceso a los recursos que necesitan para realizar su trabajo, también aumenta el riesgo de que un ataque a la red tenga éxito.

#### Resumen ejecutivo

Como se menciona en la introducción, el tema de administrar la seguridad de todos los tipos de cuentas de una red es muy importante para calcular el riesgo que corre la red de una mediana empresa. Se deben tener en cuenta las amenazas internas y externas y la solución frente a éstas debe mantener un equilibrio entre la necesidad de seguridad y que las medianas empresas puedan obtener acceso a sus recursos de red cuando lo necesiten.

Este documento ayudará a las medianas empresas a comprender los riesgos asociados con las cuentas administrativas, de servicio, relacionadas con la aplicación y predeterminadas. Esta información les ayudará a contar con la base necesaria, a partir de la cual podrán desarrollar e implementar pasos que las medianas empresas podrán realizar para mitigar esos riesgos. Para ello, es necesario tratar la naturaleza de estas cuentas, cómo identificarlas, cómo determinar los permisos adecuados que necesitan para funcionar y cómo mitigar los riesgos inherentes en cuentas de servicio y de nivel de administrador elevadas.

Como parte de la iniciativa Microsoft Trustworthy Computing, la configuración predeterminada de Microsoft® Windows Server™ 2003 se diseñó para proteger el servicio de directorio Active Directory® frente a distintos tipos de amenazas; sin embargo, hay algunos parámetros de las cuentas administrativas que se pueden reforzar aún más para aumentar el nivel de seguridad de la red de una mediana empresa. Además, también se deben proteger los servicios que no se proporcionan con el sistema operativo Windows Server 2003 y que se instalan con otras aplicaciones. Este documento explica los métodos necesarios para proteger esas cuentas y servicios, además de las prácticas recomendadas para controlar la forma de implementar y administrar los privilegios administrativos.

#### Información general

Este documento consta de cuatro secciones principales que proporcionan información sobre la protección de las cuentas de administrador y de servicio en el entorno de una mediana empresa. La primera sección es la "Introducción", que es la que está leyendo en este momento. El resto del documento tiene la siguiente estructura:

-   **Definiciones**. Esta sección ofrece alguna información previa y descripciones de la terminología incluida en el documento.

-   **Retos**. Esta sección describe algunos de los problemas habituales a los que se enfrentan las medianas empresas a la hora de determinar por qué es necesario proteger las cuentas, así como algunos de los problemas asociados con la protección de las cuentas de administrador y de servicio.

-   **Soluciones**. Esta sección está dividida en tres subsecciones que ofrecen al lector la información necesaria sobre las distintas fases de los métodos que pueden usarse para proteger las cuentas críticas y de servicio de una mediana empresa. Estos subsecciones incluyen:

    -   **Evaluación**. Esta subsección describe las consideraciones básicas para proteger las cuentas críticas y de servicio y sienta las bases para la planeación de soluciones.

    -   **Desarrollo**. Esta subsección usa la información de la subsección "Evaluación" para ofrecer soluciones que ayudarán al lector a desarrollar planes que mejoren la seguridad de las cuentas críticas y de servicio.

    -   **Implementación y administración**. Esta subsección describe los métodos recomendados para implementar cuentas de servicio y de administrador protegidas en el entorno de una mediana empresa.

#### Quién debería leer este documento:

El objetivo de este documento técnico es ayudar a los profesionales de la tecnología y a los administradores técnicos preocupados por la seguridad de las cuentas de nivel de servicio, de aplicación y de administrador en una red de Microsoft. Si bien los destinatarios no técnicos pueden usar este documento para comprender mejor los principios de una administración de cuentas segura, se deben tener conocimientos sobre los conceptos y procedimientos de la administración de cuentas de Microsoft Windows® y Active Directory para poder aprovechar al máximo la información de este documento.

[](#mainsection)[Principio de la página](#mainsection)

### Definiciones

Esta sección define una serie de términos que se usan en este documento y que tal vez sea necesario aclarar.

-   **Servicios**. Los servicios son archivos ejecutables que se ejecutan durante el inicio o que se pueden desencadenar mediante otros sucesos o instancias programadas. Se suelen ejecutar en segundo plano sin demasiada interacción o intervención del usuario.

-   **Cuentas de servicio**. En resumen, una cuenta de servicio se suele definir como cualquier cuenta que no se corresponda con una persona real. Se suele tratar de cuentas integradas que usan los servicios para tener acceso a los recursos que necesitan cuando tienen que realizar sus actividades. Sin embargo, algunos servicios necesitan cuentas de usuario reales para realizar determinadas funciones; además, muchas empresas siguen empleando también cuentas de dominio para ejecutar los servicios.

-   **Cuenta administrativa**. Si bien en cada instalación nueva de un dominio de Microsoft Windows o Active Directory se crea una cuenta de administrador predeterminada, el término "cuenta de administrador" se suele usar en un sentido general para describir cualquier cuenta a la que se le otorguen privilegios de nivel de administrador. Por claridad, en este documento se harán distinciones entre los dos tipos.

-   **Grupos administrativos**. Estos grupos pueden variar según los servicios instalados, pero pueden incluir los creados automáticamente en los contenedores Builtin y de usuarios. Estos grupos también incluyen cualquiera creado y que tenga otorgados privilegios administrativos.

-   **Cuentas críticas**. Este documento usa el término “cuenta crítica” para describir las cuentas predeterminadas que se consideran de alto riesgo porque tienen privilegios de alto nivel o presentan muchos riesgos debido a su uso ubicuo.

-   **Cuenta estándar**. Una cuenta estándar es cualquier cuenta que no sea miembro de un grupo administrativo y que no tenga ningún privilegio elevado equivalente a los de una cuenta de administrador de dominio o local. Normalmente, una cuenta estándar sería miembro del grupo Usuarios del dominio o del grupo Usuarios locales.

-   **Principio del privilegio mínimo**. El documento Department of Defense Trusted Computer System Evaluation Criteria (Criterios de evaluación de equipos de confianza del Departamento de Defensa), (DOD-5200.28-STD), o Libro naranja, es un estándar aceptado en lo que respecta a la seguridad de los equipos. Esta publicación define el privilegio mínimo como un principio que “exige que a cada sujeto de un sistema se le otorgue el conjunto de privilegios más restrictivo (o con menor autorización) necesario para la realización de tareas autorizadas. La aplicación de este principio limita el daño que se puede producir por accidentes, errores o por un uso no autorizado”.

[](#mainsection)[Principio de la página](#mainsection)

### Retos

Como se explica en la sección anterior, las cuentas de servicio y de nivel administrativo desprotegidas representan riesgos significativos para la seguridad de la red de una mediana empresa. Dada la complejidad de los entornos de red y las rápidas tasas de crecimiento que experimentan la mayoría de las redes de empresa, es bastante habitual encontrase con prácticas de administración de cuentas que incluyen importantes vulnerabilidades. Estos factores explican el motivo por el que la protección de las cuentas críticas y de los servicios que se ejecutan en una red se convierte en una tarea desalentadora.

Algunos de los problemas más habituales que tienen las medianas empresas al estudiar cómo hacer frente a esas preocupaciones por la seguridad incluyen:

-   Cómo protegerse frente a amenazas internas y externas relacionadas con la administración de cuentas y los intentos de los empleados por hacerles frente.

-   Cómo identificar todas las cuentas de servicio y de aplicación que se usan en los equipos locales y de red.

-   Cómo proteger las sensibles cuentas relacionadas con aplicaciones, administradores y servicios.

-   Cómo determinar qué cuentas están asociadas con los servicios y las aplicaciones.

-   Cómo aislar las cuentas de servicio de las directivas de contraseñas de cuentas de usuarios.

[](#mainsection)[Principio de la página](#mainsection)

### Soluciones

Las soluciones que se ofrecen en este documento siguen el método del principio del privilegio mínimo y de la cuenta de usuario de privilegio mínimo (LUA) en la administración de cuentas de servicio, administrativas y críticas.

En la mayoría de los cursos y documentación relacionados con la seguridad se menciona el principio del privilegio mínimo. Si bien dicho principio es relativamente fácil de entender, también servirá para mejorar en gran medida el perfil de seguridad de cualquier empresa que lo implemente. En resumen, este principio establece que todas las cuentas deben tener exclusivamente el conjunto de privilegios mínimo absoluto necesario para realizar las tareas actuales. Este principio se aplica no sólo a los usuarios, sino también a los equipos y servicios que se ejecutan en ellos.

Seguir este principio no sólo ayuda a protegerse frente a los atacantes malintencionados y el malware, sino que también mejora el perfil de seguridad de una empresa, ya que obliga a los profesionales de la tecnología a realizar exhaustivas investigaciones para determinar los privilegios de acceso que necesitan los distintos usuarios, equipos y aplicaciones. Tener en cuenta esta información ayuda a comprender los procesos o la configuración que tal vez no tenga la protección necesaria y, por lo tanto, se convierte en un paso esencial en cualquier iniciativa de seguridad que desee tener éxito.

Por ejemplo, según el principio del privilegio mínimo, una persona que tenga la función de administrador de dominio sólo debe usar una cuenta con el privilegio de nivel de administración de dominio al realizar tareas que necesiten ese nivel de acceso. Por el contrario, cuando no se realicen tareas que necesiten un privilegio de nivel superior, un administrador debe usar una cuenta con derechos de acceso estándar. Dicha práctica debería reducir las amenazas de seguridad originadas de los errores humanos y reducirá el daño provocado si una estación de trabajo administrativa se infectara con malware.

#### Evaluación

Para proteger las cuentas críticas y de servicio, es necesario identificar la relación de éstas con las amenazas asociadas con dichas cuentas. Sin embargo, también es importante garantizar que se conocen las consecuencias asociadas con su cambio para asegurar que el impacto en la empresa quede reducido a niveles aceptables.

##### Administración de cuentas de administrador y críticas

Para proteger las cuentas administrativas y críticas y los grupos asociados, es necesario saber las cuentas y grupos que cumplen estos criterios. Es igualmente importante comprender el alcance de los privilegios de nivel administrativo y los sistemas a los que afectan, especialmente, cuando se usan controladores de dominio.

Por lo tanto, es importante que el lector de este documento tenga un conocimiento avanzado sobre las cuentas de nivel administrativo en su entorno y conozca también todos los controladores de dominio y las cuentas que los administran.

##### Cuentas y grupos administrativos

Las cuentas de nivel administrativo de una red Active Directory incluyen:

-   La cuenta predeterminada Administrador, que se crea cuando se instala Active Directory en el primer controlador de dominio de un dominio. Esta cuenta es la más completa de un dominio, por lo que se debe proteger con contraseña cuando se cree.

-   Cualquier cuenta que se cree posteriormente y a la que se le otorguen privilegios administrativos directamente o mediante su inclusión en un grupo administrativo.

Los grupos administrativos de un dominio de Active Directory variarán, según los servicios que tenga instalados dicho dominio. Un dominio básico de Active Directory incluirá lo siguiente:

-   Grupos administrativos que se creen automáticamente en el contenedor Builtin.

-   Grupos administrativos que se creen automáticamente en el contenedor de usuarios.

-   Cualquier grupo creado posteriormente que se incluya en grupos con un privilegio administrativo o a los que se les asignen privilegios administrativos.

##### Administradores de servicios y de datos

Existen dos tipos diferentes de privilegios administrativos en cualquier entorno de Windows Server 2003 Active Directory: administradores de servicios y de datos.

-   Las cuentas de administrador de servicios controlan el mantenimiento y la entrega de los servicios de directorio, que incluyen la administración de controladores de dominio y Active Directory.

-   Las cuentas de administrador de datos controlan los datos almacenados en el servicio de directorio, en los servidores de miembros de dominio, así como en las estaciones de trabajo del dominio.

Si bien los usuarios pueden realizar ambas funciones en cualquier entorno concreto, es importante conocer las cuentas y grupos predeterminados que tienen un alcance de administradores de servicio. Las cuentas de administradores de servicio tienen muchos privilegios en un entorno de red, por lo que deben contar con la máxima protección. Estas cuentas se encargan de la configuración de todo el directorio, la instalación y mantenimiento del software, la aplicación de service packs y actualizaciones del sistema operativo en los controladores de dominio.

**Tabla 1. Grupos y cuentas de administrador de servicios predeterminados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Contenedor</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Builtin</td>
<td style="border:1px solid black;">Este grupo tiene acceso completo a todos los controladores de dominio y a todo el contenido de directorio almacenado en un dominio. Este grupo es el grupo de administrador de servicios con más privilegios y puede cambiar los miembros del resto de grupos administrativos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administradores de organización</td>
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Este grupo se agrega automáticamente al grupo Administradores de cada dominio y tiene acceso completo a la configuración de todos los controladores de dominio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administradores del dominio</td>
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Este grupo se agrega automáticamente al grupo Administradores de cada dominio de un bosque. Por lo tanto, el grupo Administradores del dominio tiene derechos sobre todos los controladores de dominio y datos almacenados en el directorio de un dominio y puede modificar los miembros de cualquier grupo administrativo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administradores de esquema</td>
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Este grupo tiene privilegios completos de administración para el esquema de Active Directory.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Operadores de cuentas</td>
<td style="border:1px solid black;">Builtin</td>
<td style="border:1px solid black;">Este grupo puede crear y administrar cuentas y grupos del dominio, pero no puede administrar cuentas de administrador de servicio. No tiene ningún miembro de manera predeterminada y, como práctica recomendada, no se debe usar para realizar ninguna delegación administrativa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Operadores de copia</td>
<td style="border:1px solid black;">Builtin</td>
<td style="border:1px solid black;">Este grupo otorga privilegios para realizar tareas de copia de seguridad y restauración en controladores de dominio y no tiene ningún miembro de manera predeterminada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Operadores de servidores</td>
<td style="border:1px solid black;">Builtin</td>
<td style="border:1px solid black;">Este grupo puede realizar tareas de mantenimiento en controladores de dominio y no tiene ningún miembro de manera predeterminada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administrador del Modo de restauración de servicios de directorio</td>
<td style="border:1px solid black;">No almacenado en Active Directory</td>
<td style="border:1px solid black;">Esta cuenta se crea durante el proceso de instalación de Active Directory. Se usa para iniciar el controlador de dominio en el Modo de restauración de servicios de directorio y, si bien no es igual que la cuenta Administrador, tiene acceso completo al controlador de dominio siempre que se encuentre en este modo.</td>
</tr>
</tbody>
</table>
  
Llos grupos y cuentas de administrador de servicio que se enumeran en la tabla anterior están protegidas por un proceso de segundo plano que comprueba y aplica de forma periódica un descriptor de seguridad concreto con información de seguridad asociada con ese objeto protegido. Este proceso se extiende a cualquier miembro de un grupo de administrador de servicio y garantiza que cualquier intento no autorizado que consiga modificar ese descriptor en un miembro de grupo administrativo se sobrescribirá con la configuración protegida que se encuentra en la estructura de datos del descriptor de seguridad.
  
Esta estructura de datos de descriptor de seguridad se encuentra en el objeto AdminSDHolder. Por lo tanto, para modificar los permisos de cualquiera de los grupos de administrador de servicio o de cualquiera de las cuentas de miembros, se debe modificar el descriptor de seguridad del objeto AdminSDHolder para que los cambios se apliquen de manera coherente. Los cambios realizados en el descriptor de seguridad se aplican a la configuración predeterminada aplicada a todas las cuentas administrativas protegidas, por lo que se debe tener cuidado al modificar los permisos con este método.
  
Para obtener más información sobre la modificación de los permisos en las cuentas de administrador de servicios, consulte la [Guía de prácticas recomendadas para proteger las instalaciones de Active Directory](http://technet.microsoft.com/es-es/library/cc773365.aspx) (en inglés), que se puede descargar de la dirección www.microsoft.com/downloads/details.aspx?FamilyID=4e734065-3f18-488a-be1e-f03390ec5f91&DisplayLang=en.
  
#### Administración de cuentas de servicio y de aplicación
  
Los servicios son archivos ejecutables que se suelen ejecutar sin interacción del usuario y que se ejecutan automáticamente durante el inicio de un sistema operativo. Por este motivo, a los servicios y a las cuentas de servicio no se les suele considerar como un riesgo para la seguridad concreto para la red de una empresa. Incluso cuando se es consciente de los riesgos de seguridad, la administración de las cuentas de servicio suele ser una tarea bastante compleja, si tenemos en cuenta que un simple cambio de contraseña puede hacer necesarios otros distintos cambios para evitar las interrupciones.
  
Si bien los servicios y las cuentas de servicio predeterminados de Windows Server 2003 están protegidos frente a amenazas, muchos servicios de terceros, e incluso otros servicios adicionales de Microsoft, se deben proteger porque deben ejecutar correctamente las cuentas de servicio. Esto resulta especialmente cierto en el caso de las herramientas de administración empresarial, como Microsoft Systems Management Server o IBM Tivoli, ya que en ellas normalmente se suele usar una cuenta con derechos para todo el dominio e incluso para otros dominios con relaciones de confianza.
  
Además, el uso de cuentas de dominio para ejecutar servicios sigue siendo habitual porque resulta más fácil administrar servicios en el dominio, en lugar de en servidores individuales, a pesar de los riesgos de seguridad asociados con esta práctica. Los servicios almacenan la información de la contraseña y la cuenta de usuario que usan en el registro, tanto si utilizan cuentas locales como de dominio. Por lo tanto, si dichos servicios usan cuentas de dominio, cuando se pone en peligro un solo equipo, esta información se puede usar para elevar los privilegios del atacante. Si un servicio usa una cuenta de dominio de nivel administrativo, dicho escenario podría suponer una amenaza para toda la red.
  
##### Escenarios de vulnerabilidad de las cuentas de servicio
  
La práctica de la configuración de servicios para usar cuentas de dominio para la autenticación supone una posible amenaza para la seguridad. El grado de exposición al riesgo depende de varios factores, entre ellos:
  
-   **El número de servidores con servicios configurados para usar cuentas de servicio**. El perfil de vulnerabilidad de una red aumenta con cada servidor que tenga servicios autenticados de una cuenta de dominio que se ejecuten en ese servidor. La existencia de dicho servidor aumenta las posibilidades de que un atacante pueda poner en peligro ese servidor, lo que puede servir para elevar los privilegios a otros recursos de la red.
  
-   **El alcance de los privilegios para cualquier cuenta de dominio determinada que usen los servicios**. Cuanto mayor sea el alcance de los privilegios que tiene una cuenta de servicio, mayor será el número de recursos de dicha cuenta que se pueden poner en peligro. Los privilegios de nivel de administrador de dominio suponen un riesgo especialmente alto, ya que en el alcance de la vulnerabilidad de dichas cuentas se incluye cualquier equipo de la red, incluidos los controladores de dominio. Debido a que dichas cuentas tienen privilegios administrativos para todos los servidores miembros, el riesgo de dicha cuenta sería grande y todos los equipos y datos del dominio serían sospechosos.
  
-   **El número de servicios configurados para usar cuentas de dominio de cualquier servidor concreto**. Algunos servicios tienen vulnerabilidades concretas, que los hacen, en cierta medida, más susceptibles a los ataques. Los intrusos normalmente intentarán atacar en primer lugar a las vulnerabilidades conocidas. Si un servicio vulnerable usa una cuenta de dominio, esto supone un riesgo mayor para otros sistemas, que se podrían haber aislado con otros medios en un solo servidor.
  
-   **El número de cuentas de dominio que se usan para ejecutar servicios en un dominio**. La supervisión y la administración de la seguridad de las cuentas de servicio exige más atención que la que se presta a las cuentas de usuario; además, cada cuenta de dominio adicional usada por los servicios no hace más que complicar aún más la administración de dichas cuentas. El hecho de que los administradores y los administradores de seguridad tengan que saber dónde se usa cada cuenta de servicio para poder detectar la actividad sospechosa enfatiza la necesidad de minimizar la cantidad de cuentas de este tipo.
  
Todos estos factores hacen que se puedan producir distintos escenarios de vulnerabilidad, cada uno con un nivel diferente de posible riesgo para la seguridad. El siguiente diagrama y la siguiente tabla describen estos escenarios.
  
En estos ejemplos se asume que las cuentas de servicio son cuentas de dominio y que cada cuenta tiene al menos un servicio en cada servidor que está usando para la autenticación. La siguiente información describe las cuentas de dominio que se muestran en la siguiente figura.
  
-   La cuenta A tiene privilegios equivalentes a un administrador para más de un controlador de dominio.
  
-   La cuenta B tiene privilegios equivalentes a un administrador en todos los servidores miembro.
  
-   La cuenta C tiene privilegios equivalentes a un administrador en los servidores 2 y 3.
  
-   La cuenta D tiene privilegios equivalentes a un administrador en los servidores 4 y 5.
  
-   La cuenta E tiene privilegios equivalentes a un administrador sólo en un servidor miembro.
  
    ![](images/Cc875826.SCASA1(es-es,TechNet.10).gif)
  
    **Figura 1. Escenarios de vulnerabilidad de las cuentas de servicio de dominio**
  
La siguiente tabla describe los escenarios que se detallan en la figura y texto anteriores y los clasifica según el grado de vulnerabilidad que presentan.
  
**Tabla 2. Clasificación de los escenarios de vulnerabilidad de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Escenario</th>
<th>Descripción</th>
<th>Nivel de riesgo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Un servicio usa la cuenta A en el servidor 1. Una vez puesto en peligro el servidor 1, se descubre la información de autenticación de la cuenta A. Cuando esto ocurre, el atacante tiene acceso al controlador de dominio DC1, por lo que todos los recursos del dominio y la información que contiene pasan a ser vulnerables.
Esta situación presenta un escenario de riesgo crítico. Nunca se deben usar cuentas de dominio con privilegios equivalentes a un administrador para el dominio o controlador de dominio a la hora de ejecutar servicios en un servidor miembro.</td>
<td style="border:1px solid black;">Crítico</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">2</td>
<td style="border:1px solid black;">Un servicio usa la cuenta B en el servidor 2. La cuenta B también tiene privilegios en el servidor 1, donde la cuenta A está ejecutando un servicio. Cuando la cuenta B se pone en peligro en el servidor 2, el atacante logra el mismo acceso que el del escenario 1, con lo que el controlador de dominio y todo el dominio pueden ser objetos de ataques.
La cuenta C también expone a la red al mismo nivel de riesgo, porque se podría usar para poner en peligro el servidor 2 con un ataque iniciado desde el servidor 3, que, a su vez, podría dejar al descubierto la cuenta A que, a su vez, dejaría al descubierto todo el dominio.
Se trata de escenarios de riesgo elevado, pero se pueden resolver si se hace frente a las posibles amenazas que se presentan en el escenario 1.</td>
<td style="border:1px solid black;">Alto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">3</td>
<td style="border:1px solid black;">Un servicio que se está ejecutando en el servidor 4 y 5 usa la cuenta D. Si la cuenta D se pone en peligro, un atacante tendrá acceso a todos los servidores para los que la cuenta D tenga privilegios. Si entre estos servidores no se incluyen los servicios que usan las cuentas con un conjunto o alcance de privilegios superior, este escenario supondría un riesgo de prioridad media porque no existiría la vulnerabilidad transitiva del escenario 2.</td>
<td style="border:1px solid black;">Medio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">4</td>
<td style="border:1px solid black;">Un servicio usa la cuenta E en un solo servidor, el servidor 5, y no tiene ningún otro privilegio o asociación de servicios. Este escenario supondría una amenaza poco importante, ya que no permite la elevación de privilegios más allá de un solo servidor.</td>
<td style="border:1px solid black;">Bajo</td>
</tr>
</tbody>
</table>
  
Los niveles de riesgo de los escenarios anteriores se pueden explicar mejor de la siguiente manera:
  
-   **Nivel de riesgo crítico**. Este riesgo pondría inmediatamente en peligro la seguridad de toda la red y la empresa.
  
-   **Nivel de riesgo alto**. Este riesgo puede poner en peligro la seguridad de toda la red, pero no de forma tan inmediata como un riesgo crítico.
  
-   **Nivel de riesgo medio**. Este riesgo se debe estudiar con atención, ya que podría afectar a varios servidores, pero no hace que un servidor crítico sea vulnerable.
  
-   **Nivel de riesgo bajo**. Este riesgo podría poner en peligro a un solo servidor pero no a los servidores críticos.
  
#### Cuentas del sistema
  
Los servicios necesitan cuentas para tener acceso a los recursos y objetos que administra el sistema operativo en el que se ejecutan. Si la cuenta que usa un servicio no tiene suficientes privilegios para iniciar sesión, el complemento de servicios Microsoft Management Console (MMC) otorgará automáticamente a dicha cuenta el derecho de usuario “Iniciar sesión como servicio” necesario para el equipo que se está administrando.
  
Windows Server 2003 incorpora las tres cuentas locales siguientes que se usan como cuentas de inicio de sesión para distintos servicios del sistema:
  
-   **Sistema local**. La cuenta del sistema local, que aparece como DOMAIN*\\&lt;nombre del equipo&gt;*$ en la red y como NT AUTHORITY\\System localmente, es una cuenta local predefinida que puede iniciar servicios y proporcionar el contexto de seguridad para dicho servicio. Esta cuenta de numerosos privilegios permite el acceso completo al equipo local, incluidos los servicios de directorio cuando se usan en controladores de dominio. Si bien algunos servicios se configuran para usar esta cuenta de manera predeterminada en Windows Server 2003, no se debe utilizar con otros fines, ya que supone un riesgo evidente para la seguridad, especialmente en los controladores de dominio.
  
-   **Servicio local**. La cuenta de servicio local (NT AUTHORITY\\LocalService) es una cuenta integrada con privilegios reducidos similar a una cuenta de usuario local autenticada.. Este acceso reducido sirve de protección en caso de que se ponga en peligro un servicio o proceso que lo usa. Los servicios que se ejecutan como cuenta de servicio local tienen acceso a los recursos de red como sesión nula; es decir, usan credenciales anónimas.
  
-   **Servicio de red**. La cuenta de servicio de red (NT AUTHORITY\\NetworkService) es una cuenta integrada que también tiene privilegios reducidos similares a los de la cuenta de servicios locales. Sin embargo, en lugar de usar credenciales anónimas, los servicios y procesos que utilizan esta cuenta tienen acceso a los recursos de la red mediante las credenciales de la cuenta del equipo.
  
**Nota**   El cambio de la configuración predeterminada de servicios puede hacer que los servicios clave no se ejecuten correctamente. Se debe tener precaución al cambiar los valores **Tipo de inicio** e **Iniciar sesión como** de los servicios configurados para iniciarse automáticamente de manera predeterminada.
  
#### Configuración de seguridad predeterminada para los servicios de Windows Server 2003
  
Antes de Windows XP y de Windows Server 2003, casi todos los servicios que creaba el sistema operativo usaban la cuenta del sistema local de manera predeterminada. Esta funcionalidad provocó evidentes riesgos para la seguridad, ya que a dichos servicios se les otorgaban derechos ilimitados para el equipo local. La configuración predeterminada cambió con el desarrollo de Windows Server 2003 para mejorar la seguridad inherente del sistema operativo. Como resultado, muchos de estos servicios usan ahora, de manera predeterminada, las cuentas de servicio local o de servicio de red, lo que implica un perfil de vulnerabilidad menor.
  
Aún existen algunos servicios en los que se debe usar la cuenta del sistema local, incluidos: Actualizaciones automáticas, Examinador de equipos, Messenger y el servicio Windows Installer. No se deben cambiar los servicios que aún usan la cuenta del sistema local para la autenticación por otras cuentas, ya que se podrían provocar graves problemas y se podría hacer que dichos servicios no se ejecutaran correctamente.
  
La siguiente tabla enumera las cuentas de servicio que ya no usan la cuenta del sistema local en Windows Server 2003, junto con el tipo de cuenta que usan ahora:
  
**Tabla 3. Nueva configuración de cuentas de servicio de Windows Server 2003**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Servicio</th>
<th>Iniciar sesión como</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicio de alerta</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio de puerta de enlace de capa de aplicación</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registro remoto</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tarjeta inteligente</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Telnet</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sistema de alimentación ininterrumpida</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente Web</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Digitalización de imágenes de Windows</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Horario de Windows</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio de Descubrimiento automático de proxy Web WinHTTP</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Coordinador de transacciones distribuidas</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente DNS</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registro de licencias</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Registro de rendimiento</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ubicador de llamadas a procedimiento remoto (RPC)</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
</tbody>
</table>
  
#### Desarrollo
  
Para desarrollar un plan que proteja las cuentas administrativas y sensibles, es importante comprender los elementos fundamentales en los que se deben basar las prácticas recomendadas. Cualquier paso que se realice para proteger las cuentas y servicios conlleva los mismos principios básicos, que también forman parte de los procesos y procedimientos de todas las prácticas recomendadas. Esta sección repasará estos principios y consideraciones clave.
  
##### Administración de cuentas de administrador y críticas
  
Las pautas de prácticas recomendadas para proteger las cuentas administrativas de Windows Server 2003 se basan en la aplicación de los principios del privilegio mínimo y el uso de un método de cuenta de usuario estándar. El primer paso de este proceso consiste en contar con un amplio conocimiento del entorno actual. Los tres aspectos fundamentales siguientes son claves para desarrollar un plan efectivo para mejorar la seguridad de las cuentas de administrador y críticas:
  
-   Conocer y documentar el entorno
  
-   Usar el principio del privilegio mínimo
  
-   Usar el método de cuenta de usuario de privilegio mínimo
  
##### Conocer y documentar el entorno
  
Aunque pueda parecer obvio, este primer paso, que es el más importante, para lograr una mejora en la seguridad con respecto a las cuentas equivalentes a las de administrador puede resultar muchas veces el más difícil del proceso. Si una empresa no restringe y documenta el uso de los privilegios de nivel de administrador, puede resultar muy difícil determinar dónde se aplican dichos privilegios, especialmente en lo que se refiere a cuentas locales.
  
En cuanto a las cuentas de nivel de administrador y otras cuentas sensibles, el conocer y documentar un entorno de red conllevar contar con información sobre quién, por qué, qué y dónde. Es decir, *quién* tiene autorización para usar las cuentas administrativas, *por qué* esas personas tienen acceso a las cuentas administrativas, *qué* tareas son adecuadas para el uso de credenciales administrativas y *dónde* es seguro usar esas credenciales.
  
El aspecto más significativo de documentar esta información es establecer procesos y procedimientos que auditen dónde se usan las cuentas administrativas, por qué se usan, quién las usa y qué acciones se realizaron mientras estaban en uso. El mejor método para registrar esta información es el proactivo, mediante procesos de abastecimiento, control de cambios y administración de incidentes que exigen que cualquier actividad se autorice y registre antes de realizarse una tarea. Dichos procesos permiten una auditoría exhaustiva del uso de los privilegios administrativos, lo cual facilita mucho, a su vez, la detección de actividades sospechosas.
  
Como se verá posteriormente en este documento, conocer y documentar un entorno de red es el paso más significativo hacia la mejora de la seguridad de las cuentas críticas. El establecimiento de procesos y procedimientos de prácticas recomendadas para el uso y la emisión de cuentas sensibles forma una parte fundamental de este proceso y se debe producir antes de que se implemente cualquier otra pauta de este documento.
  
##### Usar el principio del privilegio mínimo
  
Seguir el principio del privilegio mínimo es probablemente uno de los pasos más significativos que una empresa puede realizar para mejorar la seguridad de su entorno de red. Si bien el otorgar privilegios de nivel administrativo suele ser la forma más fácil y rápida de resolver problemas relacionados con derechos y privilegios complejos, también es la más arriesgada. Asimismo, si bien es mucho más fácil para los administradores del sistema usar una cuenta con privilegios de nivel de administrador en todo momento, dichas prácticas también aumentan el perfil de riesgo de la red de la que son responsables.
  
La aplicación más básica de este principio es la siguiente; el uso de los privilegios de nivel de administrador debe quedar restringido al personal autorizado sólo cuando la tarea en cuestión necesite la capacidad inherente de dichos privilegios elevados. Si bien puede parecer una tarea pesada el implementar prácticas que incorporen este concepto, el nivel de exposición que una empresa acepta al no ajustarse a este principio es demasiado importante como para no ser tenido en cuenta.
  
El nivel de exposición a las vulnerabilidades más habituales a las que pueden hacer frente las redes se reduce al aplicar este principio. Entre los ejemplos de estas vulnerabilidades se incluyen los siguientes:
  
-   Rootkits de modo de núcleo
  
-   Programas de registro de pulsaciones a nivel del sistema
  
-   Intentos de intercepción de contraseñas
  
-   Incidentes de software espía y adware
  
-   Acceso no autorizado a los datos
  
-   Instalaciones de troyanos
  
-   Manipulación del registro de sucesos
  
Cuando se reduce el uso de cuentas de nivel administrativo, también se reduce la capacidad de usar los privilegios elevados inherentes a dichas cuentas para la actividad malintencionada, por lo que mejora el perfil de seguridad de la red. Asimismo, al eliminar la capacidad para realizar cambios importantes en el sistema operativo, también se reduce la capacidad del malware y software espía de instalarse y ejecutarse. Por estos motivos, la aplicación del principio del privilegio mínimo puede tener un efecto muy importante en la seguridad de la red.
  
##### Usar el método de cuenta de usuario de privilegio mínimo
  
A los usuarios se les suele otorgar privilegios administrativos para sus propios equipos en muchos entornos empresariales, especialmente en el caso de equipos portátiles. Si bien pueden existir algunos motivos válidos para otorgar estos amplios privilegios, esta actitud puede exponer a la empresa a niveles de riesgo mayores.
  
El uso del método de la cuenta de usuario de privilegio mínimo (LUA) combina sugerencias de prácticas recomendadas que permiten a las empresas usar cuentas no administrativas para usar equipos basados en Windows XP. El resultado de estas prácticas es una aplicación práctica del principio del privilegio mínimo, según se aplica en los dispositivos clientes de Windows XP.
  
Debido a que este documento examina el problema de las cuentas administrativas desde un alto nivel y presta especial atención a los privilegios de nivel de red, también resulta importante tener en cuenta las ramificaciones de las cuentas de usuario local en las estaciones de trabajo. Si bien este tipo de método particular no es el objeto de este documento, podrá encontrar información más detallada de LUA en el sitio web de Microsoft. Para obtener más información, consulte el documento sobre [Aplicación del principio de privilegio mínimo para cuentas de usuarios en Windows XP](http://go.microsoft.com/fwlink/?linkid=58445) en http://go.microsoft.com/fwlink/?LinkId=58445 o el artículo "[Uso de una cuenta de usuario de privilegio mínimo](http://www.microsoft.com/technet/security/secnews/articles/lpuseacc.mspx)" (en inglés) en www.microsoft.com/technet/security/secnews/articles/lpuseacc.mspx.
  
##### Administración de cuentas de servicio
  
Al igual que sucede con la administración de cuentas de administrador y críticas, existen tres aspectos fundamentales clave para establecer un plan que consiga aumentar la seguridad de los servicios en un entorno de mediana empresa. Es importante tratar los tres aspectos siguientes durante las fases de desarrollo e incorporarlos en los procedimientos de las directivas de seguridad:
  
-   Conocer y documentar el entorno
  
-   Usar el principio del privilegio mínimo
  
-   Usar el principio del servicio mínimo
  
##### Conocer y documentar el entorno
  
Este paso recomendado puede parecer obvio, pero muchas empresas no son plenamente conscientes de todas las funciones y servicios que existen en su entorno de red. Esta falta de conocimientos y documentación puede estar causada por muchos motivos, pero suele basarse en el rápido crecimiento de los entornos de red y la falta de tiempo y recursos para prestar la atención necesaria a la necesidad de documentación.
  
Para comprender si los equipos son seguros, es necesario conocer qué servicios se ejecutan en dichos equipos y qué pueden conllevar sus propiedades. Esta información es fundamental para proteger los servidores y sus servicios, junto con las cuentas que pueden necesitar dichos servicios. Para esta tarea, suele resultar útil crear una tabla de servicios, propiedades de servicios y los equipos en los que se usan esos servicios. Aunque la creación de esa tabla pueda suponer una tarea desalentadora, los resultados merecen la pena. Asimismo, resulta relativamente fácil mantener actualizada la tabla tras su creación e integrarla en el proceso de implementación de aplicaciones y de creación de servidores.
  
Hay varias herramientas que pueden ayudarle a documentar los servicios y sus propiedades en la red. Algunas de estas herramientas incluyen:
  
-   **Herramienta Controlador de servicio (sc.exe)**. Esta utilidad de la línea de comandos está incluida en Windows Server 2003 y Windows XP. Permite comunicarse fácilmente con el componente Administrador de control de servicios de una línea de comandos para consultar y establecer las propiedades de los servicios.
  
-   **Herramienta Lista de controlador de servicio (sclist.exe)**. El Kit de recursos de Windows 2000 Server incluye una herramienta que puede enumerar los servicios en ejecución y detenidos en equipos locales o remotos. Sclist.exe se puede usar para identificar recursos que se ejecutan en servidores remotos y que no tienen monitores o que se encuentran separados físicamente del administrador.
  
-   **Instrumental de administración de Windows (WMI)**. Este componente se incluye en Windows Server 2003 y Windows XP y proporciona información de administración y control en entornos empresariales. Los administradores pueden usar WMI para consultar y establecer información en equipos, redes, aplicaciones y servicios. Además de permitir el uso de scripts para la gestión de tareas administrativas, WMI permite a los administradores identificar las dependencias de servicios, así como cualquier servicio del que dependan esos servicios.
  
-   **Línea de comandos de Instrumental de administración de Windows (WMIC)**. WMI también incluye una herramienta de la línea de comandos, WMIC, que ofrece una sencilla interfaz de la línea de comandos para WMI con el fin de administrar los equipos remotos y las consultas. Los resultados de las consultas realizadas con WMIC se pueden consultar fácilmente con un explorador, como Internet Explorer, ya que su formato es de tablas HTML.
  
##### Seguir el principio del privilegio mínimo
  
Microsoft comprende la importancia de la seguridad y cómo el principio del privilegio mínimo desempeña una función significativa en la protección de los entornos de red. Microsoft aplicó este principio en el desarrollo de Windows Server 2003 para asegurarse de que los servicios clave del sistema operativo usen la cuenta del privilegio mínimo y, por lo tanto, no es necesario realizar ninguna configuración adicional en estos servicios. Este método se debe centrar en proteger los servicios que no forman parte del sistema operativo, como los que ofrecen otros productos como Microsoft SQL Server, Microsoft Operations Manager, o bien otros productos de software de terceros.
  
Por consiguiente, el principio del privilegio mínimo se debe usar al ejecutar también cualquier otro servicio, incluso aunque en ocasiones resulte más fácil simplemente otorgar un nivel superior de privilegios a la hora de implementar nuevos productos. Por ejemplo, los servicios deben usar la cuenta del servicio local siempre que sea posible para limitar la posibilidad de que un ataque tenga éxito al equipo local y no a todo el dominio. Los servicios que necesitan un acceso autenticado a la red deben usar la cuenta del servicio de red siempre que sea posible. Los servicios que necesitan amplios privilegios deben usar la cuenta del sistema local. Por último, si un servicio necesita el uso de una cuenta de administrador de nivel de dominio, el servidor o servidores en el que se ejecuta ese servicio se deben considerar como sistemas de alta seguridad que se protegen de la misma manera que otros recursos de red y controladores de dominio críticos o sensibles.
  
También se puede usar la directiva de grupo para controlar servicios específicos que se puedan ejecutar en los equipos. Se pueden controlar varias propiedades mediante **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Servicios del sistema** y abriendo la página **Propiedades** de ese servicio. Se pueden modificar valores como el modo de inicio y los permisos para los que se pueden usar las cuentas a la hora de realizar operaciones concretas en dicho servicio (por ejemplo, iniciarlo o detenerlo).
  
La implementación del privilegio del privilegio mínimo depende del nivel de conocimiento que tengamos de los sistemas del entorno. Al combinar estos dos conceptos básicos, se puede evaluar qué servicios se están ejecutando en los equipos, así como las credenciales que se están usando para cada servicio y servidor. Sólo entonces se podrá reducir de forma efectiva y metódica cada servicio para que use los privilegios mínimos necesarios para su funcionalidad continuada mediante los procesos correctos de control de cambios, que también facilitan la documentación continuada del entorno.
  
##### Seguir el principio del servicio mínimo
  
Por último, el principio del servicio mínimo indica que el sistema operativo y los protocolos de red disponibles en cualquier recurso de red deben ejecutar sólo los servicios y protocolos exactos necesarios para que funcione la empresa. Por ejemplo, si un servidor no es necesario para alojar alguna aplicación web, el servicio World Wide Web se debe deshabilitar o eliminar.
  
La mayoría de los sistemas operativos y programas instalan muchos más servicios y protocolos en una configuración predeterminada de los que realmente se necesitan para los escenarios de uso habitual. Por lo tanto, se debe realizar un proceso de instalación personalizada siempre que sea posible para controlar los servicios y protocolos habilitados o instalados durante un proceso de aplicación. Este método permite documentar los procesos que se crean durante la instalación en caso de que, posteriormente, se determine que un servicio creado durante la instalación ya no se necesita.
  
Al implementar nuevos servidores o desarrollar imágenes del servidor, se recomienda incluir pasos en los que el administrador del sistema cierre todos los servicios, excepto los esenciales para el sistema operativo. Los servicios deshabilitados se podrá habilitar posteriormente según sea necesario para cualquier aplicación que deba ejecutar ese servidor. Por ejemplo, era habitual deshabilitar los servicios de Alerta y Messenger en los sistemas operativos Windows antes de Windows Server 2003, porque dichos servicios no se solían necesitar. Al deshabilitarlos, aumenta el perfil de seguridad del servidor que se implementa sin que esto afecte a la funcionalidad.
  
Garantizar una colocación adecuada de los servicios también es una parte importante de este principio. Por ejemplo, el servicio Enrutamiento y acceso remoto o el servicio de Internet Information Server nunca se deben colocar en controladores de dominio, porque estos servicios de segundo plano aumentan el perfil de vulnerabilidad en los controladores de dominio. Una vez puesto en peligro, un controlador de dominio puede otorgar acceso ilimitado al resto del dominio. Por lo tanto, las prácticas recomendadas de Microsoft sugieren que no se implemente en un controlador de dominio ningún servicio adicional que no sea absolutamente necesario para que un controlador de dominio funcione correctamente.
  
#### Implementación y administración
  
Después de tratar las consideraciones clave y los principios básicos, se deben tener en cuenta una serie de recomendaciones específicas basadas en estos conceptos. Realizar cualquiera de estas acciones individuales puede mejorar la seguridad de una red empresarial pero, si se combinan, formarán parte de un marco de seguridad global que puede reducir en gran medida la vulnerabilidad de la red de una mediana empresa.
  
##### Administración de cuentas de administrador y críticas
  
Se puede implementar una serie de métodos de prácticas recomendadas para proteger las cuentas administrativas en una red de Microsoft Windows. Se probaron los siguientes métodos para ayudar a reducir la vulnerabilidad asociada a dichas cuentas; estos métodos se suelen usar en las redes de medianas empresas.
  
##### Separación de las funciones de administrador de empresa y de dominio
  
La función de administrador de empresa es la más amplia en un bosque de Active Directory. Se deben realizar pasos que aseguren la protección de este tipo de cuenta y su uso se debe regular con cuidado. Hay dos métodos que permiten administrar este tipo de cuenta:
  
-   **Cuenta única controlada**. El primer método consiste en limitar esta función a una sola cuenta que se supervisa y controla de forma detallada para asegurarse de que su uso sólo coincide con solicitudes de control de cambios autorizadas para tareas en las que se debe usar. Cualquier suceso supervisado que se produzca en el nombre de esta cuenta se debe investigar de forma inmediata y debe estar acompañado por algún tipo de suceso de solicitud de cambio autorizado.
  
-   **Cuenta temporal**. Otro método sería no configurar nunca una cuenta de este tipo hasta que fuera necesario realizar una tarea autorizada. Cuando se deba autorizar, se podría crear una cuenta temporal, usarse para realizar la tarea y, a continuación, eliminarse. Como es poco habitual que se necesite una cuenta con estos elevados privilegios, dichos pasos no deberían suponer un esfuerzo adicional muy significativo para el trabajo administrativo.
  
##### Separación de las cuentas de usuario y de administrador
  
Las cuentas se suelen asociar a los usuarios. Cuando se usa el principio del privilegio mínimo, las cuentas se pueden asociar con tareas en lugar de sólo con funciones, especialmente cuando se tienen en cuenta las funciones administrativas. Para cada persona que realiza una función de administrador debería haber dos cuentas: una para el uso diario que es una cuenta de usuario normal y otra con privilegios administrativos que sólo se debe usar al realizar tareas administrativas en una estación de trabajo administrativa.
  
Las cuentas administrativas deben limitarse a las tareas y las estaciones de trabajo administrativas que formen parte de una red de confianza similar a los controladores de dominio. Las cuentas administrativas y sus estaciones de trabajo asociadas no deben tener acceso al correo electrónico ni a Internet y no se debe iniciar sesión con ellas cuando no estén utilizándose. Los administradores deben tener distintas contraseñas para sus cuentas de uso estándar y las cuentas de administrador; además, la seguridad de las contraseñas de administrador debe ser la más alta posible de la red.
  
Estas sencillas precauciones reducen significativamente la exposición de vulnerabilidad que dichas cuentas tienen al reducir su exposición al mundo exterior y limitar la cantidad de tiempo que se usan.
  
##### Uso del servicio Inicio de sesión secundario
  
Se pueden ejecutar programas con una cuenta que no sea la cuenta con la que se inició sesión actualmente o al usar el servicio Ejecutar como de Microsoft Windows 2000. Con Windows Server 2003 y Windows XP Professional esta misma funcionalidad recibió el nombre de servicio Inicio de sesión secundario.
  
Este último servicio permite a los administradores iniciar sesión en un equipo con una cuenta que no sea administrativa y realizar tareas administrativas ejecutando tareas administrativas de confianza con credenciales de administrador sin tener que cerrar la sesión. Esta funcionalidad reduce el riesgo asociado con el uso de credenciales de administrador, al emplearse una forma del concepto de separación de las cuentas de usuario y de administrador mencionado anteriormente.
  
##### Ejecución de sesiones de Terminal Services distintas para la administración
  
Las conexiones de Terminal Services y de Remote Desktop se suelen usar para administrar servidores sin tener que obtener acceso físico a la consola del servidor. Este método no sólo es eficiente sino que también es más seguro que usar una cuenta de administrador para iniciar sesión de forma interactiva en el servidor, especialmente cuando no se utiliza una cuenta de nivel de administrador en el equipo desde el que se estableció la conexión. Cuando se realiza una tarea administrativa, se debe cerrar la sesión de la cuenta de administrador y desconectarse la sesión.
  
##### Cambio de nombre de las cuentas de administrador predeterminadas
  
El cambio de nombre de la cuenta de administrador predeterminada sigue siendo una práctica habitual en muchas medianas empresas y ayuda, en cierta medida, a reducir el perfil de vulnerabilidad de dicha cuenta. Sin embargo, este método sólo obstaculiza unos cuantos tipos de ataque, ya que hay muchas herramientas y técnicas que pueden ayudar a los atacantes a determinar cuál es la cuenta de administrador integrada. Si bien el cambio de nombre de la cuenta predeterminada puede ser útil en cierta medida, realmente es más eficaz crear cuentas de administrador secundarias y, a continuación, deshabilitar las cuentas integradas originales, como se describe posteriormente en este documento.
  
##### Creación de cuentas de administrador de señuelo
  
Cuando se usan junto con un mecanismo de defensa frente a intrusiones que pueda detectar y enviar alertas sobre una actividad concreta en una cuenta, el uso de este tipo de cuentas puede actuar como un efectivo nivel de defensa adicional frente a los intentos de ataques en una red. Incluso por sí sola, esta técnica puede reducir algunos ataques si se otorgan más intentos de bloqueo de cuentas que en el caso de las cuentas físicas y determinadas contraseñas seguras. Las cuentas de administrador de señuelo no deben ser miembros de ningún grupo de seguridad con privilegios y se deben supervisar para detectar cualquier actividad sospechosa. Cualquier intento de uso de dicha cuenta debe desencadenar una investigación inmediata.
  
##### Creación de cuentas de administrador secundarias y deshabilitación de cuentas integradas
  
Incluso si a cada persona de una función administrativa no se le concede una cuenta equivalente a la de administrador única para usarla al realizar tareas administrativas (e incluso si no se usa Terminal Services para administrar el servidor), este método seguirá siendo mejor que crear una cuenta de administrador secundaria. La cuenta de administrador secundaria actúa como un mecanismo de seguridad frente a una cuenta de administrador principal en peligro y se debe crear antes de deshabilitar la cuenta de administrador integrada.
  
**Nota**    Es importante asegurarse de que se cree otra cuenta con los privilegios de administrador adecuados antes de deshabilitar la cuenta de administrador integrada. Si se deshabilita esa cuenta sin asegurarse de que exista otra cuenta equivalente, podría perderse el control administrativo sobre el dominio, con lo que tal vez haya que restaurar el sistema o reinstalarlo para corregir el problema.
  
##### Habilitación del bloqueo de cuentas para los inicios de sesión de administrador remoto
  
Si bien no se puede bloquear la cuenta de administrador integrada, se pueden bloquear los inicios de sesión remotos que usen la cuenta de administrador. Para realizar esta tarea, el Kit de recursos de Microsoft Windows 2000 Server contiene un programa de la línea de comandos denominado Passprop.exe que puede habilitar el bloqueo de cuentas para los inicios de sesión remotos. Cuando se usa esta herramienta de la línea de comandos con el parámetro /ADMINLOCKOUT, hace que el uso del inicio de sesión interactivo y remoto de la cuenta de administrador quede sujeto a las directivas de bloqueo existentes en Windows 2000 Server.
  
**Nota**    El uso de Passprop.exe /ADMINLOCKOUT en Windows Server 2003 afectará al uso del inicio de sesión remoto e interactivo de la cuenta de administrador. Se debe tener cuidado con esta funcionalidad, ya que no se podrá usar la cuenta de administrador para la administración del servidor mientras se encuentre bloqueada.
  
##### Creación de contraseñas de administrador seguras
  
Otra práctica recomendada consiste en el uso de una contraseña segura para cualquier cuenta equivalente a la de administrador, así como para las cuentas de administrador integradas. Las contraseñas seguras reducen la probabilidad de que un atacante que utiliza la fuerza bruta adquiera más privilegios. Las contraseñas seguras suelen estar constituidas por los siguientes elementos:
  
-   15 o más caracteres
  
-   Nunca contienen ninguna forma de nombres de cuentas, nombres reales o nombres de compañía.
  
-   Nunca contienen una palabra completa, jerga u otro término que se pueda buscar fácilmente.
  
-   Son considerablemente diferentes en contenido a contraseñas anteriores y no están incrementadas.
  
-   Utilizan por lo menos tres de los siguientes tipos de caracteres:
  
    -   Mayúsculas (A, B, C...)
  
    -   Minúsculas (a, b, c...)
  
    -   Números (0, 1, 2...)
  
    -   Símbolos no alfanuméricos (@, &, $...)
  
    -   Caracteres Unicode (€, ƒ, ?...)
  
##### Detección automática de contraseñas poco seguras
  
Hay dos métodos básicos que usan las herramientas de detección de contraseñas al comprobar el uso de contraseñas poco seguras o en blanco. Estos métodos son:
  
-   **Detección de contraseñas en línea**. Esta detección incluye varios intentos para iniciar sesión mediante defectos habituales de las contraseñas, como el uso de la palabra “contraseña” como contraseña o incluso el uso de contraseñas en blanco. Microsoft Baseline Security Analyzer (MBSA) es un ejemplo de herramienta que usa este método.
  
-   **Detección de contraseñas sin conexión**. Esta detección incluye varios mecanismos que usan las credenciales en caché para probar, e incluso clasificar, la seguridad de la contraseñas de distintas cuentas. Las herramientas que usan este método tienen algunas ventajas con respecto al método anterior, pero implican el uso de software de terceros.
  
Si bien hay herramientas de terceros para detectar contraseñas poco seguras, Microsoft permite descargar de forma gratuita Microsoft Baseline Security Analyzer (MBSA). MBSA puede notificar si se detecta cualquier cuenta bloqueada o deshabilitada mientras se enumeran todas las cuentas de usuario para buscar alguno de los siguientes defectos en las contraseñas:
  
-   Contraseñas en blanco
  
-   Uso de nombres de usuario en las contraseñas
  
-   Uso de nombres de equipo en las contraseñas
  
-   Uso de las palabras “contraseña”, “admin” o “administrador” en las contraseñas
  
Para obtener más información, consulte la página web de [Microsoft Baseline Security Analyzer](http://www.microsoft.com/technet/security/tools/mbsahome.mspx) (en inglés) en www.microsoft.com/technet/security/tools/mbsahome.mspx.
  
##### Restricción de tareas administrativas a equipos de confianza
  
Las credenciales de administrador suelen ser un objetivo muy tentador para los posibles intrusos y los métodos usados para obtener acceso a ellas pueden ser difíciles de detectar. Los programas de registro de pulsaciones y los de captura de pantalla son algunas de las herramientas que se suelen usar para conseguir esta valiosa información al capturar cada pulsación realizada y cada carácter escrito en un equipo puesto en peligro. Estas formas de malware pueden ser muy sigilosas y difíciles de detectar, por no hablar de lo difícil que resulta eliminarlas una vez instaladas en un equipo.
  
Por lo tanto, se recomienda garantizar que las cuentas equivalentes a las de administrador se limiten al uso del menor número de equipos posible para reducir la vulnerabilidad ante dichas amenazas. Asimismo, al limitar los recursos en los que se deben usar las cuentas administrativas, es importante garantizar que dichos sistemas sean de confianza y cuenten con una protección adecuada. Hay disponibles muchas técnicas que permiten proteger activos sensibles, como el aislamiento de redes mediante IPsec, que aplica una mayor seguridad a determinados dispositivos, además de no afectar a la capacidad de uso de la propia red.
  
Para obtener más información sobre el uso de IPsec para aislar dominios y servidores, consulte el centro de tecnología sobre [aislamiento de dominios y servidores](http://www.microsoft.com/technet/itsolutions/network/sdiso/default.mspx) (en inglés) en www.microsoft.com/technet/itsolutions/network/sdiso/default.mspx.
  
##### Auditoría de cuentas y contraseñas
  
La auditoría habitual de las cuentas ayuda a garantizar la integridad de la seguridad de un dominio frente a ataques que implican la elevación de privilegios. Si los atacantes obtienen acceso a una cuenta de nivel administrativo, pueden agregar vulnerabilidades y eludir las medidas de seguridad. Por ejemplo, los atacantes que obtengan acceso a una cuenta equivalente a la de un administrador pueden crear cuentas de usuario proxy, cambiar los miembros de las cuentas e incluso modificar los registros de sucesos para ocultar sus pistas.
  
Todos los usuarios y grupos administrativos de nivel de dominio, así como las cuentas y grupos de administrador locales de servidores sensibles se deben auditar de forma regular. Se debe auditar el uso de estas credenciales administrativas para garantizar que sólo se usan según las pautas establecidas por las directivas internas y de acuerdo con cualquier proceso interno establecido y bien documentado, como los procedimientos de control de cambios. El uso de auditorías de cuentas regulares garantiza que se sigan los procedimientos adecuados en el desarrollo de las tareas administrativas e incluso se comprueben que se cumplen las directivas sobre la seguridad de las contraseñas.
  
El Visor de sucesos puede ser una herramienta útil en el proceso de auditoría si se realizan los pasos necesarios para proteger los registros de sucesos de las alteraciones. Para obtener información sobre el uso de registros de sucesos para supervisar la seguridad de la red y sobre cómo proteger los datos del registro de sucesos, consulte la [*Guía de planificación de la detección de ataques y supervisión de la seguridad*](http://go.microsoft.com/fwlink/?linkid=41309) (en inglés) en http://go.microsoft.com/fwlink/?LinkId=41309.
  
##### Prohibición de la delegación de cuentas
  
La autenticación delegada se produce cuando un servicio de red acepta una solicitud de un usuario y asume la identidad de ese usuario para iniciar una nueva conexión a otros servicios de red. La autenticación delegada tiene varias aplicaciones útiles para aplicaciones de varios niveles que usan la función de inicio de sesión único en la red. Microsoft Outlook Web Access (OWA) usa este mecanismo para ofrecer una interfaz con bases de datos en otros equipos.
  
Las cuentas de administrador se deben designar como "La cuenta es importante y no se puede delegar". Este método ayuda a proteger las credenciales equivalentes a las de un administrador de la suplantación mediante servidores marcados como de confianza para la delegación. A las cuentas de equipos de Active Directory que se correspondan con equipos que no tengan una protección física se les debe denegar el derecho a participar en una autenticación delegada. Además, a las cuentas de administrador de dominio se les debe denegar el derecho a participar en una autenticación delegada porque tienen acceso a información y recursos sensibles de la red.
  
Para obtener más información sobre la delegación de cuentas, consulte la página [Habilitación de la autenticación delegada](http://technet2.microsoft.com/windowsserver/en/library/72612d01-622c-46b7-ab4a-69955d0687c81033.mspx?mfr=true) (en inglés) en http://technet2.microsoft.com/WindowsServer/en/Library/72612d01-622c-46b7-ab4a-69955d0687c81033.mspx?mfr=true.
  
##### Autenticación de varias fases obligatoria para cuentas de administrador
  
Los grupos Administradores, Administradores de empresa y Administradores del dominio contienen las cuentas más amplias de la red de una empresa. Consecuentemente, estas cuentas también deben ser las que estén más protegidas.
  
Los métodos de autenticación de varias fases mejoran la seguridad del proceso de inicio de sesión al exigir información de identificación adicional a los usuarios autorizados, lo que aumenta la cantidad de información que un atacante necesita saber para poner en peligro la cuenta. Como indica el nombre, una autenticación en varias fases necesita varios elementos para identificar la información. Para este método se suele necesitar lo siguiente:
  
-   Algo que tiene el usuario, como una tarjeta inteligente.
  
-   Algo que el usuario conoce, como un número de identificación personal (NIP).
  
-   Algo que el usuario es (normalmente se conocen como indicadores biométricos). Puede ser tan sencillo como usar un escáner de huellas dactilares para la autenticación.
  
El uso de la autenticación de varias fases acaba con las vulnerabilidades asociadas a los métodos de autenticación basados en contraseñas o en nombres de usuario sin cifrar, ya que se usa una tarjeta inteligente que contiene un código generado aleatoriamente y que identifica al titular de la cuenta. Cada tarjeta contiene una clave privada única que garantiza la singularidad de la información de autenticación.
  
Es más, el uso de una tarjeta inteligente exige la utilización de un NIP correspondiente, que es otro código cifrado que establece el propietario de la tarjeta y que, a continuación, se almacena en la misma. Este NIP permite el uso de la clave privada que contiene la tarjeta durante la autenticación; de lo contrario, la clave permanece cifrada y no se puede usar.
  
Para obtener más información sobre los métodos de autenticación de varias fases y las tarjetas inteligentes, consulte la [*Guía de planificación de acceso seguro mediante tarjetas inteligentes*](http://go.microsoft.com/fwlink/?linkid=41313) (en inglés) en http://go.microsoft.com/fwlink/?LinkID=41313.
  
#### Administración de cuentas de servicio y de aplicación
  
Existen también una serie de métodos basados en prácticas recomendadas que pueden aumentar la seguridad de los servicios y las cuentas de servicio. Esta sección describirá los métodos que demostraron que mejoran la seguridad de los servicios en entornos de red del mundo real. Si bien el uso de todos estos métodos combinados puede mejorar en gran medida la seguridad de las redes de las medianas empresas, es mejor evaluar cada uno de ellos por separado para determinar la combinación de métodos más adecuada para cada entorno empresarial concreto.
  
##### Auditoría de servicios para detectar propiedades esenciales
  
Como se mencionó anteriormente, el primer paso a la hora de desarrollar un plan para proteger los servicios de un entorno determinado consiste en tener un amplio conocimiento de estos servicios, dónde se producen y por qué se usan. Si bien eso parece una tarea sin mayores complicaciones, puede ser increíblemente difícil identificar los servicios que se ejecutan en cada equipo, así como el grado de administración necesario de dichos servicios.
  
Se debe auditar y documentar cada servidor de un entorno para determinar todos los servicios que se están ejecutando en él, así como las credenciales de inicio de sesión que usa cada servicio para la autenticación. Hay una serie de herramientas disponibles que ayudan a los administradores a realizar esta tarea, entre ellas:
  
-   **Información del sistema en Microsoft Windows Server 2003**. La información del sistema puede proporcionar una lista completa de propiedades para todos los servicios que se ejecutan en un equipo local. Sin embargo, esta herramienta no ofrece un método muy efectivo para auditar una gran cantidad de servidores.
  
-   **Consola de administración de servicios**. En la consola de administración de servicios, se puede usar la ficha **Iniciar sesión** de la página **Propiedades** de un servicio para determinar qué cuenta usa un servicio para la autenticación. También se puede usar la ficha **Dependencias** para determinar de qué servicios depende ese servicio y qué servicios dependen del servicio que se está viendo. Desgraciadamente, este método no es tampoco efectivo para auditar una gran cantidad de servidores.
  
-   **Instrumental de administración de Windows (WMI**). WMI se puede usar para obtener información sobre los servicios que se ejecutan en todos los servidores de una red. Si se usa con scripts u otras herramientas de programación, WMI puede servir para obtener detalles de configuración sobre la mayoría de los aspectos de los equipos de una red, así como para realizar cambios en otros equipos.
  
-   **Línea de comandos de Instrumental de administración de Windows (WMIC)**. WMIC proporciona la misma funcionalidad que WMI como herramienta de la línea de comandos que se puede usar conjuntamente con los shells existentes y con otros comandos de utilidades que se pueden ampliar con scripts u otras aplicaciones.
  
    Con el servicio WMIC, se puede obtener distinta información sobre los servicios que se ejecutan en una red, entre ellos:
  
    -   Descripción
  
    -   DisplayName
  
    -   ErrorControl
  
    -   InstallDate
  
    -   PathName
  
    -   ProcessId
  
    -   StartMode
  
    -   StartName
  
    -   Estado
  
    -   Scripts
  
        Como se mencionó anteriormente, se puede aprovechar WMIC para automatizar la administración de los equipos locales y remotos mediante el uso de scripts.
  
-   **Otras herramientas de administración empresarial**. Existe otra serie de herramientas de administración que se pueden usar para facilitar la auditoría de los servicios del servidor, incluidos:
  
    -   Microsoft Systems Management Server (SMS)
  
    -   IBM Tivoli
  
    -   HP OpenView
  
    -   Service Account Manager de Lieberman Software
  
##### Determinación de los servicios necesarios
  
Windows Server 2003 crea varios servicios predeterminados cuando se instala por primera vez y configura esos servicios para que se ejecuten al iniciarse el equipo. Estos servicios predeterminados permiten la compatibilidad de las aplicaciones, la compatibilidad de los clientes o facilitan la administración de los sistemas. Sin embargo, no en todos los entornos es necesario usar todos estos servicios. Se deben examinar todos los servicios para determinar si se puede deshabilitar alguno de ellos, con lo que se puede reducir el perfil de vulnerabilidad del servidor en el que se ejecutan.
  
La definición de los servicios necesarios y de los que se pueden deshabilitar puede ser un proceso complicado. Algunos servicios tienen respuestas obvias, pero otros puede que no presenten esas opciones tan claras. A la hora de determinar los servicios que se pueden deshabilitar se pueden usar dos criterios principales:
  
-   Si no hay motivo para usar un servicio concreto, se puede deshabilitar.
  
-   Si es necesario volver a usar el servicio en el futuro, pero no actualmente, se puede deshabilitar hasta que sea necesario.
  
Los servicios necesarios en cualquier servidor concreto dependen fundamentalmente de la función de dicho servidor concreto. Por ejemplo, el servicio Internet Information Server (IIS) sólo se debe usar en un servidor Web o en un servidor de aplicaciones en el que se utilice el mecanismo de distribución basado en Web. Si dicho servidor no usa Telnet Services o los servicios de acceso remoto, se deben deshabilitar en él.
  
Cuando se instala software en un servidor, también puede tener su propio conjunto de servicios. Por ejemplo, Microsoft Systems Management Services instalará el servicio Agente de control remoto Wuser32 para ofrecer la funcionalidad de cliente de acceso remoto para las actualizaciones de software o la administración remota. Es importante saber los servicios que puede instalar o en los que se puede basar un paquete de software para conocer su funcionalidad a la hora de determinar los servicios que se deben deshabilitar.
  
##### Uso del Asistente para configuración de seguridad (SCW)
  
Este asistente, que se proporciona con Windows Server 2003 Service Pack 1 (SP1), se puede usar para configurar rápidamente los servidores según requisitos funcionales, como un servidor Web o un controlador de dominio, mientras que los administradores podrán seguir creando directivas de seguridad para minimizar las vulnerabilidades. SCW se puede usar para ayudar a detectar qué servicios se están ejecutando en servidores de la red y las dependencias que éstos tienen.
  
**Para instalar SCW en un servidor Windows Server 2003**
  
1.  Abra el Panel de control.
  
2.  Haga doble clic en **Agregar o quitar programas**.
  
3.  Haga clic en **Agregar o quitar componentes de Windows**.
  
4.  Active la casilla **Asistente para configuración de seguridad** en **Componentes** en la pantalla **Componentes de Windows**.
  
5.  Haga clic en **Siguiente**.
  
6.  Haga clic en **Finalizar** cuando termine el proceso de instalación.
  
Se puede usar SCW para reducir la superficie de ataque de los equipos que ejecutan Windows Server 2003 con SP1. El asistente guía a los administradores por el proceso de creación de directivas de seguridad según las funciones realizadas por cualquier servidor concreto. El término *función del servidor* define la función principal que realiza un equipo en una red; además, los servicios necesarios, los puertos entrantes y la configuración variará según la función que realice un servidor. Después de crear las directivas, se pueden aplicar a los servidores, según la configuración.
  
##### Eliminación del uso de cuentas de administrador de dominio para servicios
  
Cuando finaliza la auditoría de un servidor, debe haber suficiente información sobre el entorno para identificar y eliminar todos los casos posibles de cuentas de administrador de dominio que se usen para autenticar servicios. Siempre que sea posible, se deben volver a implementar servicios con las cuentas Servicio local, Servicio de red o Sistema local.
  
Los esfuerzos para usar correctamente las cuentas equivalentes a las de administrador se pueden destinar especialmente a las siguientes situaciones:
  
-   Las cuentas de usuario con privilegios equivalentes a los del administrador que inician sesión como servicio.
  
-   Las cuentas de administrador integradas que inician sesión como servicio.
  
-   Las cuentas de administrador de dominio que inician sesión como servicio en equipos con poca seguridad.
  
##### Uso de las jerarquías del privilegio mínimo para implementar servicios
  
Como se mencionó anteriormente en este documento, los servicios siempre deben usar la cuenta con los mínimos privilegios posibles necesarios para ejecutar dicho servicio. Cualquier servicio que cuente con un nivel mayor de privilegios que los necesarios se debe volver a implementar mediante cuentas con menos privilegios.
  
Una jerarquía de privilegio mínimo consideraría a las cuentas para el uso de servicios en el siguiente orden, desde la cuenta más recomendada a la menos recomendada:
  
-   Servicio local
  
-   Servicio de red
  
-   Cuenta de usuario local única
  
-   Cuenta de usuario de dominio única
  
-   Sistema local
  
-   Cuenta de administrador local
  
-   Cuenta de administrador de dominio
  
##### Creación de grupos de servidores de alta seguridad para las excepciones
  
Los servidores de alta seguridad son básicamente servidores que contienen recursos o que ofrecen servicios de los que depende la empresa o que representan un riesgo de seguridad elevado. Normalmente, los servidores que cumplen esos criterios incluyen:
  
-   Controladores de dominio.
  
-   Servidores que usan servicios que deben autenticarse con una cuenta de administrador de dominio para poderse ejecutar.
  
-   Servidores de confianza para la delegación en un bosque.
  
-   Servidores que usan grupos comerciales sensibles o que contienen información crítica de la empresa, como un servidor de recursos humanos con información salarial.
  
-   Servidores que ejecutan servicios en los que se puede confiar para la delegación en un bosque mediante la delegación limitada de Windows Server 2003.
  
La creación de un grupo de servidores de alta seguridad suele implicar las siguientes actividades:
  
1.  Identifique los servidores que se deben designar como servidores de alta seguridad.
  
2.  Cree un grupo de seguridad universal de alta seguridad en cada bosque.
  
3.  Coloque las cuentas de los equipos del servidor designado en los nuevos grupos universales.
  
4.  Cree un grupo local de cuentas de administración de dominios en cada dominio.
  
5.  Coloque todas las cuentas de usuario equivalentes a las de administrador de dominio en el nuevo grupo local.
  
6.  Cree un objeto de directiva de grupo en cada dominio que restrinja el uso de cuentas de administrador de nivel de dominio para los servicios en todos los equipos mediante la asignación de los derechos de usuario **Denegar el inicio de sesión como servicio** y **Denegar el inicio de sesión como trabajo por lotes** y la aplicación de los permisos **Permitir-Leer** y **Permitir-Aplicar** en el GPO al grupo local del dominio de cuentas de administradores de dominio creado.
  
7.  Use filtros de directivas de grupo para el grupo de servidores de alta seguridad en cada GPO, para que los miembros de ese grupo puedan seguir usando cuentas de administrador de dominio para los servicios. Esta funcionalidad se puede lograr aplicando los permisos **Permitir-Leer** y **Denegar-Aplicar** en el GPO del grupo de servidores de alta seguridad.
  
La administración de los miembros del grupo de servidores de alta seguridad debe usar un proceso de flujo de trabajo interno que evalúe las solicitudes de inclusiones en el grupo. Este proceso debe incluir pasos que validen las solicitudes y evalúen los riesgos de seguridad asociados si se agrega un servidor al grupo. La base de este proceso puede variar entre una sencilla, como solicitudes de correo electrónico a una cuenta especificada, hasta un proceso automatizado detallado mediante cualquier serie de herramientas de aprovisionamiento, como Zero Touch Provisioning (ZTP).
  
ZTP no es el objeto de este documento porque es una herramienta orientada hacia entornos de empresas más grandes. Sin embargo, si desea más información sobre ZTP y otras herramientas similares, puede consultar el sitio Web [Centro de implementación de escritorio](http://www.microsoft.com/technet/desktopdeployment/default.mspx) (en inglés) de Microsoft en www.microsoft.com/technet/desktopdeployment/default.mspx.
  
##### Administración de cambios de contraseña de cuentas de servicio
  
Cuando se asignan cuentas a un servicio, el Administrador de control de servicios (SCM) solicita la contraseña correcta para esa cuenta antes de realizar la asignación. Si se proporciona una contraseña incorrecta, SCM rechazará la asignación. La configuración de servicios para usar las cuentas Sistema local, Servicio local o Servicio de red hace que no sea necesario administrar las contraseñas de cuentas porque es el sistema operativo el que se encarga de esto.
  
En el caso de otras cuentas de servicio, SCM almacena las contraseñas de cuentas en la base de datos de servicios. Una vez asignadas las contraseñas, SCM no comprueba las contraseñas almacenadas en esa base de datos y la contraseña asignada a una cuenta de usuario de Active Directory seguirá coincidiendo. Esto puede provocar problemas cuando se produzcan situaciones como las siguientes:
  
1.  Se configura un servicio para usar una cuenta de usuario específica.
  
2.  El servicio empieza usando esa cuenta con la contraseña actual.
  
3.  Se cambia la contraseña de esa cuenta de usuario mientras el servicio se sigue ejecutando.
  
4.  El servicio sigue ejecutándose hasta que se detiene. Después de detenerse, el servicio no se puede reiniciar porque SCM aún está intentando usar la contraseña antigua. Los cambios de contraseñas de Active Directory no se sincronizan con las contraseñas almacenadas en la base de datos de servicios.
  
Cualquier servicio que use una cuenta de usuario local o de dominio estándar se debe actualizar con la nueva información de autenticación cada vez que se cambie la contraseña de esa cuenta de usuario. Esto puede suponer mucho tiempo y esfuerzo si los servicios y cuentas que usan no están bien documentados.
  
Por supuesto, la existencia de un documento que almacene información de cuentas para todos los servicios usados en todos los servidores tiene su propio riesgo de seguridad concreto, por lo que se deben realizar todos los pasos necesarios para proteger ese documento. Las organizaciones más grandes pueden registrar esta información en un archivo cifrado, que se debe quitar de la red y almacenarse en un lugar seguro. Las organizaciones más pequeñas pueden sencillamente registrar esta información en papel y guardarla en una carpeta de ubicación segura o protegida bajo llave.
  
Algunas aplicaciones también pueden usar las contraseñas de cuentas de servicio, como Exchange Server o SQL Server™, por lo que se debe tener cuidado y cambiar las contraseñas correspondientes en la interfaz de aplicación en dichas situaciones.
  
Para obtener más información sobre cómo escribir herramientas para automatizar el proceso de cambio de contraseñas de cuentas de servicio, consulte el artículo "[Cambio de contraseña en una cuenta de usuario de servicio](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/ad/ad/changing_the_password_on_a_serviceampaposs_user_account.asp)" (en inglés) en http://msdn.microsoft.com/library/default.asp?url=/library/en-us/ad/ad/changing\_the\_password\_on\_a\_serviceampaposs\_user\_account.asp.
  
##### Uso obligatorio de contraseñas seguras
  
Como se mencionó en la sección correspondiente sobre cuentas de administrador, el uso de directivas de contraseñas seguras se debe aplicar de forma estricta en todas las cuentas equivalentes a las de administrador, así como en todas las cuentas de servicio. Para aplicar dichas reglas, se puede usar la directiva de grupo para aplicar fechas de caducidad de las contraseñas, restricciones de longitud mínima, así como otras normas de contraseñas seguras.
  
Para obtener más información sobre las directivas de contraseñas seguras, consulte el documento "[Contraseñas y directivas de cuentas](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/bpactlck.mspx)" (en inglés) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/bpactlck.mspx 
  
Para obtener más información sobre cómo aplicar el uso de contraseñas seguras, consulte la [*Guía de Seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?linkid=14845.
  
Las contraseñas poco seguras representan una de las vulnerabilidades más habituales de una red; además, cuando se usan con cuentas equivalentes a las de administrador, son una de las formas más sencillas en las que un atacante puede obtener acceso a los recursos de la red. El uso de herramientas de prueba automatizadas para detectar cuentas equivalentes a las de administrador que usan contraseñas poco seguras debe convertirse en una tarea programada con regularidad para aquellas personas responsables de la seguridad o administración de la red.
  
Para realizar esta tarea, la herramienta Microsoft Baseline Security Analyzer (MBSA) puede buscar en cada uno de los equipos de la red si hay contraseñas poco seguras. MBSA puede enumerar todas las cuentas de usuario y comprobar si existen las siguientes vulnerabilidades relacionadas con las contraseñas:
  
-   Contraseñas en blanco.
  
-   Contraseñas que coincidan con nombres de cuentas de usuarios.
  
-   Contraseñas que coincidan con nombres de equipos.
  
-   Contraseñas que usen la palabra “contraseña”, “admin” o “administrador”.
  
Cuando se utiliza, MBSA intentará usar cada una de las vulnerabilidades mencionadas para cambiar la contraseña de una cuenta. Cuando se detecta una contraseña poco segura, no se cambiará la contraseña, pero MBSA indicará que la contraseña concreta supone un riesgo para la seguridad. MBSA también indicará las cuentas o cuentas deshabilitadas que estén bloqueadas.
  
Si bien MBSA detecta las peores prácticas de contraseñas que se suelen usar con más frecuencia, no proporciona capacidades de auditoría de contraseñas con todas sus funciones. Para satisfacer estas necesidades, existen en el mercado algunas herramientas y aplicaciones de detección sin conexión de terceros.
  
Para obtener más información sobre MBSA o para descargar esta herramienta, consulte la página web de [Microsoft Baseline Security Analyzer](http://www.microsoft.com/technet/security/tools/mbsahome.mspx) en www.microsoft.com/technet/security/tools/mbsahome.mspx.
  
**Nota**    MBSA restablecerá cualquier directiva de bloqueo de cuentas que se detecte en un equipo para evitar el bloqueo de las cuentas durante el proceso de detección. Asimismo, MBSA no realizará detecciones de contraseñas en equipos que estén designados como controladores de dominio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Está claro que se pueden realizar una gran cantidad de pasos para mejorar la seguridad de las cuentas críticas y de servicio en la red de una mediana empresa. Fundamentalmente, todos estos métodos se basan en unos pocos conceptos clave, como el establecimiento de procesos bien documentados y el uso de prácticas que siguen el principio del privilegio mínimo. Con sólo comprender y usar estos pocos conceptos clave como base para administrar las cuentas, se mejorará en gran medida la seguridad de cualquier red.
  
Se puede usar cualquier combinación de las técnicas de prácticas recomendadas descritas en este documento en la red de una mediana empresa si se considera adecuada a las necesidades de la empresa. Si bien todas estas prácticas combinadas mejorarían sin duda la seguridad de cualquier red, es mejor analizar el posible impacto que tendría cada una de ellas en la red de una empresa antes de determinar la combinación de métodos más compatible.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice A: Servicios habituales
  
La siguiente tabla enumera y describe los servicios habituales de Windows Server 2003 y de Windows XP en orden alfabético. Si bien esta lista incluye tanto los servicios predeterminados como los servicios que se pueden agregar a un equipo, no se trata de una lista cerrada de todos los posibles servicios que se podrían instalar en un equipo, ya que no incluye los servicios que se podrían instalar con los paquetes de software de terceros.
  
**Tabla A.1 Descripciones de servicios de Windows XP y Windows Server 2003**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Servicio</th>
<th>Nombre del servicio</th>
<th>Iniciar sesión como</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">6to4</td>
<td style="border:1px solid black;">Servicio de ayuda de IPv6</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la conectividad IPv6 en redes IPv4.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AELookupSvc</td>
<td style="border:1px solid black;">Servicio de búsqueda sobre experiencia con aplicaciones</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Procesa las solicitudes de búsqueda de compatibilidad de aplicaciones para las aplicaciones conforme se inician. Debe estar activo para que se pueda actualizar el software de compatibilidad de aplicaciones.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio de alerta</td>
<td style="border:1px solid black;">Servicio de alerta</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Este servicio notifica a lo usuarios y equipos seleccionados las alertas administrativas y se basa en el servicio Messenger de los equipos cliente para la entrega.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ALG</td>
<td style="border:1px solid black;">Servicio de puerta de enlace de capa de aplicación</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Es compatible con los complementos que permiten a los protocolos de red pasar por el firewall y funcionar detrás de una conexión ICS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">AppMgmt</td>
<td style="border:1px solid black;">Administración de aplicaciones</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de instalación de software como Asignar, Publicar o Quitar. Si se deshabilita, no se podrán instalar aplicaciones mediante los servicios de Active Directory, como IntelliMirror®.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AppMgr</td>
<td style="border:1px solid black;">Administrador de servidores remotos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Actúa como un proveedor de instancias WMI para los objetos de alerta de Administración remota y un proveedor de métodos WMI para las tareas de Administración remota.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">aspnet_state</td>
<td style="border:1px solid black;">Servicio de estado de ASP.NET</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Es compatible con los estados de sesión fuera de proceso de ASP.NET.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AudioSrv</td>
<td style="border:1px solid black;">Audio de Windows</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra los dispositivos de audio de los programas basados en Windows.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">BINLSVC</td>
<td style="border:1px solid black;">Instalación remota</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Se trata del componente principal del Servicio de instalación remota (RIS), que responde a las solicitudes de PXE en los equipos que permiten el inicio remoto.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">BITS</td>
<td style="border:1px solid black;">Servicio de transferencia inteligente en segundo plano</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Ofrece un mecanismo de transferencia de archivos en segundo plano para el administrador de colas. Cuando se detiene este servicio, el equipo no podrá usar las características de actualización automática.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Examinador</td>
<td style="border:1px solid black;">Examinador de equipos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Mantiene una lista actualizada de equipos de la red.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CertSvc</td>
<td style="border:1px solid black;">Servicios de Certificate Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Parte del sistema operativo central que emite y administra certificados digitales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">cisvc</td>
<td style="border:1px solid black;">Servicios de Index Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite un acceso rápido a los archivos a través de un lenguaje de consulta mediante la indexación del contenido y las propiedades de los archivos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ClipSrv</td>
<td style="border:1px solid black;">ClipBook</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite al visor ClipBook crear y compartir páginas para que los usuarios remotos puedan revisar los datos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ClusSvc</td>
<td style="border:1px solid black;">Servicios de Cluster Server</td>
<td style="border:1px solid black;">Cuenta de dominio</td>
<td style="border:1px solid black;">Controla las operaciones del clúster del servidor y administra la base de datos del clúster.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">COMSysApp</td>
<td style="border:1px solid black;">Aplicación del sistema COM+</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra la configuración y el seguimiento de los componentes basados en COM+. Los componentes de COM+ no funcionarán correctamente si este servicio está deshabilitado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CORRTSvc</td>
<td style="border:1px solid black;">Servicio de soporte técnico de .NET Framework</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Notifica a los clientes suscriptores cuando los procesos especificados inicialicen el servicio de tiempo de ejecución del cliente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CryptSvc</td>
<td style="border:1px solid black;">Servicios de cifrado</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de administración de claves criptográficas para equipos basados en Windows.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DcomLaunch</td>
<td style="border:1px solid black;">Iniciador de procesos de servidor DCOM</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona parte de los servicios RPC que necesitan privilegios del sistema local, junto con el servicio RPCS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Dfs</td>
<td style="border:1px solid black;">Sistema de archivos distribuido</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Integra distintos recursos compartidos de archivos en la red en un espacio de nombre lógico único. Necesario para anunciar el recurso compartido SYSVOL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DFSR</td>
<td style="border:1px solid black;">Replicación del sistema de archivos distribuido</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Copia automáticamente las actualizaciones en los archivos y carpetas entre equipos que participan en un grupo de replicación común (agregado en Windows Server 2003 R2).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Dhcp</td>
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Administra la información de configuración de la red DHCP mediante el registro y la actualización de las direcciones IP.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DHCPServer</td>
<td style="border:1px solid black;">Servidor DHCP</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Este servicio administra DHCP y asigna direcciones IP a los equipos cliente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">dmadmin</td>
<td style="border:1px solid black;">Servicio administrativo del Administrador de discos lógicos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Realiza servicios administrativos para las solicitudes de administración de discos y configura los discos y volúmenes. Este servicio sólo se ejecuta durante estos procesos de configuración.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">dmserver</td>
<td style="border:1px solid black;">Administrador de discos lógicos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Detecta y supervisa nuevas unidades de disco y envía información de volumen al servicio dmadmin. No lo deshabilite si se usan discos dinámicos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DNS</td>
<td style="border:1px solid black;">Servidor DNS</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la resolución de nombres DNS respondiendo consultas y actualizando solicitudes de nombres DNS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Dnscache</td>
<td style="border:1px solid black;">Cliente DNS</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Resuelve y almacena en caché los nombres DNS y se debe ejecutar sólo en cualquier equipo que realice la resolución de nombres DNS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ERSvc</td>
<td style="border:1px solid black;">Servicio de informe de errores</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Recopila, almacena e informa de los errores o cierres inesperados de aplicaciones.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Eventlog</td>
<td style="border:1px solid black;">Registro de sucesos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Escribe sucesos enviados pro programas, servicios y el sistema operativo en los registros de sucesos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">EventSystem</td>
<td style="border:1px solid black;">Sistema de sucesos COM+</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la distribución automática de sucesos a los componentes COM que se suscriben.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compatibilidad de cambio rápido de usuario</td>
<td style="border:1px solid black;">Compatibilidad de cambio rápido de usuario</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite administrar las aplicaciones que necesitan asistencia en entornos de varios usuarios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Fax</td>
<td style="border:1px solid black;">Servicio de fax</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proveedor de funciones de fax compatible con TAPI.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Groveler</td>
<td style="border:1px solid black;">Groveler de almacenamiento de instancia única</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Parte integral de los Servicios de instalación remota (RIS) que busca archivos duplicados y copia el original e el almacenamiento de instancia única.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">helpsvc</td>
<td style="border:1px solid black;">Ayuda y soporte técnico</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite tener acceso a almacenes y servicios que contienen metadatos e información sobre los temas de ayuda para la aplicación Centro de ayuda y soporte técnico.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">HidServ</td>
<td style="border:1px solid black;">Acceso a dispositivo de interfaz humana</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el acceso de entrada genérico a los dispositivos USB como teclados y mouse.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">HTTPFilter</td>
<td style="border:1px solid black;">SSL HTTP</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a IIS realizar funciones SSL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">IAS</td>
<td style="border:1px solid black;">Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Realiza una autenticación, auditoría y contabilidad centralizadas de los usuarios que se conectan a una red.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IASJet</td>
<td style="border:1px solid black;">Acceso a base de datos IAS Jet</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de autenticación, autorización y cuentas mediante el protocolo RADIUS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">IISADMIN</td>
<td style="border:1px solid black;">Servicio IISAdmin</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Permite administrar los componentes de IIS, como FTP y las extensiones de servicios web.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ImapiService</td>
<td style="border:1px solid black;">Servicio COM de grabación de CD de IMAPI</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra la creación de CD mediante la interfaz COM IMAPI y escribe en CD-R cuando se le solicita.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Irmon</td>
<td style="border:1px solid black;">Monitor de infrarrojos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite compartir archivos mediante conexiones por infrarrojos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IsmServ</td>
<td style="border:1px solid black;">Mensajería entre sitios</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite intercambios de mensajes entre equipos que ejecutan Windows Server.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">kdc</td>
<td style="border:1px solid black;">Centro de distribución de claves Kerberos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite que los usuarios inicien sesión mediante el protocolo de autenticación Kerberos. Si este servicio se detiene, los clientes no podrán iniciar sesión en un dominio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">lanmanserver</td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Es compatible con RPC y con el uso compartido de archivos, recursos de impresión y canalizaciones con nombre en la red.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Estación de trabajo Lanman</td>
<td style="border:1px solid black;">Estación de trabajo</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona conexiones de red y comunicaciones para los servicios cliente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">LicenseService</td>
<td style="border:1px solid black;">Registro de licencias</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Originalmente diseñado para administrar licencias CAL, se presentó con Windows NT® Server 3.51. Sólo lo deben habilitar los usuarios de Microsoft Small Business Server.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">LMHosts</td>
<td style="border:1px solid black;">Servicio Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Es compatible con NetBIOS en TCP/IP y la resolución de nombres NetBIOS para los clientes.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">LPDSVC</td>
<td style="border:1px solid black;">Servidor de impresión TCP/IP</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la impresión basada en TCP/IP mediante el uso del protocolo LPD para la recepción de documentos de utilidades LPD que se ejecutan en plataformas UNIX.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">LSASS</td>
<td style="border:1px solid black;">Autoridad de seguridad local</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Ofrece una interfaz para administrar la seguridad local, la autenticación de dominios y los procesos de Active Directory.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MacFile</td>
<td style="border:1px solid black;">Servidor de archivos para Macintosh</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a los usuarios de Macintosh almacenar y tener acceso a los archivos de Windows Server 2003.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MacPrint</td>
<td style="border:1px solid black;">Servidor de impresión para Macintosh</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a los usuarios de Macintosh usar los servicios de impresión de Windows Server 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MDM</td>
<td style="border:1px solid black;">Administrador de depuración del equipo</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Administra la depuración local y remota para las aplicaciones.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Messenger</td>
<td style="border:1px solid black;">Messenger</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Envía o recibe mensajes del Servicio de alerta. No está relacionado con Windows Messenger y, si se deshabilita, impedirá el uso de los comandos net send y net name.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">mnmsrvc</td>
<td style="border:1px solid black;">Escritorio remoto compartido de NetMeeting</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el acceso remoto de los usuarios autorizados al Escritorio de Windows desde otros equipos mediante los servicios de Windows NetMeeting®.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">mqds</td>
<td style="border:1px solid black;">Clientes de nivel inferior de Message Queue Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite tener acceso con Active Directory a las versiones anteriores de Windows que usen el servicio Message Queue Server.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Mqtgsvc</td>
<td style="border:1px solid black;">Desencadenadores de Message Queue Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona un sistema basado en normas para supervisar los mensajes que llegan en un servicio Message Queue Server e invoca a los servicios de procesamiento de mensajes.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSDTC</td>
<td style="border:1px solid black;">Coordinador de transacciones distribuidas</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Coordina las transacciones distribuidas entre distintos equipos, bases de datos, sistemas de archivos, colas de mensajes y otros administradores de recursos con protección de transacciones.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MTA de Microsoft Exchange</td>
<td style="border:1px solid black;">Pilas de MTA de Microsoft Exchange</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Proporciona un servicio de transferencia de mensajes compatible con productos anteriores en un entorno de modo mixto.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSFTPSVC</td>
<td style="border:1px solid black;">Servicio de publicación FTP</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Permite la conectividad mediante FTP y la administración mediante el complemento IIS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSIServer</td>
<td style="border:1px solid black;">Windows Installer</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra la instalación y eliminación de aplicaciones mediante la aplicación de conjuntos de normas de configuración definidas centralmente durante los procesos de instalación.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">msmq</td>
<td style="border:1px solid black;">Message Queue Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Actúa como una infraestructura de mensajería y una herramienta de desarrollo que permite la mensajería distribuida en los programas de Windows.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSSQL$UDDI</td>
<td style="border:1px solid black;">MSSQL$UDDI</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Proporciona los servicios Universal Description, Discovery, and Integration (UDDI) al motor de la base de datos SQL Server.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MS SQL SERVER</td>
<td style="border:1px solid black;">MS SQL Server</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Proporciona servicios configurables de MS SQL Server.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ayuda de Active Directory de MS SQL Server</td>
<td style="border:1px solid black;">Ayuda de Active Directory de MS SQL Server</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a los servicios SQL Server y Análisis de SQL Server publicar información en Active Directory.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">NetDDE</td>
<td style="border:1px solid black;">DDE de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el transporte y la seguridad de red para DDE en los programas que se ejecutan en el mismo equipo o en distintos equipos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">NetDDEdsdm</td>
<td style="border:1px solid black;">DSDM de DDE de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra los recursos compartidos de red DDE.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Netlogon</td>
<td style="border:1px solid black;">Netlogon</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Mantiene un canal de seguridad entre los equipos cliente y los controladores de dominio para la autenticación de servicios y usuarios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Netman</td>
<td style="border:1px solid black;">Conexiones de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra los objetos de la carpeta Conexiones de red.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Conexiones de red</td>
<td style="border:1px solid black;">Conexiones de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra los objetos de la carpeta Conexiones de red y de acceso telefónico, desde la que se pueden ver las conexiones de red y remotas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">NLA</td>
<td style="border:1px solid black;">Conocimiento de ubicación de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Recopila y almacena información de la configuración de red y procesa la información de cambios de ubicación.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">NntpSvc</td>
<td style="border:1px solid black;">Protocolo de transferencia de noticias en red (NNTP)</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a los equipos actuar como servidores de noticias NNTP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">NtFrs</td>
<td style="border:1px solid black;">Replicación de archivos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Copia automáticamente las actualizaciones en los archivos y carpetas entre equipos que participan en un conjunto de réplicas FRS común.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">NtLmSsp</td>
<td style="border:1px solid black;">Proveedor de compatibilidad con seguridad NTLM</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Responsable de la autenticación y administración de objetos de directiva de seguridad local.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Estación de trabajo Netware</td>
<td style="border:1px solid black;">Servicio de cliente para NetWare</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Permite tener acceso a archivos y recursos de impresión de NetWare.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">nwsapagent</td>
<td style="border:1px solid black;">Agente de SAP</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Anuncia servicios de red en redes IPX mediante el protocolo IPX de SAP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">un punto</td>
<td style="border:1px solid black;">Microsoft Operations Manager 2000 Agent</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Microsoft Operations Manager (MOM) 2000 Agent.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">PlugPlay</td>
<td style="border:1px solid black;">Plug and Play</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el reconocimiento de cambios de hardware sin intervención del usuario.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">PolicyAgent</td>
<td style="border:1px solid black;">Servicio IPsec</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra la directiva IPsec, inicia IKE y coordina la configuración de la directiva IPsec en el controlador de seguridad de IP.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">POP3SVC</td>
<td style="border:1px solid black;">Servicio POP3 de Microsoft</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Permite servicios de transferencia y recuperación de correo electrónico.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Guardar información con contraseña</td>
<td style="border:1px solid black;">Guardar información con contraseña</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el almacenamiento de datos sensibles con contraseña.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RasAuto</td>
<td style="border:1px solid black;">Administrador de conexión automática de acceso remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Crea conexiones a equipos remotos siempre que los programas hagan referencia a direcciones o nombres DNS o NetBIOS remotos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RasMan</td>
<td style="border:1px solid black;">Connection Manager de acceso remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra las conexiones de acceso telefónico y VPN a las redes remotas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RDSessMgr</td>
<td style="border:1px solid black;">Administrador de sesión de Ayuda de escritorio remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra y controla la característica Asistencia remota de la aplicación Centro de ayuda y soporte técnico.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Remote_
Storage_Server</td>
<td style="border:1px solid black;">Servidor de almacenamiento remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Mueve y recupera archivos de medios de almacenamiento secundarios.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Remote_
Storage_User_
Link</td>
<td style="border:1px solid black;">Notificación de almacenamiento remoto</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">El servicio Remote_Storage_User_Link notifica a los usuarios cuando intentan leer o escribir en archivos que sólo están disponibles en medios de almacenamiento secundarios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RemoteAccess</td>
<td style="border:1px solid black;">Enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de enrutamiento de varios protocolos y servicios de acceso remoto VPN y de acceso telefónico.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RemoteRegistry</td>
<td style="border:1px solid black;">Servicio de registro remoto</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Permite a los usuarios remotos modificar la configuración de registro con los permisos adecuados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RpcLocator</td>
<td style="border:1px solid black;">Ubicador de llamadas a procedimiento remoto</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Administra la base de datos del servicio de nombres RPC para que los clientes RPC puedan encontrar los servidores RPC. Deshabilitado de manera predeterminada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RpcSs</td>
<td style="border:1px solid black;">Llamada a procedimiento remoto</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Actúa como asignador de extremos de RPC y servicio Modelo de objetos de componentes (COM).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RSoPProv</td>
<td style="border:1px solid black;">Conjunto resultante de proveedor de directivas</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite conexiones a controladores de dominio de Windows, el acceso a la base de datos de WMI, además de simular RSoP para la configuración de la directiva de grupo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RSVP</td>
<td style="border:1px solid black;">RSVP de QoS</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra el uso de las solicitudes de la API de calidad de servicio genérica de las aplicaciones.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Sacsvr</td>
<td style="border:1px solid black;">Ayuda de la consola de administración especial</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Realiza tareas de administración remota cuando el sistema operativo de una familia de Windows Server deja de funcionar debido a mensajes de error de detención.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SamSs</td>
<td style="border:1px solid black;">Administrador de cuentas de seguridad</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra la información de cuentas de grupos y usuarios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SCardSvr</td>
<td style="border:1px solid black;">Tarjeta inteligente</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Administra y controla el acceso a las tarjetas inteligentes cuando se insertan en un lector de tarjetas inteligentes instalado en el equipo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Programa</td>
<td style="border:1px solid black;">Administrador de tareas</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite analizar el rendimiento de tareas automatizadas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">seclogon</td>
<td style="border:1px solid black;">Inicio de sesión secundario</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite crear los procesos en el contexto de distintos principios de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SENS</td>
<td style="border:1px solid black;">Notificación de sucesos del sistema</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Realiza un seguimiento de los sucesos del sistema y de energía y notifica estos sucesos a los suscriptores del Sistema de sucesos COM+.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SharedAccess</td>
<td style="border:1px solid black;">Servidor de seguridad de conexión de Windows/Conexión compartida a Internet</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios NAT, de direcciones y resolución de nombres para todos los equipos de una red cuando está habilitada la Conexión compartida a Internet.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Detección
de hardware de shell</td>
<td style="border:1px solid black;">Detección de hardware de shell</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona notificaciones para sucesos de hardware de reproducción automática.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SimpTcp</td>
<td style="border:1px solid black;">Servicios simples de TCP/IP</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Proporciona servicios TCP/IP simples como: eco, desechar, hora diurna, generador de caracteres y cita del día.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SMTPSVC</td>
<td style="border:1px solid black;">Protocolo simple de transferencia de correo</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Actúa como un agente de envío y transmisión SMTP al aceptar y colocar en cola los mensajes de correo electrónico de y para destinos remotos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SNMP</td>
<td style="border:1px solid black;">Servicio SNMP</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite que el equipo local atienda las solicitudes SNMP entrantes.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SNMPTRAP</td>
<td style="border:1px solid black;">Servicio de captura SNMP</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Recibe mensajes de capturas SNMP generados por los agentes SNMP locales o remotos y, a continuación, los reenvía a los servidores de administración SNMP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cola de impresión</td>
<td style="border:1px solid black;">Cola de impresión</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra todas las colas de impresión de red y locales y controla todos los trabajos de impresión.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SQLAgent$
WEBDB</td>
<td style="border:1px solid black;">UDDI o WebDB SQL Agent$</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SrvcSurg</td>
<td style="border:1px solid black;">Servicio de administración remota</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Responsable de ejecutar tareas de Administración remota al iniciar el servidor, incluidos el aumento del recuento de inicios del servidor y la generación de alertas si no se establecen la fecha y hora del servidor.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">StiSvc</td>
<td style="border:1px solid black;">Digitalización de imágenes de Windows</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Proporciona servicios de adquisición de imágenes para escáneres y cámaras.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">srservice</td>
<td style="border:1px solid black;">Servicio Restaurar sistema</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Supervisa los cambios en los archivos del sistema y la aplicación y, a continuación, crea puntos de restauración fácilmente identificables.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SSDPSRV</td>
<td style="border:1px solid black;">Servicio de descubrimientos SSDP</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Administra anuncios de presencia de dispositivos, actualizaciones de caché y notificaciones SSDP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">StiSvc</td>
<td style="border:1px solid black;">Digitalización de imágenes de Windows (WIA)</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Permite una sólida comunicación entre aplicaciones y dispositivos de captura de imágenes para lograr una eficiente transferencia de imágenes al equipo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SwPrv</td>
<td style="border:1px solid black;">Proveedor de instantáneas de software Microsoft</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra instantáneas de software tomadas por el servicio VSS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SysmonLog</td>
<td style="border:1px solid black;">Alertas y registros de rendimiento</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Recopila información de alertas y del registro de rendimiento; sólo se ejecuta cuando hay programado al menos un suceso de recopilación de datos de rendimiento.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TapiSrv</td>
<td style="border:1px solid black;">Telefonía</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Es compatible con TAPI en el caso de programas que controlen los dispositivos de telefonía y conexiones de voz basadas en IP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">TermService</td>
<td style="border:1px solid black;">Terminal Services</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite el acceso de varios clientes a las sesiones de escritorio virtual de Windows que se ejecutan en el servidor.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TermServ
Licencias</td>
<td style="border:1px solid black;">Licencias de servicios de Terminal Services</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Proporciona licencias a clientes registrados cuando se conectan a una sesión de Terminal Services y realiza un seguimiento de dichas licencias.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">tftpd</td>
<td style="border:1px solid black;">Demonio FTP trivial</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Escucha y responde las solicitudes TFTP.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Temas</td>
<td style="border:1px solid black;">Temas</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Es compatible con la presentación de la interfaz de usuario gráfica (GUI) de Windows XP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">TlntSvr</td>
<td style="border:1px solid black;">Telnet</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de Telnet a los usuarios de Windows y admite los tipos de sesión de terminal ANSI, VT-100, VT52 y VTNT.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TrkSvr</td>
<td style="border:1px solid black;">Servidor de seguimiento de vínculos distribuido</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Almacena información para que se pueda realizar un seguimiento de los archivos movidos entre volúmenes a cada uno de los volúmenes del dominio. Se ejecuta en cada controlador de dominio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">TrkWks</td>
<td style="border:1px solid black;">Cliente de seguimiento de vínculos distribuidos</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Mantiene vínculos entre los archivos del sistema de archivos NTFS del equipo o en la red y asegura que funcionen los accesos directos y vínculos OLE después de mover o cambiar el nombre de los archivos de destino.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tssdis</td>
<td style="border:1px solid black;">Directorio de sesión de servicios de Terminal Services</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Realiza un seguimiento de las sesiones de Terminal Services desconectadas en un clúster para garantizar que los usuarios se puedan volver a conectar a esas sesiones.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Uploadmgr</td>
<td style="border:1px solid black;">Administrador de carga</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra las transferencias de archivos síncronas y asíncronas entre clientes y servidores de la red.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">upnphost</td>
<td style="border:1px solid black;">Host de dispositivo Plug and Play universal</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Implementa todos los componentes necesarios para el registro de dispositivos, el control y la respuesta a sucesos de los dispositivos alojados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">UPS</td>
<td style="border:1px solid black;">Sistema de alimentación ininterrumpida</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Administra las comunicaciones con un Sistema de alimentación ininterrumpida (SAI) conectado al equipo mediante el puerto serie.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">VDS</td>
<td style="border:1px solid black;">Servicio de disco virtual</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona una interfaz única para administrar la virtualización del almacenamiento de bloques, tanto si se realiza en el software del sistema operativo, en el almacenamiento RAID o en otros motores de virtualización.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">VSS</td>
<td style="border:1px solid black;">Instantáneas de volumen</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Administra las instantáneas de volumen que usan las aplicaciones de copia de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">W32Time</td>
<td style="border:1px solid black;">Horario de Windows</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Mantiene la sincronización de fecha y hora con NTP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">W3SVC</td>
<td style="border:1px solid black;">Servicio Publicación en World Wide Web</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Contiene un administrador de procesos y configuración para proporcionar servicios de publicación web.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente Web</td>
<td style="border:1px solid black;">Cliente Web</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Permite a las aplicaciones Win32 tener acceso a documentos de Internet.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administrador
de recursos
del sistema de Windows</td>
<td style="border:1px solid black;">Administrador de recursos del sistema de Windows</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la administración basada en directivas de la CPU y el consumo de memoria para los procesos que se están ejecutando en una sola instancia del sistema operativo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WinHttpAutoSvc</td>
<td style="border:1px solid black;">Servicio de Descubrimiento automático de proxy Web WinHTTP</td>
<td style="border:1px solid black;">Servicio local</td>
<td style="border:1px solid black;">Implementa la detección de configuración proxy en clientes WinHttp.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">winmgmt</td>
<td style="border:1px solid black;">Instrumental de administración de Windows</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona información de la administración de sistemas mediante varias interfaces.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WINS</td>
<td style="border:1px solid black;">Servicio WINS</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la resolución de nombres NetBIOS y la replicación WINS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WmdmPmSN</td>
<td style="border:1px solid black;">Número de serie de medios portátiles</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite a WMDM recuperar los números de serie de dispositivos de música portátiles conectados al equipo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Wmi</td>
<td style="border:1px solid black;">Extensiones del controlador de Instrumental de administración de Windows</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Supervisa todos los proveedores de controladores y seguimiento de sucesos configurados para publicar información de WMI o de seguimiento de sucesos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WmiApSrv</td>
<td style="border:1px solid black;">Adaptador de rendimiento de WMI</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Transforma los contadores de rendimiento suministrados por los proveedores de WMI en contadores que puede usar PDH mediante la biblioteca de rendimiento inverso de adaptador.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WMServer</td>
<td style="border:1px solid black;">Servicios de Windows Media</td>
<td style="border:1px solid black;">Servicio de red</td>
<td style="border:1px solid black;">Habilita los Servicios de Windows Media.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">wscsvc</td>
<td style="border:1px solid black;">Centro de seguridad</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Supervisa los parámetros y configuraciones de seguridad del sistema.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">wuauserv</td>
<td style="border:1px solid black;">Actualizaciones automáticas</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite descargar actualizaciones del sitio web de Microsoft Windows Update.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Wuser32</td>
<td style="border:1px solid black;">Agente de control remoto de SMS</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Proporciona servicios de administración de equipos remotos, como los servicios de transferencia de archivos remotos y de control remoto para SMS 2003.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WZCSVC</td>
<td style="border:1px solid black;">Configuración inalámbrica rápida</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite la configuración automática de adaptadores inalámbricos IEEE 802.11 para las comunicaciones inalámbricas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">xmlprov</td>
<td style="border:1px solid black;">Servicio de aprovisionamiento de red</td>
<td style="border:1px solid black;">Sistema local</td>
<td style="border:1px solid black;">Permite descargar y administrar archivos de configuración XML de los servicios de aprovisionamiento de la red como el Servicio de aprovisionamiento inalámbrico (WPS) de Microsoft.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la guía Protección de cuentas críticas y de servicio](http://go.microsoft.com/fwlink/?linkid=73609)
  
[](#mainsection)[Principio de la página](#mainsection)
