---
TOCTitle: 'Paso 3: configurar las conexiones de red'
Title: 'Paso 3: configurar las conexiones de red'
ms:assetid: '42a144c5-f08e-4a6e-b360-47ddea77bd24'
ms:contentKeyID: 21741295
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939815(v=WS.10)'
---

Paso 3: configurar las conexiones de red
========================================

Después de que haya instalado Windows Server Update Services 3.0 Service Pack 2 (WSUS 3.0 SP2), el asistente para configuración se iniciará de forma automática. También puede ejecutarlo en otro momento a través de la página **Opciones** de la consola de administración de WSUS.

Antes de iniciar el proceso de configuración, asegúrese de que conoce las respuestas a las preguntas siguientes:

1. ¿Está configurado el firewall del servidor para permitir a los clientes tener acceso al servidor?

2. ¿Puede este equipo ponerse en contacto con el servidor que precede en la cadena (como Microsoft Update)?

3. ¿Tiene el nombre del servidor proxy y las credenciales de usuario del servidor proxy, si fueran necesarias?

De manera predeterminada, WSUS 3.0 SP2 está configurado para utilizar Microsoft Update como la ubicación desde la que obtener las actualizaciones. Si tiene un servidor proxy en la red, puede configurar WSUS 3.0 SP2 para que lo use. Si hay un firewall corporativo entre WSUS e Internet, necesitará configurar el firewall para asegurarse de que WSUS puede obtener las actualizaciones.

 
<p> </p>

> [!NOTE]
> Aunque debe tener conexión a Internet para descargar las actualizaciones de Microsoft Update, WSUS ofrece la posibilidad de importar actualizaciones en redes que no estén conectadas a Internet.
 

El paso 3 contiene los procedimientos siguientes:

-   Configurar su firewall.
-   Especifique la manera en que este servidor obtendrá las actualizaciones (ya sea desde Microsoft Update o desde otro servidor WSUS).
-   Configurar el servidor proxy, de manera que WSUS pueda obtener las actualizaciones.

**Para configurar el firewall**
-   Si hay un firewall corporativo entre WSUS e Internet, necesitará configurar el firewall para asegurarse de que WSUS puede obtener las actualizaciones. Para obtener las actualizaciones de Microsoft Update, el servidor WSUS utiliza el puerto 80 para el protocolo HTTP y el puerto 443 para el protocolo HTTPS. Esta característica no se puede configurar.

-   Si la organización no permite que los puertos 80 ó estén abiertos para todas las direcciones, puede restringir el acceso sólo a los dominios siguientes, de manera que WSUS y Actualizaciones automáticas se puedan comunicar con Microsoft Update:

    -   http://windowsupdate.microsoft.com
    -   http://\*.windowsupdate.microsoft.com
    -   https://\*.windowsupdate.microsoft.com
    -   http://\*.update.microsoft.com
    -   https://\*.update.microsoft.com
    -   http://\*.windowsupdate.com
    -   http://download.windowsupdate.com
    -   http://download.microsoft.com
    -   http://\*.download.windowsupdate.com
    -   http://wustat.windows.com
    -   http://ntservicepack.microsoft.com

 
<p> </p>

> [!NOTE]
> Estas instrucciones para configurar el firewall están dirigidas a un firewall corporativo ubicado entre WSUS e Internet. Dado que WSUS inicia todo su tráfico de red, no hay necesidad de configurar el firewall de Windows en el servidor WSUS.
 

Aunque la conexión entre Microsoft Update y WSUS requiere que los puertos 80 y 443 estén abiertos, puede configurar varios servidores WSUS para sincronizar con un puerto personalizado.

En los dos procedimientos siguientes se supone que utiliza el Asistente para la configuración. En una sección posterior de este paso, aprenderá a iniciar el complemento de administración de WSUS y a configurar el servidor a través de la página Opciones.

**Para especificar la manera en que este servidor obtendrá las actualizaciones**
1.  Desde el Asistente para configuración, después de unirse al Programa de mejora de Microsoft, haga clic en **Siguiente** para elegir el servidor que precede en la cadena.

2.  Si elige sincronizar desde Microsoft Update, habrá terminado con la página Opciones. Haga clic en **Siguiente** o seleccione **Especificar servidor proxy** en el panel de navegación.

3.  Si elige sincronizar desde otro servidor WSUS, especifique el nombre del servidor y el puerto en que este servidor se comunicará con el servidor que precede en la cadena.

4.  Para usar SSL, active la casilla **Usar SSL al sincronizar la información de actualización**. En ese caso los servidores usarán el puerto 443 para la sincronización. (Debe asegurarse de que tanto este servidor como el que precede en la cadena admiten SSL).

5.  Si se trata de un servidor de réplica, active la casilla **Esto es una réplica del servidor que precede en la cadena**.

6.  En este punto, ha terminado con la configuración del servidor que precede en la cadena. Haga clic en **Siguiente** o seleccione **Especificar servidor proxy** en el panel de navegación de la izquierda.

**Para configurar el servidor proxy**
1.  En la página **Especificar servidor proxy** del Asistente para la configuración, active la casilla de verificación **Usar un servidor proxy al sincronizarse** y después escriba el nombre del servidor proxy y el número de puerto (puerto 80 de manera predeterminada) en los cuadros correspondientes.

2.  Si desea conectar el servidor proxy utilizando credenciales de usuario específicas, active la casilla de verificación **Usar credenciales de usuario para conectarse al servidor proxy** y, a continuación, escriba el nombre, dominio y contraseña de usuario en los cuadros correspondientes. Si desea habilitar la autenticación básica para el usuario que se conecta al servidor proxy, active la casilla de verificación **Permitir la autenticación básica (la contraseña se envía en texto no cifrado)**.

3.  En este punto, ha terminado con la configuración del servidor proxy. Haga clic en **Siguiente** para ir a la página siguiente, donde podrá iniciar la configuración del proceso de sincronización.

En los dos procedimientos siguientes se supone que utiliza el complemento de administración de WSUS para la configuración. Estos dos procedimientos muestran cómo iniciar el complemento de administración de WSUS y configurar el servidor desde la página **Opciones**.

**Para iniciar la consola de administración de WSUS**
-   Para iniciar la consola de administración de WSUS, haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y, a continuación, haga clic en **Microsoft Windows Server Update Services 3.0**.

 
<p> </p>

> [!NOTE]
> Para usar todas las características de la consola, debe ser miembro de los grupos de seguridad de administradores de WSUS o de administradores locales del servidor en el que está instalado WSUS. Los miembros del grupo de seguridad de informadores de WSUS tienen acceso de sólo lectura en la consola de administración.
 

**Para especificar un origen de actualización y un servidor proxy**
1.  En la consola de WSUS, haga clic en **Opciones** en el panel izquierdo situado bajo el nombre de este servidor y, a continuación, en **Actualizar origen y servidor proxy** en el panel central.

    Aparecerá un cuadro de diálogo con las fichas **Origen de la actualización** y **Servidor proxy**.

2.  En la ficha **Origen de la actualización**, seleccione la ubicación desde la que este servidor obtendrá las actualizaciones. Si elige sincronizar de Microsoft Update (la opción predeterminada), habrá terminado con esta página del asistente.

3.  Si elige sincronizar de otro servidor WSUS, deberá especificar el puerto en el que los servidores se comunicarán (el predeterminado es el puerto 80). Si elige uno puerto diferente, deberá asegurarse de que ambos servidores pueden usarlo.

4.  También debe especificar si desea usar SSL al sincronizar desde el servidor WSUS que precede en la cadena. En ese caso, los servidores usarán el puerto 443 para sincronizar desde el servidor que precede en la cadena.

5.  Si este servidor es una réplica del segundo servidor WSUS, active la casilla de verificación **Esto es una réplica del servidor que precede en la cadena**. En este caso todas las actualizaciones sólo se deben aprobar en el servidor WSUS que precede en la cadena.

6.  En la ficha **Servidor proxy**, active la casilla de verificación **Usar un servidor proxy al sincronizarse** y después escriba el nombre del servidor proxy y el número de puerto (puerto 80 de manera predeterminada) en los cuadros correspondientes.

7.  Si desea conectar el servidor proxy utilizando credenciales de usuario específicas, active la casilla de verificación **Usar credenciales de usuario para conectarse al servidor proxy** y, a continuación, escriba el nombre, dominio y contraseña de usuario en los cuadros correspondientes. Si desea habilitar la autenticación básica para el usuario que se conecta al servidor proxy, active la casilla de verificación **Permitir la autenticación básica (la contraseña se envía en texto no cifrado)**.

8.  Haga clic en **Aceptar** para guardar los cambios.

Paso siguiente
--------------

[Paso 4: configurar las actualizaciones y la sincronización](https://technet.microsoft.com/deeaa7e1-9b50-45cb-9537-d75f70de3405)

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
