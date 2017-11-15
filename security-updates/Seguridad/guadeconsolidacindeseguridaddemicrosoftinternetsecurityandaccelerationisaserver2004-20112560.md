---
TOCTitle: 'Guía de consolidación de seguridad de Microsoft Internet Security and Acceleration (ISA) Server 2004'
Title: 'Guía de consolidación de seguridad de Microsoft Internet Security and Acceleration (ISA) Server 2004'
ms:assetid: '6a9c3909-0060-4566-97d8-1d29c0c19e4c'
ms:contentKeyID: 20112560
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458738(v=TechNet.10)'
---

Guía de consolidación de la seguridad de ISA Server 2004
========================================================

Publicado: marzo 12, 2004

##### En esta página

[](#eeaa)[Introducción](#eeaa)
[](#edaa)[Protección del equipo servidor ISA](#edaa)
[](#ecaa)[Protección de la configuración](#ecaa)
[](#ebaa)[Protección de la implementación](#ebaa)
[](#eaaa)[Recursos adicionales](#eaaa)

### Introducción

Esta guía está diseñada para proporcionar información esencial acerca de cómo proteger los equipos con Microsoft Internet Security and Acceleration (ISA) Server 2004 Standard Edition. Además de recomendaciones de configuración prácticas y específicas, en esta guía se incluyen estrategias de implementación del servidor ISA.

Para equipos con Microsoft Windows Server 2003, esta guía complementa la [Guía de seguridad de Windows Server 2003](http://www.microsoft.com/spain/technet/security/prodtech/windowsserver2003/w2003hg/sgch00.mspx) (http://go.microsoft.com/fwlink/?LinkId=31584). En concreto, numerosos procedimientos de esta guía están relacionados directamente con las recomendaciones de seguridad presentadas en la *Guía de seguridad de Windows Server 2003*. Por lo tanto, antes de llevar a cabo los procedimientos presentados en esta guía, se recomienda leer primero la *Guía de seguridad de Windows Server 2003*.

Si el servidor ISA está instalado en un equipo cono Windows® 2000 Server, consulte la guía [Definición del panorama de seguridad de Windows 2000](http://www.microsoft.com/spain/technet/recursos/articulos/secmod133.mspx), o la guía [Configuraciones de seguridad de Windows 2000](http://www.microsoft.com/spain/technet/recursos/articulos/secmod220.mspx).

#### Ámbito de esta guía

Esta guía se centra expresamente en las operaciones necesarias para crear y mantener un entorno ISA Server 2004 seguro. Debe utilizar esta guía como parte de su estrategia global de seguridad para ISA Server 2004 y no como una referencia completa para crear y realizar el mantenimiento de un entorno seguro.

En concreto, en esta guía se proporcionan respuestas detalladas a las siguientes preguntas:

-   ¿Cuáles son los pasos recomendados para proteger el equipo servidor ISA?

-   ¿Qué consideraciones de seguridad se deben aplicar a la configuración del servidor ISA?

-   ¿Qué orientaciones hay disponibles para preparar una implementación de ISA Server 2004 segura?

[](#mainsection)[Principio de la página](#mainsection)

### Protección del equipo servidor ISA

Un paso importante en la protección de servidor ISA consiste en comprobar que el equipo servidor ISA está seguro físicamente y que ha aplicado las recomendaciones de configuración de seguridad básicas, entre las que se incluyen:

-   Administración de actualizaciones

-   Protección física del equipo

-   Determinación de la pertenencia a dominios

-   Consolidación de la seguridad de la infraestructura de Windows

-   Administración de funciones y permisos

-   Reducción de la superficie de ataque posible

En las siguientes secciones se describe cómo implementar estas recomendaciones. En esta sección también se describe cómo se cierra el servidor ISA cuando se identifica una amenaza de seguridad.

#### Administración de actualizaciones

Como práctica recomendada de seguridad, se recomienda instalar siempre las actualizaciones más recientes del sistema operativo, el servidor ISA y otros componentes que instala el servidor ISA: Microsoft SQL Server™ 2000 Desktop Engine (MSDE) y Office Web Components 2002 (OWC). Realice las siguientes acciones:

-   Obtenga las actualizaciones del sistema operativo. Busque actualizaciones en el [sitio de Windows Update](http://go.microsoft.com/fwlink/?linkid=28855).

-   Obtenga las actualizaciones del servidor ISA. Consulte el [Centro de descarga de ISA Server 2004](http://www.microsoft.com/spain/isaserver/downloads/default.mspx) (http://go.microsoft.com/fwlink/?LinkId=28791) para obtener la información de actualización más reciente.

-   Busque las actualizaciones más recientes de Microsoft SQL Server 2000 Desktop Engine (MSDE) y Office Web Components 2002 (OWC), en los [Boletines de seguridad de Microsoft](http://www.microsoft.com/spain/technet/security/bulletin/summary.mspx).

También se recomienda analizar la seguridad del sistema periódicamente mediante Microsoft Baseline Security Analyzer (MBSA). Puede descargar MBSA del [sitio Web de MBSA](http://technet.microsoft.com/es-es/security/cc184924.aspx).

#### Acceso físico

Asegúrese de que el equipo servidor ISA se encuentra en una ubicación físicamente segura. El acceso físico a un servidor supone un riesgo de seguridad alto. El acceso físico a un servidor por parte de un intruso puede tener como consecuencia un acceso o modificación no autorizados, así como la instalación de hardware o software diseñado para eludir la seguridad. Para mantener un entorno seguro, debe restringir el acceso físico al equipo servidor ISA.  

#### Determinación de la pertenencia a dominios

En muchos casos, puede configurar el equipo servidor ISA como miembro de un dominio. Por ejemplo, si crea una directiva que se base en la autenticación de usuarios de dominio, el servidor ISA debe pertenecer a un dominio.

Si el equipo servidor ISA protege el extremo de la red, se recomienda instalarlo en un bosque independiente (en vez de hacerlo en el bosque de la red corporativa). De esta forma, se contribuye a proteger el bosque interno, aunque se organice un ataque en el bosque del equipo servidor ISA. Para apreciar las ventajas administrativas y de seguridad del servidor ISA como miembro de dominio, se recomienda implementar el equipo servidor ISA en un bosque independiente con una confianza de una sola dirección al bosque corporativo. (La confianza de una sola dirección sólo se admite en dominios de Windows Server 2003.)

Tenga en cuenta que al instalar el servidor ISA como un miembro de dominio, puede cerrar el equipo servidor ISA mediante una directiva de grupo en vez de configurar únicamente una directiva local.

Por motivos de seguridad, si no precisa funcionalidad de dominio o de servicio de directorio de Active Directory® para el equipo servidor ISA, considere la posibilidad de instalarlo en un grupo de trabajo. Por ejemplo, si el servidor ISA va a proteger el extremo de la red, considere la posibilidad de instalar el equipo en un grupo de trabajo.

#### Consolidación de la seguridad de la infraestructura de Windows

Tal como se ha mencionado anteriormente, en esta guía se supone que ha aplicado las configuraciones recomendadas en la *Guía de seguridad de Windows Server 2003*. En concreto, debe aplicar la plantilla de seguridad de directiva de seguridad de línea de base de Microsoft. Sin embargo, no implemente los filtros de seguridad del protocolo Internet (IPSec) ni ninguna de las directivas de función de servidor.

Asimismo, debe tener en cuenta la funcionalidad del servidor ISA y proteger el sistema operativo en consecuencia.

En la siguiente tabla se enumeran los servicios principales que se deben habilitar para que el servidor ISA y el equipo servidor ISA funcionen correctamente.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del servicio</th>
<th style="border:1px solid black;" >Razón principal</th>
<th style="border:1px solid black;" >Modo de inicio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sistema de sucesos COM+</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicios de cifrado</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registro de sucesos</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicios IPSec</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de discos lógicos  </td>
<td style="border:1px solid black;">Sistema operativo principal (administración de discos)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio del administrador de discos lógicos</td>
<td style="border:1px solid black;">Sistema operativo principal (administración de discos)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Microsoft</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Control de Microsoft ISA Server</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Programador de trabajos de Microsoft ISA Server</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento de Microsoft ISA Server</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSSQL$MSFW</td>
<td style="border:1px solid black;">Requerido cuando se utiliza el registro MSDE para el servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conexiones de red</td>
<td style="border:1px solid black;">Sistema operativo principal (infraestructura de red)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Proveedor de compatibilidad con seguridad LM de Windows NT</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Plug and Play</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Almacenamiento protegido</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administrador de conexión de acceso remoto</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Llamada a procedimiento remoto (RPC)</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión secundario</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador de cuentas de seguridad</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Requerido para el recurso compartido de cliente firewall del servidor ISA</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tarjeta inteligente</td>
<td style="border:1px solid black;">Sistema operativo principal (seguridad)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQLAgent$MSFW</td>
<td style="border:1px solid black;">Requerido cuando se utiliza el registro MSDE para el servidor ISA</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Notificación de sucesos del sistema</td>
<td style="border:1px solid black;">Sistema operativo principal</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Telefonía</td>
<td style="border:1px solid black;">Requerido para el funcionamiento normal del servidor ISA</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio de disco virtual (VDS)</td>
<td style="border:1px solid black;">Sistema operativo principal (administración de discos)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Instrumental de administración de Windows (WMI)  </td>
<td style="border:1px solid black;">Sistema operativo principal (WMI)</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Adaptador de rendimiento de WMI  </td>
<td style="border:1px solid black;">Sistema operativo principal (WMI)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
</tbody>
</table>
  
##### Funciones de servidor del servidor ISA
  
El equipo servidor ISA puede funcionar en capacidades, o funciones, adicionales según el modo en que lo utilice. En la tabla siguiente se enumeran las funciones de servidor posibles, se describe cuándo se pueden necesitar y se enumeran los servicios que se deben activar cuando se habilita la función.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función de servidor</th>
<th style="border:1px solid black;" >Escenario de uso</th>
<th style="border:1px solid black;" >Servicios necesarios</th>
<th style="border:1px solid black;" >Modo de inicio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servidor de enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
<td style="border:1px solid black;">Enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
<td style="border:1px solid black;">Administrador de conexión de acceso remoto</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
<td style="border:1px solid black;">Telefonía</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
<td style="border:1px solid black;">Estación de trabajo</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de enrutamiento y acceso remoto</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
<td style="border:1px solid black;">Servidor  </td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Terminal Server para administración de escritorios remotos</td>
<td style="border:1px solid black;">Seleccione esta función para habilitar la administración remota del equipo servidor ISA.</td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Terminal Server para administración de escritorios remotos</td>
<td style="border:1px solid black;">Seleccione esta función para habilitar la administración remota del equipo servidor ISA.</td>
<td style="border:1px solid black;">Servicios de Terminal Server</td>
<td style="border:1px solid black;">Manual</td>
</tr>
</tbody>
</table>
  
![](images/Dd458738.note(es-es,TechNet.10).gif)  Nota  
El modo de inicio del servicio Servidor debe ser Automático en los siguientes casos:
  
-   Si instala ISA Server 2004: recurso compartido de instalación de cliente.
  
-   Si utiliza Administración de enrutamiento y acceso remoto en vez de Administración del servidor ISA para configurar una red privada virtual (VPN).
  
-   Otras tareas o funciones, tal como se ha descrito en la tabla anterior, requieren el servicio.
  
    El modo de inicio del servicio Enrutamiento y acceso remoto es Manual. El servidor ISA sólo inicia el servicio si hay habilitada una VPN.
  
Tenga en cuenta que el servicio Servidor sólo se necesita si utiliza Administración de enrutamiento y acceso remoto (en vez de Administración del servidor ISA) para configurar una VPN.
  
##### Tareas de servidor del servidor ISA
  
Las tareas de servidor son similares a las funciones de servidor y con frecuencia están relacionadas con dichas funciones, aunque no están incluidas en ellas. Para que un servidor realice las tareas necesarias, se deben habilitar servicios específicos, en función de las funciones que seleccione. Los servicios que no sean necesarios se deben deshabilitar. En la tabla siguiente se enumeran las tareas de servidor posibles para el servidor ISA, se describe cuándo se pueden necesitar y se enumeran los servicios que se deben activar cuando se habilita la función.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tarea de servidor</th>
<th style="border:1px solid black;" >Escenario de uso</th>
<th style="border:1px solid black;" >Servicios necesarios</th>
<th style="border:1px solid black;" >Modo de inicio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Instalación de aplicaciones localmente mediante Windows Installer</td>
<td style="border:1px solid black;">Se requiere para instalar, desinstalar o reparar aplicaciones mediante el servicio Microsoft Installer.</td>
<td style="border:1px solid black;">Windows Installer</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Copia de seguridad</td>
<td style="border:1px solid black;">Se requiere si se utiliza NTBackup u otro programa de copia de seguridad en el equipo servidor ISA.</td>
<td style="border:1px solid black;">Proveedor de instantáneas de software de Microsoft</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Copia de seguridad</td>
<td style="border:1px solid black;">Se requiere si se utiliza NTBackup u otro programa de copia de seguridad en el equipo servidor ISA.</td>
<td style="border:1px solid black;">Instantáneas de volumen</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Copia de seguridad</td>
<td style="border:1px solid black;">Se requiere si se utiliza NTBackup u otro programa de copia de seguridad en el equipo servidor ISA.</td>
<td style="border:1px solid black;">Servicio Almacenamiento de medios extraíbles</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Informe de errores</td>
<td style="border:1px solid black;">Se utiliza para habilitar el informe de errores, lo que contribuye a mejorar la confiabilidad de Windows gracias a la generación de informes de errores críticos para Microsoft con el fin de analizarlos.</td>
<td style="border:1px solid black;">Servicio de informe de errores</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ayuda y soporte técnico</td>
<td style="border:1px solid black;">Permite la recopilación de datos de equipo históricos para la transferencia de incidencias a los Servicios de soporte técnico de Microsoft.</td>
<td style="border:1px solid black;">Ayuda y soporte técnico</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ISA Server 2004: recurso compartido de instalación de cliente</td>
<td style="border:1px solid black;">Requerido para permitir que los equipos se conecten e instalen desde el recurso compartido de cliente firewall en el equipo servidor ISA.</td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ISA Server 2004: registro MSDE</td>
<td style="border:1px solid black;">Requerido para permitir el registro mediante bases de datos MSDE. Si no habilita el servicio correspondiente, puede efectuar el registro en bases de datos SQL o en archivos. No obstante, no podrá utilizar el visor de registro en modo sin conexión.</td>
<td style="border:1px solid black;">SQLAgent$MSFW</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ISA Server 2004: registro MSDE</td>
<td style="border:1px solid black;">Requerido para permitir el registro mediante bases de datos MSDE. Si no habilita el servicio correspondiente, puede efectuar el registro en bases de datos SQL o en archivos. No obstante, no podrá utilizar el visor de registro en modo sin conexión.</td>
<td style="border:1px solid black;">MSSQL$MSFW</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Monitor de sistema: recopilación en segundo plano</td>
<td style="border:1px solid black;">Permite la recopilación en segundo plano de datos de rendimiento acerca del equipo servidor ISA.</td>
<td style="border:1px solid black;">Registros y alertas de rendimiento</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Imprimir en un equipo remoto</td>
<td style="border:1px solid black;">Permite imprimir desde el equipo servidor ISA.</td>
<td style="border:1px solid black;">Administrador de colas de impresión</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Imprimir en un equipo remoto</td>
<td style="border:1px solid black;">Permite imprimir desde el equipo servidor ISA.</td>
<td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Imprimir en un equipo remoto</td>
<td style="border:1px solid black;">Permite imprimir desde el equipo servidor ISA.</td>
<td style="border:1px solid black;">Estación de trabajo</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administración remota de Windows</td>
<td style="border:1px solid black;">Permite la administración remota del servidor Windows (no se requiere para la administración remota del servidor ISA).</td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administración remota de Windows</td>
<td style="border:1px solid black;">Permite la administración remota del servidor Windows (no se requiere para la administración remota del servidor ISA).</td>
<td style="border:1px solid black;">Registro remoto</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Sincronización de la hora</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA se ponga en contacto con un servidor NTP para sincronizar el reloj. Desde un punto de vista de seguridad, un reloj preciso resulta importante para la auditoría de sucesos y otros protocolos de seguridad.</td>
<td style="border:1px solid black;">Horario de Windows</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Asistente remoto</td>
<td style="border:1px solid black;">Permite que la característica Asistencia remota se utilice en este equipo.</td>
<td style="border:1px solid black;">Ayuda y soporte técnico</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Asistente remoto</td>
<td style="border:1px solid black;">Permite que la característica Asistencia remota se utilice en este equipo.</td>
<td style="border:1px solid black;">Administrador de sesión de Ayuda de escritorio remoto</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Asistente remoto</td>
<td style="border:1px solid black;">Permite que la característica Asistencia remota se utilice en este equipo.</td>
<td style="border:1px solid black;">Servicios de Terminal Server</td>
<td style="border:1px solid black;">Manual</td>
</tr>
</tbody>
</table>
  
![](images/Dd458738.note(es-es,TechNet.10).gif)  Nota  
Las aplicaciones cliente de hora requieren que el servicio Inalámbrico o Servidor se ejecuten para funcionar correctamente.
  
##### Funciones de cliente del servidor ISA
  
Los servidores pueden ser clientes de otros servidores. Las funciones de cliente dependen de los servicios específicos de función que se hayan habilitado. En la tabla siguiente se enumeran las funciones de cliente posibles para el servidor ISA, se describe cuándo se pueden necesitar y se enumeran los servicios que se deben activar cuando se habilita la función.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función de cliente</th>
<th style="border:1px solid black;" >Escenario de uso</th>
<th style="border:1px solid black;" >Servicios necesarios</th>
<th style="border:1px solid black;" >Modo de inicio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Cliente de actualizaciones automáticas</td>
<td style="border:1px solid black;">Seleccione esta función para permitir la detección automática y la actualización desde Microsoft Windows Update.</td>
<td style="border:1px solid black;">Actualizaciones automáticas</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente de actualizaciones automáticas</td>
<td style="border:1px solid black;">Seleccione esta función para permitir la detección automática y la actualización desde Microsoft Windows Update.</td>
<td style="border:1px solid black;">Servicio de transferencia inteligente en segundo plano</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA recibe su dirección IP automáticamente desde un servidor DHCP.</td>
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente DNS</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA necesita recibir la información de resolución de nombres desde otros servidores.</td>
<td style="border:1px solid black;">Cliente DNS</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Miembro de dominio</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA pertenece a un dominio.</td>
<td style="border:1px solid black;">NLA (Network Location Awareness)</td>
<td style="border:1px solid black;">Manual</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Miembro de dominio</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA pertenece a un dominio.</td>
<td style="border:1px solid black;">Inicio de sesión de red</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Miembro de dominio</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA pertenece a un dominio.</td>
<td style="border:1px solid black;">Horario de Windows</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Registro de DNS automático</td>
<td style="border:1px solid black;">Seleccione esta función para permitir que el equipo servidor ISA registre automáticamente su nombre e información de dirección con un servidor DNS.</td>
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente de redes de Microsoft</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA tiene que conectarse a otros clientes Windows. Si no selecciona esta función, el equipo servidor ISA no podrá tener acceso a recursos compartidos en equipos remotos; por ejemplo, para publicar informes.</td>
<td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente de redes de Microsoft</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA tiene que conectarse a otros clientes Windows. Si no selecciona esta función, el equipo servidor ISA no podrá tener acceso a recursos compartidos en equipos remotos; por ejemplo, para publicar informes.</td>
<td style="border:1px solid black;">Estación de trabajo</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente WINS</td>
<td style="border:1px solid black;">Seleccione esta función si el equipo servidor ISA utiliza la resolución de nombres basada en WINS.</td>
<td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Automático</td>
</tr>
</tbody>
</table>
  
##### Creación de una plantilla de seguridad
  
Puede crear una plantilla mediante el complemento Plantillas de seguridad de Microsoft Management Console (MMC). La plantilla incluye información acerca de los servicios que se deben habilitar así como su modo de inicio. Con una plantilla de seguridad se puede configurar fácilmente una directiva de seguridad y, a continuación, aplicarla a cada equipo servidor ISA.
  
**Para crear una plantilla de seguridad, realice los siguientes pasos.**
  
1.  Para abrir Plantillas de seguridad, haga clic en **Inicio**, en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento** y, a continuación, haga clic en **Agregar**.
  
3.  Seleccione **Plantillas de seguridad**, haga clic en **Agregar**, en **Cerrar** y, a continuación, en **Aceptar**.
  
    ![](images/Dd458738.sechgd01(es-es,TechNet.10).gif)
  
4.  En el árbol de consola, haga clic en el nodo **Plantillas de seguridad**, haga clic con el botón secundario del ratón en la carpeta donde desee almacenar la nueva plantilla y haga clic en **Nueva plantilla**.
  
    ![](images/Dd458738.sechgd02(es-es,TechNet.10).gif)
  
5.  En **Nombre de plantilla**, escriba el nombre de la nueva plantilla de seguridad.
  
6.  En **Descripción**, escriba la descripción de la nueva plantilla de seguridad y, a continuación, haga clic en **Aceptar**.
  
7.  Expanda la nueva plantilla y, a continuación, haga clic en **Servicios del sistema**.
  
    [![](images/Dd458738.sechgd03(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd03_big(es-es,technet.10).gif)
  
8.  En el panel de detalles, haga clic con el botón secundario del ratón en **Sistema de sucesos COM+** y, a continuación, haga clic en **Propiedades**.
  
9.  Active **Definir esta configuración de directiva en la plantilla** y, a continuación, haga clic en el modo de inicio. (Para Sistema de sucesos COM+, el modo de inicio es **Automático**.)
  
    ![](images/Dd458738.sechgd04(es-es,TechNet.10).gif)
  
10. Repita los pasos 8 y 9 por cada uno de los servicios enumerados en la siguiente tabla.

 
    <p> </p>
<table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre del servicio</th>
    <th style="border:1px solid black;" >Nombre abreviado</th>
    <th style="border:1px solid black;" >Modo de inicio</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Actualizaciones automáticas</td>
    <td style="border:1px solid black;">wuauserv</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servicio de transferencia inteligente en segundo plano</td>
    <td style="border:1px solid black;">BITS</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Sistema de sucesos COM+</td>
    <td style="border:1px solid black;">EventSystem</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servicios de cifrado</td>
    <td style="border:1px solid black;">CryptSvc</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Cliente DHCP</td>
    <td style="border:1px solid black;">Dhcp</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Cliente DNS</td>
    <td style="border:1px solid black;">Dnscache</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Servicio de informe de errores</td>
    <td style="border:1px solid black;">ERSvc</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Registro de sucesos</td>
    <td style="border:1px solid black;">Eventlog</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Ayuda y soporte técnico</td>
    <td style="border:1px solid black;">Helpsvc</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servicios IPSec</td>
    <td style="border:1px solid black;">PolicyAgent</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Administrador de discos lógicos</td>
    <td style="border:1px solid black;">dmserver</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servicio del administrador de discos lógicos</td>
    <td style="border:1px solid black;">dmadmin</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Firewall de Microsoft</td>
    <td style="border:1px solid black;">Fwsrv</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Control de Microsoft ISA Server</td>
    <td style="border:1px solid black;">ISACtrl</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Programador de trabajos de Microsoft ISA Server</td>
    <td style="border:1px solid black;">ISASched</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Almacenamiento de Microsoft ISA Server</td>
    <td style="border:1px solid black;">ISASTG</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Proveedor de instantáneas de software de Microsoft</td>
    <td style="border:1px solid black;">SWPRV</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">MSSQL$MSFW</td>
    <td style="border:1px solid black;">MSSQL$MSFW</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Conexiones de red</td>
    <td style="border:1px solid black;">Netman</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">NLA (Network Location Awareness)</td>
    <td style="border:1px solid black;">NLA</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Proveedor de compatibilidad con seguridad LM de Windows NT</td>
    <td style="border:1px solid black;">NtLmSsp</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Registros y alertas de rendimiento</td>
    <td style="border:1px solid black;">SysmonLog</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Plug and Play</td>
    <td style="border:1px solid black;">PlugPlay</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Almacenamiento protegido</td>
    <td style="border:1px solid black;">ProtectedStorage</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Administrador de conexión de acceso remoto</td>
    <td style="border:1px solid black;">RasMan</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Administrador de sesión de Ayuda de escritorio remoto</td>
    <td style="border:1px solid black;">RDSessMgr</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Llamada a procedimiento remoto (RPC)</td>
    <td style="border:1px solid black;">RpcSs</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Almacenamiento de medios extraíbles</td>
    <td style="border:1px solid black;">NtmsSvc</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Enrutamiento y acceso remoto</td>
    <td style="border:1px solid black;">Ninguno</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Inicio de sesión secundario</td>
    <td style="border:1px solid black;">seclogon</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Administrador de cuentas de seguridad</td>
    <td style="border:1px solid black;">SamSs</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servidor</td>
    <td style="border:1px solid black;">lanmanserver</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Tarjeta inteligente</td>
    <td style="border:1px solid black;">SCardSvr</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Notificación de sucesos del sistema</td>
    <td style="border:1px solid black;">SENS</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
    <td style="border:1px solid black;">LmHosts</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Telefonía</td>
    <td style="border:1px solid black;">TapiSrv</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Servicios de Terminal Server</td>
    <td style="border:1px solid black;">TermService</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Servicio de disco virtual (VDS)</td>
    <td style="border:1px solid black;">VDS</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Instantáneas de volumen</td>
    <td style="border:1px solid black;">VSS</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Windows Installer</td>
    <td style="border:1px solid black;">MSIServer</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Instrumental de administración de Windows</td>
    <td style="border:1px solid black;">winmgmt</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Horario de Windows</td>
    <td style="border:1px solid black;">W32time</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Configuración inalámbrica</td>
    <td style="border:1px solid black;">WZCSVC</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Adaptador de rendimiento de WMI</td>
    <td style="border:1px solid black;">WmiApSrv</td>
    <td style="border:1px solid black;">Manual</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Estación de trabajo</td>
    <td style="border:1px solid black;">lanmanworkstation</td>
    <td style="border:1px solid black;">Automático</td>
    </tr>
    </tbody>
    </table>
  
![](images/Dd458738.note(es-es,TechNet.10).gif)  Nota  
El modo de inicio del servicio Servidor debe ser Automático en los siguientes casos:
  
-   Si instala ISA Server 2004: recurso compartido de instalación de cliente.
  
-   Si utiliza Administración de enrutamiento y acceso remoto en vez de Administración del servidor ISA para configurar una VPN.
  
-   Otras tareas o funciones, tal como se ha descrito en la tabla anterior, requieren el servicio.
  
    El modo de inicio del servicio Enrutamiento y acceso remoto es Manual. El servidor ISA sólo inicia el servicio si hay habilitada una VPN.  
    Las aplicaciones cliente de hora requieren que el servicio Inalámbrico o Servidor se ejecuten para funcionar correctamente.
  
**Para aplicar la nueva plantilla al equipo servidor ISA, realice los siguientes pasos.**
  
1.  Para abrir Plantillas de seguridad, haga clic en **Inicio**, en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento** y, a continuación, haga clic en **Agregar**.
  
3.  Seleccione **Configuración y análisis de seguridad**, haga clic en **Agregar**, en **Cerrar** y, a continuación, en **Aceptar**.
  
    ![](images/Dd458738.sechgd05(es-es,TechNet.10).gif)
  
4.  En el árbol de consola haga clic en **Configuración y análisis de seguridad**.
  
5.  Haga clic con el botón secundario del ratón en **Configuración y análisis de seguridad** y, a continuación, haga clic en **Abrir base de datos**.
  
6.  Escriba un nuevo nombre de base de datos y, a continuación, haga clic en **Abrir**.
  
7.  Seleccione la nueva plantilla de seguridad que desea importar y, a continuación, haga clic en **Abrir**. Seleccione la plantilla de seguridad que ha creado anteriormente.
  
    ![](images/Dd458738.sechgd06(es-es,TechNet.10).gif)
  
8.  Haga clic con el botón secundario del ratón en **Configuración y análisis de seguridad** y, a continuación, haga clic en **Configurar el equipo ahora**.
  
#### Administración de permisos y funciones
  
Debido a que el servidor ISA controla el acceso a la red, debe tener mucho cuidado al asignar permisos al equipo servidor ISA y los componentes relacionados. Determine cuidadosamente los usuarios que deben tener permiso para iniciar sesión en el equipo servidor ISA. A continuación, configure los derechos de inicio de sesión en consecuencia.
  
El servidor ISA permite aplicar funciones administrativas a usuarios y grupos. Después de determinar los grupos que tienen permiso para configurar o ver la directiva del servidor ISA y la información de supervisión, puede asignar funciones de forma apropiada.
  
En las siguientes secciones se detallan las cuestiones que se deben tener en cuenta al asignar permisos y funciones administrativas.
  
##### Funciones administrativas
  
Al igual que con cualquier aplicación de su entorno, cuando defina los permisos para el servidor ISA debe tener en cuenta las funciones de los administradores del servidor ISA y asignarles únicamente los permisos necesarios. Para simplificar el proceso, el servidor ISA utiliza funciones administrativas. Puede utilizar la administración basada en funciones para organizar a los administradores del servidor ISA en funciones independientes y predefinidas, cada una con su propio conjunto de tareas. Al asignar una función a un usuario, fundamentalmente se concede permisos a dicho usuario para que realice tareas específicas. Un usuario que tenga una función, como Administrador total del servidor ISA, puede realizar tareas del servidor ISA específicas que un usuario con otra función, como Supervisión básica del servidor ISA, no puede realizar. La administración basada en funciones implica a usuarios y grupos de Windows. Estos permisos de seguridad, pertenencia a grupos y derechos de usuario se utilizan para diferenciar a los usuarios que tienen funciones. En la siguiente tabla se describen las funciones del servidor ISA.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Supervisión básica del servidor ISA</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden supervisar el equipo servidor ISA y la actividad de red, pero no pueden configurar la funcionalidad de supervisión específica.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Supervisión extendida del servidor ISA</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden realizar todas las tareas de supervisión, incluida la configuración de registro, la configuración de definición de alertas y todas las funciones de supervisión disponibles para la función Supervisión básica del servidor ISA.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administrador total del servidor ISA</td>
<td style="border:1px solid black;">Los usuarios y grupos asignados a esta función pueden realizar cualquier tarea del servidor ISA, incluida la configuración de funciones, la aplicación de plantillas de red y la supervisión.</td>
</tr>
</tbody>
</table>
  
Los miembros de estos grupos administrativos del servidor ISA pueden ser cualquier usuario de Windows. No se precisan privilegios o permisos de Windows especiales. Con la única excepción de que para ver los contadores de rendimiento del servidor ISA, mediante perfmon o el escritorio digital del servidor ISA, el usuario debe ser miembro del grupo de usuarios Usuarios del monitor de sistema de Windows Server 2003.
  
Tenga en cuenta que los administradores con permisos de Supervisión extendida del servidor ISA pueden exportar e importar toda la información de configuración, incluida la información de configuración secreta. Esto significa que pueden descifrar la información secreta.
  
**Para asignar funciones administrativas, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004** y, a continuación, en el *nombre\_de\_servidor*.
  
3.  En la ficha **Tareas**, haga clic en **Definir funciones administrativas**.
  
    [![](images/Dd458738.sechgd07(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd07_big(es-es,technet.10).gif)
  
4.  En la página de **bienvenida** del Asistente para la delegación de administración del servidor ISA, haga clic en **Siguiente**.
  
5.  Haga clic en **Agregar**.
  
6.  En **Grupo (recomendado) o usuario**, escriba el nombre del grupo o usuario al que se asignarán los permisos administrativos específicos.
  
7.  En **Función**, seleccione la función administrativa aplicable.
  
###### Funciones y actividades
  
Cada función del servidor ISA tiene asociada una lista específica de tareas del servidor ISA. En la siguiente lista se enumeran algunas tareas de administración del servidor ISA junto con las funciones en que se realizan.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Actividad</th>
<th style="border:1px solid black;" >Permisos de Supervisión básica</th>
<th style="border:1px solid black;" >Permisos de Supervisión ampliada</th>
<th style="border:1px solid black;" >Permisos de Administrador total</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Ver escritorio digital, alertas, conectividad, sesiones, servicios</td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Confirmar alertas</td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ver información de registro</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Crear definiciones de alerta</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Crear informes</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Detener e iniciar sesiones y servicios</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ver directiva de firewall</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configurar directiva de firewall</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configurar caché</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configurar VPN</td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">X</td>
</tr>
</tbody>
</table>
  
##### Permisos
  
Aplique el principio de privilegios mínimos al configurar permisos para los administradores del servidor ISA, tal como se describe en la siguiente sección. Determine cuidadosamente los usuarios que tienen permiso para iniciar sesión en el equipo servidor ISA y elimine el acceso de los que no resulten fundamentales para el funcionamiento del servidor.
  
###### Privilegios mínimos
  
Aplique el principio de privilegios mínimos, según el cual un usuario tiene los privilegios mínimos necesarios para realizar una tarea específica. De este modo se garantiza que si la cuenta de un usuario se pone en peligro, el efecto se minimiza por los privilegios limitados que tiene dicho usuario.
  
Mantenga el grupo Administradores y otros grupos de usuarios lo más pequeños posible. Por ejemplo, un usuario que pertenezca al grupo Administradores del equipo servidor ISA puede realizar cualquier tarea en dicho equipo.
  
Tenga en cuenta que a los usuarios del grupo Administradores se les asigna implícitamente la función de administrador total del servidor ISA, lo que significa que también tienen derechos completos para configurar y supervisar el servidor ISA. Para obtener más información acerca de las funciones, consulte la sección Funciones administrativas.
  
###### Inicio de sesión y configuración
  
Al iniciar sesión en el equipo servidor ISA, hágalo con la cuenta con los privilegios mínimos necesarios para realizar la tarea. Por ejemplo, para configurar una regla, debe iniciar sesión como administrador del servidor ISA. No obstante, si sólo desea ver un informe, inicie sesión con menos privilegios.
  
En general, utilice una cuenta con permisos restrictivos para efectuar tareas rutinarias no administrativas y utilice una cuenta con más permisos únicamente cuando realice tareas administrativas específicas.
  
###### Cuentas de invitado
  
No se recomienda habilitar la cuenta Invitado en el equipo servidor ISA.
  
Cuando un usuario inicia sesión en el equipo servidor ISA, el sistema operativo comprueba si las credenciales coinciden con las de un usuario conocido. Si no coinciden, el usuario inicia sesión como Invitado, con los mismos privilegios que los de la cuenta Invitado.
  
El servidor ISA reconoce la cuenta Invitado como el conjunto de usuarios Todos los usuarios autenticados predeterminado.
  
##### Listas de control de acceso discrecional
  
Con una nueva instalación, las listas de control de acceso discrecional (DACL) del servidor ISA están configuradas correctamente. Además, el servidor ISA vuelve a configurar las DACL de forma apropiada cuando se modifican las funciones administrativas (para obtener más información, consulte la sección Funciones administrativas) y cuando se reinicia el servicio Control del servidor ISA (isactrl).
  
![](images/Dd458738.warning(es-es,TechNet.10).gif)  ADVERTENCIA  
Debido a que el servidor ISA vuelve a configurar periódicamente las DACL, no debe utilizar la herramienta Configuración y análisis de seguridad para configurar las DACL por archivo en los objetos del servidor ISA. De lo contrario, puede haber conflictos entre las DACL configuradas por Directiva de grupo y las DACL que el servidor ISA intenta configurar.
  
No modifique las DACL configuradas por el servidor ISA. Tenga en cuenta que el servidor ISA no configura DACL para los objetos de la siguiente lista. Debe configurar cuidadosamente las DACL para los objetos de la siguiente lista, asignando permisos únicamente a usuarios específicos de confianza:
  
-   Carpeta de informes (cuando se opta por publicar los informes).
  
-   Archivos de configuración creados al exportar o realizar una copia de seguridad de la configuración.
  
-   Archivos de registro de los que se hace copia de seguridad en otra ubicación.
  
Asegúrese de configurar cuidadosamente las DACL, concediendo permisos únicamente a usuarios y grupos de confianza. Asimismo, asegúrese de crear DACL estrictas en los objetos que el servidor ISA utiliza indirectamente. Por ejemplo, al crear una conexión ODBC que utilizará el servidor ISA, asegúrese de mantener el nombre de origen de datos (DSN) seguro.
  
Configure DACL estrictas para todas las aplicaciones que se ejecutan en el equipo servidor ISA. Asegúrese de configurar DACL estrictas para los datos asociados del sistema de archivos y del Registro.
  
![](images/Dd458738.tip(es-es,TechNet.10).gif)  Sugerencia  
No se recomienda guardar datos fundamentales (como ejecutables y archivos de registro) en particiones FAT32. Esto se debe a no se pueden configurar DACL para particiones FAT32.
  
#### Reducción de la superficie de ataque
  
Para proteger todavía más el equipo servidor ISA, aplique el principio de *superficie de ataque reducida*. Para reducir la cantidad de superficie de ataque, siga estas directrices:
  
-   No ejecute aplicaciones y servicios innecesarios en el equipo servidor ISA. Deshabilite los servicios y las funciones que no sean fundamentales para la tarea actual, tal como se describe en la sección Consolidación de la seguridad de la infraestructura de Windows.
  
-   Deshabilite las características del servidor ISA que no utilice. Por ejemplo, si no necesita caché, deshabilítela. Si no precisa la funcionalidad VPN del servidor ISA, deshabilite el acceso de clientes de VPN.
  
-   Identifique los servicios y tareas que no son fundamentales para el modo en que administra la red y, a continuación, deshabilite las reglas de directiva del sistema asociadas.
  
-   Limite la aplicación de las reglas de directiva del sistema únicamente a las entidades de red requeridas. Por ejemplo, el grupo de configuración de directiva del sistema de Active Directory, habilitado de forma predeterminada, se aplica a todos los equipos de la red interna. Puede limitarlo de modo que se aplique a un grupo de Active Directory específico de la red interna.
  
En las siguientes secciones se describe el modo en que se puede reducir la superficie de ataque del equipo servidor ISA.
  
##### Deshabilitación de características del servidor ISA
  
Según sus necesidades de red específicas, es posible que no precise el amplio conjunto de características incluidas en el servidor ISA. Debe analizar cuidadosamente sus necesidades específicas y determinar si necesita lo siguiente:
  
-   Acceso de clientes de VPN
  
-   Caché
  
-   Complementos
  
Si no necesita una característica concreta, deshabilítela.
  
###### Acceso de cliente de VPN
  
El acceso de cliente de VPN está deshabilitado de forma predeterminada. Esto significa que la regla de directiva del sistema pertinente, denominada *Permitir el tráfico de cliente de VPN al servidor ISA*, también está deshabilitada. La regla de red predeterminada denominada *De clientes de VPN hacia la red interna* está habilitada, aunque el acceso de cliente de VPN esté deshabilitado. Si el acceso de cliente de VPN se ha habilitado anteriormente, puede deshabilitarlo si no es necesario.
  
**Para comprobar que el acceso de cliente de VPN está deshabilitado, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Redes privadas virtuales (VPN)**.
  
3.  En el panel de detalles, haga clic en la ficha **Clientes de VPN** y, a continuación, en **Compruebe que el acceso de cliente de VPN esté habilitado**.
  
    [![](images/Dd458738.sechgd08(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd08_big(es-es,technet.10).gif)
  
4.  En la ficha **General** compruebe que **Habilitar acceso de clientes de VPN** no está activado.
  
    ![](images/Dd458738.sechgd09(es-es,TechNet.10).gif)
  
###### Caché
  
La caché está deshabilitada de forma predeterminada. Esto significa que todas las funciones de caché pertinentes, incluida la descarga programada de contenido, están deshabilitadas. Si la caché se había habilitado anteriormente para el servidor ISA, puede deshabilitarla.
  
**Para comprobar que la caché está deshabilitada, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor*, en **Configuración** y, a continuación, en **Caché**.
  
3.  En el panel de detalles, haga clic en la ficha **Unidades de caché**.
  
4.  En la ficha **Tareas**, haga clic en **Deshabilitar caché**.
  
    > [!NOTE]
    > Si la caché está deshabilitada, no aparecerá esta opción.
  
    [![](images/Dd458738.sechgd10(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd10_big(es-es,technet.10).gif)
  
###### Complementos
  
Cuando se instala el servidor ISA, también se instala un conjunto de filtros de aplicación y Web. Posteriormente, puede instalar complementos adicionales proporcionados por otros proveedores. Siga estas directrices de seguridad:
  
-   No instale filtros de aplicación o Web que no necesite.
  
-   Nunca instale un filtro que no sea de un origen de confianza.
  
-   Guarde la DLL asociada al complemento en una biblioteca protegida (por ejemplo, %ProgramFiles%\\Microsoft ISA Server). Asegúrese de configurar ACL estrictas para esta biblioteca.
  
-   Deshabilite los filtros de aplicación y Web que no necesite.
  
**Para deshabilitar un complemento, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor*, en **Configuración** y, a continuación, en **Complementos**.
  
3.  En el panel de detalles, seleccione el complemento correspondiente.
  
4.  En la ficha **Tareas**, haga clic en **Deshabilitar filtros seleccionados**.
  
##### Directiva del sistema
  
El servidor ISA incluye una configuración de directiva del sistema predeterminada, lo que permite el uso de servicios que normalmente requieren la infraestructura de red para funcionar correctamente.
  
En general, desde un punto de vista de la seguridad, se recomienda configurar la directiva del sistema de modo que no se permita el acceso a los servicios que no sean necesarios para administrar la red. Después de la instalación, revise cuidadosamente las reglas de directiva del sistema configuradas. Del mismo modo, después de efectuar tareas de administración importantes vuelva a revisar la configuración de directiva del sistema.
  
En las secciones siguientes se describen los servicios que habilitan las reglas de directiva del sistema.
  
###### Servicios de red
  
Al instalar el servidor ISA, se habilitan los servicios de red básicos. Tras la instalación, el servidor ISA puede tener acceso a los servidores de resolución de nombres y los servicios de sincronización de hora de la red interna.
  
Si los servicios de red están disponibles en otra red, debe modificar los orígenes de grupo de configuración correspondientes que se aplicarán a la red específica. Por ejemplo, suponga que el servidor DHCP no se encuentra en la red interna, sino en una red perimetral. Modifique el grupo de configuración DHCP para que se aplique a dicha red perimetral.
  
Puede modificar la directiva del sistema de modo que sólo se pueda tener acceso a determinados equipos de la red interna. Si los servicios se encuentran en otro lugar, también puede agregar redes adicionales.
  
En la siguiente tabla se muestran las reglas de directiva del sistema que se aplican a los servicios de red.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">DHCP</td>
<td style="border:1px solid black;">Permitir peticiones DHCP del servidor ISA a interna
Permitir respuestas DHCP de servidores DHCP al servidor ISA</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante los protocolos DHCP (respuesta) y DHCP (petición).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DNS</td>
<td style="border:1px solid black;">Permitir DNS del servidor ISA hacia servidores seleccionados</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a todas las redes mediante el protocolo DNS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">NTP</td>
<td style="border:1px solid black;">Permitir NTP del servidor ISA a servidores NTP de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante el protocolo NTP (UDP).</td>
</tr>
</tbody>
</table>
  
###### Servicios DHCP
  
Si el servidor DHCP no se encuentra en la red interna, tendrá que modificar la regla de directiva del sistema de modo que se aplique a la red en que se encuentra el servidor DHCP. Por ejemplo, si el servidor DHCP se encuentra en la red externa, realice los siguientes pasos.
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, haga clic en **DHCP**.
  
    [![](images/Dd458738.sechgd11(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd11_big(es-es,technet.10).gif)
  
5.  En la ficha **De**, haga clic en **Agregar**.
  
6.  En **Agregar entidades de red** seleccione un objeto de red.
  
    [![](images/Dd458738.sechgd12(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd12_big(es-es,technet.10).gif)
  
    > [!TIP]
    > Si se conoce la dirección IP del servidor DHCP, se recomienda crear un conjunto de equipos con sólo dicha dirección IP y seleccionar dicho conjunto. Esta acción se recomienda cuando el servidor DHCP se encuentra en una red que no es de confianza.
  
7.  Haga clic en **Agregar** y, a continuación, en **Cerrar**.
  
###### Servicios de autenticación
  
Una de las capacidades fundamentales del servidor ISA es el poder aplicar una directiva de firewall a usuarios específicos. No obstante, para autenticar usuarios el servidor ISA debe poder establecer comunicación con los servidores de autenticación. Por este motivo, de forma predeterminada, el servidor ISA puede establecer comunicación con los servidores Active Directory (para la autenticación de Windows) y con los servidores RADIUS que se encuentran en la red interna.
  
En la siguiente tabla se muestran las reglas de directiva del sistema que se aplican a los servicios de autenticación.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Active Directory</td>
<td style="border:1px solid black;">Permitir acceso a servicios de directorio para propósitos de autenticación
Permitir RPC del servidor ISA a servidores de confianza
Permitir CIFS de Microsoft CIFS del servidor ISA a servidores de confianza
Permitir la autenticación Kerberos del servidor ISA a servidores de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante varios protocolos LDAP, protocolo RPC (todas las interfaces), varios protocolos CIFS de Microsoft y varios protocolos Kerberos, mediante el servicio de directorio Active Directory.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RSA SecurID</td>
<td style="border:1px solid black;">Permitir la autenticación SecurID del servidor ISA a servidores de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante el protocolo RSA SecurID®.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RADIUS</td>
<td style="border:1px solid black;">Permitir la autenticación RADIUS del servidor ISA a servidores RADIUS de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante varios protocolos RADIUS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Lista de revocación de certificados</td>
<td style="border:1px solid black;">Permitir HTTP desde el servidor ISA hacia todas las redes para las descargas de CRL</td>
<td style="border:1px solid black;">Servicios de autenticación: permite HTTP desde el servidor ISA hacia redes seleccionadas para descargar listas de revocación de certificados (CRL) actualizadas.</td>
</tr>
</tbody>
</table>
  
###### DCOM
  
Si necesita utilizar el protocolo DCOM (por ejemplo, para administrar de forma remota el equipo servidor ISA), asegúrese de que no habilita **Hacer cumplir la comprobación RPC estricta**.
  
**Para comprobar que Hacer cumplir la comprobación RPC estricta no está activado, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, haga clic en **Active Directory**.
  
5.  Compruebe que **Hacer cumplir la comprobación RPC estricta** no está activado.
  
    [![](images/Dd458738.sechgd13(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd13_big(es-es,technet.10).gif)
  
    > [!TIP]
    > DCOM normalmente es necesario para varios servicios, incluida la administración remota y la inscripción automática.
  
###### Servicios de autenticación de Windows y RADIUS
  
Si no necesita la autenticación de Windows o la autenticación RADIUS, debe realizar los siguientes pasos para deshabilitar los grupos de configuración de directiva del sistema correspondientes.
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, haga clic en **Active Directory**.
  
    [![](images/Dd458738.sechgd14(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd14_big(es-es,technet.10).gif)
  
5.  En la ficha **General** compruebe que **Habilitar** no está activado.
  
    > [!NOTE]
    > Cuando se deshabilita el grupo de configuración de directiva del sistema de Active Directory, se deshabilita el acceso a todos los protocolos LDAP. Si necesita los protocolos LDAP, cree una regla de acceso que permita el uso de estos protocolos.
  
6.  Repita los pasos 4 y 5 para el grupo de configuración RADIUS.
  
    > [!TIP]
    > Si sólo necesita la autenticación de Windows, asegúrese de configurar la directiva del sistema y deshabilitar el uso de los demás mecanismos de autenticación.
  
###### Servicios de autenticación RSA SecurID
  
La comunicación con los servidores de autenticación RSA SecurID no está habilitada de forma predeterminada. Si la directiva de firewall requiere la autenticación RSA SecurID, asegúrese de habilitar este grupo de configuración.
  
###### Servicios de autenticación de CRL
  
Las listas de revocación de certificados (CRL) no se pueden descargar de forma predeterminada. Esto se debe a que el grupo de configuración Descarga de CRL no está habilitado de forma predeterminada.
  
**Para habilitar la descarga de CRL, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, haga clic en **Descarga de CRL**.
  
5.  En la ficha **General** compruebe que **Habilitar** está activado.
  
6.  En la ficha **A** seleccione las entidades de red desde las que se pueden descargar las listas de revocación de certificados.
  
    [![](images/Dd458738.sechgd15(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd15_big(es-es,technet.10).gif)
  
Se permitirá todo el tráfico HTTP desde la red del host local (el equipo servidor ISA) a las entidades de red enumeradas en la ficha **A**.
  
###### Administración remota
  
El servidor ISA normalmente se administra desde un equipo remoto. Determine cuidadosamente los equipos remotos que podrán administrar y supervisar el servidor ISA. En la siguiente tabla se enumeran las reglas de directiva del sistema que se deben configurar.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Management Console</td>
<td style="border:1px solid black;">Permitir la administración remota desde equipos seleccionados que usan MMC
Permitir la comunicación de Control de Firewall de Microsoft a equipos seleccionados</td>
<td style="border:1px solid black;">Permite que los equipos del conjunto de equipos Equipos de administración remota tengan acceso al equipo servidor ISA mediante los protocolos de control de firewall de MS y RPC (todas las interfaces).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Terminal Server</td>
<td style="border:1px solid black;">Permitir la administración remota desde equipos seleccionados por medio de Terminal Server</td>
<td style="border:1px solid black;">Permite que los equipos del conjunto de equipos Equipos de administración remota tengan acceso al equipo servidor ISA mediante el protocolo RDP (Servicios de Terminal Server).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ICMP (Ping)</td>
<td style="border:1px solid black;">Permitir peticiones ICMP (PING) de equipos seleccionados al servidor ISA</td>
<td style="border:1px solid black;">Permite que los equipos del conjunto de equipos Equipos de administración remota tengan acceso al equipo servidor ISA mediante el protocolo Ping y viceversa.</td>
</tr>
</tbody>
</table>
  
De forma predeterminada, las reglas de directiva del sistema que permiten la administración remota del servidor ISA están habilitadas. El servidor ISA se puede administrar mediante la ejecución de un complemento de Microsoft Management Console (MMC) remoto o mediante Servicios de Terminal Server.
  
De forma predeterminada, estas reglas se aplican al conjunto de equipos Equipos de administración remota integrado. Al instalar el servidor ISA, se crea este conjunto de equipos vacío. Agregue a este conjunto de equipos vacío todos los equipos que administrarán el servidor ISA de forma remota. Hasta que lo haga, no estará disponible la administración remota desde ningún equipo.
  
![](images/Dd458738.tip(es-es,TechNet.10).gif)  Sugerencia  
Limite la administración remota a equipos específicos mediante la configuración de reglas de directiva del sistema que sólo se apliquen a direcciones IP específicas.
  
**Para habilitar la administración remota, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Herramientas** haga clic en **Objetos de red**.
  
    ![](images/Dd458738.sechgd16(es-es,TechNet.10).gif)
  
4.  En la barra de herramientas situada debajo de **Objetos de red**, en **Conjuntos de equipos**, haga clic con el botón secundario del ratón en **Equipos de administración remota** y, a continuación, haga clic en **Propiedades**.
  
    ![](images/Dd458738.sechgd17(es-es,TechNet.10).gif)
  
5.  Haga clic en **Agregar** y, a continuación, en **Equipo**.
  
6.  En **Nombre** escriba el nombre del equipo.
  
7.  En **Dirección IP del equipo** escriba la dirección IP del equipo que puede administrar el servidor ISA de forma remota.
  
###### Supervisión y registro remotos
  
De forma predeterminada, el registro y la supervisión remotos están deshabilitados. Los siguientes grupos de configuración están deshabilitados de forma predeterminada:
  
-   Registro remoto (NetBIOS)
  
-   Registro remoto (SQL)
  
-   Supervisión remota del rendimiento
  
-   Microsoft Operations Manager
  
En la siguiente tabla se proporciona una descripción de los grupos de configuración.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Registro remoto (NetBIOS)</td>
<td style="border:1px solid black;">Permitir el registro remoto a servidores de confianza que usan NetBIOS</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante varios protocolos NetBIOS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Registro remoto (SQL)</td>
<td style="border:1px solid black;">Permitir el registro SQL remoto del servidor ISA a servidores seleccionados</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA utilice protocolos de Microsoft (SQL) para tener acceso a la red interna.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Supervisión remota del rendimiento</td>
<td style="border:1px solid black;">Permitir la supervisión remota de rendimiento del servidor ISA desde servidores de confianza</td>
<td style="border:1px solid black;">Permite que los equipos del conjunto de equipos Equipos de administración remota tengan acceso al equipo servidor ISA mediante varios protocolos NetBIOS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Operations Manager</td>
<td style="border:1px solid black;">Permitir la supervisión remota del servidor ISA a servidores de confianza, por medio del agente Microsoft Operations Manager (MOM).</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante el agente Microsoft Operations Manager.</td>
</tr>
</tbody>
</table>
  
###### Habilitación del registro y supervisión remotos
  
**Para habilitar la supervisión y el registro remotos, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, seleccione uno o varios de los siguientes grupos de configuración:
  
    -   Registro remoto (NetBIOS)
  
    -   Registro remoto (SQL)
  
    -   Supervisión remota del rendimiento
  
    -   Microsoft Operations Manager
  
5.  En la ficha **General** compruebe que **Habilitar** está activado.
  
###### Recurso compartido de cliente firewall
  
Si ha instalado el componente Recurso compartido de cliente firewall al instalar el servidor ISA, el grupo de configuración Recurso compartido de instalación de cliente firewall está habilitado de forma predeterminada. Todos los equipos de la red interna pueden tener acceso a la carpeta compartida. En la siguiente tabla se muestra el grupo de configuración de directiva del sistema (y la regla) que está habilitado.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Instalación de cliente firewall</td>
<td style="border:1px solid black;">Permitir acceso de equipos de confianza al recurso compartido de cliente firewall en el servidor ISA</td>
<td style="border:1px solid black;">Permite que los equipos de la red interna tengan acceso al equipo servidor ISA mediante varios protocolos CIFS y NetBIOS de Microsoft. Cuando se habilita esta regla, se permite el acceso al equipo servidor ISA mediante SMB desde cualquier red o equipo especificado. El acceso no está limitado únicamente a la carpeta de recurso compartido de instalación de cliente firewall.</td>
</tr>
</tbody>
</table>
  
Si no ha instalado el componente Recurso compartido de cliente firewall, este grupo de configuración no está habilitado.
  
###### Servicios de diagnóstico
  
De forma predeterminada, las reglas de directiva del sistema que permiten el acceso a los servicios de diagnóstico están habilitadas, con los siguientes permisos.
  
-   **ICMP.** Se permite para todas las redes. Este servicio resulta importante para determinar la conectividad a otros equipos.
  
-   **Red de Windows.** Permite la comunicación NetBIOS, de forma predeterminada para equipos de la red interna.
  
-   **Informes de error de Microsoft.** Permite el acceso HTTP al conjunto de direcciones URL de sitios de informes de error de Microsoft, con el fin de permitir la comunicación de información de errores. De forma predeterminada, este conjunto de direcciones URL incluye sitios de Microsoft específicos.
  
-   **Comprobadores de conectividad.** Permite que el equipo servidor ISA utilice los protocolos HTTP y HTTPS para comprobar si responde un equipo específico.
  
En la siguiente tabla se muestran los grupos de configuración de directiva del sistema que están habilitados de forma predeterminada.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">ICMP</td>
<td style="border:1px solid black;">Permitir peticiones ICMP del servidor ISA a servidores seleccionados</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a todas las redes mediante varios protocolos ICMP y el protocolo Ping.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Red de Windows</td>
<td style="border:1px solid black;">Permitir NetBIOS del servidor ISA a servidores de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a todas las redes mediante varios protocolos NetBIOS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Comunicación con Microsoft (Informes de error de Microsoft)</td>
<td style="border:1px solid black;">Permitir HTTP/HTTPS del servidor ISA a sitios de informes de error de Microsoft especificados</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a los miembros del conjunto de direcciones URL de sitios de informes de error de Microsoft mediante los protocolos HTTP o HTTPS.</td>
</tr>
</tbody>
</table>
  
###### Comprobadores de conectividad
  
Además, el siguiente servicio de diagnóstico no está habilitado de forma predeterminada: Comprobadores de conectividad HTTP.
  
Cuando se crea un comprobador de conectividad, el grupo de configuración Comprobadores de conectividad HTTP está habilitado, lo que permite que la red de host local utilice HTTP o HTTPS para tener acceso a los equipos de otra red. En la siguiente tabla se describe el grupo de configuración Comprobadores de conectividad HTTP.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Comprobadores de conectividad HTTP</td>
<td style="border:1px solid black;">Permitir HTTP/HTTPS de firewall a todas las redes, para los comprobadores de conectividad</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA compruebe la conectividad mediante el envío de peticiones HTTP GET al equipo especificado.</td>
</tr>
</tbody>
</table>
  
Se recomienda limitar este acceso a equipos específicos cuya conectividad se desee comprobar.
  
**Para limitar este acceso, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, haga clic en **Comprobadores de conectividad HTTP**.
  
    [![](images/Dd458738.sechgd18(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd18_big(es-es,technet.10).gif)
  
5.  En la ficha **A** haga clic en **Todas las redes (y host local)** y, a continuación, en **Quitar**.
  
6.  Haga clic en **Agregar** y, a continuación, seleccione las entidades de red cuya conectividad desee comprobar. Se permitirá todo el tráfico HTTP desde la red del host local (el equipo servidor ISA) a las entidades de red enumeradas en la ficha **A**.
  
###### SMTP
  
De forma predeterminada, el grupo de configuración SMTP está habilitado, lo que permite la comunicación SMTP del servidor ISA a los equipos de la red interna. Por ejemplo, esto se necesita cuando se desea enviar información de alerta en un mensaje de correo electrónico. En la siguiente tabla se describe el grupo de configuración SMTP.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">SMTP</td>
<td style="border:1px solid black;">Permitir SMTP del servidor ISA a servidores de confianza</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a la red interna mediante el protocolo SMTP.</td>
</tr>
</tbody>
</table>
  
###### Trabajos de descarga programada
  
De forma predeterminada, la característica de trabajos de descarga programada está deshabilitada. En la siguiente tabla se describe el grupo de configuración Trabajos de descarga programada.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Trabajos de descarga programada</td>
<td style="border:1px solid black;">Permitir HTTP del servidor ISA a equipos seleccionados, para trabajos de descarga de contenido</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a todas las redes mediante el protocolo HTTP.</td>
</tr>
</tbody>
</table>
  
Al crear un trabajo de descarga de contenido, se le pedirá que habilite esta regla de directiva del sistema. El servidor ISA podrá tener acceso a los sitios especificados en el trabajo de descarga de contenido.
  
###### Acceso al sitio Web de Microsoft
  
La directiva del sistema predeterminada permite el acceso HTTP y HTTPS de la red del host local (es decir, el equipo servidor ISA) al sitio Web microsoft.com. Esto es necesario por una serie de motivos:
  
-   Informe de errores (tal como se ha descrito en la sección Servicios de diagnóstico)
  
-   Acceso a documentación útil acerca del sitio Web del servidor ISA y de otros sitios Web relacionados
  
De forma predeterminada, el grupo de configuración Sitios permitidos está habilitado, lo que permite que el servidor ISA tenga acceso a sitios específicos que pertenecen al conjunto de nombres de dominio Sitios permitidos de directiva del sistema. En la siguiente tabla se describe el grupo de configuración Sitios permitidos.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de configuración</th>
<th style="border:1px solid black;" >Nombre de regla</th>
<th style="border:1px solid black;" >Descripción de la regla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sitos permitidos</td>
<td style="border:1px solid black;">Permitir peticiones HTTP/HTTPS del servidor ISA a sitios especificados</td>
<td style="border:1px solid black;">Permite que el equipo servidor ISA tenga acceso a los miembros del conjunto de direcciones URL de sitios permitidos de directiva del sistema mediante los protocolos HTTP o HTTPS.</td>
</tr>
</tbody>
</table>
  
Este conjunto de direcciones URL incluye varios sitios Web de Microsoft de forma predeterminada. Puede modificar el conjunto de nombres de dominio para incluir sitios Web adicionales a los que se permitirá el acceso al servidor ISA.
  
**Para modificar el conjunto de direcciones URL para incluir sitios Web adicionales, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Herramientas** haga clic en **Objetos de red**.
  
    ![](images/Dd458738.sechgd19(es-es,TechNet.10).gif)
  
4.  En **Conjuntos de nombre de dominio**, haga clic con el botón secundario del ratón en **Sitios permitidos de directiva del sistema** y, a continuación, haga clic en **Propiedades**.
  
5.  En la ficha **General** haga clic en **Nuevo** y, a continuación, escriba la dirección URL del sitio Web específico.
  
    ![](images/Dd458738.sechgd20(es-es,TechNet.10).gif)
  
El acceso HTTP y HTTPS se permitirá a los sitios Web especificados.
  
#### Modo de cierre
  
Una función crucial de un firewall es reaccionar ante un ataque. Cuando se produce un ataque, puede parecer que la primera línea de defensa sea desconectarse de Internet y aislar la red en peligro por intrusos malintencionados. No obstante, no constituye el enfoque recomendado. Aunque el ataque se debe afrontar, la conectividad de red se debe reanudar lo más pronto posible y se debe determinar el origen del ataque.
  
La función de cierre presentada en ISA Server 2004 combina la necesidad de aislamiento con la de mantener la conexión. Siempre que se produzca una situación que provoque el cierre del servicio Firewall de Microsoft, el servidor ISA pasa al modo de cierre. Esto se produce cuando:
  
-   Un suceso provoca que se cierre el servicio Firewall. Cuando se configuran las definiciones de alerta, se deciden los sucesos que provocarán el cierre del servicio Firewall. Fundamentalmente, se configura cuándo pasa el servidor ISA al modo de cierre.
  
-   El servicio Firewall se cierra manualmente. Si detecta ataques malintencionados, puede cerrar el servicio Firewall, mientras configura el equipo servidor ISA y la red para afrontar los ataques.
  
##### Funcionalidad afectada
  
En modo de cierre, se aplica la siguiente funcionalidad:
  
-   El motor de filtro de paquetes de firewall (fweng) aplica la directiva de firewall.
  
-   Se permite el tráfico saliente de la red del host local a todas las redes. Si se establece una conexión saliente, dicha conexión se puede utilizar para responder al tráfico entrante. Por ejemplo, una consulta DNS puede recibir una respuesta DNS, en la misma conexión.
  
-   No se permite tráfico entrante, a menos que haya habilitada una regla de directiva del sistema que permita específicamente el tráfico. La única excepción es el tráfico DHCP, que siempre se permite. Es decir, las peticiones DHCP en el puerto UDP 67 se permiten del host local a todas las redes y se permite que entren las respuestas DHCP en el puerto UDP 68.
  
-   Siguen siendo aplicables las siguientes reglas de directiva del sistema:
  
    -   Permitir ICMP desde servidores de confianza al host local.
  
    -   Permitir administración remota del firewall mediante MMC (RPC a través de puerto 3847).
  
    -   Permitir administración remota del firewall mediante RDP.
  
-   Los clientes de acceso remoto de VPN no pueden tener acceso al servidor ISA. De forma similar, se deniega el acceso a las redes de sitio remoto en escenarios VPN de sitio a sitio.
  
-   Cualquier cambio en la configuración de red durante el modo de cierre sólo se aplica después de que el servicio Firewall se reinicia y el servidor ISA sale del modo de cierre. Por ejemplo, si mueve físicamente un segmento de red y vuelve a configurar el servidor ISA para que se corresponda con los cambios físicos, la nueva topología sólo estará en efecto después de que el servidor ISA salga del modo de cierre.
  
-   El servidor ISA no activa alertas.
  
##### Salida del modo de cierre
  
Cuando el servicio Firewall se reinicia, el servidor ISA sale del modo de cierre y continúa funcionando, tal como lo hacía anteriormente. Los cambios efectuados en la configuración del servidor ISA se aplican después de que salga del modo de cierre.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Protección de la configuración
  
Cuando configure la directiva de firewall del servidor ISA junto con la directiva de seguridad corporativa, siga el principio de denegar todo el tráfico que no esté permitido explícitamente. El servidor ISA implementa esta directiva de forma predeterminada. Una regla de directiva de firewall, denominada Regla predeterminada, deniega el acceso de todos los usuarios a todas las redes. Debido a que esta regla se procesa en último lugar, se denegará el tráfico no permitido explícitamente.
  
#### Validación de la configuración después de la actualización
  
La directiva de ISA Server 2000 se puede migrar a ISA Server 2004, ya sea mediante actualización o mediante el Asistente para migración del servidor ISA. Revise cuidadosamente la directiva migrada. ISA Server 2004 emplea un modelo de directiva distinto de ISA Server 2000. Asegúrese de que la directiva de firewall está configurada según la directiva de seguridad de su organización.
  
#### Validación de la configuración de directiva de firewall
  
Después de crear una directiva de firewall, se recomienda comprobarla activamente. Valide que el tráfico que desea que pase esté permitido. Asimismo, valide que sólo están abiertos los puertos aplicables.
  
#### Red privada virtual
  
Es importante seguir las prácticas recomendadas para seguridad al utilizar ISA Server 2004 como un servidor de red privada virtual (VPN). A continuación se ofrece una lista de recomendaciones para proteger el equipo servidor ISA en su función de servidor VPN:
  
-   Se recomiendan las conexiones de protocolo de túnel de capa 2 (L2TP) sobre seguridad del protocolo Internet (IPSec) para obtener el máximo cifrado. Se recomienda implementar y exigir una directiva de contraseña segura, por lo que se reducen las posibilidades de un ataque de diccionario. Cuando se implementa una directiva de ese tipo, se puede deshabilitar el bloqueo de cuentas, por lo que se reducen las posibilidades de que un atacante active dicho bloqueo.
  
-   Considere la posibilidad de exigir a los clientes de VPN remotos que ejecuten determinados sistemas operativos (como Microsoft Windows Server 2003, Windows 2000 Server o Windows XP). No todos los sistemas operativos tienen los mismos niveles de seguridad en sus sistemas de archivos y en sus cuentas de usuario. Asimismo, no todas las características de acceso remoto están disponibles en todos los sistemas operativos.
  
-   Utilice la característica de control de cuarentena del servidor ISA para proporcionar acceso de red por fases a los clientes de VPN remotos. Con el control de cuarentena, los clientes están limitados a un modo de cuarentena antes de que se les permita tener acceso a la red. Aunque el control de cuarentena no protege de los piratas informáticos, se pueden comprobar las configuraciones de equipo para los usuarios autorizados y, si es necesario, corregirlas para que puedan tener acceso a la red.
  
##### Protección contra virus con VPN
  
No se impide automáticamente que los equipos cliente de VPN infectados por virus inunden el equipo servidor ISA o las redes que protege con peticiones. Para evitar que suceda esto, implemente prácticas de supervisión para detectar anomalías, como alertar o picos inusuales de cargas de tráfico, y configure la notificación de alertas para utilizar mensajes de correo electrónico. Si se identifica un equipo cliente de VPN infectado:
  
-   Restrinja el acceso de VPN por nombre de usuario mediante la directiva de acceso remoto para excluir al usuario de los clientes VPN que tienen permiso para conectarse.
  
-   Restrinja el acceso de VPN por dirección IP. Para ello, cree una nueva red que contenga las direcciones IP externas que se han bloqueado y mueva la dirección IP del cliente de la red externa a la nueva red.
  
##### Autenticación para VPN
  
Utilice métodos de autenticación que proporcionen seguridad adecuada. El método más seguro es EAP-TLS (Protocolo de autenticación extensible-Seguridad de la capa de transporte) cuando se utiliza conjuntamente con tarjetas inteligentes. A pesar de los retos de implementación que implica el uso de EAP-TLS y tarjetas inteligentes, que requieren una infraestructura de claves públicas (PKI), se considera el método de autenticación más seguro. Habilite EAP-TLS, que está deshabilitado de forma predeterminada en el perfil de una directiva de acceso remoto.
  
Cuando utilice el protocolo de autenticación EAP-TLS, debe instalar un certificado de equipo en el servidor del Servicio de autenticación de Internet (IAS). Para la autenticación de clientes y usuarios, puede instalar un certificado en el equipo cliente o puede utilizar tarjetas inteligentes. Antes de implementar certificados, debe diseñar el certificado con los requisitos correctos.
  
Si utiliza la autenticación basada en contraseñas, imponga directivas de contraseña segura en la red para que los ataques de diccionario sean más difíciles.
  
Considere la posibilidad de requerir que los clientes VPN remotos se autentiquen con protocolos de seguridad más seguros, como la versión 2 del protocolo de autenticación por desafío mutuo de Microsoft (MS-CHAP v2) o el protocolo de autenticación extensible (EAP), en vez de permitirles que utilicen protocolos como PAP (protocolo de autenticación de contraseña), SPAP (protocolo de autenticación de contraseña de Shiva) y CHAP (protocolo de autenticación por desafío mutuo).
  
Se recomienda deshabilitar PAP (protocolo de autenticación de contraseña), SPAP (protocolo de autenticación de contraseña de Shiva) y CHAP (protocolo de autenticación por desafío mutuo). De forma predeterminada, PAP, SPAP y CHAP están deshabilitados.
  
#### Traducción de vínculos
  
La característica de traducción de vínculos de ISA Server 2004 traduce los encabezados HTTP, independientemente de si está habilitada la traducción de vínculos. Esto implica que, al publicar un servidor Web especificando que se puede utilizar **Cualquier nombre de dominio**, un pirata informático puede enviar contenido malintencionado en el encabezado. Si el servidor publicado redirige peticiones a una página de cualquier equipo, la respuesta se puede infectar (se podría modificar para contener la dirección URL del encabezado enviado por el pirata informático). Si un servidor indirecto ha almacenado en caché esta página, un usuario que tuviera acceso a la página se redirigiría al sitio Web configurado por el pirata informático.
  
Por este motivo, se recomienda especificar nombres de dominio a los que se aplique la regla de publicación en Web.
  
**Para especificar nombres de dominio concretos, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En el panel de detalles, seleccione la regla de publicación en Web aplicable.
  
4.  En la ficha **Tareas** haga clic en **Editar regla seleccionada**.
  
5.  En la ficha **Nombre público**, en **Esta regla se aplica a**, seleccione **Peticiones para los sitios Web siguientes**.
  
    ![](images/Dd458738.sechgd21(es-es,TechNet.10).gif)
  
6.  Haga clic en **Agregar**.
  
7.  En **Nombre de dominio público o dirección IP**, escriba el nombre de dominio específico al que se debe aplicar la regla de publicación en Web.
  
#### Límites de conexión
  
El servidor ISA limita el número de conexión en un momento dado. Puede configurar el límite especificando un número máximo de conexiones simultáneas. Cuando se haya alcanzado el número máximo de conexiones, se denegará cualquier nueva petición de cliente para dicho servicio de escucha Web.
  
Puede limitar el número total de creación de sesiones UDP, ICMP y demás Raw IP permitidas por una regla de publicación o acceso a servidor, por segundo. Estas limitaciones no se aplican a las conexiones TCP. Cuando se sobrepasa el número especificado de conexiones, no se crearán nuevas. Las conexiones existentes no se desconectarán.
  
Se recomienda configurar límites de conexiones bajos. De este modo, se puede limitar de forma efectiva que los hosts malintencionados consuman recursos del equipo servidor ISA.
  
De forma predeterminada, los límites para conexiones que no sean TCP están configurados a 1000 por segundo y regla, y a 160 conexiones por cliente. Los límites para conexiones TCP están configurados en 160 por cliente. Se recomienda no cambiar estos límites preconfigurados. Si debe modificar los límites de conexiones, configure un número de conexiones tan pequeño como sea posible.
  
**Para configurar los límites de conexiones, realice los pasos siguientes.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor*, en **Configuración** y, a continuación, en **General**.
  
3.  En el panel de detalles, haga clic en **Definir límites de conexiones**.
  
    [![](images/Dd458738.sechgd22(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd22_big(es-es,technet.10).gif)
  
4.  En la ficha **Límite de conexiones** seleccione **Limitar el número de conexiones por cliente a**.
  
    ![](images/Dd458738.sechgd23(es-es,TechNet.10).gif)
  
5.  Realice las siguientes acciones:
  
    1.  En **Conexiones creadas por segundo por regla (no TCP)** escriba el número de conexiones permitidas por regla y segundo.
  
    2.  En **Límite de conexiones por cliente (TCP y no TCP)** escriba el número de conexiones permitidas por cliente.
  
#### Clientes firewall
  
El servidor ISA admite una forma más segura de comunicación entre el cliente firewall y el servidor ISA, que implica el uso de cifrado mediante un canal de control TCP. Puede configurar el servidor ISA para aceptar conexiones únicamente de clientes que establezcan comunicación de esta forma segura. No obstante, esto impide que se conecten versiones anteriores del software de cliente firewall.
  
Se recomienda permitir que únicamente los clientes firewall puedan establecer comunicación sobre una conexión cifrada. Esto incluye todo el software de cliente firewall para los equipos ISA Server 2004.
  
**Para configurar clientes firewall, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor*, en **Configuración** y, a continuación, en **General**.
  
3.  En el panel de detalles haga clic en **Definir la configuración del cliente firewall**.
  
    [![](images/Dd458738.sechgd24(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd24_big(es-es,technet.10).gif)
  
4.  En la ficha **Conexión** compruebe que no está activado **Permitir conexiones de cliente firewall sin usar cifrado**.
  
    ![](images/Dd458738.sechgd25(es-es,TechNet.10).gif)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Protección de la implementación
  
El primer paso en la protección del servidor ISA consiste en comprobar que el equipo servidor ISA está seguro físicamente y que ha aplicado las recomendaciones de configuración de seguridad básicas.
  
Después de proteger el equipo servidor ISA y aplicar las directrices de seguridad al configurar la directiva en el servidor, debe tener en cuenta el modo de implementar la infraestructura de red. En esta sección se describen directrices de seguridad que se deben tener en cuenta al implementar una red protegida por el servidor ISA.
  
#### Autenticación
  
Al configurar la autenticación para las peticiones Web, utilice el método de autenticación más seguro posible. Se recomienda utilizar los siguientes métodos de autenticación sobre conexiones no seguras:
  
-   Básica
  
-   Implícita
  
-   Autenticación basada en formularios de Outlook® Web Access
  
-   SecurID
  
-   RADIUS
  
##### Uso de servidores RADIUS
  
El servicio de usuario de acceso telefónico de autenticación remota (RADIUS) es un protocolo estándar del sector que se utiliza para proporcionar autenticación. Un cliente RADIUS (normalmente un servidor de acceso telefónico, un servidor VPN o un punto de acceso inalámbrico) envía las credenciales de usuario en forma de mensaje RADIUS a un servidor RADIUS. El servidor RADIUS autentica la petición de cliente RADIUS y devuelve una respuesta de mensaje RADIUS.
  
Debido a que los servidores RADIUS autorizan las credenciales de usuario, además de autenticarlos, la respuesta que el servidor ISA recibe del servidor RADIUS, en la que se indica que las credenciales de cliente no están aprobadas, puede indicar realmente que el servidor RADIUS no autoriza al cliente. Aunque las credenciales se hayan autorizado, el servidor ISA puede rechazar la petición de cliente basándose en la directiva de autorización del servidor RADIUS.
  
Siga estas directrices al implementar una directiva de VPN o firewall que requiera autenticación RADIUS:
  
-   El mecanismo de ocultación de User-Password de RADIUS puede no proporcionar seguridad suficiente para las contraseñas. El mecanismo de ocultación de RADIUS emplea el secreto compartido de RADIUS, el autenticador de peticiones y el algoritmo de hash MD5 para cifrar User-Password y otros atributos como Tunnel-Password y MS-CHAP-MPPE-Keys. RFC 2865 determina la necesidad potencial de evaluar el entorno y si se precisa establecer seguridad adicional.  
    Se puede proporcionar un nivel de protección adicional a los atributos ocultos mediante la seguridad de protocolos de Internet (IPSec) con carga de seguridad encapsuladora (ESP) y un algoritmo de cifrado, como Triple DES (3DES), que garantizan la confidencialidad de los datos del mensaje de RADIUS completo. Siga estas directrices recomendadas:
  
    -   Utilice IPSec para proporcionar seguridad adicional a clientes y servidores RADIUS.
  
    -   Exija el uso de contraseñas de usuario seguras.
  
    -   Utilice el recuento de autenticación y el bloqueo de cuentas para evitar un ataque de diccionario en una contraseña de usuario.
  
    -   Utilice un secreto compartido largo con una secuencia aleatoria de letras, números y signos de puntuación. Cámbielo con frecuencia para proteger el servidor ISA.
  
-   Si utiliza la autenticación basada en contraseñas, imponga directivas de contraseña segura en la red para que los ataques de diccionario sean más difíciles.
  
-   Cuando los nombres de usuario se especifican en un idioma distinto del inglés, el servidor ISA utilice la página de códigos actual instalada en el equipo servidor ISA para traducir los datos de usuario. El usuario sólo se puede autenticar si el cliente también utiliza la misma página de códigos.
  
-   Si cambia la directiva de servidor RADIUS mientras usuarios autenticados mediante RADIUS han iniciado la sesión, la nueva directiva no se aplica a ellos. Esto se debe a que el servidor ISA almacena en caché las credenciales de los usuarios que han iniciado la sesión cuando al tener acceso al servidor de Outlook Web Access publicado éste los autentica mediante la autenticación RADIUS.  
    Para aplicar la directiva de servidor RADIUS inmediatamente, puede desconectar la sesión.
  
##### Comprobación de la conectividad a servidores de autenticación
  
Si utiliza un servidor RADIUS para la autenticación, cree un comprobador de conectividad que supervise el estado del servidor. Configure las alertas de modo que se realice una acción adecuada cuando el servidor RADIUS no funcione.
  
**Para comprobar la conectividad, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Supervisión**.
  
3.  En el panel de detalles, haga clic en la ficha **Conectividad**.
  
4.  En la ficha **Tareas**, haga clic en **Crear nuevo comprobador de conectividad**.
  
5.  En la página **Bienvenida** del asistente, escriba un nombre para el comprobador de conectividad y, a continuación, haga clic en **Siguiente**.
  
6.  En la página **Detalles de comprobación de conectividad** haga lo siguiente:
  
    ![](images/Dd458738.sechgd26(es-es,TechNet.10).gif)
  
    1.  En **Supervisar la conectividad a este servidor o dirección URL** escriba el nombre del servidor que se supervisará.
  
    2.  En **Método de comprobación** seleccione un método para efectuar la comprobación. Haga clic en **Siguiente** y, a continuación, en **Finalizar**.
  
7.  Si la regla de directiva del sistema que permite la comprobación de conectividad HTTP no está habilitada y ha activado **Enviar una petición HTTP "Get"**, se le pedirá que habilite la regla de directiva del sistema. Haga clic en **Sí**.  
    Para obtener más información acerca de las reglas de directiva del sistema de comprobación de conectividad HTTP, consulte la sección Comprobadores de conectividad.
  
8.  En el panel de detalles, seleccione la regla que acaba de crear.
  
9.  En la ficha **Tareas** haga clic en **Editar comprobador seleccionado**.
  
10. En la ficha **Propiedades** compruebe que está activado **Desencadenar una alerta si el servidor no responde dentro del tiempo de espera especificado**.
  
    ![](images/Dd458738.sechgd27(es-es,TechNet.10).gif)
  
##### Implementación de servidores de autenticación
  
Por motivos de seguridad, se recomienda colocar los servidores de autenticación en una red de nivel de seguridad alto. Cuando sea posible, considere la posibilidad de colocar los servidores de autenticación en una red independiente (aparte de las redes interna y perimetral). De este modo, puede impedir el acceso directo desde cualquier host de las redes interna y perimetral a los servidores de autenticación.
  
En este caso, debe modificar la regla de directiva del sistema correspondiente de modo que se aplique a la red en la que se encuentra el servidor de autenticación.
  
**Para implementar servidores de autenticación, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Directiva de firewall**.
  
3.  En la ficha **Tareas**, haga clic en **Editar directiva del sistema**.
  
4.  En el Editor de directivas del sistema, en el árbol Grupos de configuración, en Servicios de autenticación, haga clic en el método de autenticación correspondiente.
  
5.  En la ficha **A**, haga clic en **Agregar**.
  
6.  En **Agregar entidades de red**, seleccione la red en la que se encuentra el servidor de autenticación.
  
#### Servidores DNS
  
DNS (sistema de nombres de dominio) es el protocolo de resolución de nombres para redes IP, como Internet. Los servidores DNS alojan la información que permite que los equipos cliente resuelvan nombres DNS alfanuméricos fáciles de recordar en las direcciones IP que los equipos utilizan para establecer comunicación entre sí.
  
El servidor ISA incluye un mecanismo de resolución de nombres similar al mecanismo de resolución de nombres del servidor DNS. De este modo, cuando un cliente efectúa una petición a un host de otra red especificando la dirección URL del equipo host, el servidor ISA puede resolver el nombre del equipo. El servidor ISA envía una petición de resolución de nombre al servidor DNS que se ha configurado para utilizarse.
  
Para evitar la infección de caché de DNS, se recomienda configurar el servidor ISA para que utilice un servidor DNS de confianza (por ejemplo, un servidor DNS de Windows) con la opción de evitar la corrupción de caché habilitada. Este servidor DNS se debe encontrar en la red interna.
  
Si implementa un servidor DNS en una red que no sea de confianza (por ejemplo, en la red externa), se recomienda que también se instale un servidor DNS en una red de confianza (por ejemplo, una red perimetral). A continuación, configure el servidor DNS en la red de confianza para que reenvíe las peticiones al servidor DNS de la red que no es de confianza.
  
**Para configurar DNS, realice los siguientes pasos en el equipo servidor ISA.**
  
1.  Haga clic en **Inicio**, seleccione **Panel de control** y haga doble clic en **Conexiones de red**.
  
2.  Haga clic con el botón secundario del ratón en la conexión que desea cambiar y, a continuación, haga clic en **Propiedades**.
  
3.  En la ficha **General**, en **Esta conexión utiliza los siguientes elementos**, haga clic en **Protocolo de Internet (TCP/IP)** y, a continuación, en **Propiedades**.
  
    ![](images/Dd458738.sechgd28(es-es,TechNet.10).gif)
  
4.  Seleccione **Usar las siguientes direcciones de servidor DNS**.
  
5.  En **Servidor DNS preferido** y en **Servidor DNS alternativo** escriba las direcciones IP de un servidor DNS de confianza de la red interna.
  
    ![](images/Dd458738.sechgd29(es-es,TechNet.10).gif)
  
#### Supervisión y solución de problemas
  
Una tarea importante y rutinaria que se debe realizar es la supervisión del tráfico de red que se permite que pase a través del servidor ISA. Una parte fundamental de la función de supervisión es el análisis atento del registro y la información de auditoría.
  
En las siguientes secciones se ofrecen sugerencias acerca de cómo garantizar la integridad de la información de registro.
  
##### Registro
  
El registro ofrece la oportunidad de revisar la actividad de red, comprobar quién ha tenido acceso a la red. Revise los registros periódica y detenidamente, buscando accesos sospechosos y el uso de recursos de red. Siga estas directrices para sacar el mayor partido al registro del servidor ISA:
  
-   Configure alertas para enviar notificaciones a los administradores. Implemente un procedimiento de respuesta rápida.
  
-   Guarde los registros en una partición de disco NTFS independiente para la máxima seguridad. Sólo los administradores del equipo servidor ISA deben tener acceso a los registros.
  
-   Cuando se guarda la información de registro en una base de datos SQL, utilice la autenticación de Windows (y no la de SQL).
  
-   Si va a registrar la información en una base de datos remota, configure cifrado y firma de datos para la información de registro que se copiará en la base de datos remota.
  
-   Para obtener la máxima seguridad, configure IPSec para las comunicaciones entre el equipo servidor ISA y SQL Server.
  
-   Si la información de registro no se puede guardar por algún motivo, cierre el equipo servidor ISA. Para ello, configure una definición de alerta para el suceso Error de registro que detenga el servicio de firewall.
  
##### Límites de almacenamiento del registro
  
Utilice la característica de mantenimiento del registro prudentemente, para garantizar que no se llena el disco en el que se almacena la información de registro.
  
Configure la definición de alerta de Límites de almacenamiento del registro para detener los servicios del servidor ISA. De este modo, sólo permitirá el acceso cuando éste se pueda auditar de forma adecuada.
  
**Para configurar los límites de almacenamiento del registro, realice los siguientes pasos.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft ISA Server** y, a continuación, haga clic en **Administración del servidor ISA**.
  
2.  En el árbol de consola de Administración del servidor ISA, haga clic en **Microsoft ISA Server 2004**, en el *nombre\_de\_servidor* y, a continuación, en **Supervisión**.
  
3.  En el panel de detalles, haga clic en la ficha **Alertas**.
  
4.  En la ficha **Tareas** haga clic en **Configurar definiciones de alerta**.
  
    [![](images/Dd458738.sechgd30(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458738.sechgd30_big(es-es,technet.10).gif)
  
5.  En **Definiciones de alerta** haga clic en **Límites de almacenamiento del registro** y, a continuación, haga clic en **Editar**.
  
    ![](images/Dd458738.sechgd31(es-es,TechNet.10).gif)
  
6.  En la ficha **General** seleccione **Habilitar**.
  
7.  En la ficha **Acciones** haga clic en **Detener los servicios seleccionados** y, a continuación, en **Seleccionar**.
  
    ![](images/Dd458738.sechgd32(es-es,TechNet.10).gif)
  
8.  En **Servicios**, seleccione **Firewall de Microsoft** y **Programador de trabajos de Microsoft ISA Server**.
  
##### Auditoría
  
Habilite la auditoría de Windows. De este modo, puede supervisar quien inicia sesión en el equipo servidor ISA.
  
**Para habilitar la auditoría, realice los siguientes pasos en el equipo servidor ISA.**
  
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y, a continuación, haga clic en **Directiva de seguridad local**.
  
2.  En el panel de detalles, haga clic en **Configuración de seguridad**, en **Directivas locales** y, a continuación, en **Directiva de auditoría**.
  
3.  En el panel de detalles, haga clic con el botón secundario el ratón en **Auditar sucesos de inicio de sesión** y, a continuación, haga clic en **Propiedades**.
  
    ![](images/Dd458738.sechgd33(es-es,TechNet.10).gif)
  
4.  Seleccione **Correcto** y **Erróneo**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Recursos adicionales
  
Para obtener información acerca de Microsoft ISA Server, visite el [sitio Web de Microsoft ISA Server](http://www.microsoft.com/isa).
  
¿Tiene comentarios acerca de este documento? Enviar [comentarios](mailto:isadocs@microsoft.com).
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar la solución completa**
  
[Guía de consolidación de la seguridad de ISA Server 2004](http://download.microsoft.com/download/c/e/c/cecc8742-2102-42d4-9fc7-6b641bebbf56/isasecurityguide.doc)
  
[](#mainsection)[Principio de la página](#mainsection)
