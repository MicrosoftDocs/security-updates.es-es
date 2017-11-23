---
TOCTitle: 'Guía de operaciones: Introducción a la guía de operaciones'
Title: 'Guía de operaciones: Introducción a la guía de operaciones'
ms:assetid: 'ddc3b305-8d31-4747-83b7-7dfab9dfea54'
ms:contentKeyID: 20112550
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458728(v=TechNet.10)'
---

Capítulo 10: Introducción a la guía de operaciones
==================================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#edaa)[Uso de la guía](#edaa)  
[](#ecaa)[Introducción a Microsoft Operations Framework](#ecaa)  
[](#ebaa)[Convenciones de diseño de las tareas](#ebaa)  
[](#eaaa)[Información adicional](#eaaa)  

### Uso de la guía

A diferencia de los capítulos anteriores, la guía de operaciones no se tiene que leer de principio a fin. Por lo tanto, tiene una estructura ligeramente distinta. Aunque los capítulos de la guía de generación normalmente sólo se utilizan durante la implementación, a los capítulos de la guía de operaciones se les hace referencia a lo largo de la vida de la solución. Es importante comprender el modo en que los capítulos de la guía de operaciones están estructurados para poder aprovechar al máximo la información que se incluye en ellos.

Los capítulos de esta guía se basan en la plantilla de la guía de operaciones de soluciones (SOG) diseñada por el equipo de Microsoft Solutions for Management (MSM). Cada SOG utiliza Microsoft Operations Framework (MOF) para analizar y clasificar todas las actividades necesarias para realizar el mantenimiento, ofrecer soporte y mejorar el funcionamiento de una solución durante su vida. En la siguiente sección se incluye una breve introducción a MOF, pero también debe consultar las referencias incluidas al final de este capítulo para obtener un conocimiento más exhaustivo del marco.

Cada capítulo está dividido en una sección de “lectura obligatoria” y una sección de referencia de mayor extensión. La sección de “lectura obligatoria” consta de los siguientes elementos:

-   Una lista de tareas de “configuración” de administración que se tienen que realizar para poner en práctica las operaciones, como, por ejemplo, el modo de configurar las copias de seguridad y la supervisión.

-   Una de las operaciones normales que se tienen que efectuar para mantener el funcionamiento de la solución. (En esta lista se incluyen cuestiones como renovar los certificados de entidad emisora.)

-   Instrucciones acerca de cómo asignar funciones operativas al personal de operaciones.

El resto del capítulo consta de los pasos detallados de las tareas operativas y de soporte a las que tendrá que hacer referencia. En la lista de tareas de configuración y operaciones normales mencionada anteriormente se hace referencia a tareas definidas en esta sección.

La sección de referencia de cada capítulo está organizada según las categorías de MOF, que se describen en la siguiente sección. A continuación se ofrece una sección breve acerca del diseño de cada tarea. Debe leerla antes de continuar en los capítulos 11 y 12.

[](#mainsection)[Principio de la página](#mainsection)

### Introducción a Microsoft Operations Framework

Los capítulos de la guía de operaciones que se ofrecen para esta solución se basan en Microsoft Solutions for Management (MSM). MSM proporciona una combinación de prácticas recomendadas, servicios de implementación de prácticas recomendadas y automatización de prácticas recomendadas para ayudar a los clientes a obtener excelentes resultados operativos, como demuestran el servicio de máxima calidad, la confiabilidad del sector, la disponibilidad, la seguridad y el bajo costo total de propiedad (TCO).

Las prácticas recomendadas se basan en Microsoft Operations Framework (MOF), con directrices para planear, implementar y mantener procesos operativos de TI que apoyen soluciones de servicio fundamentales.

MOF constituye un enfoque estructurado y flexible, basado en la IT Infrastructure Library (ITIL), que describe los procesos y las prácticas recomendadas necesarias para ofrecer soluciones de servicio fundamentales. En las siguientes secciones se ofrece una introducción a MOF y MSM.

Para comprender la estructura de esta guía y utilizarla de forma eficaz, debe entender el modelo de proceso de MOF y el modelo de equipo de MOF.

#### Modelo de proceso de MOF

El modelo de proceso de MOF se divide en cuatro cuadrantes. Cada cuadrante se ocupa de un aspecto del ciclo de vida del sistema: operativo, compatibilidad, optimización y cambio. Cada cuadrante, a su vez, consta de una serie de funciones de administración de servicio (SMF). Cada SMF se ocupa de una determinada área de actividad, como la administración de almacenamiento, la administración de incidentes o la administración de cambios. En la figura siguiente puede ver una representación gráfica del modelo de proceso de MOF.

[![](images/Dd458728.10fig10-1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458728.10fig10-1_big(es-es,technet.10).gif)

**Figura 10.1 Modelo de proceso de MOF**

##### Cuadrante operativo

El cuadrante operativo contiene todas las tareas necesarias para mantener un sistema en un estado de funcionamiento correcto, como, por ejemplo, efectuar copia de seguridad de los datos, supervisar el estado del servicio y la administración de directorios y seguridad. En esta sección encontrará todas las tareas del cuadrante operativo relacionadas con la solución, con las tareas operativas cotidianas y recomendaciones de control y supervisión. Estas dos áreas utilizan y aprovechan las secuencias de comandos incluidas en la solución.

##### Cuadrante de compatibilidad

El cuadrante de compatibilidad se ocupa de la administración de los problemas del sistema y la recuperación después de que se produzcan. Entre otras tareas, se puede mencionar la recuperación de servidores y servicios, el servicio de asistencia y el análisis y solución de los problemas. En el cuadrante de compatibilidad encontrará tareas relacionadas con la compatibilidad para la administración de la solución inalámbrica segura.

##### Cuadrante de optimización

El cuadrante de optimización se ocupa de cómo mejorar el servicio que ofrece el sistema. En esta sección encontrará información clave sobre funciones como el planeamiento de capacidades, la disponibilidad y la administración de continuidad.

##### Cuadrante de cambio

El cuadrante de cambio se encarga del planeamiento e implementación de los cambios del entorno. Contiene la administración de cambios y versiones, además de la administración de la configuración. Este cuadrante contiene el subconjunto más habitual de los cambios que puede efectuar en la infraestructura de la solución y una descripción de los procesos de cambios y versiones asociados a ellos. En el cuadrante también se describe la información que se debe mantener en un sistema de administración de la configuración.

#### Modelo de equipo de MOF

El equipo de modelo de MOF y los clústeres de funciones asociadas ofrecen directrices para garantizar que se asignan las personas adecuadas a las funciones operativas. Dichas funciones y equipos funcionales se muestran en la siguiente figura y se asignan al clúster de funciones de MOF al que, con toda probabilidad, se asignarían.

[![](images/Dd458728.10fig10-2(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458728.10fig10-2_big(es-es,technet.10).gif)

**Figura 10.2 Modelo de equipo de MOF**

Puede utilizar las descripciones del modelo de equipo de MOF anteriores para decidir quién se encargará de cada tarea en su organización y, después, dividir las tareas y responsabilidades entre todos los individuos involucrados en la administración de la infraestructura de claves públicas (PKI).

#### Implementación práctica de las funciones

El modelo de equipo de MOF define funciones que se agrupan en relación con las responsabilidades de los procesos de administración y no en función de las divisiones tecnológicas u organizativas. En organizaciones pequeñas, uno o dos miembros del departamento de TI pueden encargarse de todas las responsabilidades de estas funciones. Incluso en organizaciones de mayor tamaño, en las que existe una mayor especialización dentro del departamento de TI, puede no existir una correspondencia exacta entre las funciones de los procesos de MOF y las funciones del personal de TI.

En cada uno de los siguientes capítulos de la Guía de operaciones se definen las funciones administrativas y los grupos de seguridad correspondientes. Debe asignar las funciones y los grupos de seguridad al personal de su organización. Lea los procedimientos operativos definidos en los siguientes capítulos para evaluar qué personas de la organización se encargarán de dichas tareas.

Al realizar esta evaluación, no olvide lo siguiente:

-   Trate en todo momento de tener a más de una persona asignada a una función; de lo contrario, es probable que se produjeran problemas si la única persona asignada dejara la organización.

-   No utilice cuentas genéricas compartidas entre varias personas, ya que prácticamente no se podrían realizar controles de auditoría y responsabilidades.

-   Casi todos los profesionales de seguridad recomiendan que, como mínimo, la función de auditor sea independiente, aunque se combinen todas las demás funciones.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de diseño de las tareas

Todas las tareas documentadas en los capítulos de la guía de operaciones están clasificadas según el cuadrante de MOF y la clasificación de SMF descritos anteriormente. En el nivel máximo, las tareas están agrupadas por cuadrante y, a continuación en distintas SMF que componen el cuadrante. El orden de las tareas dentro de cada SMF y el orden de las SMF dentro de cada cuadrante no tienen especial importancia.

**Nota:** en esta guía no todas las SMF tienen tareas asociadas. Algunas SMF, como la administración de personal y financiera, se tienen que definir en el contexto de la organización.

Cada tarea tiene la siguiente estructura:

-   Nombre de tarea

-   Propósito de la tarea y breve descripción

-   Resumen de atributos de la tarea

-   Detalles de la tarea

El encabezado y el propósito de la tarea se explican por sí mismos. En el resumen de atributos de tarea se enumeran los requisitos de seguridad (en lo que se refiere a la pertenencia a grupos de seguridad), la frecuencia con la que se tiene que realizar la tarea y la tecnología y herramientas necesarias para llevar a cabo la tarea. A continuación se muestra un ejemplo:

**Información de resumen**

-   **Requisitos de seguridad:** cuenta con derechos para crear unidades organizativas en la parte designada del servicio de directorio de Active Directory®

-   **Frecuencia**: tarea de configuración

-   **Requisitos de tecnología**: complemento MMC de Management Console Usuarios y equipos de Active Directory

La sección de detalles de la tarea normalmente contiene el procedimiento paso a paso necesario para llevar a cabo la tarea. En algunas tareas (en concreto las de configuración), los detalles pueden contener información (como la descripción de los Id. de registro de sucesos) necesarios para realizar la tarea en vez de pasos de procedimiento.

[](#mainsection)[Principio de la página](#mainsection)

### Información adicional

-   Para obtener información adicional acerca de MSM, consulte la página [Plataformas más fáciles de administrar](http://www.microsoft.com/solutions/msm) en www.microsoft.com/solutions/msm.

-   Para obtener información general acerca de MOF, consulte la página [Microsoft Operations Framework](http://www.microsoft.com/mof) en www.microsoft.com/mof.

-   Para obtener información acerca de MOF, consulte el artículo [“Team Model for Operations”](http://technet.microsoft.com/es-es/library/bb232042.aspx) en www.microsoft.com/technet/itsolutions/techguide/mof/moftml.mspx.

-   Para obtener información general adicional acerca de las SMF del modelo de proceso de MOF, consulte los capítulos correspondientes de [*SMF Operations Guide*](http://technet.microsoft.com/en-us/solutionaccelerators/default.aspx) en www.microsoft.com/technet/itsolutions/techguide/msm/smf/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)