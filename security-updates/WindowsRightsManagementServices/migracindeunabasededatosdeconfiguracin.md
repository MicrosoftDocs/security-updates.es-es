---
TOCTitle: Migración de una base de datos de configuración
Title: Migración de una base de datos de configuración
ms:assetid: '980e3e94-7d28-40dd-ad01-d34eb3c8d8e6'
ms:contentKeyID: 18127883
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747607(v=WS.10)'
---

Migración de una base de datos de configuración
===============================================

Hay ocasiones en las que un servidor de base de datos se debe retirar. Una actualización de hardware del servidor de base de datos de RMS constituye un ejemplo. Antes de retirar el servidor de base de datos, la base de datos de configuración se debe mover a otro servidor de base de datos. Para proteger los datos de la base de datos de configuración, incluidos los pares de claves que contiene, debe planear e implementar detenidamente una migración.

Se recomienda crear un alias CNAME para el servidor de base de datos de RMS y, a continuación, configurar RMS para usar este alias. De este modo se elimina la necesidad de cambiar manualmente el nombre de servidor de base de datos en la base de datos de configuración de RMS si cambia el nombre del servidor. Al usar un alias CNAME, sólo se tendrá que actualizar el registro de alias.

Antes de comenzar la migración de la base de datos de configuración, asegúrese de que dispone de la siguiente información:

-   El nombre de cuenta y la contraseña que se usó originalmente para aprovisionar los servidores del clúster de RMS que usan esta base de datos.
-   Si se usa un proveedor de servicios de cifrado (CPS) basado en software para almacenar la clave privada de RMS, la contraseña de clave privada de RMS que se especificó originalmente durante el aprovisionamiento. Si se usó un módulo de seguridad de hardware (HSM) para almacenar la contraseña de clave privada, este paso no es necesario.

> [!NOTE]
> La migración de la base de datos de configuración no requiere un nuevo certificado del emisor de licencias de servidor ni una nueva clave privada de servidor porque RMS conserva la configuración de la base de datos de configuración original. 

Debe realizar una copia de seguridad de las bases de datos de RMS antes de efectuar ninguna operación en el servidor de base de datos. Si no es posible, debe, como mínimo, exportar el certificado del emisor de licencias de servidor. Para obtener más información acerca de la exportación del certificado del emisor de licencias de servidor, vea [Para exportar el certificado emisor de licencias de servidor a un archivo](https://technet.microsoft.com/d683a629-71b3-4b11-932b-4ab0317334af). Si se produce un error cuando se migran las bases de datos, puede importar el certificado del emisor de licencias de servidor en una nueva instalación de RMS y usar el contenido que estaba protegido por derechos con la instalación anterior.

Para migrar una base de datos de configuración, use los siguientes pasos:

-   Actualice la base de datos de configuración de RMS para reflejar el nombre del nuevo servidor de base de datos.
-   Actualice los archivos web.config y el Registro en cada servidor del clúster de RMS para usar el nuevo nombre de servidor de base de datos.

> [!IMPORTANT]
> En este tema se supone que las bases de datos de RMS ya están copias en el nuevo servidor de base de datos que aloja las bases de datos de RMS. 

Actualice la base de datos de configuración de RMS para usar el nuevo nombre de servidor de base de datos.
----------------------------------------------------------------------------------------------------------

El nombre del servidor de base de datos que hospeda las bases de datos de RMS está almacenado en la base de datos de configuración de RMS. Después de haber migrado los archivos de base de datos al nuevo servidor de base de datos, debe actualizar la base de datos de configuración de RMS. Esto se puede realizar con la herramienta del editor de configuración de RMS del kit de herramientas de administración de RMS o con SQL Management Studio.

Para actualizar el nombre del servidor de base de datos de RMS con el editor de configuración de RMS, use los siguientes pasos:

**Para actualizar la base de datos de configuración de RMS con el editor de configuración de RMS**
1.  Inicie sesión en un servidor de RMS del clúster como miembro de la función de base de datos Administradores del sistema.

2.  Instale el kit de herramientas de administración de RMS del Centro de descarga de Microsoft ([http://go.microsoft.com/fwlink/?LinkId=98961](http://go.microsoft.com/fwlink/?linkid=98961)).

3.  Navegue a %SystemDrive%:\\Archivos de programa\\RMS SP2 Administration Toolkit\\RMSConfigEditor y, a continuación, haga doble clic en **RMSCONFIGEDITOR.EXE**.

4.  En el cuadro **Server**, escriba el nombre del nuevo servidor que hospeda la base de datos de configuración de RMS y, a continuación, haga clic en **Go**.

5.  En el cuadro **Database**, haga clic en **DRMS\_Config\_***&lt;nombre de clúster de RMS&gt;***\_***&lt;Puerto&gt;*, donde *&lt;nombre de clúster de RMS&gt;* es el nombre del clúster de RMS y *&lt;Puerto&gt;* es el puerto TCP en el que se comunica RMS; a continuación, haga clic en **Go**.

6.  Haga clic en **DRMS\_ClusterPolicies**.

7.  En el panel de resultados, cambie el valor de la columna **PolicyData** de la fila **LoggingDatabaseServer** por el nuevo nombre de servidor de base de datos de RMS.

8.  Haga clic en **Persist**.

9.  Cambie el valor de la columna **PolicyData** de la fila **CertificationUserKeyStorageConnectionString** para reflejar el nuevo servidor de base de datos. El valor debe ser **data source=***&lt;nuevo nombre de servidor de base de datos&gt;***;integrated** donde *&lt;nuevo nombre de servidor de base de datos&gt;* es el nombre del nuevo servidor de base de datos.

10. Haga clic en **Persist**.

11. Repita los pasos 9–10 para el valor de la columna **PolicyData** de la fila **DirectoryServicesCacheDatabase**.

12. En el panel izquierdo, haga clic en **DRMS\_PluginProperties**.

13. Para **PropertyID** 101, denominado **PERSISTENT\_STORAGE**, cambie la columna **PropertyValue** para reflejar el nuevo servidor de base de datos. El valor debe ser **data source=***&lt;nuevo nombre de servidor de base de datos&gt;***;integrated** donde *&lt;nuevo nombre de servidor de base de datos&gt;* es el nombre del nuevo servidor de base de datos.

14. Haga clic en **Persist**.

15. Cierre el editor de configuración de RMS.

Para actualizar la base de datos de configuración de RMS con SQL Server Management Studio, realice los siguientes pasos:

**Para actualizar la base de datos de configuración de RMS con SQL Server Management Studio**
1.  Inicie sesión en el servidor de base de datos de configuración de RMS como administrador local u otra cuenta de usuario que sea miembro del grupo de administradores local.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Microsoft SQL Server 2005** y, a continuación, haga clic en **SQL Server Management Studio**.

3.  En la página **Conectar al servidor**, asegúrese de que el nuevo nombre de servidor de base de datos se muestra en el cuadro **Nombre de servidor** y, a continuación, haga clic en **Conectar**.

4.  Expanda **Bases de datos**, expanda **DRMS\_Config\_***&lt;nombre de clúster de RMS&gt;***\_***&lt;Puerto&gt;* y, a continuación, expanda **Tablas**.

5.  Haga clic con el botón secundario del mouse en **DRMS\_ClusterPolicies** y, a continuación, haga clic en **Abrir tabla**.

6.  En el panel de resultados, cambie el valor de la columna **PolicyData** de la fila **LoggingDatabaseServer** por el nuevo nombre de servidor de base de datos de RMS.

7.  Cambie el valor de la columna **PolicyData** de la fila **CertificationUserKeyStorageConnectionString** para reflejar el nuevo servidor de base de datos. El valor debe ser **data source=***&lt;nuevo nombre de servidor de base de datos&gt;***;integrated** donde *&lt;nuevo nombre de servidor de base de datos&gt;* es el nombre del nuevo servidor de base de datos.

8.  Repita los pasos 6–7 para el valor de la columna **PolicyData** de la fila **DirectoryServicesCacheDatabase**.

9.  En el panel Explorador de objetos, haga clic con el botón secundario en **DRMS\_PluginProperties** y, a continuación, haga clic en **Abrir tabla**.

10. Para **PropertyID** 101, denominado **PERSISTENT\_STORAGE**, cambie la columna **PropertyValue** para reflejar el nuevo servidor de base de datos. El valor debe ser **data source=***&lt;nuevo nombre de servidor de base de datos&gt;***;integrated** donde *&lt;nuevo nombre de servidor de base de datos&gt;* es el nombre del nuevo servidor de base de datos.

11. Cierre Microsoft SQL Server Management Studio.

Configure cada servidor del clúster de RMS para usar el nuevo nombre de servidor de base de datos.
--------------------------------------------------------------------------------------------------

Para configurar cada servidor del clúster de RMS para usar el nuevo nombre de servidor de base de datos, debe actualizar los archivos web.config y actualizar tres entradas del Registro. Una vez completada esta operación, debe reiniciar Internet Information Services (IIS) para que los cambios surtan efecto.

Para actualizar los archivos web.config en cada servidor del clúster de RMS:

**Para actualizar los archivos web.config en cada servidor del clúster de RMS**
1.  Inicie sesión en un servidor del clúster de RMS como miembro del grupo de administradores local.

2.  Navegue a %Systemdrive%\\inetpub\\wwwroot\\\_wmcs\\admin.

3.  Haga doble clic en **web.config**, seleccione la opción **Seleccionar el programa de una lista** y, a continuación, haga clic en **Aceptar**.

4.  Haga clic en **Bloc de notas**, desactive **Usar siempre el programa seleccionado para abrir este tipo de archivos** y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **Editar** y, a continuación, en **Reemplazar**.

6.  En el cuadro **Buscar** escriba el nombre del servidor de base de datos que se debe retirar que hospeda las bases de datos de RMS.

7.  En el cuadro **Reemplazar por** escriba el nombre del nuevo servidor de base de datos que hospeda las bases de datos de RMS.

8.  Haga clic en **Reemplazar todo** y, a continuación, en **Cancelar**.

9.  Haga clic en **Archivo** y, a continuación, en **Guardar**.

10. Cierre el Bloc de notas.

11. Repita los pasos 2–9 para los archivos web.config que se encuentran en los directorios %Systemdrive%\\inetpub\\wwwroot\\\_wmcs\\certification y %Systemdrive%\\inetpub\\wwwroot\\\_wmcs\\licensing.

12. Repita los pasos 1 a 11 por cada servidor del clúster de RMS.

Finalmente, actualice el Registro en cada servidor del clúster de RMS con el nuevo nombre del servidor de base de datos.

> [!CAUTION]
> La edición incorrecta del Registro puede causar graves daños al sistema. Antes de realizar cambios en el Registro, debe hacer una copia de seguridad de los datos de valor guardados en el equipo. 

**Para actualizar el Registro en cada servidor del clúster de RMS**
1.  Inicie sesión en un servidor del clúster de RMS como miembro del grupo de administradores local.

2.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.

3.  Escriba **regedit.exe** y, a continuación, haga clic en **Aceptar**.

4.  Navegue a **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DRMS\\1.0\\KeyProtection**.

5.  Cambie la entrada del Registro denominada PASSWORDDERIVEDKEY\_*&lt;nombre de servidor de base de datos anterior&gt;*\_DRMS\_CONFIG\_*&lt;nombre de clúster de RMS&gt;*\_*&lt;puerto&gt;* por:

    PASSWORDDERIVEDKEY\_*&lt;nombre de servidor de base de datos anterior&gt;*\_DRMS\_CONFIG\_*&lt;nombre de clúster de RMS&gt;*\_*&lt;puerto&gt;*

    donde:

    -   *&lt;nombre de servidor de base de datos anterior&gt;* es el nombre del servidor de base de datos anterior.
    -   *&lt;nombre de clúster de RMS&gt;* es el nombre del clúster de RMS.
    -   *&lt;puerto&gt;* es el puerto TCP en el que se comunica RMS.
    -   *&lt;nuevo nombre de servidor de base de datos&gt;* es el nombre del servidor de base de datos nuevo.

6.  Navegue a **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet001\\Services\\DRMS\_Logging\_&lt;nombre de clúster de RMS&gt;\_&lt;puerto&gt;\\Params**.

7.  Cambie la entrada del Registro **ConnectionString** de modo que el valor de origen de datos coincida con el nuevo nombre de servidor de base de datos.

8.  Repita los pasos 6 a 7 para **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\DRMS\_Logging\_&lt;nombre de clúster de RMS&gt;\_&lt;puerto&gt;\\Params**.

9.  En una ventana del símbolo del sistema, escriba **IISRESET** y presione ENTRAR.

10. Repita los pasos 1 a 9 por cada servidor del clúster de RMS.
