---
TOCTitle: 'Guía de operaciones: Administración de la infraestructura de seguridad de RADIUS y LAN inalámbrica.'
Title: 'Guía de operaciones: Administración de la infraestructura de seguridad de RADIUS y LAN inalámbrica.'
ms:assetid: 'b7e1c3fd-cb1f-4f56-bab9-1cff44b33269'
ms:contentKeyID: 20112552
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458730(v=TechNet.10)'
---

Capítulo 12: Administración de la infraestructura de seguridad de LAN inalámbrica y RADIUS
==========================================================================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#ejaa)[Introducción](#ejaa)
[](#eiaa)[Tareas de mantenimiento esenciales](#eiaa)
[](#ehaa)[Tecnología requerida en la Guía de operaciones](#ehaa)
[](#egaa)[Funciones administrativas de seguridad de RADIUS y WLAN](#egaa)
[](#efaa)[Tareas de cuadrante operativo](#efaa)
[](#eeaa)[Tareas del cuadrante de compatibilidad](#eeaa)
[](#edaa)[Tareas del cuadrante de optimización](#edaa)
[](#ecaa)[Tareas del cuadrante de cambio](#ecaa)
[](#ebaa)[Tablas de configuración](#ebaa)
[](#eaaa)[Información adicional](#eaaa)

### Introducción

En este capítulo se describen los procedimientos operativos necesarios para administrar la infraestructura del Servicio de usuario de acceso telefónico de autenticación remota (RADIUS) y la seguridad de LAN inalámbrica (WLAN) implementadas como parte de esta guía de *Seguridad de LAN inalámbricas*. La estructura se basa en las categorías y conceptos de Microsoft Operations Framework (MOF) tratados en el capítulo 10, "Introducción a la guía de operaciones".

Este capítulo le ayudará a implementar un sistema de administración completo para la infraestructura de RADIUS y la seguridad de WLAN, incluidas todas las tareas de configuración para comenzar a supervisar y realizar el mantenimiento del sistema. En este capítulo también se incluyen tareas operativas normales para mantener el funcionamiento correcto de la infraestructura y procedimientos de ayuda para administrar las incidencias de compatibilidad, administrar cambios en el entorno y optimizar el rendimiento del sistema.

El capítulo se divide en dos partes principales. La primera parte consta de dos secciones, "Tareas de mantenimiento esenciales" y "Funciones administrativas de seguridad de RADIUS y WLAN". Estas secciones son breves y se deben leer en su totalidad; proporcionan información fundamental acerca de la configuración de un entorno administrado correctamente para el sistema. El resto del capítulo está diseñado para utilizarse principalmente como referencia. Tendrá que implementar algunas tareas de las secciones de referencia cuando el sistema se implemente, pero se indican de forma clara en la sección "Tareas de mantenimiento esenciales".

Aunque no es necesario que se detenga en todos los detalles de la sección de referencia, debe revisarlos para familiarizarse con el contenido de modo que pueda encontrar rápidamente los elementos que necesite en el futuro.

#### Requisitos previos

Debe estar familiarizado con los conceptos de MOF descritos en el capítulo 10, "Introducción a la guía de operaciones". No es preciso un conocimiento detallado de MOF.

Debe estar familiarizado con los conceptos de RADIUS y el Servicio de autenticación de Internet (IAS) de Microsoft® en concreto, así como con los conceptos de 802.11, 802.1X y EAP-TLS. Para obtener más información acerca de estos temas técnicos, consulte las referencias de los capítulos de la guía de planeamiento.

También se precisan conocimientos de Microsoft Windows® 2000 Server (o posterior) en las siguientes áreas:

-   Operaciones básicas y mantenimiento de Microsoft Windows Server™ 2003 (incluido el uso de herramientas como Visor de sucesos, Administración de equipos y NTBackup).

-   Conceptos y tareas del servicio de directorio Active Directory®. Esto incluye la estructura de Active Directory, herramientas, manipulación de usuarios, grupos, otros objetos de Active Directory y el uso de Directiva de grupo.

-   Conceptos de seguridad del sistema de Windows, como usuarios, grupos, auditoría, listas de controla de acceso, el uso de plantillas de seguridad y la aplicación de plantillas de seguridad mediante Directiva de grupo o herramientas de la línea de comandos.

-   Administración del Servicio de autenticación de Internet.

-   Windows Scripting Host (WSH) y el lenguaje Microsoft Visual Basic® Scripting Edition (VBScript). El conocimiento de la sintaxis de la programación por lotes puede ayudarle a obtener el máximo rendimiento de las secuencias de comandos suministradas, pero no es fundamental.

Además, antes de leer este capítulo debe leer los capítulos de la guía de planeamiento y de la guía generación así como disponer de un conocimiento exhaustivo de la arquitectura y el diseño de la solución.

#### Descripción general del capítulo

En la siguiente lista se describen las principales secciones de este capítulo.

-   **Tareas de mantenimiento esenciales**. Contiene dos tablas que enumeran las tareas necesarias para configurar el sistema de administración y la lista normal de tareas que se tienen que realizar para mantener el sistema.

-   **Funciones administrativas**. Describe las funciones administrativas utilizadas en la solución, las capacidades de cada función y cómo se asignan a clústeres de funciones de MOF y los grupos de seguridad administrativos definidos para la solución.

-   **Tareas de cuadrante operativo**. Incluye todas las tareas relacionadas con el mantenimiento normal de la infraestructura de RADIUS y la seguridad de WLAN. En esta sección se incluye la supervisión, copias de seguridad y operaciones de directorio y seguridad.

-   **Tareas del cuadrante de compatibilidad**. Incluye todos los procedimientos relacionados con la recuperación de problemas del sistema. En esta sección se incluye la restauración desde la copia de seguridad y las operaciones para manejar un servidor IAS con error.

-   **Tareas del cuadrante de optimización**. Incluye algunos procedimientos de planeamiento de administración de capacidad.

-   **Tareas del cuadrante de cambio**. Incluye tareas comunes que se relacionan con la realización de cambios en la configuración del servidor IAS y su puesta en producción de un modo controlado. También se incluyen los procedimientos que le servirán para recopilar y mantener información de configuración fundamental acerca del servidor IAS.

-   **Solución de problemas**. Contiene procedimientos que le ayudarán a solucionar problemas comunes que se pueden producir con la infraestructura de RADIUS y la seguridad de WLAN. También incluye descripciones de herramientas útiles para solucionar problemas y procedimientos para habilitar el registro de distintos componentes.

-   **Tablas de configuración**. Contiene un subconjunto de los parámetros de configuración empleados en los capítulos de la guía de generación. Estos valores se utilizan como ejemplo en el texto de los procedimientos.

-   **Información adicional**. Enumera fuentes de información adicionales a las que se hace referencia en el texto.

[](#mainsection)[Principio de la página](#mainsection)

### Tareas de mantenimiento esenciales

En esta sección se enumeran las tareas clave que se deben llevar a cabo para conseguir el funcionamiento adecuado de la infraestructura de RADIUS y la seguridad de WLAN. Las tareas se enumeran en dos tablas: tareas iniciales de configuración y tareas operativas continuadas. Los nombres de tarea que aparecen en las tablas se describen con detalle más adelante en este documento. Las tareas se agrupan por cuadrante MOF y, junto a cada una de ellas, se indica la función de administración de servicio (SMF) de MOF a la que pertenece, lo que sirve de ayuda para encontrar la tarea necesaria con facilidad.

También se incluye en esta sección una lista de las herramientas y las tecnologías utilizadas en los procedimientos de este capítulo.

#### Tareas iniciales de configuración

En la tabla siguiente se muestran las tareas que se deben llevar a cabo para poner en fase de producción el funcionamiento de la infraestructura de RADIUS y la seguridad de WLAN. Según sus estándares y prácticas operativos, es posible que no tenga que realizar todas estas tareas. No obstante, revise la información de cada tarea y decida si debe realizarla o no. Quizás sea necesario, además, volver a realizar alguna de estas tareas en determinado momento. Por ejemplo, si se instala un nuevo servidor IAS, se tendrán que configurar sus trabajos de copia de seguridad y supervisión.

**Tabla 12.1: Tareas iniciales de configuración**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de tarea</th>
<th style="border:1px solid black;" >Función de administración de servicio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Cuadrante operativo</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Adición de clientes RADIUS a servidores IAS</td>
<td style="border:1px solid black;">Administración de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitación de configuración inalámbrica en equipos</td>
<td style="border:1px solid black;">Administración de servicios de directorio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Adición de equipos y usuarios a grupos de directiva de acceso remoto</td>
<td style="border:1px solid black;">Administración de servicios de directorio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">División en categorías de las alertas de supervisión</td>
<td style="border:1px solid black;">Supervisión y control de servicios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Supervisión de las restricciones de capacidad de IAS</td>
<td style="border:1px solid black;">Supervisión y control de servicios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configuración de la exportación de la configuración de IAS</td>
<td style="border:1px solid black;">Administración de almacenamiento</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Exportación de la configuración del cliente RADIUS</td>
<td style="border:1px solid black;">Administración de almacenamiento</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configuración de la copia de seguridad de los directorios de datos de IAS</td>
<td style="border:1px solid black;">Administración de almacenamiento</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Prueba de la copia de seguridad de IAS</td>
<td style="border:1px solid black;">Administración de almacenamiento</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Cuadrante de optimización</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Determinación de la carga máxima del servidor IAS</td>
<td style="border:1px solid black;">Administración de capacidad</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Determinación de los requisitos de almacenamiento y copia de seguridad para un servidor IAS</td>
<td style="border:1px solid black;">Administración de capacidad</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Cuadrante de cambio</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administración de actualizaciones del sistema operativo</td>
<td style="border:1px solid black;">Administración de cambios<br />
Administración de versión</td>
</tr>
</tbody>
</table>
 

#### Tareas de mantenimiento

En la siguiente tabla se muestran las tareas que se deben llevar a cabo regularmente para que la infraestructura de RADIUS y la seguridad de WLAN funcionen correctamente. Puede utilizar esta tabla para planear los recursos necesarios y la programación de operaciones para administrar el sistema.

Puede haber tareas que no tenga que llevar a cabo, pero revise la información sobre cada tarea para decidir si debe realizarla o no. Además, algunas de estas tareas se pueden realizar según sea necesario y otras según un programa. Por ejemplo, si se agrega un cliente RADIUS a un servidor IAS, tendrá que llevar a cabo una exportación y copia de seguridad de la configuración del servidor aunque no esté programada. Algunas tareas se indican en la columna Frecuencia. Las dependencias como éstas también se anotan automáticamente en los detalles de la tarea.

**Tabla 12.2: Tareas de mantenimiento continuadas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de tarea</th>
<th style="border:1px solid black;" >Frecuencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Adición de clientes RADIUS a servidores IAS</td>
<td style="border:1px solid black;">Al agregar AP inalámbricos a la red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Quitar clientes RADIUS de servidores IAS</td>
<td style="border:1px solid black;">Efectos de la eliminación de AP inalámbricos de la red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitación de configuración inalámbrica en equipos</td>
<td style="border:1px solid black;">Al agregar equipos a la red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Adición de equipos y usuarios a grupos de directiva de acceso remoto</td>
<td style="border:1px solid black;">Al conceder a los empleados acceso a la WLAN</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Exportación de la configuración del cliente RADIUS</td>
<td style="border:1px solid black;">Al agregar AP inalámbricos a la red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Prueba de la copia de seguridad de IAS</td>
<td style="border:1px solid black;">Mensualmente</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a los registros de solicitudes de RADIUS de IAS</td>
<td style="border:1px solid black;">Diaria o semanalmente<br />
(según los requisitos de seguridad)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Revisión de las entradas de los registros de sucesos de autenticación de RADIUS de IAS</td>
<td style="border:1px solid black;">Diaria o semanalmente<br />
(según los requisitos de seguridad)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Archivado y eliminación de las entradas de los registros de RADIUS de IAS</td>
<td style="border:1px solid black;">Mensualmente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administración de actualizaciones del sistema operativo</td>
<td style="border:1px solid black;">Diariamente</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tecnología requerida en la Guía de operaciones
  
En las tablas siguientes se enumeran las herramientas o tecnologías utilizadas en los procedimientos descritos en este capítulo.
  
**Tabla 12.3: Tecnología requerida**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de elemento</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Complemento Usuarios y equipos de Active Directory de MMC</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Secuencias de comandos MSS</td>
<td style="border:1px solid black;">Esta solución</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Editor de texto</td>
<td style="border:1px solid black;">Bloc de notas: Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio del programador de tareas de Windows</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SchTasks.exe</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Copia de seguridad de Windows</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Visor de eventos</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Monitor del sistema</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Net.exe</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consola de alertas operativas</td>
<td style="border:1px solid black;">Microsoft Operations Manager (MOM)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Medios extraíbles para almacenamiento fuera del equipo</td>
<td style="border:1px solid black;">Disquetes, CD-RW o cintas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Copia de seguridad de servidores de IAS</td>
<td style="border:1px solid black;">Servicio de copia de seguridad de red<br />
o bien<br />
dispositivo de copia de seguridad local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Consola de administración de directivas de grupo</td>
<td style="border:1px solid black;">Descarga Web desde Microsoft.com</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IASParse</td>
<td style="border:1px solid black;">Herramientas de soporte técnico de Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Access 2002</td>
<td style="border:1px solid black;">Microsoft Office XP</td>
</tr>
</tbody>
</table>
  
**Tabla 12.4: Tecnología recomendada**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de elemento</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Consola de alertas operativas</td>
<td style="border:1px solid black;">Microsoft Operations Manager u otro sistema de supervisión de servicios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Infraestructura de correo electrónico para alertas operativas (una alternativa para MOM)</td>
<td style="border:1px solid black;">Servidor y cliente de SMTP/POP3/IMAP, como Microsoft Exchange Server y Microsoft Outlook®</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Eventquery.vbs</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Herramientas de planeamiento de capacidad</td>
<td style="border:1px solid black;">Microsoft Operations Manager u otras herramientas de planeamiento de capacidad</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sistema de distribución de actualizaciones de seguridad</td>
<td style="border:1px solid black;">Microsoft Systems Management Server<br />
o bien<br />
Microsoft Software Update Services</td>
</tr>
</tbody>
</table>
 

[](#mainsection)[Principio de la página](#mainsection)

### Funciones administrativas de seguridad de RADIUS y WLAN

En la administración de una infraestructura de RADIUS y la seguridad de WLAN intervienen numerosas funciones distintas. Las dos secciones siguientes las dividen en funciones importantes y funciones auxiliares.

#### Funciones esenciales de RADIUS y WLAN

Las funciones de la siguiente tabla son esenciales para la administración de una infraestructura de RADIUS y la seguridad de WLAN.

**Tabla 12.5: Funciones esenciales de RADIUS y seguridad de WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la función</th>
<th style="border:1px solid black;" >Ámbito</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administrador del Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de la administración y configuración global de IAS para la empresa</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditor del Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de revisar, archivar y eliminar los registros de RADIUS que se encuentran en los servidores de IAS</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Operadores de copia de seguridad del Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de la copia de seguridad y restauración del estado de configuración de IAS y de los datos históricos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Personal del servicio de asistencia de WLAN</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Personal del servicio de asistencia que se encarga de solucionar los problemas de WLAN</td>
</tr>
</tbody>
</table>
  
#### Funciones de seguridad de apoyo de RADIUS y WLAN
  
Las funciones operativas de la siguiente tabla no son esenciales para la administración de la infraestructura de RADIUS y la seguridad de WLAN, pero sirven de apoyo a las funciones esenciales.
  
**Tabla 12.6: Funciones de apoyo de RADIUS y seguridad de WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la función</th>
<th style="border:1px solid black;" >Ámbito</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Operador de supervisión</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de supervisar sucesos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Planeador de capacidad</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de analizar el rendimiento y la carga para predecir futuros requisitos de capacidad</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de Active Directory</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de la configuración y el soporte técnico de la infraestructura de Active Directory</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Operaciones de Active Directory</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga del mantenimiento diario del directorio, por ejemplo el mantenimiento de grupos de seguridad, la creación de cuentas, etc.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de escritorio</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Se encarga de la configuración y el soporte técnico de los equipos de escritorio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cambio de tarjeta de aprobaciones</td>
<td style="border:1px solid black;">Empresa</td>
<td style="border:1px solid black;">Representantes comerciales y técnicos necesarios para aprobar los cambios realizados en la infraestructura</td>
</tr>
</tbody>
</table>
  
#### Asignación de funciones a grupos de seguridad
  
En la siguiente tabla se enumeran los grupos de seguridad definidos para esta solución y se describen brevemente las capacidades o permisos de cada uno.
  
En los servidores IAS, los grupos de seguridad locales y de dominio se utilizan para aplicar los permisos que son aplicables a cada función. Las cuentas de dominio se utilizan para rellenar los grupos de funciones. Se acepta que las cuentas individuales sean miembros de múltiples grupos de funciones locales si dicha condición es compatible con las directivas de TI y seguridad de la empresa.
  
**Tabla 12.7: Asignación de funciones de seguridad de RADIUS y WLAN a grupos de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la función</th>
<th style="border:1px solid black;" >Grupo de seguridad del dominio</th>
<th style="border:1px solid black;" >Grupo de seguridad local</th>
<th style="border:1px solid black;" >Capacidades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administrador del Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Administradores IAS</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Capacidad de administración completa del servidor IAS, incluida la capacidad de iniciar y detener el servicio IAS y de cambiar la configuración</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditores del Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Auditores de seguridad IAS</td>
<td style="border:1px solid black;">N/A</td>
<td style="border:1px solid black;">Capacidad de leer y eliminar los archivos de registro de solicitudes de RADIUS del volumen de registro</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Operadores de copia de seguridad de IAS</td>
<td style="border:1px solid black;">N/A</td>
<td style="border:1px solid black;">Operadores de copia de seguridad</td>
<td style="border:1px solid black;">Capacidad total de realizar copia de seguridad y restauración del estado del sistema operativo y los datos de configuración de IAS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Personal del servicio de asistencia de WLAN</td>
<td style="border:1px solid black;">N/A</td>
<td style="border:1px solid black;">N/A</td>
<td style="border:1px solid black;">Trabaja con los administradores de IAS para solucionar problemas de autenticación de IAS (puede tener permisos de lectura para los mismos recursos que los auditores de seguridad de IAS en ciertos casos)</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas de cuadrante operativo
  
El cuadrante operativo contiene los estándares de funcionamiento, procesos y procedimientos de TI que se aplican con regularidad a las soluciones de servicios para obtener y mantener los niveles de servicio que indican los parámetros predeterminados. El objetivo del cuadrante operativo consiste en una ejecución muy previsible de tareas diarias manuales y automatizadas.
  
Esta sección contiene información que es relevante para las SMF siguientes:
  
-   Administración de red
  
-   Administración de servicios de directorio
  
-   Administración de seguridad
  
-   Administración de almacenamiento
  
-   Supervisión y control de servicios
  
-   Programación de trabajos
  
No hay tareas que correspondan al resto de las SMF:
  
-   Administración de sistemas
  
-   Administración de la red
  
-   Administración de impresión y resultados
  
    **Nota:** cada descripción de tarea incluye la siguiente información de resumen: requisitos de seguridad, frecuencia y requisitos de tecnología.
  
#### Administración de red
  
La función de administración de red se encarga del diseño y mantenimiento de los componentes físicos que forman la red de la organización, por ejemplo servidores, enrutadores, conmutadores y servidores de seguridad. Para las redes inalámbricas, estos componentes incluyen puntos de acceso inalámbricos y los servidores RADIUS que les dan soporte.
  
##### Adición de clientes RADIUS a servidores IAS
  
Los AP inalámbricos necesitan autorización para llevar a cabo la autenticación y las cuentas en servidores IAS. La habilitación de puntos de acceso inalámbricos nuevos como clientes RADIUS es uno de los pocos cambios incrementales que es necesario implementar en un servidor IAS de producción. Esta tarea autoriza a los puntos de acceso inalámbricos a participar en la autenticación y contabilidad RADIUS con el servidor IAS. Lleve a cabo esta tarea cada vez que se implementen y configuren nuevos AP inalámbricos para su participación en la autenticación de red.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores de IAS
  
-   **Frecuencia**: al agregar nuevos puntos de acceso inalámbricos a la red
  
-   **Requisitos de tecnología**:
  
    -   Complemento Servidor de autenticación de Internet de MMC
  
    -   Secuencias de comandos MSS (para la secuencia de comandos GenPwd)
  
    -   Unidad de disco u otra unidad de medio extraíble con permisos de escritura
  
    -   Disquete u otro medio extraíble con permisos de escritura
  
###### Detalles de la tarea
  
Utilice una contraseña aleatoria (secreto) que sea única para cada punto de acceso inalámbrico al agregar el punto a cada servidor IAS. El uso de los mismos secretos RADIUS para varios puntos de acceso inalámbricos incrementa el riesgo de que el secreto compartido ya no lo sea durante mucho tiempo.
  
Windows Server 2003 Enterprise Edition permite que los administradores agreguen puntos de acceso inalámbricos por lotes a IAS mediante la adición de una subred de cliente RADIUS y el uso de un secreto compartido por todos los puntos de acceso de dicha red. No obstante, aunque simplifica la administración de estos secretos, da como resultado una solución de seguridad más débil que utilizar secretos exclusivos.
  
Esta solución implementa criptográficamente secretos aleatorios generados por la secuencia de comandos GenPwd que se incluye en estas guías.
  
**Para agregar clientes RADIUS a IAS de forma individual**
  
1.  En el complemento MMC del Servicio de autenticación de Internet, haga clic con el botón secundario del mouse en la carpeta **Clientes RADIUS** y, a continuación, haga clic en **Nuevo cliente RADIUS**.
  
2.  Escriba el **Nombre descriptivo** y la **Dirección del cliente (IP o DNS)** del punto de acceso inalámbrico. En la medida de lo posible, utilice una dirección IP en lugar de un nombre DNS, ya que IAS intenta reanudar cada uno de los clientes RADIUS tras el inicio del servidor. En entornos grandes con numerosos puntos de acceso inalámbricos, la resolución de los clientes mediante sus nombres DNS puede afectar negativamente al tiempo de inicio. Haga clic en **Siguiente**.
  
3.  Seleccione **Estándar de RADIUS** como atributo de cliente-proveedor y escriba el secreto compartido de este AP inalámbrico concreto.
  
    **Nota:** los pasos siguientes incluyen la utilización de un disquete u otro medio de escritura extraíble. Utilice un disco formateado y etiquételo "Clientes de RADIUS para *&lt;nombre de servidor&gt;*".
  
4.  Puede utilizar la secuencia de comandos GenPwd que se incluye con estas instrucciones para generar un secreto aleatorio para el uso individual de cada punto de acceso que esté configurado como cliente RADIUS. GenPwd generará un secreto y lo almacenará conjuntamente con un nombre descriptivo de cada cliente RADIUS en un archivo Clients.txt. GenPwd agrega automáticamente la información a un archivo clients.txt del directorio actual con el formato de valores separados mediante comas. Sin embargo, si dispone de un método para generar secretos de RADIUS, puede utilizarlo en vez de GenPwd en los siguientes pasos.
  
    **Nota:** GenPwd utiliza una función de CryptoAPI para generar una cadena aleatoria criptográficamente codificada en base64. No utiliza la función de números aleatorios de VBScript.
  
5.  Abra un símbolo del sistema y establezca el directorio A:\\ como su directorio actual. La ubicación del directorio en el sistema de archivos es importante, porque la nueva información se agregará al archivo Clients.txt del directorio actual. Si no existe ningún archivo Clients.txt, se creará uno.
  
6.  Ejecute el comando siguiente. Asegúrese de cambiar &lt;*nombre del cliente*&gt; por el nombre descriptivo del punto de acceso inalámbrico. Puede ser un nombre DNS, una dirección IP u otra cadena:
  
    cscript //job:GenPwd C:\\MSSScripts\\wl\_tools.wsf /client:nombre\_de\_cliente
  
    Después de creado, el archivo separado por comas puede importarse con facilidad a una hoja de cálculo o a una aplicación de base de datos para consultarlo o editarlo.
  
    **Importante:** los secretos del RADIUS se pueden cambiar para cada servidor IAS y punto de acceso inalámbrico periódicamente. No olvide utilizar GenPwd u otra herramienta para generar secretos seguros y guardar el nuevo secreto y el nombre del AP inalámbrico en el archivo Clients.txt. Los datos del archivo clients.txt es muy confidencial. No lo copie en el servidor; guárdelo en un sitio seguro, como una caja fuerte.
  
7.  En el complemento Servicio de autenticación de Internet de MMC, introduzca el secreto compartido en los campos **Secreto compartido** y **Confirmar secreto compartido**. Seleccione el atributo **La solicitud debe contener el atributo autenticador de mensaje** y haga clic en **Finalizar**.
  
    **Nota:** es posible que algunos clientes RADIUS requieran la configuración de atributos específicos del proveedor (VSA) para que funcionen correctamente. Consulte la documentación específica del proveedor para obtener información acerca de los requisitos de VSA.
  
##### Quitar clientes RADIUS de servidores IAS
  
La eliminación de AP inalámbricos no deseados como clientes RADIUS es uno de los pocos cambios incrementales que se deben llevar a cabo en un servidor IAS de producción implementado. Esta tarea impide que el punto de acceso inalámbrico participe en la autenticación y contabilidad RADIUS con el servidor IAS. Lleve a cabo esta tarea cada vez que se retiren puntos de acceso inalámbricos para impedir que utilicen los servicios de autenticación RADIUS y de cuentas.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: miembro del grupo de administradores de IAS
  
-   **Frecuencia**: al quitar puntos de acceso inalámbricos de la red
  
-   **Requisitos de tecnología**:
  
    -   Complemento Servidor de autenticación de Internet de MMC
  
    -   Notepad.exe u otro editor de archivos de texto
  
###### Detalle de tareas
  
Quite cada punto de acceso inalámbrico de IAS independientemente. También debe eliminar la entrada correspondiente en el archivo Clients.txt que se encuentra en el disco de clientes RADIUS guardado en un almacenamiento seguro. El archivo Clients.txt se crea mediante el siguiente procedimiento de la tarea "Adición de clientes RADIUS a servidores IAS".
  
**Para quitar clientes RADIUS del servidor IAS**
  
1.  En el complemento MMC del Servicio de autenticación de Internet, seleccione la carpeta Clientes RADIUS.
  
2.  En el panel derecho, seleccione la entrada que representa al cliente RADIUS que se desea quitar y, a continuación, elija **Eliminar**.
  
3.  Cuando se le pida confirmación, haga clic en **Sí**.
  
    **Nota:** los siguientes pasos incluyen el uso de un disquete u otro medio de escritura extraíble etiquetado "Clientes RADIUS de *&lt;nombre de servidor&gt;*", que se creó en una sección anterior. Asegúrese de utilizar el disco correcto con el servidor apropiado para evitar la pérdida de datos.
  
4.  Busque el disquete de cliente RADIUS de este servidor y abra el archivo A:\\Clients.txt con Bloc de notas.
  
5.  Busque y elimine la entrada del cliente RADIUS que desea eliminar.
  
#### Administración de servicios de directorio
  
Los servicios de directorio permiten a los usuarios y las aplicaciones localizar recursos de red como usuarios, servidores, aplicaciones, herramientas, servicios y otro tipo de información en la red. La administración de los servicios de directorio implica las operaciones, mantenimiento y soporte técnico diario del directorio de la empresa. La administración de servicios de directorio garantiza que cualquier solicitante autorizado pueda obtener acceso a la información mediante un proceso simple y organizado.
  
##### Habilitación del acceso a WLAN para usuarios y equipos
  
Se deben realizar tres tareas independientes para habilitar el acceso a la WLAN. Estas tareas se controlan mediante pertenencia a grupos de seguridad y también se pueden automatizar fácilmente con un archivo de secuencias de comandos VBScript, Jscript o comandos (lotes). Estas tareas se documentan por separado porque muchas organizaciones las realizan en fases distintas de su ejecución de WLAN.
  
**Importante:** esta solución utiliza grupos de seguridad personalizados para controlar los usuarios y equipos que recibirán certificados y configuración de directiva de WLAN así como para controlar los usuarios y equipos que pueden acceder a la WLAN mediante IAS. Se pueden utilizar grupos independientes para estos tres elementos con el fin de implementar una implementación por fases de certificados, configuración de directiva y acceso a WLAN. Si no desea un control tan preciso, puede habilitar todos los usuarios y equipos para cualquiera de estos elementos o para todos. La forma más sencilla de habilitar todos los usuarios y equipos consiste en agregar usuarios de dominio o equipos de dominio al grupo de inscripción de certificados correspondiente, grupo Directiva de grupo de WLAN (sólo equipos) y grupo Acceso a WLAN.
  
**Para habilitar el acceso WLAN de un equipo**
  
1.  Siga el procedimiento "Activación de la inscripción (o inscripción automática) de un tipo de certificado para un usuario o equipo" del capítulo 11, para agregar la cuenta de equipo al grupo de inscripción de certificados **Inscribir automáticamente la autenticación del cliente: certificado del equipo**.
  
2.  Siga el procedimiento (más adelante en esta sección) "Habilitación de configuración inalámbrica en equipos" para implementar la configuración de red correcta en el equipo. Agregue la cuenta de equipo al grupo de directiva **Directiva de red inalámbrica: Equipo**.
  
3.  Siga el procedimiento (más adelante en esta sección) "Adición de equipos y usuarios a grupos de directiva de acceso remoto" para autorizar que el equipo se conecte a la WLAN. Agregue la cuenta de equipo al grupo de seguridad Acceso remoto **Directiva de acceso remoto: Equipos inalámbricos**.
  
    **Importante:** estos pasos se pueden llevar a cabo en cualquier orden. Durante una implementación grande, todos estos pasos se deben realizar antes de habilitar el hardware de WLAN. El equipo se *debe* reiniciar una vez al menos para que reciba la pertenencia a grupos asignada en cada uno de estos procedimientos. Se agotará el tiempo de espera del símbolo de inicio de sesión del equipo al cabo de unos instantes y provocará que se actualice la pertenencia a grupos, pero este proceso puede durar hasta una semana.  
    El equipo se *debe* conectar a una red con cables para recibir el certificado y la configuración inalámbrica iniciales. Las renovaciones de certificado y los cambios futuros de la configuración inalámbrica se recibirán por la WLAN.
  
**Para habilitar el acceso WLAN de un usuario**
  
1.  Siga el procedimiento del capítulo 11,"Activación de la inscripción (o inscripción automática) de un tipo de certificado para un usuario o equipo", para agregar la cuenta de usuario al grupo de inscripción de certificados **Inscribir automáticamente la autenticación del cliente: certificado de usuario**.
  
2.  Asegúrese de que el usuario inicia sesión con un equipo WLAN autorizado y configurado (tal como se ha descrito en el procedimiento anterior). En concreto, el equipo se debe haber configurado con las opciones de directiva de WLAN correctas.
  
3.  Siga el procedimiento (más adelante en esta sección) "Adición de equipos y usuarios a grupos de directiva de acceso remoto" para autorizar que el equipo se conecte a la WLAN. Agregue la cuenta de equipo al grupo de seguridad Acceso remoto **Directiva de acceso remoto: Usuarios inalámbricos**.
  
    **Importante:** estos pasos se pueden llevar a cabo en cualquier orden; también se pueden realizar en cualquier momento antes de implementar y habilitar realmente el hardware de la WLAN. Los usuarios *deben* cerrar la sesión y, a continuación, volver a iniciarla al menos una vez para recibir la pertenencia a grupos asignada en cada uno de estos procedimientos. Se agotará el tiempo de espera del símbolo de inicio de sesión del usuario al cabo de unos instantes y provocará que se actualice la pertenencia a grupos, pero este proceso puede durar hasta una semana.  
    El equipo se *debe* conectar a una red con cables para que los usuarios reciban los certificados iniciales. Las renovaciones de certificado se recibirán por la WLAN.
  
##### Habilitación de configuración inalámbrica en equipos
  
La configuración de las opciones de red inalámbrica (como las opciones de 802.11 y 802.1X) en los equipos cliente se automatizan con Directiva de grupo de Active Directory. Los equipos que reciben esta configuración de red inalámbrica se controlan agregándolos a grupos de seguridad. Los grupos de directiva de seguridad se utilizan para filtrar el objeto de directiva de grupo (GPO) de modo que sólo los miembros del grupo reciban la configuración de directiva. Realice esta tarea cada vez que se introduzca en el entorno un nuevo equipo que tenga que utilizar la red inalámbrica.
  
###### Información de resumen
  
-   **Requisitos de seguridad:** pertenencia a Administradores de dominio o permiso para agregar usuarios a la directiva de red inalámbrica - Grupo de seguridad Equipos en Active Directory
  
-   **Frecuencia**: al agregar equipos móviles a la red
  
-   **Requisitos de tecnología**: complemento Usuarios y equipos de Active Directory de MMC
  
###### Detalles de la tarea
  
Después de configurar y activar las directivas de la red inalámbrica, la incorporación de equipos a los grupos de seguridad que controlan la aplicación de la directiva se realiza directamente.
  
**Para agregar equipos al grupo de seguridad Directiva de grupo Red inalámbrica**
  
1.  En el complemento Usuarios y equipos de Active Directory de MMC, busque el grupo de seguridad Directiva de red inalámbrica - Equipo que corresponda a la directiva de red inalámbrica que se va a aplicar. Debe haber iniciado la sesión como usuario con permisos para modificar la pertenencia al grupo.
  
2.  Agregue el equipo al grupo de seguridad seleccionado.
  
    **Nota:** se debe reiniciar el equipo para reflejar esta nueva pertenencia a grupos y para aplicar las directivas inalámbricas. La primera vez que se aplica una directiva inalámbrica, el equipo se *debe* conectar a una red con cables para recibir la configuración inalámbrica. Los cambios posteriores se pueden aplicar a través de una WLAN.
  
##### Adición de equipos y usuarios a grupos de directiva de acceso remoto
  
La adición de equipos y usuarios al grupo de seguridad de directiva de acceso remoto autoriza el acceso a la WLAN. IAS utiliza la pertenencia a este grupo en la directiva de acceso remoto como condición de coincidencia para permitir el acceso. Debe agregar los equipos y usuarios a los grupos de la directiva de acceso remoto para que se pueda producir la autorización satisfactoria para la WLAN.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia a Administradores de dominio o permiso para modificar la pertenencia a Directiva de acceso remoto - Grupos de seguridad Usuarios inalámbricos y Directiva de acceso remoto - Equipos inalámbricos de Active Directory
  
-   **Frecuencia**: Al conceder a los usuarios acceso a la WLAN
  
-   **Requisitos de tecnología**: complemento Usuarios y equipos de Active Directory de MMC
  
###### Detalles de la tarea
  
Después de crear los grupos de seguridad de la directiva de acceso remoto, la adición de equipos y usuarios adicionales a los grupos de seguridad que controlan el acceso a la WLAN es bastante sencilla.
  
**Para agregar usuarios al grupo de seguridad Directiva de acceso remoto**
  
1.  Inicie la sesión en un equipo de administración como miembro de Administradores de dominio o usuario con permisos para modificar la pertenencia al grupo de seguridad Directiva de acceso remoto - Usuarios inalámbricos.
  
2.  En el complemento Usuarios y equipos de Active Directory de MMC, busque el grupo de seguridad Directiva de acceso remoto - Usuarios inalámbricos que corresponda a la directiva de acceso remoto que controle el acceso a la LAN inalámbrica.
  
3.  Agregue el usuario al grupo de seguridad seleccionado.
  
    **Nota:** el usuario debe cerrar la sesión y volver a iniciarla para recibir la nueva pertenencia a grupos y acceder a la WLAN.
  
**Para agregar equipos al grupo de seguridad Directiva de acceso remoto**
  
1.  Inicie la sesión en un equipo de administración como miembro de Administradores de dominio o usuario con permisos de seguridad para modificar la pertenencia al grupo de seguridad Directiva de acceso remoto - Equipos inalámbricos.
  
2.  En el complemento Usuarios y equipos de Active Directory de MMC, busque el grupo de seguridad Directiva de acceso remoto - Equipos inalámbricos que corresponda a la directiva de acceso remoto que controle el acceso a la LAN inalámbrica.
  
3.  Agregue el equipo al grupo de seguridad seleccionado.
  
    **Nota:** se debe reiniciar el equipo para que reciba esta nueva pertenencia a grupos y acceda a la WLAN.
  
#### Supervisión y control de servicios
  
La supervisión del servicio permite al personal de operaciones observar la salud de un servicio de TI en tiempo real.
  
Cuando se hace referencia a Microsoft Operations Manager (MOM) en esta sección, se supone que la implementación MOM que tiene sigue las instrucciones de la MOM Operations Guide. Sin embargo, MOM no es necesario, se utiliza únicamente como ejemplo. Consulte la sección "Información adicional" que aparece al final de este capítulo para obtener información acerca de la MOM Operations Guide.
  
##### División en categorías de las alertas de supervisión
  
El sistema de supervisión sólo debe mostrar las alertas más importantes al personal de operaciones. Si todos los errores, por pequeños que sean, se trasladan a un nivel superior para producir alertas de incidentes, el personal de operaciones no podrá distinguir lo que es urgente de lo que no lo es y se requerirá un estudio a largo plazo.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: ninguno
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**: consola de alertas operativa (como MOM)
  
###### Detalles de la tarea
  
En este documento, se utilizan las categorías de alerta siguientes. De ellas, sólo las tres primeras (Servicio no disponible, Infracción de seguridad y Error crítico) deben producir alertas en la consola del operador que requieran atención inmediata. Los errores y advertencias no se consideran urgentes y se deben dirigir al personal de soporte técnico operativo de RADIUS y WLAN para su resolución. Estas categorías de sucesos son las predeterminadas que utiliza MOM y en las descripciones de tarea más adelante de esta sección se hará referencia a ellas.
  
**Tabla 12.8: Categorías de alerta**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Categoría de alerta</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicio no disponible</td>
<td style="border:1px solid black;">Cuando la aplicación o el componente está completamente no disponible.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Infracción de seguridad</td>
<td style="border:1px solid black;">Cuando se detecta un intruso o compromiso de seguridad en la aplicación.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Error crítico</td>
<td style="border:1px solid black;">Cuando la aplicación experimenta un error crítico que requiere una acción administrativa pronto (pero no inmediatamente). La aplicación o componente funciona con un nivel de rendimiento inferior, pero todavía puede realizar las operaciones más importantes.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Cuando la aplicación experimente un problema transitorio que no necesita ninguna acción o resolución administrativa inmediata. La aplicación o componente funciona con un nivel de rendimiento aceptable y todavía puede realizar todas las operaciones más importantes.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Advertencia</td>
<td style="border:1px solid black;">Cuando la aplicación genera un mensaje de aviso que no necesita ninguna acción o resolución administrativa inmediata. La aplicación o componente funciona con un nivel de rendimiento aceptable y todavía puede realizar todas las operaciones más importantes. Sin embargo, esta situación podría cambiarse a Error, Error crítico o Servicio no disponible si el problema continúa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Información</td>
<td style="border:1px solid black;">Cuando la aplicación genera un evento informativo. La aplicación o componente funciona con un nivel de rendimiento aceptable y realiza todas las operaciones importantes y secundarias.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Cuando la aplicación genera un evento de éxito. La aplicación o componente funciona con un nivel de rendimiento aceptable y realiza todas las operaciones importantes y secundarias.</td>
</tr>
</tbody>
</table>
  
##### Supervisión de las restricciones de capacidad de IAS
  
La detección de las restricciones de la capacidad potencial resulta esencial para mantener el servicio a un nivel óptimo. A medida que los subsistemas se aproximan a los límites de sus capacidades operativas, el rendimiento se reduce drásticamente (normalmente, de forma no lineal). En consecuencia, es importante supervisar las tendencias de capacidad e identificarlas para hacer frente a restricciones futuras.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: los permisos necesarios los indica la solución de supervisión
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**:
  
    -   Monitor del sistema
  
    -   Consolidador de contador de rendimiento (como MOM)
  
    -   Consola de alertas operativa (como MOM)
  
    -   Herramientas de planeamiento de capacidad
  
###### Detalles de la tarea
  
Los siguientes contadores de rendimiento son los más útiles para identificar las restricciones de capacidad en IAS. El procesador y el disco son los dos recursos que IAS utiliza más y, probablemente, indicarán restricciones antes que la red o la memoria.
  
**Tabla 12.9: Elementos que se deben supervisar para conocer las restricciones de capacidad de IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Objeto de rendimiento</th>
<th style="border:1px solid black;" >Contador de rendimiento</th>
<th style="border:1px solid black;" >Instancia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesador</td>
<td style="border:1px solid black;">% de tiempo de procesador</td>
<td style="border:1px solid black;">_Total</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Disco físico</td>
<td style="border:1px solid black;">% Tiempo de disco</td>
<td style="border:1px solid black;">_Total</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Disco físico</td>
<td style="border:1px solid black;">Long. promedio de cola de lectura de disco</td>
<td style="border:1px solid black;">_Total</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Disco físico</td>
<td style="border:1px solid black;">Long. promedio de cola de escritura de disco</td>
<td style="border:1px solid black;">D: (IAS–DATA)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interfaz de red</td>
<td style="border:1px solid black;">Total de bytes/s.</td>
<td style="border:1px solid black;">Adaptador NW</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Memoria</td>
<td style="border:1px solid black;">% de bytes asignados en uso</td>
<td style="border:1px solid black;">---</td>
</tr>
</tbody>
</table>
  
Para obtener más información general acerca de las restricciones de capacidad y los contadores de rendimiento relacionados, consulte la referencia en la sección "Información adicional" al final de este capítulo.
  
También es esencial supervisar los indicadores de capacidad en las infraestructuras de apoyo. Los elementos clave son:
  
-   **Comunicaciones de IAS con Active Directory**. IAS utiliza mucho Active Directory para llevar a cabo la autenticación y algunos servicios de autorización.
  
-   **Clientes RADIUS como puntos de acceso inalámbricos**. Estos clientes se comunican con los clientes y con IAS mediante el Protocolo de autenticación extensible (EAP) y protocolos de RADIUS.
  
-   **Comunicaciones relacionadas con el cliente y Active Directory**. Los clientes de LAN inalámbricas utilizan los controladores de dominio de Active Directory para realizar la autenticación de directivas de grupo y dominio nativo.
  
#### Administración de almacenamiento
  
La administración de almacenamiento utiliza el almacenamiento en el sitio y fuera del sitio para la restauración de datos y el archivado histórico. El equipo de administración de almacenamiento debe garantizar la seguridad física de las copias de seguridad y archivos. La administración de almacenamiento define, realiza el seguimiento y mantiene los datos y los recursos de datos en el entorno de TI de producción.
  
##### Configuración de la exportación de la configuración de IAS
  
Esta tarea programa una tarea que se produce cada noche y exporta el estado de configuración parcial de IAS para facilitar la restauración del sistema si se produce un incidente catastrófico. El estado de configuración completo de IAS contiene la configuración del cliente RADIUS, que es información de seguridad confidencial. Por ello, la instrucción de exportación de la parte del cliente RADIUS del estado de configuración se detalla por separado. Necesitará los dos tipos de copia de seguridad para llevar a cabo la restauración completa de cada servidor IAS al nivel de servicio de producción.
  
Una copia de seguridad completa del servidor IAS incluye la información de configuración del sistema operativo y cualquier otra información de estado de la que dependa el servidor IAS. Esta tarea se ha diseñado para que el servidor se pueda volver a instalar, se vuelva a instalar el componente IAS optativo y se restaure el estado de configuración. Esta configuración facilita la restauración del servicio para un servidor que haya dejado de estar en un estado de configuración conocido (no confiable) o cuya seguridad esté amenazada.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: miembro del grupo de seguridad Administradores local
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**:
  
    -   Secuencias de comandos MSS
  
    -   Servicio del programador de tareas de Windows
  
    -   SchTasks.exe
  
###### Detalles de la tarea
  
Esta tarea configura una tarea programada para la creación de una copia de seguridad nocturna del estado de configuración del servidor IAS. La copia de seguridad de IAS supone que la organización dispone de un sistema de copia de seguridad del servidor de empresa; la copia de seguridad de este procedimiento se guardará en un archivo del que, a su vez, puede hacer una copia de seguridad el sistema de copia de seguridad. El sistema de copia de seguridad principal puede ser una copia de seguridad de red, una copia de seguridad de red de área de almacenamiento (SAN) o una copia de seguridad de dispositivo local. La solución también supone que el sistema de copias de seguridad del servidor se ejecuta durante la noche para crear copias de seguridad de los discos del servidor IAS.
  
**Para configurar una copia de seguridad de la configuración de IAS**
  
1.  Programe el trabajo de copia de seguridad para que se ejecute durante la noche mediante el comando siguiente. Este comando establece que el trabajo se ejecutará a las 2:00 a.m. cada noche.
  
    SCHTASKS /Create /RU system /SC Daily /TN "IAS Backup" /TR \\"C:\\MSSScripts\\IASExport.bat\\" /ST 02:00
  
    (Este comando puede mostrarse en varias líneas; escríbalo como una sola.)
  
    **Nota:** la barra diagonal inversa y las comillas mostradas a ambos lados del nombre de secuencia de comandos C:\\MSSScripts\\IASExport.bat sólo son necesarias si el nombre de ruta o de archivo contienen espacios. El carácter de barra diagonal inversa se utiliza para indicar el código de "escape" de comillas en el nombre de la secuencia de comandos para que se guarden como parte de la línea de comandos del trabajo schtasks. Estos caracteres pueden omitirse si no hay espacios en el nombre de la ruta de acceso.
  
2.  Configure el sistema de copia de seguridad del servidor de manera que haga cada noche una copia de seguridad del contenido del directorio D:\\IASConfig en un medio extraíble. Si es posible, defina una secuencia de comandos que sea una condición previa para comprobar que la fecha y hora de los archivos de texto de configuración de IAS creados a partir del archivo IASExport.bat tengan menos de 24 horas. Si los archivos tienen una marca de fecha y hora anterior a las últimas 24 horas, significa que se produjo un error en la copia de seguridad anterior o la misma aún se encuentra en ejecución.
  
    **Nota:** la secuencia de comandos IASExport.bat puede utilizarse como punto de partida de esta tarea. Puede modificar la lógica de la secuencia de comandos IASExport.bat de manera que las situaciones de error de la herramienta **netsh** utilizada en dicha secuencia de comandos generen sucesos o notificaciones que sean detectados por el personal de operaciones.
  
Considere la posibilidad de habilitar la auditoría de archivos de Windows en el directorio D:\\IASConfig e indicar a los auditores de seguridad del servidor que revisen los datos de auditoría periódicamente por si se produce una actividad anormal (por ejemplo, errores de acceso). La información del directorio D:\\IASConfig podría ayudar a un usuario malintencionado a saber cómo poner en peligro el control de acceso a la red.
  
##### Exportación de la configuración del cliente RADIUS
  
Debe exportar la configuración del cliente RADIUS desde el servidor IAS para garantizar que se puede recuperar esta información en caso de que se produzca un error catastrófico del servidor. La información del cliente RADIUS es confidencial para la seguridad ya que contiene secretos de RADIUS empleados entre cada servidor y punto de acceso inalámbrico. Por lo tanto, los datos de cliente RADIUS exportados se exportan en un medio extraíble que debe guardar en una ubicación segura. Los datos de configuración de cliente RADIUS exportados normalmente son exclusivos de cada servidor IAS.
  
Para lograr una restauración completa de una configuración de servidor IAS, tiene que restaurar los datos de configuración de cliente RADIUS, que se han creado en esta tarea, y los datos de configuración del sistema IAS, que se han creado con la secuencia de comandos IASExport.bat del procedimiento anterior.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: miembro del grupo de seguridad Administradores de IAS
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**:
  
    -   Secuencias de comandos MSS
  
    -   Disquete u otro medio extraíble con permisos de escritura
  
###### Detalles de la tarea
  
La información del cliente RADIUS se exporta mediante el comando **netsh**. Esta guía incluye un archivo por lotes que exportará la información del cliente RADIUS a un disquete u otro medio extraíble.
  
**Para exportar la configuración del cliente RADIUS**
  
1.  Inicie la sesión en el servidor IAS desde el que desee guardar los datos de cliente RADIUS y ejecute el siguiente comando desde un símbolo del sistema:
  
    C:\\MSSScripts\\IASClientExport.bat
  
2.  Investigue los errores o advertencias mostrados y rectifíquelos. Después de que la situación se rectifique, ejecute la secuencia de comandos de nuevo.
  
3.  Almacene adecuadamente el medio de copia de seguridad. Estos datos de copia de seguridad son muy confidenciales porque contienen secretos que se pueden utilizar para obtener acceso a la WLAN corporativa. Debe tratar estos datos con el mismo nivel de seguridad que el propio servidor IAS. Debe almacenar los datos de copia de seguridad en un sitio físico distinto del propio servidor IAS, lo que permitirá recuperarlo si se destruye todo el equipo informático del sitio o no se puede acceder a él.
  
##### Configuración de la copia de seguridad de los directorios de datos de IAS
  
La finalidad de esta tarea es la de indicar qué directorios del servidor IAS requieren copia de seguridad para permitir la completa recuperación del sistema del estado de configuración de IAS y de los datos de registro de RADIUS si se produce un error de servidor fatal. Una copia de seguridad completa del servidor IAS incluye la información de configuración del sistema operativo y cualquier otra información de estado del sistema de la que dependa el servidor IAS.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: miembro del grupo de seguridad Operadores de copia de seguridad local
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**:
  
    -   Copia de seguridad de Windows o sistema de copia de seguridad de empresa
  
    -   Servicio del programador de tareas de Windows
  
    -   SchTasks.exe
  
###### Detalles de la tarea
  
Esta tarea enumera los directorios de los que se debe hacer copia de seguridad para garantizar que sea posible una restauración completa del estado de la configuración de IAS y de los datos de los archivos de registro. En esta tarea se supone que se dispone de un sistema de copia de seguridad del servidor de empresa. El sistema puede ser una copia de seguridad de red, una copia de seguridad de SAN o una copia de seguridad de dispositivo local. La solución supone también que el sistema de copia de seguridad de servidor de empresa se ejecuta todas las noches después de la copia de seguridad del estado de configuración de IAS (02:00) para realizar la copia de seguridad de los discos del servidor IAS.
  
**Para configurar una copia de seguridad del directorio de datos de IAS**
  
1.  Compruebe que la copia de seguridad del estado de configuración de IAS esté programada correctamente y que se ejecute con éxito. La tarea programada del estado de configuración de IAS copia el estado de configuración de IAS en archivos del disco duro.
  
2.  Utilice el Bloc de notas para crear un archivo llamado backuptest.txt en el directorio D:\\IASLogs. Escriba en el archivo **Utilizado para la comprobación de las copias de seguridad y restauración**. Guarde el archivo y cierre el Bloc de notas. Este archivo se utilizará posteriormente en los procedimientos de comprobación de la restauración.
  
    Configure el sistema de copia de seguridad del servidor de empresa para que realice una copia de seguridad completa, incremental o diferencial de los siguientes directorios:
  
    -   D:\\IASConfig
  
    -   D:\\IASLogs
  
3.  Revise los archivos de registro del sistema de copia de seguridad del servidor para asegurarse de que no se han producido errores ni advertencias. Si encuentra alguno, considere la posibilidad de ejecutar las secuencias de comandos de exportación de la configuración de IAS manualmente y realizar otra copia de seguridad completa de los dos directorios.
  
4.  Almacene adecuadamente el medio de copia de seguridad. Los datos de la copia de seguridad son confidenciales, ya que contienen la configuración del software del servidor que permite el acceso a la WLAN de la organización. Debe tratarlos con el mismo nivel de seguridad que se le proporciona al servidor IAS. Debe almacenar los datos de copia de seguridad en un sitio físico distinto del propio servidor IAS, lo que permitirá recuperarlo si se destruye todo el equipo informático del sitio o no se puede acceder a él.
  
##### Prueba de la copia de seguridad de IAS
  
La finalidad de esta tarea es la de garantizar que el proceso y la tecnología de la copia de seguridad funcionan correctamente, para lo que se realiza una restauración de prueba. La restauración completa de copias de seguridad en otro hardware de servidor proporciona la confianza total de que los procedimientos de copia de seguridad funcionan correctamente. Sin embargo, este procedimiento se ha creado de forma que los clientes que no tengan acceso a otro hardware de servidor puedan probar los procesos de restauración en el servidor de producción, con cierto nivel de riesgo. Las pruebas de los procedimientos de restauración en los servidores de producción tienen el riesgo de que una restauración parcial puede dejar un servidor inutilizable.
  
Las pruebas de las copias de seguridad garantizan que, si se produce un incidente catastrófico, los pasos de restauración se conocen bien y están libres de errores técnicos o de procedimiento, que podrían impedir la restauración completa.
  
Los datos de restauración del servidor IAS constan de lo siguiente:
  
-   **Datos de exportación del estado de configuración de IAS**. Se encuentran en el directorio D:\\IASConfig. Cuando se restaura de cinta, esta información se utiliza para volver a importar la configuración en el servidor IAS y se crea según los pasos de la tarea "Configuración de la exportación de la configuración de IAS" de este capítulo.
  
-   **Datos de exportación del cliente RADIUS**. Se encuentra en el disquete u otro medio extraíble con permiso de escritura etiquetado "Clientes de RADIUS para *&lt;nombre de servidor&gt;*". Esta información se utiliza para restaurar la configuración del cliente RADIUS en el servidor IAS y se crea según los pasos de la tarea "Exportación de la configuración del cliente RADIUS" de este capítulo.
  
-   **Datos de registro de solicitud de RADIUS**. Se encuentran en el directorio D:\\IASLogs. Cuando la restauración se hace desde una cinta, esta información contiene los datos históricos que utilizan los auditores de seguridad de IAS. Estos datos se crean con el tiempo, a media que el servicio IAS registra información de RADIUS en el disco.
  
Antes de llevar a cabo una restauración de prueba, debe realizar manualmente una exportación de los datos de exportación de la configuración de IAS y los datos de exportación del cliente RADIUS. Siga este procedimiento con una copia de seguridad no programada de los datos del servidor en cintas especiales y guárdelas para utilizarlas sólo si se produce un problema durante la restauración de prueba. Este enfoque reduce el riesgo de que no se perciban errores y cintas con problemas al realizar copias de seguridad normales, lo que haría que sólo se consiguiera una restauración parcial del servidor de producción.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: administradores locales u operadores de copia de seguridad en equipo de prueba
  
-   **Frecuencia**:
  
    -   Antes de que el servidor IAS esté operativo
  
    -   Mensualmente
  
    -   Vuelva a hacer pruebas siempre que se haga algún cambio en la tecnología o el proceso de copia de seguridad
  
-   **Requisitos de tecnología**:
  
    -   Copia de seguridad de Windows o sistema de copia de seguridad de empresa
  
    -   Secuencias de comandos MSS
  
###### Detalles de la tarea
  
En esta tares se describe la restauración y comprobación de los datos de IAS. Se restaurarán los tres tipos de datos y se utilizarán procedimientos especiales para comprobar la restauración. Asegúrese de utilizar una copia de seguridad reciente (de la noche anterior) que se llevó a cabo correctamente. Asimismo, asegúrese, antes de comenzar la prueba, que no se ha efectuado ningún trabajo de administración (por ejemplo, algún tipo de cambio de configuración) en el servidor de destino desde la última copia de seguridad.
  
Si intenta restaurar en una copia recién instalada de Windows Server 2003, debe realizar los requisitos previos de generación de servidor del capítulo 8, "Implementación de la infraestructura de RADIUS para la seguridad de LAN inalámbricas", con el fin de garantizar que el hardware y el software del servidor están configurados correctamente para IAS.
  
**Nota:** es posible que deba volver a seleccionar RAS y el certificado de autenticación de servidor IAS recién instalados desde la directiva de acceso a WLAN restaurada.
  
**Para probar la copia de seguridad de IAS**
  
**Nota:** el primer paso de este procedimiento es optativo y se utiliza en entornos de laboratorios de pruebas en hardware de servidores que no son de producción. Resulta útil asegurarse de que un servidor se puede recuperar desde un estado de instabilidad o de peligro para la seguridad.
  
1.  Para restaurar un servidor que ha sufrido un error de hardware o software irrecuperable o su seguridad ha estado en peligro (como una infección de virus), reinstale Windows Server 2003 según lo indicado en el capítulo 8, "Implementación de la infraestructura de RADIUS". Asegúrese de copiar las secuencias de comandos de MSS desde los medios de distribución al directorio C:\\MSSScripts del servidor.
  
2.  Acceda al directorio D:\\IASLogs y busque el archivo backuptest.txt. Si no existe, continúe en el siguiente paso. Si encuentra el archivo backuptest.txt, elimínelo. El archivo backuptest.txt se ha creado durante el procedimiento "Configuración de la copia de seguridad de los directorios de datos de IAS". Se ha hecho de configuración del mismo con los registros de solicitudes de RADIUS de IAS y permite comprobar que puede restaurar datos de la copia de seguridad sin tener que restaurar los registros de RADIUS. Si lo prefiere, puede restaurar los datos del registro de solicitudes de RADIUS desde D:\\IASLogs. Sin embargo, la sobrescritura de los datos del archivo de registro puede producir la pérdida de datos si falla la restauración.
  
3.  3. Abra el complemento Servicio de autenticación de Internet de MMC, seleccione las propiedades del objeto **Servicio de autenticación de Internet (local)** y observe la ficha **General**. Agregue el texto "**(Prueba de restauración)**" al campo **Descripción de servidor**. Haga clic en **Aceptar** para cerrar el cuadro de diálogo Propiedades de IAS. Cambiar la cadena de descripción del servidor permite ver si las opciones de configuración de IAS de las que se ha hecho copia de seguridad anteriormente se han restaurado. Después de restaurar las opciones de configuración de IAS anteriores, la cadena **Descripción de servidor** se habrá sobrescrito por el valor anterior y habrá desparecido el texto "**(Prueba de restauración)**".
  
4.  Con el complemento **Servicio de autenticación de Internet** de MMC, haga clic con el botón secundario del mouse en la carpeta **Clientes RADIUS** y seleccione **Nuevo cliente RADIUS**. Escriba **Prueba de restauración** como **Nombre descriptivo** y **127.0.0.1** como **Dirección del cliente (IP o DNS)**. Escriba una contraseña en los campos **Secreto compartido** y **Confirmar secreto compartido** para este cliente RADIUS y haga clic en **Finalizar**. Una restauración correcta sobrescribirá la información de cliente de RADIUS y este nuevo RADIUS habrá desaparecido.
  
5.  Busque los medios de copia de seguridad que desea probar (como la copia de seguridad programada de la noche anterior) y utilícelos para restaurar los datos siguientes en el disco duro del servidor:
  
    -   D:\\IASConfig\\\*.\*
  
    -   D:\\IASLogs\\BACKUPTEST.TXT
  
6.  Ejecute el siguiente comando en el símbolo del sistema para restaurar en la base de datos de IAS la configuración de IAS guardada anteriormente como archivos de texto. No olvide investigar los errores o las advertencias que aparezcan durante la ejecución de la secuencia de comandos:
  
    C:\\MSSScripts\\IASImport.bat
  
    **Nota:** los siguientes pasos incluyen el uso de un disquete u otro medio extraíble con permisos de escritura etiquetado "Clientes de RADIUS de *&lt;nombre de servidor&gt;*". Asegúrese de utilizar el disco correcto con el servidor adecuado para evitar la pérdida de datos.
  
7.  Busque el disco (u otro medio extraíble y con permiso de escritura) de configuración del cliente RADIUS de este servidor e insértelo en la unidad del servidor. Ejecute el siguiente comando en el símbolo del sistema. No olvide investigar los errores o las advertencias que aparezcan durante la ejecución de la secuencia de comandos:
  
    C:\\MSSScripts\\IASClientImport.bat
  
8.  Cierre y vuelva a abrir el complemento **Servicio de autenticación de Internet** de MMC, seleccione las propiedades del objeto **Servicio de autenticación de Internet (local)** y revise la ficha **General** para asegurarse de que el texto **(Prueba de restauración)** ya no aparece en el campo **Descripción de servidor**. Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Propiedades de IAS**.
  
9.  Seleccione la carpeta Clientes RADIUSy asegúrese de que el cliente RADIUS **Prueba de restauración** ya no aparece en la lista de clientes del panel derecho.
  
10. El resto de la configuración del complemento **Servicio de autenticación de Internet** de MMC debe mostrar los valores anteriores a la prueba de restauración.
  
11. Vaya al directorio D:\\IASLogs y compruebe que aparezca el archivo backuptest.txt. Si los pasos de restauración de este procedimiento se han realizado en un servidor de producción, haga que un auditor de seguridad de IAS revise los archivos de registro para garantizar que están intactos y al día al menos hasta el momento de la copia de seguridad.
  
12. Debe volver a guardar los medios de copia de seguridad y los disquetes en un lugar seguro.
  
#### Administración de seguridad
  
La administración de seguridad es responsable de mantener un entorno de equipo seguro. La seguridad es una parte importante de cualquier infraestructura de TI de una empresa. La mayoría de los sistemas de información con una base de seguridad débil, acabarán experimentando una infracción en seguridad.
  
##### Registros de solicitudes de RADIUS de acceso a IAS
  
IAS puede, opcionalmente, registrar diversos sucesos que se originan en solicitudes de RADIUS de AP inalámbricos en registros de solicitudes de RADIUS ubicados en el disco duro del servidor. Los registros de RADIUS resultan útiles por varias razones, como la identificación de posibles ataques al sistema y el acceso no autorizado a la red de la organización. En esta tarea se describen métodos de inspección de los registros de solicitudes de RADIUS, si bien una descripción pormenorizada de dichos registros está fuera del alcance de esta guía.
  
Se pueden utilizar varios métodos para analizar los registros de solicitudes de RADIUS, porque se guardan como texto en formato de IAS o en formato de importación de base de datos. Esta solución ha elegido el formato de importación de base de datos para los archivos de registro debido a la relativa facilidad con que se importan en aplicaciones que aceptan archivos de texto delimitado por comas. Los métodos para revisar los registros de solicitudes de RADIUS de IAS son:
  
-   **Explorando los archivos de registro directamente con la utilidad IASPARSE**. Esta herramienta está disponible en las Herramientas de soporte técnico de Windows Server 2003 y, por motivos de rendimiento, normalmente se instala y ejecuta en mismo servidor IAS. Por lo tanto, se requiere una sesión de conexión de Escritorio remoto (u otro medio de ejecución remota). De manera predeterminada, esta solución no está configurada para admitir este método de revisión de los archivos de registro.
  
-   **Importación de los archivos de registro en Microsoft Access 2002 desde un equipo de administración remoto**. Con este método, un administrador puede importar los registros en una tabla de Microsoft Access para realizar consultas ocasionales o como parte de un esquema de archivado de informes estructurado. Este método de revisión de archivos de registro es la opción de utilizada por esta solución ya que supone un buen equilibrio entre simplicidad y flexibilidad. Los clientes empresariales también pueden considerar la siguiente opción utilizando el registro basado en Microsoft SQL Server™ 2000.
  
-   **Acceso a la información de registro a través de un clúster central de SQL Server 2000** en el que se han replicado los datos desde MSDE 2000 en cada servidor IAS. Cada servidor IAS registra en su instancia local de MSDE. La configuración para esta situación es bastante compleja; sin embargo, Microsoft ha publicado notas del producto y código que le ayudarán en el proceso. Para obtener ayuda y configurar el registro de SQL de esta forma, póngase en contacto con un socio de Microsoft o el jefe de su cuenta de Microsoft, que le pueden poner en contacto con el socio adecuado o los profesionales de los servicios de consultoría de Microsoft.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: miembro del grupo de seguridad Auditores de seguridad de IAS
  
-   **Frecuencia**: diaria o semanalmente, según los requisitos de seguridad
  
-   **Requisitos de tecnología**:
  
    -   IASPARSE
  
    -   Microsoft Access
  
    -   Microsoft Excel
  
###### Detalles de la tarea
  
Los registros de solicitudes de RADIUS se generan en cada servidor de esta solución y se guardan en un volumen de disco dedicado. Los pasos para tener acceso a estos archivos de registro son: establecer una conexión de red con cada servidor IAS, revisar los archivos de registro y eliminarlos cuando ya no sean necesarios. Los servidores IAS de esta solución están configurados para crear un nuevo registro de solicitudes de RADIUS al mes, pero puede cambiar este intervalo para adaptarlo a sus necesidades concretas.
  
La tabla que cree con Access recibirá un formato adecuado para el tipo de datos que contenga cada campo. Aunque en este ejemplo se muestra cómo crear una nueva tabla, también puede importar un registro en una tabla existente.
  
**Para importar archivos de registro de solicitudes de RADIUS en Microsoft Access**
  
1.  Inicie la sesión en una estación de trabajo de administración como miembro del grupo de seguridad Auditores de seguridad de IAS de Active Directory y asigne una conexión de unidad al servidor IAS cuyos registros desea revisar. Introduzca el siguiente comando en un símbolo del sistema y reemplace HQ-IAS-01 por el nombre de su servidor IAS:
  
    NET USE X: \\\\HQ-IAS-01\\IASLogs
  
2.  Busque el archivo de registro correspondiente al mes que desea ver. El nombre del archivo de registro un formato que muestra la fecha de creación del archivo. Cree una copia del archivo de registro y cambie el nombre de la copia por una extensión de nombre de archivo .txt.
  
3.  Agregue las dos líneas completas del archivo de texto C:\\MSSScripts\\IASAccessPrep.txt al comienzo del archivo de registro copiado. La primera línea contiene los nombres de atributo de cada campo del registro y Access los utiliza para crear los nombres de los campos de la tabla. La utilización de nombres de atributo facilita la interpretación de las entradas del registro. Access utiliza la segunda línea para configurar el tipo de datos adecuado para cada columna de la tabla. Después de importar el archivo de registro, debe eliminar estas entradas de la tabla de Access.
  
4.  En Access 2002, haga clic en **Base de datos en blanco**. En **Archivo nueva base de datos**, especifique un nombre de archivo y, a continuación, haga clic en **Crear una tabla introduciendo datos**. Haga clic en **Archivo**, en **Obtener datos externos** y, a continuación, en **Importar**.
  
5.  Haga clic en **Importar**, en **Archivos de tipo**, en **Archivos de texto**, busque el archivo de registro de IAS, selecciónelo y, finalmente, haga clic en **Importar**. En el **Asistente para importación de texto**, haga clic en **Avanzado**.
  
6.  Haga clic en **Especificación de importación**:
  
7.  En **Formato de archivo**, haga clic en **Delimitado**.
  
8.  En **Delimitador de campo**, seleccione **,** (coma).
  
9.  En **Cualificador de texto**, seleccione " (comillas).
  
10. En **Fechas, hora y número**, seleccione **Años en cuatro cifras** y **Ceros no significativos en fechas** y, a continuación, escriba el **Orden de la fecha** (por ejemplo, MDA) adecuado, **Delimitador de fecha** (por ejemplo, **/** o **barra diagonal**), **Delimitador de hora** como **:** (dos puntos) y **Símbolo decimal** como . (punto).
  
11. En el cuadro de diálogo **Asistente de importación de texto**, haga clic en **Siguiente**, seleccione **Primera fila contiene nombres de campos** y, a continuación, haga clic en **Siguiente**. Seleccione **En una nueva tabla** y, a continuación, haga clic en **Siguiente**.
  
12. Deje los valores predeterminados en **Opciones de campo** y, a continuación, haga clic en **Siguiente**. Haga clic en **Permitir a Access agregar la clave principal** y, a continuación, haga clic en **Siguiente**. En **Importar a la tabla** escriba el nombre de la nueva tabla. Haga clic en **Finalizar**.
  
13. En el cuadro de diálogo **Nombre de archivo: base de datos**, escriba el nombre de la base de datos y, a continuación, haga clic en **Abrir** para ver la tabla.
  
##### Revisión de las entradas de los registros de sucesos de autenticación de RADIUS de IAS
  
Los auditores de seguridad pueden utilizar esta tarea periódicamente para comprobar si ha habido intentos de acceso no autorizado a la red inalámbrica. La directiva de seguridad interna puede indicar la necesidad de revisar periódicamente los sucesos de autenticación de RADIUS en el registro de sucesos para detectar intentos de autenticación o el uso de credenciales de certificados robadas. También puede utilizar una herramienta de administración, como MOM, para generar alertas cuando se registren sucesos sospechosos.
  
Esta tarea es opcional y se puede considerar como una alternativa al registro RADIUS de IAS descrito anteriormente. Para realizar esta tarea es necesario ser miembro del grupo Administradores de IAS o del grupo Administradores local del servidor.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo Administradores de IAS o al grupo de Administradores incorporado local
  
-   **Frecuencia**: diaria o semanalmente, según los requisitos de seguridad
  
-   **Requisitos de tecnología**:
  
    -   Visor de eventos
  
    -   Si se desea, se puede utilizar EventCombMT o EventFilter del Kit de recursos de Windows Server 2003
  
###### Detalles de la tarea
  
Esta tarea resulta adecuada para entornos de TI en los que los auditores de seguridad de IAS y los administradores del sistema de IAS son las mismas personas. Por el contrario, los registros de RADIUS los pueden ver operadores que no son administradores locales del servidor. Esta solución no proporciona a los auditores de seguridad el privilegio de administradores locales. Para poder realizar esta tarea, debe agregar al auditor al grupo de seguridad Administradores de IAS en Active Directory.
  
**Para buscar errores de intento de autenticación en el Registro de sucesos mediante Visor de sucesos**
  
1.  Inicie la sesión en uno de los servidores IAS como miembro del grupo de seguridad Administradores de IAS.
  
2.  Abra Visor de sucesos (haga clic en **Inicio**, **Todos los programas** y, a continuación, en **Herramientas administrativas**).
  
3.  Haga clic en el **Registro de sucesos del sistema**.
  
4.  En el menú **Ver**, haga clic en **Filtro**.
  
5.  Seleccione un **Origen de sucesos** de **IAS** y un **Id. de suceso** de **2**.
  
6.  Investigue los errores de autenticación frecuentes u otras entradas sospechosas.
  
    **Nota:** también puede utilizar la herramienta Eventquery (en Windows XP y Windows Server 2003) y las herramientas EventFilter o EventCombMT del Kit de recursos de Windows Server 2003 para ver los sucesos de IAS.
  
##### Archivado y eliminación de los archivos de registro de RADIUS de IAS
  
IAS incluye una característica para eliminar el archivo de registro de RADIUS de IAS cuando se llena el disco de registro. Si no utiliza esta función automatizada, tendrá que archivar y eliminar manualmente los archivos de registro de solicitudes de RADIUS de IAS para asegurarse de que IAS no se queda sin espacio en disco. La falta de espacio provocará que IAS deje de servir las solicitudes de autenticación y de cuentas de los puntos de acceso inalámbricos. También puede automatizar el archivado de registros mediante una secuencia de comandos o una estrategia de replicación de SQL Server 2000 automatizada (según lo descrito en la tarea "Acceso a los registros de solicitudes de RADIUS de IAS" anteriormente en este capítulo).
  
**Nota:** esta solución utiliza la característica de IAS para eliminar automáticamente el archivo de registro más antiguo después de un suceso de disco lleno.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Auditores de seguridad de IAS de Active Directory
  
-   **Frecuencia**: mensual
  
-   **Requisitos de tecnología**: comandos de Windows nativos
  
###### Detalles de la tarea
  
Existen numerosos métodos de archivado y eliminación para los registros de solicitudes de autenticación y de cuentas de RADIUS. Por ejemplo, una secuencia de comandos de copia de seguridad basada en el servidor puede notificar a los auditores de seguridad de IAS por correo electrónico que la copia de seguridad de los archivos de registro termina correctamente. Así, los auditores de seguridad pueden conectarse al servidor IAS y eliminar los archivos de registro más antiguos. O bien los auditores de seguridad de IAS pueden realizar una copia de seguridad de los archivos de registro de RADIUS en una cinta o dispositivo de CD-RW conectado a su equipo de administración y, a continuación, conectarse al servidor IAS y eliminar los archivos de registro más antiguos que ya no se necesitan.
  
En esta solución, IAS está configurado para crear un nuevo archivo de registro cada mes.
  
Debe diseñar una estrategia que conserve suficientes datos en línea para reconstruir la información de acceso a la red para varios escenarios. Por ejemplo, si tiene los datos en línea correspondientes a tres meses en tres archivos de registro independientes, podría necesitar sólo los dos últimos para reconstruir la información de acceso a la red y hacer el seguimiento de los sucesos de seguridad. Por ello, puede archivar y eliminar el más antiguo de los tres archivos de registro y guardar los dos más recientes.
  
Encontrará información sobre la copia de seguridad de los registros de solicitudes de RADIUS y otros datos de IAS en la tarea "Configuración de la copia de seguridad de los directorios de datos de IAS" de este mismo capítulo. En esta tarea se ofrecen instrucciones para archivar y eliminar registros de RADIUS desde una estación de trabajo de administración.
  
**Para archivar y eliminar archivos de registro de solicitudes de RADIUS**
  
1.  Inicie la sesión en una estación de trabajo de administración como miembro del grupo de seguridad Auditores de seguridad de IAS.
  
2.  Asigne una unidad al servidor IAS que archivará los archivos de registro mediante el siguiente comando y reemplace HQ-IAS-01 por el nombre de su servidor IAS:
  
    NET USE X: \\\\HQ-IAS-01\\IASLogs
  
3.  Busque los archivos de registro más antiguos del servidor IAS que se van a archivar y eliminar del servidor. Use NTBACKUP, el comando **copy** u otra herramienta para archivar los archivos de registro seleccionados del recurso compartido en línea en un medio secundario.
  
4.  Elimine los archivos de registro que no desee del recurso compartido en línea.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas del cuadrante de compatibilidad
  
Las SMF del cuadrante de compatibilidad proporcionan tareas reactivas y preventivas para mantener los niveles de servicio deseados. Las funciones reactivas dependen de la capacidad de la organización para reaccionar y resolver incidentes y problemas rápidamente. Las funciones más útiles y preventivas intentan evitar toda interrupción del servicio identificando y resolviendo problemas antes de que los niveles de servicio se vean afectados. Estas funciones realizan una buena supervisión de la solución de servicio según umbrales predefinidos y proporcionan al personal de operaciones el tiempo suficiente para reaccionar ante problemas potenciales antes de que se conviertan en interrupciones del servicio. El cuadrante de compatibilidad está estrechamente relacionado con la SMF de control y supervisión de servicios que se describe en el cuadrante operativo. El control y supervisión de servicios proporciona la información esencial mediante la que el personal de operaciones y de soporte puede detectar los problemas. Los procedimientos descritos en esta sección están diseñados para solucionar las incidencias más comunes que se pueden producir y permiten recuperarse de ellas.
  
Esta sección contiene información relevante para las SMF siguientes:
  
-   Administración de incidentes
  
No hay tareas que correspondan al resto de las SMF:
  
-   Administración de problemas
  
-   Soporte técnico del servicio
  
    **Nota:** cada descripción de tarea incluye la siguiente información de resumen: requisitos de seguridad, frecuencia y requisitos de tecnología.
  
#### Administración de incidentes
  
La administración de incidentes es el proceso de administración y control de errores e interrupciones en el uso o implementación de servicios de TI a partir de su informe por parte de clientes o asociados de TI. La administración de incidentes intenta restaurar el funcionamiento normal del servicio tan rápido como sea posible y minimizar el impacto adverso sobre las operaciones empresariales, asegurando así el mantenimiento de la mayor calidad y disponibilidad posibles de los niveles de servicio. El funcionamiento normal del servicio se define como el funcionamiento del servicio dentro de los límites del contrato de nivel de servicio (SLA).
  
**Nota:** para la solución general de problemas de cliente inalámbrico de Windows XP, consulte las referencias de la sección "Información adicional" al final de este capítulo.
  
##### Comprobación del estado de la carpeta de conexiones de red del cliente
  
La carpeta Conexiones de red y los iconos de notificación de Windows XP proporcionan información de estado de la autenticación de WLAN. Esta tarea permite a los usuarios finales o al personal de asistencia técnica comprobar el estado de la conexión inalámbrica del equipo cliente. Si una autenticación requiere información adicional por parte del usuario, como la selección de un certificado de usuario entre varios, se muestra un globo de texto con instrucciones para el usuario. Esta tarea se utiliza durante la solución de problemas.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores local para hacer modificaciones en las opciones de la WLAN
  
-   **Frecuencia**: al solucionar un problema de un usuario
  
-   **Requisitos de tecnología**: Windows XP Professional
  
###### Detalle de tareas
  
En la carpeta Conexiones de red, el texto que se muestra debajo del nombre de la conexión correspondiente al adaptador de red inalámbrica describe el estado de la autenticación.
  
Cuando se consulta el estado de la conexión, se puede ver la intensidad de la señal en la ficha **General** y la configuración de dirección IP en la ficha **Compatibilidad**. Si el adaptador inalámbrico tiene una dirección IP privada automática (APIPA) (169.254.0.0/16) o está configurado con la dirección IP alternativa en las propiedades del Protocolo de control de transmisión/Protocolo Internet (TCP/IP) del adaptador, se ha producido un error de autenticación pero el cliente inalámbrico de Windows XP sigue asociado al punto de acceso inalámbrico. Si se produce un error de autenticación y sigue existiendo la asociación, Windows habilita el adaptador inalámbrico y TCP/IP efectúa su proceso de configuración normal. En este ejemplo, debido a que el cliente no se ha autenticado correctamente en la WLAN, no se puede encontrar un servidor DHCP (Protocolo de configuración dinámica de host), por lo que TCP/IP configura automáticamente una APIPA o una dirección alternativa. En tales casos, se recomienda revisar el motivo del error de autenticación de WLAN en el servidor IAS o habilitar y revisar el seguimiento en el equipo cliente.
  
**Para comprobar el estado de la carpeta Conexiones de red**
  
-   Haga clic en **Inicio**, en **Ejecutar**, escriba **ncpa.cpl** y, a continuación, haga clic en **Aceptar**.
  
##### Activación y desactivación del seguimiento en equipos cliente
  
Windows admite información de seguimiento detallada que ayude al personal del servicio de asistencia y a los desarrolladores a solucionar problemas con los componentes del software. El seguimiento brinda un nivel de detalle superior al que se encuentra en los registros de sucesos y guarda esta información en archivos de registro de texto.
  
Para obtener información pormenorizada sobre el proceso de autenticación de EAP, debe activar el seguimiento de los componentes EAP a través de una LAN (EAPOL) y Servicio de acceso remoto - Seguridad de la capa de transporte (RASTLS).
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores local
  
-   **Frecuencia**: según sea necesario al solucionar problemas de clientes de WLAN
  
-   **Requisitos de tecnología**:
  
    -   Windows XP Professional
  
    -   Notepad.exe
  
###### Detalle de tareas
  
Una vez que se hayan emitido los siguientes comandos, vuelva a intentar realizar el proceso de autenticación y revise los archivos Eapol.log y Rastls.log de la carpeta %systemroot%\\Tracing.
  
**Para habilitar el seguimiento en equipos cliente**
  
-   Ejecute los siguientes comandos:
  
    -   **netsh ras set tracing eapol enabled**
  
    -   **netsh ras set tracing rastls enabled**
  
**Para deshabilitar el seguimiento en equipos cliente**
  
-   Ejecute los siguientes comandos:
  
    -   **netsh ras set tracing eapol disabled**
  
    -   **netsh ras set tracing rastls disabled**
  
    **Nota:** el seguimiento consume recursos del sistema y crea archivos de registro que crecen rápidamente. No olvide volver a deshabilitar el seguimiento cuando finalice la tarea de solución de problemas.
  
##### Comprobación del nombre de dominio en equipos cliente
  
La siguiente tarea resulta útil si ha decidido habilitar la comprobación de nombres de dominio de certificado en los equipos cliente. Esta configuración no está habilitada en esta solución porque puede generar cuadros de diálogo de WLAN que posiblemente creen confusión a los usuarios. Windows XP Professional SP1 también tiene esta opción deshabilitada de manera predeterminada.
  
Los equipos cliente no pueden llevar a cabo la comprobación de la revocación de certificados durante la autenticación mutua EAP - TLS, porque normalmente las ubicaciones de la lista de revocación de certificados (CRL) no están disponibles hasta que se concede el acceso a la WLAN. No obstante, los clientes de Windows pueden validar la totalidad o parte del nombre del servidor en el certificado que presenta el servidor IAS. Esta capacidad se configura en las opciones de las directivas de redes inalámbricas en el GPO de clientes inalámbricos (aquí las opciones tienen una interfaz de usuario similar a las propiedades de Redes inalámbricas en las propiedades de adaptador de red inalámbrico del equipo cliente).
  
Si el cliente inalámbrico intenta validar el certificado del servidor y se ha escrito un valor incorrecto para el dominio del servidor IAS en el campo **Conectar si el nombre del servidor termina con**, se producirá un error de autenticación. Es posible que tenga que realizar esta tarea al solucionar problemas de autenticación de cliente si ha decidido activar la opción **Conectar a estos servidores**.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores local
  
-   **Frecuencia**: al instalar o al solucionar problemas de usuario de WLAN
  
-   **Requisitos de tecnología**: Windows XP Professional
  
###### Detalle de tareas
  
Esta tarea permite comprobar que la cadena de nombre de dominio es correcta en el cuadro de diálogo **Propiedades**de la conexión de red del adaptador de red de la WLAN en el cliente o en el GPO Directivas de redes inalámbricas.
  
**Para comprobar la cadena de nombre de dominio en equipos cliente**
  
1.  Haga clic en **Inicio**, en **Ejecutar**, escriba **ncpa.cpl** y, a continuación, haga clic en **Aceptar**.
  
2.  Revise las propiedades de la conexión de red inalámbrica.
  
3.  En la ficha **Redes inalámbricas**, seleccione el Identificador del conjunto de servicios (SSID) de la red de destino entre las redes preferidas y consulte sus propiedades.
  
4.  En la ficha **Autenticación**, observe las propiedades y asegúrese de que la cadena **Conectar si el nombre de servidor termina con** es igual que el nombre de dominio de los servidores IAS.
  
##### Visualización de los sucesos de autenticación de IAS en el registro de sucesos
  
Los sucesos de error de autenticación y de autenticación correcta de los clientes se registran de manera predeterminada en el Registro de sucesos del sistema en los servidores IAS, que puede resultar útil para la solución de problemas. El registro de sucesos está activado de manera predeterminada para todos los tipos de suceso de IAS (sucesos de autenticación rechazados, desechados y correctos) en la ficha **Servicio** de las propiedades del servidor IAS del complemento Servicio de autenticación de Internet de MMC.
  
Con esta tarea, los administradores de IAS pueden ayudar al personal del servicio de asistencia a solucionar problemas de autenticación de usuarios y equipos, mediante la observación de los sucesos de autenticación de los registros de sucesos de servidor IAS.
  
Si el personal del servicio de asistencia requiere acceso a la información de autenticación de clientes inalámbricos de los registros de sucesos del sistema de IAS, dispone de varias opciones:
  
-   Solicite ayuda a un administrador de IAS que pertenezca al grupo de seguridad Administradores de IAS y, así, tenga acceso a los mensajes del registro de sucesos del sistema de IAS. En esta tarea se utiliza esta opción.
  
-   Use un sistema de administración de registros de sucesos corporativo, como MOM, para exportar los registros a una ubicación a la que tenga acceso el personal del servicio de asistencia.
  
-   Conceda al personal del servicio de asistencia el permiso de lectura del recurso compartido IASLogs y del directorio subyacente D:\\IASLogs de NTFS. Indíqueles cómo examinar los archivos de registro con herramientas como IASPARSE, descrita en la tarea "Acceso a los registros de solicitudes de RADIUS de IAS" de este capítulo. La mayor parte de los clientes deseará tener en cuenta esta opción, ya que requiere la infraestructura más sencilla y no representa un riesgo de seguridad excesivo.
  
Conceder a los usuarios que no son administradores acceso a los registros de sucesos del sistema de IAS puede suponer un riesgo de seguridad. Esto resulta un problema para los servidores que combinan IAS y funciones de servidor de controlador de dominio.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad local Administradores de IAS o a un grupo con acceso de lectura y almacenamiento al registro de sucesos del sistema
  
-   **Frecuencia**: al solucionar problemas de autenticación de clientes
  
-   **Requisitos de tecnología**: complemento Visor de sucesos de MMC o EventCombMT del Kit de recursos de Windows Server 2003
  
###### Detalle de tareas
  
Ver los intentos de autenticación en el registro de sucesos del sistema resulta útil para la solución de problemas de los intentos rechazados por IAS. Si dispone de varias directivas de acceso remoto configuradas, puede utilizar el registro para determinar el nombre de la directiva de acceso remoto que aceptó o rechazó el intento de conexión (consulte Directiva - Nombre en la descripción del suceso). Además, el suceso de autenticación (Origen: IAS, Id. de suceso 1 para aceptar y 2 para rechazar) muestra los códigos de las causas con las descripciones correspondientes, como se menciona en Ayuda y soporte técnico de Windows Server 2003.
  
La activación de los registros de sucesos de IAS y la lectura del texto de los sucesos de autenticación de IAS en el registro de sucesos del sistema constituye el mejor método para solucionar problemas de errores de autenticación de IAS.
  
**Para ver el registro de sucesos del sistema de sucesos de autenticación**
  
1.  Haga clic en **Inicio**, **Ejecutar**, escriba **Eventvwr** y, a continuación, haga clic en **Aceptar**.
  
2.  Seleccione **Registro de sucesos del sistema**.
  
3.  En el menú **Ver**, seleccione **Filtro**, elija **IAS** como **Origen del suceso** y, a continuación, haga clic en **Aceptar**.
  
##### Activación y desactivación del seguimiento en el servidor IAS
  
Windows admite información de seguimiento detallada que ayude al personal del servicio de asistencia y a los desarrolladores a solucionar problemas con los componentes del software. El seguimiento brinda un nivel de detalle superior al que se encuentra en los registros de sucesos y guarda esta información en archivos de registro de texto.
  
Microsoft Windows Server 2003 tiene una gran capacidad de seguimiento que se puede utilizar para solucionar problemas complejos de componentes específicos. Puede habilitar los componentes de Windows 2003 Server para que registren la información de seguimiento en archivos mediante el comando **netsh**.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores local del servidor IAS
  
-   **Frecuencia**: según sea necesario al solucionar problemas de conexión a WLAN de cliente
  
-   **Requisitos de tecnología**:
  
    -   Netsh
  
    -   Bloc de notas
  
    -   Regedit
  
###### Detalle de tareas
  
Utilice el comando **netsh** para habilitar y deshabilitar el seguimiento de componentes específicos o de todos los componentes. Los componentes cuya habilitación resulta más útil para el seguimiento de los problemas de autenticación 802.1x basada en EAP-TLS son los siguientes:
  
-   **IASSAM** (**archivo Iassam.log de la carpeta %*systemroot%*\\tracing)**. Este registro es el archivo de seguimiento que se utiliza más habitualmente para problemas de IAS ya que describe funciones como averiguación de nombres de usuario, enlace a un controlador de dominio o verificación de credenciales. Se trata del "centro" de los archivos de seguimiento de IAS y suele ser necesario para depurar los problemas relacionados con la autenticación.
  
-   **RASTLS (archivo Rastls.log de la carpeta %*systemroot%*\\tracing)**. Para todas las autenticaciones relacionadas con EAP y PEAP, este registro contiene la mayor parte de la información de depuración crucial. No obstante, este archivo de registro resulta difícil de leer. Microsoft se está ocupando de producir información que simplifique la interpretación de estos datos.
  
La siguiente información de seguimiento de IAS no se requiere habitualmente para la solución de problemas en la autenticación 802.1X mediante EAP–TLS, pero puede resultar útil para la solución de problemas de otras tareas:
  
-   **IASRAD (archivo Iasrad.log de la carpeta** ***%systemroot%*\\tracing)**. Este registro describe todas las operaciones relacionadas con el protocolo RADIUS. Describe los puertos en los que el servidor escucha, etc. Tampoco se utiliza habitualmente en la depuración de problemas en el servidor IAS.
  
-   **IASSDO (archivo Iassdo.log de la carpeta** ***%systemroot%*\\tracing)**. El registro IASSDO realiza un seguimiento desde la interfaz de usuario hasta los archivos MDB que almacenan la configuración y el diccionario del servidor. Se trata del registro utilizado para depurar problemas de servicio o problemas relacionados con la interfaz de usuario.
  
**Para habilitar el seguimiento en el servidor IAS**
  
-   Ejecute los comandos **netsh** que corresponden a la información de seguimiento requerida. Para la solución de problemas de autenticación de EAP-TLS con 802.1X, se recomiendan los registros IASSAM y RASTLS.
  
    Los comandos **netsh** correspondientes son:
  
    -   **netsh ras set tracing iassam enabled**
  
    -   **netsh ras set tracing rastls enabled**
  
    -   **netsh ras set tracing iasrad enabled**
  
    -   **netsh ras set tracing iassdo enabled**
  
**Para deshabilitar el seguimiento en el servidor IAS**
  
-   Ejecute los comandos **netsh** que corresponden a la información de seguimiento que desea deshabilitar.
  
    Los comandos **netsh** correspondientes son:
  
    -   **netsh ras set tracing iassam disabled**
  
    -   **netsh ras set tracing rastls disabled**
  
    -   **netsh ras set tracing iasrad disabled**
  
    -   **netsh ras set tracing iassdo disabled**
  
        **Nota:** debido a que el seguimiento consume recursos del sistema, no se debe utilizar en exceso para identificar los problemas de la red. Cuando haya realizado el seguimiento o identificado el problema, debe desactivar el seguimiento inmediatamente.
  
Debido a que los registros de seguimiento de IASSAM tienen un tamaño predeterminado de sólo un megabyte (MB), se puede sobrescribir información valiosa de los archivos de registro durante los períodos de gran carga. Realice los siguientes pasos para configurar el registro de seguimiento de IASSAM en 15 MB. Cuando el tamaño del registro llega a 15 MB, se cambia el nombre del archivo a IASSAM.old y se crea un nuevo IASSAM.log. Este procedimiento permite conservar 30 MB de datos en el servidor.
  
**Para configurar el archivo de registro de seguimiento de IASSAM en 15 MB**
  
1.  Inicie Regedit.exe.
  
2.  Vaya a la siguiente clave del Registro: **\\HKLM\\Software\\Microsoft\\Tracing\\**.
  
3.  Actualice la clave **IASSAM** con el valor **MaxFileSize**, el tipo **REG\_DWORD** y el valor de datos **0xF00000**.
  
##### Activación del registro de SChannel en el servidor IAS
  
Canal seguro (SChannel) es un proveedor de compatibilidad de seguridad (SSP) que admite varios protocolos de seguridad de Internet, como Capa de sockets seguros (SSL) y Seguridad de la capa de transporte (TLS).
  
###### Información de resumen
  
-   **Requisitos de seguridad**: pertenencia al grupo de seguridad Administradores local
  
-   **Frecuencia**: según sea necesario al solucionar problemas de conexión del cliente en el servidor IAS
  
-   **Requisitos de tecnología**:
  
    -   Regedit
  
    -   Bloc de notas
  
###### Detalle de tareas
  
El registro de los errores de validación de certificados del cliente es un suceso de canal seguro y no está activado en el servidor IAS de manera predeterminada.
  
**Para habilitar el registro de SChannel en el servidor IAS**
  
Puede habilitar sucesos de canal seguro adicionales cambiando el valor de la siguiente clave del Registro de **1** (tipo **REG\_DWORD**, datos **0x00000001**) a **3** (tipo **REG\_DWORD**, datos **0x00000003**):
  
**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\SecurityProviders**  
**\\SCHANNEL\\EventLogging**
  
**Advertencia:** la edición incorrecta del Registro puede dañar el sistema gravemente. Antes de hacer cambios en el Registro, debe hacer copias de seguridad de todos los datos del equipo.
  
Asegúrese de deshabilitar el registro de SChannel cuando esté solucionando problemas ya que consume recursos del sistema y puede inundar el registro de sucesos con entradas no deseadas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas del cuadrante de optimización
  
El cuadrante de optimización incluye las SMF necesarias para administrar costos y mantener o mejorar los niveles de servicio. Este cuadrante comprende la revisión de incidentes e interrupciones de actividad, examen de las estructuras de costos, evaluación del personal, disponibilidad, análisis de rendimiento y previsiones de capacidad.
  
Esta sección contiene información relevante para las SMF siguientes:
  
-   Administración de capacidad
  
No hay tareas que correspondan al resto de las SMF:
  
-   Administración del nivel de servicio
  
-   Administración financiera
  
-   Administración de la disponibilidad
  
-   Administración de la continuidad del servicio de TI
  
-   Administración de la fuerza de trabajo
  
    **Nota:** cada descripción de tarea incluye la siguiente información de resumen: requisitos de seguridad, frecuencia y requisitos de tecnología.
  
#### Administración de capacidad
  
La administración de capacidad es el proceso de planear, ajustar el tamaño y controlar la capacidad de la solución del servicio para satisfacer la demanda del usuario dentro de los niveles de rendimiento establecidos en el SLA. Este proceso requiere información acerca de las situaciones de uso, patrones y características de carga máxima de la solución del servicio, así como los requisitos de rendimiento establecidos.
  
##### Determinación de la carga máxima del servidor IAS
  
En esta sección se ofrece información sobre la carga máxima probable del servidor IAS.
  
Los problemas de rendimiento en servidores RADIUS IAS con la configuración y el tamaño correctos son muy poco habituales. Los servidores RADIUS de IAS admiten una mayor carga en los momentos de picos de carga, por ejemplo las mañanas, cuando muchos usuarios inician la sesión a la vez, poco después de una interrupción de la actividad de la red o si se produce un error del servidor RADIUS cuando los puntos de acceso inalámbricos conmutan por error a un servidor de copia de seguridad.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: ninguno
  
-   **Frecuencia**: tarea de configuración
  
-   **Requisitos de tecnología**: ninguno
  
###### Detalles de la tarea
  
Las pruebas internas de Microsoft han demostrado que IAS puede alcanzar picos de carga en hardware modesto, que dará servicio a las necesidades de la mayor parte de los clientes. La mejor forma de estimar el número de autenticaciones que IAS puede ofrecer se representa mediante autenticaciones por segundo. IAS ha alcanzado las siguientes cifras de rendimiento en un servidor Intel Pentium 4 a 2 GHz con Windows Server 2003 y Active Directory en otro servidor Intel Pentium 4 a 2 GHz.
  
**Tabla 12.10: Determinación de la carga en el servidor IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de autenticación</th>
<th style="border:1px solid black;" >Autenticaciones por segundo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nuevas autenticaciones de EAP-TLS</td>
<td style="border:1px solid black;">36</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nuevas autenticaciones de EAP-TLS con compatibilidad para tarjetas de descarga</td>
<td style="border:1px solid black;">50</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Autenticaciones con reconexión rápida</td>
<td style="border:1px solid black;">166</td>
</tr>
</tbody>
</table>
  
**Nota:** esta información se ofrece sin garantía alguna de exactitud y sólo se debe utilizar como orientación con objeto de planear la capacidad y no para realizar comparaciones de rendimiento.
  
IAS puede configurarse para generar registros de texto basados en disco que contengan diversos volúmenes de información de solicitudes de RADIUS. Debe planear un disco de alto rendimiento para almacenar los registros de RADIUS debido a la carga que suponen para los servidores RADIUS. Los subsistemas de disco lentos pueden retrasar las respuestas de RADIUS de IAS a los puntos de acceso inalámbricos, provocando tiempos de espera de protocolo y errores innecesarios de los puntos de acceso inalámbricos de servidores RADIUS secundarios. Para obtener más información acerca de las opciones de registro de RADIUS, consulte el capítulo 5, "Diseño de una infraestructura de RADIUS para la seguridad de LAN inalámbricas".
  
Además, la habilitación de las características de seguimiento del software de Windows Server 2003 (tal como se describe en la sección "Activación y desactivación del seguimiento en el servidor IAS" anterior) impondrá una carga adicional en los servidores IAS. No obstante, puede ser necesario de forma ocasional para solucionar problemas de acceso a la red. Los servidores IAS deben disponer de la capacidad de ejecutarse con el seguimiento habilitado durante períodos de tiempo limitados a la vez que atienden la carga de producción.
  
##### Determinación de los requisitos de almacenamiento y copia de seguridad para un servidor IAS
  
En esta sección se ofrece información de capacidad para los parámetros de almacenamiento de IAS. Esta información ayudará a los planeadores de capacidad a calcular los requisitos futuros de almacenamiento para el disco en línea y los medios de almacenamiento de copia de seguridad sin conexión.
  
###### Información de resumen
  
-   **Requisitos de seguridad**: ninguno
  
-   **Frecuencia**: según sea necesario
  
-   **Requisitos de tecnología**: ninguno
  
###### Detalles de la tarea
  
Los archivos de registro de RADIUS de IAS son el único componente de los servidores IAS que requiere planear el almacenamiento. Los registros de solicitudes de RADIUS para esta solución están configurados para crear un nuevo registro cada mes; el hardware probado al desarrollar esta solución contenía un volumen de disco de 18 GB dedicado a los archivos de registro.
  
Debe estimar la carga en los servidores IAS del entorno y, a continuación, seleccionar opciones de registro y llevar a cabo pruebas en un entorno de laboratorio para simular clientes de producción inalámbricos que autentican en IAS y, por lo tanto, generan datos de registro. En las estimaciones se puede utilizar una lógica como la siguiente:
  
La cantidad media de usuarios por punto de acceso inalámbrico es de 25 (usuarios o equipos). Cada usuario o equipo realiza una autenticación inicial y se vuelve a autenticar cada 10-60 minutos (según los requisitos de seguridad). Cada autenticación genera un kilobyte (KB) de información de registro en el disco, con el registro de las solicitudes de autenticación y las solicitudes de auditoría y sin registrar las solicitudes provisionales (el tamaño de archivo varía según las opciones de registro). Debe calcular la cantidad de espacio de registro en disco que genera cada punto de acceso inalámbrico por hora al dar soporte a 25 clientes. Después, calcule el número máximo de AP inalámbricos al que el servidor IAS dará servicio en los momentos de mayor carga de servidor o de conmutación por error del servidor.
  
Los registros de solicitudes de RADIUS IAS son datos que se pueden comprimir mucho. Si bien no se recomienda su uso frecuente, la compresión se puede activar en la carpeta de archivos de registro de solicitudes de RADIUS si es necesario. Debe estar preparado para admitir carga adicional en un servidor IAS que tenga que comprimir datos.
  
###### Ventana de copia de seguridad de los archivos de registro de RADIUS IAS
  
Si se supone que se realizó una copia de seguridad de red con un funcionamiento ideal en un conmutador dedicado de 100 Mbps (megabits por segundo) en el servidor de copias de seguridad, puede realizarse una copia de seguridad de una base de datos de 3 gigabytes (GB) más 500 MB del estado del sistema en 15-20 minutos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas del cuadrante de cambio
  
El cuadrante de cambio incluye los procesos y procedimientos requeridos para identificar, revisar, aprobar e incorporar cambios en un entorno administrado de TI. Los cambios incluyen activos de hardware y software, así como cambios específicos en procesos y procedimientos.
  
El objetivo del proceso de cambios es introducir en el entorno de TI nuevas tecnologías, sistemas, aplicaciones, hardware, herramientas y procesos, además de cambios en las funciones y responsabilidades, y hacerlo con rapidez y la mínima interrupción del servicio posible.
  
#### Administración de cambios
  
La SMF de administración de cambios es la responsable de administrar los cambios en un entorno de TI. Un objetivo clave del proceso de administración de cambios consiste en asegurar que todas las partes afectadas por el cambio conocen y entienden el impacto del cambio. Debido a que la mayor parte de sistemas están estrechamente interrelacionados, cualquier cambio que se realice en una parte del sistema podría tener un profundo impacto en otra. La administración de cambios trata de identificar todos los sistemas y procesos afectados antes de implementar el cambio, para reducir o eliminar los efectos negativos. Normalmente, el “objetivo” o entorno administrado es el entorno de producción, pero también debe incluir los entornos clave de integración, pruebas y almacenamiento temporal.
  
Todos los cambios realizados en la infraestructura de RADIUS y la seguridad de WLAN deben utilizar el siguiente proceso de administración de cambios de MOF estándar:
  
1.  **Solicitud de cambio**. La iniciación formal de un cambio a través del envío de una solicitud de cambio (RFC).
  
2.  **Clasificación de cambio**. La asignación de una prioridad y una categoría al cambio, utilizando como criterios su urgencia e impacto sobre la infraestructura o los usuarios. Esta asignación afecta a la ruta y la velocidad de implementación.
  
3.  **Autorización de cambio**. La consideración, la aprobación y la desaprobación del cambio por parte del administrador de cambios y la junta consultiva de cambios (CAB), una junta que incluye a los representantes empresariales y de TI.
  
4.  **Desarrollo de cambio**. El planeamiento y el desarrollo del cambio, un proceso que puede variar inmensamente de ámbito e incluye revisiones en etapas interinas importantes.
  
5.  **Lanzamiento de cambio**. El lanzamiento y la implementación del cambio en el entorno de producción.
  
6.  **Revisión de cambio**. Proceso posterior a la implementación que revisa si el cambio ha logrado los objetivos establecidos para el mismo y determina si debe mantenerse en vigencia o eliminarse.
  
Los procedimientos de esta sección describen los procedimientos de desarrollo de cambios para algunos de los cambios clave que podrían requerirse normalmente en el entorno. Cada procedimiento de desarrollo de cambio vendrá acompañado de un procedimiento de lanzamiento del cambio que describe cómo se debe implementar el cambio en la producción.
  
##### Administración de actualizaciones del sistema operativo
  
La administración de actualizaciones de seguridad de los componentes de software de RADIUS y WLAN forma parte de la administración de revisiones de Windows general. Este tema se trata en las dos guías de solución de Microsoft que describen las actualizaciones de sistemas operativos Windows mediante Microsoft Systems Management Server (SMS) o Servicios de actualización de software de Microsoft (SUS). Consulte la sección "Información adicional" que aparece al final de este capítulo para obtener información acerca de cómo obtenerlas.
  
La administración de revisiones incluye componentes de administración de lanzamiento y configuración, así como un componente de administración de cambios. Sin embargo, las tres SMF se tratan en los documentos a los que se hace referencia en los párrafos anteriores.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tablas de configuración
  
En las tablas siguientes encontrará los valores de información de configuración específicos del sitio y de la solución que se utilizan en los procedimientos descritos en este capítulo. Estas tablas constituyen un subconjunto de las tablas de configuración de planeamiento del capítulo 8, "Implementación de la infraestructura de RADIUS" y del capítulo 9, "Implementación de la infraestructura de seguridad para LAN inalámbricas" y sólo se muestran como referencia.
  
#### Parámetros de la configuración por sitio
  
**Tabla 12.11: Elementos de configuración definidos por el usuario**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nombre DNS del dominio raíz del bosque de Active Directory de Microsoft</td>
<td style="border:1px solid black;">woodgrovebank.com</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de dominio NetBIOS (servicio básico de entrada y salida de red)</td>
<td style="border:1px solid black;">WOODGROVEBANK</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre del servidor IAS principal</td>
<td style="border:1px solid black;">HQ-IAS-01</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre del servidor IAS secundario</td>
<td style="border:1px solid black;">HQ-IAS-02</td>
</tr>
</tbody>
</table>
  
#### Parámetros de la configuración de la solución
  
**Tabla 12.12: Elementos de la configuración que recomienda la solución**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Nombre completo del grupo administrativo que controla la configuración de IAS</td>
<td style="border:1px solid black;">Administradores IAS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Nombre del grupo administrativo que controla la configuración de IAS en versiones anteriores a Windows 2000</td>
<td style="border:1px solid black;">Administradores IAS</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Nombre completo del grupo que revisa los registros de solicitudes de autenticación y de cuentas de IAS con fines de seguridad</td>
<td style="border:1px solid black;">Auditores de seguridad IAS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Nombre del grupo que revisa los registros de peticiones contables y las autenticaciones de IAS con fines de seguridad en versiones anteriores a Windows 2000</td>
<td style="border:1px solid black;">Auditores de seguridad IAS</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory con los usuarios que requieren certificados de autenticación de 802.1X</td>
<td style="border:1px solid black;">Inscribir automáticamente la autenticación del cliente: certificado de usuario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory con los equipos que requieren certificados de autenticación de 802.1X</td>
<td style="border:1px solid black;">Inscribir automáticamente la autenticación del cliente: certificado del equipo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory de Microsoft con los servidores IAS que requieren certificados de autenticación de 802.1X</td>
<td style="border:1px solid black;">Inscribir automáticamente el certificado de autenticación de servidor IAS y RAS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Nombre anterior a Windows 2000 del grupo global de Active Directory de Microsoft con los servidores IAS que requieren certificados de autenticación de 802.1X</td>
<td style="border:1px solid black;">Inscribir automáticamente el certificado de autenticación de servidor IAS y RAS</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory que contiene los usuarios que pueden obtener acceso a la red inalámbrica</td>
<td style="border:1px solid black;">Directiva de acceso remoto: usuarios inalámbricos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory que contiene los equipos que pueden obtener acceso a la red inalámbrica</td>
<td style="border:1px solid black;">Directiva de acceso remoto: equipos inalámbricos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Cuentas] Grupo universal de Active Directory que contiene el grupo de usuarios inalámbricos y el grupo de equipos inalámbricos</td>
<td style="border:1px solid black;">Directiva de acceso remoto - Acceso inalámbrico</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Cuentas] Grupo global de Active Directory con los equipos que requieren la configuración de propiedades de redes inalámbricas a través de la Directiva de grupo de Active Directory</td>
<td style="border:1px solid black;">Directiva de red inalámbrica - Equipos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Certificados] Plantilla de certificado utilizada para generar certificados para la autenticación del cliente usuario</td>
<td style="border:1px solid black;">Autenticación de cliente: usuario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Certificados] Plantilla de certificado utilizada para generar certificados para la autenticación del equipo cliente</td>
<td style="border:1px solid black;">Autenticación de cliente: equipo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Certificados] Plantilla de certificado utilizada para generar certificados de autenticación de servidor para que IAS los utilice</td>
<td style="border:1px solid black;">Autenticación de servidor IAS y RAS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Secuencias de comandos] Ruta para las secuencias de comandos de instalación</td>
<td style="border:1px solid black;">C:\MSSScripts</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Secuencias de comandos] Archivo por lotes de exportación de configuración de IAS</td>
<td style="border:1px solid black;">IASExport.bat</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Secuencias de comandos] Archivo por lotes de importación de configuración de IAS</td>
<td style="border:1px solid black;">IASImport.bat</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Secuencias de comandos] Archivo por lotes de exportación de configuración de cliente RADIUS de IAS</td>
<td style="border:1px solid black;">IASClientExport.bat</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Secuencias de comandos] Archivo por lotes de importación de configuración de cliente RADIUS de IAS</td>
<td style="border:1px solid black;">IASClientImport.bat</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Config] Ruta para archivos de copia de seguridad de la configuración</td>
<td style="border:1px solid black;">D:\IASConfig</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Registros de solicitudes] Ubicación de los registros de solicitudes de autenticación y auditoría IAS</td>
<td style="border:1px solid black;">D:\IASLogs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Registros de solicitudes] Nombre compartido de los registros de solicitudes RADIUS</td>
<td style="border:1px solid black;">IASLogs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Directiva de acceso remoto] Nombre de directiva</td>
<td style="border:1px solid black;">Permitir acceso inalámbrico</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">[Directiva de grupo] Nombre del objeto Directiva de grupo de Microsoft Active Directory</td>
<td style="border:1px solid black;">Directiva de red inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">[Directiva de grupo] Directiva de redes inalámbricas dentro del objeto directiva de grupo</td>
<td style="border:1px solid black;">Configuración inalámbrica de equipo cliente</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
-   Para obtener más información acerca del modelo de proceso y el modelo de equipo de MOF, consulte la [página de Microsoft Operations Framework](http://technet.microsoft.com/es-es/library/bb232042.aspx) en www.microsoft.com/technet/itsolutions/techguide/mof/default.mspx.
  
-   Para obtener más información acerca de las restricciones de capacidad y los contadores de rendimiento relacionados, consulte el artículo Q146005 de Microsoft Knowledge Base, "[Optimizing Windows NT for Performance](http://support.microsoft.com/default.aspx?kbid=146005)", en http://support.microsoft.com/default.aspx?kbid=146005.
  
-   Para obtener más información acerca de la solución de problemas de redes inalámbricas, consulte lo siguiente:
  
    -   El artículo Q313242 de Microsoft Knowledge Base, "[How to troubleshoot wireless network connections in Windows XP](http://support.microsoft.com/?kbid=313242)", en http://support.microsoft.com/?scid=313242.
  
    -   Las notas del producto ["Troubleshooting Windows XP IEEE 802.11 Wireless Access](http://www.microsoft.com/windowsxp/pro/techinfo/administration/networking/troubleshooting.asp)" en www.microsoft.com/windowsxp/pro/techinfo/administration/  
        networking/troubleshooting.asp.
  
-   Para obtener información acerca de la implementación de MOM, consulte la guía [*MOM 2000 SP1 Operations Guide*](http://www.microsoft.com/resources/documentation/mom/2000sp1/all/opsguide/en-us/1_in781g.mspx) en www.microsoft.com/resources/documentation/mom/2000sp1/all/opsguide/en-us/1\_in781g.mspx.
  
-   Para obtener información acerca de la administración de revisiones con Microsoft SMS 2003, consulte "[Patch Management Using Microsoft Systems Management Server 2003](http://www.microsoft.com/downloads/details.aspx?familyid=959ee7d6-7ddf-409a-9522-7d270bdcf12a&displaylang=en)" en www.microsoft.com/technet/itsolutions/techguide/msm/swdist/pmsms/2003/pmsms031.mspx.
  
-   Para obtener información acerca de la administración de revisiones con Microsoft SMS 2.0, consulte "[Patch Management Using Microsoft Systems Management Server 2.0](http://technet.microsoft.com/es-es/solutionaccelerators/default(en-us).aspx)" en www.microsoft.com/technet/itsolutions/techguide/msm/swdist/pmsms/20/pmsmsin.mspx.
  
-   En "[Plataformas más fáciles de administrar](http://go.microsoft.com/fwlink/?linkid=16284)", en http://go.microsoft.com/fwlink/?LinkId=16284, se puede encontrar más información acerca de la administración de revisiones en la plataforma de Microsoft.
  
-   Para obtener más información acerca de cómo obtener y utilizar la Consola de administración de directivas de grupo (GPMC), consulte "[Enterprise Management with the Group Policy Management Console](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx)" en www.microsoft.com/windowsserver2003/gpmc/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
