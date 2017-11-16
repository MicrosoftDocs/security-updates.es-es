---
TOCTitle: 'Apéndice A: Configuración de directivas de grupo de seguridad'
Title: 'Apéndice A: Configuración de directivas de grupo de seguridad'
ms:assetid: '8d9736fa-99de-4dee-98be-59a595c3a026'
ms:contentKeyID: 20105778
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb679962(v=MSDN.10)'
---

Guía de seguridad de Windows Vista
==================================

### Apéndice A: Configuración de directivas de grupo de seguridad

Publicado: noviembre 8, 2006

##### En esta página

[](#eeaa)[Información general](#eeaa)
[](#edaa)[Directiva de dominio](#edaa)
[](#ecaa)[Directiva de equipos](#ecaa)
[](#ebaa)[Directiva de usuario](#ebaa)
[](#eaaa)[Más información](#eaaa)

### Información general

En este apéndice se describen las configuraciones de directivas de seguridad para los entornos de Cliente de empresa (EC) y Seguridad especializada: funcionalidad limitada (SSLF). Asimismo, el apéndice también ofrece los valores configurados mediante el proceso automatizado que recomienda la *Guía de seguridad de Windows* *Vista* en el capítulo 1, “Implementación de líneas de base de seguridad”, y en el capítulo 5, “Seguridad especializada: funcionalidad limitada”. El archivo Windows Vista Security Guide Settings.xls (en inglés) que acompaña la guía es otro recurso útil para comparar los valores de configuración.

El apéndice presenta la configuración tal como aparece en la interfaz de usuario del Editor de objetos de directiva de grupo del sistema operativo Windows Vista™.

**Nota**   Las configuraciones de directiva de grupo nuevas en Windows Vista se indican con el símbolo §.

Las configuraciones de seguridad que aborda esta guía se agrupan en las tres secciones principales siguientes:

-   **Directiva de dominio**. La configuración de esta sección se aplica al dominio.

-   **Directiva de equipos**. La configuración de esta sección se aplica a los equipos portátiles y de escritorio del dominio.

-   **Directiva de usuario**. La configuración de esta sección se aplica a los usuarios del dominio.

En cada una de las secciones principales, aparecen sendas tablas donde se enumeran los nombres de los valores así como los valores de línea de base que el equipo de ingeniería desarrolló para las dos configuraciones de seguridad (EC y SSLF) que se recomiendan en esta guía.

Los valores aceptables varían en gran medida según la configuración. La mayoría de los valores se configura en **Habilitado** o **Deshabilitado** o bien en algún otro valor incluido en el Editor de objetos de directiva de grupo. No obstante, muchos otros requieren que especifique valores numéricos o grupos de seguridad.

La configuración de directivas de derechos de usuarios requiere nombres de usuarios y grupos específicos. Si un derecho de usuario en particular no se otorga a algún usuario o grupo, el Editor de objetos de directiva de grupo muestra el valor como habilitado pero no aparece ningún usuario ni grupo. Las tablas de este apéndice muestran el valor **Ninguno** para describir los valores configurados de este modo.

Los objetos de directiva de grupo (GPO) incluidos en esta guía no afectan a los valores configurados como **No definido** o **Sin configurar**. Esta configuración es muy distinta de la realizada en **Ninguno** que se explicaba antes. Los administradores de equipos locales pueden modificar con facilidad las configuraciones que no modifican los GPO incluidos con esta guía siempre que no estén configuradas ya por otro GPO del entorno. Como consecuencia pueden producirse incoherencias de configuración en el entorno que, en ocasiones, ponen en peligro la seguridad. Por este motivo, muchas de las configuraciones recomendadas sólo aplican la configuración predeterminada de Windows Vista.

En la tabla siguiente se muestra un par de ejemplos de posibles configuraciones distintas:

**Tabla A1. Ejemplos de Asignación de derechos de usuario**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir inicio de sesión a través de Terminal Services</td>
<td style="border:1px solid black;">Administradores, Usuarios de escritorio remoto</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ajustar las cuotas de la memoria para un proceso</td>
<td style="border:1px solid black;">Administradores, Servicio local, Servicio de red</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores, Servicio local, Servicio de red</td>
</tr>
</tbody>
</table>
  
El valor predeterminado para **Permitir inicio de sesión a través de Terminal Services** es **No definido** en **GPO de equipos para EC**, lo que significa que no se aplica cambio alguno al valor predeterminado. Sin embargo, en **GPO de equipos para SSLF**, el valor **Ninguno** (un valor habilitado que está en blanco en el Editor de objetos de directiva de grupo) indica que ningún usuario ni grupo tiene derecho a iniciar sesión en dichos servicios. Es más, ni siquiera el administrador de equipos locales tiene facilidades para cambiar este valor ya que se aplica por medio de una directiva de grupo.
  
De igual modo, el valor predeterminado para **Ajustar cuotas de memoria para un proceso** en **GPO de equipos para EC** no modifica la opción predeterminada. En esta configuración, el administrador de equipos locales puede modificar sin problemas este valor. Sin embargo, en el entorno SSLF, no sería posible porque el **GPO de equipos para SSLF** aplica por fuerza el valor predeterminado.
  
Por último, varias de las configuraciones recomendadas en la guía necesitan determinada información de entorno para ofrecer una funcionalidad correcta. Como no se pueden incluir estos valores en los GPO de esta guía, se configuran en las tablas con el valor **Recomendado**. Obtenga más información sobre estos valores a fin de determinar la configuración adecuada.
  
**Advertencia:**
  
La funcionalidad de numerosas configuraciones de este apéndice depende de otras configuraciones; se trata de dependencias de diseño. Además, los valores de algunas configuraciones exigen su personalización según las necesidades concretas del entorno para funcionar correctamente. Por estos motivos, si modifica alguno de los valores de configuración recomendados en cualquiera de los entornos (EC o SSLF), debe organizar pruebas exhaustivas en los equipos cliente del entorno para garantizar una funcionalidad completa.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de dominio
  
Las configuraciones de seguridad de esta sección del apéndice se aplican al dominio mediante el nodo **Configuración del equipo** del Editor de objetos de directiva de grupo. Dentro de este nodo, el subnodo **Configuración de Windows** presenta los grupos de configuraciones siguientes:
  
-   [Directiva de contraseñas](#_password_policy_settings)
  
-   [Directiva de bloqueo de cuentas](#_account_lockout_policy)
  
#### Directiva de contraseñas
  
Si usa contraseñas complejas y las cambia a menudo, disminuye la probabilidad de que se produzca con éxito un ataque contra las contraseñas. La configuración de la directiva de contraseñas controla la complejidad y la duración de éstas. Sólo se configura por directiva de grupo de nivel de dominio.
  
Puede establecer la configuración de directiva de contraseñas en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directiva de contraseñas**
  
En la siguiente tabla se resumen las recomendaciones acerca de la configuración de la directiva de contraseñas para los dos tipos de entornos seguros definidos en esta guía. Cada uno de los valores se describe en las subsecciones que aparecen a continuación.
  
**Tabla A2. Recomendaciones para la configuración de la directiva de contraseñas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >Valor predeterminado del controlador de dominio</th>
<th style="border:1px solid black;" >GPO de dominio de VSG para EC</th>
<th style="border:1px solid black;" >GPO de dominio de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Exigir historial de contraseñas</td>
<td style="border:1px solid black;">0 contraseñas recordadas</td>
<td style="border:1px solid black;">24 contraseñas recordadas</td>
<td style="border:1px solid black;">24 contraseñas recordadas</td>
<td style="border:1px solid black;">24 contraseñas recordadas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Vigencia máxima de la contraseña</td>
<td style="border:1px solid black;">42 días</td>
<td style="border:1px solid black;">42 días</td>
<td style="border:1px solid black;">90 días</td>
<td style="border:1px solid black;">90 días</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Vigencia mínima de la contraseña</td>
<td style="border:1px solid black;">0 días</td>
<td style="border:1px solid black;">1 día</td>
<td style="border:1px solid black;">1 día</td>
<td style="border:1px solid black;">1 día</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Longitud mínima de la contraseña</td>
<td style="border:1px solid black;">0 caracteres</td>
<td style="border:1px solid black;">7 caracteres</td>
<td style="border:1px solid black;">8 caracteres</td>
<td style="border:1px solid black;">12 caracteres</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">La contraseña debe cumplir los requisitos de complejidad</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenar contraseñas usando cifrado reversible</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Exigir historial de contraseñas**  
Esta configuración de directiva determina el número de contraseñas únicas renovadas que se debe asociar a una cuenta de usuario antes de poder reutilizar alguna contraseña antigua. El valor de esta configuración de directiva debe estar comprendido entre 0 y 24 contraseñas. El valor predeterminado para Windows Vista es de 0 contraseñas pero, en los dominios, es de 24 contraseñas. Para mantener la eficacia de esta configuración de directiva, utilice el parámetro **Vigencia mínima de la contraseña** con objeto de evitar que los usuarios cambien repetidamente sus contraseñas.
  
Configure el valor **Exigir historial de contraseñas** en **24 contraseñas** en los dos entornos de seguridad de esta guía.
  
**Vigencia máxima de la contraseña**  
Los valores de esta configuración de directiva están comprendidos entre 1 y 999 días. También se puede establecer en 0 para especificar que las contraseñas no caducan nunca. Esta configuración de directiva define durante cuánto tiempo pueden emplear los usuarios sus contraseñas antes de que caduquen. El valor predeterminado de esta configuración de directiva es de 42 días. Como los atacantes pueden apropiarse de las contraseñas, cuanto más frecuente sea el cambio de éstas, menos oportunidades tienen los atacantes de usar contraseñas robadas. En cambio, cuanto menor sea este valor, mayores son las posibilidades de que aumenten las llamadas al departamento de soporte técnico porque los usuarios deben cambiar su contraseña o porque olvidan la vigente.
  
Configure el valor **Vigencia máxima de la contraseña** en **90 días** en los dos entornos de seguridad definidos en esta guía.
  
**Vigencia mínima de la contraseña**  
Esta configuración de directiva determina el número de días que se debe usar una contraseña antes de poder cambiarla. Los valores posibles para esta configuración de directiva van de 1 día a 999 días aunque también se puede establecer en 0 para permitir el cambio inmediato de las contraseñas. El valor predeterminado es de 0 días.
  
El valor de la configuración **Vigencia mínima de la contraseña** debe ser inferior al especificado para **Vigencia máxima de la contraseña**, a menos que el valor deesta última opción se configure como 0, lo que hace que la contraseña nunca caduque. Si el valor de **Vigencia máxima de la contraseña** se establece en 0, el valor de esta configuración de directiva se puede establecer en cualquier valor comprendido entre 0 y 999.
  
Para que la configuración **Exigir historial de contraseñas** sea eficaz, este valor se tiene que configurar en un número superior a  . Si la configuración **Vigencia mínima de la contraseña** es 0, los usuarios pueden cambiar de contraseña hasta que se les permita reutilizar una antigua.
  
Configure el valor **Vigencia mínima de la contraseña** en **1 día** en los dos entornos de seguridad definidos en esta guía. Este valor impide que los usuarios reutilicen la misma contraseña, ya que debe esperarse un día entero antes de poder cambiar la contraseña. También les anima a recordar las nuevas contraseñas, ya que deben utilizarlas durante al menos un día antes del restablecimiento. Por último, evita que los usuarios burlen la restricción de la configuración **Exigir historial de contraseñas**.
  
**Longitud mínima de la contraseña**  
Esta configuración de directiva determina el número mínimo de caracteres que componen una contraseña para una cuenta de usuario. Hay distintas teorías sobre la longitud óptima de las contraseñas en cada organización; quizá sería mejor emplear “frases codificadas” en lugar de simples contraseñas. En Microsoft® Windows 2000 y versiones posteriores, las frases codificadas pueden ser bastante largas e incluso tener espacios. Así, “Quiero beberme un batido de 5 €” es una frase cifrada válida bastante más segura que una cadena compuesta de 8 o 10 caracteres que incluya números y letras aleatorios. Además, es más fácil de recordar. Recuerde que es necesario instruir a los usuarios acerca de la selección y el mantenimiento adecuados de las contraseñas, sobre todo en lo referente a su longitud.
  
En el entorno EC, asegúrese de que el valor para el parámetro **Longitud mínima de la contraseña** se configure en **8 caracteres**. Esta configuración de directiva es lo bastante larga como para ofrecer una seguridad adecuada. En el entorno SSLF, configure el valor en **12 caracteres.**
  
**La contraseña debe cumplir los requisitos de complejidad**  
Esta configuración de directiva comprueba todas las contraseñas nuevas para garantizar que se cumplen los requisitos básicos de una contraseña segura. De manera predeterminada, el valor de esta configuración de directiva en Windows Vista se configura en **Deshabilitado**; en cambio, está **Habilitado** en los dominios de Microsoft Windows Server® 2003 de los dos entornos descritos en esta guía.
  
Si esta directiva se encuentra habilitada, las contraseñas han de cumplir los requisitos mínimos siguientes:
  
-   No pueden contener más de dos caracteres seguidos del nombre de la cuenta del usuario ni tampoco partes del nombre completo del usuario.
  
-   Deben tener, como mínimo, seis caracteres.
  
-   Los caracteres pueden pertenecer a tres de las cuatro categorías siguientes:
  
    -   Mayúsculas válidas en inglés (de la A a la Z)
  
    -   Minúsculas válidas en inglés (de la a a la z)
  
    -   Dígitos en base 10 (del 0 al 9)
  
    -   Caracteres no alfabéticos (por ejemplo, !, $, \# o %)
  
Cada carácter adicional de una contraseña aumenta su complejidad de forma exponencial. Así, una contraseña de siete letras minúsculas tendría unas 267 (alrededor de 8 x 109 u 8.000 millones) combinaciones posibles. A razón de 1.000.000 de intentos por segundo (capacidad que ofrecen muchas utilidades de descifrado de contraseñas), sólo se necesitarían 133 minutos para descifrarla. Una contraseña alfabética de 7 caracteres en la que se distingan mayúsculas y minúsculas tiene 527 combinaciones. Una contraseña alfanumérica de 7 caracteres en la que se distingan mayúsculas y minúsculas sin puntuación tiene 627 combinaciones. Una contraseña de 8 caracteres tiene 268, o 2 x 1011, combinaciones posibles. Aunque pueda parecer una cifra descomunal, a 1.000.000 de intentos por segundo, sólo harían falta 59 horas para probar todas las posibles contraseñas. Recuerde que estos plazos aumentan de manera significativa al incluir en las contraseñas caracteres ALT y otros caracteres de teclado especiales como “!” o “@”. Si se usa con propiedad la configuración de contraseñas, se dificultan los ataques por fuerza bruta.
  
**Almacenar contraseñas usando cifrado reversible**  
Esta configuración de directiva determina si el sistema operativo almacena contraseñas de modo que se emplee el cifrado reversible, lo cual es necesario para los protocolos de aplicaciones que deben conocer la contraseña de los usuarios para la autenticación. Las contraseñas almacenadas con cifrado reversible coinciden básicamente con las versiones de texto sin formato de las contraseñas. Por ello, esta configuración de directiva sólo se debe habilitar cuando los requisitos de las aplicaciones sean más importantes que la necesidad de proteger la información sobre contraseñas. El valor predeterminado de esta configuración de directiva es **Deshabilitado**.
  
Es preciso habilitar esta configuración de directiva al usar el Protocolo de autenticación por desafío mutuo (CHAP) por acceso remoto o el Servicio de autenticación de Internet (IAS). También se exige cuando se usa la autenticación implícita en los Servicios de Internet Information Server (IIS).
  
Asegúrese de que la configuración **Almacenar contraseñas usando cifrado reversible para todos los usuarios del dominio** esté **Deshabilitada**, tal como se encuentra en el objeto de directiva de grupo (GPO) de dominio predeterminado de Windows Server 2003 y en la directiva de seguridad local para estaciones de trabajo y servidores. Esta configuración de directiva también está **Deshabilitada** en los dos entornos que se definen en esta guía.
  
##### Cómo conseguir que los usuarios cambien de contraseña sólo cuando sea necesario
  
Además de estas directivas de contraseñas, el control centralizado de todos los usuarios es un requisito para algunas organizaciones. En esta sección se describe cómo impedir que los usuarios cambien las contraseñas excepto en aquellos casos en los que sea necesario.
  
El control centralizado de las contraseñas de los usuarios es la piedra angular de cualquier esquema de seguridad de un sistema Windows Vista bien diseñado. Puede usar la directiva de grupo para establecer las vigencias mínima y máxima de las contraseñas tal y como se ha descrito antes. Sin embargo, el hecho de que sea necesario cambiar frecuentemente las contraseñas puede dar lugar a que a los usuarios burlen la configuración **Exigir historial de contraseñas** del entorno. El requisito de que las contraseñas sean demasiado largas también puede provocar más llamadas al departamento de soporte técnico por parte de usuarios que olviden sus contraseñas.
  
Los usuarios pueden cambiar de contraseña durante el período que transcurre entre las vigencias mínima y máxima establecidas para las contraseñas. Sin embargo, el diseño de seguridad para el entorno SSLF requiere que los usuarios cambien sus contraseñas únicamente cuando el sistema operativo así lo solicite, después de que sus contraseñas hayan llegado a la vigencia máxima de 42 días. Para lograr este grado de control, los administradores pueden deshabilitar el botón **Cambiar contraseña** en el cuadro de diálogo **Seguridad de Windows** que aparece al presionar Ctrl+Alt+Supr.
  
Esta configuración se puede implementar en todo el dominio con la directiva de grupo o para uno o varios usuarios concretos mediante la edición del Registro. Para obtener más información acerca de esta configuración, consulte el artículo 324744 de Microsoft Knowledge Base, “[Cómo impedir que los usuarios cambien una contraseña excepto cuando se les pida en Windows Server 2003](http://support.microsoft.com/kb/324744)”. Si el dominio está basado en Windows 2000, consulte el artículo 309799 de Knowledge Base, “[CÓMO: Impedir que los usuarios cambien una contraseña excepto cuando se les pida](http://support.microsoft.com/kb/309799)”.
  
#### Configuración de directiva de bloqueo de cuentas
  
La directiva de bloqueo de cuentas es una característica de seguridad del servicio de directorios Active Directory® que bloquea las cuentas de usuario. El bloqueo impide el inicio de sesión después de un número determinado de intentos de inicio de sesión sin éxito dentro del período especificado. Los controladores de dominio realizan el seguimiento de los intentos; el número de intentos permitidos y el período se basan en los valores establecidos en la configuración del bloqueo de cuentas. Además, se puede especificar la duración del bloqueo.
  
Estas configuraciones de directiva ayudan a evitar que los atacantes puedan averiguar las contraseñas de los usuarios y reducen las probabilidades de ataques con éxito en el entorno de red. Sin embargo, es probable que la habilitación de una directiva de bloqueo de cuentas provoque más problemas de soporte para los usuarios de red. Antes de habilitar la configuración siguiente, asegúrese de que su organización desea aceptar esta carga de administración adicional. Para muchas organizaciones, una solución mejorada y menos costosa consiste en analizar los registros de eventos de seguridad para los controladores de dominio y generar alarmas administrativas cuando parezca que alguien intenta adivinar las contraseñas de cuentas de usuario.
  
Puede establecer la configuración de directiva de bloqueo de cuentas en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**  
**\\Directivas de cuenta\\Directiva de bloqueo de cuentas**
  
La tabla siguiente incluye las recomendaciones sobre la configuración de la directiva de bloqueo de cuentas para los dos entornos de seguridad que se definen en esta guía. Cada uno de los valores se describe en las subsecciones que aparecen a continuación.
  
**Tabla A3. Recomendaciones para la configuración de la directiva de bloqueo de cuentas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >Valor predeterminado del controlador de dominio</th>
<th style="border:1px solid black;" >GPO de dominio de VSG para EC</th>
<th style="border:1px solid black;" >GPO de dominio de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Duración del bloqueo de cuenta</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">15 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Umbral de bloqueo de la cuenta</td>
<td style="border:1px solid black;">0 intentos de inicio de sesión no válidos</td>
<td style="border:1px solid black;">0 intentos de inicio de sesión no válidos</td>
<td style="border:1px solid black;">50 intentos de inicio de sesión no válidos</td>
<td style="border:1px solid black;">10 intentos de inicio de sesión no válidos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Restablecer recuentos de bloqueo de cuenta tras</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">15 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
</tr>
</tbody>
</table>
  
**Duración del bloqueo de cuenta**  
Esta configuración de directiva determina el tiempo que debe transcurrir antes de que una cuenta bloqueada se desbloquee y de que el usuario pueda volver a intentar iniciar sesión. Para ello, hay que especificar el número de minutos que la cuenta bloqueada permanece no disponible. Si el valor de esta configuración de directiva está establecido en 0, las cuentas permanecen bloqueadas hasta que el administrador las desbloquee de forma manual. El valor predeterminado de Windows Vista para esta configuración de directiva es **No definido**.
  
Para reducir el número de llamadas al departamento de soporte técnico y proporcionar una infraestructura segura, configure el valor de **Duración del bloqueo de cuenta** en **15 minutos** para los entornos EC y SSLF que se definen en esta guía.
  
Aunque quizá parezca una buena idea configurar un valor elevado para esta configuración de directiva, es probable que, en ese caso, se incremente el número de llamadas al departamento de soporte técnico para desbloquear cuentas bloqueadas por error. El valor de configuración recomendado de 15 minutos se considera un tiempo razonable de espera de los usuarios antes de intentar iniciar sesión otra vez y ofrece un grado aceptable de protección frente a ataques de fuerza bruta contra las contraseñas. Los usuarios han de saber el tiempo que permanecen activos los bloqueos para que sólo llamen al departamento de soporte técnico en caso de que el acceso al equipo sea del todo improrrogable.
  
**Umbral de bloqueo de cuenta**  
Esta configuración de directiva determina el número de intentos sin éxito para iniciar sesión antes de que se produzca el bloqueo. Los usuarios autorizados pueden bloquear sus propias cuentas en caso de no recordar su contraseña, escribirla incorrectamente o cambiarla en un equipo mientras han iniciado sesión en otro. El equipo con la contraseña incorrecta puede intentar de forma continuada autenticar al usuario y, puesto que la contraseña que usa para ello es incorrecta, tiene lugar el bloqueo. Para evitar el bloqueo accidental de usuarios autorizados, establezca el umbral de bloqueos de la cuenta en un número alto. El valor predeterminado para esta configuración de directiva es de 0 intentos de inicio de sesión no válidos, con lo que se deshabilita la característica del bloqueo de cuentas.
  
Establezca el valor para la configuración **Umbral de bloqueo de cuenta** en **50**  **intentos de inicio de sesión no válidos** para entornos EC y **10 intentos de inicio de sesión no válidos** para entornos SSLF.
  
Dado que un atacante puede aprovechar este estado de bloqueo como una denegación de servicio (DoS) y desencadenar un bloqueo que afecte a un gran número de cuentas, es aconsejable que la organización determine si debe aplicar esta configuración de directiva en función de las amenazas identificadas y de los riesgos que se desee evitar. Son dos las opciones que se deben considerar en el caso de esta configuración de directiva.
  
-   Establezca el valor de **Umbral de bloqueo de cuenta** en **0** para asegurarse de que las cuentas no se bloquean. Este valor evitará los ataques DoS que intenten bloquear las cuentas de su organización. Se reducirán también las llamadas al servicio de asistencia, ya que los usuarios no podrán bloquear sus cuentas accidentalmente. Sin embargo, este valor de configuración no evitará un ataque de fuerza bruta. También deben considerarse las siguientes defensas:
  
    -   Una directiva de contraseñas que obligue a los usuarios a tener contraseñas complejas compuestas de 8 o más caracteres.
  
    -   Un mecanismo de auditoría eficaz que avise a los administradores cuando se produzca una serie de bloqueos de cuentas en el entorno. Por ejemplo, la solución de auditoría debe supervisar el evento de seguridad 539, en el que se señala un error de inicio de sesión. Este evento indica el bloqueo de la cuenta en el momento en que se intenta iniciar sesión.
  
La segunda opción es la siguiente:
  
-   Configure el **Umbral de bloqueo de cuenta** con un valor que proporcione a los usuarios la posibilidad de escribir incorrectamente su contraseña varias veces de forma accidental pero que bloquee la cuenta si se produce un ataque de fuerza bruta. Un valor de configuración de 50 inicios de sesión no válidos para entornos EC y 10 para entornos de tipo SSLF garantiza un nivel de seguridad adecuado y una capacidad de uso aceptable. Esta configuración evita que las cuentas se bloqueen por error y reduce el número de llamadas al servicio de soporte técnico pero no impide los ataques DoS.
  
**Restablecer recuentos de bloqueo de cuenta tras**  
Esta configuración de directiva determina el plazo de tiempo antes de que el **Umbral de bloqueo de cuenta** se restablezca a cero. El valor predeterminado de esta configuración de directiva es **No definido**. Si se define el **Umbral de bloqueo de cuenta**, este tiempo de restablecimiento debe ser inferior o igual al valor de **Duración del bloqueo de cuenta**.
  
Establezca el valor de la configuración **Restablecer recuentos de bloqueo de cuenta tras** en **15** **minutos** para los entornos EC y SSLF que se definen en esta guía.
  
Si deja el valor predeterminado para esta configuración de directiva o configura el valor con un intervalo demasiado largo, su entorno podría ser vulnerable a un ataque de DoS. Un atacante podría realizar una serie de intentos de inicio de sesión malintencionados en todas las cuentas de usuario de la organización y bloquearlas, como ya se describió en este apéndice. Si no se determina ninguna directiva para restablecer el bloqueo de las cuentas, los administradores deben hacerlo de forma manual. Por el contrario, si se establece un valor de tiempo razonable para esta configuración de directiva, los usuarios no tendrán acceso durante un período de tiempo establecido hasta que todas las cuentas se desbloqueen automáticamente. El valor de configuración recomendado de 15 minutos se considera un tiempo razonable que es probable que acepten los usuarios y que ayuda a reducir al mínimo el número de llamadas al departamento de soporte técnico. Los usuarios han de saber el tiempo que deben esperar para volver a iniciar sesión para que sólo llamen al departamento de soporte técnico en caso de que el acceso al equipo sea del todo improrrogable.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de equipos
  
Las configuraciones de seguridad de esta sección del apéndice se aplican a los equipos portátiles y de escritorio del dominio mediante el nodo **Configuración del equipo** del Editor de objetos de directiva de grupo. Dentro de este nodo, estas configuraciones aparecen en los subnodos **Configuración de Windows** y **Plantillas administrativas**.
  
#### Configuración del equipo\\Configuración de Windows
  
El subdirectorio Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales presenta los grupos de configuraciones siguientes:
  
-   [Directiva de auditoría](#_audit_policy_settings_1)
  
-   [Asignación de derechos de usuario](#_user_rights_assignment_1)
  
-   [Opciones de seguridad](#_security_options_settings)
  
El subdirectorio Configuración del equipo\\Configuración de Windows\\Configuración de seguridad presenta los grupos de configuraciones siguientes:
  
-   [Seguridad del registro de eventos](#_event_log_security)
  
-   [Firewall de Windows con seguridad avanzada](#_windows_firewall_with)
  
##### Directiva de auditoría
  
Las directivas de auditoría determinan los eventos de seguridad que se envían a los administradores, de modo que se registre la actividad del sistema o del usuario en las categorías de eventos especificadas. El administrador puede supervisar la actividad relacionada con la seguridad como, por ejemplo, quién tiene acceso a un objeto, el momento en que los usuarios inician o cierran sesión en sus equipos o si se realizan cambios en una configuración de directiva de auditoría. Por todo ello, Microsoft recomienda que se cree una directiva de auditoría para un administrador con el fin de implementarla en el entorno.
  
Sin embargo, antes de implementar una directiva de auditoría, tiene que decidir qué categorías de eventos deben ser auditadas en el entorno. La configuración de auditoría que se seleccione en las categorías de eventos definirá la directiva de auditoría. Cuando defina una configuración de auditoría para categorías de eventos específicas, un administrador podrá crear una directiva de auditoría que responda a las necesidades de su organización en materia de seguridad.
  
Si no se establece ninguna configuración de auditoría, resulta difícil o no se puede determinar lo que sucede durante un incidente de seguridad. No obstante, si se configura la auditoría de manera que demasiadas actividades autorizadas generen eventos, el registro de eventos de seguridad se sobrecarga de datos. La información de las secciones siguientes le ayuda a decidir qué debe supervisar para facilitar la recopilación de datos de auditoría pertinentes para su organización.
  
Windows Vista incluye las nueve categorías de directivas de auditoría que existen en versiones anteriores de Windows, a saber:
  
-   [Sistema](#_system_2)
  
-   [Inicio/cierre de sesión](#_logon/logoff_1)
  
-   [Acceso a objetos](#_object_access)
  
-   [Uso de privilegios](#_privilege_use)
  
-   [Seguimiento detallado](#_detailed_tracking_1)
  
-   [Cambio de directiva](#_policy_change)
  
-   [Administración de cuentas](#_account_management)
  
-   [Acceso DS](#_ds_access_1)
  
-   [Inicio de sesión de cuenta](#_account_logon)
  
La diferencia estriba en que, con Windows Vista, la administración de las directivas de auditoría es más precisa puesto que se incluyen cincuenta subcategorías de directivas de auditoría. Aunque no todas las subcategorías se aplican a equipos basados en Windows Vista, muchas de ellas se pueden configurar para registrar eventos concretos que aportan información de enorme utilidad.
  
En otras versiones, la configuración de cualquiera de las nueve categorías de auditoría resultaba una tarea muy sencilla gracias a la directiva de grupo. Si bien cabe esa misma posibilidad con Windows Vista, las nuevas subcategorías no se pueden configurar de manera individual con el Editor de objetos de directiva de grupo porque no se encuentran expuestas en éste. Al configurar cualquiera de las categorías de auditoría en Windows Vista con los valores presentes en el Editor de objetos de directiva de grupo, también se configuran todas las subcategorías. En este caso, lo más probable es que se produzca un registro excesivo de auditoría que llene con rapidez los registros de eventos.
  
La acción recomendada consiste en configurar sólo las subcategorías de auditoría necesarias. Para configurar cada subcategoría, hay que usar una herramienta de línea de comandos incluida en Windows Vista denominada *AuditPol.exe*.
  
El uso de una herramienta de línea de comandos dificulta la implementación de la directiva de auditoría recomendada en varios equipos. La buena noticia es que Microsoft también ofrece una solución para configurar las subcategorías de auditoría con la directiva de grupo. Esta solución se implementa de forma automática mediante las secuencias de comandos y los GPO incluidos con esta guía.
  
Al ejecutar la secuencia de comandos GPOAccelerator.wsf como se explica en los capítulos 1 y 5 de la guía, ésta copia automáticamente los archivos siguientes en el recurso compartido NETLOGON de alguno de los controladores de dominio.
  
Para el entorno EC:
  
-   EC-VSGAuditPolicy.cmd
  
-   EC-VSGApplyAuditPolicy.cmd
  
-   EC-VSGAuditPolicy.txt
  
Para el entorno SSLF:
  
-   SSLF-VSGAuditPolicy.cmd
  
-   SSLF-VSGApplyAuditPolicy.cmd
  
-   SSLF-VSGAuditPolicy.txt
  
A continuación, estos archivos se replican de forma automática al recurso compartido NETLOGON de los controladores del dominio de Active Directory. Los GPO específicos de los equipos que crea la secuencia de comandos GPOAccelerator.wsf incluyen una secuencia de comandos de inicio del equipo que ejecuta estos archivos con el fin de establecer las configuraciones de directivas de auditoría recomendadas. La primera vez que se ejecutan dichos archivos en un equipo, se crea una tarea programada llamada VSGAudit. Esta tarea se ejecuta cada hora para garantizar que las configuraciones de la directiva de auditoría estén actualizadas.
  
Para obtener más información sobre la solución de configuración de nuevos valores de directivas de auditoría en Windows Vista en dominios basados en Windows Server 2003, consulte el artículo 921469 de Knowledge Base, “[Cómo usar Directiva de grupo para configurar las opciones detalladas de auditoría de seguridad de los equipos cliente Windows Vista en un dominio de Windows Server 2003 o de Windows 2000](http://support.microsoft.com/kb/921469)”.
  
En la tabla siguiente se resumen las recomendaciones sobre la configuración de directivas de auditoría para equipos cliente de escritorio y portátiles en los dos tipos de entornos seguros que se tratan en esta guía. Debe revisar estas recomendaciones y ajustarlas según corresponda para su organización. Al final de esta sección se aporta información sobre el procedimiento para modificar las configuraciones de directivas de auditoría configuradas por los GPO incluidos con esta guía.
  
No obstante, es importante tener especial precaución con los parámetros de auditoría que puedan generar un gran volumen de tráfico. Por ejemplo, si habilita la auditoría de errores y aciertos para todas las **subcategorías de uso de privilegios**, se generan tantos eventos de auditoría que resulta complicado encontrar otros tipos de entradas en el registro de eventos de seguridad. Ese tipo de configuración podría tener también una repercusión significativa en el rendimiento.
  
En las secciones siguientes se describe con brevedad cada una de las directivas de auditoría. Cada sección dispone de una tabla con recomendaciones para equipos cliente tanto de escritorio como portátiles en los dos tipos de entornos seguros que se tratan en esta guía.
  
**Nota**   Por cuestiones de tiempo, en esta guía no se ofrecen descripciones de todas las subcategorías de directivas de auditoría. La próxima versión de la guía sobre [*amenazas y contramedidas*](http://go.microsoft.com/fwlink/?linkid=15159) incluirá descripciones detalladas de las 50 subcategorías de directivas de auditoría.
  
###### Sistema
  
La categoría de auditoría del sistema permite supervisar eventos del sistema correctos y erróneos. Asimismo, proporciona un registro de estos eventos que puede ayudar a determinar los accesos no autorizados al sistema. Entre los eventos del sistema se incluyen el inicio y el apagado de los equipos del entorno, los registros de eventos completos u otros eventos relacionados con la seguridad que afectan a todo el sistema.
  
En Windows Vista, la categoría de auditoría del sistema contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A4. Recomendaciones para las subcategorías de la directiva de auditoría del sistema**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Extensión del sistema de seguridad</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Integridad del sistema</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Controlador IPsec</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Otros eventos del sistema</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Cambio de estado de seguridad</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Inicio/cierre de sesión
  
Esta categoría de auditoría genera eventos que registran la creación y la destrucción de sesiones de inicio. Estos eventos se producen en el equipo al que se tiene acceso. En el caso de inicios de sesión interactivos, estos eventos se generan en el equipo en el que se inicia sesión. Si se lleva a cabo un inicio de sesión de red para tener acceso a un recurso compartido, estos eventos se generan en el equipo que alberga el recurso al que se obtiene acceso.
  
Si configura el valor **Auditar eventos de inicio de sesión** como **Sin auditoría**, resulta difícil o no se puede determinar qué usuario tiene o intenta tener acceso a equipos de la organización.
  
En Windows Vista, la categoría de auditoría de eventos de inicio/cierre de sesión contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A5. Recomendaciones para las subcategorías de la directiva de auditoría de inicios/cierres de sesión**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Inicio de sesión</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Cerrar sesión</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Bloqueo de cuenta
<strong>Nota</strong>   No se asigna ningún evento a esta subcategoría.</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Modo principal IPsec</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Modo rápido IPsec</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Modo extendido IPsec</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Inicio de sesión especial</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Otros eventos de inicio/cierre de sesión</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Acceso de objeto
  
Por sí misma, esta configuración de directiva no provoca que se audite ningún evento. Determina si debe auditarse el evento de un usuario que tiene acceso a un objeto (por ejemplo, un archivo, una carpeta, una clave de Registro o una impresora) con la lista de control de acceso al sistema (SACL) especificada, lo que provoca que tenga lugar la auditoría.
  
Una SACL se compone de entradas de control de acceso (ACE), cada una de las cuales contiene tres fragmentos de información:
  
-   Entidad de seguridad (usuario, equipo o grupo) que se debe auditar.
  
-   Tipo de acceso concreto que se va a auditar, denominado máscara de acceso.
  
-   Indicador de si se deben auditar los eventos de acceso erróneos, los correctos o ambos.
  
Si configura el parámetro **Auditar acceso a objetos** como **Correcto**, se genera una entrada de auditoría cada vez que un usuario tiene acceso a un objeto con una SACL especificada. Si establece esta configuración de directiva como **Erróneo**, se genera una entrada de auditoría cada vez que un usuario intenta sin éxito tener acceso a un objeto con la SACL especificada.
  
Al configurar las listas de acceso al sistema, las organizaciones deben definir sólo las acciones que desean habilitar. Por ejemplo, quizá desee habilitar la configuración de auditoría **Escribir datos y Anexar datos** para los archivos ejecutables, con el fin de realizar un seguimiento de cuándo se cambian o reemplazan, ya que los virus, los gusanos y los troyanos suelen dirigirse a los archivos ejecutables. Asimismo, quizá desee realizar un seguimiento de cuándo se tiene acceso o se cambian documentos confidenciales.
  
La categoría de auditoría de eventos de acceso a objetos contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A6. Recomendaciones para las subcategorías de la directiva de auditoría de acceso a objetos**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Sistema de archivos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Registro</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Erróneo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Objeto de kernel</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ SAM</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Servicios de certificación</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Generación por aplicación</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Manipulación de identificadores</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Recurso compartido de archivos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Filtrado de colocación de paquetes de la plataforma</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Filtrado de conexión de la plataforma</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Otros eventos de acceso a objetos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
En los siguientes procedimientos se analiza la forma de configurar las reglas de auditoría para un archivo o una carpeta y de comprobar dichas reglas con cada objeto de la carpeta o del archivo que se haya especificado.
  
**Nota**   Configure con *Auditpol.exe* la subcategoría Sistema de archivos de manera que se auditen los eventos **Correctos y erróneos** para que, en los pasos siguientes, se registren estos eventos en el registro de eventos de seguridad.
  
**Para definir una regla de auditoría para un archivo o una carpeta**
  
1.  En el Explorador de Windows, busque el archivo o la carpeta que le interese y haga clic en el objeto.
  
2.  En el menú **Archivo**, elija **Propiedades**.
  
3.  Haga clic en la ficha **Seguridad** y, a continuación, en el botón **Opciones avanzadas**.
  
4.  Haga clic en la ficha **Auditoría**.
  
5.  Si se le piden credenciales administrativas, elija **Continuar**, escriba su nombre de usuario y su contraseña y presione ENTRAR.
  
6.  Elija el botón **Agregar**. Se muestra el cuadro de diálogo **Seleccionar usuario**,**equipo**,o **grupo**.
  
7.  Haga clic en el botón **Tipos de objetos** y, a continuación, en el cuadro de diálogo **Tipos de objetos**, seleccione los tipos de objetos que desee buscar.
  
    **Nota**   Los tipos de objetos **Usuario**, **Grupo** y **Principio de seguridad integrado** se encuentran seleccionados de forma predeterminada.
  
8.  Haga clic en el botón **Ubicaciones** y, en el cuadro de diálogo **Ubicación**, seleccione su dominio o equipo local.
  
9.  En el cuadro de diálogo **Seleccionar usuarios o grupos**, escriba el nombre del grupo o usuario que desee auditar. A continuación, en **Escriba los nombres de objeto que desea seleccionar**, escriba **Usuarios autenticados** (para auditar el acceso de todos los usuarios autenticados) y haga clic en **Aceptar**. Se mostrará el cuadro de diálogo **Entrada de auditoría**.
  
10. Determine el tipo de acceso que desea auditar en el archivo o carpeta utilizando el cuadro de diálogo **Entrada de auditoría**.
  
    **Nota**   Recuerde que cada acceso puede generar varios eventos en el registro de eventos y provocar un rápido crecimiento del registro.
  
11. En el cuadro de diálogo **Entrada de auditoría**, situado junto a **Listar carpeta / Leer datos**, seleccione **Correcto y Erróneo** y después haga clic en **Aceptar**.
  
12. Las entradas de auditoría habilitadas se mostrarán en la ficha **Auditoría** del cuadro de diálogo **Configuración de seguridad avanzada**.
  
13. Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Propiedades**.
  
**Para probar una regla de auditoría para el archivo o la carpeta**
  
1.  Abra el archivo o la carpeta.
  
2.  Cierre el archivo o la carpeta.
  
3.  Inicie el Visor de eventos. En el registro de eventos de seguridad aparecen varios eventos de acceso a objetos con el **Id. del evento 4663**.
  
4.  Haga doble clic en los eventos según sea necesario para ver información sobre los mismos.
  
###### Uso de privilegios
  
La categoría de auditoría de uso de privilegios determina si se debe auditar cada caso en el que un usuario ejerza un derecho de usuario. Si configura este valor como **Correcto**, se genera una entrada de auditoría cada vez que un derecho de usuario se ejerce correctamente. Si configura este valor como **Erróneo**, se genera una entrada de auditoría cada vez que un derecho de usuario se ejerce sin éxito. Esta configuración de directiva puede generar un gran número de registros de eventos.
  
La categoría de auditoría de eventos de **uso de privilegios** contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A7. Recomendaciones para las subcategorías de la directiva de auditoría de uso de privilegios**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Uso de privilegios reservados</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Uso de privilegios no reservados</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Otros eventos de uso de privilegios<br />
<strong>Nota</strong>   No se asigna ningún evento a esta subcategoría.</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Seguimiento detallado
  
La categoría de auditoría de seguimiento detallado determina si se debe auditar información detallada de seguimiento de eventos tales como la activación de programas, la salida de procesos, la duplicación de identificadores y el acceso indirecto a objetos. La habilitación de la configuración **Auditar el seguimiento de procesos** genera un número considerable de eventos, por lo que, en general, se establece en **Sin auditoría**. Sin embargo, esta configuración puede resultar muy útil durante la respuesta a un incidente a partir del registro detallado de los procesos iniciados y la hora de inicio de cada uno de ellos.
  
La categoría de auditoría de eventos de seguimiento detallado contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A8. Recomendaciones para las subcategorías de la directiva de auditoría de seguimiento detallado**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Finalización de procesos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Actividad de DPAPI</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Eventos de RPC</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Creación de procesos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Cambio de directiva
  
La categoría de auditoría de cambio de directiva determina si se debe auditar cada cambio de directivas de asignación de derechos de usuario, directivas de Firewall de Windows o directivas de confianza o bien los cambios en la propia directiva de auditoría. Los parámetros recomendados le permitirán ver los privilegios de una cuenta que un atacante intente elevar, por ejemplo, mediante la incorporación del privilegio **Depurar programas** o del privilegio **Realizar copias de seguridad de archivos y directorios**.
  
La categoría de auditoría de eventos de **cambio de directiva** contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A9. Recomendaciones para las subcategorías de la directiva de auditoría de cambio de directiva**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Auditar el cambio de directivas</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Cambio de directiva de autenticación</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Cambio de directiva de autorización</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Cambio de directiva para reglas MPSSVC</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Filtrado de cambio de directiva de la plataforma</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Otros eventos de cambio de directiva</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Administración de cuentas
  
La categoría de auditoría de administración de cuentas se emplea para realizar un seguimiento de los intentos de creación de usuarios o grupos, del cambio del nombre de éstos, de la activación o la desactivación de cuentas de usuario, del cambio de contraseñas de cuentas y de la habilitación de la auditoría para los eventos de administración de cuentas. Si habilita esta configuración de directiva de auditoría, los administradores podrán realizar un seguimiento de los eventos con el fin de detectar la creación autorizada, accidental o malintencionada de cuentas de grupos y usuarios.
  
La categoría de auditoría de eventos de **administración de cuentas** contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A10. Recomendaciones para las subcategorías de la directiva de auditoría del sistema de administración de cuentas**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Administración de cuentas de usuario</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Administración de cuentas de equipo</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Administración de grupo de seguridad</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Administración de grupo de distribución</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Administración de grupo de aplicación</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Otros eventos de administración de cuentas</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Acceso DS
  
La categoría de auditoría de acceso DS sólo se aplica a los controladores de dominio. Por ello, tanto la categoría principal como todas sus subcategorías se configuran en **Sin auditoría** en los dos entornos que se abordan en esta guía.
  
La categoría de auditoría de eventos de acceso DS contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A11. Recomendaciones para las subcategorías de la directiva de auditoría de acceso DS**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Cambios del servicio de directorio</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Replicación del servicio de directorio</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Replicación detallada del servicio de directorio</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Acceso del servicio de directorio</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Inicio de sesión de la cuenta
  
La categoría de auditoría de inicio de sesión de cuenta genera eventos para la validación de credenciales. Estos eventos se producen en el equipo con autorización para las credenciales. En el caso de las cuentas de dominio, el controlador de dominio tiene autorización mientras que, para las cuentas locales, es el equipo local el que la tiene. En los entornos de dominio, la mayoría de los eventos de Inicio de sesión de cuenta se producen en el registro de seguridad de los controladores de dominio que tienen autorización para las cuentas de dominio. Sin embargo, estos eventos pueden producirse en otros equipos de la organización si se emplean cuentas locales para iniciar sesión.
  
La categoría de auditoría de eventos de **inicio de sesión de cuenta** contiene las subcategorías representadas en la tabla siguiente.
  
**Tabla A12. Recomendaciones para las subcategorías de la directiva de auditoría de inicio de sesión de cuenta**

 
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
<th style="border:1px solid black;" >Subcategoría</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Validación de credenciales</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">Correcto y erróneo</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Eventos de vale Kerberos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Otros eventos de inicio de sesión de cuenta
<strong>Nota</strong>   No se asigna ningún evento a esta subcategoría.</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Modificación de la configuración de la directiva de auditoría
  
Si desea modificar las subcategorías de la directiva de auditoría y los valores configurados por los GPO incluidos en esta guía, debe usar Auditpol.exe para modificar la configuración de un equipo del entorno y generar un archivo que contenga la configuración de la directiva de auditoría para el entorno. Acto seguido, los GPO de equipo incluidos con la guía aplican la directiva de auditoría modificada a los equipos del entorno.
  
**Para modificar la configuración de la directiva de auditoría**
  
1.  Inicie sesión como administrador de dominio en un equipo que ejecute Windows Vista y que esté asociado al dominio que use Active Directory donde creará los GPO.
  
2.  En el escritorio, elija el botón Inicio de Windows Vista, haga clic en **Todos los programas**, elija **Accesorios**, haga clic con el botón secundario en **Símbolo del sistema** y, a continuación, elija **Ejecutar como administrador**.
  
3.  Borre la configuración actual de directiva de auditoría. Para hacerlo, escriba la línea siguiente en el símbolo del sistema y presione ENTRAR:
  
    ```  
auditpol /clear  
```
  
4.  Con la herramienta de línea de comandos Auditpol.exe, establezca la configuración personalizada de directiva de auditoría que le interese. Escriba, por ejemplo, las líneas siguientes en el símbolo del sistema. Presione ENTRAR después de cada línea.
  
    **Nota** Algunas partes del siguiente fragmento de código están dispuestas en varias líneas sólo para facilitar su lectura. Deben especificarse en una sola línea.
  
    ```  
auditpol /set /subcategory:"IPSEC Main Mode" /failure:enable  
```
  
    **Nota** Para ver todas las categorías y subcategorías posibles, escriba la línea siguiente en el símbolo del sistema y presione ENTRAR:  
    **auditpol /list /subcategory:\***
  
    Escriba la línea siguiente en el símbolo del sistema y presione ENTRAR:
  
    ```  
auditpol /backup /file:EC-AuditPolicy.txt (o SSLF-AuditPolicy.txt)  
```
  
5.  Copie el nuevo archivo **EC-AuditPolicy.txt** (o **SSLF-AuditPolicy.txt**) en el recurso compartido NETLOGON de alguno de los controladores de dominio del entorno y sobrescriba la versión existente.
  
Los GPO de equipo incluidos con la guía emplearán el nuevo archivo EC-AuditPolicy.txt (o SSLF-AuditPolicy.txt) para modificar y establecer la configuración de la directiva de auditoría en los equipos.
  
###### Eliminación de la configuración de la directiva de auditoría
  
Como ya se indicó, la solución implementada por los GPO incluidos con la guía para configurar las subcategorías de la directiva de auditoría crea la tarea programada VSGAudit en todos los equipos del entorno. Si se quitan dichos GPO del entorno, quizá desee eliminar también la tarea programada VSGAudit. En principio, esta tarea no afecta al rendimiento de los equipos que ejecutan Windows Vista aunque se quiten del entorno los GPO incluidos con la guía.
  
**Para eliminar la tarea programada VSGAudit de los equipos del entorno**
  
1.  Según el entorno, elimine los tres archivos siguientes del recurso compartido NETLOGON de uno de los controladores de dominio del entorno:
  
    Para el entorno EC:
  
    -   EC-VSGAuditPolicy.cmd
  
    -   EC-VSGApplyAuditPolicy.cmd
  
    -   EC-VSGAuditPolicy.txt
  
    Para el entorno SSLF:
  
    -   SSLF-VSGAuditPolicy.cmd
  
    -   SSLF-VSGApplyAuditPolicy.cmd
  
    -   SSLF-VSGAuditPolicy.txt
  
2.  Cree un archivo de texto vacío, asígnele el nombre DeleteVSGAudit.txt y cópielo en el recurso compartido NETLOGON de alguno de los controladores de dominio del entorno. El archivo de texto se replica de manera automática a todos los controladores de dominio del entorno.
  
La tarea programada VSGAudit busca el archivo DeleteVSGAudit.txt cada vez que se ejecuta y, cuando lo encuentra, se elimina a sí misma. Como su ejecución está configurada para cada hora, no suele pasar mucho tiempo hasta que se elimina la tarea de todos los equipos del entorno.
  
###### Directivas de auditoría para equipos que ejecuten Windows XP en el entorno EC
  
Los GPO incluidos con esta guía contienen valores para configurar las categorías de auditoría presentes en versiones anteriores de Windows. Si usa la secuencia de comandos y esos GPO, dicha configuración no se aplicará a los equipos que ejecuten Windows Vista.
  
Los GPO destinados al entorno EC están diseñados para funcionar con equipos basados en Windows XP. En estos GPO se incluye la configuración para las categorías de auditoría con el fin de que los equipos con Windows XP del entorno reciban la configuración recomendada de directiva de auditoría para equipos basados en Windows XP.
  
Puede establecer la configuración de directiva de auditoría en Windows Vista en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**  
**\\Directivas locales\\Directiva de auditoría**
  
En la tabla siguiente se resumen las recomendaciones sobre la configuración de directivas de auditoría para equipos cliente de escritorio y portátiles en los dos tipos de entornos seguros que se tratan en este capítulo.
  
**Tabla A13. Recomendaciones para la configuración de la directiva de auditoría**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Auditar eventos de inicio de sesión de cuenta</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar la administración de cuentas</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditar el acceso del servicio de directorio</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar eventos de inicio de sesión</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditar el acceso a objetos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar el cambio de directivas</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditar el uso de privilegios</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar el seguimiento de procesos</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditar eventos del sistema</td>
<td style="border:1px solid black;">Sin auditoría</td>
<td style="border:1px solid black;">Correcto</td>
<td style="border:1px solid black;">No definido</td>
</tr>
</tbody>
</table>
  
**Nota**   Como los GPO del entorno EC están diseñados para funcionar con equipos que ejecuten Windows XP, estos GPO incluyen la configuración recomendada de directiva de auditoría. En cambio, como los GPO de SSLF sólo están diseñados para funcionar con equipos que dispongan de Windows Vista, en ellos no se incluye la configuración de directiva de auditoría.
  
##### Configuración de Asignación de derechos de usuario
  
Además de los numerosos grupos con privilegios de Windows Vista, es posible asignar una serie de derechos a usuarios o grupos que normalmente no los tienen.
  
Para establecer el valor de un derecho de usuario en **Ninguno**, habilite esta configuración pero no agregue ningún usuario ni grupo. Si desea establecerlo en **No definido**, no habilite la configuración.
  
Puede establecer la configuración de asignación de derechos de usuario en Windows Vista en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario**
  
En la tabla siguiente se resumen las recomendaciones para la configuración de la asignación de derechos de usuario (de la letra A a la E) para equipos cliente de escritorio y portátiles en los dos tipos de entornos seguros que se tratan en esta guía. Cada uno de los valores se describe con más detalle en las subsecciones que aparecen a continuación.
  
Las recomendaciones sobre derechos de usuario que empiezan por las restantes letras del alfabeto se resumen en la Tabla A5 y se proporciona información adicional detallada acerca de esos derechos de usuario en las subsecciones que siguen a esa tabla.
  
**Nota**   Muchas características de IIS requieren que ciertas cuentas como IIS\_WPG, IIS IUSR\_*&lt;equipo&gt;* e* *IWAM\_*&lt;equipo&gt;* cuenten con privilegios específicos. Para obtener más información acerca de qué derechos de usuario requieren las cuentas relacionadas con IIS, consulte el artículo sobre [IIS 6.0 y las cuentas integradas](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx) (en inglés).
  
###### Derechos de usuario A – E
  
En la tabla siguiente se resumen las recomendaciones sobre la asignación de derechos de usuario desde la letra A hasta la E. Cada uno de los valores se describe con más detalle en las subsecciones que aparecen a continuación.
  
**Tabla A14. Recomendaciones para la configuración de la asignación de derechos de usuario:** **primera parte**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Tener acceso a este equipo desde la red</td>
<td style="border:1px solid black;">Todos, Administradores, Usuarios, Operadores de copia de seguridad</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Actuar como parte del sistema operativo</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ajustar las cuotas de la memoria para un proceso</td>
<td style="border:1px solid black;">Administradores, Servicio local, Servicio de red</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores, Servicio local, Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir el inicio de sesión local</td>
<td style="border:1px solid black;">Invitado, Administradores, Usuarios, Operadores de copia de seguridad</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir inicio de sesión a través de Terminal Services</td>
<td style="border:1px solid black;">Administradores, Usuarios de escritorio remoto</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Hacer copias de seguridad de archivos y directorios</td>
<td style="border:1px solid black;">Administradores, Operadores de copia de seguridad</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Omitir la comprobación de recorrido</td>
<td style="border:1px solid black;">Todos, Administradores, Usuarios,  Operadores de copia de seguridad, Servicio local, Servicio de red</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores, Usuarios, Servicio local, Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cambiar la hora del sistema</td>
<td style="border:1px solid black;">Servicio local, Administradores</td>
<td style="border:1px solid black;">Servicio local, Administradores</td>
<td style="border:1px solid black;">Servicio local, Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Cambiar la zona horaria</td>
<td style="border:1px solid black;">Servicio local, Administradores, Usuarios</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Servicio local, Administradores, Usuarios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Crear un archivo de paginación</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Crear objetos compartidos permanentes</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Crear un objeto símbolo (token)</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Crear objetos globales</td>
<td style="border:1px solid black;">Administradores, Servicio, Servicio local, Servicio de red</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores, Servicio, Servicio local, Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Crear vínculos simbólicos</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Depurar programas</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Denegar el acceso desde la red a este equipo</td>
<td style="border:1px solid black;">Invitado</td>
<td style="border:1px solid black;">Invitados</td>
<td style="border:1px solid black;">Invitados</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Denegar el inicio de sesión como trabajo por lotes</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Invitados</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Denegar el inicio de sesión localmente</td>
<td style="border:1px solid black;">Invitado</td>
<td style="border:1px solid black;">Invitados</td>
<td style="border:1px solid black;">Invitados</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Denegar inicio de sesión a través de Terminal Services</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Todos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Habilitar confianza con el equipo y las cuentas de usuario para delegación</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
**Tener acceso a este equipo desde la red**  
Esta configuración de directiva permite a otros usuarios de la red conectarse al equipo y constituye un requisito de diversos protocolos de red entre los que se incluyen los protocolos basados en bloques de mensajes de servidor (SMB), NetBIOS, el sistema común de archivos de Internet (CIFS) y el modelo de objetos componentes Plus (COM+).
  
La configuración **Tener acceso a este equipo desde la red** se establece en **Administradores** y **Usuarios** en el entorno EC y en **Administradores** en el entorno SSLF.
  
**Actuar como parte del sistema operativo**  
Esta configuración de directiva permite a un proceso asumir la identidad de cualquier usuario y obtener acceso de ese modo a los recursos autorizados al usuario.
  
Por eso, la configuración **Actuar como parte del sistema operativo** queda restringida a **Ninguno** para los dos entornos que se tratan en esta guía.
  
**Ajustar las cuotas de la memoria para un proceso**  
Esta configuración de directiva permite a un usuario ajustar la cantidad máxima de memoria disponible para un proceso. La posibilidad de ajustar cuotas de memoria resulta útil para optimizar el sistema, pero es susceptible de ser utilizada indebidamente. En malas manos, puede servir para lanzar un ataque DoS.
  
Por ese motivo, la configuración **Ajustar las cuotas de la memoria para un proceso** queda restringida a **Administradores**, al **Servicio local** y al **Servicio de red** en el entorno SSLF y se configura como **No definido** en el entorno EC.
  
**Permitir el inicio de sesión local**  
Esta configuración de directiva determina qué usuarios pueden iniciar sesión interactivamente en los equipos de su entorno. Para los inicios de sesión con la secuencia del teclado Ctrl+Alt+Supr en el equipo del cliente se requiere este derecho de usuario. Este derecho también es necesario para los usuarios que intenten iniciar la sesión mediante Terminal Services o IIS.
  
A la cuenta **Invitado** se le asigna este derecho de usuario de forma predeterminada. Aunque esta cuenta está deshabilitada de forma predeterminada, Microsoft recomienda habilitar este parámetro a través de Directiva de grupo. No obstante, por lo general se debe restringir este derecho de usuario a los grupos **Administradores** y **Usuarios**. Asigne este derecho de usuario a los **Operadores de copia de seguridad** si su organización requiere que tengan esta capacidad.
  
La configuración **Permitir el inicio de sesión local** queda restringida a los grupos **Usuarios** y **Administradores** para los dos entornos que se tratan en esta guía.
  
**Permitir inicio de sesión a través de Terminal Services**  
Esta configuración de directiva determina qué usuarios o grupos tienen derecho a iniciar sesión como cliente de los Servicios de Terminal Server. Los usuarios de escritorio remoto requieren este derecho de usuario. Si su organización utiliza Asistencia remota como parte de su estrategia de soporte técnico, cree un grupo y asígnele este derecho de usuario a través de Directiva de grupo. Si el departamento de soporte de la organización no usa Asistencia remota, asigne este derecho de usuario sólo al grupo **Administradores** o sírvase de la característica de grupos restringidos para garantizar que ninguna cuenta de usuario forme parte del grupo **Usuarios de escritorio remoto**.
  
Restrinja este derecho de usuario al grupo **Administradores** y, si es posible, al grupo **Usuarios de escritorio remoto** para evitar que usuarios no deseados obtengan acceso a equipos de la red por medio de la característica Asistencia remota.
  
El parámetro **Permitir inicio de sesión a través de Servicios de Terminal Server** está configurado como **No definido** para el entorno EC. Para mayor seguridad, esta configuración de directiva se establece en **Ninguno** en el entorno SSLF.
  
**Hacer copias de seguridad de archivos y directorios**  
Esta configuración de directiva permite a los usuarios eludir los permisos de archivo y directorio para realizar una copia de seguridad del sistema. Este derecho de usuario se habilita sólo cuando una aplicación (como NTBACKUP) intenta tener acceso a un archivo o a un directorio a través de la interfaz de programación aplicaciones (API) de copia de seguridad del sistema de archivos NTFS. De lo contrario, se aplican los permisos asignados con respecto a los archivos y directorios.
  
El valor **Hacer copias de seguridad de archivos y directorios** se configura como **No definido** en el entorno EC y para el grupo **Administradores** en el entorno SSLF.
  
**Omitir la comprobación de recorrido**  
Esta configuración de directiva permite a los usuarios que carecen del permiso de acceso especial “Recorrer carpeta” pasar por las carpetas cuando examinan alguna ruta de objetos del sistema de archivos NTFS o del Registro. Este derecho de usuario no permite a los usuarios enumerar el contenido de una carpeta; sólo atravesar los directorios.
  
El parámetro **Omitir la comprobación de recorrido** se configura como **No definido** para equipos en el entorno EC. En el entorno SSLF, se configura en las cuentas y los grupos**Administradores**,**Usuarios**,**Servicio local** y **Servicio de red**.
  
**Cambiar la hora del sistema**  
Esta configuración de directiva determina qué usuarios y grupos pueden cambiar la hora y la fecha en el reloj interno de los equipos en su entorno. Los usuarios a los que se asigna este derecho pueden influir en el aspecto de los registros de eventos. Cuando se cambia la configuración de la hora en un equipo, los eventos registrados registran la nueva hora, no la hora real en que se produjeron.
  
El valor **Cambiar la hora del sistema** se configura para el **Servicio local** y el grupo **Administradores** en los dos entornos que se tratan en esta guía.
  
**Nota**   Las discrepancias entre la hora del equipo local y la de los controladores de dominio del entorno pueden acarrear problemas para el protocolo de autenticación Kerberos, lo cual puede imposibilitar que los usuarios inicien sesión en el dominio u obtengan autorización de acceso a los recursos del dominio tras iniciar sesión. Asimismo, surgirán problemas cuando se aplique la Directiva de grupo a los equipos cliente si la hora del sistema no está sincronizada con los controladores de dominio.
  
**Cambiar la zona horaria**  
Esta configuración determina los usuarios que pueden cambiar la zona horaria del equipo. Esta capacidad no entraña ningún riesgo grave para el equipo y resulta útil para los empleados móviles.
  
El valor **Cambiar la zona horaria** se configura en **No definido** en el entorno EC y en **Administradores**, **Servicio local** y **Usuarios** en el entorno SSLF.
  
**Crear un archivo de paginación**  
Esta configuración de directiva permite a los usuarios cambiar el tamaño del archivo de paginación. Un atacante podría deteriorar el rendimiento de un equipo expuesto si modifica el tamaño de un archivo de paginación de modo que resulte extremadamente grande o pequeño.
  
El valor **Crear un archivo de paginación** se configura para **Administradores** tanto en el entorno EC como en el entorno SSLF.
  
**Crear objetos compartidos permanentes**  
Esta configuración de directiva permite a los usuarios crear objetos de directorio en el administrador de objetos. Este derecho de usuario resulta útil para componentes de modo de núcleo que amplían el espacio de nombres de objetos. De cualquier forma, en los componentes que se ejecutan en modo kernel, ese derecho es intrínseco por lo que, en general, no hace falta asignar este derecho de usuario de manera específica.
  
El valor **Crear objetos compartidos permanentes** se configura como **No definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
**Crear un objeto símbolo (token)**  
Esta configuración de directiva permite a un proceso crear un símbolo (token) de acceso, que puede proporcionar derechos elevados para el acceso a datos confidenciales. En los entornos donde la seguridad es prioritaria, este derecho no debe ser asignado a ningún usuario. Cualquier proceso que requiera esta capacidad deberá utilizar la cuenta Sistema local, a la que se asigna este derecho de usuario de forma predeterminada.
  
El valor **Crear un objeto símbolo (token)** se configura como **No definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
**Crear objetos globales**  
Esta configuración de directiva determina si los usuarios pueden crear objetos globales que están disponibles para todas las sesiones. Los usuarios pueden crear de todas formas objetos que son específicos a su propia sesión si no tienen este derecho de usuario.
  
Aquellos usuarios que pueden crear objetos globales pueden afectar los procesos que se ejecutan en otras sesiones de usuario. Esto podría crear una serie de problemas, como errores en la aplicación o daños en los datos.
  
El valor **Crear objetos globales** se configura en **No definido** en el entorno EC y en **Administradores**, **Servicio**, **Servicio local** y **Servicio de red** en el entorno SSLF.
  
**Crear vínculos simbólicos**  
Esta configuración de directiva determina los usuarios que pueden crear vínculos simbólicos. En Windows Vista, se puede obtener acceso a los objetos existentes del sistema de archivos NTFS (por ejemplo, archivos y carpetas) mediante referencias a un objeto nuevo del sistema de archivos denominado vínculo simbólico. Los vínculos simbólicos son punteros (muy parecidos a los accesos directos o los archivos .lnk) a otros objetos del sistema de archivos que pueden ser archivos, carpetas, accesos directos o cualquier otro vínculo simbólico. La diferencia entre un acceso directo y un vínculo simbólico radica en que el primero sólo funciona desde dentro del shell de Windows. Para otros programas y otras aplicaciones, los accesos directos son sólo un archivo más, mientras que, en el caso de los vínculos simbólicos, el concepto del acceso directo se implementa como una característica del sistema de archivos NTFS.
  
Los vínculos simbólicos podrían exponer las vulnerabilidades de seguridad en las aplicaciones que no estén diseñadas para su uso. Por ello, el privilegio para crear vínculos simbólicos sólo se debe asignar a usuarios de confianza. De manera predeterminada, los administradores son los únicos con esta capacidad.
  
El valor **Crear vínculos simbólicos** se configura como **No definido** para los equipos del entorno EC y para el grupo **Administradores** en el entorno SSLF a fin de aplicar la configuración predeterminada.
  
**Depurar programas**  
Esta configuración de directiva determina qué cuentas de usuario tienen derecho a adjuntar un depurador a cualquier proceso o al kernel, lo que proporciona un acceso completo a componentes reservados y críticos del sistema operativo. Los desarrolladores que depuren sus propias aplicaciones no necesitan que se les asigne este derecho de usuario; en cambio, los que depuren nuevos componentes del sistema sí lo necesitan.
  
**Nota**   Microsoft publicó en octubre de 2003 varias actualizaciones de seguridad en las que se usaba una versión de Update.exe que requería que el administrador dispusiera del derecho de usuario **Depurar programas**. Los administradores que no tenían este derecho de usuario no pudieron instalar estas actualizaciones de seguridad hasta que reconfiguraron sus derechos de usuario. Ese comportamiento no es propio de las actualizaciones del sistema operativo. Para obtener más información, consulte el artículo 830846 de Knowledge Base “[Actualizaciones de productos de Windows podría dejar de responder o utilizar casi todos los recursos de CPU](http://support.microsoft.com/default.aspx?kbid=830846)”.
  
Dado que un atacante podría aprovechar este derecho de usuario, sólo se asigna al grupo Administradores de forma predeterminada. El valor de directiva **Depurar programas** se configura en **Administradores** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
**Denegar el acceso desde la red a este equipo**  
Esta configuración de directiva prohíbe a los usuarios conectarse a un equipo a través de la red, una posibilidad que les permitiría obtener acceso a datos de forma remota y, en algunos casos, de modificarlos. En los entornos SSLF, no debe existir la necesidad de que los usuarios remotos tengan acceso a los datos de un equipo. En vez de eso, el uso compartido de archivos debería tener lugar a través de los servidores de la red.
  
El valor **Denegar el acceso desde la red a este equipo** se configura en el grupo **Invitados** para los equipos de los dos entornos que se tratan en esta guía.
  
**Denegar el inicio de sesión como trabajo por lotes**  
Esta configuración de directiva prohíbe el inicio de sesión a los usuarios a través de un servicio de cola por lotes, una característica de Windows Server 2003 que se utiliza para programar trabajos de modo que se ejecuten automáticamente una o varias veces con posterioridad.
  
El valor **Denegar el inicio de sesión como trabajo por lotes** se configura como **No definido** en el entorno EC y en el grupo **Invitados** en el entorno SSLF.
  
**Denegar el inicio de sesión localmente**  
Esta configuración de directiva prohíbe a los usuarios un inicio de sesión local en la consola del equipo. Si un usuario no autorizado pudiera iniciar sesión localmente en un equipo, tendría la ocasión de descargar código malintencionado o de elevar sus privilegios en el equipo. No digamos si un atacante obtuviera acceso físico a la consola; entonces, habría otros riesgos que tener en cuenta. Este derecho de usuario no debe asignarse a los usuarios que necesitan acceso físico a la consola del equipo.
  
El valor **Denegar el inicio de sesión localmente** se configura en el grupo **Invitados** para los dos entornos que se tratan en esta guía. Asimismo, a cualquier cuenta de servicio para el entorno SSLF que se agregue al equipo se le debe asignar este derecho de usuario para evitar su uso indebido.
  
**Denegar inicio de sesión a través de Terminal Services**  
Esta configuración de directiva prohíbe a los usuarios iniciar sesión en equipos de su entorno a través de conexiones de Escritorio remoto. Si asigna este derecho de usuario al grupo **Todos**, también impedirá a los miembros del grupo **Administradores** predeterminado que utilice Servicios de Terminal Server para iniciar sesión en equipos de su entorno.
  
El parámetro **Denegar inicio de sesión a través de Servicios de Terminal Server** se configura como **No definido** en el entorno EC y para el grupo **Todos** en el entorno SSLF.
  
**Habilitar confianza con el equipo y las cuentas de usuario para delegación**  
Esta configuración de directiva permite a los usuarios cambiar el parámetro **De confianza para delegación** en un objeto de equipo en Active Directory. El uso indebido de este privilegio podría permitir a usuarios no autorizados suplantar a otros usuarios en la red.
  
Por ese motivo, el valor **Habilitar confianza con el equipo y las cuentas de usuario para delegación** se configura como **No definido** en el entorno EC y como **Ninguno** en el entorno SSLF.
  
###### Derechos de usuario F–T
  
En la tabla siguiente se resumen las recomendaciones sobre la asignación de derechos de usuario desde la letra F hasta la T. Cada uno de los valores se describe con más detalle en las subsecciones que aparecen a continuación.
  
**Tabla A15. Recomendaciones para la configuración de la asignación de derechos de usuario:** **segunda parte**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Forzar cierre desde un sistema remoto</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Generar auditorías de seguridad</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Suplantar a un cliente tras la autenticación</td>
<td style="border:1px solid black;">Administradores, Servicio, Servicio local, Servicio de red</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores, Servicio, Servicio local, Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Aumentar el espacio de trabajo de un proceso</td>
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Aumentar prioridad de programación</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cargar y descargar controladores de dispositivos</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Bloquear páginas en la memoria</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Iniciar sesión como proceso por lotes</td>
<td style="border:1px solid black;">Administradores, Operadores de copia de seguridad</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Iniciar sesión como servicio</td>
<td style="border:1px solid black;">Ninguno</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administrar registro de auditoría y de seguridad</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Modificar valores de entorno firmware</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Realizar tareas de mantenimiento del volumen</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Analizar un solo proceso</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Analizar el rendimiento del sistema</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Quitar equipo de la estación de acoplamiento</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reemplazar un símbolo (token) de nivel de proceso</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
<td style="border:1px solid black;">Servicio local, Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Restaurar archivos y directorios</td>
<td style="border:1px solid black;">Administradores, Operadores de copia de seguridad</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Apagar el sistema</td>
<td style="border:1px solid black;">Administradores, Operadores de copia de seguridad, Usuarios</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
<td style="border:1px solid black;">Administradores, Usuarios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tomar posesión de archivos y otros objetos</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
**Forzar cierre desde un sistema remoto**  
Esta configuración de directiva permite a los usuarios apagar equipos Windows Vista desde ubicaciones remotas de la red. Cualquier usuario al que se le haya asignado este derecho puede provocar una situación DoS, con lo que el equipo dejaría de estar disponible para las solicitudes del usuario del servicio. Por lo tanto, Microsoft recomienda que sólo se asigne este derecho de usuario a los administradores de máxima confianza.
  
El valor **Forzar cierre desde un sistema remoto** se configura para el grupo **Administradores** en los dos entornos que se describen en esta guía.
  
**Generar auditorías de seguridad**  
Esta configuración de directiva determina qué usuarios o procesos pueden generar registros de auditoría en el registro de seguridad. Un atacante podría utilizar esta capacidad para crear un gran número de eventos auditados, lo que dificultaría a un administrador de sistema la localización de una actividad ilícita. Asimismo, si el registro de eventos se configura para sobrescribir eventos según sea necesario, cualquier evidencia de actividades no autorizadas podría ser sobrescrita por una gran cantidad de eventos no relacionados.
  
Por ese motivo, el valor **Generar auditorías de seguridad** se configura para los grupos **Servicio local** y **Servicio de red** en los dos entornos que se describen en esta guía.
  
**Suplantar a un cliente tras la autenticación**  
Esta configuración de directiva permite a los programas que se ejecutan en nombre de un usuario (u otra cuenta especificada) suplantar al usuario en cuestión. Si este derecho de usuario se requiere para este tipo de suplantación, un usuario no autorizado no podrá convencer a un cliente de que se conecte, por ejemplo, por llamada a procedimiento remoto (RPC) o canalizaciones con nombre, a un servicio creado para suplantar a ese cliente, que podría elevar los permisos del usuario no autorizado a niveles administrativos o de sistema.
  
Los servicios que se inician mediante el Administrador de control de servicios tienen agregado de forma predeterminada el grupo Servicio integrado en sus símbolos (token) de acceso. Los servidores COM que se inician mediante la infraestructura COM y se configuran para que se ejecuten bajo cuentas específicas tienen agregado el grupo Servicio a sus símbolos (token) de acceso. Como consecuencia, al iniciarse estos servicios se les asigna este derecho de usuario.
  
Además, un usuario puede suplantar un símbolo (token) de acceso si se da alguna de las siguientes condiciones:
  
-   El símbolo (token) de acceso que se suplanta está destinado al usuario.
  
-   El usuario, en esta sesión de inicio, inició sesión en la red con credenciales explícitas para crear el símbolo (token) de acceso.
  
-   El nivel solicitado es menor que Suplantar, por ejemplo, Anónimo o Identificar.
  
Un atacante con el derecho de usuario **Suplantar a un cliente tras la autenticación** podría crear un servicio, engañar a un cliente para que se conecte al servicio y, a continuación, suplantar a ese cliente para elevar el nivel de acceso del atacante al mismo del cliente.
  
Por ello, el valor **Suplantar a un cliente tras la autenticación** se configura como **No definido** en el entorno EC y como **Administradores,** **Servicio,** **Servicio localy Servicio de red** en el entorno SSLF.
  
**Aumentar el espacio de trabajo de un proceso**  
Este privilegio determina qué cuentas de usuario pueden aumentar o reducir el tamaño del espacio de trabajo de un proceso. El espacio de trabajo de un proceso es el conjunto de páginas de memoria que son visibles en el momento para el proceso en la memoria RAM física. Se trata de páginas residentes que se encuentran a disposición de la aplicación sin que se desencadene ningún error de página. Los tamaños mínimo y máximo del espacio de trabajo afectan al comportamiento de paginación de la memoria virtual de los procesos.
  
Este derecho se otorga a todos los usuarios de manera predeterminada. Ahora bien, al aumentar el tamaño del espacio de trabajo de un proceso, disminuye la cantidad de memoria física disponible para el resto del sistema. Se podría usar un código malintencionado que aumentara el espacio de trabajo de un proceso hasta tal punto que el rendimiento del sistema se viera gravemente afectado y acabara con una denegación de servicio. Algunos entornos mitigan este riesgo limitando los usuarios con capacidad para aumentar el espacio de trabajo de los procesos.
  
Por ello, el derecho de usuario Aumentar el espacio de trabajo de un proceso se configura como **No definido** en el entorno EC y como **Administradores** en el entorno SSLF.
  
**Aumentar prioridad de programación**  
Esta configuración de directiva permite a los usuarios cambiar la cantidad de tiempo de procesador que utiliza un proceso. Un atacante podría utilizar esta capacidad para aumentar la prioridad de un proceso a tiempo real y crear una situación de denegación de servicio para un equipo.
  
Por ese motivo, el valor **Aumentar prioridad de programación** se configura para el grupo **Administradores** en los dos entornos que se describen en esta guía.
  
**Cargar y descargar controladores de dispositivo**  
Esta configuración de directiva permite a los usuarios cargar dinámicamente un nuevo controlador de dispositivo en un sistema. Un atacante podría utilizar esta capacidad para instalar código malintencionado con la apariencia de un controlador de dispositivo. Este derecho de usuario es necesario para que los usuarios puedan agregar controladores de impresora o impresoras locales en Windows Vista.
  
Dado que los atacantes podrían aprovechar este derecho de usuario, el valor **Cargar y descargar controladores de dispositivo** se configura para el grupo **Administradores** en los dos entornos que se describen en esta guía.
  
**Bloquear páginas en la memoria**  
Esta configuración de directiva permite que un proceso mantenga datos en la memoria física. Esto evita que el sistema pagine los datos en la memoria virtual del disco. Si asigna este derecho al usuario, podría afectar de manera significativa al rendimiento del sistema.
  
Por ese motivo, el valor **Bloquear páginas en la memoria** se configura como **Ninguno** en los dos entornos que se describen en esta guía.
  
**Iniciar sesión como proceso por lotes**  
Esta configuración de directiva permite que las cuentas inicien sesión mediante el servicio del programador de tareas. Dado que el programador de tareas se utiliza a menudo con fines administrativos, puede que se necesite en el entorno EC. Sin embargo, su uso debe ser restringido en el entorno SSLF para evitar la utilización indebida de recursos de sistema o para evitar que algún atacante utilice el derecho con el objetivo de iniciar código malintencionado tras obtener acceso de nivel de usuario a un equipo.
  
Por lo tanto, el derecho de usuario **Iniciar sesión como proceso por lotes** se configura como **No definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
**Iniciar sesión como servicio**  
Esta configuración de directiva permite a las cuentas iniciar servicios de red o registrar un proceso como un servicio que se ejecuta en el sistema. Este derecho de usuario debe estar restringido en todos los equipos de los entornos SSLF pero, dado que muchas aplicaciones pueden requerir este privilegio, se debe evaluar y probar con detenimiento antes de configurarlo en un entorno EC. En los equipos basados en Windows Vista, ningún usuario ni grupo cuenta con este privilegio de manera predeterminada.
  
El valor **Iniciar sesión como servicio** se configura como **No definido** para el entorno EC y como **Ninguno** para el entorno SSLF.
  
**Administrar registro de auditoría y de seguridad**  
Esta configuración de directiva determina qué usuarios pueden cambiar las opciones de auditoría de archivos y directorios así como borrar el registro de seguridad.
  
Dado que esta capacidad representa una amenaza relativamente moderada, la configuración **Administrar registro de seguridad y auditoría** aplica el valor predeterminado del grupo **Administradores** a los dos entornos que se describen en esta guía.
  
**Modificar valores de entorno firmware**  
Esta configuración de directiva permite a los usuarios configurar las variables de entorno del sistema que afectan a la configuración de hardware. Esta información suele almacenarse en la última configuración válida conocida. La modificación de estos valores podría llevar a un error de hardware que provocaría una denegación de servicio.
  
Dado que esta capacidad representa una amenaza relativamente moderada, la configuración **Modificar valores de entorno firmware** aplica el valor predeterminado del grupo **Administradores** a los dos entornos que se describen en esta guía.
  
**Realizar tareas de mantenimiento del volumen**  
Esta configuración de directiva permite a los usuarios administrar la configuración de volúmenes o discos del sistema, lo que podría permitir a un usuario eliminar un volumen y provocar una pérdida de datos, así como una denegación de servicio.
  
La configuración **Realizar tareas de mantenimiento del volumen** aplica el valor predeterminado del grupo **Administradores** en los dos entornos que se describen en esta guía.
  
**Analizar un solo proceso**  
Esta configuración de directiva determina qué usuarios pueden utilizar herramientas para supervisar el rendimiento de procesos que no son del sistema. Por lo general no es necesario configurar este derecho de usuario para utilizar el complemento Rendimiento de Microsoft Management Console (MMC). Sin embargo, sí necesita este derecho de usuario si el Monitor de sistema se configura para reunir datos con el instrumental de administración de Windows (WMI). Con la restricción del derecho de usuario **Analizar un solo proceso**, se evita que los intrusos obtengan información adicional que pueda utilizarse para llevar a cabo un ataque al sistema.
  
El valor **Analizar un solo proceso** se configura como **No definido** para los equipos del entorno EC y para el grupo **Administradores** en el entorno SSLF.
  
**Analizar el rendimiento del sistema**  
Esta configuración de directiva permite a los usuarios utilizar herramientas para ver el rendimiento de distintos procesos del sistema, posibilidad que se podría utilizar indebidamente para que un atacante determinara los procesos activos de un sistema y conociera mejor la superficie vulnerable a ataques en el equipo.
  
La configuración **Analizar el rendimiento del sistema** aplica el valor predeterminado del grupo **Administradores** en los dos entornos que se describen en esta guía.
  
**Quitar equipo de la estación de acoplamiento**  
Esta configuración de directiva permite al usuario de un equipo portátil hacer clic en **Retirar equipo** en el menú **Inicio** para quitar el equipo de la estación de acoplamiento.
  
El valor **Quitar equipo de la estación de acoplamiento** se configura para los grupos **Administradores** y **Usuarios** en los dos entornos que se describen en esta guía.
  
**Reemplazar un símbolo (token) de nivel de proceso**  
Esta configuración de directiva permite a un proceso o servicio iniciar otro servicio o proceso con un símbolo (token) de acceso de seguridad distinto, lo que se puede utilizar para modificar el símbolo (token) de acceso de seguridad de ese subproceso y dar lugar a un incremento de privilegios.
  
El valor **Reemplazar un símbolo (token) de nivel de proceso** se configura con los valores predeterminados de **Servicio local** y **Servicio de red** en los dos entornos que se describen en esta guía.
  
**Restaurar archivos y directorios**  
Esta configuración de directiva determina qué usuarios pueden evitar los permisos de archivo, directorio, registro y otros objetos persistentes al restaurar copias de seguridad de archivos y directorios en los equipos con Windows Vista del entorno. Este derecho de usuario determina también qué usuarios pueden establecer entidades principales de seguridad válidas como propietarios de objetos; es similar al derecho de usuario **Hacer copias de seguridad de archivos y directorios** .
  
El parámetro **Restaurar archivos y directorios** se configura como **No definido** en equipos del entorno EC y para el grupo **Administradores** en el entorno SSLF.
  
**Apagar el sistema**  
Esta configuración de directiva determina qué usuarios que han iniciado sesión localmente en los equipos del entorno pueden cerrar el sistema operativo con el comando Apagar. El uso incorrecto de este derecho puede dar lugar a un situación de denegación de servicio. En entornos SSLF, Microsoft recomienda que este derecho se asigne sólo a los grupos **Administradores** y **Usuarios**.
  
El valor **Apagar el sistema** se configura para los grupos **Administradores** y **Usuarios** en los dos entornos que se describen en esta guía.
  
**Tomar posesión de archivos y otros objetos**  
Esta configuración de directiva permite a los usuarios tomar posesión de archivos, carpetas, claves del Registro, procesos o subprocesos. Este derecho de usuario pasa por alto cualquier permiso diseñado para proteger objetos y proporcionar la posesión al usuario especificado.
  
La configuración **Tomar posesión de archivos y otros objetos** se establece en el valor predeterminado del grupo **Administradores** en los dos entornos que se describen en esta guía.
  
##### Configuración de Opciones de seguridad
  
La configuración de las opciones de seguridad que se aplican mediante la directiva de grupo en equipos del entorno en los que se ejecuta Windows Vista permite habilitar o deshabilitar capacidades y características tales como el acceso al disquete, el acceso a unidades de CD-ROM y los mensajes de inicio de sesión. Esta configuración se utiliza también para configurar otros parámetros, como los de firma digital de datos, nombres de cuenta de administrador e invitado y el funcionamiento de la instalación de controladores.
  
Puede configurar las opciones de seguridad en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad**
  
No todas las configuraciones que se incluyen en esta sección existen en todos los tipos de sistemas. Por lo tanto, puede que los parámetros que incluyen la parte de Opciones de seguridad de Directiva de grupo que se definen en esta sección se deban modificar manualmente en los sistemas en los que se presentan para funcionar sin impedimentos. Asimismo, las plantillas de Directiva de grupo se pueden editar por separado para incluir las opciones de configuración adecuadas, de modo que las opciones de configuración recomendadas puedan aplicarse en su totalidad.
  
En las siguientes secciones se proporcionan recomendaciones para la configuración de opciones de seguridad, que se agrupan por tipo de objeto. Cada sección incluye una tabla en la que se resumen los parámetros de configuración, y en las subsecciones que siguen a cada tabla se proporciona información detallada. Se ofrecen recomendaciones para equipos cliente tanto de escritorio como portátiles en los dos tipos de entornos seguros que se describen en esta guía: el entorno de Cliente de empresa (EC) y el entorno de Seguridad especializada: funcionalidad limitada (SSLF).
  
Esta sección del apéndice incluye tablas y recomendaciones para las configuraciones de tipos de objetos siguientes, las cuales residen en el subdirectorio **Opciones deseguridad**:
  
-   [Cuentas](#_accounts)
  
-   [Auditoría](#_audit)
  
-   [Dispositivos](#_devices)
  
-   [Miembro de dominio](#_domain_member)
  
-   [Inicio de sesión interactivo](#_interactive_logon)
  
-   [Cliente de redes de Microsoft](#_microsoft_network_client)
  
-   [Configuración de MSS](#_mss_settings_1)
  
-   [Servidor de red Microsoft](#_microsoft_network_server)
  
-   [Acceso a la red](#_network_access)
  
-   [Seguridad de red](#_network_security)
  
-   [Consola de recuperación](#_recovery_console)
  
-   [Apagar](#_shutdown)
  
-   [Criptografía de sistema](#_system_cryptography)
  
-   [Objetos de sistema](#_system_objects)
  
-   [Control de cuentas de usuario](#_user_account_control)
  
###### Cuentas
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para las cuentas. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A16. Recomendaciones para la configuración de opciones de seguridad: Cuentas**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Cuentas: estado de la cuenta de administrador</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cuentas: estado de la cuenta de invitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar sesión en la consola</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cuentas: cambiar el nombre de la cuenta de administrador</td>
<td style="border:1px solid black;">Administrador</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cuentas: cambiar el nombre de la cuenta de invitado</td>
<td style="border:1px solid black;">Invitado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
**Cuentas: estado de la cuenta de administrador**  
Esta configuración de directiva habilita o deshabilita la cuenta del administrador durante el funcionamiento normal. Cuando un equipo se inicia en el modo a prueba de fallos, la cuenta del administrador siempre está habilitada, independientemente de la configuración de este parámetro.
  
El valor **Cuentas: estado de la cuenta de administrador** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Cuentas: estado de la cuenta de invitado**  
Esta configuración de directiva determina si la cuenta de invitado se habilita o se deshabilita. La cuenta de invitado permite a usuarios de red no autenticados obtener acceso al sistema.
  
El valor **Cuentas: estado de la cuenta de invitado** es una opción de seguridad que se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar sesión en la consola**  
Esta configuración de directiva determina si las cuentas locales que no están protegidas con contraseña se pueden utilizar para iniciar sesión desde ubicaciones distintas a la consola física del equipo. Si habilita esta configuración de directiva, las cuentas locales que tienen contraseñas en blanco no pueden iniciar sesión en la red desde equipos cliente remotos. Dichas cuentas sólo podrán iniciar sesión a través del teclado del equipo.
  
El valor **Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar sesión en la consola** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Cuentas: cambiar el nombre de la cuenta de administrador**  
El nombre de la cuenta de administrador local integrada es bien conocido y constituye uno de los principales objetivos de los atacantes. Microsoft recomienda que elija otro nombre para esta cuenta y que evite los nombres que denotan cuentas administrativas o de acceso elevado. Asegúrese también de cambiar la descripción predeterminada del administrador local (a través de la consola de administración de equipos).
  
La recomendación de usar la configuración **Cuentas: cambiar el nombre de la cuenta de administrador** se aplica a los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva no se establece en las plantillas de seguridad ni tampoco se sugiere ningún nombre de usuario para la cuenta en esta guía. Se omite la recomendación de ningún nombre de usuario para garantizar que las organizaciones que implementen esta instrucción no usen el mismo nombre de usuario nuevo en sus entornos.
  
**Cuentas: cambiar el nombre de cuenta de invitado**  
La cuenta integrada de invitado local es otro de los nombres bien conocidos por los atacantes. Microsoft también recomienda que cambie el nombre de esta cuenta para no revelar su propósito. Incluso si deshabilita esta cuenta de invitado (lo cual se recomienda), asegúrese de cambiar el nombre como medida de seguridad adicional.
  
La recomendación de usar la configuración **Cuentas: cambiar el nombre de cuenta de invitado** se aplica a los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva no se establece en las plantillas de seguridad ni tampoco se sugiere ningún nombre de usuario nuevo para la cuenta en este documento. Se omite la recomendación de ningún nombre de usuario para garantizar que las organizaciones que implementen esta instrucción no usen el mismo nombre de usuario nuevo en sus entornos.
  
###### Auditoría
  
La tabla siguiente resume la configuración de auditoría recomendada. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A17. Recomendaciones para la configuración de opciones de seguridad: Auditoría**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Auditoría: auditar el acceso de objetos globales del sistema</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditoría: auditar el uso del privilegio de copias de seguridad y restauración</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Auditoría: forzar la configuración de subcategorías de la directiva de auditoría (Windows Vista o posterior) para invalidar la configuración de la categoría de directiva de auditoría</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditoría: apagar el sistema de inmediato si no se pueden registrar las auditorías de seguridad</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
**Auditoría: auditar el acceso de objetos globales del sistema**  
Esta configuración de directiva crea una lista de control de acceso del sistema (SACL) predeterminada para objetos del sistema tales como exclusiones mutuas, eventos, semáforos y dispositivos MS-DOS® y, además, provoca que se audite el acceso a estos objetos del sistema.
  
Si la configuración **Auditoría: auditar el acceso de objetos globales del sistema** está habilitada, un gran número de eventos de seguridad podría llenar con rapidez el registro de eventos de seguridad. Por lo tanto, esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Auditoría: auditar el uso del privilegio de copias de seguridad y restauración**  
Esta configuración de directiva determina si se debe auditar el uso de todos los privilegios de usuario, incluido el de copia de seguridad y restauración, cuando se habilita el parámetro **Auditar el uso de privilegios**. Si habilita ambas directivas, se generará un evento de auditoría para cada archivo del que se realiza una copia de seguridad o que se restaura.
  
Si la configuración **Auditoría: auditar el uso del privilegio de copias de seguridad y restauración** está habilitada, un gran número de eventos de seguridad podría llenar con rapidez el registro de eventos de seguridad. Por lo tanto, esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Auditoría: forzar la configuración de subcategorías de la directiva de auditoría (Windows Vista o posterior) para invalidar la configuración de la categoría de directiva de auditoría**  
Esta configuración de directiva permite a los administradores habilitar las capacidades de auditoría más precisas con las que cuenta Windows Vista.
  
La configuración de directiva de auditoría disponible en Windows Server 2003 Active Directory aún no contiene valores para administrar las nuevas subcategorías de auditoría. A fin de aplicar correctamente las directivas de auditoría recomendadas en esta guía, la configuración **Auditoría: forzar la configuración de subcategorías de la directiva de auditoría (Windows Vista o posterior) para invalidar la configuración de la categoría de directiva de auditoría** se debe establecer en **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Auditoría: apagar el sistema de inmediato si no se pueden registrar las auditorías de seguridad**  
Esta configuración de directiva determina si el sistema se debe cerrar en caso de que no pueda registrar eventos de seguridad. Constituye un requisito para que las certificaciones Trusted Computer System Evaluation Criteria (TCSEC)-C2 y Common Criteria impidan que se produzcan eventos susceptibles de ser auditados si el sistema de auditoría no puede registrarlos. Microsoft ha decidido cumplir este requisito de forma que el sistema se detenga y muestre un mensaje de detención cuando se produce un error del sistema de auditoría. Cuando esta configuración de directiva esté habilitada, el sistema se cerrará si no se puede registrar una auditoría de seguridad por algún motivo.
  
Si está habilitada la configuración **Auditoría: apagar el sistema de inmediato si no se pueden registrar las auditorías de seguridad**, existe la posibilidad de que se produzcan errores inesperados en el sistema. Por lo tanto, esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
###### Dispositivos
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los dispositivos. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A18. Recomendaciones para la configuración de opciones de seguridad: Dispositivos**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Dispositivos: permitir desacoplamiento sin tener que iniciar sesión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Dispositivos: permitir formatear y expulsar medios extraíbles</td>
<td style="border:1px solid black;">No definido (no existe ningún valor de Registro predeterminado)</td>
<td style="border:1px solid black;">Administradores, Usuarios interactivos</td>
<td style="border:1px solid black;">Administradores</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Dispositivos: impedir que los usuarios instalen controladores de impresora<br />
(equipos de escritorio)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Dispositivos: impedir que los usuarios instalen controladores de impresora<br />
(equipos portátiles)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente</td>
<td style="border:1px solid black;">No definido (no existe ningún valor de Registro predeterminado)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Dispositivos: restringir el acceso a disquetes sólo al usuario con sesión iniciada localmente</td>
<td style="border:1px solid black;">No definido (no existe ningún valor de Registro predeterminado)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Dispositivos: permitir desacoplamiento sin tener que iniciar sesión**  
Esta configuración de directiva determina si un equipo portátil puede retirarse de la estación de acoplamiento en caso de que el usuario no haya iniciado sesión en el sistema. Habilite esta configuración de directiva para eliminar el requisito de inicio de sesión y permitir el uso de un botón de hardware externo para retirar el equipo. Si deshabilita esta configuración de directiva, los usuarios que no hayan iniciado sesión deben tener asignado el derecho de usuario **Quitar equipo de la estación de acoplamiento** para desacoplar el equipo.
  
El valor **Dispositivos:** **permitir desacoplamiento sin tener que iniciar sesión** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Dispositivos: permitir formatear y expulsar medios extraíbles**  
Esta configuración de directiva determina a quién se permite formatear y expulsar medios extraíbles. Puede utilizar esta configuración de directiva para evitar que usuarios no autorizados extraigan datos de un equipo para tener acceso a esa información en otro equipo para el que tienen privilegios de administrador local.
  
El valor **Dispositivos:** **permitir formatear y expulsar medios extraíbles** está restringido a los grupos **Administradores** y **Usuarios interactivos** en el entorno EC y en exclusiva al grupo **Administradores** en el entorno SSLF para mayor seguridad.
  
**Dispositivos: impedir que los usuarios instalen controladores de impresora**  
Los atacantes pueden disfrazar un programa de caballo de Troya como un controlador de impresora. Este programa hace creer a los usuarios que deben utilizarlo para imprimir, pero en realidad puede introducir código malintencionado en la red del equipo. Para reducir las posibilidades de que ocurra algo así, la instalación de controladores de impresora sólo se debe permitir a los administradores. Sin embargo, dado que los equipos portátiles son dispositivos móviles, es probable que, de vez en cuando, sea necesario que los usuarios de estos equipos instalen un controlador de impresora desde un origen remoto a fin de continuar su trabajo. Por tanto, esta configuración de directiva se debe deshabilitar para ese tipo de usuarios, aunque debe estar siempre habilitada para los usuarios de equipos de escritorio.
  
El valor **Dispositivos:** **impedir que los usuarios instalen controladores de impresora** se configura como **Habilitado** para los equipos de escritorio en los dos entornos que se describen en esta guía y como **Deshabilitado** para los usuarios de equipos portátiles en ambos entornos.
  
**Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente**  
Esta configuración de directiva determina si pueden tener acceso simultáneamente a la unidad de CD-ROM los usuarios locales y remotos. Si habilita esta configuración de directiva, sólo los usuarios que han iniciado sesión interactivamente podrán obtener acceso a medios de la unidad de CD-ROM. Cuando está habilitada esta configuración de directiva y nadie ha iniciado sesión, el contenido de la unidad de CD-ROM estará disponible a través de la red. Al habilitar esta configuración, la utilidad de copias de seguridad de Windows genera un error si se especifican instantáneas de volumen para el trabajo de copia de seguridad. Lo mismo sucede con los productos de copia de seguridad de otros fabricantes que usan instantáneas de volumen.
  
El valor **Dispositivos:** **restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Dispositivos: restringir el acceso a disquetes sólo al usuario con sesión iniciada localmente**  
Esta configuración de directiva determina si pueden tener acceso simultáneamente a la unidad de disquete los usuarios locales y remotos. Si habilita esta configuración de directiva, sólo los usuarios que han iniciado sesión interactivamente podrán obtener acceso a medios de la unidad de disquete. Si esta configuración de directiva está habilitada y nadie ha iniciado sesión, el contenido de la unidad de disquete estará disponible a través de la red. Al habilitar esta configuración, la utilidad de copias de seguridad de Windows genera un error si se especifican instantáneas de volumen para el trabajo de copia de seguridad. Lo mismo sucede con los productos de copia de seguridad de otros fabricantes que usan instantáneas de volumen.
  
El valor **Dispositivos:** **restringir el acceso a disquetes sólo al usuario con sesión iniciada localmente** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
###### Miembro del dominio
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los miembros de dominio. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A19. Recomendaciones para la configuración de opciones de seguridad: Miembro de dominio**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Miembro de dominio: cifrar o firmar digitalmente datos de un canal seguro (siempre)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Miembro de dominio: cifrar digitalmente datos de un canal seguro (cuando sea posible)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Miembro de dominio: duración máxima de contraseña de cuenta de equipo</td>
<td style="border:1px solid black;">30 días</td>
<td style="border:1px solid black;">30 días</td>
<td style="border:1px solid black;">30 días</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Miembro de dominio: requerir clave de sesión segura (Windows 2000 o posterior)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Miembro de dominio: cifrar o firmar digitalmente datos de un canal seguro (siempre)**  
Esta configuración de directiva determina si todo el tráfico de canal seguro iniciado por el miembro de dominio se debe firmar o cifrar. Si un sistema está configurado para cifrar o firmar siempre los datos de canales seguros, no puede establecer ningún canal seguro con un controlador de dominio que no tenga capacidad para firmar o cifrar todo el tráfico del canal seguro porque todos los datos de ese canal están firmados y cifrados.
  
El valor **Miembro de dominio: cifrar o firmar digitalmente datos de un canal seguro (siempre)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Miembro de dominio: cifrar digitalmente datos de un canal seguro (cuando sea posible)**  
Esta configuración de directiva determina si un miembro de dominio debe intentar negociar el cifrado para todo el tráfico de canal seguro que inicie. Si habilita esta configuración de directiva, el miembro de dominio solicitará cifrado de todo el tráfico de canal seguro. Si deshabilita esta configuración de directiva, se impedirá que el miembro de dominio negocie cifrado de canal seguro.
  
El valor **Miembro de dominio: cifrar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)**  
Esta configuración de directiva determina si un miembro de dominio debe intentar negociar que todo el tráfico de canal seguro que inicie tenga una firma digital. Las firmas digitales protegen el tráfico frente a la posibilidad de que sea modificado por alguien que capture los datos cuando atraviesan la red.
  
El valor **Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo**  
Esta configuración de directiva determina si un miembro de dominio puede cambiar con cierta periodicidad su contraseña de cuenta de equipo. Si habilita esta configuración de directiva, se impedirá al miembro de dominio cambiar su contraseña de cuenta en el equipo. Si deshabilita esta configuración de directiva, el miembro de dominio puede cambiar su contraseña de cuenta de equipo según lo especifique la configuración **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** que, de manera predeterminada, asciende a 30 días. Los equipos que no pueden cambiar de forma automática las contraseñas de sus cuentas son, en potencia, vulnerables ya que un atacante puede determinar la contraseña de la cuenta de dominio del sistema.
  
Por lo tanto, el valor **Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Miembro de dominio: duración máxima de contraseña de cuenta de equipo**  
Esta configuración de directiva determina la duración máxima admisible para una contraseña de cuenta de equipo. De forma predeterminada, los miembros de dominio cambian automáticamente sus contraseñas cada 30 días. Si aumenta este intervalo de forma significativa o se establece en 0 para que no se cambien las contraseñas de los equipos, se da más tiempo al atacante para emprender un ataque de fuerza bruta contra una de las cuentas de equipo.
  
Por lo tanto, el valor **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** se configura en **30 días** en los dos entornos que se describen en esta guía.
  
**Miembro de dominio: requerir clave de sesión segura (Windows 2000 o posterior)**  
Cuando esta configuración de directiva está habilitada, sólo se puede establecer un canal seguro con controladores de dominio capaces de cifrar datos de canal seguro con una clave de sesión segura (de 128 bits).
  
Para habilitar esta configuración de directiva, todos los controladores del dominio deben ser capaces de cifrar datos de canal seguro con una clave protegida, lo que significa que en todos los controladores de dominio debe estar ejecutándose Microsoft Windows 2000 o posterior. Si se requiere comunicación con dominios que no estén basados en Windows 2000, Microsoft recomienda deshabilitar esta configuración de directiva.
  
El valor **Miembro de dominio: requerir clave de sesión segura** **(Windows 2000 o posterior)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
###### Inicio de sesión interactivo
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el inicio de sesión interactivo. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A20. Recomendaciones para la configuración de opciones de seguridad: Inicio de sesión interactivo**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Inicio de sesión interactivo: no mostrar el último nombre de usuario</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión</td>
<td style="border:1px solid black;">En blanco</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión</td>
<td style="border:1px solid black;">En blanco</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inicio de sesión interactivo: número de inicios de sesión anteriores que se almacenarán en caché (si el controlador de dominio no está disponible)<br />
(equipos de escritorio)</td>
<td style="border:1px solid black;">10</td>
<td style="border:1px solid black;">2</td>
<td style="border:1px solid black;">0</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión interactivo: número de inicios de sesión anteriores que se almacenarán en caché (si el controlador de dominio no está disponible)<br />
(equipos portátiles)</td>
<td style="border:1px solid black;">10</td>
<td style="border:1px solid black;">2</td>
<td style="border:1px solid black;">2</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inicio de sesión interactivo: pedir al usuario que cambie la contraseña antes de que expire</td>
<td style="border:1px solid black;">14 días</td>
<td style="border:1px solid black;">14 días</td>
<td style="border:1px solid black;">14 días</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear la estación de trabajo (equipos de escritorio)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear la estación de trabajo (equipos portátiles)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente</td>
<td style="border:1px solid black;">Ninguna acción</td>
<td style="border:1px solid black;">Bloquear estación de trabajo</td>
<td style="border:1px solid black;">Bloquear estación de trabajo</td>
</tr>
</tbody>
</table>
  
**Inicio de sesión interactivo: no mostrar el último nombre de usuario**  
Esta configuración de directiva determina si el nombre de la cuenta del último usuario que ha iniciado sesión en los equipos cliente de la organización aparecerá en la pantalla de inicio de sesión de Windows de cada equipo. Habilite esta configuración de directiva para impedir que algún intruso pueda ver los nombres de cuenta de las pantallas de equipos de escritorio o portátiles de la organización.
  
El valor **Inicio de sesión interactivo: no mostrar el último nombre de usuario** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr**  
La combinación de teclas Ctrl+Alt+Supr establece una ruta de confianza al sistema operativo cuando el usuario escribe un nombre de usuario y una contraseña. Cuando está habilitada esta configuración de directiva, no es necesario que los usuarios utilicen esta combinación de teclas para iniciar sesión en la red. Sin embargo, esta configuración conlleva un riesgo para la seguridad, ya que ofrece a los usuarios la oportunidad de iniciar sesión con credenciales no seguras.
  
El valor **Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión**  
Esta configuración de directiva especifica un mensaje de texto que se muestra a los usuarios cuando inician sesión. A menudo, este texto se utiliza por motivos legales; por ejemplo, para advertir a los usuarios acerca de las consecuencias del uso indebido de información empresarial o acerca de las acciones que se pueden auditar.
  
**Nota**   Las advertencias que decida mostrar deben recibir primero la aprobación de los representantes de asuntos jurídicos y recursos humanos de su organización. Además, las configuraciones **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** e **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar *ambas* habilitadas para funcionar sin problemas.
  
**Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión**  
Esta configuración de directiva permite especificar texto en la barra de título de la ventana que ven los usuarios cuando inician sesión en el sistema. El razonamiento para utilizar esta configuración de directiva es el mismo que para el anterior parámetro de texto de mensaje. Las organizaciones que no utilizan esta configuración de directiva son más vulnerables legalmente ante los intrusos que ataquen el sistema.
  
**Nota**   Las advertencias que decida mostrar deben recibir primero la aprobación de los representantes de asuntos jurídicos y recursos humanos de su organización. Además, las configuraciones **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** e **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** deben estar ambas habilitadas para funcionar sin problemas.
  
**Inicio de sesión interactivo: número de inicios de sesión anteriores que se almacenarán en caché (si el controlador de dominio no está disponible)**  
Esta configuración de directiva determina si un usuario puede iniciar sesión en un dominio de Windows utilizando la información de cuenta almacenada en caché. La información de inicio de sesión para cuentas de dominio se puede guardar localmente en caché para que los usuarios puedan iniciar sesión incluso si no es posible la comunicación con un controlador de dominio. Esta configuración de directiva determina el número de usuarios únicos cuya información de inicio de sesión se almacenará localmente en caché. El valor predeterminado de esta configuración de directiva es 10. Si este valor se establece en 0, la característica de caché de inicio de sesión se deshabilita, de forma que, si un atacante obtiene acceso al sistema de archivos del servidor, podría localizar esta información almacenada en caché y realizar un ataque de fuerza bruta para determinar las contraseñas de usuario.
  
El valor **Inicio de sesión interactivo: número de inicios de sesión anteriores que se almacenarán en caché (si el controlador de dominio no está disponible)** se configura en **2** para los equipos tanto de escritorio como portátiles en el entorno EC y para los equipos portátiles en el entorno SSLF. Sin embargo, esta configuración de directiva se establece en **0** para los equipos de escritorio en el entorno SSLF, porque estos equipos siempre debe estar conectados de forma segura a la red de la organización.
  
**Inicio de sesión interactivo: pedir al usuario que cambie la contraseña antes de que expire**  
Esta configuración de directiva determina con cuánta antelación se advertirá a los usuarios de la fecha de caducidad de las contraseñas. Microsoft recomienda establecer esta configuración de directiva en 14 días para advertir con suficiente antelación a los usuarios de la fecha de caducidad de sus contraseñas.
  
El valor **Inicio de sesión interactivo: pedir al usuario que cambie la contraseña antes de que expire** se configura en **14 días** en los dos entornos que se describen en esta guía.
  
**Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear la estación de trabajo**  
Cuando esta configuración de directiva está habilitada, un controlador de dominio debe autenticar la cuenta de dominio utilizada para desbloquear el equipo. Si esta configuración de directiva está deshabilitada, se pueden utilizar las credenciales en caché para desbloquear el equipo. Microsoft recomienda que esta configuración de directiva esté deshabilitada para los usuarios de equipos portátiles en ambos entornos, ya que éstos no disponen de acceso de red a controladores de dominio.
  
El valor **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear la estación de trabajo** se configura como **Habilitado** para los equipos de escritorio tanto en el entorno EC como en el entorno SSLF. Sin embargo, esta configuración de directiva se establece como **Deshabilitada** para los equipos portátiles en los dos entornos, lo que permite a estos usuarios trabajar cuando no se encuentran en la propia oficina.
  
**Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente**  
Esta configuración de directiva determina lo que ocurre cuando la tarjeta inteligente de un usuario que ha iniciado sesión se retira del lector de tarjetas inteligentes. Cuando se establece como **Bloquear estación de trabajo**, esta configuración de directiva bloquea la estación de trabajo en el momento en que se retira la tarjeta inteligente, lo que permite a los usuarios salir del área, llevarse sus tarjetas inteligentes y que sus estaciones de trabajo queden automáticamente bloqueadas. Si establece esta configuración de directiva como **Forzar cierre de sesión**, se cerrará automáticamente la sesión de los usuarios cuando se retire la tarjeta inteligente.
  
El valor **Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente** se configura en la opción **Bloquear estación de trabajo** en los dos entornos que se describen en esta guía.
  
###### Cliente de redes de Microsoft
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los equipos cliente de redes de Microsoft. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A21. Recomendaciones para la configuración de opciones de seguridad: Cliente de redes de Microsoft**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente de redes de Microsoft: enviar contraseña sin cifrar a servidores SMB de terceros</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)**  
Esta configuración de directiva determina si el componente de cliente SMB requiere la firma de paquetes. Si habilita esta configuración de directiva, el equipo cliente de redes de Microsoft no puede comunicarse con un servidor de red Microsoft salvo que dicho servidor acepte la firma de paquetes SMB. En entornos combinados con equipos cliente heredados, esta opción se debe configurar como **Deshabilitado**, ya que dichos equipos no se podrán autenticar u obtener acceso a controladores de dominio. No obstante, puede utilizar esta configuración de directiva en entornos con Windows 2000 o versiones posteriores.
  
El valor **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Habilitado** para los equipos de los dos entornos que se abordan en esta guía.
  
**Nota**   Si los equipos basados en Windows Vista tienen esta configuración de directiva habilitada y se conectan a recursos compartidos de archivos o impresión de servidores remotos, es importante que esta configuración se encuentre sincronizada con el valor correspondiente, **Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)**, de esos servidores. Para obtener más información sobre estas configuraciones, consulte la sección “Servidor y cliente de red de Microsoft: firmar digitalmente las comunicaciones (cuatro valores relacionados)” del capítulo 5 de la guía sobre [*amenazas y contramedidas*](http://go.microsoft.com/fwlink/?linkid=15159).
  
**Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)**  
Esta configuración de directiva determina si el cliente SMB intentará negociar la firma de paquetes SMB. La implementación de la firma digital en redes basadas en Windows ayuda a evitar el secuestro de sesiones. Si habilita esta configuración de directiva, el cliente de redes de Microsoft utilizará la firma sólo si el servidor con el que se comunica acepta comunicación firmada digitalmente.
  
El valor **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Habilite esta configuración de directiva en los clientes SMB de la red para permitirles la firma de paquetes con todos los clientes y servidores del entorno.
  
**Cliente de redes de Microsoft: enviar contraseña sin cifrar a servidores SMB de terceros**  
Deshabilite esta configuración de directiva para evitar que, durante la autenticación, el redirector SMB envíe contraseñas de texto sin formato a servidores SMB de terceros que no admitan el cifrado de contraseñas. Microsoft recomienda deshabilitar esta configuración de directiva a no ser que exista una razón empresarial de peso para habilitarla. Si esta configuración de directiva está habilitada, se permitirán contraseñas no cifradas en la red.
  
El valor **Cliente de redes de Microsoft: enviar contraseña sin cifrar a servidores SMB de terceros** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
###### Servidor de red Microsoft
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los servidores de red Microsoft. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A22. Recomendaciones para la configuración de opciones de seguridad: Servidor de red Microsoft**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servidor de red Microsoft: tiempo de inactividad requerido antes de suspender la sesión</td>
<td style="border:1px solid black;">15 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
<td style="border:1px solid black;">15 minutos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de red Microsoft: firmar digitalmente las comunicaciones (si el cliente lo permite)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de red Microsoft: desconectar a los clientes cuando expire el tiempo de inicio de sesión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Servidor de red Microsoft: tiempo de inactividad requerido antes de suspender la sesión**  
Esta configuración de directiva le permite especificar el tiempo de inactividad que debe transcurrir de forma ininterrumpida en una sesión SMB antes de que la sesión se suspenda por inactividad. Los administradores pueden utilizar esta configuración de directiva para controlar el momento en que un equipo suspende una sesión SMB inactiva. Al reanudarse la actividad del cliente, se restablece de forma automática la sesión.
  
El valor **Servidor de red Microsoft: tiempo de inactividad requerido antes de suspender la sesión** se configura en un período de **15 minutos** en los dos entornos que se describen en esta guía.
  
**Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)**  
Esta configuración de directiva determina si el servicio SMB de servidor es necesario para la firma de paquetes SMB. Habilite esta configuración de directiva en un entorno mixto para evitar que los clientes indirectos utilicen la estación de trabajo como un servidor de red.
  
El valor **Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Servidor de red Microsoft: firmar digitalmente las comunicaciones (si el cliente lo permite)**  
Esta configuración de directiva determina si el servicio SMB de servidor puede firmar paquetes SMB cuando lo solicite un cliente que intenta establecer una conexión. Si no hay ninguna solicitud de firma procedente del cliente, se permite una conexión sin firma en caso de que la configuración **Servidor de red Microsoft: firmar digitalmente las comunicaciones (siempre)** no esté habilitada.
  
El valor **Servidor de red Microsoft: firmar digitalmente las comunicaciones (si el cliente lo permite)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Habilite esta configuración de directiva en los clientes SMB de la red para permitirles la firma de paquetes con todos los clientes y servidores del entorno.
  
**Servidor de red Microsoft: desconectar a los clientes cuando expire el tiempo de inicio de sesión**  
Esta configuración de directiva determina si se desconecta a los usuarios que estén conectados al equipo local fuera de las horas de inicio de sesión válidas correspondientes a sus cuentas de usuario. Afecta al componente SMB. Si habilita esta configuración de directiva, se fuerza la desconexión de las sesiones de cliente con el servicio SMB cuando se agoten las horas de inicio de sesión del cliente. Si deshabilita esta configuración de directiva, las sesiones de cliente establecidas se mantienen después de que transcurran las horas de inicio de sesión del cliente. Si habilita esta configuración de directiva, también debe habilitar **Seguridad de red:** **forzar el cierre de sesión cuando expire la hora de inicio de sesión**.
  
Si la organización configura el tiempo de sesión de los usuarios, resulta buena idea habilitar esta configuración de directiva.
  
El valor **Cliente de redes de Microsoft: desconectar a los clientes cuando expire el tiempo de inicio de sesión** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
###### Configuración de MSS
  
La configuración siguiente incluye entradas de valor del Registro que no se muestran de manera predeterminada con el Editor de configuración de seguridad (SCE). El grupo Microsoft Solutions for Security desarrolló estas configuraciones (a las cuales se antepone siempre el prefijo **MSS:**) para la anterior guía de seguridad. La secuencia de comandos GPOAccelerator.wsf que se explica en el capítulo 1, “Implementación de líneas de base de seguridad”, modifica el SCE de modo que exhiba correctamente la configuración de MSS.
  
En la tabla siguiente se resume la configuración de MSS recomendada en cada uno de los entornos que se abordan en esta guía. A continuación de la tabla se amplía la información sobre los valores.
  
**Tabla A23. Recomendaciones para la configuración de opciones de seguridad: Configuración de MSS**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">MSS: (AutoAdminLogon) Enable Automatic Logon<br />
(not recommended)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Highest Protection, source routing is completely disabled.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">300000 or 5 minutes (recomendado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (NoDefaultExempt) Configure IPSec exemptions for various types of network traffic</td>
<td style="border:1px solid black;">Multicast, broadcast, and ISAKMP are exempt (idóneo para Windows XP)</td>
<td style="border:1px solid black;">Multicast, broadcast, and ISAKMP are exempt (idóneo para Windows XP)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)</td>
<td style="border:1px solid black;">255, disable Autorun for all drives</td>
<td style="border:1px solid black;">255, disable Autorun for all drives</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure DefaultGateway addresses (could lead to DoS)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires<br />
(0 recommended)</td>
<td style="border:1px solid black;">0</td>
<td style="border:1px solid black;">0</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Connections timeout sooner if SYN attack is detected</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (TCPMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">3 &amp; 6 seconds, half-open connections dropped after 21 seconds</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS: (TCPMaxDataRetransmissions) How many times unacknowledged data is retransmitted<br />
(3 recommended, 5 is default)</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">3</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">90</td>
</tr>
</tbody>
</table>
  
**MSS: (AutoAdminLogon) Enable Automatic Logon**  
La entrada de valor del Registro **AutoAdminLogon** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\**. La entrada aparece como **MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)** en el SCE.
  
Esta configuración es independiente de la característica de pantalla de bienvenida de Windows XP y Windows Vista; aunque deshabilite esa característica, el valor no se ve afectado. Si configura un equipo para inicio de sesión automático, cualquier persona que pueda obtener acceso físicamente al equipo puede obtener acceso también a sus recursos, incluida cualquier red a la que se conecte el equipo. Además, si habilita el inicio de sesión automático, la contraseña se almacena en el Registro en texto sin formato y el grupo Usuarios autenticados puede leer de forma remota la clave de Registro específica que almacena este valor. Por estos motivos, esta configuración se establece como **No definido** en el entorno EC mientras que, en el entorno SSLF, se aplica de forma explícita el valor predeterminado **Deshabilitado**.
  
Para obtener más información, consulte el artículo 315231 de Knowledge Base, “[Habilitar el inicio de sesión automático en Windows XP](http://support.microsoft.com/default.aspx?scid=315231)”.
  
**MSS: (DisableIPSourceRouting) IP source routing protection level**  
La entrada de valor de Registro **DisableIPSourceRouting** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)** en el SCE.
  
El enrutamiento de origen IP es un mecanismo que permite al remitente determinar la ruta IP que un datagrama debe tomar a través de la red. Este valor se configura en **No definido** en el entorno EC y en **Highest Protection,** **source routing is completely disabled** en el entorno SSLF.
  
**MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways**  
La entrada de valor de Registro **EnableDeadGWDetect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)** en el SCE.
  
Cuando se habilita la detección de puertas de enlace inactivas, IP puede cambiar a una puerta de enlace de reserva si varias conexiones experimentan dificultades. Esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes**  
La entrada de valor de Registro **EnableICMPRedirect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes** en el SCE.
  
Las redirecciones del Protocolo de mensajes de control de Internet (ICMP) provocan que la pila asocie rutas de host. Estas rutas invalidan las rutas generadas con el protocolo para abrir primero la ruta de acceso más corta (OSPF). Esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**MSS: (Hidden) Hide Computer From the Browse List**  
La entrada de valor del Registro **Hidden** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Lanmanserver\\Parameters\\**. La entrada aparece como **MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)** en el SCE.
  
Puede configurar un equipo para que no envíe anuncios a exploradores en el dominio. Si lo hace, oculta el equipo de la lista de búsqueda, lo que significa que el equipo deja de anunciarse a otros equipos de la misma red. Si el atacante sabe el nombre de un equipo, puede reunir con más facilidad información adicional acerca del sistema. Habilite esta configuración con el fin de quitar un método que puede aprovechar el atacante para reunir información acerca de los equipos de la red. Además, si habilita esta configuración, ayuda a reducir el tráfico de la red. Sin embargo, no son muchas las ventajas que aporta este parámetro desde el punto de vista de la seguridad, porque los atacantes pueden utilizar métodos alternativos para identificar y localizar los destinos potenciales. Por ello, Microsoft recomienda que habilite esta configuración sólo en entornos SSLF.
  
Esta configuración de directiva se establece como **No definido** en el entorno EC y como **Habilitado** en el entorno SSLF.
  
Para obtener más información, consulte el artículo 321710 de Knowledge Base, “[CÓMO: ocultar un equipo basado en Windows 2000 de la lista de exploradores](http://support.microsoft.com/default.aspx?scid=321710)” (en inglés).
  
**MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds**  
La entrada de valor del Registro **KeepAliveTime** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds (300,000 is recommended)** en el SCE.
  
Este valor controla la frecuencia con la que TCP intenta comprobar si una conexión inactiva permanece intacta mediante el envío de un paquete de mantenimiento de conexión. Si el equipo remoto sigue estando disponible, reconoce el paquete de mantenimiento de conexión. Esta configuración se establece como **No definido** en el entorno EC y como **300000** or **5 minutes** en el entorno SSLF.
  
**MSS: (NoDefaultExempt) Configure IPSec exemptions for various types of network traffic**  
La entrada de valor del Registro **NoDefaultExempt** se agregó al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\IPSEC\\**. La entrada aparece como **MSS: (NoDefaultExempt) Configure IPSec exemptions for various types of network traffic** en el SCE.
  
En la Ayuda en pantalla del sistema operativo oportuno se detallan las exenciones predeterminadas a los filtros de la directiva IPsec. Estos filtros hacen posible que funcionen Internet Key Exchange (IKE) y el protocolo de autenticación Kerberos. Los filtros también hacen posible que se señalice (RSVP) la calidad del servicio (QoS) de la red para el tráfico de datos protegido por IPsec y también para el tráfico que carezca de esa protección como, por ejemplo, el tráfico de difusión y multidifusión.
  
IPsec se usa cada vez más para el filtrado de paquetes básico de host a firewall, en especial en situaciones de exposición a Internet y, sin embargo, el efecto de estas exenciones predeterminadas no se comprende por completo. Por ello, algunos administradores de IPsec pueden crear directivas IPsec que consideran seguras pero que en realidad no lo son contra ataques entrantes que usan las exenciones predeterminadas. Microsoft recomienda que se aplique la configuración predeterminada para Windows XP con SP2, **Multicast,** **broadcast,** **and ISAKMP are exempt**, en los dos entornos que se describen en esta guía.
  
Para obtener más información, consulte el artículo 811832 de Knowledge Base, “[Las exenciones predetermiandas IPSec se pueden utilizar para omitir la protección IPsec en ciertos entornos](http://support.microsoft.com/default.aspx?scid=811832)” (en inglés).
  
**MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives**  
La entrada de valor del Registro **NoDriveTypeAutoRun** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\**  
**Policies\\Explorer\\**. La entrada aparece como **MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)** en el SCE.
  
La ejecución automática inicia la lectura de una unidad del equipo tan pronto como se insertan medios en ella. Como resultado, el archivo de instalación de los programas o el sonido de los medios de audio se inicia de inmediato. Esta configuración se establece en **255,** **Disable Autorun for all drives** en los dos entornos que se describen en esta guía.
  
**MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers**  
La entrada de valor del Registro **NoNameReleaseOnDemand** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Netbt\\**  
**Parameters\\**. La entrada aparece como **MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers** en el SCE.
  
NetBIOS sobre TCP/IP es un protocolo de red que, entre otras funciones, facilita la resolución de los nombres NetBIOS que se registran en sistemas basados en Windows en las direcciones IP configuradas en ellos. Esta configuración determina si el equipo libera su nombre NetBIOS al recibir una solicitud de liberación de nombre. Se establece como **No definido** en el entorno EC y como **Habilitado** en el entorno SSLF.
  
**MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames**  
La entrada de valor de Registro **NtfsDisable8dot3NameCreation** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\FileSystem\\**. La entrada aparece como **MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)** en el SCE.
  
Windows Server 2003 admite formatos de nombre de archivo 8.3 para la compatibilidad con aplicaciones de 16 bits anteriores. La convención de nombres de archivo 8.3 es un formato de nombre que permite una longitud máxima de ocho caracteres en los nombres de archivo. Esta configuración de directiva se establece como **No definido** en el entorno EC y como **Habilitado** en el entorno SSLF.
  
**MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses**  
La entrada de valor de Registro **PerformRouterDiscovery** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)** en el SCE.
  
Esta configuración habilita o deshabilita el protocolo de descubrimiento de enrutadores en Internet (IRDP), que permite al equipo detectar y configurar direcciones de puerta de enlace predeterminadas de manera automática (como se describe en RFC 1256) por interfaz. Esta configuración de directiva se establece como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**MSS: (SafeDllSearchMode) Enable Safe DLL Search Order**  
La entrada de valor de Registro **SafeDllSearchMode** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Control\\Session Manager\\**. La entrada aparece como **MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)** en el SCE.
  
La orden de búsqueda de DLL se puede configurar para que busque los archivos DLL que han solicitado los procesos en curso de una de estas dos formas:
  
-   Buscar primero en las carpetas especificadas en la ruta de acceso del sistema y, a continuación, buscar en la carpeta de trabajo actual.
  
-   Buscar primero en la carpeta de trabajo actual y, a continuación, buscar en las carpetas especificadas en la ruta de acceso del sistema.
  
Si se encuentra habilitado, el valor del Registro se establece en 1, lo que provoca que el equipo busque primero en las carpetas especificadas en la ruta de acceso del sistema y, después, en la carpeta de trabajo actual. Cuando se deshabilita, el valor de Registro se establece en 0 y el sistema busca primero la carpeta de trabajo actual y después busca las carpetas que se especifican en la ruta de acceso del sistema. Esta configuración se establece como **Habilitado** en los dos entornos que se describen en esta guía.
  
**MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires**  
La entrada de valor del Registro **ScreenSaverGracePeriod** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\SYSTEM\\Software\\Microsoft\\**  
**Windows NT\\CurrentVersion\\Winlogon\\**. La entrada aparece como **MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)** en el SCE.
  
Windows incluye un período de gracia que abarca desde que se inicia el protector de pantalla hasta que se bloquea la consola de forma automática si se habilita el bloqueo del protector de pantalla. Esta configuración se establece en **0** segundos en los dos entornos que se describen en esta guía.
  
**MSS: (SynAttackProtect) Syn attack protection level**  
La entrada de valor de Registro **SynAttackProtect** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)** en el SCE.
  
Esta configuración hace que TCP ajuste la retransmisión de SYN-ACK. Al configurar este valor, las respuestas de conexión exceden el tiempo de espera más rápidamente en caso de que se detecte un ataque de solicitud de conexión (SYN). Este valor se configura como **No definido** en el entorno EC y como **Connections timeout sooner if SYN attack is detected** en el entorno SSLF.
  
**MSS: (TCPMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged**  
La entrada de valor del Registro **TCPMaxConnectResponseRetransmissions** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\**  
**Services\\Tcpip\\Parameters\\**. La entrada aparece como **MSS: (TcpMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged** en el SCE.
  
Esta configuración determina el número de veces que TCP retransmite un SYN antes de anular el intento de conexión. El tiempo de espera de retransmisión se duplica con cada retransmisión sucesiva en el intento de conexión en cuestión. El valor de tiempo de espera inicial es de tres segundos. Esta configuración se establece como **No definido** en el entorno EC y como **3 & 6 seconds,** **half-open connections dropped after 21 seconds** en el entorno SSLF.
  
**MSS: (TCPMaxDataRetransmissions) How many times unacknowledged data is retransmitted**  
La entrada de valor del Registro **TCPMaxDataRetransmissions** está agregada al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip**  
**\\Parameters\\**. La entrada aparece como **MSS: (TcpMaxDataRetransmissions) How many times unacknowledged data is retransmitted (3 recommended,** **5 is default)** en el SCE.
  
Esta configuración controla el número de veces que TCP retransmite un segmento de datos individual (segmento sin conexión) antes de que se anule la conexión. El tiempo de espera de retransmisión se duplica con cada retransmisión sucesiva en una conexión. Se restablece cuando se reanudan las respuestas. El valor base de tiempo de espera se determina de forma dinámica según el tiempo de retorno medido en la conexión. Esta configuración se establece como **No definido** en el entorno EC y como **3** en el entorno SSLF.
  
**MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning**  
La entrada de valor de Registro **WarningLevel** se ha agregado al archivo de plantilla en la clave de Registro **HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Services\\Eventlog\\Security\\**. La entrada aparece como **MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning** en el SCE.
  
Esta configuración genera una auditoría de seguridad en el registro de eventos de seguridad cuando el registro alcanza el umbral definido por el usuario. Este parámetro de configuración de directiva se establece como **No definido** para el entorno EC y como **90** para el entorno SSLF.
  
**Nota**   Si la configuración del registro se establece en **Sobrescribir eventos cuando sea necesario** o en **Sobrescribir eventos que tengan más de** ***x*** **días**, no se genera este evento.
  
###### Acceso a la red
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el acceso a la red. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A24. Recomendaciones para la configuración de opciones de seguridad: Acceso a la red**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Acceso de red: permitir traducción SID/nombre anónima</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a redes: no permitir el almacenamiento de credenciales o cuentas de Passport Network para la autenticación de la red</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a redes: permitir la aplicación de los permisos Todos a los usuarios anónimos</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a redes: canalizaciones con nombre accesibles anónimamente</td>
<td style="border:1px solid black;">netlogon, lsarpc, samr, browser</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">netlogon, lsarpc, samr, browser</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a redes: rutas del Registro accesibles remotamente</td>
<td style="border:1px solid black;">System\CurrentControlSet\<br />
Control\ProductOptions
System\CurrentControlSet\<br />
Control\Server Applications
Software\Microsoft\Windows NT\CurrentVersion</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">System\CurrentControlSet\<br />
Control\ProductOptions
System\CurrentControlSet\<br />
Control\Server Applications
Software\Microsoft\Windows NT\CurrentVersion</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Acceso a redes: rutas y subrutas de registro accesibles remotamente</td>
<td style="border:1px solid black;">System\CurrentControlSet\<br />
Control\Print\Printers
System\CurrentControlSet\<br />
Services\Eventlog
Software\Microsoft\OLAP Server
Software\Microsoft\Windows NT\CurrentVersion\Print
Software\Microsoft\Windows NT\CurrentVersion\Windows
System\CurrentControlSet\<br />
ContentIndex
System\CurrentControlSet\<br />
Control\Terminal Server
System\CurrentControlSet\<br />
Control\Terminal Server\User Config
System\CurrentControlSet\<br />
Control\Terminal Server\Default User Config
Software\Microsoft\Windows NT\CurrentVersion\perflib
System\CurrentControlSet\<br />
Services\SysmonLog</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">System\CurrentControlSet\<br />
Control\Print\Printers
System\CurrentControlSet\<br />
Services\Eventlog
Software\Microsoft\OLAP Server
Software\Microsoft\Windows NT\CurrentVersion\Print
Software\Microsoft\Windows NT\CurrentVersion\Windows
System\CurrentControlSet\<br />
ContentIndex
System\CurrentControlSet\<br />
Control\Terminal Server
System\CurrentControlSet\<br />
Control\Terminal Server\User Config
System\CurrentControlSet\<br />
Control\Terminal Server\Default User Config
Software\Microsoft\Windows NT\CurrentVersion\perflib
System\CurrentControlSet\<br />
Services\SysmonLog</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a redes: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a redes: recursos compartidos accesibles anónimamente</td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a redes: modelo de seguridad y uso compartido para cuentas locales</td>
<td style="border:1px solid black;">Clásico: usuarios locales se autentican con credenciales propias</td>
<td style="border:1px solid black;">Clásico: usuarios locales se autentican con credenciales propias</td>
<td style="border:1px solid black;">Clásico: usuarios locales se autentican con credenciales propias</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
**Acceso de red: permitir traducción SID/nombre anónima**  
Esta configuración de directiva determina si un usuario anónimo puede solicitar atributos del identificador de seguridad (SID) para otro usuario o usar un SID para obtener el nombre de usuario correspondiente. Deshabilite esta configuración de directiva para evitar que los usuarios no autenticados obtengan nombres de usuario asociados a sus respectivos SID.
  
El valor **Acceso de red: permitir traducción SID/nombre anónima** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM**  
Esta configuración de directiva controla la capacidad de los usuarios anónimos para enumerar las cuentas en el Administrador de cuentas de seguridad (SAM). Si habilita esta configuración de directiva, los usuarios con conexiones anónimas no pueden enumerar nombres de usuario de cuentas de dominio en las estaciones de trabajo de su entorno. Esta configuración de directiva también permite restricciones adicionales en conexiones anónimas.
  
El valor **Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM**  
Esta configuración de directiva controla la capacidad de los usuarios anónimos para enumerar cuentas SAM y recursos compartidos. Si habilita esta configuración de directiva, los usuarios anónimos no podrán enumerar nombres de usuario de cuentas de dominio ni nombres de recursos compartidos de red en las estaciones de trabajo de su entorno.
  
El valor **Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Acceso a redes: no permitir el almacenamiento de credenciales o cuentas de Passport Network para la autenticación de la red**  
Esta configuración de directiva controla el almacenamiento de contraseñas y credenciales de autenticación en el sistema local.
  
El valor **Acceso a redes: no permitir el almacenamiento de credenciales o cuentas de Passport Network para la autenticación de la red** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Acceso a redes: permitir la aplicación de los permisos Todos a los usuarios anónimos**  
Esta configuración de directiva determina qué permisos adicionales se asignan para conexiones anónimas al equipo. Si habilita esta configuración de directiva, se permite que los usuarios anónimos de Windows realicen ciertas actividades, tal como enumerar los nombres de cuentas de dominio y de recursos compartidos de red. Un usuario no autorizado podría obtener de forma anónima una lista de los nombres de las cuentas y los recursos compartidos y usar dicha información para averiguar contraseñas o realizar ataques de ingeniería social.
  
Por lo tanto, el valor **Acceso a redes: permitir la aplicación de los permisos Todos a los usuarios anónimos** se configura como **Deshabilitado** en los dos entornos que se abordan en esta guía.
  
**Acceso a redes: canalizaciones con nombre accesibles anónimamente**  
Esta configuración de directiva determina qué sesiones de comunicación, o canalizaciones, tendrán atributos y permisos que permitan el acceso anónimo.
  
En el entorno EC, el valor **Acceso a redes: canalizaciones con nombre accesibles anónimamente** se configura como **No definido**. Sin embargo, se aplican los siguientes valores predeterminados para el entorno SSLF:
  
-   Netlogon
  
-   Isarpc
  
-   Samr
  
-   Explorador
  
**Acceso a redes: rutas del Registro accesibles remotamente**  
Esta configuración de directiva determina qué rutas del Registro serán accesibles después de hacer referencia a la clave WinReg para determinar permisos de acceso a las rutas de acceso.
  
En el entorno EC, el valor **Acceso a redes: rutas del Registro accesibles remotamente** se configura como **No definido**. Sin embargo, en el entorno SSLF se aplican los siguientes valores predeterminados:
  
-   System\\CurrentControlSet\\Control\\ProductOptions
  
-   System\\CurrentControlSet\\Control\\Server Applications
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion
  
**Acceso a redes: rutas y subrutas de registro accesibles remotamente**  
Esta configuración de directiva determina qué rutas y subrutas del registro serán accesibles cuando una aplicación o proceso haga referencia a la clave de **WinReg** para determinar los permisos de acceso.
  
El valor **Acceso a redes: rutas y subrutas del Registro accesibles remotamente** se configura como **No definido** en el entorno EC. En el entorno SSLF, en cambio, esta configuración se establece en lo siguiente:
  
-   System\\CurrentControlSet\\Control\\Print\\Printers
  
-   System\\CurrentControlSet\\Services\\Eventlog
  
-   Software\\Microsoft\\OLAP Server
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\Print
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows
  
-   System\\CurrentControlSet\\ContentIndex
  
-   System\\CurrentControlSet\\Control\\Terminal Server
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\User Config
  
-   System\\CurrentControlSet\\Control\\Terminal Server\\Default User Config
  
-   Software\\Microsoft\\Windows NT\\CurrentVersion\\perflib
  
-   System\\CurrentControlSet\\Services\\SysmonLog
  
**Acceso a redes: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos**  
Cuando está habilitada, esta configuración de directiva restringe el acceso anónimo a los recursos compartidos y las canalizaciones con nombre en las configuraciones **Acceso a redes: canalizaciones con nombre accesibles anónimamente** y **Acceso a redes: recursos compartidos accesibles anónimamente**. Esta configuración de directiva controla el acceso de sesión nulo a los recursos compartidos de los equipos agregando **RestrictNullSessAccess** con el valor **1** a la clave del Registro **HKLM\\System**  
**\\CurrentControlSet\\Services\\LanManServer\\Parameters**. El valor de registro activa y desactiva los recursos compartidos de sesión nula para controlar si el servicio de servidor restringe el acceso de los clientes sin autenticación a los recursos con nombre. Las sesiones nulas son un punto débil que puede explotarse a través de los distintos recursos compartidos (incluidos los predeterminados) en los equipos de su entorno.
  
El valor **Acceso a redes: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Acceso a redes: recursos compartidos accesibles anónimamente**  
Esta configuración de directiva determina a qué recursos compartidos de red pueden tener acceso los usuarios anónimos. El parámetro predeterminado de esta configuración de directiva tiene pocas repercusiones, ya que todos los usuarios se deben autenticar para poder obtener acceso a los recursos compartidos del servidor.
  
El valor **Acceso a redes: recursos compartidos accesibles anónimamente** se configura como **No definido** en el entorno EC. Sin embargo, debe asegurarse de que este valor se configure como **Ninguno** en el entorno SSLF.
  
**Nota**   Puede ser muy peligroso agregar otros recursos compartidos a esta configuración de directiva de grupo. Cualquier usuario de la red puede tener acceso a los recursos compartidos que se enumeran, lo que podría dar lugar a que datos confidenciales quedaran expuestos o resultaran dañados.
  
**Acceso a redes: modelo de seguridad y uso compartido para cuentas locales**  
Esta configuración de directiva determina el modo en que se autentican los inicios de sesión de red que utilizan cuentas locales. La opción **Clásico** permite un control preciso del acceso a los recursos, incluida la capacidad de asignar distintos tipos de acceso a usuarios diferentes para el mismo recurso. La opción **Sólo invitado** le permite tratar a todos los usuarios del mismo modo. En este contexto, todos los usuarios se autentican como **Sólo invitado** para recibir el mismo nivel de acceso a un recurso determinado.
  
Por lo tanto, la configuración **Acceso a redes: modelo de seguridad y recursos compartidos para cuentas locales** usa la opción **Clásico** predeterminada en los dos entornos que se describen en esta guía.
  
###### Seguridad de red
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la seguridad de red. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A25. Recomendaciones para la configuración de opciones de seguridad: Seguridad de red**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">No definido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Seguridad de red: nivel de autenticación de LAN Manager</td>
<td style="border:1px solid black;">Enviar sólo respuesta NTLMv2</td>
<td style="border:1px solid black;">Enviar sólo respuesta NTLMv2 y rechazar LM</td>
<td style="border:1px solid black;">Enviar sólo respuesta NTLMv2 y rechazar LM y NTLM</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Seguridad de red: requisitos de firma de cliente LDAP</td>
<td style="border:1px solid black;">Negociar firma</td>
<td style="border:1px solid black;">Negociar firma</td>
<td style="border:1px solid black;">Negociar firma</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Seguridad de red: seguridad de sesión mínima para clientes NTLM basados en SSP (incluida RPC segura)</td>
<td style="border:1px solid black;">Sin mínimo</td>
<td style="border:1px solid black;">Requerir seguridad de sesión NTLMv2, Requerir cifrado de 128 bits</td>
<td style="border:1px solid black;">Requerir seguridad de sesión NTLMv2, Requerir cifrado de 128 bits</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Seguridad de red: seguridad de sesión mínima para servidores NTLM basados en SSP (incluida RPC segura)</td>
<td style="border:1px solid black;">Sin mínimo</td>
<td style="border:1px solid black;">Requerir seguridad de sesión NTLMv2, Requerir cifrado de 128 bits</td>
<td style="border:1px solid black;">Requerir seguridad de sesión NTLMv2, Requerir cifrado de 128 bits</td>
</tr>
</tbody>
</table>
  
**Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña**  
Esta configuración de directiva determina si el valor de hash de LAN Manager (LM) para la contraseña nueva se almacena al cambiar la contraseña. El hash de LM es relativamente débil y propenso a ataques en comparación con el hash de Microsoft Windows NT®, más seguro desde el punto de vista criptográfico.
  
Por este motivo, el valor **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Puede que los sistemas operativos más antiguos y algunas aplicaciones de terceros no funcionen de manera correcta cuando está habilitada esta configuración de directiva. Asimismo, será necesario cambiar la contraseña de todas las cuentas tras habilitarlo.
  
**Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión**  
Esta configuración de directiva, que determina si se desconecta a los usuarios que estén conectados al equipo local fuera de las horas de inicio de sesión válidas correspondientes a sus cuentas de usuario, afecta al componente SMB. Si habilita esta configuración de directiva, se fuerza la desconexión de las sesiones de cliente con el servidor SMB cuando se agoten las horas de inicio de sesión del cliente. Si deshabilita esta configuración de directiva, las sesiones de cliente establecidas se mantienen después de que transcurran las horas de inicio de sesión del cliente.
  
El valor **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión** se configura como **No definido** en los dos entornos que se abordan en el apéndice.
  
**Seguridad de red: nivel de autenticación de LAN Manager**  
Esta configuración de directiva determina el tipo de autenticación desafío/respuesta que se emplea para los inicios de sesión de red. La autenticación de LM es el método menos seguro; da ocasión a que se descifren las contraseñas cifradas porque se pueden interceptar con facilidad en la red. NT LAN Manager (NTLM) es un tanto más seguro. NTLMv2 es la versión más completa de NTLM disponible en Windows Vista, Windows XP Professional, Windows Server 2003, Windows 2000 y Service Pack 4 (SP4) de Windows NT 4.0 o posteriores. NTLMv2 también se encuentra disponible para Windows 95 y Windows 98 con el cliente de servicios de directorio opcional.
  
Microsoft recomienda que establezca esta configuración de directiva en el nivel de autenticación más seguro que sea posible para su entorno. En entornos en los que sólo se ejecuten estaciones de trabajo basadas en Windows 2000 Server o Windows Server 2003 con Windows Vista o Windows XP Professional, establezca esta configuración de directiva en la opción **Enviar sólo respuesta NTLMv2 y rechazar LM y NTLM** para contar con el máximo grado de seguridad.
  
El valor **Seguridad de red: nivel de autenticación de LAN Manager** se configura como **Enviar sólo respuesta NTLMv2 y rechazar LM** en el entorno EC. Sin embargo, esta configuración de directiva se establece en el valor más restrictivo **Enviar sólo respuesta NTLMv2 y rechazar LM y NTLM** en el entorno SSLF.
  
**Seguridad de red: requisitos de firma de cliente LDAP**  
Esta configuración de directiva determina el nivel de firma de datos que se solicita en nombre de clientes que emiten peticiones LDAP BIND. Dado que el tráfico de red sin firmar es susceptible de sufrir ataques de tipo "Man-in-the-middle", un atacante podría provocar que un servidor LDAP tome decisiones basadas en consultas falsas del cliente LDAP.
  
Por ello, el valor de la configuración **Seguridad de red: requisitos de firma de cliente LDAP** se establece en **Negociar firma** en los dos entornos que se abordan en esta guía.
  
**Seguridad de red: seguridad de sesión mínima para clientes NTLM basados en SSP (incluida RPC segura)**  
Esta configuración de directiva determina los estándares de seguridad mínimos en las comunicaciones de aplicación a aplicación para clientes. Las opciones para esta configuración de directiva son:
  
-   Requerir seguridad de sesión NTLMv2
  
-   Requerir cifrado de 128 bits
  
Si todos los equipos de la red admiten NTLMv2 y cifrado de 128 bits (por ejemplo, Windows Vista, SP2 de Windows XP Professional y SP1 de Windows Server 2003), se pueden elegir las cuatro opciones de configuración para contar con el máximo grado de seguridad.
  
Ambas opciones, **Requerir seguridad de sesión NTLMv2** y **Requerir cifrado de 128 bits**, se encuentran habilitadas para la configuración **Seguridad de red: seguridad de sesión mínima para clientes NTLM basados en SSP (incluida RPC segura)** en los dos entornos que se abordan en esta guía.
  
**Seguridad de red: seguridad de sesión mínima para servidores NTLM basados en SSP (incluida RPC segura)**  
Esta configuración de directiva es semejante al parámetro anterior, pero afecta al lado del servidor de la comunicación con las aplicaciones. Las opciones para esta configuración son las mismas:
  
-   Requerir seguridad de sesión NTLMv2
  
-   Requerir cifrado de 128 bits
  
Si todos los equipos de la red admiten NTLMv2 y cifrado de 128 bits (por ejemplo, Windows Vista, SP2 de Windows XP Professional y SP1 de Windows Server 2003), se pueden elegir las cuatro opciones para contar con el máximo grado de seguridad.
  
Ambas opciones, **Requerir seguridad de sesión NTLMv2** y **Requerir cifrado de 128 bits**, se encuentran habilitadas para la configuración **Seguridad de red: seguridad de sesión mínima para servidores NTLM basados en SSP (incluida RPC segura)** en los dos entornos que se abordan en esta guía.
  
###### Consola de recuperación
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la consola de recuperación. En las subsecciones que siguen se amplía la información.
  
**Tabla A26. Recomendaciones para la configuración de opciones de seguridad: Consola de recuperación**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Consola de recuperación: permitir el inicio de sesión administrativo automático</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Consola de recuperación: permitir el inicio de sesión administrativo automático**  
La consola de recuperación es un entorno de línea de comandos que se utiliza para solucionar problemas en el sistema. Si habilita esta configuración de directiva, se iniciará automáticamente una sesión con la cuenta de administrador en la consola de recuperación al invocarla durante el inicio. Microsoft recomienda deshabilitar esta configuración de directiva puesto que obliga a los administradores a escribir una contraseña para obtener acceso a la consola de recuperación.
  
El valor **Consola de recuperación: permitir el inicio de sesión administrativo automático** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas**  
Mediante esta configuración de directiva estará disponible el comando SET de la consola de recuperación, lo que permitirá establecer las siguientes variables de entorno de la consola de recuperación:
  
-   **AllowWildCards**. Habilita la compatibilidad con caracteres comodín de algunos comandos (por ejemplo, DEL).
  
-   **AllowAllPaths**. Facilita el acceso a todos los archivos y a todas las carpetas del equipo.
  
-   **AllowRemovableMedia**. Permite la copia de archivos en medios extraíbles como discos.
  
-   **NoCopyPrompt**. No solicita confirmación al sobrescribir un archivo existente.
  
El valor **Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas** se configura como **No definido** en el entorno EC. Sin embargo, para contar con un máximo nivel de seguridad, este parámetro se configura como **Deshabilitado** para el entorno SSLF.
  
###### Apagar
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el apagado. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A27. Recomendaciones para la configuración de opciones de seguridad: Apagar**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Apagado: permitir apagar el sistema sin tener que iniciar sesión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Apagado: borrar el archivo de paginación de la memoria virtual (equipos de escritorio)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Apagado: borrar el archivo de paginación de la memoria virtual (equipos portátiles)</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Apagado: permitir apagar el sistema sin tener que iniciar sesión**  
Esta configuración de directiva determina si un equipo se puede apagar cuando el usuario no haya iniciado sesión en él. Si se habilita esta configuración de directiva, el comando de apagado estará disponible en la pantalla de inicio de sesión de Windows. Microsoft recomienda que deshabilite esta configuración de directiva para restringir la capacidad de apagar el equipo a sólo aquellos usuarios con credenciales en el sistema.
  
El valor **Apagado: permitir apagar el sistema sin tener que iniciar sesión** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Apagado: borrar el archivo de paginación de la memoria virtual**  
Esta configuración de directiva determina si el archivo de paginación de la memoria virtual se borra cuando se apaga el sistema. Con esta configuración de directiva habilitada, el archivo de paginación del sistema se borra cada vez que el sistema se apaga como es debido. Si se habilita esta configuración de seguridad, el archivo de hibernación (Hiberfil.sys) se borra cuando se deshabilita la hibernación en un equipo portátil. Esto aumenta el tiempo empleado en apagar y reiniciar el equipo, y resulta especialmente evidente en equipos con grandes archivos de paginación.
  
Por ello, el valor **Apagado: borrar el archivo de paginación de la memoria virtual** se configura como **Habilitado** en los equipos portátiles SSLF y como **Deshabilitado** en los demás tipos de equipos de los dos entornos que se abordan en esta guía.
  
###### Criptografía de sistema
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para la criptografía de sistema. A continuación de la tabla se amplía la información.
  
**Tabla A28. Recomendaciones para la configuración de opciones de seguridad: Criptografía de sistema**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Criptografía de sistema: usar algoritmos que cumplan FIPS para cifrado, firma y operaciones hash</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Criptografía de sistema: usar algoritmos que cumplan FIPS para cifrado, firma y operaciones hash**  
Esta configuración de directiva determina si el proveedor de seguridad de tipo Seguridad de la capa de transporte/Capa de sockets seguros (TLS/SSL) es compatible sólo con el conjunto cifrado TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA. Aunque esta configuración de directiva aumente la seguridad, la mayoría de los sitios Web públicos protegidos con TLS o SSL no son compatibles con estos algoritmos. Los equipos cliente que tengan esta configuración de directiva habilitada tampoco pueden conectar a Terminal Services de los servidores que no estén configurados para usar algoritmos que cumplan la norma FIPS.
  
El valor **Criptografía de sistema: usar algoritmos que cumplan FIPS para cifrado,** **firmay operaciones hash** se configura como **No definido** en el entorno EC y como **Deshabilitado** en el entorno SSLF.
  
**Nota**   Si habilita esta configuración de directiva, el rendimiento de los equipos se ralentiza porque el proceso 3DES se ejecuta tres veces en cada uno de los bloques de datos del archivo. Únicamente se debe habilitar esta configuración de directiva en el caso de que la empresa deba cumplir la norma FIPS.
  
###### Objetos de sistema
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para los objetos de sistema. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A29. Recomendaciones para la configuración de opciones de seguridad: Objetos de sistema**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Objetos de sistema: requerir no distinguir mayúsculas de minúsculas para subsistemas que no sean de Windows</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">No definido</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Objetos de sistema: requerir no distinguir mayúsculas de minúsculas para subsistemas que no sean de Windows**  
Esta configuración de directiva determina si no se requerirá la distinción entre mayúsculas y minúsculas en todos los subsistemas. El subsistema Microsoft Win32® hace distinción de mayúsculas y minúsculas. Sin embargo, el kernel admite la distinción entre mayúsculas y minúsculas en otros subsistemas como la interfaz del sistema operativo portátil para UNIX (POSIX). Dado que Windows no hace distinción de mayúsculas y minúsculas (pero el subsistema POSIX sí), si no se exige esta configuración un usuario del subsistema POSIX podrá crear un archivo con el mismo nombre que otro archivo utilizando mayúsculas y minúsculas en el nombre. Esto puede bloquear el acceso a estos archivos de otro usuario que use herramientas normales de Win32 porque sólo se encuentra disponible uno de esos archivos.
  
Para asegurar la coherencia de los nombres de archivo, el valor **Objetos de sistema: requerir no distinguir mayúsculas de minúsculas para subsistemas que no sean de Windows** se configura como **No definido** en el entorno EC y como **Habilitado** en el entorno SSLF.
  
**Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema**  
Esta configuración de directiva determina la fuerza de la lista de control de acceso discrecional (DACL) predeterminada de los objetos. Esta configuración ayuda a proteger los objetos que pueden ser localizados y compartidos entre procesos y su configuración predeterminada refuerza la DACL porque permite a los usuarios que no son administradores leer objetos compartidos al tiempo que les impide modificar ninguno que no hayan creado.
  
Por ello, la configuración **Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema** (por ejemplo, vínculos simbólicos) se establece en el valor predeterminado **Habilitado** en los dos entornos que se tratan en esta guía.
  
###### Control de cuentas de usuario
  
El Control de cuentas de usuario (UAC) reduce la exposición y la superficie de ataque del sistema operativo al exigir la ejecución de todos los usuarios en modo estándar de usuario aunque hayan iniciado sesión con credenciales administrativas. Esta restricción ayuda a minimizar la capacidad de los usuarios para realizar cambios que puedan desestabilizar sus equipos o exponer por accidente la red a virus mediante software malintencionado que, sin detectarlo, haya infectado el equipo.
  
Si el usuario intenta realizar alguna tarea administrativa, el sistema operativo debe elevar su nivel de seguridad para permitir la ejecución de dicha tarea. Las configuraciones de UAC de los GPO determinan el modo de respuesta del sistema operativo ante las solicitudes para elevar los privilegios de seguridad.
  
En la tabla siguiente se resume la configuración recomendada de opciones de seguridad para el control de cuentas de usuario. En las subsecciones que siguen a la tabla se amplía la información.
  
**Tabla A30. Recomendaciones para la configuración de opciones de seguridad: Control de cuentas de usuario**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Control de cuentas de usuario: Modo de aprobación de administrador para la cuenta Administrador integrado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Control de cuentas de usuario: comportamiento del indicador de elevación para los administradores en Modo de aprobación de administrador</td>
<td style="border:1px solid black;">Pedir consentimiento</td>
<td style="border:1px solid black;">Pedir credenciales</td>
<td style="border:1px solid black;">Pedir credenciales</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Control de cuentas de usuario: comportamiento del indicador de elevación para los usuarios estándar</td>
<td style="border:1px solid black;">Pedir credenciales</td>
<td style="border:1px solid black;">Denegar automáticamente solicitudes de elevación</td>
<td style="border:1px solid black;">Denegar automáticamente solicitudes de elevación</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Control de cuentas de usuario: detectar instalaciones de aplicaciones y pedir confirmación de elevación</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Control de cuentas de usuario: elevar sólo los archivos ejecutables firmados y validados</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Control de cuentas de usuario: elevar sólo aplicaciones UIAccess instaladas en ubicaciones seguras</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Control de cuentas de usuario: ejecutar todos los administradores en Modo de aprobación de administrador</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Control de cuentas de usuario: cambiar al escritorio seguro cuando se pida confirmación de elevación</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Control de cuentas de usuario: virtualizar los errores de archivo y escritura de Registro por ubicaciones de usuario</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
**Control de cuentas de usuario: Modo de aprobación de administrador para la cuenta Administrador integrado**  
Esta configuración de directiva indica si la cuenta de administrador integrado se ejecuta en Modo de aprobación de administrador. El comportamiento predeterminado de esta configuración es variable ya que Windows Vista configura la cuenta de administrador integrado según los criterios específicos de la instalación.
  
Windows Vista configura el valor como **Deshabilitado** de manera predeterminada en las instalaciones nuevas y las actualizaciones si el administrador integrado *no* es el único administrador local activo en el equipo. Windows Vista deshabilita la cuenta de administrador integrado de forma predeterminada en las instalaciones y las actualizaciones llevadas a cabo en equipos unidos en un dominio.
  
Windows Vista configura el valor como **Habilitado** de manera predeterminada en las actualizaciones si determina que la cuenta de administrador integrado constituye el único administrador local activo en el equipo. En este caso, Windows Vista habilita esa cuenta después de la actualización.
  
La configuración **Control de cuentas de usuario: Modo de aprobación de administrador para la cuenta Administrador integrado** se establece en **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Control de cuentas de usuario: comportamiento del indicador de elevación para los administradores en Modo de aprobación de administrador**  
Esta configuración determina el comportamiento de Windows Vista cuando un administrador, después de iniciar sesión, intenta realizar alguna tarea que exige la elevación de privilegios. Admite tres valores:
  
-   **No preguntar**. Al usar este valor, se elevan los privilegios de forma automática y de forma silenciosa.
  
-   **Pedir consentimiento**. Al usar este valor, UAC solicita permiso antes de elevar los privilegios pero no se exigen credenciales.
  
-   **Pedir credenciales**. Al usar este valor, UAC obliga al administrador a escribir unas credenciales de administrador válidas cuando se le solicite antes de elevar los privilegios.
  
La configuración **Control de cuentas de usuario: comportamiento del indicador de elevación para los administradores en Modo de aprobación de administrador** se establece como **Pedir credenciales** en los dos entornos que se abordan en esta guía.
  
**Control de cuentas de usuario: comportamiento del indicador de elevación para los usuarios estándar**  
Esta configuración determina el comportamiento de Windows Vista cuando un usuario, después de iniciar sesión, intenta realizar alguna tarea que exige la elevación de privilegios. Admite dos valores:
  
-   **Denegar automáticamente solicitudes de elevación**. Al usar este valor, se impide que aparezcan las solicitudes de elevación, de manera que el usuario no puede realizar tareas administrativas a menos que emplee el comando **Ejecutar** como administrador o inicie sesión con una cuenta de administrador.
  
-   **Pedir credenciales**. Al usar este valor, UAC obliga al administrador a escribir unas credenciales de administrador válidas cuando se le solicite antes de elevar los privilegios.
  
La configuración **Control de cuentas de usuario: comportamiento del indicador de elevación para los usuarios estándar** se establece en **Denegar automáticamente solicitudes de elevación** en los dos entornos que se abordan en esta guía.
  
Esta configuración impide que los usuarios estándar eleven sus privilegios, es decir, los usuarios estándar no pueden suministrar credenciales de cuentas administrativas a fin de realizar tareas administrativas. En el caso de los usuarios estándar, el procedimiento consistente en hacer clic con el botón secundario y elegir **Ejecutar como administrador** no funciona. Si un usuario estándar necesita llevar a cabo alguna tarea administrativa, debe cerrar la sesión y volver a iniciarla con una cuenta administrativa. Aunque este proceso es algo engorroso, resulta muy eficaz para mejorar la seguridad del entorno.
  
**Control de cuentas de usuario: detectar instalaciones de aplicaciones y pedir confirmación de elevación**  
Esta configuración determina cómo responde Windows Vista a las solicitudes de instalación de aplicaciones. Para instalar una aplicación, es preciso elevar los privilegios. Admite dos valores:
  
-   **Habilitado**. Al usar este valor, Windows Vista solicita al usuario, en cuanto detecta un instalador, su consentimiento o las credenciales oportunas, según el comportamiento establecido con la configuración de solicitud de elevación.
  
-   **Deshabilitado**. Al usar este valor, se produce un error de forma silenciosa o no determinista en la instalación de aplicaciones.
  
La configuración **Control de cuentas de usuario: detectar instalaciones de aplicaciones y pedir confirmación de elevación** se configura como **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Control de cuentas de usuario: elevar sólo los archivos ejecutables firmados y validados**  
Esta configuración permite impedir la ejecución de aplicaciones que no estén firmadas o validadas. Antes de habilitarla, es esencial que los administradores tengan la absoluta certeza de que todas las aplicaciones necesarias se encuentren firmadas o validadas. Admite dos valores:
  
-   **Habilitado**. Al usar este valor, sólo se permite la ejecución de archivos ejecutables firmados. Esta configuración bloquea la ejecución de aplicaciones no firmadas.
  
-   **Deshabilitado**. Al usar este valor, se permite la ejecución de ejecutables tanto firmados como sin firma.
  
La configuración **Control de cuentas de usuario: elevar sólo los archivos ejecutables firmados y validados** se establece en **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Control de cuentas de usuario: elevar sólo aplicaciones UIAccess instaladas en ubicaciones seguras**  
Esta configuración ayuda a proteger los equipos basados en Windows Vista al permitir, en exclusiva, la ejecución con privilegios elevados de aplicaciones instaladas en ubicaciones seguras del sistema de archivos, por ejemplo, las carpetas Archivos de programa o Windows\\System32.
  
La configuración **Control de cuentas de usuario: elevar sólo aplicaciones UIAccess instaladas en ubicaciones seguras** se establece en **Habilitado** en los dos entornos que se describen en esta guía.
  
**Control de cuentas de usuario: ejecutar todos los administradores en Modo de aprobación de administrador**  
Esta configuración sirve para deshabilitar UAC. Admite dos valores:
  
-   **Habilitado**. Al usar este valor, se formulan preguntas tanto a administradores como a usuarios estándar cuando cualquiera de ellos intenta realizar alguna operación administrativa. El estilo de la solicitud depende de la directiva.
  
-   **Deshabilitado**. Al usar este valor, se deshabilita el tipo de usuario en Modo de aprobación de administrador así como todas las directivas de UAC relacionadas. Si elige este valor, el Centro de seguridad avisa de la merma en la seguridad general del sistema operativo.
  
La configuración **Control de cuentas de usuario: ejecutar todos los administradores en Modo de aprobación de administrador** se establece en **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Control de cuentas de usuario: cambiar al escritorio seguro cuando se pida confirmación de elevación**  
Esta configuración ayuda a proteger el equipo y a los usuarios contra el posible uso malintencionado de las solicitudes de elevación. El escritorio seguro de Windows Vista sólo puede ejecutar procesos SYSTEM que, en general, eliminan los mensajes provenientes de software malintencionado. Como resultado, suele resultar imposible suplantar entradas de solicitudes de consentimiento y credenciales en el escritorio seguro. Además, las solicitudes de consentimiento se encuentran protegidas de la suplantación de salida. Sí existe cierto riesgo con las solicitudes de credenciales porque cabe la posibilidad de que el software malintencionado las suplante. Esta configuración cuenta con dos valores:
  
-   **Habilitado**. Al usar este valor, se muestra la solicitud de elevación de UAC en el escritorio seguro.
  
-   **Deshabilitado**. Al usar este valor, se muestra la solicitud de elevación de UAC en el escritorio de usuario.
  
La configuración **Control de cuentas de usuario: cambiar al escritorio seguro cuando se pida confirmación de elevación** se configura como **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Control de cuentas de usuario: virtualizar los errores de archivo y escritura de Registro por ubicaciones de usuario**  
Si una aplicación carece de una entrada de base de datos para la compatibilidad de aplicaciones o bien de la marca solicitada de nivel de ejecución en el manifiesto de aplicaciones, significa que no es compatible con UAC. Las aplicaciones que no son compatibles con UAC intentan escribir en zonas protegidas como, entre otras, Archivos de programa y %*systemroot*%. Estas aplicaciones generan un error de forma silenciosa si no logran finalizar el proceso de escritura. Al habilitar esta configuración, Windows Vista virtualiza las escrituras de archivos y del Registro en ubicaciones de usuario y, como consecuencia, permite la ejecución de estas aplicaciones.
  
En principio, las aplicaciones compatibles con UAC no escriben en zonas protegidas, por lo que no generan errores de escritura. Así pues, en los entornos donde sólo se empleen aplicaciones compatibles con UAC, conviene deshabilitar esta configuración.
  
Esta configuración admite dos valores:
  
-   **Habilitado**. En los entornos donde se utilice software que no sea compatible con UAC, conviene establecer esta configuración en **Habilitado**.
  
-   **Deshabilitado**. En los entornos donde se utilice software compatible con UAC, conviene establecer esta configuración en **Deshabilitado**.
  
Si no sabe con certeza si todas las aplicaciones del entorno son compatibles con UAC, configure este valor en **Habilitado**.
  
Por este motivo, la configuración **Control de cuentas de usuario: virtualizar los errores de archivo y escritura de Registro por ubicaciones de usuario** se establece en **Habilitado** en los dos entornos que se abordan en esta guía.
  
##### Configuración de seguridad del registro de eventos
  
El registro de eventos registra eventos en el sistema y el registro de seguridad registra eventos de auditoría. El contenedor de registro de eventos de directiva de grupo se utiliza para definir atributos relacionados con la aplicación, la seguridad y los registros de eventos del sistema como, por ejemplo, el tamaño máximo del registro, los derechos de acceso para los registros, así como la configuración y los métodos de retención.
  
Puede establecer la configuración del registro de eventos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Registro de eventos**
  
En esta sección se proporcionan detalles sobre la configuración recomendada en los entornos que se abordan en esta guía. Para obtener un resumen de las configuraciones recomendadas en esta sección, consulte el archivo Windows Vista Security Guide Settings.xls. Para obtener más información acerca de la configuración predeterminada y una explicación detallada de las configuraciones descritas en esta sección, consulte la guía sobre [*amenazas y contramedidas*](http://go.microsoft.com/fwlink/?linkid=15159). Esta guía complementaria incluye también información detallada acerca de la posibilidad de perder datos del registro de eventos cuando el tamaño de registro se establece en valores muy elevados.
  
En la siguiente tabla se resumen las recomendaciones sobre la configuración de seguridad del registro de eventos para equipos cliente de escritorio y portátiles en los dos tipos de entornos que se describen en esta guía. Cada uno de los valores se describe con detalle en las subsecciones que aparecen a continuación.
  
**Tabla A31. Recomendaciones para la configuración de opciones de seguridad: configuración de seguridad del registro de eventos**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Tamaño máximo del registro de la aplicación</td>
<td style="border:1px solid black;">No aplicable<br />
(valor predeterminado = 20480)</td>
<td style="border:1px solid black;">32768 KB</td>
<td style="border:1px solid black;">32768 KB</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tamaño máximo del registro de seguridad</td>
<td style="border:1px solid black;">No aplicable<br />
(valor predeterminado = 20480)</td>
<td style="border:1px solid black;">81920 KB</td>
<td style="border:1px solid black;">81920 KB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tamaño máximo del registro del sistema</td>
<td style="border:1px solid black;">No aplicable<br />
(valor predeterminado = 20480)</td>
<td style="border:1px solid black;">32768 KB</td>
<td style="border:1px solid black;">32768 KB</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Método de retención del registro de la aplicación</td>
<td style="border:1px solid black;">No aplicable (valor predeterminado = Sobrescribir cuando sea necesario)</td>
<td style="border:1px solid black;">Según se necesite</td>
<td style="border:1px solid black;">Según se necesite</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Método de retención del registro de seguridad</td>
<td style="border:1px solid black;">No aplicable (valor predeterminado = Sobrescribir cuando sea necesario)</td>
<td style="border:1px solid black;">Según se necesite</td>
<td style="border:1px solid black;">Según se necesite</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Método de retención del registro del sistema</td>
<td style="border:1px solid black;">No aplicable (valor predeterminado = Sobrescribir cuando sea necesario)</td>
<td style="border:1px solid black;">Según se necesite</td>
<td style="border:1px solid black;">Según se necesite</td>
</tr>
</tbody>
</table>
  
**Tamaño máximo del registro de la aplicación**  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de la aplicación, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de aplicación varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
La configuración **Tamaño máximo del registro de la aplicación** se establece en **32768** **KB** para todos los equipos de los dos entornos que se abordan en esta guía.
  
**Tamaño máximo del registro de seguridad**  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos de seguridad, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de seguridad varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
La configuración **Tamaño máximo del registro de seguridad** se establece en **81920 KB** para todos los equipos de los dos entornos que se abordan en esta guía.
  
**Tamaño máximo del registro del sistema**  
Esta configuración de directiva especifica el tamaño máximo del registro de eventos del sistema, que tiene una capacidad máxima de 4 GB. Sin embargo, no se recomienda este tamaño a causa del riesgo de fragmentación de memoria, que provoca una pérdida de rendimiento y errores en el registro de eventos. Los requisitos del tamaño del registro de aplicación varían en función de la plataforma y la necesidad de registros históricos de los eventos relacionados con aplicaciones.
  
La configuración **Tamaño máximo del registro del sistema** se establece en **32768 KB** para todos los equipos de los dos entornos que se abordan en esta guía.
  
**Método de retención del registro de la aplicación**  
Esta configuración de directiva determina el método de "ajuste" del registro de la aplicación. Es de gran importancia que el registro de aplicaciones se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
**Método de retención del registro de la aplicación** se configura como **Según se necesite** en los dos entornos que se abordan en esta guía.
  
**Método de retención del registro de seguridad**  
Esta configuración de directiva determina el método de "ajuste" del registro de seguridad. Es de gran importancia que el registro de seguridad se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
**Método de retención del registro de seguridad** se configura como **Según se necesite** en los dos entornos que se abordan en esta guía.
  
**Método de retención del registro del sistema**  
Esta configuración de directiva determina el método de "ajuste" del registro del sistema. Es de gran importancia que el registro del sistema se archive regularmente si se desea disponer de eventos históricos para fines de argumentación y solución de problemas. La sobrescritura de eventos según sea necesario garantiza que el registro almacenará siempre los eventos más recientes, aunque esta configuración pueda ocasionar la pérdida de datos históricos.
  
**Método de retención del registro del sistema** se configura como **Según se necesite** en los dos entornos que se abordan en esta guía.
  
##### Configuración de Firewall de Windows con seguridad avanzada
  
El firewall incluido con Windows Vista permite ejercer un control más preciso de su configuración.
  
Puede establecer la configuración de Firewall de Windows con seguridad avanzada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**  
**Firewall de Windows con seguridad avanzada**
  
Para controlar estas configuraciones, haga clic en el vínculo **Propiedades de Firewall de Windows** de la sección Firewall de Windows con seguridad avanzada del Editor de objetos de directiva de grupo. En el cuadro de diálogo **Firewall de Windows con seguridad avanzada**, especifique la configuración adecuada para los perfiles privado, público y de dominio. En cada perfil se pueden especificar valores generales en la sección **Estado** y valores personalizados eligiendo el botón **Personalizar** de la sección **Configuración**. Esta sección del apéndice incluye tablas y recomendaciones para los perfiles susceptibles de configuración en el cuadro de diálogo **Firewall de Windows con seguridad avanzada**.
  
###### Perfil de dominio
  
Este perfil se aplica cuando el equipo está conectado a una red y realiza la autenticación en un controlador del dominio al que pertenece el equipo.
  
**Tabla A32. Configuración recomendada del perfil de dominio**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Estado del firewall</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Conexiones entrantes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Conexiones salientes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Configuraciones personalizadas</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Mostrar una notificación</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Permitir respuesta de unidifusión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Aplicar reglas de firewall local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Aplicar reglas de seguridad de conexión local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
La configuración recomendada de Firewall de Windows con seguridad avanzada en el entorno EC incluye reglas de firewall que permiten las comunicaciones de Escritorio remoto y Asistencia remota. Además, los administradores locales de equipos del entorno EC tienen la posibilidad de configurar reglas de firewall locales con el fin de permitir otras comunicaciones con los equipos.
  
En el entorno SSLF, en cambio, todas las comunicaciones entrantes se encuentran bloqueadas de manera predeterminada y los equipos pasan por alto las reglas de firewall locales. Toda adición a las reglas de firewall o modificación en ellas se debe configurar con el Editor de objetos de directiva de grupo.
  
**Importante**   La configuración recomendada de firewall para el entorno SSLF limita en gran medida las conexiones entrantes en los equipos. Conviene llevar a cabo pruebas exhaustivas con esta configuración de firewall en el entorno con objeto de garantizar el correcto funcionamiento de todas las aplicaciones.
  
Para controlar las reglas definidas para el perfil de dominio, haga clic en el vínculo **Reglas de entrada** de la sección Firewall de Windows con seguridad avanzada del Editor de objetos de directiva de grupo.
  
###### Perfil privado
  
Este perfil sólo se aplica si el usuario con privilegios de administrador local lo asigna a una red en la que esté establecido el uso del perfil público. Microsoft recomienda que no se cambie el perfil a Privado salvo en las redes de confianza.
  
**Tabla A33. Configuración recomendada del perfil privado**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Estado del firewall</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Conexiones entrantes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Conexiones salientes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Configuraciones personalizadas</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Mostrar una notificación</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Permitir respuesta de unidifusión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Aplicar reglas de firewall local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Aplicar reglas de seguridad de conexión local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sí (predeterminado)</td>
<td style="border:1px solid black;">No</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
La configuración recomendada de Firewall de Windows con seguridad avanzada en el entorno EC incluye reglas de firewall que permiten las comunicaciones de Escritorio remoto. Además, los administradores locales de equipos del entorno EC tienen la posibilidad de configurar reglas de firewall locales con el fin de permitir otras comunicaciones con los equipos.
  
En el entorno SSLF, en cambio, todas las comunicaciones entrantes se encuentran bloqueadas de manera predeterminada y los equipos pasan por alto las reglas de firewall locales. Toda adición a las reglas de firewall o modificación en ellas se debe configurar con el Editor de objetos de directiva de grupo.
  
Para controlar las reglas definidas para el perfil privado, haga clic en el vínculo **Reglas de entrada** de la sección Firewall de Windows con seguridad avanzada del Editor de objetos de directiva de grupo.
  
###### Perfil público
  
Este perfil constituye el tipo de ubicación de red predeterminado cuando el equipo no está conectado a ningún dominio. La configuración del perfil público debe ser lo más restrictiva posible ya que el equipo se encuentra conectado a una red pública donde la seguridad no es tan hermética como en los entornos de TI.
  
**Tabla A34. Configuración recomendada del perfil público**

 
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
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Valor predeterminado de Windows Vista</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para EC</th>
<th style="border:1px solid black;" >GPO de equipos de VSG para SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Estado del firewall</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
<td style="border:1px solid black;">Activado (recomendado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Conexiones entrantes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
<td style="border:1px solid black;">Bloquear (predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Conexiones salientes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
<td style="border:1px solid black;">Permitir (predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Configuraciones personalizadas</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Mostrar una notificación</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Permitir respuesta de unidifusión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Aplicar reglas de firewall local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Aplicar reglas de seguridad de conexión local</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
Tanto en el entorno EC como en el entorno SSLF, todas las comunicaciones entrantes se bloquean de manera predeterminada y no existe ninguna regla de firewall que permita otras comunicaciones con los equipos. Es más, los equipos pasan por alto las reglas de firewall locales en los dos entornos que se describen en esta guía. Toda adición a las reglas de firewall aplicables al perfil público o modificación en ellas se debe configurar con el Editor de objetos de directiva de grupo.
  
En las secciones siguientes se ofrece una breve descripción de los valores que se pueden configurar en cada uno de los perfiles de firewall.
  
**Estado del firewall**  
Seleccione **Activado (recomendado)** si desea que Firewall de Windows con seguridad avanzada use la configuración de este perfil para filtrar el tráfico de la red. Si selecciona **Desactivado**, Firewall de Windows con seguridad avanzada prescinde de todas las reglas de firewall y de seguridad de las conexiones que correspondan al perfil.
  
**Conexiones entrantes**  
Esta configuración determina el comportamiento cuando se trata de conexiones entrantes que no coincidan con ninguna regla de firewall de entrada. El comportamiento predeterminado consiste en bloquear las conexiones a menos que exista alguna regla de firewall que las permita.
  
**Conexiones salientes**  
Esta configuración determina el comportamiento cuando se trata de conexiones salientes que no coincidan con ninguna regla de firewall de salida. El comportamiento predeterminado consiste en permitir las conexiones a menos que exista alguna regla de firewall que las bloquee.
  
**Importante**   Si **Conexiones salientes** se establece en **Bloquear** y, acto seguido, se implementa la directiva de firewall con un GPO, los equipos que reciban la configuración del GPO no pueden recibir las subsiguientes actualizaciones de la directiva de grupo a no ser que cree e implemente una regla de salida para habilitar el funcionamiento de dicha directiva. Las reglas predefinidas para Redes principales incluyen reglas de salida que habilitan el funcionamiento de la directiva de grupo. Asegúrese de que esas reglas de salida se encuentren activas y realice pruebas exhaustivas con los perfiles de firewall antes de implementar ninguno.
  
**Mostrar una notificación**  
Seleccione esta opción para que Firewall de Windows con seguridad avanzada muestre notificaciones al usuario cada vez que se bloquee la recepción de conexiones entrantes en un programa.
  
**Nota**   Si la configuración **Aplicar reglas de firewall local** se establece en **No**, Microsoft recomienda configurar el valor **Mostrar una notificación** también en **No**. Si se omite este paso, los usuarios no dejan de recibir mensajes donde se les pregunta si desean desbloquear la conexión entrante restringida a pesar de que no se acata su respuesta.
  
**Permitir respuesta de unidifusión**  
Esta opción resulta de utilidad para controlar si los equipos reciben respuestas de unidifusión a sus mensajes salientes de difusión o multidifusión. Si esta configuración está habilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows con seguridad avanzada espera hasta tres segundos respuestas de unidifusión de los otros equipos y, después, bloquea todas las respuestas posteriores. Sin embargo, si está deshabilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows con seguridad avanzada bloquea las respuestas de unidifusión que envían esos otros equipos.
  
**Aplicar reglas de firewall local**  
Esta configuración controla si los administradores locales tienen permiso para crear reglas de firewall locales que se apliquen junto con las reglas de firewall configuradas mediante la directiva de grupo. Aunque configure este valor en **No**, los administradores pueden crear reglas de firewall; no obstante, no se aplican. Esta configuración sólo se encuentra disponible al configurar la regla por medio de la directiva de grupo.
  
**Aplicar reglas de seguridad de conexión local**  
Esta configuración controla si los administradores locales tienen permiso para crear reglas de seguridad de las conexiones que se apliquen junto con las reglas de seguridad de conexión configuradas mediante la directiva de grupo. Aunque configure este valor en **No**, los administradores pueden crear reglas de firewall; no obstante, no se aplican. Esta configuración sólo se encuentra disponible al configurar la regla por medio de la directiva de grupo.
  
#### Configuración del equipo\\Plantillas administrativas
  
A continuación figuran los grupos de configuraciones recomendadas para la directiva de equipos. Estas configuraciones aparecen en el subnodo **Configuración del equipo\\Plantillas administrativas** del Editor de objetos de directiva de grupo.
  
-   [Conexiones de red](#_network_connections)
  
-   [Sistema](#_system)
  
    -   [Inicio de sesión](#_logon)
  
    -   [Directiva de grupo](#_group_policy)
  
    -   [Asistencia remota](#_remote_assistance)
  
    -   [Llamada a procedimiento remoto](#_remote_procedure_call)
  
    -   [Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet](#_internet_communication_management--)
  
-   [Componentes de Windows](#_windows_components_2)
  
    -   [Directivas de reproducción automática](#_autoplay_policies)
  
    -   [Interfaz de usuario de credenciales](#_credential_user_interface)
  
    -   [Internet Explorer](#_internet_explorer_2)
  
    -   [NetMeeting](#_netmeeting)
  
    -   [Terminal Services](#_terminal_services)
  
    -   [Windows Messenger](#_windows_messenger)
  
    -   [Windows Update](#_windows_update)
  
##### Conexiones de red
  
No hay configuraciones específicas relacionadas con la seguridad en el contenedor de Red de Directiva de grupo. Sin embargo, hay varias opciones de configuración muy importantes en el contenedor **Conexiones de red\\Firewall de Windows**.
  
Microsoft recomienda configurar Firewall de Windows con los valores de Firewall de Windows con seguridad avanzada disponibles en el Editor de objetos de directiva de grupo. Ahora bien, debe tener en cuenta que la configuración recomendada para Firewall de Windows con seguridad avanzada altera el estado en varios valores de este área de la directiva de grupo. Asimismo, varios de los valores recomendados ayudan a mantener la compatibilidad con los equipos que ejecuten Windows XP en el entorno EC descrito en la guía.
  
En Windows XP, la configuración de Firewall de Windows se establece en dos perfiles: Perfil de dominio y Perfil estándar. Siempre que se detecte un entorno de dominio, se emplea el perfil de dominio; si se detecta un entorno que no sea de dominio, se usa el perfil estándar.
  
Cuando una opción de configuración de Firewall de Windows aparece **Recomendada** en una de los dos tablas siguientes, el valor específico que se debe utilizar variará según la organización. Como cada organización posee una lista propia de aplicaciones para las que definir excepciones en Firewall de Windows, no resulta factible definir en esta guía una lista de uso universal.
  
Cuando necesite determinar qué aplicaciones o puertos se deben exceptuar, quizá sea útil habilitar el registro de Firewall de Windows, la auditoría de Firewall de Windows y el seguimiento de red. Para obtener más información, consulte el artículo sobre la [configuración de un equipo para solucionar problemas de Windows Firewall](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/operations/bfdeda55-46fc-4b53-b4cd-c71838ef4b41.mspx) (en inglés).
  
Normalmente, el Perfil de dominio se configura de modo que sea menos restrictivo que el Perfil estándar, ya que un entorno de dominio suele proporcionar capas de protección adicionales. Los nombres de configuración de directiva son idénticos en ambos perfiles. En las dos tablas siguientes se resumen las configuraciones de directiva para los distintos perfiles y se proporcionan explicaciones más detalladas en las subsecciones que siguen a las tablas.
  
###### Conexiones de red\\Firewall de Windows\\Perfil de dominio
  
Los valores de esta sección sirven para configurar el perfil de dominio de Firewall de Windows. Puede establecer esta configuración en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Red\\Conexiones de red**  
**\\Firewall de Windows\\Perfil de dominio**
  
**Tabla A35. Configuración recomendada del perfil de dominio de Firewall de Windows**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones ICMP</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepción de administración remota de entrada</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de Escritorio remoto de entrada</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de entorno UPnP de entrada</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de puerto local</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de programa local</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: definir excepciones de puerto de entrada</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: definir excepciones de programa de entrada</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: no permitir excepciones</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: no permitir notificaciones</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: proteger todas las conexiones de red</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Nota**   Las configuraciones **Recomendadas** para Firewall de Windows en esta tabla poseen valores distintos según la organización ya que cada una posee una lista propia de aplicaciones para las que definir excepciones en Firewall de Windows. Por ello, no resulta factible definir en esta guía una lista de uso universal.
  
###### Conexiones de red\\Firewall de Windows\\Perfil estándar
  
Los valores de esta sección sirven para configurar el Perfil estándar de Firewall de Windows. Este perfil suele ser más restrictivo que el de dominio, en el cual se da por sentado que el entorno del dominio ofrece un mínimo de seguridad. En general, el perfil estándar se usa cuando el equipo se encuentra en una red que no es de confianza, por ejemplo, la red de un hotel o un punto de acceso inalámbrico público. Esos entornos conllevan amenazas desconocidas por lo que exigen medidas de seguridad adicionales.
  
**Nota**   El Perfil estándar sólo se aplica a los equipos con Windows XP. Las recomendaciones siguientes se aplican en exclusiva al entorno EC descrito en la guía para mantener la compatibilidad con Windows XP.
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Red\\Conexiones de red**  
**\\Firewall de Windows\\Perfil estándar**
  
**Tabla A36. Configuración recomendada del perfil estándar de Firewall de Windows**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones ICMP</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepción de administración remota de entrada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de Escritorio remoto de entrada</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de entorno UPnP de entrada</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de puerto local</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: permitir excepciones de programa local</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: definir excepciones de puerto de entrada</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">No se recomienda</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: definir excepciones de programa de entrada</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: no permitir excepciones</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: no permitir notificaciones</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Firewall de Windows: proteger todas las conexiones de red</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
</tbody>
</table>
  
**Nota**   Las configuraciones **Recomendadas** para Firewall de Windows en esta tabla poseen valores distintos según la organización ya que cada una posee una lista propia de aplicaciones para las que definir excepciones en Firewall de Windows. Por ello, no resulta factible definir en esta guía una lista de uso universal.
  
**Firewall de Windows: permitir excepciones ICMP**  
Esta configuración de directiva define el conjunto de tipos de mensajes ICMP (Protocolo de mensajes de control de Internet) que permitirá Firewall de Windows. Las utilidades se sirven de mensajes ICMP para determinar el estado de otros equipos; por ejemplo, la utilidad Ping emplea el mensaje de solicitud de eco.
  
Si establece la configuración **Firewall de Windows: permitir excepciones ICMP** en **Habilitado**, debe especificar qué tipos de mensajes ICMP permite Firewall de Windows que envíe o reciba el equipo. Cuando se establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows bloquea todos los tipos de mensajes ICMP entrantes no solicitados y los tipos de mensajes ICMP salientes enumerados. Como consecuencia de ello, las utilidades que dependen de ICMP pueden no funcionar.
  
Son numerosas las herramientas de ataque que se aprovechan de los equipos que aceptan mensajes ICMP y usan esos mensajes para montar ataques diversos. El problema radica en que algunas aplicaciones necesitan determinados mensajes ICMP para funcionar de manera correcta. Asimismo, los mensajes ICMP se utilizan para calcular el rendimiento de la red cuando se descarga y se procesa Directiva de grupo; si los mensajes ICMP se bloquean, no se puede aplicar Directiva de grupo a los sistemas afectados. Por eso, Microsoft recomienda establecer la configuración **Firewall de Windows: permitir excepciones ICMP** en **Deshabilitado** siempre que sea posible. Si en su entorno es necesario que algunos mensajes ICMP atraviesen Firewall de Windows, establezca esta configuración de directiva con los tipos de mensajes adecuados.
  
Siempre que el equipo se encuentre en una red que no sea de confianza, la configuración **Firewall de Windows: permitir excepciones ICMP** debe estar establecida en **Deshabilitado**.
  
**Nota**   Si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite la entrada de mensajes ICMP de solicitud de eco (como los enviados por la utilidad Ping) aunque el valor de directiva **Firewall de Windows: permitir excepciones ICMP** esté configurado para bloquearlos. Las configuraciones de directiva que pueden abrir el puerto TCP 445 son **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**, **Firewall de Windows: permitir excepción de administración remota de entrada** y **Firewall de Windows: definir excepciones de puerto de entrada**.
  
**Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**  
Esta configuración de directiva crea una excepción que permite el uso compartido de archivos e impresoras. Configura Firewall de Windows de modo que se abra los puertos UDP 137 y 138 así como los puertos TCP 139 y 445. Si habilita esta configuración de directiva, Firewall de Windows abre dichos puertos con el fin de que el equipo pueda recibir trabajos de impresión y solicitudes de acceso a los archivos compartidos. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes.
  
Si deshabilita la configuración **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**, Firewall de Windows bloquea estos puertos e impide que el equipo comparta archivos e impresoras.
  
Dado que, por lo general, los equipos del entorno en los que se ejecute Windows Vista no comparten archivos ni impresoras, Microsoft recomienda configurar el valor **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada** en **Deshabilitado**.
  
**Nota**   Si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite la entrada de mensajes ICMP de solicitud de eco (como los enviados por la utilidad Ping) aunque el valor de directiva **Firewall de Windows: permitir excepciones ICMP** esté configurado para bloquearlos. Las configuraciones de directiva que pueden abrir el puerto TCP 445 son **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**, **Firewall de Windows: permitir excepción de administración remota de entrada** y **Firewall de Windows: definir excepciones de puerto de entrada**.
  
**Firewall de Windows: permitir excepción de administración remota de entrada**  
Muchas organizaciones se valen de la administración remota de equipos en sus operaciones cotidianas. Sin embargo, algunos ataques aprovechan los puertos que suelen usar los programas de administración remota; Firewall de Windows ayuda a bloquear estos puertos.
  
A fin de otorgar flexibilidad a la administración remota, se ofrece la configuración **Firewall de Windows: permitir excepción de administración remota de entrada**. Si se habilita esta configuración de directiva, el equipo puede recibir mensajes entrantes no solicitados asociados a la administración remota en los puertos TCP 135 y 445. Esta configuración de directiva permite también que Svchost.exe y Lsass.exe reciban mensajes entrantes no solicitados y que los servicios alojados abran otros puertos asignados de forma dinámica (por lo general, en el intervalo que va de 1024 a 1034 aunque puede ser cualquiera de los comprendidos entre el 1024 y el 65535. Si habilita esta configuración de directiva, también debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si establece la configuración **Firewall de Windows: permitir excepción de administración remota de entrada** en **Deshabilitado**, Firewall de Windows no aplica ninguna de las excepciones descritas. La repercusión de establecer esta configuración de directiva como **Deshabilitada** puede ser inaceptable para un gran número de organizaciones, ya que no permite que funcionen muchas herramientas de administración remota ni de detección de puntos vulnerables. Así pues, Microsoft recomienda que sólo las organizaciones más sensibles desde el punto de vista de la seguridad habiliten esta configuración de directiva.
  
Para el perfil de dominio, Microsoft recomienda que la configuración **Firewall de Windows: permitir excepción de administración remota de entrada** se establezca en **Habilitado** en los equipos del entorno EC sólo cuando sea necesario. Al habilitar esta configuración, los equipos del entorno aceptan solicitudes de administración remota del menor número de equipos posible. Para maximizar la protección que ofrece Firewall de Windows, asegúrese de especificar sólo las direcciones IP y las subredes de equipos que se utilizan en la administración remota.
  
Microsoft recomienda que la configuración **Firewall de Windows: permitir excepción de administración remota de entrada** se establezca en **Deshabilitado** en todos los equipos del perfil estándar con objeto de evitar ataques conocidos que aprovechen de forma específica los puertos TCP 135 y 445.
  
**Nota**   Si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite la entrada de mensajes ICMP de solicitud de eco (como los enviados por la utilidad Ping) aunque el valor de directiva **Firewall de Windows: permitir excepciones ICMP** esté configurado para bloquearlos. Las configuraciones de directiva que pueden abrir el puerto TCP 445 son **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**, **Firewall de Windows: permitir excepción de administración remota de entrada** y **Firewall de Windows: definir excepciones de puerto de entrada**.
  
**Firewall de Windows: permitir excepciones de Escritorio remoto de entrada**  
Muchas organizaciones usan conexiones de Escritorio remoto en sus procedimientos u operaciones normales para la solución de problemas. Sin embargo, en algunos ataques se han aprovechado los puertos que suele utilizar Escritorio remoto.
  
A fin de otorgar flexibilidad a la administración remota, se ofrece la configuración **Firewall de Windows: permitir excepciones de Escritorio remoto** **de entrada**. Si habilita esta configuración de directiva, Firewall de Windows abre el puerto TCP 3389 para las conexiones entrantes. También debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes.
  
Si deshabilita esta configuración de directiva, Firewall de Windows bloquea este puerto e impide que el equipo reciba solicitudes de Escritorio remoto. Si un administrador agrega este puerto a una lista de excepciones de puerto local para intentar abrirlo, Firewall de Windows no abre el puerto.
  
Para mantener las capacidades de administración mejorada que proporciona Escritorio remoto, debe establecer esta configuración de directiva como **Habilitada** para el entorno EC. Tiene que especificar las direcciones IP y las subredes de los equipos que se utilizan para la administración remota. Los equipos del entorno aceptan solicitudes de Escritorio remoto del menor número de equipos posible.
  
**Firewall de Windows: permitir excepciones de entorno UPnP de entrada**  
Esta configuración de directiva permite a un equipo recibir mensajes Plug and Play no solicitados que envían dispositivos de red tales como enrutadores con servidores de seguridad integrados. A fin de recibir estos mensajes, Firewall de Windows abre el puerto TCP 2869 y el puerto UDP 1900.
  
Si habilita la configuración **Firewall de Windows: permitir excepciones de entorno UPnP de entrada**, Firewall de Windows abre esos puertos para que el equipo reciba mensajes Plug and Play. Debe especificar las direcciones IP o las subredes desde las que se permiten estos mensajes entrantes. Si deshabilita esta configuración de directiva, Firewall de Windows bloquea estos puertos e impide que el equipo reciba mensajes Plug and Play.
  
El bloqueo del tráfico de red UPnP reduce de forma eficaz la superficie de ataque de los equipos del entorno. En redes de confianza, Microsoft recomienda establecer la configuración **Firewall de Windows: permitir excepciones de entorno UPnP de entrada** en **Deshabilitado** a menos que use dispositivos UPnP en la red. Esta configuración de directiva siempre debe estar **Deshabilitada** para redes que no son de confianza.
  
**Firewall de Windows: permitir excepciones de puerto local**  
Esta configuración de directiva permite a los administradores usar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de puerto local. Firewall de Windows puede usar dos listas de excepciones de puerto; la otra se define mediante **Firewall de Windows: definir excepciones de puerto**.
  
Si habilita la configuración **Firewall de Windows: permitir excepciones de puerto local**, el componente Firewall de Windows del Panel de control permite a los administradores definir una lista de excepciones de puertos locales. Al deshabilitar esta configuración de directiva, se garantiza que el componente Firewall de Windows del Panel de control impida a los administradores definir esa lista.
  
En general, los administradores locales no están autorizados para anular las directivas organizativas y establecer sus propias listas de excepciones de puertos. Por eso, Microsoft recomienda que la configuración **Firewall de Windows: permitir excepciones de puerto local** se establezca en **Deshabilitado**.
  
**Firewall de Windows: permitir excepciones de programa local**  
Esta configuración de directiva controla si los administradores pueden usar el componente del Panel de control Firewall de Windows para definir una lista de excepciones de programa local. Si deshabilita esta configuración de directiva, los administradores no podrán definir una lista de excepciones de programa local; asimismo, esta configuración garantiza que esas excepciones de programa sólo procedan de la Directiva de grupo. Si se habilita esta configuración de directiva, los administradores locales podrán utilizar el Panel de control para definir excepciones de programa localmente.
  
Para equipos cliente de empresa, es posible que existan condiciones que justifiquen excepciones de programa de ámbito local. Estas condiciones pueden incluir aplicaciones que no se analizaron cuando se creó la directiva de firewall de la organización o aplicaciones nuevas que requieren una configuración de puertos no estándar. Si opta por habilitar la configuración **Firewall de Windows: permitir excepciones de programa local** para esas situaciones, recuerde que la superficie de ataque de los equipos afectados se incrementa.
  
**Firewall de Windows: definir excepciones de puerto de entrada**  
La directiva de grupo debe definir la lista de excepciones de puertos de Firewall de Windows; de este modo, puede administrar e implementar con acciones centralizadas las excepciones de puertos y, al mismo tiempo, garantizar que los administradores locales no creen ninguna configuración menos segura.
  
Si habilita la configuración **Firewall de Windows: definir excepciones de puerto de entrada**, puede ver y cambiar la lista de excepciones de puertos que define la directiva de grupo. Para ver y modificar la lista de excepciones de puerto, configure el parámetro como **Habilitado** y haga clic en el botón **Mostrar**. Tenga en cuenta que si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores, lo que significa que puede crear accidentalmente varias entradas para el mismo puerto y que entren en conflicto los valores de Ámbito o Estado.
  
Si deshabilita la configuración **Firewall de Windows: definir excepciones de puerto de entrada**, la lista de excepciones de puertos que define la directiva de grupo se elimina pero es posible que otros valores de configuración sigan abriendo o bloqueando puertos. Asimismo, si existe una lista de excepciones de puerto local, se pasa por alto a menos que habilite la configuración **Firewall de Windows: permitir excepciones de puerto local**.
  
Para los entornos con aplicaciones no estándar que requieren que se abran determinados puertos debe considerarse la posibilidad de implementar excepciones de programa, en lugar de excepciones de puerto. Microsoft recomienda que la configuración **Firewall de Windows: definir excepciones de puerto de entrada** se establezca en **Habilitado** y que especifique una lista de excepciones de puertos sólo cuando no se puedan definir excepciones de programas. Las excepciones de programas permiten a Firewall de Windows aceptar tráfico de red no solicitado siempre y cuando el programa especificado se encuentre en ejecución a diferencia de las excepciones de puertos, que mantienen los puertos indicados abiertos en todo momento.
  
**Nota**   Si alguna configuración de directiva abre el puerto TCP 445, Firewall de Windows permite la entrada de mensajes ICMP de solicitud de eco (como los enviados por la utilidad Ping) aunque el valor de directiva **Firewall de Windows: permitir excepciones ICMP** esté configurado para bloquearlos. Las configuraciones de directiva que pueden abrir el puerto TCP 445 son **Firewall de Windows: permitir la excepción Compartir impresoras y archivos de entrada**, **Firewall de Windows: permitir excepción de administración remota de entrada** y **Firewall de Windows: definir excepciones de puerto de entrada**.
  
**Firewall de Windows: definir excepciones de programa de entrada**  
Es posible que algunas aplicaciones necesiten abrir y utilizar puertos de red que no suele permitir Firewall de Windows. La configuración **Firewall de Windows: definir excepciones de programa de entrada** permite ver y cambiar la lista de excepciones de programas que define la directiva de grupo.
  
Si esta configuración de directiva está **Habilitada**, puede ver y cambiar la lista de excepciones de programa. Si agrega un programa a esta lista y establece su estado como **Habilitado**, ese programa podrá recibir mensajes entrantes no solicitados en cualquier puerto que solicite a Firewall de Windows que se abra, aunque dicho puerto esté bloqueado por otro parámetro. Si establece esta configuración de directiva como **Deshabilitada**, se elimina la lista de excepciones de programa que ha definido Directiva de grupo.
  
**Nota**   Si escribe una cadena de definición no válida, Firewall de Windows la agrega a la lista sin comprobar si contiene errores. Como la entrada no se comprueba, puede agregar programas que aún no tenga instalados. También es posible crear accidentalmente varias excepciones para el mismo programa y que entren en conflicto los valores de Ámbito o Estado.
  
**Firewall de Windows: no permitir excepciones**  
Esta configuración de directiva provocó que Firewall de Windows bloqueara todos los mensajes entrantes no solicitados. Anula todos los demás parámetros de Firewall de Windows que permitan dichos mensajes. Si habilita esta configuración de directiva en el elemento Firewall de Windows del Panel de control, se activa la casilla de verificación **No permitir excepciones** y ni siquiera los administradores pueden desactivarla.
  
Muchos entornos cuentan con aplicaciones y servicios que han de tener permiso para recibir comunicaciones entrantes no solicitadas como parte de su funcionamiento normal. En dichos entornos, configure el valor **Firewall de Windows: no permitir excepciones** en **Deshabilitado** para permitir que esas aplicaciones y esos servicios se ejecuten sin problemas. No obstante, antes de establecer esta configuración de directiva, debe probar el entorno para determinar con exactitud qué comunicaciones deben permitirse.
  
**Nota**   Esta configuración de directiva proporciona una sólida defensa frente a atacantes externos y debe establecerse en **Habilitado** en situaciones en las que se necesite una protección completa frente a ataques desde el exterior tales como gusanos nuevos en la red. Si establece esta configuración de directiva como **Deshabilitada**, Firewall de Windows podrá aplicar otros parámetros de configuración de directiva que permitan mensajes entrantes no solicitados.
  
**Firewall de Windows: no permitir notificaciones**  
Firewall de Windows puede mostrar notificaciones a los usuarios cada vez que algún programa le solicite que lo agregue a la lista de excepciones de programas. Esta situación se produce cuando los programas intentan abrir un puerto y no se les permite debido a las reglas actuales de Firewall de Windows.
  
La configuración **Firewall de Windows: no permitir notificaciones** determina si se muestran dichos mensajes a los usuarios. Si establece esta configuración de directiva como **Habilitada**, Firewall de Windows impide que se muestren estas notificaciones. Si se establece como **Deshabilitada**, Firewall de Windows permite que se muestren estas notificaciones.
  
**Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión**  
Esta configuración de directiva ayuda a impedir que un equipo reciba respuestas de unidifusión a sus mensajes salientes de difusión o multidifusión. Cuando esta configuración de directiva está habilitada y el equipo envía mensajes de difusión o multidifusión a otros equipos, Firewall de Windows bloquea las respuestas de monodifusión que envían esos otros equipos. Cuando esta configuración de directiva está deshabilitada y el equipo envía un mensaje de difusión o multidifusión a otros equipos, Firewall de Windows espera hasta tres segundos respuestas de monodifusión de los demás equipos y después bloquea todas las respuestas posteriores.
  
Por norma general, no se desea recibir respuestas de unidifusión a mensajes de difusión o multidifusión. Tales respuestas pueden indicar un ataque de denegación de servicio (DoS) o un intento de sondear un equipo activo conocido. Microsoft recomienda que la configuración **Firewall de Windows: no permitir respuesta de monodifusión a peticiones de difusión o multidifusión** se establezca en **Habilitado** para ayudar a prevenir este tipo de ataques.
  
**Nota**   Esta configuración de directiva no surte efecto si el mensaje de unidifusión es la respuesta a un mensaje de difusión DHCP enviado por el equipo. Firewall de Windows siempre admite las respuestas DHCP. Sin embargo, esta configuración de directiva puede interferir en los mensajes NetBIOS que detecten conflictos de nombres.
  
**Firewall de Windows: proteger todas las conexiones de red**  
Esta configuración de directiva habilita Firewall de Windows, el cual reemplaza al Servidor de seguridad de conexión a Internet en todos los equipos en los que se ejecute Windows Vista. En esta guía se recomienda que establezca esta configuración de directiva como **Habilitada** con el fin de proteger las conexiones de red de los equipos en todos los entornos que se tratan en esta guía.
  
Si **Firewall de Windows: proteger todas las conexiones de red** se configura como **Deshabilitado**, se desactiva Firewall de Windows y se omiten todos sus otros valores.
  
**Nota**   Si habilita esta configuración de directiva, se ejecuta Firewall de Windows y se omite el valor de **Configuración del equipo\\Plantillas administrativas\\Red\\Conexiones de red**  
**\\Prohibir el uso de Servidor de seguridad de conexión a Internet en su red de dominio DNS**.
  
##### Sistema
  
En Configuración del equipo\\Plantillas administrativas\\Sistema se configuran estas otras secciones:
  
-   [Inicio de sesión](#_logon)
  
-   [Directiva de grupo](#_group_policy)
  
-   [Asistencia remota](#_remote_assistance)
  
-   [Llamada a procedimiento remoto](#_remote_procedure_call)
  
-   [Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet](#_internet_communication_management--)
  
###### Inicio de sesión
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Inicio de sesión**
  
La tabla siguiente resume la configuración recomendada de inicio de sesión. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A37. Configuración recomendada de inicio de sesión**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No procesar la lista de ejecución heredada</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No procesar la lista de una sola ejecución</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No procesar la lista de ejecución heredada**  
Esta configuración de directiva hace que se pase por alto la lista de ejecución, que es la lista de programas que Windows Vista ejecuta de manera automática cuando se inicia. Las listas de ejecución personalizadas de Windows Vista se almacenan en las siguientes ubicaciones del Registro:
  
-   **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**
  
-   **HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run**
  
Habilite la configuración **No procesar la lista de ejecución heredada** para impedir que, cada vez que Windows Vista se inicie, un usuario malintencionado ejecute algún programa que ponga en peligro los datos del equipo o cause otros daños. Cuando esta configuración de directiva se habilita, evita que determinados programas de sistema se ejecuten, como el software antivirus, así como la distribución de software y el software de supervisión. Microsoft le recomienda que evalúe el nivel de amenaza en el entorno antes de determinar si se debe usar esta configuración de directiva en su organización.
  
La configuración **No procesar la lista de ejecución heredada** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**No procesar la lista de una sola ejecución**  
Esta configuración de directiva hace que se pase por alto la lista de una sola ejecución, que es la lista de programas que Windows Vista ejecuta de manera automática cuando se inicia. Esta configuración de directiva difiere de **No procesar la lista de ejecución heredada** en que los programas de la lista se ejecutarán una sola vez cuando se reinicie el equipo cliente. A veces se agregan a esta lista programas de configuración e instalación para finalizar las instalaciones después de que un equipo cliente se reinicie. Si habilita esta configuración de directiva, en general, los atacantes no pueden usar la lista de una sola ejecución para iniciar aplicaciones malintencionadas, lo cual era un método común de ataque en el pasado. Un usuario malintencionado puede aprovechar la lista de una sola ejecución para instalar programas que entrañen riesgos para la seguridad de los equipos cliente basados en Windows Vista.
  
**Nota**   Las listas personalizadas de una sola ejecución se almacenan en la ubicación siguiente del Registro: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.
  
El parámetro **No procesar la lista de una sola ejecución** debe causar una pérdida mínima de funcionalidad a los usuarios de su entorno, especialmente si los equipos cliente se han configurado con todo el software estándar de la organización antes de que esta configuración de directiva se aplique a través de Directiva de grupo. La configuración **No procesar la lista de una sola ejecución** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
###### Directiva de grupo
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Directiva de grupo**
  
**Tabla A38. Configuración recomendada de la directiva de grupo**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesamiento de directivas de Registro</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesamiento de directivas de Registro**  
Esta configuración de directiva determina cuándo se actualizan las directivas de Registro. Afecta a todas las directivas de la carpeta Plantillas administrativas y a cualquier otra directiva que almacene valores en el Registro. Si esta configuración de directiva se habilita, están disponibles las opciones siguientes:
  
-   **No aplicar durante el procesamiento periódico en segundo plano.**
  
-   **Procesar incluso si los objetos de directiva de grupo no han cambiado.**
  
Algunas configuraciones que se establecen mediante las plantillas administrativas se realizan en áreas del Registro accesibles para los usuarios. Los cambios realizados en estos parámetros por los usuarios se sobrescribirán si se habilita esta configuración de directiva.
  
El valor **Procesamiento de directivas de Registro** se configura como **Habilitado** en los dos entornos que se tratan en esta guía.
  
###### Asistencia remota
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Asistencia remota**
  
La tabla siguiente resume la configuración recomendada de Asistencia remota. En las subsecciones que siguen se amplía la información acerca de cada configuración.
  
**Tabla A39. Configuración recomendada de Asistencia remota**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Ofrecer Asistencia remota</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Asistencia remota solicitada</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Ofrecer Asistencia remota**  
Esta configuración de directiva determina si un empleado de soporte técnico o un administrador de TI “experto” puede ofrecer asistencia remota a los equipos del entorno sin que el usuario lo solicite de manera explícita a través de un canal como el correo electrónico o la mensajería instantánea.
  
**Nota**   El experto no puede conectarse al equipo sin avisar ni controlarlo sin permiso del usuario. Cuando el experto intente conectarse, el usuario podrá optar por rechazar la conexión o proporcionar al experto privilegios de sólo vista. El usuario debe hacer clic explícitamente en el botón **Sí** para permitir que el experto controle remotamente la estación de trabajo, después de establecer el parámetro **Ofrecer asistencia remota** como **Habilitado**.
  
Si esta configuración de directiva se habilita, están disponibles las opciones siguientes:
  
-   **Sólo permitirles ver el equipo**
  
-   **Permitirles controlar el equipo**
  
Al establecer esta configuración de directiva también puede especificar una lista de usuarios o grupos de usuarios conocidos como "servicios de ayuda" que pueden ofrecer asistencia remota.
  
**Para configurar la lista de servicios de ayuda**
  
1.  En la ventana de configuración del parámetro **Ofrecer asistencia remota**, haga clic en **Mostrar**. Aparecerá una ventana nueva en la que puede introducir los nombres de los servicios de ayuda.
  
2.  Agregue cada usuario o grupo a la lista de **servicios de ayuda** en uno de los siguientes formatos:
  
    -   *&lt;Nombre de dominio&gt;*\\*&lt;Nombre de usuario&gt;*
  
    -   *&lt;Nombre de dominio&gt;*\\*&lt;Nombre de grupo&gt;*
  
Si esta configuración de directiva se deshabilita o no está configurada, los usuarios y los grupos no podrán ofrecer asistencia remota no solicitada a los usuarios del entorno.
  
La configuración **Ofrecer Asistencia remota** se establece en **Sin configurar** en el entorno EC. Sin embargo, se establece en **Deshabilitado** en el entorno SSLF con el fin de evitar el acceso a equipos cliente de Windows Vista por la red.
  
**Asistencia remota solicitada**  
Esta configuración de directiva determina si se puede solicitar asistencia remota desde los equipos con Windows Vista del entorno. Tiene la posibilidad de habilitar esta configuración de directiva para que los usuarios puedan solicitar asistencia remota a administradores de TI "expertos".
  
**Nota**   Los expertos no pueden conectarse al equipo sin avisar ni controlarlo sin permiso del usuario. Cuando el experto intente conectarse, el usuario podrá optar por rechazar la conexión o proporcionar al experto privilegios de sólo vista. El usuario debe hacer clic en el botón **Sí** para permitir que el experto controle de forma remota la estación de trabajo.
  
Si se habilita la configuración **Asistencia remota solicitada**, están disponibles las opciones siguientes:
  
-   **Permitirles controlar el equipo**
  
-   **Sólo permitirles ver el equipo**
  
Asimismo, las siguientes opciones están disponibles para configurar cuánto tiempo se mantiene la validez de una solicitud de ayuda de un usuario:
  
-   **Validez máxima del vale (valores)**
  
-   **Validez máxima del vale (unidades): horas,** **minutos o días**
  
Cuando un vale (solicitud de ayuda) caduca, el usuario debe enviar otra solicitud para que un experto pueda conectarse al equipo. Si deshabilita la configuración **Asistencia remota solicitada**, los usuarios no pueden enviar solicitudes de ayuda ni el experto puede conectarse a los equipos.
  
Si no se configura **Asistencia remota solicitada**, los usuarios pueden configurar este valor en el Panel de control. En el Panel de control se encuentran habilitadas de forma predeterminada las configuraciones de **asistencia remota solicitada**, **Buddy support** y **control remoto**. El valor de **Validez máxima del vale** se establece en **30 días**. Si esta configuración de directiva se deshabilita, nadie puede tener acceso a los equipos cliente con Windows Vista a través de la red.
  
La configuración **Asistencia remota solicitada** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
###### Llamada a procedimiento remoto
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Sistema\\Llamada a procedimiento remoto**
  
La tabla siguiente resume la configuración recomendada de Llamada a procedimiento remoto. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A40. Configuración recomendada de Llamada a procedimiento remoto**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Restricciones para clientes RPC no autenticados</td>
<td style="border:1px solid black;">Habilitado: autenticado</td>
<td style="border:1px solid black;">Habilitado: autenticado</td>
<td style="border:1px solid black;">Habilitado: autenticado</td>
<td style="border:1px solid black;">Habilitado: autenticado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Autenticación de clientes del Asignador de extremos de RPC</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Restricciones para clientes RPC no autenticados**  
Esta configuración de directiva establece el Tiempo de ejecución de RPC en un servidor RPC para limitar la conexión de clientes RPC no autenticados al servidor RPC. Se considera que un cliente está autenticado si usa alguna canalización con nombre para comunicarse con el servidor o si emplea seguridad RPC. Las interfaces RPC cuyo acceso solicitan de forma explícita los clientes no autenticados se pueden eximir de esta restricción en función del valor seleccionado para esta directiva. Si habilita esta configuración de directiva, están disponibles los siguientes valores:
  
-   **Ninguno**. Permite a todos los clientes RPC conectarse a servidores RPC que se ejecutan en el equipo en el cual se aplica la directiva.
  
-   **Autenticado**. Sólo permite a los clientes RPC autenticados conectarse a servidores RPC que se ejecuten en el equipo en que se aplique la directiva. Se otorga la exención a las interfaces que pidan eximirse de esta restricción.
  
-   **Autenticado sin excepciones**. Sólo permite a los clientes RPC autenticados conectarse a servidores RPC que se ejecuten en el equipo en que se aplique la directiva. No se consiente excepción alguna.
  
Dado que la comunicación RPC sin autenticación puede crear un punto vulnerable de seguridad, el valor **Restricciones para clientes RPC no autenticados** se configura como **Habilitado** y el valor **Restricción de clientes sin autenticar del tiempo de ejecución RPC que desea aplicar** se establece en **Autenticado** en los dos entornos que se describen en esta guía.
  
**Nota**   Las aplicaciones RPC que no autentican solicitudes de conexión de entrada no solicitadas pueden no funcionar correctamente cuando se aplica esta configuración. Asegúrese de probar las aplicaciones antes de implementar esta configuración de directiva en el entorno. Aunque el valor Autenticado para esta configuración de directiva no sea completamente seguro, puede resultar útil por lo que respecta a la compatibilidad de las aplicaciones en su entorno.
  
**Autenticación de clientes del Asignador de extremos de RPC**  
Si habilita esta configuración de directiva, se exigirá a los equipos cliente que se comunican con este equipo que proporcionen autenticación antes de que se establezca una comunicación RPC. De forma predeterminada, los clientes RPC no utilizarán la autenticación para comunicarse con el Servicio de asignador de extremos cuando solicitan el extremo de un servidor. Sin embargo, esta configuración predeterminada se cambió para el entorno SSLF a fin de requerir la autenticación de los equipos cliente antes de que se permita una comunicación RPC.
  
###### Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet
  
El grupo Configuración de comunicaciones de Internet dispone de varios valores de configuración. En esta guía se recomienda la restricción de muchas de estas configuraciones, sobre todo para ayudar a aumentar el nivel de confidencialidad de los datos en los sistemas informáticos. Si no se restringen estos valores, los atacantes podrían interceptar la información y usarla a su antojo. Aunque las probabilidades de que se produzca hoy este tipo de ataque son escasas, una configuración adecuada de estos parámetros ayudará a proteger su entorno contra futuros ataques.
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet**
  
La tabla siguiente resume la configuración recomendada de las comunicaciones de Internet. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A41. Configuración recomendada de comunicaciones de Internet**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la tarea “Publicar en Web” para archivos y carpetas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar la actualización de archivos de contenido del Asistente para búsqueda</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar impresión a través de HTTP</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Desactivar la descarga de controladores de impresión a través de HTTP</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la búsqueda de controladores de dispositivo en Windows Update</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Desactivar la tarea “Publicar en Web” para archivos y carpetas**  
Esta configuración de directiva especifica si las tareas **Publicar este archivo en Web**, **Publicar esta carpeta en Web** y **Publicar los elementos seleccionados en Web** están disponibles en las Tareas de archivo y carpeta en las carpetas de Windows. El Asistente para la publicación en Web se usa para descargar una lista de proveedores y permite que los usuarios publiquen contenido en Web.
  
Si configura el valor **Desactivar la tarea “Publicar en Web” para archivos y carpetas** como **Habilitado**, estas opciones se quitan de Tareas de archivo y carpeta en las carpetas de Windows. De forma predeterminada, la opción de publicar en Web está disponible. Dado que esta capacidad se podría utilizar para exponer contenido protegido ante un equipo cliente Web no autenticado, esta configuración de directiva se configura como **Habilitada** para los entornos EC y SSLF.
  
**Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea**  
Esta configuración de directiva controla si Windows descargará una lista de proveedores de los asistentes para la publicación en Web y para pedidos en línea. Si esta configuración de directiva se habilita, se evita que Windows descargue proveedores; sólo se muestran los proveedores de servicios almacenados en caché en el Registro local.
  
Dado que la configuración **Desactivar** **la tarea “Publicar en Web” para archivos y carpetas** se habilita en los entornos EC y SSLF (consulte la sección anterior), esta opción no se necesita. Sin embargo, el parámetro **Desactivar descargas de Internet en los asistentes para la publicación en Web y para pedidos en línea** se configura como **Habilitado** para minimizar la superficie de ataque de los equipos cliente y para asegurar que esta capacidad no se pueda aprovechar de otras maneras.
  
**Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger**  
Esta configuración de directiva especifica si Windows Messenger puede recopilar información anónima acerca del uso del servicio y del software Windows Messenger. Puede habilitar esta configuración de directiva para asegurarse de que Windows Messenger no recopila información de uso y para evitar que se muestren parámetros de configuración de usuario que posibiliten la recopilación de información de uso.
  
En muchos entornos de grandes empresas quizá no sea deseable la recopilación de información de los equipos cliente administrados. El valor **Desactivar el Programa para la mejora de la experiencia del cliente de Windows Messenger** se configura como **Habilitado** en los dos entornos que se describen en esta guía a fin de evitar que se recopile información.
  
**Desactivar la actualización de archivos de contenido del Asistente para búsqueda**  
Esta configuración de directiva especifica si el Asistente para búsqueda debe descargar automáticamente actualizaciones de contenido durante las búsquedas locales y en Internet. Si establece esta configuración de directiva como **Habilitada**, evitará que el Asistente para búsqueda descargue actualizaciones de contenido durante las búsquedas.
  
El parámetro **Desactivar la actualización de archivos de contenido del Asistente para búsqueda** se configura como **Habilitado** para los entornos EC y SSLF con objeto de controlar comunicaciones de red innecesarias desde cada equipo cliente administrado.
  
**Nota**   Las búsquedas en Internet siguen enviando el texto de la búsqueda e información acerca de la búsqueda a Microsoft y al proveedor de búsqueda elegido. Si selecciona Búsqueda clásica, la característica de Asistente para búsqueda no estará disponible. Puede seleccionar la búsqueda clásica si hace clic en **Inicio**, **Buscar**, **Cambiar preferencias** y, a continuación, en **Cambiar el comportamiento de búsqueda en Internet**.
  
**Desactivar impresión a través de HTTP**  
Mediante esta configuración de directiva es posible deshabilitar la capacidad del equipo cliente de imprimir a través de HTTP, que permite al equipo imprimir con impresoras de la intranet y de Internet. Si habilita esta configuración de directiva, el equipo cliente no podrá imprimir con impresoras de Internet a través de HTTP.
  
La información que se transmite a través de HTTP mediante esta capacidad no se protege y puede ser interceptada por usuarios malintencionados. Por eso se utiliza pocas veces en entornos de empresa. El parámetro **Desactivar impresión a través de HTTP** se configura como **Habilitado** para los entornos EC y SSLF como medida para evitar una posible infracción de la seguridad a través de un trabajo de impresión inseguro.
  
**Nota**   Esta configuración de directiva afecta en exclusiva a los clientes de impresión de Internet. Independientemente de cómo se configura, un equipo podría actuar como servidor de impresión de Internet y hacer que sus impresoras compartidas estén disponibles a través de HTTP.
  
**Desactivar la descarga de controladores de impresión a través de HTTP**  
Esta configuración de directiva controla si el equipo puede descargar paquetes de controladores de impresión a través de HTTP. Para configurar la impresión HTTP, quizá sea necesario descargar a través de HTTP los controladores de impresión que no están disponibles en la instalación del sistema operativo estándar.
  
El parámetro **Desactivar la descarga de controladores de impresión a través de HTTP** se configura como **Habilitado** para evitar que se descarguen controladores de impresión a través de HTTP.
  
**Nota**   Esta configuración de directiva no impide que el equipo cliente use impresoras de la intranet o de Internet por HTTP. Sólo desautoriza la descarga de controladores que no se encuentren instalados ya en una ubicación local.
  
**Desactivar la búsqueda de controladores de dispositivo en Windows Update**  
Esta configuración de directiva especifica si Windows deberá buscar mediante Windows Update controladores de dispositivo cuando no se encuentren localmente.
  
Dado que existe un cierto grado de riesgo al descargar controladores de dispositivo de Internet, el parámetro **Desactivar la búsqueda de controladores de dispositivo en Windows Update** se configura como **Habilitado** para el entorno SSLF y como **Deshabilitado** para el entorno EC. El motivo de esta configuración es que, normalmente, los tipos de ataques que pueden aprovechar descargas de controladores se reducirán mediante una administración apropiada de los recursos de la empresa y las configuraciones. Además, así se asegura la compatibilidad y la estabilidad en todos los equipos del entorno.
  
**Nota**   Consulte también la configuración **Desactivar la intervención del usuario en búsquedas de controladores de dispositivo en Windows Update** de **Plantillas administrativas/Sistema**, que indica si se pregunta al administrador antes de buscar en Windows Update controladores de dispositivo que no se encuentren en ninguna ubicación local.
  
##### Componentes de Windows
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**
  
En la sección Plantillas administrativas\\Componentes de Windows se configuran los valores siguientes:
  
-   [Directivas de reproducción automática](#_autoplay_policies)
  
-   [Interfaz de usuario de credenciales](#_credential_user_interface)
  
-   [Internet Explorer](#_internet_explorer_2)
  
-   [NetMeeting](#_netmeeting)
  
-   [Servicios de Terminal Server](#_terminal_services)
  
-   [Windows Messenger](#_windows_messenger)
  
-   [Windows Update](#_windows_update)
  
###### Directivas de reproducción automática
  
Reproducción automática es una característica de Windows que permite abrir o iniciar de manera automática archivos multimedia o programas de instalación en cuanto los detecta el equipo. Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Directivas de reproducción automática**
  
**Tabla A42. Configuración recomendada de reproducción automática**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar reproducción automática</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado:<br />
todas las unidades</td>
<td style="border:1px solid black;">Habilitado:<br />
todas las unidades</td>
</tr>
</tbody>
</table>
 

**Desactivar reproducción automática**
Reproducción automática inicia la lectura desde una unidad en cuanto inserte el medio en la misma, lo que provoca el inicio inmediato del archivo de configuración de programas y medios de audio. Un atacante podría utilizar esta característica para iniciar un programa capaz de dañar el equipo o los datos que contiene. Puede habilitar el parámetro **Desactivar reproducción automática** para deshabilitar la característica de reproducción automática. La característica Reproducción automática está deshabilitada de forma predeterminada en algunos tipos de unidades extraíbles, como la unidad de disquete y de red, pero no en las unidades de CD-ROM.

La configuración **Desactivar reproducción automática** se establece en **Sin configurar** en el entorno EC y en **Habilitado: todas las unidades** sólo en el entorno SSLF.

**Nota**   No puede usar esta configuración de directiva para habilitar Reproducción automática en las unidades del equipo en las que esté deshabilitada de forma predeterminada como los disquetes y las unidades de red.

###### Interfaz de usuario de credenciales

Esta configuración controla la interfaz que ven los usuarios cuando se les pide que suministren su nombre de cuenta y su contraseña a la hora de autorizar la elevación para tareas que requieren una aprobación mediante el escritorio seguro. Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Interfaz de usuario de credenciales**

**Tabla A43. Configuración recomendada de la interfaz de usuario de credenciales de UAC**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Enumerate administrator accounts on elevation (Enumerar cuentas de administrador para la elevación)</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Require trusted path for credential entry (Requerir ruta de confianza para la entrada de credenciales)</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones de la directiva de grupo nuevas en Windows Vista.
  
**Enumerate administrator accounts on elevation (Enumerar cuentas de administrador para la elevación)**  
De forma predeterminada, se muestran todas las cuentas de administrador cada vez que se intenta elevar una aplicación en ejecución. Si habilita esta directiva, los usuarios deben escribir siempre un nombre de usuario y una contraseña para proceder a la elevación. Si la deshabilita, aparecen todas las cuentas de administrador local disponibles en el equipo para que el usuario elija una y escriba la contraseña correcta.
  
La configuración **Enumerate administrator accounts on elevation (Enumerar cuentas de administrador para la elevación)** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** sólo en el entorno SSLF.
  
**Require trusted path for credential entry (Requerir ruta de confianza para la entrada de credenciales)**  
Si habilita esta configuración de directiva, los usuarios deben escribir sus credenciales de Windows en el escritorio seguro por medio de un mecanismo de ruta de confianza. Ello significa que, antes de escribir la cuenta y la contraseña a fin de autorizar la solicitud de elevación, el usuario ha de presionar Ctrl+Alt+Supr. Al exigir el uso de una ruta de confianza, se impide que caballos de Troya u otros tipos de código malintencionado roben las credenciales de Windows del usuario.
  
Si deshabilita esta configuración de directiva o no la establece, los usuarios escriben sus credenciales de Windows durante la sesión de escritorio lo que, en potencia, podría permitir el acceso de código malintencionado a ellas.
  
La configuración **Require trusted path for credential entry setting (Requerir ruta de confianza para la entrada de credenciales)** se establece en **Sin configurar** en el entorno EC y en **Habilitado** sólo en el entorno SSLF.
  
###### Internet Explorer
  
La directiva de grupo de Microsoft Internet Explorer® ayuda a cumplir los requisitos de seguridad de los equipos con Windows Vista, así como a evitar el intercambio de contenido no deseado a través de Internet Explorer. Aplique los criterios siguientes a fin de asegurar Internet Explorer en las estaciones de trabajo del entorno:
  
-   Asegúrese de que las peticiones a Internet sólo se producen como respuesta directa a acciones del usuario.
  
-   Asegúrese de que la información enviada a sitios Web específicos sólo llega a los mismos, a menos que se produzcan acciones concretas del usuario que permiten la transmisión de información a otros destinos.
  
-   Asegúrese de que los canales de confianza a servidores o sitios están identificados con toda claridad junto con el propietario de los mismos en cada canal.
  
-   Asegúrese de que toda secuencia de comandos o programa que se ejecute con Internet Explorer lo haga en un entorno restringido. Puede ser que los programas enviados a través de canales de confianza estén habilitados para funcionar fuera del entorno restringido.
  
**Importante**   Asegúrese de que Internet Explorer esté configurado de manera correcta para obtener acceso a Internet antes de aplicar los GPO incluidos con esta guía. Muchos entornos requieren una configuración de proxy concreta para que el acceso a Internet sea adecuado. La configuración recomendada en esta guía impide a los usuarios cambiar la configuración de los valores de proxy de Internet Explorer.
  
Establezca la configuración recomendada de Internet Explorer para los equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**
  
En la tabla siguiente se resumen muchas de las recomendaciones sobre la configuración de Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A44. Configuración recomendada de Internet Explorer**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la instalación automática de componentes de Internet Explorer</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir que usuarios habiliten ni deshabiliten complementos</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configuración de proxy por equipo y no por usuario</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zonas de seguridad: no permitir que los usuarios cambien las directivas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zonas de seguridad: usar sólo la configuración del equipo</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Desactivar la detección de bloqueos</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Deshabilitar la instalación automática de componentes de Internet Explorer**  
Si habilita esta configuración de directiva, Internet Explorer no podrá descargar componentes cuando los usuarios exploren sitios Web que requieran los componentes para funcionar completamente. Si esta configuración de directiva se deshabilita o no está configurada, se preguntará a los usuarios si desean descargar e instalar los componentes cada vez que visiten sitios Web que los utilicen.
  
El valor **Deshabilitar la instalación automática de componentes de Internet Explorer** se configura como **Habilitado** en los dos entornos que se tratan en el apéndice.
  
**Nota**   Antes de habilitar esta configuración de directiva, Microsoft recomienda que configure una estrategia alternativa para actualizar Internet Explorer con Microsoft Update o un servicio semejante.
  
**Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer**  
Si habilita esta configuración de directiva, Internet Explorer no podrá determinar si hay disponible una versión posterior del explorador y avisar a los usuarios en ese caso. Si esta configuración de directiva se deshabilita o no está configurada, Internet Explorer busca actualizaciones cada 30 días (su configuración predeterminada) y avisa a los usuarios si hay una versión nueva disponible.
  
El valor **Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Antes de habilitar esta configuración de directiva, Microsoft recomienda que configure una estrategia alternativa para los administradores de su organización con el fin de asegurar que acepten cada cierto tiempo las actualizaciones nuevas de Internet Explorer en los equipos cliente del entorno.
  
**Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa**  
Esta configuración de directiva especifica que los programas que utilizan los canales de distribución de software de Microsoft no avisarán a los usuarios cuando instalen nuevos componentes. Los canales de distribución de software se utilizan para actualizar el software dinámicamente en los equipos de los usuarios; esta funcionalidad se basa en tecnologías de distribución abierta de software (OSD).
  
El valor **Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa** se configura como **Habilitado** en los dos entornos que se tratan en esta guía.
  
**No permitir que usuarios habiliten ni deshabiliten complementos**  
Esta configuración de directiva le permite administrar si los usuarios tienen la capacidad de permitir o denegar complementos a través de Administrar complementos. Si se establece esta configuración de directiva como **Habilitado**, los usuarios no podrán habilitar ni deshabilitar los complementos a través de la característica Administrar complementos. La única excepción se produce si se introduce un complemento de forma explícita en la configuración de directiva **Lista de complementos** de manera que los usuarios puedan seguir administrando el complemento. En ese caso, deben hacerlo con Administrar complementos. Al establecer esta configuración de directiva en **Deshabilitado**, los usuarios pueden habilitar y deshabilitar los complementos.
  
No es infrecuente que los usuarios instalen complementos vedados por la directiva de seguridad de la organización. Ese tipo de complementos puede entrañar riesgos considerables para la seguridad y la privacidad en la red. Por lo tanto, esta configuración de directiva se establece como **Habilitada** para los dos entornos que se tratan en esta guía.
  
**Nota**   Revise la configuración de GPO en Internet Explorer\\Características de seguridad\\Administración de complementos para asegurarse de que en su entorno aún se pueden ejecutar los complementos autorizados que correspondan. Por ejemplo, quizá le interese leer el artículo 555235 de Knowledge Base, el cual trata sobre [Outlook Web Access y Lugar de trabajo remoto en Web de Windows Small Business Server, cuyo funcionamiento impide el bloqueo de complementos del Service Pack 2 de XP habilitado con la directiva de grupo](http://support.microsoft.com/default.aspx?kbid=555235) (en inglés).
  
**Configuración de proxy por equipo y no por usuario**  
Si habilita esta configuración de directiva, no se permitirá a los usuarios alterar parámetros de configuración de proxy específicos del usuario. Deben utilizar las zonas que se crean para todos los usuarios de los equipos a los que tienen acceso.
  
La configuración **Configuración de proxy por equipo y no por usuario** se establece en **Habilitado** en los equipos cliente de escritorio de los dos entornos que se describen en esta guía. Sin embargo, la configuración de directiva está configurada como **Deshabilitada** para equipos cliente portátiles porque los usuarios móviles quizá tengan que cambiar su configuración de proxy cuando viajan.
  
**Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios**  
Habilite esta configuración de directiva para deshabilitar los parámetros de administración de sitios para zonas de seguridad. Para consultar la configuración de la administración de sitios para las zonas de seguridad, abra Internet Explorer, elija **Herramientas**, elija **Opciones de Internet**, haga clic en la pestaña de la ficha **Seguridad** y, a continuación, elija **Sitios**. Si deshabilita o no establece esta configuración de directiva, los usuarios pueden agregar sitios Web a las zonas de **sitios de confianza** y de **sitios restringidos** o quitarlos de ellas, además de modificar la configuración de la zona **Intranet local**.
  
El valor **Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Si habilita la configuración **Deshabilitar la página Seguridad** (ubicada en \\Configuración de usuario\\  
Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet), se quita la ficha **Seguridad** de la interfaz y la configuración dedeshabilitación tiene prioridad sobreestevalor.
  
**Zonas de seguridad: no permitir que los usuarios cambien las directivas**  
Si habilita esta configuración de directiva, se deshabilita el botón **Nivel personalizado** y el control deslizante de **Nivel de seguridad de la zona** en la etiqueta **Seguridad** en el cuadro de diálogo **Opciones de Internet**. Si esta configuración de directiva se deshabilita o no está configurada, los usuarios podrán cambiar la configuración de las zonas de seguridad. Evita que los usuarios cambien la configuración de la zona de seguridad establecida por el administrador.
  
El valor **Zonas de seguridad: no permitir que los usuarios cambien las directivas** se configura como **Habilitado** en los dos entornos que se tratan en esta guía.
  
**Nota**   Si habilita la configuración **Deshabilitar la página Seguridad** (ubicada en \\Configuración de usuario\\  
Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet), se quita la ficha **Seguridad** de Internet Explorer en el Panel de control y la configuración dedeshabilitación tiene prioridad sobreeste valor.
  
**Zonas de seguridad: usar sólo la configuración del equipo**  
Esta configuración de directiva afecta a la forma en que se aplican los cambios de zona de seguridad a diferentes usuarios. Se pretende asegurar que la configuración de la zona de seguridad está presente de modo uniforme en el mismo equipo y que no varía de usuario a usuario. Si habilita esta configuración de directiva, los cambios que realice un usuario en una zona de seguridad se aplicarán a todos los usuarios de ese equipo. Si esta configuración de directiva se deshabilita o no se establece, los usuarios del mismo equipo podrán establecer su propia configuración de zona de seguridad.
  
El valor **Zonas de seguridad: usar sólo la configuración del equipo** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Desactivar la detección de bloqueos**  
Esta configuración de directiva le permite administrar la característica de detección de bloqueos en la administración de complementos de Internet Explorer. Si habilita esta configuración de directiva, un bloqueo en Internet Explorer es similar al de un equipo en el que se ejecute Windows XP Professional con Service Pack 1 (SP1) o versiones anteriores: se invoca el Informe de errores de Windows. Si deshabilita esta configuración de directiva, la característica de detección de bloqueos de la administración de complementos sigue en funcionamiento.
  
Dado que los informes de bloqueos de Internet Explorer podrían contener información confidencial de la memoria del equipo, el valor **Desactivar la detección de bloqueos** se configura como **Habilitado** en los dos entornos que se describen en esta guía. Si experimenta bloqueos frecuentes y necesita informar de éstos para la solución de problemas en fase de seguimiento, podría establecer temporalmente la configuración de directiva como **Deshabilitada.**
  
En **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer** se configuran estas otras secciones:
  
-   [Panel de control Internet\\Página Opciones avanzadas](#_internet_explorer-internet_control)
  
-   [Características de seguridad\\Restricción de seguridad del protocolo MK](#_internet_explorer-security_features)
  
-   [Características de seguridad\\Administración de MIME consistente](#_security_features-consistent_mime)
  
-   [Características de seguridad\\Características de seguridad de examen de MIME](#_security_features-mime_sniffing)
  
-   [Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos](#_security_features-scripted_window)
  
-   [Características de seguridad\\Protección contra elevación de zona](#_security_features-protection_from)
  
-   [Características de seguridad\\Limitar la instalación de ActiveX](#_security_features-restrict_activex)
  
-   [Características de seguridad\\Limitar la descarga de archivos](#_security_features-restrict_file)
  
-   [Características de seguridad\\Administración de complementos](#_security_features-add-on_management)
  
-   [Lista de complementos](#_internet_explorer_add-on)
  
Los valores predeterminados de estas configuraciones proporcionan mecanismos de seguridad mejorados con respecto a versiones anteriores de Windows. Sin embargo, quizá desee revisar estas configuraciones para determinar si desea que sean requeridas en mayor o menor medida en su entorno a fin de facilitar el uso o la compatibilidad con aplicaciones.
  
Por ejemplo, ahora se puede configurar Internet Explorer de modo que bloquee los elementos emergentes en todas las zonas de Internet de forma predeterminada. Quizá desee asegurarse de que esta configuración de directiva se aplica en todos los equipos del entorno para evitar la aparición de ventanas emergentes y reducir la posibilidad de instalaciones de software espía y malintencionado que a menudo se inician desde sitios Web de Internet. También ocurre lo contrario: puede que algunas aplicaciones del entorno deban usar elementos emergentes en su funcionamiento. En ese caso, podría configurar esta directiva para permitir elementos emergentes de sitios Web de la intranet.
  
###### Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Opciones avanzadas (página)**
  
**Tabla A45. Configuración recomendada de la página Opciones avanzadas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir que el software se ejecute o instale incluso si la firma no es válida</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Permitir que el software se ejecute o instale incluso si la firma no es válida**  
Los controles Microsoft ActiveX® y los archivos que se descargan suelen tener adjuntas firmas digitales que garantizan tanto la integridad del archivo como la identidad del firmante (creador) del software. La firma garantiza que el software descargado no está alterado y que es posible identificar a los firmantes activos con objeto de determinar si gozan de confianza suficiente como para ejecutar el software.
  
El parámetro **Permitir que el software se ejecute o instale incluso si la firma no es válida** le permite controlar si el software descargado puede ser instalado o ejecutado por los usuarios aunque la firma no sea válida. Una firma no válida podría indicar que el archivo está manipulado. Si habilita esta configuración de directiva, se pregunta a los usuarios si desean instalar o ejecutar los archivos que carezcan de una firma válida. Si la deshabilita, los usuarios no pueden instalar ni ejecutar archivos sin firma válida.
  
Puesto que el software sin firmar puede crear una vulnerabilidad de seguridad, esta configuración de directiva se establece en **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Puede haber software y controles legítimos con firma no válida aunque sean correctos. Deberá probar cuidadosamente ese software en un entorno aislado antes de permitir su uso en la red de la organización.
  
###### Internet Explorer\\Características de seguridad\\Restricción de seguridad del protocolo MK
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Restricción de seguridad del protocolo MK**
  
**Tabla A46. Configuración recomendada del protocolo MK**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (protocolo MK)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (protocolo MK)**  
Esta configuración de directiva reduce el área de superficie de ataque al bloquear el protocolo MK, que raramente se utiliza. Algunas aplicaciones Web más antiguas utilizan el protocolo MK para recuperar información de archivos comprimidos. Si establece esta configuración de directiva como **Habilitada**, se bloqueará el protocolo MK para el Explorador de Windows e Internet Explorer, lo que provocará errores de los recursos que utilizan el protocolo MK. Si deshabilita esta configuración de directiva, permitirá a otras aplicaciones que utilicen la API del protocolo MK.
  
Como el protocolo MK no es de uso común, se debe bloquear siempre que no sea necesario. Esta configuración de directiva se establece en **Habilitado** en los dos entornos que se describen en esta guía. Microsoft recomienda bloquear el protocolo MK, a menos que lo necesite específicamente en su entorno.
  
**Nota**   Cuando implementa esta configuración de directiva, se produce un error en los recursos que usan el protocolo MK; por ello, debe asegurarse de que ninguna de las aplicaciones lo hace.
  
###### Internet Explorer\\Características de seguridad\\Administración de MIME consistente
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Administración de MIME consistente**
  
**Tabla A47. Configuración recomendada de administración de MIME consistente**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (administración de MIME consistente)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (administración de MIME consistente)**  
Internet Explorer utiliza datos MIME (Extensiones multipropósito de correo Internet) para determinar los procedimientos de administración de archivos que se reciben a través de un servidor Web. El parámetro **Administración de MIME consistente** determina si Internet Explorer debe requerir que toda la información de tipo de archivo proporcionada por los servidores Web sea coherente. Por ejemplo, si el tipo MIME de un archivo es text/plain pero los datos MIME indican que se trata, en realidad, de un archivo ejecutable, Internet Explorer cambia su extensión para que refleje esa condición. Esta capacidad resulta útil para garantizar que el código ejecutable no se enmascare como otro tipo de datos de confianza.
  
Si habilita esta configuración de directiva, Internet Explorer examina todos los archivos recibidos y les aplica datos MIME coherentes. Si deshabilita o no establece esta configuración de directiva, Internet Explorer no requerirá que los datos MIME sean coherentes en todos los archivos recibidos y utilizará los datos MIME que proporciona el archivo.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Debe asegurarse de que estos archivos son coherentes y están debidamente etiquetados como medida para evitar descargas de archivos malintencionados que pueden infectar su red. Esta configuración de directiva se establece en **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva funciona junto con la configuración **Característica de seguridad de examen de MIME**, no la reemplaza.
  
###### Internet Explorer\\Características de seguridad\\Característica de seguridad de examen de MIME
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Característica de seguridad de examen de MIME**
  
**Tabla A48. Configuración recomendada de examen de MIME**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (examen de MIME)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (examen de MIME)**  
El examen de MIME es un proceso en el que se evalúa el contenido de un archivo MIME para determinar su contexto (si se trata de un archivo de datos, de un archivo ejecutable o de algún otro tipo de archivo). Esta configuración de directiva determina si el examen de MIME de Internet Explorer impide el cambio de los archivos de un tipo a otro tipo de archivo más peligroso. Si se establece en **Habilitado**, el examen de MIME no realiza ese cambio a tipos de archivos peligrosos. Si deshabilita esta configuración de directiva, el examen de MIME configura los procesos de Internet Explorer de modo que permitan la conversión de un archivo de un tipo determinado a otro tipo de archivo más peligroso. Por ejemplo, un archivo de texto podría ser convertido en un archivo ejecutable, lo cual resulta peligroso porque se ejecutaría cualquier código que hubiera en el supuesto archivo de texto.
  
La imitación de un tipo de archivo MIME constituye una amenaza potencial para su organización. Microsoft recomienda asegurarse de que estos archivos se tratan de un modo coherente como medida para evitar descargas de archivos malintencionados que pueden infectar su red.
  
El valor **Procesos de Internet Explorer (examen de MIME)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva funciona junto con la configuración **Administración de MIME consistente**, no la reemplaza.
  
###### Internet Explorer\\Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Restricciones de seguridad de ventanas con secuencias de comandos**
  
**Tabla A49. Configuración recomendada de restricciones de ventanas con secuencias de comandos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (restricciones de seguridad de ventanas con secuencias de comandos)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (restricciones de seguridad de ventanas con secuencias de comandos)**  
Internet Explorer facilita la programación de secuencias de comandos para abrir distintos tipos de ventanas o bien cambiar su tamaño o su ubicación. Hay sitios Web de mala reputación que cambian el tamaño de las ventanas para ocultar otras o que obligan al visitante a interaccionar con una ventana que contiene código malintencionado.
  
El parámetro **Procesos de Internet Explorer** (**Restricciones de seguridad de ventanas con secuencias de comandos**) restringe las ventanas emergentes e impide que a través de secuencias de comandos se muestren ventanas en las que las barras de título y estado no son visibles para el usuario o que se oculten las barras de título y estado de otras ventanas. Si habilita esta configuración de directiva, no se mostrarán ventanas emergentes en el Explorador de Windows ni en los procesos de Internet Explorer. Si deshabilita o no establece esta configuración de directiva, las secuencias de comandos aún podrán crear ventanas emergentes y ventanas que oculten a otras.
  
El valor **Procesos de Internet Explorer** **(restricciones de seguridad de ventanas con secuencias de comandos)** se configura como **Habilitado** en los dos entornos que se describen en esta guía. Cuando está habilitada, esta configuración de directiva dificulta que, desde sitios Web malintencionados, se controlen sus ventanas de Internet Explorer o se engañe a los usuarios para que hagan clic en la ventana indebida.
  
###### Internet Explorer\\Características de seguridad\\Protección contra elevación de zona
  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Protección contra elevación de zona**
  
**Tabla A50. Configuración recomendada de protección contra elevación de zona**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (protección contra elevación de zona)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (protección contra elevación de zona)**  
Internet Explorer establece restricciones para cada página Web que abre. Estas restricciones dependen de la ubicación de la página Web (zona Internet, zona de intranet o zona de equipo local). Las páginas Web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Equipo local, lo que convierte esta zona en un objetivo prioritario para los atacantes malintencionados.
  
Si habilita el parámetro **Procesos de Internet Explorer (Protección contra elevación de zona)**, se puede proteger cualquier zona de modo que los procesos de Internet Explorer no puedan llevar a cabo una elevación de zona. Este método ayuda a impedir que se apliquen privilegios elevados de una zona al contenido de otra. Si deshabilita esta configuración de directiva, ninguna zona recibe esta clase de protección en los procesos de Internet Explorer.
  
A causa de la gravedad y relativa frecuencia de los ataques de elevación de zona, el valor **Procesos de Internet Explorer (protección contra elevación de zona)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
###### Internet Explorer\\Características de seguridad\\Limitar la instalación de ActiveX
  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Limitar la instalación de ActiveX**
  
**Tabla A51. Configuración de limitación de la instalación de ActiveX**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (limitar la instalación de ActiveX)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (limitar la instalación de ActiveX)**  
Esta configuración de directiva proporciona la capacidad de bloquear mensajes de instalación de controles ActiveX para procesos de Internet Explorer. Si habilita esta configuración de directiva, se bloquearán los mensajes de instalación de controles de ActiveX en procesos de Internet Explorer. Si deshabilita esta configuración de directiva, no se bloquearán los mensajes de instalación de controles de ActiveX, de modo que los usuarios verán esos mensajes.
  
A menudo, los usuarios deciden instalar software (como, por ejemplo, controles de ActiveX) que no permite la directiva de seguridad de su organización. Ese tipo de software puede entrañar riesgos considerables para la seguridad y la privacidad en las redes. Por lo tanto, el valor **Procesos de Internet Explorer (limitar la instalación de ActiveX)** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva impide también que los usuarios instalen controles legítimos de ActiveX que interfieran en el funcionamiento de componentes importantes del sistema como Windows Update. Si habilita esta configuración de directiva, asegúrese de implementar alguna forma alternativa de distribuir las actualizaciones de seguridad como Windows Server Update Services (WSUS). Para obtener más información acerca de WSUS, consulte la página [Introducción a Windows Server Update Services](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx).
  
###### Internet Explorer\\Características de seguridad\\Limitar la descarga de archivos
  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Limitar la descarga de archivos**
  
**Tabla A52. Configuración recomendada de limitación de la descarga de archivos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Procesos de Internet Explorer (limitar la descarga de archivos)</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Procesos de Internet Explorer (limitar la descarga de archivos)**  
En determinadas circunstancias los sitios Web pueden iniciar diálogos de descarga de archivos sin la interacción de los usuarios. Esta técnica permite a los sitios Web colocar archivos no autorizados en el disco duro de un usuario si éste elige el botón equivocado y acepta la descarga.
  
Si establece el parámetro **Procesos de Internet Explorer (limitar la descarga de archivos)** como **Habilitado**, se bloquean los mensajes de descarga de archivos que no inician los usuarios en los procesos de Internet Explorer. Si establece esta configuración de directiva como **Deshabilitado**, se mostrarán mensajes para descargas de archivos que no inicien los usuarios en los procesos de Internet Explorer.
  
El valor **Procesos de Internet Explorer (limitar la descarga de archivos)** se configura como **Habilitado** en los dos entornos que se describen en esta guía como medida para evitar que un atacante introduzca código arbitrario en equipos de usuarios.
  
###### Internet Explorer\\Características de seguridad\\Administración de complementos
  
Puede establecer esta configuración recomendada de equipos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Características de seguridad\\Administración de complementos**
  
**Tabla A53. Configuración de la administración de complementos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Denegar complementos a menos que se permitan específicamente en la Lista de complementos</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Lista de complementos</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
<td style="border:1px solid black;">Recomendado</td>
</tr>
</tbody>
</table>
  
**Denegar complementos a menos que se permitan específicamente en la Lista de complementos**  
Esta configuración de directiva, junto con el parámetro **Lista de complementos**, le permite controlar complementos de Internet Explorer. De manera predeterminada, la configuración **Lista de complementos** define una lista con los complementos que se permiten o se rechazan de acuerdo con la directiva de grupo. La configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** garantiza que se denieguen todos los complementos a menos que figuren en la configuración **Lista de complementos**.
  
Si habilita esta configuración de directiva, Internet Explorer sólo permite complementos que se enumeran (y permiten) específicamente a través de la **Lista de complementos.** Si deshabilita esta configuración de directiva, los usuarios pueden usar el administrador de complementos para permitir o denegar cualquier complemento.
  
Considere la posibilidad de emplear tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en el entorno. Así se garantiza que sólo se usen los complementos autorizados.
  
**Lista de complementos**  
Esta configuración de directiva, junto con el parámetro **Denegar complementos a menos que se permitan específicamente en la Lista de complementos**, le permite controlar los complementos de Internet Explorer. De manera predeterminada, la configuración **Lista de complementos** define una lista con los complementos que se permiten o se rechazan de acuerdo con la directiva de grupo. La configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** garantiza que se denieguen todos los complementos a menos que figuren en la configuración **Lista de complementos**.
  
Si habilita el parámetro **Lista de complementos**, deberá enumerar los complementos que deben ser permitidos o denegados por Internet Explorer. Como la lista específica de complementos que se deben incluir en esta lista varía según la organización, en esta guía no se proporciona una relación detallada. Con cada entrada que agregue a la lista, debe aportar la información siguiente:
  
-   **Nombre del valor**. Identificador de clase (CLSID) del complemento que desee agregar a la lista; debe aparecer entre llaves, por ejemplo, {000000000-0000-0000-0000-0000000000000}. El CLSID de un complemento se puede obtener si se lee la etiqueta OBJECT de una página Web que haga referencia al complemento.
  
-   **Valor**. Un número que indica si Internet Explorer debe denegar o permitir que se cargue el complemento. Son válidos los valores siguientes:
  
    -   **0** Denegar este complemento
  
    -   **1** Permitir este complemento
  
    -   **2** Permitir este complemento y que el usuario lo administre con Administrar complementos
  
Si deshabilita el parámetro **Lista de complementos**, la lista se elimina. Considere la posibilidad de emplear tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en el entorno. Así se garantiza que sólo se usen los complementos autorizados.
  
###### NetMeeting
  
Microsoft NetMeeting® permite que los usuarios mantengan reuniones virtuales en la red de la organización. Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**NetMeeting**
  
**Tabla A54. Configuración recomendada de NetMeeting**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Desactivar Compartir escritorio remoto</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Desactivar Compartir escritorio remoto**  
Esta configuración de directiva deshabilita la característica de uso compartido de escritorio remoto que ofrece NetMeeting. Si habilita esta configuración de directiva, los usuarios no podrán configurar NetMeeting para permitir el control remoto del escritorio local.
  
La configuración **Desactivar Compartir escritorio remoto** se establece en **Sin configurar** en el entorno EC. Sin embargo, se configura como **Habilitado** para el entorno SSLF con objeto de evitar que los usuarios compartan escritorios de forma remota a través de NetMeeting.
  
###### Servicios de Terminal Server
  
La configuración de Servicios de Terminal Server ofrece opciones para redireccionar los recursos del equipo cliente a servidores a los que otorguen acceso. Esta sección incluye las configuraciones siguientes:
  
-   Cliente de Conexión a Escritorio remoto
  
-   Terminal Server\\Conexiones
  
-   Terminal Server\\Redirección de dispositivos y recursos
  
-   Terminal Server\\Seguridad
  
Terminal Services\\Cliente de Conexión a Escritorio remoto  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Plantillas administrativas\\Componentes de Windows\\Terminal Services**  
**\\Cliente de Conexión a Escritorio remoto**
  
**Tabla A55. Configuración recomendada de No permitir que se guarden las contraseñas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir que se guarden las contraseñas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No permitir que se guarden las contraseñas**  
Esta configuración de directiva ayuda a impedir que los clientes de Servicios de Terminal Server guarden contraseñas en los equipos. Si habilita esta configuración de directiva, se deshabilita la casilla de verificación de almacenamiento en los clientes de Servicios de Terminal Server, de modo que los usuarios no podrán guardar contraseñas.
  
Puesto que el guardar las contraseñas entraña más riesgos para la seguridad, el valor **No permitir que se guarden las contraseñas** se configura como **Habilitado** en los dos entornos que se abordan en esta guía.
  
**Nota**   Si esta configuración de directiva estaba establecida en **Deshabilitado** o **Sin configurar**, todas las contraseñas guardadas se eliminan la primera vez que el cliente de Servicios de Terminal Server se desconecte de cualquier servidor.
  
Terminal Services\\Terminal Server\\Conexiones  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Terminal Services\\Terminal Server\\Conexiones**
  
**Tabla A56. Configuración recomendada de conexiones**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Permitir que los usuarios se conecten de forma remota utilizando Servicios de Terminal Server</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Permitir que los usuarios se conecten de forma remota utilizando Servicios de Terminal Server**  
Esta configuración de directiva permite controlar si los usuarios se pueden conectar a un equipo con Servicios de Terminal Server o Escritorio remoto.
  
En el entorno SSLF, se obliga a los usuarios a iniciar sesión directamente en la consola física del equipo. Por ello, la configuración **Permitir que los usuarios se conecten de forma remota utilizando Servicios de Terminal Server** se establece en **Deshabilitado** en el entorno SSLF. En cambio, se configura como **Habilitado** en el entorno EC.
  
Terminal Services\\Terminal Server\\Redirección de dispositivos y recursos  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Terminal Services\\Terminal Server\\Redirección de dispositivos y recursos**
  
**Tabla A57. Configuración recomendada de redirección de dispositivos y recursos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir redirección de unidad</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No permitir redirección de unidad**  
Esta configuración de directiva impide que los usuarios compartan las unidades locales de los equipos cliente que utilizan para obtener acceso a servicios de Terminal Server. Las unidades asignadas aparecen en el árbol de carpetas de la sesión con este formato:
  
\\\\TSClient\\*&lt;driveletter&gt;*$
  
Si las unidades locales se comparten serán vulnerables a los intrusos que deseen aprovechar los datos que almacenan. Por ese motivo, el parámetro **No permitir redirección de unidad** se configura como **Habilitado** para el entorno SSLF. En cambio, se configura como **Habilitado** en el entorno EC.
  
Terminal Services\\Terminal Server\\Seguridad  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas**  
**\\Componentes de Windows\\Terminal Services\\Terminal Server\\Seguridad**
  
**Tabla A58. Configuración recomendada de seguridad de Servicios de Terminal Server**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Portátil<br />
EC</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Pedir siempre al cliente la contraseña al conectarse</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Establecer el nivel de cifrado de conexión de cliente</td>
<td style="border:1px solid black;">Habilitado: alto nivel</td>
<td style="border:1px solid black;">Habilitado: alto nivel</td>
<td style="border:1px solid black;">Habilitado: alto nivel</td>
<td style="border:1px solid black;">Habilitado: alto nivel</td>
</tr>
</tbody>
</table>
  
**Pedir siempre al cliente la contraseña al conectarse**  
Esta configuración de directiva especifica si los Servicios de Terminal Server deben solicitar siempre una contraseña al cliente al realizar la conexión. Puede utilizarla para forzar la petición de una contraseña a los usuarios que inicien sesión en los Servicios de Terminal Server, aunque ya se haya proporcionado una en el cliente de Conexión a Escritorio remoto. De forma predeterminada, los Servicios de Terminal Server permiten a los usuarios iniciar sesión de forma automática si escriben una contraseña en el cliente de Conexión a Escritorio remoto.
  
El valor **Pedir siempre al cliente la contraseña al conectarse** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Si no establece esta configuración de directiva, el administrador del equipo local puede usar la herramienta de configuración de Servicios de Terminal Server para permitir o impedir que se envíen de forma automática las contraseñas.
  
**Establecer el nivel de cifrado de conexión de cliente**  
Esta configuración de directiva especifica si el equipo que está a punto de alojar la conexión remota exigirá que se aplique un nivel de cifrado para todos los datos que intercambie con el equipo cliente para la sesión remota.
  
El cifrado se establece en **Habilitado: nivel alto** para que se aplique un cifrado de 128 bits en los dos entornos que se describen en esta guía.
  
###### Windows Messenger
  
Windows Messenger sirve para enviar mensajes instantáneos a otros usuarios de una red de equipos. En estos mensajes se pueden incluir archivos u otros datos adjuntos.
  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas**  
**\\Componentes de Windows\\Windows Messenger**
  
**Tabla A59. Configuración recomendada de Windows Messenger**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No permitir que se ejecute Windows Messenger</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No permitir que se ejecute Windows Messenger**  
Puede habilitar la configuración **No permitir que se ejecute Windows Messenger** para deshabilitar Windows Messenger y evitar que se ejecute el programa. Dado que esta aplicación se ha utilizado con fines malintencionados tales como el envío de correo no deseado, la distribución de software malintencionado y la divulgación de datos confidenciales, Microsoft recomienda configurar el parámetro **No permitir que se ejecute Windows Messenger** como **Habilitado** para los entornos EC y SSLF.
  
**Nota**   Esta configuración de directiva sólo afecta al software Windows Messenger incluido en Windows XP. No impide que los usuarios ejecuten MSN® Messenger ni Windows Live™ Messenger.
  
###### Windows Update
  
Los administradores usan la configuración de Windows Update para administrar la forma en que se aplican las actualizaciones y las revisiones en las estaciones de trabajo basadas en Windows Vista. Las actualizaciones se encuentran disponibles en Windows Update. Asimismo, se puede configurar un sitio Web en la intranet para distribuir las actualizaciones y las revisiones de forma parecida y con mayor control administrativo.
  
Windows Server Update Services (WSUS) es un servicio de infraestructuras que aumenta la eficacia de las tecnología de Microsoft Windows Update y Software Update Services (SUS). WSUS administra y distribuye actualizaciones críticas de Windows que resuelven vulnerabilidades conocidas en la seguridad así como otros problemas de estabilidad en los sistemas operativos Windows.
  
WSUS elimina los pasos de actualización manual gracias a un sistema dinámico de notificación de actualizaciones críticas disponibles para los equipos cliente basados en Windows a través del servidor de intranet. Para utilizar este servicio no se necesita acceso a Internet desde los equipos cliente. Esta tecnología ofrece, además, una forma sencilla y automática de distribuir actualizaciones a las estaciones de trabajo y los servidores basados en Windows.
  
Windows Server Update Services también proporciona las siguientes características:
  
-   **Control del administrador sobre la sincronización de contenido en la intranet**. Este servicio de sincronización es un componente de servidor que recupera las últimas actualizaciones críticas de Windows Update. A medida que se agregan actualizaciones en Windows Update, el servidor que ejecuta WSUS las descarga y las almacena de acuerdo a una programación definida por el administrador.
  
-   **Un servidor de Windows Update alojado en la intranet**. Este sencillo servidor actúa como servidor virtual de Windows Update para los equipos cliente. Contiene herramientas administrativas y un servicio de sincronización para administrar las actualizaciones. Atiende solicitudes de actualizaciones aprobadas desde los equipos cliente conectados a través del protocolo HTTP. Este servidor también puede alojar actualizaciones críticas que se descargan del servicio de sincronización y, posteriormente, informar a los equipos cliente de las mismas.
  
-   **Control del administrador sobre las actualizaciones**. El administrador puede probar y aprobar las actualizaciones desde el sitio público de Windows Update antes de distribuirlas en la intranet de su organización. La distribución tiene lugar según una programación que crea el administrador. Si WSUS se ejecuta en varios servidores, el administrador controla qué equipos obtienen acceso a determinados servidores que ejecuten este servicio. Los administradores habilitan este grado de control con la directiva de grupo en los entornos de Active Directory o mediante claves del Registro.
  
-   **Actualizaciones automáticas en equipos (estaciones de trabajo o servidores)**. Actualizaciones automáticas es una característica de Windows que se puede configurar para la búsqueda de actualizaciones que se publiquen en Windows Update. WSUS utiliza esta característica de Windows para notificar al administrador la existencia de actualizaciones aprobadas en una intranet.
  
**Nota**   Si decide distribuir las actualizaciones con otro método, por ejemplo, Microsoft Systems Management Server (SMS), se recomienda que deshabilite la configuración **Configurar actualizaciones automáticas**.
  
Hay varias opciones de configuración de Windows Update. Se requieren como mínimo tres valores de configuración para que Windows Update funcione: **Configurar actualizaciones automáticas**, **No reiniciar automáticamente para instalaciones de actualizaciones automáticas** y **Volver a programar la instalación programada de actualizaciones automáticas**. La configuración del cuarto valor es opcional y depende de los requisitos de la organización: **Especificar la ubicación del servicio Windows Update de la intranet**.
  
Puede establecer la configuración recomendada para los equipos en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**\\Windows Update**
  
Los parámetros que se tratan en esta sección no solucionan por separado ninguna amenaza para la seguridad en particular, sino que más bien guardan relación con las preferencias del administrador. No obstante, la configuración de Windows Update resulta fundamental para la seguridad del entorno ya que contribuye a garantizar que los equipos cliente reciban las actualizaciones de seguridad desde Microsoft tan pronto como se encuentren disponibles.
  
**Nota**   Windows Update depende de varios servicios, incluidos los de registro remoto y transferencia inteligente en segundo plano.
  
La tabla siguiente resume la configuración recomendada de Windows Update. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A60. Configuración recomendada de Windows Update**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Cliente de empresa - Escritorio</th>
<th style="border:1px solid black;" >Cliente de empresa - Portátil</th>
<th style="border:1px solid black;" >SSLF - Escritorio</th>
<th style="border:1px solid black;" >SSLF - Portátil</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No mostrar la opción ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No ajustar la opción predeterminada a ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configurar actualizaciones automáticas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No reiniciar automáticamente para instalaciones de actualizaciones automáticas</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Volver a programar la instalación programada de actualizaciones automáticas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No mostrar la opción ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar**  
Esta configuración de directiva le permite administrar si la opción **Instalar actualizaciones y Apagar** se muestra en el cuadro de diálogo **Apagar**. Si deshabilita esta configuración de directiva, se muestra la opción **Instalar actualizaciones y apagar** en el cuadro de diálogo **Salir de Windows** en caso de que haya actualizaciones disponibles cuando el usuario elige la opción **Apagar** en el menú **Inicio**.
  
Dado que las actualizaciones son importantes para la seguridad de los equipos en general, el valor **No mostrar la opción ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía. Esta configuración de directiva funciona junto con la configuración **No ajustar la opción predeterminada a ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar**, que se trata a continuación.
  
**No ajustar la opción predeterminada a ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar**  
Esta configuración de directiva le permite administrar si se posibilita que la opción **Instalar actualizaciones y Apagar** sea la predeterminada en el cuadro de diálogo **Salir de Windows**. Si deshabilita esta configuración de directiva, la opción **Instalar actualizaciones y Apagar** será la predeterminada en el cuadro de diálogo **Salir de Windows** en caso de que haya actualizaciones disponibles para la instalación cuando el usuario seleccione la opción **Apagar equipo** en el menú **Inicio**.
  
Dado que las actualizaciones son importantes para la seguridad de los equipos en general, el valor **No ajustar la opción predeterminada a ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva no tiene ningún efecto si la configuración **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Update\\No mostrar la opción ‘Instalar actualizaciones y apagar’ en el cuadro de diálogo Apagar** se establece en **Habilitado**.
  
**Configurar actualizaciones automáticas**  
Esta configuración de directiva especifica si los equipos del entorno recibirán actualizaciones de seguridad desde Windows Update o WSUS. Si establece esta configuración de directiva en **Habilitado**, el sistema operativo reconoce cuándo se encuentra disponible una conexión en red para buscar Windows Update o el sitio designado en la intranet para las actualizaciones correspondientes.
  
Una vez establecida la configuración de directiva como **Habilitada**, seleccione una de las tres opciones siguientes en el cuadro de diálogo **Propiedades de Configurar actualizaciones automáticas** para especificar cómo funcionará este servicio:
  
-   **Notificar antes de descargar las actualizaciones y notificar de nuevo antes de instalarlas**.
  
-   **Descargar las actualizaciones automáticamente y enviar una notificación cuando se puedan instalar**. **(Configuración predeterminada)**
  
-   **Descargar las actualizaciones automáticamente e instalarlas en la programación especificada debajo**.
  
Si deshabilita esta configuración de directiva, debe descargar e instalar de forma manual cualquier actualización disponible de Windows Update.
  
El valor **Configurar actualizaciones automáticas** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**No reiniciar automáticamente para instalaciones de actualizaciones automáticas**  
Si esta configuración de directiva se habilita, el equipo esperará a que un usuario que haya iniciado la sesión reinicie para finalizar una instalación programada; de otro modo, el equipo se reiniciará automáticamente. Cuando está habilitada, esta configuración de directiva también evitará que Actualizaciones automáticas reinicie los equipos durante una instalación programada. Si un usuario inicia una sesión en el equipo y Actualizaciones automáticas necesita reiniciar para finalizar una instalación, el usuario recibirá una notificación y podrá retardar el reinicio del sistema. Actualizaciones automáticas no detectará actualizaciones posteriores mientras no se reinicie el equipo.
  
Si el valor **No reiniciar automáticamente para instalaciones de actualizaciones automáticas** se configura como **Deshabilitado** o **Sin configurar**, Actualizaciones automáticas notifica al usuario que el equipo se reiniciará de manera automática al cabo de cinco minutos para completar la instalación. Si los reinicios automáticos constituyen un motivo de preocupación, puede configurar el parámetro **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** como **Habilitado.** Si habilita esta configuración de directiva, programe los equipos cliente para que se reinicien transcurrido el horario laboral habitual, a fin de asegurar que la instalación esté completa.
  
El valor **No reiniciar automáticamente para instalaciones de actualizaciones automáticas** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Esta configuración de directiva sólo funciona cuando Actualizaciones automáticas se configura para realizar instalaciones de actualizaciones programadas. Si el parámetro **Configurar actualizaciones automáticas** se ha establecido como **Deshabilitado**, no funcionará.
  
**Volver a programar la instalación programada de actualizaciones automáticas**  
Esta configuración de directiva determina el período de tiempo que transcurrirá antes de que las instalaciones programadas de Actualizaciones automáticas se lleven a cabo tras el inicio del sistema. Si establece esta configuración de directiva como **Habilitada**, cuando el equipo se inicie de nuevo comenzará una instalación anteriormente programada cuando haya transcurrido un tiempo especificado en minutos. Si establece esta configuración de directiva en **Deshabilitado** o **Sin configurar**, las instalaciones programadas con anterioridad tienen lugar durante el siguiente momento de instalación según la programación regular.
  
El valor **Volver a programar la instalación programada de actualizaciones automáticas** se configura como **Habilitado** en los dos entornos que se describen en esta guía. Después de habilitar esta configuración de directiva, podrá cambiar el período de espera predeterminado a otro más adecuado para el entorno.
  
**Nota**   Esta configuración de directiva sólo funciona cuando Actualizaciones automáticas se configura para realizar instalaciones de actualizaciones programadas. Si el parámetro **Configurar actualizaciones automáticas** se establece como **Deshabilitado**, el parámetro **Volver a programar la instalación programada de actualizaciones automáticas** no tendrá efecto. Puede habilitar los dos parámetros anteriores para asegurarse de que las instalaciones que falten se programarán para realizarse cada vez que se reinicie el equipo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directiva de usuario
  
En las restantes secciones de este apéndice se incluyen recomendaciones sobre los valores de Configuración de usuario. Recuerde que esta configuración debe aplicarse a los usuarios, no a los equipos. Debe implementarse en una directiva de grupo que esté vinculada a la unidad organizativa que contenga los usuarios que desee configurar. Aplique estas opciones de configuración a través de un GPO vinculado a una UO que contenga cuentas de usuario.
  
**Nota**   Los valores de configuración de los usuarios se aplican a cualquier equipo basado en Windows Vista en el que inicie sesión un usuario en un dominio Active Directory. Sin embargo, los parámetros de configuración del equipo se aplican a todos los equipos cliente controlados por un GPO en Active Directory, independientemente del usuario que inicie sesión en el equipo.
  
#### Configuración de usuario\\Plantillas administrativas
  
A continuación figuran los grupos de configuraciones recomendadas para la directiva de usuarios. Estas configuraciones aparecen en el subnodo **Configuración de usuario\\Plantillas administrativas** del Editor de objetos de directiva de grupo:
  
-   [Sistema](#_internet_explorer_1)
  
    -   [Administración de energía](#_power_management)
  
-   [Componentes de Windows](#_windows_components_3)
  
    -   [Administrador de datos adjuntos](#_attachment_manager_1)
  
    -   [Internet Explorer](#_internet_explorer_3)
  
    -   [Explorador de Windows](#_windows_explorer)
  
##### Sistema
  
Puede establecer la configuración recomendada en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para el Editor del Registro.
  
**Tabla A61. Configuración recomendada de usuarios del sistema**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Impedir el acceso a herramientas de edición del Registro</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Impedir el acceso a herramientas de edición del Registro**  
Esta configuración de directiva deshabilita los editores del Registro de Windows Regedit.exe y Regedt32.exe. Si habilita esta configuración de directiva, cuando los usuarios traten de usar algún editor del Registro, se muestra un mensaje en el que se les informa de que no pueden utilizar ninguno de estos editores. Esta configuración de directiva niega a usuarios e intrusos la posibilidad de tener acceso al Registro mediante estas herramientas pero no el acceso al Registro.
  
La configuración **Impedir el acceso a herramientas de edición del Registro** se establece en **Sin configurar** en el entorno EC. En cambio, se configura como **Habilitado** en el entorno SSLF.
  
###### Administración de energía
  
Puede establecer la configuración recomendada en esta ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema\\Administración de energía**
  
En la tabla siguiente se resumen los valores de configuración recomendados para **Solicitar contraseña al reanudar tras hibernación o suspensión**.
  
**Tabla A62. Configuración de usuario recomendada para Sistema\\Administración de energía**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Solicitar contraseña al reanudar tras hibernación o suspensión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Solicitar contraseña al reanudar tras hibernación o suspensión**  
Esta configuración de directiva controla si los equipos cliente del entorno están bloqueados cuando reanudan el funcionamiento normal tras un estado de hibernación o suspensión. Si habilita esta configuración de directiva, los equipos cliente se bloquean cuando reanudan el funcionamiento normal y los usuarios deben escribir sus contraseñas para desbloquearlos. Pueden producirse infracciones de seguridad graves si esta configuración de directiva se deshabilita o no se establece, ya que cualquier persona puede tener acceso a los equipos cliente.
  
Por ese motivo, el valor **Solicitar contraseña al reanudar tras hibernación o suspensión** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
##### Componentes de Windows
  
Puede establecer la configuración recomendada en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para el Editor del Registro.
  
###### Administrador de datos adjuntos
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Administrador de datos adjuntos**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Administrador de datos adjuntos. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A63. Configuración de usuario recomendada para Administrador de datos adjuntos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No conservar la información de zona en los datos adjuntos de archivos</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ocultar mecanismos para eliminar la información de zona</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Notificar a los programas antivirus cuando se abren datos adjuntos</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**No conservar la información de zona en los datos adjuntos de archivos**  
Esta configuración de directiva permite decidir si Windows debe marcar los archivos adjuntos de Internet Explorer o de Microsoft Outlook® Express con información acerca de su zona de origen (restringida, Internet, intranet o local). Esta configuración de directiva requiere que los archivos sean descargados en particiones de disco NTFS para funcionar correctamente. Si no se conserva la información de zona, Windows no puede realizar evaluaciones de riesgo adecuadas basadas en la zona de donde procedan los datos adjuntos.
  
Si se habilita el parámetro **No conservar la información de zona en los datos adjuntos de archivos**, no se marcarán los archivos adjuntos con información de zona. Si esta configuración de directiva se deshabilita, Windows deberá almacenar los archivos adjuntos con la información de zona correspondiente. Como los datos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza (como la zona Internet), Microsoft recomienda establecer esta configuración de directiva en **Deshabilitado** para garantizar que se conserve la máxima cantidad de información de seguridad posible con cada archivo.
  
El valor **No conservar la información de zona en los datos adjuntos de archivos** se configura como **Deshabilitado** en los dos entornos que se tratan en esta guía.
  
**Ocultar mecanismos para eliminar la información de zona**  
Esta configuración de directiva le permite administrar si los usuarios pueden quitar manualmente la información de zona de los archivos adjuntos guardados. Normalmente, los usuarios pueden hacer clic en el botón **Desbloquear** en la hoja de **Propiedades** del archivo o activar una casilla de verificación en el cuadro de diálogo **Advertencia de seguridad**. Si se quita la información de la zona, los usuarios pueden abrir archivos adjuntos potencialmente peligrosos que Windows ha impedido que abran.
  
Cuando se habilita el parámetro **Ocultar mecanismos para eliminar la información de zona**, Windows oculta la casilla de verificación y el botón **Desbloquear**. Cuando se deshabilita esta configuración de directiva, Windows muestra la casilla de verificación y el botón **Desbloquear**. Como los datos adjuntos peligrosos suelen descargarse de zonas de Internet Explorer que no son de confianza (como la zona Internet), Microsoft recomienda establecer esta configuración de directiva en **Habilitado** para garantizar que se conserve la máxima cantidad de información de seguridad posible con cada archivo.
  
El valor **Ocultar mecanismos para eliminar la información de zona** se configura como **Habilitado** en los dos entornos que se tratan en esta guía.
  
**Nota**   Para configurar si los archivos se deben guardar con información de zona, consulte la configuración anterior **No conservar la información de zona en los datos adjuntos de archivos**.
  
**Notificar a los programas antivirus cuando se abren datos adjuntos**  
Los programas antivirus son obligatorios en muchos entornos y constituyen una sólida línea defensiva contra los ataques.
  
El parámetro **Notificar a los programas antivirus cuando se abren datos adjuntos** le permite administrar cómo se notifica a los programas antivirus registrados. Cuando se habilita, esta configuración de directiva determina que Windows llame al programa antivirus registrado para que analice los archivos adjuntos cuando los abren los usuarios. Si la exploración antivirus genera un error, los datos adjuntos se bloquean y no se abren. Si esta configuración de directiva se deshabilita, Windows no llama al programa antivirus registrado cuando se abren archivos adjuntos. Para procurar que los programas de detección de virus examinen todos los archivos antes de que sean abiertos, Microsoft recomienda establecer esta configuración de directiva como **Habilitada** en todos los entornos.
  
El valor **Notificar a los programas antivirus cuando se abren datos adjuntos** se configura como **Habilitado** en los dos entornos que se describen en esta guía.
  
**Nota**   Es preciso tener instalado un programa antivirus actualizado para que esta configuración de directiva funcione correctamente.
  
###### Internet Explorer
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A64. Configuración de usuario recomendada para Internet Explorer**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Configurar Outlook Express</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la configuración del Historial</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: 40</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar Autocompletar para formularios</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar cambio de valores de Configuración automática</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar cambio de configuración de certificados</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar cambio de configuración de conexión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar el cambio de configuración de proxy</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No permitir que usuarios habiliten ni deshabiliten complementos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Impedir el uso de la funcionalidad “Ajustar configuración”</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Impedir la eliminación de archivos temporales de Internet y cookies</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Desactivar la funcionalidad “Eliminar el historial de exploración”</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">§ Desactivar la característica de comprobación de la configuración de seguridad</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Activar la característica Autocompletar para nombres de usuario y contraseñas en formularios</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
**Configurar Outlook Express**  
Esta configuración de directiva permite a los administradores habilitar y deshabilitar la capacidad de los usuarios de Microsoft Outlook Express® de guardar o abrir datos adjuntos que pueden contener un virus. Los usuarios no pueden deshabilitar el parámetro **Configurar Outlook Express** para que deje de bloquear datos adjuntos. Para exigir que se aplique esta configuración de directiva, haga clic en **Habilitar** y seleccione **Bloquear datos adjuntos que puedan contener virus**.
  
La configuración **Configurar Outlook Express** se establece en **Habilitado** con la opción **Bloquear datos adjuntos que puedan contener virus** en el entorno EC que se aborda en esta guía.
  
**Deshabilitar la configuración del Historial**  
Esta configuración especifica el número de días durante los cuales Internet Explorer realiza el seguimiento de las páginas vistas de la lista del Historial. La opción **Eliminar el historial de exploración** se encuentra en la ficha **Herramientas-Opciones de Internet-General**. También está disponible directamente como **Eliminar historial** en **Herramientas-Opciones de Internet-Eliminar el historial de exploración** en Internet Explorer 7.
  
Si habilita esta configuración de directiva, el usuario no puede establecer el número de días durante los que Internet Explorer realiza el seguimiento de las páginas vistas de la lista del Historial. Ha de especificar el número de días durante los que Internet Explorer realiza el seguimiento de las páginas vistas de la lista del Historial. Los usuarios no podrán eliminar el historial de exploración. Si deshabilita o no establece esta configuración de directiva, el usuario puede establecer ese número de días y disfruta, además, de la posibilidad de **eliminar el historial de exploración**.
  
La configuración **Deshabilitar la configuración del historial** se establece en **Sin configurar** en el entorno EC y en **Habilitado: 40** en el entorno SSLF.
  
**Deshabilitar Autocompletar para formularios**  
Esta configuración de directiva controla si se rellenan de forma automática los campos de los formularios presentes en las páginas Web. Si habilita esta configuración de directiva, la característica Autocompletar no sugiere posibles opciones para rellenar el formulario, lo cual puede resultar útil para proteger datos confidenciales en determinados entornos.
  
La configuración **Deshabilitar Autocompletar para formularios** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**Deshabilitar cambio de valores de Configuración automática**  
Esta configuración de directiva impide a los usuarios cambiar los valores configurados de forma automática. Los administradores usan la configuración automática para actualizar de manera periódica la configuración de los exploradores. Si habilita esta configuración de directiva, se atenúan las propiedades de configuración de Internet Explorer. (Estos valores se ubican en la sección **Configuración automática** del cuadro de diálogo **Configuración LAN**). Además, esta configuración de directiva impide a los usuarios cambiar los valores configurados mediante la directiva de grupo.
  
**Para ver el cuadro de diálogo Configuración LAN**
  
1.  Abra el cuadro de diálogo **Opciones de Internet** y haga clic en la ficha **Conexiones**.
  
2.  Haga clic en el botón **Configuración LAN** para ver los parámetros.
  
El valor **Deshabilitar cambio de valores de Configuración automática** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Nota**   La configuración **Deshabilitar la página Conexiones** quita la ficha **Conexiones** de Internet Explorer en el Panel de control y tiene prioridad con respecto a esta opción de configuración, **Deshabilitar cambio de valores de Configuración automática**. Al habilitar la primera configuración, se hace caso omiso de la segunda. La configuración **Deshabilitar la página Conexiones** se ubica en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet, en el Editor de objetos de directiva de grupo.
  
**Deshabilitar cambio de configuración de certificados**  
Esta configuración de directiva impide que los usuarios puedan cambiar la configuración de certificados en Internet Explorer. Los certificados sirven para comprobar la identidad de los editores del software. Si habilita esta configuración de directiva, se atenúan los parámetros de certificado en el área **Certificados** de la ficha **Contenido**, en el cuadro de diálogo **Opciones de Internet**. Además, esta configuración de directiva impide a los usuarios cambiar los valores configurados mediante la directiva de grupo.
  
El valor **Deshabilitar cambio de configuración de certificados** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Nota**   Cuando se habilita esta configuración de directiva, los usuarios aún pueden hacer doble clic en el archivo de certificados de publicación de software (.spc) con el fin de ejecutar el Asistente para la importación de certificados. Este asistente permite a los usuarios importar y configurar propiedades para los certificados de los fabricantes de software que aún no se han configurado en Internet Explorer.
  
**Nota**   La configuración **Deshabilitar la página Contenido** quita la ficha **Contenido** de Internet Explorer en el Panel de control y tiene prioridad con respecto a esta opción de configuración, **Deshabilitar cambio de configuración de certificados**. Al habilitar la primera configuración, se hace caso omiso de la segunda. La configuración **Deshabilitar la página Contenido** se ubica en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet, en el Editor de objetos de directiva de grupo.
  
**Deshabilitar cambio de configuración de conexión**  
Esta configuración de directiva impide a los usuarios cambiar los parámetros de conexión de acceso telefónico. Si habilita esta configuración de directiva, se atenuará el botón **Configuración** de la ficha **Conexiones** en el cuadro de diálogo **Opciones de Internet**. Además, esta configuración de directiva impide a los usuarios cambiar los valores configurados mediante la directiva de grupo. Quizá convenga deshabilitar esta configuración de directiva para los usuarios de equipos portátiles si sus desplazamientos los obligan a cambiar la configuración de conexión.
  
El valor **Deshabilitar cambio de configuración de conexión** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Nota**   Si configura el valor **Deshabilitar la página Conexiones**, no hace falta establecer esta configuración de directiva. La configuración **Deshabilitar la página Conexiones** quita la ficha **Conexiones** de la interfaz. La configuración **Deshabilitar la página Conexiones** se ubica en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet, en el Editor de objetos de directiva de grupo.
  
**Deshabilitar el cambio de configuración de proxy**  
Esta configuración de directiva impide a los usuarios cambiar los parámetros de proxy. Si habilita esta configuración de directiva, se atenúan las opciones de proxy. La configuración de proxy se ubica en la sección **Servidor proxy** del cuadro de diálogo **Configuración LAN**, que aparece cuando el usuario hace clic en la pestaña de la ficha **Conexiones** y elige el botón **Configuración LAN** del cuadro de diálogo **Opciones de Internet**. Además, esta configuración de directiva impide a los usuarios cambiar los valores configurados mediante la directiva de grupo. Quizá convenga deshabilitar esta configuración de directiva para los usuarios de equipos portátiles si sus desplazamientos los obligan a cambiar la configuración de conexión.
  
El valor **Deshabilitar el cambio de configuración de proxy** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Nota**   Si configura el valor **Deshabilitar la página Conexiones**, no hace falta establecer esta configuración de directiva. La configuración **Deshabilitar la página Conexiones** quita la ficha **Conexiones** de la interfaz. Esta configuración se ubica en \\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet, en el Editor de objetos de directiva de grupo.
  
**No permitir que usuarios habiliten ni deshabiliten complementos**  
Esta configuración de directiva permite decidir si los usuarios tienen la capacidad de permitir o denegar complementos con el **administrador de complementos**. Al habilitar esta configuración de directiva, los usuarios no pueden habilitar ni deshabilitar complementos con el **administrador de complementos**. La única excepción se produce si se introduce un complemento de forma explícita en la configuración de directiva ‘**Lista de complementos**’ de manera que los usuarios puedan seguir administrando el complemento. En ese caso, deben hacerlo con el **administrador de complementos** .Si deshabilita o no establece esta configuración de directiva, el usuario tiene a su disposición los controles oportunos del **administrador de complementos**.
  
La configuración **No permitir que usuarios habiliten ni deshabiliten complementos** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**Impedir el uso de la funcionalidad “Ajustar configuración”**  
Esta configuración de directiva impide que los usuarios hagan uso de la funcionalidad “**Ajustar configuración**” relacionada con la característica **Comprobación de la configuración de seguridad** de Internet Explorer. Si habilita esta configuración de directiva, los usuarios no pueden elegir la opción **Ajustar la configuración automáticamente** del menú contextual de la barra de información que aparece cuando Internet Explorer determina que la configuración no es segura.
  
La configuración **Impedir el uso de la funcionalidad “Ajustar configuración”** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
**Impedir la eliminación de archivos temporales de Internet y cookies**  
Esta configuración de directiva sirve para administrar las cookies y los archivos temporales de Internet asociados al historial de exploración en Internet y se encuentra disponible eligiendo **Herramientas-Opciones de Internet-Eliminar el historial de exploración** en Internet Explorer 7. Si habilita esta configuración de directiva, los usuarios no pueden eliminar las cookies ni los archivos temporales de Internet. Si deshabilita o no establece esta configuración de directiva, los usuarios pueden eliminar las cookies y los archivos temporales de Internet.
  
La configuración **Impedir la eliminación de archivos temporales de Internet y cookies** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**Desactivar la funcionalidad “Eliminar el historial de exploración”**  
Esta configuración de directiva impide que los usuarios hagan uso de la acción “**Eliminar el historial de exploración**” en Internet Explorer. Si habilita esta configuración de directiva, los usuarios no pueden ejecutar la acción “**Eliminar el historial de exploración**” de **Opciones de Internet** en Internet Explorer 7. Sin embargo, si la deshabilita o no la configura, los usuarios sí pueden realizar la acción “**Eliminar el historial de exploración**” de **Opciones de Internet** en Internet Explorer 7.
  
La configuración **Desactivar la funcionalidad “Eliminar el historial de exploración”** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**Desactivar la característica de comprobación de la configuración de seguridad**  
Esta configuración de directiva desactiva la característica **Comprobación de la configuración de seguridad**, que se encarga de comprobar la configuración de seguridad de Internet Explorer con el fin de determinar si entraña algún riesgo. Si habilita esta configuración de directiva, no se lleva a cabo ninguna comprobación de la configuración de seguridad. Si la deshabilita, se lleva a cabo la comprobación de la configuración de seguridad. Si no configura este valor de directiva, el usuario puede cambiar la configuración “**Deshabilitar la comprobación de la configuración de seguridad**”.
  
La configuración **Desactivar la característica de comprobación de la configuración de seguridad** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
**Activar la característica Autocompletar para nombres de usuario y contraseñas en formularios**  
Esta configuración de directiva deshabilita el relleno automático de los nombres de usuario y las contraseñas en formularios de páginas Web e impide que se pregunte al usuario si desea guardar las contraseñas. Si habilita esta configuración de directiva, se atenúan las casillas de verificación **Nombres de usuario y contraseñas en formularios** y **Preguntar si se guardan las contraseñas**. Además, se impide que los usuarios guarden las contraseñas en una ubicación local.
  
El valor **Activar la característica Autocompletar para nombres de usuario y contraseñas en formularios** se configura como **Deshabilitado** en los dos entornos que se describen en esta guía.
  
En **Configuración de equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer** se configuran estas otras secciones:
  
-   [Menús del explorador](#_browser_menus)
  
-   [Panel de control Internet](#_internet_control_panel)
  
-   [Panel de control Internet\\Página Opciones avanzadas](#_internet_control_panel-advanced)
  
-   [Panel de control Internet\\Página Seguridad](#_internet_control_panel-security)
  
-   [Panel de control Internet\\Página Seguridad\\Zona Internet](#_security_page_internet_1)
  
-   [Panel de control Internet\\Página Seguridad\\Zona de sitios restringidos](#_internet_control_pane-security)
  
-   [Páginas sin conexión](#_offline_pages)
  
###### Menús del explorador
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Menús del explorador**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A65. Configuración recomendada de menús del explorador**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la opción Guardar este programa en disco</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Deshabilitar la opción Guardar este programa en disco**  
Esta configuración de directiva impide que los usuarios guarden en el disco duro un programa o un archivo que haya descargado Internet Explorer. Si habilita esta configuración de directiva, los usuarios no pueden guardar los programas en el disco mediante la opción **Guardar este programa en disco**. El archivo de programa no se descarga y se informa al usuario de que el comando no se encuentra disponible. Esta configuración de directiva ayuda a proteger los entornos SSLF ya que los usuarios no pueden descargar con Internet Explorer programas nocivos en potencia y guardarlos en el disco.
  
El valor **Deshabilitar la opción Guardar este programa en disco** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
###### Panel de control Internet
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Panel de control Internet**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A66. Configuración de usuario recomendada para el panel de control Internet de Internet Explorer**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la página Opciones avanzadas</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la página Seguridad</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Impedir omitir errores de certificado</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
**Deshabilitar la página Opciones avanzadas**  
Esta configuración de directiva funciona junto con otras configuraciones para que los usuarios no puedan cambiar los valores de la ficha **Opciones avanzadas** de Internet Explorer.
  
El valor **Deshabilitar la página Opciones avanzadas** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Deshabilitar la página Seguridad**  
Esta configuración de directiva funciona conjuntamente con otros parámetros para que los usuarios no puedan cambiar los valores que se configuran a través de Directiva de grupo. Con esta configuración de directiva se quita la ficha **Seguridad** del cuadro de diálogo **Opciones de Internet**. Si habilita esta configuración de directiva, los usuarios no pueden ver ni cambiar parámetros de las zonas de seguridad tales como las secuencias de comandos, las descargas y la autenticación de usuarios. Microsoft recomienda habilitar esta configuración de directiva para que los usuarios no puedan cambiar parámetros y debilitar otras opciones de configuración de seguridad de Internet Explorer.
  
El valor **Deshabilitar la página Seguridad** se configura como **Habilitado** sólo en el entorno SSLF. En cambio, se establece en **Sin configurar** en el entorno EC.
  
**Impedir omitir errores de certificado**  
Si se generan errores de certificados de TLS/SSL como “caducado”, “revocado” o “nombres que no coinciden”, Internet Explorer impide al usuario continuar la exploración del sitio Web. Si esta configuración de directiva se habilita, el usuario no puede seguir explorando el sitio Web. Si la deshabilita o no la configura, el usuario puede optar por hacer caso omiso de los errores de certificado y continuar con la exploración.
  
La configuración **Impedir omitir errores de certificado** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
###### Panel de control Internet\\Página Opciones avanzadas
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A67. Configuración recomendada de la página Opciones avanzadas**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">§ Permitir instalación a petición (Internet Explorer)</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Permitir que el software se ejecute o instale incluso si la firma no es válida</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Comprobar automáticamente si hay actualizaciones de Internet Explorer</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Comprobar la revocación del certificado del servidor</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
**Permitir instalación a petición (Internet Explorer)**  
Esta configuración de directiva permite decidir si los usuarios pueden descargar e instalar de manera automática **componentes de Web** (por ejemplo, fuentes) susceptibles de instalación con **Instalación activa de Internet Explorer**. Por ejemplo, si abre una página Web que requiere compatibilidad con caracteres japoneses, Internet Explorer pide al usuario que descargue el componente de **Language Pack en japonés** si no está instalado.
  
Si habilita esta configuración de directiva, los **componentes de Web** (como las fuentes) se instalan de forma automática cuando sea necesario. Si deshabilita esta configuración de directiva, se pide la intervención de los usuarios cuando sea necesario descargar **componentes de Web** como, por ejemplo, fuentes. Si no configura esta directiva, se pide la intervención de los usuarios cuando sea necesario descargar **componentes de Web** como, por ejemplo, fuentes.
  
La configuración **Permitir instalación a petición (Internet Explorer)** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
**Permitir que el software se ejecute o instale incluso si la firma no es válida**  
Esta configuración de directiva permite controlar si los usuarios pueden instalar o ejecutar software (como controles ActiveX y descargas de archivos) aunque la firma no sea válida. Una firma no válida podría indicar que el archivo está manipulado.
  
Si habilita esta configuración de directiva, se pregunta a los usuarios si desean instalar o ejecutar los archivos que carezcan de una firma válida. Si la deshabilita, los usuarios no pueden instalar ni ejecutar archivos sin firma válida. Si no configura esta directiva, los usuarios no pueden instalar ni ejecutar archivos sin firma válida.
  
La configuración **Permitir que el software se ejecute o instale incluso si la firma no es válida** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
**Comprobar automáticamente si hay actualizaciones de Internet Explorer**  
Esta configuración de directiva sirve para administrar si Internet Explorer busca en Internet versiones nuevas. Al establecer Internet Explorer de modo que lleve a cabo esta acción, las comprobaciones tienen lugar cada 30 días más o menos y se insta a los usuarios a que instalen las nuevas versiones en cuanto se encuentren disponibles.
  
Si habilita esta configuración de directiva, Internet Explorer comprueba en Internet si existe alguna versión nueva cada 30 días aproximadamente y, si la encuentra, invita al usuario a descargarla. Si deshabilita esta configuración, Internet Explorer no realiza dicha comprobación, por lo que no se pide al usuario que instale nada. Si no configura este valor, Internet Explorer no realiza dicha comprobación, por lo que tampoco se pide al usuario que instale nada.
  
La configuración **Comprobar automáticamente si hay actualizaciones de Internet Explorer** se establece en **Sin configurar** en el entorno EC y en **Deshabilitado** en el entorno SSLF.
  
**Comprobar la revocación del certificado del servidor**  
Esta configuración de directiva sirve para administrar si Internet Explorer comprueba el estado de revocación de los certificados de los servidores. Los certificados se revocan cuando su seguridad está en entredicho o se quedan sin validez; esta opción protege a los usuarios en el sentido de que les impide enviar datos confidenciales a sitios que puedan ser fraudulentos o que no sean seguros.
  
Si habilita esta configuración de directiva, Internet Explorer comprueba si los certificados de servidor están revocados. Si la deshabilita, Internet Explorer no lleva a cabo esa comprobación. Si no configura este valor, Internet Explorer tampoco lleva a cabo la comprobación.
  
La configuración **Comprobar si se revocó certificado de servidor** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
###### Panel de control Internet\\Página Seguridad
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Panel de control Internet\\Página Seguridad**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A68. Configuración recomendada de la página Seguridad**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sitio de intranet: incluir todas las rutas de red (UNCs)</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
</tbody>
</table>
  
**Sitio de intranet: incluir todas las rutas de red (UNCs)**  
Esta configuración de directiva controla si las URL que representan UNC están asignadas en la zona de seguridad de la intranet local. Si habilita esta configuración de directiva, todas las rutas de red se asignan en la **zona de intranet**. Si la deshabilita, no es necesario que todas las rutas de red se asignen en la **zona de intranet** (la asignación se puede realizar con otras reglas).
  
Si no establece esta configuración de directiva, los usuarios deciden si las rutas de red se asignan en la **zona de intranet**.
  
La configuración **Sitios de intranet: incluir todas las rutas de red (UNCs)** se establece en **Deshabilitado** en el entorno SSLF y en **Sin configurar** en el entorno EC.
  
###### Panel de control Internet\\Página Seguridad\\Zona Internet
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Panel de control Internet\\Página Seguridad\\Zona Internet**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Nota**   Los valores de configuración de las zonas de Internet y de sitios restringidos son muy parecidos. A continuación se describen las configuraciones de ambas zonas.
  
**Tabla A69. Configuración recomendada de la zona Internet**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Tener acceso a origen de datos entre dominios</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Permitir arrastrar y colocar o copiar y pegar archivos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Permitir la descarga de fuentes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Permitir la instalación de los elementos de escritorio</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Permitir operaciones de cortar, copiar o pegar desde el portapapeles mediante scripts</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Permitir que se abran ventanas iniciadas por scripts sin ninguna restricción de tamaño o posición</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Zona Internet\Permitir actualizaciones de barra de estado a través de scripts</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Preguntar automáticamente si se debe descargar un archivo</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Descargar los controles ActiveX firmados</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Descargar los controles ActiveX sin firmar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Inicializar y activar los scripts de los controles de ActiveX no marcados como seguros</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Permisos de Java</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar Java</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Ejecutar aplicaciones y archivos en IFRAME</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Opciones para el inicio de sesión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Preguntar por el nombre de usuario y la contraseña</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Navegar entre los submarcos de dominios distintos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Abrir archivos basándose en el contenido, no en la extensión de archivo</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Permisos de canal de software</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Seguridad alta</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona Internet\Usar el bloqueador de elementos emergentes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona Internet\Los sitios Web en zonas de contenido Web con menores privilegios pueden navegar en esta zona</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
###### Panel de control Internet\\Página Seguridad\\Zona de sitios restringidos
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Panel de control Internet\\Página Seguridad\\Zona de sitios restringidos**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Nota**   Los valores de configuración de las zonas de Internet y de sitios restringidos son muy parecidos. A continuación se describen las configuraciones de ambas zonas.
  
**Tabla A70. Configuración recomendada de la zona de sitios restringidos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Tener acceso a origen de datos entre dominios</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir Active scripting</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir los comportamientos de binarios y secuencias de comandos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir operaciones de cortar, copiar o pegar desde el portapapeles mediante scripts</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir arrastrar y colocar o copiar y pegar archivos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir la descarga de archivos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir la descarga de fuentes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir la instalación de los elementos de escritorio</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir META REFRESH</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permitir que se abran ventanas iniciadas por scripts sin ninguna restricción de tamaño o posición</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">§ Zona de sitios restringidos\Permitir actualizaciones de barra de estado a través de scripts</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Preguntar automáticamente si se debe descargar un archivo</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Descargar los controles ActiveX firmados</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Descargar los controles ActiveX sin firmar</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Inicializar y activar los scripts de los controles de ActiveX no marcados como seguros</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permisos de Java</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar Java</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Ejecutar aplicaciones y archivos en IFRAME</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Opciones para el inicio de sesión</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Inicio de sesión anónimo</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Navegar entre los submarcos de dominios distintos</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Abrir archivos basándose en el contenido, no en la extensión de archivo</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Ejecutar componentes que dependen de .NET Framework sin firma de Authenticode</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Ejecutar componentes que dependen de .NET Framework firmados con Authenticode</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Ejecutar los controles y complementos para ActiveX</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Generar scripts de los controles ActiveX marcados como seguros para scripting</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Scripting de applets de Java</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Permisos de canal de software</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Seguridad alta</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Zona de sitios restringidos\Usar el bloqueador de elementos emergentes</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Habilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Zona de sitios restringidos\Los sitios Web en zonas de contenido Web con menores privilegios pueden navegar hacia esta zona</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado: Deshabilitar</td>
</tr>
</tbody>
</table>
  
**§**: indica configuraciones nuevas de la directiva de grupo en Windows Vista.
  
**Tener acceso a origen de datos entre dominios**  
Esta configuración de directiva permite decidir si Internet Explorer tiene acceso a los datos de otras zonas de seguridad mediante Microsoft XML Parser (MSXML) o ActiveX Data Objects (ADO).
  
Si habilita esta configuración de directiva, los usuarios pueden cargar páginas de la zona que use MSXML o ADO con el fin de tener acceso a los datos de otro sitio de la zona. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la carga de la página en cuestión en la zona que use MSXML o ADO para obtener acceso a los datos de otro sitio de la zona.
  
Si deshabilita esta configuración de directiva, los usuarios no pueden cargar páginas de la zona que use MSXML o ADO con el fin de tener acceso a los datos de otro sitio de la zona.
  
Si no establece esta configuración de directiva, los usuarios no pueden cargar páginas de la zona que use MSXML o ADO con el fin de tener acceso a los datos de otro sitio de la zona.
  
La configuración **Tener acceso a origen de datos entre dominios** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir Active scripting**  
Esta configuración de directiva sirve para administrar si se ejecuta código de scripts en las páginas de la zona. Si habilita esta configuración de directiva, el código de scripts que aparezca en las páginas de la zona se puede ejecutar de manera automática. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la ejecución de código de scripts en las páginas de la zona. Si deshabilita esta configuración de directiva, se impide la ejecución del código de scripts que aparezca en las páginas de la zona. Si no la configura, también se impide la ejecución del código de scripts que aparezca en las páginas de la zona.
  
La configuración **Permitir Active scripting** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Permitir los comportamientos de binarios y secuencias de comandos**  
Esta configuración de directiva permite administrar los comportamientos de binarios y scripts dinámicos, que son componentes que encapsulan la funcionalidad específica de los elementos HTML a los que están conectados. Si habilita esta configuración de directiva, los comportamientos de binarios y scripts se encuentran disponibles. Si selecciona **Aprobado por el administrador** en el cuadro desplegable, sólo se hallan disponibles los comportamientos que figuran en **Comportamientos aprobados por el administrador**, en la directiva **Restricción de seguridad del comportamiento de binarios**.
  
Si deshabilita esta configuración de directiva, los comportamientos de binarios y scripts no están disponibles a menos que las aplicaciones implementen algún administrador de seguridad personalizado. Si no la configura, los comportamientos de binarios y scripts tampoco están disponibles a menos que las aplicaciones implementen algún administrador de seguridad personalizado.
  
La configuración **Permitir los comportamientos de binarios y secuencias de comandos** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Permitir operaciones de cortar, copiar o pegar desde el portapapeles mediante scripts**  
Esta configuración de directiva permite decidir si los scripts pueden realizar operaciones del Portapapeles (por ejemplo, cortar, copiar y pegar) en las zonas especificadas. Si habilita esta configuración de directiva, los scripts pueden llevar a cabo operaciones con el Portapapeles. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir las operaciones con el Portapapeles. Si deshabilita esta configuración de directiva, los scripts no pueden llevar a cabo operaciones con el Portapapeles. Si no la configura, los scripts tampoco pueden llevar a cabo operaciones con el Portapapeles.
  
La configuración **Permitir operaciones de cortar, copiar o pegar desde el portapapeles mediante scripts** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir arrastrar y colocar o copiar y pegar archivos**  
Esta configuración de directiva permite administrar si los usuarios pueden arrastrar archivos o bien copiarlos desde algún origen de la zona. Si habilita esta configuración de directiva, los usuarios pueden arrastrar archivos de la zona o bien copiarlos de ella y pegarlos en el destino elegido de forma automática. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir el arrastre o la copia de archivos de la zona. Si deshabilita esta configuración de directiva, se impide a los usuarios arrastrar archivos desde la zona o bien copiarlos de ella y pegarlos en el destino elegido.
  
Si no la configura, se pregunta a los usuarios si desean permitir el arrastre o la copia de archivos de la zona.
  
La configuración **Permitir arrastrar y colocar o copiar y pegar archivos** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir la descarga de archivos**  
Esta configuración de directiva sirve para administrar si se permiten descargas de archivos desde la zona. La opción está condicionada por la zona de la página donde aparezca el vínculo que permite iniciar la descarga, no por la zona desde donde se entregue el archivo. Si habilita esta configuración de directiva, se pueden descargar archivos de la zona. Si deshabilita esta configuración de directiva, se impide la descarga de archivos desde la zona. Si no la configura, también se impide la descarga de archivos desde la zona.
  
La configuración **Permitir la descarga de archivos** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Permitir la descarga de fuentes**  
Esta configuración de directiva sirve para administrar si las páginas de la zona pueden descargar fuentes HTML.
  
Si habilita esta configuración de directiva, se pueden descargar fuentes HTML de la zona de manera automática. Si habilita esta configuración de directiva y selecciona Preguntar en el cuadro desplegable, se pregunta a los usuarios si desean permitir la descarga de fuentes HTML. Si deshabilita esta configuración de directiva, se impide la descarga de fuentes HTML. Si no la configura, se pregunta a los usuarios si desean permitir la descarga de fuentes HTML.
  
La configuración **Permitir la descarga de fuentes** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir la instalación de los elementos de escritorio**  
Esta configuración de directiva sirve para administrar si los usuarios pueden instalar elementos de Active Desktop desde la zona. Éstos son los valores posibles para la configuración:
  
**Habilitar**: los usuarios pueden instalar de forma automática elementos de escritorio desde la zona.
  
**Preguntar**: se pregunta a los usuarios si desean instalar elementos de escritorio desde la zona.
  
**Deshabilitar**: se impide a los usuarios la instalación de elementos de escritorio desde la zona.
  
Si no establece esta configuración de directiva, se impide a los usuarios instalar elementos de escritorio desde la zona.
  
La configuración **Permitir la instalación de los elementos de escritorio** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir META REFRESH**  
Esta configuración de directiva permite decidir si el explorador acata las instrucciones de las páginas Web en caso de que su autor use un valor de **Meta Refresh** a fin de redirigir los exploradores a otras páginas. Al habilitar esta configuración de directiva, si el explorador del usuario carga alguna página que contenga un valor activo de **Meta Refresh**, se permite su redirección a otra página Web. Al deshabilitarla, si el explorador del usuario carga alguna página que contenga un valor activo de **Meta Refresh**, se impide su redirección a otra página Web. Si no se configura y el explorador del usuario carga alguna página que contenga un valor activo de **Meta Refresh**, se impide su redirección a otra página Web.
  
La configuración **Permitir META REFRESH** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Permitir que se abran ventanas iniciadas por scripts sin ninguna restricción de tamaño o posición**  
Esta configuración de directiva permite administrar las restricciones impuestas a las ventanas emergentes iniciadas por scripts así como a las ventanas que incluyan barras de título y estado. Si habilita esta configuración de directiva, no se aplica la opción de seguridad **Restricciones para ventanas** en la zona. La zona de seguridad se ejecuta sin la capa agregada de seguridad que brinda esta característica. Si deshabilita esta configuración de directiva, no cabe la posibilidad de ejecutar las posibles acciones dañinas que puedan contener las ventanas emergentes iniciadas por scripts y las ventanas con barras de título y estado. Esta característica de seguridad de Internet Explorer se encuentra activada en la zona según indique la configuración de control de la característica **Restricciones de seguridad de ventanas con secuencias de comandos** para el proceso. Si no configura este valor de directiva, no cabe la posibilidad de ejecutar las posibles acciones dañinas que puedan contener las ventanas emergentes iniciadas por scripts y las ventanas con barras de título y estado. Esta característica de seguridad de Internet Explorer se encuentra activada en la zona según indique la configuración de control de la característica **Restricciones de seguridad de ventanas con secuencias de comandos** para el proceso.
  
La configuración **Permitir que se abran ventanas iniciadas por scripts sin ninguna restricción de tamaño o posición** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permitir actualizaciones de barra de estado a través de scripts**  
Esta configuración de directiva sirve para administrar si se permite a los scripts actualizar la barra de estado en la zona. Si habilita esta configuración de directiva, los scripts pueden actualizar la barra de estado. Si la deshabilita, los scripts no pueden actualizar la barra de estado. Si no configura este valor de directiva, se deshabilita la actualización de la barra de estado mediante scripts.
  
La configuración **Permitir actualizaciones de barra de estado a través de scripts** se establece en **Deshabilitado** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Preguntar automáticamente si se debe descargar un archivo**  
Esta configuración de directiva determina si se pregunta a los usuarios si desean permitir descargas de archivos que no hayan iniciado ellos mismos. Sea cual sea el valor elegido, ante el usuario se presenta un cuadro de diálogo de descarga de archivos o bien de descarga iniciada por el usuario. Si habilita esta configuración, el usuario ve un cuadro de diálogo de descarga de archivos cuando se intente realizar una descarga automática.
  
Si deshabilita o no configura este valor, se bloquean las descargas de archivos que no haya iniciado el usuario; además, aparece la **barra de información** en lugar del cuadro de diálogo de descarga de archivos. Si lo desea, el usuario puede hacer clic en la **barra de información** para permitir la descarga del archivo en cuestión.
  
La configuración **Preguntar automáticamente si se debe descargar un archivo** se establece en **Habilitado: Habilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Descargar los controles ActiveX firmados**  
Esta configuración de directiva permite administrar si los usuarios pueden descargar controles ActiveX firmados desde las páginas de la zona. Si habilita esta directiva, los controles firmados se descargan sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la descarga de controles firmados por editores que no son de confianza. Todo código cuya firma corresponda a editores de confianza se descarga de forma silenciosa. Si establece esta configuración de directiva en **Deshabilitar**, los controles firmados no se pueden descargar.
  
Si no la configura, se pregunta a los usuarios si desean permitir la descarga de controles firmados por editores que no son de confianza. Todo código cuya firma corresponda a editores de confianza se descarga de forma silenciosa.
  
La configuración **Descargar los controles ActiveX firmados** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Descargar los controles ActiveX sin firmar**  
Esta configuración de directiva permite administrar si los usuarios pueden descargar controles ActiveX sin firmar desde la zona. Dicho código puede entrañar graves riesgos, en especial si procede de alguna zona que no sea de confianza.
  
Si habilita esta configuración de directiva, los controles sin firmar se pueden ejecutar sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la ejecución de controles sin firmar. Si deshabilita esta configuración de directiva, los usuarios no pueden ejecutar controles sin firmar. Si no la configura, los usuarios tampoco pueden ejecutar controles sin firmar.
  
La configuración **Descargar los controles ActiveX sin firmar** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Inicializar y activar los scripts de los controles de ActiveX no marcados como seguros**  
Esta configuración de directiva permite administrar los controles ActiveX que no están marcados como seguros. Si habilita esta configuración de directiva, los controles ActiveX se ejecutan, se cargan con parámetros y generan scripts sin establecer ningún tipo de seguridad de objetos para los datos o los scripts que no sean de confianza. No se recomienda habilitar esta configuración salvo en zonas seguras y administradas. Este valor provoca que se inicialicen controles y se activen scripts tanto seguros como no seguros y que se omita el valor de la opción **Generar scripts de los controles ActiveX marcados como seguros para scripting**.
  
Si habilita esta configuración de directiva y selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la carga del control con parámetros o la activación de sus scripts.
  
Si deshabilita esta configuración de directiva, no se cargan con parámetros los controles ActiveX cuya seguridad no se pueda garantizar ni se generan los scripts correspondientes. Si no la configura, tampoco se cargan con parámetros los controles ActiveX cuya seguridad no se pueda garantizar ni se generan scripts.
  
La configuración **Inicializar y activar los scripts de los controles de ActiveX no marcados como seguros** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Permisos de Java**  
Esta configuración de directiva permite administrar los permisos para los applets de Java. Si habilita esta configuración de directiva, puede seleccionar una de las opciones disponibles en el cuadro desplegable. **Personalizado**: permite controlar la configuración de cada uno de los permisos por separado. **Seguridad baja**: permite que los applets realicen cualquier operación**. Seguridad media**: permite que los applets se ejecuten en su recinto (un área de la memoria fuera de la cual el programa no puede realizar llamadas), además de ofrecer capacidades como el espacio de desecho (una zona segura de almacenamiento en el equipo cliente) o E/S de archivos controlada por el usuario. **Seguridad alta**: permite que los applets se ejecuten en su recinto. Deshabilitar Java: impide la ejecución de todos los applets. Si deshabilita esta configuración de directiva, los applets de Java no pueden ejecutarse. Si no configura este valor de directiva, el permiso se establece en **Seguridad alta**.
  
La configuración **Permisos de Java** se establece en **Habilitado: Deshabilitar Java** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Ejecutar aplicaciones y archivos en IFRAME**  
Esta configuración de directiva permite decidir si se pueden ejecutar aplicaciones y descargar archivos desde una referencia IFRAME del código HTML de las páginas de la zona. Si habilita esta configuración de directiva, se pueden ejecutar aplicaciones y descargar archivos de IFRAME de las páginas de la zona sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la ejecución de aplicaciones o la descarga de archivos de IFRAME de las páginas de la zona.
  
Si deshabilita esta configuración de directiva, se impide tanto la ejecución de aplicaciones como la descarga de archivos de IFRAME de las páginas de la zona. Si no la configura, se pregunta a los usuarios si desean permitir la ejecución de aplicaciones o la descarga de archivos de IFRAME de las páginas de la zona.
  
La configuración **Ejecutar aplicaciones y archivos en IFRAME** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Opciones para el inicio de sesión**  
Esta configuración de directiva permite administrar la configuración de opciones para el inicio de sesión. Si habilita esta configuración de directiva, puede seleccionar cualquiera de estas opciones para el inicio de sesión:
  
**Inicio de sesión** **anónimo**: deshabilita la autenticación HTTP y usa la cuenta de invitado sólo para el protocolo de Sistema de archivos Internet comunes (CIFS).
  
**Preguntar por el nombre de usuario y la contraseña**: solicita al usuario que especifique su identificador y su contraseña. Después de formular la pregunta al usuario, estos valores se usan de forma silenciosa para el resto de la sesión.
  
**Inicio de sesión automático sólo en la zona de intranet**: solicita al usuario que especifique su identificador y su contraseña en las demás zonas. Después de formular la pregunta al usuario, estos valores se usan de forma silenciosa para el resto de la sesión.
  
**Inicio de sesión automático con el nombre de usuario y contraseña actuales**: intenta iniciar sesión con el método de respuesta de desafío de Windows NT (también conocido como autenticación NTLM). Si el servidor admite la respuesta de desafío de Windows NT, se emplean el nombre y la contraseña del usuario para iniciar la sesión. Si el servidor no admite esta autenticación, se solicita al usuario que proporcione un nombre de usuario y una contraseña.
  
Si deshabilita esta configuración de directiva, el inicio de sesión se establece en **Inicio de sesión automático sólo en la zona de intranet**. Si no la configura, el inicio de sesión también se establece en **Inicio de sesión automático sólo en la zona de intranet**.
  
La configuración **Opciones para el inicio de sesión** se establece en **Habilitado: Preguntar por el nombre de usuario y la contraseña** en el entorno SSLF para **Zona Internet** y en **Habilitado: Inicio de sesión anónimo** para **Zona de sitios restringidos** .El valor es **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Navegar entre los submarcos de dominios distintos**  
Esta configuración de directiva permite administrar la apertura de submarcos así como el acceso de las aplicaciones de dominios distintos. Si habilita esta configuración de directiva, los usuarios pueden abrir submarcos desde otros dominios y obtener acceso a aplicaciones de esos otros dominios. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la aparición de submarcos o el acceso a aplicaciones de otros dominios.
  
Si deshabilita esta configuración de directiva, los usuarios no pueden abrir submarcos ni obtener acceso a aplicaciones de dominios diferentes. Si no la configura, los usuarios tampoco pueden abrir submarcos desde otros dominios ni obtener acceso a aplicaciones de esos otros dominios.
  
La configuración **Navegar entre los submarcos de dominios distintos** se establece en **Deshabilitado** en el entorno SSLF para **Zona Internet** y en **Habilitado: Deshabilitar** para **Zona de sitios restringidos** .El valor es **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Abrir archivos basándose en el contenido, no en la extensión de archivo**  
Esta configuración de directiva permite administrar el examen de MIME para cambiar los archivos de un tipo a otro tipo en función del examen realizado. El examen de MIME consiste en el reconocimiento por parte de Internet Explorer del tipo de archivo basándose en la firma de bits. Si habilita esta configuración de directiva, no se aplica la opción **Característica de seguridad de examen de MIME** en la zona. La zona de seguridad se ejecuta sin la capa agregada de seguridad que brinda esta característica. Si deshabilita esta configuración de directiva, se impide la ejecución de acciones que podrían resultar dañinas. Esta característica de seguridad de Internet Explorer se encuentra activada en la zona según indique la configuración de control de la característica para el proceso. Si no establece esta configuración de directiva, no se aplica la opción **Característica de seguridad de examen de MIME** en la zona.
  
La configuración **Abrir archivos basándose en el contenido,** **no en la extensión de archivo** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configura**r en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Ejecutar componentes que dependen de .NET Framework sin firma de Authenticode**  
Esta configuración de directiva permite administrar si se pueden ejecutar componentes de .NET Framework que no estén firmados con Authenticode® desde Internet Explorer. Entre otros componentes, se incluyen los controles administrados a los que se hace referencia en etiquetas de objetos así como los ejecutables administrados cuya referencia proviene de vínculos.
  
Si habilita esta configuración de directiva, Internet Explorer puede ejecutar componentes administrados que carezcan de firma. Si selecciona **Preguntar** en el cuadro desplegable, Internet Explorer pregunta al usuario si desea permitir la ejecución de componentes administrados sin firma. Si deshabilita esta configuración de directiva, Internet Explorer no ejecuta ningún componente administrado que carezca de firma. Si no la configura, Internet Explorer tampoco ejecuta ningún componente administrado que carezca de firma.
  
La configuración **Ejecutar componentes que dependen de .NET Framework sin firma de Authenticode** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Ejecutar componentes que dependen de .NET Framework firmados con Authenticode**  
Esta configuración de directiva permite administrar si se pueden ejecutar componentes de .NET Framework que estén firmados con Authenticode desde Internet Explorer. Entre otros componentes, se incluyen los controles administrados a los que se hace referencia en etiquetas de objetos así como los ejecutables administrados cuya referencia proviene de vínculos.
  
Si habilita esta configuración de directiva, Internet Explorer puede ejecutar componentes administrados que dispongan de firma. Si selecciona **Preguntar** en el cuadro desplegable, Internet Explorer pregunta al usuario si desea permitir la ejecución de componentes administrados con firma. Si deshabilita esta configuración de directiva, Internet Explorer no ejecuta ningún componente administrado firmado. Si no la configura, Internet Explorer tampoco ejecuta ningún componente administrado firmado.
  
La configuración **Ejecutar componentes que dependen de .NET Framework firmados con Authenticode** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Ejecutar los controles y complementos para ActiveX**  
Esta configuración de directiva permite administrar si se pueden ejecutar complementos y controles ActiveX de las páginas de la zona. Si habilita esta configuración de directiva, los controles y los complementos se pueden ejecutar sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la ejecución de controles o complementos. Si deshabilita esta configuración de directiva, se impide la ejecución de complementos y controles. Si no la configura, también se impide la ejecución de complementos y controles.
  
La configuración **Ejecutar los controles y complementos para ActiveX** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Generar scripts de los controles ActiveX marcados como seguros para scripting**  
Esta configuración de directiva permite decidir si los controles ActiveX marcados como seguros para la generación de scripts pueden interaccionar con scripts. Si habilita esta configuración de directiva, la interacción de los scripts puede tener lugar de forma automática sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir la interacción de los scripts. Si deshabilita o no establece esta configuración de directiva, se impide la interacción de los scripts.
  
La configuración **Generar scripts de los controles ActiveX marcados como seguros para scripting** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Scripting de applets de Java**  
Esta configuración de directiva sirve para administrar si los applets están expuestos para los scripts en la zona. Si habilita esta configuración de directiva, los scripts pueden tener acceso a los applets de forma automática sin intervención del usuario. Si selecciona **Preguntar** en el cuadro desplegable, se pregunta a los usuarios si desean permitir el acceso de los scripts a los applets. Si deshabilita o no establece esta configuración de directiva, se impide el acceso de los scripts a los applets.
  
La configuración **Scripting de applets de Java** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC para **Zona de sitios restringidos**.
  
**Permisos de canal de software**  
Esta configuración de directiva permite administrar los permisos de los canales de software. Si habilita esta configuración de directiva, puede seleccionar una de estas opciones del cuadro desplegable:
  
**Seguridad baja**: permite notificar al usuario las actualizaciones de software por correo electrónico así como descargar de forma automática paquetes de software a los equipos de los usuarios e instalarlos en ellos.
  
**Seguridad media**: permite notificar al usuario las actualizaciones de software por correo electrónico así como descargar de forma automática paquetes de software a los equipos de los usuarios pero no instalarlos.
  
**Seguridad alta**: impide la notificación al usuario de las actualizaciones de software por correo electrónico así como la descarga automática de paquetes de software a los equipos de los usuarios y su instalación.
  
Si deshabilita esta configuración de directiva, el permiso se establece en **Seguridad alta**.
  
La configuración **Permisos de canal de software** se establece en **Habilitado: Seguridad alta** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Usar el bloqueador de elementos emergentes**  
Esta configuración de directiva permite decidir si emergen las ventanas que no se deseen. No se bloquean las ventanas emergentes que se abren al hacer clic en un vínculo. Si habilita esta configuración de directiva, se impide la aparición de numerosas ventanas emergentes no deseadas. Si deshabilita esta configuración de directiva, no se impide la aparición de ventanas emergentes. Aunque no la configure, se impide la aparición de numerosas ventanas emergentes no deseadas.
  
La configuración **Usar el bloqueador de elementos emergentes** se establece en **Habilitado: Habilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
**Los sitios Web en zonas de contenido Web con menores privilegios pueden navegar hacia esta zona**  
Esta configuración de directiva permite administrar si los sitios Web de zonas con menos privilegios (por ejemplo, **Zona de sitios restringidos**) pueden navegar hasta la zona. Si habilita esta configuración de directiva, los sitios Web de zonas con menos privilegios pueden abrir nuevas ventanas de la zona o navegar hasta ellas. La zona de seguridad se ejecuta sin la capa agregada de seguridad que brinda la característica de seguridad **Protección contra elevación de zona**. Si selecciona **Preguntar** en el cuadro desplegable, el usuario recibe la advertencia de que la navegación quizá entrañe algunos riesgos.
  
Si deshabilita esta configuración de directiva, se impide toda navegación que conlleve posibles riesgos. Esta característica de seguridad de Internet Explorer se encuentra activada en la zona según establezca el control de la característica **Protección contra elevación de zona**. Si no establece esta configuración de directiva, los sitios Web de zonas con menos privilegios pueden abrir nuevas ventanas de la zona o navegar hasta ellas.
  
La configuración **Los sitios Web en zonas de contenido Web con menores privilegios pueden navegar hacia esta zona** se establece en **Habilitado: Deshabilitar** en el entorno SSLF y en **Sin configurar** en el entorno EC tanto para **Zona Internet** como para **Zona de sitios restringidos**.
  
###### Páginas sin conexión
  
Puede establecer esta configuración recomendada en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Internet Explorer\\Páginas sin conexión**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para Internet Explorer. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Nota   **Estos valores no se aplican a Internet Explorer 7. Sólo se configuran en el entorno EC porque puede incluir equipos en los que se ejecuta Windows XP con Internet Explorer 6.0.
  
**Tabla A71. Configuración recomendada de las páginas sin conexión**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Usuario de EC</th>
<th style="border:1px solid black;" >Usuario de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la posibilidad de agregar canales</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar todas las páginas sin conexión programadas</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilita totalmente la interfaz de usuario del canal</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilita la descarga del contenido de las suscripciones a sitios</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la edición y creación de grupos de programaciones</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la edición de programaciones para páginas sin conexión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la cuenta de visitas a la página sin conexión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Deshabilitar la posibilidad de quitar canales</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Deshabilitar la eliminación de programaciones para páginas sin conexión</td>
<td style="border:1px solid black;">Habilitado</td>
<td style="border:1px solid black;">Sin configurar</td>
</tr>
</tbody>
</table>
  
**Deshabilitar la posibilidad de agregar canales**  
Esta configuración de directiva impide a los usuarios agregar canales a Internet Explorer. Los canales son sitios Web que se actualizan automáticamente en los equipos en los que se ejecuta Internet Explorer, según una programación de actualizaciones especificada por el proveedor de canal. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática. Es aconsejable permitir al equipo la descarga de páginas de Internet sólo cuando el usuario la solicite.
  
Por ese motivo, la configuración **Deshabilitar la posibilidad de agregar canales** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión**  
Esta configuración de directiva impide a los usuarios especificar que las páginas Web se puedan descargar y ver sin conexión. Esa capacidad permitiría a los usuarios ver páginas Web cuando sus equipos no están conectados a Internet.
  
La configuración **Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar todas las páginas sin conexión programadas**  
Esta configuración de directiva deshabilita las programaciones que se hayan configurado para descargar páginas Web destinadas a la visualización sin conexión. Si habilita esta directiva, se desactivarán las casillas de verificación correspondientes a las programaciones en la ficha **Programación** del cuadro de diálogo de **propiedades de la página Web** para impedir que los usuarios las seleccionen. Para que se muestre esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas**, **Sincronizar**, seleccionar una página Web y hacer clic en el botón **Propiedades** y en la ficha **Programación**. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
La configuración **Deshabilitar todas las páginas sin conexión programadas** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilita totalmente la interfaz de usuario del canal**  
Esta configuración de directiva impide que los usuarios vean la interfaz de la Barra de canales. Los canales son sitios Web que se actualizan automáticamente en los equipos, con una programación especificada por el proveedor de canal. Si habilita esta configuración de directiva, los usuarios no podrán tener acceso a la interfaz de la Barra de canales y activar la casilla de verificación **Barra de canales de Internet Explorer** en la ficha **Web** del cuadro de diálogo **Propiedades de Pantalla**. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
La configuración **Deshabilita totalmente la interfaz de usuario del canal** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilita la descarga del contenido de las suscripciones a sitios**  
Esta configuración de directiva impide a los usuarios descargar contenido de suscripciones de los sitios Web. Sin embargo, la sincronización del contenido de la página Web se sigue produciendo cuando el usuario vuelve a una página a la que tuvo acceso anteriormente para determinar si se ha actualizado algún contenido. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
La configuración **Deshabilita la descarga del contenido de las suscripciones a sitios** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la edición y creación de grupos de programaciones**  
Esta configuración de directiva impide a los usuarios agregar, editar o quitar programaciones para la revisión sin conexión de páginas Web y grupos de páginas Web a los que se suscriban. Un grupo de suscripción es una página Web favorita que incluye las páginas Web a las que está vinculada. Si habilita esta directiva, se atenúan los botones **Agregar**, **Quitar** y **Editar** de la ficha **Programación** del cuadro de diálogo **Propiedades de la página Web**. Para que se muestre esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas** y después **Sincronizar** en Internet Explorer, seleccionar una página Web, hacer clic en el botón **Propiedades** y después hacer clic en la ficha **Programación.** Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
Por ese motivo, la configuración **Deshabilitar la edición y creación de grupos de programaciones** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la edición de programaciones para páginas sin conexión**  
Esta configuración de directiva impide a los usuarios editar las programaciones que se hayan configurado para descargar páginas Web a fin de revisarlas sin conexión. Si habilita esta directiva, los usuarios no podrán hacer que se muestren las propiedades de programación de las páginas que han configurado para la revisión sin conexión. No se mostrará ninguna propiedad cuando los usuarios hagan clic en **Herramientas**, **Sincronizar** en Internet Explorer, seleccionen una página Web y después hacen clic en el botón **Propiedades.** Los usuarios no reciben ningún mensaje que indique que el comando no está disponible. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
La configuración **Deshabilitar la edición de programaciones para páginas sin conexión** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la cuenta de visitas a la página sin conexión**  
Esta configuración de directiva impide que los proveedores de canal puedan registrar la frecuencia con que los usuarios ven sus páginas de canal cuando están sin conexión. Esta configuración de directiva es uno de los parámetros que bloquean la capacidad de Internet Explorer para descargar contenido automáticamente.
  
La configuración **Deshabilitar la cuenta de visitas a la página sin conexión** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la posibilidad de quitar canales**  
Esta configuración de directiva impide que los usuarios deshabiliten la sincronización de canales en Internet Explorer. Es aconsejable permitir al equipo la descarga de páginas de Internet sólo cuando el usuario la solicite.
  
Por ese motivo, la configuración **Deshabilitar la posibilidad de quitar canales** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
**Deshabilitar la eliminación de programaciones para páginas sin conexión**  
Esta configuración de directiva impide a los usuarios que desactiven la configuración previa de las páginas Web con el fin de descargarlas para verlas sin conexión. Si habilita esta configuración de directiva, la configuración previa de las páginas Web se protege. Esta configuración de directiva es uno de los valores que bloquean la capacidad de Internet Explorer para descargar contenido de manera automática.
  
La configuración **Deshabilitar la eliminación de programaciones para páginas sin conexión** se establece en **Habilitado** en el entorno EC y en **Sin configurar** en el entorno SSLF.
  
###### Explorador de Windows
  
El Explorador de Windows se usa para examinar el sistema de archivos en equipos cliente en los que se ejecuta Windows Vista.
  
Puede establecer la configuración recomendada para los usuarios en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows**  
**\\Explorador de Windows**
  
La tabla siguiente resume los parámetros de configuración de usuario recomendados para el Explorador de Windows. En las subsecciones que siguen a la tabla se amplía la información acerca de cada configuración.
  
**Tabla A72. Configuración de usuario recomendada para el Explorador de Windows**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Equipo de EC</th>
<th style="border:1px solid black;" >Equipo de SSLF</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Quitar las características de grabación de CD</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Quitar la ficha Seguridad</td>
<td style="border:1px solid black;">Sin configurar</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
**Quitar las características de grabación de CD**  
Esta configuración de directiva quita las características integradas de Windows Vista que permiten a los usuarios grabar CDs con el Explorador de Windows. Windows Vista permite crear y modificar CDs regrabables si tiene una unidad de CD de lectura y escritura conectada al equipo. Esta característica se puede utilizar para copiar grandes cantidades de datos de un disco duro en un CD, que se puede extraer del equipo.
  
La configuración **Quitar las características de grabación de CD** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
**Nota**   Esta configuración de directiva no impide que las aplicaciones de terceros que usen la grabadora de CDs creen o modifiquen CDs. En esta guía se recomienda el uso de directivas de restricción de software para bloquear la creación o la modificación de CD desde aplicaciones de terceros.
  
Otra forma de impedir que los usuarios graben CD consiste en quitar las grabadoras de CD de los equipos cliente del entorno o reemplazarlas por unidades de CD de sólo lectura.
  
**Quitar la ficha Seguridad**  
Esta configuración de directiva deshabilita la ficha **Seguridad** en los cuadros de diálogo de propiedades de carpeta y de archivo en el Explorador de Windows. Si habilita esta configuración de directiva, los usuarios no podrán obtener acceso a la ficha **Seguridad** después de abrir el cuadro de diálogo **Propiedades** para todos los objetos de sistema de archivos, lo que incluye carpetas, archivos, accesos directos y unidades. Dado que la ficha **Seguridad** es inaccesible, los usuarios no pueden cambiar la configuración ni ver la lista de usuarios.
  
Por ello, la configuración **Quitar la ficha Seguridad** se establece en **Sin configurar** en el entorno EC y en **Habilitado** en el entorno SSLF.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
Los siguientes vínculos proporcionan información adicional acerca de estos temas de seguridad así como más detalles sobre los conceptos y las recomendaciones de seguridad que se ofrecen en esta guía de Windows Vista:
  
-   [Artículo sobre la configuración de un equipo para solucionar problemas de Firewall de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/operations/bfdeda55-46fc-4b53-b4cd-c71838ef4b41.mspx) (en inglés), en Microsoft TechNet®.
  
-   [Procedimiento de ocultación de un equipo Windows 2000 de la lista del examinador](http://support.microsoft.com/default.aspx?scid=321710) (en inglés), artículo 321710 de Knowledge Base.
  
-   “[Cómo impedir que los usuarios cambien una contraseña excepto cuando se les pida en Windows Server 2003](http://support.microsoft.com/default.aspx?scid=324744)”, artículo 324744 de Knowledge Base.
  
-   ["CÓMO Impedir que los usuarios cambien una contraseña excepto cuando se les pida](http://support.microsoft.com/default.aspx?scid=309799)”, artículo 309799 de Knowledge Base.
  
-   “[Habilitar el inicio de sesión automático en Windows XP](http://support.microsoft.com/default.aspx?scid=315231)”, artículo 315231 de Knowledge Base.
  
-   “[Cómo usar Directiva de grupo para configurar las opciones detalladas de auditoría de seguridad de los equipos cliente Windows Vista en un dominio de Windows Server 2003 o de Windows 2000](http://support.microsoft.com/kb/921469)”, artículo 921469 de Knowledge Base.
  
-   [Artículo sobre IIS 6.0 y las cuentas integradas](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx) (en inglés), en TechNet.
  
-   [Artículo sobre la posibilidad de usar las exenciones predeterminadas de IPsec para pasar por alto la protección IPsec en algunas situaciones](http://support.microsoft.com/default.aspx?scid=811832) (en inglés), artículo 811832 de Knowledge Base.
  
-   [Artículo sobre Outlook Web Access y Lugar de trabajo remoto en Web de Windows Small Business Server, cuyo funcionamiento impide el bloqueo de complementos del Service Pack 2 de XP habilitado con la directiva de grupo](http://support.microsoft.com/default.aspx?kbid=555235) (en inglés), artículo 555235 de Knowledge Base.
  
-   [Artículo sobre el instalador de paquetes (antes Update.exe) para sistemas operativos Microsoft Windows y componentes de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/deployment/winupdte.mspx) (en inglés), en TechNet.
  
-   [*Introducción a las amenazas y contramedidas*](http://go.microsoft.com/fwlink/?linkid=15159), capítulo 5, “Opciones de seguridad”.
  
-   [Información sobre Firewall de Windows](http://www.microsoft.com/windowsfirewall) (en inglés), en TechNet.
  
-   [Introducción a Windows Server Update Services](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx), en Microsoft.com.
  
-   [Microsoft Update](http://update.microsoft.com/), en Microsoft.com.
  
#### Soporte técnico y comentarios
  
El equipo Solution Accelerators: Security and Compliance (SASC) agradece sus ideas acerca de éste y otros aceleradores de soluciones.
  
Aporte sus observaciones en el grupo de noticias sobre [debates de seguridad](http://windowshelp.microsoft.com/communities/newsgroups/en-us/default.mspx?dg=microsoft.public.windows.vista.security&lang=en&cr=us&r=9dcac6a3-b8e7-4ba3-aa06-4e38b8ee9f35) disponible en el sitio Web para ayuda y soporte técnico de Windows Vista.
  
O envíe sus comentarios por correo electrónico a la dirección siguiente: [secwish@microsoft.com](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide).
  
Esperamos sus comentarios.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Consiga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)
  
[](#mainsection)[Principio de la página](#mainsection)
