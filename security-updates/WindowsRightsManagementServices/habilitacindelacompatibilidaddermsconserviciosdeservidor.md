---
TOCTitle: Habilitación de la compatibilidad de RMS con servicios de servidor
Title: Habilitación de la compatibilidad de RMS con servicios de servidor
ms:assetid: '6288323c-0638-41b6-bef8-67a7c9433424'
ms:contentKeyID: 18127770
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747593(v=WS.10)'
---

Habilitación de la compatibilidad de RMS con servicios de servidor
==================================================================

RMS también puede proporcionar certificados de cuenta de permisos y licencias de uso a aplicaciones compatibles con RMS. Al configurar servicios de servidor deben tenerse en cuenta los siguientes puntos:

-   Las listas de control de acceso discrecional (DACL) en las canalizaciones RMS utilizan de forma predeterminada la configuración más segura. Cuando utilice servicios de servidor de RMS, debe modificar la DACL.
-   Si el cliente de RMS se instala en un servidor basado en Windows Server 2003 y está habilitada la configuración de seguridad mejorada de Internet Explorer, debe agregar la dirección URL del clúster de RMS a la zona de sitios de confianza de Internet Explorer.
-   Muchos servicios de servidor utilizan la funcionalidad avanzada de servicios de directorio de Active Directory, que sólo está disponible si todos los controladores de dominio de Active Directory ejecutan Windows Server 2003. Si utiliza cualquier servicio de servidor (por ejemplo, Microsoft Office SharePoint Server 2007 o Microsoft Exchange Server 2007), se recomienda que todos los controladores de dominio ejecuten Windows Server 2003 y que los niveles funcionales de Active Directory de dominio y de bosque estén en el nivel de Windows Server 2003.

Lista de control de acceso discrecional (DACL) predeterminada en la canalización de certificación de servidor
-------------------------------------------------------------------------------------------------------------

Las aplicaciones como Microsoft Office SharePoint Server 2007 o Microsoft Exchange Server 2007 son compatibles con RMS para solicitar licencias de uso en nombre de los usuarios. En una instalación predeterminada de RMS, la DACL de la canalización de certificación de servidor de RMS está restringida, lo que significa que una aplicación no puede obtener certificados ni licencias para sus usuarios. Sin embargo, si tiene una aplicación compatible con RMS para estos equipos, puede habilitarlos para participar en el sistema RMS configurando las DACL en la canalización de certificación de servidor de RMS.

Las aplicaciones de servidor compatibles con RMS se conectarán con el servicio de certificación de RMS mediante el archivo ServerCertification.asmx.

Cuando RMS crea estos archivos, las DACL de los archivos están establecidas para permitir exclusivamente el acceso a procesos del sistema. Se recomienda crear un grupo de seguridad de Active Directory para servicios de servidor y, a continuación, rellenar este grupo con los objetos de Active Directory de los equipos que solicitan licencias de uso en nombre de sus usuarios.

Una vez creado el grupo, puede modificar la DACL del archivo ServerCertification.asmx para permitir al grupo disponer de permiso de Lectura & ejecución en el servicio. También debe agregar el grupo de servicio de RMS a la DACL con el permiso Lectura & ejecución.

> [!NOTE]
> Si existe más de un servidor de RMS en el clúster, la DACL del archivo ServerCertification.asmx se debe cambiar en cada servidor del clúster. 

Para Microsoft Exchange Server 2007, el objeto de equipo de Active Directory de cada servidor cabeza de puente de Exchange se debe agregar al grupo de servicios de servidor. Si no se realiza esta adición, el servidor cabeza de puente de Exchange no podrá solicitar licencias en nombre de los usuarios que reciben el correo electrónico.

Para Office SharePoint Server 2007, debe agregar el objeto de equipo de Active Directory del servidor que ejecuta Office SharePoint Server 2007 al grupo de servicios de servidor. Si el servidor Office SharePoint Server 2007 está configurado para utilizar el servidor predeterminado en Active Directory, debe agregar el grupo de servicio de RMS y el grupo creado para servicios de servidor al archivo ServiceLocater.asmx, y permitir el permiso Lectura & ejecución.

> [!IMPORTANT]
> Después de cambiar la DACL en ServerCertification.asmx y ServiceLocater.asmx, es necesario reiniciar Servicios de Internet Information Services (IIS). Para restablecer IIS, ejecute el comando **iisreset** desde el símbolo del sistema. 
