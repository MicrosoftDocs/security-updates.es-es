---
TOCTitle: Configuración de SMS o de una directiva de grupo para admitir la implementación de clientes
Title: Configuración de SMS o de una directiva de grupo para admitir la implementación de clientes
ms:assetid: '9e37c27b-8cc1-40c6-adb7-0937aa64c8db'
ms:contentKeyID: 18127910
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747703(v=WS.10)'
---

Configuración de SMS o de una directiva de grupo para admitir la implementación de clientes
===========================================================================================

Al implementar RMS, debe instalarse una aplicación compatible con RMS en el equipo de los usuarios para que éstos protejan el contenido y utilicen contenido protegido con RMS.

Para que una aplicación sea compatible con RMS, debe integrar el cliente de RMS en sus operaciones. Antes de Windows Vista®, el cliente RMS estaba disponible como un componente de Windows descargado por separado del Centro de descarga Microsoft. Sin embargo, si no desea descargar el cliente individualmente para cada equipo cliente de la empresa, puede utilizar Microsoft Systems Management Server (SMS), directiva de grupo o secuencias de comandos para automatizar la entrega de los clientes de RMS a los equipos cliente.

| ![](images/Cc747703.Important(WS.10).gif)Importante                             |
|--------------------------------------------------------------------------------------------------------------|
| El cliente RMS está integrado en Windows Vista. Por tanto, ya no es necesaria una instalación independiente. |

Si utiliza SMS para distribuir el cliente de RMS, deberá hacer lo siguiente:

-   Cree un archivo de definición de paquete nuevo.
-   Extraiga los archivos de Windows Installer del archivo WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe. Para hacerlo, guarde primero el archivo WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe. No lo instale. En este ejemplo, supongamos que el archivo se guarda en c:\\nombre\_carpeta. Abra una ventana de símbolo de sistema y escriba el siguiente comando:
    `c:\folder_name\WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe /x/t:c:\folder_name`
    Este comando extraerá los archivos MSDrmClient.msi y RMClientBackCompat.msi del archivo .exe y se ubicarán en c:\\*nombre\_carpeta*.
-   Utilice los archivos de Windows Installer para la definición y origen de paquete.
-   Anuncie la disponibilidad de los paquetes a través de su red.

| ![](images/Cc747703.note(WS.10).gif)Nota                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Se necesitan derechos administrativos para instalar software; es posible que una directiva de seguridad de su organización requiera que un administrador del sistema instale el software de cliente de RMS. |

Para obtener más información acerca del uso de SMS para distribuir software, consulte la guía de conceptos, planificación e implementación de Systems Management Server 2003 ([http://go.microsoft.com/fwlink/?LinkID=17401](http://go.microsoft.com/fwlink/?linkid=17401)).

Para obtener más información acerca de la implementación de software de cliente mediante una directiva de grupo, consulte los temas relacionados con la implementación de software basada en la directiva de grupo ([http://go.microsoft.com/fwlink/?LinkID=38997](http://go.microsoft.com/fwlink/?linkid=38997)).
