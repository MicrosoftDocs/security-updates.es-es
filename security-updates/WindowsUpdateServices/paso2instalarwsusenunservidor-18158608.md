---
TOCTitle: 'Paso 2: instalar WSUS en un servidor'
Title: 'Paso 2: instalar WSUS en un servidor'
ms:assetid: 'f593532c-e92e-47f3-914a-38a6c2519e94'
ms:contentKeyID: 18158608
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708622(v=WS.10)'
---

Paso 2: instalar WSUS en un servidor
====================================

Una vez que repase los requisitos de la instalación, estará preparado para instalar WSUS. Debe iniciar la sesión en el servidor en el que tiene previsto instalar WSUS con una cuenta que pertenezca al grupo local Administradores. Sólo los miembros del grupo local Administradores pueden instalar WSUS.

En el procedimiento siguiente se utilizan las opciones predeterminadas de instalación de WSUS para Windows Server 2003, que incluyen: instalar Windows SQL Server 2000 Desktop Engine (WMSDE) para el software de base de datos de WSUS, almacenar las actualizaciones localmente y utilizar el sitio Web predeterminado de IIS en el puerto 80. En las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés) encontrará los procedimientos para utilizar opciones de instalación personalizadas, como utilizar un sistema operativo diferente, software de base de datos diferente o un sitio Web con un número de puerto personalizado.

**Para instalar WSUS en Windows Server 2003**
1.  Haga doble clic en el archivo del instalador **WSUSSetup.exe**.

    | ![](images/Cc708622.note(WS.10).gif)Nota                                                                                                                                                                                               |
    |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | La versión más reciente de WSUSSetup.exe está disponible en el [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=47374) para Windows Server Update Services, en la dirección http://go.microsoft.com/fwlink/?LinkId=47374 (puede que esté en inglés). |

2.  En la página de bienvenida del asistente, haga clic en **Siguiente**.

3.  Lea los términos del contrato de licencia detenidamente, haga clic en **Acepto los términos del Contrato de licencia** y, a continuación, haga clic en **Siguiente**.

4.  En la página **Seleccionar origen de la actualización**, puede especificar el lugar de donde los clientes obtendrán las actualizaciones. Si activa la casilla de verificación **Almacenar actualizaciones localmente**, las actualizaciones se almacenarán en el servidor WSUS, y deberá seleccionar la ubicación del sistema de archivos en la que se guardarán. Si las actualizaciones no se almacenan localmente, los equipos cliente se conectarán a Microsoft Update para obtener las actualizaciones autorizadas.

    Mantenga las opciones predeterminadas y haga clic en **Siguiente**.

    ![](images/Cc708622.fa6ac6a6-6814-4b7e-96e8-e08af5e534b8(WS.10).gif)

5.  En la página **Opciones de base de datos**, seleccione el software que se utilizará para administrar la base de datos de WSUS. De manera predeterminada, el programa de instalación de WSUS propone instalar WMSDE si el equipo donde va a realizar la instalación ejecuta Windows Server 2003.

    Si no se puede utilizar WMSDE, debe especificar la instancia de SQL Server que utilizará WSUS; para ello, haga clic en **Usar un servidor de base de datos existente en este equipo** y escriba el nombre de la instancia en el cuadro **Seleccionar instancia SQL**. Para obtener más información acerca de otras opciones de software de base de datos que no sean WMSDE, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés).

    Mantenga las opciones predeterminadas y haga clic en **Siguiente**.

    ![](images/Cc708622.bc0b73ad-b338-437c-a3c7-0299e819840d(WS.10).gif)

6.  En la página **Selección de sitio Web**, especifique el sitio Web que utilizará WSUS. En esta página también aparecen dos direcciones URL importantes que dependen de lo que seleccione: la dirección URL a la que deben obtener acceso los equipos cliente WSUS para obtener actualizaciones y la dirección URL de la consola de WSUS donde se configurará WSUS.

    Si ya tiene un sitio Web en el puerto 80, puede que necesite crear el sitio Web de WSUS en un puerto personalizado. Para obtener más información sobre cómo ejecutar WSUS en un puerto personalizado, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés).

    Mantenga la opción predeterminada y haga clic en **Siguiente**.

    ![](images/Cc708622.64ed7643-a050-4f54-bf9f-04cf7931adc0(WS.10).gif)

7.  En la página **Configuración de actualización reflejada**, puede especificar la función de administración de este servidor WSUS. Si es el primer servidor WSUS de la red o desea una topología de administración distribuida, omita esta pantalla.

    Si desea una topología de administración centralizada y éste no es el primer servidor WSUS de la red, active la casilla de verificación y escriba el nombre de un servidor WSUS adicional en el cuadro **Nombre de servidor**. Para obtener más información acerca de las funciones de administración, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés).

    Mantenga la opción predeterminada y haga clic en **Siguiente**.

    ![](images/Cc708622.f26e09d5-983c-418d-8511-8960850403ef(WS.10).gif)

8.  En la página **Listo para instalar Microsoft Windows Server Update Services**, revise las opciones seleccionadas y haga clic en **Siguiente**.

    ![](images/Cc708622.20de7d09-3d30-4867-9253-6f353dd1923d(WS.10).gif)

9.  Si la última página del asistente confirma que la instalación de WSUS se ha realizado correctamente, haga clic en **Finalizar**.
