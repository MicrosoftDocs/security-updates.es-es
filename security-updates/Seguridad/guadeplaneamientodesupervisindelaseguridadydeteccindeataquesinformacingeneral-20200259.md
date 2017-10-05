---
TOCTitle: 'Guía de planeamiento de supervisión de la seguridad y detección de ataques: Información general'
Title: 'Guía de planeamiento de supervisión de la seguridad y detección de ataques: Información general'
ms:assetid: '8f1a0933-91df-4615-bca1-21d7b3f729c0'
ms:contentKeyID: 20200259
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163158(v=TechNet.10)'
---

Guía de planeamiento de supervisión de la seguridad y detección de ataques
==========================================================================

### Información general

Actualizado: mayo 23, 2005

Los numerosos informes de los medios acerca de la propagación de software malintencionado a través de Internet ha aumentado considerablemente el perfil de las amenazas externas existentes para los recursos de red de las organizaciones. No obstante, algunas de las mayores amenazas para la infraestructura de una organización provienen de los ataques que se originan en la red interna. Los ataques internos que presentan el mayor potencial de producir daño derivan de las actividades realizadas por las personas con las posiciones de mayor confianza, como los administradores de red. El análisis de las amenazas internas y externas ha llevado a numerosas organizaciones a llevar cabo investigaciones sobre sistemas capaces de supervisar las redes y detectar ataques.

En el caso de las organizaciones cuyas operaciones están limitadas por normativas, la supervisión de la seguridad es un requisito operativo. El número cada vez mayor de requisitos normativos impuestos por varias instituciones de todo el mundo obliga aún más a las organizaciones a supervisar sus redes, comprobar las consultas de acceso a recursos e identificar a los usuarios que inician y cierran sesión en la red. Las consideraciones normativas también pueden exigir a las empresas que archiven los datos de seguridad supervisados durante ciertos períodos de tiempo.

Los registros de seguridad de Microsoft® Windows® constituyen un punto de inicio para los paquetes que pueden supervisar la seguridad. No obstante, los registros de seguridad por sí solos no proporcionan información suficiente para planear la respuesta a un incidente determinado. Sin embargo, junto con otras tecnologías de recopilación de datos, sí que pueden formar parte importante de un sistema de supervisión de la seguridad y detección de ataques.

En esta guía se describe el modo de planear un sistema de supervisión de la seguridad en redes basadas en Windows. Este sistema puede detectar ataques que se originan en los recursos internos y externos. El objetivo principal de un sistema de supervisión de la seguridad es identificar sucesos no usuales en la red que indican actividad malintencionada o errores de procedimiento.

##### En esta página

[](#sghj)[El desafío empresarial](#schj)
[](#rotl)[Las ventajas empresariales](#rotl)
[](#ytre)[Destinatarios de la guía](#ytre)
[](#quop)[Requisitos previos del lector](#quop)
[](#ghgh)[Información general de la guía de planeamiento](#ghgh)
[](#iouy)[Capítulo 1: Introducción](#iouy)
[](#wqaw)[Capítulo 2: Enfoques para la supervisión de la seguridad](#wqaw)
[](#klie)[Capítulo 3: Problemas y requisitos](#klie)
[](#opie)[Capítulo 4: Diseño de la solución](#opie)

### El desafío empresarial

Las empresas hacen frente a numerosos retos a la hora de implementar sistemas eficaces de supervisión de la seguridad en redes de gran tamaño. Las empresas deben:

-   Identificar la necesidad de proteger la información.

-   Definir niveles de autorización para administradores y usuarios.

-   Implementar una directiva de supervisión completa.

-   Establecer una correlación de esta directiva con los sucesos de seguridad detectados.

Estos retos también se presentan ante organizaciones con requisitos de red menos complejos.

[](#mainsection)[Principio de la página](#mainsection)

### Las ventajas empresariales

La supervisión de la seguridad aporta dos ventajas principales para las organizaciones, independientemente de su tamaño: la capacidad de identificar ataques de forma instantánea y la capacidad de realizar análisis forenses de los sucesos ocurridos antes, durante y después de un ataque.

Gracias a la capacidad de detectar ataques de forma instantánea, los departamentos de seguridad pueden reaccionar rápidamente para reducir el daño producido en la infraestructura de la red. Los datos forenses también ayudan a los investigadores a identificar la extensión del ataque. Entre otras de las ventajas de la supervisión de la seguridad, se incluyen:

-   Reduce el efecto de los ataques.

-   Proporciona personal de seguridad para identificar rápidamente patrones anormales de comportamiento.

-   Crea información de auditoría para cumplir los requisitos normativos.

Para obtener más información sobre estas ventajas, consulte el capítulo 2 "Enfoques para la supervisión de la seguridad".

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

En esta guía, se ofrece información útil para las organizaciones con normas estrictas de privacidad, sobre todo para aquellas que se ven limitadas por las normativas vigentes. Esta guía va dirigida a organizaciones de cualquier tamaño que requieren sistemas de protección de identidad y control de acceso a datos.

Entre los usuarios a los que va dirigida esta guía, se incluyen administradores y especialistas de TI, como arquitectos y administradores de seguridad empresariales. Asimismo, los consultores que deben planear, implementar o trabajar con redes basadas en Windows, y el personal de toma de decisiones, encontrarán esta información de gran utilidad.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos del lector

Para comprender las soluciones que se exponen en esta guía, el lector debe comprender y conocer los problemas de seguridad y el perfil de riesgo de su red. Además, debe estar familiarizado con el servicio de registro de sucesos de Windows.

Esta guía utiliza los cuadrantes de funcionamiento y compatibilidad del modelo de proceso de Microsoft Operations Framework (MOF). También utiliza las funciones de administración de servicio (SMF) de administración de incidentes y seguridad de MOF. Para obtener más información acerca de MOF, visite el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof) en http://www.microsoft.com/mof (en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la guía de planeamiento

Esta guía consta de cuatro capítulos en los que se tratan los problemas y conceptos fundamentales relativos al planeamiento de una solución de supervisión de la seguridad y detección de ataques. Éstos son:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan los desafíos y las ventajas empresariales, se sugieren los destinatarios recomendados de la guía, se indica una lista de requisitos previos del lector y se brinda información general de los capítulos y ejemplos de la solución de esta guía.

**Capítulo 2: Enfoques para la supervisión de la seguridad**

En este capítulo se ofrece información general acerca de las distintas opciones disponibles para implementar una solución de supervisión de la seguridad y detección de ataques que utiliza tecnologías Microsoft y de terceros.

**Capítulo 3: Problemas y requisitos**

En este capítulo se describe el modo de establecer la correlación del ámbito de la supervisión de la seguridad con otros requisitos empresariales y con el intervalo conocido de posibles amenazas y ataques a una red empresarial. Por otro lado, se describen los retos empresarial, técnico y de seguridad que suponen:

-   Detectar infracciones a directivas

-   Identificar ataques externos

-   Implementar análisis forenses

Este capítulo define una infracción a directiva como toda desviación de las normativas organizativas. Por último, en este capítulo se incluyen los requisitos de la solución de un sistema de detección de ataques y supervisión de la seguridad.

**Capítulo 4: Diseño de la solución**

En este capítulo se ofrece información detallada sobre el uso de la supervisión de la seguridad para detectar ataques e implementar archivos de auditorías de seguridad. Se describe la configuración recomendada de un sistema de supervisión de la seguridad y los cambios que deben llevar a cabo las organizaciones para elaborar directivas de seguridad.

Asimismo, se proporcionan instrucciones detalladas con carácter normativo sobre la implementación de sistemas avanzados de supervisión de la seguridad en organizaciones de gran tamaño. Estas directrices describen el modo de tratar los problemas de almacenamiento de auditoría de grandes volúmenes de sucesos de seguridad, así como el modo de planear la detección de ataques en redes distribuidas.

#### Comuníquenos su opinión

Microsoft valora su opinión acerca de este material. Apreciaríamos especialmente cualquier comentario relacionado con las preguntas siguientes:

-   ¿En qué medida ha resultado útil la información proporcionada?

-   ¿Fueron los procedimientos paso a paso precisos?

-   ¿Le resultaron los capítulos fáciles de leer e interesantes?

-   ¿Cómo calificaría esta solución en líneas generales?

Envíe sus comentarios a la siguiente dirección de correo electrónico: [cisfdbk@microsoft.com](mailto:cisfdbk@microsoft.com?subject=guía%20de%20planeamiento%20de%20supervisión%20de%20la%20seguridad%20y%20detección%20de%20ataques)

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

[](#piyr)[Resumen ejecutivo](#piyr)
[](#ciar)[Información general de la guía de planeamiento](#ciar)
Resumen ejecutivo
-----------------

Los numerosos informes de los medios acerca de la propagación de software malintencionado a través de Internet ha aumentado considerablemente el perfil de las amenazas externas existentes para los recursos de red de las organizaciones. No obstante, algunas de las mayores amenazas para la infraestructura de una organización provienen de los ataques que se originan en la red interna. Los ataques internos que presentan el mayor potencial de producir daño derivan de las actividades realizadas por las personas con las posiciones de mayor confianza, como los administradores de red. El análisis de las amenazas internas y externas ha llevado a numerosas organizaciones a llevar cabo investigaciones sobre sistemas capaces de supervisar las redes y detectar ataques.

En el caso de las organizaciones cuyas operaciones están limitadas por normativas, la supervisión de la seguridad es un requisito operativo. El número cada vez mayor de requisitos normativos impuestos por varias instituciones de todo el mundo obliga aún más a las organizaciones a supervisar sus redes, comprobar las consultas de acceso a recursos e identificar a los usuarios que inician y cierran sesión en la red. Las consideraciones normativas también pueden exigir a las empresas que archiven los datos de seguridad supervisados durante ciertos períodos de tiempo.

Los registros de seguridad de Microsoft® Windows® constituyen un punto de inicio para los paquetes que pueden supervisar la seguridad. No obstante, los registros de seguridad por sí solos no proporcionan información suficiente para planear la respuesta a un incidente determinado. Sin embargo, junto con otras tecnologías de recopilación de datos, sí que pueden formar parte importante de un sistema de supervisión de la seguridad y detección de ataques.

En esta guía se describe el modo de planear un sistema de supervisión de la seguridad en redes basadas en Windows. Este sistema puede detectar ataques que se originan en los recursos internos y externos. El objetivo principal de un sistema de supervisión de la seguridad es identificar sucesos no usuales en la red que indican actividad malintencionada o errores de procedimiento.

#### El desafío empresarial

Las empresas hacen frente a numerosos retos a la hora de implementar sistemas eficaces de supervisión de la seguridad en redes de gran tamaño. Las empresas deben:

-   Identificar la necesidad de proteger la información.

-   Definir niveles de autorización para administradores y usuarios.

-   Implementar una directiva de supervisión completa.

-   Establecer una correlación de esta directiva con los sucesos de seguridad detectados.

Estos retos también se presentan ante organizaciones con requisitos de red menos complejos.

#### Las ventajas empresariales

La supervisión de la seguridad aporta dos ventajas principales para las organizaciones, independientemente de su tamaño: la capacidad de identificar ataques de forma instantánea y la capacidad de realizar análisis forenses de los sucesos ocurridos antes, durante y después de un ataque.

Gracias a la capacidad de detectar ataques de forma instantánea, los departamentos de seguridad pueden reaccionar rápidamente para reducir el daño producido en la infraestructura de la red. Los datos forenses también ayudan a los investigadores a identificar la extensión del ataque. Entre otras de las ventajas de la supervisión de la seguridad, se incluyen:

-   Reduce el efecto de los ataques.

-   Proporciona personal de seguridad para identificar rápidamente patrones anormales de comportamiento.

-   Crea información de auditoría para cumplir los requisitos normativos.

Para obtener más información sobre estas ventajas, consulte el capítulo 2 "Enfoques para la supervisión de la seguridad".

#### Destinatarios de la guía

En esta guía se ofrece información útil para las organizaciones con normas estrictas de privacidad, sobre todo para aquellas que se ven limitadas por las normativas vigentes. Esta guía va dirigida a organizaciones de cualquier tamaño que requieren sistemas de protección de identidad y control de acceso a datos.

Entre los usuarios a los que va dirigida esta guía, se incluyen administradores y especialistas de TI, como arquitectos y administradores de seguridad empresariales. Asimismo, los consultores que deben planear, implementar o trabajar con redes basadas en Windows, y el personal de toma de decisiones, encontrarán esta información de gran utilidad.

#### Requisitos previos del lector

Para comprender las soluciones que se exponen en esta guía, el lector debe comprender y conocer los problemas de seguridad y el perfil de riesgo de su red. Además, debe estar familiarizado con el servicio de registro de sucesos de Windows.

Esta guía utiliza los cuadrantes de funcionamiento y compatibilidad del modelo de proceso de Microsoft Operations Framework (MOF). También utiliza las funciones de administración de servicio (SMF) de administración de incidentes y seguridad de MOF. Para obtener más información acerca de MOF, visite el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof) en http://www.microsoft.com/mof (en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la guía de planeamiento

Esta guía consta de cuatro capítulos en los que se tratan los problemas y conceptos fundamentales relativos al planeamiento de una solución de supervisión de la seguridad y detección de ataques. Éstos son:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan los desafíos y las ventajas empresariales, se sugieren los destinatarios recomendados de la guía, se indica una lista de requisitos previos del lector y se brinda información general de los capítulos y ejemplos de la solución de esta guía.

**Capítulo 2: Enfoques para la supervisión de la seguridad**

En este capítulo se ofrece información general acerca de las distintas opciones disponibles para implementar una solución de supervisión de la seguridad y detección de ataques que utiliza tecnologías Microsoft y de terceros.

**Capítulo 3: Problemas y requisitos**

En este capítulo se describe el modo de establecer la correlación del ámbito de la supervisión de la seguridad con otros requisitos empresariales y con el intervalo conocido de posibles amenazas y ataques a una red empresarial. Por otro lado, se describen los retos empresarial, técnico y de seguridad que suponen:

-   Detectar infracciones a directivas

-   Identificar ataques externos

-   Implementar análisis forenses

Este capítulo define una infracción a directiva como toda desviación de las normativas organizativas. Por último, en este capítulo se incluyen los requisitos de la solución de un sistema de detección de ataques y supervisión de la seguridad.

**Capítulo 4: Diseño de la solución**

En este capítulo se ofrece información detallada sobre el uso de la supervisión de la seguridad para detectar ataques e implementar archivos de auditorías de seguridad. Se describe la configuración recomendada de un sistema de supervisión de la seguridad y los cambios que deben llevar a cabo las organizaciones para elaborar directivas de seguridad.

Asimismo, se proporcionan instrucciones detalladas con carácter normativo sobre la implementación de sistemas avanzados de supervisión de la seguridad en organizaciones de gran tamaño. Estas directrices describen el modo de tratar los problemas de almacenamiento de auditoría de grandes volúmenes de sucesos de seguridad, así como el modo de planear la detección de ataques en redes distribuidas.

### Capítulo 2: Enfoques para la supervisión de la seguridad

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Implementación de supervisión de la seguridad](#ecaa)
[](#eban)[Correlación de sucesos de auditoría de seguridad](#eban)
[](#eaam)[Soluciones de proveedores de software independientes](#eaam)
### Introducción

Ninguna empresa contemplaría la idea de realizar negocios desde instalaciones que no contaran con un sistema de seguridad físico adecuado, como cerraduras, sistemas de alarma, cámaras, vallas o guardias de seguridad. Sin embargo, numerosas empresas no han hecho más que comenzar a descubrir la necesidad de disponer de medidas de seguridad de igual eficacia para proteger sus activos de red tanto de ataques externos como de intrusiones internas.

Los sistemas de seguridad, como las cámaras y los detectores de movimiento, resultan de gran utilidad para detectar intentos de intrusión en edificios o áreas restringidas. No obstante, las organizaciones también necesitan implementar sistemas que les permitan supervisar los activos de red y detectar posibles atacantes. Por todo ello, la supervisión de la seguridad es un componente fundamental para aplicar estrategias de seguridad de red correctas.

En agosto de 2004, el servicio secreto de Estados Unidos, junto con el centro de coordinación CERT del Software Engineering Institute de la universidad de Carnegie Mellon, publicó un artículo en el que se documentan casos en los que varias instituciones han sido víctimas de fraudes masivos cometidos por sus propios usuarios internos. Para obtener más información, consulte el artículo "[Estudio de amenazas internas: actividad cibernética ilícita en el sector bancario y financiero](http://www.secretservice.gov/ntac/its_report_040820.pdf)" en el sitio Web http://www.secretservice.gov/ntac/its\_report\_040820.pdf. Este informe está en inglés.

Los documentos del estudio de 2004 E-Crime ponen aún más en evidencia esta amenaza. Entre los encuestados del estudio se incluyen gobiernos y organizaciones de los sectores bancario, financiero, de la información y de las telecomunicaciones. El estudio reveló que el 43% de los encuestados había notado un aumento de los delitos electrónicos e intrusiones a datos, y que el 70% había notificado, como mínimo, un delito electrónico el año anterior. El costo total por los delitos electrónicos sufridos por todos los encuestados había ascendido a más de 600 millones de dólares estadounidenses. Para obtener más información sobre el estudio de 2004 E-Crime, consulte el comunicado de prensa [El estudio de 2004 E-Crime Watch muestra un aumento considerable en delitos electrónicos](http://www.csoonline.com/) en http://www.csoonline.com/releases/ecrimewatch04.pdf (en inglés).

El número cada vez más alto de normativas empresariales y un mayor conocimiento de las amenazas que suponen los atacantes externos e internos han dado lugar al aumento de la demanda para implementar sistemas de supervisión de la seguridad eficaces. Para planear un sistema efectivo para la supervisión de la seguridad, hay que conocer las tecnologías de implementación de soluciones disponibles. En este capítulo se describen las tecnologías de Microsoft que permiten la supervisión de la seguridad y posibilitan la correlación de registros de seguridad para el análisis y el almacenamiento.

**Nota:** En este documento se distingue entre ataques internos y externos. Un ataque interno es aquel cometido por un empleado, normalmente un administrador. Un ataque externo, en cambio, proviene del exterior de la organización. Aunque la importancia cada vez mayor de tecnologías como las redes inalámbricas permite que los atacantes externos lancen ataques desde el interior del perímetro de la red, éstos aún se consideran ataques externos.

[](#mainsection)[Principio de la página](#mainsection)

### Implementación de supervisión de la seguridad

Los sucesos de seguridad se pueden registrar mediante el archivo de registro de sucesos de seguridad integrado que se incluye en todas las versiones de Microsoft® Windows®, desde Microsoft Windows NT® 3.1 y posteriores. Este archivo de registro constituye la base para la supervisión de la seguridad de las redes basadas en Windows. Otras utilidades y programas adicionales pueden establecer la correlación de los sucesos registrados en un repositorio central.

El archivo de registro de sucesos de seguridad utiliza un formato de base de datos personalizado para registrar los datos de supervisión de la seguridad. Las partes de este archivo, como los nombres de equipos y las direcciones IP, se pueden leer en un editor de texto. No obstante, para leer toda la información de los registros de seguridad, se debe contar con un programa adecuado, como la consola del Visor de sucesos. El archivo de registro de sucesos de seguridad (SecEvent.evt) reside en el directorio %systemroot%\\System32\\config. Al contrario de los registros de aplicación y sistema, los permisos predeterminados del sistema de archivos NTFS sólo permiten el acceso a este archivo a los miembros del grupo de administradores y de la cuenta del sistema.

El registro de sucesos de seguridad registra dos tipos de sucesos: auditorías correctas e incorrectas. Los sucesos de auditoría correcta indican que un usuario, servicio o programa completó una operación correctamente. Las auditorías incorrectas, en cambio, indican que una operación similar no se completó correctamente. Por ejemplo, si se habilitan auditorías de inicio de sesión para sucesos incorrectos, el registro de sucesos de seguridad registra los intentos de inicio de sesión incorrectos.

**Nota:** Microsoft** **Windows Server™ 2003 con Service Pack 1 permite configurar distintos niveles de auditoría de seguridad para usuarios diferentes. Para obtener más información sobre esta característica, consulte el capítulo 4 "Diseño de la solución".

En la tabla siguiente se enumeran las distintas categorías de sucesos de seguridad y los sucesos registrados por cada una.

**Tabla 2.1: Categorías de auditoría de sucesos de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Categoría</th>
<th style="border:1px solid black;" >Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sucesos de inicio de sesión de cuenta</td>
<td style="border:1px solid black;">Audita los intentos de inicio de sesión en una cuenta local de un equipo. Si la cuenta de usuario es una cuenta de dominio, este suceso también aparece en el controlador de dominios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administración de cuentas</td>
<td style="border:1px solid black;">Audita la creación, modificación y eliminación de cuentas de usuario o grupo, junto con cambios y restablecimientos de contraseña.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso del servicio de directorio</td>
<td style="border:1px solid black;">Audita el acceso a objetos en el servicio de directorio de Active Directory®.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Sucesos de inicio de sesión</td>
<td style="border:1px solid black;">Audita los intentos de inicio de sesión en estaciones de trabajo y servidores de miembros.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a objetos</td>
<td style="border:1px solid black;">Audita los intentos de obtener acceso a objetos como archivos, carpetas, claves de registro o impresoras con configuraciones de auditoría definidas dentro de la lista de control de acceso al sistema (SACL) de los mismos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cambio de directivas</td>
<td style="border:1px solid black;">Audita los cambios en las directivas de auditoría, cuenta, confianza o de asignación de derechos de usuario.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Uso de privilegios</td>
<td style="border:1px solid black;">Audita cada una de las instancias que se crean cuando un usuario ejerce un derecho, como el cambio de la hora del sistema.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Seguimiento de procesos</td>
<td style="border:1px solid black;">Audita el comportamiento de la aplicación, como el inicio y la finalización de un programa.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sucesos del sistema</td>
<td style="border:1px solid black;">Audita los sucesos del sistema informático, como el inicio y el apagado, y los sucesos que repercuten en la seguridad del sistema o el registro de seguridad.</td>
</tr>
</tbody>
</table>
  
La configuración de directiva de auditoría de Directiva de grupo controla los sucesos que crean entradas en los registros de seguridad. La ruta correspondiente a esta configuración es Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales. Los valores de la directiva de auditoría se pueden configurar a través de la consola Configuración de seguridad local, o en el nivel de sitio, dominio u organización a través de Directiva de grupo junto con Active Directory.
  
Los registros de seguridad constituyen una base adecuada para la supervisión completa de la seguridad. Los valores de Directiva de grupo representan una configuración centralizada de los niveles de auditoría de registro de seguridad. La configuración predeterminada sólo permite obtener acceso a los registros de seguridad a los administradores. No obstante, la supervisión de los ataques distribuidos y la implementación de análisis forenses requieren un sistema de supervisión capaz de establecer la correlación de los sucesos de auditoría de forma central.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Correlación de sucesos de auditoría de seguridad
  
La correlación de sucesos de auditoría de seguridad conlleva la recopilación de sucesos de seguridad de varios equipos y la colocación de esta información en una ubicación central. El personal de seguridad puede posteriormente analizar este repositorio central para identificar infracciones de directiva o ataques externos. El repositorio también se puede utilizar como la base para llevar a cabo los análisis forenses. En esta sección se proporciona información sobre los productos y utilidades de Microsoft capaces de establecer la correlación de varios registros de sucesos de seguridad. Varios productos de terceros también pueden realizar estas funciones.
  
#### Event Comb MT
  
Event Comb MT (subprocesos múltiples) es un componente de la Guía de seguridad de Windows Server 2003 que permite analizar y recopilar sucesos de varios registros de sucesos en equipos diferentes. Event Comb MT ejecuta una aplicación de subprocesos múltiples que permite especificar numerosos parámetros al analizar registros de sucesos, como:
  
-   Id. de suceso (individual o múltiple)
  
-   Intervalos de Id. de sucesos
  
-   Orígenes de sucesos
  
-   Texto de suceso específico
  
-   Vigencia del suceso en minutos, horas o días
  
Determinadas categorías de búsqueda están integradas en Event Comb, como los bloqueos de cuentas, que busca los sucesos siguientes:
  
-   529: error de inicio de sesión (nombre de usuario o contraseña incorrectos)
  
-   644: cuenta de usuario bloqueada automáticamente
  
-   675: error de autenticación previa en un controlador de dominio (contraseña incorrecta)
  
-   676: error de solicitud de vale de autenticación
  
-   681: error de inicio de sesión
  
Para buscar ataques en la cuenta predeterminada Administrador, puede agregar el suceso 12294 (umbral de bloqueos de cuenta superado) del registro del sistema. Este suceso es particularmente importante, ya que el umbral de bloqueos de cuenta no se aplica a la cuenta predeterminada Administrador. Por tanto, un atacante puede realizar varios intentos para poner en peligro la cuenta predeterminada Administrador sin activar el mecanismo de bloqueo de cuentas.
  
**Nota:** El suceso 12294** **aparece como un suceso Administrador de cuentas de seguridad (SAM) en el registro del sistema, no en el de seguridad.
  
Event Comb MT puede guardar sucesos en una tabla de una base de datos de Microsoft SQL Server™, lo que demuestra su utilidad para el almacenamiento a largo plazo y el análisis. Se pueden utilizar varios programas cliente para obtener acceso a la información de las tablas de SQL Server, como el Analizador de consultas de SQL, Microsoft Visual Studio® .NET u otras utilidades de terceros.
  
Event Comb MT v10.0 también incluye opciones de línea de comandos que se pueden utilizar para crear secuencias de comandos con el fin de automatizar la recopilación de sucesos de los registros de seguridad a intervalos regulares. Debido a que Event Comb MT no ofrece ningún tipo de agente de recopilación cliente ni reenvía automáticamente los sucesos a un repositorio central, su uso puede no resultar adecuado en todos los escenarios de amenaza.
  
Event Comb MT está disponible para su descarga gratuita en el sitio Web de las [herramientas de administración y bloqueo de cuentas](http://www.microsoft.com/downloads/details.aspx?displaylang=en&familyid=7af2e69c-91f3-4e63-8629-b999adde0b9e) en http://www.microsoft.com/downloads/details.aspx?displaylang=en&familyid=7af2e69c-91f3-4e63-8629-b999adde0b9e (en inglés).
  
La [Guía de seguridad de Windows Server 2003](http://www.microsoft.com/latam/technet/seguridad/guias/ws_2003/guia_ws2003.mspx) está disponible en http://www.microsoft.com/latam/technet/seguridad/articulos/ddmmyy\_guia\_seguridad\_windows\_server\_2003.asp.
  
#### Microsoft Operations Manager 2005
  
Microsoft Operations Manager (MOM) permite supervisar varios servidores de un entorno empresarial. El agente MOM recopila sucesos de los registros de sucesos y los reenvía al servidor de administración de MOM. Este último coloca a continuación los sucesos en la base de datos de MOM. MOM 2005 y versiones posteriores permiten recopilar sucesos de equipos que no ejecutan agentes MOM.
  
MOM utiliza las reglas de su paquete de administración para identificar los problemas que repercuten en la efectividad operativa de los servidores. Se pueden definir reglas adicionales para buscar determinados sucesos y, cuando éstos ocurran, enviar notificaciones instantáneas por correo electrónico, a través de mensajes emergentes o a dispositivos localizadores.
  
Aunque ofrece un gran número de funciones útiles para la supervisión de la seguridad y la detección de ataques, MOM no se ha diseñado para este propósito. Probablemente, las futuras versiones de MOM proporcionen un mayor número de funciones para la recopilación de registros de seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Soluciones de proveedores de software independientes
  
Los productos de Microsoft no proporcionan una solución completa para todos los aspectos de la supervisión de la seguridad. Entre las ausencias clave de los productos de Microsoft actuales se incluyen:
  
-   Alarmas de registro de sucesos en tiempo real.
  
-   Sistemas de recopilación de registros de sucesos seguros.
  
Los socios de Microsoft ofrecen los productos siguientes (enumerados en orden alfabético) que suplen estas ausencias:
  
-   **EventReporter de Adiscon.** EventReporter permite a los administradores combinar funciones de informe de registro de sucesos y alerta de UNIX y Windows en un único entorno. Es compatible con el protocolo syslog estándar de UNIX para la integración con sistemas basados en este sistema operativo, así como con el protocolo simple de transferencia de correo (SMTP) para el reenvío de alertas. EventReporter incluye un agente que se puede configurar para recopilar sucesos de seguridad de varios equipos, filtrarlos y, a continuación, colocarlos en una base de datos. En función del suceso de seguridad, se podrá reenviar estos sucesos por correo electrónico, iniciar aplicaciones y crear mensajes de red, entre otros. Para obtener más información sobre EventReporter de Adiscon, consulte el sitio Web de [EventReporter](http://www.eventreporter.com/) en www.eventreporter.com (en inglés).
  
-   **GFI LANguard Security Event Log Monitor (SELM) de GFI.** LANguard Security Event Log Monitor realiza la detección de intrusiones basada en los registros de sucesos y lleva a cabo la administración de éstos en toda la red. Asimismo, almacena y analiza los registros de sucesos de todos los equipos de red y alerta en tiempo real acerca de los problemas de seguridad, ataques y otros sucesos críticos. Security Event Log Monitor puede almacenar los registros de sucesos en una base de datos central y ofrece reglas e informes personalizados para el análisis forense. Para obtener más información, consulte el sitio Web de [GFI LANguard Security Event Log Monitor](http://www.gfihispana.com/) en http://www.gfihispana.com/.
  
-   **Systrack 3 de Lakeside Software, Inc.** Systrack 3 emite alarmas de registro de suceso prácticamente en tiempo real a través de Event Log Monitor. Event Log Monitor inspecciona de forma periódica todos los registros de sucesos de un equipo con el fin de determinar si ocurrió algo nuevo desde la última inspección. Systrack 3 filtra los sucesos recién descubiertos y realiza la acción pertinente. Estos filtros pueden utilizar la configuración predeterminada, la configuración definida por el usuario o una combinación de ambas. Las cadenas de caracteres específicos en las propiedades de los sucesos, como el nombre de una estación de trabajo o un usuario, pueden desencadenar alarmas de registro de sucesos. Un suceso también puede ejecutar una secuencia de comandos o reiniciar el equipo. Los filtros también pueden generar capturas del protocolo simple de administración de redes (SNMP), mensajes emergentes de Windows o alertas de correo electrónico. Para obtener más información sobre Systrack 3, consulte el sitio Web de [Lakeside Software](http://www.lakesidesoftware.com/) en www.lakesidesoftware.com (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 3: Problemas y requisitos
  
[](#ddra)[Introducción](#ddra)  
[](#elaa)[Detección de infracciones a directivas](#elaa)  
[](#emaa)[Identificación de ataques externos](#emaa)  
[](#enaa)[Implementación de análisis forenses](#enaa)  
[](#ejaa)[Resumen](#ejaa)  
### Introducción
  
Parte fundamental de una estrategia de seguridad eficaz consiste en realizar una valoración precisa de las amenazas a la red. Al igual que las organizaciones tienen distintos puntos de vista sobre lo que constituye un riesgo para la seguridad física, también tienen distinta opinión sobre los riesgos para los datos de red. Esta opinión depende de numerosos factores, como, por ejemplo, el sector en que opera la organización, el valor de los datos y si han sufrido ataques en la red con anterioridad. Para obtener más información sobre la administración de riesgos de seguridad, consulte la [Guía de administración de riesgos de seguridad](http://www.microsoft.com/spain/technet/recursos/articulos/srsgch00.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos  
/srsgch00.mspx.
  
A través de los datos de clientes y socios de Microsoft y de la información derivada de la red corporativa de Microsoft, se han identificado tres elementos principales de preocupación que la supervisión de la seguridad y detección de ataques pueden resolver. Dichas zonas de preocupación son:
  
-   Deteción de infracciones a directivas
  
-   Identificación de ataques externos
  
-   Implementación de análisis forenses
  
En este capítulo se describe cada ejemplo, mientras que el capítulo 4, "Diseño de la solución", muestra la forma de configurar la supervisión de la seguridad y el archivado para tratar estas amenazas.
  
Para identificar actividades anormales en una red es necesario saber lo que se considera normal en el entorno. Esta guía intenta distinguir entre el comportamiento normal y el inusual.
  
Para identificar anomalías también se necesita implementar una línea base segura en todos los equipos. Sin ella, no se pueden identificar los equipos que no cumplan los requisitos de la línea base. Para obtener más información sobre la forma de implementar líneas base seguras, consulte los [artículos con instrucciones](http://www.microsoft.com/technet/itsolutions/howto/default.mspx) para la seguridad en http://www.microsoft.com/technet/itsolutions/howto/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Detección de infracciones a directivas
  
Las infracciones a directivas representan la mayor categoría de problemas de seguridad con los que las organizaciones se tienen que enfrentar. En este tipo de infracciones, se incluyen las acciones siguientes:
  
-   Creación de cuentas de usuario fuera del proceso correcto
  
-   Uso de privilegios de administrador sin la autorización pertinente
  
-   Empleo de cuentas de servicios para inicios de sesión interactivos
  
-   Intentos de obtener acceso a archivos a los que un usuario no tiene permiso
  
-   Eliminación de archivos a los que el usuario tiene permiso de acceso
  
-   Ejecución de programas no autorizados
  
El tipo más habitual de infracción a directiva son los intentos no intencionados de acceso del usuario, como intentar abrir directorios no autorizados. Sin embargo, las restricciones de acceso y los derechos limitados, suelen evitar que los usuarios causen daños significativos en estos intentos. Las infracciones a directivas causadas por administradores, tanto deliberadas como accidentales, son un motivo de preocupación mucho mayor.
  
Los administradores de redes no confiables suponen una amenaza considerable para una organización. Estos usuarios necesitan elevados niveles de derechos y privilegios de acceso al sistema para realizar su trabajo. Los administradores pueden crear cuentas de usuario, restablecer contraseñas y cambiar la propiedad de archivos y carpetas. No obstante, por el hecho de que puedan efectuar un procedimiento, no significa que tengan autorización para ello. Los derechos de los administradores les permiten además ver recursos de red que no deberían ver, como los registros financieros.
  
#### Problemas empresariales
  
La mayoría de las organizaciones deben dar prioridad a la detección de infracciones a directivas debido a la probabilidad de que una de ellas ocurra y por el potencial que éstas tienen para producir daños. En el tratamiento de problemas empresariales con la detección y prevención de infracciones a directivas, se incluyen las instrucciones para:
  
-   Establecer la obligación de comprobaciones de antecedentes estrictas antes de contratar y a intervalos regulares durante el periodo de empleo.
  
-   Mantener comprobaciones de seguridad independientes de las acciones del administrador.
  
-   Realizar comprobaciones regulares del sistema de supervisión de la seguridad.
  
-   Identificar rápidamente infracciones de la seguridad.
  
-   Confirmar el alcance de la infracción de la seguridad.
  
-   Limitar el daño que causen las infracciones de la seguridad.
  
Las organizaciones empresariales suelen realizar comprobaciones de la seguridad pertinentes antes de que un nuevo empleado se les una. Sin embargo, muchas no continúan la supervisión para detectar si los usuarios internos muestran un comportamiento arriesgado.
  
Resulta fundamental que los usuarios internos firmen términos y condiciones explícitos que les alerten de los requisitos de supervisión de la seguridad de la red. Deben comprender que, si intentan abrir un archivo u obtener acceso a un recurso compartido al que no tienen permiso, los registros de seguridad mostrarán dicho intento. Los usuarios internos que trabajan con archivos de gran valor deben saber que los registros de seguridad realizarán un seguimiento cada vez que obtengan acceso a los mismos.
  
**Nota: **Cada vez es más difícil demandar o despedir a empleados sin pruebas de que eran plenamente conscientes de la supervisión de la seguridad interna y de las consecuencias de cualquier intento deliberado de obtener acceso a datos confidenciales o de destruirlos. Además, puede que los requisitos de protección de datos y la legislación de los derechos humanos exijan consentimiento explícito.
  
##### Responsabilidades independientes
  
Es recomendable que las organizaciones implementen una estricta separación de responsabilidades, de modo que los diferentes individuos o grupos, como el departamento de seguridad o de auditoría, estén a cargo de la inspección de las acciones de los administradores. Dicho grupo de inspección no debe tener permiso para realizar acciones que efectúen los administradores, para tener la garantía de que los inspectores no se convertirán en atacantes.
  
##### Pruebas de las funciones de supervisión
  
Las organizaciones deben efectuar pruebas regulares de las funciones de supervisión. Un método consiste en utilizar evaluaciones de penetración o una cuenta de administrador de prueba para garantizar el funcionamiento correcto de las alertas. Estas pruebas se deben producir en una programación irregular cada semana, con el fin de evitar que un atacante utilice la prueba de penetración como una oportunidad para actuar.
  
##### Definición de respuestas y procesos de seguridad
  
Con el objetivo de identificar rápidamente infracciones de la seguridad, una organización debe disponer de procesos completos que definan la forma de efectuar determinadas operaciones de red. Por ejemplo, puede utilizar un sistema de administración de identidades como Microsoft Identity Integration Server (MIIS) 2003 para crear (facilitar) cuentas de usuario. Aunque los administradores pueden crear cuentas de usuario directamente, la directiva organizativa especificaría que no deben hacerlo. De este modo, si el sistema de supervisión de la seguridad detecta el suceso 624 (creación de una cuenta de usuario), éste debe vincular con la cuenta suministrada de MIIS 2003 y no con la cuenta de un administrador individual.
  
Para limitar el daño que causan las infracciones de seguridad, una organización debe definir respuestas adecuadas a incidentes anticipados, como la rápida movilización del personal de seguridad interno. La velocidad y eficacia de las respuestas a incidentes pueden aportar una mejora significativa al perfil de seguridad de una organización, ya que, si los usuarios o administradores saben que, tras un incidente de seguridad, se produce una investigación exhaustiva, es menos probable que intenten infringir una directiva de seguridad.
  
Existe abundante cobertura informativa sobre las amenazas a las redes desde fuentes externas. Sin embargo, la experiencia demuestra que la probabilidad de riesgo o pérdida de datos debido a atacantes externos es significativamente inferior a la probabilidad de pérdida de datos porque los administradores de redes realizan una configuración incorrecta. Aunque no es recomendable ser complaciente con respecto a las amenazas externas, no se debe olvidar que muchas organizaciones desean vender soluciones que mantengan a los intrusos externos alejados de la red, puesto que es algo relativamente sencillo de conseguir. Por otro lado, nadie puede vender un paquete que evite que los administradores cometan errores o actúen malintencionadamente. 
  
#### Problemas técnicos
  
Para implementar un sistema funcional de supervisión de la seguridad y detección de ataques basado en el registro de sucesos de seguridad de Windows, se debe plantear la forma de:
  
-   **Administrar una elevada cantidad de sucesos de seguridad**. Para enfrentarse a elevados niveles de sucesos de seguridad, hay que considerar detenidamente qué configuración de auditoría de seguridad se debe habilitar. Este caso es especialmente útil para auditar el acceso a objetos y archivos, lo cual puede generar una elevada cantidad de datos.
  
-   **Almacenar y administrar numerosos sucesos en un repositorio central**. El almacenamiento de sucesos puede implicar la administración de terabytes de datos. Puesto que este requisito técnico es de mayor importancia para los análisis forenses, se trata de forma más detallada en la sección "Implementación de análisis forenses" incluida más adelante en este capítulo.
  
-   **Identificar patrones de ataques**. Para identificar firmas de ataques, se deben conocer los patrones de sucesos que indican que se ha producido uno. Siempre se debe responder de forma adecuada y oportuna en el momento en que una firma de ataque identifica una intrusión.
  
-   **Restringir administradores para que no puedan eludir los controles de auditoría de la seguridad**. Para impedir que los administradores burlen los controles de auditoría, se deben compartimentar las responsabilidades de los administradores y crear o asignar un grupo de especialistas en seguridad que supervise las auditorías de administradores.
  
#### Problemas de seguridad
  
La identificación de problemas de seguridad representa el tema central en un sistema de detección de ataques y supervisión de la seguridad. Para realizar una supervisión de la seguridad eficaz, se deben identificar las siguientes incidencias:
  
-   Intentos de obtener acceso a recursos a través de cambios en permisos de archivos
  
-   Intentos de obtener acceso a recursos a través de restablecimientos de contraseñas
  
-   Creación de usuarios
  
-   Colocación de usuarios en grupos
  
-   Uso de cuentas administrativas no autorizadas
  
-   Inicios de sesión en la consola que utiliza las credenciales de cuentas de servicios
  
-   Ejecución de programas no autorizados
  
-   Daño deliberado a archivos (no se incluyen los daños causados por errores de disco)
  
-   Introducción de sistemas operativos no autorizados
  
-   Creación o eliminación de relaciones de confianza
  
-   Inicios de sesión con una cuenta incorrecta, como una cuenta administrativa general
  
-   Cambios no autorizados en la directiva de seguridad
  
Para identificar estas acciones correctamente, debe tener en cuenta las secuencias de sucesos características y ser capaz de extraer dichas secuencias de otros sucesos de seguridad.
  
#### Requisitos de la solución
  
Para detectar infracciones en la directiva de seguridad y organizativa, la solución debe incluir:
  
-   Procedimientos de seguridad bien definidos que abarquen todas las operaciones de red.
  
-   Registros de auditoría de la seguridad completos.
  
-   Recopilación centralizada confiable de los registros de seguridad con filtros adecuados para el análisis.
  
-   Niveles ajustables de auditorías de seguridad.
  
-   Investigación de cualquier discrepancia, como omisiones, registros que faltan, etc.
  
Para identificar errores de configuración, la solución debe incluir:
  
-   Procedimientos de administración de cambios bien definidos (que incluyan validación) para cubrir todas las operaciones de red.
  
-   Registros de auditoría de seguridad eficaces.
  
-   Una recopilación centralizada confiable de los registros de seguridad.
  
-   Análisis automatizados de los registros de seguridad para identificar cambios en la configuración.
  
Para obtener más información sobre la forma de implementar una solución de este tipo, consulte el capítulo 4, "Diseño de la solución".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Identificación de ataques externos
  
Los ataques externos se producen de dos formas principales: ataques perpetrados por personas y los efectuados por aplicaciones malintencionadas. Ambos tipos tienen diferentes características y perfiles de amenaza. Los atacantes humanos pueden aprender detalles sobre la red de destino y modificar el ataque como sea pertinente, mientras que las aplicaciones malintencionadas pueden afectar a varios equipos y dejar puertas traseras para que las utilicen los atacantes.
  
Las aplicaciones malintencionadas incluyen varias amenazas posibles, como virus, gusanos y troyanos. Aunque estas aplicaciones pueden ser problemáticas y causar trastornos considerables, estos ataques son más sencillos de evitar que los perpetrados por personas.
  
**Nota: **Esta** **guía no incluye ninguna información sobre ataques que impliquen el uso de dispositivos de hardware, como, por ejemplo, capturadores de teclado en línea, ya que la supervisión de la seguridad no puede detectarlos.
  
#### Problemas empresariales
  
En esta guía, se tratan los problemas empresariales que surgen debido a ataques externos que intentan penetrar la red y que son detectables en el nivel de presentación o de aplicación. La supervisión de la seguridad no resulta especialmente útil para identificar un ataque de denegación de servicio distribuida (DDoS), aunque otros mecanismos, como los registros de Servicios de Internet Information Server (IIS), pueden identificar la duración, el tipo de paquete, la dirección IP aparente (probablemente falsa) y otros detalles del ataque DDoS.
  
La identificación de aplicaciones malintencionadas es de importancia considerable para las organizaciones de todos los sectores, aunque sobre todo para aquéllas que funcionan en el sector financiero o que deben cumplir normativas. Por ejemplo, ese tipo de organizaciones sienten más preocupación hacia la presencia de aplicaciones espía. Las aplicaciones espía pueden residir en un servidor o estación de trabajo y transmitir información confidencial a terceros externos.
  
Un problema empresarial importante con las aplicaciones malintencionadas es la inseguridad de que existan en una red. Un ejemplo especialmente inquietante es cuando el componente de software malintencionado es un rootkit o programa similar que toma el control absoluto de un equipo y, a continuación, enmascara el hecho de que a partir de ese momento un atacante lo controla. Es difícil tener la certeza de que los equipos no ejecutan tales aplicaciones malintencionadas, ya que puede que el rootkit tenga más destreza en ocultarse que la empresa en detectarlo.
  
#### Problemas técnicos
  
El aumento en la cantidad de ataques a las organizaciones es consecuencia de las acciones de atacantes sin experiencia que utilizan secuencias de comandos configuradas previamente para explotar vulnerabilidades. Mucho más peligro revisten los miembros del pequeño y dedicado conjunto de atacantes muy experimentados y capacitados (que también cooperan entre sí), que puede utilizar un conjunto de ataques diferentes para intentar penetrar una red.
  
**Nota: **En esta guía, un atacante es una persona que realiza un ataque deliberado; un virus, gusano o troyano que actúa por sí solo no es un atacante.
  
La principal forma de identificar aplicaciones malintencionadas es realizar el seguimiento de procesos. Al hacerlo, se identifica cada programa que se inicia o se detiene en una estación de trabajo o servidor. La desventaja que presenta es que genera una gran cantidad de sucesos, la mayoría de los cuales carecen de interés.
  
El análisis de procesos de los que se ha realizado un seguimiento puede ser difícil en las dos zonas siguientes:
  
-   **Servidores Web que utilizan CGI (Common Gateway Interface)**. Cada visita a la página crea un proceso.
  
-   **Estaciones de trabajo de desarrollo**. Las compilaciones de las aplicaciones crean numerosos procesos en un breve período de tiempo.
  
Estos factores pueden causar elevadas cantidades de sucesos en poco tiempo o crear muchos sucesos continuamente. En cualquier caso, se necesitan filtros eficaces que extraigan los sucesos de ataques diferenciándolos de los legítimos.
  
#### Problemas de seguridad
  
Los problemas de seguridad que causan los ataques externos son considerables, ya que los atacantes disponen de gran flexibilidad para elegir el método de intrusión en la red. Los atacantes externos pueden penetrar las redes a través de los siguientes mecanismos:
  
-   Intento de conseguir contraseñas
  
-   Cambio o restablecimiento de contraseñas
  
-   Explotación de vulnerabilidades
  
-   Engaño a un usuario para que ejecute una aplicación malintencionada
  
-   Uso de la elevación de privilegios para comprometer a equipos adicionales (lo que en inglés se denomina *island hopping*, saltos a otros sistemas)
  
-   Instalación de un rootkit o troyano
  
-   Uso de una estación de trabajo no autorizada
  
-   Uso de un ataque *phishing*, en el cual una dirección de correo electrónico fraudulenta dirige a un sitio Web malintencionado
  
El principal método para detectar atacantes y aplicaciones malintencionadas consiste en realizar un seguimiento de los procesos. Se necesita aplicar este método con mucha atención e integrarlo con directivas de restricción de software en Directiva de grupo. Tenga en cuenta que se deben definir directivas estrictas que estipulen qué programas se pueden ejecutar en los equipos dentro de las redes perimetrales.
  
**Nota: **Las directivas de restricción de software pueden provocar efectos no previstos en equipos portátiles o en entornos empresariales. Cree siempre objetos de directiva de grupo (GPO) para administrar las directivas de restricción de software y no aplique restricciones de software a través de la directiva de dominio predeterminada.
  
Para obtener más información sobre el uso de directivas de restricción de software, consulte el artículo [Using Software Restriction Policies to Protect Against Unauthorized Software](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx) en http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx.
  
#### Requisitos de la solución
  
Los requisitos de la solución para identificar a atacantes externos coinciden en parte con los necesarios para identificar amenazas internas. Entre estos requisitos, se incluyen:
  
-   Un método de defensa en profundidad para implementar la seguridad.
  
-   Registros de auditoría de seguridad eficaces.
  
-   Recopilación centralizada confiable de los registros de seguridad.
  
-   Análisis automatizados de los registros de seguridad para identificar firmas de ataques.
  
Los requisitos de la solución para detectar aplicaciones malintencionadas comparten algunos de los necesarios para identificar amenazas internas. Entre estos requisitos, se incluyen:
  
-   Procedimientos eficaces para auditar todo software no autorizado en la red.
  
-   Registros de auditoría de seguridad configurados correctamente.
  
-   Recopilación centralizada confiable y filtros de registros de seguridad.
  
-   Análisis automatizados de los registros de seguridad para identificar comportamiento sospechoso, con el uso de programas de terceros si es necesario.
  
Para obtener más información sobre la protección contra ataques de virus, consulte la [Guía de defensa en profundidad antivirus](http://www.microsoft.com/spain/technet/recursos/articulos/avdind_0.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/avdind\_0.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Implementación de análisis forenses
  
Se puede utilizar el análisis forense para realizar un seguimiento de la hora, la gravedad y las consecuencias de una infracción de la seguridad, así como para identificar los sistemas que los atacantes han puesto en peligro. El análisis forense debe registrar:
  
-   Hora del ataque
  
-   Duración del ataque
  
-   Equipos afectados
  
-   Cambios que el atacante realizó en la red
  
Dado que el análisis forense constituye un tema muy extenso, no se puede tratar completamente en esta guía. En concreto, esta guía no describe los requisitos de manipulación de pruebas de los análisis forenses ni la cobertura de fuentes de datos forenses, excepto el registro de sucesos de seguridad.
  
#### Problemas empresariales
  
El análisis forense difiere de otros ejemplos de solución en que investiga incidentes después de que hayan sucedido, en lugar de en tiempo real. El análisis forense debe proporcionar una lista detallada de todos los sucesos de interés en uno o varios equipos. El sistema de análisis debe poder administrar y archivar grandes cantidades de datos en una base de datos adecuada.
  
Una decisión empresarial clave es cuánto tiempo se deben conservar los datos forenses. Las organizaciones deben identificar la edad máxima de los mismos, tras la cual la información quedará anticuada. En la siguiente tabla se muestran los períodos de retención habituales de los datos forenses.
  
**Tabla 3.1: Límites de almacenamiento de análisis forenses**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Factores de almacenamiento</th>
<th style="border:1px solid black;" >Límite de almacenamiento</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Almacenamiento en línea (base de datos)</td>
<td style="border:1px solid black;">  21 días</td>
<td style="border:1px solid black;">Proporciona acceso rápido a los sucesos recientes</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento fuera de línea (copia de seguridad)</td>
<td style="border:1px solid black;">180 días</td>
<td style="border:1px solid black;">Límite razonable para la mayoría de las organizaciones</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Entorno normativo</td>
<td style="border:1px solid black;">    7 años</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Agencias de inteligencia</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;"> </td>
</tr>
</tbody>
</table>
  
**Nota: **Algunas organizaciones (como hospitales y organismos públicos) especifican límites en términos de "no mantener durante más de", en lugar de establecer un período de retención.
  
Una opción consiste en utilizar bases de datos en línea que retengan las tres últimas semanas de sucesos, a continuación, archiven los más antiguos en un formato de compresión elevada, como archivos de texto de variables separadas por comas (CSV), para su almacenamiento fuera de línea. Si es necesario, a continuación, se pueden importar estos archivos CSV a la bases de datos para su análisis.
  
Independientemente del sistema que utilice, asegúrese de que éste cumple con sus requisitos de investigación rápida de sucesos recientes, con la habilidad de recuperar sucesos más antiguos, si es necesario. La experiencia con sucesos de seguridad en el propio entorno debe servir de orientación sobre cuál es la mejor combinación de períodos de retención de datos para almacenamientos en línea y fuera de línea.
  
#### Problemas técnicos
  
La implementación de la supervisión de la seguridad para el análisis forense requiere el almacenamiento y la recopilación confiables de gran cantidad de sucesos. Los requisitos de supervisión de la seguridad en el cliente son similares a los expuestos para los otros ejemplos de solución, aunque requieren mucho más almacenamiento en base de datos y una administración de datos extremadamente eficaz.
  
Entre los retos técnicos se incluyen los siguientes factores:
  
-   Almacenamiento confiable y seguro de datos en línea
  
-   Disposición de gran cantidad de espacio en un disco de alto rendimiento para el almacenamiento en línea
  
-   Copia de seguridad confiable de sucesos antiguos en medios de almacenamiento
  
-   Administración del movimiento de copias de seguridad más antiguas a un almacén apropiado, en caso necesario
  
-   Restauración de información de copias de seguridad antiguas
  
Estos retos no son específicos de la supervisión de la seguridad, ya que los administradores de bases de datos tienen preocupaciones similares con aplicaciones como las bases de datos OLTP (procesamiento de transacciones en línea). No obstante, a diferencia de las OLTP y otras aplicaciones de bases de datos tradicionales, las de análisis forense deben enfrentarse a volúmenes mucho mayores de escrituras que de lecturas.
  
#### Problemas de seguridad
  
Normalmente, los datos recopilados para análisis forenses crecen continuamente. En pocas ocasiones, alguien, como el administrador de la seguridad empresarial, puede necesitar acceso a dicha información . Nadie más debe poder tener acceso a esa información, interrumpir su recopilación o modificarla. La seguridad de la base de datos debe ser completa, de forma que sólo uno o dos individuos de extrema confianza puedan obtener acceso a los datos de seguridad.
  
#### Requisitos de la solución
  
Los requisitos de la solución para implementar el análisis forense son los siguientes:
  
-   Registros de seguridad configurados correctamente
  
-   Comprobación segura de entradas en los registros de seguridad
  
-   Recopilación centralizada y segura de los registros de seguridad
  
-   Almacenamiento confiable de información de la supervisión de la seguridad
  
-   Mecanismos de archivado eficaces
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo, se han descrito los requisitos de la solución para los tres ejemplos incluidos en esta guía. El capítulo 4, "Diseño de la solución", explica la forma de incorporar estos elementos para crear el plan de detección de ataques y supervisión de la seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Diseño de la solución
  
[](#efaa)[Introducción](#efaa)  
[](#ezaa)[Elementos de la solución](#ezaa)  
[](#exaa)[Detección de infracciones a directivas](#exaa)  
[](#eyaa)[Identificación de ataques externos](#eyaa)  
[](#ewaa)[Implementación de análisis forenses](#ewaa)  
[](#evaa)[Resumen](#evaa)  
### Introducción
  
El paso final en la creación de un plan para un sistema de supervisión de la seguridad y detección de ataques consiste en elaborar el diseño de solución que cumpla los requisitos de la misma. Este diseño debe ir destinado a los problemas de los tres escenarios definidos:
  
-   Detectar infracciones a directivas
  
-   Identificar ataques externos
  
-   Implementar análisis forenses
  
Puesto que el objetivo principal de la solución es identificar y perfilar los ataques, en gran parte de este capítulo se explican los sucesos que pueden indicar que se está produciendo un ataque. Los perfiles de ataque guardan relación con los problemas de seguridad de cada uno de los escenarios que se abordan el capítulo 3, "Problemas y requisitos". La implementación exacta de esta solución variará según la topología de la red de la organización.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Elementos de la solución
  
El diseño de la solución utiliza los mismos componentes básicos para los tres escenarios. Aunque la implementación del análisis forense necesita recursos adicionales para el almacenamiento en línea, sin conexión y archivo, la arquitectura que presenta la solución no difiere en gran medida de la implementación de los otros dos escenarios.
  
#### Concepto de la solución
  
El concepto de la solución para la supervisión de la seguridad y la detección de ataques requiere que se examinen y planeen los niveles adecuados de auditorías de seguridad en las siguientes áreas:
  
-   Acciones de administración de cuentas, como crear usuarios y agregarlos a grupos
  
-   Acceso a archivos protegidos
  
-   Cambios en la directiva de seguridad
  
-   Creación y eliminación de confianzas
  
-   Empleo de derechos de usuario
  
-   Reinicios del sistema y modificaciones de la hora del mismo
  
-   Cambios en la configuración del registro
  
-   Ejecución de programas desconocidos
  
El sistema de supervisión de la seguridad y detección de ataques recopila información de los registros de sucesos de seguridad y la organiza de forma central. El administrador puede analizar estos datos para buscar actividades sospechosas. Asimismo, la información se puede almacenar y archivar para posteriores análisis forenses.
  
Un componente principal de esta solución es la habilidad de configurar auditorías por usuario, la cual es una característica de Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1) y Microsoft Windows® XP con Service Pack 2 (SP2). Las auditorías por usuario permiten especificar distintos niveles de auditoría para cuentas de usuario específicas, con niveles superiores para individuos sospechosos o cuentas confidenciales.
  
#### Requisitos previos de la solución
  
Los requisitos previos de la solución para la configuración de un sistema de supervisión de la seguridad y detección de ataques son:
  
-   Los servidores deben ejecutar Windows Server 2003 SP1 o posterior como parte de un dominio de servicio de directorio de Active Directory®.
  
-   Los equipos cliente deben utilizar Windows XP Service Pack 2 o posterior como miembros de un dominio Active Directory. 
  
**Nota:** Dado que los equipos de una red perimetral pueden ser miembros de un grupo de trabajo en vez de un dominio, no se pueden configurar dichos equipos con valores de Directiva de grupo de Active Directory. Sin embargo, se pueden utilizar directivas locales y archivos de plantilla para configurarlos.
  
En esta guía no se recomienda ninguna tecnología concreta para la organización central de los sucesos de seguridad, sino que se centra en la identificación de las firmas características de un ataque. Tras decidir un mecanismo de recopilación adecuado, se pueden utilizar los sucesos y las secuencias de sucesos que describe este capítulo para crear consultas que identifiquen ataques.
  
#### Planeamiento de la solución
  
Antes de implementar un sistema de supervisión de la seguridad y detección de ataques, se aconseja realizar lo siguiente:
  
-   Revisar la configuración de auditoría de seguridad actual
  
-   Evaluar las funciones de administrador y tareas de usuario
  
-   Revisar las directivas y los procedimientos organizativos
  
-   Identificar equipos vulnerables
  
-   Enumerar los activos más valiosos
  
-   Identificar las cuentas sospechosas o confidenciales
  
-   Enumerar los programas autorizados
  
Para obtener más información sobre los requisitos de almacenamiento, consulte la sección "Implementación de análisis forenses" incluida más adelante en este capítulo.
  
##### Revisión de la configuración de auditoría de seguridad actual
  
Las organizaciones deben revisar la configuración de su actual archivo de registros de sucesos de seguridad y auditoría de seguridad, a fin de ofrecer una línea base para los cambios recomendados en este capítulo. Con esta revisión, se debe obtener:
  
-   La configuración eficaz de la auditoría de seguridad actual.
  
-   El nivel al que se aplican estos valores (equipo local, sitio, dominio o unidad organizativa).
  
-   La configuración actual del archivo de registro (tamaño, comportamiento cuando se alcanza el tamaño máximo).
  
-   La configuración de auditoría de seguridad adicional que se aplica (por ejemplo, auditar el uso de privilegios de copia de seguridad y restauración).
  
Se puede utilizar el apéndice B, "Implementación de la configuración de Directiva de grupo" a modo de ayuda para identificar qué valores se necesitan registrar. Para obtener más información sobre la configuración de auditorías de seguridad, consulte la [Guía de seguridad de Windows Server 2003](http://www.microsoft.com/spain/technet/seguridad/recursos/guias/guia_ws2003.mspx) en http://www.microsoft.com/spain/technet/seguridad/recursos/guias/guia\_ws2003.mspx.
  
##### Evaluación de funciones de administrador y tareas de usuario
  
Un elemento clave para implementar una supervisión de la seguridad eficaz consiste en saber con toda seguridad quiénes son los administradores de la organización y qué funciones y responsabilidades tienen. Por ejemplo, la mayoría de las organizaciones incluye a los administradores en el grupo de administradores de dominio. En este grupo, pueden crear cuentas de usuario en el dominio. No obstante, las directivas organizativas pueden especificar que sólo el sistema de suministro pueda crear cuentas. En tal situación, si un administrador crea una cuenta de usuario, esa acción llamaría inmediatamente la atención.
  
Evaluar las tareas de usuario es más sencillo, ya que los usuarios tienen considerablemente menos acceso a los recursos de red que los administradores. Por ejemplo, puesto que no suelen tener acceso a los sistemas de archivos de los equipos de la red perimetral, es poco probable que sea necesario supervisar la actividad de los usuarios en dichos servidores.
  
##### Revisión de directivas y procedimientos organizativos
  
Las revisiones de los procedimientos organizativos se corresponden con la evaluación de las funciones y responsabilidades del administrador. Por ejemplo, el proceso de agregar usuarios a grupos requiere una revisión cuidadosa. Los departamentos deben establecer procedimientos para las solicitudes de cambio y definir métodos que las implementen. Si se agrega un usuario a un grupo fuera del proceso aprobado, se precisa una investigación.
  
##### Identificación de equipos vulnerables
  
Los equipos vulnerables son aquellos a los que, con toda probabilidad, un atacante externo intentará obtener primero acceso en la red de una organización. En la mayoría de los escenarios de ataque, estos equipos forman parte de la red perimetral.
  
Se recomienda llevar a cabo una revisión completa de todos los equipos vulnerables a fin de garantizar lo siguiente:
  
-   Se han aplicado todos los Service Packs y actualizaciones de seguridad.
  
-   Se han deshabilitado las cuentas de usuario y los servicios innecesarios.
  
-   Se han configurado los servicios para que se ejecuten en las cuentas Servicio local o Servicio de red siempre que se pueda.
  
-   Se han comprobado los servicios que se ejecutan con credenciales de cuentas de usuario (en particular, los que tienen derechos administrativos), para garantizar que necesitan cuentas de usuario.
  
-   Se han aplicado plantillas de directivas de equipos de alta seguridad.
  
**Nota: **Este proceso de revisión no es exclusivo de los equipos vulnerables. Las prácticas idóneas para la seguridad aconsejan aplicar estas comprobaciones a todos los equipos de la red.
  
Para obtener más información sobre la forma de ejecutar servicios con seguridad, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/spain/technet/security/guidance/serversecurity/serviceaccount/default.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/serviceaccount/default.mspx.
  
##### Lista de los activos más valiosos
  
Aunque con toda probabilidad una organización ya haya identificado sus activos más valiosos, puede necesitar formalizar este hecho como parte de una directiva organizativa; para ello, documentará dichos activos y la protección de los mismos. Por ejemplo, una empresa puede utilizar listas de control de acceso (ACL) y cifrado para almacenar registros financieros de forma segura en particiones del sistema de archivos NTFS. Sin embargo, la directiva organizativa debe identificar estos registros como archivos protegidos a los que los usuarios o administradores no autorizados no deben intentar obtener acceso. Éstos además deben conocer dicha restricción.
  
La organización debe, a continuación, investigar cualquier modificación realizada en la ACL de estos archivos protegidos. Los cambios de propiedad revisten particular importancia, ya que pueden indicar que un atacante ha intentado obtener acceso a un archivo sin la debida autorización. Puesto que estos cambios no suceden muy a menudo, detectarlos suele ser sencillo.
  
##### Identificación de cuentas sospechosas o confidenciales
  
Se deben revisar todas las cuentas confidenciales para identificar las que precisan niveles de auditoría más elevados. Entre esas cuentas, se incluyen la cuenta de administrador, todos los miembros de los grupos de administradores de organización, dominio y esquema, así como cualquier cuenta que los servicios utilicen para iniciar sesión.
  
Si se observa actividad sospechosa de un individuo, los requisitos de la directiva de seguridad deben exigir niveles de auditoría más elevados para esa persona. Para obtener más información sobre la forma de cambiar niveles de auditoría en cuentas de usuario, consulte la sección "Habilitación de auditorías selectivas", incluida más adelante en este capítulo.
  
##### Lista de programas autorizados
  
Debido a que los atacantes deben ejecutar programas para descubrir información sobre la red, la limitación de los programas que se puedan ejecutar en ella reduce extraordinariamente la amenaza de ataques externos. Se recomienda realizar una auditoría de todos los programas autorizados y considerar los desconocidos sospechosos. Microsoft Systems Management Server 2003 puede efectuar auditorías de software para entornos empresariales de gran tamaño.
  
**Nota: **Puede que sea necesario aplicar excepciones con algunos equipos, como las estaciones de trabajo de los desarrolladores, ya que los archivos ejecutables que ellos crean no se encuentran en la lista aprobada. Un método más seguro consiste en solicitar que los desarrolladores utilicen equipos virtuales sin conectividad a la red corporativa para desarrollar y probar programas.
  
#### Arquitectura de la solución
  
La solución para la supervisión de la seguridad y detección de ataques contiene varios componentes que se coordinan con el objetivo de proporcionar advertencias de seguridad. Entre estos componentes, se incluyen:
  
-   Controladores de dominio de Active Directory®
  
-   Infraestructura de correlación de sucesos
  
-   Estaciones de trabajo de supervisión y análisis
  
-   Base de datos de almacenamiento en línea
  
-   Medios de copia de seguridad
  
-   Almacenamiento a corto plazo en las instalaciones
  
-   Almacenamiento a largo plazo fuera de las instalaciones
  
Los controladores de dominio de Active Directory no constituyen un requisito estricto, porque se pueden configurar los niveles de auditoría de seguridad a través de los valores de seguridad locales. Sin embargo, la solución necesita Active Directory si se va a utilizar Directiva de grupo para implementar auditorías de seguridad.
  
#### Cómo funciona la solución
  
Los componentes en la arquitectura de la solución funcionan de la siguiente manera:
  
1.  El administrador utiliza la configuración de Directiva de grupo para aplicar los cambios necesarios en los niveles de auditoría. Para obtener una lista de la configuración recomendada de Directiva de grupo, consulte el apéndice B, "Implementación de la configuración de Directiva de grupo".
  
2.  Directiva de grupo propaga estos cambios a los equipos designados.
  
3.  El administrador aplica cambios en la directiva de seguridad local de los equipos que no forman parte del dominio, como los que están en la red perimetral.
  
4.  Los registros de sucesos de seguridad recopilan sucesos de acuerdo a la configuración en Directiva de grupo.
  
5.  El sistema de correlación de sucesos explora los registros de sucesos de seguridad a intervalos regulares y guarda esta información en una base de datos apropiada.
  
6.  Un administrador de seguridad puede analizar directamente la información en la base de datos o emplear utilidades como SysTrack 3 de Lakeside Software para identificar actividades sospechosas.
  
La implementación de la supervisión de la seguridad para análisis forense requiere que se realicen las acciones adicionales siguientes:
  
1.  El sistema de correlación de sucesos extrae los sucesos relevantes a intervalos regulares y los coloca en la base de datos en línea.
  
2.  El sistema de copias de seguridad en la base de datos en línea archiva y elimina los registros obsoletos de la misma a intervalos determinados previamente (normalmente a diario).
  
3.  El medio de copia de seguridad permanece en el almacenamiento a corto plazo del sitio durante el período especificado.
  
4.  A intervalos regulares (normalmente cada semana), un mensajero lleva el medio de copia de seguridad antiguo a las instalaciones externas para el almacenamiento a largo plazo.
  
5.  El administrador responsable de las operaciones de restauración efectúa una restauración de prueba al mes, para comprobar que las copias de seguridad todavía funcionan.
  
#### Habilitación de auditorías selectivas
  
Las nuevas características incluidas en Windows Server 2003 con Service Pack 1 permiten niveles de auditoría selectiva en las cuentas de usuario. Por ejemplo, se puede auditar la actividad de inicio y cierre de sesión para todas las personas, además de auditar toda la actividad de un usuario determinado. Asimismo, se puede auditar toda la actividad de cada persona, excepto de una cuenta de usuario concreta. Los niveles de auditoría selectiva permiten reducir la cantidad de sucesos de rutina que hay que filtrar para realizar un seguimiento de los individuos sospechosos. Se pueden auditar de forma selectiva cuentas de usuario exclusivamente, sin grupos de seguridad ni de distribución.
  
Use la utilidad de la línea de comandos **auditusr.exe** para implementar niveles de auditoría selectiva. Windows Server 2003 con SP1 y Windows XP con SP2 disponen de ella. Para obtener más información sobre la forma de configurar auditorías por usuario, ejecute **auditusr.exe /?** en el símbolo del sistema.
  
**Nota: **Las auditorías por usuario no pueden excluir sucesos de miembros del grupo de administradores integrado.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Detección de infracciones a directivas
  
El capítulo 3, "Problemas y requisitos", identifica que los usuarios internos en la organización representan las mayores amenazas a una red. Incluso las instituciones con los procedimientos de selección y contratación más estrictos no se deben permitir descuidarse en el control de los usuarios internos de más confianza. En este capítulo se incluye la mayoría de los escenarios de amenaza interna, junto con instrucciones sobre la forma de detectarlos.
  
Los errores no intencionados en la configuración de red o del sistema se suelen deber a acciones de administradores. Por ejemplo, un administrador que haya seguido un proceso de aprobación antes de implementar un cambio de configuración y que, a continuación, haya utilizado las credenciales de administrador correctas para iniciar sesión en una estación de trabajo visible para otros usuarios. En ese ejemplo, el administrador no ha intentado ocultar sus actos. Con factores tales como si un administrador intenta ocultar su actividad, se suele distinguir entre un sabotaje intencionado y errores de configuración accidentales.
  
**Nota: **La implementación de supervisión de la seguridad resulta mucho más eficaz si ya se ha creado e implementado un proceso de administración de cambios adecuado. Sin este proceso, es mucho más complicado comprobar que los cambios se han realizado a través de los procedimientos correctos, ya que no hay referencia para dicha comprobación.
  
La creación de perfiles de ataques para las infracciones a directivas se basa en la identificación de un suceso o secuencia de sucesos que puede indicar un ataque potencial. Se puede utilizar esta información con el sistema de correlación de sucesos para buscar firmas de ataques.
  
En la detección de infracciones a directivas, se incluyen las siguientes actividades:
  
-   Acceso a recursos a través de la modificación de permisos de archivos
  
-   Accso a recursos a través del restablecimiento de contraseñas
  
-   Creación, cambio o eliminación de cuentas de usuario
  
-   Inclusión de usuarios en grupos
  
-   Intento de utilizar cuentas no autorizadas
  
-   Inicio de sesión interactivo con credenciales de cuentas de servicios
  
-   Ejecución de programas no autorizados
  
-   Acceso a recursos no autorizados
  
-   Daño a archivos autorizados (no se incluyen los daños causados por errores de disco)
  
-   Introducción de sistemas operativos no autorizados
  
-   Obtención de credenciales de otros usuarios
  
-   Intento de eludir auditorías
  
-   Creación o interrupción de relaciones de confianza
  
-   Cambios no autorizados en la directiva de seguridad
  
#### Acceso a recursos a través de la modificación de permisos de archivos
  
Para ver archivos a los cuales no tienen permiso de lectura, los administradores cambian la propiedad del archivo y, a continuación, se agregan a sí mismos a la lista de permisos de lectura del mismo. En Windows Server 2003 y posterior, pueden ocultar esta acción si cambian la propiedad y los permisos al estado original.
  
Resulta contraproducente configurar la auditoría de acceso a objetos en todos los archivos, porque una actividad ilícita pasaría desapercibida entre el volumen tan elevado de sucesos. Sin embargo, se deben establecer niveles de auditoría de seguridad que comprueben todos los accesos o cambios en los archivos más valiosos y las carpetas que los contienen. Las entradas a ACL solas no representan una defensa apropiada ante el acceso no autorizado.
  
Para frustrar cualquier actividad ilegal con eficacia, se deben identificar los siguientes factores en todos los archivos de gran valor:
  
-   ¿A qué objetos se dirigió el intento de acceso?
  
-   ¿Qué usuario solicitó el acceso?
  
-   ¿Está el usuario autorizado a obtener acceso a dicho objeto?
  
-   ¿Qué tipo de acceso (lectura, escritura, de lista, etc.) intentó el usuario?
  
-   ¿Fue el resultado de la auditoría de suceso una operación correcta o incorrecta?
  
-   ¿Desde qué equipo intentó el usuario obtener acceso?
  
Puesto que el Visor de sucesos no proporciona suficientes valores de filtro para identificar esta información, se debe utilizar EventComb MT u otras utilidades de terceros para realizar este análisis.
  
En la siguiente tabla, se incluyen los sucesos de auditoría que pueden causar los cambios en los permisos de archivos. La categoría de auditoría es Acceso de objetos.
  
**Tabla 4.1: Sucesos de cambios de permisos de archivos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">560</td>
<td style="border:1px solid black;">Acceso otorgado a objeto existente</td>
<td style="border:1px solid black;">Estos sucesos muestran dónde un objeto ha dado acceso correctamente a una solicitud, como de lista, lectura, creación y eliminación. Compruebe los campos <strong>Id. de inicio de sesión principal</strong>, <strong>Nombre de usuario cliente</strong> y <strong>Nombre de usuario principal</strong> para detectar intentos no autorizados de cambiar los permisos de archivos. Compruebe el campo <strong>Accesos</strong> para identificar el tipo de operación. Este suceso sólo muestra que se solicitó u otorgó el acceso, no que el mismo tuvo lugar. El usuario que actúa es el <strong>usuario cliente</strong> (si está presente); de lo contrario, es el <strong>usuario principal</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">567</td>
<td style="border:1px solid black;">Se ha utilizado un permiso asociado con un identificador</td>
<td style="border:1px solid black;">Este suceso se produce en la primera instancia de un tipo de acceso (de lista, lectura, creación, entre otros) a un objeto. Para establecer una correlación con el suceso 560, compare los campos <strong>Id. de identificador</strong> de ambos sucesos.</td>
</tr>
</tbody>
</table>
  
#### Acceso a recursos a través de restablecimiento de contraseñas
  
Para restablecer contraseñas, debe siempre existir un marco aprobado. Los niveles de auditoría de seguridad configurados adecuadamente deben incluir los restablecimientos de contraseña en los registros de sucesos de seguridad e identificarlos cuando no sigan los procedimientos correctos.
  
En la siguiente tabla se incluyen los sucesos de auditoría que causan los restablecimientos de contraseñas. La categoría de auditoría es Administración de cuentas.
  
**Tabla 4.2: Sucesos de restablecimiento de contraseña**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">627</td>
<td style="border:1px solid black;">Intento de cambio de contraseña</td>
<td style="border:1px solid black;">Este suceso es consecuencia de una solicitud de cambio de contraseña en la que el usuario proporciona la contraseña original a la cuenta. Compare el <strong>nombre de cuenta principal</strong> con <strong>Nombre de cuenta de destino</strong> para determinar si el propietario de la cuenta u otra persona ha intentado cambiar la contraseña. Si el <strong>nombre de cuenta principal</strong> no es igual que <strong>Nombre de cuenta de destino</strong>, alguien que no es el propietario de la cuenta ha intentado cambiar la contraseña. En los equipos con Microsoft Windows Me o Windows NT®, es habitual ver <em>Anónimo</em> como la cuenta que solicita el cambio. Esto se debe a que puede que el usuario no se haya autenticado. No obstante, el solicitante tuvo que suministrar la contraseña antigua, por lo que no representa un riesgo de seguridad significativo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">628</td>
<td style="border:1px solid black;">Contraseña de cuenta de usuario establecida o restablecida</td>
<td style="border:1px solid black;">Registra si un usuario o proceso restablece la contraseña de una cuenta a través de una interfaz administrativa, como Usuarios y equipos de Active Directory, en lugar de a través de un proceso de cambio de contraseña. Únicamente las personas o procesos autorizados deben llevar a cabo este proceso, como el departamento de soporte o el restablecimiento de contraseña personalizado del usuario.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">698</td>
<td style="border:1px solid black;">Cambio de contraseña del modo de restauración de servicios de directorio</td>
<td style="border:1px solid black;">Registra si alguien intenta cambiar la contraseña del modo de restauración de servicios de directorio en un controlador de dominio. Compruebe la <strong>IP de la estación de trabajo</strong> y el <strong>nombre de cuenta</strong> e investigue de inmediato.</td>
</tr>
</tbody>
</table>
  
#### Creación, cambio o eliminación de cuentas de usuario
  
Siempre se debe cumplir el proceso establecido para crear una cuenta de usuario. En grandes organizaciones con sistemas de suministro automatizados, ese proceso puede implicar procesos lógicos empresariales de varios pasos que requieren que los administradores inicien sesión en un sitio Web para aprobar las creaciones de cuentas de los nuevos empleados. Incluso en pequeñas organizaciones, la creación de una cuenta de usuario en Active Directory debe ser resultado exclusivo de una solicitud oficial. A continuación, cada suceso que registre la creación de una cuenta de usuario se deberá corresponder con las solicitudes de esa creación. Un administrador no confiable puede crear con facilidad una cuenta de usuario verosímil para un empleado que no exista y, a continuación, utilizarla para accesos no autorizados y actividades malintencionadas.
  
Se recomienda también confirmar que sólo pase un breve intervalo de tiempo entre la creación de una cuenta de usuario y el momento en que ese usuario inicia sesión y cambia la contraseña. Si un nuevo usuario no inicia sesión en la nueva cuenta transcurrido un marco temporal determinado previamente, el sistema de suministro debe deshabilitar la cuenta y el representante de seguridad investigar el motivo del retraso.
  
Para utilizar supervisión de la seguridad y detección de ataques a fin de identificar problemas con cuentas de usuario, se deben configurar consultas que:
  
-   Busquen actividades de cuentas de red irregulares o inusuales.
  
-   Identifiquen a los administradores que se aprovechen de sus privilegios para crear o modificar cuentas.
  
-   Detecten patrones de actividades de cuenta que infrinjan las directivas de seguridad de la organización.
  
En la siguiente tabla se incluyen los sucesos que identifican cambios en cuentas de usuario. Todos los sucesos pertenecen a la categoría de auditoría Administración de cuentas.
  
**Tabla 4.3: Sucesos de cambio de cuenta de usuario**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">624</td>
<td style="border:1px solid black;">Creación de una cuenta de usuario</td>
<td style="border:1px solid black;">Sólo las personas y los procesos autorizados pueden crear cuentas de red. Examine el campo <strong>Nombre de usuario principal</strong> para detectar si una persona o un proceso autorizado ha creado una cuenta. Este suceso detecta además si algún administrador crea cuentas al margen de las directrices de las directivas organizativas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">630</td>
<td style="border:1px solid black;">Eliminación de una cuenta de usuario</td>
<td style="border:1px solid black;">Sólo las personas y los procesos autorizados pueden eliminar cuentas de red. Busque dichos sucesos y examine el campo de <strong>nombre de cuenta principal</strong> para detectar si alguien no autorizado ha eliminado cuentas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">642</td>
<td style="border:1px solid black;">Cambio de una cuenta de usuario</td>
<td style="border:1px solid black;">Este suceso registra los cambios realizados en las propiedades relacionadas con la seguridad de las cuentas de usuario que los sucesos del 627al 630 no tratan.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">685</td>
<td style="border:1px solid black;">Cambio de un nombre de cuenta</td>
<td style="border:1px solid black;">Compruebe que el <strong>nombre de cuenta principal</strong> se corresponde con una persona o proceso autorizado.</td>
</tr>
</tbody>
</table>
  
#### Inclusión de usuarios en grupos
  
Las prácticas idóneas para la seguridad recomiendan el principio de privilegios mínimos, lo cual quiere decir dar a los usuarios los mínimos derechos y permisos que necesitan para realizar las tareas. La mayoría de las cuentas de usuario debe ser sólo miembro del grupo de usuarios de dominio, junto con cualquier grupo de seguridad específica de la organización.
  
La inclusión de usuarios en grupos de seguridad, en especial los usuarios que tienen privilegios elevados, como administradores de organización, dominio o esquema, se debe producir únicamente de acuerdo a las directrices de la directiva y debe hacer uso de las cuentas o procesos establecidos y aprobados. Cualquier otro cambio se debe considerar sospechoso e investigar con mayor profundidad.
  
**Nota**: La pertenencia a un grupo de distribución no proporciona acceso a recursos de red, ya que estos grupos no son entidades principales de seguridad. No obstante, la pertenencia a determinados grupos de distribución puede crear otros tipos de problemas de seguridad. Por ejemplo, la inclusión accidental de cuentas de usuario en el grupo de distribución de vicepresidentes o directores podría causar que los usuarios recibiesen mensajes de correo electrónico que no son pertinentes dado su puesto.
  
En la siguiente tabla se incluyen los sucesos que identifican cambios en grupos. Todos los sucesos pertenecen a la categoría de auditoría Administración de cuentas.
  
**Tabla 4.4: Sucesos de cambio de pertenencias a grupos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">De 631 a 634</td>
<td style="border:1px solid black;">Cambios en grupo global habilitado de seguridad</td>
<td style="border:1px solid black;">Examine este suceso en grupos que tienen privilegios de acceso globales o amplios, como el grupo de administradores de dominio, con el objetivo de garantizar que no se produzcan cambios al margen de las restricciones de la directiva organizativa. El nombre del grupo está en el campo <strong>Nombre de cuenta de destino</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">De 635 a 638</td>
<td style="border:1px solid black;">Cambios en grupo local habilitado de seguridad</td>
<td style="border:1px solid black;">Examine este suceso en grupos como administradores, operadores de servidor y operadores de copia, para garantizar que no se produzcan cambios al margen de las restricciones de la directiva. El nombre del grupo está en el campo <strong>Nombre de cuenta de destino</strong>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">639
641
668</td>
<td style="border:1px solid black;">Cambios en grupo habilitado de seguridad</td>
<td style="border:1px solid black;">Estos sucesos indican otros cambios en un grupo, aparte de cambios de pertenencia, creación o eliminación. Se deben examinar estos sucesos en grupos con elevados niveles de privilegio, para garantizar que no se produzcan cambios al margen de las restricciones de la directiva. El nombre del grupo está en el campo <strong>Nombre de cuenta de destino</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">De 659 a 662</td>
<td style="border:1px solid black;">Cambios en grupo universal habilitado de seguridad</td>
<td style="border:1px solid black;">Examine grupos que tienen elevados niveles de privilegio, como administradores de organización o esquema, para garantizar que no se produzcan cambios al margen de las restricciones de la directiva. El nombre del grupo está en el campo <strong>Nombre de cuenta de destino</strong>.</td>
</tr>
</tbody>
</table>
  
#### Intento de utilizar cuentas no autorizadas
  
El ascenso del primer controlador de dominio de Active Directory en un bosque crea una cuenta de administrador que es miembro de los grupos de administradores de dominio y de organización. Esta cuenta requiere especial protección, porque es la única a la que el valor de bloqueo de cuenta no se aplica. Por todo ello, incluso con una directiva de bloqueo de cuentas establecida, esta cuenta es vulnerable a ataques de diccionario.
  
La supervisión de la seguridad debe identificar todo intento de iniciar sesión en esta cuenta de administrador, incluso si le han cambiado el nombre. Para obtener más información sobre la elevación de seguridad en cuentas administrativas, consulte la [Guía de planeamiento de la seguridad de las cuentas de administrador](http://go.microsoft.com/fwlink/?linkid=41307) en http://go.microsoft.com/fwlink/?LinkId=41307.
  
Los intentos de iniciar sesión en cuentas deshabilitadas o caducadas pueden indicar que un empleado anterior, temporal o contratista ha intentado obtener acceso a la red sin la autorización actual. Estos sucesos requieren investigación inmediata.
  
En la siguiente tabla se incluyen los sucesos que identifican el uso de cuentas no autorizadas. Los sucesos pertenecen a las categorías de auditoría Inicio de sesión de la cuenta e Inicio de sesión.
  
**Tabla 4.5: Sucesos de inicio de sesión no autorizado**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">528/540</td>
<td style="border:1px solid black;">Inicio de sesión correcto</td>
<td style="border:1px solid black;">Sospechoso si <strong>Nombre de cuenta de destino</strong> es igual a la cuenta de administrador predeterminada. Sin embargo, el suceso 528 ocurre con frecuencia con el uso operativo habitual.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">529</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: contraseña o nombre de usuario desconocido</td>
<td style="border:1px solid black;">Compruebe los intentos en los que <strong>Nombre de cuenta de destino</strong> sea igual al administrador o a la cuenta de administrador predeterminada con el nombre cambiado. Compruebe varios errores de inicio de sesión que estén debajo del umbral de bloqueos de cuenta.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">531</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: cuenta deshabilitada</td>
<td style="border:1px solid black;">Investigue siempre este suceso. Compruebe el valor de <strong>Nombre de cuenta de destino</strong> y <strong>Nombre de estación de trabajo</strong>. Este suceso puede señalar un intento de abuso por parte de anteriores usuarios internos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">532</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: cuenta caducada</td>
<td style="border:1px solid black;">Investigue siempre este suceso. Compruebe el valor de <strong>Nombre de cuenta de destino</strong> y <strong>Nombre de estación de trabajo</strong>. Este suceso puede señalar un intento de abuso por parte de usuarios internos temporales o contratistas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">576</td>
<td style="border:1px solid black;">Privilegios especiales asignados a un nuevo inicio de sesión</td>
<td style="border:1px solid black;">Este suceso aparece si un nuevo inicio de sesión obtiene privilegios que podrían facilitar acceso de administrador o alterar la pista de auditoría. Para establecer la correlación con el suceso 528 o 540, compare el campo <strong>Id. de inicio de sesión</strong> en los dos sucesos. El suceso 576 constituye una forma rápida de comprobar si una cuenta obtuvo la equivalencia de administrador en el momento de iniciar sesión. Este método es más sencillo que intentar calcular la pertenencia a grupo.</td>
</tr>
</tbody>
</table>
  
#### Inicio de sesión interactivo con credenciales de cuentas de servicios
  
Siempre que un servicio se inicia, debe presentar credenciales de inicio de sesión. En algunos casos, las cuentas de servicios pueden necesitar que una cuenta de dominio se conecte y ejecute servicios en equipos remotos. Algunas cuentas de servicios se deben ejecutar con credenciales de administrador o interactuar con el escritorio.
  
En Windows Server 2003 y posterior, se pueden iniciar algunas cuentas de servicios (como el Servicio de alerta) con el modificador **–LocalService**. Los servicios que necesitan conectividad de red pueden utilizar la cuenta Servicio de red, NT AUTHORITY\\NetworkService. Se deben comprobar todos los servicios que requieren cuentas de usuario, para asegurarse de que éstas utilizan contraseñas seguras. La supervisión de la seguridad debe confirmar que los sucesos de inicio de sesión en dichas cuentas se producen únicamente cuando se inicia el servicio correspondiente. Para obtener más información sobre la elevación de seguridad en cuentas de servicios, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/spain/technet/security/guidance/serversecurity/serviceaccount/default.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/serviceaccount/default.mspx.
  
La principal preocupación sobre la seguridad surge cuando una cuenta de servicio inicia sesión de forma interactiva en lugar de como un servicio. Este suceso puede ocurrir sólo si un intruso ha descubierto la contraseña a la cuenta de servicio e inicia sesión en la misma. Si esa cuenta de servicio tiene privilegios de administrador, el intruso tendrá considerable capacidad para interrumpir los servicios de red normales.
  
Se recomienda identificar todos los recursos a los que puede obtener acceso una cuenta de servicio. Por ejemplo, aunque, algunas veces, una cuenta de servicio puede tener un buen motivo para necesitar permisos de escritura en el directorio de un archivo de registro, no se trata de un caso normal. Las cuentas de servicios no deben obtener permisos sin explicación para tener acceso a datos de gran valor. Se deben investigar estrechamente las cuentas de servicios que puedan interactuar con el escritorio, ya que éstas ofrecen mayores oportunidades a los atacantes.
  
En la siguiente tabla se incluyen los sucesos que identifican el uso no autorizado de credenciales de cuentas de servicios. Los sucesos pertenecen a las categorías de auditoría Inicio de sesión de la cuenta e Inicio de sesión.
  
**Tabla 4.6: Sucesos de inicio de sesión con credenciales de cuentas de servicios**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">528</td>
<td style="border:1px solid black;">Inicio de sesión correcto: ataque de consola o Servicios de Terminal Server</td>
<td style="border:1px solid black;">Si un registro de sucesos muestra el suceso 528 con una cuenta de servicio o un sistema local con el <strong>tipo de inicio de sesión 2</strong>, se está produciendo un ataque, el atacante ha obtenido la contraseña a la cuenta de servicio y ha iniciado sesión en la consola. Si un registro de sucesos muestra el <strong>tipo de inicio de sesión 10</strong>, un atacante ha utilizado Servicios de Terminal Server para iniciar sesión. En cualquier caso, se debe iniciar la investigación de inmediato.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">534</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: no se permite el tipo de inicio de sesión</td>
<td style="border:1px solid black;">Compruebe <strong>Nombre de cuenta de destino</strong>, <strong>Nombre de estación de trabajo</strong> y el <strong>tipo de inicio de sesión</strong>. Este suceso indica un intento incorrecto de iniciar sesión de forma interactiva con credenciales de cuentas de servicios, cuando la configuración de Directiva de grupo impide que dicha cuenta lo haga.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">600</td>
<td style="border:1px solid black;">Se ha asignado un testigo principal a un proceso</td>
<td style="border:1px solid black;">Este suceso se produce cuando un servicio utiliza un cuenta con nombre para iniciar sesión en un equipo con Windows XP o posterior. Establezca la correlación con los sucesos 672, 673, 528 y 592.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">601</td>
<td style="border:1px solid black;">Usuario intenta instalar un servicio</td>
<td style="border:1px solid black;">Este suceso debería suceder en muy raras ocasiones, puesto que la instalación de servicios no es una acción corriente. Se debe investigar las operaciones correctas e incorrectas con este suceso.</td>
</tr>
</tbody>
</table>
  
#### Ejecución de programas no autorizados
  
Dado que los administradores son empleados de confianza, pueden instalar y ejecutar programas. Las organizaciones deben crear una lista de programas aprobados (y con licencia) y un proceso para aprobar nuevos programas. Además de realizar pruebas en los programas nuevos en segmentos de red aislados, los administradores no deben ejecutar ningún programa que no se incluya en la lista aprobada.
  
Las auditorías de seguridad en el seguimiento de procesos pueden identificar programas no autorizados. Sin embargo, el seguimiento de procesos genera varias entradas en el registro de seguridad, por lo que se debe asegurar que el número de sucesos no inunde el mecanismo de detección.
  
En la siguiente tabla se incluyen los sucesos que identifican el uso de programas no autorizados. Los sucesos pertenecen a la categoría de auditoría de seguimiento de procesos.
  
**Tabla 4.7: Ejecución de programas no autorizados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">592</td>
<td style="border:1px solid black;">Creación de un proceso</td>
<td style="border:1px solid black;">Busque nuevos procesos en <strong>Nombre de archivo de imagen</strong> y <strong>Nombre de usuario</strong>. Todos los procesos deben estar presentes en la lista de programas autorizados.<strong> </strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">602</td>
<td style="border:1px solid black;">Creación de un trabajo programado</td>
<td style="border:1px solid black;">Compruebe la autorización para ejecutar procesos programados en <strong>Nombre de destino</strong> y busque la correlación de sucesos con programas de tareas conocidos en el campo de <strong>hora de tarea</strong>.</td>
</tr>
</tbody>
</table>
  
#### Acceso a recursos no autorizados
  
Este caso requiere la identificación de errores de auditoría en el Id. de suceso 560. En la siguiente tabla se incluyen los sucesos que son consecuencia de accesos a recursos no autorizados. La categoría de auditoría es Acceso de objetos.
  
**Tabla 4.8: Sucesos de intentos de acceso a recursos no autorizados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">560</td>
<td style="border:1px solid black;">Acceso denegado a objeto existente</td>
<td style="border:1px solid black;">Supervise errores de auditoría. En el campo <strong>Nombre de objeto</strong>, está el recurso al que se ha obtenido acceso. Establezca la correlación con los campos <strong>Nombre de usuario principal</strong> y <strong>Dominio principal</strong>, o los campos <strong>Nombre de usuario cliente</strong> y <strong>Dominio cliente</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">568</td>
<td style="border:1px solid black;">Intento de crear un vínculo físico a un archivo auditado</td>
<td style="border:1px solid black;">Este suceso se produce cuando un usuario o programa intenta crear un vínculo físico a un archivo u objeto. Tras crear un vínculo físico, el usuario puede manipular un archivo dentro de sus propios derechos sin crear una pista de auditoría.</td>
</tr>
</tbody>
</table>
  
#### Daño a archivos autorizados
  
En este caso, un usuario daña deliberadamente archivos a los que tiene acceso, porque no le preocupan las consecuencias. Este tipo de comportamiento es sobre todo frecuente cuando la organización ha despedido a un usuario, pero el administrador no ha deshabilitado aún la cuenta del mismo.
  
Para reducir las oportunidades de tales sabotajes malintencionados, hay que establecer estrategias de eliminación eficaces y bien documentadas que deshabiliten inmediatamente la cuenta del usuario, con lo que éste queda fuera de sesión obligatoriamente.
  
#### Introducción de sistemas operativos no autorizados
  
Los administradores y usuarios pueden introducir sistemas operativos no autorizados en una red a través de los siguientes mecanismos:
  
-   Equipos domésticos conectados a la red
  
-   Sistemas operativos que se inician desde un CD
  
-   Reinstalación de Windows XP u otro sistema operativo Windows
  
-   Imágenes de Microsoft Virtual PC
  
Los sistemas operativos no autorizados pueden causar problemas importantes, como los siguientes:
  
-   Reducción de la protección de vulnerabilidades debido a actualizaciones de seguridad no aplicadas.
  
-   Direcciones IP duplicadas, donde el sistema operativo no autorizado tiene la misma dirección que otro equipo en la red.
  
-   Aumento de la vulnerabilidad a virus y demás software malintencionado.
  
-   Aumento de la probabilidad de daños en archivos.
  
-   Incremento de las llamadas al departamento de soporte.
  
-   Disminución de la productividad.
  
Las directivas organizativas pueden especificar si los usuarios que trabajan desde ubicaciones remotas se pueden conectar a la red corporativa a través de servicios de acceso remoto o redes privadas virtuales. Para obtener más información sobre la forma de asegurar que los equipos remotos cumplan las directivas de seguridad de la organización antes de conectarse a la red, consulte [Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft](http://go.microsoft.com/fwlink/?linkid=41307) en http://go.microsoft.com/fwlink/?LinkId=41307 (en inglés).
  
**Nota: **Algunas distribuciones de software de fuente abierta están disponibles en CD de inicio. Para iniciar uno de estos sistemas operativos, el usuario puede insertar el CD y reiniciar el equipo. Puede que la supervisión del registro de sucesos no pueda detectar esta incidencia, ya que el software de fuente abierta se ejecuta independientemente de Windows. Sin embargo, los intentos de inicio de sesión del usuario "raíz" en un entorno homogéneo podrían indicar la presencia de sistemas operativos no autorizados. La eliminación de unidades de CD de los equipos cliente puede solucionar este problema, aunque no siempre resulta práctico.
  
Los usuarios pueden además obtener un CD de instalación de Windows XP y reiniciar los equipos para volver a instalarlo. En tal caso, puede que la supervisión del registro de sucesos de otros equipos detecte intentos de inicio de sesión del usuario "Administrador" con un nombre de grupo de trabajo no identificado o el nombre predeterminado de "Grupo de trabajo".
  
Las imágenes de Virtual PC ofrecen una emulación completa del entorno del equipo en un equipo host. Esta emulación ejecuta su propio sistema operativo con un nombre de equipo, cuentas, pertenencias a dominios o grupo de trabajo, además de programas. La imagen del equipo virtual se puede iniciar, ejecutar y cerrar sin afectar el equipo host. También puede solicitar una dirección IP y obtener acceso a recursos de red corporativa. Las imágenes de Virtual PC suponen una amenaza, puesto que es poco probable que sean seguras, a menudo las contraseñas están en blanco o se pueden adivinar fácilmente. Un usuario que ejecuta una imagen insegura de Virtual PC puede asignar unidades a recursos compartidos de red o instalar componentes, como Servicios de Internet Information Server (IIS), los cuales poseen vulnerabilidades inherentes que Service Packs o actualizaciones de seguridad posteriores han solucionado.
  
Se recomienda configurar la supervisión de seguridad para que detecte:
  
-   Nombres de dominio, grupo de trabajo, equipo o usuario no reconocidos.
  
-   Direcciones IP duplicadas o fuera del intervalo.
  
-   Intentos de iniciar sesión con la cuenta de administrador predeterminada.
  
En la siguiente tabla se incluyen los sucesos que identifican el uso de sistemas operativos no autorizados. Los sucesos pertenecen a la categoría de auditoría de seguimiento de procesos.
  
**Tabla 4.9: Sucesos de ejecución de plataformas no autorizadas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">529</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: contraseña o nombre de usuario desconocido</td>
<td style="border:1px solid black;">Busque los intentos en los que <strong>Nombre de cuenta de destino</strong> es igual a Administrador y <strong>Nombre de dominio</strong> es desconocido, o <strong>Nombre de cuenta de destino</strong> es igual a raíz.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">592</td>
<td style="border:1px solid black;">Creación de un proceso</td>
<td style="border:1px solid black;">Busque nuevos procesos en <strong>Nombre de archivo de imagen</strong> y <strong>Nombre de usuario</strong>. Todos los procesos deben ser programas autorizados.<strong> </strong></td>
</tr>
</tbody>
</table>
  
**Nota: **A fin de garantizar una detección más confiable de rootkits, evalúe productos de terceros, como RootkitRevealer de Sysinternals o Blacklight de F-Secure. Para obtener más información sobre RootkitRevealer, consulte [RootKitRevealer](http://technet.microsoft.com/es-es/sysinternals/bb897445.aspx) en http://www.sysinternals.com/ntw2k/freeware/rootkitreveal.shtml (en inglés). Para obtener más información sobre Blacklight, consulte el comunicado de prensa [Revolucionaria tecnología BlackLight de F-Secure](http://www.f-secure.com/news/items/news_2005030701.shtml) en http://www.f-secure.com/news/items/news\_2005030701.shtml (en inglés).
  
#### Obtención de credenciales de otros usuarios
  
Una consecuencia no intencionada de una buena directiva de contraseñas (como el requisito de una determinada longitud y la obligatoriedad de cambios regulares) consiste en que los usuarios escriben sus contraseñas. Esta situación es especialmente evidente en entornos heterogéneos que tienen varios almacenes de identidades, que requieren que los usuarios inicien sesión varias veces.
  
**Nota:** Para obtener información sobre la administración de contraseñas en entornos heterogéneos, consulte los [Informes sobre administración del acceso y la identidad](http://technet.microsoft.com/es-es/security/bb977553.aspx) en http://www.microsoft.com/technet/security/topics/identity/idmanage/default.mspx (en inglés).
  
Las organizaciones se deben proteger contra usuarios que anotan sus contraseñas y las dejan a plena vista, ya que una persona no autorizada puede, a continuación, entrar en la oficina y encontrar con facilidad las credenciales de inicio de sesión del usuario. La supervisión de la seguridad debe detectar si un usuario inicia sesión en un equipo que normalmente no utiliza. La detección de este tipo de ataque requiere correlación cruzada de inicios de sesión correctos con nombres de estaciones de trabajo, además del acceso o la autorización del usuario a dichas estaciones de trabajo.
  
**Nota:** Active Directory permite controlar las estaciones de trabajo en las que el usuario puede iniciar sesión. Esta característica necesita soporte para la nomenclatura del sistema básico de entrada y salida de red (NetBIOS), por ejemplo, a través del Servicio de nombres Internet de Windows (WINS).
  
Los sucesos con estas incidencias son idénticos a los incluidos en la tabla 4.5, "Sucesos de inicio de sesión no autorizados".
  
#### Intento de eludir auditorías
  
Un atacante puede utilizar distintos métodos para evitar ser descubierto. Por ejemplo, un atacante puede cambiar la directiva de seguridad de un equipo o dominio, de modo que los registros de sucesos no muestren las actividades sospechosas, o puede borrar deliberadamente los registros de seguridad para que se pierdan los datos de auditoría. La detección de intentos de encubrir ataques puede resultar todo un desafío, ya que muchos de estos sucesos se producen con regularidad como parte de operaciones de red normales.
  
En la siguiente tabla se incluyen los sucesos que se identifican como probablemente causados por atacantes que intentan ocultar pruebas de infracciones a la seguridad. Estos sucesos pertenecen a varias categorías de auditoría.
  
**Tabla 4.10: Sucesos de elusión de auditoría**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">512</td>
<td style="border:1px solid black;">Se está iniciando Windows</td>
<td style="border:1px solid black;">Suele aparecer después del suceso 513. Investigue reinicios imprevistos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">513</td>
<td style="border:1px solid black;">Se está apagando Windows</td>
<td style="border:1px solid black;">Suele aparecer antes del suceso 512. Con equipos muy valiosos, el personal autorizado debe reiniciarlos de acuerdo a las directivas establecidas. Investigue inmediatamente cuando este suceso se produzca en cualquier servidor.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">516</td>
<td style="border:1px solid black;">Error de auditoría</td>
<td style="border:1px solid black;">Este suceso puede ocurrir si el búfer del registro de sucesos se inunda con demasiados sucesos de seguridad. Limite la cantidad de sucesos que auditar. Este suceso también se puede producir si configura que el registro de seguridad no sobrescriba. Se deben supervisar atentamente los equipos en áreas en donde es necesario mantener elevados niveles de registro de auditoría. La configuración de la seguridad puede provocar que algunos equipos se apaguen si los registros de seguridad se llenan. Supervise el suceso 516 en todos los equipos, si existe preocupación sobre la seguridad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">517</td>
<td style="border:1px solid black;">Borrado de registros de sucesos de seguridad</td>
<td style="border:1px solid black;">Los administradores no deben borrar los registros de sucesos de seguridad sin autorización. Compruebe <strong>Nombre de usuario cliente</strong> y <strong>Dominio cliente</strong>; a continuación, establezca una correlación cruzada con personal autorizado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">520</td>
<td style="border:1px solid black;">Cambio de la hora del sistema</td>
<td style="border:1px solid black;">Esta acción puede inducir a error en la investigación forense o proporcionar una coartada falsa a un atacante. El nombre del proceso es <strong>%windir %\system32\svchost.exe</strong>. Compruebe <strong>Nombre de usuario cliente</strong> y <strong>Dominio cliente</strong>; a continuación, establezca una correlación cruzada con personal autorizado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">521</td>
<td style="border:1px solid black;">No se pueden registrar sucesos</td>
<td style="border:1px solid black;">Windows no puede realizar entradas en el registro de sucesos de seguridad. Se debe investigar este suceso inmediatamente si sucede en equipos muy valiosos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">608</td>
<td style="border:1px solid black;">Se ha asignado un privilegio de cuenta de usuario</td>
<td style="border:1px solid black;">Esta acción garantiza un nuevo privilegio a una cuenta de usuario. El registro de sucesos incluye esta acción junto con el identificador de seguridad (SID) de la cuenta de usuario, no el nombre de ésta.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">609</td>
<td style="border:1px solid black;">Se ha quitado un privilegio de cuenta de usuario</td>
<td style="border:1px solid black;">Esta acción quita un privilegio de cuenta de usuario. El registro de sucesos incluye esta acción junto con el SID de la cuenta de usuario, no el nombre de ésta.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">612</td>
<td style="border:1px solid black;">Cambio en la directiva de auditoría</td>
<td style="border:1px solid black;">Este suceso no indica necesariamente un problema. No obstante, un atacante puede cambiar la directiva de auditoría como parte de un ataque al sistema informático. Se recomienda supervisar este suceso en controladores de dominio y equipos de gran valor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">621</td>
<td style="border:1px solid black;">Se ha otorgado acceso al sistema a una cuenta</td>
<td style="border:1px solid black;">Un usuario ha recibido acceso a un sistema. Compruebe <strong>Nombre de usuario</strong> y <strong>Cuenta modificada</strong>, sobre todo si el permiso de acceso es interactivo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">622</td>
<td style="border:1px solid black;">Se ha quitado el acceso al sistema de una cuenta</td>
<td style="border:1px solid black;">Este suceso puede indicar que un atacante ha quitado pruebas del suceso 621 o que intenta denegar servicio a otras cuentas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">643</td>
<td style="border:1px solid black;">Cambio de la directiva de seguridad de dominio</td>
<td style="border:1px solid black;">Este suceso indica un intento de modificar la configuración de la directiva de contraseñas u otra directiva de seguridad de dominio. Compruebe el nombre de usuario del sujeto y establezca la correlación con la autorización.</td>
</tr>
</tbody>
</table>
  
#### Creación o interrupción de relaciones de confianza
  
Las relaciones de confianza permiten que las cuentas de usuario en un dominio obtengan acceso a los recursos de red de otro dominio. Las relaciones de confianza transitivas bidireccionales automáticas abarcan todos los dominios dentro del mismo bosque de Active Directory. Puede que necesite crear manualmente relaciones de confianza en otras situaciones, como las siguientes:
  
-   Confianzas que incluyen dominios de Windows NT 4.0.
  
-   Confianzas de acceso directo entre dominios.
  
-   Confianzas entre dominios en bosques diferentes en Windows 2000 Server.
  
-   Confianzas entre bosques en Windows Server 2003.
  
La creación de relaciones de confianza no es una operación rutinaria que únicamente un administrador empresarial puede realizar a través de un proceso claramente definido, aprobado y establecido. De forma similar, un administrador empresarial sólo debe interrumpir relaciones de confianza tras un profundo análisis del efecto en la red y con referencia a un proceso claramente definido, aprobado y establecido.
  
En la siguiente tabla se incluyen los sucesos que identifican acciones en relaciones de confianza. Los sucesos pertenecen a la categoría de auditoría de cambios de directiva.
  
**Tabla 4.11: Sucesos de cambio en relaciones de confianza**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">610
611
620</td>
<td style="border:1px solid black;">Se ha creado, eliminado o modificado una relación de confianza con otro dominio</td>
<td style="border:1px solid black;">Estos sucesos aparecen en el controlador de dominio en el cual se ha creado el objeto de dominio de confianza. Este suceso debe generar una alerta y la investigación inmediata. Compruebe <strong>Nombre de usuario</strong> del sujeto que ha llevado a cabo la operación de confianza.</td>
</tr>
</tbody>
</table>
  
#### Cambios no autorizados en la directiva de seguridad
  
Sólo se deben producir cambios de las configuraciones de seguridad aprobadas en el marco de un conjunto de procedimientos y un proceso acordados. Se deben ver todos los cambios en las configuraciones de la seguridad fuera de este marco, ya sea como un error no intencionado del administrador o como sabotaje deliberado.
  
Entre los valores de la configuración de seguridad que no deben cambiar al margen de un marco definido, se incluyen:
  
-   Configuración de Directiva de grupo
  
    -   Directiva de contraseñas de cuentas de usuario
  
    -   Directiva de bloqueo de cuentas de usuarios
  
    -   Directiva de auditoría
  
    -   Valores del registro de sucesos que se aplican al registro de sucesos de seguridad
  
    -   Directiva IPSec
  
    -   Directivas de red inalámbrica (IEEE 802.11)
  
    -   Directivas de claves públicas, especialmente las que se aplican al sistema de cifrado de archivos (EFS)
  
    -   Directivas de restricción de software
  
-   Configuración de seguridad
  
    -   Asignación de derechos de usuario
  
    -   Directiva de contraseñas de cuentas de usuario
  
    -   Opciones de seguridad
  
Esta lista representa los requisitos mínimos. Probablemente, la mayoría de las organizaciones agregará más valores de Directiva de grupo. Se necesita configurar auditorías de seguridad para identificar los intentos correctos e incorrectos de cambiar estos valores. Se debe establecer una correlación de todos los intentos correctos con una cuenta de usuario que disponga de las autorizaciones pertinentes.
  
En la siguiente tabla se enumeran los sucesos que identifican cambios en directivas, tanto Directiva de grupo como directiva del sistema local. Los sucesos pertenecen a la categoría de auditoría de cambios de directiva.
  
**Tabla 4.12: Sucesos de cambios de directivas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">612</td>
<td style="border:1px solid black;">Cambio en la directiva de auditoría</td>
<td style="border:1px solid black;">Identifica todo cambio ocurrido en la directiva de auditoría. Establezca una correlación de este suceso con cambios que personal autorizado realice en la directiva del sistema.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">613
614
615</td>
<td style="border:1px solid black;">Cambio de la directiva IPsec</td>
<td style="border:1px solid black;">Supervise estos sucesos e investigue todas las incidencias aparte de inicios del sistema.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">618</td>
<td style="border:1px solid black;">Directiva de recuperación de datos cifrados</td>
<td style="border:1px solid black;">Si la directiva de recuperación de datos cifrados está en uso, supervise este suceso e investigue cualquier incidencia al margen de la directiva especificada.</td>
</tr>
</tbody>
</table>
  
Para obtener más información sobre los valores de Directiva de grupo, consulte el tema [Configuración de Directiva de seguridad](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/techref/en-us/w2k3tr_sepol_set.asp) en http://www.microsoft.com/resources/Documentation/windowsserv/2003/all/techref/en-us/W2K3TR\_sepol\_set.asp (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Identificación de ataques externos
  
Los ataques externos son el resultado de acciones de una persona o los efectos de programas malintencionados. Estos ataques se pueden solapar; por ejemplo, un troyano obtiene acceso a un equipo de escritorio y, a continuación, una persona se puede aprovechar directamente de esta situación.
  
Los atacantes externos intentan a menudo poner en peligro la seguridad a través de la elevación de privilegios hasta que obtienen acceso administrativo a uno o varios equipos. Este método se suele iniciar con una intrusión correcta a través de una cuenta de usuario que tiene privilegios limitados. A continuación, el atacante intenta obtener más privilegios; para ello, crea un proceso o servicio que se ejecute en el contexto del sistema. Más adelante, carga y ejecuta software que explore la red más a fondo (por ejemplo, herramientas que interceptan contraseñas o exploran paquetes de red).
  
Un atacante puede también intentar instalar un rootkit en un servidor. Los rootkits son componentes de software que toman control absoluto de un equipo y esconden su existencia de las herramientas de diagnóstico estándar. Puesto que los rootkits operan en un nivel muy bajo de hardware, pueden interceptar y modificar llamadas del sistema. No se puede detectar un rootkit mediante una búsqueda del ejecutable, ya que el rootkit se quita a sí mismo de la lista de resultados de la búsqueda. Las exploraciones de puerto no revelan que los puertos que el rootkit utiliza están abiertos, porque éste evita que la exploración los detecte. Por todo ello, una dificultad fundamental cuando se trata de solucionar problemas con rootkits es garantizar primero que ninguno exista.
  
Las aplicaciones de troyanos suelen ser menos complicadas de detectar que los rootkits, aunque pueden ser más destructivas. Los troyanos pueden ofrecer funcionalidad de control remoto, parecida a los rootkits, o puede simplemente destruir datos como haría un virus. La principal característica de un troyano es que, como su clásico homónimo, intenta engañar al usuario para que lo ejecute porque parece ser de utilidad.
  
La mayoría de los programas malintencionados no son tan flexibles o reactivos como un ataque humano. No obstante, se debe prestar especial atención a posibles mecanismos de entrega de virus, como el correo electrónico, que burlan la red perimetral. Los filtros estrictos para archivos adjuntos a mensajes de correo pueden ayudar a reducir este tipo de ataque.
  
Entre los ataques externos, se incluyen las siguientes categorías:
  
-   Intento de arriesgar las credenciales
  
-   Aprovechamiento de vulnerabilidades
  
-   Instalación de un rootkit o troyano
  
-   Engaño a un usuario para que ejecute un programa malintencionado
  
-   Acceso a un equipo no autorizado
  
#### Intento de arriesgar credenciales
  
Los atacantes utilizan varios métodos para obtener las credenciales de cuentas de usuario. El más conocido somete una única cuenta de usuario a un ataque de diccionario. En este caso, el atacante sólo conoce el nombre de una cuenta de usuario. Otro método consiste en aplicar el mismo conjunto de contraseñas a cada cuenta de usuario incluida en la base de datos de servicios de directorio. En este segundo caso, el atacante probablemente tenga acceso al servicio de directorio de la organización. Para detectar este tipo de ataque, se necesita supervisar los bloqueos de cuenta y varios errores de inicio de sesión en una serie de cuentas, incluso si el total de intentos de inicio de sesión está por debajo del umbral de bloqueo de cuentas.
  
Los cambios o restablecimientos de contraseña constituyen otra forma de obtener información de inicio de sesión de un usuario. Dado que el cambio o restablecimiento de contraseñas genera el mismo suceso con operaciones correctas e incorrectas, un atacante puede evitar ser descubierto si elude la directiva de bloqueo de cuentas. Una solución de supervisión de la seguridad debe identificar varios intentos de cambio o restablecimiento de contraseñas, en concreto los que se produzcan al margen del marco organizativo para estas operaciones.
  
El ciclo de contraseñas no supone un ataque, sino que ocurre cuando una secuencia de comandos iniciada por un usuario que pasa de forma cíclica a través de varias contraseñas cambia y permite que el usuario vuelva a una contraseña utilizada con anterioridad. El número de intentos de cambio de contraseña es igual al umbral de reutilización de contraseñas. Este escenario aparece como una rápida serie de sucesos 627, en los cuales el nombre de cuenta principal es igual al nombre de cuenta de destino. La implementación de una edad mínima de la contraseña hace que estos intentos de cambio resulten incorrectos.
  
En la siguiente tabla se incluyen los sucesos que son resultado de ataques que tienen como objetivo credenciales de usuario. No obstante, estos sucesos pueden también ocurrir como parte de operaciones normales de red o cuando los usuarios legítimos olvidan sus contraseñas.
  
**Tabla 4.13: Sucesos de ataques a credenciales de autenticación**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">529</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: contraseña o nombre de usuario desconocido</td>
<td style="border:1px solid black;">Compruebe los intentos en los que <strong>Nombre de cuenta de destino</strong> sea igual al administrador o a la cuenta de administrador predeterminada con el nombre cambiado. Compruebe varios errores de inicio de sesión que estén debajo del umbral de bloqueos de cuenta. Este suceso puede indicar que un individuo no autorizado intenta adivinar la contraseña del administrador local. Establezca la correlación del suceso 529 con el 539 para identificar un patrón de continuos bloqueos de cuenta.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">534</td>
<td style="border:1px solid black;">Inicio de sesión incorrecto: no se permite el tipo de inicio de sesión</td>
<td style="border:1px solid black;">Un usuario ha intentado iniciar una sesión con un tipo de inicio de sesión no permitido como, por ejemplo, de red, interactivo, por lotes o servicio. Compruebe <strong>Nombre de cuenta de destino</strong>, <strong>Nombre de estación de trabajo</strong> y el <strong>tipo de inicio de sesión</strong>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">539</td>
<td style="border:1px solid black;">Cuenta bloqueada</td>
<td style="border:1px solid black;">Un usuario ha intentado iniciar sesión en una cuenta que ya se ha bloqueado. Establezca la correlación con el suceso 529 para detectar un patrón de bloqueos continuos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">553</td>
<td style="border:1px solid black;">Ataque de reproducción detectado</td>
<td style="border:1px solid black;">Este suceso se produce cuando el paquete de autenticación (normalmente Kerberos) detecta un intento de iniciar sesión con la reproducción de las credenciales de un usuario. Investigue inmediatamente. Asimismo, esto puede ser señal de una configuración de red incorrecta.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">627</td>
<td style="border:1px solid black;">Intento de cambio de contraseña</td>
<td style="border:1px solid black;">Compare el <strong>nombre de cuenta principal</strong> con <strong>Nombre de cuenta de destino</strong> para determinar si el propietario de la cuenta u otra persona ha intentado cambiar la contraseña de cuenta. Si el <strong>nombre de cuenta principal</strong> no es igual que <strong>Nombre de cuenta de destino</strong>, alguien que no es el propietario de la cuenta intentó cambiar la contraseña.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">628</td>
<td style="border:1px solid black;">Contraseña de cuenta de usuario establecida o restablecida</td>
<td style="border:1px solid black;">Únicamente las personas o procesos autorizados, como el departamento de soporte o el restablecimiento de contraseña personalizado del usuario, deben llevar a cabo esta tarea. Investigue este suceso inmediatamente si no es ése el caso.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">644</td>
<td style="border:1px solid black;">Cuenta de usuario bloqueada automáticamente</td>
<td style="border:1px solid black;">Una cuenta de usuario se ha bloqueado porque el número de intentos de inicios de sesión secuenciales incorrectos es mayor que el límite para el bloqueo de cuenta. Establezca la correlación de este suceso con los sucesos 529, 675, 676 (sólo Windows 2000 Server) y 681. Consulte además la entrada en esta tabla para el suceso 12294.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">675</td>
<td style="border:1px solid black;">Error en la autenticación previa</td>
<td style="border:1px solid black;">Establezca la correlación con el suceso 529 para encontrar el motivo adicional para que el inicio de sesión haya sido incorrecto. Entre los motivos, se pueden encontrar sincronización de hora o cuentas de equipo que no se han unido al dominio correctamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">12294</td>
<td style="border:1px solid black;">Intento de bloqueo de cuenta</td>
<td style="border:1px solid black;">Este suceso indica un posible ataque de fuerza bruta contra la cuenta de administrador predeterminada. Puesto que esta cuenta no bloquea, los registros de sucesos del sistema muestran en su lugar el suceso 12294 de SAM. Investigue incluso una única incidencia de este suceso inmediatamente, puesto que puede también indicar la presencia de un sistema operativo no autorizado. Compruebe en el campo <strong>Nombre de dominio</strong> si hay dominios desconocidos.</td>
</tr>
</tbody>
</table>
  
#### Aprovechamiento de vulnerabilidades
  
Debido a que se pueden dar vulnerabilidades en cualquier equipo, los atacantes intentan aprovecharse de ellas para introducirse en la red de una organización. La protección idónea contra atacantes que intentan hacer esto consiste en definir un proceso de administración de revisiones eficaz que utilice Microsoft Systems Management Server 2003 o Microsoft Software Update Services.
  
Para obtener más información sobre la administración de revisiones, consulte [Administración de revisiones con Systems Management Server 2003](http://www.microsoft.com/spain/smserver/default.mspx) en http://www.microsoft.com/downloads/details.aspx?FamilyID=e9eab1bd-13e7-4e25-85c5-ce2d191c3d63 (en inglés) y [Administración de revisiones con Software Update Services](http://www.microsoft.com/spain/empresas/seguridad/articulos/dep_patches_sus_1_0.mspx) en http://www.microsoft.com/downloads/details.aspx?familyid=38d7e99b-e780-43e5-aa84-cdf6450d8f99 (en inglés).
  
La supervisión de la seguridad en la red perimetral resulta de especial importancia, ya que esos equipos son los más expuestos a un atacante. A menos que exista un mecanismo para detectar la posibilidad de un ataque, puede que las organizaciones no se den cuenta de que hay un problema hasta que un atacante ponga en peligro la red. La supervisión de la seguridad en los equipos de la red perimetral debe ser capaz de detectar un intervalo de sucesos.
  
Entre las incidencias normales de aprovechamiento de vulnerabilidades, se incluyen los intentos de acceso no autorizados y el uso de identidad con privilegios. En la siguiente tabla se aborda algunos de los sucesos que pueden identificar posibles ataques en los equipos.
  
**Nota: **Consulte la Tabla 4.13, "Sucesos de ataques a credenciales de autenticación", para ver sucesos adicionales que pueden identificar estos tipos de ataques.
  
**Tabla 4.14: Identificación de sucesos con aprovechamiento de vulnerabilidades a través de escala de privilegios**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">528
538</td>
<td style="border:1px solid black;">Inicio y cierre de sesión local</td>
<td style="border:1px solid black;">Los inicios de sesión local son operaciones muy poco habituales en equipos perimetrales. Establezca una correlación en el campo Id. de inicio de sesión. Investigue en caso de valores no previstos en <strong>Nombre de cuenta de usuario</strong>, <strong>Hora</strong> o <strong>Nombre de estación de trabajo</strong>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">576</td>
<td style="border:1px solid black;">Inicio de sesión con privilegios</td>
<td style="border:1px solid black;">En<strong> </strong>Windows Server 2003 con SP1 o posterior, este suceso indica un inicio de sesión de “administrador”: un inicio de sesión con suficientes privilegios para alterar la TCB (base de computación de confianza) o controlar el equipo. Con versiones anteriores de Windows, este suceso es de interés únicamente si contiene un privilegio conflictivo, como <strong>SeSecurityPrivilege</strong> o <strong>SeDebugPrivilege</strong>.</td>
</tr>
</tbody>
</table>
  
**Nota:** Las versiones de Windows anteriores a Windows Server 2003 incluirá el suceso 576 en la categoría Uso de privilegios. En Windows Server 2003 y posterior, la categoría Inicio de sesión también incluye este suceso. Por tanto, la configuración de los valores de auditoría con cada categoría causa la aparición de este suceso.
  
#### Instalación de un rootkit o troyano
  
Detectar la instalación de un rootkit a través de la supervisión de la seguridad es una tarea difícil, aunque no imposible. Un programa desconocido que se inicia y detiene en sucesiones rápidas puede indicar la presencia de un rootkit. Una vez iniciado un rootkit, el sistema operativo ya no lo puede detectar. Por tanto, el programa parece que se cierra y no genera más sucesos.
  
Los troyanos suelen ser más fáciles de identificar que los rootkits puesto que no poseen las características de ocultación de éstos. Los capturadores de teclado (programas que intentan registrar pulsaciones de teclas) también residen en esta categoría.
  
En la siguiente tabla se incluyen los sucesos que se pueden producir por instalación de un rootkit.
  
**Tabla 4.15: Sucesos de rootkit o troyano**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">592</td>
<td style="border:1px solid black;">Creación de un proceso</td>
<td style="border:1px solid black;">Busque nuevos procesos en <strong>Nombre de archivo de imagen</strong> y <strong>Nombre de usuario</strong>. Todos los procesos deben ser programas autorizados.</td>
</tr>
</tbody>
</table>
  
#### Engaño a un usuario para que ejecute un programa malintencionado
  
En este método, el atacante intenta eludir el firewall y la red perimetral para enviar un archivo ejecutable adjunto al usuario. Aunque el correo electrónico es el mecanismo de entrega más habitual, otras conexiones, como las establecidas con un sitio Web infectado, pueden lograr el mismo resultado.
  
El primer desafío del atacante es lograr que el usuario ejecute el programa. De hacerlo, el programa se inicia en el contexto de seguridad del usuario. A continuación, puede intentar escalar privilegios, por ejemplo para obtener la equivalencia de administrador o acceso a la red.
  
Para detectar intentos de inicio de programas, se puede configurar el seguimiento de procesos. Si se han establecido directivas de restricción de software para limitar los programas que un usuario puede ejecutar, los intentos de inicio de programas no autorizados crean un suceso de error de auditoría que se debe investigar. Motivos de especial preocupación los suponen los siguientes sucesos:
  
-   **Se generaron procesos como LocalSystem.** Los procesos que se ejecutan como LocalSystem deben estar bien definidos, normalmente como ejecutables de servicios, tales como **services.exe**. El suceso 592, por el cual el suceso muestra la presencia de alguna otra imagen ejecutable, exige una investigación más profunda.
  
-   **Se generaron procesos en horas no previstas.** Si el equipo no utiliza actividades programadas de procesos por lotes, como copias de seguridad, CGI o secuencias de comandos, se deben investigar más profundamente los procesos creados en horas inusuales (como por la noche). Busque incidencias del suceso 592.
  
La tabla 4.15, "Sucesos de rootkit o troyano", incluye los sucesos que se pueden producir si un atacante engaña a un usuario para que inicie una aplicación malintencionada.
  
#### Acceso a un equipo no autorizado
  
Cada vez más, los administradores utilizan utilidades de administración remota, como Servicios de Terminal Server, para conectarse con determinados equipos. Por este motivo, se recomienda controlar si se producen intentos de inicio de sesión interactivo en dichos equipos y comprobar la validez de los intentos de conexión. En esta comprobación, se incluye:
  
-   Identificar inicios de sesión que utilicen cuentas de servicios
  
-   Registrar intentos de obtener acceso a servidores con cuentas no autorizadas
  
-   Comprobar intentos para obtener acceso a servidores desde zonas geográficas no previstas
  
-   Enumerar intentos de obtener acceso a servidores desde un intervalo de direcciones IP externas
  
Este tipo de supervisión es particularmente importante con activos de gran valor, como registros financieros y de clientes. Se recomienda ubicar estos recursos en un servidor independiente y habilitar estrictas directivas que rijan quiénes tienen acceso a los mismos.
  
La supervisión de la seguridad debe indicar quién intenta establecer conexión con estos equipos y la organización debe establecer referencias cruzadas de esta información con la lista de usuarios autorizados. En la siguiente tabla se incluyen los sucesos que se originan por utilizar un equipo no autorizado.
  
**Tabla 4.16: Sucesos de uso de equipos no autorizados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Id. de suceso</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">528</td>
<td style="border:1px solid black;">Inicio de sesión correcto</td>
<td style="border:1px solid black;">Compruebe <strong>Nombre de estación de trabajo</strong> y, a continuación, <strong>Nombre de cuenta de usuario</strong>. Compruebe que <strong>Dirección de red de origen</strong> se encuentra en el intervalo de direcciones IP de la organización.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">530</td>
<td style="border:1px solid black;">Inicio de sesión correcto: restricciones de hora</td>
<td style="border:1px solid black;">Este suceso indica un intento de inicio de sesión fuera de las horas permitidas. Compruebe el valor de <strong>Nombre de cuenta de usuario</strong> y <strong>Nombre de estación de trabajo</strong>.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Implementación de análisis forenses
  
En el capítulo 3, "Problemas y requisitos", se explica en qué modo el análisis forense es en esencia diferente a la detección de infracciones a directivas y la identificación de atacantes externos. Aunque el análisis forense utiliza gran cantidad de los elementos que esta guía ya ha tratado, se centra en el análisis y el almacenamiento a largo plazo de los datos resultantes. A continuación, la mayoría de las investigaciones forenses continúan como si fueran una “lista de todos los sucesos para el usuario A” o una “lista de todos los sucesos desde el equipo B”.
  
La supervisión de la seguridad para el análisis forense requiere que la organización realice lo siguiente:
  
-   Seleccionar qué tipos de sucesos se almacenan
  
-   Calcular la cantidad prevista de sucesos al día
  
-   Determinar límites de tiempo para almacenamientos en línea, sin conexión y de archivo
  
-   Escalar la base de datos en línea para enfrentarse a los números de sucesos previstos
  
-   Especificar un sistema de copia de seguridad que se enfrente a la carga de sucesos diarios prevista
  
-   Decidir cómo se administra el sistema de almacenamiento
  
Existen tres factores principales que determinan el requisito de almacenamiento:
  
-   El número de sucesos que se necesita registrar
  
-   La velocidad a la que los equipos de destino generan estos sucesos
  
-   El tiempo que se necesita mantener la información disponible en línea
  
**Nota:** Un** **controlador de dominio con todas las categorías de auditoría habilitadas, excepto el acceso a objetos, puede producir alrededor de 3.000 sucesos de seguridad por hora. Con el almacenamiento de esta información en un archivo .CSV de Event Comb MT, se obtiene un archivo de 1 MB. El uso de auditorías de acceso a objetos y del seguimiento de procesos puede aumentar estas cifras considerablemente.
  
El resultado de los análisis puede ascender a requisitos de almacenamiento nada realistas. De ser así, se debe buscar un equilibrio entre la cantidad de equipos supervisados, los sucesos que se controlan y la duración que éstos se almacenan en línea antes de volver a ubicarse para el almacenamiento sin conexión.
  
En el apéndice A de esta guía, "Exclusión de sucesos innecesarios", se incluyen los sucesos que no facilitan información útil. Este apéndice pretende servir de ayuda para que se excluyan los sucesos que no agregan ninguna información de seguridad práctica.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Un sistema de supervisión de la seguridad y detección de ataques eficaz constituye un componente fundamental para mantener la integridad de la red. Para planear una solución de supervisión y detección de ataques basada en auditorías de seguridad de Windows, se precisa disponer de completos conocimientos de los objetivos del sistema. Asimismo, se requiere valorar con conocimientos los riesgos de amenaza ante los que la red es susceptible y las firmas de ataque relacionadas con cada tipo de amenaza.
  
Windows Server 2003 proporciona los componentes básicos para un sistema de supervisión de la seguridad y detección de ataques que utiliza registros de seguridad. Microsoft ofrece componentes basados en servidores, como Microsoft Operations Manager, y utilidades como Event Comb MT que pueden establecer correlaciones de los registros de sucesos de varios equipos y facilitar análisis de sucesos de seguridad. Los socios de Microsoft aportan herramientas y utilidades adicionales que permiten la rápida identificación de perfiles de ataque.
  
[](#mainsection)[Principio de la página](#mainsection)
  
##### Descargar
  
[![](images/Cc163158.icon_exe(es-es,TechNet.10).gif) Guía de planeamiento de supervisión de la seguridad y detección de ataques](http://www.microsoft.com/downloads/details.aspx?familyid=95a85136-f08f-4b20-942f-dc9ce56bcd1a&displaylang=en)
  
[](#mainsection)[Principio de la página](#mainsection)
