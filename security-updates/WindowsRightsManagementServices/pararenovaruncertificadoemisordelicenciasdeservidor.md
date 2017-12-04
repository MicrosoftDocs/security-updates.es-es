---
TOCTitle: Para renovar un certificado emisor de licencias de servidor
Title: Para renovar un certificado emisor de licencias de servidor
ms:assetid: 'affce9cf-8b46-4293-8e1c-ee06f2ca6537'
ms:contentKeyID: 18127933
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747636(v=WS.10)'
---

Para renovar un certificado emisor de licencias de servidor
===========================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Si ha seleccionado utilizar la renovación sin conexión y va a utilizar un equipo que disponga de una configuración de seguridad de explorador ampliada, como un equipo con Windows Server 2003 o Windows XP con Service Pack 2 para conectarse a Internet y solicitar un certificado emisor de licencias de servidor, asegúrese de agregar la dirección URL del sitio Web de servicio de inscripción a la zona de sitios de confianza para permitir la descarga del certificado emisor de licencias de servidor. Esta dirección URL es https://activation.drm.microsoft.com.

Si va a utilizar el proceso de inscripción fuera de línea, asegúrese de que el equipo que utiliza para enviar la solicitud de inscripción al servicio de inscripción de Microsoft tiene GTE Cyber Trust Root CA instalado en el almacén de certificados. De forma predeterminada, esta entidad emisora de certificados es de confianza en los equipos con Windows Server 2003. Si el equipo tiene otra versión de Windows, para que esta entidad emisora de certificados sea de confianza, deberá instalar las actualizaciones de certificados más recientes desde Windows Update.

Renovación de certificados emisores de licencias de servidor
------------------------------------------------------------

#### Para renovar un certificado emisor de licencias de servidor

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee renovar un certificado, haga clic en **Administrar RMS en este sitio Web**.

2.  En la página **Administración**, en el área **Recursos de clúster**, haga clic en el botón **Renovar**. Se abrirá el cuadro de diálogo Renovar.

3.  Si el servidor está conectado a Internet, seleccione la opción **En línea** y haga clic en **Renovar** para renovar automáticamente el certificado emisor de licencias de servidor.

4.  Si el servidor no está conectado a Internet, seleccione la opción **Sin conexión** y, a continuación, haga clic en el botón **Exportar**. Aparecerá el cuadro de diálogo **Descarga de archivos**.

5.  Haga clic en **Guardar**. Aparecerá el cuadro de diálogo **Guardar como**.

    > [!NOTE]
    > En el cuadro de diálogo **Descarga de archivos**, no haga clic en **Abrir**. Si hace clic en **Abrir**, aparecerá un mensaje de error y el archivo de la solicitud de inscripción no se guardará. 

6.  Haga clic en **Guardar** para exportar la solicitud de renovación a un archivo. De forma predeterminada, el archivo se guardará en el escritorio y se llamará *nombre\_servidor*RenewalRequest.xml, donde *nombre\_servidor* es el nombre del servidor de RMS. Puede guardar el archivo en otra ubicación; para ello, seleccione la ubicación que desee en el menú desplegable Guardar en. También puede cambiar el nombre predeterminado del archivo escribiendo un nuevo nombre en **Nombre de archivo**.

7.  Una vez que haya guardado el archivo de solicitud de renovación, aparecerá el cuadro de diálogo **Descarga completa**. Puede hacer clic en **Abrir** para ver el código XML en el archivo, pero no es posible modificar el archivo. Para abrir la carpeta en la que está almacenado el archivo, haga clic en **Abrir carpeta**. Haga clic en **Cerrar** si ha terminado de consultar el archivo y de comprobar su ubicación.

8.  Traslade el archivo de solicitud de renovación de su servidor a un equipo que se pueda conectar a Internet y, a continuación, vaya al  https://go.microsoft.com/fwlink/?LinkId=25828.

9.  Siga las instrucciones del sitio Web para obtener un certificado emisor de licencias de servidor.

10. Traslade el certificado emisor de licencias de servidor de nuevo a este servidor de certificación raíz.

11. En el área **Recursos de clúster**, haga clic en **Renovar**. Se abrirá el cuadro de diálogo **Renovar**.

12. En el cuadro de diálogo **Renovar**, haga clic en el botón **Examinar** y localice el certificado emisor de licencias de servidor que había descargado; a continuación, haga clic en el botón **Importar**.

13. Haga clic en **Sí** para confirmar que desea importar ese certificado.

14. Una vez que el certificado emisor de licencias de servidor se haya renovado satisfactoriamente, el área **Recursos de clúster** se actualizará y mostrará la nueva fecha de caducidad del certificado emisor de licencias de servidor.

Para obtener más información acerca de la renovación de certificados emisores de licencias de servidor, vea "[Administración de certificados emisores de licencias de servidor](https://technet.microsoft.com/549979ad-13ee-4abc-8281-3e002a5a9561)", anteriormente en este tema.
