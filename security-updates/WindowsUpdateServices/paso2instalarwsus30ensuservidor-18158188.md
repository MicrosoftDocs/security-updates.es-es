---
TOCTitle: 'Paso 2: instalar WSUS 3.0 en su servidor'
Title: 'Paso 2: instalar WSUS 3.0 en su servidor'
ms:assetid: '191e62a0-7671-41eb-9841-17c64313fa68'
ms:contentKeyID: 18158188
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720469(v=WS.10)'
---

Paso 2: instalar WSUS 3.0 en su servidor
========================================

Tras asegurarse de que el servidor cumple con los requisitos de instalación, podrá instalar WSUS 3.0. Tiene que iniciar sesión en el servidor en el que va a instalar WSUS 3.0 utilizando una cuenta que es miembro del grupo de administradores local. Sólo los miembros del grupo de administradores local pueden instalar WSUS 3.0.

El procedimiento siguiente usa las opciones de instalación predeterminadas de WSUS, que incluyen la instalación de Windows Internal Database para el software de base de datos de WSUS 3.0, almacenar las actualizaciones localmente y utilizar el sitio web predeterminado de IIS en el puerto 80.

**Para instalar WSUS 3.0**
1.  Haga doble clic en el archivo del instalador, **WSUSSetup.exe**.

2.  En la página de **bienvenida** del Asistente para la instalación, haga clic en **Siguiente**.

3.  En la página **Selección del modo de instalación**, haga clic en **Instalación de servidor completa incluida la consola de administración** si desea instalar el servidor en este equipo o **Sólo la consola de administración** si únicamente desea instalar la consola de administración.

4.  En la página **Contrato de licencia**, lea los términos del contrato de licencia con atención, haga clic en **Acepto los términos del Contrato de licencia** y después haga clic en **Siguiente**.

    ![](images/Cc720469.fa6ac6a6-6814-4b7e-96e8-e08af5e534b8(WS.10).gif)

5.  En la página **Seleccionar origen de la actualización** del Asistente para la instalación, puede especificar dónde obtienen las actualizaciones los clientes. Si activa la casilla de verificación **Almacenar actualizaciones localmente**, las actualizaciones se almacenarán en el servidor WSUS 3.0 y seleccionará una ubicación en el sistema de archivos para almacenar actualizaciones. Si no almacena las actualizaciones localmente, los equipos cliente se conectarán a Microsoft Update para obtener actualizaciones aprobadas. Conserve las opciones predeterminadas y haga clic en **Siguiente**.

    ![](images/Cc720469.c8bac396-ca39-4491-8b0c-742a0e470535(WS.10).gif)

6.  En la página **Opciones de base de datos**, seleccione el software utilizado para administrar la base de datos de WSUS 3.0. De manera predeterminada, el programa de instalación de WSUS ofrece la opción de instalar Windows Internal Database, si el equipo en el que se realiza la instalación ejecuta Windows Server 2003.

7.  Si no desea usar Windows Internal Database, deberá indicar una instancia de SQL Server para WSUS, haciendo clic en **Usar** **un servidor de base de datos existente en este equipo** y escribiendo el nombre de instancia en el cuadro. El nombre de la instancia debe aparecer como &lt;*nombreServidor*&gt;\\&lt;*nombreInstancia*&gt;, donde *nombreServidor* es el nombre del servidor y *nombreInstancia* es el nombre de la instancia SQL. Realice la selección y, después, haga clic en **Siguiente**.

8.  En la página **Conectando con la instancia de SQL Server**, WSUS intentará conectarse a la instancia especificada de SQL Server. Cuando se haya conectado correctamente, haga clic en **Siguiente** para continuar.

    ![](images/Cc720469.36c6af0c-a61e-4151-ae50-c754a106cb1b(WS.10).gif)

9.  En la página **Selección de sitio Web**, indique el sitio Web que utilizará WSUS 3.0. Si desea utilizar el sitio Web de IIS predeterminado en el puerto 80, seleccione la primera opción. Si ya tiene un sitio Web en el puerto 80, podrá crear un sitio alternativo en el puerto 8530 si selecciona la segunda opción. Conserve la opción predeterminada y haga clic en **Siguiente**.

10. En la página **Preparado para instalar Windows Server Update Services**, compruebe las selecciones y haga clic en **Siguiente**.

11. La página final del Asistente para la instalación le dirá si la instalación de WSUS 3.0 se completó correctamente. Después de hacer clic en **Finalizar**, el Asistente para la configuración se iniciará.
