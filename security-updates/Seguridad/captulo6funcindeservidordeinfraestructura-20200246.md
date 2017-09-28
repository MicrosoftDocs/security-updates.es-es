---
TOCTitle: 'Capítulo 6: Función de servidor de infraestructura'
Title: 'Capítulo 6: Función de servidor de infraestructura'
ms:assetid: 'ed0c9484-c1e8-4399-8da1-488342ca6503'
ms:contentKeyID: 20200246
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163125(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 6: Función de servidor de infraestructura

##### En esta página

Actualizado: 27/12/05

[](#ehaa)[Información general](#ehaa)
[](#egaa)[Configuración de directiva de auditoría](#egaa)
[](#efaa)[Configuración de Asignación de derechos de usuario](#efaa)
[](#eeaa)[Opciones de seguridad](#eeaa)
[](#edaa)[Configuración del registro de eventos](#edaa)
[](#ecaa)[Configuración de seguridad adicional](#ecaa)
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

En este capítulo se explica la configuración de directiva que se puede usar para reforzar la seguridad de los servidores de infraestructura que ejecutan Windows Server 2003 con Service Pack 1 en los tres entornos definidos en esta guía. Para los propósitos de esta guía, un servidor de infraestructura es uno que proporciona los servicios DHCP o la funcionalidad de Microsoft WINS.

La mayor parte de los parámetros que se describen en este capítulo se configuran y aplican mediante Directiva de grupo. Se puede vincular un objeto de directiva de grupo (GPO) que complemente a la directiva de línea de base de servidores miembro (MSBP) a las unidades organizativas (UO) adecuadas que contengan los servidores de infraestructura para proporcionar una seguridad adicional a los servidores. Este capítulo sólo trata aquellas configuraciones de la directiva que varían del MSBP.

En los casos en los que es posible, estas configuraciones de directiva se han recopilado en un objeto de directiva de grupo incremental que se aplicará a la UO Servidores de infraestructura. Parte de los ajustes que se muestran en este capítulo no se pueden aplicar mediante Directiva de grupo. Se proporciona información detallada acerca de cómo configurar estos ajustes manualmente.

En la siguiente tabla se incluyen los nombres de las plantillas de seguridad de servidor de infraestructura para los tres entornos definidos en esta guía. Estas plantillas proporcionan la configuración de directiva para la plantilla de servidor de infraestructura incremental, que a su vez se usa para crear un nuevo GPO que está vinculado a la UO Servidores de infraestructura en el entorno adecuado. Se proporcionan instrucciones detalladas en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", para ayudarle a crear las UO y Directivas de grupo, e importar la plantilla de seguridad apropiada en cada GPO.

**Tabla 6.1 Plantillas de seguridad de servidor de infraestructura**

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
<td style="border:1px solid black;"><p>LC-Infrastructure Server.inf</p></td>
<td style="border:1px solid black;"><p>EC-Infrastructure Server.inf</p></td>
<td style="border:1px solid black;"><p>SSLF-Infrastructure Server.inf</p></td>
</tr>
</tbody>
</table>
  
Para obtener más información acerca de la configuración de la directiva en el MSBP, consulte el capítulo 4, “Directiva de línea de base de servidores miembro”. Para obtener más información acerca de todas las configuraciones predeterminadas de la directiva, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159)*, *que está disponible en * *http://go.microsoft.com/fwlink/?LinkId=15159.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de directiva de auditoría
  
La configuración de directiva de auditoría para los servidores de infraestructura de los tres entornos definidos en esta guía se establece a través de la directiva MSBP. Para obtener más información acerca de la directiva MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de la directiva MSBP garantiza que toda la información de auditoría de seguridad pertinente se registre en los servidores de infraestructura.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de Asignación de derechos de usuario
  
Las asignaciones de derechos de usuario para los servidores de infraestructura de los tres entornos definidos en esta guía se establecen a través de la directiva MSBP. Para obtener más información acerca de la directiva MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de la directiva MSBP establece de forma uniforme todas las asignaciones de derechos de usuario en todos los servidores de infraestructura.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Opciones de seguridad
  
La configuración de opciones de seguridad para los servidores de infraestructura de los tres entornos definidos en esta guía se establece a través de la directiva MSBP. Para obtener más información acerca de la directiva MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de la directiva MSBP establece de forma uniforme las opciones de seguridad relevantes en todos los servidores de infraestructura.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del registro de eventos
  
La configuración del registro de eventos para los servidores de infraestructura de los tres entornos definidos en esta guía se establece a través de la directiva MSBP. Para obtener más información acerca del MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de seguridad adicional
  
La configuración de seguridad aplicada por la directiva MSBP aumenta notablemente la seguridad de los servidores de infraestructura. En esta sección se analizan algunos parámetros de configuración adicionales. Los parámetros de esta sección no se pueden configurar mediante la directiva de grupo y se deben establecer de forma manual en todos los servidores de infraestructura.
  
#### Configuración del registro de DHCP
  
El servicio DHCP sólo registra de forma predeterminada los eventos de inicio y cierre en el registro de eventos. Siga los pasos siguientes para habilitar un registro más detallado en el servidor DHCP:
  
1.  Haga clic con el botón secundario del mouse en el servidor DHCP en la herramienta de administración de DHCP.
  
2.  Seleccione **Propiedades**.
  
3.  En la ficha **General** del cuadro de diálogo **Propiedades**, haga clic en **Habilitar la auditoría del registro DHCP**.
  
Al finalizar estos pasos, el servidor DHCP creará un archivo de registro en la siguiente ubicación:
  
**%systemroot%\\system32\\dhcp\\**
  
La información de los clientes DHCP suele ser difícil de localizar en los archivos de registro, ya que la única información que se almacena en la mayoría de los registros son nombres de equipos, no direcciones IP. Los registros de auditoría DHCP proporcionan una herramienta adicional para localizar los orígenes de los ataques internos o las actividades involuntarias.
  
Sin embargo, la información de estos registros no es de ningún modo infalible, ya que los nombres de host y el control de acceso a medios (MAC) se pueden falsificar. (La suplantación de identidad hace que una transmisión parezca venir de un usuario distinto del que realizó la acción.) Sin embargo, las ventajas que esta información proporciona compensan los costos en que se incurre si está habilitado el registro en un servidor DHCP. Puede ser muy útil disponer de varias direcciones IP y nombres de equipo a la hora de determinar el modo en que una dirección IP concreta se ha utilizado en una red.
  
De forma predeterminada, los grupos **Opers. de servidores** y **Usuarios autenticados** disponen de permisos de lectura en los archivos de registro DHCP. Para proteger mejor la integridad de la información registrada por un servidor DHCP, se recomienda limitar el acceso a estos registros a los administradores de los servidores. Los grupos **Opers. de servidores** y **Usuarios autenticados** se deben quitar de la lista de control de acceso (ACL) de la carpeta **%systemroot%\\system32\\dhcp\\**.
  
En teoría, los registros de auditoría de DHCP podrían llenar el disco en el que están almacenados. No obstante, la configuración predeterminada de **Habilitar la auditoría del registro DHCP** asegura que el registro se detenga si hay menos de 20 MB de espacio libre en el disco del servidor. Esta configuración predeterminada resulta adecuada para los servidores de la mayoría de los entornos, aunque se puede modificar para garantizar que haya suficiente espacio en disco para otras aplicaciones de un servidor. Para obtener información acerca de cómo modificar esta configuración, consulte la página que contiene información sobre [DhcpLogMinSpaceOnDisk](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/f7802dce-3ff9-406a-b3e6-c0c6b3ed4941.mspx) en el sitio de Windows Server 2003 Tech Center en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/  
DepKit/f7802dce-3ff9-406a-b3e6-c0c6b3ed4941.mspx (en inglés).
  
#### Protección frente a los ataques de denegación del servicio de DHCP
  
Los servidores DHCP son recursos esenciales que proporcionan el acceso de clientes a la red; por este motivo, se pueden convertir en los principales objetivos de un ataque DoS. Si un servidor DHCP sufre un ataque y no puede atender las solicitudes DHCP, los clientes de éste no podrán adquirir concesiones finalmente. Estos clientes perderán su concesión de dirección IP existente y la capacidad para tener acceso a los recursos de la red.
  
No sería muy complicado escribir una secuencia de comandos de herramienta de ataque que solicite todas las direcciones disponibles en un servidor DHCP. Esta secuencia de comandos agotaría el grupo de direcciones IP disponibles para posteriores solicitudes legítimas de clientes DHCP. También es posible que un usuario malintencionado configure todas las direcciones IP de DHCP en el adaptador de red de un equipo que administre, lo que causaría que el servidor DHCP detectase los conflictos de dirección IP de todas las direcciones de su ámbito y rechazase la asignación de concesiones DHCP.
  
Asimismo, tal y como sucede con los demás servicios de red, un ataque DoS que agote la capacidad del servidor DHCP para responder al tráfico legítimo (por ejemplo, el agotamiento de la CPU o el llenado del búfer de solicitudes del proceso de escucha de DHCP) podría impedir a los clientes solicitar concesiones y renovaciones. Este tipo de problema se puede evitar si se crea un diseño apropiado de los servicios DHCP.
  
Puede configurar servidores DHCP en pares y seguir la recomendación de la regla 80/20 regla (es decir, dividir los ámbitos de los servidores DHCP entre los servidores de modo que un 80% de las direcciones se distribuyan con un servidor DHCP y un 20% con otro) para ayudar a mitigar la repercusión de estos tipos de ataques. Estas sugerencias de configuración son útiles para garantizar que los clientes pueden seguir recibiendo la configuración de dirección IP a pesar de que se produzca un error en el servidor. Para obtener más información sobre la regla 80/20 y el protocolo DHCP, consulte la página que contiene detalles sobre [DHCP](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/default.asp?url=/resources/documentation/windows/2000/server/reskit/en-us/cnet/cncb_dhc_klom.asp) del Kit de recursos de Windows 2000 Server en www.microsoft.com/resources/documentation/Windows/2000/server/  
reskit/en-us/cnet/cncb\_dhc\_klom.asp (en inglés).
  
**Nota**: la regla 80/20 descrita en el Kit de recursos de Windows 2000 Server también es aplicable a los servicios DHCP de Windows Server 2003 con SP1.
  
#### Seguridad de las cuentas conocidas
  
Windows Server 2003 con SP 1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.
  
El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.
  
**Para proteger las cuentas conocidas en los servidores de infraestructura**
  
-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.
  
-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás con el mismo nombre de cuenta y contraseña.
  
-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.
  
-   Registre cualquier cambio que haga en una ubicación segura.
  
    **Nota**: se puede cambiar el nombre de la cuenta integrada Administrador desde Directiva de grupo. Esta configuración de directiva no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque cada organización debe escoger un nombre único para esta cuenta. Sin embargo, puede configurar el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de las cuentas de administrador en los tres entornos que se definen en esta guía. Esta configuración de directiva forma parte de la configuración Opciones de seguridad de un GPO.
  
#### Seguridad de las cuentas de servicios
  
A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de la directiva utilizando SCW
  
Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.
  
Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración de directiva para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, instale el sistema operativo en un hardware similar al hardware que se utiliza en su implementación para garantizar la mayor compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
Durante los pasos de creación de la directiva de servidor probablemente elimine la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.
  
**Para crear la directiva de servidor de infraestructura**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el equipo al dominio, que aplicará toda la configuración de seguridad de las UO principales.
  
4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor que comparte esta función. Los ejemplos incluyen servicios específicos de la función, software y agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
6.  Compruebe que las funciones de servidor detectadas son adecuadas para su entorno; por ejemplo, las funciones de servidor DHCP y servidor WINS.
  
7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
9.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
11. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.
  
12. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
13. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.
  
14. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-Infrastructure Server.inf).
  
15. Guarde la directiva con un nombre apropiado (por ejemplo, Infrastructure Server.xml).
  
#### Prueba de la directiva utilizando SCW
  
Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método original de implementación le permite deshacer fácilmente las directivas implementadas desde el SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.
  
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
scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Infrastructure.xml" /g:"Infrastructure Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración de directiva deseada. Para finalizar este procedimiento, confirme que se ha establecido la configuración de directiva apropiada y que la funcionalidad no se ve afectada.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se ha explicado la configuración de directiva que se puede usar para los servidores DHCP y WINS que ejecutan Windows Server 2003 con SP1 en los tres entornos definidos en esta guía. La mayoría de los parámetros de estas funciones se aplican a través de MSBP. El objetivo principal de crear un objeto de directiva de infraestructura para los servidores DHCP y WINS es habilitar los servicios necesarios para que el funcionamiento de estas funciones sea íntegro y seguro.
  
Aunque la directiva MSBP ofrece un alto nivel de seguridad, en este capítulo se han analizado otras consideraciones para las funciones de servidor de infraestructura. Una de las consideraciones principales fue la generación de archivos de registro.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con reforzar la seguridad de los servidores de infraestructura que ejecutan Windows Server 2003 con SP1.
  
-   Para obtener información acerca de cómo ha cambiado el registro DHCP en Windows Server 2003, consulte el artículo de Microsoft Knowledge Base “[Cambios en el registro DHCP de Windows Server 2003](http://support.microsoft.com/?kbid=328891)” en http://support.microsoft.com/?kbid=328891.
  
-   Para obtener más información acerca de DHCP, consulte la página que contiene detalles sobre el [Protocolo de configuración dinámica de host](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/default.asp?url=/resources/documentation/windows/2000/server/reskit/en-us/cnet/cncb_dhc_klom.asp) en www.microsoft.com/resources/documentation/Windows/2000/server/reskit/  
    en-us/cnet/cncb\_dhc\_klom.asp (en inglés).
  
-   Para obtener más información acerca de WINS, consulte la página que contiene una [descripción general del servicio de nombres de Internet de Windows (WINS) de Windows 2000 Server](http://www.microsoft.com/technet/archive/windows2000serv/evaluate/featfunc/nt5wins.mspx) en www.microsoft.com/technet/archive/windows2000serv/evaluate/featfunc/nt5wins.mspx (en inglés).
  
-   Para obtener información acerca de la instalación de WINS en Windows Server 2003, consulte la página que contiene detalles sobre la [instalación y administración de servidores WINS](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/a29d0a59-8bdd-4a82-a980-b53bd72fcb0e.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/  
    ServerHelp/a29d0a59-8bdd-4a82-a980-b53bd72fcb0e.mspx (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
