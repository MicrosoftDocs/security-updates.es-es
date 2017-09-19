---
TOCTitle: 'Para instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) a fin de proporcionar compatibilidad con bases de datos para RMS'
Title: 'Para instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) a fin de proporcionar compatibilidad con bases de datos para RMS'
ms:assetid: 'c9b9cd08-98c4-424f-b3fc-d685f57c002e'
ms:contentKeyID: 18127951
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747667(v=WS.10)'
---

Para instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) a fin de proporcionar compatibilidad con bases de datos para RMS
===================================================================================================================================

Instalación de Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) a fin de proporcionar compatibilidad con bases de datos para RMS
------------------------------------------------------------------------------------------------------------------------------------

#### Para instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) a fin de proporcionar compatibilidad con bases de datos para RMS

1.  Inicie sesión con una cuenta de dominio que sea miembro del grupo local Administradores en el servidor en el que desea instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000).

2.  Descargue MSDE 2000 del [sitio Web de Microsoft](http://www.microsoft.com/) (http://www.microsoft.com/) y guárdelo en una ubicación de su equipo.

3.  Ejecute el archivo MSDE2000A.exe para extraer el paquete de instalación de MSDE 2000 a una carpeta. De forma predeterminada, esta carpeta se llamará MSDERelA, pero puede especificar otro nombre.

4.  Abra un símbolo del sistema y desplácese a la ubicación en la que guardó la instalación de MSDE 2000.

5.  Escriba el siguiente comando para instalar la aplicación Microsoft SQL Server 2000 Desktop Engine con la configuración correcta para trabajar con RMS y sustituya *password* por la contraseña segura que desee:

    **Setup.exe /i setup\\sqlrun10.msi INSTANCENAME=RMS DISABLEAGENTSTARTUP=1 SAPWD=***password*

    | ![](images/Cc747667.Important(WS.10).gif)Importante                                                                                                                                                                                                                          |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | El servicio MSDE debe iniciarse tras su instalación. Puede iniciar el servicio desde **Servicios** en el **Panel de control**. Es recomendable configurar el servicio para que se inicie automáticamente para garantizar que la base de datos MSDE esté siempre disponible cuando RMS se esté ejecutando. |

No establezca los servicios en línea de RMS en un servidor hasta tener una base de datos instalada para admitir la base de datos de configuración de RMS.

Se recomienda el uso de Microsoft SQL Server Desktop Engine para permitir las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no incluye las herramientas necesarias para que funcione completamente una base de datos a nivel corporativo. Además, dado que MSDE no permite el trabajo con red remota, debe instalarlo en el mismo servidor que RMS y no puede añadir servidores de RMS adicionales al clúster de RMS. Las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Con esta restricción, no podrá realizar y restaurar copias de seguridad de la base de datos de configuración de RMS, ver información de registro o modificar directamente datos almacenados en la base de datos de configuración.
