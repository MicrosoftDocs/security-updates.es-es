---
TOCTitle: Para inscribir manualmente un servidor de certificación raíz
Title: Para inscribir manualmente un servidor de certificación raíz
ms:assetid: 'aecdebb5-b28b-4b58-937a-392bb6ce9643'
ms:contentKeyID: 18127913
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747727(v=WS.10)'
---

Para inscribir manualmente un servidor de certificación raíz
============================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción Ejecutar como para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Si va a utilizar el proceso de inscripción fuera de línea, debe asegurarse de que los clientes de RMS no intenten conectarse al servidor de RMS para obtener licencias hasta que haya tenido lugar la inscripción. Si los clientes intentan conectarse a un servidor de RMS que no está inscrito, los servicios Web darán un error que no permitirá utilizarlos. Si no puede garantizar que los clientes no intenten conectarse al servidor de RMS, lo mejor es restablecer IIS después de realizar la inscripción para eliminar las condiciones de error que se hayan podido generar.

Si ha seleccionado utilizar la inscripción fuera de línea y va a utilizar un equipo que disponga de una configuración de seguridad de navegador ampliada, como un equipo con Windows Server 2003 o Windows XP Service Pack 2, para conectarse a Internet y solicitar un certificado emisor de licencias de servidor, asegúrese de agregar la dirección URL del sitio Web de servicio de inscripción a la zona de sitios de confianza para permitir la descarga del certificado emisor de licencias de servidor. Esta dirección URL es https://activation.drm.microsoft.com.

Si va a utilizar el proceso de inscripción fuera de línea, asegúrese de que el equipo que utiliza para enviar la solicitud de inscripción al servicio de inscripción de Microsoft tiene GTE Cyber Trust Root CA instalado en el almacén de certificados. De forma predeterminada, esta entidad emisora de certificados es de confianza en los equipos con Windows Server 2003. Si el equipo tiene otra versión de Windows, para que esta entidad emisora de certificados sea de confianza, deberá instalar las actualizaciones de certificados más recientes desde Windows Update.

Inscripción manual de un servidor de certificación raíz
-------------------------------------------------------

#### Para inscribir manualmente un servidor de certificación raíz

1.  Tras instalar RMS en el servidor que desea que sea el servidor de certificación raíz, abra la página **Administración global** y, a continuación, haga clic en **Administrar RMS en este sitio Web** junto al sitio Web al que desee importar un certificado emisor de licencias de servidor raíz.

2.  En el área **Recursos de clúster**, haga clic en **Inscribir**. Se abrirá el cuadro de diálogo deinscripción.

3.  Seleccione la opción **Sin conexión** y, a continuación, haga clic en el botón **Exportar**. Aparecerá el cuadro de diálogo **Descarga de archivos**.

4.  Haga clic en **Guardar**. Aparecerá el cuadro de diálogo **Guardar como**.

    > [!NOTE]
    > En el cuadro de diálogo **Descarga de archivos**, no haga clic en **Abrir**. Si hace clic en **Abrir**, aparecerá un mensaje de error y el archivo de la solicitud de inscripción no se guardará. 

5.  Haga clic en **Guardar** para exportar la solicitud de inscripción a un archivo. De forma predeterminada, el archivo se guardará en el escritorio y se llamará *nombre\_servidor*EnrollRequest.xml, donde *nombre\_servidor* es el nombre del servidor de RMS. Puede guardar el archivo en otra ubicación; para ello, seleccione la ubicación que desee en el menú desplegable **Guardar en**. También puede cambiar el nombre predeterminado del archivo escribiendo un nuevo nombre en **Nombre de archivo**.

6.  Cuando haya guardado el archivo de la solicitud de inscripción, aparecerá el cuadro de diálogo **Descarga completa**. Puede hacer clic en **Abrir** para ver el código XML en el archivo, pero no es posible modificar el archivo. Para abrir la carpeta en la que está almacenado el archivo, haga clic en **Abrir carpeta**. Haga clic en **Cerrar** si ha terminado de consultar el archivo y de comprobar su ubicación.

7.  Traslade el archivo de la solicitud de inscripción del servidor a un equipo con conexión a Internet y vaya al [sitio Web de Servicio de inscripción]().

8.  Siga las instrucciones del sitio Web para obtener un certificado emisor de licencias de servidor.

9.  Traslade el certificado emisor de licencias de servidor de nuevo a este servidor de certificación raíz.

10. En el área **Recursos de clúster**, haga clic en **Inscribir**. Se abrirá el cuadro de diálogo deinscripción.

11. En el cuadro de diálogo de **inscripción**, haga clic en el botón **Examinar** y localice el certificado emisor de licencias de servidor que había descargado; a continuación, haga clic en el botón **Importar**.

12. Haga clic en **Sí** para confirmar que desea importar ese certificado.

13. El área **Recursos de clúster** se actualizará para mostrar el certificado emisor de licencias de servidor.
