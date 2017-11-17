---
TOCTitle: Proceso de administración de revisiones
Title: Proceso de administración de revisiones
ms:assetid: 'd90522b7-21dd-4183-a81e-cfc05a0315dc'
ms:contentKeyID: 20200255
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc700840(v=TechNet.10)'
---

Proceso de administración de revisiones
=======================================

### Fase 3: Evaluación y planeación

Actualizado: junio 1, 2007

#### En esta página

[](#eyc)[Descripción del módulo](#eyc)
[](#edd)[Objetivos](#edd)
[](#epd)[Aplicable a](#epd)
[](#esd)[Uso del módulo](#esd)
[](#ege)[Información general](#ege)
[](#e4e)[Determinar la respuesta apropiada](#e4e)
[](#eaeac)[Planear el lanzamiento](#eaeac)
[](#eeiac)[Crear el lanzamiento](#eeiac)
[](#etiac)[Pruebas de aceptación](#etiac)
[](#eljac)[Resumen](#eljac)
[](#exjac)[Paso a la fase de implementación](#exjac)
Descripción del módulo
----------------------

En este módulo se describe la tercera fase, Evaluación y planeación, del proceso de administración de actualizaciones de cuatro fases. La fase de evaluación y planeación se centra en decidir si se implementará una actualización, determinar qué se necesita para implementarla y probar la actualización de software en un entorno similar al de producción con el fin de confirmar que no pone en peligro los sistemas y aplicaciones empresariales críticos.

El objetivo de este módulo es describir los principios de la fase de evaluación y planeación del proceso de administración de actualizaciones, así como presentar los tipos de tareas que permiten llevar a cabo la evaluación y planeación mediante Microsoft Windows Server Update Service (WSUS) y Microsoft Systems Management Server (SMS).

Nota: la versión beta 2 del próximo lanzamiento de SMS, denominada System Center Configuration Manager 2007, está disponible para su descarga en <http://www.microsoft.com/technet/sms/2007/evaluate/download.mspx>. Con excelentes mejoras en simplicidad, configuración, implementación y seguridad, Configuration Manager 2007 simplifica en gran medida la implementación del sistema, la automatización de tareas, la administración del cumplimiento de normativas así como la administración de la seguridad basada en directivas, lo cual permite la mejora de la agilidad empresarial.

Sin un proceso de evaluación y planeación, no dispondrá de un conjunto claro de criterios que le permita decidir si necesita llevar a cabo la implementación de una actualización, no sabrá lo que se necesita para implementar una actualización y no tendrá los procedimientos para crear un lanzamiento de software confiable y bien probado.

[](#mainsection)[Principio de la página](#mainsection)

Objetivos
---------

Use este módulo para:

-   Determinar si una implementación de actualización es realmente necesaria.

-   Planear el lanzamiento de la actualización de software.

-   Crear el lanzamiento.

-   Realizar pruebas de aceptación del lanzamiento.

[](#mainsection)[Principio de la página](#mainsection)

Aplicable a
-----------

Este módulo se aplica a todos los productos y tecnologías de Microsoft.

[](#mainsection)[Principio de la página](#mainsection)

Uso del módulo
--------------

Aunque las tareas básicas necesarias para realizar una evaluación y planeación mediante el uso de WSUS y SMS se describen en este módulo, puede encontrar instrucciones más detalladas en las bibliotecas técnicas indicadas a continuación.

Para obtener el máximo rendimiento de este módulo, debe realizar las siguientes acciones:

-   Lea el capítulo Introducción del módulo "Proceso de administración de actualizaciones". En este capítulo se ofrece información general de todas las fases del proceso de administración de actualizaciones de cuatro fases y se proporciona una introducción a las herramientas disponibles para aplicar la administración de actualizaciones en los entornos del sistema operativo Microsoft Windows.

-   Use las bibliotecas técnicas de WSUS y SMS para obtener materiales de referencia más detallados. Estas bibliotecas se encuentran en:

    -   [Biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)

    -   [Biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx)

[](#mainsection)[Principio de la página](#mainsection)

Información general
-------------------

La fase de evaluación y planeación es la tercera fase del proceso de administración de actualizaciones que se muestra en la figura 1.

![](images/Cc700840.secmod196figure1-0(es-es,TechNet.10).gif)

**Figura 1 El proceso de administración de actualizaciones**

En esta tercera fase, se evalúa la actualización de software y, en caso de que se apruebe para su implementación, se planea ésta en el entorno de producción.

El punto de entrada de la fase de evaluación y planeación es una solicitud de cambio (RFC) para una actualización de software que se ha identificado como relevante para su entorno de producción.

Al final de la fase de evaluación y planeación, debe haber determinado si la solicitud de cambio se puede clasificar como una emergencia, haber revisado y aprobado la solicitud y haber determinado las tareas necesarias para implementar los cambios aprobados en producción. También debe haber probado la actualización de software en un entorno similar al de producción con el fin de confirmar que no pone en peligro los sistemas y aplicaciones empresariales críticos.

Este módulo se centra en los requisitos clave para la evaluación y la planeación, que son:

-   Determinar la respuesta apropiada.

-   Planear el lanzamiento de la actualización de software.

-   Crear el lanzamiento.

-   Realizar pruebas de aceptación del lanzamiento.

[](#mainsection)[Principio de la página](#mainsection)

Determinar la respuesta apropiada
---------------------------------

La RFC determina la clasificación de los cambios necesarios en el entorno de producción, como implementar la actualización de software, aplicar contramedidas que mitiguen una vulnerabilidad o ambas acciones, y describe el cambio necesario de manera que otros puedan actuar sobre él.

El primer paso al evaluar y planear es revisar la RFC y determinar la respuesta más apropiada para una vulnerabilidad o amenaza de software. Esto incluirá:

-   Asignación de prioridad y categoría a la solicitud.

-   Obtención de autorización para implementar la actualización de software.

### Asignar de prioridad y categoría a una solicitud para una actualización de software

Antes de autorizar una solicitud para una actualización de software se debe determinar su prioridad y categoría. Aunque el iniciador de cambio asigna inicialmente la prioridad y categoría y se incluye en la RFC, estas asignaciones se deben comprobar, y aprobar o cambiar, para que se pueda autorizar la solicitud de cambio.

#### Asignar prioridad a una actualización de software

El nivel de prioridad es especialmente importante, ya que determina la rapidez con la que pasa la actualización de software por el proceso de cambio. Las siguientes consideraciones pueden ayudarle a determinar el nivel de prioridad de una actualización de software:

-   ¿Cuáles son los activos empresariales críticos? ¿Estarán expuestos a una posible infracción de seguridad o a la inestabilidad del sistema hasta que la actualización de software se instale? Debe dar prioridad a las solicitudes de cambio en función de la repercusión de la actualización de los activos de gran valor.

-   ¿Aplicará la actualización de software a un sistema que ejecuta un servicio empresarial crítico, como una aplicación de línea de negocios (LOB), que ha sido objetivo de ataques en el pasado? Ésta puede ser un buen motivo para aumentar la prioridad de una solicitud de cambio.

-   ¿Ha implementado contramedidas que deben minimizar la exposición de una vulnerabilidad de seguridad determinada? Esto puede disminuir la prioridad de la solicitud de cambio, aunque aún puede ser adecuado implementar la actualización de software con el fin de eliminar la vulnerabilidad.

-   ¿Cuál es la amenaza de la vulnerabilidad en cuestión para el entorno de producción? Muchos boletines de seguridad y actualizaciones de software relacionadas pueden aplicarse sólo a algunos equipos de su entorno. Si la amenaza de vulnerabilidad es baja, puede disminuir la prioridad de la solicitud.

Las siguientes tablas pueden ayudarle a valorar la prioridad de la solicitud en relación con otras solicitudes. En la tabla 1 se asignan niveles de prioridad para intervalos de tiempo recomendados y para intervalos de tiempo mínimos recomendados.

**Tabla 1: Prioridades de actualización e intervalos de tiempo de implementación recomendados**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Prioridad</th>
<th style="border:1px solid black;" >Intervalo de tiempo recomendado</th>
<th style="border:1px solid black;" >Intervalo de tiempo mínimo recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Emergencia</td>
<td style="border:1px solid black;">Antes de 24 horas</td>
<td style="border:1px solid black;">Antes de 2 semanas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Alta</td>
<td style="border:1px solid black;">Antes de 1 mes</td>
<td style="border:1px solid black;">Antes de 2 meses</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Media</td>
<td style="border:1px solid black;">Según la disponibilidad, implemente un nuevo Service Pack o conjunto de actualizaciones que incluya una revisión para esta vulnerabilidad antes de 4 meses.</td>
<td style="border:1px solid black;">Implemente la actualización de software antes de 6 meses</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Baja</td>
<td style="border:1px solid black;">Según la disponibilidad, implemente un nuevo Service Pack o conjunto de actualizaciones que incluya una revisión para esta vulnerabilidad antes de 1 año.</td>
<td style="border:1px solid black;">Implemente la actualización de software antes de 1 año, o bien, puede optar por no implementarla.</td>
</tr>
</tbody>
</table>
  
En la tabla 2 se proporcionan ejemplos de factores que pueden aumentar o disminuir la prioridad.
  
**Tabla 2: Factores que afectan a las prioridades de actualización**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Factor de entorno o de organización</th>
<th style="border:1px solid black;" >Ajuste de prioridad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Resultarán afectados activos de gran valor o exposición.</td>
<td style="border:1px solid black;">Aumento</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Activos que han sido objetivos de ataques en repetidas ocasiones.</td>
<td style="border:1px solid black;">Aumento</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Factores atenuantes aplicados, como contramedidas que minimizan la amenaza.</td>
<td style="border:1px solid black;">Más baja</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Resultarán afectados activos de poco valor o exposición.</td>
<td style="border:1px solid black;">Más baja</td>
</tr>
</tbody>
</table>
  
**Solicitud de cambio de emergencia**
  
Si la vulnerabilidad que la actualización de seguridad corrige ya se ha aprovechado o está por aprovecharse, o si la actualización corrige una inestabilidad del sistema que se encontró en el entorno de producción, debe clasificar la solicitud como una “emergencia” y proporcionar a esta solicitud una prioridad sobre todos los demás cambios que se suceden en el entorno de producción.
  
#### Asignar categoría a una actualización de software
  
La categoría de una actualización de software es importante, pues ayuda a quienes revisan el cambio a comprender la repercusión que tendrá en los sistemas y servicios en el entorno de producción. Con el fin de establecer la categoría (o repercusión) de la solicitud de cambio debe determinar:
  
-   En qué equipos debe instalar la actualización de software y las funciones (empresariales críticas) de dichos equipos.
  
    Por ejemplo, una actualización de software que requiera que se reinicie un equipo empresarial crítico tendrá una repercusión si se compara con una que no lo requiera.
  
-   Si se necesitarán cambios adicionales para admitir la implementación de la actualización de software.
  
    Si, por ejemplo, la actualización de software se aplica sólo al Service Pack actual y ese Service Pack no está instalado en algunos sistemas de producción, es posible que no se puedan proteger esos sistemas contra una vulnerabilidad de seguridad determinada. En este caso, la repercusión y, como consecuencia, la categoría de la solicitud de cambio deben ser mayores, ya que tanto el Service Pack como la actualización de software se deben implementar.
  
-   Si la actualización de software se puede desinstalar una vez se ha instalado.
  
    Si no es, representa un riesgo aún mayor para el entorno de producción que otra que se pueda quitar correctamente. Aunque puede ser necesario implementar dichas actualizaciones de software con el fin de proporcionar protección contra una vulnerabilidad de seguridad determinada o para atacar una inestabilidad específica del sistema, la categoría de la solicitud debe reflejarlo.
  
-   Las posibles repercusiones en la infraestructura de la red.
  
    Implementar una actualización de software muy grande en varios equipos simultáneamente puede degradar el rendimiento de la red y afectar de manera negativa al funcionamiento correcto de todo el entorno. Debe revisar atentamente todos los documentos de actualización de software y siempre debe conocer el tamaño de la actualización de software y la cantidad de equipos que la recibirán. Esta información puede ayudarle a programar correctamente el lanzamiento.
  
-   Si se deben detener, interrumpir o cerrar algunos servicios durante la instalación.
  
    Esto puede afectar a los servicios críticos de la organización o impedir que el usuario final trabaje en el equipo mientras se lleva a cabo la instalación.
  
Para obtener más información acerca de la configuración de la prioridad y categoría de una solicitud de cambio consulte la función de administración de servicios (SMF) Administración de cambios en <http://www.microsoft.com/technet/itsolutions/cits/mo/smf/default.mspx>.
  
### Obtener autorización para implementar la actualización de software
  
Una vez que se han asignado la prioridad y la categoría a la solicitud de cambio, se debe revisar y autorizar para que la actualización de software se pueda implementar en producción. Para obtener la autorización de la solicitud de cambio debe:
  
-   Determinar quién debe participar en el proceso de toma de decisiones.
  
-   Revisar la solicitud de cambio, evaluar los riesgos y consecuencias de implementar la actualización de software y seleccionar la acción más adecuada.
  
-   Identificar quién será responsable de implementar la actualización de software en todos los sistemas afectados.
  
#### Determinar quién debe participar
  
Es importante determinar quién debe participar en la revisión y autorización de una actualización de software para implementarla en producción. Para actualizaciones que no son emergencias, la revisión y la autorización las debe realizar un comité asesor de cambios (CAB), constituido por representantes de todas las áreas de la empresa que se verán afectadas.
  
Los miembros del comité deben ser personas que tengan experiencia en las tecnologías y servicios específicos que se usarán para implementar la actualización. En este grupo también se deben incluir representantes de la empresa, red, seguridad, departamento de servicios y equipos de soporte técnico.
  
Para obtener más información acerca de los comités asesores de cambios y cómo se pueden formar, consulte la SMF Administración de cambios, que se puede descargar de <http://www.microsoft.com/technet/itsolutions/cits/mo/smf/default.mspx>.
  
**Solicitud de cambio de emergencia**
  
Cuando se debe tomar una decisión rápida acerca de una solicitud crítica, una diseñada para cerrar una vulnerabilidad de seguridad o evitar un error crítico en el sistema, el comité de emergencia CAB (CAB/EC) debe conceder la autorización.
  
Un CAB/EC debe estar formado por personas que posean autoridad para aprobar cambios de emergencia y que estén disponibles para tomar decisiones rápidas. Puede encontrar más información acerca de CAB/EC en la SMF Administración de cambios, que se puede descargar de: <http://www.microsoft.com/technet/itsolutions/cits/mo/smf/default.mspx>.
  
#### Revisar la solicitud de cambio
  
Una vez que haya reunido a las personas apropiadas, debe evaluar los riesgos y la repercusión de la actualización de software en el entorno de producción y determinar si se debe implementar. Al tomar esta decisión, debe discutir los siguientes temas:
  
-   ¿Qué más va a suceder en el entorno de producción?
  
-   ¿Cuál es la repercusión de aplicar o no la actualización de software?
  
-   ¿Cuál es el costo anticipado de implementar o no la actualización de software?
  
-   ¿Qué pasos se deben dar, si los hubiera, para mitigar la exposición a una vulnerabilidad de seguridad o inestabilidad del sistema, mientras se está implementando la actualización de software?
  
-   ¿Cuál es la repercusión del tiempo de inactividad de los equipos? Será necesario comparar y tener en cuenta los riesgos de posponer la implementación de una actualización de software según los riesgos que se producirán en que incurrirá al ocasionar un tiempo de inactividad de los equipos cuando implemente una actualización de software en su entorno.
  
-   ¿Cuál será el mejor mecanismo y el más efectivo para implementar la actualización de software?
  
-   ¿Existen algunos problemas o efectos secundarios conocidos con la actualización de software y se necesita reiniciar el sistema?
  
-   ¿Existen suficientes recursos disponibles para implementar la actualización de software o para afrontar cualquier problema que se haya producido durante la implementación?
  
-   ¿Cómo abordará cualquier dependencia o requisito previo que se deba cumplir antes de que se pueda implementar la actualización de software?
  
Aunque la mejor respuesta a una vulnerabilidad de software es implementar la actualización de software que resuelva el problema, algunas veces puede ser preferible implementar una contramedida a corto plazo, como cerrar los puertos de red o desactivar el acceso externo a los sistemas, mientras se está ejecutando la actualización de software en los sistemas del entorno de producción. La aplicación de contramedidas puede tener algunas ventajas:
  
-   La mayoría de actualizaciones de software requiere que los equipos de destino se reinicien antes de terminar la instalación y el equipo esté protegido. Si se le ha advertido de que no implemente inmediatamente una actualización de software en su entorno pues los reinicios de su equipo están limitados a intervalos de mantenimiento específicos, implementar las contramedidas recomendadas puede proteger efectivamente su equipo hasta que la actualización de software se pueda implementar. Por otro lado, algunas veces las actualizaciones de seguridad se pueden implementar y se puede evitar el reinicio automático. En este caso, la actualización de seguridad se debe instalar durante el horario normal y el equipo se debe reiniciar en el momento adecuado durante el intervalo de mantenimiento.
  
-   Las contramedidas pueden tener un riesgo más bajo y se pueden aplicar más rápidamente con menos pruebas que la propia actualización de software. Puede ser considerablemente fácil, por ejemplo, deshabilitar los puertos de red o desactivar los servicios o sistemas que estén expuestos a una vulnerabilidad de seguridad determinada y aplicar la actualización de software más adelante.
  
La implementación de las contramedidas de protección del equipo con frecuencia puede proteger el equipo de numerosas vulnerabilidades de seguridad habituales. Bloquear algunos puertos de red y deshabilitar los servicios que no está usando son sólo dos de las contramedidas que, cuando se implementan, pueden proteger los equipos de manera efectiva.
  
Para obtener más información acerca de las contramedidas de protección de equipos, consulte la guía de amenazas y contramedidas en <http://www.microsoft.com/downloads/details.aspx?displaylang=en&familyid=1b6acf93-147a-4481-9346-f93a4081eea8>
  
**Nota:** incluso si se implementa una contramedida para reducir la exposición a una vulnerabilidad de seguridad, la actualización de seguridad debe programarse para la implementación.
  
Por ejemplo, si los sistemas permanecen en un estado no actualizado y un equipo que está infectado con un gusano o virus se introduce en la red, la infección se extenderá rápidamente a todos los sistemas desprotegidos. La implementación de las contramedidas simplemente debe disminuir la prioridad de la solicitud de cambio, en lugar de eliminar la necesidad de una actualización de software.
  
#### Decidir a quién se le asignará la implementación de la actualización de software
  
Una vez se haya llegado a un acuerdo para implementar la actualización de software y usar cualquier contramedida (si fuera apropiado), necesita identificar quién será el responsable de asegurarse de que se realicen estos cambios. Esta persona debe:
  
-   Desarrollar un plan para realizar los cambios necesarios.
  
-   Determinar y obtener los recursos necesarios.
  
-   Organizar el desarrollo de scripts, herramientas y documentos que sean necesarios para implementar los cambios.
  
-   Asegurarse de que se realizan las pruebas adecuadas.
  
-   Asegurarse de que los cambios se implementan en producción.
  
-   Evaluar el éxito o el fracaso de la implementación.
  
Sin un propietario designado que se encargue de supervisar las actividades anteriores, existe el riesgo de que la actualización de software no se implemente. El propietario designado es generalmente la función de Jefe de lanzamiento al que se hace referencia en la SMF Administración de versiones de lanzamiento en: <http://www.microsoft.com/technet/itsolutions/cits/mo/smf/default.mspx>.
  
[](#mainsection)[Principio de la página](#mainsection)
  
Planear el lanzamiento  
----------------------
  
La planeación del lanzamiento es el proceso de trabajar en el modo de lanzar la actualización de software en el entorno de producción.
  
Existen esencialmente tres etapas al planear el lanzamiento de una nueva actualización de software:
  
-   Determinar lo que se debe actualizar.
  
-   Identificar los problemas y limitaciones clave.
  
-   Crear el plan de lanzamiento.
  
### Determinar lo que se debe actualizar
  
Para decidir lo que se debe actualizar es necesario un conocimiento exacto y actualizado de lo que hay en el entorno.
  
En un entorno WSUS, es probable que los administradores necesiten examinar de nuevo con Microsoft Baseline Security Analyzer (MBSA) para establecer los sistemas que necesitan la actualización de software. Si se implementa SMS, la información que recuperan las herramientas de inventario y los agentes cliente se puede usar para determinar los equipos en los que se debe instalar la actualización.
  
Para obtener más información acerca de estas herramientas, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true) y la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).
  
### Identificar los problemas y limitaciones clave
  
Es probable que exista una serie de problemas y limitaciones que determine los pasos necesarios para implementar completamente la actualización de software en producción. Por ejemplo, cuando realice la tarea de implementar la actualización de software, debe tener en cuenta lo siguiente:
  
-   ¿Cuánto tiempo debe proporcionar a los usuarios antes de que la actualización de software se instale automáticamente? La cantidad de tiempo permitido dependerá de varios factores, incluidas las funciones y responsabilidades de los usuarios, así como la naturaleza de la inestabilidad del sistema o vulnerabilidad de seguridad para la que está diseñada la actualización de software.
  
-   En la figura 2 se muestra el ejemplo de una escala de tiempo de implementación de actualización de software (un contrato de nivel de servicio \[SLA\]), que indica los servidores que deben actualizarse a los siete días de la llegada de una actualización de software que no se considere crítica desde el punto de vista empresarial. Se otorga permiso a los administradores para iniciar la actualización en un período de siete días, pero deben saber que los equipos se actualizarán obligatoriamente o se desconectarán de la red una vez transcurra el período de tiempo.
  
    [![](images/Cc700840.secmod196figure2-0_l(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc700840.secmod196figure2-0(es-es,technet.10).gif)  
    **Figura 2 Ejemplo de SLA de implementación de actualizaciones para servidores**
  
Puede aplicarse una escala de tiempo de cumplimiento similar a estaciones de trabajo de su entorno, aunque variarán los tiempos y acciones de respuesta específicos.
  
-   Algunas actualizaciones de software requieren derechos administrativos en el equipo en donde se instalarán. La mayoría de usuarios finales no tienen derechos de administrador local, de manera que la herramienta que se usa para instalar la actualización de software debe ser capaz de adquirir derechos y privilegios altos a fin de instalar la actualización de software en los equipos cliente.
  
-   Si la actualización de software requiere un determinado espacio de disco para la instalación o si la actualización de software se debe almacenar en caché antes de la instalación, debe revisar la cantidad de espacio libre en el disco de cada equipo cliente.
  
-   Si la actualización de software es grande, por ejemplo, varios megabytes de tamaño, los clientes móviles tardarán algún tiempo en descargarla. Si la actualización de software no está clasificada como una emergencia, puede ser adecuado posponer la instalación en esos clientes hasta que estén físicamente conectados a la red.
  
-   Los equipos empresariales críticos pueden tener horas determinadas en las que se permiten los cambios y los reinicios de equipo (intervalos de interrupción). La implementación de una actualización de software y cualquier reinicio del sistema necesario se debe programar durante esos intervalos de interrupción.
  
-   Si los equipos cliente están bloqueados por el uso de una determinada configuración de directiva de grupo, se puede ver afectada la capacidad de la actualización de software para instalarse correctamente.
  
-   Si el producto que se va a actualizar se implementó con Windows Installer, es probable que Windows Installer requiera obtener acceso a los archivos de instalación originales. Estos archivos deben estar en la misma ubicación que se encontraban cuando se instaló originalmente el producto, si está realizando una instalación desatendida de la actualización de software. Si el producto se instaló originalmente desde un medio físico, por ejemplo, una unidad de CD, Windows Installer intentará encontrar los archivos originales en el CD que esté insertado.
  
-   Si se usó una imagen administrativa para la instalación original de un producto de Microsoft Office, por ejemplo, debe realizar una instalación administrativa de la actualización de software en la imagen en lugar de aplicarla directamente al cliente. Para obtener más información acerca de los problemas relacionados con la actualización de una imagen administrativa, consulte [/technet/prodtechnol/sms/sms2/depopt/smsoffxp.mspx.](http://www.microsoft.com/technet/prodtechnol/sms/sms2/depopt/smsoffxp.mspx)
  
-   Si existen aplicaciones que se instalaron por usuario, en lugar de por equipo para todos los usuarios, debe volver a instalar la aplicación por equipo y, a continuación, aplicar la actualización de software a la nueva instalación.
  
Si usa SUS y desea evitar la implementación fuera de los intervalos de interrupción, deberá usar objetos de directiva de grupo (GPO) para especificar que esas actualizaciones se deben descargar, pero no instalar. Cuando sepa que se ha descargado una actualización, debe iniciar sesión en cada servidor empresarial crítico e iniciar la instalación dentro del intervalo de interrupción permitido. Para estaciones de trabajo, también existe una configuración de GPO para garantizar que los equipos que han perdido una instalación programada (por ejemplo, porque el equipo cliente estaba apagado) volverán a programar de manera automática la instalación cuando se inicie el servicio de Actualizaciones automáticas al arrancar. Para obtener información más detallada acerca del uso de WSUS en la evaluación y planeación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true) y para obtener más información acerca de cómo usar SMS para programar la implementación, consulte la [biblioteca técnica para Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).
  
#### Solicitud de cambio de emergencia
  
Si tiene una solicitud de cambio que indique que la actualización de software es una emergencia, debe tener en cuenta los siguientes factores:
  
-   Puede que deba implementar la actualización de software en un tiempo considerablemente más corto de lo normal. La implementación completa, por ejemplo, se puede esperar en las 24 horas siguientes a la aprobación de la solicitud de cambio.
  
    En la figura 3 se muestra un SLA con una escala de tiempo de implementación de actualización de software. La escala de tiempo indica que todos los servidores se deben revisar en el plazo de ocho horas después de la recepción de una notificación de actualización de software importante.
  
    [![](images/Cc700840.secmod196figure3-0_l(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc700840.secmod196figure3-0(es-es,technet.10).gif)  
    **Figura 3 Ejemplo de un SLA de implementación de emergencia de ocho horas**
  
    En el ejemplo anterior, una vez que la organización conoce la actualización de software, la actualización de los servidores empresariales críticos debe empezar en un plazo de dos horas (12:00, tal como se muestra) con el 98% de todos los servidores adecuados al cumplimiento a las 18:00. El resto de servidores deben estar adecuados al cumplimento a las 22:00, de lo contrario existe el riesgo de desconexión de la red. Una escala de tiempo de cumplimiento similar se puede aplicar para las estaciones de trabajo de su entorno, aunque el intervalo de tiempo y la velocidad de respuesta pueden ser distintos para su organización.
  
-   Los intervalos de interrupción que determinan cuándo se pueden actualizar o reiniciar algunos sistemas empresariales críticos se deben reemplazar para permitir que la actualización de software se implemente en el intervalo de tiempo acordado.
  
-   Debe aplicar la actualización de software a todos los sistemas afectados, independientemente de su conexión a la red.
  
Si usa WSUS, puede emplear directivas de grupo para obligar a los clientes a instalar una actualización de software antes de un intervalo de mantenimiento programado regularmente. Antes de hacerlo, también debe asegurarse de que es forzosa una réplica en cualquier servidor WSUS secundario, que generalmente se programan para sincronizar las actualizaciones en los períodos tranquilos de la red, mediante el uso de la opción Sincronizar ahora en la página de administración del servidor WSUS. Para obtener más información acerca del uso de WSUS en la fase de evaluación y planeación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS).](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)
  
En un entorno SMS, debe configurar los emisores entre sitios SMS para permitir que los paquetes de alta prioridad y transacciones de anuncio se repliquen a todas horas del día. Es importante que el parámetro de alta prioridad sólo se use para paquetes y anuncios de actualización de software. Para obtener más información acerca del uso de SMS en la fase de evaluación y planeación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).
  
### Crear un plan de lanzamiento
  
Éste es el punto en el cual necesita planear y determinar el orden en que los equipos de su entorno de producción implementarán la actualización de software. A continuación se indican algunas de las cuestiones que debe tener en cuenta al crear el plan de lanzamiento:
  
-   Si la actualización de software se aplica a todos los servidores del entorno de producción, ¿deben actualizarse en primer lugar los servidores que ejecutan WSUS y SMS o herramientas de supervisión?
  
    La actualización de la infraestructura de administración garantiza, en primer lugar, que los administradores puedan usar estos servicios para supervisar el progreso de la implementación.
  
-   ¿Existe algún motivo empresarial por el que una parte del entorno de producción deba actualizarse antes que otra?
  
    Pueden existir motivos muy convincentes para aplicar la actualización de software a equipos que estén en riesgo debido a una vulnerabilidad de seguridad o posible inestabilidad del sistema, una vez estos equipos estén actualizados, continúe con la instalación en otro sitio.
  
-   ¿Qué repercusión tiene el ancho de banda de red disponible en el orden de instalación?
  
    Puede que sea difícil trasladar la actualización de software a algunos sitios de manera tan rápida como a otros debido a las limitaciones del ancho de banda de red. La actualización de software se puede implementar más rápidamente en sitios con buena conectividad de red que en otros en los que la disponibilidad de red es limitada.
  
Finalmente, necesita determinar cómo y cuándo la información sobre la actualización de software, su gravedad, repercusión y los pasos necesarios para implementarla, se comunicará a los usuarios, a la empresa y al departamento de servicios.
  
#### Solicitud de cambio de emergencia
  
En caso de que la solicitud de cambio sea una emergencia, debe tener en cuenta lo siguiente:
  
-   Si los componentes de arquitectura de administración como Microsoft Operations Manager (MOM), WSUS y los servidores de sitio SMS 2003 también se deben actualizar, puede ser apropiado planear la actualización manual de estos equipos, por parte de administradores locales, para asegurarse de que estos servidores no se reinicien durante la ejecución de la actualización de software en otros equipos en el entorno de producción.
  
-   Si un sitio o grupo de equipos ya ha sufrido una infracción de seguridad o inestabilidad del sistema que corrige la actualización de software, la implementación de actualización de software se debe dirigir primero a esos equipos una vez se han realizado los pasos de corrección adecuados (ejemplo: eliminación de virus. etc.).
  
[](#mainsection)[Principio de la página](#mainsection)
  
Crear el lanzamiento  
--------------------
  
Al contar con un plan de lanzamiento, la siguiente etapa del proceso es desarrollar los scripts, las herramientas y los procedimientos que los administradores usarán para implementar la actualización de software en el entorno de producción. Las tareas y actividades que se deben realizar en este momento dependerán principalmente de si la actualización de software se puede implementar mediante WSUS o SMS 2003.
  
Si usa WSUS, tenga en cuenta que las actualizaciones se descargan directamente de los servidores públicos de Windows Update y que ya están empaquetadas en un formato ejecutable (.exe), de manera que no necesita realizar ningún trabajo adicional para volverlas a empaquetar para su implementación. Para obtener más información acerca del uso de WSUS en la fase de evaluación y planeación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).
  
Si usa SMS, crear el lanzamiento es muy sencillo si la actualización se puede implementar mediante el uso del Asistente para distribuir actualizaciones de software de SMS 2003. Este asistente puede crear de manera automática el paquete SMS, así como el programa necesario para distribuir e instalar la actualización de software. Todas las actualizaciones de seguridad que se aplican a una combinación de paquete de producto y servicio determinada se pueden combinar a su vez en un paquete de ejecución de seguridad que simplifique el manejo y la administración y que reduzca de manera considerable el número de reinicios de equipo necesarios. Para actualizaciones que no se pueden implementar con el Asistente para distribuir actualizaciones de software de SMS 2003, debe usar los procedimientos de distribución de software estándar SMS a fin de crear un paquete y anuncio, especifique el archivo por lotes, el archivo de Microsoft Installer (MSI) o un ejecutable que se ejecutará en el equipo cliente y, si no se suministra la actualización con un ejecutable de instalación, también deberá crear un ejecutable mediante el uso de las herramientas de creación de MSI. Para obtener más información acerca del uso de SMS en la fase de evaluación y planeación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).
  
[](#mainsection)[Principio de la página](#mainsection)
  
Pruebas de aceptación  
---------------------
  
En este momento, el propósito de las pruebas ha sido confirmar que la actualización de software y el paquete de lanzamiento funcionen correctamente en un entorno de desarrollo.
  
La prueba de aceptación permite a los desarrolladores y representantes empresariales revisar que las actualizaciones funcionen en un entorno que refleja detalladamente la producción y que los sistemas empresariales críticos continuarán funcionando correctamente una vez que se implemente la actualización de software. Los administradores, junto con los representantes empresariales, deben elaborar un conjunto de pruebas que se aplique cuando una actualización de software se considere crítica para la empresa y un conjunto de pruebas más detallado que se pueda usar cuando la actualización de software tenga una prioridad más baja.
  
No importa lo crítica que sea la actualización, siempre debe realizar un nivel mínimo de pruebas para demostrar que:
  
-   Una vez completada la instalación, el equipo se reiniciará según está diseñado para hacerlo.
  
-   La actualización de software, si está destinada para equipos conectados en conexiones de red lentas o poco confiables, se puede descargar mediante estos vínculos y, una vez se termine de descargar se instala con éxito.
  
-   La actualización de software se suministra con una rutina de desinstalación, que se puede usar para eliminar correctamente la actualización de software.
  
-   Los sistemas y servicios empresariales más importantes siguen ejecutándose una vez que la actualización de software se ha instalado.
  
Antes de implementar la actualización de software en producción, es importante recopilar información acerca de cualquier paso de solución de problemas, procedimientos y herramientas que se usan durante las pruebas y ponerlas a disposición del personal del departamento de servicios y el equipo de operaciones.
  
Debe esperar que la prueba dará como resultado la creación de:
  
-   Artículos de base de conocimientos interna que describan los pasos de solución de problemas estándar, junto con cualquier solución relacionada.
  
-   Una lista de contactos y una ruta de transferencia de incidencias.
  
-   Los scripts, reglas e información como (contadores, eventos y umbrales), que permitirán a su equipo de operaciones controlar efectivamente el lanzamiento en producción.
  
No importa cuántas pruebas realice, instalar una actualización de software en producción con frecuencia produce efectos que nunca se pueden anticipar o replicar en un entorno de laboratorio. Para evitar afectar a un gran número de equipos cliente con un error potencial, los administradores deben plantearse la posibilidad de ejecutar la actualización de software en una pequeña muestra representativa de equipos y confirmar que los sistemas y aplicaciones empresariales más importantes continúan ejecutándose, antes de implementarla en toda la organización.
  
[](#mainsection)[Principio de la página](#mainsection)
  
Resumen  
-------
  
Aspectos clave que debe recordar en la fase de evaluación y planeación:
  
-   Necesita un proceso formal para determinar si la implementación de una actualización de software beneficia a la empresa.
  
-   Debe contar con un propietario identificado de la actualización de software que sea responsable de garantizar que se implemente.
  
-   Una vez aprobada una actualización de software, debe planear cómo aplicarla en producción.
  
-   Debe probar el paquete en un laboratorio y, si fuera necesario, realizar una prueba piloto en un entorno de producción para confirmar que no se ponen en peligro las aplicaciones de la LOB.
  
[](#mainsection)[Principio de la página](#mainsection)
  
Paso a la fase de implementación  
--------------------------------
  
El activador para el paso a la fase de implementación del proceso de administración de actualizaciones es que:
  
-   El paquete está listo para la implementación en producción.
  
-   Ha recibido la aprobación para implementar la actualización de software en el entorno de producción. Para obtener más información acerca de la fase de implementación, lea el módulo "[Fase 4 de la administración de actualizaciones: implementación](http://wwwppe/spain/technet/security/guidance/patchmanagement/secmod197.mspx)".
  
**Descargar la solución completa**
  
[Administración de revisiones con SMS 2003](http://www.microsoft.com/downloads/details.aspx?familyid=e9eab1bd-13e7-4e25-85c5-ce2d191c3d63&displaylang=en)
  
[](#mainsection)[Principio de la página](#mainsection)
