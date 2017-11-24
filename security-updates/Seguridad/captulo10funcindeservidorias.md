---
TOCTitle: 'Capítulo 10: Función de servidor IAS'
Title: 'Capítulo 10: Función de servidor IAS'
ms:assetid: 'edd5e9dd-fda5-41a5-8b71-80ce960bc394'
ms:contentKeyID: 20200250
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163133(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 10: Función de servidor IAS

Actualizado: 27/12/05

##### En esta página

[](#ehaa)[Información general](#ehaa)  
[](#egaa)[Directiva de auditoría](#egaa)  
[](#efaa)[Asignaciones de derechos de usuario](#efaa)  
[](#eeaa)[Opciones de seguridad](#eeaa)  
[](#edaa)[Registro de eventos](#edaa)  
[](#ecaa)[Configuración de seguridad adicional](#ecaa)  
[](#ebaa)[Creación de la directiva utilizando SCW](#ebaa)  
[](#eaaa)[Resumen](#eaaa)

### Información general

Este capítulo proporciona recomendaciones y recursos que le ayudarán a consolidar los servidores del Servicio de autenticación de Internet (IAS) de su entorno en los que se ejecuta Microsoft Windows Servidor 2003 con SP1. IAS es la implementación de Microsoft de un servidor RADIUS (Servicio de usuario de acceso telefónico de autenticación remota) y proxy que permite la administración centralizada de las operaciones de autenticación y autorización, así como de las cuentas de los usuarios. IAS se puede utilizar para autenticar a los usuarios en bases de datos de Windows Server 2003, Windows NT® 4.0 o controladores de dominio de Windows 2000. IAS también admite una variedad de servidores de acceso a red (NAS), incluidos los servidores de enrutamiento y acceso remoto (RRAS).

El mecanismo de ocultación de RADIUS emplea el secreto compartido de RADIUS, el autenticador de solicitudes y el algoritmo de hash MD5 para cifrar User-Password y otros atributos como Tunnel-Password y MS-CHAP-MPPE-Keys. RFC 2865 determina la necesidad potencial de evaluar el entorno y determinar si es preciso establecer mecanismos de seguridad adicionales.

La configuración que se muestra en este capítulo se realiza y aplica mediante Directiva de grupo. Un objeto de directiva de grupo (GPO) que complementa la Directiva de línea de base de servidores miembro (MSBP) puede vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores IAS con el fin de proporcionar los cambios de configuración de seguridad necesarios para esta función de servidor. Este capítulo sólo trata aquellas configuraciones de la directiva que varían del MSBP.

Siempre que sea posible, esta configuración se reunirá en una plantilla incremental de Directiva de grupo que se aplicará a la unidad organizativa de servidores IAS. Parte de los ajustes que se muestran en este capítulo no se pueden aplicar mediante Directiva de grupo. Se proporciona información detallada acerca de cómo configurar estos ajustes manualmente.

El nombre de la plantilla de seguridad de servidores de infraestructura para el entorno de cliente de empresa es EC-Infrastructure Server.inf. Esta plantilla proporciona la configuración para la plantilla incremental de servidor de IAS que, a su vez, se utiliza para crear un nuevo GPO que se vincula a la unidad organizativa de servidores de IAS. Se proporcionan instrucciones detalladas en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003", para ayudarle a crear las UO y Directivas de grupo, e importar la plantilla de seguridad apropiada en cada GPO.

Para obtener más información acerca de la configuración en MSBP, consulte el capítulo 4, “Directiva de línea de base de servidores miembro”. Si desea más información acerca de todas las configuraciones predeterminadas, consulte la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.

**Nota**: las configuraciones recomendadas para la función de servidor IAS se han probado exclusivamente en el entorno de cliente de empresa. Por ese motivo, no se incluye la información acerca de los ataques DoS especificada para la mayoría de las funciones restantes de servidor definidas en la guía.

[](#mainsection)[Principio de la página](#mainsection)

### Directiva de auditoría

La configuración de la directiva de auditoría para servidores IAS en el entorno EC se configura a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro". La configuración de MSBP garantiza que en todos los servidores IAS de una organización se registre la información de auditoría de seguridad pertinente.

[](#mainsection)[Principio de la página](#mainsection)

### Asignaciones de derechos de usuario

Las asignaciones de derechos de usuario para servidores IAS en el entorno de cliente de empresa se configura también a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, “Configuración de la directiva de línea de base de servidores miembro". La configuración de MSBP permite garantizar que se configura de forma uniforme el acceso adecuado a los servidores IAS en la organización.

[](#mainsection)[Principio de la página](#mainsection)

### Opciones de seguridad

La configuración de opciones de seguridad para servidores IAS en el entorno de cliente de empresa también se establece a través de MSBP. Para obtener más información acerca de MSBP, consulte el capítulo 4, “Configuración de la directiva de línea de base de servidores miembro". La configuración de MSBP permite garantizar que en una organización se configura de forma uniforme el acceso adecuado a los servidores IAS.

[](#mainsection)[Principio de la página](#mainsection)

### Registro de eventos

La configuración del registro de eventos para servidores IAS en el entorno de cliente de empresa también se establece a través de MSBP. Para obtener más información acerca del MSBP, consulte el capítulo 4, "Directiva de línea de base de servidores miembro".

[](#mainsection)[Principio de la página](#mainsection)

### Configuración de seguridad adicional

Aunque la configuración de seguridad que se aplica a través de MSBP aumenta considerablemente el nivel de protección de los servidores IAS, en esta sección se plantean algunas consideraciones adicionales. No obstante, los parámetros de configuración de esta sección no se pueden aplicar a través de Directiva de grupo y por lo tanto deben establecerse manualmente en todos los servidores IAS.

#### Seguridad de las cuentas conocidas

Windows Server 2003 con SP1 dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son *Invitado* y *Administrador*.

De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. Por tanto, la protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.

El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada. Sin embargo, sus grupos operativos pueden controlar fácilmente los intentos de ataques contra esta cuenta de Administrador si cambia el nombre por uno único.

**Para proteger las cuentas conocidas en los servidores IAS**

-   Cambie el nombre de las cuentas de Administrador e Invitado y modifique sus contraseñas utilizando un valor largo y complejo en cada dominio y servidor.

-   Utilice nombres y contraseñas distintas en cada servidor. Si se utilizan los mismos nombres de cuenta y las mismas contraseñas en todos los dominios y servidores, un atacante que obtuviera acceso a un servidor miembro podría tener acceso a los demás.

-   Cambie las descripciones predeterminadas de las cuentas para evitar su fácil identificación.

-   Registre cualquier cambio que haga en una ubicación segura.

    **Nota**: se puede cambiar el nombre de la cuenta integrada Administrador desde Directiva de grupo. Esta configuración de directiva no se implementó en ninguna de las plantillas de seguridad que se proporcionan con esta guía porque en cada entorno se debe elegir un nombre único para esta cuenta. Sin embargo, el parámetro **Cuentas: cambiar el nombre de la cuenta del administrador** se puede configurar para cambiar el nombre de las cuentas de administrador en el entorno de cliente de empresa. Esta configuración de directiva forma parte de la sección de configuración de opciones de seguridad de un GPO.

#### Seguridad de las cuentas de servicios

A menos que sea absolutamente necesario, nunca configure un servicio para que se ejecute en el contexto de seguridad de una cuenta de dominio. Si el servidor se encuentra físicamente afectado, las contraseñas de la cuenta de dominio podrían obtenerse fácilmente mediante el volcado de secretos de la Autoridad de seguridad local (LSA). Para obtener más información acerca de cómo asegurar las cuentas de servicio, consulte la [Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx) en www.microsoft.com/technet/security/topics/serversecurity/serviceaccount/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Creación de la directiva utilizando SCW

Para implementar la configuración necesaria de seguridad, deberá utilizar el Asistente para la configuración de seguridad (SCW) y las plantillas de seguridad que se incluyen con la versión descargable de esta guía para crear una directiva de servidor.

Al crear su propia directiva, asegúrese de omitir las secciones "Configuración del Registro" y “Directiva de auditoría”. Las plantillas de seguridad proporcionan esta configuración para el entorno escogido. Este enfoque es necesario para asegurar que los elementos de la directiva proporcionados por las plantillas tienen prioridad sobre los configurados por SCW.

Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, la instalación debe realizarse en hardware similar al que se utiliza en su implementación para garantizar la máxima compatibilidad posible. La instalación nueva se llama *equipo de referencia*.

Durante los pasos de creación de la directiva de servidor probablemente elimine la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.

**Para crear la directiva de servidores IAS**

1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.

2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.

3.  Una el equipo al dominio, que aplicará toda la configuración de seguridad de las UO principales.

4.  Instale y configure sólo las aplicaciones obligatorias que estarán en cada servidor que comparte esta función. Los ejemplos incluyen servicios específicos de la función, software y agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.

5.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.

6.  Asegúrese de que las funciones de servidor detectadas sean apropiadas para su entorno; por ejemplo, la función de servidor **IAS (RADIUS)**.

7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.

8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.

9.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.

10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.

11. Compruebe que la casilla de verificación **Omitir esta sección** está activada en la sección "Seguridad de red" y, a continuación, haga clic en **Siguiente**. Los puertos y las aplicaciones apropiados identificados anteriormente se configuran como excepciones para el Firewall de Windows.

12. En la sección "Configuración del Registro", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.

13. En la sección "Directiva de auditoría", haga clic en la casilla de verificación **Omitir esta sección** y, a continuación, haga clic en **Siguiente**. Esta configuración de la directiva se importa desde el archivo INF suministrado.

14. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-IAS Server.inf).

15. Guarde la directiva con un nombre apropiado (por ejemplo, IAS Server.xml).

#### Prueba de la directiva utilizando SCW

Después que crear y guardar la directiva, Microsoft recomienda que la implemente a su entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.

Hay dos opciones disponibles para probar la directiva. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.

Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para instaurar una directiva a un solo servidor cada vez, o usar Scwcmd para instaurar la directiva en un grupo de servidores. El método original de implementación le permite deshacer fácilmente las directivas implementadas desde el SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios a las directivas durante el proceso de la prueba.

La directiva se prueba para asegurar que la aplicación de esta directiva a los servidores de destino no afectará sus funciones críticas. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.

Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.

Para obtener más información acerca de cómo probar las directivas del SCW, consulte la [Guía de implementación para el Asistente para la configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx y la [documentación del Asistente para la configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.

#### Conversión e implementación de la directiva

Después de probar completamente la directiva, complete los pasos siguientes para convertirla en un GPO e implementarla:

1.  En el símbolo de sistema, escriba el siguiente comando:

    ```
        scwcmd transform /p:<PathToPolicy.xml> /g:<GPODisplayName>
    ```
    
    y, a continuación, pulse Entrar. Por ejemplo:

    
    ```
        scwcmd transform /p:"C:\Windows\Security\msscw\Policies\IAS 
        Server.xml" /g:"IAS Policy"
    ```

    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.

2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.

Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en Firewall de Windows.

Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que la funcionalidad no se ve afectada.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

En este capítulo se han explicado los parámetros de configuración que se pueden utilizar para consolidar los servidores IAS en los que se ejecuta Windows Server 2003 con SP1 en el entorno de cliente de empresa que se define en esta guía. Estos parámetros también deben funcionar correctamente con los otros dos entornos definidos en esta guía, aunque no se han probado ni validado. Los parámetros se han configurado y aplicado a través de un objeto de directiva de grupo (GPO) que se diseñó como complemento de MSBP. Los objetos GPO pueden vincularse a las unidades organizativas (UO) apropiadas que contengan los servidores IAS de la organización para proporcionar un nivel de seguridad adicional.

#### Información adicional

Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores IAS en los que se ejecuta Windows Server 2003 con SP1.

-   Para obtener más información acerca de IAS, consulte la página [Understanding IAS](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/ab4eeeb2-b0aa-4b4a-a959-3902b2b3f1af.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
    ServerHelp/ab4eeeb2-b0aa-4b4a-a959-3902b2b3f1af.mspx.

-   Para obtener más información acerca de IAS y cuestiones de seguridad, consulte la página [Servicio de autenticación de Internet](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/d98eb914-258c-4f0b-ad04-dc4db9e4ee63.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
    ServerHelp/d98eb914-258c-4f0b-ad04-dc4db9e4ee63.mspx.

-   Para obtener información acerca de IAS y *Windows Server 2003*, consulte la página [IAS and firewalls](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/518e70a9-9e7a-422b-a13f-f3193d4fd215.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
    ServerHelp/518e70a9-9e7a-422b-a13f-f3193d4fd215.mspx.

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
