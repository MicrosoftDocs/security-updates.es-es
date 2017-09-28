---
TOCTitle: 'Capítulo 3: Protección de datos confidenciales'
Title: 'Capítulo 3: Protección de datos confidenciales'
ms:assetid: '5bc7f568-b49e-400f-8584-efbec2f70bda'
ms:contentKeyID: 20105777
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb629455(v=MSDN.10)'
---

Capítulo 3: Protección de datos confidenciales
==============================================

### Capítulo 3: Protección de datos confidenciales

Publicado: noviembre 8, 2006

Cada año, miles de equipos que no cuentan con la protección adecuada acaban perdidos, robados o desechados de forma inapropiada en todo el mundo. La encuesta sobre seguridad y piratería informática realizada por el CSI/FBI en 2006 indica que los costos asociados a pérdidas de datos han experimentado un incremento del 65 por ciento durante el último año.

La inclusión de características y servicios tecnológicos eficientes para reducir los riesgos de robo y acceso no autorizado a los datos constituía una de las principales solicitudes de los clientes que Microsoft debía tener en cuenta durante el desarrollo de Windows Vista™. En parte, esto se debe a que los usuarios malintencionados pueden ejecutar un sistema operativo diferente en un equipo cliente, trasladar la unidad de disco a otro equipo o utilizar otros métodos de ataque sin conexión para obtener acceso a los datos en equipos robados o perdidos. En muchos casos, legislaciones y normas gubernamentales recientes destinadas a salvaguardar la privacidad y la información del consumidor han convertido la protección de datos en requisito legal.

Por estas razones de seguridad, Microsoft ha desarrollado características y servicios nuevos y mejorados para ayudar a las organizaciones a proteger con mayor eficacia los datos que residen en sus equipos cliente. Las características y los servicios descritos en este capítulo se han diseñado para proteger los datos en equipos cliente que ejecutan Windows Vista en el entorno de cliente de empresa (EC). La configuración de estas características dependerá de los requisitos y el entorno particulares. Este capítulo ofrece un proceso de diseño que le permitirá identificar el modo de configuración de las características y los servicios siguientes con el fin de satisfacer las necesidades de protección de datos en su empresa:

-   Cifrado de unidad BitLocker

-   Sistema de cifrado de archivos (EFS)

-   Servicios de Windows Rights Management (RMS)

-   Control de dispositivos

Puede utilizar BitLocker, EFS, RMS y el control de dispositivos para contribuir a la protección de datos confidenciales en la organización. Sin embargo, cada método y cada tecnología desempeñan funciones concretas en el terreno de la seguridad de los datos. De hecho, todos estos métodos y tecnologías son elementos complementarios de la protección de datos y Microsoft recomienda encarecidamente su uso como parte de la estrategia de seguridad global de la empresa. Puede utilizarlos de forma individual o conjunta, según sus requisitos de seguridad específicos. La tabla siguiente proporciona algunos ejemplos de la forma en que estos métodos y tecnologías ofrecen protección en diferentes situaciones empresariales.

**Tabla 3.1 Comparación de tecnologías de protección de datos en Windows Vista**

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
<th><p>Entorno</p></th>
<th><p>    BitLocker</p></th>
<th><p>        EFS</p></th>
<th><p>        RMS</p></th>
<th><p>Control de dispositivos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección de datos en equipos portátiles</p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protección de datos en servidores de sucursales</p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección local de archivos y carpetas de usuario único</p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protección de datos en equipos de escritorio</p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección de archivos y carpetas en equipos compartidos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protección remota de archivos y carpetas</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección de administrador de redes no confiables</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Aplicación de directivas de uso remoto para documentos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección del contenido durante desplazamientos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protección del contenido durante colaboraciones</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protección contra robo de datos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>          <img src="images/Bb629455.check(es-es,MSDN.10).gif" /></p></td>
</tr>
</tbody>
</table>
  
##### En esta página
  
[](#eeaa)[Cifrado de unidad BitLocker](#eeaa)  
[](#edaa)[Cifrado del sistema de archivos](#edaa)  
[](#ecaa)[Servicios de Windows Rights Management](#ecaa)  
[](#ebaa)[Control de dispositivos](#ebaa)  
[](#eaaa)[Más información](#eaaa)
  
### Cifrado de unidad BitLocker
  
El cifrado de unidad BitLocker™ contribuye a la protección de los datos en equipos cliente. Todo el volumen de Windows se presenta cifrado para evitar que usuarios no autorizados puedan anular medidas de protección del sistema y los archivos de Windows o conseguir acceso a los datos sin conexión en la unidad protegida. Nada más empezar el proceso de inicio, BitLocker comprueba la integridad del sistema y el hardware del equipo cliente. Si BitLocker encuentra que se ha intentado interferir con los datos o algún archivo, el equipo no completará el proceso de inicio.
  
BitLocker impide que un usuario malintencionado que inicia otro sistema operativo o que ejecuta una herramienta de ataque de software pueda omitir las medidas de protección de sistema y archivos de Windows Vista o conseguir acceso sin conexión a los archivos almacenados en la unidad protegida.
  
El cifrado de unidad BitLocker puede bloquear la secuencia de inicio normal hasta que el usuario proporcione un número de identificación personal (PIN) o inserte una unidad flash USB con las claves de descifrado correctas. El nivel de protección óptimo se obtiene cuando el equipo dispone de un Módulo de plataforma segura (TPM 1.2) para proteger los datos del usuario y reducir las posibilidades de manipulación del equipo cliente con Windows Vista cuando el sistema está desconectado. Para obtener información sobre la tecnología TPM, consulte las especificaciones y los materiales incluidos en el sitio Web de [Trusted Computing Group](http://www.trustedcomputinggroup.org/) (en inglés). Si no hay disponible ningún tipo de tecnología TPM, BitLocker continuará ofreciendo protección de datos, pero no se realizará la comprobación de la integridad del sistema.
  
BitLocker está disponible en las ediciones Enterprise y Ultimate del sistema operativo Windows Vista para equipos cliente.
  
**Nota**   BitLocker protege la partición de Windows y no sirve de reemplazo a EFS. BitLocker no cifra los datos almacenados fuera de la partición de Windows. Sin embargo, proporciona una capa de seguridad adicional para EFS al cifrar las claves de EFS en la partición de Windows.
  
#### Evaluación de riesgos
  
Los equipos portátiles suelen estar expuestos a entornos no seguros con grandes riesgos de pérdida o robo. Si un usuario malintencionado obtiene el control físico de un sistema, podrá omitir numerosas medidas de seguridad diseñadas para proteger los datos y el sistema. Los equipos de escritorio en entornos públicos o compartidos también tienen asociados riesgos considerables. El riesgo principal que BitLocker está diseñado para mitigar es la sustracción de datos de equipos portátiles robados o perdidos.
  
Cuando el atacante obtiene el acceso físico al equipo, las posibles consecuencias incluyen:
  
-   El atacante puede iniciar la sesión en Windows Vista y copiar archivos.
  
-   El atacante puede reiniciar el equipo cliente en un sistema operativo alternativo para:
  
    -   Ver nombres de archivos.
  
    -   Copiar archivos.
  
    -   Leer el contenido del archivo de hibernación o del archivo de paginación para descubrir copias de texto simple de documentos en proceso.
  
    -   Leer el contenido del archivo de hibernación para descubrir copias de texto simple de claves privadas de software.
  
Aunque los archivos estén cifrados con EFS, un usuario descuidado podría mover o copiar un archivo de una ubicación cifrada a una ubicación sin cifrar, lo que podría dejar la información del archivo en formato de texto simple. El personal de TI insuficientemente informado también podría descuidar el cifrado de carpetas ocultas, donde las aplicaciones guardan copias de seguridad de archivos en proceso. Además, hay que tener en cuenta los riesgos operativos, como la manipulación y la modificación de archivos de inicio y de sistema por parte de personal no autorizado, que podrían dar lugar a un funcionamiento incorrecto del sistema.
  
#### Reducción de riesgos
  
Para reducir estos riesgos, el equipo debería proteger la secuencia de inicio de forma que el sistema sólo se inicie cuando se disponga de la autorización debida. El sistema operativo y los archivos de datos deberían estar igualmente protegidos.
  
#### Consideraciones para la reducción de riesgos
  
BitLocker puede asistir en la reducción de los riesgos mencionados en la sección "Evaluación de riesgos". No obstante, antes de utilizar BitLocker, es importante considerar los requisitos y recomendaciones siguientes en relación con esta característica de protección de datos:
  
-   A fin de usar BitLocker con la configuración óptima, la placa base del equipo cliente debe proporcionar un chip TPM 1.2 que incluya una implementación de BIOS compatible con Trusted Computing Group. Además y, de forma opcional, se requiere una clave de inicio que proporcione un factor de autenticación suplementario. La clave de inicio es una clave física adicional (una unidad flash USB con una clave que pueda leer el equipo) o una entrada de PIN que establece el usuario. También se requieren protocolos de inicio de sesión y contraseña seguros.
  
-   Para utilizar BitLocker, deberá establecer correctamente una partición en el disco duro del equipo. El uso de BitLocker requiere dos volúmenes de unidad NTFS: uno para el volumen del sistema y otro para el volumen del sistema operativo. La partición del volumen del sistema debe tener un tamaño mínimo de 1,5 GB.
  
-   Las configuraciones de BitLocker que no aprovechan la autenticación de claves externas podrían verse afectadas por ataques basados en hardware.
  
-   Si utiliza BitLocker con una clave USB o un PIN, deberá establecer procedimientos que cubran las eventualidades de claves perdidas y números de identificación olvidados.
  
-   Aunque mínima, BitLocker tiene cierta influencia en el sistema que, por lo general, pasa desapercibida. No obstante, si el rendimiento del sistema es crítico (por ejemplo, en el caso de un servidor), pruebe la configuración minuciosamente para asegurarse de que la sobrecarga provocada por BitLocker no afecta al rendimiento de forma considerable.
  
-   Según el proveedor del equipo, es posible que las herramientas de administración TPM requieran algunos pasos manuales para configurar el estado del dispositivo TPM y una contraseña de administrador BIOS durante el proceso de generación, lo que podría impedir la automatización o la generación total de las implementaciones y las actualizaciones del sistema.
  
-   Para utilizar un dispositivo TPM, éste deberá tener aplicada una credencial de clave de aprobación (EK), proporcionada por el proveedor del equipo o un revendedor de valor añadido (VAR), o por el personal de TI con posterioridad a la entrega del sistema. La EK se debe almacenar de forma segura. Además, es necesario realizar un seguimiento de esta clave durante el uso del equipo.
  
-   Si TPM no está disponible en el sistema, el equipo debería admitir dispositivos USB para utilizar una clave de inicio con el fin de desbloquear el volumen durante la secuencia de inicio.
  
-   Es posible que BitLocker tenga algún efecto en los procedimientos de distribución del software si las actualizaciones del software o el sistema se distribuyen de forma remota por la noche y los equipos se reinician sin la presencia del usuario. Por ejemplo:
  
    -   Si el equipo tiene un tipo protector de TPM y PIN o de TPM y clave de inicio y, a las 2:00 a.m., implementa una actualización de software en el equipo que requiere el reinicio, el sistema no se iniciará sin el PIN o la clave de inicio.
  
    -   Si utiliza el modo Wake-on-LAN o una característica de encendido automático de BIOS para iniciar los equipos con fines de mantenimiento, estos equipos se verían igualmente afectados por un protector de TPM y PIN o clave de inicio.
  
-   Las actualizaciones de firmware BIOS/TPM distribuidas por fabricantes de equipos originales pueden afectar a equipos habilitados para BitLocker. Deberá revisar las instrucciones de instalación de los fabricantes de equipos originales para determinar si la información de recuperación (claves y contraseñas de recuperación) se conservará después de la actualización y si se mantendrán los protectores adicionales (PIN o claves de inicio).
  
-   Las actualizaciones de aplicaciones pueden afectar a equipos habilitados para BitLocker. Durante la instalación o la actualización, si las actualizaciones realizan cambios en el administrador o los archivos de inicio que utiliza BitLocker, se producirá un error de inicio del sistema y el equipo entrará en modo de recuperación. Antes de instalar o actualizar aplicaciones que afectan al entorno de inicio de Windows Vista, pruébelas en equipos habilitados para BitLocker.
  
-   Todos los controladores de dominio en el dominio deben ejecutar Microsoft® Windows Server® 2003 con Service Pack 1 (SP1) o una versión posterior.
  
    **Nota**   Windows Server 2003 requiere la ampliación del esquema para admitir el almacenamiento de la información de recuperación de BitLocker en el servicio de directorio de Active Directory®.
  
#### Proceso de reducción de riesgos
  
Use el proceso de reducción de riesgos siguiente para determinar la configuración óptima de BitLocker de modo que contribuya a la protección de datos confidenciales en los equipos cliente que administra.
  
**Para usar este proceso:**
  
1.  Estudie la tecnología BitLocker y sus capacidades.
  
    **Nota**   Para obtener más información acerca de BitLocker, consulte la página Web [Cifrado de unidad BitLocker](http://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) en Microsoft TechNet® (en inglés).
  
2.  Evalúe la necesidad de BitLocker en el entorno.
  
3.  Compruebe que el hardware, el firmware y el software de su organización cumplen los requisitos de BitLocker.
  
4.  Identifique los sistemas de la empresa que podrían beneficiarse de la protección que ofrece BitLocker.
  
5.  Identifique el nivel de protección que precisan sus sistemas. Es posible que necesite un PIN o una clave USB con claves de cifrado para iniciar el sistema operativo. El sistema operativo no se iniciará sin estas claves.
  
6.  Instale los controladores necesarios en un sistema de prueba.
  
7.  Use objetos de directiva de grupo (GPO) para configurar BitLocker en sistemas de prueba.
  
8.  Si las pruebas resultan satisfactorias, instale los controladores y configure BitLocker en los sistemas de producción.
  
##### Uso de la directiva de grupo en la reducción de riesgos para BitLocker
  
Hay dos plantillas de directiva de grupo que Microsoft recomienda para administrar la configuración de BitLocker. Estas plantillas permiten administrar la configuración de TPM de forma independiente al resto de BitLocker. La tabla siguiente proporciona información sobre la configuración de directiva de grupo disponible para BitLocker en la plantilla VolumeEncryption.admx. Puede establecer esta configuración en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Cifrado de unidad BitLocker**
  
**Tabla 3.2 Configuración del cifrado de unidad BitLocker**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar copia de seguridad de BitLocker en servicios de dominio de Active Directory</p></td>
<td style="border:1px solid black;"><p>Permite la copia de seguridad de la información de recuperación de BitLocker en Active Directory. Esta información incluye la contraseña de recuperación y algunos datos de identificación únicos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configuración del Panel de control: configurar carpeta de recuperación</p></td>
<td style="border:1px solid black;"><p>Determina si el Asistente para instalar BitLocker pedirá al usuario que guarde la clave de recuperación en una carpeta. Especifica la ruta predeterminada que se muestra cuando el Asistente para instalar BitLocker solicita al usuario que escriba la ubicación de la carpeta en la que desea guardar la clave de recuperación.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Configuración del Panel de control: configurar opciones de recuperación</p></td>
<td style="border:1px solid black;"><p>Determina si el Asistente para instalar BitLocker pedirá al usuario que cree una contraseña de recuperación. Esta contraseña es una secuencia de 48 dígitos generada de forma aleatoria.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configuración del Panel de control: habilitar opciones de inicio avanzadas</p></td>
<td style="border:1px solid black;"><p>Determina si el Asistente para instalar BitLocker pedirá al usuario que cree un PIN en el equipo. El PIN es una secuencia de 4 a 20 dígitos que el usuario debe escribir cada vez que se inicia el equipo. No es posible utilizar directivas para establecer el número de dígitos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Configurar método de cifrado</p></td>
<td style="border:1px solid black;"><p>Determina el algoritmo de cifrado y el tamaño de la clave que utiliza BitLocker. Esta configuración de directiva se aplica a discos completamente descifrados. Si el disco ya está cifrado o si el cifrado se está llevando a cabo, la modificación del método de cifrado no tendrá efecto alguno.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configurar perfil de validación de la plataforma TPM</p></td>
<td style="border:1px solid black;"><p>Determina el modo en que TPM protege la clave de cifrado del volumen de disco. Este parámetro de directiva no es aplicable si el equipo no cuenta con un TPM compatible. Además, la modificación de esta directiva no afecta de ningún modo a las copias existentes de la clave de cifrado.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
La tabla siguiente proporciona información sobre la configuración de directiva de grupo disponible para TPM en la plantilla TPM.admx. Puede establecer esta configuración en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Servicios de Módulo de plataforma segura**
  
**Tabla 3.3 Configuración de Módulo de plataforma segura**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar copia de seguridad de TPM en servicios de dominio de Active Directory</p></td>
<td style="border:1px solid black;"><p>Administra la copia de seguridad de la información de recuperación de TPM en Active Directory. Esta información incluye una derivación criptográfica de la contraseña de propietario de TPM.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configurar lista de comandos TPM bloqueados</p></td>
<td style="border:1px solid black;"><p>Administra la lista de directiva de grupo que enumera los comandos TPM bloqueados por Windows.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Omitir lista predeterminada de comandos TPM bloqueados</p></td>
<td style="border:1px solid black;"><p>Administra la aplicación de la lista predeterminada del equipo que enumera los comandos TPM bloqueados.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Omitir lista local de comandos TPM bloqueados</p></td>
<td style="border:1px solid black;"><p>Administra la aplicación de la lista local del equipo que enumera los comandos TPM bloqueados.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Las directivas de seguridad que utilice deberán ofrecer compatibilidad satisfactoria con la administración de claves y contraseñas de BitLocker. Estas directivas deben ser lo suficientemente completas como para proteger la información, sin llegar a ser tan restrictivas, pues dificultarían la compatibilidad con BitLocker. La lista incluida a continuación presenta algunos ejemplos de directivas:
  
-   Exija siempre la copia de seguridad de contraseñas de recuperación en Active Directory.
  
-   Exija siempre la copia de seguridad de la información de propietario de TPM en Active Directory.
  
-   Junto con las contraseñas de recuperación, haga uso de claves de recuperación como método de copia de seguridad o de recuperación alternativo.
  
-   Si utiliza TPM y un PIN o claves de inicio USB, asegúrese de renovar estos datos con frecuencia.
  
-   En equipos compatibles con TPM, utilice una contraseña de administrador BIOS para impedir el acceso.
  
-   Asegúrese de que los usuarios no almacenan información sobre claves (por ejemplo, claves de inicio USB) en el equipo.
  
-   Guarde las claves de recuperación en una ubicación central con fines de mantenimiento y recuperación de desastres.
  
-   Guarde copias de seguridad de los datos de recuperación en ubicaciones seguras de almacenamiento sin conexión.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Cifrado del sistema de archivos
  
Puede usar el sistema de cifrado de archivos (EFS) para cifrar archivos y carpetas como protección de los datos contra intentos de acceso no autorizado. EFS está integrado en el sistema de archivos NTFS y su funcionamiento es completamente transparente ante las aplicaciones. Cuando algún usuario o un programa tratan de obtener acceso a un archivo cifrado, de forma automática, el sistema operativo intenta obtener una clave de descifrado para el contenido. Seguidamente y, de forma silenciosa, realiza el cifrado y el descifrado en nombre del usuario. Los usuarios con claves autorizadas cuentan con acceso a los archivos cifrados y pueden trabajar con ellos del mismo modo que lo harían con cualquier otro archivo, mientras que el acceso de otros usuarios será denegado. Windows Vista incluye numerosas características nuevas de seguridad, rendimiento y administración relacionadas con EFS. Estas son algunas de ellas:
  
-   Es posible almacenar claves de usuario en tarjetas inteligentes.
  
-   Es posible almacenar claves de recuperación en tarjetas inteligentes, lo que permite la recuperación de datos seguros sin necesidad de recurrir a una estación de recuperación dedicada, incluso en sesiones de escritorio remoto.
  
-   Es posible cifrar el archivo de paginación de Windows mediante EFS con una clave generada durante el inicio del sistema. La clave se destruye al apagar el equipo.
  
-   Es posible cifrar la memoria caché de archivos sin conexión mediante EFS. En Windows Vista, esta característica de cifrado se sirve de la clave del usuario en lugar de usar la clave del sistema. De este modo, cada archivo en la memoria caché de archivos sin conexión sólo permanecerá accesible para el usuario en cuyo nombre se ha almacenado.
  
-   La directiva de grupo proporciona diversas opciones nuevas de configuración para asistir en la aplicación de directivas de empresa.
  
-   EFS admite una gama más amplia de claves y certificados de usuario.
  
Windows Vista incluye varias opciones nuevas de directiva de grupo para ayudar a los administradores a definir e implementar directivas organizativas para EFS. Estas opciones incluyen la capacidad de exigir tarjetas inteligentes para EFS y cifrado de archivos de página, determinar la longitud mínima de claves para EFS y requerir el cifrado de la carpeta Documentos del usuario.
  
**Nota**   Microsoft recomienda el uso conjunto de BitLocker y EFS para conseguir una protección óptima de los datos.
  
#### Evaluación de riesgos
  
El acceso no autorizado a los datos puede influir de forma negativa en los procesos y la rentabilidad de la empresa. Los riesgos son mayores en entornos donde varios usuarios disponen de acceso al mismo sistema o cuando se utilizan equipos portátiles. El riesgo principal que EFS está diseñado para mitigar es la sustracción de datos debida a la pérdida o el robo de equipos portátiles o al descubrimiento de la información por parte de usuarios internos a la organización. Los equipos compartidos también son vulnerables a este riesgo.
  
Cuando el atacante obtiene acceso físico a un equipo con datos sin cifrar, las posibles consecuencias incluyen:
  
-   El atacante puede reiniciar el equipo y elevar sus privilegios de usuario a administrador local para obtener acceso a los datos. El atacante podría descargar herramientas que le permitan obtener la contraseña del usuario mediante un ataque por fuerza bruta. De este modo, podrá iniciar la sesión en nombre del usuario y obtener acceso a sus datos.
  
-   El atacante podría tratar de iniciar la sesión en Windows Vista y copiar todos los datos disponibles en un dispositivo extraíble, enviarlos por correo electrónico, copiarlos a través de la red o transmitirlos mediante FTP a un servidor remoto.
  
-   El atacante podría reiniciar el equipo en un sistema operativo alternativo y copiar archivos directamente desde el disco duro.
  
-   El atacante podría conectar el equipo a otra red e iniciar la sesión en el equipo robado de forma remota.
  
-   Si el usuario almacena sus archivos de red en la memoria caché de archivos sin conexión, el atacante podría elevar sus privilegios a administrador del sistema local para inspeccionar el contenido de la memoria caché de archivos sin conexión.
  
-   Algún compañero de trabajo curioso podría abrir archivos confidenciales de otros usuarios en un equipo compartido.
  
-   El atacante podría reiniciar el equipo en un sistema operativo alternativo y leer el contenido del archivo de paginación para descubrir copias de texto simple de documentos en proceso.
  
#### Reducción de riesgos
  
Para reducir estos riesgos potenciales de acceso no autorizado a sus datos, puede cifrar la información al almacenarla en el disco duro. Las mejoras en la tecnología EFS de Windows Vista le ayudarán a resolver las situaciones siguientes:
  
-   Puede hacer uso de EFS para impedir que un atacante lea sus archivos cifrados a través de un sistema operativo alternativo al establecer como requisito que el atacante deba obtener una clave capaz de descifrar el contenido. Si almacena esta clave en una tarjeta inteligente, se beneficiará de seguridad adicional.
  
-   Puede reforzar la seguridad del cifrado de EFS mediante el uso de la directiva de grupo.
  
-   Los planes del atacante que intenta obtener acceso a los datos del usuario mediante un ataque de contraseña por fuerza bruta quedarán frustrados si las claves de EFS del usuario se almacenan en una tarjeta inteligente o al utilizar BitLocker en combinación con EFS para denegar el acceso del atacante a los valores hash de la contraseña y las credenciales en caché del usuario.
  
-   Es posible impedir que el atacante obtenga acceso a los datos confidenciales del usuario con la aplicación de cifrado a la carpeta Documentos del usuario mediante la directiva de grupo. De forma alternativa, puede exigir el cifrado de otras ubicaciones o de toda la partición de datos del usuario por medio de una secuencia de comandos de inicio de sesión.
  
-   Puede utilizar EFS para cifrar varias unidades y recursos compartidos de red.
  
-   Además, EFS le permitirá proteger el contenido del archivo de paginación del sistema y la memoria caché de archivos sin conexión.
  
#### Consideraciones para la reducción de riesgos
  
EFS en Windows Vista le ayudará a reducir los riesgos mencionados en la sección "Evaluación de riesgos". Sin embargo, antes de implementar EFS, es importante tener en cuenta lo siguiente:
  
-   Necesitará implementar procedimientos probados en relación con los requisitos de administración de claves y recuperación de datos. Si no cuenta con procedimientos confiables y bien definidos, la información importante podría quedar inaccesible en caso de darse la pérdida de claves.
  
-   En condiciones normales, la sobrecarga ocasionada por EFS es insignificante. No obstante, si el rendimiento del sistema es crítico, deberá realizar pruebas rigurosas para asegurarse de que EFS no influye en el rendimiento de forma negativa.
  
-   Si habilita EFS en un volumen, no podrá comprimir archivos en el mismo volumen.
  
-   Si es necesario, implemente y pruebe secuencias de comandos adicionales para cifrar ubicaciones de archivos confidenciales.
  
-   Los usuarios y el personal de TI necesitan aprender que, entre otras cosas, no deberían:
  
    -   Mover o copiar archivos de una ubicación cifrada a una ubicación sin cifrar; esto podría dejar los archivos en formato de texto simple.
  
    -   Descuidar el cifrado de carpetas ocultas, donde las aplicaciones guardan copias de seguridad de archivos en proceso.
  
-   Pruebe concienzudamente la configuración de EFS para asegurarse de que están cifradas todas las ubicaciones de archivos confidenciales, por ejemplo, la carpeta Documentos, el escritorio y las carpetas temporales.
  
**Nota**   EFS únicamente se puede implementar en las ediciones de Windows Vista siguientes: Business, Enterprise y Ultimate.
  
#### Proceso de reducción de riesgos
  
Haga uso del proceso de reducción de riesgos siguiente para determinar la configuración óptima de EFS de modo que contribuya a la protección de datos confidenciales en los equipos cliente que administra.
  
**Para usar este proceso:**
  
1.  Estudie la tecnología EFS y sus capacidades.
  
    **Nota**   Para obtener más información, consulte el artículo "[Recomendaciones sobre el sistema de cifrado de archivos](http://support.microsoft.com/default.aspx?scid=kb;en-us;223316)" en Microsoft.com (en inglés).
  
2.  Evalúe la necesidad de EFS en el entorno.
  
3.  Estudie la configuración de EFS con la directiva de grupo.
  
4.  Identifique los sistemas y los usuarios que requieren EFS.
  
5.  Identifique el nivel de protección que precisa. Por ejemplo, ¿requiere su organización el uso de tarjetas inteligentes con EFS?
  
6.  Configure EFS de forma óptima para su entorno mediante la directiva de grupo.
  
##### Medidas de reducción de riesgos específicas para EFS
  
Con el fin de utilizar la directiva de grupo en la administración de EFS, existen varios parámetros de seguridad en esta ubicación:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas\\Sistema de cifrado de archivos**
  
Para agregar o crear un agente de recuperación de datos (DRA), haga clic con el botón secundario en **Sistema de cifrado de archivos** y, a continuación, haga clic en **Propiedades** para abrir el cuadro de diálogo **Propiedades del sistema de cifrado de archivos**.
  
[![](images/Bb629455.VSGF0301(es-es,MSDN.10).gif)](https://technet.microsoft.com/es-es/bb629455.vsgf0301_big(es-es,msdn.10).gif)
  
**Figura 3.1 Cuadro de diálogo Propiedades del sistema de cifrado de archivos**
  
Además, hay cuatro plantillas de directiva de grupo que incluyen parámetros de configuración de EFS; se enumeran en la tabla siguiente.
  
**Tabla 3.4 Configuración de directiva de grupo para EFS**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Plantilla y parámetro de configuración</p></th>
<th><p>Ruta y descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>GroupPolicy.admx</strong><br />
Procesamiento de directivas de recuperación EFS</p></td>
<td style="border:1px solid black;"><p><strong>Configuración del equipo\</strong><br />
<strong>Plantillas administrativas\</strong><br />
<strong>Sistema\Directiva de grupo</strong><br />
Determina cuándo se actualizan las directivas de cifrado.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>EncryptFilesonMove.admx</strong><br />
No cifrar automáticamente archivos trasladados a carpetas cifradas</p></td>
<td style="border:1px solid black;"><p><strong>Configuración del equipo\</strong><br />
<strong>Plantillas administrativas\</strong><br />
<strong>Sistema\</strong><br />
Impide que Windows Explorer cifre archivos que se han trasladado a una carpeta cifrada.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>OfflineFiles.admx</strong><br />
Cifrar la memoria caché de archivos sin conexión</p></td>
<td style="border:1px solid black;"><p><strong>Configuración del equipo\</strong><br />
<strong>Plantillas administrativas\</strong><br />
<strong>Red\Archivos sin conexión\</strong><br />
Determina el cifrado de los archivos de conexión.</p>
<p><strong>Nota</strong>   En Windows XP, estos archivos están cifrados con la clave del sistema, mientras que, en Windows Vista, el cifrado se lleva a cabo con la clave del usuario.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>Search.admx</strong><br />
Permitir la indización de archivos cifrados</p></td>
<td style="border:1px solid black;"><p><strong>Configuración del equipo\</strong><br />
<strong>Plantillas administrativas\</strong><br />
<strong>Componentes de Windows\</strong><br />
<strong>Búsqueda</strong><br />
Este parámetro permite la indización de elementos cifrados por parte de la Búsqueda de Windows.</p>
<p><strong>Nota</strong>   Pueden darse problemas de seguridad si se aplica la indización a los archivos cifrados y el índice no está bien protegido por EFS o por algún otro medio.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Servicios de Windows Rights Management
  
El diseño de Servicios de Windows Rights Management (RMS) tiene como finalidades la provisión de seguridad y la aplicación de directivas de uso en relación con correo electrónico, documentos, contenido Web y otros tipos de información confidenciales. RMS proporciona seguridad de datos mediante el cifrado continuo de la información. De este modo, cuando se transmite un archivo o un mensaje de correo electrónico en la empresa o por Internet, solamente obtendrán acceso a estos datos los usuarios autenticados que cuentan con la autorización explícita. RMS consta de tres componentes:
  
-   **Servidor RMS**. Windows Vista requiere los Servicios de Windows Rights Management para Windows Server 2003 o versiones posteriores.
  
-   **Cliente RMS**. Incluido en Windows Vista.
  
-   **Plataforma o aplicación RMS**. Se trata de una aplicación o una plataforma diseñada para cifrar y controlar el uso de la información que administra.
  
#### Evaluación de riesgos
  
RMS puede asistir a las empresas en la reducción del riesgo de acceso a la información confidencial por parte de usuarios no autorizados. Es posible que los datos se hayan distribuido o dejado accesibles por error o de forma intencionada. Entre los ejemplos de este tipo de riesgo se incluyen los siguientes:
  
-   Algún usuario no autorizado examina la red y obtiene acceso a unidades de disco duro portátiles o flash USB, o a unidades de almacenamiento y recursos compartidos del servidor que no cuentan con la protección adecuada.
  
-   Algún usuario autorizado envía información confidencial a destinatarios no autorizados dentro o fuera de la organización.
  
-   Algún usuario autorizado copia o mueve información confidencial a ubicaciones o aplicaciones no autorizadas, o la traslada de un dispositivo autorizado a uno sin autorización, por ejemplo, a un dispositivo de almacenamiento extraíble.
  
-   De forma accidental, algún usuario autorizado proporciona acceso a la información confidencial a usuarios no autorizados mediante tecnologías punto a punto (P2P) o mensajería instantánea.
  
-   Algún usuario autorizado imprime archivos confidenciales que caen en manos de usuarios no autorizados; estos podrían distribuir los datos, copiarlos o enviarlos por fax o correo electrónico.
  
#### Reducción de riesgos
  
Con el fin de proteger la información que los usuarios comparten y usan en colaboraciones independientemente de los mecanismos que utilicen, Microsoft recomienda reforzar la seguridad de esta información directamente mediante RMS de forma que la protección sea continuada durante la transmisión de los datos entre sistemas host, dispositivos y recursos compartidos.
  
#### Consideraciones para la reducción de riesgos
  
Puede utilizar RMS para reducir los riesgos mencionados en la sección "Evaluación de riesgos". Sin embargo, antes de implementar RMS, es importante tener en cuenta lo siguiente:
  
-   RMS requiere los Servicios de Windows Rights Management para Windows Server 2003 (o una versión posterior) como servidor RMS, y aplicaciones habilitadas con derechos instaladas en el equipo cliente.
  
-   Es necesario disponer de Microsoft SharePoint® Server para aprovechar la integración SharePoint-RMS (RMS protege los documentos y la información en los sitios SharePoint).
  
-   Si desea beneficiarse de la integración opcional de tarjetas inteligentes que ofrece la solución RMS, asegúrese de que cada equipo cliente utilizado para obtener acceso al contenido es compatible con el uso de tarjetas inteligentes.
  
-   Para usar aplicaciones basadas en Web, como Outlook Web Access (OWA) con RMS, se necesita el complemento Rights Management para Internet Explorer.
  
-   El personal de TI deberá aprender a implementar RMS, así como a proporcionar soporte técnico y solucionar problemas sobre esta tecnología.
  
#### Proceso de reducción de riesgos
  
Haga uso del proceso de reducción de riesgos siguiente para determinar la configuración óptima de RMS de modo que contribuya a la protección de datos confidenciales en los equipos cliente que administra.
  
**Para usar este proceso:**
  
1.  Estudie la tecnología RMS y sus capacidades.
  
    **Nota**   Para obtener más información acerca de RMS, consulte el centro de tecnología de los [Servicios de Windows Rights Management](http://www.microsoft.com/windowsserver2003/technologies/rightsmgmt/default.mspx) (en inglés).
  
2.  Evalúe la necesidad de RMS en el entorno.
  
3.  Identifique la compatibilidad de aplicaciones y servicios con RMS.
  
4.  Evalúe posibles arquitecturas de implementación de RMS, como:
  
    -   Servidor único (o clúster único)
  
    -   Certificación única, licencia única
  
    -   Certificación única, licencia múltiple
  
    -   Certificación múltiple, licencia única
  
    -   Certificación múltiple, licencia múltiple
  
5.  Identifique la información que desea proteger con RMS.
  
6.  Determine los usuarios y los grupos que requieren acceso a información concreta.
  
7.  Configure RMS de forma que permita únicamente el acceso requerido a la información.
  
#### Administración de RMS mediante la directiva de grupo
  
Los parámetros de directiva de grupo para la configuración de RMS no forman parte de la instalación de Windows Vista. RMS es, principalmente, una solución basada en servidor, de modo que la configuración del comportamiento de los servicios se debe establecer en el servidor RMS.
  
Además, es posible que las aplicaciones compatibles con RMS cuenten con parámetros de configuración individuales para controlar el tratamiento del contenido protegido por RMS. Por ejemplo, hay parámetros de configuración específicos para Microsoft Office 2003 o versiones posteriores, y también para aplicaciones como Microsoft Outlook® y Microsoft Word. Para obtener más información sobre estos parámetros, consulte [Archivos de plantilla de directiva y herramientas de planeamiento para la implementación de Office 2003](http://office.microsoft.com/en-us/assistance/ha011513711033.aspx) (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Control de dispositivos
  
La capacidad de los usuarios para agregar hardware Plug and Play (PnP) nuevo a sus equipos cliente (por ejemplo, unidades USB y otros dispositivos de almacenamiento extraíbles) da lugar a problemas de seguridad considerables para los administradores de TI. Estos tipos de dispositivos pueden dificultar el mantenimiento de los equipos cliente cuando los usuarios los utilizan para instalar hardware no compatible pero, además, pueden dar lugar a amenazas de seguridad de los datos.
  
Un usuario malintencionado podría usar un dispositivo de almacenamiento extraíble para robar la propiedad intelectual de la empresa. El atacante también podría utilizar un dispositivo de almacenamiento extraíble con software malintencionado que incluya una secuencia de comandos de ejecución automática para instalar software malintencionado en un equipo cliente desatendido.
  
Windows Vista permite a los administradores de TI hacer uso de la directiva de grupo para administrar la instalación de dispositivos no compatibles o no autorizados. Por ejemplo, puede permitir a los usuarios que instalen clases completas de dispositivos (como impresoras) pero, al mismo tiempo, puede prohibir el uso de cualquier tipo de dispositivo de almacenamiento extraíble. Puede otorgar a un administrador el permiso de invalidar estas directivas con el fin de instalar hardware autorizado.
  
Sin embargo, es importante entender que un dispositivo está instalado para un equipo y no para usuarios determinados. Cuando un usuario instala algún dispositivo, este suele permanecer disponible para todos los usuarios del equipo. Windows Vista incluye controles de acceso a nivel de usuario para el acceso de lectura y escritura en dispositivos instalados. Por ejemplo, ahora podrá permitir acceso total de lectura y escritura en relación con un dispositivo instalado (como una unidad flash USB) a una cuenta de usuario y, al mismo tiempo, otorgar acceso de sólo lectura a otra cuenta de usuario en el mismo equipo.
  
Para obtener más información acerca del control de dispositivos y su configuración, consulte la [*Guía paso a paso para controlar la instalación y el uso de dispositivos mediante la directiva de grupo*](http://www.microsoft.com/technet/windowsvista/library/9fe5bf05-a4a9-44e2-a0c3-b4b4eaaa37f3.mspx) (en inglés).
  
#### Evaluación de riesgos
  
Cuando los usuarios agregan o retiran dispositivos sin autorización, los riesgos de seguridad aumentan considerablemente: un atacante podría ejecutar software malintencionado, quitar datos y agregar información no deseada. A continuación, se incluyen algunos ejemplos:
  
-   Algún usuario autorizado podría copiar archivos confidenciales de un dispositivo autorizado a un dispositivo de almacenamiento extraíble no autorizado, ya sea accidentalmente o de forma intencionada. Esto puede incluir la copia de una ubicación cifrada a una ubicación sin cifrar en un dispositivo extraíble.
  
-   El atacante puede iniciar la sesión en Windows Vista y copiar datos en un dispositivo de almacenamiento extraíble.
  
-   El atacante podría utilizar un dispositivo de almacenamiento extraíble con software malintencionado para utilizar una secuencia de comandos de ejecución automática que instale software malintencionado en un equipo cliente desatendido.
  
-   Un atacante puede instalar un dispositivo no autorizado de registro de claves, que se podría utilizar para registrar datos de cuentas de usuarios con los que realizar ataques adicionales.
  
#### Reducción de riesgos
  
Con el fin de reducir estos riesgos, Microsoft recomienda la protección de los sistemas informáticos contra la instalación y el uso de dispositivos no autorizados. Puede utilizar la configuración de la directiva de grupo para controlar el uso de dispositivos PnP, como unidades flash USB y otros dispositivos de almacenamiento extraíbles.
  
#### Consideraciones para la reducción de riesgos
  
Puede utilizar la directiva de grupo en Windows Vista para reducir los riesgos mencionados en la sección "Evaluación de riesgos" mediante el uso de los parámetros de instalación de dispositivos. Sin embargo, antes de implementar el control de dispositivos en los equipos cliente de su entrono, tenga en cuenta las siguientes consideraciones:
  
-   La restricción de dispositivos podría dificultar el trabajo de usuarios legítimos que comparten archivos o utilizan equipos portátiles.
  
-   La restricción de dispositivos podría impedir el uso de una clave USB como parte del proceso de cifrado de unidad BitLocker. Por ejemplo, si el parámetro de directiva Discos extraíbles: denegar acceso de escritura, está activo para un usuario, aunque el usuario sea administrador, el programa de instalación de BitLocker no podrá escribir su clave de inicio en una unidad flash USB.
  
-   Algunos dispositivos se identifican como almacenamiento extraíble y como almacenamiento local al mismo tiempo, por ejemplo, esto suele darse con unidades flash USB de arranque. Por lo tanto, es importante probar los GPO rigurosamente para asegurarse de restringir y permitir los dispositivos correctos.
  
#### Proceso de reducción de riesgos
  
Haga uso del proceso de reducción de riesgos siguiente para determinar la configuración óptima del control de dispositivos de modo que contribuya a la protección de datos confidenciales en los equipos cliente que administra.
  
**Para usar este proceso:**
  
1.  estudie las capacidades del control de dispositivos de Windows Vista.
  
    **Nota**   Para obtener más información, consulte la [*Guía paso a paso para controlar la instalación y el uso de dispositivos mediante la directiva de grupo*](http://www.microsoft.com/technet/windowsvista/library/9fe5bf05-a4a9-44e2-a0c3-b4b4eaaa37f3.mspx) (en inglés).
  
2.  Evalúe la necesidad del control de dispositivos en el entorno.
  
3.  Estudie la configuración de directiva de grupo para el control de dispositivos.
  
4.  Identifique los dispositivos extraíbles que requiere en el entorno y registre los Id. de compatibilidad y hardware requeridos para todos ellos.
  
5.  Identifique los sistemas y los usuarios que requieren los dispositivos extraíbles.
  
6.  Configure la directiva de grupo para permitir la instalación de clases de dispositivos requeridas específicamente.
  
7.  Configure la directiva de grupo para permitir la instalación de dispositivos en sistemas que específicamente requieren la capacidad concreta.
  
##### Uso de la directiva de grupo para controlar la instalación de dispositivos
  
Con el fin de administrar el control de la instalación de dispositivos, Microsoft recomienda el uso de la plantilla de directiva de grupo DeviceInstallation.admx. La tabla 3.5 describe la configuración de directiva de grupo disponible en esta plantilla. Puede establecer esta configuración en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Instalación de dispositivos\\Restricciones de instalación de dispositivos**
  
**Tabla 3.5 Configuración del control de dispositivos USB**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Permitir a los administradores invalidar directivas de instalación de dispositivos</p></td>
<td style="border:1px solid black;"><p>Permite a los miembros del grupo Administradores instalar y actualizar los controladores para cualquier dispositivo, independientemente de otros parámetros de directiva. De lo contrario, los administradores estarán sujetos a todas las directivas que restringen la instalación de dispositivos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Permitir la instalación de dispositivos mediante controladores que coinciden con estas clases de instalación de dispositivos</p></td>
<td style="border:1px solid black;"><p>Especifica una lista de GUID de clases de instalación de dispositivos que describen los dispositivos que pueden instalar los usuarios, a menos que lo impidan específicamente los parámetros de directiva siguientes:<br />
<strong>Impedir la instalación de dispositivos que coinciden con estos Id. de dispositivos</strong><br />
<strong>Impedir la instalación de dispositivos para estas clases de dispositivos</strong><br />
<strong>Impedir la instalación de dispositivos extraíbles</strong><br />
Utilice este parámetro de configuración sólo cuando esté habilitado el parámetro <strong>Impedir la instalación de dispositivos no descritos por otros parámetros de directiva</strong>.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Impedir la instalación de dispositivos mediante controladores que coinciden con estas clases de instalación de dispositivos</p></td>
<td style="border:1px solid black;"><p>Especifica un mensaje personalizado que se muestra al usuario en el título del globo de notificación cuando esta directiva impide la instalación de un dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Mostrar un mensaje personalizado cuando la directiva impide la instalación (título del globo)</p></td>
<td style="border:1px solid black;"><p>Especifica un mensaje personalizado que se muestra al usuario en el título del globo de notificación cuando un parámetro de directiva impide la instalación.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Mostrar un mensaje personalizado cuando la directiva impide la instalación (título del globo)</p></td>
<td style="border:1px solid black;"><p>Especifica un mensaje personalizado que se muestra al usuario en el texto del globo de notificación cuando la directiva impide la instalación de un dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Permitir la instalación de dispositivos que coinciden con cualquiera de estos Id. de dispositivos</p></td>
<td style="border:1px solid black;"><p>Especifica una lista de Id. de hardware Plug and Play e Id. compatibles que describen los dispositivos que se pueden instalar, a menos que los parámetros siguientes lo impidan de forma específica:<br />
<strong>Impedir la instalación de dispositivos que coinciden con estos Id. de dispositivos</strong><br />
<strong>Impedir la instalación de dispositivos para estas clases de dispositivos</strong><br />
<strong>Impedir la instalación de dispositivos extraíbles</strong><br />
Utilice este parámetro de configuración sólo cuando esté habilitado el parámetro <strong>Impedir la instalación de dispositivos no descritos por otros parámetros de directiva</strong>.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Impedir la instalación de dispositivos que coinciden con estos Id. de dispositivos</p></td>
<td style="border:1px solid black;"><p>Especifica una lista de Id. de hardware Plug and Play e Id. compatibles para los dispositivos que los usuarios no pueden instalar.<br />
<strong>Nota</strong>   Este parámetro de directiva tiene prioridad sobre cualquier otro parámetro de directiva que permite la instalación del dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Impedir la instalación de dispositivos extraíbles</p></td>
<td style="border:1px solid black;"><p>Si habilita este parámetro de configuración, los usuarios no podrán instalar dispositivos extraíbles y los dispositivos extraíbles existentes no podrán recibir actualizaciones de controladores.<br />
<strong>Nota</strong>   Este parámetro de directiva tiene prioridad sobre cualquier otro parámetro de directiva que permite la instalación del dispositivo.<br />
Para que se aplique esta directiva, los controladores del dispositivo deben identificar correctamente que el dispositivo es extraíble. Para obtener más información, consulte la <a href="http://www.microsoft.com/technet/windowsvista/library/9fe5bf05-a4a9-44e2-a0c3-b4b4eaaa37f3.mspx"><em>Guía paso a paso para controlar la instalación y el uso de dispositivos mediante la directiva de grupo</em></a> (en inglés).</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Impedir la instalación de dispositivos no descritos por otros parámetros de directiva</p></td>
<td style="border:1px solid black;"><p>Si habilita este parámetro de configuración, cualquier dispositivo que no aparezca descrito por alguno de los parámetros siguientes no podrá recibir actualizaciones de controladores:<br />
<strong>Permitir la instalación de dispositivos que coinciden con estos Id. de dispositivos</strong><br />
<strong>Permitir la instalación de dispositivos para estas clases de dispositivos</strong></p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Uso de la directiva de grupo para controlar la utilización de dispositivos
  
Además de contribuir al control de la instalación de dispositivos, Windows Vista permite controlar el nivel de acceso de los usuarios a clases de dispositivos concretas después de la instalación. Las dos plantillas descritas en las tablas siguientes incluyen parámetros de configuración que pueden influir en el comportamiento de los dispositivos: RemovableStorage.admx contiene el parámetro siguiente para dispositivos de almacenamiento extraíbles y se encuentra en esta ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Acceso a medios de almacenamiento extraíble**
  
**Tabla 3.6 Configuración de dispositivos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todas las clases de almacenamiento extraíble: denegar todo acceso</p></td>
<td style="border:1px solid black;"><p>Configura el acceso a todas las clases de dispositivos de almacenamiento extraíbles.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Todos los medios de almacenamiento extraíbles: permitir acceso directo en sesiones remotas</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración otorga a las cuentas de usuario estándar el acceso a los dispositivos de almacenamiento extraíbles en sesiones remotas. La configuración predeterminada no permite este acceso para sesiones remotas.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CD y DVD: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura para la clase de almacenamiento extraíble de CD y DVD. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CD y DVD: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura para la clase de almacenamiento extraíble de CD y DVD. La configuración predeterminada permite el acceso de escritura para esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Clases personalizadas: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura para las clases de dispositivos personalizadas. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Clases personalizadas: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura a las clases de dispositivos personalizadas. La configuración predeterminada permite el acceso de escritura a esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Unidades de disquete: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura a las unidades de disquete. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Unidades de disquete: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura a las unidades de disquete. La configuración predeterminada permite el acceso de escritura a esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Discos extraíbles: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura a las unidades extraíbles. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Discos extraíbles: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura a las unidades extraíbles. La configuración predeterminada permite el acceso de escritura a esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Unidades de cinta: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura a las unidades de cinta. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Unidades de cinta: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura a las unidades de cinta. La configuración predeterminada permite el acceso de escritura a esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Dispositivos WPD: denegar acceso de lectura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de lectura a los dispositivos portátiles de Windows, como reproductores multimedia y teléfonos móviles. La configuración predeterminada permite el acceso de lectura.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Dispositivos WPD: denegar acceso de escritura</p></td>
<td style="border:1px solid black;"><p>Este parámetro de configuración deniega el acceso de escritura a los dispositivos portátiles de Windows, como reproductores multimedia y teléfonos móviles. La configuración predeterminada permite el acceso de escritura a esta clase de dispositivo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Uso de la directiva de grupo para controlar la reproducción y la ejecución automáticas
  
La plantilla Autoplay.admx incluye los parámetros de configuración siguientes que influyen en el comportamiento de la reproducción y la ejecución automáticas para dispositivos de almacenamiento extraíbles y dispositivos portátiles en Windows Vista. Encontrará la configuración para esta plantilla en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Directivas de reproducción automática**
  
**Tabla 3.7 Configuración de directivas de reproducción automática**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Configuración predeterminada en Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Desactivar reproducción automática</p></td>
<td style="border:1px solid black;"><p>Permite deshabilitar la característica de reproducción automática para unidades de CD, DVD-ROM y extraíbles o para todas las unidades.</p></td>
<td style="border:1px solid black;"><p>No configurado ‡</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Comportamiento predeterminado para la ejecución automática</p></td>
<td style="border:1px solid black;"><p>Este parámetro configura el comportamiento predeterminado para comandos de ejecución automática. De forma predeterminada, Windows Vista pregunta al usuario si debe ejecutarse el comando de ejecución automática.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información acerca de un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Estos parámetros aparecen también bajo la configuración del usuario en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del usuario\\Plantillas administrativas\\Componentes de Windows\\Directivas de reproducción automática**
  
Si se produce algún conflicto en los parámetros de configuración del control de dispositivos, el parámetro de la configuración del equipo tendrá prioridad sobre el parámetro de la configuración de usuario.
  
**Nota**   Algunos parámetros de directiva especifican el uso de GUID de clases de instalación de dispositivos; otros utilizan GUID de clases de instalación de dispositivos Plug and Play. Para obtener más información, consulte [Selección de controladores por parte de la instalación](http://go.microsoft.com/fwlink/?linkid=54881) (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
Para obtener información adicional sobre las características y tecnologías de seguridad nuevas y mejoradas que contribuyen a la protección de datos confidenciales en Windows Vista, consulte los recursos siguientes:
  
-   "[Recomendaciones sobre el sistema de cifrado de archivos](http://support.microsoft.com/default.aspx?scid=kb;en-us;223316)" en Microsoft.com (en inglés).
  
-   [Cifrado de unidad BitLocker](http://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) en TechNet (en inglés).
  
-   Control de dispositivos en la [*Guía paso a paso para controlar la instalación y el uso de dispositivos mediante la directiva de grupo*](http://www.microsoft.com/technet/windowsvista/library/9fe5bf05-a4a9-44e2-a0c3-b4b4eaaa37f3.mspx) en TechNet (en inglés).
  
-   Instalación y administración de dispositivos (DMI) en la [*Guía paso a paso para controlar la instalación y el uso de dispositivos mediante la directiva de grupo*](http://www.microsoft.com/technet/windowsvista/library/9fe5bf05-a4a9-44e2-a0c3-b4b4eaaa37f3.mspx) en TechNet (en inglés).
  
-   El artículo "[Introducción: características de seguridad nuevas en Windows Vista](https://www.microsoft.com/technet/technetmag/issues/2006/05/firstlook/default.aspx)" en TechNet con información general sobre las características de seguridad en Windows Vista (en inglés).
  
-   La sección "[Protección de datos](http://www.microsoft.com/technet/windowsvista/evaluate/feat/secfeat.mspx)" de la página Web sobre mejoras de protección de datos y seguridad en Windows Vista en TechNet (en inglés).
  
-   El artículo "[Sistema de cifrado de archivos](http://www.microsoft.com/technet/security/topics/cryptographyetc/efs.mspx)" en TechNet (en inglés).
  
-   El sitio Web de [Trusted Computing Group](http://www.trustedcomputinggroup.org/) (en inglés).
  
-   [Archivos de plantilla de directiva y herramientas de planeamiento para la implementación de Office 2003](http://office.microsoft.com/en-us/assistance/ha011513711033.aspx) en Microsoft.com (en inglés).
  
-   El centro de tecnología de [Servicios de Windows Rights Management](http://www.microsoft.com/windowsserver2003/technologies/rightsmgmt/default.mspx)(en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Consiga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)
  
[](#mainsection)[Principio de la página](#mainsection)
