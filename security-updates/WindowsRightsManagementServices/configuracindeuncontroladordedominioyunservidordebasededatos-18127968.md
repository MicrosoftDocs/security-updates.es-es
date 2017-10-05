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

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Componente de infraestructura</th>
<th style="border:1px solid black;" >Pasos para configurar un controlador de dominio y un servidor de base de datos</th>
<th style="border:1px solid black;" >Notas para la implementación en un entorno de producción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sistema operativo</td>
<td style="border:1px solid black;">En un equipo que cumple con los requisitos de hardware de RMS pero que todavía no está conectado a la red, instale Windows 2000 Server con SP3 o posterior o Windows Server 2003. Utilice el sistema de archivos NTFS de la partición.</td>
<td style="border:1px solid black;">Se recomienda encarecidamente que instale siempre el Service Pack y las actualizaciones más recientes. Utilice particiones con formato NTFS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conexión de red</td>
<td style="border:1px solid black;">Realice una conexión a una red que proporcione acceso a Internet pero que esté aislada del entorno de producción.</td>
<td style="border:1px solid black;">La conexión a Internet debe poseer un servidor de seguridad adecuado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Dirección IP</td>
<td style="border:1px solid black;">Asigne una dirección IP estática a este equipo.</td>
<td style="border:1px solid black;">Utilice siempre direcciones IP estáticas para los servidores.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Active Directory</td>
<td style="border:1px solid black;">Inicie sesión como administrador local.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Haga clic en <strong>Inicio</strong>, haga clic en <strong>Ejecutar</strong>, escriba <code>dcpromo</code> en el cuadro <strong>Abrir</strong> y por último haga clic en <strong>Aceptar</strong>.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Cuando aparezca el asistente para la instalación de Active Directory, siga los pasos del asistente para crear un nuevo dominio en un bosque nuevo y aceptar las opciones predeterminadas, excepto las opciones siguientes:
Especifique el nombre del dominio, por ejemplo, contoso.com.
Permita que el asistente configure DNS en el equipo.
Seleccione <strong>Permisos compatibles sólo con servidores Windows 2000</strong> si todos los controladores de dominio se ejecutan en Windows 2000 o posterior.
Proporcione una contraseña segura para el administrador local.</td>
<td style="border:1px solid black;">Si se necesitan nuevos dominios para implementar RMS, configúrelos en Active Directory.
Utilice siempre contraseñas seguras para todas las cuentas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Reinicie el equipo cuando lo solicite el sistema.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Para comprobar el nivel funcional, abra el complemento <strong>Usuarios y equipos de Active Directory</strong> haciendo clic con el botón secundario en el nombre de dominio y después en <strong>Propiedades</strong>, y compruebe la configuración del cuadro <strong>Modo de operación del dominio</strong>. Si no existen controladores de dominio anteriores a los de Windows 2000, haga clic en <strong>Cambiar el modo</strong> para que el dominio funcione en <strong>Modo nativo</strong>.
Nota: En Windows Server 2003, la opción <strong>Modo de operación del dominio</strong> se reemplaza con <strong>Nivel funcional del dominio</strong>.</td>
<td style="border:1px solid black;">Para conseguir una seguridad y una manejabilidad óptimas, no debe utilizar el nivel funcional mixto de Windows 2000 para la compatibilidad de RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cuentas de usuario</td>
<td style="border:1px solid black;">Cree una cuenta de usuario de dominio para utilizarla como cuenta de servicio de RMS para RMS, como por ejemplo ContosoRMS@contoso.com. Especifique una contraseña segura. Asegúrese de especificar una dirección de correo electrónico para el usuario. Si no se especifica la dirección de correo electrónico en Active Directory, el usuario no podrá obtener licencias y certificados de RMS.
Nota: La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS.</td>
<td style="border:1px solid black;">Debe crear una cuenta independiente en Active Directory para que la utilice la cuenta de servicio de RMS. Incluya una dirección de correo electrónico. No otorgue a la cuenta ningún permiso especial.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQL Server 2000</td>
<td style="border:1px solid black;">Inicie sesión en el servidor en el que desee instalar la base de datos. Si se trata del mismo servidor que el controlador de dominio, debe iniciar sesión como administrador de dominio.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Siga las instrucciones proporcionadas por el software de base de datos para instalar el software del servidor de base de datos.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Utilice procedimientos recomendados de servidor para instalar el servidor de base de datos, como por ejemplo:
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
<td style="border:1px solid black;">Debe utilizar un modo Autenticación de Windows integrado. Si no puede ejecutar el servidor de base de datos en este modo, póngase en contacto con el administrador de dominio y con el administrador de servidor de base de datos para determinar qué cambios pueden requerirse en la configuración de RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Compruebe si el servicio de base de datos está detenido.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Instale las actualizaciones de software necesarias para su servidor de base de datos. Cuando se le pida una contraseña, utilice la misma contraseña que especificó durante la instalación.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Reinicie el equipo. Compruebe si el servicio de base de datos está iniciado.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Compruebe si las cuentas de usuario tienen atributos de dirección de correo electrónico válidos en Active Directory.</td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Compruebe si el usuario de dominio que administrará RMS (y establecerá servicios en línea para la certificación raíz y los servidores de licencia) tiene los permisos de servidor de base de datos requeridos. Si utiliza SQL Server como servidor de base de datos, puede agregar un identificador de inicio de sesión para el usuario que está utilizando el complemento <strong>Administrador corporativo de SQL Server</strong>. En el complemento, expanda el servidor y el grupo de servidor y, a continuación, expanda el elemento <strong>Seguridad</strong>. Haga clic en el elemento <strong>Inicios de sesión</strong>, agregue un nuevo inicio de sesión para la cuenta de dominio del usuario, haga clic en la ficha <strong>Funciones del servidor</strong> y, a continuación, seleccione la casilla de verificación <strong>Administradores de servidor</strong>.</td>
<td style="border:1px solid black;">Importante: Todos los usuarios y grupos que utilizan RMS para adquirir licencias y publicar contenido deben tener una dirección de correo electrónico que esté configurada en el complemento Usuarios y grupos de Active Directory de MMC, en la ficha <strong>General</strong> de <strong>Propiedades</strong> del usuario.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Conexión a Internet
(opcional)</td>
<td style="border:1px solid black;">Compruebe si el explorador y el servidor (incluidas las configuraciones requeridas de servidor proxy), TCP/IP y LMHOSTS/HOSTS están configurados correctamente para obtener acceso a Internet. Para comprobarlo, vaya a http://uddi.microsoft.com. Si puede abrir esta página, RMS puede conectarse al servicio de inscripción de Microsoft.</td>
<td style="border:1px solid black;">Vaya a http://uddi.microsoft.com para comprobar el acceso a Internet.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Actualizaciones de software</td>
<td style="border:1px solid black;">Descargue e instale las actualizaciones más recientes para el software que está instalado en este equipo (incluidas las últimas actualizaciones de Windows de www.microsoft.com).</td>
<td style="border:1px solid black;">Descargue e instale siempre las actualizaciones de servicios más recientes.</td>
</tr>
</tbody>
</table>
  
Una vez que haya seguido todos los pasos anteriores, ya puede realizar la configuración inicial (incluida la instalación de software como requisito previo) en los equipos que ejecutarán RMS.
