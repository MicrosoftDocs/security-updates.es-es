---
TOCTitle: Problemas de administración de RMS
Title: Problemas de administración de RMS
ms:assetid: '97013c08-d3fa-4ea0-8914-995b6c97f900'
ms:contentKeyID: 18127882
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747605(v=WS.10)'
---

Problemas de administración de RMS
==================================

Una vez que RMS esté correctamente establecido en el servidor, pueden surgir errores en la administración diaria de RMS. La información que contienen las secciones siguientes le ayudará a resolver algunos de estos problemas.

Mensaje "SQL Server no existe o acceso denegado" recibido al intentar abrir el sitio Web de administración de RMS
-----------------------------------------------------------------------------------------------------------------

Si ha instalado RMS utilizando una nueva instalación de SQL Server 2005 como servidor de base de datos, es posible que no se haya iniciado el servicio de SQL Server. En SQL Server 2005 el servicio MSSQLSERVER no está configurado para iniciarse automáticamente al iniciar el servidor. Si ha reiniciado el SQL Server desde que instaló RMS y no ha configurado este servicio para reiniciarse automáticamente, RMS no podrá funcionar, y sólo estará accesible la página Administración global de RMS.

Cuando haya iniciado el servicio MSSQLSERVER, debe reiniciar IIS en el servidor de RMS para restaurar las funciones de RMS.

No se puede completar el proceso de inscripción sin conexión
------------------------------------------------------------

Si el archivo de la solicitud de inscripción está incompleto o se modifica antes de enviarse al sitio Web EnrollService, no puede completar la inscripción sin conexión. El archivo de la solicitud de inscripción puede haber sido dañado por un programa malicioso, error de usuario o error de sistema.

Según qué información falte, el sitio Web EnrollService puede aceptar el archivo y devolver un certificado emisor de licencias de servidor o bien denegar el archivo de la solicitud y presentar un error.

Si se devuelve un certificado emisor de licencias de servidor, éste reflejará las omisiones o errores presentes en el archivo de la solicitud de inscripción y RMS presentará un error cuando intente importar el certificado.

Si no puede completar el proceso de inscripción, asegúrese de que el equipo con conexión a Internet no tenga virus, vuelva a exportar el archivo de la solicitud de inscripción del servidor de RMS y, a continuación, utilice diferentes medios para transferirlo al equipo con conexión a Internet. Si vuelve a encontrar este error, debería ponerse en contacto con los servicios de soporte técnico de Microsoft.

No se crean archivos de registro
--------------------------------

El servicio de registro de RMS requiere el servicio de Message Queue Server (también conocido como MSMQ) y acceso a la base de datos de registro. Si no se están creando archivos de registro, es posible que los componentes no estén configurados correctamente o que se hayan interrumpido las comunicaciones entre los componentes.

Asegúrese de que el servidor de RMS y el servidor de bases de datos tienen conexión a la red. Si la tienen, utilice los procedimientos siguientes para revisar los requisitos previos del servicio de registro de RMS y asegúrese de que todas las dependencias de software estén configuradas correctamente.

Primero, compruebe que la configuración de Message Queue Server sea correcta. Los servicios de Message Queue Server deben estar instalados y la integración con Active Directory debe estar activada.

**Para comprobar si Message Queue Server se ha instalado y configurado correctamente**
1.  En **Panel de control**, haga clic en **Agregar o quitar programas** y, a continuación, haga clic en **Agregar o quitar componentes de Windows** para abrir el **Asistente para componentes de Windows**.

2.  En el **Asistente para componentes de Windows**, seleccione la casilla de verificación **Servidor de aplicaciones** y haga clic en **Detalles**.

3.  Seleccione la casilla de verificación **Servicios de Message Queue Server** y haga clic en **Detalles**.

4.  Si la casilla de verificación **Integración con Active Directory** está seleccionada, vaya al paso siguiente y compruebe si Message Queue Server se está ejecutando. Si la casilla de verificación no está seleccionada, prosiga con los pasos del 5 al 9.

5.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Windows RMS** y haga clic en **Administración de Windows RMS** para abrir la página Administración global.

6.  Junto al sitio Web donde están establecidos los servicios en línea de RMS, seleccione **Quitar RMS de este sitio Web** y haga clic en **Aceptar**.

7.  En **Agregar o quitar programas**, en el **Panel de control**, haga clic en **Agregar o quitar componentes de Windows**, **Servidor de aplicaciones** y, finalmente, en **Message Queue Server**.

8.  Para activar la **Integración con Active Directory**, haga clic en **Detalles**, seleccione la casilla de verificación **Integración con Active Directory** y haga clic en **Aceptar**.

9.  Abra la página **Administración global**. Junto al nombre del sitio Web en el que desee establecer los servicios en línea de RMS, haga clic en **Establecer los servicios en línea de RMS en este sitio Web**.

En segundo lugar, compruebe si Message Queue Server se está ejecutando en su servidor.

**Para comprobar si Message Queue Server se está ejecutando en el servidor**
1.  En el **Panel de control**, haga clic en **Herramientas administrativas** y haga clic en **Servicios**.

2.  Desplácese por la lista de servicios hasta que encuentre el servicio de **Message Queue Server**.

3.  En la columna **Estado**, el servicio debería aparecer como **Iniciado**; si no lo está, haga clic con el botón secundario del mouse en el servicio y, a continuación, haga clic en **Inicio**.

En tercer lugar, compruebe si el servicio de registro tiene permiso para registrar sucesos en la base de datos de registro. El servicio de registro de RMS se ejecuta utilizando la cuenta de servicio de RMS. Compruebe si se ha iniciado sesión correctamente en la cuenta de servicio de RMS y si ésta tiene todos los permisos requeridos para permitirle crear bases de datos y escribir información en los archivos.

Una vez que se cumplan todos los prerrequisitos, detenga y reinicie el servicio de registro de RMS mediante el complemento Services. Cuando se haya reiniciado el servicio de registro de RMS, deberían crearse los archivos de registro en el servidor de base de datos. Si utiliza SQL Server como servidor de base de datos, puede comprobar si se crean archivos de registro siguiendo este procedimiento.

**Para comprobar si se crean los archivos de registro en SQL Server**
1.  En el Administrador corporativo de SQL Server, vaya a la base de datos de registro, expanda **Bases de datos** y después expanda la base de datos que contiene la base de datos de registro de RMS.

2.  Haga clic en la base de datos de registro, después en **Tablas**, haga clic con el botón secundario en **DRMS\_log\_master**, y a continuación, en **Abrir tabla Devolver todas las filas**. Si se están creando archivos de registro, verá uno o más archivos.

Restauración de la base de datos de configuración
-------------------------------------------------

RMS no puede funcionar sin una base de datos de configuración operativa. Si tiene problemas con la base de datos de configuración, como errores de base de datos o del disco duro en el servidor de base de datos, puede restaurar las funciones de RMS si restaura una copia de seguridad de la base de datos de configuración. Para restaurar la base de datos de configuración de RMS de una copia de seguridad, necesita la información siguiente:

-   El nombre de la copia de seguridad más reciente de la base de datos.
-   El nombre del equipo en el que se restaurará la copia de seguridad de la base de datos.
-   El nombre de cuenta y la contraseña que se utilizó originalmente para establecer RMS.
-   La contraseña que se especificó originalmente para la protección de clave privada de software (si se utilizó).

Para restaurar la copia de seguridad de la base de datos, no es necesario un nuevo certificado emisor de licencias de servidor ni una nueva clave privada, puesto que RMS conserva todos los valores (que obtiene de la copia de seguridad de la base de datos de configuración).

Puede restaurar una copia de seguridad de base de datos siguiendo este procedimiento.

**Para restaurar una copia de seguridad de base de datos**
1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Windows RMS** y haga clic en **Administración de Windows RMS** para abrir la página **Administración global**.

2.  Junto al sitio Web donde están establecidos los servicios en línea de RMS, seleccione **Quitar RMS de este sitio Web** y haga clic en **Aceptar**.

3.  Restaure los archivos de la copia de seguridad de la base de datos de configuración. Si hizo una copia de seguridad de la base de datos de registro durante el proceso de copia de seguridad y desea mantener la continuidad de los datos, restaure también la base de datos de registro.

    -   Si está restaurando el sistema después de un error total del sistema, restaure el registro utilizando una copia de seguridad del estado del sistema antes de restaurar los archivos de copia de seguridad de la base de datos.

4.  Si la base de datos que se está restaurando es sólo para un servidor de certificación raíz, modifique la siguiente clave del registro antes de intentar volver a establecer el servicio:

    -   En equipos con la versión de 32 bits de Windows Server 2003:
        `HKEY_LOCAL_MACHINE\Software\Microsoft\DRMS\1.0\`
    -   En equipos con la versión de 64 bits de Windows Server 2003:
        `HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\DRMS\1.0\`

    Agregue la siguiente entrada como valor de cadena y deje el valor en blanco:

    `GicURL`

    Esto omitirá la detección de Active Directory del servidor de certificación raíz y le permitirá obtener acceso a las páginas de establecimiento del servidor de certificación raíz.

5.  Si utilizó un módulo de seguridad de hardware para asegurar la clave privada de RMS, restaure el entorno de seguridad de la copia de seguridad para poder recuperar las claves.

6.  Siga alguno de estos pasos:

    -   Para restaurar la base de datos para un único servidor, en lugar de un clúster, haga clic en Establecer los servicios en línea de RMS en este sitio Web para el sitio Web donde desee establecer los servicios en línea de RMS.
        O bien
    -   Para restaurar la base de datos para un clúster, haga clic en Agregar este servidor a un clúster para el sitio Web donde desee establecer los servicios en línea de RMS.

7.  Especifique la cuenta de servicio de RMS que se utilizó para establecer los servicios en línea en el servidor originalmente.

8.  Especifique la copia de seguridad de la base de datos de configuración (incluido el nombre de la base de datos y el nombre del equipo en el que está ubicada la base de datos) que desea utilizar.

9.  Especifique la misma contraseña que utilizó para establecer los servicios en línea en este servidor originalmente.

10. Haga clic en **Enviar**.

Empezará el proceso de establecimiento, y volverá a establecerse RMS en el servidor.

For more information, see System Recovery Planning and Backing Up and Restoring the RMS System in Planning an RMS Deployment in this documentation collection.

Ha caducado la contraseña de la cuenta de servicio de RMS
---------------------------------------------------------

Si RMS deja de funcionar, podría ser porque la contraseña de la cuenta de servicio de RMS ha caducado. Consulte el Administrador IIS. Si los grupos de aplicaciones de RMS se han detenido y no puede reiniciarlos, es posible que la contraseña de la cuenta de servicio de RMS haya caducado.

Si la contraseña de la cuenta de servicio de RMS caduca, debe cambiar la contraseña en todos los servidores de RMS que utilizan la cuenta con la contraseña caducada y, a continuación, reiniciar IIS. Para obtener más información, vea "Cambio de la contraseña de la cuenta de servicio de RMS" en "Operación de un servidor de RMS" en esta recopilación de documentación.

Restauración de una instalación previa de RMS
---------------------------------------------

Si falla el hardware o el software del servidor de RMS, puede restaurar un servidor de RMS utilizando la base de datos de configuración instalada previamente para establecer una nueva instancia de servidor.

> [!NOTE]
> Este procedimiento se aplica sólo si falla el servidor que está ejecutando RMS. Si falla el servidor que está ejecutando la base de datos de configuración, vea "Restauración de la base de datos de configuración", anteriormente en este tema. Si el servidor de RMS es también el servidor de base de datos, deberá restaurar todo el servidor desde una copia de seguridad. 

Utilice el procedimiento siguiente para seleccionar la misma base de datos de configuración que se utilizó para la instalación original.

**Para restaurar una instalación previa de RMS**
1.  Inicie sesión en el equipo que desea configurar como servidor de RMS utilizando una cuenta con privilegios de administrador. Asegúrese de que el equipo cumpla los requisitos mínimos de sistema para RMS. Para obtener más información acerca de requisitos de sistema para RMS, vea "Requisitos de hardware" para RMS en "Planeamiento de una implementación de RMS" en esta recopilación de documentación.

2.  Si utiliza un módulo de seguridad de hardware para proteger las claves privadas de RMS, asegúrese de que esté configurado correctamente utilizando la misma configuración y el mismo entorno de seguridad que se utilizó con la instalación anterior de RMS.

3.  Instale RMS en el equipo.

4.  Cuando haya completado la instalación de RMS, haga clic en **Inicio**, seleccione **Todos los programas** y **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS** para abrir la página de **Administración global**.

5.  Junto al sitio Web en el que desee establecer los servicios en línea de RMS, haga clic en **Agregar este servidor a un clúster**.

6.  En el área **Cuenta de servicio de RMS**, escriba el nombre de cuenta de servicio de RMS, con el formato nombre\_dominio\\nombre\_usuario y la contraseña de la cuenta de servicio de RMS con la que se ejecutará RMS para la mayoría de las operaciones normales. Debe ser una cuenta de dominio.

7.  En el área **Base de datos de configuración**, especifique el nombre del servidor de base de datos y el nombre de la base de datos de configuración de la instalación original de RMS que desea recuperar.

8.  En el área **Protección de clave privada**, seleccione el mecanismo utilizado por este clúster para proteger la clave privada. Si utilizó protección de clave privada de software, debe proporcionar la contraseña que se utilizó para cifrar la clave privada cuando se establecieron originalmente los servicios en línea en este clúster.

9.  Haga clic en **Enviar**.

Los clientes no pueden abrir contenido protegido con RMS, puesto que los permisos han caducado
----------------------------------------------------------------------------------------------

Si los permisos de un usuario han caducado, el usuario no puede utilizar contenido protegido con RMS. Si el reloj del sistema del servidor de RMS va más adelantado que el reloj del sistema del cliente de RMS, es posible que el usuario no pueda utilizar contenido protegido con RMS aunque no hayan caducado los permisos. Al no estar sincronizado el reloj de los dos equipos, puede aparecer el siguiente error cuando el equipo cliente intenta abrir el contenido:

**No tiene permiso para abrir este mensaje porque su permiso ha caducado. ¿Desea abrirlo utilizando otro conjunto de credenciales?**  

Tanto la licencia de cliente como la licencia de contenido son válidas, pero la diferencia de reloj hace que el cliente interprete la licencia de contenido como no válida y muestra este mensaje de error. Esto puede hacer que el usuario crea que tiene problemas con su certificado de cuenta de RMS o con los derechos concedidos al documento. Cuando el reloj del cliente haya alcanzado el intervalo de tiempo de validez de la licencia de publicación de contenido, el usuario podrá abrir el contenido.

Es aconsejable asegurarse de que los clientes y los servidores del sistema de RMS se sincronicen con el mismo servicio de hora.

Error de "Acceso denegado" cuando RMS intenta registrar sucesos en el registro de sucesos de aplicación
-------------------------------------------------------------------------------------------------------

De forma predeterminada, los componentes como RMS que se ejecutan desde una página ASP se crean en la cuenta IUSR\_COMPUTERNAME. Esta cuenta forma parte del grupo de invitados, y los privilegios de seguridad necesarios para escribir en el registro de sucesos de aplicación impiden a las cuentas de invitado introducir datos en el registro de sucesos.

Para solucionar este problema, puede utilizar el editor del registro para modificar las claves del registro que controlan este comportamiento.

> [!CAUTION]
> La edición incorrecta del Registro puede dañar gravemente el sistema. Antes de realizar cambios en el Registro, debe realizar una copia de seguridad de los datos de valor del equipo. 

Establezca la siguiente clave del registro en 0 en lugar de 1, y reinicie el equipo para que se apliquen los cambios.

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\EventLog\Application`

Nombre: `RestrictGuestAccess`

Tipo: `REG_DWORD`

> [!NOTE]
> Esto permite a todas las cuentas de invitado escribir en el registro de sucesos de aplicación. 

Para obtener más información acerca de la causa de este error, consulte el artículo sobre la habilitación del registro desde páginas ASP en [Microsoft Knowledge Base](http://go.microsoft.com/fwlink/?linkid=44167).
