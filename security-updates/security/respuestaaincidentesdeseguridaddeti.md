---
TOCTitle: Respuesta a incidentes de seguridad de TI
Title: Respuesta a incidentes de seguridad de TI
ms:assetid: '916b5e5a-9d9e-42f3-b6f4-d1961baecc35'
ms:contentKeyID: 20200235
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc700825(v=TechNet.10)'
---

Respuesta a incidentes de seguridad de TI
=========================================

#### En esta página

[](#ehaa)[Introducción](#ehaa)  
[](#egaa)[Antes de comenzar](#egaa)  
[](#efaa)[Minimización de la cantidad y gravedad de los incidentes de seguridad](#efaa)  
[](#eeaa)[Creación de un CSIRT principal](#eeaa)  
[](#edaa)[Definición de un plan de respuesta a incidentes](#edaa)  
[](#ecaa)[Contención de daños y minimización de riesgos](#ecaa)  
[](#ebaa)[Información relacionada](#ebaa)

### Introducción

¿Qué preparación tiene su departamento o administrador de tecnologías de la información (TI) para tratar con incidentes de seguridad? Muchas organizaciones aprenden a responder a incidentes de seguridad sólo después de sufrir ataques. Para entonces, los incidentes a menudo pasan a ser mucho más costosos de lo necesario. La respuesta apropiada a un incidente debe ser una parte esencial de la directiva de seguridad general y de la estrategia de mitigación de riesgos.

El hecho de responder a los incidentes de seguridad tiene ventajas directas evidentes. No obstante, también pueden existir ventajas financieras indirectas. Por ejemplo, puede que su compañía de seguros le ofrezca descuentos si puede demostrar que su organización es capaz de controlar los ataques rápidamente y de manera rentable. O, si se trata de un proveedor de servicios, un plan formal de respuesta a incidentes puede ayudarle a aumentar su negocio, ya que muestra que se toma en serio el proceso de seguridad de la información.

Este documento presenta un proceso y procedimientos recomendados para responder a intrusiones identificadas en entornos de red pequeños o medianos. Se explica el valor de formar un equipo de respuesta a incidentes de seguridad con funciones explícitas para los miembros del equipo, así como la forma de definir un plan de respuesta a incidentes de seguridad.

Para responder correctamente a cualquier incidente, se necesita lo siguiente:

-   Minimizar la cantidad y gravedad de los incidentes de seguridad.

-   Crear un CSIRT principal (Computer Security Incident Response Team, Equipo de respuesta a incidentes de seguridad informática).

-   Definir un plan de respuesta a incidentes.

-   Contener los daños y minimizar los riesgos.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

Los administradores de sistemas pasan mucho tiempo con los entornos de red y están muy familiarizados con las redes. Documentan los entornos y crean copias de seguridad. Debe existir un proceso de auditoría ya implementado para supervisar el rendimiento y la utilización. Debe haberse alcanzado cierto nivel de conciencia antes de implementar un equipo de respuesta a incidentes.

Por más detalles que se conozcan del entorno de red, el riesgo de ataques persiste. Toda estrategia de seguridad sensata debe incluir detalles sobre la forma de responder a diferentes tipos de ataque.

[](#mainsection)[Principio de la página](#mainsection)

### Minimización de la cantidad y gravedad de los incidentes de seguridad

En la mayoría de los ámbitos de la vida, es mejor prevenir que curar, y la seguridad no es una excepción. Siempre que sea posible, se deseará evitar que, en primer lugar, se produzcan incidentes de seguridad. No obstante, resulta imposible evitar todos los incidentes de seguridad. Cuando se produce un incidente de seguridad, se debe garantizar que se minimice su repercusión. Para minimizar la cantidad y repercusión de los incidentes de seguridad, debe seguir estas pautas:

-   Establecer claramente y poner en práctica todas las directivas y procedimientos. Muchos incidentes de seguridad están provocados accidentalmente por el personal de TI, que no ha seguido o no ha entendido los procedimientos de administración de cambios, o bien no ha configurado correctamente los dispositivos de seguridad, como pueden ser los firewall o los sistemas de autenticación. Las directivas y los procedimientos se deben probar exhaustivamente para garantizar que son prácticos y claros, y que ofrecen el nivel de seguridad apropiado.

-   Obtener compatibilidad administrativa para las directivas de seguridad y el control de incidentes.

-   Evaluar de forma regular las vulnerabilidades del entorno. Las evaluaciones deben ser realizadas por un experto en seguridad con la autoridad necesaria (con derechos de administrador de los sistemas) para llevar a cabo estas acciones.

-   Comprobar con regularidad todos los sistemas y dispositivos de red para garantizar que tienen instaladas las revisiones más recientes.

-   Establecer programas de formación sobre la seguridad tanto para el personal de TI como para los usuarios finales. La mayor vulnerabilidad de cualquier sistema es el usuario carente de experiencia. El gusano ILOVEYOU aprovechó de forma eficaz esa vulnerabilidad entre el personal de TI y los usuarios finales.

-   Se deben enviar pancartas de seguridad que recuerden a los usuarios sus responsabilidades y restricciones, junto con la advertencia de que se pueden emprender acciones legales en caso de infracción. Estas pancartas facilitan el hecho de reunir pruebas y procesar a los atacantes. Se debe buscar asesoramiento legal para asegurarse de que la redacción de las pancartas de seguridad es apropiada.

-   Desarrollar, implementar y poner en práctica una directiva que requiera contraseñas seguras. Para obtener más información sobre contraseñas, consulte el apartado "Aplicación del uso de contraseñas seguras en las organizaciones" del kit de orientaciones sobre seguridad.

-   Supervisar y analizar con regularidad el tráfico de red y el rendimiento del sistema.

-   Comprobar con regularidad todos los registros y mecanismos de registro, incluidos los registros de eventos del sistema operativo, los registros específicos de aplicación y los registros de sistema de detección de intrusiones.

-   Comprobar los procedimientos de restauración y copia de seguridad. Debe saber dónde se almacenan las copias de seguridad, quién tiene acceso a ellas y los procedimientos para la restauración de datos y la recuperación del sistema. Asegúrese de que las copias de seguridad y los medios se comprueban con regularidad mediante la restauración selectiva de datos.

-   Crear un CSIRT para abordar los incidentes de seguridad. Para obtener más información sobre los CSIRT, consulte la siguiente sección de este documento.

[](#mainsection)[Principio de la página](#mainsection)

### Creación de un CSIRT principal

El CSIRT es crucial para tratar con los incidentes de seguridad del entorno. El equipo debe estar formado por un grupo de personas responsables de abordar los incidentes de seguridad. Los miembros del equipo deben haber definido claramente sus tareas para asegurar que no quede ningún área de la respuesta sin cubrir.

El hecho de reunir un equipo antes de que se produzca cualquier incidente es muy importante para la organización e influirá positivamente en la manera de tratar los incidentes. Un equipo adecuado realizará las siguientes tareas:

-   Supervisar los sistemas en busca de infracciones de seguridad.

-   Servir como punto central de comunicación, tanto para recibir los informes de incidentes de seguridad, como para difundir información esencial sobre los incidentes a las entidades correspondientes.

-   Documentar y catalogar los incidentes de seguridad.

-   Aumentar el nivel de conciencia con respecto a la seguridad dentro de la compañía para ayudar a evitar que se den incidentes en la organización.

-   Posibilitar la auditoría de sistemas y redes mediante procesos como la evaluación de vulnerabilidades y pruebas de penetración.

-   Obtener más información sobre las nuevas vulnerabilidades y estrategias de ataque empleadas por los atacantes.

-   Investigar acerca de nuevas revisiones de software.

-   Analizar y desarrollar nuevas tecnologías para minimizar los riesgos y vulnerabilidades de seguridad.

-   Ofrecer servicios de consultoría sobre seguridad.

-   Perfeccionar y actualizar continuamente los sistemas y procedimientos actuales.

Al crear un CSIRT, debe preparar al equipo para tratar con los incidentes. Para preparar al equipo, debe seguir estas pautas:

-   Formarlos en el uso adecuado y la ubicación de las herramientas de seguridad críticas. También ha de estudiar el hecho de facilitarles equipos portátiles preconfigurados con estas herramientas para asegurar que no se malgasta tiempo en la instalación y configuración de las herramientas, de modo que puedan responder a los incidentes. Estos sistemas y las herramientas asociadas deben estar protegidos adecuadamente cuando no se usen.

-   Reunir toda la información de comunicación pertinente. Debe asegurarse de que cuenta con los nombres y números de teléfono de contacto de las personas de la organización a las haya que avisar (incluidos los miembros del CSIRT, los responsables de mantener todos los sistemas y los encargados de las relaciones con los medios). También necesita los detalles del proveedor de servicios de Internet (ISP) y las autoridades locales y nacionales. Hable con la asesoría legal para contactar con las autoridades locales pertinentes antes de que se produzca un incidente. Esto le ayudará a asegurarse de que entiende los procedimientos apropiados para comunicar los incidentes y reunir pruebas. Debe informar a la asesoría legal de cualquier contacto con las autoridades.

-   Colocar toda la información del sistema de emergencia en una ubicación central y sin conexión, como una carpeta física o un equipo sin conexión. Esta información de emergencia incluye las contraseñas de los sistemas, las direcciones IP, la información sobre la configuración de los enrutadores, las listas de conjuntos de reglas del firewall, copias de las claves de entidad emisora de certificados, los nombres y números de teléfono de contacto, los procedimientos de extensión, etc. Esta información debe estar disponible con facilidad y se debe mantener en un lugar seguro. Un método para proteger y hacer esta información fácilmente disponible consiste en cifrarla en un equipo portátil de seguridad dedicado, guardado en una caja fuerte con acceso limitado a ciertos individuos, como el coordinador del CSIRT, o el director del departamento informático o tecnológico.

La pertenencia y estructura ideal del CSIRT depende del tipo de organización y de la estrategia de administración de riesgos. No obstante, como regla general, el CSIRT debe pertenecer en parte o totalmente al equipo de seguridad de la organización. El equipo principal está compuesto por profesionales responsables de coordinar una respuesta a cualquier incidente. El número de miembros del CSIRT dependerá normalmente del tamaño y la complejidad de la organización. No obstante, debe asegurarse de que cuenta con suficientes miembros para cubrir adecuadamente todas las tareas del equipo en cualquier momento.

#### Establecimiento de las funciones en el equipo

Un equipo adecuado del CSIRT está formado por varios miembros clave.

**Coordinador de equipo del CSIRT.** El CSIRT debe tener a alguien a cargo de sus actividades. Generalmente, el coordinador de equipo del CSIRT será responsable de las actividades del CSIRT y coordinará las revisiones de sus acciones. Esto quizás acarree cambios en las directivas y procedimientos para el control de futuros incidentes.

**Coordinador de incidentes del CSIRT.** En caso de que se produzca un incidente, se debe designar un individuo responsable de coordinar la respuesta. El coordinador de incidentes del CSIRT es propietario del incidente o del conjunto de incidentes de seguridad relacionados. Toda comunicación acerca del evento se coordina a través del coordinador de incidentes: al hablar con cualquiera que no pertenezca al CSIRT, representará a todo el equipo. El coordinador de incidentes puede variar según la naturaleza del incidente y, a menudo, no se trata del coordinador de equipo del CSIRT.

**Miembros asociados al CSIRT.** Aparte del equipo del CSIRT principal, se debe contar con varias personas concretas que traten y respondan a incidentes concretos. Los miembros asociados provienen de varios departamentos diferentes de la organización. Deben especializarse en áreas afectadas por incidentes de seguridad que el CSIRT principal no trata directamente. Los miembros asociados pueden implicarse directamente en un incidente o servir de punto de entrada para delegar la responsabilidad a alguien más apropiado dentro de su departamento. En la siguiente tabla se muestran algunas sugerencias con respecto a los miembros asociados y sus funciones.

**Miembros asociados al CSIRT**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Miembro asociado</th>
<th style="border:1px solid black;" >Descripción de su función</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Contacto de TI</td>
<td style="border:1px solid black;">Este miembro es principalmente responsable de coordinar la comunicación entre el coordinador de incidentes del CSIRT y el resto del grupo de TI. El contacto de TI quizás no tenga la experiencia técnica específica para responder a un incidente concreto; sin embargo, será el responsable principal de encontrar a la persona del grupo de TI adecuada para tratar con eventos de seguridad particulares.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Representante legal</td>
<td style="border:1px solid black;">Este miembro es un abogado muy familiarizado con las directivas de respuesta a incidentes establecidas. El representante legal determina cómo proceder durante un incidente con responsabilidad legal mínima y capacidad máxima para procesar a los delincuentes.
Antes de que ocurra un incidente, el representante legal debe tener información sobre las labores de supervisión y las directivas de respuesta para garantizar que la organización no sufre riesgos legales durante una operación de limpieza o contención. Es muy importante tener en cuenta las implicaciones legales de apagar un sistema y posiblemente infringir los contratos de nivel de servicios o de suscripción establecidos con sus clientes, o de no apagar un sistema en peligro y ser responsable de daños causados por ataques iniciados desde ese sistema.
Cualquier comunicación con las autoridades legales u organismos de investigación externas debe estar coordinada con el representante legal.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Encargado de relaciones públicas</td>
<td style="border:1px solid black;">Generalmente, este miembro forma parte del departamento de relaciones públicas y es responsable de proteger y promocionar la imagen de la organización.
Puede que este individuo no sea quien dé la cara ante los medios y clientes, pero es responsable de escribir el mensaje (el contenido y objetivo del mensaje son generalmente responsabilidad de la dirección). Todas las preguntas de los medios deben dirigirse al departamento de relaciones públicas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administración</td>
<td style="border:1px solid black;">Dependiendo del incidente concreto, puede que se implique sólo a los jefes de departamento o tal vez sea necesario que intervengan directivos de toda la organización. El directivo adecuado variará según la repercusión, la ubicación, la gravedad y el tipo de incidente.
Si tiene un contacto en la dirección, podrá identificar rápidamente al individuo más apropiado para las circunstancias concretas. La dirección es responsable de aprobar y dirigir la directiva de seguridad.
También es responsable de determinar la repercusión total (tanto financiera como en otros aspectos) del incidente en la organización. La dirección indica al encargado del departamento de comunicaciones qué información se debe divulgar a los medios y determina el nivel de interacción entre el representante legal y las autoridades competentes.</td>
</tr>
</tbody>
</table>
 

#### Respuesta a un incidente

En caso de incidente, el CSIRT coordinará una respuesta desde el CSIRT principal y se comunicará con los miembros asociados. En la tabla siguiente se exponen las responsabilidades de estos individuos durante el proceso de respuesta a incidentes.

**Responsabilidades del CSIRT durante el proceso de respuesta al incidente**

<p> </p>
<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Actividad</th>
<th style="border:1px solid black;" >Función</th>
<th style="border:1px solid black;" ></th>
<th style="border:1px solid black;" ></th>
<th style="border:1px solid black;" ></th>
<th style="border:1px solid black;" ></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"><strong>Coordinador de incidentes del CSIRT</strong></td>
<td style="border:1px solid black;"><strong>Contacto de TI</strong></td>
<td style="border:1px solid black;"><strong>Representante legal</strong></td>
<td style="border:1px solid black;"><strong>Encargado del departamento de comunicaciones</strong></td>
<td style="border:1px solid black;"><strong>Administración</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Evaluación inicial</td>
<td style="border:1px solid black;">Propietario</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Respuesta inicial</td>
<td style="border:1px solid black;">Propietario</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reunir pruebas forenses</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Propietario</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Implementar una solución temporal</td>
<td style="border:1px solid black;">Propietario</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Asesoramiento</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Enviar comunicaciones</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Propietario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Consultar a las autoridades locales pertinentes</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Propietario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Implementar soluciones permanentes</td>
<td style="border:1px solid black;">Propietario</td>
<td style="border:1px solid black;">Implementación</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Determinar la repercusión financiera en el negocio</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Asesoramiento</td>
<td style="border:1px solid black;">Actualizaciones</td>
<td style="border:1px solid black;">Propietario</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Definición de un plan de respuesta a incidentes
  
Todos los miembros del entorno de TI deben saber cómo actuar en caso de incidente. El CSIRT realizará la mayoría de las acciones en respuesta a un incidente, pero todo el personal de TI debe saber cómo informar de incidentes internamente. Los usuarios finales deben informar de cualquier actividad sospechosa al personal de TI directamente o a través de un personal de asistencia, no directamente al CSIRT.
  
Cada miembro del equipo debe revisar el plan de respuesta a incidentes detalladamente. El hecho de que el plan sea fácilmente accesible para todo el personal de TI ayudará a garantizar que, cuando se produzca un incidente, se seguirán los procedimientos correctos.
  
Para elaborar un plan satisfactorio de respuesta a incidentes se deben seguir estos pasos:
  
-   Realizar una evaluación inicial.
  
-   Comunicar el incidente.
  
-   Contener el daño y minimizar el riesgo.
  
-   Identificar el tipo y la gravedad del ataque.
  
-   Proteger las pruebas.
  
-   Notificar a los organismos externos, si corresponde.
  
-   Recuperar los sistemas.
  
-   Compilar y organizar la documentación del incidente.
  
-   Valorar los daños y costos del incidente.
  
-   Revisar las directivas de respuesta y actualización.
  
Estos pasos no son puramente secuenciales, sino que se suceden a lo largo del incidente. Por ejemplo, la documentación comienza al principio y continúa durante todo el ciclo de vida del incidente; las comunicaciones también se producen durante todo el incidente.
  
Algunos aspectos del proceso se desarrollan junto a otros. Por ejemplo, como parte de la evaluación inicial, se hará una idea de la naturaleza general del ataque. Es importante usar esta información para contener el daño y minimizar el riesgo tan pronto como sea posible. Si actúa con rapidez, podrá ahorrar tiempo y dinero, y salvar la reputación de la organización.
  
No obstante, hasta que conozca mejor el tipo y la gravedad del ataque, no podrá contener el daño ni minimizar el riesgo de forma realmente efectiva. Una respuesta excesiva podría causar aún más daño que el ataque inicial. Al llevar a cabo estos pasos de manera conjunta, obtendrá la mejor unión entre acciones rápidas y efectivas.
  
**Nota:** es muy importante que pruebe a conciencia el proceso de respuesta a incidentes antes de que se produzca uno. De lo contrario, no puede estar seguro de que las medidas que ha desarrollado serán efectivas al responder a los incidentes.
  
#### Evaluación inicial
  
Muchas actividades podrían indicar un posible ataque a su organización. Por ejemplo, cuando un administrador de red realiza labores de mantenimiento del sistema, puede parecer que alguien está iniciando alguna forma de ataque. En otros casos, un sistema mal configurado puede llevar a varios falsos positivos en el sistema de detección de intrusiones, lo que dificulta la identificación de los verdaderos incidentes.
  
Como parte de su evaluación inicial, debe realizar las siguientes acciones:
  
-   Tomar medidas para determinar si está tratando con un incidente verdadero o un falso positivo.
  
-   Hacerse una idea general del tipo y la gravedad del ataque. Debe reunir al menos suficiente información para su investigación adicional y para empezar a contener los daños y minimizar el riesgo.
  
-   Registrar las acciones minuciosamente. Estos registros se usarán más adelante para documentar el incidente (ya sea real o falso).
  
**Nota:** debe evitar los falsos positivos siempre que sea posible; no obstante, siempre es preferible actuar sobre un falso positivo que no hacerlo sobre un verdadero incidente. La evaluación inicial debe, por lo tanto, ser tan breve como sea posible a la vez que se eliminan los falsos positivos obvios.
  
#### Comunicación del incidente
  
Cuando sospeche que hay un incidente de seguridad, debe comunicar rápidamente la infracción al resto del CSIRT principal. El coordinador de incidentes, junto con el resto del equipo, debe identificar rápidamente con quién debe contactar fuera del CSIRT principal. Así se garantiza que se puede mantener un control y una coordinación de incidentes adecuada, al tiempo que se minimizan los daños.
  
Tenga en cuenta que los daños pueden producirse de muchas formas y que un titular en el periódico que describa una infracción de seguridad puede ser mucho más destructivo que muchas intrusiones en el sistema. Por este motivo y para evitar que los atacantes estén avisados, sólo se debe informar a aquellos implicados en la respuesta a incidentes hasta que el incidente esté totalmente controlado. Basándose en cada situación concreta, el equipo determinará a quién se debe informar acerca del incidente. Podría tratarse de cualquiera, desde personas concretas hasta toda la compañía y los clientes externos. La comunicación externa debe estar coordinada con el representante legal.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Contención de daños y minimización de riesgos
  
Al actuar rápidamente para reducir los efectos reales y potenciales de un ataque, puede marcar la diferencia entre un ataque de menor o mayor importancia. La respuesta exacta dependerá de la organización y de la naturaleza del ataque al que se enfrente. No obstante, se sugieren las siguientes prioridades como punto de partida:
  
1.  **Proteger la vida humana y la seguridad de las personas.** Por supuesto, esta debe ser siempre la máxima prioridad.
  
2.  **Proteger la información secreta y confidencial.** Como parte de su plan de respuesta a incidentes, debe definir claramente qué información es secreta o confidencial. Esto le permitirá establecer prioridades a sus respuestas de protección de datos.
  
3.  **Proteger otra información, como datos científicos, sobre propiedad o del ámbito directivo.** Puede que otra información de su entorno también sea valiosa. Debe proteger en primer lugar los datos más valiosos antes de pasar a otros menos útiles.
  
4.  **Proteger el hardware y software contra el ataque.** Esto incluye protegerlos contra la pérdida o la modificación de los archivos de sistema y contra daños físicos al hardware. Los daños en los sistemas pueden tener como consecuencia un costoso tiempo de inactividad.
  
5.  **Minimizar la interrupción de los recursos informáticos (incluidos los procesos).** Aunque el tiempo de producción sea muy importante en la mayoría de los entornos, el hecho de mantener los sistemas en funcionamiento durante un ataque puede tener como consecuencia problemas más graves en el futuro. Por este motivo, la minimización de la interrupción de los recursos informáticos debe ser generalmente una prioridad relativamente baja.
  
Existen varias medidas que se pueden tomar para contener el daño y minimizar el riesgo en el entorno. Como mínimo, debe llevar a cabo las siguientes acciones:
  
-   Intentar evitar que los atacantes sepan que conoce sus actividades. Puede resultar difícil, porque algunas respuestas esenciales pueden alertar a los atacantes. Por ejemplo, si hay una reunión de emergencia del CSIRT o solicita un cambio inmediato de todas las contraseñas, algún atacante interno puede saber que está al corriente de un incidente.
  
-   Comparar el costo de dejar sin conexión los sistemas en peligro y los sistemas relacionados con el riesgo de continuar funcionando. En la inmensa mayoría de los casos, debe desconectar el sistema de la red inmediatamente. No obstante, puede tener contratos de servicio en funcionamiento que requieran que los sistemas estén disponibles, incluso con la posibilidad de sufrir daños adicionales. En estas circunstancias, puede decidir mantener un sistema conectado con conectividad limitada para reunir pruebas adicionales durante un ataque en proceso.  
    A veces, el daño y el alcance de un incidente pueden ser tan extensos que tenga que tomar medidas que apelen a las cláusulas penales especificadas en sus contratos de nivel de servicio. En todo caso, es muy importante que las acciones que lleve a cabo en caso de incidente se traten de antemano y se describan en el plan de respuesta para que se puedan tomar medidas inmediatas cuando ocurra un ataque.
  
-   Determinar los puntos de acceso usados por el atacante e implementar las medidas adecuadas para evitar futuros accesos. Las medidas pueden incluir la deshabilitación de un módem, la adición de entradas de control de acceso en un enrutador o firewall, o el aumento de las medidas de seguridad físicas.
  
-   Considere la opción de volver a crear un sistema con discos duros nuevos (se deben eliminar los discos duros existentes y almacenarlos, ya que se pueden usar como prueba si decide procesar a los atacantes). Asegúrese de que cambia las contraseñas locales. También debería cambiar las contraseñas de las cuentas de servicio y administrativas en todo el entorno.
  
#### Identificación de la gravedad del ataque
  
Para poder recuperarse de forma eficaz de un ataque, debe determinar la gravedad de la situación de peligro que han sufrido los sistemas. Esto determinará cómo contener y minimizar el riesgo, cómo recuperarse de él, en qué momento y a quién comunicar el incidente, y si se debe intentar obtener una indemnización legal.
  
Debe intentar:
  
-   Determinar la naturaleza del ataque (puede ser diferente a lo que sugiere la evaluación inicial).
  
-   Determinar el punto de origen del ataque.
  
-   Determinar la intención del ataque. ¿Estaba el ataque dirigido específicamente a su organización para conseguir información concreta o fue un ataque aleatorio?
  
-   Identificar los sistemas puestos en peligro.
  
-   Identificar los archivos a los que se ha tenido acceso y determinar su grado de confidencialidad.
  
Al realizar estas acciones, podrá determinar las respuestas apropiadas para su entorno. Un buen plan de respuesta a incidentes resumirá los procedimientos específicos que ha de seguir hasta obtener más información sobre el ataque. Generalmente, la naturaleza de los síntomas del ataque determinará el orden en el que deberá seguir los procedimientos definidos en el plan. Ya que el tiempo es de suma importancia, los procedimientos que requieran menos tiempo tendrán prioridad ante los que consuman más tiempo. Para ayudar a determinar la gravedad del ataque, debe llevar a cabo estas acciones:
  
-   Ponerse en contacto con otros miembros del equipo de respuesta para informarles de sus conclusiones, hacer que comprueben sus resultados, determinar si están al corriente de actividades relacionadas o ataques potenciales, y ayudar a determinar si el incidente es un falso positivo. A veces, lo que quizás parezca ser un incidente verdadero en la evaluación inicial, resultará un falso positivo.
  
-   Determinar si se ha usado hardware no autorizado en la red o si hay signos de acceso no autorizado a través de controles de seguridad físicos puestos en peligro.
  
-   Examinar los grupos clave (administradores de dominio, administradores, etc.) en busca de entradas no autorizadas.
  
-   Buscar software de evaluación o de detección de vulnerabilidades de seguridad. A menudo, se pueden encontrar utilidades de violación en los sistemas en peligro durante la recopilación de pruebas.
  
-   Buscar procesos o aplicaciones no autorizados en ejecución o configurados para ejecutarse usando las carpetas de inicio o las entradas del Registro.
  
-   Buscar espacios en blanco, o la ausencia de los mismos, en los registros del sistema.
  
-   Revisar los registros del sistema de detección de intrusiones en busca de signos de intrusión, qué sistemas pueden estar afectados, los métodos de ataque, el tiempo y la duración del ataque, así como el grado de los posibles daños.
  
-   Examinar otros archivos de registro en busca de conexiones inusuales, auditorías de seguridad correctas no habituales, inicio de sesión fallidos, intentos de inicio de sesión en cuentas predeterminadas, actividad fuera del horario laboral, cambios de permisos en los archivos, directorios y recursos compartidos, y permisos de usuario elevados o cambiados.
  
-   Comparar los sistemas con comprobaciones de integridad del sistema y los archivos realizadas con anterioridad. Esto le permite identificar las adiciones, supresiones, modificaciones y modificaciones del permiso y control realizadas en el sistema de archivos y el Registro. Puede ahorrar mucho tiempo al responder a los incidentes si identifica exactamente qué ha sufrido peligro y qué áreas hay que recuperar.
  
-   Buscar datos confidenciales, como los números de tarjeta de crédito y empleado o los datos del cliente, que se puedan haber cambiado de ubicación o escondido para modificarlos o recuperarlos en el futuro. Puede que también deba comprobar si en los sistemas hay información no empresarial, copias ilegales de software y mensajes de correo electrónico u otros registros que puedan ayudar en una investigación. Si existe la posibilidad de infringir la privacidad u otras leyes al buscar en un sistema durante la investigación, debe contactar con su asesoría jurídica antes de continuar.
  
-   Comparar el rendimiento de los sistemas sospechosos con sus niveles de rendimiento de línea de base. Por supuesto, se presupone que las líneas de base se han creado y actualizado adecuadamente.
  
Al determinar qué sistemas se han puesto en peligro y cómo, generalmente comparará los sistemas con una línea de base registrada con anterioridad del mismo sistema antes de sufrir estos ataques. El hecho de asumir que una instantánea reciente del sistema es suficiente para la comparación puede ponerle en una situación difícil si la instantánea anterior proviene de un sistema que ya ha sido atacado.
  
**Nota:** las herramientas como EventCombMT, DumpEL y Microsoft Operations Manager (MOM) pueden ayudarle a determinar el nivel de ataques que ha sufrido un sistema. Los sistemas de detección de intrusiones de terceros avisan de los ataques de antemano y otras herramientas muestran los cambios en los archivos de los sistemas.
  
#### Protección de las pruebas
  
En muchos casos, si el entorno ha sufrido un ataque intencionado, puede que desee poner una denuncia contra los autores. Para conservar esta opción, debe reunir pruebas que se puedan usar contra ellos, incluso si finalmente se decide no llevar a cabo tal acción. Es muy importante realizar copias de seguridad de los sistemas en peligro tan pronto como sea posible. Realice copias de seguridad de los sistemas antes de realizar cualquier acción que pueda afectar a la integridad de los datos en los medios originales.
  
Alguien cualificado en el análisis forense informático debe hacer al menos dos copias de seguridad completas bit a bit del sistema entero con medios totalmente nuevos. Al menos se debe realizar una copia de seguridad en un medio que admita una sola escritura pero múltiples lecturas, como CD-R o DVD-R. Esta copia de seguridad se debe usar sólo para propósitos legales y se debe proteger en lugar seguro hasta que se necesite.
  
La otra copia de seguridad se puede usar para la recuperación de datos. No se debe tener acceso a estas copias de seguridad a menos que sea con propósitos legales, de modo que se deben proteger físicamente. Asimismo, necesitará documentar la información acerca de las copias de seguridad: quién realizó las copias de seguridad de los sistemas, cuándo, cómo se protegieron y quién tenía acceso a ellas.
  
Una vez que se hayan realizado las copias de seguridad, debe eliminar los discos duros originales y almacenarlos en una ubicación físicamente segura. Estos discos se pueden usar como prueba forense en un juicio. Los discos duros nuevos se deben usar para restaurar el sistema.
  
En ocasiones, la ventaja de conservar los datos puede que no iguale a los costos de retrasar la respuesta y la recuperación del sistema. Los costos y las ventajas de conservar los datos se deben comparar con los de una recuperación más rápida para cada evento.
  
Para sistemas muy grandes, puede que no sea posible realizar copias completas de todos los sistemas en peligro. En lugar de esta operación, debe realizar copias de seguridad de todos los registros y de las partes seleccionadas y violadas del sistema.
  
Si es posible, realice también copias de seguridad de los datos de estado del sistema. Pueden pasar meses o años hasta que se celebre un juicio, de modo que es importante tener archivados todos los detalles del incidente para su uso en el futuro.
  
A menudo, el aspecto legal más difícil de procesar un crimen informático es reunir pruebas de forma que se adapten a las leyes de presentación de pruebas de la jurisdicción en cuestión. De ahí que el componente más importante del proceso forense sea la documentación detallada y completa sobre cómo se procedió con los sistemas, quién y cómo lo hizo, para aportar pruebas confiables. Firme y ponga fecha a cada página de la documentación.
  
Una vez que cuente con copias de seguridad comprobadas y funcionales, puede borrar los sistemas infectados y volverlos a crear. Esto le permitirá empezar a trabajar de nuevo. Las copias de seguridad ofrecen la prueba crítica y definitiva necesaria para emprender acciones legales. Se debe usar una copia de seguridad distinta a la forense para restaurar los datos.
  
#### Notificación a organismos externos
  
Después de contener el incidente y reunir los datos necesarios para un posible juicio, debe plantearse si debe comunicárselo a los organismos externos adecuados. Toda comunicación externa se debe coordinar con el representante legal. Entre los organismos a los que puede acudir se encuentran los siguientes: autoridades competentes locales y nacionales, organismos externos de seguridad y expertos en virus. Los organismos externos pueden ofrecer ayuda técnica, una resolución más rápida e información derivada de incidentes similares para ayudarle a recuperarse completamente del incidente y evitar que se vuelva a producir en el futuro.
  
En sectores y tipos de infracciones concretos, quizás tenga que notificar la situación a los clientes y al público general, especialmente si los clientes pueden verse directamente afectados por el incidente.
  
Si el evento causó una repercusión financiera considerable, puede que desee informar del incidente a las autoridades competentes.
  
Para compañías e incidentes de un perfil superior, puede que los medios de comunicación se vean implicados. La atención de los medios a un incidente de seguridad no suele ser deseable, pero a menudo resulta inevitable. La atención de los medios puede permitir a su organización tomar una postura proactiva en la comunicación del incidente. Como mínimo, los procedimientos de respuesta a incidentes deben definir claramente a los individuos autorizados a hablar con los representantes de los medios.
  
Normalmente, el departamento de relaciones públicas de la organización hablará con los medios. No debe intentar negar a los medios que se ha producido un incidente, porque hacerlo probablemente dañará su reputación más que la admisión proactiva y las respuestas visibles. Esto no significa que deba notificar a los medios cada incidente independientemente de su naturaleza o gravedad. Debe valorar la respuesta apropiada a los medios según el caso.
  
#### Recuperación de los sistemas
  
La forma de recuperar el sistema dependerá generalmente del alcance de la infracción de seguridad. Deberá determinar si puede restaurar el sistema existente dejando intacto todo lo posible, o si es necesario volver a crear completamente el sistema.
  
Para restaurar los datos se asume, por supuesto, que cuenta con copias de seguridad limpias, realizadas antes de que ocurriera el incidente. El software de integridad de archivos puede ayudar a señalar el primer daño en aparecer. Si el software le avisa sobre un archivo modificado, sabrá que la copia de seguridad que hizo antes de la alerta es adecuada y que debe conservarla para su uso cuando vuelva a crear el sistema en peligro.
  
Un incidente podría dañar los datos almacenados varios meses antes de su descubrimiento. Por lo tanto, es muy importante que, como parte del proceso de respuesta a incidentes, determine la duración del incidente. (El software de integridad del sistema y archivos, junto con los sistemas de detección de intrusiones, puede ayudarle en esta tarea.) En algunos casos, la última o incluso las últimas copias de seguridad pueden no ser adecuadas para recuperar un estado apropiado, de modo que debe archivar con regularidad copias de seguridad de los datos en una ubicación externa.
  
#### Recopilación y organización de pruebas del incidente
  
El CSIRT debe documentar minuciosamente todos los procesos al tratar con un incidente. Se debe incluir una descripción de la infracción y detalles de cada acción tomada (quién llevó a cabo la acción, cuándo lo hizo y por qué motivos). Se debe avisar a todas las personas implicadas con acceso durante el proceso de respuesta.
  
Después, se debe organizar la documentación cronológicamente, comprobar que está completa, y firmarla y revisarla con la directiva y los representantes legales. Asimismo, deberá proteger las pruebas recopiladas en la fase de protección de pruebas. Debe plantearse la presencia de dos personas durante todas las fases, que puedan aprobar cada paso. Esto ayudará a reducir la probabilidad de que las pruebas se consideren no admisibles y de que se modifiquen después.
  
Recuerde que el atacante puede ser un empleado, contratista, empleado temporal u otra persona de la organización. Sin documentación completa y detallada, la identificación de un atacante interno será muy difícil. Una documentación apropiada también le proporciona la mejor oportunidad de procesar legalmente a los atacantes.
  
#### Valoración de los daños y costos del incidente
  
Al determinar los daños que sufre la organización, debe considerar tanto los costos directos como los indirectos. El daño y los costos del incidente constituirán una prueba importante y necesaria si decide emprender acciones legales. Entre ellos, se pueden contar los siguientes:
  
-   Costos debidos a la pérdida de la ventaja competitiva por la divulgación de información confidencial o de propietario.
  
-   Costos legales.
  
-   Costos laborales por el análisis de las infracciones, la reinstalación del software y la recuperación de datos.
  
-   Costos relacionados con el tiempo de inactividad del sistema (por ejemplo, productividad de los empleados perdida, ventas perdidas, sustitución del hardware, del software y de otras propiedades).
  
-   Costos relacionados con la reparación y posible actualización de las medidas de seguridad físicas dañadas o ineficaces (cierres, paredes, cajas, etc.).
  
-   Otros daños derivados, como la pérdida de la reputación o de la confianza del cliente.
  
#### Revisión de la respuesta y actualización de las directivas
  
Una vez que se hayan finalizado las fases de documentación y recuperación, debe revisar el proceso minuciosamente. Determine con su equipo qué pasos se siguieron correctamente y qué errores se cometieron. En casi todos los casos, descubrirá que debe modificar algunos procesos para controlar mejor futuros incidentes.
  
Encontrará debilidades en su plan de respuesta a incidentes. Este análisis posterior tiene como objetivo encontrar oportunidades de mejora, que iniciarán un nuevo proceso de planificación de la respuesta a incidentes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información relacionada
  
Gran parte de este documento trata sobre las medidas que se pueden tomar para minimizar el riesgo de sufrir un ataque. No obstante, las organizaciones tienen más probabilidades de alcanzar sus objetivos de seguridad si hacen todo lo posible para minimizar las oportunidades de ataque y si planifican lo que harán en caso de ser atacadas. Parte de este proceso consiste en llevar a cabo auditorías detalladas en busca de ataques. Otra parte igualmente importante es contar con un conjunto claramente definido y bien ensayado de respuestas que puede poner en práctica en caso de ataque.
  
Para obtener más información acerca de la creación de un plan de respuesta a incidentes, consulte los siguientes recursos:
  
-   *Hacking Exposed Windows 2000* por Joel Scambray y Stuart McClure (McGraw-Hill Professional Publishing, ISBN: 007292623).
  
-   [Handbook for Computer Security Incident Response Teams](http://go.microsoft.com/fwlink/?linkid=22398) en el sitio web de SEI en [http://go.microsoft.com/fwlink/?LinkId=22398](http://go.microsoft.com/fwlink/?linkid=22398).
  
-   [Forum of Incident Response and Security Teams (FIRST)](http://go.microsoft.com/fwlink/?linkid=22399) en el sitio web de FIRST en [http://go.microsoft.com/fwlink/?LinkId=22399](http://go.microsoft.com/fwlink/?linkid=22399).
  
-   *Incident Response: Investigating Computer Crime* por Chris Prosise y Kevin Mandia (McGraw-Hill Professional Publishing, ISBN: 00723829).
  
Para obtener más información acerca de la seguridad, consulte:
  
-   *The Internet Security Guidebook: &gt;From Planning to Deployment* por Juanita Ellis y Tim Speed (Academic Press, ISBN: 0223747).
  
[](#mainsection)[Principio de la página](#mainsection)
