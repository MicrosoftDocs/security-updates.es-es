---
TOCTitle: 'Guía de generación: Implementación de la infraestructura de seguridad para LAN inalámbricas'
Title: 'Guía de generación: Implementación de la infraestructura de seguridad para LAN inalámbricas'
ms:assetid: '4dcbde01-d2ca-4a3c-b6de-13f492fb6d77'
ms:contentKeyID: 20112547
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458725(v=TechNet.10)'
---

Capítulo 9: Implementación de la infraestructura de seguridad para LAN inalámbricas
===================================================================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#eiaa)[Introducción](#eiaa)
[](#ehaa)[Hoja de trabajo de planeamiento de WLAN mediante 802.1X](#ehaa)
[](#egaa)[Preparación del entorno para una WLAN segura](#egaa)
[](#efaa)[Configuración e implementación de certificados de autenticación de WLAN](#efaa)
[](#eeaa)[Configuración de la estructura de acceso de WLAN](#eeaa)
[](#edaa)[Habilitación del acceso a WLAN para usuarios y equipos](#edaa)
[](#ecaa)[Configuración de AP inalámbricos para redes 802.1X](#ecaa)
[](#ebaa)[Pruebas y comprobación](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Introducción

En este capítulo se proporcionan instrucciones detalladas para implementar la seguridad de LAN inalámbricas (WLAN) con el protocolo 802.1X que está basado en Microsoft® Windows Server™ 2003 y Microsoft Windows® XP Service Pack 1 (SP1). En las instrucciones de este capítulo se incluye la configuración de los grupos de seguridad del servicio de directorio Active Directory®, la implementación de los certificados X.509 para la autenticación de WLAN, la modificación de la configuración del servidor de Servicio de autenticación de Internet (IAS) de Microsoft, la implementación de la directiva de grupo de WLAN y sugerencias para configurar puntos de acceso inalámbricos. En este capítulo se incluyen todas las opciones necesarias para implementar la seguridad de WLAN mediante 802.1X y EAP-TLS (Protocolo de autenticación extensible-Seguridad de la capa de transporte).

El objetivo de este capítulo es proporcionar instrucciones de implementación para el diseño de WLAN segura descrito en el capítulo 6, “Diseño de seguridad para LAN inalámbrica mediante 802.1X”. En el capítulo no se intenta explicar ninguno de los conceptos generales de 802.1X, EAP, RADIUS (Servicio de usuario de acceso telefónico de autenticación remota) ni ninguno de los aspectos específicos de una implementación de WLAN segura basada en 802.1X. Para obtener información general acerca de muchas de estas tecnologías, consulte el artículo "Windows XP Wireless Deployment Technology and Component Overview", que se enumera en la sección "Información adicional" al final de este capítulo.

Este capítulo complementa los capítulos de la guía de planeamiento y la guía de operaciones de la infraestructura de claves públicas (PKI), RADIUS y WLAN. En los capítulos de la guía de planeamiento se explica la lógica subyacente en las decisiones de implementación empleadas aquí. En el capítulo de la guía de operaciones se explican las tareas y procesos necesarios para mantener de forma correcta la infraestructura de 802.1X- Si todavía no lo ha hecho, debe leer los capítulos de planeamiento antes de continuar con este capítulo. También debe leer y comprender las implicaciones de los requisitos de asistencia del capítulo de operaciones antes de implementar esta guía en un entorno de producción.

#### Requisitos previos

En esta sección se incluyen listas de comprobación que le ayudarán a decidir la preparación de su organización para la WLAN basada en 802.1X. (“Preparación” se emplea aquí con un significado logístico en vez de un sentido empresarial; la motivación empresarial para implementar esta solución se trata en capítulos anteriores de la guía de planeamiento.)

##### Requisitos previos de conocimientos

Debe estar familiarizado con los conceptos de 802.1X y la implementación de este estándar en los productos de Microsoft correspondientes, como Windows Server 2003 y Windows XP Service Pack 1. También se precisan conocimientos de Windows Server 2003 o de Windows 2000 en las siguientes áreas:

-   Conceptos de Active Directory (incluidas las estructuras y herramientas de Active Directory, manipulación de usuarios, grupos y otros objetos de Active Directory, así como el uso de la directiva de grupo).

-   Seguridad del sistema de Windows, conceptos de seguridad como usuarios, grupos y listas de control de acceso (ACL), así como el uso de las herramientas de la línea de comandos.

-   Comprensión de las secuencias de comandos de archivos por lotes. El conocimiento de Windows Scripting Host y el lenguaje Microsoft Visual Basic® Scripting Edition (VBScript) le ayudará a sacar el máximo provecho de las secuencias de comandos suministradas, pero no es esencial.

Antes de continuar con este capítulo, también debe leer los capítulos de planeamiento y disponer de un conocimiento exhaustivo de la arquitectura y el diseño de la solución.

##### Requisitos previos organizativos

Debe consultar a otros miembros de la organización que puedan tener necesidad de participar en la implementación de esta solución, como:

-   Patrocinadores empresariales

-   Personal de seguridad y auditoría

-   Personal de ingeniería, administración y operaciones de Active Directory

-   Personal de ingeniería de asistencia, administración y operaciones

-   Personal de ingeniería, administración y operaciones de DNS (sistema de nombres de dominio) y redes

##### Requisitos previos de la infraestructura de TI

En el capítulo también se supone lo siguiente:

-   Ya existe una infraestructura de dominios de Active Directory de Windows Server 2003 implementada. Todos los usuarios de la solución de 802.1X deben ser miembros de dominios del mismo bosque de Active Directory.

    **Nota:** para obtener más información acerca de la compatibilidad con versiones anteriores de Microsoft Windows, consulte el apéndice A, “Matriz de compatibilidad de versiones de Windows”.

-   No se dispone de una solución WLAN basada en 802.1X existente. Aunque esta solución no impide la implementación junto con una solución WLAN 802.1X existente, no se incluye orientación para la integración en una infraestructura de 802.1X existente.

-   Se ha implementado una PKI según lo descrito en el capítulo 7, "Implementación de la infraestructura de claves públicas" y está preparada para realizar la inscripción automática de certificados.

-   Se debe implementar una infraestructura de apoyo, como DNS y DHCP (protocolo de configuración dinámica de host), y estar preparada para dar servicio a los equipos cliente de la WLAN.

-   Dos o más servidores con IAS como servidores RADIUS como se ha descrito en el capítulo 8, "Implementación de la infraestructura de RADIUS". Durante este capítulo se efectuará una configuración adicional de estos servidores.

-   Una WLAN con puntos de acceso inalámbricos compatibles con 802.1X y clientes de Windows XP Professional Service Pack 1 con privacidad equivalente por cable (WEP) de 128 bits o WPA y tarjetas de interfaz de red WLAN con capacidades 802.1X. Durante este capítulo se efectuará una configuración adicional de estos componentes.

#### Descripción general del capítulo

El diagrama de la figura muestra el proceso de implementar la seguridad de WLAN mediante 802.1X, según se ha descrito en este capítulo.

![](images/Dd458725.09fig9-1(es-es,TechNet.10).gif)

**Figura 9.1 Diagrama del proceso de implementación de la infraestructura de 802.1X**

Estos pasos están reflejados en la organización del capítulo y se describen en la siguiente lista. Cada uno consta de tareas de instalación o configuración. Asimismo, cada paso dispone de procedimientos de comprobación, por lo que puede comprobar que todo funciona antes de continuar con el paso siguiente.

-   **Hoja de trabajo de planeamiento de WLAN mediante 802.1X**. Presenta la información de configuración utilizada en este capítulo para configurar los diversos componentes de la WLAN 802.1X. Contiene una tabla donde se describe la información que se debe proporcionar antes de empezar la implementación de las instrucciones de este capítulo.

-   **Preparación del entorno para una WLAN segura**. Describe la preparación de los grupos de seguridad de Active Directory necesarios para configurar y administrar la WLAN 802.1X en un período de tiempo. Además, se proporcionan recomendaciones de alto nivel para DHCP.

-   **Configuración e implementación de certificados de autenticación de WLAN**. Describe la creación e implementación de las plantillas de certificados X.509 necesarios para las autenticaciones WLAN 802.1X. También se incluye la comprobación de la implementación.

-   **Configuración de la estructura de acceso de WLAN**. Describe la creación y configuración de la directiva de acceso remoto IAS para redes basadas en 802.1X y EAP-TLS. También se incluye la adición de puntos de acceso inalámbricos como clientes del Servicio RADIUS a los servidores IAS.

-   **Habilitación del acceso a WLAN para usuarios y equipos**. Describe la configuración de permisos de usuario y equipo mediante Active Directory para habilitar el acceso a WLAN segura. En esta sección se incluyen también los pasos para crear e implementar la directiva de grupo de Active Directory para configurar clientes de WLAN con la configuración de 802.1X y 802.11 adecuada.

-   **Configuración de AP inalámbricos para redes 802.1X**. Enumera los aspectos que se deben tener en cuenta para configurar puntos de acceso inalámbricos para redes basadas en 802.1X.

-   **Pruebas y comprobación**. Proporciona el método para probar la funcionalidad de una WLAN basada en 802.1X.

[](#mainsection)[Principio de la página](#mainsection)

### Hoja de trabajo de planeamiento de WLAN mediante 802.1X

En las tablas de esta sección se indican los parámetros de configuración utilizados en la solución. Utilícelas como lista de comprobación cuando tome decisiones de planeamiento.

Muchos de los parámetros de estas tablas se configuran manualmente y forman parte de los procedimientos que se describen en este capítulo. Muchos se establecen mediante una secuencia de comandos que se ejecuta como parte de uno de los procedimientos o se les hace referencia en una secuencia de comandos para completar otra configuración o tarea operativa.

**Nota:** las secuencias de comandos utilizadas en la guía de generación se describen más detalladamente en el archivo Léame.txt que se incluye con las mismas.

#### Elementos de configuración definidos por el usuario

En la siguiente tabla se enumeran parámetros específicos de organización tomados de la compañía ficticia Woodgrove Bank. Asegúrese de que ha recopilado, o tomado decisiones sobre valores equivalentes para su organización, todos estos elementos antes de iniciar el procedimiento de instalación. Los valores ficticios que se muestran aquí se utilizan en todo el capítulo en los comandos de muestra proporcionados. Debe sustituir estos valores por los adecuados para su organización. Los lugares en los que debe utilizar sus propios valores se muestran en cursiva.

**Tabla 9.1: Elementos de configuración definidos por el usuario**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento de configuración</p></th>
<th><p>Configuración</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre DNS del dominio raíz del bosque de Active Directory</p></td>
<td style="border:1px solid black;"><p><em>woodgrovebank.com</em></p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre de dominio NetBIOS (servicio básico de entrada y salida de red)</p></td>
<td style="border:1px solid black;"><p><em>WOODGROVEBANK</em></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del servidor IAS principal</p></td>
<td style="border:1px solid black;"><p><em>HQ-IAS-01</em></p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre del servidor IAS secundario</p></td>
<td style="border:1px solid black;"><p><em>HQ-IAS-02</em></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del servidor IAS de sucursal opcional</p></td>
<td style="border:1px solid black;"><p><em>BO-IAS-03</em></p></td>
</tr>  
</tbody>  
</table>
  
#### Elementos de configuración recomendados por la solución
  
La configuración especificada en esta tabla no se debe cambiar en su instalación, a menos que sea necesario utilizar valores diferentes a los del diseño de la solución. Cambiar los parámetros de diseño proporcionados es perfectamente aceptable si se es consciente de que, al hacerlo, se dejará de utilizar la solución probada. Asegúrese de que comprende todas las implicaciones del cambio de una configuración y sus dependencias antes de alterar uno de los valores en los procedimientos de configuración y en las secuencias de comandos suministradas.
  
**Tabla 9.2: Elementos de configuración que recomienda la solución**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Configuración</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que controla la implementación de certificados de autenticación de usuario de 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente la autenticación del cliente: certificado de usuario</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Nombre anterior a Windows 2000 del grupo global de Active Directory que controla la implementación de certificados de autenticación de usuario de 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente la autenticación del cliente: certificado de usuario</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que controla la implementación de certificados de autenticación de equipo de 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente la autenticación del cliente: certificado del equipo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Nombre anterior a Windows 2000 del grupo global de Active Directory que controla la implementación de certificados de autenticación de equipo de 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente la autenticación del cliente: certificado del equipo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene servidores IAS que requieren certificados de autenticación 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente el certificado de autenticación de servidor IAS y RAS</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Nombre anterior a Windows 2000 del grupo global de Active Directory que contiene servidores IAS que requieren certificados de autenticación 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente el certificado de autenticación de servidor IAS y RAS</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene los usuarios que pueden obtener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto: usuarios inalámbricos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Nombre anterior a Windows 2000 para el grupo global de Active Directory que contiene los usuarios que pueden obtener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto: usuarios inalámbricos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene los equipos que pueden obtener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto: equipos inalámbricos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene los equipos que pueden obtener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto: equipos inalámbricos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo universal de Active Directory que contiene el grupo de usuarios inalámbricos y el grupo de equipos inalámbricos</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto - Acceso inalámbrico</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Grupo universal de Active Directory que contiene el grupo de usuarios inalámbricos y el grupo de equipos inalámbricos</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto - Acceso inalámbrico</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene los equipos que requieren la configuración de las propiedades de red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de red inalámbrica - Equipo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Cuentas] Grupo global de Active Directory que contiene los equipos que requieren la configuración de las propiedades de red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de red inalámbrica - Equipo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Certificados] Plantilla de certificado utilizada para generar certificados para la autenticación del cliente usuario</p></td>
<td style="border:1px solid black;"><p>Autenticación de cliente: usuario</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Certificados] Plantilla de certificado utilizada para generar certificados para la autenticación del equipo cliente</p></td>
<td style="border:1px solid black;"><p>Autenticación de cliente: equipo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Certificados] Plantilla de certificado utilizada para generar certificados de autenticación de servidor para que IAS los utilice</p></td>
<td style="border:1px solid black;"><p>Autenticación de servidor IAS y RAS</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Secuencias de comandos] Ruta para las secuencias de comandos de instalación</p></td>
<td style="border:1px solid black;"><p>C:\MSSScripts</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Config] Ruta para archivos de copia de seguridad de la configuración</p></td>
<td style="border:1px solid black;"><p>D:\IASConfig</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Registros de solicitudes] Ubicación de los registros de textos de autenticación y auditoría IAS</p></td>
<td style="border:1px solid black;"><p>D:\IASLogs</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Directiva de acceso remoto] Nombre de directiva</p></td>
<td style="border:1px solid black;"><p>Permitir acceso inalámbrico</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>[Directiva de grupo] Nombre del objeto Directiva de grupo (GPO) de Active Directory</p></td>
<td style="border:1px solid black;"><p>Directiva de red inalámbrica</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>[Directiva de grupo] Directiva de red inalámbrica del GPO</p></td>
<td style="border:1px solid black;"><p>Configuración inalámbrica de equipo cliente</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación del entorno para una WLAN segura
  
Antes de implementar redes inalámbricas seguras basadas en 802.1X debe preparar la infraestructura de soporte del entorno. La infraestructura de soporte está formada por servidores de Active Directory y DHCP. Para obtener instrucciones de planeamiento de WLAN pormenorizadas, consulte el manual “Deploying a Wireless LAN” del *Kit de implementación de Windows Server 2003* y los demás recursos mencionados en la sección “Información adicional” al final de este módulo.
  
#### Creación de los grupos de Active Directory necesarios para el acceso a WLAN
  
Debe ejecutar la siguiente secuencia de comandos como usuario con permiso de creación de grupos de seguridad de Active Directory. Esta secuencia de comandos crea los grupos necesarios para la inscripción de certificados de autenticación inalámbrica, la directiva de acceso remoto y la directiva de grupo de red inalámbrica:
  
Cscript //job:CreateWirelessGroups C:\\MSSScripts\\wl\_tools.wsf
  
La secuencia de comandos crea los siguientes grupos de seguridad basados en Active Directory, que se utilizan en toda esta guía:
  
-   Inscribir automáticamente la autenticación del cliente: certificado de usuario
  
-   Inscribir automáticamente la autenticación del cliente: certificado del equipo
  
-   Inscribir automáticamente el certificado de autenticación de servidor IAS y RAS
  
-   Directiva de acceso remoto: usuarios inalámbricos
  
-   Directiva de acceso remoto: equipos inalámbricos
  
-   Directiva de acceso remoto - Acceso inalámbrico
  
-   Directiva de red inalámbrica - Equipo
  
En un bosque con múltiples dominios, estos grupos deben crearse en el mismo dominio que los usuarios inalámbricos.
  
**Nota:** la mayoría de los grupos creados aquí son globales, pero, si es necesario, se pueden sustituir por grupos universales. La secuencia de comandos que crea los grupos de seguridad se puede modificar fácilmente; copie la sintaxis empleada para crear el grupo universal Directiva de acceso remoto - Acceso inalámbrico.
  
#### Comprobación de la configuración de DHCP
  
Para trabajar con redes inalámbricas, debe configurar servidores DHCP con ámbitos específicos para redes inalámbricas y tiempos de concesión de direcciones del Protocolo de Internet (IP) menores que los de los clientes cableados. Consulte a los administradores de los servidores DHCP para asegurarse de que ha configurado los servidores DHCP correctamente para su compatibilidad con una solución inalámbrica.
  
Puede encontrar instrucciones de planeamiento de DHCP para redes inalámbricas en el capítulo “Deploying a Wireless LAN” del *Kit de implementación de Windows Server 2003.*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración e implementación de certificados de autenticación de WLAN
  
La solución WLAN segura que se describe en esta guía utiliza certificados de X.509 para realizar la autenticación de equipos y usuarios con EAP-TLS. En la sección siguiente se describe la creación e implementación de los certificados que se mencionan:
  
-   Autenticación de cliente: equipo
  
-   Autenticación de cliente: usuario
  
-   Autenticación de servidor IAS y RAS
  
    **Nota:** consulte el capítulo 11, “Administración de la infraestructura de claves públicas”, para obtener información detallada acerca de estas tareas y las funciones necesarias para realizarlas.
  
#### Creación de plantillas de certificados para la autenticación de servidores
  
En el servidor IAS se necesita un certificado de servidor para autenticar el equipo a los clientes durante el protocolo de enlace de EAP-TLS. El administrador de Servicios de Certificate Server debe llevar a cabo los pasos siguientes con el complemento Consola de administración de plantillas de certificados de Microsoft (MMC) en el servidor de los servicios de certificados para crear una plantilla de certificados de autenticación de servidores, para su utilización con los servidores IAS.
  
**Para crear una plantilla de certificados de autenticación de servidores**
  
1.  Cree un duplicado de la plantilla de certificados de servidor** **IAS y RAS. Escriba **Autenticación de servidor IAS y RAS** en el campo **Nombre para mostrar plantilla** en la ficha **General** de las propiedades de la nueva plantilla.
  
2.  En la ficha **Extensiones**, asegúrese de que las directivas de aplicación sólo contienen **Autenticación de servidor** (OID 1.3.6.1.5.5.7.3.1).
  
3.  También en la ficha **Extensiones**, edite las directivas de emisión y agregue la directiva **Seguridad media**.
  
4.  En la ficha **Nombre de sujeto**, seleccione **Construido a partir de esta información de Active Directory**. Además, asegúrese de que **Formato de nombre de sujeto** tiene el valor **Nombre común** y de que sólo **Nombre DNS** está seleccionado en **Incluir esta información en un nombre de sujeto alternativo**.
  
5.  En la ficha **Tratamiento de la petición**, haga clic en el botón **CSP**, compruebe que está seleccionado **Las solicitudes tienen que usar uno de los siguientes CSP** y que sólo está seleccionado **Microsoft RSA SChannel Cryptographic Provider**.
  
6.  En la ficha **Seguridad**, agregue el grupo de seguridad Certificado de autenticación de servidor IAS y RAS inscrito automáticamente con permisos de **Lectura**, **Inscripción** e **Inscripción automática**.
  
    **Importante:** debe eliminar los demás grupos que tengan permisos para inscribir y/o inscribir automáticamente esta plantilla de certificado. Los usuarios o grupos que deban inscribir estos certificados deben agregarse al grupo de inscripción (o de inscripción automática) de plantilla de certificados pertinente. Esta configuración impide que los usuarios o los grupos puedan inscribir inadvertidamente certificados que no deberían. Consulte la sección "Creación de grupos de inscripción de plantillas de certificados" del capítulo 11, "Administración de la infraestructura de claves públicas", para obtener más información.
  
En el capítulo 4, “Diseño de la infraestructura de claves públicas”, se describe la configuración de este tipo de certificado para que requiera la aprobación del administrador de certificados. Puesto que se considera que este certificado tiene un valor relativamente alto, debe considerar la posibilidad de habilitar esta opción para proporcionar una comprobación adicional en el caso de que alguien tratara de inscribir un servidor IAS falso. Con este enfoque significa que será necesaria la aprobación manual para emitir el certificado (si bien la solicitud será enviada automáticamente por el servidor IAS y el certificado se recuperará automáticamente cuando sea aprobado).
  
#### Creación de plantillas de certificados para la autenticación de usuarios
  
Los usuarios finales necesitan certificados de usuario para la autenticación en el servidor IAS durante la autenticación EAP-TLS. El administrador de Servicios de Certificate Server debe llevar a cabo los pasos siguientes con el complemento Consola de administración de plantillas de certificados de Microsoft (MMC) en el servidor de los servicios de certificados para crear una plantilla de certificados de autenticación de usuarios.
  
**Para crear una plantilla de certificados de autenticación de usuarios**
  
1.  Cree un duplicado de la plantilla Sesión autenticada. Escriba **Autenticación de cliente: usuario** en el campo **Nombre para mostrar plantilla** de la ficha **General** de la nueva plantilla.
  
2.  En la ficha **Tratamiento de la petición**, seleccione **CSP** y desactive las casillas de verificación de **Microsoft Base DSS Cryptographic Provider**.
  
3.  En la ficha **Nombre de sujeto**, compruebe que está activado **Construido a partir de esta información de Active Directory**. En **Formato de nombre de sujeto**,** **seleccione **Nombre común**. Asegúrese de que **Nombre principal del usuario (UPN**) es la única opción seleccionada en **Incluir esta información en un nombre de sujeto alternativo**.
  
4.  En la ficha **Extensiones**, asegúrese de que sólo **Autenticación de cliente (OID 1.3.6.1.5.5.7.3.2)** se incluye en **Directivas de aplicación**.
  
5.  También en la ficha **Extensiones**, edite las directivas de emisión y agregue la directiva **Seguridad baja**.
  
6.  En la ficha **Seguridad**, agregue el grupo de seguridad Inscribir automáticamente la autenticación del cliente: certificado de usuario con permisos de **Lectura**, **Inscripción** e **Inscripción automática**.
  
    **Importante:** debe eliminar los demás grupos que tengan permisos para inscribir y/o inscribir automáticamente esta plantilla de certificado. Los usuarios o grupos que deban inscribir estos certificados deben agregarse al grupo de inscripción (o de inscripción automática) Plantilla de certificado pertinente. Consulte la nota anterior.
  
#### Creación de plantillas de certificados para la autenticación de equipos
  
Es necesario un certificado para la autenticación de equipos en el servidor IAS durante la autenticación EAP-TLS. El administrador de Servicios de Certificate Server debe llevar a cabo los pasos siguientes con el complemento Consola de administración de plantillas de certificados de Microsoft (MMC) en el servidor de los servicios de certificados para crear una plantilla de certificados de autenticación de equipos.
  
**Para crear una plantilla de certificados de autenticación de equipos**
  
1.  Cree un duplicado de la plantilla Autenticación de estación de trabajo. Escriba **Autenticación de cliente: equipo** en el campo **Nombre para mostrar plantilla** de la ficha **General** de la nueva plantilla.
  
2.  En la ficha **Nombre de sujeto**, compruebe que está activado **Construido a partir de esta información de Active Directory**. En **Formato de nombre de sujeto**, seleccione **Nombre común**. Asegúrese de que **Nombre DNS** es la única opción seleccionada en **Incluir esta información en un nombre de sujeto alternativo**.
  
3.  En la ficha **Extensiones**, edite las directivas de aplicación y asegúrese de que sólo se incluye **Autenticación de cliente (OID 1.3.6.1.5.5.7.3.2)**.
  
4.  También en la ficha **Extensiones**, edite las directivas de emisión y agregue la directiva **Seguridad baja**.
  
5.  En la ficha **Seguridad**, agregue el grupo de seguridad Autenticación de cliente inscrito automáticamente: certificado de equipo** **(WOODGROVEBANK\\Autenticación de cliente inscrito automáticamente: certificado de equipo) con los permisos de **Lectura**, **Inscripción **e **Inscripción automática**.
  
    **Importante:** debe eliminar los demás grupos que tengan permisos para inscribir y/o inscribir automáticamente esta plantilla de certificado. Los usuarios o grupos que deban inscribir estos certificados deben agregarse al grupo de inscripción (o de inscripción automática) Plantilla de certificado pertinente. Consulte la nota anterior.
  
#### Adición de los certificados de autenticación de WLAN a la Entidad emisora de certificados
  
Una vez que se han configurado las plantillas de certificados de autenticación de WLAN, debe agregarlos a la entidad emisora de certificados (CA) para habilitar la inscripción. El administrador de Servicios de Certificate Server debe llevar a cabo los pasos siguientes para agregar plantillas de certificado a la CA.
  
**Agregar plantillas de certificados a la CA**
  
En el complemento Entidad emisora de certificados de MMC, haga clic con el botón secundario del mouse en la carpeta **Plantillas de certificados**, seleccione **Nueva** y, a continuación, **Plantilla de certificado que se va a emitir**. Seleccione los certificados siguientes y, a continuación, haga clic en **Aceptar**:
  
-   Autenticación de cliente: equipo
  
-   Autenticación de cliente: usuario
  
-   Autenticación de servidor IAS y RAS
  
#### Inscripción del certificado de servidor IAS
  
La distribución de certificados de autenticación de servidores en los servidores IAS es una tarea relativamente sencilla y automatizada. Para realizar esta tarea, lleve a cabo los pasos de la sección siguiente.
  
**Para inscribir un certificado de autenticación de servidor IAS desde la CA**
  
1.  Use el complemento MMC de usuarios y equipos de Active Directory para agregar las cuentas de equipo IAS al grupo de seguridad Certificado de autenticación de servidor IAS y RAS inscrito automáticamente.
  
    **Importante:** tendrá que reiniciar el servidor para que reciba esta nueva pertenencia a grupos.
  
2.  Inicie sesión en IAS como miembro del grupo local Administradores y ejecute GPUPDATE /force en un símbolo del sistema.
  
3.  Abra MMC,** **y, a continuación, agregue el complemento **Certificados**. Cuando se le pida, seleccione la opción **Cuenta de equipo** y, a continuación, **Equipo local**.
  
4.  Seleccione **Certificados (equipo local)** en el árbol de la consola, seleccione **Todas las tareas** en el menú **Acción** y, a continuación, haga clic en **Inscribir certificados automáticamente**.
  
    **Nota:** si la opción para solicitar la aprobación del administrador de certificados se seleccionó para este tipo de certificado, necesitará ponerse en contacto con el administrador de la entidad emisora para comprobar que es una solicitud legítima de un servidor IAS. Una vez comprobado, el administrador de CA emitirá el certificado.
  
#### Comprobación de la implementación de certificados de servidor IAS
  
La velocidad con la que se emitirá e implementará un certificado de servidor IAS inscrito en el almacén de certificados de servidor depende de la configuración de la aprobación de certificados en la plantilla de certificados. También se pueden producir retrasos porque el servidor sólo sondea la entidad tras varias horas.
  
**Para comprobar que el certificado de autenticación de servidor IAS se ha implementado**
  
1.  Inicie la sesión como miembro del grupo local Administradores en el equipo local, abra el complemento Certificados de MMC** **y, a continuación, agregue el complemento **Certificados**. Cuando se le pida, seleccione la opción **Cuenta de equipo** y, a continuación, **Equipo local**.
  
2.  Abra el almacén **Certificados (equipo local)**, **Personal**, **Certificados** y busque un certificado emitido para el nombre del equipo local desde la plantilla de certificado de autenticación de servidor IAS y RAS. Puede ver el nombre de la plantilla en el panel situado a la derecha. Es posible que deba desplazarse horizontalmente para ver la columna adecuada.
  
3.  Si el certificado necesario no aparece en el complemento** **Certificados de MMC, seleccione **Certificados (equipo local)** en el árbol de la consola, seleccione **Todas las tareas** en el menú **Acción** y, a continuación, seleccione **Inscribir certificados automáticamente**. Espere un momento hasta que la acción se lleve a cabo y después actualice la vista de la carpeta** **Personal, Certificados.
  
    **Nota:** también se puede saber si la inscripción automática de certificados se ha realizado correctamente mediante los sucesos del Registro de sucesos de aplicación que tienen como origen Inscripción automática y el Id. de suceso 19.
  
#### Adición de usuarios y equipos a grupos para la inscripción automática
  
La distribución de certificados de autenticación de WLAN a usuarios y equipos es un proceso normalmente transparente para los usuarios finales. El proceso requiere una conexión con una red de área local (LAN), una cuenta de usuario basada en el dominio y un equipo que se haya unido a un dominio de Active Directory.
  
Los usuarios y equipos que necesiten acceso a la nueva WLAN deben tener certificados implementados de antemano para garantizar que pueden llevar a cabo la autenticación EAP-TLS. En equipos con Windows XP y Windows Server 2003, los certificados de equipo y de usuario se pueden inscribir y renovar automáticamente sin acción alguna por parte del usuario final. La inscripción y renovación de los certificados se controla mediante grupos de seguridad de Active Directory.
  
**Nota:** esta solución utilizar grupos de seguridad personalizados (Inscribir automáticamente la autenticación del cliente: certificado de usuario e Inscribir automáticamente la autenticación del cliente: certificado del equipo) para restringir los usuarios y equipos que inscribirán automáticamente certificados de WLAN. Si desea que todos los usuarios y equipos del dominio reciban certificados de WLAN, puede agregar Usuarios del dominio al grupo Inscribir automáticamente la autenticación del cliente: certificado de usuario y Equipos del dominio al grupo Inscribir automáticamente la autenticación del cliente: certificado del equipo.
  
**Para agregar usuarios y equipos a grupos de seguridad para la inscripción automática**
  
1.  Abra el complemento MMC Usuarios y equipos de Active Directory.
  
2.  Agregue usuarios al grupo Inscribir automáticamente la autenticación del cliente: certificado de usuario
  
3.  Agregue equipos al grupo Inscribir automáticamente la autenticación del cliente: certificado del equipo.
  
    **Importante:** los usuarios no recibirán esta nueva pertenencia a grupos en sus símbolos de acceso hasta que cierren la sesión y vuelvan a iniciarla. Los equipos no recibirán esta nueva pertenencia a grupos en sus símbolos de acceso hasta que se reinicien. Asegúrese de que se realizan ambas acciones antes de continuar los pasos de comprobación.
  
##### Comprobación de la implementación de certificados de usuario
  
Lleve a cabo los pasos siguientes cuando haya iniciado la sesión como usuario que se ha agregado al grupo Inscribir automáticamente la autenticación del cliente: certificado de usuario.
  
**Para comprobar la implementación de certificados de autenticación de usuario**
  
1.  Si todavía no lo ha hecho, cierre la sesión y vuelva a iniciarla como el usuario seleccionado. Abra MMC** **y agréguele el complemento **Certificados**. Si se le pide, seleccione la opción **Mi cuenta de usuario**.
  
2.  Abra el almacén **Certificados - Usuario actual**, **Personal**, **Certificados** y busque un certificado emitido para el usuario desde la plantilla de certificado Autenticación de cliente: usuario. Debe ver el nombre de la plantilla en el panel situado a la derecha. Es posible que deba desplazarse horizontalmente para ver la columna adecuada.
  
3.  Si el certificado que requiere no aparece en el complemento **Certificados**, ejecute GPUPDATE /force en un símbolo del sistema, espere unos minutos y, a continuación, renueve la carpeta** **Personal, Certificados.
  
##### Comprobación de la implementación de certificados de equipo
  
Lleve a cabo los pasos siguientes en un equipo cliente que se haya agregado al grupo Inscribir automáticamente la autenticación del cliente: certificado del equipo.
  
**Para comprobar la implementación de certificados de autenticación de equipo**
  
1.  Si no ha reiniciado el equipo después de agregarlo al grupo Inscripción automática, reinícielo ahora.
  
2.  Inicie la sesión como miembro del grupo local Administradores en el equipo local, abra MMC** **y, a continuación, agregue el complemento **Certificados**. Cuando se le pida, seleccione la opción **Cuenta de equipo** y, a continuación, **Equipo local**.
  
3.  Abra el almacén **Certificados (equipo local)**, **Personal**, **Certificados** y busque un certificado emitido para el nombre del equipo local desde la plantilla de certificado Autenticación de cliente: equipo. Debe ver el nombre de la plantilla en el panel situado a la derecha. Es posible que deba desplazarse horizontalmente para ver la columna adecuada.
  
4.  Si el certificado que requiere no aparece en el complemento **Certificados**, ejecute GPUPDATE /force en un símbolo del sistema, espere unos minutos y, a continuación, renueve la carpeta** **Personal, Certificados.
  
    **Sugerencia:** puede reiniciar el equipo para que se realice el reintento de inscripción automática del certificado. También se puede saber si la inscripción automática de certificados se ha realizado correctamente mediante los sucesos del Registro de sucesos de aplicación que tienen como origen Inscripción automática y el Id. de suceso 19.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de la estructura de acceso de WLAN
  
Debe configurar el servidor IAS principal con opciones de directiva de acceso remoto y solicitud de conexión que determinen la autenticación y autorización de usuarios y equipos inalámbricos en la WLAN. A continuación, esta configuración se debe replicar en los demás servidores IAS; para ello, utilice el procedimiento descrito en la sección “Implementación de la configuración en varios servidores IAS” del capítulo 8, “Implementación de la infraestructura de RADIUS”. Tras ello, cada uno de los servidores IAS se debe configurar de forma exclusiva de manera que acepte conexiones desde clientes RADIUS, como puntos de acceso inalámbricos. Después, los puntos de acceso inalámbricos se deben configurar para utilizar los servidores IAS como origen de la autenticación y las cuentas de la red 802.1X.
  
#### Creación de una directiva de acceso remoto IAS para WLAN
  
Utilice el complemento Servicio de autenticación de MMC para realizar los siguientes pasos con el fin de configurar IAS con una directiva de acceso remoto para redes inalámbricas.
  
**Para crear una directiva de acceso remoto en IAS**
  
1.  Haga clic con el botón secundario del mouse en la carpeta Directivas de acceso remoto y seleccione **Crear nueva directiva de acceso remoto**.
  
2.  Dé a la directiva el nombre **Permitir acceso inalámbrico** e indique al asistente que configure **Una directiva típica para un escenario común**.
  
3.  Seleccione **Inalámbrico** como método de acceso.
  
4.  Conceda el acceso basado en grupo y utilice el grupo de seguridad Directiva de acceso remoto - Acceso inalámbrico.
  
5.  Seleccione **Tarjeta inteligente u otro certificado** como tipo de Protocolo de autenticación extensible (EAP) y, a continuación, seleccione el certificado de autenticación de servidor instalado para IAS. Finalice el asistente y ciérrelo.
  
    **Nota:** la nueva directiva** **Permitir acceso inalámbrico puede coexistir con otras directivas de acceso remoto creadas por el usuario o predeterminadas. Sin embargo, asegúrese de que las directivas de acceso remoto predeterminadas se eliminan o se enumeran después de la directiva Permitir acceso inalámbrico en la carpeta** **Directivas de acceso remoto.
  
##### Modificación de la configuración del perfil de la directiva de acceso a WLAN
  
La configuración predeterminada de la directiva de acceso remoto creada anterior se debe cambiar para omitir la configuración de acceso telefónico de usuario desde Active Directory, que podría origina problemas con determinados puntos de acceso inalámbrico. Además, se deben definir los atributos de RADIUS para la reautenticación de clientes a intervalos regulares, para garantizar que se actualizan las claves de sesión de WEP. Para obtener más información acerca de la configuración de directivas de acceso remoto, consulte el capítulo 6, “Diseño de la seguridad para LAN inalámbrica mediante 802.1X”.
  
**Para modificar la configuración del perfil de la directiva de acceso inalámbrico**
  
1.  Abra las propiedades de la directiva Permitir acceso inalámbrico y, a continuación, haga clic en **Editar perfil**.
  
2.  En la ficha **Restricciones de marcado**, seleccione la opción **Minutos que el cliente puede estar conectado (tiempo límite de sesión)** y escriba el valor **10 minutos**.
  
    **Nota:** puede utilizar un valor de tiempo de espera mayor de hasta 60 minutos, sin que haya una pérdida importante de la seguridad. Esto le permitirá una instalación que sea más resistente a las interrupciones de red temporales e impone menos carga en los servidores IAS.
  
3.  En la ficha **Avanzada**, agregue el atributo **Ignorar las propiedades de acceso telefónico del usuario**, establézcalo en **Verdadero**; a continuación, agregue el atributo **Terminación-acción** y establézcalo en **Petición de RADIUS**.
  
##### Comprobación de la directiva de petición de conexión para WLAN
  
La directiva de petición de conexión IAS predeterminada está configurada para indicar a IAS que autentique los usuarios y clientes directamente en Active Directory. Lleve a cabo los pasos siguientes para comprobar la configuración de la directiva de petición de conexión predeterminada.
  
**Para comprobar la configuración de la directiva de petición de conexión predeterminada**
  
1.  Abra el complemento Servicio de autenticación de Internet de MMC para ver las propiedades de la directiva de** **petición de conexión **Usar autenticación de Windows para todos los usuarios**.
  
2.  Compruebe que las lista de condiciones de directiva contiene **Coincidencias de fecha y hora** **“Dom 00:00-24:00; Lun 00:00-24:00; Mar 00:00-24:00; Mié 00:00-24:00; Jue 00:00-24:00; Vie 00:00-24:00; Sáb 00:00-24:00”**
  
3.  Haga clic en el botón **Editar perfil**. En la ficha **Autenticación**, asegúrese de que está seleccionado **Autenticar solicitudes en este servidor**.
  
4.  Asegúrese de que no hay reglas en la ficha **Atributo**.
  
    **Nota:** para esta solución no es necesaria ninguna otra configuración de directiva de solicitud de conexión. Sin embargo, su organización puede tener opciones adicionales configuradas para diversos escenarios.
  
Después de configurar el acceso de WLAN, cualquier cambio de configuración efectuado en el servidor IAS principal se debe replicar en los demás servidores IAS. Utilice el procedimiento descrito en la sección “Implementación de la configuración en varios servidores IAS” del capítulo 8, “Implementación de la infraestructura de RADIUS”.
  
##### Adición de clientes de RADIUS a IAS
  
Debe agregar puntos de acceso inalámbricos y servidores proxy de RADIUS como clientes de RADIUS a IAS para que puedan utilizar servicios de autenticación y cuentas a través del protocolo RADIUS. Para agregar AP a IAS, lleve a cabo los pasos siguientes en el complemento de MMC Servicio de autenticación de Internet.
  
**Para agregar clientes de RADIUS a IAS**
  
1.  Haga clic con el botón secundario del mouse en la carpeta **Clientes de RADIUS** y seleccione **Nuevo cliente de RADIUS**.
  
2.  Escriba un nombre descriptivo y la dirección IP del punto de acceso inalámbrico.
  
3.  Seleccione **Estándar de RADIUS** como atributo de cliente-proveedor y, a continuación, escriba el secreto compartido de este punto de acceso inalámbrico concreto. (Puede utilizar la secuencia de comandos GenPwd, que se describe en el siguiente procedimiento, para generar un secreto seguro.) A continuación, seleccione el atributo **La solicitud debe contener el atributo autenticador de mensaje**.
  
    **Nota:** es posible que algunos clientes RADIUS requieran la configuración de atributos específicos del proveedor (VSA) para que funcionen correctamente. Consulte la documentación del punto de acceso para obtener información acerca de los requisitos de VSA.
  
Puede utilizar la secuencia de comandos GenPwd que se incluye en esta guía para generar secretos seguros de 23 caracteres y aleatorios para uso individual de cada punto de acceso inalámbrico configurado como cliente de RADIUS. GenPwd generará criptográficamente un secreto aleatorio y lo almacenará conjuntamente con un nombre descriptivo de cada cliente RADIUS en un archivo Clients.txt. GenPwd agrega automáticamente la información a un archivo Clients.txt del directorio actual con el formato de valores separados mediante comas.
  
*No* copie este archivo en el disco duro del servidor. Guarde el archivo en un disco u otro medio extraíble y con permiso de escritura etiquetado “Clientes RADIUS para el servidor ***HQ-IAS-01***” (utilice el nombre de su servidor en vez de *HQ-IAS-01*) y almacénelo de forma segura. Este disco específico del servidor se utiliza para exportar e importar clientes de RADIUS en el capítulo 12, “Administración de la infraestructura de seguridad de RADIUS y LAN inalámbrica”.
  
**Para utilizar GenPwd para generar clientes de RADIUS en un archivo Clients.txt**
  
1.  Abra un símbolo del sistema y establezca A: como directorio actual. (Si utiliza un tipo de medio que no es un disco, utilice la letra de unidad correspondiente.) La ubicación del directorio en el sistema de archivos es importante, porque la nueva información se agregará al archivo Clients.txt del directorio predeterminado. Si no existe ningún archivo Clients.txt, se creará uno.
  
2.  Ejecute el comando siguiente. Asegúrese de cambiar *NombreCliente* por el nombre descriptivo del punto de acceso inalámbrico. Puede ser un nombre DNS u otra cadena:
  
    Cscript //job:GenPWD C:\\MSSScripts\\wl\_tools.wsf /client:*NombreCliente*
  
    **Importante:** debe guardar el disco de almacenamiento de clientes de RADIUS en un lugar seguro y accesible, por si fuera necesaria una restauración de emergencia. Una vez creado, el archivo separado mediante comas puede importarse con facilidad a una hoja de cálculo o a una aplicación de base de datos para consultarlo o editarlo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Habilitación del acceso a WLAN para usuarios y equipos
  
Los últimos pasos para la habilitación de usuarios y equipos para el acceso a WLAN segura son acciones que se deben realizar en objetos de Active Directory. Se trata de la comprobación de los permisos de las cuentas, la modificación de la pertenencia a grupos y la implementación de la configuración de directiva de grupo de WLAN. Puede realizar estas acciones de manera controlada, que se ajuste a una programación de implementación por fases y así reducir los riesgos de cambios importantes en el entorno.
  
#### Comprobación de los permisos de acceso remoto de Active Directory
  
Las cuentas de usuarios y equipos de Active Directory deben tener los permisos adecuados de acceso remoto para poder utilizar la directiva de acceso remoto. De manera predeterminada, el permiso de acceso remoto de las cuentas de un dominio de Active Directory en modo nativo se establecen en **Controlar acceso a través de la directiva de acceso remoto**;** **por lo tanto, normalmente no es necesaria ninguna modificación.
  
No obstante, puede comprobar que los usuarios y equipos de destino están configurados correctamente con el complemento Usuarios y equipos de Active Directory de MMC. Compruebe que se ha seleccionado **Controlar acceso a través de la directiva de acceso remoto** en la opción **Permiso de acceso remoto (acceso telefónico o red privada virtual)** en la ficha **Marcado** de las propiedades de la cuenta.
  
#### Adición de usuarios a grupos de directivas de acceso remoto
  
La directiva de acceso remoto de IAS utiliza los grupos de seguridad basados en Active Directory para determinar si los usuarios y equipos están autorizados a conectarse a la WLAN. Los grupos de seguridad que se han creado anteriormente en este capítulo son los que se describen en la siguiente tabla.
  
**Tabla 9.3: Grupos de seguridad de Active Directory**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Grupo de seguridad</p></th>  
<th><p>Descripción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directiva de acceso remoto: usuarios inalámbricos</p></td>
<td style="border:1px solid black;"><p>Grupo global de los usuarios que requieren acceso a la WLAN.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva de acceso remoto: equipos inalámbricos</p></td>
<td style="border:1px solid black;"><p>Grupo global de los equipos que requieren acceso a la WLAN.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directiva de acceso remoto - Acceso inalámbrico</p></td>
<td style="border:1px solid black;"><p>Grupo universal que debe contener los dos grupos globales anteriores.</p></td>
</tr>  
</tbody>  
</table>
  
Utilice el complemento Usuarios y equipos de Active Directory de MMC para agregar los grupos Directiva de acceso remoto: usuarios inalámbricos y Directiva de acceso remoto: equipos inalámbricos al grupo Directiva de acceso remoto - Acceso inalámbrico.
  
**Importante:** esta solución utiliza grupos de seguridad personalizados (Directiva de acceso remoto: usuarios inalámbricos y Directiva de acceso remoto: equipos inalámbricos) para restringir el acceso a la WLAN de usuarios y equipos. Si desea que todos los usuarios y equipos del dominio tengan acceso a la WLAN, puede incluir los grupos de usuarios y equipos del dominio en estos grupos de seguridad personalizados para simplificar el proceso de administración.
  
La estructura del grupo estará lista para rellenarse con los usuarios y equipos autorizados a tener acceso a la WLAN.
  
**Para agregar usuarios y equipos a los grupos de acceso a la WLAN**
  
1.  Abra el complemento MMC Usuarios y equipos de Active Directory.
  
2.  Agregue los usuarios con permiso de acceso a la WLAN al grupo Directiva de acceso remoto - Usuarios inalámbricos (WOODGROVEBANK\\Directiva de acceso remoto - Usuarios inalámbricos).
  
3.  Agregue los equipos con permiso de acceso a la WLAN al grupo Directiva de acceso remoto - Equipos inalámbricos (WOODGROVEBANK\\Directiva de acceso remoto - Equipos inalámbricos).
  
    **Nota:** para obtener más información acerca de la necesidad de habilitar la autenticación de usuarios y equipos en la WLAN, consulte el capítulo 6, “Diseño de seguridad para LAN inalámbrica mediante 802.1X”.
  
#### Creación de la directiva de grupo de WLAN de Active Directory
  
Puede automatizar y hacer cumplir la configuración WLAN del equipo cliente si utiliza Directiva de grupo de Windows. La MMC Directiva de grupo en Windows Server 2003 expone las opciones de **Directiva de red inalámbrica**, incluidas las relacionadas con la seguridad basada en 802.1X y los comportamientos de WLAN 802.11.
  
Para crear un perfil de Directiva de grupo de red inalámbrica de la nueva WLAN habilitada para 802.1X para los equipos cliente, lleve a cabo los pasos siguientes mediante el complemento Usuarios y equipos de Active Directory de MMC.
  
**Notas:**  
Es posible que la creación de GPO en el nivel del dominio no sea el procedimiento adecuado para todas las organizaciones. Revise la estrategia de directiva de grupo de la organización para determinar la mejor ubicación de los GPO.  
La configuración de GPO inalámbricos no se mostrará en la MMC GPO si edita el GPO desde un sistema Windows 2000 l Windows XP. Debe editarla desde un sistema Windows Server 2003 o un sistema que tenga instaladas las herramientas de administración de Windows Server 2003. Puede utilizar esta configuración de GPO en Active Directory de Windows 2000 o Windows Server 2003.
  
**Para crear una Directiva de grupo de red inalámbrica**
  
1.  Seleccione las propiedades de su objeto de dominio (como woodgrovebank.com) y, en la ficha **Directiva de grupo**, haga clic en **Nuevo** y asigne al GPO el nombre **Directiva de red inalámbrica**.
  
2.  Haga clic en el botón **Propiedades** y, en la ficha **Seguridad**, conceda al grupo de seguridad Directiva de red inalámbrica: equipo los permisos de **Lectura** y **Aplicar directiva de grupo**. Asimismo, quite el permiso **Aplicar directiva de grupo** de Usuarios autenticados en el GPO.
  
3.  En la ficha **General**, seleccione **Deshabilitar los parámetros de configuración de usuario** del objeto de directiva y haga clic en **Sí** en todos los mensajes de advertencia que aparezcan. Aplique los cambios y cierre la ventana **Propiedades** del GPO.
  
4.  Haga clic en el botón **Editar** para editar la directiva y vaya a \\Configuración de equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de red inalámbrica (IEEE 802.11).
  
5.  Seleccione el objeto **Directivas de red inalámbrica (IEEE 802.11)** en el panel de exploración y, a continuación, seleccione **Crear directiva de red inalámbrica** en el menú **Acción**. Utilice el asistente para asignar el nombre **Configuración inalámbrica de equipo cliente** a la directiva. Deje la opción **Editar propiedades** seleccionada y, a continuación, haga clic en **Finalizar** para cerrar el asistente.
  
6.  Seleccione **Agregar** en la ficha **Redes preferidas** de la directiva** **Configuración inalámbrica de equipo cliente y, a continuación, escriba el nombre de red o el Id. del conjunto de servicios (SSID) de la red inalámbrica.
  
    **Nota:** si los clientes utilizan una WLAN existente, debe elegir otro SSID para la nueva LAN inalámbrica 802.1X. Este SSID es el que se debe escribir después en el perfil de red inalámbrica de 802.1X.
  
7.  Haga clic en la ficha **IEEE 802.1x** y, a continuación, abra la configuración del tipo de EAP **Tarjeta inteligente u otro certificado**. En **Entidades emisoras raíz de confianza**, seleccione el certificado de la entidad emisora raíz para la PKI que ha emitido los certificados de servidor IAS (es decir, la PKI instalada en el capítulo 7, “Implementación de la infraestructura de claves públicas”).
  
8.  Cierre las propiedades de **Configuración inalámbrica de equipo cliente** y el Editor de objetos de directiva de grupo.
  
#### Adición de equipos a grupos de seguridad para la directiva de grupo de WLAN
  
Los grupos de seguridad basados en Active Directory se utilizan para determinar los equipos a los que se han aplicado directivas de red inalámbrica para configurar automáticamente las opciones de 802.11 y 802.1X.
  
Debe implementar la configuración de Directiva de grupo de red inalámbrica en la nueva red basada en 802.1X mucho antes de configurar los parámetros de 802.1X en los puntos de acceso inalámbricos y de activar la nueva WLAN. Con este enfoque se garantiza que los equipos cliente podrán descargar y aplicar Directiva de grupo basada en equipos, a pesar de que sólo se conecten a la LAN con cable en muy pocas ocasiones.
  
La configuración de Directiva de grupo se puede aplicar al equipo antes de que Windows instale y configure una tarjeta de interfaz de red (NIC) de WLAN. Una vez instalada una NIC de LAN, se recuperará y aplicará automáticamente la Directiva de grupo de red inalámbrica correcta.
  
**Importante:** esta solución utiliza un grupo de seguridad personalizado (Directiva de red inalámbrica: equipo) para determinar los equipos que recibirán la configuración de la WLAN. Si desea que todos los equipos reciban la configuración de la WLAN, puede incluir los grupos de usuarios autenticados o equipos del dominio a este grupo para simplificar el proceso de administración. Debe tener en cuenta que esto provocará que la configuración de directiva se aplique a todos los servidores así como a todos los equipos cliente del dominio (si utiliza Equipos del dominio) o bosque (si utiliza Usuarios autenticados).
  
**Para agregar equipos a grupos de la Directiva de grupo de red inalámbrica**
  
1.  Utilice el complemento Usuarios y equipos de Active Directory de MMC para agregar equipos al grupo Directiva de red inalámbrica: equipo.
  
2.  Asegúrese de que los sistemas se reinician antes de que intenten utilizar la WLAN. (Este paso es necesario para permitir que el equipo reciba la nueva pertenencia a grupos configurada en el paso anterior.)
  
    **Nota:** la configuración de red inalámbrica se actualizará en los equipos cliente durante el siguiente intervalo de actualización de la Directiva de grupo. Si lo desea, puede utilizar el comando  GPUPDATE /force en un símbolo del sistema para forzar la actualización de la directiva de equipo.
  
#### Comprobación de la aplicación de la Directiva de grupo de WLAN
  
Lleve a cabo los pasos siguientes desde un equipo cliente que se haya agregado al grupo de seguridad **Configuración inalámbrica de equipo cliente** de Active Directory.
  
**Nota:** los equipos deben tener un adaptador de red inalámbrica instalado y reconocido por Windows para que la directiva de red inalámbrica sea visible.
  
**Para comprobar la implementación de la configuración de red inalámbrica**
  
1.  Inicie sesión como administrador en el equipo local, haga clic en **Inicio**, **Ejecutar** y escriba el siguiente comando para abrir la carpeta Conexiones de red:
  
    ncpa.cpl
  
2.  Consulte las propiedades del icono **Conexión de red inalámbrica** que corresponda a la tarjeta inalámbrica. En la ficha **Redes inalámbricas**, debe ver el nuevo nombre de SSID de red inalámbrica en **Redes preferidas**. Seleccione la nueva configuración de red inalámbrica y haga clic en **Propiedades** para examinar las propiedades y comprobar que coincidan con las seleccionadas en la Directiva de grupo de redes inalámbricas.
  
3.  Si el nombre de SSID no aparece en **Redes preferidas** o la configuración de la red no coincide con la de la Directiva de grupo de redes inalámbricas, cierre todos los cuadros de diálogo de redes inalámbricas y ejecute GPUPDATE /force en el símbolo del sistema. Después de unos minutos, vuelva a comprobar la configuración.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de AP inalámbricos para redes 802.1X
  
El procedimiento para configurar puntos de acceso inalámbricos varía mucho según la marca y el modelo del dispositivo. Sin embargo, los proveedores de puntos de acceso inalámbricos ofrecen por lo general instrucciones para configurar el dispositivo con:
  
-   Configuración de redes de 802.1X.
  
-   Dirección IP del servidor de autenticación de RADIUS principal.
  
-   Dirección IP del servidor de cuentas de RADIUS principal.
  
-   Secreto de RADIUS compartido con el servidor de RADIUS principal.
  
-   Dirección IP del servidor de autenticación de RADIUS secundario.
  
-   Dirección IP del servidor de cuentas de RADIUS secundario.
  
-   Secreto de RADIUS compartido con el servidor de RADIUS secundario.
  
Consulte la documentación del proveedor para obtener información acerca de la configuración de los puntos de acceso inalámbricos para 802.1X.
  
Si los usuarios de su entorno utilizan actualmente puntos de acceso inalámbricos sin seguridad o sólo seguridad WEP estática, tendrá que desarrollar un plan de migración. Para obtener más información acerca de la migración desde una red inalámbrica existente, consulte el capítulo 6, “Diseño de seguridad para LAN inalámbrica mediante 802.1X”. Si bien el objetivo de esta guía no es proporcionar instrucciones de configuración de puntos de acceso inalámbricos de distintos proveedores, en el capítulo 6 también se describen temas de seguridad relacionados con los puntos de acceso inalámbricos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Pruebas y comprobación
  
Debe probar la funcionalidad de la WLAN basada en 802.1X en un equipo cliente configurado con un certificado de equipo, un certificado de usuario, directiva de grupo de red inalámbrica y una NIC de WLAN.
  
**Para probar la funcionalidad de red inalámbrica**
  
1.  Reinicie el equipo cliente que pertenece al grupo de seguridad Directiva de acceso remoto - Equipos inalámbricos.
  
2.  Inicie la sesión en el equipo como un usuario del grupo Directiva de acceso remoto - Usuarios inalámbricos.
  
3.  Desde el símbolo del sistema, utilice el comando **ping** para probar la conexión a través de la red con otro equipo de la misma.
  
Para obtener procedimientos de prueba más detallados, consulte el capítulo 13, “Cómo probar la solución”.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Si ha realizado todos los procedimientos de este capítulo, debe haber completado las siguientes tareas:
  
-   Creado y configurado grupos de seguridad de Active Directory utilizados para administrar componentes de seguridad de WLAN.
  
-   Creado las plantillas de certificado necesarias e implementado certificados inalámbricos en los servidores IAS, los equipos seleccionados y los usuarios finales seleccionados.
  
-   Creado y configurado la directiva de acceso remoto basada en IAS y la directiva de petición de conexión para redes inalámbricas.
  
-   Configurado puntos de acceso inalámbricos para 802.1X.
  
-   Creado e implementado la Directiva de grupo de red inalámbrica en equipos cliente seleccionados.
  
Después de terminar estas tareas, la infraestructura de seguridad de la WLAN basada en 802.1X debe estar totalmente operativa y preparada para reforzar la seguridad de red de su organización.
  
#### Información adicional
  
-   El artículo [“Managing Remote Access on a Per-group Basis Using Windows 2000 Remote Access Policies”](http://www.microsoft.com/windows2000/techinfo/administration/management/pgremote.asp) está disponible www.microsoft.com/windows2000/techinfo/  
    administration/management/pgremote.asp
  
-   La [documentación del producto Windows Server 2003](http://www.microsoft.com/windowsserver2003/proddoc/default.mspx) está disponible en www.microsoft.com/windowsserver2003/proddoc/default.mspx. La documentación del producto ofrece una descripción general de las características de IAS, instrucciones básicas de configuración y las mejores prácticas de implementación.
  
-   La [referencia técnica de IAS](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/techref/en-us/w2k3tr_ias_intro.asp) proporciona información técnica acerca de IAS que se puede utilizar como referencia cuando se precise más información. Está disponible en http://www.microsoft.com/resources/documentation/windowsServ/2003/all/techref/en-us/W2K3TR\_ias\_intro.asp.
  
-   El capítulo [“Implementación de una LAN inalámbrica”](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbm_wir_overview.asp) del *Kit de implementación de Microsoft Windows Server 2003* está disponible en www.microsoft.com/resources/documentation/  
    WindowsServ/2003/all/deployguide/en-us/DNSBM\_WIR\_OVERVIEW.asp.  
    Este capítulo del kit de implementación contiene instrucciones de implementación para el uso de IAS en distintos escenarios que quedan fuera del alcance de esta guía acerca de la seguridad de redes inalámbricas pero que afectan a las decisiones de diseño.
  
-   Para obtener información exhaustiva acerca de WLAN 802.1X, problemas de seguridad de WLAN y estándares relacionados, consulte la [página Web no oficial acerca de la seguridad de 802.11](http://www.drizzle.com/~aboba/ieee/) en www.drizzle.com/~aboba/IEEE/.
  
-   Para obtener información acerca de soluciones de WLAN e información del sector, visite el [sitio Web de la asociación WiFi Alliance](http://www.wi-fialliance.org/) en www.wi-fialliance.org.
  
-   Para obtener información acerca de la tecnología WLAN, con información general, estudios de mercado, notas de producto y programas de aprendizaje, visite el [centro de formación de la asociación de LAN inalámbricas (WLANA, Wireless LAN Association)](http://www.wlana.org/learning_center.html) en http://www.wlana.org/learning\_center.html.
  
-   Para obtener información acerca de EAP-TLS, EAP sobre LAN (EAPOL), EAP-RADIUS, RADIUS y otros estándares de Internet que se utilizan con 802.1X, visite el [sitio Web del grupo de trabajo de ingeniería de Internet (IETF, The Internet Engineering Task Force)](http://www.ietf.org/) en www.ietf.org/.
  
-   Los estándares de WLAN pertinentes son: 802.11, 802.11b, 802.11a, 802.11g, 802.1X, 802.11i, entre otros. Puede encontrar información acerca de estos estándares en la [zona de estándares inalámbricos del IEEE](http://standards.ieee.org/wireless/) en http://standards.ieee.org/wireless/.
  
-   Para obtener más información acerca de las tecnología WLAN 802.1X, consulte el artículo ["Windows XP Wireless Deployment Technology and Component Overview"](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wificomp.mspx) en www.microsoft.com/technet/prodtechnol/winxppro/maintain/wificomp.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
