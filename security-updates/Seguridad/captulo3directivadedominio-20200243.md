---
TOCTitle: 'Capítulo 3: Directiva de dominio'
Title: 'Capítulo 3: Directiva de dominio'
ms:assetid: '833fddab-0361-4209-bef6-ee3b14acd18d'
ms:contentKeyID: 20200243
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163113(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 3: Directiva de dominio

Actualizado: 27/12/05

### En esta página

[](#ehaa)[Información general](#ehaa)
[](#egaa)[Directiva de dominio](#egaa)
[](#efaa)[Directivas de cuentas](#efaa)
[](#eeaa)[Directiva de contraseñas](#eeaa)
[](#edaa)[Directiva de bloqueo de cuentas](#edaa)
[](#ecaa)[Directivas Kerberos](#ecaa)
[](#ebaa)[Opciones de seguridad](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

En este capítulo se utiliza la construcción de un entorno de dominio para demostrar formas de abordar la seguridad de una infraestructura con Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1).

Este capítulo se centra en los temas siguientes:

-   La configuración de seguridad y las contramedidas en el nivel de dominio.

-   La forma de garantizar la seguridad de un dominio Windows Server 2003 para los entornos Cliente heredado (LC), Cliente de empresa (EC) y Seguridad Especializada: Funcionalidad limitada (SSLF) definidos en el capítulo 1, "Introducción a la Guía de seguridad de Windows Server 2003".

Esta información proporciona una base y una perspectiva acerca de cómo transformar un entorno LC en uno SSLF dentro de una infraestructura de dominios.

Windows Server 2003 con SP1 se proporciona con los valores predeterminados establecidos en un estado conocido sumamente seguro. Para aprovechar mejor el contenido de este material, en este capítulo sólo se describen las configuraciones cuyos valores predeterminados se han modificado. Para obtener más información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y*
*Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.

[](#mainsection)[Principio de la página](#mainsection)

### Directiva de dominio

Puede aplicar la configuración de seguridad de Directiva de grupo a los distintos niveles de una organización. En el entorno de línea de base descrito en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", se utilizó la directiva de grupo para aplicar la configuración en los tres siguientes niveles de la jerarquía de la infraestructura del dominio:

-   **Nivel de dominio:** la configuración de este nivel se ocupa de requisitos de seguridad comunes, como las directivas de cuentas y contraseñas que se deben aplicar en todos los servidores del dominio.

-   **Nivel de línea de base:** la configuración de este nivel aborda requisitos de seguridad específicos de servidor que son comunes a todos los servidores de la infraestructura del dominio.

-   **Nivel específico de función:** la configuración de este nivel se encarga de los requisitos de seguridad de funciones de servidor específicas. Por ejemplo, los requisitos de seguridad de los servidores de infraestructura difieren de los de los servidores que ejecutan los Servicios de Internet Information Server (IIS) de Microsoft.

En las siguientes secciones de este capítulo sólo se tratará en detalle la directiva de nivel de dominio. La mayoría de las configuraciones de seguridad del dominio que se describen se refieren a las cuentas de usuario y contraseñas. Cuando revise estas configuraciones y recomendaciones, recuerde que toda la configuración se aplica a cada uno de los usuarios del límite del dominio.

#### Descripción general de la directiva de dominio

La directiva de dominio es extremadamente eficaz, ya que permite al administrador crear una configuración estándar para los equipos de la red. Los objetos de directiva de grupo (GPO) pueden ser una parte importante de la solución de administración de configuración de cualquier organización, puesto que permiten a los administradores realizar simultáneamente cambios de seguridad en todos los equipos del dominio o subconjuntos del dominio.

Las secciones siguientes proporcionan información detallada acerca de la configuración de seguridad que puede utilizar para mejorar la seguridad de Windows Server 2003 con SP1. Se proporcionan tablas en las que se resumen las configuraciones, así como descripciones detalladas sobre cómo alcanzar los objetivos de seguridad de cada configuración. Las configuraciones se dividen en categorías que se corresponden con su presentación en la interfaz de usuario del Editor de configuración de seguridad (SCE) de Windows Server 2003.

A través de la directiva de grupo es posible aplicar simultáneamente los siguientes tipos de cambios de seguridad:

-   Modificación de permisos en el sistema de archivos

-   Modificación de permisos en los objetos del Registro

-   Cambio de la configuración del Registro

-   Cambio en las asignaciones de los derechos de usuario

-   Configuración de los servicios del sistema

-   Configuración de los registros de eventos y auditoría

-   Configuración de las directivas de cuentas y contraseñas

En esta guía se recomienda crear una nueva directiva de grupo en la raíz del dominio para que las directivas descritas en el capítulo se apliquen a todo el dominio. Este enfoque facilitará la realización de pruebas o la solución de problemas en la nueva directiva de grupo, ya que simplemente tendrá que deshabilitarla si necesita revertir los cambios. Sin embargo, algunas aplicaciones diseñadas para ejecutarse con Active Directory realizan los cambios en la directiva de dominio predeterminada integrada. Estas aplicaciones no serán conscientes de la nueva directiva de grupo implementada según las recomendaciones de esta guía. Antes de implementar nuevas aplicaciones empresariales, asegúrese de probarlas minuciosamente. Si detecta problemas, compruebe si la aplicación ha modificado directivas de cuentas, creado nuevas cuentas de usuario, cambiado derechos de usuario o realizado otros cambios en la directiva de dominio predeterminada o en las directivas de los equipos locales.

[](#mainsection)[Principio de la página](#mainsection)

### Directivas de cuentas

Las directivas de cuentas, que incluyen la configuración de seguridad de la directiva de contraseñas, la directiva de bloqueo de cuentas y la directiva Kerberos, sólo son relevantes en la directiva de dominio de los tres entornos definidos en esta guía. La directiva de contraseñas proporciona una manera de establecer complejidad y cambiar programaciones en los entornos con una elevada seguridad. La directiva de bloqueo de cuentas permite realizar un seguimiento de los intentos de inicio de sesión con contraseña no correctos con el fin de iniciar bloqueos de cuentas si es necesario. Las directivas Kerberos se utilizan para las cuentas de usuario de dominio y determinan la configuración relacionada con el protocolo de autenticación Kerberos, como la vigencia y obligatoriedad de los vales.

[](#mainsection)[Principio de la página](#mainsection)

### Directiva de contraseñas

Las contraseñas complejas que se modifican de forma periódica reducen la probabilidad de que se produzcan ataques a las mismas. La configuración de la directiva de contraseñas controla la complejidad y la duración de las contraseñas. En esta sección se describen las configuraciones específicas de la directiva de contraseñas y su relación con los tres entornos definidos en esta guía: Cliente heredado, Cliente de empresa y Seguridad especializada: Funcionalidad limitada.

Unos requisitos estrictos en cuanto a la longitud y la complejidad de las contraseñas no significa necesariamente que los usuarios y los administradores vayan a utilizar contraseñas seguras. Aunque la directiva de contraseñas pueda exigir a los usuarios el cumplimiento de los requisitos técnicos de complejidad, es necesario implementar una directiva de seguridad eficaz adicional para garantizar que los usuarios creen contraseñas que sean difíciles de comprometer. Por ejemplo, "¡desayuno!" puede cumplir todos los requisitos de complejidad de contraseñas, pero no es muy complicado averiguarla.

Si conoce algunos datos sobre la persona que crea una contraseña, es posible adivinarla basándose en su comida, automóvil o película favoritos. Una estrategia de los programas de seguridad de las organizaciones que intentan educar a los usuarios acerca del uso de contraseñas seguras consiste en crear un póster con descripciones de contraseñas inadecuadas y colocarlo en zonas comunes como, por ejemplo, junto al dispensador de agua o la fotocopiadora. Es necesario que su organización establezca una serie de instrucciones para la creación de contraseñas seguras que incluyan lo siguiente:

-   Evitar el uso de palabras que aparezcan en un diccionario de cualquier idioma, como palabras comunes o escritas incorrectamente de forma hábil.

-   No crear una contraseña nueva con simplemente agregar un dígito a la contraseña actual.

-   Evitar el uso de contraseñas que empiecen o terminen con un número, ya que se pueden averiguar más fácilmente que las que lo contienen en medio.

-   Evitar el uso de contraseñas que puedan adivinar los demás fácilmente al observar el escritorio (como nombres de mascotas, equipos de fútbol y familiares).

-   Evitar el uso de palabras de la cultura popular.

-   Aplicar contraseñas cuya escritura requiera utilizar el teclado con las dos manos.

-   Utilizar símbolos, números y letras en mayúsculas y minúsculas en todas las contraseñas.

-   Usar espacios y caracteres que se puedan generar solamente si se presiona la tecla ALT.

Estas instrucciones también se deben seguir para todas la contraseñas de cuentas de servicios de la organización.

#### Configuración de la directiva de contraseñas

La tabla siguiente incluye recomendaciones sobre la configuración de la directiva de contraseñas para los tres entornos definidos en esta guía. Puede establecer la configuración de directiva de contraseñas en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directivas de contraseñas**

La información adicional para cada configuración se proporciona en las subsecciones que se muestran después de la tabla.

**Tabla 3.1 Recomendaciones sobre la configuración de la directiva de contraseñas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Cliente heredado</th>
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Seguridad especializada: Funcionalidad limitada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Forzar el historial de contraseñas</td>
<td style="border:1px solid black;">Se recuerdan 24 contraseñas</td>
<td style="border:1px solid black;">Se recuerdan 24 contraseñas</td>
<td style="border:1px solid black;">Se recuerdan 24 contraseñas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Vigencia máxima de la contraseña</td>
<td style="border:1px solid black;">42 días</td>
<td style="border:1px solid black;">42 días</td>
<td style="border:1px solid black;">42 días</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Vigencia mínima de la contraseña</td>
<td style="border:1px solid black;">1 día</td>
<td style="border:1px solid black;">1 día</td>
<td style="border:1px solid black;">1 día</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Longitud mínima de la contraseña</td>
<td style="border:1px solid black;">8 caracteres</td>
<td style="border:1px solid black;">8 caracteres</td>
<td style="border:1px solid black;">12 caracteres</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Las contraseñas deben cumplir los requerimientos de complejidad</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
### Forzar el historial de contraseñas
  
Esta configuración de directiva determina el número de nuevas contraseñas únicas que se deben asociar a una cuenta de usuario antes de que se pueda volver a utilizar una contraseña antigua. El valor se puede establecer entre 0 y 24 contraseñas.
  
El valor predeterminado de **Forzar el historial de contraseñas** en Windows Server 2003 con SP1 es el máximo permitido; es decir, 24 contraseñas. Microsoft recomienda usar este valor en los tres entornos, porque permite garantizar que no se reutilizan continuamente las contraseñas antiguas ya que las vulnerabilidades comunes están asociadas a la reutilización de contraseñas y un número bajo en esta configuración permitirá a los usuarios reciclar continuamente un número reducido de contraseñas una y otra vez. Además, no se han detectado problemas al aplicar esta recomendación a entornos que incluyen clientes heredados.
  
Para mejorar la eficacia de esta configuración de directiva, también puede configurar **Vigencia mínima de la contraseña** de modo que las contraseñas no se puedan cambiar inmediatamente. Esta combinación dificulta a los usuarios la reutilización de contraseñas, bien por accidente o de forma intencionada.
  
### Vigencia máxima de la contraseña
  
Esta configuración de directiva define el período en el que un atacante que ha descifrado una contraseña podrá utilizarla para tener acceso a un equipo de la red antes de que caduque. Los valores de esta configuración de directiva están comprendidos entre 1 y 999 días. Puede configurar **Vigencia máxima de la contraseña** de modo que las contraseñas caduquen con la frecuencia necesaria para su entorno. El valor predeterminado de esta configuración es de 42 días.
  
Cambiar las contraseñas periódicamente puede ser útil para impedir que resulten comprometidas. La mayoría de las contraseñas se pueden averiguar si un atacante tiene suficiente tiempo y recursos informáticos. Cuanto mayor sea la frecuencia con la que se cambia la contraseña, menor será el tiempo del que dispondrá un atacante para averiguarla. No obstante, cuanto menor sea el valor que se establezca, mayor será la probabilidad de que aumente el número de llamadas al servicio de soporte técnico.
  
Microsoft recomienda dejar **Vigencia máxima de la contraseña** en el valor predeterminado de 42 días para los tres entornos de seguridad definidos en esta guía. Esta configuración garantiza el cambio periódico de las contraseñas, pero no requiere que los usuarios las modifiquen tan a menudo que no las recuerden. Para equilibrar las necesidades de seguridad y utilización, puede aumentar el valor de esta configuración de directiva en los entornos Cliente heredado y Cliente de empresa.
  
### Vigencia mínima de la contraseña
  
Esta configuración de directiva determina el número de días que se debe utilizar una contraseña antes de que un usuario la pueda cambiar. El intervalo de valores de **Vigencia mínima de la contraseña** es de 0 a 999 días; un valor de 0 permite cambiar inmediatamente la contraseña. El valor predeterminado de esta configuración de directiva es de 1 día.
  
El valor de **Vigencia mínima de la contraseña** debe ser inferior al de **Vigencia máxima de la contraseña**, a menos queesta última opción esté configurada como **0**, lo que indicaría que las contraseñas no caducarán nunca. Configure **Vigencia mínima de la contraseña** de forma que sea superior a 0 si desea que se aplique la configuración **Forzar el historial de contraseñas**. Sin una vigencia mínima de la contraseña, los usuarios pueden pasar de una contraseña a otra repetidamente hasta que pueden reutilizar su favorita anterior.
  
Microsoft recomienda utilizar el valor predeterminado de 1 día en **Vigencia máxima de la contraseña** para los tres entornos de seguridad definidos en esta guía. Si esta configuración se utiliza con un valor bajo similar en **Forzar el historial de contraseñas**, los usuarios pueden usar una y otra vez las mismas contraseñas. Por ejemplo, si **Vigencia mínima de la contraseña** está configurado en 1 día y **Forzar el historial de contraseñas** está establecido en 2 contraseñas, los usuarios sólo tendrán que esperar 2 días para poder reutilizar una contraseña antigua favorita. Sin embargo, si **Vigencia mínima de la contraseña** está configurado en 1 día y **Forzar el historial de contraseñas** está establecido en 24, los usuarios tendrán que cambiar las contraseñas todos los días durante al menos 24 días para poder reutilizar una contraseña, algo bastante improbable.
  
### Longitud mínima de la contraseña
  
Esta configuración de directiva garantiza que las contraseñas tengan al menos un número especificado de caracteres. Las contraseñas largas, es decir, de ocho o más caracteres, son generalmente más seguras que las cortas. Cuando se utiliza la configuración **Longitud mínima de la contraseña**, los usuarios no pueden usar contraseñas en blanco y deben crear contraseñas que tengan un número específico de caracteres. El valor predeterminado de esta configuración es de siete caracteres.
  
En esta guía se recomienda configurar **Longitud mínima de contraseña** en ocho caracteres para los entornos Cliente heredado y Cliente de empresa. Esta configuración es suficientemente larga para proporcionar el nivel de seguridad adecuado y, al mismo tiempo, lo bastante corta para que los usuarios la recuerden con facilidad. Además, proporciona un mecanismo de defensa bastante seguro contra los ataques de diccionario y de fuerza bruta que se producen con frecuencia.
  
(Los ataques de diccionario utilizan listas de palabras para averiguar una contraseña mediante el método de ensayo y error. Los ataques de fuerza bruta prueban con todos los posibles valores de contraseña o texto cifrado. La probabilidad de que un ataque de fuerza bruta consiga su fin depende de la longitud de la contraseña, el tamaño del conjunto de caracteres potencial y la capacidad del equipo del atacante.)
  
En esta guía se recomienda configurar **Longitud mínima de la contraseña** en 12 caracteres para el entorno Seguridad especializada: Funcionalidad limitada.
  
Cada carácter adicional de una contraseña aumenta su complejidad de forma exponencial. Por ejemplo, una contraseña de 7 caracteres debería tener 267 ó 1 x 107 combinaciones posibles. Una contraseña alfabética de 7 caracteres en la que se distingan mayúsculas y minúsculas tiene 527 combinaciones. Una contraseña alfanumérica de 7 caracteres en la que se distingan mayúsculas y minúsculas sin puntuación tiene 627 combinaciones. Con 1.000.000 de intentos por segundo, sólo se tardarían unos 40 días en averiguarla. Una contraseña de 8 caracteres tiene 268 ó 2 x 1011 combinaciones posibles. Aunque este número pueda parecer muy alto, con 1.000.000 de intentos por segundo (capacidad que admiten muchas utilidades de averiguación de contraseñas) sólo se tardarían 59 horas en probar con todas las contraseñas posibles. Recuerde que estos tiempos se incrementarán considerablemente en el caso de las contraseñas con caracteres ALT y otros caracteres especiales del teclado, tales como ! o @.
  
Las contraseñas se almacenan en la base de datos del Administrador de cuentas de seguridad (SAM) o en Active Directory después de pasar por un algoritmo hash unidireccional (no reversible). Por tanto, la única forma de saber si dispone de la contraseña correcta consiste en ejecutarla con el mismo algoritmo hash unidireccional y comparar los resultados. Los ataques de diccionario ejecutan diccionarios completos a través del proceso de cifrado, en busca de coincidencias. Aunque se trata de un enfoque simplista, es muy eficaz para determinar qué usuarios utilizan palabras comunes como "contraseña" o "invitado" en las contraseñas de sus cuentas.
  
Las versiones más antiguas de Windows utilizaban un tipo específico de algoritmo hash conocido como hash de LAN Manager (LMHash). Este algoritmo divide la contraseña en bloques de siete o menos caracteres y luego calcula un valor hash distinto para cada bloque. Aunque Windows 2000 Server, Windows XP y Windows Server 2003 utilizan un algoritmo hash más reciente, siguen calculando y almacenando el LMHash para ofrecer compatibilidad con versiones anteriores.
  
Cuando hay valores LMHash, los usuarios que intentan averiguar las contraseñas disponen de un acceso directo. Si una contraseña tiene 7 o menos caracteres, la segunda mitad del LMHash se resuelve en un valor específico que puede informar a un atacante de que la contraseña tiene menos de 8 caracteres. Las contraseñas con al menos 8 caracteres refuerzan la seguridad de hasta el LMHash más débil, ya que al ser más largas los atacantes tienen que descifrar dos partes de cada contraseña en lugar de una. Es posible atacar ambas partes de un LMHash en paralelo y, si la segunda mitad del LMHash es de sólo un carácter, podrá sucumbir a un ataque de fuerza bruta en milisegundos. Por lo tanto, no es una solución muy útil, excepto si la contraseña es parte de un conjunto de caracteres con ALT.
  
Por este motivo, no se recomienda el uso de contraseñas más cortas en lugar de más largas. Sin embargo, requerir el uso de una longitud mínima que sea demasiado larga puede generar muchos errores tipográficos, lo que puede provocar un mayor número de cuentas bloqueadas y llamadas al servicio de soporte técnico. Asimismo, exigir el uso de una contraseña extremadamente larga puede reducir realmente la seguridad de la organización, ya que es más probable que los usuarios las anoten para no olvidarlas.
  
### Las contraseñas deben cumplir los requerimientos de complejidad
  
Esta configuración de directiva comprueba todas las contraseñas nuevas cuando se crean para garantizar que cumplen los requisitos de complejidad. Las reglas de directiva de Windows Server 2003 no se pueden modificar directamente, si bien se puede crear una nueva versión del archivo Passfilt.dll para aplicar un conjunto de reglas diferente. Para obtener más información acerca de la creación de un archivo Passfilt.dll personalizado, consulte el artículo de MSDN® que describe un [ejemplo de filtro de contraseñas](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/secmgmt/security/sample_password_filter.asp) en http://msdn.microsoft.com/library/default.asp?url=/library/en-us/secmgmt/  
security/sample\_password\_filter.asp (en inglés).
  
En realidad, una contraseña de 20 o más caracteres se puede establecer de forma que, aparte de ser más segura, al usuario le resulte más fácil de recordar que una de 8 caracteres. Supongamos por ejemplo que se utiliza la siguiente contraseña de 28 caracteres: **me encanta la pizza 4 quesos**. Un usuario podría recordar este tipo de contraseña, que no es sino una frase, con más facilidad que una contraseña corta como **C@55t0ña**.
  
En combinación con un valor de **Longitud mínima de contraseña** de 8, esta configuración hará realmente difícil que se pueda realizar un ataque de fuerza bruta. Si incluye letras en mayúsculas y minúsculas y números en los espacios, el número de caracteres disponibles aumenta de 26 a 62 caracteres. Una contraseña de 8 caracteres tiene 2,18 x 1.014 combinaciones posibles. A 1.000.000 de intentos por segundo, llevaría 6,9 años pasar por todas las combinaciones posibles.
  
Por estas razones, Microsoft recomienda configurar el valor de **Las contraseñas deben cumplir los requerimientos de complejidad** en **Habilitado** para los tres entornos de seguridad definidos en esta guía.
  
### Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio
  
Esta configuración de directiva determina si el sistema operativo utiliza cifrado reversible para almacenar las contraseñas. Es compatible con las aplicaciones que usan protocolos que necesitan que el usuario especifique una contraseña para autenticarse.
  
Las contraseñas almacenadas con un método de cifrado que se puede revertir se pueden recuperar más fácilmente que las almacenadas con cifrado irreversible. Si se habilita esta configuración, la vulnerabilidad aumenta.
  
Por este motivo, Microsoft recomienda configurar el valor de **Almacenar contraseña utilizando cifrado reversible** como **Deshabilitado**, salvo si los requisitos de la aplicación compensan la necesidad de proteger la información de contraseña. Además, los entornos que implementan el protocolo de autenticación por desafío mutuo (CHAP) a través del acceso remoto o IAS y entornos que usan autenticación de texto implícita para los Servicios de Internet Information Server (IIS) requieren que esta configuración de directiva esté habilitada.
  
#### Cómo impedir que los usuarios cambien una contraseña excepto cuando se les pida
  
Aunque la configuración de la directiva de contraseñas descrita en la sección anterior proporciona varias opciones, algunas organizaciones necesitan disponer de un control centralizado de todos los usuarios. En esta sección se describe cómo impedir que los usuarios cambien las contraseñas, excepto en aquellos casos en los que sea necesario.
  
El control centralizado de las contraseñas de los usuarios es la piedra angular de cualquier esquema de seguridad de un sistema Windows Server 2003 bien diseñado. Puede utilizar la directiva de grupo para establecer las vigencias mínima y máxima de las contraseñas tal y como se ha descrito anteriormente, pero sin olvidar que los requisitos de cambiar frecuentemente las contraseñas pueden favorecer el que los usuarios burlen la configuración del historial de contraseñas del entorno. El requisito de que las contraseñas sean demasiado largas también puede provocar más llamadas al servicio de soporte técnico por parte de usuarios que olviden sus contraseñas.
  
Los usuarios pueden cambiar sus contraseñas en el período entre la vigencia mínima y máxima de la contraseña. Sin embargo, el diseño del entorno Seguridad especializada: Funcionalidad limitada requiere que los usuarios cambien sus contraseñas únicamente cuando el sistema operativo así lo solicite, después de los 42 días establecidos en **Vigencia máxima de la contraseña**. Para impedir que se cambien las contraseñas (excepto cuando sea necesario), puede deshabilitar la opción **Cambiar contraseña** del cuadro de diálogo **Seguridad de Windows** que aparece al presionar CTRL+ALT+SUPR. Tenga en cuenta que es posible que los usuarios preocupados por la seguridad cambien sus contraseñas con mayor frecuencia y que tengan que ponerse en contacto con el administrador para hacerlo, lo que aumentará los costos de soporte técnico.
  
Esta configuración se puede implementar en todo el dominio a través de la directiva de grupo o para uno o varios usuarios específicos mediante la edición del Registro. Para obtener instrucciones más detalladas sobre esta configuración, consulte el artículo de Microsoft Knowledge Base "[Cómo impedir que los usuarios cambien una contraseña excepto cuando se les pida en Windows Server 2003](http://support.microsoft.com/?kbid=324744)" en http://support.microsoft.com/?kbid=324744.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de bloqueo de cuentas
  
La directiva de bloqueo de cuentas es una característica de seguridad de Windows Server 2003 con SP1 que bloquea las cuentas de usuario después de un número determinado de intentos erróneos de inicio de sesión en un período de tiempo especificado. El número de intentos permitidos y el período de tiempo se basan en los valores configurados para la directiva. Windows Server 2003 con SP1 hace un seguimiento de los intentos de inicio de sesión, y el software de servidor se puede configurar para deshabilitar las cuentas después de un número preestablecido de inicios de sesión erróneos como respuesta a posibles ataques.
  
Estas configuraciones de directiva son útiles para proteger las contraseñas de los usuarios y evitar que los atacantes las averigüen, además de reducir las probabilidades de que se consiga atacar la red. Sin embargo, al habilitar la directiva de bloqueo de cuentas los costos de soporte técnico serán probablemente superiores, ya que los usuarios que olviden o escriban incorrectamente la contraseña varias veces necesitarán ayuda. Antes de habilitar las siguientes configuraciones, asegúrese de que su organización está preparada para asumir esta carga adicional. Para muchas organizaciones, una solución mejorada y menos costosa consiste en supervisar automáticamente los registros de eventos de seguridad de los controladores de dominio y generar alertas administrativas cuando parezca que alguien intenta adivinar las contraseñas de las cuentas de usuario. Consulte el capítulo 2, "Directivas de nivel de dominio", de la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), para obtener información adicional sobre estas configuraciones y su interacción.
  
#### Configuración de directiva de bloqueo de cuentas
  
En la tabla siguiente se resume la configuración recomendada de la directiva de bloqueo de cuentas. Puede utilizar el Editor de objetos de directiva de grupo para configurar estos parámetros en la siguiente ubicación en la directiva de grupo del dominio:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directiva de bloqueo de cuentas**
  
La información adicional para cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 3.2 Configuración de la directiva de bloqueo de cuentas**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Cliente heredado</th>
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Seguridad especializada: Funcionalidad limitada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Duración del bloqueo de cuenta</td>
<td style="border:1px solid black;">30 minutos</td>
<td style="border:1px solid black;">30 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Umbral de bloqueos de la cuenta</td>
<td style="border:1px solid black;">50 intentos de inicio de sesión no válidos</td>
<td style="border:1px solid black;">50 intentos de inicio de sesión no válidos</td>
<td style="border:1px solid black;">10 intentos de inicio de sesión no válidos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Restablecer la cuenta de bloqueos después de</td>
<td style="border:1px solid black;">30 minutos</td>
<td style="border:1px solid black;">30 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
</tr>
</tbody>
</table>
  
### Duración del bloqueo de cuenta
  
Esta configuración de directiva determina el tiempo que debe transcurrir para que una cuenta se desbloquee y un usuario pueda volver a intentar iniciar sesión. Especifica el número de minutos que una cuenta bloqueada permanece no disponible. Si establece el valor de **Duración del bloqueo de cuenta** en 0, las cuentas estarán bloqueadas hasta que el administrador las desbloquee. El valor predeterminado de esta configuración de directiva en Windows Server 2003 con SP1 es **No está definido**.
  
Aunque pueda parecer una buena idea establecer el valor de **Duración del bloqueo de cuenta** en no desbloquear nunca automáticamente, esta configuración puede aumentar el número de llamadas que recibe el servicio de soporte técnico para desbloquear cuentas bloqueadas por error.
  
En esta guía se recomienda configurar el valor de **Duración del bloqueo de cuenta** en **30 minutos** para los entornos Cliente heredado y Cliente de empresa y en **15 minutos** para el entorno Seguridad especializada: Funcionalidad limitada. Esta configuración disminuye la cantidad de carga operativa durante un ataque por denegación de servicio (DoS). En un ataque DoS, el atacante realiza una serie de intentos de inicio de sesión malintencionados en todas las cuentas de usuario de la organización, lo que bloquea las cuentas. Con la configuración recomendada, los usuarios bloqueados tienen la posibilidad de volver a iniciar sesión en un plazo de tiempo razonable sin tener que solicitar asistencia al servicio de soporte técnico. Sin embargo, la información acerca del valor de este parámetro debe comunicarse a los usuarios.
  
### Umbral de bloqueos de la cuenta
  
Esta configuración de directiva determina el número de intentos que puede realizar un usuario para iniciar sesión en una cuenta antes de que ésta se bloquee.
  
Los usuarios autorizados pueden bloquear su propio acceso a las cuentas de varios modos. Por ejemplo, pueden escribir incorrectamente la contraseña o cambiarla en un equipo mientras tienen iniciada sesión en otro. El equipo con la contraseña incorrecta puede intentar de forma continuada autenticar al usuario y, puesto que la contraseña que utiliza para ello es incorrecta, la cuenta del usuario al final se bloquea. Para evitar el bloqueo de usuarios autorizados, configure el valor de **Umbral de bloqueos de la cuenta** en un número alto.
  
Debido a que pueden existir vulnerabilidades tanto cuando se configura **Umbral de bloqueos de la cuenta** como cuando no, se han definido distintas contramedidas para cada una de las posibilidades. Su organización debe valorar las dos alternativas y tener en cuenta las amenazas y riesgos identificados que se intentan evitar.
  
-   Para evitar bloqueos de cuenta, establezca el valor de **Umbral de bloqueos de la cuenta** en 0. Esta configuración permite reducir las llamadas al servicio de soporte técnico, puesto que los usuarios no pueden bloquear por error sus propias cuentas. Además, los ataques DoS que intenten bloquear las cuentas de la organización de forma intencionada no lo conseguirán. Dado que no se evitará un ataque de fuerza bruta, seleccione esta configuración sólo si se cumplen explícitamente ambos criterios:
  
    -   La directiva de contraseñas obliga a los usuarios a tener contraseñas complejas compuestas de 8 o más caracteres.
  
    -   Hay un eficaz mecanismo de auditoría que puede avisar a los administradores cuando se producen varios inicios de sesión erróneos en el entorno. Por ejemplo, el mecanismo de auditoría debe supervisar el evento de seguridad 539, en el que se señala que ha habido un error de inicio de sesión y que la cuenta se bloqueó en el momento en el que se intentó realizar el inicio de sesión. Este evento significa que la cuenta se bloqueó cuando se alcanzó el umbral de intentos de inicio de sesión. Sin embargo, el evento 539 sólo muestra un bloqueo de cuenta y no un intento sin éxito de contraseña. Por lo tanto, los administradores también deberían controlar los intentos en los que se especifique la contraseña incorrecta.
  
-   Si no se cumplen estos criterios, la segunda opción consiste en configurar **Umbral de bloqueos de la cuenta** en un valor lo suficientemente alto como para permitir que los usuarios puedan escribir incorrectamente sus contraseñas varias veces sin que se bloqueen sus cuentas. Sin embargo, el valor debe permitir garantizar que la cuenta se bloqueará ante un ataque de contraseña de fuerza bruta.
  
En esta guía se recomienda configurar el valor de **Umbral de bloqueos de la cuenta** en **50** para los entornos Cliente heredado y Cliente de empresa, lo que debería proporcionar una seguridad adecuada y un nivel aceptable de utilización. Este valor evitará que las cuentas se bloqueen por error y reducirá el número de llamadas al servicio de soporte técnico, pero no impedirá los ataques DoS, como se ha descrito anteriormente. No obstante, en esta guía se recomienda establecer esta configuración de directiva en **10** para los entornos Seguridad especializada: Funcionalidad limitada.
  
### Restablecer la cuenta de bloqueos después de
  
Esta configuración de directiva determina el plazo de tiempo antes de que el **Umbral de bloqueos de la cuenta** se restablezca a cero y la cuenta se desbloquee. Si se define un **Umbral de bloqueos de la cuenta**, este tiempo de restablecimiento debe ser inferior o igual al valor de **Duración del bloqueo de cuenta**.
  
**Restablecer la cuenta de bloqueos después de** funciona junto con otros parámetros de configuración. Si deja el valor predeterminado de esta configuración de directiva o configura el valor en un intervalo demasiado largo, el entorno podría ser vulnerable a un ataque DoS de bloqueo de cuentas. Sin una configuración de directiva para restablecer el bloqueo de cuentas, los administradores tendrán que desbloquear manualmente todas las cuentas. Por el contrario, si no se establece un valor de tiempo razonable para esta configuración, los usuarios se bloquearán durante un período de tiempo establecido hasta que todas las cuentas se desbloqueen automáticamente.
  
En esta guía se recomienda configurar el valor de **Restablecer la cuenta de bloqueos después de** en 30 minutos para los entornos Cliente heredado y Cliente de empresa. Esta configuración define un período de tiempo razonable que los usuarios muy probablemente aceptarán sin tener que solicitar asistencia al servicio de soporte técnico. Sin embargo, en esta guía se recomienda establecer esta configuración de directiva en 15 minutos para el entorno Seguridad especializada: Funcionalidad limitada.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directivas Kerberos
  
Las directivas Kerberos se utilizan para cuentas de usuario de dominio. Estas directivas determinan la configuración relacionada con el protocolo de autenticación Kerberos, versión 5, como la vigencia y la obligatoriedad de los vales. Las directivas Kerberos no existen en la directiva de equipo local. Si reduce la vigencia de los vales Kerberos, disminuye el riesgo de que un atacante intente robar las contraseñas para suplantar la identidad legítima de las cuentas de usuario. No obstante, la necesidad de mantener estas directivas aumenta la carga de autorizaciones que es necesario realizar.
  
En la mayoría de los entornos, los valores predeterminados de estas directivas no se deberían modificar. La configuración de Kerberos se incluye en la directiva predeterminada de dominio, donde también se aplica. Por lo tanto, no se incluye en las plantillas de seguridad que acompañan a esta guía.
  
Esta guía recomienda no realizar ningún cambio en las directivas Kerberos predeterminadas. Para obtener más información acerca de estas configuraciones de directiva, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
Los tres tipos de directivas de cuentas que se han tratado anteriormente en este capítulo se definen en el nivel de dominio y las aplican todos los controladores de dominio del dominio. Un controlador de dominio siempre obtiene la directiva de cuenta del GPO Directiva predeterminada de dominio, aunque se aplique una directiva de cuenta distinta a la unidad organizativa que contiene el controlador.
  
Hay tres configuraciones de opciones de seguridad que son similares a las directivas de cuentas. Debe aplicar estas configuraciones en el nivel de todo el dominio y no en unidades organizativas (UO) individuales. Puede establecer estas configuraciones en la siguiente ubicación en el Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Seguridad\\Opciones**
  
#### Configuración de opciones de seguridad
  
En la tabla siguiente se resume la configuración recomendada para las opciones de seguridad. La información adicional para cada configuración se proporciona en las subsecciones que se muestran después de la tabla.
  
**Figura 3.3 Configuración de opciones de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Configuración</th>
<th style="border:1px solid black;" >Cliente heredado</th>
<th style="border:1px solid black;" >Cliente de empresa</th>
<th style="border:1px solid black;" >Seguridad especializada: Funcionalidad limitada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso de red: permitir traducción SID/nombre anónima</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
<td style="border:1px solid black;">Habilitada</td>
</tr>
</tbody>
</table>
  
### Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión
  
Esta configuración de directiva determina si se desconectará a los usuarios que se conecten al equipo local fuera de las horas de inicio de sesión válidas de las cuentas de usuario correspondientes. Esta configuración de directiva afecta al componente Bloques de mensajes de servidor (SMB). Cuando está habilitada, las sesiones de cliente con el servicio SMB se desconectan a la fuerza cuando ha transcurrido el tiempo de sesión válido del cliente. Si está deshabilitada, se podrá mantener una sesión de cliente establecida una vez transcurrido el tiempo de sesión del cliente. Al habilitar esta configuración de directiva, asegúrese de que también está habilitado el parámetro **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión**.
  
Si en la organización se han configurado las horas de inicio de sesión de los usuarios, es razonable habilitar el parámetro **Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión**. De lo contrario, los usuarios que no deban tener acceso a los recursos de la red fuera de las horas de sesión que les corresponden podrían continuar utilizando los recursos en sesiones iniciadas durante las horas permitidas.
  
En esta guía se recomienda configurar **Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión** en **Habilitado** para los tres entornos aquí definidos. Si no se utiliza tiempo de sesión, esta configuración de directiva no tendrá ninguna repercusión.
  
### Acceso de red: permitir traducción SID/nombre anónima
  
Esta configuración de directiva determina si un usuario anónimo puede solicitar el SID de otro usuario.
  
Si se habilita **Acceso de red: permitir traducción SID/nombre anónima** en un controlador de dominio, un usuario que conozca los atributos de SID estándar conocidos de un administrador podría ponerse en contacto con un equipo que también tuviera esta directiva habilitada y utilizar dicho SID para obtener el nombre del administrador. Esa persona podría entonces utilizar el nombre de cuenta para iniciar un ataque de contraseña.
  
Como la configuración predeterminada de **Acceso de red: permitir traducción SID/nombre anónima** es **Deshabilitado** en los equipos miembro, estos no se verán afectados por esta configuración de directiva. Sin embargo, la configuración predeterminada para los controladores de dominio es **Habilitado**. Si deshabilita esta configuración de directiva, es posible que los equipos que ejecutan sistemas operativos más antiguos no puedan comunicarse con dominios basados en Windows Server 2003 con SP1. Algunos ejemplos de este tipo de equipos son:
  
-   Servidores de servicio de acceso remoto (RAS) basados en Windows NT® 4.0.
  
-   Microsoft SQL Server™ en equipos Windows NT 3.X o Windows NT 4.0.
  
-   Equipos basados en servidores de servicio de acceso remoto Windows 2000 ubicados en dominios Windows NT 3.x o Windows NT 4.0.
  
En esta guía se recomienda configurar **Acceso de red: permitir traducción SID/nombre anónima** en **Deshabilitado** para los tres entornos aquí definidos.
  
### Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión
  
Esta configuración de directiva determina si se desconectará a los usuarios que se conectan a un equipo local fuera de las horas de inicio de sesión válidas de las cuentas de usuario correspondientes. Este parámetro afecta al componente SMB.
  
Si habilita **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión**, las sesiones de cliente con el servidor SMB se desconectarán a la fuerza cuando terminen las horas de inicio de sesión del usuario. El usuario no podrá iniciar sesión en el equipo hasta la próxima hora de acceso programada. Si deshabilita esta configuración de directiva, los usuarios podrán mantener una sesión de cliente establecida después de caducar las horas de inicio de sesión. Para que tenga efecto sobre las cuentas de dominio, esta configuración se debe definir en la directiva predeterminada de dominio.
  
En esta guía se recomienda configurar **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión** en **Habilitado** para los tres entornos aquí definidos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se ha descrito la necesidad de revisar todas las configuraciones del dominio de la organización. Sólo se puede configurar un conjunto de directivas de protocolo de autenticación de la versión 5 de Kerberos, de bloqueo de cuentas y de contraseñas por cada dominio. El resto de parámetros de configuración de bloqueo de cuentas y contraseñas sólo afectará a las cuentas locales de los servidores miembro. Considere la posibilidad de configurar parámetros que se aplicarán a todos los servidores miembro del dominio y asegúrese de que proporcionan un nivel adecuado de seguridad en la organización.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la directiva de dominio para servidores que ejecutan Windows Server 2003 con SP1.
  
-   Para obtener información sobre la capacidad de los usuarios anónimos de solicitar atributos de identificadores de seguridad para otros usuarios, consulte la página sobre la configuración [Acceso de red: permitir traducción SID/nombre anónima](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/299803be-0e85-4c60-b0b5-1b64486559b3.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/  
    299803be-0e85-4c60-b0b5-1b64486559b3.mspx (en inglés).
  
-   Para obtener información sobre la seguridad de red y cómo forzar el cierre de sesión cuando transcurren las horas de inicio de sesión, consulte el documento que contiene [respuestas técnicas de Microsoft](http://www.microsoft.com/technet/archive/community/columns/inside/techan32.mspx) en www.microsoft.com/technet/archive/community/columns/inside/techan32.mspx (en inglés).
  
    Además, consulte el artículo de Microsoft Knowledge Base sobre la[incapacidad de usar cuentas de invitado cuando está deshabilitado el acceso anónimo](http://support.microsoft.com/kb/218756/es) en http://support.microsoft.com/?kbid=251171 (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
