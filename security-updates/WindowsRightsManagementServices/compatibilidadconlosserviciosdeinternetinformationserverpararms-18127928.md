---
TOCTitle: Compatibilidad con los Servicios de Internet Information Server para RMS
Title: Compatibilidad con los Servicios de Internet Information Server para RMS
ms:assetid: 'bd4dc69f-1e4e-4e95-9ae2-c925d8a14d4c'
ms:contentKeyID: 18127928
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747649(v=WS.10)'
---

Compatibilidad con los Servicios de Internet Information Server para RMS
========================================================================

Los servicios principales de RMS se suministran a través de un conjunto de servicios Web de ASP .NET. Estos servicios Web se ejecutan en los Servicios de Internet Information Server (IIS) de Microsoft®. Durante el proceso de establecimiento de servicios en línea en los servidores, RMS configura directorios virtuales en IIS, en los que se instalan los archivos de aplicación de los servicios Web.

Durante el establecimiento de servicios en línea en los servidores, se puede seleccionar de la lista de los sitios Web que existen en el servidor el sitio Web en el que se desea crear los directorios virtuales. Antes de establecer servicios en línea en un servidor, es aconsejable crear un sitio Web especial para RMS. De este modo, se podrán configurar restricciones de autenticación y de acceso específicas para la instalación de RMS específica.

De forma predeterminada, los archivos de servicios Web y los directorios virtuales están protegidos por listas de control de acceso discrecional (DACL), para evitar el acceso no autorizado a sus características. Las entradas de control de acceso (ACE) en estos elementos son las siguientes:

-   El grupo Administradores tiene control completo.
-   La cuenta del sistema local tiene control completo.
-   El grupo de servicio de RMS (RMS Service Group) tiene permisos de lectura y ejecución.
-   Los invitados y usuarios tienen permisos de lectura y ejecución, visualización del contenido de la carpeta y lectura.
-   El acceso anónimo no está autorizado.

En la tabla siguiente, se enumeran los directorios virtuales que se crean en IIS y los servicios que se instalan en dichos directorios.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Directorio virtual</th>
<th>Servicio</th>
<th>Archivo del servicio Web</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">_wmcs</td>
<td style="border:1px solid black;">Directorio virtual de administración del clúster de RMS</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certification</td>
<td style="border:1px solid black;">Directorio virtual que contiene los servicios que permiten la certificación de RMS</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Proxy de activación</td>
<td style="border:1px solid black;">Activation.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Certificación de cuentas</td>
<td style="border:1px solid black;">Certification.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Precertificación</td>
<td style="border:1px solid black;">Precertification.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Localización de servicios</td>
<td style="border:1px solid black;">ServiceLocator.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Server.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Certificación de servidores</td>
<td style="border:1px solid black;">ServerCertification.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Certificación de dispositivos móviles</td>
<td style="border:1px solid black;">MobileDeviceCertfication.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Inscripción</td>
<td style="border:1px solid black;">SubEnrollService.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Licencias</td>
<td style="border:1px solid black;">Directorio virtual que contiene los servicios que hacen posible la emisión de licencias de RMS</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Licencias</td>
<td style="border:1px solid black;">License.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Publicación</td>
<td style="border:1px solid black;">Publish.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Servidor</td>
<td style="border:1px solid black;">Server.asmx</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Localización de servicios</td>
<td style="border:1px solid black;">ServiceLocator.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Admin</td>
<td style="border:1px solid black;">Directorio virtual que contiene los servicios que permiten la administración de RMS</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Administración</td>
<td style="border:1px solid black;">AdminSvc.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DrmRemote</td>
<td style="border:1px solid black;">Interfaz de .NET Remoting</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DirectoryServices</td>
<td style="border:1px solid black;">Éste es un subdirectorio de DrmRemote</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747649.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| El servicio de administración tiene restricciones más estrictas que el resto de los servicios Web, porque las interfaces que contiene permiten configurar RMS. Por ello, los integrantes del grupo Usuarios no pueden obtener acceso a este servicio. Además, el filtro IP está habilitado para conceder acceso sólo al equipo local. El directorio virtual DirectoryServices no otorga acceso a los usuarios invitados. El servicio de localización de servicios también otorga control absoluto a la cuenta Servicio de red. Para establecer los servicios en línea en un servidor de licencias, debe cambiar las entradas ACE predeterminadas de RMS para permitir el acceso al administrador de RMS. |
