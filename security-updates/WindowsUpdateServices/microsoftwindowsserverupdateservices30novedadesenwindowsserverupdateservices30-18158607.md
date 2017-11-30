---
TOCTitle: 'Microsoft Windows Server Update Services 3.0 - Novedades en Windows Server Update Services 3.0'
Title: 'Microsoft Windows Server Update Services 3.0 - Novedades en Windows Server Update Services 3.0'
ms:assetid: 'f3809191-6e2f-4c85-b019-8c16afa54742'
ms:contentKeyID: 18158607
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708601(v=WS.10)'
---

Microsoft Windows Server Update Services 3.0
============================================

### Novedades en Windows Server Update Services 3.0

Publicado: septiembre 11, 2007

Windows Server Update Services (WSUS) 3.0 ofrece varias características nuevas que facilitan su uso, implementación y compatibilidad. Concretamente, WSUS 3.0 ofrece mejoras en las áreas siguientes:

##### En esta página

[](#eeaa)[Facilidad de uso](#eeaa)  
[](#edaa)[Opciones de implementación mejoradas](#edaa)  
[](#ecaa)[Mayor compatibilidad con las jerarquías de servidores complejas](#ecaa)  
[](#ebaa)[Mayor optimización del rendimiento y el ancho de banda](#ebaa)  
[](#eaaa)[Ampliación de WSUS 3.0 con las API mejoradas](#eaaa)  

### Facilidad de uso

#### Administración de WSUS desde la consola de administración

La consola de la administración de WSUS 3.0 ha pasado de una consola basada en la Web a ser un complemento para la versión 3.0 de Microsoft Management Console. La nueva interfaz de usuario ofrece las características siguientes:

-   Páginas de inicio en cada nodo que contienen una introducción a las tareas asociadas con el nodo

-   Filtrado avanzado

-   Nuevas columnas que permiten clasificar las actualizaciones según el número de MSRC, la gravedad de MSRC, el artículo de Microsoft Knowledge Base y el estado de la instalación

-   Selección, clasificación y reorganización de columnas

-   Menús contextuales que le permiten hacer clic con el botón secundario y elegir una acción

-   Informes integrados con vistas de las actualizaciones

-   Vistas personalizadas

#### Administración remota de WSUS

La consola de administración de WSUS 3.0 puede instalarse en otros equipos de la red de forma que se pueda administrar el servidor WSUS 3.0 de forma remota.

#### Configuración de las tareas posteriores a la instalación mediante un asistente

Un asistente de configuración indica a los nuevos usuarios el proceso de configuración del servidor tras la instalación.

#### Generación de múltiples informes de mayor precisión

Ahora es posible generar los informes directamente desde la vista de actualización. Puede generar informes en un subconjunto de actualizaciones, como las actualizaciones de seguridad que necesitan los equipos pero que no han sido todavía aprobadas para proceder con la instalación. Se pueden crear informes en todos los equipos administrados por una jerarquía de réplicas y guardarlos en formato de Excel o PDF.

#### Mayor facilidad en el mantenimiento del estado del servidor

WSUS 3.0 ahora registra información detallada sobre el estado del servidor en el registro de eventos. El paquete de Microsoft Operations Manager (MOM) está ahora disponible para supervisar eventos generados por el servidor WSUS.

#### Obtención de mensajes de correo electrónico acerca de nuevas actualizaciones

El servidor dispone de una compatibilidad integrada para la notificación por correo electrónico de las nuevas actualizaciones y los resúmenes de cumplimiento de éstas.

#### Facilidad en la eliminación de la información antigua

El asistente para la limpieza permite quitar equipos, actualizaciones y archivos de actualización antiguos de su servidor.

#### Actualización sin problemas de WSUS 2.0 a WSUS 3.0

WSUS 3.0 puede instalarse en un servidor que ya tenga WSUS 2.0 instalado. El proceso de instalación realiza una actualización local que conserva toda la configuración y aprobaciones anteriores. El proceso de actualización de una jerarquía de servidores debe iniciarse desde el servidor central y continuar en dirección descendente en la línea jerárquica. Un servidor WSUS 2.0 puede sincronizarse desde un servidor WSUS 3.0; sin embargo, un servidor WSUS 3.0 no podrá sincronizarse desde un servidor WSUS 2.0. La actualización de WSUS 2.0 a WSUS 3.0 es un proceso unidireccional; volver a WSUS 2.0 requiere primero quitar WSUS 3.0 y, a continuación, volver a instalar WSUS 2.0.

[](#mainsection)[Principio de la página](#mainsection)

### Opciones de implementación mejoradas

#### Obtenga actualizaciones de forma más rápida

Con WSUS 3.0 puede configurar un servidor para que sincronice automáticamente las actualizaciones con una frecuencia máxima de una vez por hora (en comparación con WSUS 2.0, cuya frecuencia máxima era de una vez al día). Esta mejora permite que las actualizaciones nuevas se repliquen a través de la organización más rápidamente.

#### Establecimiento de más aprobaciones automáticas

Las reglas de aprobación automática de WSUS 3.0 permiten especificar diversos productos y clasificaciones de actualizaciones como, por ejemplo, la aprobación automática para las actualizaciones de definiciones de Microsoft Word. Además, WSUS 3.0 admite la creación de múltiples reglas de aprobación automática en lugar de una regla única. Las reglas de aprobación automática ahora se aplicarán a todas las actualizaciones que haya en esos momentos en el servidor WSUS.

#### Limitación de acceso a los informes de sólo lectura

Los miembros del grupo de seguridad "Informadores de WSUS" dispondrán de acceso de sólo lectura al servidor. Los miembros pueden generar informes pero no pueden aprobar actualizaciones ni configurar el servidor.

[](#mainsection)[Principio de la página](#mainsection)

### Mayor compatibilidad con las jerarquías de servidores complejas

#### Administración de múltiples servidores desde una única consola

La consola de administración de WSUS 3.0 le permitirá inspeccionar y administrar todos los servidores WSUS de la jerarquía.

#### Creación de informes para todos los equipos

Ahora puede crear informes de actualizaciones para todos los equipos administrados por una jerarquía de réplicas.

#### Configuración de los servidores en clúster

Los servidores WSUS 3.0 ahora pueden configurarse en un clúster para mayor tolerancia a errores. Dichos servidores deben hacer referencia a la misma instancia de la base de datos de SQL Server, que también puede estar en un clúster.

#### Alternar el modo de réplica

Ahora puede cambiar un servidor secundario entre el modo de réplica y el modo autónomo sin necesidad de volver a instalar WSUS 3.0.

#### Asignación de clientes a múltiples grupos de destino

En WSUS 3.0, mismo un equipo puede pertenecer a múltiples grupos de destino (por ejemplo, a un grupo de "Escritorios" y a un grupo de "Pruebas"). Además, puede crear grupos jerárquicos (por ejemplo, un grupo de "Servidores" de destino con los grupos secundarios "Servidores críticos" y "Servidores no críticos"). Se pueden especificar aprobaciones para el grupo de destino principal que serán, a su vez, las que automáticamente heredarán los equipos de los grupos secundarios.

[](#mainsection)[Principio de la página](#mainsection)

### Mayor optimización del rendimiento y el ancho de banda

#### Benefíciese de un rendimiento más rápido

WSUS 3.0 registra una mejora en la escalabilidad de aproximadamente un 50 por ciento más que WSUS 2.0. Además, WSUS 3.0 incorpora una compatibilidad nativa de x64 para obtener incluso mayores mejoras de rendimiento y escalabilidad en el hardware de 64 bits.

#### Especificación de los idiomas en las sucursales

Para ahorrar espacio en disco y evitar cargar la red, ahora puede configurar una sucursal para descargar actualizaciones en menos idiomas que el servidor central. Por ejemplo, puede configurar el servidor central para descargar actualizaciones en todos los idiomas y una sucursal para descargar actualizaciones sólo en inglés.

#### Configuración de contenido independiente y de canales de metadatos

Las sucursales con conexiones de banda estrecha al servidor central pero conexiones de banda ancha a Internet ahora pueden configurarse para obtener metadatos del servidor central y contenido de actualizaciones de Microsoft Update.

[](#mainsection)[Principio de la página](#mainsection)

### Ampliación de WSUS 3.0 con las API mejoradas

#### Cambio a la compatibilidad de .NET Framework 2.0

La nueva API está basada en .NET Framework 2.0.

#### Vaya más allá de la consola de WSUS con las API destinadas a herramientas de administración avanzada

Las nuevas API se han creado para usarse con las herramientas de administración avanzada (como, por ejemplo, System Center Essentials). Estas características no se exponen en la consola de administración de WSUS.

#### Agregue aprobaciones opcionales de instalación a las opciones del administrador

La nueva API admite la creación de aprobaciones para una "instalación opcional", que indica al Agente de Windows Update que haga que la actualización esté disponible para su instalación en el cuadro de diálogo **Agregar o quitar programas**, pero no a través del servicio Actualizaciones automáticas.

#### Recopilación de inventarios de hardware y software

La nueva API admite la recopilación de los inventarios de hardware y software de los dispositivos administrados.

#### Ampliación del conjunto de actualizaciones mediante publicación local

La nueva API admite las aplicaciones de publicación y actualizaciones de terceros, lo cual, a su vez, permite que la infraestructura de WSUS pueda distribuir también actualizaciones de otras compañías.

> [!NOTE]
> Para obtener más información acerca de las características de WSUS, consulte [Características de Windows Server Update Services](http://www.microsoft.com/spain/technet/windowsserver/library/wsus/caracteristicas.mspx) que encontrará más adelante en este documento.

[](#mainsection)[Principio de la página](#mainsection)
