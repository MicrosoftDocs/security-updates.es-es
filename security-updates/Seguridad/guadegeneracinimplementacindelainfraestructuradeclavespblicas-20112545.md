---
TOCTitle: 'Guía de generación: implementación de la infraestructura de claves públicas'
Title: 'Guía de generación: implementación de la infraestructura de claves públicas'
ms:assetid: '58468c19-c1db-43c3-9f2d-893d4b5bff47'
ms:contentKeyID: 20112545
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458723(v=TechNet.10)'
---

Capítulo 7: Implementación de la infraestructura de claves públicas
===================================================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#ekaa)[Introducción](#ekaa)  
[](#ejaa)[Hoja de trabajo de planeamiento de los Servicios de Certificate Server](#ejaa)  
[](#eiaa)[Creación de los servidores](#eiaa)  
[](#ehaa)[Preparación de Active Directory para la PKI](#ehaa)  
[](#egaa)[Protección de Windows Server 2003 para Servicios de Certificate Server](#egaa)  
[](#efaa)[Otras tareas de configuración de Windows](#efaa)  
[](#eeaa)[Instalación y configuración de la entidad emisora raíz](#eeaa)  
[](#edaa)[Instalación y configuración de la CA emisora](#edaa)  
[](#ecaa)[Configuración posterior a la creación](#ecaa)  
[](#ebaa)[Configuración de cliente](#ebaa)  
[](#eaaa)[Resumen](#eaaa)  

### Introducción

En este capítulo se proporcionan instrucciones detalladas para generar una infraestructura de claves públicas (PKI) basada en Servicios de Certificate Server de Microsoft® Windows Server™ 2003. El procedimiento incluye la instalación y configuración de las entidades emisoras de certificados (CA), la preparación del servicio de directorio Active Directory® y de Servicios de Internet Information Server (IIS) de Microsoft y la configuración de la directiva de certificados de cliente. Esta guía está diseñada para ayudarle a crear la infraestructura de certificados que se utilizará en los capítulos posteriores para generar una completa solución de seguridad para LAN inalámbricas.

El objetivo de este capítulo es ofrecerle instrucciones de implementación para el diseño de PKI descrito en el capítulo 4, "Diseño de la infraestructura de claves públicas". No se intentan explicar los conceptos generales de PKI ni los aspectos específicos de la implementación de Servicios de Certificate Server de Microsoft.

Este capítulo complementa los capítulos de planeamiento y operaciones de la PKI (capítulos 4 y 11, respectivamente). En el capítulo de la guía de planeamiento se explica la lógica subyacente en las decisiones de implementación empleadas en este capítulo. En el capítulo de la guía de operaciones se explican las tareas y procesos necesarios para un mantenimiento correcto de la PKI. Si todavía no lo ha hecho, es recomendable que lea los capítulos de la guía de planeamiento antes de continuar con este capítulo. También debe leer y comprender las implicaciones de los requisitos de asistencia de la guía de operaciones antes de utilizar la guía de este capítulo para implementar la PKI.

#### Requisitos previos

En esta sección se incluyen listas de comprobación que le ayudarán a establecer la preparación de su organización para implementar la PKI. ("Preparación" se emplea con un significado logístico en vez de un sentido empresarial; la motivación empresarial para implementar esta solución se trata en capítulos anteriores de la guía de planeamiento.)

##### Requisitos previos de conocimientos

Debe estar familiarizado con los conceptos de PKI y Servicios de Certificate Server de Microsoft en concreto. También se precisan conocimientos de Windows 2000 Server o de Windows Server 2003 en las siguientes áreas:

-   Instalación del sistema operativo Microsoft Windows®.

-   Conceptos de Active Directory (incluidas las estructuras y herramientas de Active Directory, manipulación de usuarios, grupos y otros objetos de Active Directory, así como el uso de la directiva de grupo).

-   Seguridad del sistema de Windows, conceptos de seguridad como usuarios, grupos y auditoría, listas de control de acceso (ACL), uso de plantillas de seguridad y aplicación de plantillas de seguridad mediante Directiva de grupo o herramientas de la línea de comandos.

-   Administración de IIS.

-   Los conocimientos de Windows Scripting Host y del lenguaje Microsoft Visual Basic® Scripting Edition (VBScript) le resultarán útiles para obtener el máximo provecho de las secuencias de comandos suministradas, pero no es esencial.

Antes de continuar con este capítulo, también debe haber leído la guía de planeamiento y disponer de un conocimiento exhaustivo de la arquitectura y el diseño de la solución.

##### Requisitos previos organizativos

Debe consultar a otros miembros de la organización que puedan tener necesidad de participar en la implementación de esta solución, como:

-   Patrocinadores empresariales.

-   Personal de seguridad y auditoría.

-   Personal de ingeniería, administración y operaciones de Active Directory.

-   Personal de ingeniería de DNS (sistema de nombres de dominio), servidor Web y redes

-   Personal de administración y operaciones

##### Requisitos previos de la infraestructura de TI

En este capítulo se supone lo siguiente en relación con la infraestructura de TI existente:

-   Existe una infraestructura de dominios de Active Directory de Windows 2000 o Windows Server 2003 implementada. Todos los usuarios de Servicios de Certificate Server de esta solución deben ser miembros de un dominio del mismo bosque de Active Directory.

    **Notas:**  
    Aunque el uso de Servicios de Certificate Server de Windows Server 2003 y Servicio de autenticación de Internet (implementación de RADIUS de IAS–Microsoft) con Windows 2000 Active Directory es totalmente compatible, esta solución no se ha probado en dicha configuración; sólo se ha probado con Active Directory de Windows 2003. No obstante, en esta guía se incluyen instrucciones para utilizar Active Directory de Windows 2000.  
    Aunque es posible implementar esta solución para varios bosques con pocas modificaciones, dicha tarea queda fuera del alcance de esta guía. Para obtener más información acerca de las implementaciones en varios bosques, consulte la nota de la sección "Información adicional" al final del capítulo.  
    Esta solución no incluye instrucciones para la integración en una PKI existente. No obstante, la solución no impide la implementación en una PKI existente.

-   Disponibilidad de hardware de servidor adecuado para ejecutar Servicios de Certificate Server de Windows Server 2003. Como parte de la guía se proporciona una configuración sugerida.

-   Esta solución no está diseñada para integrarse en una PKI existente. No obstante, la solución no impide la implementación en una PKI existente.

-   Están disponibles licencias, medios de instalación y claves de producto de Windows Server 2003 Standard Edition y Enterprise Edition.

#### Descripción general del capítulo

En la siguiente figura se muestra el proceso de crear la PKI tal como se describe en este capítulo.

![](images/Dd458723.07fig7-1(es-es,TechNet.10).gif)

**Figura 7.1 Diagrama del proceso de creación de la PKI**

Estos pasos están reflejados en la organización del capítulo y se describen en la siguiente lista. Cada uno consta de tareas de instalación o configuración. Asimismo, cada paso dispone de procedimientos de comprobación, por lo que puede comprobar que todo funciona antes de continuar con el paso siguiente.

-   **Hoja de trabajo de planeamiento de Servicios de Certificate Server**. Se enumera la información de configuración empleada en este capítulo para instalar y configurar Servicios de Certificate Server. Se incluye una tabla de información que debe proporcionar antes de empezar la implementación.

-   **Creación de los servidores**. Se describe la selección y configuración del hardware, la instalación de Windows Server 2003 y la instalación de componentes opcionales como IIS.

-   **Preparación de Active Directory para la PKI**. Se explican los requisitos previos para el dominio y el bosque de Active Directory en que se implementará la PKI, junto con los pasos de preparación esenciales. También se explica la creación de usuarios y grupos de seguridad de administración y la configuración de los permisos correctos para delegar tareas de administración.

-   **Protección de Windows Server 2003 para Servicios de Certificate Server**. Describe la implementación de seguridad en el nivel de sistema operativo mediante la aplicación de plantillas de seguridad. Las plantillas utilizadas proceden de la *Guía de seguridad de Windows Server 2003*. Consulte la sección "Información adicional" que aparece al final de este capítulo para obtener información acerca de cómo obtener esta guía.

-   **Otras tareas de configuración de Windows**. Indica algunas tareas comunes para realizar la instalación básica de los servidores.

-   **Instalación y configuración de la entidad emisora raíz**. Se describen los pasos de preparación, instalación de software y configuración de Servicios de Certificate Server, incluida la definición de funciones administrativas para el servidor. El paso final consiste en publicar el certificado de entidad emisora raíz y la lista de revocación de certificados (CRL) en Active Directory y el servidor Web.

-   **Instalación y configuración de la CA emisora**. Similar a la instrucciones de la entidad emisora raíz, pero también se incluye la obtención de un certificado de entidad emisora desde la entidad emisora raíz. El paso de comprobación final confirma que se pueden inscribir certificados de la CA emisora.

-   **Configuración posterior a la creación**. Se describe la configuración de los tipos de certificado predeterminados que emite la CA emisora, la definición de permisos para un bosque de múltiples dominios y la realización de una copia de seguridad antes de insertar las entidades emisoras en un entorno de producción.

-   **Configuración de cliente**. Se describe cómo habilitar la inscripción automática para todos los usuarios y equipos del dominio y cómo configurar directivas de confianza de certificado raíz.

[](#mainsection)[Principio de la página](#mainsection)

### Hoja de trabajo de planeamiento de los Servicios de Certificate Server

En las tablas de esta sección se indican todos los parámetros de configuración de PKI utilizados en la solución. Utilícelas como lista de comprobación cuando tome decisiones de planeamiento.

Algunos de los parámetros de estas tablas se introducen manualmente y forman parte de los procedimientos documentados en este capítulo. Otros se establecen mediante una secuencia de comandos que se ejecuta como parte de uno de los procedimientos; en otros casos, una secuencia de comandos hace referencia de algún modo al parámetro para completar una configuración o tarea operativa. En estos casos, el nombre de la secuencia de comandos relacionada se incluye en la tabla.

**Nota:** las secuencias de comandos utilizadas en este capítulo se describen más detalladamente en el apéndice A y en el archivo ToolsReadme.txt que se incluye con las mismas.

#### Elementos de configuración definidos por el usuario

En la siguiente tabla se enumeran parámetros específicos de organización tomados de la compañía ficticia Woodgrove Bank. Asegúrese de que ha recopilado, o tomado decisiones sobre valores equivalentes para su organización, todos estos elementos antes de iniciar el procedimiento de instalación. Los valores ficticios que se muestran en esta tabla se utilizan en todo el capítulo en los comandos de muestra. Debe sustituir estos valores por los adecuados para su organización. Los lugares en el texto en los que debe utilizar sus propios valores se muestran en cursiva.

**Tabla 7.1: Elementos de configuración definidos por el usuario**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Referencia a la secuencia de comandos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nombre DNS del dominio raíz del bosque de Active Directory</td>
<td style="border:1px solid black;">woodgrovebank.com</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre distintivo (DN) de raíz de bosque</td>
<td style="border:1px solid black;">DC=woodgrovebank,DC=com</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre NetBIOS (servicio básico de entrada y salida de red) del dominio</td>
<td style="border:1px solid black;">WOODGROVEBANK</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre NetBIOS de grupo de trabajo de entidad emisora raíz</td>
<td style="border:1px solid black;">WGB-Root</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre de servidor de entidad emisora raíz</td>
<td style="border:1px solid black;">HQ-CA-01</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de servidor de CA emisora</td>
<td style="border:1px solid black;">HQ-CA-02</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre común (CN) X.500 de entidad emisora raíz</td>
<td style="border:1px solid black;">Entidad emisora raíz WoodGrove Bank</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CN X.500 de CA emisora</td>
<td style="border:1px solid black;">CA emisora WoodGrove Bank 1</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre completo de host del servidor Web utilizado para publicar información acerca del certificado de entidad emisora y la revocación</td>
<td style="border:1px solid black;">www.woodgrovebank.com</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
</tbody>
</table>
  
#### Elementos de configuración recomendados por la solución
  
La configuración especificada en esta tabla no se debe cambiar en su instalación, a menos que sea necesario utilizar valores diferentes a los del diseño de la solución. Los parámetros del diseño se pueden cambiar, siempre que se sea consciente de que, al hacerlo, se dejará de utilizar la solución probada. Asegúrese de que comprende todas las implicaciones del cambio de una configuración y sus dependencias antes de alterar uno de los valores aquí y en los procedimientos de configuración y en las secuencias de comandos suministradas.
  
**Tabla 7.2: Elementos de configuración que recomienda la solución**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Referencia a la secuencia de comandos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Grupos de seguridad de función de administración</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Contenedor de configuración de los administradores de servicios de claves públicas.</td>
<td style="border:1px solid black;">Administradores de PKI de empresa</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo administrativo que puede publicar listas de revocación de certificados (CRL) y certificados de entidad emisora en el contenedor de configuración de la empresa.</td>
<td style="border:1px solid black;">Editores de PKI de empresa</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Grupo administrativo que configura y mantiene las entidades emisoras; también controla la posibilidad de asignar todas las demás funciones de entidad emisora y de renovar el certificado de entidad emisora.</td>
<td style="border:1px solid black;">Administradores de entidad emisora</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo administrativo que aprueba las solicitudes de inscripción y revocación de certificados. Ésta es una función de oficial de entidad emisora</td>
<td style="border:1px solid black;">Administradores de certificados</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Grupo administrativo que administra las auditorías y los registros de seguridad de la entidad emisora.</td>
<td style="border:1px solid black;">Auditores de entidad emisora</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo administrativo que administra las copias de seguridad de la entidad emisora.</td>
<td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
<td style="border:1px solid black;">ca_setup.wsf</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Configuración de IIS</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre del directorio virtual de Servicios de Internet Information Server (IIS) utilizado para publicar información de certificados de entidad emisora y lista CRL.</td>
<td style="border:1px solid black;">pki</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ruta de acceso física de CA emisora que se asigna al directorio virtual de IIS.</td>
<td style="border:1px solid black;">C:\CAWWWPub</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Parámetros comunes de entidad emisora</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidad y ruta de acceso para guardar los archivos de solicitud de Servicios de Certificate Server.</td>
<td style="border:1px solid black;">C:\CAConfig</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidad y ruta de acceso para guardar los registros de base de datos de Servicios de Certificate Server.</td>
<td style="border:1px solid black;">%windir%\System32\CertLog</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Configuración de entidad emisora raíz</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Longitud de clave de entidad emisora raíz
(consulte la nota que se encuentra después de la tabla).</td>
<td style="border:1px solid black;">4096</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de validez del certificado de entidad emisora raíz.</td>
<td style="border:1px solid black;">16</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Años</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período máximo de validez de los certificados emitidos por la entidad emisora raíz.</td>
<td style="border:1px solid black;">8</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Años</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Intervalo de publicación de lista CRL para la entidad emisora raíz.</td>
<td style="border:1px solid black;">6</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">meses</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de coincidencia de lista CRL (tiempo transcurrido entre la publicación de una nueva lista CRL y la fecha de caducidad de una lista CRL antigua).</td>
<td style="border:1px solid black;">10</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Días</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de publicación de diferencia entre listas CRL para entidad emisora raíz — 0 = deshabilitar diferencia entre listas CRL.</td>
<td style="border:1px solid black;">0</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Horas</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Parámetros de CA emisora</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Unidad y ruta de acceso para guardar la base de datos de Servicios de Certificate Server.</td>
<td style="border:1px solid black;">D:\CertLog</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Longitud de clave de CA emisora.</td>
<td style="border:1px solid black;">2048</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de validez del certificado de CA emisora.</td>
<td style="border:1px solid black;">8</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Años</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período máximo de validez de certificados emitidos por la CA emisora.</td>
<td style="border:1px solid black;">4</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Años</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Intervalo de publicación de lista CRL para CA emisora.</td>
<td style="border:1px solid black;">7</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Días</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de coincidencia de lista CRL (tiempo transcurrido entre la publicación de una nueva lista CRL y la fecha de caducidad de una lista CRL antigua).</td>
<td style="border:1px solid black;">4</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Días</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de publicación de diferencia entre listas CRL para CA emisora — 0 = deshabilitar diferencia entre listas CRL.</td>
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Días</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de coincidencia de diferencia entre listas CRL (tiempo transcurrido entre la publicación de una nueva diferencia entre listas CRL y la fecha de caducidad de una diferencia entre una lista CRL antigua).</td>
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Unidades del valor anterior.</td>
<td style="border:1px solid black;">Días</td>
<td style="border:1px solid black;">Pkiparams.vbs</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Varios</strong></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ruta de acceso de las secuencias de comandos de instalación.</td>
<td style="border:1px solid black;">C:\MSSScripts</td>
<td style="border:1px solid black;"> </td>
</tr>
</tbody>
</table>
  
**Importante:** la configuración de claves con una longitud de 4096 bits puede causar problemas de compatibilidad si los certificados deben emitirse o utilizarse en algunos dispositivos (como un enrutador) o software antiguo de otros proveedores que no puedan procesar claves que superen cierto tamaño. Debe probar las aplicaciones con certificados con una clave de certificado de entidad emisora raíz de este tamaño antes de implementar la PKI. Si le preocupan las longitudes de clave, reduzca el tamaño de la clave de entidad emisora raíz a 2048 bits. (Debe especificar esto en el archivo CAPolicy.inf durante la instalación de la entidad emisora raíz; consulte la sección "Instalación y configuración de la entidad emisora raíz".)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de los servidores
  
En esta sección se describen las tareas básicas de preparación del hardware de servidor e instalación del sistema operativo. Se necesitan dos servidores: uno para la entidad emisora raíz y otro para la CA emisora.
  
**Importante:** antes de empezar a crear las entidades emisoras, debe leer "Administración de la seguridad de las entidades emisoras de certificados" del capítulo 4, "Diseño de la infraestructura de claves públicas". Esto puede afectar al entorno de seguridad empleado para crear los servidores.
  
#### Selección y configuración del hardware de servidor
  
En las subsecciones siguientes se describen las especificaciones básicas de servidor para ambas funciones de entidad emisora. En el capítulo 4, "Diseño de la infraestructura de claves públicas", se examinan con más detalle algunos de los criterios clave para la selección de hardware.
  
##### Hardware de servidor de entidad emisora raíz
  
En la tabla siguiente se muestra una especificación de hardware recomendada para la entidad emisora raíz, que se basa en la recomendaciones de hardware genéricas para Windows Server 2003. No obstante, es posible que no tenga que adquirir hardware nuevo si dispone de un servidor que se ajuste a los criterios descritos en el capítulo 4 que se va a retirar por motivos de rendimiento.
  
**Tabla 7.3: Especificación de hardware sugerido para el servidor de entidad emisora raíz**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CPU</td>
<td style="border:1px solid black;">Procesador a 733 MHz o superior</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Memoria</td>
<td style="border:1px solid black;">256 MB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interfaces de red</td>
<td style="border:1px solid black;">Ninguna (o deshabilitada)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento en disco</td>
<td style="border:1px solid black;">Controlador RAID (matriz redundante de discos independientes) IDE (electrónica integrada de dispositivos) o SCSI (interfaz estándar de equipos pequeños)</br></br>  
2 x 18 GB (SCSI) o 2 x 20 GB (IDE) configurados como volumen RAID 1 (unidad C)</br></br>
Medios de almacenamiento local extraíbles (CD-RW o cinta para copia de seguridad)</br></br>
Unidad de disco de 1,44 MB para la transferencia de datos</td>
</tr>
</tbody>
</table>
 

##### Hardware de servidor de CA emisora

Aunque existen requisitos de rendimiento para la entidad emisora, no son de gran importancia ya que, normalmente, la entidad emisora realizará pocas tareas en comparación con otros tipos de servidores. En este caso se puede aplicar el mismo criterio de calidad y confiabilidad que para seleccionar hardware para el servidor de entidad emisora raíz. Existen algunas diferencias pequeñas con la especificación de entidad emisora raíz en redes y almacenamiento, tal como se muestra en la tabla siguiente:

**Tabla 7.4: Especificación de hardware sugerido para el servidor de CA emisora**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CPU</td>
<td style="border:1px solid black;">Procesador a 733 MHz o superior</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Memoria</td>
<td style="border:1px solid black;">256 MB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interfaces de red</td>
<td style="border:1px solid black;">2 tarjetas de interfaz de red (NIC) independientes, unidas para obtener mayor resistencia</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento en disco</td>
<td style="border:1px solid black;">Controlador RAID IDE o SCSI</br></br>
2 x 18 GB (SCSI) o 2 x 20-GB (IDE) configurados como volúmenes RAID 1 (unidades C y D)</br></br>
Medios de almacenamiento local extraíbles (CD-RW o cinta para copia de seguridad) si no existe un servicio de copia de seguridad de red</br></br>
Unidad de disco de 1,44 MB para la transferencia de datos</td>
</tr>
</tbody>
</table>
 

**Importante:** la especificación de servidor de esta tabla está ajustada a una población de 5.000 usuarios aproximadamente. Si tiene más usuarios, al menos debe duplicar la capacidad de disco de la unidad secundario (aproximadamente 2 GB por 1000 usuarios) y duplicar la memoria instalada. Para obtener directrices acerca del uso de disco, consulte "Determinación de los requisitos de almacenamiento y copia de seguridad para una entidad emisora" del capítulo 11, "Administración de la infraestructura de claves públicas".

##### Preparación del hardware

Complete toda la configuración de hardware de acuerdo con las recomendaciones del proveedor. Entre estas recomendaciones se puede incluir la aplicación de las actualizaciones de BIOS y firmware más recientes.

Utilice el software de administración de controlador de disco incluido con el hardware para crear los volúmenes RAID 1, tal como se explica en la tabla anterior (un volumen de disco para la entidad emisora raíz y dos volúmenes de disco para la CA emisora).

#### Preparación del servidor de entidad emisora raíz

En las tareas de esta sección se describe la instalación de Windows en el servidor que se utilizará para la entidad emisora raíz.

##### Instalación de Windows Server 2003 Standard Edition

Muchas organizaciones disponen de un proceso de instalación de servidores automatizado. Si los parámetros utilizados en esta sección se pueden incluir en el proceso de creación automatizado, es aceptable que se utilice para la creación de los servidores.

Una excepción la constituye el hecho de que la creación dependa de una conexión de red. En tal caso, debe considerar la posibilidad de realizar una creación manual, al menos en la entidad emisora raíz. Gran parte de la garantía de seguridad de una entidad emisora de certificados depende de que no esté ni haya estado conectada a una red. Esto limita considerablemente la posibilidad de que el equipo haya sufrido un ataque externo (ya que el atacante necesitaría algún tipo de acceso físico).

**Para instalar Windows Server 2003**

1.  Inicie el sistema con el CD de Windows Server 2003 Standard Edition en la unidad de CD-ROM. Compruebe que el CD-ROM se haya establecido como dispositivo de inicio en la configuración del BIOS del servidor.

2.  Cree una partición en el volumen principal, formatéela como NTFS y seleccione la opción para instalar Windows en dicha partición.

3.  Seleccione la configuración regional adecuada.

4.  Escriba el nombre y la información de la empresa en la que se va a registrar Windows.

5.  Escriba una contraseña segura para la cuenta del administrador local (con un mínimo de 10 caracteres, combinando caracteres alfabéticos en mayúsculas y minúsculas, numéricos y signos de puntuación).

6.  Cuando se le solicite, escriba el nombre del equipo, como **HQ-CA-01** (reemplace este valor por el nombre de su equipo).

    **Importante:** aunque la entidad emisora raíz no tendrá conexión, es fundamental que tenga un nombre único dentro de la organización.

7.  Cuando se le pida, seleccione unirse a un grupo de trabajo. Escriba el nombre del grupo de trabajo, ***WGB-Root*** (reemplace este valor por el nombre de grupo de trabajo de su elección).

8.  Cuando se le pida, no instale ningún componente opcional.

    El servidor se reiniciará al final del proceso de instalación principal. Siga con los pasos siguientes.

9.  Instale los Service Pack de Windows actuales (cuando se redactó este documento, acababa de empezar la fabricación de Windows Server 2003 y no había Service Pack disponibles) y las actualizaciones de seguridad recomendadas (utilice una herramienta como Microsoft Baseline Security Analyzer para determinar las actualizaciones recomendadas). También debe instalar las actualizaciones funcionales críticas (no relacionadas con la seguridad) o las actualizaciones que se necesiten como resultado de sus propias pruebas.

10. Active esta copia de Windows. La activación se debe realizar sin conexión para que el servidor no se conecte a una red en ningún momento.

##### Configuración de la red

La entidad emisora raíz no está conectada a la red. Debe deshabilitar las interfaces de red en el sistema mediante **Conexiones de red** en Panel de control para impedir que se pueda tener acceso a la entidad emisora raíz a través de la red si se conecta a la misma por error.

##### Comprobación de la instalación

Debe comprobar que la instalación del sistema operativo ha finalizado correctamente y que los parámetros configurados son los esperados.

**Para ver la configuración del sistema actual**

1.  Ejecute el programa systeminfo en un símbolo del sistema.

2.  Compruebe los siguientes elementos de información del sistema. Se han omitido otros detalles para una mayor brevedad y se indican con "..." (puntos suspensivos):

    Nombre de host: HQ-CA-01

    Nombre del sistema operativo: Microsoft® Windows® Server 2003, Standard Edition

    ...

    Configuración del sistema operativo: Servidor independiente

    Propiedad de: *SuNombre*

    Organización registrada: *NombreDeLaOrganización*

    ...

    Directorio de Windows: C:\\WINDOWS

    Directorio del sistema: C:\\WINDOWS\\System32

    Dispositivo de inicio: \\Device\\HarddiskVolume1

    Configuración regional del sistema: *ConfiguraciónRegionalDelSistema*

    Idioma: *SuIdioma*

    Zona horaria: *SuZonaHoraria*

    ...

    Dominio: WGB-Root

    Servidor de inicio de sesión: \\\\HQ-CA-01

    Revisión(es): X revisión(es) instaladas.
    
    [01]: Qxxxxxx
        
    ...
    
    [nn]: Qnnnnnn

    Tarjeta(s) de red: N/A

3.  Si estos valores no son los que esperaba, debe volver a configurar el servidor mediante el Panel de control o volver a realizar la instalación.

#### Preparación del servidor de CA emisora

En las tareas de esta sección se describe la instalación de Windows en el servidor que se utilizará para la entidad emisora.

##### Instalación de Windows Server 2003 Enterprise Edition

Siga el proceso para crear el servidor de entidad emisora raíz con las excepciones siguientes.

A diferencia de la entidad emisora raíz, si es necesario, puede crear el servidor de entidad emisora mediante un método de creación basado en red. No obstante, debe adoptar precauciones razonables para asegurarse de que la entidad emisora no se expone a amenazas de seguridad. Por ejemplo, debe instalarla en una red aislada sin ruta que se pueda enrutar a Internet o a la red principal de la organización. No olvide que antes de instalar las últimas actualizaciones de seguridad, el sistema puede ser vulnerable a las amenazas procedentes de la red.

**Para instalar Windows Server 2003 Enterprise Edition**

1.  Siga los pasos 1 a 5 para instalar el sistema operativo Windows en la entidad emisora raíz, con la diferencia de que se utilizará la versión Enterprise Edition de Windows Server 2003 en vez de Standard Edition.

2.  Cuando se le solicite, escriba el nombre del equipo, como **HQ-CA-02** (reemplace este valor por el nombre de su equipo).

3.  Cuando se le pida, seleccione la opción para unirse a un dominio. Escriba el nombre del dominio de Active Directory al que se van a unir los servidores, como *WOODGROVEBANK* (reemplace este valor por el nombre del dominio en que va a instalar la entidad emisora). Cuando se le pida, escriba las credenciales del usuario que está autorizado para unir equipos a este dominio.

    **Nota:** para un bosque de varios dominios, los servidores de certificados normalmente se instalan en el dominio raíz del bosque; aunque no es fundamental, así se supone en esta solución.

4.  No instale ningún componente opcional.

    El servidor se reiniciará al final del proceso de instalación principal. Siga con los pasos siguientes.

5.  Instale los Service Packs actuales y las revisiones requeridas, de la misma forma que para la entidad emisora raíz.

6.  Cree una partición en el segundo volumen del disco duro, asígnele la letra de unidad D y dele formato con NTFS.

7.  Cree una carpeta en la unidad D: con el nombre D:\\CertLog.

8.  Active esta copia de Windows. La activación se debe realizar sin conexión para no exponer el servidor a Internet de ninguna forma.

##### Configuración de la red

La CA emisora tiene una única interfaz de red (aunque se puede implementar uniendo dos tarjetas de red físicas para obtener una mayor resistencia). La interfaz de red se debe configurar con una dirección fija del Protocolo de Internet (IP) y otros parámetros de configuración de IP (puerta de enlace predeterminada, configuración de DNS, etc.), tal como corresponda a la red.

Por motivos de seguridad, debe bloquear toda conectividad de entrada o salida entre la CA emisora e Internet. Incluso la concesión de acceso de sólo salida puede hacer que los virus u otro software malintencionado sean mucho más peligrosos. Por ejemplo, les permitiría descargar código adicional de Internet o robar y transportar el material de claves privadas de entidad emisora fuera de la organización.

##### Comprobación de la instalación

Debe comprobar que la instalación del sistema operativo ha finalizado correctamente y que los parámetros configurados son los esperados.

**Para ver la configuración del sistema actual**

1.  Ejecute el programa systeminfo en un símbolo del sistema.

2.  Compruebe los elementos siguientes del resultado de la información del sistema (se han omitido algunos detalles del resultado en aras de la brevedad):

    Nombre de host: HQ-CA-02

    Nombre del sistema operativo: Microsoft® Windows® Server 2003, Enterprise Edition

    ...

    Configuración del sistema operativo: Servidor miembro

    Propiedad de: *SuNombre*

    Organización registrada: *NombreDeLaOrganización*

    ...

    Directorio de Windows: C:\\WINDOWS

    Directorio del sistema: C:\\WINDOWS\\System32

    Dispositivo de inicio: \\Device\\HarddiskVolume1

    Configuración regional del sistema: ConfiguraciónRegionalDelSistema

    Idioma: SuIdioma

    Zona horaria: SuZonaHoraria

    ...

    Dominio: woodgrovebank.com

    Servidor de inicio de sesión: \\\\NombreDelControladorDeDominio

    Revisión(es): X revisión(es) instaladas.
    
    [01]: Qxxxxxx
            
    ...
    
    [nn]: Qnnnnnn

    Tarjeta(s) de red: 1 Tarjetas de interfaz de red instaladas.

    \[01\]: ModeloYProveedorDeTarjetaDeRed

    Nombre de conexión: Conexión de área local

    DHCP habilitado: No

    Direcciones IP

    [01]: 10.1.1.11

3.  Si estos valores no son los que esperaba, debe volver a configurar el servidor mediante el Panel de control o volver a realizar la instalación.

#### Instalación de secuencias de comandos de configuración en los servidores

Con la solución se proporciona una serie de secuencias de comandos y archivos de configuración auxiliares que ayudan a simplificar algunos aspectos de su configuración y funcionamiento. Debe instalarlos en todos los servidores de entidad emisora. Algunas de estas secuencias de comandos se necesitan para realizar las operaciones descritas en los capítulos de la guía de operaciones, de modo que no debe eliminarlas una vez finalizada la instalación de la entidad emisora.

**Para instalar las secuencias de comandos de instalación en todos los servidores**

1.  Cree una carpeta llamada C:\\MSSScripts.

2.  Copie las secuencias de comandos del medio de distribución en esta carpeta.

#### Instalación y configuración de Servicios de Internet Information Server

Esta sección describe la instalación y configuración de Servicios de Internet Information Server (IIS) en la CA emisora. IIS se utiliza para proporcionar puntos de descarga de listas CRL y certificados de entidad emisora para clientes que no utilicen Windows. Se recomienda no instalar IIS en la entidad emisora raíz. Aunque puede instalar IIS en la CA emisora, un enfoque más seguro lo constituye el alojamiento de los puntos de descarga Web para el certificado y la lista CRL de la entidad emisora en un servidor distinto de la propia entidad emisora. Es probable que exista un gran número de usuarios de certificados (internos y externos) que necesiten recuperar información de las listas CRL o la cadena de CA y no dispongan de permiso de acceso a la entidad emisora. Esta restricción de acceso no se podrá conseguir si los puntos de descarga se alojan en la propia entidad emisora de certificados.

**Importante:** para simplificar la guía de esta solución, el servidor de la CA emisora se utiliza para alojar el servidor Web y los puntos de descarga de las listas CRL y los certificados de entidad emisora. No obstante, se recomienda que utilice un servidor Web independiente en el propio entorno para mejorar la seguridad de las entidades emisoras de certificados. Los pasos descritos aquí se pueden utilizar para instalar y configurar IIS en la CA emisora o en un servidor independiente.

IIS también puede alojar las páginas de inscripción Web de Servicios de Certificate Server, aunque no se utilizan en esta solución. Si instala las páginas de inscripción Web en un servidor distinto de la entidad emisora, debe marcar este servidor como "Se confía para delegación" configurando esta propiedad en el objeto de equipo del servidor en Active Directory.

##### Instalación de Servicios de Internet Information Server en la CA emisora

IIS se instala con el administrador de componentes opcionales de Windows (al que se puede tener acceso mediante **Agregar o quitar componentes** del Panel de control). En la tabla siguiente se enumeran los componentes que se deben instalar. La sangría refleja la relación jerárquica entre los componentes, como se verían en el asistente del administrador de componentes opcionales (**Habilitar el acceso de red COM+** es un subcomponente de **Servidor de aplicaciones** de Microsoft, por ejemplo). Los componentes que no están seleccionados no se muestran en la tabla.

**Tabla 7.5: Componentes opcionales que deben instalarse**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Componente</th>
<th style="border:1px solid black;" >Estado de instalación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servidor de aplicaciones</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">      Habilitar el acceso de red COM+</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">      Servicios de Internet Information Server</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">            Archivos comunes</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">            Administrador de servicios de Internet Information Server</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">            Servicio World Wide Web</td>
<td style="border:1px solid black;">Seleccionado</td>
</tr>
</tbody>
</table>
  
**Para instalar IIS**
  
1.  Ejecute el siguiente comando en el símbolo del sistema:
  
    sysocmgr /i:sysoc.inf /u:C:\\MSSScripts\\OC\_AddIIS.txt
  
    Este comando indica al administrador de componentes adicionales que utilice las configuraciones de componentes especificada en el archivo de instalación desatendida C:\\MSSScripts\\OC\_AddIIS.txt:
  
    ```
    [Components]
    complusnetwork = On
    iis_common = On
    iis_asp = On
    iis_inetmgr = On
    iis_www = On
    ```
  
    **Nota:** esta configuración habilita las Páginas Active Server en la línea iis\_asp = on. Esta opción es necesaria para admitir la extensión de la solución con páginas de inscripción Web de Servicios de Certificate Server pero no para la solución principal. Debe considerar deshabilitar ASP (eliminar la línea iis\_asp = on antes de ejecutar sysocmgr.exe) si no necesita las páginas de inscripción Web. Si es necesario, puede habilitar esta configuración más adelante.
  
2.  Ejecute el administrador de componentes opcionales de nuevo del siguiente modo y compruebe que los componentes instalados coincidan con los de la tabla anterior.
  
    sysocmgr /i:sysoc.inf
  
    No se requiere ningún otro subcomponente del **servidor de aplicaciones** y, por lo tanto, no es necesario seleccionarlo.
  
##### Configuración de IIS para el Acceso a la información de entidad emisora (AIA) y la publicación de Puntos de distribución de CRL (CDP) en la CA emisora
  
Debe crear un directorio virtual en IIS para utilizarlo como ubicación del protocolo de transferencia de hipertexto (HTTP) para los puntos de publicación de certificados y listas CRL de entidad emisora (denominados AIA y CDP, respectivamente).
  
**Para crear un directorio virtual en IIS**
  
1.  Inicie sesión en el servidor IIS (CA emisora) con privilegios de administrador local.
  
2.  Cree la carpeta C:\\CAWWWPub que contendrá certificados de entidad emisora y listas CRL.
  
3.  Establezca la seguridad en la carpeta con el Explorador de Windows; en la tabla siguiente se muestran los permisos que se deben aplicar. Los cuatro primeros ya deben aparecer.
  
    **Tabla 7.6: Permisos de directorio virtual**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Usuario/grupo</th>
    <th style="border:1px solid black;" >Permiso</th>
    <th style="border:1px solid black;" >Permitir o denegar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Administradores</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Sistema</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Propietarios del creador</td>
    <td style="border:1px solid black;">Control total (sólo subcarpetas y archivos)</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Usuarios</td>
    <td style="border:1px solid black;">Leer
    Listar el contenido de la carpeta</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">IIS_WPG</td>
    <td style="border:1px solid black;">Leer
    Listar el contenido de la carpeta</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Cuenta de invitado para Internet</td>
    <td style="border:1px solid black;">Escritura</td>
    <td style="border:1px solid black;">Denegar</td>
    </tr>
    </tbody>
    </table>
  
4.  En la consola de administración de Servicios de Internet Information Server cree un nuevo directorio virtual en el siguiente sitio Web predeterminado:
  
    -   Escriba el nombre *pki* para el directorio virtual.
  
    -   Especifique *C:\\CAWWWPub* como ruta de acceso.
  
5.  Borre la opción **Ejecutar secuencias de comandos (por ejemplo, ASP)** en los permisos de acceso al directorio virtual.
  
6.  Compruebe que la autenticación anónima esté habilitada para el directorio virtual.
  
##### Elección de un alias DNS para el punto de publicación HTTP
  
Debe crear un alias DNS genérico (CNAME) que se resuelva en el servidor IIS que aloja CDP y AIA; por ejemplo, www.woodgrovebank.com. Este alias DNS se debe utilizar al configurar las rutas de acceso de CDP y AIA para las entidades emisoras en las secciones posteriores. Con este alias se pueden mover fácilmente los puntos de publicación de entidad emisora a otro servidor o ubicación de red en el futuro sin tener que volver a emitir los certificados de entidad emisora.
  
##### Comprobación de la instalación de IIS
  
Debe comprobar el funcionamiento básico de IIS antes de continuar. Si se produce un error en alguna de las pruebas siguientes, debe comprobar de nuevo la instalación y configuración de IIS de los pasos anteriores de esta sección.
  
**Para comprobar el funcionamiento del directorio virtual de IIS**
  
1.  Inicie sesión en el servidor IIS (CA emisora) como miembro del grupo de administradores locales y cree un archivo con un editor de texto como Bloc de notas. Escriba algún texto reconocible (no importa lo que sea y no requiere etiquetas HTML). Por ejemplo:
  
    Hola a todos
  
2.  Guarde el archivo como **test.htm** en la carpeta que creó para publicar la información de CDP y AIA en los pasos anteriores: C:\\CAWWWPub. Guarde el mismo archivo como **test.asp** en la misma carpeta.
  
3.  Abra un explorador y escriba la dirección URL para intentar recuperar las páginas:
  
    http://*www.woodgrovebank.com*/pki/test.htm
  
    **Nota:** si todavía no ha configurado este alias en DNS, puede especificarlo temporalmente en el archivo de hosts locales (%systemroot%\\system32\\drivers\\etc\\hosts) en la dirección IP del servidor IIS. También puede utilizar el nombre de host real del servidor IIS en lugar del alias. Sin embargo, tenga en cuenta que deberá comprobar el funcionamiento correcto del alias DNS más adelante.
  
4.  Debe ver el texto "Hola a todos" (o lo que haya escrito en el paso 1) mostrado en el explorador.
  
**Para comprobar que se ha deshabilitado el permiso de ejecución**
  
1.  Abra un explorador y escriba la dirección URL siguiente para intentar recuperar las páginas:
  
    http://*www.woodgrovebank.com*/pki/test.asp
  
2.  En el explorador se debe mostrar el siguiente mensaje de error (o uno similar):
  
    **No se puede mostrar la página**
  
    Ha intentado ejecutar CGI, ISAPI u otro programa ejecutable de un directorio que no permite ejecutar programas.
  
    También se debe mostrar el siguiente código de error:
  
    HTTP Error 403.1 - Prohibido: permiso de ejecución denegado.
  
    Servicios de Internet Information Server (IIS)
  
Tiene que asegurarse de que se ha habilitado el acceso anónimo al sitio. Dado que Microsoft Internet Explorer intentará autenticar automáticamente y en silencio a los usuarios de un sitio Web, en ocasiones resulta difícil determinar si se ha utilizado un acceso anónimo en vez de uno autenticado. Un método consiste en cambiar la configuración de la zona de seguridad de Internet Explorer para forzar la utilización del acceso anónimo y repetir las pruebas anteriores. Como alternativa, puede realizar el procedimiento siguiente, que utiliza telnet.exe para exigir el acceso no autenticado. En este procedimiento se supone que se va a probar el sitio Web desde el propio servidor IIS; no funciona a través de un servidor proxy.
  
**Para comprobar que se ha habilitado el acceso anónimo**
  
1.  Ejecute el programa telnet en un símbolo del sistema.
  
2.  Cuando se le pida, escriba el comando siguiente para activar la visualización local de los caracteres escritos:
  
    set localecho
  
3.  Escriba el comando para conectar con IIS mediante el alias DNS definido anterior:
  
    open *www.woodgrovebank.com* 80
  
4.  Escriba el texto siguiente (exactamente como se muestra, incluidas mayúsculas y minúsculas) para recuperar la página test.htm:
  
    GET /pki/test.htm
  
    **Nota:** el cursor habrá vuelto a la parte superior de la página, lo que significa que el texto escrito sobrescribirá el texto de la pantalla. Por este motivo, la visualización se mostrará ligeramente borrosa. Puede pasar por alto este hecho sin problemas.  
    Si comete algún error al escribir, presione ENTRAR y, a continuación, escriba el comando **open** (como en el paso 3) de nuevo para volver a conectar y reintentar el comando **GET**.
  
5.  Verá la siguiente información:
  
    Hola a todos
  
    Connection to host lost.
  
    Press any key to continue...
  
6.  Escriba **quit** para salir de telnet.
  
Si las tres pruebas de esta sección han finalizado correctamente, elimine los archivos test.htm y test.asp de la carpeta del servidor Web.
  
#### Instalación y configuración de componentes de sistema operativo adicionales
  
En esta sección se describe la instalación y configuración de los demás componentes que necesite el servidor. Debe seguir estos procedimientos para los servidores de entidad emisora raíz y CA emisora.
  
##### Eliminación del servicio Actualización de certificados raíz
  
Debe quitar el servicio Actualización de certificados raíz. Éste es un componente opcional que se instala de forma predeterminada. No es recomendable que la confianza de raíz de las entidades emisoras se actualice automáticamente. En cualquier caso, el servicio no funcionará si no puede tener acceso a Internet y registrará errores en el registro de sucesos. Evidentemente, la entidad emisora sin conexión no tendrá acceso de red, pero también debe bloquear cualquier tipo de conectividad de entrada o salida entre la CA emisora e Internet, tal como se ha explicado anteriormente.
  
**Para quitar el servicio Actualización de certificados raíz.**
  
-   Ejecute el siguiente comando en el símbolo del sistema:
  
    sysocmgr /i:sysoc.inf /u:C:\\MSSScripts\\OC\_RemoveRootUpdate.txt
  
Este comando configura el administrador de componentes opcionales para utilizar la configuración de componentes especificada en el siguiente archivo C:\\MSSScripts\\OC\_ RemoveRootUpdate.txt:
  
```
[Components]
rootautoupdate = Off
```
#### Comprobación de los Service Pack y las actualizaciones de seguridad
  
Debe volver a comprobar el Service Pack y la lista de actualizaciones instaladas en este punto (ya que es posible que se hayan instalado componentes adicionales como IIS). Utilice una herramienta como Microsoft Baseline Security Analyzer (MBSA) para realizar la comprobación, obtener las actualizaciones requeridas y, después de las pruebas adecuadas, instalarlas en el servidor.
  
Para obtener instrucciones acerca de cómo utilizar MBSA, consulte el vínculo correspondiente de la sección "Información adicional", al final de este capítulo.
  
**Nota:** tendrá que descargar por separado la lista de actualizaciones de seguridad de Microsoft actual, mssecure.xml, para poder ejecutar MBSA sin conexión. Esto se describe en la documentación y en el vínculo de MBSA.
  
#### Instalación de software adicional
  
En esta sección se describe la instalación de software adicional requerido en las entidades emisoras.
  
##### CAPICOM
  
Se necesita CAPICOM 2.0 (en realidad la versión actual es 2.0.0.3) en la entidad emisora raíz y la CA emisora para algunas de las secuencias de comandos de instalación y administración proporcionadas con esta solución. Para obtener información acerca de dónde encontrar la versión más reciente de CAPICOM, consulte la sección "Información adicional" al final de este capítulo.
  
Siga las instrucciones del archivo ejecutable autoextraíble para instalar y registrar la biblioteca de vínculos dinámicos (DLL) CAPICOM.
  
##### Herramientas de soporte técnico de Windows Server 2003
  
Aunque no es estrictamente necesario, resulta de gran ayuda tener las herramientas de soporte de Windows 2000 instaladas en el servidor de la CA emisora. Muchas de las herramientas resultan útiles para algunas operaciones de la entidad emisora y otras, para la solución de problemas. Puede instalar las herramientas de soporte desde el CD de instalación de Windows (Suptools.msi en Support\\Tools).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación de Active Directory para la PKI
  
En esta sección se describe cómo preparar Active Directory para la instalación de Servicios de Certificate Server de Windows Server 2003.
  
#### Preparación del esquema de Active Directory
  
Existen algunos requisitos fundamentales en la infraestructura de dominios de Active Directory para esta solución. Estos requisitos varían en función de si se instala la solución en un entorno de Active Directory de Windows 2000 o en uno actualizado a (o instalado inicialmente con) Active Directory de Windows Server 2003.
  
##### Requisitos para todas las versiones de Active Directory
  
Esta solución requiere un nivel funcional de dominio mínimo de modo nativo de Windows 2000, al menos para el dominio en que están instalados los servidores de entidad emisora de certificados. Este requisito es necesario porque la solución utiliza grupos universales de Active Directory, que primero están disponibles en modo nativo de Windows 2000. Si el dominio no cumple este requisito, tiene que cambiarlo según las instrucciones de la documentación del producto (consulte la sección "Información adicional" al final de este capítulo).
  
**Nota:** el nivel funcional de dominio predeterminado de Active Directory siempre es el modo mixto, aunque se haya instalado sólo mediante controladores de dominio de Active Directory de Windows 2003. Debe aumentar este nivel antes de continuar. Si no puede aumentar el nivel de dominio del modo mixto porque necesita admitir controladores de dominio de Microsoft Windows NT® versión 4.0, tendrá que crear manualmente grupos globales de dominio en lugar de grupos universales.
  
En la solución se supone un bosque de Active Directory con el nivel de funcionalidad de bosque predeterminado de Windows 2000, como mínimo. No es necesario cambiarlo. Para obtener información adicional acerca de estos conceptos, consulte la referencia al final de este capítulo.
  
##### Instalación en un dominio de Windows 2000
  
**Importante:** aunque Microsoft admite la instalación y el uso de Servicios de Certificate Server de Windows Server 2003 en un dominio que utilice controladores de dominio de Windows 2000, esta solución no se ha probado exhaustivamente con dicha combinación.
  
Si la solución se va a instalar en un bosque de Active Directory de Windows 2000, debe actualizar el esquema de directorio para la instalación de Servicios de Certificate Server de Windows 2003 para que funcione correctamente. También debe asegurarse de que todos los controladores de dominio de Windows 2000 tienen aplicado Service Pack 3 (o posterior). El Service Pack se requiere para que la herramienta de actualización de esquema funcione correctamente y para que los controladores de dominio admitan la firma LDAP (Protocolo ligero de acceso a directorios). La firma LDAP es una mejora de seguridad que requieren las entidades emisoras de Windows Server 2003 y los clientes de Windows XP que utilicen la inscripción automática de certificados.
  
Muchas de las funciones de Servicios de Certificate Server de Windows 2003 (como la inscripción automática de usuarios y las plantillas editables) requieren la versión de esquema de Active Directory de Windows Server 2003. No obstante, este requisito no significa que alguno o todos los controladores de dominio deban ejecutar Windows Server 2003. Lo que sucede es que Servicios de Certificate Server de Windows Server 2003 requiere extensiones de esquema que no están presentes en el esquema de Active Directory de Windows 2000. Puede actualizar el esquema de directorio mediante la herramienta ADPrep.exe, que está disponible en la carpeta i386 del medio de distribución de Windows Server 2003.
  
Para utilizar Adprep, debe haber aplicado Service Pack 3 a los controladores de dominio de Windows 2000 (Adprep funcionará con Service Pack 1, más algunas actualizaciones posteriores, aunque, dado que se necesita SP3 de todos modos, esto no es especialmente relevante). No intente utilizar la herramienta sin asegurarse de que todos los controladores de dominio tienen el nivel correcto de revisiones.
  
**Advertencia:** el uso de esta herramienta provoca un cambio irreversible en el esquema de directorio. Aunque el procedimiento es seguro, cerciórese de leer la documentación relacionada exhaustivamente antes de comenzar.
  
En el controlador de dominio principal del esquema del bosque, ejecute el comando siguiente:
  
ADPrep /ForestPrep
  
Para realizar esta tarea, debe ser un miembro del grupo de administradores de esquema o solicitar que un administrador con los permisos correctos realice este cambio por su parte.
  
Para obtener más información acerca de la herramienta ADPrep, consulte la referencia al final de este capítulo.
  
##### Comprobación de la preparación de Active Directory
  
Puede comprobar el nivel funcional de dominio y la versión de esquema con los pasos siguientes.
  
**Para comprobar el nivel funcional de dominio**
  
1.  Abra Usuarios y equipos de Active Directory.
  
2.  Lea las propiedades del objeto de dominio.
  
3.  En la ficha **General**, el **nivel funcional del dominio** debe aparecer como uno de los siguientes:
  
    -   Windows 2000 nativo
  
    -   Windows Server 2003
  
**Para comprobar la versión de esquema**
  
1.  En el símbolo del sistema, escriba lo siguiente (asegúrese de sustituir el DN de su dominio raíz del bosque):
  
    dsquery \* "cn=schema,cn=configuration, *DC=woodgrovebank,DC=com*" -scope base -attr objectversion
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
    **Nota:** tendrá que ejecutar este comando desde un servidor Windows 2003. Dsquery.exe no se encuentra disponible en Windows XP o Windows 2000 de forma predeterminada.
  
2.  El resultado debe mostrar una versión de esquema de 30 (o superior), como se muestra a continuación:
  
      objectversion
  
      30
  
#### Grupos y usuarios de Active Directory
  
En esta sección se describe la creación de los grupos de seguridad y cuentas de usuario de Active Directory que utilizan las entidades emisoras.
  
##### Creación de grupos de administración de entidades emisoras y PKI
  
Las funciones y capacidades administrativas se definen mediante cuentas de usuario de dominio y grupos de seguridad.
  
**Nota:** esta solución define varios grupos de seguridad correspondientes a funciones administrativas distintas. Este enfoque proporciona un gran control sobre la delegación de responsabilidades para la administración de entidades emisoras. Sin embargo, no debe pensar que *tiene que* usar todas o algunas de estas funciones si no se corresponden con el modelo administrativo que utiliza. Si sólo tiene un administrador de PKI que se encarga de todos los aspectos del servicio, puede agregar esta cuenta a todos los grupos de funciones de la entidad emisora. En la práctica, la mayoría de las organizaciones utilizan la separación de funciones, pero sólo unas pocas utilizan todas las capacidades de separación funciones de Servicios de Certificate Server.
  
**Para crear grupos de administración de entidades emisoras en el dominio**
  
1.  Inicie la sesión en un equipo miembro del dominio con una cuenta que disponga de permisos suficientes para crear objetos de usuario y de grupo en el contenedor de usuarios.
  
2.  Ejecute el comando siguiente para crear el grupo de administración de entidades emisoras de dominio:
  
    Cscript //job:CertDomainGroups C:\\MSSScripts\\ca\_setup.wsf
  
Esta secuencia de comandos crea los grupos de seguridad que se enumeran en la tabla siguiente. Los grupos se crean como grupos universales en el contenedor Usuarios y, a continuación, deben trasladarse a una unidad organizativa (UO) más adecuada. (En una sección posterior se muestra una ilustración de una estructura de UO adecuada.)
  
**Precaución:** esta secuencia de comandos crea grupos de seguridad a los que se asigna un gran poder en el bosque de Active Directory. Debe tener mucho cuidado al asignar miembros a estos grupos. Específicamente:
  
**Administradores de PKI de empresa**. Se trata de un grupo con un gran poder. Tendrá control completo sobre la PKI en todo el bosque de Active Directory, incluida la capacidad de instalar y reemplazar entidades emisoras raíz y de empresa, cambiar confianzas de raíz e instalar certificados cruzados. Trátelo con la misma precaución empleada para el grupo Administradores de organización.
  
**Editores de PKI de empresa**. Aunque suene inocuo, este grupo también dispone de capacidades eficaces. Tendrá la capacidad de instalar y quitar entidades emisoras raíz y certificados cruzados de todo el bosque. Aunque no tiene tanto poder como Administradores de empresa, se debe tratar con cuidado.
  
**Tabla 7.7: Nombres y finalidades de los grupos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de grupo</th>
<th style="border:1px solid black;" >Finalidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administradores de PKI de empresa</td>
<td style="border:1px solid black;">Contenedor de configuración de los administradores de servicios de claves públicas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Editores de PKI de empresa</td>
<td style="border:1px solid black;">Pueden publicar listas CRL y certificados de entidad emisora en el contenedor de configuración de la empresa</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administradores de entidad emisora</td>
<td style="border:1px solid black;">Tienen capacidades de administración total para la CA, incluida la determinación de la propiedad de otras funciones</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administradores de certificados</td>
<td style="border:1px solid black;">Administran la emisión y revocación de certificados</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditores de entidad emisora</td>
<td style="border:1px solid black;">Administran los datos de auditoría de la CA</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
<td style="border:1px solid black;">Tienen permisos de copia de seguridad y restauración de claves y datos de la CA</td>
</tr>
</tbody>
</table>
  
**Notas:**  
Si requiere administradores de entidades emisoras, administradores de certificados, auditores y operadores de copia de seguridad distintos para cada entidad emisora de certificados de empresa, debe crear grupos de dominio distintos para cada entidad emisora, en lugar de grupos únicos para toda la empresa, como se muestra aquí. Asígneles nombres como Administradores de CA *NombreCA* o similares.  
La mayoría de estos grupos de dominio tienen grupos locales equivalentes creados en entidades emisoras sin conexión.  
El grupo local Administradores del servidor de entidad emisora también desempeña una función importante en la administración de una entidad emisora. Este grupo existe en servidores Windows de forma predeterminada.  
Para un bosque de varios dominios, debe crear estos grupos en el mismo dominio que los servidores de certificados; en el resto de esta guía se supone que se utiliza este enfoque. (Debido a que se trata de grupos universales, puede utilizarlos para administrar entidades emisoras instaladas en cualquier dominio de bosque.)
  
##### Creación de usuarios de prueba de administración de entidades emisoras y PKI
  
A modo de prueba e ilustración, la secuencia de comandos de esta sección crea cuentas de usuario genérico que corresponden a cada una de las funciones definidas por los grupos de administración creados anteriormente. Sin embargo, si las cuentas que se utilizarán ya existen en este punto o se han definido y puede crearlas, debe omitir este paso y utilizar dichas cuentas.
  
**Para crear cuentas de usuario de administración de entidad emisora de prueba**
  
1.  Inicie la sesión en un equipo miembro del dominio con una cuenta que disponga de permisos suficientes para crear objetos de usuario y de grupo en el contenedor de usuarios.
  
2.  Cree cuentas de usuario de dominio para las personas que administrarán la entidad emisora ejecutando la secuencia de comandos siguiente:
  
    Cscript //job:CertDomainTestAccts C:\\MSSScripts\\ca\_setup.wsf
  
    La secuencia de comandos define contraseñas aleatorias en todas las cuentas (en lugar de dejarlas con contraseñas en blanco). Anótelas a partir del resultado de la secuencia de comandos o sustituya las contraseñas asignadas automáticamente por otras de su elección.
  
    **Precaución:** el uso de cuentas genéricas como éstas, con contraseñas compartidas entre administradores, hace que la auditoría prácticamente no se pueda realizar. En cualquier caso distinto de un entorno de pruebas, siempre debe utilizar cuentas que pueda relacionar con alguna persona.
  
La secuencia de comandos crea las cuentas de dominio que se describen en la tabla siguiente. La secuencia de comandos crea usuarios en el contenedor Usuarios, que debe trasladar a una UO más adecuada. (En una sección se proporciona una ilustración al respecto.)
  
**Tabla 7.8: Nombres y finalidades de las cuentas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cuenta de usuario</th>
<th style="border:1px solid black;" >Finalidad de la cuenta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">EntPKIAdmin</td>
<td style="border:1px solid black;">Contenedor de configuración de administrador de servicios de claves públicas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">EntPKIPub</td>
<td style="border:1px solid black;">Pueden publicar listas CRL y certificados de entidad emisora en el contenedor de configuración de la empresa</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CAAdmin</td>
<td style="border:1px solid black;">Tiene capacidades de administración total para la CA, incluida la determinación de la propiedad de otras funciones</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CertManager</td>
<td style="border:1px solid black;">Administra la emisión y revocación de certificados</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CAAuditor</td>
<td style="border:1px solid black;">Administra los datos de auditoría de la CA</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CABackup</td>
<td style="border:1px solid black;">Tiene permisos de copia de seguridad y restauración de claves y datos de la CA</td>
</tr>
</tbody>
</table>
  
**Nota:** las cuentas de prueba ilustran la configuración más compleja de funciones administrativas, en la que cada función de entidad emisora corresponde a una persona distinta (cuenta de usuario). Sin embargo, disponer de cuentas independientes para cada función normalmente aporta pocas ventajas, a menos que dichas funciones las realicen personas distintas. Es aceptable disponer de cuentas de usuario únicas en varios grupos de funciones, o incluso en todos los grupos de funciones, si así se refleja de forma más precisa la estructura administrativa. Consulte la siguiente sección, "Creación de un modelo de administración simplificado para la entidad emisora de certificados de empresa".
  
##### Población de grupos de administración de entidades emisoras
  
Debe llenar los grupos de administración de entidades emisoras con las cuentas del personal de administración adecuado de la organización. Para obtener una descripción completa de cómo se asignan estos grupos a las funciones administrativas de la infraestructura de Servicios de Certificate Server, consulte la sección "Funciones administrativas" del capítulo 4, "Diseño de la infraestructura de claves públicas". Para obtener más información acerca de las funciones administrativas de Servicios de Certificate Server de Windows Server 2003, consulte el tema "Administración basada en funciones" en la ayuda en pantalla o consulte la referencia al final de este capítulo.
  
**Nota:** si ha creado las cuentas de dominio de prueba, de todos modos debe agregarlas manualmente como miembros de sus grupos de seguridad correspondientes. Como medida de seguridad, la secuencia de comandos no realiza este paso de forma predeterminada.
  
Los procedimientos de configuración del resto de este documento requieren que se realicen algunas acciones de configuración con cuentas miembro de los grupos de administradores de PKI de empresa, editores de PKI de empresa y administradores de entidad emisora de certificados. Este enfoque evita la necesidad de utilizar privilegios de administrador de empresa o de dominio en los casos en que no es absolutamente necesario.
  
**Nota:** es posible forzar la separación estricta de funciones en Servicios de Certificate Server de Windows Server 2003 (sólo Enterprise Edition). Esto significa que no se permitirá ninguna función administrativa en la entidad emisora a cualquier cuenta a la que se le asigne más de una función (directamente o a través de la pertenencia a un grupo). Esta opción no está habilitada en el producto de forma predeterminada o en esta solución, de modo que puede asignar varias funciones administrativas a la misma cuenta de usuario si es conveniente para la organización.
  
##### Creación de un modelo de administración simplificado para la entidad emisora de certificados de empresa
  
Las cuentas y grupos administrativos de prueba ilustran la configuración más compleja de funciones administrativas, en la que cada función de entidad emisora corresponde a una persona distinta (cuenta de usuario). No obstante, es legítimo disponer de cuentas únicas en varios grupos de funciones, o incluso en todos los grupos de funciones, si así se refleja de forma más precisa la estructura administrativa.
  
Muchas organizaciones sólo utilizarán tres funciones: administrador de entidad emisora, auditor y operador de copia de seguridad. Estas funciones se muestran en la tabla siguiente (mediante un subconjunto de las cuentas de prueba creadas anteriormente para la ilustración).
  
**Tabla 7.9: Asignación de grupos del modelo de administración simplificada**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cuenta de usuario de función de administración simplificada</th>
<th style="border:1px solid black;" >Pertenencia a grupos de la cuenta de usuario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CAAdmin</td>
<td style="border:1px solid black;">Administradores de PKI de empresa
Administradores de entidad emisora
Administradores de certificados
Administradores (administradores locales de la entidad emisora)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CAAuditor</td>
<td style="border:1px solid black;">Auditores de entidad emisora
Administradores (administradores locales de la entidad emisora)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CABackup</td>
<td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
</tr>
</tbody>
</table>
  
Con esta disposición, la cuenta CAAdmin podría realizar todas las tareas administrativas en entidades emisoras de certificados de empresa (incluida la aprobación y revocación de certificados) y tendría el control administrativo de toda la información de configuración de PKI de empresa de Active Directory (los permisos para las mismas se establecen más adelante en el documento).
  
##### Estructura de UO de dominio sugerida para la administración de plantillas de certificados y entidades emisoras
  
Existen varios grupos y cuentas de usuario asociados a la administración y funcionamiento de una PKI. Debe organizar estos grupos y cuentas de usuario en unidades organizativas que permitan una administración más fácil. En la tabla siguiente se muestra una estructura de UO y se describe la finalidad de cada UO (los elementos con sangría son UO secundarias de la UO de Servicios de Certificate Server).
  
Debe otorgar los permisos de grupo de administradores de PKI de empresa para crear y eliminar grupos y usuarios en la UO y en todos los contenedores secundarios.
  
**Tabla 7.10: Estructura de UO de ejemplo**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >UO</th>
<th style="border:1px solid black;" >Finalidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicios de Certificate Server</td>
<td style="border:1px solid black;">UO principal.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">\—Administración de Servicios de Certificate Server</td>
<td style="border:1px solid black;">Contiene grupos administrativos para la administración de la configuración de la entidad emisora y la PKI de empresa.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">\—Administración de plantillas de certificados</td>
<td style="border:1px solid black;">Contiene grupos para administrar plantillas de certificados individuales.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">\—Inscripción de plantillas de certificados</td>
<td style="border:1px solid black;">Contiene grupos que poseen permisos de inscripción o inscripción automática en plantillas del mismo nombre. El control de estos grupos puede delegarse al personal adecuado para permitir un régimen de inscripción flexible sin tocar las plantillas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">\—Usuarios de prueba de Servicios de Certificate Server</td>
<td style="border:1px solid black;">Contiene cuentas de prueba temporales.</td>
</tr>
</tbody>
</table>
  
Para obtener más información sobre el uso de estas UO y los grupos que contienen, consulte las secciones correspondientes del capítulo 11, "Administración de la infraestructura de claves públicas".
  
**Para crear la jerarquía de administración de UO de Servicios de Certificate Server**
  
1.  Inicie sesión con una cuenta con permisos para crear UO y para delegar permisos en las mismas. (Como creador de las UO nuevas, siempre podrá concederse permisos para delegar el control de las mismas.)
  
2.  Cree la estructura de UO que se muestra en la tabla anterior en una ubicación adecuada del dominio. (Se supone, sin que sea imprescindible, que es el dominio raíz del bosque.)
  
3.  Conceda permisos al grupo de administradores de la infraestructura de claves públicas de la empresa para crear y borrar grupos de la UO y todos los contenedores secundarios.
  
    **Nota:** esta estructura de UO es sólo un ejemplo. No es necesario adoptarlo.
  
#### Seguridad de Servicios de clave pública de Active Directory
  
En esta sección se describe cómo delegar el control del contenedor Servicios de clave pública a los grupos de seguridad de administración de PKI.
  
##### Concesión de permisos para el contenedor Servicios de clave pública
  
La información de configuración de PKI del bosque se almacena en el contenedor Configuración de Active Directory. Los permisos para cambiar este contenedor y todos sus subcontenedores y objetos están limitados al grupo de seguridad Administradores de organización de forma predeterminada.
  
Debe modificar la seguridad en el contenedor Servicios de clave pública por los siguientes motivos:
  
-   Para permitir que los administradores de PKI de empresa instalen entidades emisoras de empresa y configuren plantillas de certificados sin tener que ser miembros del grupo de seguridad Administradores de empresa.
  
-   Para permitir que los editores de PKI de empresa publiquen listas de revocación de certificados y certificados de CA sin tener que ser miembros de Administradores de empresa.
  
Si no es miembro del grupo de administradores de empresa de Active Directory, debe solicitar que un miembro de dicho grupo realice el primer procedimiento en su lugar.
  
**Precaución:** este procedimiento delega una parte muy delicada de Active Directory, la que afecta a los usuarios y equipos en todo el bosque. Debe ser muy cuidadoso con los usuarios a los que concede control sobre el contenedor Servicios de clave pública. Las cuentas con permisos para controlar este contenedor pueden, entre otras acciones, agregar y quitar entidades emisoras raíz de confianza, agregar y quitar entidades emisoras de empresa y crear credenciales válidas para cualquier usuario del bosque.
  
**Para conceder permisos al grupo de administradores de PKI de empresa**
  
1.  Inicie sesión como miembro del grupo de seguridad Administradores de organización.
  
2.  En el complemento Sitios y servicios de Active Directory de Microsoft Management Console (MMC), muestre el nodo **Servicios** (en el menú **Ver**). Vaya al subcontenedor Servicios de clave pública y abra las propiedades.
  
3.  En la ficha **Seguridad**, agregue el grupo de seguridad Administradores de la infraestructura de claves públicas de la empresa y concédale permisos de **Control total**.
  
4.  En **Opciones avanzadas**, edite los permisos del grupo para asegurarse de que se aplica **Control total** a **Este objeto y todos los secundarios**.
  
5.  Seleccione el contenedor Servicios y abra las propiedades.
  
6.  En la ficha **Seguridad**, agregue el grupo de seguridad Administradores de la infraestructura de claves públicas de la empresa y concédale permisos de **Control total**.
  
7.  En **Opciones avanzadas**, edite los permisos del grupo para asegurarse de que se aplica **Control total** a **Sólo a este objeto**.
  
**Para conceder permisos al grupo de editores de PKI de empresa**
  
1.  Inicie sesión como miembro del grupo de seguridad Administradores de la infraestructura de claves públicas de la empresa (o el grupo de administradores de organización).
  
2.  En el complemento Sitios y servicios de Active Directory de MMC, muestre el nodo **Servicios** y abra las propiedades del contenedor Servicios de clave pública\\AIA.
  
3.  En la ficha **Seguridad**, agregue el grupo de seguridad Editores de PKI de empresa y concédale los permisos siguientes.
  
    -   Leer
  
    -   Escritura
  
    -   Crear todos los objetos secundarios
  
    -   Borrar todos los objetos secundarios
  
4.  En **Opciones avanzadas**, edite los permisos del grupo para asegurarse de que se aplican permisos a **Este objeto y todos los secundarios**.
  
5.  Repita los pasos del 2 al 4 para los contenedores siguientes:
  
    -   Servicios de clave pública\\CDP
  
    -   Servicios de clave pública\\Entidades emisoras de certificados
  
        **Nota:** después de que los permisos se han concedido a los administradores de PKI de empresa en el procedimiento anterior, un miembro de este grupo puede conceder permisos a los editores de PKI de empresa.
  
##### Concesión de permisos para el grupo de publicadores de certificados
  
El grupo de seguridad Publicadores de certificados contiene las cuentas de equipo de todas las entidades emisoras de certificados de empresa del dominio. Este grupo se utiliza para aplicar permisos a objetos usuario y equipo y a los objetos del contenedor CDP mencionados en el procedimiento anterior. Cuando se instala una entidad emisora, es necesario agregar su cuenta de equipo al grupo. De forma predeterminada, sólo los grupos de administradores de dominio, administradores de organización o el grupo de administradores de dominio integrado tienen permisos para modificar la pertenencia a grupo de los publicadores de certificados. Para habilitar a los miembros del grupo de administradores de PKI de empresa para instalar entidades emisoras de certificados de empresa, debe cambiar los permisos del grupo de seguridad.
  
**Para conceder el permiso de modificación de pertenencia a grupo de publicadores de certificados**
  
1.  Inicie sesión como miembro del grupo de administradores de dominio (del dominio en que se instalará la entidad emisora).
  
2.  Abra el complemento MMC Usuarios y equipos de Active Directory.
  
3.  En el menú **Ver** de MMC, asegúrese de que esté activado **Características avanzadas**.
  
4.  Busque el grupo de publicadores de certificados(de forma predeterminada en el contenedor Usuarios) y lea las propiedades del grupo.
  
5.  En la ficha **Seguridad**, **agregue** el grupo **Administradores de PKI de empresa** y haga clic en el botón **Opciones avanzadas**.
  
6.  Seleccione el grupo **Administradores de PKI de empresa** de la lista y haga clic en el botón **Editar**.
  
7.  Seleccione la ficha **Propiedades** y compruebe que **sólo este objeto** esté seleccionado en el cuadro **Aplicar en**:.
  
8.  Desplácese hacia abajo y haga clic en el cuadro **Escribir Miembros** de la columna **Permisos**.
  
9.  Para cerrar todos los diálogos y guardar los cambios, haga clic en **Aceptar** en cada uno.
  
10. Antes de instalar el componente Servicios de Certificate Server, deberá reiniciar el servidor de la CA emisora. Al reiniciar el equipo, el servidor podrá incluir la nueva pertenencia a grupo en su símbolo de acceso.
  
##### Concesión de permisos para administradores de PKI de empresa
  
Para instalar entidades emisoras de certificados de empresa, es necesario tener derecho Restaurar archivos y directorios en el dominio en que se va a instalar la entidad emisora. El proceso de instalación de Servicios de Certificate Server requiere este derecho de usuario para que se puedan instalar plantillas de certificados en el dominio. En concreto, este derecho es necesario para que se puedan combinar descriptores de seguridad de las plantillas y otros objetos de directorio para conceder los permisos correctos para objetos de la infraestructura de claves públicas del dominio. Los grupos de dominio integrados de administradores, operadores de servidores y operadores de copia de seguridad tienen este derecho de forma predeterminada.
  
Dado que utilizará el grupo Administradores de PKI para realizar la instalación de la entidad emisora, debe conceder el derecho Restaurar archivos y directorios a este grupo.
  
**Para conceder derechos de restauración a los administradores de PKI de empresa:**
  
1.  Inicie sesión como miembro del grupo de administradores de dominio (del dominio en que se instalará la entidad emisora).
  
2.  Abra el complemento MMC Usuarios y equipos de Active Directory.
  
3.  Seleccione la UO Controladores de dominio y abra las propiedades.
  
4.  En la ficha Directiva de grupo, seleccione el GPO **Directiva predeterminada de controladores de dominio** y haga clic en **Editar**.
  
5.  Desplácese a Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario y haga doble clic en **Restaurar archivos y directorios**.
  
6.  Agregue el grupo de administradores de PKI de empresa a la lista que se muestra.
  
7.  Cierre el cuadro de diálogo y el GPO editando MMC.
  
    **Importante:** si tiene otros GPO que establecen el derecho de usuario **Restaurar archivos y directorios** en los controladores de dominio, debe realizar el procedimiento anterior en el GPO con mayor prioridad, en lugar de **Directiva predeterminada de controladores de dominio**. Los valores de configuración de derechos de usuario no se acumulan y sólo será efectivo el último GPO aplicado (es decir, el que tenga mayor prioridad) que tenga este derecho establecido.
  
#### Comprobación
  
Es posible comprobar la creación de grupos, usuarios y UO mediante la MMC Usuarios y equipos de Active Directory y desplazándose hasta los usuarios y grupos. Los usuarios deben ser miembros de los grupos adecuados (tanto si utiliza los usuarios de prueba o las cuentas de usuario de administración de PKI reales).
  
Para comprobar la aplicación de permisos en el contenedor Servicios de clave pública, realice los pasos siguientes. Deberá instalar una copia de las herramientas de soporte técnico de Windows Server 2003 en el sistema en el que va a realizar este procedimiento. Este procedimiento no tiene que realizarse en una entidad emisora.
  
**Nota:** en los siguientes procedimientos, en vez de iniciar sesión con distintas cuentas de usuario, puede utilizar Runas o la opción de menú contextual **Ejecutar como** en el Explorador de Windows para ejecutar la MMC ADSIEdit en el contexto de los usuarios requeridos.
  
**Para comprobar los permisos para Servicios de clave pública**
  
1.  Inicie sesión en un servidor miembro del dominio (como el servidor de la CA emisora) como miembro del grupo de administradores de PKI de empresa.
  
2.  Ejecute mmc.exe y cargue el complemento Edición de ADSI.
  
3.  Haga clic con el botón secundario del mouse en la carpeta de edición de ADSI, seleccione **Connect to** y, a continuación, seleccione **Configuration** en la lista desplegable **Select a well known Naming Context**.
  
4.  Desplácese hasta el contenedor Servicios de clave pública y haga clic con el botón secundario del mouse sobre el mismo. A continuación, seleccione **Nuevo** y **Objeto**.
  
5.  Seleccione **Contenedor** en la lista y asígnele un nombre, como por ejemplo **Prueba**.
  
    El objeto contenedor debe crearse correctamente en el contenedor Servicios de clave pública.
  
6.  Elimine el objeto contenedor que acaba de crear.
  
7.  Debe poder crear un objeto contenedor en cualquier parte del contenedor Configuración aparte del contenedor Servicios y sus contenedores secundarios.
  
8.  Inicie sesión como miembro del grupo Editores de PKI de empresa.
  
9.  Cargue ADSIEdit y conéctese al contexto de nomenclatura **Configuración**.
  
10. Intente crear un objeto contenedor en el contenedor Servicios de clave pública. Se producirá un error.
  
11. Cree un objeto de prueba (un objeto contenedor) en cada uno de los subcontenedores de AIA, CDP y entidades emisoras.
  
12. Quite estos objetos de prueba después de comprobar que se han creado correctamente.
  
    **Precaución:** preste atención para eliminar sólo los objetos de prueba que ha creado. En concreto, los miembros de Administradores de PKI de empresa ahora disponen de permisos suficientes para eliminar todo el contenedor Servicios de clave pública.
  
    **Nota:** si decidió no instalar las herramientas de soporte técnico de Windows Server 2003, ADSIEdit no estará disponible. Puede realizar estos pasos de comprobación desde la línea de comandos mediante las utilidades incorporadas dsadd.exe y dsrm.exe. No obstante, debe procurar utilizar la sintaxis y las rutas de objeto de directorio correctas al emplear estas utilidades. Pruebe los comandos atentamente en un sistema de pruebas antes de utilizarlos en un bosque de Active Directory.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Protección de Windows Server 2003 para Servicios de Certificate Server
  
En esta sección se describe cómo aplicar directivas de seguridad y otras medidas de seguridad a Windows Server antes de instalar Servicios de Certificate Server. También debe leer la sección acerca de la seguridad física en el capítulo 4, "Diseño de la infraestructura de claves públicas".
  
#### Implementación de seguridad en el servidor de entidad emisora raíz
  
Las secciones siguientes describen la configuración de grupos locales y cuentas de usuario y la aplicación de directivas de seguridad en el servidor de entidad emisora.
  
##### Creación de cuentas de usuario y grupos de seguridad locales en la entidad emisora raíz
  
Dado que la entidad emisora raíz no forma parte de un dominio, las capacidades y funciones administrativas se definen mediante cuentas de usuario y grupos de seguridad locales.
  
**Para crear cuentas de usuario y grupos locales en el servidor de entidad emisora raíz**
  
1.  En la entidad emisora raíz, ejecute la secuencia de comandos siguiente para crear grupos de administración de entidad emisora locales:
  
    Cscript //job:CertLocalGroups C:\\MSSScripts\\ca\_setup.wsf
  
    La secuencia de comandos crea los grupos locales que se describen en la tabla siguiente.
  
    **Tabla 7.11: Nombres y finalidades de los grupos**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de grupo</th>
    <th style="border:1px solid black;" >Finalidad</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Administradores de entidad emisora</td>
    <td style="border:1px solid black;">Tienen capacidades de administración total para la CA, incluida la determinación de la propiedad de otras funciones.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Administradores de certificados</td>
    <td style="border:1px solid black;">Administran la emisión y revocación de certificados.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Auditores de entidad emisora</td>
    <td style="border:1px solid black;">Administran los datos de auditoría de la CA.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
    <td style="border:1px solid black;">Tienen permisos de copia de seguridad y restauración de claves y datos de la CA.</td>
    </tr>
    </tbody>
    </table>
  
2.  Cree cuentas de usuario locales para las personas que administrarán la entidad emisora. Con la finalidad de crear pruebas e ilustraciones, la secuencia de comandos siguiente crea cuentas locales genéricas correspondientes a cada una de las funciones definidas por los grupos anteriores. Sin embargo, si en este momento puede crear las cuentas reales, omita este paso y créelas.
  
    Cscript //job:CertLocalTestAccts C:\\MSSScripts\\ca\_setup.wsf
  
    La secuencia de comandos utiliza CAPICOM para generar contraseñas pseudoaleatorias en todas las cuentas (en lugar de dejarlas con contraseñas en blanco). Anótelas a partir del resultado o sustitúyalas por otras de su elección.
  
    **Nota:** el uso de cuentas genéricas con contraseñas compartidas entre administradores hace que las pistas de auditoría prácticamente no tengan significado. En un entorno de producción de alta seguridad, siempre debe utilizar cuentas que pueda relacionar con alguna persona.
  
    La secuencia de comandos crea las cuentas locales que se describen en la tabla siguiente.
  
    **Tabla 7.12: Nombres y finalidades de las cuentas**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de cuenta</th>
    <th style="border:1px solid black;" >Finalidad</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">CAAdmin</td>
    <td style="border:1px solid black;">Tiene capacidades de administración total para la CA, incluida la determinación de la propiedad de otras funciones.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">CertManager</td>
    <td style="border:1px solid black;">Administra la emisión y revocación de certificados.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">CAAuditor</td>
    <td style="border:1px solid black;">Administra los datos de auditoría de la CA.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">CABackup</td>
    <td style="border:1px solid black;">Tiene permisos de copia de seguridad y restauración de claves y datos de la CA.</td>
    </tr>
    </tbody>
    </table>
  
    **Nota:** las cuentas de prueba ilustran la configuración más compleja de funciones administrativas, en la que cada función de entidad emisora corresponde a una persona distinta (cuenta de usuario). Sin embargo, disponer de cuentas independientes para cada función aporta pocas ventajas, a menos que dichas funciones las realicen personas distintas. Es aceptable disponer de cuentas únicas en varios grupos de funciones, o incluso en todos los grupos de funciones, si así se refleja de forma más precisa la estructura administrativa.
  
3.  Agregue estas cuentas de usuario a los grupos de seguridad de administración según resulte adecuado. Utilice la tabla siguiente para las cuentas de prueba o utilice sus propias cuentas de acuerdo con las directivas de seguridad y funciones de TI definidas en la organización.
  
    **Tabla 7.13: Nombres de cuenta y pertenencia a grupos**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de cuenta</th>
    <th style="border:1px solid black;" >Pertenencia al grupo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">CAAdmin</td>
    <td style="border:1px solid black;">Administradores de entidad emisora</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">CertManager</td>
    <td style="border:1px solid black;">Administradores de certificados</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">CAAuditor</td>
    <td style="border:1px solid black;">–Auditores de entidad emisora
    –Administradores</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">CABackup</td>
    <td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
    </tr>
    </tbody>
    </table>
  
    **Nota:** también puede convertir en miembros del grupo Administradores de entidad local a los miembros del grupo de administradores locales. Existen ciertas tareas que requieren privilegios de administración locales y es posible que desee combinarlos con la función de los administradores de entidades emisoras.
  
###### Creación de un modelo de administración simplificada para la entidad emisora raíz
  
La mayoría de las organizaciones no necesita una estructura de administración tan compleja como la que se describe en el procedimiento anterior. Es posible que algunas organizaciones no necesiten ninguna separación de funciones. Muchas de ellas utilizan tres funciones: administrador de CA, auditor y operador de copia de seguridad. Se muestran en la tabla siguiente (mediante un subconjunto de las cuentas de prueba creadas anteriormente).
  
**Tabla 7.14: Asignación de grupos del modelo de administración simplificada**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función de administración simplificada</th>
<th style="border:1px solid black;" >Pertenencia al grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CAAdmin</td>
<td style="border:1px solid black;">Administradores de entidad emisora
Administradores de certificados
Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditor de entidad emisora</td>
<td style="border:1px solid black;">Auditores de entidad emisora
Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CABackup</td>
<td style="border:1px solid black;">Operadores de copia de seguridad de CA</td>
</tr>
</tbody>
</table>
  
###### Comprobación de grupos y cuentas
  
Compruebe la creación de grupos, usuarios y pertenencias a grupo observando el nodo Usuarios y grupos de la MMC Administración de equipos.
  
##### Aplicación de configuración de seguridad de sistema en el servidor de entidad emisora raíz
  
Los servidores de entidad emisora se protegen mediante la función de Servicios de Certificate Server Cliente de empresa definida en la *Guía de Seguridad de Windows Server 2003* (consulte la referencia en la sección "Información adicional" al final de este capítulo).
  
La entidad emisora raíz no es miembro de un dominio y no puede utilizar Directiva de grupo de dominio, por lo que las plantillas y los procedimientos de seguridad se deben aplicar manualmente. Obtenga las plantillas de seguridad siguientes de la *Guía de seguridad de Windows Server 2003* y cópielas en la carpeta C:\\MSSScripts del servidor de entidad emisora raíz:
  
-   Enterprise Client–Domain.inf
  
-   Enterprise Client–Member Server Baseline.inf
  
-   Enterprise Client–Certificate Services.inf
  
Personalice las plantillas de seguridad y aplíquelas al servidor de acuerdo con el procedimiento siguiente.
  
**Para personalizar plantillas de seguridad**
  
1.  Inicie sesión como miembro del grupo de administradores locales y cargue Enterprise Client – Certificate Services.inf en la MMC Plantillas de seguridad.
  
2.  En Directivas locales\\Opciones de seguridad, cambie los elementos siguientes de acuerdo con los estándares de seguridad de la organización:
  
    -   Cuentas: cambiar el nombre de la cuenta del administrador: *NuevoNombreDelAdministrador*
  
    -   Cuentas: cambiar el nombre de la cuenta de invitado: *NuevoNombreDelInvitado*
  
    -   Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión: *TextoDelAvisoLegal*
  
    -   Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión: *TítuloDelAvisoLegal*
  
        **Nota:** debe determinar el valor de estos elementos en función de las directivas actuales de la organización. No es necesario configurar estos valores, pero es recomendable.
  
3.  En Directivas locales\\Asignación de derechos de usuario agregue el grupo local Auditores de entidad emisora al derecho de usuario **Administrar registros de auditoría y seguridad**.
  
4.  En Directivas locales\\Asignación de derechos de usuario agregue el grupo local Operadores de copia de seguridad de entidad emisora a los siguientes derechos de usuario:
  
    -   Realizar copias de seguridad de archivos y directorios
  
    -   Restaurar archivos y directorios
  
5.  En Directivas locales\\Asignación de derechos de usuario, agregue los grupos locales siguientes al derecho **Permitir inicio de sesión local**:
  
    -   Administradores
  
    -   Operadores de copia de seguridad
  
    -   Administradores de entidad emisora
  
    -   Administradores de certificados
  
    -   Auditores de entidad emisora
  
    -   Operadores de copia de seguridad de CA
  
6.  Abra las propiedades de los siguientes servicios en la carpeta de servicios del sistema y haga clic en **Definir esta configuración de la directiva en la plantilla**. Acepte los permisos predeterminados haciendo clic en **Aceptar**. Establezca el valor **Seleccionar el modo de inicio del servicio** en **Automático**.
  
    -   Almacenamiento de medios extraíbles
  
    -   Instantáneas de volumen
  
    -   MS Software Shadow Copy Provider
  
        **Nota:** estos servicios están deshabilitados en la plantilla de seguridad de línea de base de servidores miembro, pero NTBackup.exe los requiere.
  
7.  Con la plantilla seleccionada, guarde los cambios de la plantilla (haciendo clic en **Guardar** en el menú **Archivo**) y, a continuación, cierre MMC.
  
8.  Ejecute los comandos siguientes en el orden especificado para aplicar las plantillas de seguridad requeridas. La herramienta Secedit puede indicar que se han generado algunas advertencias; estos mensajes los puede obviar (no obstante, los errores se deben investigar):
  
    secedit /configure /db %temp%\\casec.db /cfg "C:\\MSSScripts\\Enterprise Client - Domain.inf" /overwrite /log "%temp%\\Enterprise Client - Domain.log"
  
    secedit /configure /db %temp%\\casec.db /cfg "C:\\MSSScripts\\Enterprise Client–Member Server Baseline.inf" /log "%temp%\\Enterprise Client–Member Server Baseline.log"
  
    secedit /configure /db %temp%\\casec.db /cfg "C:\\MSSScripts\\Enterprise Client - Certificate Services.inf" /log "%temp%\\Enterprise Client - Certificate Services.log"
  
    (Estos comandos pueden mostrarse en varias líneas; escríbalos en una sola.)
  
    **Nota:** en la *Guía de seguridad de Windows Server* 2003 se incluyen explicaciones más detalladas de estas configuraciones de seguridad.
  
###### Comprobación de la configuración de seguridad
  
Para comprobar la correcta aplicación de la configuración de seguridad, lleve a cabo el siguiente procedimiento.
  
**Para comprobar la configuración de seguridad de la entidad emisora raíz**
  
1.  Observe los registros de secedit producidos en la sección anterior y compruebe que no se hayan producido errores importantes. (Es normal ver una serie de advertencias y errores menores, pero nada que pueda provocar un error en la aplicación de la plantilla de seguridad.)
  
2.  Reinicie el servidor y compruebe que se inician todos los servicios deseados y que no se registran errores en el registro de sucesos.
  
3.  Trate de iniciar la sesión con las cuentas de prueba, o las cuentas reales, que ha creado. Debe aparecer el texto del aviso legal y debe poder iniciar la sesión.
  
#### Implementación de seguridad en el servidor de CA emisora
  
En las secciones siguientes se describe la aplicación de directivas de seguridad al servidor de entidad emisora.
  
##### Aplicación de configuración de seguridad de sistema en el servidor de CA emisora
  
Los servidores de entidades emisoras se protegen mediante la función de Servicios de Certificate Server definida en la *Guía de seguridad de Windows Server 2003*. Dado que la CA emisora es miembro de un dominio, la configuración de directivas de seguridad se aplica mediante una directiva de grupo basada en dominio.
  
Para aplicar la configuración de seguridad, es necesario crear una estructura de UO que contenga los objetos de equipo del servidor de entidad emisora y una estructura de GPO. Debe crear tres GPO:
  
-   Cliente empresarial: Línea de base de servidores miembro
  
-   Cliente empresarial: Servicios de Certificate Server
  
-   Cliente empresarial: IIS de Servicios de Certificate Server (sólo si se ha instalado IIS en la entidad emisora)
  
    **Nota:** la *Guía de seguridad de Windows Server 2003* también incluye una configuración recomendada para la directiva de dominio (directivas de bloqueo de cuentas y contraseñas). Todos los equipos del dominio heredan esta configuración. Si no desea modificar la directiva de nivel de dominio, pero desea utilizar la configuración recomendada para la CA emisora, también debe crear un cuarto GPO vinculado a la UO de entidad emisora:  
    Cliente empresarial: directivas de cuenta de Servicios de Certificate Server  
    Debe seguir el procedimiento siguiente para importar la plantilla de directiva de dominio a este GPO. Esta configuración sólo afectará a las cuentas locales de la propia entidad emisora.
  
El procedimiento siguiente describe cómo se pueden crear unidades organizativas y objetos de directiva de grupo para una organización. Los nombres de GPO y UO son sólo ejemplos. El procedimiento debe adaptarse a los estándares de UO y GPO del dominio.
  
**Para crear las UO y GPO del servidor de entidad emisora**
  
1.  Obtenga las siguientes plantillas de seguridad de la *Guía de seguridad de Windows Server 2003*:
  
    -   Cliente empresarial: Dominio
  
    -   Cliente empresarial: Línea de base de servidores miembro
  
    -   Cliente empresarial: Servicios de Certificate Server
  
    -   Cliente empresarial: Servidor IIS (sólo si se ha instalado IIS en la entidad emisora)
  
2.  Inicie sesión como miembro de Administradores de dominio o como usuario con derechos de creación de las unidades organizativas descritas en el paso 4. También deberá ser miembro del grupo de propietarios del creador de directivas de grupo.
  
3.  Abra el complemento MMC Usuarios y equipos de Active Directory.
  
4.  Cree la siguiente estructura de UO:
  
    woodgrovebank.com (dominio)
  
    Servidores miembro
  
         Entidad emisora
  
5.  Abra las propiedades del contenedor de dominio y, en la ficha **Directiva de grupo**, haga clic en **Nuevo** para crear un GPO nuevo. Asígnele el nombre **Directiva de dominio.**
  
6.  Edite el GPO y desplácese hasta Configuración del equipo\\Configuración de Windows\\Configuración de seguridad. Haga clic con el botón secundario del mouse en la carpeta Configuración de seguridad y, a continuación, seleccione **Importar**. Busque el archivo Enterprise Client - Domain.inf y selecciónelo como la plantilla que desea importar.
  
7.  Cierre el GPO.
  
8.  Repita los tres pasos anteriores para la combinación de OU, GPO y plantillas de seguridad que se muestran en la siguiente tabla.
  
    **Tabla 7.15: Asignación de GPO a plantillas de seguridad y UO**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >UO</th>
    <th style="border:1px solid black;" >GPO</th>
    <th style="border:1px solid black;" >Plantilla de seguridad</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Servidores miembro</td>
    <td style="border:1px solid black;">Cliente empresarial: Línea base de servidor miembro</td>
    <td style="border:1px solid black;">Enterprise Client — Member Server Baseline.inf</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Entidad emisora</td>
    <td style="border:1px solid black;">Cliente empresarial: Servicios de Certificate Server</td>
    <td style="border:1px solid black;">Enterprise Client — Certificate Services.inf</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Entidad emisora</td>
    <td style="border:1px solid black;">(Opcional; consulte la nota anterior)
    Cliente empresarial: directivas de cuenta de Servicios de Certificate Server</td>
    <td style="border:1px solid black;">Enterprise Client — Domain.inf</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Entidad emisora</td>
    <td style="border:1px solid black;">(Opcional; si IIS está en la entidad emisora)
    Cliente empresarial: IIS de Servicios de Certificate Server</td>
    <td style="border:1px solid black;">Enterprise Client — IIS Server.inf</td>
    </tr>
    </tbody>
    </table>
  
    **Nota:** si ha decidido instalar IIS en la CA emisora (según lo descrito en este capítulo), debe crear un GPO de IIS distinto para las entidades emisoras. Aunque es posible que tenga un GPO de IIS para los servidores IIS de la intranet, se recomienda crear un GPO distinto para su uso exclusivo por parte de las entidades emisoras. Este enfoque garantiza que los cambios en el GPO de IIS no afectarán a la seguridad de las entidades emisoras y que la configuración de seguridad de entidad emisora permanece por completo bajo control de los administradores de GPO de CA.
  
Después de crear los GPO e importar las plantillas, debe personalizar la configuración de los GPO y aplicarlos a los equipos de Servicios de Certificate Server como se describe en el procedimiento siguiente.
  
**Para personalizar y aplicar el GPO de Servicios de Certificate Server**
  
1.  Desde Usuarios y equipos de Active Directory, edite el GPO Cliente empresarial: Servicios de Certificate Server. En Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad, cambie los siguientes elementos de acuerdo con los estándares de seguridad de la organización:
  
    -   Cuentas: cambiar el nombre de la cuenta del administrador: *NuevoNombreDelAdministrador*
  
    -   Cuentas: cambiar el nombre de la cuenta de invitado: *NuevoNombreDelInvitado*
  
    -   Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión: *TextoDelAvisoLegal*
  
    -   Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión: *TítuloDelAvisoLegal*
  
2.  En Directivas locales\\Asignación de derechos de usuario agregue el grupo de dominio Auditores de entidad emisora al derecho de usuario **Administrar registros de auditoría y seguridad**.
  
3.  En Directivas locales\\Asignación de derechos de usuario, Operadores de copia de seguridad de entidad emisora a los siguientes derechos de usuario:
  
    -   Realizar copias de seguridad de archivos y directorios
  
    -   Restaurar archivosy directorios
  
4.  En la asignación de directivas locales y derechos de usuario, agregue los siguientes grupos locales y de dominio al derecho **Permitir** **el inicio de sesión loca**l:
  
    -   (local) Administradores
  
    -   (local) Operadores de copia de seguridad
  
    -   (dominio) Administradores de PKI de empresa
  
    -   (dominio) Editores de PKI de empresa
  
    -   (dominio) Administradores de entidad emisora  
  
    -   (dominio) Administradores de certificados
  
    -   (dominio) Auditores de entidad emisora
  
    -   (dominio) Operadores de copia de seguridad de entidad emisora
  
5.  En **Sistema de archivos**, agregue la carpeta D:\\CertLog. Asegúrese de que los permisos aparecen tal como se muestra en la tabla siguiente.
  
    **Tabla 7.16: Permisos de carpeta de base de datos de entidad emisora**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Usuario/grupo</th>
    <th style="border:1px solid black;" >Permiso</th>
    <th style="border:1px solid black;" >Permitir o denegar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Administradores</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Sistema</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Operadores de copia de seguridad</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Propietario del creador</td>
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    </tbody>
    </table>
  
6.  Para la misma carpeta, agregue las entradas de auditoría que se muestran en la tabla siguiente para el grupo Todos (haga clic en el botón **Opciones avanzadas** del cuadro de diálogo **Seguridad** y, a continuación, haga clic en la ficha **Auditoría**). Escriba **Todos** cuando se le pida un nombre de usuario o grupo. Al agregar el grupo Todos se mostrará un cuadro de diálogo titulado **Entrada de auditoría para D:\\CertLog** en el que puede especificar la configuración de auditoría detallada. Compruebe que esté seleccionada la opción **Esta carpeta, subcarpetas y archivos** en el campo **Aplicar en**. Seleccione todos los elementos para los que aparezca Sí en la tabla.
  
    **Tabla 7.17: Auditoría de carpeta de base de datos de entidad emisora**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Permiso</th>
    <th style="border:1px solid black;" >Correcto</th>
    <th style="border:1px solid black;" >Fallido</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">control total</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Recorrer carpeta/Ejecutar archivo</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Listar carpeta/Leer datos</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Atributos de lectura</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Atributos extendidos de lectura</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Crear archivos/Escribir datos</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Crear carpetas/Anexar datos</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Atributos de escritura</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Atributos extendidos de escritura</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Eliminar subcarpetas y archivos</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Eliminar</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Permisos de lectura</td>
    <td style="border:1px solid black;"> </td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Cambiar permisos</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Tomar posesión</td>
    <td style="border:1px solid black;">Sí</td>
    <td style="border:1px solid black;">Sí</td>
    </tr>
    </tbody>
    </table>
  
7.  Abra las propiedades de los siguientes servicios en la carpeta Servicios del sistema y, a continuación, haga clic en **Definir esta configuración de la directiva en la plantilla**. Acepte los permisos predeterminados haciendo clic en **Aceptar**. Establezca el valor **Seleccionar el modo de inicio del servicio** en **Automático**.
  
    -   Almacenamiento de medios extraíbles
  
    -   Instantáneas de volumen
  
    -   MS Software Shadow Copy Provider
  
    -   Programador de tareas
  
        **Nota:** estos servicios están deshabilitados en la plantilla de seguridad de línea de base de servidores miembro, pero NTBackup.exe requiere los tres primeros. Algunas secuencias de comandos operativas requieren el servicio del Programador de tareas.
  
8.  Traslade la cuenta de equipo de CA emisora a la UO de Servicios de Certificate Server.
  
9.  En la CA emisora (el servidor en que se instalará la entidad emisora), ejecute el siguiente comando para aplicar la configuración de GPO al equipo:
  
    gpupdate
  
    **Nota:** en la *Guía de seguridad de Windows Server 2003* se incluyen explicaciones más detalladas de estas configuraciones de seguridad.
  
###### Comprobación de la configuración de seguridad
  
Para comprobar la correcta aplicación de la configuración de seguridad, lleve a cabo los pasos del siguiente procedimiento.
  
**Para comprobar la configuración de seguridad de la entidad emisora raíz**
  
1.  Compruebe en el registro de sucesos de la aplicación si aparecen sucesos del origen SceCli. Debe aparecer el suceso con Id. 1704 después de la ejecución del comando **gpupdate**. El texto del suceso debe ser:
  
    Se ha aplicado satisfactoriamente la directiva de seguridad en los objetos de directiva de grupo.
  
2.  Reinicie el servidor y compruebe que se inician todos los servicios deseados y que no aparecen errores en el registro de sucesos.
  
3.  Trate de iniciar la sesión con las cuentas de prueba, o las cuentas reales, que ha creado. Debe aparecer el texto del aviso legal y debe poder iniciar la sesión.
  
##### Configuración de seguridad de Servicios de Terminal Server en la CA emisora
  
Debe deshabilitar Servicios de Terminal Services en la CA emisora porque proporciona un medio adicional para que un intruso ataque la entidad emisora y reduce significativamente el efecto de las medidas de seguridad que protegen el servidor. Si debe dejarlo habilitado (para administración remota), debe configurar los parámetros descritos en la siguiente tabla.
  
**Nota:** el estado de Servicios de Terminal Server en la entidad emisora raíz es irrelevante porque no está conectada a la red.
  
Esta configuración debe establecerse en el GPO de seguridad de Servicios de Certificate Server o en otro GPO que se aplique a las entidades emisoras en línea.
  
**Tabla 7.18: Configuración para Configuración de equipo\\Plantillas administrativas\\Componentes de Windows\\Servicios de Terminal Server**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Ruta de configuración</th>
<th style="border:1px solid black;" >Directiva</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Denegar el cierre de sesión a un administrador con una sesión iniciada en la consola</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir a los administradores locales personalizar permisos</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Establece reglas para el control remoto de sesiones de usuario de Servicios de Terminal Server</td>
<td style="border:1px solid black;">Control remoto no permitido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Redirección de datos cliente-servidor</td>
<td style="border:1px solid black;">Permitir redirección de zona horaria</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir redirección del portapapeles</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Permitir redirección de audio</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir redirección de puertos COM</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir redirección de impresoras de cliente</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir redirección de puertos LPT</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No permitir redirección de unidad</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">No establecer impresora predeterminada de cliente como impresora predeterminada para una sesión</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cifrado y seguridad</td>
<td style="border:1px solid black;">Pedir siempre al cliente la contraseña al conectarse</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Establecer el nivel de cifrado de conexión de cliente</td>
<td style="border:1px solid black;">Alta</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cifrado y seguridad\Seguridad de llamada a procedimiento remoto</td>
<td style="border:1px solid black;">Servidor seguro (requerir seguridad)</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sesiones</td>
<td style="border:1px solid black;">Establecer el límite de tiempo para sesiones desconectadas</td>
<td style="border:1px solid black;">10 minutos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Permitir reconexiones sólo desde el cliente original</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
Cualquier grupo de seguridad o cuenta de dominio que requiera el acceso de Servicios de Terminal Server a la entidad emisora debe agregarse al grupo de usuarios de escritorio remoto (a menos que ya sea un miembro del grupo de administradores locales).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Otras tareas de configuración de Windows
  
Seguramente, necesitará realizar otras tareas de configuración en la entidad emisora raíz y la CA emisora, Estas tareas pueden incluir:
  
-   Habilitación de copias de seguridad (según lo descrito en el capítulo 11) o instalación de copia de seguridad.
  
-   Configuración de las opciones del Protocolo simple de administración de redes (SNMP) o del Instrumental de administración de Windows (WMI).
  
-   Instalación de agentes de administración como los componentes de cliente de Microsoft Operations Manager (MOM) o Microsoft Systems Management Server (SMS).
  
-   Instalación de software antivirus.
  
-   Instalación de agentes de detección de intrusiones.
  
Debe comprobar estos elementos a medida que se instalan, de acuerdo con las instrucciones proporcionadas con el producto.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Instalación y configuración de la entidad emisora raíz
  
En esta sección se describe cómo se instala y configura Servicios de Certificate Server en la entidad emisora raíz.
  
#### Preparación del archivo Capolicy.inf para la entidad emisora raíz
  
Antes de configurar una entidad emisora raíz de Windows 2003, debe crear el archivo Capolicy.inf. Este archivo especifica las características del certificado de entidad emisora raíz, como la longitud de la clave, el período de validez del certificado, las ubicaciones de publicación de listas CRL y AIA, las directivas de certificados y la declaración de prácticas de certificados (CPS), si la ha creado.
  
**Nota:** consulte la sección "Creación de una declaración de prácticas de certificados" del capítulo 4, "Diseño de la infraestructura de claves públicas" para obtener una descripción detallada de la CPS y si debe considerar la creación de una. Un CPS es un documento legal, no un elemento técnico, por lo que debe asegurarse de que lo necesita antes de configurarlo en la CA.
  
La información de listas CRL y AIA no se requiere para el certificado de entidad emisora de certificados en sí, de modo que los parámetros CRLDistributionPoint y AuthorityInformationAccess están definidos como **Vacío** en el archivo Capolicy.inf.
  
**Para crear el archivo CAPolicy.inf**
  
1.  En un editor de texto, como Bloc de notas, escriba el texto siguiente:
  
    ```
    [Version]
    Signature= "$Windows NT$"

    [Certsrv_Server]
    RenewalKeyLength=4096 
    RenewalValidityPeriod=Years 
    RenewalValidityPeriodUnits=16

    [CRLDistributionPoint]
    Empty=true

    [AuthorityInformationAccess]
    Empty=true
    ```
  
    **Precaución**: la configuración de una longitud de clave de 4096 bits puede provocar problemas de compatibilidad. Determinados dispositivos (por ejemplo, algunos enrutadores) y software antiguo de otros proveedores no pueden procesar claves de un cierto tamaño.
  
2.  Si ha definido una CPS para esta entidad emisora, incluya la información siguiente en el archivo Capolicy.inf (debe reemplazar los elementos en cursiva por los valores correspondientes):
  
    ```
    [CAPolicy]
    Policies=WoodGrove Bank Root CA CPS

    [WoodGrove Bank Root CA CPS]
    OID=your.Orgs.OID
    URL = "http://www.woodgrovebank.com/YourCPSPage.htm"
    ```
  
3.  Guarde el archivo como %windir%\\Capolicy.inf (reemplace %windir% por la ruta de acceso absoluta en que se haya instalado Windows, como C:\\Windows). Debe ser administrador local o tener permisos de escritura en la carpeta Windows para realizar este paso.
  
#### Instalación de componentes de software de Servicios de Certificate Server
  
Utilice el Asistente para componentes de Windows con el fin de instalar componentes de software de entidad emisora. Tenga en cuenta que para completar la instalación, se requiere el CD de instalación de Windows Server 2003 o la ruta de acceso de red.
  
**Para instalar los Servicios de Certificate Server**
  
1.  Inicie sesión como miembro del grupo de administradores locales y ejecute el administrador de componentes opcionales (o, en Panel de control, haga clic en **Agregar o quitar programas**/**Agregar o quitar componentes de Windows**):
  
    sysocmgr /i:sysoc.inf.
  
2.  Seleccione el componente **Servicios de Certificate Server** (haga clic en **Sí** para descartar el cuadro de mensaje de advertencia para cambiar el nombre).
  
3.  Seleccione el tipo de entidad emisora como **Entidad emisora raíz independiente** y asegúrese de seleccionar la casilla de verificación **Utilizar la siguiente configuración personalizada**.
  
4.  En el cuadro de diálogo **Pareja de claves pública y privada**, deje la configuración predeterminada, excepto para el valor de longitud de clave, que debe establecer en 4096. El **tipo de proveedor de servicios de cifrado** debe ser **Microsoft Strong Cryptographic Provider**.
  
5.  Escriba la información de identificación de la entidad emisora de certificados como se indica a continuación:
  
    -   Nombre común de entidad emisora: *entidad emisora raíz de WoodGrove Bank* 
  
    -   Sufijo de nombre distintivo: *DC=woodgrovebank,DC=com*  
        (el nombre raíz de bosque de Active Directory de la organización)
  
    -   Período de validez: **8 año*s***
  
        **Nota:** si en este equipo se ha instalado anteriormente una entidad emisora, un cuadro de diálogo de advertencia le avisará de que se sobrescribirá la clave privada de la instalación anterior. Antes de continuar, debe comprobar que la clave no se volverá a necesitar nunca. En caso de duda, cancele el procedimiento de instalación y realice una copia de seguridad de la información clave existente. (Utilice una copia de seguridad del sistema o una copia de seguridad del certificado y la clave privada de la entidad emisora existentes; consulte los procedimientos correspondientes en el capítulo 11, "Administración de la infraestructura de claves públicas".)
  
    El CSP genera el par de claves, que se escribe en el almacén de clave de equipo local.
  
6.  Deje los valores predeterminados para la ubicación de la base de datos de certificados, los registros de base de datos y la carpeta de configuración.
  
    **Notas:**   
    El programa de instalación puede mostrar una advertencia acerca de que no se puede crear una carpeta compartida, porque todas las interfaces de red se han deshabilitado anteriormente. Puede omitir esta advertencia y continuar.  
    Debe guardar la base de datos de certificados y el registro de la base de datos de certificados en unidades NTFS locales.
  
    A continuación, el administrador de componentes opcionales instala los componentes de Servicios de Certificate Server. Esta parte del proceso requiere el medio de instalación de Windows Server 2003.
  
7.  Haga clic en **Aceptar** para cerrar la advertencia acerca de IIS y continuar con la instalación hasta que finalice.
  
#### Comprobación de la instalación de la entidad emisora raíz
  
Puede comprobar que la instalación de los Servicios de Certificate Server ha sido correcta como se indica a continuación:
  
**Para comprobar que la instalación de la entidad emisora raíz es correcta**
  
1.  Abra la consola de administración Entidad emisora de certificados (desde **Todos los programas**, **Herramientas administrativas**). Compruebe que se han iniciado los Servicios de Certificate Server y que puede ver las propiedades de la CA.
  
2.  En la ficha **General**, seleccione el certificado de entidad emisora (o **Certificado nº 0** en la lista si hay varios certificados) y, a continuación, haga clic en **Ver certificado**.
  
3.  Consulte la ficha **Detalles** del certificado de entidad emisora y compruebe que los valores que se muestran coinciden con los de la tabla siguiente.
  
    **Tabla 7.19: Propiedades y extensiones de certificado de entidad emisora raíz**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Atributo del certificado</th>
    <th style="border:1px solid black;" >Opción requerida</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Campos Emisor y Asunto</td>
    <td style="border:1px solid black;">Ambos campos deben ser idénticos y deben mostrar el nombre común completo de la entidad emisora y el sufijo DN especificados durante la instalación.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">No antes de - No después de</td>
    <td style="border:1px solid black;">16 años.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Longitud de la clave pública</td>
    <td style="border:1px solid black;">RSA (4096 bits).</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Uso de claves</td>
    <td style="border:1px solid black;">Firma digital, Firma de certificados, Firma CRL sin conexión, Firma CRL (86).</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Restricciones básicas (esenciales)</td>
    <td style="border:1px solid black;">Tipo de asunto=CA
    Restricción de longitud de ruta=Ninguna</td>
    </tr>
    </tbody>
    </table>
 
    La presencia del tipo de sujeto Restricciones básicas es muy importante porque este valor distingue el certificado de entidad emisora del certificado de una entidad final. Además, no deben enumerarse extensiones CDP o AIA.

    Si alguno de los valores no es el que esperaba, debe volver a iniciar la instalación de Servicios de Certificate Server.

    **Nota:** si vuelve a ejecutar la instalación de Servicios de Certificate Server, aparecerá una advertencia de que la clave privada ya existe. Si está seguro de que no ha emitido ningún certificado con esta clave, puede omitir la advertencia y generar una clave nueva. Si la entidad emisora ya ha emitido certificados (además de los de prueba), no se debe reinstalar Servicios de Certificate Server hasta que se haya hecho una copia de seguridad segura de la clave y el certificado anterior (este procedimiento se describe en el capítulo 11, “Administración de la infraestructura de claves públicas”).

4.  Para una comprobación adicional o para solucionar problemas en caso de error, puede consultar el registro de configuración de Servicios de Certificate Server (%systemroot%\\certocm.log).

#### Configuración de las propiedades de la entidad emisora raíz

El procedimiento de configuración de la entidad emisora aplica una serie de parámetros específicos del entorno. Los valores de dichos parámetros se documentan en una sección anterior del capítulo, "Hoja de trabajo de planeamiento de los Servicios de Certificate Server". Este procedimiento configura las propiedades de la entidad emisora tal como se enumeran en la siguiente tabla.

**Tabla 7.20: Propiedades de la entidad emisora que se deben configurar**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Propiedad de la CA</th>
<th style="border:1px solid black;" >Descripción de la opción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Direcciones URL de punto de distribución de la CRL</td>
<td style="border:1px solid black;">Especifica las ubicaciones HTTP, LDAP y FILE desde las que se puede obtener una lista CRL actual.<br/><br/>
La ubicación FILE es una carpeta local que utiliza la entidad emisora para almacenar las listas CRL que emite. Los certificados que se emiten sólo incluyen las ubicaciones HTTP y LDAP.<br/><br/>
La dirección URL de HTTP se muestra secuencialmente antes que LDAP, de modo que los clientes que utilicen certificados de entidad emisora raíz no dependen de Active Directory para obtener listas CRL.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Direcciones URL de AIA</td>
<td style="border:1px solid black;">Ubicaciones donde se pueden obtener los certificados de entidad emisora.<br/><br/>
Al igual que con los CDP, la ubicación del archivo sólo se utiliza para publicar el certificado de entidad emisora y la dirección URL de HTTP tiene prioridad sobre la de LDAP.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de validez</td>
<td style="border:1px solid black;">Período de validez máximo de los certificados emitidos (no es el mismo que el período de validez del certificado de entidad emisora, que se establece en CAPolicy.inf o mediante la CA principal).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de la CRL</td>
<td style="border:1px solid black;">Frecuencia de publicación de la CRL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de coincidencia de lista CRL</td>
<td style="border:1px solid black;">Período de coincidencia desde la emisión de una nueva CRL y la fecha de caducidad de la CRL anterior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de diferencia entre listas CRL</td>
<td style="border:1px solid black;">Frecuencia de publicación de diferencia entre listas CRL (en la entidad emisora raíz, la diferencia entre listas CRL está deshabilitada).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditoría de CA</td>
<td style="border:1px solid black;">Configuración de auditoría de CA. De forma predeterminada, toda la auditoría está habilitada.</td>
</tr>
</tbody>
</table>
  
**Nota:** las propiedades mostradas en esta tabla afectan a los certificados emitidos por la entidad emisora raíz, no el propio certificado de la entidad emisora raíz.
  
**Para configurar las propiedades de la entidad emisora raíz**
  
1.  Inicie la sesión en el servidor de la CA como miembro del grupo de administradores.
  
2.  Personalice la siguiente secuencia de comandos (C:\\MSSScripts\\pkiparams.vbs) para incluir el DN correcto de su raíz del bosque de Active Directory y la dirección URL de HTTP que indica el servidor Web de publicación de CDP y AIA. Cambie el valor de la configuración **AD\_ROOT\_DN** para que coincida con su DN de dominio de raíz del bosque de Active Directory. Cambie la configuración **HTTP\_PKI\_VROOT** para que coincida con al ruta de acceso HTTP al directorio virtual de IIS que configuró anteriormente.
  
    **Nota:** aquí sólo se muestra parte del archivo pkiparams.vbs. No edite ni quite otros elementos del archivo a menos que entienda las implicaciones que esto conllevaría.
  
    ```
    '**************************************************************************
    '    USER SETTABLE CONSTANTS        
    '
    ' These values MUST be set to reflect actual values used
    ' by the organization.
    '**************************************************************************

    ' This is the URL where CRL and CA certs are to be published.
    CONST CA_HTTP_PKI_VROOT        = " http://www.woodgrovebank.com/pki"

    ' This needs to be set only if non Active directory clients need to query
    ' the ldap URL for CRLs. Normally they are OK with HTTP. If you do set this 
    ' (to a specific DC FQDN) ALL clients will use this DC to query. Left blank
    ' AD clients use their default LDAP server (local DC) to query.
    CONST CA_LDAP_SERVER        = ""

    ' This needs to be set to the DN of the Active Directory Forest root domain
    ' This is used to set the Root CA CDP and AIA paths so that clients can 
    ' obtain CRL and CA Certificate information from the Active Directory 
    CONST AD_ROOT_DN            = "DC=woodgrovebank,DC=com"
    ```
  
3.  A continuación, ejecute la siguiente secuencia de comandos:
  
    Cscript //job:RootCAConfig C:\\MSSScripts\\ca\_setup.wsf
  
##### Configuración de funciones administrativas
  
Para utilizar las funciones administrativas en la entidad emisora (como auditor y administrador de certificados), debe asignar los grupos de seguridad creados anteriormente a dichas funciones.
  
**Nota:** esta solución utiliza los grupos creados anteriormente para definir varias funciones independientes. Este enfoque proporciona máxima flexibilidad para delegar responsabilidades en la administración de entidad emisora de certificados. Sin embargo, si no requiere este grado de delegación, es recomendable utilizar el modelo de grupo de administración simplificado especificado anteriormente en el capítulo. Este modelo simplificado le permitirá utilizar un número menor de cuentas para realizar las funciones administrativas de entidad emisora de certificados.
  
**Para configurar funciones administrativas en la entidad emisora raíz**
  
1.  Desde la consola de administración Entidad emisora de certificados, haga clic en **Propiedades** para editar las propiedades de la entidad emisora.
  
2.  Haga clic en la ficha **Seguridad** y agregue los grupos de seguridad que se enumeran en la tabla siguiente. Para cada grupo, agregue los permisos que se muestran.
  
    **Tabla 7.21: Entradas de permisos de entidad emisora de certificados que deben agregarse**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de grupo</th>
    <th style="border:1px solid black;" >Permiso</th>
    <th style="border:1px solid black;" >Permitir o denegar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Administradores de entidad emisora</td>
    <td style="border:1px solid black;">Administración de entidad emisora de certificados</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Administradores de certificados</td>
    <td style="border:1px solid black;">Emisión y administración de certificados</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    </tbody>
    </table>
  
    **Nota:** si desea conseguir una mayor separación de funciones, debe quitar los permisos de administración de entidad emisora del grupo de administradores locales. (Debido a que la entidad emisora raíz está instalada en la versión Standard Edition de Windows Server, no puede exigir la separación de funciones, ya que esta opción sólo está disponible en la versión Enterprise Edition.)
  
3.  Se han definido otras funciones de seguridad de entidad emisora para esta entidad emisora a través de la directiva de seguridad aplicada anteriormente al servidor:
  
    -   Se han concedido derechos de usuario de administración de registros de auditoría y seguridad a los auditores de entidad emisora.
  
    -   Los operadores de copia de seguridad tienen los derechos necesarios para realizar una copia de seguridad y restaurar la entidad emisora.
  
#### Transferencia a disco del certificado y la lista CRL de entidad emisora raíz
  
Debe copiar el certificado y la lista CRL de entidad emisora raíz para que se puedan publicar en Active Directory y en el servidor de publicación de certificados y listas CRL de IIS.
  
**Para copiar en el disco el certificado y la lista CRL de entidad emisora raíz**
  
1.  Inicie sesión en la entidad emisora raíz como miembro del grupo de administradores de entidades emisoras locales y, a continuación, coloque el disco que se utilizará para la transferencia a la unidad.
  
2.  Ejecute la secuencia de comandos siguiente para copiar el certificado de entidad emisora en el disco:
  
    Cscript //job:GetCACerts C:\\MSSScripts\\CA\_Operations.wsf
  
3.  Ejecute la secuencia de comandos siguiente para copiar la lista CRL de entidad emisora en el disco:
  
    Cscript //job:GetCRLs C:\\MSSScripts\\CA\_Operations.wsf
  
4.  Etiquete el disco **Transfer-\[***HQ-CA-01***\]**, asígnele una fecha y guárdelo para una fase posterior del procedimiento.
  
    **Nota:** el disco no contiene información de seguridad importante (como material de claves privadas de entidad emisora), por lo que no tiene que adoptar precauciones de seguridad especiales.
  
#### Publicación de información de la entidad emisora raíz
  
Antes de instalar la CA emisora, debe publicar el certificado de entidad emisora raíz en el almacenamiento raíz de confianza de Active Directory y publicar la lista CRL de entidad emisora raíz en el contenedor CDP de Active Directory. Esto hará que todos los miembros del dominio (incluida la CA emisora) importen el certificado de entidad emisora raíz a sus propios almacenes raíz y les permitirá comprobar el estado de revocación de los certificados emitidos por la entidad emisora raíz. (La CA emisora debe poder comprobar el estado de revocación de su propio certificado antes de iniciar Servicios de Certificate Server.)
  
**Nota:** puede llevar a cabo el procedimiento siguiente desde cualquier miembro del dominio, aunque requiere que se instalen Certutil.exe y las bibliotecas auxiliares certadm.dll y certcli.dll en dicho sistema; certutil.exe (junto con las bibliotecas requeridas) se instala como parte de Windows Server 2003. Puede utilizar el servidor de CA emisora sin configurar para realizar el procedimiento.
  
**Para publicar el certificado y la lista CRL de entidad emisora raíz en Active Directory**
  
1.  Inicie sesión en un equipo miembro del dominio como miembro del equipo Administradores de PKI de empresa e inserte el disco que ha utilizado antes para almacenar el certificado y la lista CRL de entidad emisora raíz (etiquetado como **Transfer-\[***HQ-CA-01***\]**).
  
2.  Ejecute la secuencia de comandos siguiente para publicar el certificado de entidad emisora en Active Directory:
  
    Cscript //job:PublishCertstoAD C:\\MSSScripts\\CA\_Operations.wsf
  
3.  Ejecute la secuencia de comandos siguiente para publicar las listas CRL de entidad emisora en Active Directory:
  
    Cscript //job:PublishCRLstoAD C:\\MSSScripts\\CA\_Operations.wsf
  
##### Publicación de certificados y listas CRL de entidad emisora raíz en el servidor Web
  
Esta tarea es necesaria porque las versiones HTTP de las direcciones URL de CDP y AIS están especificadas en las extensiones de los certificados emitidos por esta entidad emisora. Si dichas extensiones están presentes, deben publicarse las listas CRL y los certificados en las direcciones URL configuradas en los certificados para utilizarlos.
  
**Nota:** este procedimiento es el mismo tanto si el servidor Web de publicación AIA y CDP se encuentra en la CA emisora como en otro servidor. Se supone que el directorio virtual coincide con el configurado en el procedimiento anterior para configurar IIS: C:\\CAWWWPub. Si ha optado por utilizar una ruta de acceso distinta, tendrá que actualizar el valor WWW\_LOCAL\_PUB\_PATH en el archivo C:\\MSSScripts\\PKIParams.vbs.
  
**Para publicar el certificado y la lista CRL de entidad emisora raíz en la dirección URL Web**
  
1.  Inicie sesión en el servidor Web como administrador local o con una cuenta que tenga permisos de escritura para la carpeta C:\\CAWWWPub.
  
2.  Compruebe que el disco (con la etiqueta **Transfer-\[***HQ-CA-01***\]**) que contiene los certificados y listas CRL de entidad emisora esté en la unidad.
  
3.  Ejecute la secuencia de comandos siguiente para publicar el certificado de entidad emisora en la carpeta de servidor Web:
  
    Cscript //job:PublishRootCertstoIIS
  
    C:\\MSSScripts\\CA\_Operations.wsf
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
4.  Ejecute la secuencia de comandos siguiente para publicar las listas CRL de entidad emisora en la carpeta de servidor Web:
  
    Cscript //job:PublishRootCRLstoIIS
  
    C:\\MSSScripts\\CA\_Operations.wsf
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
##### Comprobación de la publicación de información de la entidad emisora raíz
  
Es necesario comprobar que la publicación de información de la entidad emisora raíz se ha realizado correctamente. Para realizar estos pasos, debe iniciar la sesión en un equipo miembro del dominio conectado a la red y utilizar una cuenta de usuario de dominio válida.
  
**Nota:** es posible que tenga que espera a que se produzca la replicación de Active Directory. Utilice el comando certutil -pulse para forzar la descarga de certificados de entidad emisora antes de comprobar la publicación de información de la entidad emisora raíz.
  
**Para comprobar la publicación de información de la entidad emisora raíz**
  
1.  Para comprobar la publicación del certificado de entidad emisora en el almacenamiento raíz de confianza, ejecute el comando siguiente:
  
    certutil -viewstore -enterprise Root
  
2.  Debe aparecer un certificado. Compruebe que los valores para **Emisor** y **Asunto** coincidan con los que ha configurado para el nombre de entidad emisora raíz y que la fecha **Válido desde** sea la fecha actual.
  
3.  Para comprobar la publicación de la lista CRL de entidad emisora raíz en el directorio, ejecute el comando siguiente, reemplazando los elementos en cursiva con los valores de la instalación (nombre común de entidad emisora, nombre corto de host de entidad emisora y DN de raíz de bosque de Active Directory):
  
    certutil -store -enterprise "ldap:///cn=WoodGrove Bank Root CA,cn=HQ-CA-01,cn=CDP,CN=Public Key Services,CN=Services,CN=Configuration,DC=woodgrovebank,DC=com?certificateRevocationList?base?objectClass=crlDistributionPoint"
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
4.  Los resultados deberán ser similares a los siguientes. Compruebe que el valor **Emisor** coincida con el nombre que ha configurado para la entidad emisora raíz:
  
    ================ CRL 0 ================
  
    Emisor: CN=WoodGrove Bank Root CA,DC=woodgrovebank,DC=com
  
    Versión de entidad emisora: V1.0
  
    Número CRL: Número CRL=1
  
    Hash de CRL (sha1): 73 03 a1 c7 5f a3 c3 f9 8a 09 d0 3c b5 09 00 9c b5 a3 de fe
  
    CertUtil: -comando de almacenamiento completado correctamente.
  
5.  Para comprobar la publicación del certificado de entidad emisora en el servidor Web, escriba la dirección URL siguiente en un explorador y sustituya los elementos en cursiva por los valores utilizados en su propio entorno:
  
    http://*www.woodgrovebank.com*/pki/*HQ-CA-01\_WoodGrove Bank Root CA*.crt
  
    **Nota:** es posible que tenga que utilizar el nombre DNS completo del servidor de entidad emisora en el nombre de archivo de certificado (es decir, *HQ-CA-01*.*woodgrovebank.com\_WoodGrove Bank Root CA*.crt en vez del nombre mostrado anteriormente).
  
6.  Se le solicitará que abra o guarde el archivo. Ábralo y compruebe que aparezca el certificado de la entidad emisora raíz.
  
7.  Para comprobar la publicación de la lista CRL de entidad emisora raíz en el servidor Web, escriba la dirección URL siguiente en un explorador y sustituya los elementos en cursiva por los valores reales utilizados en el entorno:
  
    http://*www.woodgrovebank.com*/pki/*WoodGrove Bank Root CA*.crl
  
8.  Se le solicitará que abra o guarde el archivo. Ábralo y compruebe que aparezca la lista CRL de la entidad emisora raíz.
  
    **Nota:** si dispone de un certificado de entidad emisora renovado o ha emitido más de una lista CRL, pueden aparecer números de versión diferentes en los resultados de estos comandos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Instalación y configuración de la CA emisora
  
En esta sección se describe cómo instalar y configurar Servicios de Certificate Server en la CA emisora. Durante el proceso de instalación, se produce un conjunto de interacciones complejo entre esta entidad emisora, la entidad emisora raíz, Active Directory y el servidor Web. Estas interacciones se muestran en el diagrama siguiente. Es posible que este diagrama le resulte de ayuda a lo largo de esta sección.
  
[![](images/Dd458723.07fig7-2(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458723.07fig7-2_big(es-es,technet.10).gif)
  
**Figura 7.2 Interacción entre entidades emisoras, Active Directory y el servidor Web durante la instalación de la CA emisora**
  
En el diagrama se muestran las interacciones principales entre sistemas distintos durante la instalación de la CA emisora. Estas interacciones son:
  
1.  Publicación de certificados y listas CRL de entidad emisora raíz en Active Directory
  
2.  Publicación de certificados y listas CRL de entidad emisora raíz en el servidor Web
  
3.  Instalación del software Servicios de Certificate Server, que genera una petición de certificados que debe trasladar a la entidad emisora raíz en disco. En la entidad emisora raíz se emite el certificado para esa solicitud.
  
4.  Instalación del certificado de CA emisora.
  
5.  Publicación de certificados y listas CRL de CA emisora en el servidor Web
  
    **Nota:** los pasos 1 y 2 se describen en la sección anterior, "Publicación de entidad emisora raíz". El paso etiquetado como X en el diagrama sucede automáticamente como parte de la configuración de valores de lista CRL y AIA en la CA emisora durante el paso "Configuración de las propiedades de la CA emisora". El resto de pasos se describe en esta sección.
  
#### Preparación del archivo Capolicy.inf para la CA emisora
  
El archivo CAPolicy.inf no es estrictamente necesario para la CA emisora. Sin embargo, necesitará uno si desea cambiar el tamaño de clave que utiliza la entidad emisora. Debe crear el archivo Capolicy.inf antes de configurar la CA emisora (aunque es posible agregar uno más tarde y renovar el certificado de entidad emisora). Este archivo especifica algunas de las características del certificado de entidad emisora, como la longitud de clave y la CPS (si la ha creado).
  
**Para crear el archivo CAPolicy.inf**
  
1.  En un editor de texto como el Bloc de notas, escriba el texto siguiente.
  
    ```
    [Version]
    Signature= "$Windows NT$"

    [Certsrv_Server]
    RenewalKeyLength=2048 
    ```
  
2.  Si ha definido una CPS para esta entidad emisora, incluya la información siguiente en el archivo Capolicy.inf (debe reemplazar los elementos en cursiva por los valores correspondientes):
  
    ```
    [CAPolicy]
    Policies=WoodGrove Bank Issuing CA 1 CPS

    [WoodGrove Bank Issuing CA 1 CPS]
    OID=your.Orgs.OID
    URL = "http://www.woodgrovebank.com/YourCPSPage.htm"
    ```
  
    **Nota:** consulte la sección "Creación de una declaración de prácticas de certificados" del capítulo 4, "Diseño de la infraestructura de claves públicas" para obtener una descripción detallada de la CPS y si debe considerar la creación de una. Un CPS es un documento legal, no un elemento técnico, por lo que debe asegurarse de que lo necesita antes de configurarlo en la CA.
  
3.  Guarde el archivo como %windir%\\Capolicy.inf (o reemplace %windir% por la ruta de acceso absoluta en que se haya instalado Windows, como C:\\Windows). Debe ser administrador local o tener permisos de escritura en la carpeta Windows para realizar este paso.
  
#### Instalación de componentes de software de Servicios de Certificate Server
  
Utilice el Asistente para componentes de Windows con el fin de instalar componentes de software de entidad emisora. Tenga en cuenta que es posible que necesite el medio (CD) de instalación de Windows Server 2003 para completar la instalación.
  
**Para instalar los Servicios de Certificate Server**
  
1.  Inicie sesión en el servidor como miembro del grupo local Administradores y ejecute el administrador de componentes opcionales (o haga clic en **Agregar o quitar programas**/**Componentes de Windows** en el Panel de control).
  
    sysocmgr /i:sysoc.inf
  
    **Nota:** sólo tiene que ser miembro del grupo local Administradores para realizar la primera parte de la instalación. En el siguiente procedimiento también tiene que ser miembro de Administradores de PKI de empresa (o Administradores de empresa) para instalar el certificado de entidad emisora.
  
2.  Seleccione el componente Servicios de Certificate Server (haga clic en **Aceptar** para cerrar el cuadro de mensaje de advertencia para cambiar el nombre).
  
3.  Seleccione el tipo de entidad emisora **Entidad emisora subordinada de la empresa** y compruebe que ha activado la casilla de verificación **Utilizar la siguiente configuración personalizada**.
  
4.  En el cuadro de diálogo **Pareja de claves pública y privada**, deje la configuración predeterminada, excepto para el valor de longitud de clave, que debe establecer en **2048** bits. El tipo de proveedor de servicios de CSP debe ser **Microsoft Strong Cryptographic Provider**.
  
5.  Escriba la información de identificación de la entidad emisora de certificados como se indica a continuación:
  
    -   Nombre común de entidad emisora: *Entidad emisora raíz de WoodGrove Bank 1* 
  
    -   Sufijo de nombre distintivo: *DC=woodgrovebank,DC=com*  
        (el nombre de raíz de bosque de Active Directory de la organización)
  
    -   Período de validez: determinado por la entidad emisora principal
  
        **Nota:** si en este equipo se ha instalado anteriormente una entidad emisora, un cuadro de diálogo de advertencia le avisará de que se sobrescribirá la clave privada de la instalación anterior. Antes de continuar, debe comprobar que la clave no se volverá a necesitar nunca. En caso de duda, cancele el procedimiento de instalación y realice una copia de seguridad de la información clave existente. (Utilice una copia de seguridad del sistema o una copia de seguridad del certificado y la clave privada de la entidad emisora existentes; consulte los procedimientos correspondientes en el capítulo 11, "Administración de la infraestructura de claves públicas".)
  
6.  El CSP generará el par de claves y lo escribe en el almacén de claves del equipo local.
  
7.  Escriba las ubicaciones de la base de datos de certificados, registros de la base de datos y la carpeta de configuración como sigue:
  
    -   Base de datos de certificados: **D:\\CertLog**
  
    -   Registro de base de datos de certificados: **%windir%\\System32\\CertLog**
  
    -   Carpeta compartida: deshabilitado
  
    Por motivos de rendimiento y resistencia, debe almacenar las bases de datos y registros de entidad emisora en volúmenes separados físicamente siempre que sea posible. (Si la base de datos está dañada por algún motivo, puede utilizar la última copia de seguridad y registros para restaurar la entidad emisora al punto donde se produjo el error.) La base de datos de certificados y los registros de la misma deben estar en unidades locales con formato NTFS.
  
8.  Copie el archivo de solicitudes de certificados en disco. La petición de certificado se genera y se guarda en la ruta de acceso de la carpeta compartida. Copie el archivo *HQ-CA-02.woodgrovebank.com*\_*WoodGrove Bank Issuing CA 1.req* en el disco y asígnele la etiqueta **Transfer-\[***HQ-CA-02***\]**.
  
    A continuación, el administrador de componentes opcionales instalará los componentes de Servicios de Certificate Server. En esta instalación se necesita el medio de instalación (CD) de Windows Server 2003.
  
9.  Haga clic en **Aceptar** para eliminar la advertencia sobre IIS y continuar con la instalación hasta que termine. El asistente para la configuración mostrará un aviso que le indicará que necesita obtener el certificado de entidad emisora principal antes de continuar.
  
    **Notas:**   
    Durante las últimas fases de la instalación aparecerá una advertencia que indica que no la entidad emisora no se ha podido agregar al **grupo Acceso compatible con versiones anteriores de Windows 2000**. Esto sólo es relevante si necesita utilizar la función de restricciones de administradores de certificados de Servicios de Certificate Server. Si necesita esta característica, debe pedir al administrador de dominio que agregue la cuenta de equipo de la entidad emisora a este grupo.  
    Servicios de Certificate Server no se iniciará hasta que la entidad emisora raíz procese la petición de certificado y se obtenga e instale el certificado en la entidad emisora.
  
#### Envío de la petición de certificado a la entidad emisora raíz
  
A continuación, debe enviar la petición de certificado de la CA emisora a la entidad emisora raíz para que se firme y se emita un certificado para la CA emisora.
  
**Para enviar la petición de certificado a la entidad emisora raíz**
  
1.  Inicie sesión en la entidad emisora raíz como miembro del grupo de administradores de certificados.
  
2.  En la consola de administración Entidad emisora de certificados, en el menú **Tareas** de la entidad emisora, seleccione **Enviar solicitud nueva** y, a continuación, envíe la petición transferida desde la CA emisora (en el disco **Transfer-\[***HQ-CA-02***\]**).
  
    **Nota:** si se produjo un error en una configuración de entidad emisora y la repite de nuevo, no vuelva a utilizar el archivo de petición de la configuración de entidad emisora anterior; está asociado al material de claves anteriores y no a la entidad emisora actual que se está instalando.
  
3.  La entidad emisora raíz requiere que se aprueben manualmente todas las solicitudes. Busque la petición en el contenedor Peticiones pendientes de la MMC Entidad emisora de certificados, compruebe que el campo **Nombre común** contiene el nombre de la CA emisora y, a continuación, haga clic con el botón secundario del mouse en la petición y en **Emitir** para aprobar la solicitud.
  
4.  Busque el certificado recién emitido en el contenedor Certificados emitidos y ábralo.
  
5.  Compruebe que los detalles de certificado sean correctos y, a continuación, haga clic en **Copiar al archivo** para exportar el certificado a un archivo y guárdelo como archivo PKCS\#7 (seleccione la opción para incluir todos los certificados posibles de la cadena) en el disco etiquetado como **Transfer-\[***HQ-CA-02***\]** (para transferirlo de nuevo a la CA emisora).
  
#### Instalación del certificado de CA emisora
  
Las tareas de esta sección garantizan que la información de entidad emisora raíz publicada anteriormente en Active Directory se puede descargar en la CA emisora. A continuación, el certificado de CA emisora podrá instalarse en la entidad emisora.
  
##### Actualización de la información de certificado de la CA emisora
  
El certificado de entidad emisora raíz se publicó con anterioridad en el almacenamiento raíz de confianza de Active Directory. Ahora debe asegurarse de que la CA emisora ha descargado esta información y ha situado el certificado en su propio almacenamiento raíz.
  
**Para actualizar la información de confianza del certificado en la CA emisora**
  
1.  Inicie sesión en la CA emisora como administrador local.
  
2.  Ejecute el siguiente comando en el símbolo del sistema:
  
    certutil –pulse
  
Este comando forzará a la entidad emisora a descargar la información de raíz de confianza del directorio y colocar el certificado de entidad emisora raíz en su almacenamiento raíz de confianza local.
  
**Nota:** este procedimiento no es estrictamente necesario, ya que el último paso de la instalación del certificado en la entidad emisora colocará automáticamente el certificado de entidad emisora raíz en su almacenamiento raíz de confianza. Sin embargo, este paso le permite comprobar que los pasos de publicación anteriores de Active Directory se han completado correctamente. Es fundamental que esta publicación se realice correctamente, ya que todos los clientes del dominio recibirán su información de confianza acerca de las entidades emisoras y raíz de Active Directory.
  
**Para comprobar la descarga de confianza de entidad emisora raíz de Active Directory**
  
1.  Ejecute mmc.exe y agregue el complemento **Certificados**.
  
2.  Seleccione **Cuenta de equipo** como el almacén de certificados que se administrará.
  
3.  Compruebe que el certificado de entidad emisora raíz se encuentre en la carpeta Entidades emisoras de certificados raíz de confianza (los certificados se enumeran con la forma descriptiva del nombre de asunto de entidad emisora, es decir, el elemento CN).
  
##### Instalación del certificado
  
Ya puede instalarse la respuesta firmada (el paquete PKCS\#7 que contiene el certificado) de la entidad emisora raíz en la CA emisora. Para publicar correctamente el certificado de entidad emisora en el almacén NTAuth de Active Directory (que identifica a la entidad emisora como entidad emisora de certificados de empresa), debe instalar el certificado de entidad emisora mediante una cuenta que sea miembro *tanto* del grupo de administradores de PKI de empresa como del grupo de administradores locales. El primer grupo tiene derechos para publicar el certificado en el directorio, mientras que el segundo tiene derechos para instalar el certificado de entidad emisora en el servidor de entidad emisora. Si utiliza el modelo simple de administración sugerido anteriormente, la función CAAdmin es miembro de ambos grupos.
  
**Para instalar el certificado de CA emisora**
  
1.  Inicie sesión en la CA emisora utilizando una cuenta que sea miembro tanto del grupo de administradores de PKI de empresa como del grupo de administradores locales.
  
2.  Inserte el disco (**Transfer-\[***HQ-CA-02***\]**) que contenga el certificado emitido por la entidad emisora raíz.
  
3.  En la consola de administración Entidad emisora de certificados, en el menú **Tarea** de la entidad emisora, seleccione **Instalar certificado** e instale el certificado de CA emisora desde el disco.
  
Debe iniciarse la entidad emisora.
  
#### Comprobación de la instalación de la CA emisora
  
Puede comprobar que la instalación de los Servicios de Certificate Server ha sido correcta como se indica a continuación:
  
**Para comprobar la instalación de la CA emisora**
  
1.  Abra la consola de administración Entidad emisora de certificados. Compruebe que se han iniciado los Servicios de Certificate Server y que puede ver las propiedades de la CA.
  
2.  En la ficha **General**, seleccione el certificado de entidad emisora (o **Certificado nº 0** si se muestran varios certificados) y, a continuación, haga clic en **Ver certificado**.
  
3.  En la ficha **Detalles** del certificado de entidad emisora compruebe que los valores que se muestran coinciden con los de la tabla siguiente.
  
    **Tabla 7.22: Propiedades y extensiones de certificado de CA emisora**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Atributo del certificado</th>
    <th style="border:1px solid black;" >Opción requerida</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Emisor</td>
    <td style="border:1px solid black;">Nombre común de entidad emisora raíz (más sufijo DN)</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Asunto</td>
    <td style="border:1px solid black;">Nombre común de CA emisora (más sufijo DN)</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">No antes de - No después de</td>
    <td style="border:1px solid black;">8 años</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Longitud de la clave pública</td>
    <td style="border:1px solid black;">2048 bits</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Uso de claves</td>
    <td style="border:1px solid black;">Firma digital, Firma de certificados, Firma CRL sin conexión, Firma CRL (86)</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Restricciones básicas (esenciales)</td>
    <td style="border:1px solid black;">Tipo de asunto=CA
    Restricción de longitud de ruta=Ninguna</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Puntos de distribución de CRL</td>
    <td style="border:1px solid black;">2 entradas — Direcciones URL HTTP y LDAP</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Acceso a la información de entidad emisora</td>
    <td style="border:1px solid black;">2 entradas — Direcciones URL HTTP y LDAP</td>
    </tr>
    </tbody>
    </table>
  
    La presencia del tipo de sujeto Restricciones básicas es muy importante porque este valor distingue el certificado de entidad emisora del certificado de una entidad final. Además, aparecerá en la lista otra extensión, **Identificador de clave de entidad emisora**, que no aparece en el certificado de entidad emisora raíz. Este valor debe coincidir con **Identificador de clave de asunto** del certificado de entidad emisora raíz.
  
    Si alguno de los valores anteriores no es el que esperaba, debe volver a iniciar la instalación de Servicios de Certificate Server.
  
    **Nota:** si vuelve a ejecutar la instalación de Servicios de Certificate Server, aparecerá una advertencia de que la clave privada ya existe. Si está seguro de que no ha emitido ningún certificado con esta clave, puede omitir la advertencia y generar una clave nueva. Si la entidad emisora ya ha emitido certificados (además de los de prueba), no se debe reinstalar Servicios de Certificate Server hasta que se haya hecho una copia de seguridad segura de la clave y el certificado anterior (este procedimiento se describe en el capítulo 11, "Administración de la infraestructura de claves públicas").
  
4.  Consulte los datos de la ficha **Ruta de certificación** y compruebe que el certificado de CA emisora se ajusta correctamente a la entidad emisora raíz.
  
5.  Para una comprobación adicional o para solucionar los errores que se produzcan, puede consultar el registro de configuración de Servicios de Certificate Server (%systemroot%\\certocm.log).
  
#### Configuración de las propiedades de la CA emisora
  
El procedimiento de configuración de la entidad emisora aplica una serie de parámetros específicos del entorno. Los valores de dichos parámetros se documentan en una sección anterior del capítulo, "Hoja de trabajo de planeamiento de los Servicios de Certificate Server". Este procedimiento configura las propiedades de la entidad emisora tal como se describen en la siguiente tabla.
  
**Tabla 7.23: Propiedades de la entidad emisora que se deben configurar**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Propiedad de la CA</th>
<th style="border:1px solid black;" >Descripción de la opción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Direcciones URL de punto de distribución de la CRL</td>
<td style="border:1px solid black;">Especifica las ubicaciones HTTP, LDAP y FILE desde las que se puede obtener una lista CRL actual.<br/><br/>
La ubicación FILE es una carpeta local que utiliza la entidad emisora para almacenar las listas CRL que emite. Los certificados que se emiten sólo incluyen las ubicaciones HTTP y LDAP.<br/><br/>
La dirección URL de LDAP se enumera de forma secuencial antes de la HTTP, de modo que los controladores de dominio serán los destinatarios preferidos de descargas de listas CRL, pero consulte la nota que sigue a la tabla.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Direcciones URL de AIA</td>
<td style="border:1px solid black;">Ubicaciones donde se pueden obtener los certificados de entidad emisora.<br/><br/>
Al igual que con los CDP, la ubicación del archivo sólo se utiliza para publicar el certificado de entidad emisora y la dirección URL de LDAP tiene prioridad sobre la de HTTP, pero consulte la nota que sigue a la tabla.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de validez</td>
<td style="border:1px solid black;">Período de validez máximo de los certificados emitidos (no es el mismo que el período de validez del certificado de entidad emisora, que se establece en CAPolicy.inf o mediante la CA principal).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de la CRL</td>
<td style="border:1px solid black;">Frecuencia de publicación de la CRL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de coincidencia de lista CRL</td>
<td style="border:1px solid black;">Período de coincidencia desde la emisión de una nueva CRL y la fecha de caducidad de la CRL anterior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de diferencia entre listas CRL</td>
<td style="border:1px solid black;">Frecuencia de publicación de diferencia entre listas CRL.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Coincidencia de diferencia entre listas CRL</td>
<td style="border:1px solid black;">Período de coincidencia desde la emisión de una nueva CRL y la fecha de caducidad de la CRL anterior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditoría de CA</td>
<td style="border:1px solid black;">Configuración de auditoría de CA. De forma predeterminada, toda la auditoría está habilitada.</td>
</tr>
</tbody>
</table>
  
**Importante:** si necesita compatibilidad para clientes que no sean del dominio (según se ha descrito en el capítulo 4, "Diseño de la infraestructura de claves públicas"), debe cambiar el orden de las entradas CDP y AIA para que la entrada HTTP tenga mayor prioridad. Para cambiar este orden, tiene que editar la secuencia de comandos de configuración de entidad emisora (ca\_setup.vbs) o utilizar la MMC Entidad emisora de certificados para cambiar manualmente las entradas CDP y AIA. Debido a que las direcciones URL de LDAP sólo funcionan de forma confiable para los clientes del dominio, puede optar por utilizar únicamente direcciones URL de HTTP. Si lo hace así, debe asegurarse de que los servidores Web que alojan los puntos de publicación AIA y CDP de HTTP son resistentes.
  
**Para configurar las propiedades de la CA emisora**
  
1.  Inicie la sesión en el servidor de la CA como miembro del grupo de administradores.
  
2.  Al configurar la entidad emisora raíz, debe haber personalizado la secuencia de comandos C:\\MSSScripts\\pkiparams.vbs en función de la configuración específica de la organización. Es necesario replicar estos cambios en la copia de C:\\MSSScripts\\pkiparams.vbs que ha instalado en la CA emisora.
  
3.  A continuación, ejecute la siguiente secuencia de comandos:
  
    Cscript //job:IssCAConfig C:\\MSSScripts\\ca\_setup.wsf
  
##### Configuración de funciones administrativas
  
Para utilizar las funciones administrativas en la entidad emisora (como auditor y administrador de certificados), debe asignar los grupos de seguridad a dichas funciones.
  
**Nota:** esta solución utiliza los grupos creados anteriormente para definir varias funciones independientes. Este enfoque proporciona máxima flexibilidad para delegar responsabilidades en la administración de entidad emisora de certificados. Sin embargo, si no requiere este grado de delegación, es recomendable utilizar el modelo de grupo de administración simplificado especificado anteriormente en el capítulo. Este modelo simplificado le permitirá utilizar un número menor de cuentas para realizar las funciones administrativas de entidad emisora de certificados.
  
**Para configurar funciones administrativas en la CA emisora**
  
1.  En la consola de administración Entidad emisora de certificados, haga clic en **Propiedades** para editar las propiedades de la entidad emisora.
  
2.  Haga clic en la ficha **Seguridad** y agregue los grupos de seguridad del dominio que se enumeran en la tabla siguiente. Para cada grupo, agregue los permisos que se muestran.
  
    **Tabla 7.24: Entradas de permisos de entidad emisora de certificados que deben agregarse**

    <p> </p>
    <table style="border:1px solid black;">
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de grupo</th>
    <th style="border:1px solid black;" >Permiso</th>
    <th style="border:1px solid black;" >Permitir o denegar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Administradores de entidad emisora</td>
    <td style="border:1px solid black;">Administración de entidad emisora de certificados</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Administradores de certificados</td>
    <td style="border:1px solid black;">Emisión y administración de certificados</td>
    <td style="border:1px solid black;">Permitir</td>
    </tr>
    </tbody>
    </table>
  
    **Nota:** si desea forzar la separación total de funciones, debe quitar los permisos de administración de entidad emisora del grupo local Administradores.
  
3.  Existen otras funciones de seguridad de entidad emisora que requieren una configuración adicional (aunque se han definido parcialmente a través de la directiva de seguridad aplicada previamente al servidor):
  
    -   Se han concedido derechos de usuario de administración de registros de auditoría y seguridad a los auditores de entidad emisora. Agregue este grupo al grupo de administradores locales.
  
    -   Se han concedido derechos de copia de seguridad y restauración de la entidad emisora para los operadores de copia de seguridad de entidad emisora. Este grupo no necesita más configuración.
  
#### Publicación de información de CA emisora
  
Los certificados y CRL se publican automáticamente desde la CA emisora en Active Directory. No obstante, la publicación del certificado y las listas CRL de entidad emisora en las rutas de acceso CDP y AIA de HTTP no es automática; debe configurar un trabajo programado para realizar estas tareas.
  
##### Publicación de certificados y listas CRL de CA emisora en el servidor Web
  
Los certificados y listas CRL de CA emisora deben publicarse en las ubicaciones AIA y CDP de HTTP, respectivamente. Técnicamente, es posible configurar la entidad emisora para que publique directamente en la carpeta del servidor Web. Si dicho servidor está alojado en la CA emisora, esto resulta muy fácil. Sin embargo, no siempre resulta posible por motivos de seguridad y conectividad de red. El siguiente método utiliza una técnica de copia de archivos simple que puede ampliarse para adaptarse a la mayor parte de configuraciones.
  
**Nota:** este método no resulta adecuado para publicar directamente en un servidor Web conectado a Internet porque requiere conectividad de red directa y utilizar el uso compartido de archivos de red de Windows, que normalmente se bloquea en los servidores de seguridad de Internet. Para publicar en un servidor de Internet, utilice el procedimiento siguiente para publicar en una ubicación intermedia y, a continuación, utilice el método estándar que desee para publicar contenido en el servidor Web de forma segura. Debe tener en cuenta el efecto que este paso adicional puede tener en la actualización de las listas CRL.
  
El certificado de entidad emisora se actualiza con poca frecuencia, por lo que puede publicar en AIA manualmente cuando se renueve el certificado de entidad emisora.
  
**Para publicar el certificado de CA emisora**
  
1.  Inicie la sesión en la CA emisora con una cuenta que disponga de permisos de escritura en la carpeta del servidor Web publicada.
  
2.  Si el servidor Web se encuentra en un servidor remoto, asegúrese de que la carpeta del servidor Web esté compartida. Anote la ruta de acceso UNC de la carpeta compartida.
  
3.  Si el servidor Web está en el mismo servidor que la entidad emisora, anote la ruta de acceso local de la carpeta.
  
4.  Actualice el parámetro WWW\_REMOTE\_PUB\_PATH en C:\\MSSScripts\\PKIParams.vbs para que coincida con la ruta de acceso de destino de la carpeta del servidor Web (el valor predeterminado es la ruta local C:\\CAWWWPub).
  
5.  Ejecute el siguiente comando para publicar el certificado de entidad emisora en el servidor Web:
  
    Cscript //job:PublishIssCertsToIIS
  
    C:\\MSSScripts\\CA\_Operations.wsf
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
Las listas CRL se emiten desde la CA emisora de forma más periódica (cada día o cada hora en el caso de diferencia entre listas CRL) que el certificado de entidad emisora, de modo que se requiere un método automatizado para replicar las listas CRL en el servidor Web.
  
**Para automatizar la publicación de las listas CRL**
  
1.  Inicie sesión en la CA emisora con una cuenta miembro del grupo de administradores locales.
  
2.  Asegúrese de que se pueda obtener acceso a la carpeta del servidor Web (como carpeta compartida o como ruta de acceso local) desde este servidor.
  
3.  Si el servidor Web es remoto, conceda acceso de escritura a la CA emisora para la carpeta del sistema de archivos (permitiendo el acceso **Modificar**) y para la carpeta compartida (permitiendo el acceso **Cambiar**). Si el servidor Web es miembro del bosque, puede utilizar el grupo Publicadores de certificados del dominio para conceder acceso.  Esto garantizará que cualquier entidad emisora de empresa del dominio tenga los permisos necesarios para publicar certificados y listas CRL en esta carpeta. No es necesario modificar los permisos de servidor Web (consulte la sección anterior acerca de la configuración de IIS para la publicación de CDP y AIA).
  
4.  Cree un trabajo programado para copiar las listas CRL mediante la ejecución del comando siguiente:
  
    schtasks /create /tn "Publicar listas CRL" /tr "cscript.exe
  
    //job:PublishIssCRLsToIIS C:\\MSSScripts\\CA\_Operations.wsf"
  
    /sc Hourly /ru "Sistema"
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
    **Nota:** con este procedimiento se creará un trabajo programado por horas para publicar las listas CRL en el servidor Web. Esta frecuencia es suficiente para hacer frente a un programa de publicación de diferencia entre listas CRL cada día o incluso cada medio día. Si el programa de CRL es más frecuente, haga que la tarea programada se ejecute con mayor frecuencia. Una buena referencia es que el programa de trabajo debe ser del cinco al diez por ciento del programa de diferencia entre listas CRL.
  
##### Comprobación de la publicación de información de la CA emisora
  
Es necesario comprobar que la publicación de información de la CA emisora se haya realizado correctamente. Para realizar estos pasos, debe iniciar la sesión en un equipo miembro del dominio conectado a la red y utilizar una cuenta de dominio válida.
  
**Para comprobar la publicación de información de la CA emisora**
  
1.  Para comprobar la publicación del certificado de entidad emisora en el almacenamiento de entidad emisora intermedia, ejecute el comando siguiente:
  
    certutil -viewstore -enterprise CA
  
2.  Deben aparecer dos certificados: uno para la entidad emisora raíz y otro para la CA emisora. Haga doble clic en el certificado de CA emisora y compruebe que el nombre **Asunto** coincida con el que haya configurado para la CA emisora y que la fecha **Válido desde** sea la fecha actual.
  
3.  Para comprobar la publicación del certificado de entidad emisora en el almacenamiento de entidad emisora NTAuth (donde todas las entidades emisoras de certificados de empresa se publican), ejecute el comando siguiente:
  
    certutil -viewstore -enterprise NTAuth
  
    Debe aparecer el mismo certificado mostrado para la CA emisora.
  
4.  Para comprobar la publicación de la lista CRL de CA emisora, ejecute el comando siguiente, reemplazando los elementos en cursiva con los valores de la instalación (nombre común de entidad emisora, nombre corto de host de entidad emisora y DN de raíz de bosque de Active Directory):
  
    certutil -store -enterprise "ldap:///cn=*Entidad emisora de Woodgrove Bank 1*,cn=*HQ-CA-02*,cn=CDP,CN=Public Key Services, CN=Services,CN=Configuration,DC=*woodgrovebank*,DC=*com*?certificateRevocationList?base?objectClass= cRlDistributionPoint"
  
    (Este comando se muestra en varias líneas; escríbalo en una sola.)
  
5.  Los resultados deberán ser similares a los siguientes. Compruebe que el valor **Emisor** coincida con el nombre que haya configurado para la CA emisora:
  
    ================ CRL 0 ================
  
    Emisor: CN= Entidad emisora de WoodGrove Bank,DC=woodgrovebank,DC=com
  
    Versión de entidad emisora: V1.0
  
    Número CRL: Número CRL=1
  
    Hash de CRL (sha1): 73 03 a1 c7 5f a3 c3 f9 8a 09 d0 3c b5 09 00 9c b5 a3 de fe
  
    CertUtil: -comando de almacenamiento completado correctamente.
  
6.  Para comprobar la publicación del certificado de entidad emisora en el servidor Web, escriba la dirección URL siguiente en un explorador y reemplace los elementos en cursiva por los valores utilizados en su propia instalación:
  
    http://*www.woodgrovebank.com*/pki/*HQ-CA-02\_WoodGrove Bank Issuing CA 1*.crt
  
7.  Se le solicitará que abra o guarde el archivo. Ábralo y compruebe que aparezca el certificado de CA emisora.
  
8.  Para comprobar la publicación de la lista CRL de CA emisora en el servidor Web, escriba la dirección URL siguiente en un explorador y reemplace los elementos en cursiva por los valores reales utilizados en su instalación:
  
    http://*www.woodgrovebank.com*/pki/*WoodGrove Bank Issuing CA 1*.crl
  
9.  Se le solicitará que abra o guarde el archivo. Ábralo y compruebe que aparezca la lista CRL de la entidad emisora raíz.
  
    **Nota:** si dispone de un certificado de entidad emisora renovado o ha emitido más de una lista CRL, pueden aparecer números de versión diferentes en los resultados de estos comandos.
  
#### Comprobación de la inscripción de certificados
  
Debe comprobar que puede inscribir certificados desde la CA emisora.
  
**Para comprobar la inscripción de certificados**
  
1.  Inicie sesión en un equipo del mismo dominio que la CA emisora. Utilice una cuenta de dominio.
  
2.  Abra el complemento Certificados de MMC para el usuario actual. (Tendrá que agregar este complemento en una MMC en blanco con **Agregar o quitar complemento** porque no hay uno predefinido.)
  
3.  Haga clic con el botón secundario del mouse en la carpeta Personal y seleccione **Solicitar un nuevo certificado** desde el submenú **Todas las tareas**.
  
4.  Se le mostrará una lista de tipos de certificado para que elija uno. Debe elegir el tipo **Usuario**. No active la casilla de verificación **Opciones avanzadas**.
  
5.  Asigne un nombre reconocible y descriptivo al certificado, como **Comprobación de CA emisora**.
  
6.  Haga clic en **Finalizar** para inscribir el certificado.
  
7.  Desplácese hasta la carpeta Certificados de la carpeta personal. Debe ver el certificado **Comprobación de CA emisora**. (Es posible que primero tenga que actualizar el almacén haciendo clic con el botón secundario en el objeto raíz **Certificados-Usuario actual** en el panel izquierdo de la MMC y, a continuación, haciendo clic en **Actualizar**.)
  
Si se produce un error en la prueba de comprobación, debe revisar los pasos de este capítulo y rectificar los problemas que identifique. Si sigue teniendo problemas, consulte la sección "Solución de problemas" del capítulo 11, "Administración de la infraestructura de claves públicas".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración posterior a la creación
  
Aunque ya ha creado la entidad emisora raíz y la CA emisora para la organización, todavía quedan algunas tareas de configuración importantes que deben realizarse. Se describen en esta sección.
  
#### Configuración de plantillas de certificado
  
La mayoría de estas tareas están relacionadas con la configuración de los tipos de certificado que pueden emitir las CA emisoras, quién controla la emisión y para quién o qué se emiten los certificados.
  
##### Eliminación de plantillas no deseadas de la CA emisora
  
Hasta que necesite un tipo de certificado, es una práctica recomendada quitar la plantilla correspondiente de la configuración de entidad emisora para que los certificados no se emitan accidentalmente. No obstante, las plantillas siempre están disponibles en el directorio y se pueden volver a agregar si es necesario.
  
**Para quitar plantillas no deseadas de la CA emisora**
  
1.  Inicie sesión como miembro del grupo de dominio Administradores de entidad emisora.
  
2.  Desde la entidad emisora de MMC, seleccione el contenedor Plantillas de certificado.
  
3.  Quite los tipos de plantilla siguientes:
  
    -   Agente de recuperación de EFS
  
    -   EFS básico
  
    -   Servidor Web
  
    -   Equipo
  
    -   User
  
    -   Entidad emisora de certificados subordinada
  
    -   Administrador
  
        **Nota:** este procedimiento elimina todas las plantillas de la CA emisora excepto las de Controlador de dominio, Autenticación de controlador de dominio y Replicación de directorio de correo electrónico. Los controladores de dominio de Windows 2000 utilizan certificados de Controlador de dominio para habilitar el inicio de sesión de tarjeta inteligente y la replicación de Active Directory de protocolo simple de transferencia de correo (SMTP). Los controladores de dominio de Windows Server 2003 utilizan certificados de Autenticación de controlador de dominio para admitir el inicio de sesión de tarjeta inteligente y LDAP seguro, así como utilizar el certificado Replicación de directorio de correo electrónico para la replicación de Active Directory de SMTP.  
        Todas las plantillas eliminadas se pueden volver a agregar en el futuro si es necesario. Mientras tanto, es una práctica recomendada permitir únicamente los tipos de certificado cuya emisión se haya elegido deliberadamente.
  
##### Creación y administración de plantillas de certificado
  
Las plantillas de certificados de empresa se pueden administrar y utilizar de forma eficaz con grupos de seguridad. Estos grupos pueden controlar los usuarios que pueden modificar las propiedades de cada plantilla y los usuarios que pueden inscribir certificados de dicho tipo.
  
**Nota:** los grupos de administración de plantillas resultan útiles cuando existe la posibilidad de delegar el control sobre las plantillas a administradores distintos. Si su estructura de administración de PKI no es grande o compleja, es probable que no se requiera esta capacidad. En tal caso, sólo podrán administrar las plantillas de certificado los miembros del grupo de administradores de organización integrado y del grupo de administradores de PKI de empresa (creados como parte de esta solución).
  
Para obtener instrucciones acerca de la creación y el mantenimiento de grupos de administración de plantillas de certificado, consulte los procedimientos operativos documentados en el capítulo 11, "Administración de la infraestructura de claves públicas".
  
Para obtener instrucciones acerca de la creación de plantillas de certificado específicas para esta solución, consulte la sección "Configuración e implementación de certificados de autenticación de LAN inalámbricas" del capítulo 9, "Implementación de la infraestructura de seguridad para LAN inalámbricas".
  
Para obtener instrucciones generales acerca de la creación y modificación de plantillas de certificados, consulte la sección "Administración de plantillas de certificado" de la documentación del producto y el documento técnico, *Implementing and Administering Certificate Templates in Windows Server 2003*. (Consulte la sección de referencia al final de este capítulo.)
  
##### Administración de inscripción de certificados
  
Los grupos de inscripción de plantillas facilitan la administración de los usuarios que se pueden inscribir o se inscriben automáticamente para un determinado tipo de certificado. Los usuarios se pueden agregar o quitar de un grupo de seguridad. El control sobre la pertenencia a grupos del grupo de inscripción de plantillas también se puede conceder al personal administrativo que no desee que edite directamente las propiedades de las plantillas de certificado.
  
Para obtener instrucciones acerca de la creación y el mantenimiento de grupos de inscripción de plantillas de certificado, consulte el capítulo 11, "Administración de la infraestructura de claves públicas".
  
#### Establecimiento de permisos para la implementación en dominios múltiples
  
Si va a implementar esta solución en un bosque con múltiples dominios, es posible que tenga que emitir certificados a usuarios y equipos en dominios distintos al de la entidad emisora. Si es así, tendrá que cambiar el valor predeterminado de los permisos para permitir que las entidades emisoras publiquen correctamente certificados en otros dominios del bosque de Active Directory.
  
Al establecer permisos de inscripción para usuarios en entidades emisoras y plantillas de certificado, debe incluir explícitamente usuarios y equipos de todos los dominios en que desee que dichos usuarios y equipos puedan inscribir certificados.
  
**Para permitir la publicación de certificados a usuarios y equipos de otros dominios**
  
1.  Inicie sesión en un miembro del dominio en que desee habilitar la publicación de certificados. Debe ser un miembro del grupo de administradores para este dominio o un miembro de un grupo con derechos suficientes para cambiar permisos en el objeto de dominio.
  
2.  Abra el complemento Usuarios y equipos de Active Directory de MMC y haga clic con el botón secundario del mouse en el nodo de dominio.
  
    **Nota:** puede realizar esta operación desde otro dominio siempre que la cuenta tenga los permisos correctos en el dominio de destino. Tiene que conectarse al dominio de destino desde Usuarios y equipos de Active Directory.
  
3.  Haga clic en **Delegar control** para iniciar el Asistente para nueva delegación.
  
4.  En el asistente, haga clic en **Siguiente** y, a continuación, agregue el grupo Publicadores de certificados del dominio en que instaló la CA emisora. A continuación, haga clic en **Siguiente**.
  
5.  Seleccione **Crear una tarea personalizada para delegar** y haga clic en **Siguiente**.
  
6.  Seleccione **Sólo los siguientes objetos** **en la carpeta**.
  
7.  Seleccione los **Objetos de usuario** y haga clic en **Siguiente**.
  
8.  Seleccione la opción **Específico de la propiedad**.
  
9.  Seleccione las opciones **Leer userCertificate** y **Escribir userCertificate**.
  
10. Haga clic en **Siguiente** y, a continuación, haga clic en **Finalizado**.
  
11. Repita los pasos del 3 al 10, pero en el paso 7 seleccione **Objetos de equipo** en lugar de **Objetos de usuario**.
  
Este procedimiento garantiza que las entidades emisoras de empresa tienen permiso para publicar correctamente certificados para usuarios y equipos en este dominio.
  
#### Copia de seguridad de claves y servidores de entidad emisora
  
Una vez creadas la entidad emisora raíz y la CA emisora, debe realizar una copia de seguridad de las mismas tan pronto como sea posible para proteger sus claves y bases de datos de certificados de posibles errores o corrupciones de datos.
  
Realice los siguientes procedimientos según lo documentado en el capítulo 11, "Administración de la infraestructura de claves públicas".
  
-   "Configuración de la copia de seguridad de la CA emisora"
  
-   "Configuración y realización de la copia de seguridad de la entidad emisora raíz"
  
-   "Copia de seguridad de claves y certificados de entidad emisora" (esta tarea debe realizarse para cada entidad emisora)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de cliente
  
En esta sección se describen una serie de tareas de configuración de cliente importantes. Son sólo unas pocas porque la mayoría de las configuración relacionada con el cliente es específica de la aplicación o servicio que utiliza Servicios de Certificate Server, como WLAN o redes privadas virtuales (VPN), en lugar de tareas comunes a todas las aplicaciones de certificados.
  
#### Habilitación de la inscripción automática de certificados de usuario y equipo
  
Las medidas descritas en la sección anterior, "Administración de inscripción de certificados", permiten utilizar grupos de seguridad y permisos de plantilla para controlar la inscripción automática en un nivel muy preciso. No obstante, la capacidad de inscripción automática de los clientes de Windows XP está deshabilitada de forma predeterminada. Para habilitarla, debe configurar la configuración correcta en Directiva de grupo. Si utiliza grupos de seguridad para controlar la inscripción automática, puede habilitar la capacidad de inscripción automática para todos los usuarios y equipos del dominio y utilizar los grupos de seguridad de inscripción para determinar los usuarios que reciben los certificados de cada tipo.
  
**Precaución:** este procedimiento habilita la inscripción automática para *todos* los equipos y usuarios del dominio. Asegúrese de haber quitado las plantillas predeterminadas de la CA emisora antes de iniciar este procedimiento para evitar que todos los certificados de equipo y usuario predeterminados se inscriban en cada equipo y usuario del dominio. En este procedimiento se supone que controlará la inscripción automática mediante grupos de seguridad, como se describe en el capítulo 11, "Administración de la infraestructura de claves públicas".
  
**Para habilitar la inscripción automática para todos los usuarios y equipos del dominio**
  
1.  Inicie sesión con una cuenta que tenga permisos para crear GPO (un miembro del grupo de propietarios del creador de directivas de grupo) y vincularlos al dominio. También puede pedir que un administrador del dominio cree y vincule el GPO y que le otorgue permisos de lectura y escritura para el mismo.
  
2.  En Usuarios y equipos de Active Directory, seleccione el objeto de dominio, haga clic con el botón secundario del mouse en éste y, a continuación, haga clic en **Propiedades**.
  
3.  En la ficha **Directiva de grupo**, haga clic en **Nuevo** y escriba un nombre para el GPO (por ejemplo, *Directivas de PKI de dominio*).
  
4.  Haga clic en **Editar** para editar el GPO y desplazarse hasta Directivas de claves públicas en Configuración del equipo\\Configuración de Windows\\Configuración de seguridad.
  
5.  En el panel de detalles, haga doble clic en **Configuración de inscripción automática**.
  
6.  Compruebe que los elementos siguientes estén seleccionados:
  
    -   **Registrar certificados automáticamente**
  
    -   **Renovar certificados caducados, actualizar certificados pendientes y quitar certificados revocados**
  
    -   **Actualizar certificados que usan plantillas de certificados**
  
7.  Repita los pasos 5 y 6 para Configuración de inscripción automática de usuario en Configuración de usuario\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas.
  
8.  Cierre el GPO.
  
9.  Asegúrese de que el GPO tenga una prioridad mayor que el GPO de la directiva de dominio predeterminada.
  
    **Notas:**  
    Si tiene un bosque de Active Directory de dominios múltiples, debe realizar este procedimiento para cada dominio del bosque en el que desee habilitar la inscripción automática de certificados.  
    Si no desea habilitar la inscripción automática para todos los usuarios o equipos del dominio, puede crear GPO vinculados a las UO que contengan el subconjunto de usuarios y/o equipos para los que desee habilitar la inscripción automática.  
    Si los usuarios no utilizan perfiles itinerantes y permite la inscripción automática de forma universal, los certificados se inscribirán para los usuarios en cada equipo en que inicien sesión. Puede impedir que los administradores y los operadores inscriban automáticamente certificados cuando inicien sesión en los servidores. puede crear un GPO que se aplique a dichos servidores (por ejemplo, vinculándolos a la UO de servidores). En este GPO, deshabilite la inscripción automática para los usuarios seleccionando **No registrar certificados automáticamente**. En el mismo GPO, habilite el procesamiento de bucle invertido de GPO habilitando el **Modo de procesamiento de bucle invertido de la directiva de grupo de usuario de Configuración del equipo\\Plantillas administrativas\\Sistema\\Directiva de grupo** y seleccionando la opción **Reemplazar**.
  
La habilitación de la inscripción automática de certificados también se describe detalladamente en los documentos que se enumeran en la sección "Información adicional", al final de este capítulo.
  
Sólo los clientes con Windows XP y posterior admiten la inscripción automática de certificados de usuario y de equipo. Los clientes con Windows 2000 sólo admiten la inscripción automática de certificados de equipo (aunque algunas aplicaciones como EFS tienen sus propios mecanismos de inscripción automática para los certificados de usuario).
  
Si va a implementar esta solución en un entorno de Active Directory de Windows 2000, debe editar la configuración de inscripción automática en los GPO desde un equipo con Windows Server 2003 o Windows XP Professional con las herramientas de administración de Windows Server 2003 instaladas (Windows XP requiere un nivel de Service Pack y revisión específico para admitir lar herramientas de administración de Windows Server 2003).
  
#### Configuración de directivas de dominio de entidad emisora raíz
  
En esta sección se describe cómo administrar las entidades emisoras de certificados raíz comerciales en las que confían los clientes de la organización y el control que desea tener sobre si los usuarios individuales pueden cambiar las entidades emisoras de certificados raíz en las que confían.
  
##### Administración de confianza de otros fabricantes
  
De forma predeterminada, los clientes de Windows están configurados para confiar en un gran número de entidades emisoras de certificados raíz comerciales (conocidas como raíces asimiladas). Si desea evitar que los usuarios confíen automáticamente en estas entidades emisoras raíz de terceros, existe un procedimiento en la sección "To prevent users from trusting third-party root certification authorities with a Group Policy" de la ayuda en pantalla. También hay un vínculo a un artículo acerca de este tema en la sección "Información adicional".
  
**Nota:** la deshabilitación de raíces de otros fabricantes puede provocar errores en aplicaciones cliente, de modo que no debe hacerlo sin probar correctamente las consecuencias. Por ejemplo, las conexiones cliente a la mayoría de sitios Web seguros provocarán un error de confianza.
  
Puede corregir algunos problemas quitando todas las confianzas de otros fabricantes de distintas formas:
  
-   Puede volver a agregar raíces individuales de forma selectiva agregándolas a la configuración de la directiva Entidades emisoras de certificados raíz de confianza en la directiva de grupo.
  
-   Puede agregar los certificados raíz a listas de certificados de confianza e implementarlos a través de la configuración de Confianza empresarial de la directiva de grupo. Este método también le permite controlar los usos para los que confiará en los certificados que emiten las raíces. No obstante, debido a que tiene compatibilidad de cliente limitada, sólo se recomienda si no se dispone de otras alternativas.
  
-   Puede crear certificados cruzados (o crear una relación de confianza de subordinación completa) con otras entidades emisoras. Este método le proporciona todavía más control sobre los usos y parámetros de certificado en los que se confiará dentro de la organización.
  
El uso de listas de certificados de confianza o la subordinación completa son la forma más segura de implementar raíces de confianza de otros fabricantes en la organización. Este tema se trata con más detalle en el capítulo 4, "Diseño de la infraestructura de claves públicas".
  
##### Administración del control de usuario sobre raíces de confianza
  
También puede utilizar Directiva de grupo para evitar que los usuarios opten por confiar en entidades emisoras de certificados raíz nuevas. Esto es especialmente importante si ha creado confianzas de subordinación completa o una lista de certificados de confianza para controlar el uso de certificados de otros fabricantes en la organización. Puede encontrar el procedimiento para utilizar Directiva de grupo con el fin de administrar el control de usuario sobre raíces de confianza en la sección "To prevent users from selecting new root certification authorities with a Group Policy" de la ayuda en pantalla o desde el vínculo que se indica en la sección "Información adicional".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Si ha realizado todos los procedimientos de este capítulo, ha completado las siguientes tareas:
  
-   Instalación y configuración de una entidad emisora raíz sin conexión.
  
-   Instalación y configuración de una CA emisora en línea.
  
-   Instalación y configuración de un servidor Web para publicar listas CRL y certificados de entidad emisora.
  
-   Configuración de usuarios y grupos administrativos para administrar la información de configuración de PKI de Active Directory y las entidades emisoras.
  
-   Configuración de Active Directory y la directiva de grupo para que admitan la PKI.
  
Ahora ya está preparado para configurar aplicaciones para utilizar la PKI. Se describe en los dos siguientes capítulos de esta guía: capítulo 8, "Implementación de la infraestructura de RADIUS" y capítulo 9, "Implementación de la infraestructura de seguridad para LAN inalámbricas".
  
También debe leer las partes correspondientes del capítulo 11, "Administración de la infraestructura de claves públicas" y asegúrese de que el personal de operaciones pertinente dispone de los conocimientos adecuados. En este capítulo se incluye información fundamental acerca de cómo mantener el funcionamiento seguro y confiable de la PKI.
  
#### Información adicional
  
##### Información general acerca de PKI y Servicios de Certificate Server de Windows
  
-   Para obtener una introducción a los conceptos de PKI y las características de Servicios de Certificate Server de Windows 2000, consulte [*An Introduction to the Windows 2000 Public-Key Infrastructure*](http://www.microsoft.com/technet/archive/windows2000serv/evaluate/featfunc/pkiintro.mspx) en http://www.microsoft.com/technet/archive/windows2000serv/  
    evaluate/featfunc/pkiintro.mspx
  
-   Para ver una descripción de la funcionalidad mejorada de PKI en Windows Server 2003 y Windows XP PKI, consulte [*PKI Enhancements in Windows XP Professional and Windows Server 2003*](http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx) en http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx
  
-   Para obtener la documentación del producto que describe los conceptos clave y las tareas de administración, consulte la sección "Servicios de Certificate Server" de la ayuda en pantalla o la [sección de la infraestructura de claves públicas](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/se_pki.mspx) de la documentación del producto de Windows Server 2003 en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/proddocs/entserver/SE\_PKI.mspx
  
##### Información sobre temas específicos
  
-   Para obtener más información acerca de la implementación de una PKI en un entorno de Active Directory de bosques múltiples, consulte ["To publish certificates in a foreign Active Directory forest"](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_cs_procs_xforest_cert_pub.mspx) en la documentación del producto de Windows Server 2003 en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/proddocs/entserver/sag\_CS\_procs\_xforest\_cert\_pub.mspx.
  
-   CAPICOM se puede descargar del [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/details.aspx?displaylang=en&familyid=860ee43a-a843-462f-abb5-ff88ea5896f6) en http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=860EE43A-A843-462F-ABB5-FF88EA5896F6. No obstante, busque "CAPICOM" en el sitio del Centro de descarga para asegurarse de que obtiene la versión más reciente.
  
-   Para obtener instrucciones acerca de cómo utilizar Microsoft Baseline Security Analyzer (MBSA), consulte la página [Microsoft Baseline Security Analyzer v1.2](http://www.microsoft.com/technet/security/tools/mbsahome.mspx) en http://www.microsoft.com/technet/security/tools/mbsahome.mspx.
  
-   Para obtener información acerca de los niveles funcionales de dominio de Active Directory e instrucciones acerca de cómo cambiar de uno a otro, consulte las siguientes secciones de la documentación del producto de Windows Server 2003.
  
    -   En la [sección acerca de la funcionalidad de dominio y bosque](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_levels.mspx) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
        proddocs/entserver/sag\_levels.mspx se describen los distintos niveles de dominio y bosque.
  
    -   En la página titulada ["To raise the domain functional level"](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_changedomlevel.mspx) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
        proddocs/entserver/sag\_changedomlevel.mspx se describe el modo de cambiar el nivel de dominio y bosque.
  
-   Para obtener más información acerca de la herramienta ADPrep, consulte el artículo Q325379 de Microsoft Knowledge Base, "[How to upgrade Windows 2000 domain controllers to Windows Server 2003](http://support.microsoft.com/?kbid=325379)" en http://support.microsoft.com/?kbid=325379  
    y la página [ADPrep](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/adprep.mspx) en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/proddocs/entserver/adprep.mspx.
  
-   Para obtener más información acerca de los requisitos de nivel de revisión de ADPrep, consulte el artículo Q331161 de Microsoft Knowledge Base, ["Hotfixes to install on Windows 2000 domain controllers before running Adprep /Forestprep"](http://support.microsoft.com/?kbid=331161) en http://support.microsoft.com/?kbid=331161.
  
-   Para obtener una descripción más completa de Servicios de Certificate Server, consulte "[Managing role-based administration](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_cs_manage_role_based_admin_topnode.mspx)" en la documentación del producto de Windows Server 2003 en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/entserver/sag\_CS\_Manage\_Role\_based\_admin\_topnode.mspx.
  
-   Para obtener más información acerca de las funciones de seguridad y las funciones de servidor que se utilizan en esta guía, consulte la [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845), en http://www.microsoft.com/Spain/technet/seguridad/guias/guia\_ws2003.asp.
  
-   Para obtener información acerca de cómo crear y modificar plantillas de certificados, consulte el documento técnico [*Implementing and Administering Certificate Templates in Windows Server 2003*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03crtm.mspx) en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/echnologies/security/ws03crtm.mspx y la sección [Administrar plantillas de certificados para una entidad emisora de certificados de empresa.](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_cs_procs_temps.mspx) de la documentación del producto en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/entserver/sag\_CS\_procs\_temps.mspx.
  
-   Para obtener información acerca de cómo deshabilitar la confianza automática para entidades emisoras de terceros, consulte  
    ["To prevent users from trusting third-party root certification authorities with a Group Policy"](http://www.microsoft.com/resources/documentation/windowsserv/2003/enterprise/proddocs/en-us/sag_pkpprocsconfig3rdpartyrootca.asp) en http://www.microsoft.com/resources/documentation/  
    WindowsServ/2003/enterprise/proddocs/en-us/sag\_pkpprocsconfig3rdpartyrootca.asp.
  
-   Para obtener información acerca de cómo administrar el control de usuario sobre raíces de confianza, consulte  
    ["To prevent users from selecting new root certification authorities with a Group Policy"](http://www.microsoft.com/resources/documentation/windowsserv/2003/enterprise/proddocs/en-us/sag_pkpprocsconfigtrustedrootca.asp) en http://www.microsoft.com/resources/documentation/WindowsServ/  
    2003/enterprise/proddocs/en-us/sag\_pkpprocsconfigtrustedrootca.asp.
  
-   Para obtener más información acerca de la inscripción automática de certificados, consulte [*Certificate Autoenrollment in Windows XP*](http://www.microsoft.com/windowsxp/pro/techinfo/administration/autoenroll/default.asp) en http://www.microsoft.com/WindowsXP/pro/techinfo/  
    administration/autoenroll/default.asp y ["Checklist: Configuring certificate autoenrollment"](http://technet.microsoft.com/en-us/library/cc773385.aspx) en http://www.microsoft.com/resources/documentation/  
    WindowsServ/2003/datacenter/proddocs/en-us/certsrv\_checklist\_autoenroll.asp.
  
-   Para obtener más información acerca de la inscripción de certificados avanzada, consulte [Advanced Certificate Enrollment and Management](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/advcert.mspx) en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/technologies/security/advcert.mspx.
  
-   Para obtener más información acerca de la inscripción Web, consulte  
    [Configuring and Troubleshooting Windows 2000 and  
    Windows Server 2003 Certificate Services Web Enrollment](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/webenroll.mspx) en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/technologies/security/webenroll.mspx.
  
-   Para obtener más información acerca de la administración de una PKI de Windows (además de la información del capítulo 11, "Administración de la infraestructura de claves públicas"), consulte la [*Windows Server 2003 PKI Operations Guide*](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03pkog.mspx) en http://www.microsoft.com/technet/prodtechnol/  
    windowsserver2003/technologies/security/ws03pkog.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)