---
TOCTitle: 'Capítulo 12: Función de los hosts de baluarte'
Title: 'Capítulo 12: Función de los hosts de baluarte'
ms:assetid: 'c663fb69-d017-4f65-b812-01882f39a34b'
ms:contentKeyID: 20200252
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163137(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 12: Función de los hosts de baluarte

Actualizado: 27/12/05

##### En esta página

[](#ehaa)[Información general](#ehaa)
[](#egaa)[Configuración de directiva de auditoría](#egaa)
[](#efaa)[Asignaciones de derechos de usuario](#efaa)
[](#eeaa)[Opciones de seguridad](#eeaa)
[](#edaa)[Configuración del registro de eventos](#edaa)
[](#ecaa)[Configuración de seguridad adicional](#ecaa)
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Este capítulo se centra en cómo reforzar la seguridad de los hosts de baluarte que ejecutan Microsoft® Windows* *Server™* *2003* *con Service Pack 1 (SP1) en el entorno. Los hosts de baluarte son equipos seguros a los que todo el mundo puede obtener acceso y que se ubican en el lado público de la red perimetral de una organización (también conocida como DMZ, zona desmilitarizada y subred protegida). Estos tipos de hosts no se encuentran protegidos por un servidor de seguridad o un enrutador de filtrado, por lo que quedan totalmente a merced de cualquier ataque. Para reducir al mínimo la posibilidad de que resulten comprometidos, los hosts de baluarte se deben diseñar y configurar con mucha atención.

Los hosts de baluarte se utilizan a menudo como servidores web, servidores DNS, servidores de protocolo de transferencia de archivos (FTP), servidores de protocolo simple de transferencia de correo (SMTP) y servidores de protocolo de transferencia de noticias a través de la red (NNTP). Lo ideal es que los hosts de baluarte se dediquen a desempeñar solamente una de estas funciones, ya que cuantas más funciones tengan que proporcionar, mayor será la probabilidad de que se pase por alto un error en la seguridad. Resulta más fácil proteger sólo un servicio en un único host de baluarte que garantizar la seguridad de varios servicios. Las organizaciones que se pueden permitir tener varios hosts de baluarte se pueden beneficiar enormemente de las ventajas que ofrece este tipo de arquitectura de red.

Los hosts de baluarte seguros se configuran de forma muy distinta a los hosts convencionales. Se deshabilitan o quitan todos los servicios, protocolos, programas e interfaces de red que no son necesarios y, a continuación, cada host de baluarte se configura para desempeñar una función específica. El uso de este mecanismo para reforzar la seguridad de los hosts de baluarte le permite limitar los métodos posibles de ataque.

En las siguientes secciones de este capítulo se describen distintas configuraciones de seguridad que permiten proteger los hosts de baluarte de cualquier entorno. Los pasos incluidos en este capítulo le ayudarán a crear un host de baluarte SMTP. Deberá modificar los archivos de configuración que se incluyen con la guía para agregar cualquier funcionalidad adicional.

#### Directiva local de host de baluarte

Las funciones de servidor descritas anteriormente en esta guía utilizaban la directiva de grupo para configurar los servidores. La directiva de grupo no se puede aplicar a los servidores host de baluarte, ya que están configurados como hosts independientes que no pertenecen a un dominio del servicio de directorio de Active* *Directory®. Debido a su riesgo de sufrir un ataque y a que no están protegidos por otros dispositivos, sólo se recomienda un conjunto determinado de instrucciones para los servidores host de baluarte de los tres entornos que se definen en esta guía. Las configuraciones de seguridad descritas en este capítulo se basan en la directiva de línea de base de servidores miembro (MSBP) para el entorno SSLF definido en el capítulo 4, "Directiva de línea de base de servidores miembro", y se incluyen en una plantilla de seguridad que se debe aplicar a la directiva local de host de baluarte (BHLP) de cada host.

**Tabla 12.1 Plantillas de seguridad de servidor host de baluarte**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Cliente heredado</p></th>
<th><p>Cliente de empresa</p></th>
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>SSLF-Bastion Host.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Bastion Host.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Bastion Host.inf</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
La configuración de directiva de auditoría de BHLP para los hosts de baluarte se incluye en el archivo SSLF-Bastion Host.inf y es la misma que la especificada en el archivo** **SSLF-Member Server Baseline.inf. Para obtener más información acerca de la directiva MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de la directiva MSBP garantiza que toda la información de auditoría de seguridad pertinente se registre en todos los servidores host de baluarte.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Asignaciones de derechos de usuario
  
El archivo SSLF-Bastion Host.inf incluye las asignaciones de derechos de usuario de la directiva BHLP para los host de baluarte. Estas configuraciones de directiva se basan en las especificadas en el archivo SSLF-Member Server Baseline.inf en el capítulo 4, "Directiva de línea de base de servidores miembro". En la información de la siguiente tabla se resumen las diferencias entre las directivas BHLP y MSBP. En las subsecciones que siguen a la tabla se proporciona información detallada.
  
**Tabla 12.2 Configuración recomendada de las asignaciones de derechos de usuario**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Asignación de derechos de usuario</p></th>  
<th><p>Configuración</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el acceso desde la red a este equipo</p></td>
<td style="border:1px solid black;"><p>INICIO DE SESIÓN ANÓNIMO; Administrador integrado; Support_388945a0; Invitado; todas las cuentas de servicio que NO sean del sistema operativo</p></td>
</tr>  
</tbody>  
</table>
  
#### Denegar el acceso desde la red a este equipo
  
**Nota**: INICIO DE SESIÓN ANÓNIMO, Administrador integrado, Support\_388945a0; Invitado; y todas las cuentas de servicio que NO sean del sistema operativo no se incluyen en la plantilla de seguridad. Estas cuentas y grupos tienen identificadores de seguridad únicos (SID). Por lo tanto, deberá agregarlas manualmente a la directiva BHLP.
  
Esta configuración de directiva determina qué usuarios no pueden tener acceso a un equipo a través de la red. Deniega una serie de protocolos de red, entre los que se encuentran los protocolos basados en bloque de mensajes del servidor (SMB), NetBIOS, sistema común de archivos de Internet (CIFS), HTTP y el modelo de objetos componentes Plus (COM+). Esta configuración de directiva invalida la configuración **Tener acceso a este equipo desde la red** cuando una cuenta de usuario está sujeta a ambas directivas. Si configura este derecho de usuario para otros grupos, podría limitar la capacidad de los usuarios de realizar tareas administrativas delegadas en su entorno.
  
En el capítulo 4, "Directiva de línea de base de servidores miembro", se recomienda incluir el grupo **Invitados** en la lista de usuarios y grupos que están asignados a este derecho de usuario para proporcionar el máximo nivel posible de seguridad. No obstante, la cuenta IUSR que se utiliza para el acceso anónimo a IIS es miembro de forma predeterminada del grupo **Invitados**.
  
La configuración **Denegar el acceso desde la red a este equipo** está establecida para incluir INICIO DE SESIÓN ANÓNIMO; Administrador integrado; Support\_388945a0; Invitado y todas las cuentas de servicio que NO sean del sistema operativo de los host de baluarte en el entorno SSLF que se define en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
Las configuraciones de las opciones de seguridad de BHLP para los hosts de baluarte son las mismas que las especificadas en el archivo SSLF-Member Server Baseline.inf del capítulo 4, "Directiva de línea de base de servidores miembro". Estas configuraciones de la directiva BHLP garantizan que todas las opciones de seguridad relevantes se establezcan de forma uniforme en los servidores host de baluarte.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
Las configuraciones del registro de eventos de BHLP para los hosts de baluarte son las mismas que las especificadas en el archivo SSLF-Member Server Baseline.inf del capítulo 4, "Directiva de línea de base de servidores miembro". Estas configuraciones de la directiva BHLP garantizan que todas las opciones del registro de eventos relevantes se establezcan de forma uniforme en los servidores host de baluarte.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
La configuración de seguridad aplicada por la directiva BHLP mejora considerablemente la seguridad de los servidores host de baluarte. Sin embargo, es preciso tener en cuenta una serie de configuraciones adicionales. Estas configuraciones no se pueden aplicar mediante la directiva de grupo; se deben configurar manualmente en todos los servidores host de baluarte.
  
#### Adición manual de grupos de seguridad únicos a las asignaciones de derechos de usuario
  
La mayor parte de las asignaciones de derechos de usuario que se aplican a través de MSBP contienen los grupos de seguridad adecuados especificados en las plantillas de seguridad que acompañan a esta guía. Sin embargo, existen algunas cuentas y grupos de seguridad que no se pueden incluir en las plantillas debido a que sus identificadores de seguridad (SID) son específicos de dominios individuales de Windows* *Server* *2003. Las configuraciones de las asignaciones de derechos de usuario que se indican en la siguiente tabla se deben establecer manualmente.
  
**Advertencia**: en la siguiente tabla se incluyen valores para la cuenta integrada Administrador. No hay que confundir esta cuenta con el grupo de seguridad **Administradores** integrado. Si se agrega el grupo de seguridad **Administradores** al derecho de usuario "Denegar acceso", deberá iniciar sesión localmente para corregir el error.
  
Además, es posible que se haya cambiado el nombre de la cuenta de administrador integrada, tal como se recomienda en el capítulo 4, "Directiva de línea de base de servidores miembro". Al agregar la cuenta de administrador a un derecho de usuario, asegúrese de especificar la cuenta cuyo nombre ha cambiado.
  
**Tabla 12.3 Asignaciones de derechos de usuario agregadas manualmente**

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
<th><p>Configuración</p></th>  
<th><p>Cliente heredado</p></th>  
<th><p>Cliente de empresa</p></th>  
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Denegar el acceso desde la red a este equipo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
<td style="border:1px solid black;"><p>Administrador integrado; Support_388945a0;</p>
<p>Invitado; todas las cuentas de servicios que NO sean del sistema operativo</p></td>
</tr>
</tbody>
</table>
<p> </p>

**Importante**: “Todas las cuentas de servicio del sistema que no sean del sistema operativo” incluye las cuentas de servicio que se utilizan para aplicaciones específicas en una empresa, pero NO incluye las cuentas de SISTEMA LOCAL, SERVICIO LOCAL ni de SERVICIO DE RED (las cuentas incorporadas que el sistema operativo utiliza).

#### Seguridad de las cuentas conocidas

Windows Server 2003 con SP 1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.

De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.

El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.

**Para proteger las cuentas conocidas en los servidores host de baluarte**

-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada servidor.

-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los servidores, un atacante que obtuviera acceso a un servidor podría tener acceso a los demás.

-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.

-   Registre cualquier cambio que haga en una ubicación segura.

#### Informe de errores

**Tabla 12.4 Configuración recomendada de informes de errores**

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
<th><p>Configuración</p></th>
<th><p>Cliente heredado</p></th>
<th><p>Cliente de empresa</p></th>
<th><p>Seguridad especializada: Funcionalidad limitada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Desactivar Informe de errores de Windows</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
<td style="border:1px solid black;"><p>Habilitada</p></td>
</tr>  
</tbody>  
</table>
  
Este servicio ayuda a Microsoft a realizar un seguimiento de los errores así como a solucionarlos. Puede configurar este servicio para generar informes para los errores del sistema operativo, componentes de Windows o de programa. Sólo está disponible en Windows XP Professional y Windows Server 2003.
  
El servicio **Informe de errores** puede informar de dichos errores a Microsoft a través de Internet o a un recurso compartido de archivos internos. Aunque los informes de error puedan incluir datos corporativos de contenido delicado o incluso confidenciales, la directiva de privacidad de Microsoft con respecto a la notificación de errores asegura que Microsoft no utilizará dichos datos de forma incorrecta. No obstante, los datos se transmiten en HTTP de texto sin formato y podrían ser interceptados en Internet y visualizados por terceros.
  
La configuración **Desactivar Informe** **de errores de Windows** controla si el servicio **Informe de errores** transmite datos.
  
Puede configurar esta configuración de directiva en Windows Server 2003 en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Administración de comunicaciones de Internet\\Configuración de comunicaciones de Internet**
  
Establezca la configuración **Desactivar Informe** **de errores de Windows** como **Habilitado** en la BHLP para los tres entornos que se definen en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de la directiva utilizando SCW
  
Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
Durante los pasos de creación de la directiva de servidor probablemente elimine la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.
  
**Para crear la directiva de host de baluarte**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada host de baluarte. Por ejemplo, programas antivirus o contra software espía.
  
4.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
5.  Compruebe que las funciones de servidor detectadas son adecuadas para el host de baluarte (por ejemplo, servidor web). Quite las demás funciones de servidor.
  
6.  Compruebe que las características de cliente detectadas son adecuadas para su entorno. Quite todas las características de cliente que no necesite. Por ejemplo, debería quitar las características **Cliente de redes de Microsoft** y **Cliente DHCP** para reducir la superficie de ataque del servidor.
  
7.  Para contar con una protección máxima, quite todas las opciones administrativas menos Firewall de Windows. Las opciones adicionales aumentarán la capacidad de administración del host de baluarte, pero incrementarán también su superficie de ataque. Sopese minuciosamente las ventajas de cualquier opción que no sea crucial para un funcionamiento adecuado del host de baluarte frente a los riesgos de seguridad potenciales que puede conllevar.
  
8.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
9.  Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
10. Compruebe que la casilla de verificación **Omitir esta sección** está desactivada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows. Desactive todos los puertos, excepto los necesarios para la función de host de baluarte.
  
11. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
12. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
13. Incluya la plantilla de seguridad apropiada (por ejemplo, SSLF-Bastion Host.inf).
  
14. Guarde la directiva con un nombre apropiado (por ejemplo, Bastion Host.xml).
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Como los equipos de la función de host de baluarte no están conectados a un dominio, debe aplicar la configuración con SCW. No puede utilizar la directiva de grupo sin un dominio.
  
La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.
  
Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.
  
Para obtener más información acerca de cómo probar las directivas del SCW, consulte la [Guía de implementación para el Asistente para la configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx* *y la [documentación del Asistente para la configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.
  
#### Implementación de la directiva
  
Después de probar completamente la directiva, siga los pasos siguientes para implementarla:
  
1.  Inicie la interfaz gráfica de usuario de SCW.
  
2.  Seleccione **Aplicar una directiva de seguridad existente**.
  
3.  Seleccione el archivo XML creado anteriormente. Por ejemplo, Bastion Host.xml.
  
4.  Siga los pasos del asistente de SCW para aplicar la configuración.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Ahora, debe realizar una última prueba para asegurarse de que SCW aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Como los servidores host de baluarte que ejecutan Windows* *Server* *2003 con SP1 no están protegidos por otros dispositivos, como un servidor de seguridad, están expuestos a los ataques externos. Se deben proteger tanto como sea posible para aumentar al máximo su disponibilidad y reducir la posibilidad de que su seguridad resulte comprometida. Los servidores host de baluarte más seguros limitan el acceso a sólo las cuentas que merecen mucha confianza y habilitan únicamente los servicios que son necesarios para desempeñar por completo sus funciones.
  
En este capítulo se ha explicado la configuración y los procedimientos que se pueden utilizar para reforzar la seguridad de los servidores host de baluarte. Gran parte de los parámetros de configuración se pueden aplicar a través de la Directiva de grupo local. También se ha proporcionado una orientación acerca de cómo configurar y aplicar la configuración manual.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con reforzar la seguridad de los servidores host de baluarte que ejecutan Windows Server 2003 con SP1.
  
-   Para obtener más información sobre la creación de redes privadas, consulte el artículo "[Firewalls and Virtual Private Networks](http://www.wiley.com/legacy/compbooks/press/0471348201_09.pdf)" redactado por Elizabeth D. Zwicky, Tonelero de Simon y Brent D. Chapman en www.wiley.com/legacy/compbooks/press/0471348201\_09.pdf (en inglés).
  
-   Para obtener información acerca de la seguridad y los firewall, consulte el artículo "[Internet Firewalls and Security – A Technology Overview](http://www.itmweb.com/essay534.htm)" redactado por Chuck Semeria en www.itmweb.com/essay534.htm (en inglés).
  
-   Para obtener información acerca del modelo de defensa en profundidad, consulte la página sobre la [defensa en profundidad](http://usmilitary.about.com/careers/usmilitary/library/glossary/d/bldef01834.htm) de la institución militar de EE.UU. en http://usmilitary.about.com/careers/usmilitary/library/glossary/d/bldef01834.htm (en inglés).
  
-   Para obtener información sobre las medidas de seguridad para hacer frente a los intrusos, consulte el artículo "[Intruder Detection Checklist](http://www.cert.org/tech_tips/intruder_detection_checklist.html)" redactado por Jay Beale en www.cert.org/tech\_tips/intruder\_detection\_checklist.html (en inglés).
  
-   Para obtener más información acerca de cómo reforzar los host de baluarte, consulte el artículo "[Hardening Bastion Hosts](http://www.sans.org/rr/whitepapers/basics/420.php)" de SANS Info Sec Reading Room en www.sans.org/rr/whitepapers/basics/420.php (en inglés).
  
-   Para obtener información acerca de la solución de problemas de la herramienta Configuración y análisis de seguridad, consulte el artículo de Microsoft Knowledge Base sobre los [problemas después de importar varias plantillas a la herramienta Configuración y análisis de seguridad](http://support.microsoft.com/?kbid=279125) en http://support.microsoft.com/?kbid=279125 (en inglés).
  
-   Para obtener información acerca de la seguridad de los sitios, consulte el manual "[Site Security Handbook](http://www.faqs.org/rfcs/rfc2196.html)" en www.faqs.org/rfcs/rfc2196.html (en inglés).
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
