---
TOCTitle: 'Microsoft Windows Server Update Services 3.0 Características de Windows Server Update Services 3.0'
Title: 'Microsoft Windows Server Update Services 3.0 Características de Windows Server Update Services 3.0'
ms:assetid: '87a8575f-9a8d-4fdd-98ac-a6d15f2831d5'
ms:contentKeyID: 18158392
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708464(v=WS.10)'
---

Microsoft Windows Server Update Services 3.0
============================================

### Características de Windows Server Update Services 3.0

Publicado: septiembre 11, 2007

##### En esta página

[](#ebaa)[Características del servidor](#ebaa)  
[](#eaaa)[Características del cliente](#eaaa)

### Características del servidor

El componente del servidor de la solución WSUS incluye las características siguientes:

#### Más actualizaciones

Microsoft Update publica actualizaciones para los productos siguientes:

-   Windows 2000

-   Windows XP (ediciones de 32 bits, IA-64 y x64)

-   Windows Vista

-   Windows Server 2003

-   Windows Small Business Server 2003

-   Exchange Server 2000

-   Exchange Server 2003

-   Exchange Server 2007

-   SQL Server

-   SQL Server 2005

-   Office XP

-   Office 2003

-   Microsoft ISA Server 2004

-   Microsoft Data Protection Manager

-   Microsoft ForeFront

-   Windows Live

-   Windows Defender

Al menos un servidor de WSUS que precede en la cadena se conecta a Microsoft Update para obtener las actualizaciones e información que haya disponibles, mientras que otros servidores que siguen en la cadena obtienen sus actualizaciones desde el servidor que precede en la cadena.

#### Se puede establecer que algunas actualizaciones concretas se descarguen automáticamente

Cuando un servidor de WSUS descarga actualizaciones que están disponibles, desde Microsoft Update o desde un servidor de WSUS que precede en la cadena, se produce una sincronización.

Los administradores pueden elegir qué actualizaciones se descargan en un servidor de WSUS durante la sincronización, según los criterios siguientes:

-   El producto o familia de productos (por ejemplo, Microsoft Windows Server 2003 o Microsoft Office)

-   La clasificación de la actualización (por ejemplo, actualizaciones críticas o controladores)

-   El idioma (por ejemplo, sólo inglés y japonés)

Además de esto, los administradores también pueden especificar una programación para que la sincronización se inicie automáticamente.

#### Acciones automatizadas para actualizaciones determinadas a través de la aprobación del administrador

Un administrador debe aprobar cada acción automatizada que se llevará a cabo para la actualización.

Se incluyen las acciones de aprobación siguientes:

-   Aprobar

-   Quitar (esta acción sólo es posible si la actualización admite la desinstalación)

-   Rechazar

Además, el administrador puede aplicar una fecha límite, es decir, una fecha y una hora concretas para instalar o quitar (desinstalar) las actualizaciones. El administrador puede obtener una descarga inmediata si configura una fecha límite para una hora ya pasada.

#### Notificación por correo electrónico de actualizaciones nuevas e informes de estado

WSUS 3.0 puede configurarse de tal modo que se envíen notificaciones por correo electrónico sobre las actualizaciones nuevas e informes de estado. Los destinatarios especificados pueden recibir notificaciones de actualizaciones a medida que vayan llegando al servidor de WSUS. Los informes de estado pueden enviarse a las horas e intervalos especificados.

#### Capacidad de determinar la aplicabilidad de las actualizaciones antes de instalarlas

WSUS 3.0 ahora examina automáticamente las actualizaciones para determinar en qué equipos hay que instalarlas. De hecho, antes de planear e implementar una actualización para su instalación, el administrador puede analizar la repercusión que ésta podría tener en el equipo por medio de un informe de estado generado directamente desde la vista de la actualización para una sola actualización, un subconjunto de actualizaciones o bien todas las actualizaciones.

#### Destinatarios

La especificación de destinatarios permite que los administradores implementen las actualizaciones en equipos y grupos de equipos específicos. Los destinatarios pueden configurarse en el servidor de WSUS directamente, en el servidor de WSUS mediante una directiva de grupo en un entorno de red de Active Directory o bien en el equipo cliente por medio de la edición de la configuración del registro.

A continuación se muestran ejemplos de tareas de especificación de destinatarios que pueden realizar los administradores:

-   Implementación de actualizaciones nuevas para un grupo de equipos de prueba y posterior evaluación de dichas actualizaciones antes de distribuirlas en el entorno de producción.

-   Protección de los equipos que ejecutan aplicaciones específicas. Por ejemplo, si una actualización crítica es incompatible con una aplicación usada sólo por algunos equipos, un administrador puede asegurarse de que esa actualización no se distribuya en esos equipos.

-   Especificación de una fecha límite antes de la cual debe instalarse una actualización y posterior configuración de las diversas fechas límite para equipos o grupos de equipos diferentes.

-   Hacer que el mismo equipo sea miembro de más de un grupo. Por ejemplo, es posible que un equipo sea miembro del grupo "Prueba" y también del grupo "Aplicaciones especiales".

#### Opciones de bases de datos

La base de datos de WSUS almacena la información de las actualizaciones, la información de eventos relativos a las acciones de las actualizaciones en equipos cliente y los valores de configuración del servidor de WSUS.

Los administradores disponen de las opciones siguientes para configurar la base de datos de WSUS 3.0:

-   La base de datos interna de Windows puede ser instalada junto con WSUS durante la instalación en Windows Server 2003.

-   Una base de datos existente de Microsoft SQL Server™ 2005 Service Pack 1.

#### Sincronización e informes de réplicas

WSUS permite a los administradores crear una infraestructura de administración de las actualizaciones formada por una jerarquía de los servidores de WSUS. Los servidores de WSUS pueden escalarse horizontalmente para poder administrar cualquier número de clientes.

Con la sincronización de réplicas, el administrador del servidor central de WSUS puede crear actualizaciones, grupos de destino y aprobaciones que se propagarán automáticamente a los servidores de WSUS designados como servidores de réplica. Esto significa que los clientes de las sucursales pueden obtener actualizaciones desde la oficina central que hayan sido aprobadas desde un servidor local sin necesidad de tener un administrador local de WSUS. Asimismo, las oficinas que disponen de un vínculo con poco ancho de banda al servidor central son incluso menos problemáticas, ya que el servidor de WSUS de la sucursal se conecta sólo al servidor central de WSUS. Los informes de estado de las actualizaciones pueden generarse para todos los clientes de un servidor de réplica.

#### Administración de diversos servidores de WSUS desde una única consola

WSUS 3.0 ahora permite que los administradores administren una jerarquía de servidores WSUS desde una única consola de WSUS. El complemento de administración de WSUS para Microsoft Management Console puede instalarse en cualquier equipo de la red.

#### Generación de informes

Con los informes de WSUS, los administradores pueden supervisar la actividad siguiente (todos los informes tienen formato imprimible y pueden exportarse a archivos de hoja de cálculo de Excel o archivos .pdf de Adobe):

-   **Estado de las actualizaciones**: Los administradores pueden supervisar el nivel de cumplimiento de las actualizaciones para los equipos cliente de forma continuada mediante informes de estado de las actualizaciones. Estos informes facilitan el estado para la aprobación e implementación de las actualizaciones por actualización, equipo y grupo de equipos, en función de los eventos que se envían al equipo cliente.

-   **Estado del equipo**: Los administradores pueden valorar el estado de las actualizaciones en los equipos cliente. Por ejemplo, pueden solicitar un resumen de las actualizaciones que se han instalado o que se necesitan para un equipo determinado.

-   **Estado de cumplimiento del equipo**: Los administradores pueden ver o imprimir un resumen sobre la información de cumplimiento relativa a un equipo específico, incluida información básica del software y hardware, la actividad de WSUS y el estado de las actualizaciones.

-   **Estado de cumplimiento de las actualizaciones**: Los administradores pueden ver o imprimir un resumen sobre la información de cumplimiento relativa a una actualización específica, incluidas sus propiedades y el estado acumulativo para cada grupo de equipos.

-   **Estado de sincronización (o descarga)**: Los administradores pueden supervisar el estado y la actividad de sincronización durante un período de tiempo concreto. También pueden consultar las últimas actualizaciones descargadas.

-   **Valores de configuración de WSUS**: Los administradores pueden consultar un resumen de las opciones especificadas para la implementación de WSUS.

#### Solución de problemas

El paquete de administración de WSUS permite a los administradores solucionar problemas relacionados con la infraestructura de WSUS, incluidos la conectividad de la red, los permisos, la conectividad de SQL y los servicios relacionados con WSUS. El paquete de administración de WSUS expone esta información en la vista Estado de Microsoft Operations Manager. Los administradores pueden obtener información detallada acerca de la causa del problema y de las soluciones relacionadas.

#### Extensibilidad

Hay disponible un kit de desarrollo de software (SDK) que permite que administradores y desarrolladores trabajen con una API basada en un entorno .NET.

Los administradores pueden crear código personalizado para administrar tanto las actualizaciones automáticas como los servidores de WSUS. Estas nuevas API permiten a los administradores recopilar inventarios de hardware y software de los dispositivos administrados, crear aprobaciones para la instalación a través del cuadro de diálogo **Agregar o quitar programas** e integrar la administración de WSUS con la de otras herramientas de administración como, por ejemplo, System Center Essentials.

Los desarrolladores pueden crear aplicaciones de administración para integrarlas con WSUS o bien para publicar actualizaciones de terceros con la infraestructura de WSUS.

#### Opciones de comunicación configurables

Los administradores tienen flexibilidad para configurar los equipos y obtener actualizaciones directamente desde Microsoft Update, desde un servidor de la intranet de WSUS que distribuye actualizaciones internamente o desde una combinación de ambos, en función de la configuración de la red.

También pueden configurar un servidor de WSUS para que, si lo consideran pertinente, use un puerto personalizado para conectarse a la intranet o a Internet. (El puerto predeterminado que usa un servidor de WSUS es el puerto 80.) También es posible conectarse a través del protocolo SSL, en cuyo caso el puerto predeterminado es el 443.

Los administradores pueden configurar los valores del servidor proxy si el servidor de WSUS se conecta a Internet a través de un servidor de este tipo.

#### Importación y exportación y migración de datos desde la línea de comandos

Los administradores pueden importar y exportar metadatos y contenido de las actualizaciones entre los servidores de WSUS. Se trata de una tarea necesaria en una red que tiene una conectividad a Internet limitada o restringida.

Los administradores pueden migrar sin problemas sus valores de configuración administrativos, aprobaciones de contenido y contenido anteriores desde un servidor WSUS 2.0 a un WSUS 3.0. La migración también puede servir para facilitar la consolidación de los servidores de WSUS. Por ejemplo, los administradores pueden migrar aprobaciones para grupos de destino específicos de un servidor de WSUS a otro.

#### Copia de seguridad y restauración

WSUS es compatible con ntbackup para archivos de contenido de actualizaciones y metadatos de SQL Server.

[](#mainsection)[Principio de la página](#mainsection)

### Características del cliente

Las características siguientes incluyen el componente del cliente de la solución WSUS.

#### Administración eficaz y ampliada del servicio de actualizaciones automáticas

En un entorno de servicios de Active Directory, los administradores pueden configurar el comportamiento de las actualizaciones automáticas mediante una directiva de grupo. En otros casos, pueden configurar de forma remota las actualizaciones automáticas mediante las claves de registro a través de un script de inicio de sesión u otro mecanismo similar.

Entre las capacidades del administrador para configurar equipos cliente se incluyen las siguientes:

-   Configuración de opciones de notificación y programación para usuarios a través de directivas de grupo.

-   Configuración de la frecuencia con la que el equipo cliente comprobará el origen de las actualizaciones (ya sea Microsoft Update u otro servidor de WSUS) para obtener actualizaciones nuevas.

-   Configuración de Actualizaciones automáticas para poder instalar las actualizaciones que no requieren rearranques ni interrupciones de servicios tan pronto como se encuentren y no se tenga que esperar hasta la hora programada de instalación automática.

-   Administración de los equipos cliente a través de la API basada en el modelo de objetos componentes (COM). Hay un SDK disponible.

#### Actualización automática para los equipos cliente

Los equipos cliente de WSUS pueden detectar desde el servidor de WSUS si hay una versión disponible más reciente de Actualizaciones automáticas y, a continuación, actualizar automáticamente el servicio.

#### Detección automática de las actualizaciones aplicables

El servicio de Actualizaciones automáticas puede descargar e instalar las actualizaciones que sean verdaderamente aplicables para el equipo. Este servicio trabaja con el servidor de WSUS para evaluar qué actualizaciones deben aplicarse a un equipo cliente específico.

#### Eficacia subyacente

El servicio de Actualizaciones automáticas funciona en segundo plano para que la repercusión perceptible en la productividad del empleado y en la funcionalidad de la red sea mínima.

Actualizaciones automáticas consolida las actualizaciones que requieren que se reinicie el equipo con un solo reinicio.

Además, elimina la necesidad de los usuarios de un entorno administrado de interactuar con los Términos de licencia del software de Microsoft. Los administradores aceptan los términos de licencia en el servidor de WSUS en nombre de los equipos cliente.

BITS 2.0 emplea la compresión delta para facilitar las descargas que son invisibles para el usuario. Por ejemplo, después de que el servicio Actualizaciones automáticas haya descargado una actualización para un equipo cliente, continuará supervisando el servidor de WSUS que precede en la cadena o bien Microsoft Update y, a continuación, descargará sólo los cambios en un archivo de actualización para ese equipo cliente. Esta tecnología también permite una distribución eficaz de los Service Packs a través de Actualizaciones automáticas.

[](#mainsection)[Principio de la página](#mainsection)
