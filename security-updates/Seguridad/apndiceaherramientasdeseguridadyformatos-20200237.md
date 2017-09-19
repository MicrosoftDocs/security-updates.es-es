---
TOCTitle: 'Apéndice A: Herramientas de seguridad y formatos'
Title: 'Apéndice A: Herramientas de seguridad y formatos'
ms:assetid: 'bb480ff2-c590-4af4-8f5d-b8d09bb272bf'
ms:contentKeyID: 20200237
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163100(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Apéndice A: Herramientas de seguridad y formatos

Actualizado: 27/12/05

Puede ser un desafío crear, probar, implementar y administrar un conjunto completo de directivas y plantillas para su organización. Este apéndice proporciona información general sobre las herramientas disponibles de Microsoft y los formatos que pueden tener las directivas de seguridad.

##### En esta página

[](#ebaa)[Herramientas de seguridad](#ebaa)
[](#eaaa)[Formatos de los archivos de seguridad](#eaaa)

### Herramientas de seguridad

Las herramientas siguientes están disponibles con el sistema operativo Windows Server™ 2003 o como archivos que se pueden descargar gratuitamente del sitio web de Microsoft.

#### Asistente para configuración de seguridad

El Asistente para configuración de seguridad (SCW) se incorporó en el SP1 de Windows* *Server* *2003. A diferencia de la directiva de grupo, no está integrado con el servicio de directorio de Active* *Directory® y, por tanto, no se puede usar para configurar las directivas de nivel de dominio. Sin embargo, proporciona una metodología coherente de seguridad basada en funciones que utiliza asistentes, lo que facilita la creación de directivas seguras.

Con SCW, puede crear de un modo rápido y sencillo directivas prototipo para varias funciones de servidor que se basen en las últimas orientaciones y recomendaciones de Microsoft. SCW administrará automáticamente la configuración de servicios, la configuración del Registro, las excepciones del Firewall de Windows y mucho más. Incluye capacidad para crear de forma remota perfiles de equipos de destino, implementar directivas y revertir directivas. La herramienta de línea de comandos Scwcmd permite usar a la vez SCW y la directiva de grupo para implementar directivas en grupos de equipos o convertir directivas en objetos GPO.

#### Editor de configuración de seguridad

Las herramientas del Editor de configuración de seguridad (SCE) se utilizan para definir plantillas de directiva de seguridad que se pueden aplicar a equipos individuales o a grupos de equipos a través de la directiva de grupo de Active Directory. SCE apareció primero como un complemento de Windows NT® 4.0 y se ha convertido en una parte esencial de la directiva de grupo.

SCE ya no es un componente independiente y se utiliza en los siguientes complementos de Microsoft Management Console (MMC) y utilidades administrativas:

-   Complemento MMC Configuración y análisis de seguridad

-   Complemento MMC Plantillas de seguridad

-   Complemento Editor de directivas de grupo (usado para la sección Configuración de seguridad del árbol Configuración del equipo)

-   Herramienta Configuración de seguridad local

-   Herramienta Directiva de seguridad del controlador de dominio

-   Herramienta Directiva de seguridad de dominio

Como todas estas herramientas utilizan SCE, los administradores de Windows disponen de una interfaz coherente y eficaz para crear y editar las directivas, ya se vayan a destinar a un equipo independiente o se vayan a implementar como un objeto GPO.

Hay disponible más información acerca de SCE en la Ayuda de Windows.

#### Usuarios y equipos de Active Directory

El complemento MMC Usuarios y equipos de Active* *Directory proporciona la interfaz gráfica de usuario principal para crear y administrar unidades organizativas (UO) dentro del dominio. Puede vincular los GPO y las UO, controlar el orden y la herencia de las directivas, así como iniciar el Editor de objetos de directiva de grupo como un proceso independiente para modificar los GPO. Sin embargo, el complemento no ofrece una manera coherente e integrada de crear un inventario, escribir y administrar las directivas de grupo.

Hay disponible más información acerca del complemento MMC Usuarios y equipos de Active Directory en la Ayuda de Windows.

#### Consola de administración de directivas de grupo

Microsoft creó la Consola de administración de directivas de grupo (GPMC) como respuesta a los comentarios de clientes que necesitaban una manera mejor de controlar la directiva de grupo en un entorno grande. GPMC se debe ejecutar en Windows XP con SP1 o Windows Server 2003 y consta de un complemento MMC y un conjunto de interfaces de secuencias de comandos que se pueden utilizar para administrar la directiva de grupo. Puede administrar tanto dominios de Windows 2000 Server como de Windows Server 2003.

GPMC proporciona:

-   Una interfaz de usuario que se centra en el uso y la administración de la directiva de grupo.

-   La capacidad de hacer copias de seguridad, restaurar, importar, exportar, copiar y pegar rápidamente objetos GPO.

-   Una administración simplificada de la seguridad relacionada con la directiva de grupo.

-   Capacidades de crear informes de GPO y datos Conjunto resultante de directivas (RSoP).

-   Operaciones de GPO de secuencias de comandos.

Todos los clientes de Windows* *Server* *2003 pueden descargar gratuitamente la [Consola de administración de directivas de grupo con el Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0a6d4c24-8cbd-4b35-9272-dd3cbfc81887&displaylang=en) en www.microsoft.com/downloads/details.aspx?FamilyID=0a6d4c24-8cbd-4b35-9272-dd3cbfc81887&DisplayLang=en.

[](#mainsection)[Principio de la página](#mainsection)

### Formatos de los archivos de seguridad

Las directivas de seguridad se pueden crear y almacenar en una variedad de formatos. En las secciones siguientes se describen los formatos de archivos comunes que usa Windows Server 2003:

#### Directiva de SCW (.xml)

SCW incorpora un nuevo formato de archivo basado en XML. Las directivas nativas de SCW se guardan con la extensión .xml. Estos archivos de directiva XML no tienen un esquema oficial, pero se pueden identificar por el elemento &lt;SecurityPolicy Version="1.0"&gt;.

El archivo de directiva de SCW es realmente un manifiesto completo de varios tipos distintos de configuración:

-   Modo de inicio de servicios del sistema

-   Excepciones del Firewall de Windows

-   Funciones de los equipos seleccionados

-   Tareas de los equipos seleccionados

-   Configuración del Registro

-   Configuración de directiva

-   Directivas de auditoría

Además, las directivas de SCW se pueden vincular a una o más plantillas de directiva para proporcionar funcionalidad adicional que no es nativa de SCW, como el servicio del sistema o las listas de control de acceso (ACL) del Registro.

#### Plantilla de directiva (.inf)

Las plantillas de directiva son archivos de texto que usan un formato estándar para los archivos de datos de Windows: uno o más secciones separadas del resto con palabras clave encerradas entre corchetes, y seguidas de uno o más pares de atributos y valores.

Las plantillas de directiva pueden contener una o más secciones que definen los tipos siguientes de datos:

-   Directivas de contraseña

-   Directivas de desbloqueo

-   Directivas de protocolo de autenticación Kerberos

-   Directivas de auditoría

-   Configuración del registro de eventos

-   Valores del Registro

-   Modos de inicio de servicio

-   Permisos del servicio

-   Derechos de usuario

-   Restricciones de pertenencia a grupo

-   Permisos del Registro

-   Permisos del sistema de archivos

Las plantillas de directiva son compatibles con la mayoría de las herramientas indicadas anteriormente en este apéndice, y el mismo formato de plantilla se puede usar para las directivas de equipos locales y las directivas de grupo de Active* *Directory. Las plantillas se deben importar con la herramienta apropiada para que se puedan usar.

#### Objetos de directiva de grupo (GPO)

Los GPO son los datos de directiva que se almacenan en Active Directory y como una colección de archivos dentro de directorios especiales de los controladores de dominio. Estos archivos de directiva representan directivas de equipo y de usuario y no se manipulan normalmente de forma directa. Puede utilizar una herramienta como GPMC para modificar la configuración o exportar un GPO a una plantilla de directiva.

Puede exportar o hacer una copia de seguridad de un GPO desde GPMC para guardar toda la información almacenada en el GPO en el sistema de archivos. Las copias de seguridad de un GPO que se crean de este modo contienen la siguiente información:

-   Identificador global único (GUID) y dominio del GPO

-   Configuración del GPO

-   Lista de control de acceso discrecional (DACL) del GPO

-   Vínculo del filtro WMI, si hay uno (pero no el filtro en sí mismo)

-   Vínculos a las directivas de seguridad IP, si hay alguno

-   Informe XML de la configuración de GPO, que se puede ver como HTML desde GPMC

-   Marca de fecha y hora que indica cuándo se realizó la copia de seguridad

-   Descripción proporcionada por el usuario sobre la copia de seguridad

Sin embargo, esta copia de seguridad no guarda ningún dato que sea externo al GPO. En concreto, este archivo no contendrá la información de vínculos de sitios, dominios o unidades organizativas y no incluirá filtros WMI ni directivas de seguridad IP reales.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
