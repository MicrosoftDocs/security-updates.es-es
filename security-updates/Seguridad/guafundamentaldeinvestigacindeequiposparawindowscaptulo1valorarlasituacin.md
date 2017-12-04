---
TOCTitle: 'Guía fundamental de investigación de equipos para Windows: Capítulo 1: Valorar la situación'
Title: 'Guía fundamental de investigación de equipos para Windows: Capítulo 1: Valorar la situación'
ms:assetid: '08013562-8f01-4ad5-a5de-a8901f590df3'
ms:contentKeyID: 20200202
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162832(v=TechNet.10)'
---

Guía fundamental de investigación de equipos para Windows
=========================================================

### Capítulo 1: Valorar la situación

Publicado: enero 11, 2007

En este capítulo se describe cómo realizar una evaluación exhaustiva de la situación, cómo establecer el ámbito y los recursos necesarios para una investigación interna. Utilice el proceso de cinco pasos que se muestra en la figura siguiente.

![](images/Cc162832.a76f2b24-206d-4cda-9c0f-34af70fa63ca(es-es,TechNet.10).gif)

**Figura 1.1. Fase de evaluación del modelo de investigación de equipos**

##### En esta página

[](#efaa)[Notificar a los responsables de la toma de decisiones y obtener autorización](#efaa)  
[](#eeaa)[Revisar las directivas y leyes](#eeaa)  
[](#edaa)[Identifique a los miembros del equipo de investigación](#edaa)  
[](#ecaa)[Realice una evaluación exhaustiva](#ecaa)  
[](#ebaa)[Prepare la adquisición de evidencias](#ebaa)

### Notificar a los responsables de la toma de decisiones y obtener autorización

Para realizar una investigación de equipo, primero debe obtener la autorización adecuada, a no ser que las directivas y los procedimientos existentes proporcionen la autorización de respuesta a incidentes. Después, debe realizar una evaluación exhaustiva de la situación y definir una línea de acción. Siga las recomendaciones siguientes:

-   Si no existe ninguna directiva ni procedimientos de respuesta a incidentes escritos, notifique a los directores y obtenga la autorización escrita de un director autorizado para realizar la investigación de equipo.

-   Documente todas las acciones que emprenda relacionadas con esta investigación. Asegúrese de que hay un resumen documentado completo y preciso de los eventos y las decisiones producidos durante el incidente y la respuesta al incidente. Esta documentación se puede utilizar, en última instancia, en el tribunal para determinar la línea de acción seguida durante la investigación.

-   En función del ámbito del incidente y en ausencia de problemas de seguridad nacional o de seguridad para vida, la prioridad principal es proteger a la organización de daños adicionales. Cuando la organización esté segura, la restauración de servicios (si es necesaria) y la investigación del incidente serán las siguientes prioridades.

Las decisiones que tome pueden cuestionarse al igual que la evidencia. Dado que la evidencia de equipo es compleja, diferentes investigaciones (como las llevadas a cabo por la parte opuesta) pueden tomar decisiones diferentes y llegar a conclusiones diferentes.

[](#mainsection)[Principio de la página](#mainsection)

### Revisar las directivas y leyes

Al principio de una investigación de equipo es importante conocer las leyes aplicables a la investigación, así como las directivas internas de la organización que puedan existir. Tenga en cuenta las consideraciones y recomendaciones siguientes:

-   Determine si tiene la autoridad legal para llevar a cabo una investigación. ¿Su organización dispone de las directivas y los procedimientos sobre derechos de privacidad de empleados, contratistas u otras personas que utilicen su red? ¿Alguna de dichas directivas y procedimientos especifican las circunstancias en las que se permite la supervisión? Muchas organizaciones indican en sus directivas y procedimientos que no se espera privacidad en el uso del equipo, el correo electrónico, los servicios web, el teléfono ni el correo de la organización, y que la compañía se reserva el derecho como una condición de empleo para supervisar y buscar estos recursos. Los abogados de la organización deben revisar estas directivas y procedimientos y debe informarse a todos los empleados, contratistas y visitantes de su existencia. Si no está seguro de su autoridad, póngase en contacto con administración, los abogados o (si es necesario) la autoridad local.

-   Consulte a sus abogados para evitar posibles problemas de control inadecuado de la investigación. Estos problemas pueden incluir:

    -   Poner en peligro datos personales de los clientes.

    -   Infringir alguna ley federal o estatal, como las reglas de privacidad federales.

    -   Incurrir en alguna responsabilidad criminal o civil por intercepción impropia de comunicaciones electrónicas. Considere las pancartas de advertencia.

    -   Ver información confidencial o privilegiada. Los datos confidenciales que puedan comprometer la confidencialidad de la información del cliente sólo deben estar disponibles como parte de la documentación relacionada con la investigación si pertenece directamente a la investigación.

-   Asegúrese de que se abordan las siguientes cuestiones de privacidad y confidencialidad del cliente:

    -   Todos los datos deben transferirse de forma segura, almacenarse en equipos locales (no servidores de red) y no tener un acceso fácil.

    -   Todos los datos (incluida la documentación) deben mantenerse durante el período especificado por los abogados o la política local cuando se haya cerrado la investigación de equipo. Si los datos forman parte de una posible causa penal, consulte a la autoridad judicial competente que investiga el caso. Si se trata de un caso civil, consulte a los abogados de la organización. Además, revise los problemas de retención de datos relacionados con la Ley Sarbanes-Oxley de 2002 u otros requisitos legales para la retención de datos.

-   Conserve copias digitales de la evidencia, impresiones de la evidencia y la cadena de custodia de toda la evidencia, en caso de una acción legal. La conservación de la cadena de custodia se consigue mediante documentación verificable que indique quién dirigió la evidencia, cuándo se llevó cabo, y las ubicaciones, fechas y horas en que almacenó la evidencia. La evidencia debe almacenarse en un lugar seguro, de lo contrario, no se podrá verificar la custodia.

[](#mainsection)[Principio de la página](#mainsection)

### Identifique a los miembros del equipo de investigación

Es importante determinar quién debe responder ante un incidente para llevar a cabo una investigación interna de equipos satisfactoria. Idealmente, deben establecerse los miembros del equipo antes de que sea necesario un equipo para una investigación real. Es importante que los equipos de la investigación estén estructurados adecuadamente y tengan las habilidades apropiadas. La organización podría establecer los miembros del equipo como parte de un proceso de planificación de recuperación de desastres. Utilice las recomendaciones siguientes como orientación para formar un equipo de investigación:

-   Identifique a una persona que sepa cómo realizar una investigación. Recuerde que la credibilidad y las habilidades de la persona que lleve a cabo la investigación se examinan a menudo si una situación tiene como resultado un proceso legal ante un tribunal de justicia.

-   Identifique a los miembros del equipo y defina las responsabilidades de cada miembro.

-   Asigne a un miembro del equipo como técnico principal de la investigación. El técnico principal tiene, generalmente, grandes habilidades técnicas y experiencia en investigaciones de equipo. En las investigaciones que impliquen sospechosos con conocimientos técnicos, puede que necesite seleccionar miembros del equipo de investigación que tengan más conocimientos que los sospechosos.

-   Cree un equipo de investigación lo más pequeño posible para garantizar la confidencialidad y proteger a la organización contra escapes de información no deseados.

-   Contrate un equipo de investigación externo de confianza si la organización no tiene personal con las habilidades necesarias.

-   Asegúrese de que todos los miembros del equipo tengan el espacio y la autorización necesarios para realizar las tareas que tengan asignadas. Esta consideración es especialmente importante si hay algún personal externo, como consultores, implicado en la investigación.

> [!IMPORTANT]
> La naturaleza volátil de las evidencias digitales dificulta la realización de las investigaciones de manera puntual. Procure garantizar la disponibilidad de todos los miembros del equipo durante una investigación. 

[](#mainsection)[Principio de la página](#mainsection)

### Realice una evaluación exhaustiva

Es necesaria una evaluación exhaustiva y bien documentada de la situación para priorizar las acciones y justificar los recursos para la investigación interna. Esta evaluación debe definir el impacto actual y potencial en la empresa del incidente, identificar la infraestructura afectada y obtener una comprensión lo más global posible de la situación. Esta información le ayudará a definir una línea de acción apropiada.

Tenga en cuenta las recomendaciones siguientes para realizar una evaluación completa:

-   Utilice toda la información disponible para describir la situación, su gravedad potencial, las partes potencialmente afectadas y (si está disponible) las partes sospechosas.

-   Identifique la repercusión y el carácter de la investigación en su organización. Por ejemplo, evalúe si implica datos de clientes, detalles financieros, informes médicos o información confidencial de la empresa. No se olvide de evaluar su potencial repercusión en las relaciones públicas. Esta evaluación probablemente no esté dentro de las competencias de TI y debe realizarse en colaboración con la administración y asesores legales.

-   Analice la repercusión en la empresa del incidente en la investigación. Indique las horas necesarias para recuperarse del incidente, las horas de inactividad, el coste del equipo dañado, la pérdida de ingresos y el valor de los secretos comerciales. Esta evaluación debe ser realista y no exagerada. Los costes reales del incidente se determinarán más adelante.

-   Analice los recursos intangibles afectados, la repercusión futura en la reputación, las relaciones con clientes y en la moral del empleado. No exagere la gravedad del incidente. Este análisis tiene fines informativos, le ayudará conocer el alcance del incidente. La repercusión real se determinará más adelante. Esta evaluación probablemente no esté dentro de las competencias de TI y debe realizarse en colaboración con la administración y asesores legales.

Utilice las recomendaciones siguientes para identificar, analizar y documentar la infraestructura y los equipos afectados por la situación. Es posible que gran parte de estas indicaciones ya se hayan realizado como parte de un proceso de evaluación de riesgos para preparar un plan de recuperación de desastres.

-   Identifique las redes implicadas, el número de equipos afectados y el tipo de equipos afectados.

-   Obtenga la documentación de topología de red, que debe incluir un diagrama detallado de la red que proporcione información de infraestructura acerca de servidores, hardware de red, servidores de seguridad, conexiones de Internet y otros equipos de la red.

-   Identifique los dispositivos de almacenamiento externos y los equipos remotos que deban incluirse. Los dispositivos de almacenamiento externo pueden ser memorias USB, tarjetas de memoria y flash, discos ópticos y discos magnéticos.

-   Capture el tráfico de red durante un espacio de tiempo si es necesario un análisis en directo. Este tipo de análisis sólo es necesario si se cree que hay un tráfico sospechoso continuo en la red y, normalmente, sólo se realiza después de haber agotado la auditoría y el registro como fuentes de evidencia. Microsoft® Windows® XP y Windows Server® 2003 incluyen herramientas de captura de red integradas como Netcap y Rasdiag, que pueden capturar tráfico de red local sin necesidad de instalar productos como Netmon o Ethereal. Use herramientas como Windows Network Monitor (NetMon) y Windows Sysinternals TDIMon para realizar análisis de datos de red. Las herramientas de Windows Sysinternals se pueden descargar en la página [Windows Sysinternals](http://www.microsoft.com/technet/sysinternals/default.mspx) de Microsoft TechNet.

> [!IMPORTANT]
> La detección de red (captura de tráfico de red) puede suponer una violación de la intimidad, según el ámbito de la captura. Por lo tanto, debe ser muy cauteloso a la hora de implementar herramientas de captura de red en su red. 

-   Use estas herramientas para examinar el estado de las aplicaciones de software y los sistemas operativos de equipos que probablemente estén afectados. Algunas herramientas útiles para esta tarea son los registros de aplicaciones de Windows, los registros de sistema y Windows Sysinternals PsTools.

-   Examine el archivo y los servidores de aplicaciones afectados. Use herramientas de Windows Sysinternals como PsTools, PsFile, ShareEnum y los registros de seguridad internos de Windows para examinar y documentar la actividad en estos servidores.

> [!IMPORTANT]
> Parte de la información recolectada durante esta evaluación (como los procesos en ejecución y los datos en memoria) la capturan las herramientas en tiempo real. Asegúrese de que los registros generados se almacenan de forma segura para evitar la pérdida de estos datos volátiles. 

Además, las recomendaciones siguientes le pueden ayudar a obtener una comprensión global de la situación.

-   Cree una escala de tiempo y asígnele todo. Una escala de tiempo es especialmente importante en el caso de incidentes globales. Documente todas las discrepancias entre la fecha y la hora de los host, como los equipos de escritorio, y la hora y la fecha del sistema, como el servicio de hora de Windows en Windows Server 2003.

-   Identifique y entreviste a todas las personas que puedan estar implicadas en el incidente, como administradores del sistema y usuarios. En algunas situaciones, es posible que estas personas sean externas a la organización. Las entrevistas a los usuarios y el personal afectado suelen ofrecen buenos resultados y perspectivas de la situación. Las entrevistas deben realizarlas entrevistadores experimentados.

-   Documente todos los resultados de las entrevistas. Los necesitará más adelante para entender completamente la situación.

-   Recupere información (registros) de los dispositivos de red internos y externos, como servidores de seguridad y enrutadores, que se puedan utilizar en la ruta de acceso posible del ataque.

-   Alguna información, tal como la dirección IP y la propiedad de nombre de dominio, es pública por su naturaleza. Por ejemplo, puede utilizar la herramienta [Whois](http://go.microsoft.com/?linkid=6013254) de Windows Sysinternals o el [Registro Americano de Números de Internet](http://www.arin.net/index.shtml) para identificar al propietario de una dirección IP.

[](#mainsection)[Principio de la página](#mainsection)

### Prepare la adquisición de evidencias

Para preparar la fase Obtención de datos, asegúrese de que ha determinado correctamente las acciones y el resultado de la fase Valorar la situación. Un documento detallado que contenga toda la información considera pertinente proporciona un punto de partida para la fase siguiente y para la preparación del informe final. Además, si el incidente se convierte en algo más que una investigación interna y requiere un procedimiento legal, es posible que terceros hagan uso de todos los procesos utilizados en la recopilación de evidencia para intentar obtener los mismos resultados.

Este documento debe ofrecer información detallada acerca de la situación e incluir lo siguiente:

-   Una estimación inicial del impacto de la situación en el negocio de la organización.

-   Un diagrama de la topología de red detallado que destaque los equipos afectados y ofrezca detalles acerca de cómo pueden estar afectados estos sistemas.

-   Los resúmenes de las entrevistas con usuarios y administradores de sistemas.

-   Los resultados de las interacciones legales y de terceros.

-   Los informes y registros generados por las herramientas utilizadas durante la fase de evaluación.

-   Una línea de acción propuesta.

> [!IMPORTANT]
> La creación de documentación coherente, precisa y detallada a través del proceso de investigación de equipos le ayudará con la investigación en curso. A menudo, esta documentación es esencial para el éxito del proyecto y nunca se debe pasar por alto. A medida que cree la documentación, sea siempre consciente de que constituye una evidencia que se puede utilizar en un procedimiento legal. Antes de empezar la fase siguiente, asegúrese de que ha obtenido la aprobación por parte de una persona responsable de la documentación que creó durante la fase de evaluación. 

**Descargar**

[Obtenga la Guía fundamental de investigación de equipos para Windows](http://go.microsoft.com/fwlink/?linkid=80345)

**Notificaciones de actualización**

[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)

[](#mainsection)[Principio de la página](#mainsection)
