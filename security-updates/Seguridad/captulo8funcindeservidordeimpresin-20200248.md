---
TOCTitle: 'Capítulo 8: Función de servidor de impresión'
Title: 'Capítulo 8: Función de servidor de impresión'
ms:assetid: '897b32c2-f09c-4b08-b10c-37f73aa516df'
ms:contentKeyID: 20200248
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163129(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 8: Función de servidor de impresión

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

Este capítulo se centra en cómo consolidar los servidores de impresión en los que se ejecuta Microsoft® Windows* *Server™ * *2003 con SP1, un proceso que puede plantear dificultades. Los servicios básicos que proporcionan estos servidores requieren los protocolos de Bloque de mensajes del servidor (SMB) y Sistema común de archivos de Internet (CIFS). Estos dos protocolos pueden ofrecer una gran cantidad de información a los usuarios no autenticados. A menudo, estos protocolos están deshabilitados en los servidores de impresión en entornos Windows de alta seguridad. Sin embargo, será difícil tanto para los administradores como para los usuarios obtener acceso a los servidores de impresión si estos protocolos se deshabilitan en su entorno.

La mayor parte de los parámetros que se describen en este capítulo se configuran y aplican mediante Directiva de grupo. Un objeto de directiva de grupo (GPO) que complementa la Directiva de línea de base de servidores miembro (MSBP) puede vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores de impresión con el fin de proporcionar la configuración de seguridad necesaria para esta función de servidor. Este capítulo sólo trata aquellas configuraciones de la directiva que varían del MSBP.

Siempre que sea posible, estos parámetros de configuración se reunirán en una plantilla incremental de Directiva de grupo que se aplicará a la unidad organizativa de servidores de impresión. Parte de los ajustes que se muestran en este capítulo no se pueden aplicar mediante Directiva de grupo. Se proporciona información detallada acerca de cómo configurar estos ajustes manualmente.

En la siguiente tabla se muestran los nombres de las plantillas de seguridad de servidor de impresión para los tres entornos que se definen en esta guía. Estas plantillas proporcionan la configuración de directiva para la plantilla incremental de servidor de impresión que, a su vez, se utiliza para crear un nuevo GPO. Éste se vincula a la unidad organizativa Servidores de impresión en el entorno apropiado. Se proporcionan instrucciones detalladas en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", para ayudarle a crear las UO y Directivas de grupo, e importar la plantilla de seguridad apropiada en cada GPO.

**Tabla 8.1 Plantillas de seguridad de servidor de impresión para los tres entornos**

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
<td style="border:1px solid black;"><p>LC-Print Server.inf</p></td>
<td style="border:1px solid black;"><p>EC-Print Server.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Print Server.inf</p></td>
</tr>  
</tbody>  
</table>
  
Para obtener más información acerca de la configuración en el MSBP, consulte el capítulo 4, “Directiva de línea de base de servidores miembro”. Para obtener más información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159)*, *que está disponible en* *http://go.microsoft.com/fwlink/?LinkId=15159.
  
**Nota**: sólo es posible un acceso fiable a los servidores de impresión que se protegen con la plantilla de seguridad SSLF-Print Server.inf desde equipos cliente protegidos con una configuración compatible. Consulte la *Guía de seguridad de Windows XP* para obtener más información acerca de cómo asegurar equipos cliente con la configuración compatible con SSLF.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
Las configuraciones de directiva de auditoría para los servidores de impresión en los tres entornos que se definen en esta guía se establecen a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP activa el registro de información de auditoría de seguridad en todos los servidores de impresión.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Asignaciones de derechos de usuario
  
La configuración de asignaciones de derechos de usuario para los servidores de impresión en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP establece de un modo uniforme las asignaciones de derechos de los usuarios en todos los servidores de impresión.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
La mayoría de los parámetros de configuración para los servidores de impresión en los tres entornos que se definen en esta guía se configuran a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". Las diferencias entre MSBP y la Directiva de grupo de servidor de impresión se describen en la sección siguiente.
  
#### Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)
  
**Tabla 8.2 Configuración recomendada para firmar digitalmente las comunicaciones (siempre)**

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
<td style="border:1px solid black;"><p>Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
<td style="border:1px solid black;"><p>Deshabilitado</p></td>
</tr>  
</tbody>  
</table>
  
Esta configuración de directiva determina si el componente de servidor SMB requiere la firma de paquetes. El protocolo SMB constituye la base del uso compartido de recursos de impresión y de archivos, además de otras muchas operaciones de red en Microsoft, como la administración remota de Windows. Para evitar ataques de intermediario, con los que se modifican los paquetes SMB en tránsito, el protocolo SMB admite la firma digital de paquetes SMB. Esta configuración de directiva determina si la firma de paquetes SMB se debe negociar antes de que se permita una nueva comunicación con un cliente SMB.
  
Aunque el parámetro **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)** se deshabilita de forma predeterminada, MSBP habilita este parámetro para servidores del entorno SSLF, lo que permite a los usuarios imprimir pero no ver la cola de impresión. Los usuarios que intenten tener acceso a la cola de impresión verán un mensaje indicándoles que se les deniega el acceso.
  
El parámetro **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)** se configura como **Deshabilitado** para los servidores de impresión en los tres entornos que se definen en esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
La configuración de registro de eventos para los servidores de impresión en los tres entornos que se definen en esta guía se establece a través de MSBP. Para obtener más información acerca del MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
Aunque la configuración de seguridad aplicada a través de MSBP mejora considerablemente la seguridad de los servidores de impresión, hay algunos parámetros de configuración adicionales que deben tenerse en cuenta. Los parámetros de configuración de esta sección no se pueden aplicar a través de Directiva de grupo y, por lo tanto, deben establecerse manualmente en todos los servidores de impresión.
  
#### Seguridad de las cuentas conocidas
  
Microsoft Windows Server 2003 con SP 1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.
  
El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.
  
**Para proteger las cuentas conocidas en los servidores de impresión**
  
-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.
  
-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás.
  
-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.
  
-   Registre cualquier cambio que haga en una ubicación segura.
  
    **Nota**: el nombre de la cuenta integrada de Administrador puede cambiarse mediante la utilización de la directiva de grupo. Esta configuración no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque cada organización debe escoger un nombre único para esta cuenta. Sin embargo, se puede configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de las cuentas de administrador en los tres entornos que se definen en esta guía. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.
  
#### Seguridad de las cuentas de servicios
  
A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de la directiva utilizando SCW
  
Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
**Para crear la directiva de servidor de impresión**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el equipo al dominio, que aplicará toda la configuración de seguridad de las UO principales.
  
4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor que comparte esta función. Los ejemplos incluyen servicios específicos de la función, software y agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
6.  Asegúrese de que las funciones de servidor detectadas sean apropiadas para su entorno; por ejemplo, la función de servidor de impresión.
  
7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
9.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
11. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.
  
12. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
13. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
14. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-Print Server.inf).
  
15. Guarde la directiva con un nombre apropiado (por ejemplo, Print Server.xml).
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método nativo de implementación ofrece la ventaja de poder deshacer fácilmente las directivas implementadas desde SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.
  
La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.
  
Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.
  
Para obtener más información acerca de cómo probar las directivas del SCW, consulte la [Guía de implementación para el Asistente para la configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx* *y la [documentación del Asistente para la configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.
  
#### Conversión e implementación de la directiva
  
Después de probar completamente la directiva, complete los pasos siguientes para convertirla en un GPO e implementarla:
  
1.  En el símbolo de sistema, escriba el siguiente comando:
  
    ```  
scwcmd transform /p:&lt;PathToPolicy.xml&gt; /g:&lt;GPODisplayName&gt;  
```
  
    y, a continuación, pulse Entrar. Por ejemplo:
  
    ```  
scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Print Server.xml" /g:"Print Server Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han explicado las configuraciones de directiva que se pueden utilizar para servidores de impresión en los que se ejecuta Windows Server 2003 con SP1 para los tres entornos que se definen en esta guía. La mayoría de las configuraciones de la directiva se aplican mediante un objeto de directiva de grupo (GPO) que se diseñó para complementar el MSBP. Los GPO pueden vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores de impresión para proporcionar seguridad adicional.
  
Algunas configuraciones de directiva que se han tratado no se pueden aplicar a través de Directiva de grupo. Para esta configuración de directiva, se proporcionan detalles sobre la configuración manual.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores de impresión en los que se ejecuta Windows Server 2003 con SP1.
  
-   Para obtener información general acerca de los servidores de impresión, consulte "[Technical Overview of Windows Server 2003 Print Services](http://www.microsoft.com/windowsserver2003/techinfo/overview/print.mspx)", que se puede descargar en www.microsoft.com/windowsserver2003/techinfo/overview/print.mspx.
  
-   Para obtener más información acerca de los servidores de impresión, consulte "[What's New in File and Print Services](http://www.microsoft.com/windowsserver2003/evaluation/overview/technologies/fileandprint.mspx)" en www.microsoft.com/windowsserver2003/evaluation/overview/technologies/  
    fileandprint.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
