---
TOCTitle: Problemas de establecimiento de servicios en línea de RMS
Title: Problemas de establecimiento de servicios en línea de RMS
ms:assetid: 'b0e6ef48-ab38-4426-be5b-811cf64c45c0'
ms:contentKeyID: 18127929
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747638(v=WS.10)'
---

Problemas de establecimiento de servicios en línea de RMS
=========================================================

Al establecer los servicios en línea de RMS, se configuran y establecen los archivos de recurso y las conexiones entre los diferentes componentes de los que depende RMS. Si se produce algún error mientras RMS intenta configurar un recurso, el establecimiento de servicios en línea falla y aparece un mensaje de error. En esta sección se describen las causas más habituales de estos errores para ayudarle a solucionar problemas inesperados que impiden el correcto establecimiento de servicios en línea de RMS.

No se pueden establecer los servicios en línea en el servidor de certificación raíz
-----------------------------------------------------------------------------------

Es posible que no pueda establecer los servicios en línea en un servidor de certificación raíz porque no aparecen las páginas de establecimiento de servicios en línea correctas. Esto puede ocurrir al hacer clic en Establecer los servicios en línea de RMS en este sitio Web para establecer los servicios en línea en el primer servidor de certificación raíz en la página Administración global. Sin embargo, en lugar de las páginas de establecimiento de servicios en línea para un servidor de certificación raíz, aparecen las páginas para establecer los servicios en línea en un servidor de licencias.

Este problema se produce si no se han anulado los servicios en línea en el último servidor de certificación raíz en este bosque de Active Directory antes de desinstalar RMS y, a continuación, se intentan establecer los servicios en línea en un servidor de certificación raíz. Al anular los servicios en línea en el único servidor de certificación raíz de un bosque de Active Directory, se elimina el punto de conexión de servicio de Active Directory. Si no anula los servicios en línea en el último servidor de certificación raíz del bosque antes de desinstalar RMS, no podrá volver a establecer el servicio en línea en un servidor de certificación raíz que se encuentre en este bosque antes de quitar manualmente el punto de conexión de servicio de Active Directory.

Si aparecen las páginas de establecimiento de servicios en línea en un servidor de licencias cuando intenta establecer los servicios en línea en el primer servidor de certificación raíz de un bosque de Active Directory, quite el punto de conexión de servicio de Active Directory tal como se indica a continuación:

**Para quitar el punto de conexión de servicio de RMS**
1.  Si es necesario, instale las herramientas de soporte técnico de Windows Server:

    En el caso de Windows Server 2003, ejecute Suptools.msi desde la carpeta \\Support\\Tools que se encuentra en el CD de instalación.

    En el caso de Windows 2000 Server, ejecute Setup.exe desde la carpeta \\Support Tools que se encuentra en el CD de instalación.

2.  Inicie sesión en el controlador de dominio del que es miembro el servidor de certificación raíz utilizando una cuenta que sea miembro del grupo de administradores del dominio.

3.  En el símbolo del sistema, escriba el siguiente comando y presione ENTRAR:

    **ldp**

4.  Haga clic en **Conexión** y después en **Conectar**.

5.  Presione ENTRAR. No escriba ninguna información.

6.  Haga clic en **Conexión** y, a continuación, en **Enlazar**.

7.  Presione ENTRAR. No escriba ninguna información.

8.  Haga clic en **Ver** y después en **Árbol**.

9.  Presione ENTRAR. No escriba ninguna información.

    En el panel izquierdo, aparece **dc=YourDomain,dc=com**.

10. Expanda **dc=YourDomain,dc=com**.

11. Expanda **Configuración**.

12. Expanda **Servicios**.

13. Elimine **RightsManagementServices**.

O bien

1.  Descargue e instale el kit de herramientas administrativas de RMS. El kit de herramientas puede descargarse del [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=33841).
2.  Abra un símbolo del sistema; para ello, haga clic en **Inicio**, **Ejecutar**. En el cuadro de diálogo **Ejecutar**, escriba **cmd** y, a continuación, haga clic en **Aceptar**.
3.  En el símbolo del sistema, escriba el comando siguiente:
    **ADSCPRegister.exeunregisterscp** &lt;*URL\_para\_anular\_registro*&gt;
4.  En lugar de &lt;*URL\_para\_anular\_registro*&gt; escriba la dirección URL del punto de conexión de servicio de RMS, por ejemplo, https://mi\_dominio/\_wmcs/Certification.

Cuando finalice estos pasos, podrá establecer los servicios en línea en el servidor de certificación raíz.

No se puede generar el contexto SSPI
------------------------------------

Es posible que aparezca el error "No se puede generar el contexto SSPI" durante el establecimiento de servicios en línea si no se autenticó la cuenta de servicio de RMS al inscribir el servidor de certificación raíz con el servicio de inscripción de Microsoft.

Si recibe este mensaje de error, compruebe que la cuenta de servicio de RMS sea una cuenta de dominio válida. Si se trata de una cuenta de grupo, compruebe que la pertenencia al grupo esté actualizada, que puede resolver todas las cuentas de usuario del grupo en el dominio y que las cuentas poseen permisos para las bases de datos de SQL.