---
TOCTitle: Configuración de un controlador de dominio y un servidor de base de datos
Title: Configuración de un controlador de dominio y un servidor de base de datos
ms:assetid: 'd20f8305-9f9e-4760-bfbf-82824db60d1f'
ms:contentKeyID: 18127968
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747681(v=WS.10)'
---

Configuración de un controlador de dominio y un servidor de base de datos
=========================================================================

Antes de instalar un servidor de certificación raíz o un servidor de licencias, asegúrese de haber implementado la compatibilidad de dominio y de base de datos mediante Active Directory y un servidor de base de datos, como SQL Server 2000 con Service Pack 3 (SP3) o Microsoft® SQL Server 2000 Desktop Engine (MSDE 2000) Versión A. Aunque ya se estén ejecutando los componentes requeridos en el entorno de producción, se recomienda que no utilice el entorno de producción para realizar pruebas.

Los procedimientos siguientes configuran un controlador de dominio y un servidor de base de datos en un único equipo en una red aislada para realizar pruebas de servidor.

| ![](images/Cc747681.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En este ejemplo, el servidor de base de datos se ejecuta en el controlador de dominio. En un entorno de producción, generalmente no es recomendable alojar otros componentes en un controlador de dominio. En este ejemplo, Active Directory y el servidor de base de datos están instalados en el mismo equipo para habilitar la instalación de toda la infraestructura en un número mínimo de equipos. |

Si decide utilizar MSDE 2000 como servidor de bases de datos, debe tener en cuenta que no acepta interfaces de red y que los términos de uso de MSDE 2000 especifican que no puede utilizar herramientas de cliente de SQL Server para manipular una base de datos MSDE. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración. Por tanto, se recomienda utilizar MSDE 2000 sólo para permitir bases de datos de RMS en entornos de prueba.

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
<th>Pasos para configurar un controlador de dominio y un servidor de base de datos</th>
<th>Notas para la implementación en un entorno de producción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Sistema operativo</p></td>
<td style="border:1px solid black;"><p>En un equipo que cumple con los requisitos de hardware de RMS pero que todavía no está conectado a la red, instale Windows 2000 Server con SP3 o posterior o Windows Server 2003. Utilice el sistema de archivos NTFS de la partición.</p></td>
<td style="border:1px solid black;"><p>Se recomienda encarecidamente que instale siempre el Service Pack y las actualizaciones más recientes. Utilice particiones con formato NTFS.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Conexión de red</p></td>
<td style="border:1px solid black;"><p>Realice una conexión a una red que proporcione acceso a Internet pero que esté aislada del entorno de producción.</p></td>
<td style="border:1px solid black;"><p>La conexión a Internet debe poseer un servidor de seguridad adecuado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Dirección IP</p></td>
<td style="border:1px solid black;"><p>Asigne una dirección IP estática a este equipo.</p></td>
<td style="border:1px solid black;"><p>Utilice siempre direcciones IP estáticas para los servidores.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Active Directory</p></td>
<td style="border:1px solid black;"><p>Inicie sesión como administrador local.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Haga clic en <strong>Inicio</strong>, haga clic en <strong>Ejecutar</strong>, escriba <code>dcpromo</code> en el cuadro <strong>Abrir</strong> y por último haga clic en <strong>Aceptar</strong>.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Cuando aparezca el asistente para la instalación de Active Directory, siga los pasos del asistente para crear un nuevo dominio en un bosque nuevo y aceptar las opciones predeterminadas, excepto las opciones siguientes:</p>
<p>Especifique el nombre del dominio, por ejemplo, contoso.com.</p>  
<p>Permita que el asistente configure DNS en el equipo.</p>  
<p>Seleccione <strong>Permisos compatibles sólo con servidores Windows 2000</strong> si todos los controladores de dominio se ejecutan en Windows 2000 o posterior.</p>
<p>Proporcione una contraseña segura para el administrador local.</p></td>
<td style="border:1px solid black;"><p>Si se necesitan nuevos dominios para implementar RMS, configúrelos en Active Directory.</p>
<p>Utilice siempre contraseñas seguras para todas las cuentas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Reinicie el equipo cuando lo solicite el sistema.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Para comprobar el nivel funcional, abra el complemento <strong>Usuarios y equipos de Active Directory</strong> haciendo clic con el botón secundario en el nombre de dominio y después en <strong>Propiedades</strong>, y compruebe la configuración del cuadro <strong>Modo de operación del dominio</strong>. Si no existen controladores de dominio anteriores a los de Windows 2000, haga clic en <strong>Cambiar el modo</strong> para que el dominio funcione en <strong>Modo nativo</strong>.</p>
<p>Nota: En Windows Server 2003, la opción <strong>Modo de operación del dominio</strong> se reemplaza con <strong>Nivel funcional del dominio</strong>.</p></td>
<td style="border:1px solid black;"><p>Para conseguir una seguridad y una manejabilidad óptimas, no debe utilizar el nivel funcional mixto de Windows 2000 para la compatibilidad de RMS.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cuentas de usuario</p></td>
<td style="border:1px solid black;"><p>Cree una cuenta de usuario de dominio para utilizarla como cuenta de servicio de RMS para RMS, como por ejemplo ContosoRMS@contoso.com. Especifique una contraseña segura. Asegúrese de especificar una dirección de correo electrónico para el usuario. Si no se especifica la dirección de correo electrónico en Active Directory, el usuario no podrá obtener licencias y certificados de RMS.</p>
<p>Nota: La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS.</p></td>
<td style="border:1px solid black;"><p>Debe crear una cuenta independiente en Active Directory para que la utilice la cuenta de servicio de RMS. Incluya una dirección de correo electrónico. No otorgue a la cuenta ningún permiso especial.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SQL Server 2000</p></td>
<td style="border:1px solid black;"><p>Inicie sesión en el servidor en el que desee instalar la base de datos. Si se trata del mismo servidor que el controlador de dominio, debe iniciar sesión como administrador de dominio.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Siga las instrucciones proporcionadas por el software de base de datos para instalar el software del servidor de base de datos.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Utilice procedimientos recomendados de servidor para instalar el servidor de base de datos, como por ejemplo:</p>
<ul>  
<li>Proporcione un nombre para la cuenta de administrador del sistema de base de datos y un nombre de organización, como por ejemplo Contoso.<br />  
<br />  
</li>  
<li>Proporcione una contraseña segura de administrador de sistema.<br />  
<br />  
</li>  
<li>Utilice métodos de autenticación de Windows integrados.<br />  
<br />  
</li>
</ul></td>
<td style="border:1px solid black;"><p>Debe utilizar un modo Autenticación de Windows integrado. Si no puede ejecutar el servidor de base de datos en este modo, póngase en contacto con el administrador de dominio y con el administrador de servidor de base de datos para determinar qué cambios pueden requerirse en la configuración de RMS.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Compruebe si el servicio de base de datos está detenido.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Instale las actualizaciones de software necesarias para su servidor de base de datos. Cuando se le pida una contraseña, utilice la misma contraseña que especificó durante la instalación.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Reinicie el equipo. Compruebe si el servicio de base de datos está iniciado.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Compruebe si las cuentas de usuario tienen atributos de dirección de correo electrónico válidos en Active Directory.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Compruebe si el usuario de dominio que administrará RMS (y establecerá servicios en línea para la certificación raíz y los servidores de licencia) tiene los permisos de servidor de base de datos requeridos. Si utiliza SQL Server como servidor de base de datos, puede agregar un identificador de inicio de sesión para el usuario que está utilizando el complemento <strong>Administrador corporativo de SQL Server</strong>. En el complemento, expanda el servidor y el grupo de servidor y, a continuación, expanda el elemento <strong>Seguridad</strong>. Haga clic en el elemento <strong>Inicios de sesión</strong>, agregue un nuevo inicio de sesión para la cuenta de dominio del usuario, haga clic en la ficha <strong>Funciones del servidor</strong> y, a continuación, seleccione la casilla de verificación <strong>Administradores de servidor</strong>.</p></td>
<td style="border:1px solid black;"><p>Importante: Todos los usuarios y grupos que utilizan RMS para adquirir licencias y publicar contenido deben tener una dirección de correo electrónico que esté configurada en el complemento Usuarios y grupos de Active Directory de MMC, en la ficha <strong>General</strong> de <strong>Propiedades</strong> del usuario.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Conexión a Internet</p>
<p>(opcional)</p></td>
<td style="border:1px solid black;"><p>Compruebe si el explorador y el servidor (incluidas las configuraciones requeridas de servidor proxy), TCP/IP y LMHOSTS/HOSTS están configurados correctamente para obtener acceso a Internet. Para comprobarlo, vaya a http://uddi.microsoft.com. Si puede abrir esta página, RMS puede conectarse al servicio de inscripción de Microsoft.</p></td>
<td style="border:1px solid black;"><p>Vaya a http://uddi.microsoft.com para comprobar el acceso a Internet.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Actualizaciones de software</p></td>
<td style="border:1px solid black;"><p>Descargue e instale las actualizaciones más recientes para el software que está instalado en este equipo (incluidas las últimas actualizaciones de Windows de www.microsoft.com).</p></td>
<td style="border:1px solid black;"><p>Descargue e instale siempre las actualizaciones de servicios más recientes.</p></td>
</tr>  
</tbody>  
</table>
  
Una vez que haya seguido todos los pasos anteriores, ya puede realizar la configuración inicial (incluida la instalación de software como requisito previo) en los equipos que ejecutarán RMS.
