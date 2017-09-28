---
TOCTitle: Preparación para la instalación del servidor de certificación raíz
Title: Preparación para la instalación del servidor de certificación raíz
ms:assetid: 'ed51605e-8b17-4155-8d83-f6777f499b7b'
ms:contentKeyID: 18128011
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747726(v=WS.10)'
---

Preparación para la instalación del servidor de certificación raíz
==================================================================

En la instalación de prueba del ejemplo, sólo existe un servidor de certificación raíz. Si lo desea, puede configurar servidores adicionales, ya sea como parte de un clúster de certificación raíz o como clúster de servidor de licencias independiente. La configuración de la infraestructura de todos estos servidores es la misma; por tanto, deberá llevar a cabo el procedimiento que se explica en este tema en cada uno de los servidores.

Cuando haya instalado el controlador de dominio y configurado los servidores de base de datos (como se describe en la sección anterior), realice los pasos descritos en la tabla siguiente y estará listo para instalar RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente de infraestructura</th>
<th>Para preparar el servidor para la instalación de RMS</th>
<th>Notas para la implementación en un entorno de producción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Sistema operativo</p></td>
<td style="border:1px solid black;"><p>En un equipo que cumple los requisitos de hardware de RMS pero que todavía no está conectado a la red, instale el sistema operativo Windows Server 2003 y utilice el sistema de archivos NTFS para la partición.</p></td>
<td style="border:1px solid black;"><p>Se recomienda instalar siempre las revisiones y los Service Packs más recientes. Utilice particiones con formato NTFS.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Conexión a Internet</p>
<p>(opcional)</p></td>
<td style="border:1px solid black;"><p>Establezca una conexión Ethernet con una red que proporcione conexión a Internet, pero que esté aislada del entorno de producción. Si va a utilizar la inscripción en línea para inscribir el servidor de RMS como parte del proceso de establecimiento de servicios en línea, el servidor debe tener conexión a Internet.</p></td>
<td style="border:1px solid black;"><p>Si utiliza la inscripción en línea, asegúrese de que la conexión a Internet cuente con un cortafuegos adecuado.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Dirección IP</p></td>
<td style="border:1px solid black;"><p>Asigne una dirección IP estática a este equipo.</p></td>
<td style="border:1px solid black;"><p>Utilice siempre direcciones IP estáticas para los servidores.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Unión del equipo al dominio</p></td>
<td style="border:1px solid black;"><p>Inicie sesión en el equipo como administrador local. Haga clic en <strong>Inicio</strong>, haga clic con el botón secundario en <strong>Mi PC</strong>, seleccione <strong>Propiedades</strong>, la ficha <strong>Nombre de equipo</strong> y haga clic en <strong>Cambiar</strong>.</p></td>
<td style="border:1px solid black;"><p>Use el mismo dominio para todos los servidores.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>No cambie el nombre de equipo, haga clic en <strong>Dominio</strong>, escriba el nombre del dominio (por ejemplo, Contoso.com) y después haga clic en <strong>Aceptar</strong>. Proporcione las credenciales de usuario que le permitan unirse al dominio, haga clic en <strong>Aceptar</strong> y después reinicie el equipo cuando lo solicite el sistema. Cuando el equipo vuelva a iniciarse y se le pida las credenciales de inicio de sesión, proporcione el dominio, el nombre de usuario y la contraseña pertinentes.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Usuario e inicio de sesión</p></td>
<td style="border:1px solid black;"><p>Haga clic con el botón secundario en <strong>Mi PC</strong>, seleccione <strong>Administrar</strong>, expanda <strong>Usuarios locales y grupos</strong>, haga clic en <strong>Grupos</strong> y después doble clic en <strong>Administradores</strong>.</p>
<p>Haga clic en <strong>Agregar</strong>, especifique el nombre de la cuenta de usuario que desee agregar (por ejemplo, usuario@contoso.com) y haga clic en <strong>Aceptar</strong>. Otorgue privilegios de administrador a la cuenta de usuario. Cuando se le soliciten las credenciales, proporcione las credenciales adecuadas, por ejemplo Contoso\Administrador.</p>
<p>Inicie sesión como usuario del dominio con privilegios de administrador en el equipo.</p></td>
<td style="border:1px solid black;"><p>Son necesarios permisos de administrador para agregar componentes a este equipo. Es posible que no pueda completar algunos pasos de la instalación utilizando la cuenta de administrador local. Debe existir al menos un usuario de dominio en este servidor que sea administrador. Además, SQL Server requiere permisos de administrador del sistema para crear bases de datos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Conexión a Internet</p>
<p>(opcional)</p></td>
<td style="border:1px solid black;"><p>Con un explorador de Internet, vaya a http://uddi.microsoft.com/ para comprobar el acceso a Internet. En equipos que ejecuten Windows Server 2003, puede ser necesario modificar los archivos Lmhosts y Hosts para que incluyan el controlador de dominio.</p></td>
<td style="border:1px solid black;"><p>Vaya a http://uddi.microsoft.com para comprobar el acceso a Internet.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Activación de Windows</p></td>
<td style="border:1px solid black;"><p>Puede utilizar el Asistente para activación para activar Windows con Microsoft mediante una conexión a Internet, o puede activar Windows a través del teléfono. Para obtener más información sobre la activación del producto Windows Server 2003, vea el Centro de ayuda y soporte técnico de Windows Server 2003.</p></td>
<td style="border:1px solid black;"><p>Debe activar Windows Server 2003 en un plazo de 14 días a partir de la instalación.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Actualizaciones de software</p></td>
<td style="border:1px solid black;"><p>Asegúrese de instalar las actualizaciones más recientes para el software que se instala en este equipo.</p></td>
<td style="border:1px solid black;"><p>Instale las actualizaciones de software más recientes.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configure Internet Explorer</p></td>
<td style="border:1px solid black;"><p>RMS utiliza una interfaz Web para la administración. Es posible que algunas opciones de seguridad predeterminadas impidan que las páginas se muestren correctamente. Algunas páginas del sitio Web de administración de RMS utilizan ventanas emergentes para algunas opciones de configuración.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>
</tbody>
</table>
  
Cuando haya realizado los pasos anteriores en los dos servidores, ya estará listo para instalar RMS y establecer los servicios en línea en los servidores.
