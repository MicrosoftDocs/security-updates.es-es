---
TOCTitle: 'Capítulo 2: Defensa ante el software malintencionado'
Title: 'Capítulo 2: Defensa ante el software malintencionado'
ms:assetid: 'dbb3a7b2-f9c7-4953-b9eb-81550fec35ad'
ms:contentKeyID: 20105775
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb629436(v=MSDN.10)'
---

Capítulo 2: Defensa ante el software malintencionado
====================================================

### Capítulo 2: Defensa ante el software malintencionado

Publicado: noviembre 8, 2006

*Software malintencionado* es cualquier programa o archivo capaz de perjudicar a los usuarios de equipos. Aquí se incluyen programas de virus, gusanos, caballos de Troya y spyware, software destinado a recopilar información sobre el usuario del equipo sin su consentimiento.

Windows Vista™ ofrece varias tecnologías nuevas que mejoran la protección contra software malintencionado en equipos que ejecutan este sistema operativo. Estas características y servicios se pueden usar como complemento a la configuración de los objetos de directiva de grupo descrita en el capítulo anterior (algunos de estos objetos sirven también de protección contra software malintencionado).

Asimismo, en Windows Vista, Microsoft® Internet Explorer® 7 incluye diversas mejoras que contribuyen a la protección contra software malintencionado. Las tecnologías que impiden la instalación de software no deseado, al igual que aquellas que evitan la transmisión no autorizada de datos personales, incrementan considerablemente la seguridad del explorador y la protección de la privacidad.

Este capítulo proporciona información general sobre estas tecnologías y recomendaciones para la configuración de las mismas cuando corresponda. Es posible implementar estas recomendaciones en los objetos de directiva de grupo apropiados descritos en el capítulo 1, "Implementación de líneas de base de seguridad". Sin embargo, es importante tener en cuenta que la configuración de estas tecnologías suele requerir información específica del entorno. Por esta razón, la mayoría de los valores recomendados para estos parámetros de configuración adicionales no se incluyen en los objetos de directiva de grupo descritos en el capítulo anterior.

De forma predeterminada, estas tecnologías están configuradas para ofrecer protección mejorada en equipos que ejecutan Windows Vista en un entorno de cliente de empresa (EC). Sin embargo, se pueden utilizar algunos parámetros nuevos de configuración de directiva de grupo para personalizar el comportamiento y la funcionalidad de las tecnologías con el fin de proporcionar mayor protección contra software malintencionado en el entorno.

Este capítulo distingue entre las tecnologías nuevas y mejoradas de Windows Vista y las de Internet Explorer 7:

-   Tecnologías de defensa de Windows Vista

-   Tecnologías de defensa de Internet Explorer 7

**Nota**   En cada una de estas secciones en el capítulo, se resalta una configuración de directiva de grupo concreta para documentar la configuración predeterminada de la instalación original de Windows Vista. Las modificaciones o recomendaciones de configuración particulares aparecen marcadas con el símbolo ‡. Para obtener más detalles sobre los valores de configuración, consulte el apéndice A, "Configuración de directivas de grupo de seguridad".

##### En esta página

[](#ecaa)[Tecnologías de defensa de Windows Vista](#ecaa)
[](#ebaa)[Tecnologías de defensa de Internet Explorer 7](#ebaa)
[](#eaaa)[Más información](#eaaa)

### Tecnologías de defensa de Windows Vista

Windows Vista incluye varias tecnologías nuevas y mejoradas que incrementan la protección contra software malintencionado. Entre estas tecnologías se incluyen:

-   Control de cuentas de usuario

-   Windows Defender

-   Firewall de Windows

-   Centro de seguridad de Windows

-   Herramienta de eliminación de software malintencionado

-   Directivas de restricción de software

Además del uso de estas tecnologías de protección, el inicio de sesión mediante una cuenta de usuario estándar continúa siendo una práctica de seguridad altamente recomendada. Incluso con la implementación de estas tecnologías de protección, si se descuida el acceso a los equipos a nivel administrativo, estos sistemas quedan expuestos a riesgos de seguridad.

#### Control de cuentas de usuario

Windows Vista incluye el control de cuentas de usuario (UAC) como método para separar privilegios y tareas de usuario estándar de aquellos que requieren acceso administrativo. UAC incrementa la seguridad al mejorar la experiencia del usuario durante el uso de una cuenta de usuario estándar. Ahora, los usuarios pueden realizar más tareas y beneficiarse de una compatibilidad de aplicaciones superior sin necesidad de iniciar la sesión con privilegios a nivel administrativo. Esto contribuye a reducir los riesgos asociados al software malintencionado y a la instalación de software no autorizado, así como los cambios en el sistema que no han sido aprobados.

**Nota**   En versiones anteriores de Windows, el grupo de usuarios avanzados permitía a los miembros de este grupo realizar tareas relacionadas con el sistema, como instalar aplicaciones sin permisos de administración completos. UAC no hace uso del grupo de usuarios avanzados y, en Windows Vista, se han eliminado los permisos asociados a este grupo. Sin embargo, el grupo está aún disponible para ofrecer compatibilidad con versiones anteriores del sistema operativo. El uso del grupo de usuarios avanzados en Windows Vista exige la aplicación de una plantilla de seguridad nueva para cambiar los permisos predeterminados en las carpetas del sistema y el Registro de forma que los miembros del grupo reciban permisos equivalentes a los del mismo grupo en Windows XP.

En Windows Vista, los usuarios con privilegios estándar pueden realizar muchas tareas que anteriormente requerían acceso administrativo pero que no influían de forma negativa en la seguridad. Entre estas tareas se cuentan la modificación de la configuración de las zonas horarias, la conexión a redes inalámbricas seguras y la instalación de dispositivos aprobados y controles ActiveX® de Microsoft.

Además, la característica Modo de aprobación de administrador de la tecnología UAC contribuye a proteger los equipos con Windows Vista contra algunos tipos de software malintencionado. De forma predeterminada, los administradores pueden ejecutar la mayoría de los programas y las tareas con privilegios de usuario estándar. Cuando los usuarios necesiten realizar tareas administrativas, por ejemplo, instalar software o modificar ciertos aspectos de la configuración del sistema, deberán proporcionar la autorización debida antes de poder llevar a cabo las tareas en cuestión. No obstante, este modo no ofrece el mismo nivel de protección que una cuenta de usuario estándar y no garantiza que el software malintencionado que ya está instalado en el equipo cliente no pueda interferir con el software elevado. Tampoco garantiza que el mismo software elevado no vaya a realizar intentos de acciones malintencionadas después de la elevación.

Con el fin de aprovechar al máximo esta tecnología, la nueva configuración de directiva de grupo de Windows Vista se puede adaptar para que controle el comportamiento de UAC. La configuración de directiva de grupo tal y como se describe en el capítulo anterior está habilitada para forzar el comportamiento prescrito de UAC. Sin embargo, Microsoft aconseja la revisión de estas recomendaciones de configuración, descritas en el apéndice A, "Configuración de directivas de grupo de seguridad", con el fin de garantizar una configuración óptima que cumpla los requisitos del entorno.

##### Evaluación de riesgos

Los usuarios con privilegios administrativos inician la sesión con sus capacidades administrativas habilitadas. Esto podría dar lugar a tareas administrativas realizadas de forma accidental o malintencionada sin el conocimiento del individuo. Por ejemplo:

-   Sin saberlo, el usuario descarga e instala software malintencionado de un sitio Web malintencionado o infectado.

-   El usuario abre datos adjuntos de correo electrónico con software malintencionado que se ejecuta y, posiblemente, se instala automáticamente en el equipo.

-   Se inserta una unidad extraíble en el equipo y la reproducción automática intenta ejecutar el software malintencionado.

-   El usuario instala aplicaciones no compatibles que pueden tener un efecto negativo en el rendimiento o la confiabilidad del equipo.

##### Reducción de riesgos

El enfoque de mitigación recomendado consiste en asegurarse de que todos los usuarios inician la sesión con cuentas de usuario estándar para realizar las tareas habituales. Los usuarios únicamente deberían utilizar cuentas administrativas para tareas que requieren este nivel de acceso. Además, UAC debería configurarse para preguntar al usuario cada vez que se produzca un intento de realizar tareas que exigen el uso de privilegios administrativos.

##### Consideraciones para la reducción de riesgos

UAC puede asistir en la reducción de los riesgos mencionados en la sección "Evaluación de riesgos". Sin embargo, es importante tener en cuenta lo siguiente:

-   Si la organización cuenta con desarrolladores de aplicaciones internos, Microsoft recomienda que descarguen y consulten el artículo "[Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad con el control de cuentas de usuario](http://www.microsoft.com/downloads/details.aspx?familyid=ba73b169-a648-49af-bc5e-a2eebb74c16b&displaylang=en)" (en inglés). Este documento describe los procesos de diseño y desarrollo de aplicaciones compatibles con UAC para el uso con Windows Vista.

-   UAC puede introducir problemas en aplicaciones que no son compatibles con UAC. Por ello, es primordial probar estas aplicaciones con UAC de forma previa a la implementación. Para obtener más información acerca de pruebas de compatibilidad de aplicaciones, visite el sitio Web [Desktop Deployment](http://www.microsoft.com/technet/desktopdeployment) de Microsoft TechNet® (en inglés).

-   Las solicitudes de UAC para la elevación de credenciales y privilegios administrativos incrementan los pasos requeridos para completar muchas tareas administrativas típicas. Es aconsejable evaluar las implicaciones de la ampliación de estos pasos para el personal administrativo. Si los mensajes adicionales de UAC afectan considerablemente a estos usuarios, la configuración de la directiva de UAC "Comportamiento del indicador de elevación para los administradores en Modo de aprobación de administrador" se puede establecer en "Elevar sin preguntar". No obstante, la modificación de esta directiva puede incrementar los riesgos de seguridad en el entorno y el Centro de seguridad de Windows ofrecerá las advertencias oportunas.

-   Los usuarios con privilegios administrativos pueden deshabilitar el Modo de aprobación de administrador, impedir que UAC solicite credenciales para la instalación de aplicaciones y cambiar el comportamiento de las solicitudes de elevación de privilegios. De modo que es importante controlar el número de usuarios con acceso a los privilegios administrativos en los equipos de la empresa.

-   Microsoft recomienda la asignación de dos cuentas al personal administrativo. Para tareas habituales, deberían hacer uso de una cuenta de nivel estándar. Cuando se requieran tareas administrativas concretas, estos usuarios pueden usar la cuenta de nivel administrativo, realizar las tareas y, de inmediato, regresar a la cuenta de usuario estándar.

-   La configuración de directiva de grupo de esta guía elimina la capacidad de los usuarios estándar para elevar privilegios. Este es el enfoque recomendado, ya que garantiza que las tareas administrativas quedan exclusivamente al cargo de cuentas que se han configurado específicamente al nivel administrativo.

-   Si una aplicación se identificara incorrectamente como aplicación administrativa o de usuario (por ejemplo, con el símbolo (token) "administrador" o "estándar"), Windows Vista podría iniciar la aplicación en el contexto de seguridad equivocado.

##### Proceso de reducción de riesgos

El punto de partida del proceso de reducción de riesgos debe ser la investigación de las capacidades totales de UAC. Para obtener más información, consulte [*Guía paso a paso sobre el control de cuentas de usuario en Windows Vista*](http://www.microsoft.com/technet/windowsvista/library/0d75f774-8514-4c9e-ac08-4c21f5c6c2d9.mspx) (en inglés) e [Introducción al control de cuentas de usuario en Windows Vista](http://www.microsoft.com/technet/windowsvista/library/f72d606c-ad66-403b-be70-3d59e4e5c10f.mspx) (en inglés).

**Para usar este proceso:**

1.  Identifique el número de usuarios que pueden llevar a cabo tareas administrativas.

2.  Determine la frecuencia con que deben realizarse dichas tareas.

3.  Decida si debería bastar con confirmar la solicitud de UAC para que los administradores puedan realizar las tareas o si deberán proporcionar credenciales determinadas.

4.  Determine si los usuarios estándar podrán elevar sus privilegios para realizar tareas administrativas. La configuración de directiva aplicada como parte de esta guía bloquea específicamente esta capacidad.

5.  Determine el tratamiento de la instalación de aplicaciones.

6.  Adapte la configuración de directiva de grupo de UAC para cumplir los requisitos de la organización.

###### Uso de la directiva de grupo en la reducción de riesgos para UAC

Puede modificar la configuración de UAC en la ubicación siguiente del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad**

La tabla siguiente proporciona información sobre la configuración de seguridad específica de esta tecnología en Windows Vista.

**Tabla 2.1 Configuración del control de UAC**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Modo de aprobación de administrador para la cuenta Administrador integrado</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina el comportamiento del Modo de aprobación de administrador para la cuenta administrativa integrada.</p></td>
<td style="border:1px solid black;"><p>Deshabilitado ‡</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Comportamiento del indicador de elevación para los administradores en Modo de aprobación de administrador</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina el comportamiento de la solicitud de confirmación de elevación de privilegios para los administradores.</p></td>
<td style="border:1px solid black;"><p>Pedir consentimiento ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Comportamiento del indicador de elevación para los usuarios estándar</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina el comportamiento de la solicitud de confirmación de elevación para usuarios estándar.</p></td>
<td style="border:1px solid black;"><p>Pedir credenciales ‡</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Detectar instalaciones de aplicaciones y pedir confirmación de elevación</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina el comportamiento de la detección de instalación de aplicaciones para todo el sistema.</p></td>
<td style="border:1px solid black;"><p>Habilitado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Elevar sólo los archivos ejecutables firmados y validados</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad exige la comprobación de firmas PKI en cualquier aplicación interactiva que solicita la elevación de privilegios. Los administradores de empresa pueden controlar la lista de aplicaciones de administrador permitidas mediante el uso de certificados en el almacén de editores de confianza de los equipos locales.</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Elevar sólo aplicaciones UIAccess instaladas en ubicaciones seguras</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad exige que las aplicaciones que requieren la ejecución con un nivel de integridad UIAccess residan en una ubicación segura del sistema de archivos.</p></td>
<td style="border:1px solid black;"><p>Habilitado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Ejecutar todos los administradores en Modo de aprobación de administrador</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina el comportamiento de las directivas UAC para todo el sistema.</p></td>
<td style="border:1px solid black;"><p>Habilitado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Cambiar al escritorio seguro cuando se pida confirmación de elevación</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad determina si la solicitud de elevación mostrará un mensaje en el escritorio interactivo del usuario o en el escritorio seguro.</p></td>
<td style="border:1px solid black;"><p>Habilitado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Virtualizar los errores de escritura de Registro y de archivo en ubicaciones por usuario</p></td>
<td style="border:1px solid black;"><p>Este parámetro de seguridad permite el redireccionamiento de errores de escritura de aplicaciones heredadas a ubicaciones definidas tanto en el Registro como en el sistema de archivos.</p></td>
<td style="border:1px solid black;"><p>Habilitado</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Puede configurar la interfaz de usuario de las credenciales de UAC en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Interfaz de usuario de credenciales**
  
La tabla siguiente proporciona información sobre la configuración de seguridad específica de esta tecnología en Windows Vista.
  
**Tabla 2.2 Configuración de la interfaz de usuario de credenciales de UAC**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Enumerar cuentas de administrador para la elevación</p></td>
<td style="border:1px solid black;"><p>De forma predeterminada, se muestran todas las cuentas de administrador cada vez que un usuario intenta elevar una aplicación en ejecución. La habilitación de este parámetro exige que los usuarios escriban su nombre de usuario y contraseña para elevar sus privilegios.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Requerir ruta de confianza para la entrada de credenciales</p></td>
<td style="border:1px solid black;"><p>Con este parámetro habilitado, Windows Vista requiere la entrada de credenciales por parte del usuario mediante una ruta de confianza para evitar que caballos de Troya u otros tipos de software malintencionado puedan robar las credenciales de Windows del usuario. Esta directiva únicamente afecta a tareas de autenticación sin inicio de sesión. Como método de seguridad recomendado, esta directiva debería mantenerse habilitada.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Puede modificar la configuración del Servicio del instalador de ActiveX en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Servicio del instalador de ActiveX**
  
La tabla siguiente proporciona información sobre la configuración de seguridad específica del Servicio del instalador de ActiveX en Windows Vista.
  
**Tabla 2.3 Servicio del instalador de ActiveX**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Sitios de instalación aprobados para controles ActiveX</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a los administradores habilitar cuentas de usuario estándar para que puedan instalar controles ActiveX de una lista de sitios de instalación aprobados.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de este parámetro. Para obtener más información sobre este parámetro, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
#### Windows Defender
  
Windows Defender es un programa incluido en Windows Vista disponible también como descarga para Windows XP. Ayuda a proteger los equipos frente a elementos emergentes, reducción del rendimiento y amenazas de seguridad causadas por spyware y otros programas de software no deseado. En tiempo real, Windows Defender supervisa puntos de comprobación importantes del sistema operativo Windows Vista que constituyen el objetivo de este tipo de software, por ejemplo, la carpeta Inicio y las entradas de ejecución automática en el Registro.
  
Además, Windows Defender facilita la detección y la eliminación de aplicaciones no deseadas, como programas adware, registradores de claves y spyware. Cuando un programa intenta modificar una zona protegida en Windows Vista, Windows Defender solicita al usuario que permita o rechace el cambio como protección contra la instalación de spyware. Este tipo de supervisión mejora la confiabilidad de los equipos que ejecutan Windows Vista y proporciona protección adicional de la privacidad del usuario. Windows Defender está habilitado en Windows Vista de forma predeterminada y, aunque la tecnología brinda protección mejorada contra spyware, se puede utilizar también con otros productos de seguridad de terceros. Con el fin de ofrecer protección óptima contra software malintencionado, Microsoft recomienda encarecidamente la implementación de una solución antivirus completa junto con Windows Defender.
  
La nueva configuración de directiva de grupo de Windows Vista se puede adaptar para que controle el comportamiento de Windows Defender. La configuración de directiva de grupo descrita en el capítulo anterior no contiene ningún parámetro para modificar el comportamiento predeterminado de Windows Defender, ya que estos parámetros suelen ser específicos de los requisitos del entorno.
  
##### Comunidad Microsoft SpyNet
  
Microsoft SpyNet es una comunidad en línea dedicada a asistir a los usuarios de equipos en el tratamiento de amenazas potenciales de spyware. Además, la comunidad contribuye a detener la propagación de infecciones de spyware nuevas.
  
Cuando Windows Defender detecta software o cambios de software que aún no cuentan con una clasificación de riesgo, puede ver las medidas que otros miembros han tomado con respecto a la alerta. Al mismo tiempo, sus acciones ayudan a otros miembros de la comunidad a elegir la mejor respuesta ante amenazas y permiten a Microsoft identificar el software que debe investigar en busca de posibles riesgos. Puede enviar información básica o adicional sobre el software detectado. La información adicional contribuye a mejorar el funcionamiento de Windows Defender. Por ejemplo, la tecnología puede incluir la ubicación de elementos detectados en el equipo si se ha eliminado software perjudicial. En estos casos, Windows Defender recopilará y enviará la información a la comunidad de forma automática.
  
##### Evaluación de riesgos
  
Los programas spyware presentan varios riesgos graves para las organizaciones que es necesario mitigar con el fin de garantizar la seguridad de los datos y los equipos. Los riesgos identificables más comunes que este tipo de software supone para una organización incluyen los siguientes:
  
-   La información confidencial de la empresa podría quedar expuesta al uso por parte de individuos no autorizados.
  
-   Los datos personales de los empleados podrían quedar expuestos al uso por parte de individuos no autorizados.
  
-   Los equipos pueden quedar bajo el control de atacantes.
  
-   El nivel de productividad puede disminuir por la presencia de spyware que afecta al rendimiento y la estabilidad de los equipos.
  
-   Aumentan los costos de asistencia debido a las infecciones de spyware.
  
-   La organización puede ser víctima de chantajes cuando las infecciones dejan información confidencial al descubierto.
  
##### Reducción de riesgos
  
Windows Defender está diseñado para reducir los riesgos relacionados con programas spyware. Las actualizaciones regulares de la tecnología se proporcionan automáticamente a través de Windows Update, aunque también es posible usar Microsoft Windows Server Update Services (WSUS).
  
Además de la protección contra spyware ofrecida por Windows Defender, Microsoft recomienda encarecidamente la instalación de un paquete antivirus que amplíe la protección a la detección de virus, caballos de Troya y gusanos. Por ejemplo, productos como Microsoft Forefront Client Security proporcionan una defensa unificada ante software malintencionado para los equipos de escritorio, los portátiles y los sistemas operativos de servidor de la empresa.
  
##### Consideraciones para la reducción de riesgos
  
Windows Defender está habilitado en Windows Vista de forma predeterminada. La tecnología está diseñada para ofrecer una protección discreta a los usuarios en condiciones operativas normales. Sin embargo, las organizaciones deberían considerar las recomendaciones siguientes como parte de la implementación de Windows Vista:
  
-   Compruebe la interoperabilidad de los programas de detección de spyware o antivirus en tiempo real de terceros que desee utilizar en la empresa.
  
-   Diseñe un sistema para administrar las implementaciones de actualizaciones de definición de firmas si la organización incluye un gran volumen de equipos.
  
-   Asegúrese de que los empleados conocen los trucos más comunes que los programas spyware emplean para conseguir que el usuario ejecute código malintencionado.
  
-   Adapte la hora de detección programada a las necesidades de la organización. La configuración predeterminada es 2:00 a.m. todos los días. Si el equipo no puede realizar la detección en el momento programado, el usuario recibirá una notificación y se le pedirá que ejecute la detección. Si la operación no se lleva a cabo en un plazo de dos días, la detección tendrá lugar aproximadamente 10 minutos después del próximo reinicio del equipo. La detección se ejecuta como proceso de prioridad baja, de forma que el efecto sobre el cliente sea mínimo. Gracias a las mejoras de rendimiento relacionadas con el tratamiento de entrada y salida (E/S) en Windows Vista, el efecto sobre el usuario de este proceso de detección de prioridad baja es mucho menor que en Windows XP.
  
-   Windows Defender no está diseñado como aplicación anti spyware para empresas. No proporciona un mecanismo centralizado de control, supervisión o generación de informes a nivel empresarial. Si necesita funciones adicionales de control o generación de informes, debería considerar el uso de otros productos, como Microsoft Forefront Client Security.
  
-   Establezca directivas en la organización para informar de posibles amenazas de spyware a la comunidad en línea Microsoft SpyNet.
  
##### Proceso de reducción de riesgos
  
De forma predeterminada, Windows Defender forma parte integral del sistema operativo, por lo que no se requieren pasos adicionales para activar este componente. Sin embargo, debería considerar la aplicación de algunas medidas recomendadas por Microsoft para garantizar la protección continuada de la empresa.
  
**Para usar este proceso:**
  
1.  Estudie las capacidades anti spyware de Windows Vista y Windows Defender.
  
2.  Estudie la configuración de directiva de grupo para Windows Defender.
  
3.  Considere protección antivirus adicional para la organización.
  
4.  Desarrolle un plan de actualización óptimo para los equipos de la empresa. Es posible que los equipos portátiles requieran una configuración de actualizaciones distinta.
  
5.  Asegúrese de que los usuarios aprenden a identificar actividades sospechosas en los equipos.
  
6.  Asegúrese de que los usuarios aprenden a utilizar las herramientas de Windows Defender para facilitar la resolución de las solicitudes de asistencia técnica.
  
###### Uso de la directiva de grupo en la reducción de riesgos para Windows Defender
  
Puede revisar y modificar la configuración disponible de Windows Defender en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Windows Defender**
  
**Tabla 2.4 Configuración del control de Windows Defender**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar actualizaciones de definiciones mediante WSUS y Windows Update</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite configurar Windows Defender para comprobar e instalar actualizaciones de definiciones desde Windows Update cuando no se encuentra disponible un servidor de Windows Server Update Services (WSUS) administrado localmente.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Buscar firmas nuevas previamente a las detecciones programadas</p></td>
<td style="border:1px solid black;"><p>Si habilita este parámetro, se buscarán firmas nuevas antes de que se lleve a cabo la detección programada en el equipo. Si el valor de este parámetro se establece en <strong>Deshabilitado</strong> o <strong>Sin configurar</strong>, la detección programada se iniciará sin descargar firmas nuevas.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Desactivar Windows Defender</p></td>
<td style="border:1px solid black;"><p>El valor predeterminado de este parámetro activa la protección en tiempo real de Windows Defender.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Desactivar mensajes de protección en tiempo real sobre detección de actividad desconocida</p></td>
<td style="border:1px solid black;"><p>Este parámetro determina si Windows Defender solicitará al usuario que permita o bloquee actividades desconocidas.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar detecciones de registro sin riesgo conocidas</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite que se acepten datos de detección de registro durante la protección en tiempo real cuando Windows Defender detecta archivos conocidos que no suponen riesgo alguno. La detección de registro ofrece información detallada sobre los programas que se ejecutan en los equipos supervisados.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Activar detecciones de registro desconocidas</p></td>
<td style="border:1px solid black;"><p>Este parámetro activa la detección de registro durante la protección en tiempo real cuando Windows Defender detecta archivos desconocidos. La detección de registro ofrece información detallada sobre los programas que se ejecutan en los equipos supervisados.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descargar conjunto de firmas completo</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite la descarga de un conjunto completo de firmas, en lugar de obtener únicamente las firmas actualizadas desde la última descarga. La descarga del conjunto de firmas completo puede ayudar a solucionar problemas de instalación de firmas, aunque el archivo es bastante grande y la descarga puede llevar más tiempo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configurar informes de Microsoft SpyNet</p></td>
<td style="border:1px solid black;"><p>Este parámetro establece la participación en la comunidad en línea Microsoft SpyNet.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
#### Servidor de seguridad de Windows
  
Un servidor de seguridad personal constituye una línea de defensa básica contra muchos tipos de software malintencionado. Al igual que ocurre con la funcionalidad de servidor de seguridad en Windows XP Service Pack 2 (SP2), el servidor de seguridad de Windows Vista está activado de forma predeterminada para contribuir a la protección del equipo del usuario en cuanto el sistema operativo entra en funcionamiento.
  
En Windows Vista, Firewall de Windows incluye filtrado de entrada y salida para proteger a los usuarios mediante la restricción de recursos del sistema operativo que presentan un comportamiento inusual. Además, el servidor de seguridad se integra con el reconocimiento de redes de Windows Vista, de forma que puedan aplicarse reglas especializadas según la ubicación del equipo cliente. Por ejemplo, si un equipo portátil se encuentra ubicado en la red de la organización, el administrador del entorno de red de dominio puede definir reglas del servidor de seguridad que coincidan con los requisitos de seguridad de la red. Sin embargo, cuando el usuario intenta conectar el mismo equipo portátil a Internet a través de una red pública, por ejemplo, a una red inalámbrica gratuita, se pueden utilizar automáticamente reglas del servidor de seguridad diferentes para garantizar la protección del equipo contra posibles ataques.
  
Además y, por primera vez en un sistema operativo Windows, Windows Vista integra la administración del servidor de seguridad con la seguridad del protocolo de Internet (IPsec). En Windows Vista, una consola única, Firewall de Windows con seguridad avanzada, integra IPsec y la administración del servidor de seguridad. La consola centraliza el filtrado de tráfico entrante y saliente, así como la configuración de aislamiento del dominio y del servidor IPsec, en la interfaz de usuario para simplificar la configuración y reducir conflictos de directivas.
  
##### Evaluación de riesgos
  
Una conexión de red es fundamental en las empresas modernas. No obstante, esta conexión se ha convertido al mismo tiempo en un objetivo principal de los atacantes. Es necesario mitigar las amenazas asociadas a la conectividad para garantizar la seguridad de los datos y los equipos. Los riesgos identificables más comunes que los ataques basados en red suponen para una organización incluyen los siguientes:
  
-   Atacantes que pudieran lograr acceso a los equipos y, seguidamente, obtener privilegios a nivel administrativo en los sistemas.
  
-   Aplicaciones de detección de redes que los atacantes pueden usar para identificar, de forma remota, los puertos de red abiertos que servirían para el lanzamiento de ataques.
  
-   Información confidencial de la empresa que podría quedar expuesta a usuarios sin autorización en el caso de que un caballo de Troya consiga abrir una conexión de red no autorizada entre un equipo cliente y un atacante.
  
-   Equipos portátiles que pudieran estar expuestos a ataques de red mientras se encuentran fuera del servidor de seguridad de la red de la organización
  
-   Equipos en una red interna que pudieran estar expuestos a un ataque basado en red desde un equipo infectado que conecta directamente a la red interna.
  
-   El riesgo potencial de chantajes a la organización si un atacante consigue acceso a los equipos internos.
  
##### Reducción de riesgos
  
El servidor de seguridad de Windows Vista ofrece protección inmediata a los equipos cliente. Bloqueará la mayor parte del tráfico entrante no solicitado hasta que el administrador o la directiva de grupo realicen algún cambio.
  
Además, Firewall de Windows incluye filtrado de tráfico de red saliente. Esta regla se encuentra configurada de fábrica para permitir todo el tráfico de red saliente. Puede hacer uso de la configuración de directiva de grupo para ajustar estas reglas en el servidor de seguridad de Windows Vista de forma que la seguridad de los equipos cliente sea constante.
  
##### Consideraciones para la reducción de riesgos
  
Hay algunas cuestiones que debería considerar a la hora de determinar el uso del servidor de seguridad incluido en Windows Vista:
  
-   Compruebe la interoperabilidad de las aplicaciones requeridas en los equipos de la organización. Cada aplicación debería contar con un registro de los requisitos de puertos de red para garantizar que sólo se abren los puertos necesarios a través de Firewall de Windows.
  
-   El servidor de seguridad de Windows XP utiliza un perfil de dominio y un perfil estándar. El perfil de dominio está activo cuando el cliente está conectado a una red que contiene los controladores del dominio en que reside su cuenta de equipo. Esto permite crear reglas específicas a los requisitos de la red interna de la organización. El servidor de seguridad de Windows Vista incluye un perfil público y un perfil privado para proporcionar un nivel de control más preciso durante la protección de equipos cliente que los usuarios utilizan fuera de las defensas de red de la organización.
  
-   Evalúe las funciones de registro de Firewall de Windows para determinar su capacidad de integración con las soluciones de supervisión y generación de informes existentes en la empresa.
  
-   De forma predeterminada, Firewall de Windows bloquea el control remoto o la administración remota de los equipos basados en Windows Vista. Microsoft ha creado una serie de reglas específicamente para estas tareas remotas en Firewall de Windows. Si desea que los equipos de la organización admitan estas tareas remotas, deberá habilitar las reglas necesarias en relación con cada perfil para el que se requerirá la tarea. Por ejemplo, quizás desee habilitar la regla de escritorio remoto para el perfil de dominio de forma que el personal de soporte técnico pueda asistir a los usuarios en la red de la organización. Al mismo tiempo, es posible que desee dejar esta regla desactivada para los perfiles público y privado con el fin de reducir la superficie de ataque de los equipos cuando se encuentran fuera de la red.
  
###### Reducción de riesgos mediante Firewall de Windows con seguridad avanzada
  
Windows Vista incluye una configuración nueva de directiva de grupo y una interfaz de usuario de administración que simplifican la configuración de la nueva funcionalidad disponible en el servidor de seguridad de Windows Vista. La configuración de seguridad avanzada de Windows Vista no se aplica a equipos cliente con Windows XP.
  
Microsoft recomienda que revise atentamente estas nuevas capacidades para determinar si pueden ofrecer seguridad mejorada a su entorno. Si se dispone a modificar el funcionamiento predeterminado del servidor de seguridad de Windows Vista, Microsoft aconseja el uso de la configuración de directiva de grupo de Firewall de Windows con seguridad avanzada para administrar equipos cliente que ejecutan Windows Vista.
  
Puede revisar y modificar la nueva configuración de directiva de grupo y el complemento de administración disponibles para Firewall de Windows en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Firewall de Windows con seguridad avanzada**
  
Firewall de Windows con seguridad avanzada es compatible con los siguientes perfiles de entorno:
  
-   **Perfil de dominio.** Se aplica cuando el equipo está conectado a una red y realiza la autenticación con un controlador de dominio en el dominio al que pertenece el equipo.
  
-   **Perfil público.** Este perfil constituye el tipo de ubicación de red predeterminado cuando el equipo no está conectado a un dominio. La configuración del perfil público debe ser lo más restrictiva posible, ya que el equipo se encuentra conectado a una red pública donde la seguridad no se puede controlar de forma tan hermética como en un entorno de TI.
  
-   **Perfil privado.** Este perfil únicamente es aplicable si un usuario con privilegios de administrador local lo asigna a una red configurada previamente como pública. Microsoft recomienda que esto sólo se lleve a cabo con redes de confianza.
  
Es importante entender que no puede haber más de un perfil activo a la vez. Si el equipo cuenta con varias interfaces y están conectadas a varias ubicaciones de red, la selección del perfil que debe aplicarse se rige por las consideraciones siguientes:
  
1.  Si todas las interfaces de red están conectadas a una ubicación de red de dominio, aplique el perfil de dominio.
  
2.  Si todas las interfaces de red están conectadas a una ubicación de red privada, aplique el perfil privado.
  
3.  Si una interfaz de red está conectada a una ubicación de red pública, aplique el perfil público.
  
Microsoft recomienda activar Firewall de Windows con seguridad avanzada para los tres perfiles. Además de las reglas de servidor de seguridad avanzadas, Firewall de Windows admite reglas de seguridad de conexión. La seguridad de conexión conlleva la autenticación de dos equipos antes de que inicien cualquier comunicación y la protección de datos enviados entre los equipos. Firewall de Windows con seguridad avanzada incluye la tecnología IPsec para ofrecer compatibilidad con intercambios de claves, autenticación, integridad de la información y, de forma opcional, cifrado de datos.
  
Para obtener más información, consulte la página Web [IPsec](http://technet.microsoft.com/en-us/network/bb531150.aspx) de Microsoft TechNet (en inglés).
  
El apéndice A, "Configuración de directivas de grupo de seguridad" describe la configuración prescrita de Firewall de Windows con seguridad avanzada e indica los parámetros que requieren información específica del entorno.
  
#### Centro de seguridad de Windows
  
El Centro de seguridad de Windows (WSC) se ejecuta como proceso en segundo plano en equipos cliente con Windows Vista y Windows XP SP2. En Windows Vista, esta característica comprueba y muestra constantemente el estado de cuatro categorías de seguridad importantes:
  
-   Firewall
  
-   Actualizaciones automáticas
  
-   Protección ante software malintencionado
  
-   Configuración adicional de seguridad
  
El proceso WSC también sirve como punto de partida para obtener acceso a otras áreas del equipo relacionadas con la seguridad y proporciona un único punto de referencia para la búsqueda de asistencia y recursos sobre seguridad. Por ejemplo, WSC incluye un vínculo de ayuda que permite a los usuarios que no disponen de software antivirus consultar ofertas de proveedores de soluciones antivirus compatibles con WSC.
  
Microsoft ha mejorado WSC en Windows Vista con una nueva categoría de configuración adicional de seguridad. Esta categoría muestra el estado de la configuración de seguridad de Internet Explorer y del control de cuentas de usuario. Otra categoría nueva en Windows Vista hace referencia a la protección contra software malintencionado, que incluye supervisión de software antivirus y anti spyware. Además de la protección predeterminada ofrecida por Windows Vista, WSC puede supervisar diferentes soluciones de seguridad de terceros para Firewall de Windows, así como software antivirus y anti spyware en ejecución en el mismo equipo cliente, e indicar qué soluciones están habilitadas y actualizadas.
  
En lo que respecta a equipos cliente que ejecutan Windows Vista, WSC proporciona vínculos directos a proveedores que puede utilizar para solucionar problemas que puedan darse en el equipo. Por ejemplo, si una solución antivirus o anti spyware de terceros se encuentra desactivada o no está actualizada, WSC ofrece un botón donde puede hacer clic para iniciar una solución del proveedor en el equipo que corrija el problema. Adicionalmente, WSC incluye vínculos al sitio Web del proveedor para que el usuario pueda activar o renovar la suscripción y obtener actualizaciones. El conocimiento del estado del software de seguridad (si está activado, actualizado, etc.) y la capacidad de descargar actualizaciones fácilmente pueden determinar la protección óptima de los equipos y sistemas o, por el contrario, su vulnerabilidad a ataques de software malintencionado.
  
WSC se ejecuta de forma predeterminada en equipos con Windows Vista. La configuración de directiva de grupo descrita en el capítulo anterior no contiene ningún parámetro para modificar el comportamiento predeterminado de WSC. Sin embargo, los administradores pueden hacer uso de la directiva de grupo para garantizar que la interfaz del usuario del cliente WSC permanece habilitada o deshabilitada en equipos miembros del dominio. Puede revisar y modificar la configuración de la directiva de grupo disponible para WSC en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Centro de seguridad**
  
La plantilla Securitycenter.admx contiene la información referente a XML para esta configuración de directiva. La tabla siguiente describe este parámetro de configuración.
  
**Tabla 2.5 Configuración del Centro de seguridad de Windows**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar el Centro de seguridad (sólo equipos de dominio)</p></td>
<td style="border:1px solid black;"><p>Este parámetro especifica si el Centro de seguridad está activado o desactivado en equipos unidos a un dominio que utiliza Active Directory. Si se utiliza la configuración predeterminada Sin configurar, el Centro de seguridad permanecerá desactivado para equipos miembros del dominio.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de este parámetro. Para obtener más información sobre este parámetro, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
#### Herramienta de eliminación de software malintencionado
  
La Herramienta de eliminación de software malintencionado de Microsoft Windows está diseñada para eliminar software malintencionado de equipos infectados. Con carácter mensual, Microsoft publica una nueva versión de la herramienta a través de Microsoft Update, Windows Update, WSUS y el Centro de descarga de Microsoft. Esta herramienta no presenta funcionalidad antivirus total, por lo que Microsoft recomienda encarecidamente la ejecución de software antivirus para la detección y la eliminación continuadas de virus. La herramienta ejecuta un proceso de detección en segundo plano y genera un informe en caso de detectar infecciones en el equipo. Esta herramienta no se instala en el sistema operativo en proceso de detección. La herramienta no cuenta con parámetros de configuración de directiva de grupo en Windows Vista.
  
##### Evaluación de riesgos
  
Microsoft recomienda la ejecución de un programa antivirus en tiempo real en todos los equipos como complemento a los servicios de protección ofrecidos con Windows Vista. No obstante, incluso con estas medidas de protección en vigor, existen dos riesgos que aún pueden afectar a una organización:
  
-   Es posible que el programa antivirus en tiempo real no detecte algún programa de software malintencionado.
  
-   Es posible que el software malintencionado consiga desactivar el programa antivirus en tiempo real instalado.
  
En estas circunstancias, la Herramienta de eliminación de software malintencionado proporciona una capa adicional de seguridad para asistir en la detección y la eliminación de programas típicos de software malintencionado.
  
##### Reducción de riesgos
  
Con el fin de reducir estos riesgos, Microsoft recomienda la configuración de los equipos cliente para ejecutar Actualizaciones automáticas. Así, se llevará a cabo la descarga y la ejecución de la Herramienta de eliminación de software malintencionado cada vez que se publique.
  
Si está considerando el uso de la herramienta en su entorno, la lista que incluimos a continuación destaca algunos factores que contribuirán a garantizar una implementación satisfactoria:
  
-   La Herramienta de eliminación de software malintencionado tiene un tamaño aproximado de 4 MB. Esto puede influir en la conexión a Internet de la organización si hay muchos equipos cliente que intentan descargar la herramienta al mismo tiempo.
  
-   La herramienta va destinada principalmente a usuarios no corporativos que no disponen de un producto antivirus instalado en el equipo. Sin embargo, puede implementar la herramienta en un entorno empresarial para mejorar la protección existente y como parte de una estrategia de defensa en profundidad. Para implementar la herramienta en un entorno empresarial, puede hacer uso de uno o varios de los métodos siguientes:
  
    -   Windows Server Update Services
  
    -   Paquete de software de SMS
  
    -   Secuencia de comandos de inicio de equipo basada en directiva de grupo
  
    -   Secuencia de comandos de inicio de sesión de usuario basada en directiva de grupo
  
    Para entornos corporativos, Microsoft recomienda la revisión del artículo 891716 de Microsoft Knowledge Base "[Implementación de la Herramienta de eliminación de software malintencionado de Microsoft Windows en un entorno empresarial](http://support.microsoft.com/default.aspx?kbid=891716)" (en inglés).
  
-   Generalmente, la ejecución de la herramienta crea un directorio temporal nombrado de forma aleatoria en la unidad raíz del equipo. Este directorio incluirá varios archivos, entre ellos Mrtstub.exe. En la mayoría de los casos, esta carpeta se elimina automáticamente tras la ejecución de la herramienta o tras el siguiente reinicio del equipo. Sin embargo, hay ocasiones en que la carpeta pudiera no eliminarse de forma automática. En estas circunstancias, puede eliminar la carpeta manualmente sin que se produzcan efectos negativos en el equipo.
  
-   Es posible que un usuario inicie la sesión en un equipo durante la ejecución de la herramienta en segundo plano. Quizás la herramienta se esté ejecutando como parte de una implementación que usa Windows Server Update Services. De ser así, Windows advertirá al usuario que el perfil de usuario actual está dañado y se está creando un perfil nuevo. Puede eliminar el perfil nuevo para resolver este problema. El usuario podrá volver a iniciar la sesión en el sistema cuando la herramienta no esté en ejecución. Este problema suele darse sobre todo en equipos basados en Windows 2000.
  
##### Proceso de reducción de riesgos
  
Para hacer un uso eficaz de la Herramienta de eliminación de software malintencionado, siga el proceso descrito a continuación.
  
**Para usar este proceso:**
  
1.  Estudie las capacidades de la Herramienta de eliminación de software malintencionado.
  
    Para obtener más información, consulte la página Web dedicada a la [Herramienta de eliminación de software malintencionado](http://www.microsoft.com/security/malwareremove/default.mspx) (en inglés).
  
2.  Evalúe la necesidad de la herramienta en el entorno.
  
3.  Determine el método más apropiado para la implementación de la herramienta en la organización.
  
4.  Identifique los sistemas de la empresa que podrían beneficiarse de la protección que ofrece la herramienta.
  
5.  Implemente la herramienta con el método seleccionado.
  
#### Directivas de restricción de software
  
Las directivas de restricción de software proporcionan a los administradores un mecanismo para identificar software de aplicaciones y controlar su capacidad de ejecución en los equipos locales. Esta característica puede ser útil para proteger los equipos que ejecutan Windows Vista y Windows XP Professional contra conflictos conocidos y ataques de software malintencionado, como virus y caballos de Troya. Las directivas de restricción de software se integran completamente con Active Directory y la directiva de grupo. También es posible usar esta característica en equipos independientes. Puede utilizar las directivas de restricción de software para realizar lo siguiente:
  
-   Controlar el software que se puede ejecutar en los equipos cliente del entorno.
  
-   Restringir el acceso a archivos específicos en equipos multiusuario.
  
-   Decidir qué usuarios pueden agregar editores de confianza a los equipos cliente.
  
-   Definir si las directivas afectan a todos los usuarios o a un subconjunto de usuarios de los equipos cliente.
  
-   Impedir la ejecución de archivos ejecutables en los equipos locales según las directivas establecidas en los niveles de equipo, unidad organizativa, sitio y dominio.
  
**Importante**   Es importante que pruebe minuciosamente todos los parámetros de configuración de directiva descritos en esta guía antes de implementarlos en el entorno de producción. Esto se aplica especialmente a la configuración de directivas de restricción de software. Los errores en el diseño o la implementación de esta característica pueden causar importante frustración en los usuarios.
  
Las directivas de restricción de software no han cambiado de forma significativa en Windows Vista. Por ello, esta guía no se ocupa de este tema. Para obtener más información sobre el diseño y la implementación de estas directivas, consulte el artículo ["Uso de directivas de restricción de software como protección contra software no autorizado"](http://www.microsoft.com/technet/windowsvista/security/rstrplcy.mspx) en TechNet (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tecnologías de defensa de Internet Explorer 7
  
Los sitios Web malintencionados pueden suponer riesgos para los equipos cliente que administra. Internet Explorer 7 incluye tecnologías que contribuyen a impedir la instalación de software no deseado y otras que pueden evitar la transmisión no autorizada de datos personales, lo que mejora considerablemente la seguridad del explorador y la protección de la privacidad. Las nuevas tecnologías de seguridad de Internet Explorer 7 incluyen:
  
-   Modo protegido de Internet Explorer
  
-   ActiveX Opt-in
  
-   Protección contra ataques de secuencias de comandos entre dominios
  
-   Barra de estado de seguridad
  
-   Filtro de suplantación de identidad (phishing)
  
-   Características de seguridad adicionales
  
Internet Explorer 7 está disponible para Windows Vista y Windows XP. Windows Vista ofrece una experiencia mejorada de Internet Explorer. Por ejemplo, algunas características de Internet Explorer 7, como el Modo protegido y el Control parental, no están disponibles al usar el explorador en equipos cliente con Windows XP. Además, la interfaz de usuario Aero no está disponible con Internet Explorer 7 en equipos que ejecutan Windows XP.
  
#### Modo protegido de Internet Explorer
  
El Modo protegido de Internet Explorer en Windows Vista ofrece defensas adicionales para proporcionar a los usuarios una experiencia de exploración de Internet más segura. Adicionalmente, este modo contribuye a impedir intentos malintencionados de tomar el control del explorador del usuario y ejecutar código mediante privilegios elevados.
  
El Modo protegido reduce las vulnerabilidades previas del software en las extensiones del explorador al eliminar la posibilidad de utilizarlas para la instalación silenciosa de código malintencionado. Hace uso de mecanismos con niveles de integridad superiores en Windows Vista que restringen el acceso a los procesos, los archivos y las claves del Registro para lograr este objetivo. La interfaz de programación de aplicaciones (API) del Modo protegido permite a los proveedores de software desarrollar extensiones y complementos para Internet Explorer capaces de interactuar con el sistema de archivos y el Registro mientras el explorador se encuentra en este modo.
  
En Modo protegido, Internet Explorer 7 se ejecuta con permisos reducidos para evitar que la configuración o los archivos del sistema o del usuario se modifiquen sin el permiso explícito del usuario. La nueva arquitectura del explorador incluye, además, un proceso de negociación que permite la habilitación de aplicaciones existentes para la elevación fuera del Modo protegido de forma más segura. Esto impide la descarga de datos fuera de los directorios en modo restringido del explorador, por ejemplo, la carpeta Archivos temporales de Internet.
  
El Modo protegido está habilitado en Internet Explorer 7 de forma predeterminada para todas las zonas de seguridad, a excepción de la zona Sitios de confianza. Sin embargo, los usuarios pueden desactivar el modo, lo que reduce la seguridad general. Por este motivo, la configuración de directiva de grupo descrita en el capítulo anterior habilita el Modo protegido en todas las zonas de contenido Web para el explorador, excepto en la zona Sitios de confianza, e impide que los usuarios puedan desactivarlo.
  
Puede revisar y modificar la configuración de la directiva de grupo para el Modo protegido de Internet Explorer 7 en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet\\Página Seguridad\\&lt;*Zona*&gt;**
  
La tabla siguiente describe este parámetro de configuración.
  
**Tabla 2.6 Configuración del Modo protegido**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Activar Modo protegido *</p></td>
<td style="border:1px solid black;"><p>Con este parámetro habilitado, el Modo protegido estará activado y los usuarios no podrán desactivarlo.<br />
Con este parámetro deshabilitado, el Modo protegido estará desactivado y los usuarios no podrán activarlo.<br />
Si este parámetro se establece en <strong>Sin</strong> <strong>configurar,</strong> los usuarios podrán activar y desactivar el Modo protegido.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
\* Este parámetro sólo funciona en Internet Explorer 7 con Windows Vista.
  
Esta tabla ofrece una descripción sencilla de este parámetro. Para obtener más información sobre este parámetro, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
El Modo protegido está disponible para las áreas y zonas de seguridad siguientes en Internet Explorer 7:
  
-   Internet
  
-   Intranet
  
-   Máquina local
  
-   Internet bloqueado
  
-   Intranet bloqueado
  
-   Máquina local bloqueada
  
-   Sitios restringidos bloqueados
  
-   Sitios de confianza bloqueados
  
-   Sitios restringidos
  
-   Sitios de confianza
  
#### ActiveX Opt-in
  
Internet Explorer 7 en Windows Vista ofrece un mecanismo de seguridad innovador y eficaz para la plataforma ActiveX que facilita la protección de la información del usuario y los sistemas informáticos. ActiveX Opt-in desactiva automáticamente todos los controles no permitidos explícitamente por el usuario. Esto reduce el riesgo de que se produzca un uso incorrecto de los controles preinstalados.
  
En Windows Vista, la barra de información solicita la confirmación del usuario antes de ofrecer acceso a controles ActiveX instalados previamente que aún no se han utilizado en Internet. Este mecanismo de notificación permite al usuario otorgar o denegar acceso para cada control individual, lo que reduce el área de superficie vulnerable a ataques. Los usuarios malintencionados no podrán utilizar sitios Web para iniciar ataques automatizados con controles ActiveX cuyo uso original no está destinado a Internet.
  
#### Protección contra ataques de secuencias de comandos entre dominios
  
Las nuevas barreras de secuencias de comandos entre dominios restringen la capacidad de sitios Web malintencionados para aprovechar puntos vulnerables en otros sitios Web. Por ejemplo, sin la protección contra ataques de secuencias de comandos entre dominios, un usuario podría visitar una página incluida en un sitio Web malintencionado que abre una ventana del explorador nueva con una página legítima (como un sitio Web bancario) donde se solicita la información de cuenta del usuario. Seguidamente, una secuencia de comandos puede extraer esta información para facilitársela al atacante. Con Internet Explorer 7, la protección contra ataques de secuencias de comandos entre dominios contribuye al fracaso de este tipo de ataques.
  
#### Barra de estado de seguridad
  
La nueva barra de estado de seguridad en Internet Explorer 7 permite a los usuarios distinguir rápidamente entre sitios Web auténticos y sitios Web sospechosos o malintencionados. Para proporcionar esta información, la barra de estado de seguridad mejora el acceso a los datos de certificados digitales que facilitan la identificación de sitios Web seguros (HTTPS).
  
La barra ofrece a los usuarios indicaciones visuales claras y prominentes sobre la seguridad y la identidad de los sitios Web. Además, la tecnología utiliza información sobre certificados de seguridad alta para identificar con claridad los sitios seguros (HTTPS) que cuentan con medidas de identificación más eficaces.
  
#### Filtro de suplantación de identidad (phishing)
  
La suplantación de identidad es una técnica que muchos atacantes utilizan para conseguir que los usuarios de equipos revelen sus datos personales o financieros en un mensaje de correo electrónico o un sitio Web. El atacante se hace pasar por una persona o una empresa legítimas para lograr que el usuario proporcione sus datos, por ejemplo, contraseñas de cuenta o números de tarjeta de crédito. El filtro de suplantación de identidad de Internet Explorer 7 informa a los usuarios acerca de sitios Web sospechosos o conocidos por este tipo de ataque para que puedan hacer un uso más seguro de Internet. El filtro analiza el contenido de los sitios Web en busca de técnicas de suplantación de identidad conocidas y hace uso de una red global de recursos de datos para evaluar el nivel de confianza de los sitios.
  
Los desarrolladores que se ocupan de crear mensajes de correo electrónico, anuncios en línea y sitios Web fraudulentos aprovechan la falta de comunicación y el uso compartido limitado de la información. El nuevo filtro de suplantación de identidad de Internet Explorer 7, que se sirve de un servicio en línea para actualizar el filtro varias veces cada hora, consolida la información más reciente de la industria sobre sitios Web fraudulentos y la comparte con los clientes de Internet Explorer 7 para proporcionarles advertencias de forma activa y ofrecerles protección.
  
El filtro combina búsquedas de características de sitios Web sospechosos del lado cliente con un servicio en línea opcional. Ofrece protección a los usuarios frente a ataques de suplantación de identidad de tres modos distintos:
  
-   Compara las direcciones de sitios Web que el usuario intenta visitar con una lista de sitios legítimos especificados almacenada en el equipo.
  
-   Analiza los sitios Web que el usuario visita en busca de características típicas de los sitios de suplantación de identidad.
  
-   Envía las direcciones de los sitios Web que el usuario desea visitar a un servicio en línea mantenido por Microsoft, donde se comprueban inmediatamente en una lista de sitios de suplantación de identidad actualizada con frecuencia. Estos sitios han quedado confirmados como fraudulentos por fuentes fidedignas que proporcionan la información a Microsoft.
  
Aunque un sitio concreto sea desconocido en el servicio de filtro de suplantación de identidad, Internet Explorer 7 puede examinar el comportamiento del sitio e informar al usuario de cualquier actividad sospechosa, por ejemplo, la recopilación de datos del usuario sin un certificado SSL. Así, el filtro evita que los sitios puedan recopilar información sobre el usuario antes de que se haya informado de ellos de forma oficial.
  
Al ejecutar Internet Explorer 7, el filtro de suplantación de identidad está configurado de forma predeterminada para solicitar al usuario la habilitación o la deshabilitación del filtro. La configuración de directiva de grupo descrita en el capítulo anterior no contiene ningún parámetro para modificar este comportamiento predeterminado. Sin embargo, los administradores pueden controlar el comportamiento del filtro mediante la directiva de grupo.
  
Puede revisar y modificar la configuración de directiva de grupo disponible para el filtro de suplantación de identidad en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**
  
La tabla siguiente describe este parámetro de configuración.
  
**Tabla 2.7 Configuración del filtro de suplantación de identidad**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Deshabilitar administración del filtro de suplantación de identidad *</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite al usuario habilitar un filtro de suplantación de identidad para recibir advertencias en caso de que los sitios Web visitados sean conocidos por intentos fraudulentos de recopilar información personal mediante ataques de suplantación de identidad.<br />
De forma predeterminada, se solicitará al usuario que elija el modo de operación del filtro.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
\* Para aprovechar este parámetro de configuración, el equipo debe ejecutar Internet Explorer 7 con cualquiera de los sistemas operativos siguientes: Windows Vista, Windows XP SP2 o Windows Server 2003 Service Pack 1 (SP1).
  
Esta tabla ofrece una descripción sencilla de este parámetro. Para obtener más información sobre este parámetro, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Microsoft recomienda establecer el filtro en **Habilitado** y el modo de operación en **Automático**. No obstante, los administradores deben tener en cuenta que esta configuración permite envíos automáticos de datos a Microsoft por parte del explorador sin informar al usuario.
  
#### Características de seguridad adicionales
  
Internet Explorer incluye diversas características de seguridad especializadas que contribuyen a la protección contra software malintencionado. Es posible administrar todos estos parámetros de configuración a través de la directiva de grupo.
  
Puede revisar y modificar la configuración de las características de seguridad de la directiva de grupo disponible para Internet Explorer 7 en la ubicación siguiente del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad**
  
Esta sección ofrece información general sobre estos parámetros en Internet Explorer 7. Para obtener una lista completa de los parámetros de configuración de directiva de grupo para Internet Explorer 7, consulte el Editor de objetos de directiva de grupo.
  
**Nota**   Todas las características incluidas en esta sección funcionan también en equipos con Internet Explorer 6.0 y versiones posteriores con los sistemas operativos siguientes: Windows XP SP2 y Windows Server 2003 SP1.
  
##### Administración de complementos
  
Puede hacer uso de la configuración de la directiva en esta sección para restringir los complementos que puede utilizar Internet Explorer 7. Los parámetros de configuración de esta tabla sirven para administrar los complementos.
  
**Tabla 2.8 Configuración de la administración de complementos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de complementos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite administrar una lista de complementos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Denegar complementos a menos que se permitan específicamente en la Lista de complementos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite el uso exclusivo de los complementos especificados por el usuario para la ejecución con Internet Explorer 7.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite seleccionar si las preferencias de usuario afectan a los procesos (como refleja el Administrador de complementos) o a la configuración de la directiva.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite seleccionar si las preferencias de usuario afectan a los procesos en la lista (como se especifica en el Administrador de complementos) o a la configuración de la directiva.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Restricción de seguridad de comportamiento binario
  
Internet Explorer incluye comportamientos binarios dinámicos: componentes que encapsulan la funcionalidad específica de los elementos HTML a los que se adjuntaron. Puede hacer uso de los parámetros de configuración de esta tabla para restringir estos comportamientos.
  
**Tabla 2.9 Configuración de la restricción de seguridad de comportamiento binario**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro sirve para permitir o evitar la restricción de seguridad de comportamiento binario.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Sin</strong> <strong>configurar</strong> o <strong>Habilitado</strong>, se evitarán los comportamientos binarios en procesos del Explorador de Windows e Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Comportamientos aprobados por el administrador</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro como <strong>Habilitado</strong>, se permitirá la definición de una lista de comportamientos en cada zona para Permitir los comportamientos de binarios y secuencias de comandos como Aprobado por el administrador.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Administración coherente de MIME
  
Internet Explorer utiliza datos MIME (Extensiones seguras multipropósito de correo de Internet) para determinar los procedimientos de administración de archivos recibidos a través de un servidor Web. La tabla siguiente proporciona información sobre la configuración de directiva de grupo con MIME disponible para Internet Explorer 7.
  
**Tabla 2.10 Configuración de la administración coherente de MIME**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro determina si Internet Explorer debe requerir que toda la información de tipo de archivo proporcionada por los servidores Web sea coherente.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Este parámetro determina si Internet Explorer debe requerir la coherencia de los datos MIME para todos los archivos recibidos.<br />
Si establece este parámetro en <strong>Sin</strong> <strong>configurar</strong> o <strong>Habilitado</strong>, Internet Explorer exigirá la coherencia de los datos MIME para todos los archivos recibidos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Barra de información
  
La configuración de directivas de esta sección permite seleccionar la presentación de la barra de dirección para procesos ajenos a Internet Explorer cuando existen restricciones de instalación de código o archivos. De forma predeterminada, la barra de información está presente sólo durante procesos de Internet Explorer. La tabla siguiente proporciona información sobre la configuración que puede utilizar para modificar este comportamiento.
  
**Tabla 2.11 Configuración de la barra de información**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, la barra de información se mostrará para todos los procesos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Deshabilitado</strong>, la barra de información no se mostrará para procesos de Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite seleccionar la presentación de la barra de dirección para procesos específicos cuando existen restricciones de instalación de código o archivos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
##### Seguridad de bloqueo de zona Máquina local
  
Internet Explorer establece restricciones de zona para cada página Web que abre. Las restricciones dependen de la ubicación de las páginas (Internet, intranet, máquina local, etc). Las páginas Web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Máquina local. La seguridad de la zona Máquina local se aplica a todos los archivos y contenidos locales. Esta característica contribuye a reducir los ataques cuando la zona Máquina local se usa como vector de ataque para cargar código HTML malintencionado.
  
**Tabla 2.12 Configuración de seguridad de bloqueo de la zona Máquina local**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, la seguridad de la zona Máquina local se aplica a todos los archivos y contenidos locales que utilicen los procesos ajenos a Internet Explorer o que no están definidos en una lista de procesos.<br />
De forma predeterminada, la seguridad de la zona Máquina local no se aplica al contenido ni a los archivos locales que utilizan los procesos ajenos a Internet Explorer o que no están definidos en una lista de procesos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Sin</strong> <strong>configurar</strong> o <strong>Habilitado</strong>, la seguridad de la zona Máquina local se aplica a todos los archivos y contenidos locales procesados por Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong> y define un nombre de proceso con un valor de <strong>1</strong>, se aplicará la seguridad de la zona Máquina local. Si define un valor de <strong>0</strong>, no se aplicará la seguridad de la zona Máquina local.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Característica de seguridad de examen de MIME
  
Esta característica contribuye a evitar la conversión de un archivo de un tipo determinado a un tipo de archivo más peligroso. La tabla siguiente enumera los parámetros disponibles para esta característica.
  
**Tabla 2.13 Configuración de la característica de seguridad de examen de MIME**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, la característica de seguridad de examen de MIME estará habilitada para todos los procesos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si configura este parámetro como <strong>Deshabilitado</strong>, los procesos de Internet Explorer permitirán un examen de MIME que convierta un tipo de archivo a un tipo más peligroso.<br />
La configuración predeterminada (<strong>Sin</strong> <strong>configurar</strong>) no permite la conversión.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro de directiva permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Restricción de seguridad del protocolo MK
  
El parámetro de directiva Restricción de seguridad del protocolo MK reduce el área de superficie de ataque al bloquear el protocolo MK. Si habilita este parámetro, se producirán errores en los recursos alojados en el protocolo MK.
  
**Tabla 2.14 Configuración de la restricción de seguridad del protocolo MK**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Esta restricción está deshabilitada de forma predeterminada para todos los procesos. Sin embargo, si establece este parámetro en <strong>Habilitado</strong>, se bloqueará el protocolo MK para todos los procesos. Asimismo, quedará bloqueado cualquier uso del protocolo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Deshabilitado</strong>, las aplicaciones podrán usar la API del protocolo MK y los recursos alojados en el protocolo funcionarán con los procesos del Explorador de Windows e Internet Explorer.<br />
La configuración predeterminada bloquea el protocolo MK para el Explorador de Windows e Internet Explorer, así como los recursos alojados en el protocolo.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro de directiva permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Bloqueo de protocolo de red
  
Es posible configurar Internet Explorer 7 para evitar que el contenido activo obtenido a través de protocolos restringidos se ejecute de forma no segura. Este parámetro de directiva sirve para permitir o evitar la restricción de contenido obtenido a través de protocolos restringidos.
  
**Tabla 2.15 Configuración del bloqueo de protocolo de red**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, se permitirá la restricción de contenido obtenido a través de protocolos restringidos para todos los procesos ajenos al Explorador de Windows y a Internet Explorer. Si establece este parámetro en <strong>Deshabilitado</strong>, se impedirá la restricción de contenido obtenido a través de protocolos restringidos para todos los procesos ajenos al Explorador de Windows y a Internet Explorer. La configuración predeterminada (<strong>Sin</strong> <strong>configurar</strong>) no aplica esta directiva a los procesos ajenos al Explorador de Windows y a Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, se permitirá la restricción de contenido obtenido a través de protocolos restringidos para los procesos del Explorador de Windows e Internet Explorer. Si establece este parámetro en <strong>Deshabilitado</strong>, se impedirá la restricción de contenido obtenido a través de protocolos restringidos para los procesos del Explorador de Windows e Internet Explorer. Si se utiliza la configuración predeterminada (<strong>Sin configurar</strong>), Internet Explorer omitirá este parámetro de configuración.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a los administradores definir aplicaciones para las que desean permitir o impedir la restricción de contenido obtenido a través de protocolos restringidos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
Para cada zona, se puede configurar la restricción de seguridad ofrecida por el bloqueo de protocolo de red para evitar que el contenido activo obtenido a través de protocolos restringidos se ejecute de forma no segura, ya sea mediante la intervención del usuario o la deshabilitación del contenido.
  
**Nota**   Si establece directivas para una zona tanto en la configuración del equipo como en la configuración del usuario, esta acción restringirá ambas listas de protocolo en relación con dicha zona.
  
**Tabla 2.16 Configuración de protocolos restringidos para zonas de seguridad**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Protocolos restringidos para la zona Internet</p></td>
<td style="border:1px solid black;"><p>La habilitación de este parámetro crea una lista de protocolos restringidos para la zona Internet.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protocolos restringidos para la zona Intranet</p></td>
<td style="border:1px solid black;"><p>La habilitación de este parámetro crea una lista de protocolos restringidos para la zona Intranet.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protocolos restringidos para la zona Máquina local</p></td>
<td style="border:1px solid black;"><p>La habilitación de este parámetro crea una lista de protocolos restringidos para la zona Máquina local.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Protocolos restringidos para la zona Sitios restringidos</p></td>
<td style="border:1px solid black;"><p>La habilitación de este parámetro crea una lista de protocolos restringidos para la zona Sitios restringidos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Protocolos restringidos para la zona Sitios de confianza</p></td>
<td style="border:1px solid black;"><p>La habilitación de este parámetro crea una lista de protocolos restringidos para la zona Sitios de confianza.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Protección de caché de objetos
  
Este parámetro de directiva establece si las referencias a objetos permanecen accesibles cuando el usuario navega en un mismo dominio o a un dominio nuevo.
  
**Tabla 2.17 Configuración de la protección de caché de objetos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Deshabilitado</strong> o <strong>Sin</strong> <strong>configurar</strong>, las referencias a objetos se mantienen durante la navegación en un mismo dominio o en dominios diferentes en la zona Sitios restringidos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si utiliza este parámetro como <strong>Sin configurar</strong> o lo establece en <strong>Habilitado</strong>, las referencias a objetos no permanecerán accesibles durante la navegación en un mismo dominio o en dominios diferentes para los procesos de Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Protección contra elevación de zona
  
Internet Explorer establece restricciones para cada página Web que abre. Las restricciones dependen de la ubicación de las páginas (Internet, intranet, máquina local, etc). Por ejemplo, las páginas Web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Máquina local, lo que convierte la zona de seguridad Máquina local en un objetivo principal para los usuarios malintencionados.
  
**Tabla 2.18 Configuración de la protección contra elevación de zona**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si establece este parámetro en <strong>Habilitado</strong>, podrá ofrecer protección contra la elevación a cualquier zona para todos los procesos.<br />
Si utiliza este parámetro como <strong>Sin</strong> <strong>configurar</strong> o lo establece en <strong>Deshabilitado</strong>, los procesos ajenos a Internet Explorer o que no se encuentren definidos en la lista de procesos no recibirán esta protección.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si utiliza este parámetro como <strong>Sin</strong> <strong>configurar</strong> o lo establece en <strong>Habilitado</strong>, podrá ofrecer protección a cualquier zona contra la elevación por procesos de Internet Explorer.<br />
Si establece este parámetro en <strong>Deshabilitado</strong>, la protección no se aplicará a procesos de Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro de directiva permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Limitar la instalación de ActiveX
  
Estos parámetros de directiva aplican restricciones a la instalación de controles ActiveX.
  
**Tabla 2.19 Configuración de limitación de la instalación de ActiveX**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a las aplicaciones que alojan el control del explorador Web bloquear los avisos automáticos sobre la instalación de controles ActiveX.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite bloquear avisos de instalación de controles ActiveX para procesos de Internet Explorer.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Con este parámetro, los administradores pueden definir una lista de ejecutables para los que es posible bloquear o permitir los avisos automáticos sobre la instalación de controles ActiveX. Esta característica de seguridad está habilitada de forma predeterminada.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Limitar la descarga de archivos
  
Estos parámetros de directiva aplican restricciones a las descargas de archivos que se intentan iniciar de forma automática sin intervención del usuario.
  
**Tabla 2.20 Configuración de la limitación de la descarga de archivos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite a las aplicaciones que alojan el control del explorador Web bloquear los avisos automáticos sobre la descarga de archivos sin intervención del usuario.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Este parámetro permite bloquear los avisos automáticos sobre la descarga de archivos sin intervención del usuario.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Con este parámetro, los administradores pueden definir una lista de ejecutables para los que es posible bloquear o permitir los avisos automáticos sobre la descarga de archivos sin intervención del usuario.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
##### Restricciones de seguridad de ventanas con secuencias de comandos
  
Internet Explorer permite que las secuencias de comandos, mediante programación, abran ventanas de diferentes tipos y cambien su tamaño y ubicación. Esta característica de seguridad restringe las ventanas emergentes y prohíbe que las secuencias de comandos muestren ventanas con títulos y barras de estado no visibles para los usuarios o que obstruyan el título y la barra de estado de otras ventanas.
  
**Tabla 2.21 Configuración de las restricciones de seguridad de ventanas con secuencias de comandos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto de directiva</p></th>
<th><p>Descripción</p></th>
<th><p>Valores predeterminados de Windows Vista</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Todos los procesos</p></td>
<td style="border:1px solid black;"><p>Si utiliza este parámetro como <strong>Sin</strong> <strong>configurar</strong> o lo establece en <strong>Habilitado</strong>, no se restringirá el uso de ventanas con secuencias de comandos. Si establece este parámetro en <strong>Habilitado</strong>, las ventanas con secuencias de comandos quedarán restringidas para todos los procesos.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Procesos de Internet Explorer</p></td>
<td style="border:1px solid black;"><p>Si utiliza este parámetro como <strong>Sin</strong> <strong>configurar</strong> o lo establece en <strong>Habilitado</strong>, se aplicarán las restricciones de ventanas emergentes, entre otras, a los procesos del Explorador de Windows e Internet Explorer. Sin embargo, si establece el parámetro en <strong>Deshabilitado</strong>, las secuencias de comandos podrán crear ventanas emergentes, entre otras, que obstruyan la presentación de otras ventanas.</p></td>
<td style="border:1px solid black;"><p>Sin configurar ‡</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Lista de procesos</p></td>
<td style="border:1px solid black;"><p>Este parámetro de directiva permite a los administradores definir aplicaciones con las que desean usar o evitar esta característica de seguridad.</p></td>
<td style="border:1px solid black;"><p>Sin configurar</p></td>
</tr>
</tbody>
</table>
  
Esta tabla ofrece una descripción sencilla de los parámetros de configuración. Para obtener más información sobre un parámetro concreto, consulte la ficha **Explicación** del parámetro en el Editor de objetos de directiva de grupo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
Para obtener información adicional sobre las características y tecnologías de seguridad nuevas y mejoradas de Windows Vista, consulte los recursos siguientes:
  
-   [Herramienta de eliminación de software malintencionado](http://www.microsoft.com/security/malwareremove/default.mspx) en Microsoft.com (en inglés)
  
-   El capítulo [Directiva de restricción de software para clientes Windows XP](http://www.microsoft.com/technet/security/prodtech/windowsxp/secwinxp/xpsgch06.mspx) de la *Guía de seguridad de Windows XP* en Microsoft TechNet (en inglés)
  
-   [Control de cuentas de usuario](http://www.microsoft.com/technet/windowsvista/security/uacppr.mspx) en TechNet (en inglés)
  
-   ["Uso de directivas de restricción de software como protección contra software no autorizado"](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx) en TechNet (en inglés)
  
-   [Windows Defender](http://www.microsoft.com/windowsdefender) en TechNet (en inglés)
  
-   [Firewall de Windows](http://www.microsoft.com/windowsfirewall) en TechNet (en inglés)
  
-   [Directiva de grupo](http://www.microsoft.com/windowsserver2003/technologies/management/grouppolicy/default.mspx) de Windows Server 2003 en Microsoft.com (en inglés)
  
-   [Mejoras de seguridad y protección de datos en Windows Vista](http://www.microsoft.com/technet/windowsvista/evaluate/feat/secfeat.mspx) en TechNet (en inglés)
  
-   [Shell de comandos de Windows XP: información general](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/ntcmds_shelloverview.mspx) en Microsoft.com (en inglés)
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Consiga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)
  
[](#mainsection)[Principio de la página](#mainsection)
