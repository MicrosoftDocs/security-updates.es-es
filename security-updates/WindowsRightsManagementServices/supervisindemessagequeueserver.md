---
TOCTitle: Supervisión de Message Queue Server
Title: Supervisión de Message Queue Server
ms:assetid: 'a7109399-3a84-4681-874b-f6ea1646b0a0'
ms:contentKeyID: 18127902
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747716(v=WS.10)'
---

Supervisión de Message Queue Server
===================================

El registro de RMS utiliza Message Queue Server (que también se conoce como MSMQ) para enviar sucesos a la base de datos de registro. Cada servidor de solicitudes de cliente de RMS envía mensajes al servicio de Message Queue Server y el servicio de escucha de registro de cada servidor de solicitudes de cliente recupera mensajes de registro de Message Queue Server y los escribe en la base de datos de registro. Si la base de datos de registro o el servidor de base de datos no está disponible o si se detiene el servicio de escucha de registro, Message Queue Server almacena los mensajes en la cola. Si planea cerrar la base de datos de registro o el servidor de base de datos, es recomendable que cierre en primer lugar el servicio de escucha de registro de cada servidor de solicitudes de cliente y, después, reinicie el servicio de escucha de registro en cada servidor de solicitudes de cliente tras reiniciar la base de datos o el servidor de base de datos.

Si la base de datos falla y el servicio de escucha de registro aún se está ejecutando, éste no podrá escribir mensajes de registro en la base de datos. El servicio de escucha de registro moverá los mensajes a una cola de Message Queue Server para “mensajes con problemas de entrega” hasta que la base de datos esté disponible, en cuyo momento los mensajes de registro nuevos se escribirán en la base de datos. Los mensajes de la cola para mensajes con problemas de entrega no se escribirán automáticamente en la base de datos de registro. Para ver y eliminar los mensajes en la cola para mensajes con problemas de entrega, siga estos pasos:

1.  Abra el complemento Administración de equipos de Microsoft Management Console (MMC). Para hacerlo, haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y haga clic en **Administración de equipos**.
2.  En Servicios y Aplicaciones, en el árbol de la consola, haga clic en Message Queue Server y después en Colas privadas.
3.  Verá dos colas. El nombre de ambas comienza con "**drms\_logging**" seguido del nombre del clúster. Una de ellas se llama "**drms\_logging\_***&lt;nombre del clúster&gt;***\_deadletter**". Se trata de la cola para mensajes con problemas de entrega. Haga clic en el nombre de la cola y, a continuación, en la cola Mensajes de la cola.
4.  Haga doble clic en cada mensaje para ver sus propiedades.
5.  Para eliminar la cola, haga clic con el botón secundario en la cola **Mensajes de la cola**, seleccione **Todas las tareas** y después haga clic en **Purgar**.

En la configuración predeterminada, Message Queue Server almacena todos los mensajes de la cola hasta el límite de espacio de almacenamiento libre en el servidor. Si Message Queue Server utiliza todo el espacio disponible en el disco duro, el servidor de RMS no puede procesar las solicitudes de cliente. Para impedir que esto ocurra, siga estos pasos para limitar la cantidad de espacio en disco que Message Queue Server puede utilizar para las colas:

1.  Abra el complemento Administración de equipos de Microsoft Management Console (MMC). Para hacerlo, haga clic en Inicio, seleccione Todos los programas, Herramientas administrativas y haga clic en Administración de equipos.
2.  En Servicios y Aplicaciones, en el árbol de la consola, haga clic en Servicios de Message Queue Server y después en Colas privadas.
3.  Verá dos colas. El nombre de ambas comienza con "drms\_logging". Realice los siguientes pasos en cada cola:
    -   Haga clic en Propiedades.
    -   Seleccione la casilla de verificación Limitar el almacenamiento de mensajes a (KB) y después escriba el tamaño total, en kilobytes, de todos los mensajes que pueden almacenarse en la cola.

Si la cola se llena, se descartarán los mensajes de RMS a medida que lleguen y se enviará al registro de sucesos del sistema el siguiente mensaje asociado con el id. de suceso 48:

"No se pudo enviar la bolsa de propiedades a Message Queue Server."

Es recomendable que configure las herramientas de supervisión del sistema para que le avisen cuando se produzca este suceso, ya que indica que existe un problema con la base de datos de registro.
