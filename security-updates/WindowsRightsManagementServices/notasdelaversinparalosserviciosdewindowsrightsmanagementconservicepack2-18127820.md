---
TOCTitle: Notas de la versión para los Servicios de Windows Rights Management con Service Pack 2
Title: Notas de la versión para los Servicios de Windows Rights Management con Service Pack 2
ms:assetid: '78067886-681f-49a6-b43d-bfd08a369b69'
ms:contentKeyID: 18127820
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747637(v=WS.10)'
---

Notas de la versión para los Servicios de Windows Rights Management con Service Pack 2
======================================================================================

*Fecha de edición: Diciembre de 2006*

Antes de comenzar
-----------------

Revise la siguiente información antes de instalar los Servicios de Microsoft® Windows® Rights Management (RMS) con Service Pack 2 (SP2). La información contenida en estas notas de la versión se aplica al servidor de RMS con SP2 y no al cliente de RMS. Para obtener información sobre clientes de RMS, consulte Servicios de Rights Management ([http://go.microsoft.com/fwlink/?LinkId=68637](http://go.microsoft.com/fwlink/?linkid=68637)).

#### Requisitos del sistema

Los requisitos de hardware para ejecutar RMS con SP2 se indican en la siguiente tabla.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Requisito</th>
<th style="border:1px solid black;" >Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Equipo con un procesador III (800 MHz o superior)</td>
<td style="border:1px solid black;">Equipo con dos procesadores Pentium 4 (1500 MHz o superiores)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">256 MB de RAM</td>
<td style="border:1px solid black;">512 MB de RAM</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">20 GB de espacio libre en el disco duro</td>
<td style="border:1px solid black;">40 GB de espacio libre en el disco duro</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747637.note(WS.10).gif)Nota                                                                          |  
|------------------------------------------------------------------------------------------------------------------------------------------------|  
| El servidor de RMS con SP2 se ha diseñado para un equipo de 32 bits. Si se instala en un equipo de 64 bits, se ejecutará en modo de emulación. |
  
Los requisitos software para los servidores en los que se ejecuta RMS con SP2 se indican en la siguiente tabla.
  
###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Componente</th>
<th style="border:1px solid black;" >Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sistema operativo</td>
<td style="border:1px solid black;">Microsoft Windows Server® 2003, excepto Web Edition, para RMS con SP2.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicios de Rights Management con SP2</td>
<td style="border:1px solid black;">Debe instalarse RMS con Service Pack 1 (SP1) antes de poder realizar una actualización a RMS con SP2. Este requisito no está presente para el cliente de RMS con SP2.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sistema de archivos</td>
<td style="border:1px solid black;">Se recomienda el sistema de archivos NTFS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Componentes obligatorios previos</td>
<td style="border:1px solid black;"><ul>
<li>Message Queue Server (también conocido como MSMQ) con servicio de integración de directorio Active Directory® habilitado.<br />
<br />
</li>
<li>Servicios de Internet Information Server (IIS) con ASP.NET habilitado.<br />
<br />
</li>
<li>Microsoft .NET Framework 1.1<br />
<br />
</li>
</ul></td>
</tr>
</tbody>
</table>
 

| ![](images/Cc747637.note(WS.10).gif)Nota                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Si configura RMS con SP2 para permitir la administración remota, en el equipo conectado al servicio de administración de RMS con SP2 debe utilizarse Internet Explorer 6.0 o superior. |

Los requisitos de infraestructura para los servidores en los que se ejecuta RMS con SP2 se indican en la siguiente tabla.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Componente</th>
<th style="border:1px solid black;" >Requisitos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicios de directorio</td>
<td style="border:1px solid black;">Active Directory en controladores de dominio en los que se ejecute Windows Server 2000 con Service Pack 3 o posterior, en el mismo dominio en que está instalado RMS. Todos los usuarios y grupos que utilizan RMS para adquirir licencias y publicar contenido deben tener una dirección de correo electrónico que esté configurada en Active Directory.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de base de datos</td>
<td style="border:1px solid black;">RMS con SP2 necesita una base de datos y procedimientos almacenados para realizar operaciones. Puede utilizar Microsoft SQL Server™ 2000 con SP3 o posterior, o bien Microsoft SQL Server 2005. Para realizar pruebas o implementación en un solo equipo, puede utilizarse Microsoft SQL Server Desktop Engine (MSDE 2000) versión A o Microsoft SQL Server 2005 Express Edition.</td>
</tr>
</tbody>
</table>
  
RMS se ha diseñado y probado para servidores de base de datos en los que se ejecuta Microsoft SQL Server 2000 y Microsoft SQL Server 2005. RMS puede ejecutarse en otros servidores de base de datos si reúnen los siguientes criterios:
  
-   Compatibilidad con las interfaces ADO.NET proporcionadas por Microsoft .NET Framework 1.1.  
-   Cumplir con Transact-SQL, el lenguaje de consultas estructurado utilizado por Microsoft SQL Server, ya que lo utilizan las secuencias de comandos de inicialización y los procedimientos almacenados de RMS.  
-   Compatibilidad con las extensiones específicas de Microsoft SQL Server.  
-   Responder a llamadas de método del espacio de nombres System.Data.SqlClient de .NET Framework.  
-   Proporcionar la funcionalidad correspondiente del espacio de nombres System.Data.SqlClient.  
-   Utilizar el modo de autenticación de Windows.
  
Para averiguar si el servidor de base de datos reúne estos requisitos, póngase en contacto con el correspondiente distribuidor de base de datos.
  
En la siguiente tabla se muestran los permisos de usuario necesarios para realizar diferentes actividades con RMS.
  
###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Actividad</th>
<th style="border:1px solid black;" >Requisitos de cuenta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Instalación de RMS</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Establecimiento de un clúster raíz de RMS</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local y búsqueda y escritura en Active Directory</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Establecimiento de un clúster de RMS de sólo licencia</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local y búsqueda en Active Directory</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Establecimiento al utilizar una nueva base de datos con configuración nueva</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local y lectura, escritura y creación en el equipo en que se ejecuta SQL Server</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Establecimiento al utilizar una base de datos con configuración existente</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local y lectura, y escritura en el equipo en que se ejecuta SQL Server</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administración de RMS</td>
<td style="border:1px solid black;">Usuario del dominio con credenciales de administrador del equipo local</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747637.note(WS.10).gif)Nota                                                                                                                                                                                                                             |  
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Para obtener más información sobre la configuración de Windows Server, Active Directory, Message Queuing, IIS y los sistemas de archivos, consulte el sitio Web TechCenter de Windows Server 2003 ([http://go.microsoft.com/fwlink/?LinkId=78135](http://go.microsoft.com/fwlink/?linkid=78135)). |
  
Si utiliza RMS en una implementación de clúster, tenga en cuenta los elementos que se indican en la tabla siguiente.
  
###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Condición</th>
<th style="border:1px solid black;" >Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Gran número de escritorios en los que se utilizará RMS</td>
<td style="border:1px solid black;">Utilice Systems Management Server (SMS) o una directiva de grupo para instalar el cliente de RMS con SP2.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Gran número de solicitudes de clientes</td>
<td style="border:1px solid black;">Utilice un servidor de equilibrio de carga, el servicio de equilibrio de carga de red del sistema operativo Windows Server o el equilibrio de carga de hardware para distribuir las solicitudes por el clúster.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Dos adaptadores de red que utilizan la dirección IP virtual para prestar servicio a solicitudes de la extranet y de la intranet</td>
<td style="border:1px solid black;">Asegúrese de que cualquier registro de Domain Name System (DNS) que exponga la dirección IP virtual a la extranet también exponga la dirección a la intranet.</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747637.Important(WS.10).gif)Importante                                                                                                                                                                                                                                                                                                                                                                                                                                                              |  
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Si no se realiza el registro de DNS para la intranet, no se aceptarán las solicitudes internas de licencia de cliente. Si no puede modificar la configuración de DNS, es posible modificar la tabla de hosts de cada servidor del clúster para asignar la dirección URL del clúster a la dirección IP virtual del clúster. Debe realizarse el registro de DNS antes de establecer los servicios en línea de RMS. Si ya ha establecido el servicio, deberá eliminar RMS del servidor y, a continuación, repetir el proceso de establecimiento. |
  
#### Clientes compatibles con esta versión
  
El cliente de RMS sin Service Pack, el cliente de RMS con SP1 o el cliente de RMS con SP2 se pueden instalar en cualquier equipo que ejecute Microsoft Windows 2000, Windows XP y Windows Server 2003. Esta versión no admite versiones anteriores de sistemas operativos de Windows.
  
| ![](images/Cc747637.Caution(WS.10).gif)Precaución                                                         |  
|----------------------------------------------------------------------------------------------------------------------------------------|  
| Si usa el cliente de RMS sin Service Pack, el cliente no podrá usar la publicación en línea en un servidor de RMS con SP1 o posterior. |
  
Cambios en la funcionalidad  
---------------------------
  
Hay varias funciones nuevas en RMS con SP2:
  
-   [Expansión de grupos entre bosques mejorada](#bkmk_cif1)  
-   [Cambios en el registro de base de datos](#bkmk_cif2)  
-   [Tamaños de lotes de servidor más grandes](#bkmk_cif3)  
-   [Compatibilidad con Microsoft SQL Server 2005](#bkmk_cif4)
  
<span id="BKMK_CIF1"></span>
#### Expansión de grupos entre bosques mejorada
  
#### ¿Para que sirve esta función?
  
En RMS, la expansión de grupos entre bosques facilita la posibilidad de que RMS expanda la pertenencia universal a grupos de Active Directory en un bosque diferente donde las pertenencias a grupo no se replican entre dos bosques. Cuando un usuario de un bosque envía contenido con permisos protegidos a un usuario de otro bosque, RMS atraviesa un período de descubrimiento en el que verifica que el usuario tiene acceso al contenido. Este procedimiento de verificación se realiza por medio de una consulta LDAP de un bosque a otro con el fin de encontrar el punto de conexión del servicio (SCP) RMS del bosque remoto. Cuando se descubre el SCP del bosque remoto, la cuenta del servicio RMS envía una solicitud a la canalización de expansión de grupos. La solicitud pregunta al bosque remoto si un usuario es miembro de un grupo.
  
#### ¿A quién se aplica esta función?
  
Esta función nueva es de interés para clientes de RMS en un entorno de Active Directory de varios bosques cuyas pertenencias universales de grupo no se replican entre bosques.
  
#### ¿Por qué es importante este cambio?
  
El nuevo protocolo de expansión de confianza de bosque mejorará la fiabilidad para los clientes que estén implementando un entorno de Active Directory de varios bosques.
  
#### ¿Cuál es la diferencia?
  
Con anterioridad a RMS con SP2, la expansión de grupos entre bosques se llevaba a cabo realizando llamadas remotas mediante .NET. En esta versión, el protocolo de expansión de grupos entre bosques se ha cambiado a un servicio Web de ASP.NET que utiliza solicitudes SOAP/HTTP a la canalización de expansión de grupos de confianza del bosque.
  
| ![](images/Cc747637.note(WS.10).gif)Nota                                                                                                                                                                                                                                   |  
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Para la compatibilidad con versiones anteriores, se mantiene la compatibilidad con las llamadas remotas de .NET en RMS con SP2. Sin embargo, para sacar el máximo partido del nuevo protocolo de expansión de grupos entre bosques, en todos los clústeres de RMS debe ejecutarse al menos RMS con SP2. |
  
#### ¿Qué opciones de configuración se han añadido o modificado en RMS con SP2?
  
La nueva canalización de expansión de grupos de RMS se ha configurado con los valores predeterminados más seguros en RMS con SP2, donde sólo disponen de acceso los grupos locales de administradores y servicio de RMS. Para obtener acceso a una cuenta, debe modificar la lista de control de acceso en la canalización de expansión de grupos que se encuentra en wwwroot\\\_wmcs\\GroupExpansion\\GroupExpansion.asmx.
  
| ![](images/Cc747637.Important(WS.10).gif)Importante                                                                                                                                                                                                                                                                                                                                                                   |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Compruebe que la cuenta de servicio de RMS de cada bosque de Active Directory tiene acceso a la canalización de expansión de grupos en cada servidor de RMS del clúster. Si no existe acceso para las cuentas, se producirán errores en la expansión de grupos. Si lo desea, puede crear la misma cuenta en cada bosque y asignarles la misma contraseña. En este caso, sólo debería añadir dicha cuenta a la canalización de expansión de grupos. |
  
Se han añadido nuevos sucesos a RMS con SP2 para informarle de mensajes de problemas que no se incluyeron en el servicio de Message Queue Server. En estos registros de sucesos se incluyen sucesos para notificarle cuando un mensaje no puede firmarse digitalmente o validarse. Entre varios casos de problemas de validación se incluye un mensaje incorrecto, la falta de un algoritmo hash o una firma o un algoritmo hash incorrectos.
  
<span id="BKMK_CIF2"></span>
#### Cambios en el registro de base de datos
  
#### ¿Para que sirve esta función?
  
RMS utiliza un servicio de escucha de registros que envía toda la comunicación de RMS a la base de datos de registro mediante Message Queue Server. El clúster de RMS envía mensajes a Message Queue Server y el servicio de escucha de registros los recupera de Message Queue Server y los escribe en la base de datos de registro.
  
#### ¿A quién se aplica esta función?
  
Esta función se aplica a los usuarios actuales de RMS que utilizan el servicio de escucha de registro de RMS y a los nuevos usuarios de RMS con SP2 que se están planteando utilizar el servicio de escucha de registro de RMS.
  
#### ¿Por qué es importante este cambio?
  
En versiones anteriores de RMS, la cola de registro de RMS se protegía mediante el uso de listas de control de acceso, pero no se permitía la autenticación. Sin autenticación, un usuario malintencionado podría escribir mensajes erróneos en la cola de registro de RMS.
  
#### ¿Cuál es la diferencia?
  
En RMS con SP2, se proporciona autenticación adicional en los mensajes transmitidos mediante el clúster de RMS utilizando Message Queue Server. Además de las listas de control de acceso que previenen el acceso no autorizado a la cola de mensajes, la cola de Message Queue Server también está protegida mediante un mecanismo de autenticación de mensajes. Cuando se envía un mensaje a Message Queue Server, las canalizaciones de RMS generan un algoritmo hash del mensaje y lo firman digitalmente mediante la clave privada del clúster de RMS. El servicio de escucha de registro calcula primero su propio algoritmo hash del mensaje y lo compara con el que se incluye en el mensaje. Si los algoritmos coinciden, el servicio de escucha de registro verifica la firma utilizando la clave pública del clúster y el algoritmo hash en el mensaje. Si se verifican los algoritmos hash y la firma, el mensaje se envía a la base de datos de registro. Si se producen errores en los pasos de validación, el mensaje se elimina permanentemente de la cola de Message Queue Server y se escribe una advertencia de suceso en el registro de la aplicación del Visor de sucesos.
  
#### ¿Qué opciones de configuración se han añadido o modificado en RMS con SP2?
  
Se añaden a RMS con SP2 los nuevos sucesos diseñados para indicar los mensajes de problemas que no se incluyeron en la cola de Message Queue Server. Dichos eventos se escriben en el registro de la aplicación e incluyen mensajes que no se pueden firmar digitalmente o las firmas digitales del mensaje que no se pueden validar. Entre varios casos de problemas de validación se incluye un mensaje incorrecto, la falta de un algoritmo hash o una firma o un algoritmo hash incorrectos.
  
<span id="BKMK_CIF3"></span>
#### Tamaños de lotes de servidor más grandes
  
#### ¿Para que sirve esta función?
  
Los procesos por lotes en RMS aumentan el rendimiento al permitir que se envíen varias solicitudes de licencia al clúster de RMS como una única solicitud, en lugar de realizar una solicitud para cada licencia.
  
#### ¿A quién se aplica esta función?
  
La compatibilidad de tamaños de lotes de servidor más grandes resulta de interés para las aplicaciones con RMS habilitado para las que es necesario adquirir varias licencias de una sola vez para contenido con permisos protegidos.
  
#### ¿Por qué es importante este cambio?
  
Los procesos por lotes de RMS permiten que se realice una única solicitud a la canalización de adquisición de licencias de RMS con el fin de obtener licencias de usuario para varios certificados de cuenta de permisos (RAC) frente a una o más licencias de publicación. Sin un tamaño de proceso por lotes mayor de 1, la aplicación con RMS habilitado tendría que solicitar individualmente una licencia de uso para cada usuario.
  
#### ¿Cuál es la diferencia?
  
En versiones de RMS anteriores a RMS con SP2, el clúster RMS admitía un tamaño de procesos por lotes máximo de 1. Si el tamaño máximo del proceso por lotes se establecía en un número mayor de 1, el clúster lo ignoraba. En RMS con SP2, el tamaño máximo puede ser 100.
  
| ![](images/Cc747637.note(WS.10).gif)Nota        |  
|------------------------------------------------------------------------------|  
| Sólo la canalización AcquireLicense de RMS admite las solicitudes por lotes. |
  
Se ha mejorado el informe de errores en RMS con SP2 para las cuentas con solicitudes por lotes. Por ejemplo, si envía un lote de diez solicitudes y se producen errores en la segunda y la tercera, se escribe un suceso en el registro de sucesos por cada error.
  
<span id="BKMK_CIF4"></span>
#### Compatibilidad con Microsoft SQL Server 2005
  
#### ¿Para que sirve esta función?
  
En RMS con SP2, Microsoft SQL Server 2005 puede utilizarse como servidor de base de datos para admitir la configuración de RMS y las bases de datos de registro sin realizar ninguna configuración adicional.
  
#### ¿A quién se aplica esta función?
  
La compatibilidad de Microsoft SQL Server 2005 con RMS con SP2 resulta de interés para los usuarios de RMS que deseen utilizar Microsoft SQL Server 2005 como base de datos de RMS.
  
#### ¿Por qué es importante este cambio?
  
En versiones anteriores de RMS, los tipos de datos de algunos de los parámetros utilizados en la tabla de mensajes de sistema eran incompatibles con las especificaciones del formato Microsoft SQL Server 2005. Para obtener más información, consulte el artículo 913372 en Microsoft Knowledge Base ([http://go.microsoft.com/fwlink/?LinkId=68638](http://go.microsoft.com/fwlink/?linkid=68638)).
  
#### ¿Cuál es la diferencia?
  
En versiones de RMS anteriores a RMS con SP2, las sentencias SQL RAISERROR se utilizaban para notificar al usuario de RMS que se había producido un error. La sentencia RAISERROR consulta la tabla de mensajes del sistema para recuperar los mensajes de error de RMS almacenados en la misma. RMS con SP2 utiliza una técnica diferente para propagar los errores de SQL de modo que ya no hay una dependencia de la tabla de mensajes del sistema.
  
| ![](images/Cc747637.note(WS.10).gif)Nota                                                                                                                                                                                                                                                 |  
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Si está realizando una actualización de RMS con SP1 a RMS con SP2, ya no se consultan los mensajes de error en la tabla de mensajes del sistema, pero los mensajes de error permanecen en dicha tabla. Una instalación partiendo de cero de RMS con SP2 no añade entradas nuevas en la tabla de mensajes del sistema. |
  
Problemas conocidos  
-------------------
  
En las secciones siguientes se tratan los problemas conocidos de esta versión de RMS.
  
#### El archivo de Ayuda aún hace referencia a RMS con Service Pack 1
  
El archivo de Ayuda incluido en la instalación de RMS con SP2 aún hace referencia a RMS con SP1. Para obtener información sobre clientes de RMS con SP2, consulte Servicios de Rights Management ([http://go.microsoft.com/fwlink/?LinkId=68637](http://go.microsoft.com/fwlink/?linkid=68637)).
  
#### Windows Update no puede instalar el cliente de RMS con SP2 en equipos basados en x64 o Itanium
  
Si el cliente de RMS o RMS con SP1 se instala en un equipo basado en x64 y se intenta actualizar el cliente a RMS con SP2 (x64) desde Windows Update, se producirá un error en la instalación. Aunque los clientes de RMS anteriores, creados para sistemas de 32 bits, funcionaban en equipos basados en x64, no pueden actualizarse al cliente de RMS con SP2 (x64). Debe desinstalar primero el cliente de RMS anterior y, a continuación, iniciar de nuevo la actualización. Windows Update detecta la versión del sistema operativo y proporciona el cliente de RMS con SP2 adecuado. Lo mismo sucede con respecto a los equipos basados en arquitectura Itanium.
  
#### El restablecimiento siempre produce errores al iniciar al servicio de escucha de registro
  
Cuando se anula el establecimiento del clúster, el servicio de escucha de registro no abandona el servicio en estado de detención. Para detener por completo el servicio, debe reiniciar el equipo.
  
#### No se puede eliminar un dominio de publicación de confianza no basado en software
  
Después de importar un dominio de publicación de confianza con una implementación de clave privada no basada en software, no es posible eliminarlo. La importación de una clave privada no basada en software no debe realizarse desde la consola de administración de Servicios de Windows Rights Management. Póngase en contacto con el distribuidor de hardware adecuado para obtener instrucciones sobre cómo exportar e importar la clave privada.
  
#### Microsoft .NET Framework 2.0 cambia las raíces virtuales de IIS cuando está instalado en el servidor de RMS
  
RMS con SP2 utiliza la asignación de secuencia de comandos ASP.NET que se incluye con la versión 1.1 de .NET Framework. La asignación que proporcionan versiones posteriores no es compatible con RMS con SP2. Sin embargo, ambas versiones pueden coexistir sin interferencias con otras aplicaciones dependientes. Si el servidor tiene instalado .NET Framework 1.1 y .NET Framework 2.0 o posterior, aunque la instalación y el establecimiento de servicios en línea de RMS con SP2 parezcan haberse completado satisfactoriamente, es posible que el servidor de RMS no funcione correctamente. Esto ocurre porque las raíces virtuales de RMS deben registrarse con la versión 1.1 de la asignación de secuencia de comandos ASP.NET y no con la versión 2.0. Para registrar las raíces virtuales de RMS con la versión 1.1 de la asignación de script ASP.NET, ejecute el comando siguiente en el símbolo del sistema:
  
**%windir%\\Microsoft.NET\\Framework\\v1.1.4322&gt;aspnet\_regiis.exe -s W3SVC/1/ROOT/\_wmcs**
  
Si se ejecuta este comando, se registrarán correctamente las raíces virtuales de RMS, y RMS con SP2 podrá ejecutarse en el servidor.
  
#### Puede faltar la pertenencia a grupos si se utiliza el nivel funcional nativo de Windows 2000 de Active Directory
  
Al implementar RMS en un entorno donde los niveles de la infraestructura de Active Directory se han elevado al nivel funcional nativo de Windows 2000, puede que RMS no pueda leer el atributo memberOf de los objetos de Active Directory al intentar ampliar la pertenencia a grupos de las listas de distribución ocultas. Para que los RMS pueda leer el atributo memberOf, la cuenta de servicio de RMS debe utilizar una cuenta de dominio que sea miembro del grupo Acceso compatible con versiones anteriores de Windows 2000. Para obtener información, consulte el artículo 812841 de Microsoft Knowledge Base ([http://go.microsoft.com/fwlink/?LinkId=78152](http://go.microsoft.com/fwlink/?linkid=78152)).
  
#### El servicio de escucha de registro envía mensajes de Message Queue Server a la cola de mensajes con problemas de entrega cuando no se puede acceder a la base de datos
  
Hay instancias (por ejemplo, base de datos desconectada, problemas de conectividad en red, etc.) en las que el servicio de escucha de registro no puede conectarse con la base de datos. En este caso, los mensajes se envían a una cola de mensajes con problemas de entrega. El único modo de recuperar estos mensajes (es decir, enviarlos a la base de datos de registro) es utilizar la herramienta de recuperación de mensajes de RMS que se incluye con el juego de herramientas de administración de RMS. Para descargar el juego de herramientas de administración de RMS, consulte [http://go.microsoft.com/fwlink/?LinkId=33841](http://go.microsoft.com/fwlink/?linkid=33841).
  
| ![](images/Cc747637.note(WS.10).gif)Nota                                                                                                                                                                      |  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Recover y RecoverandPurge se han eliminado de LogRecoveryCmd. De este modo, se asegura que todos los mensajes se redirigen a través del servicio de Message Queue Server y se autentican antes de enviarse a la base de datos de registro. |
  
#### Debe actualizar RMS con SP2 antes de actualizar Microsoft SQL Server 2005
  
Al realizar la actualización a RMS con SP2 y de Microsoft SQL Server 2000 a Microsoft SQL Server 2005, asegúrese de actualizar RMS primero. De este modo se evitarán problemas de compatibilidad con la actualización de Microsoft SQL Server.
  
#### RMS con SP2 no se puede establecer en los sitios Web cuyo nombre contenga un apóstrofe (')
  
Si intenta establecer servicios en línea de RMS con SP2 en un sitio Web cuyo nombre incluye un carácter de apóstrofe ('), se producirá un error en el proceso de establecimiento de servicios en línea y aparecerá el mensaje de error "**Parámetro no válido**". Para establecer RMS con SP2 en el sitio Web, elimine el apóstrofe del nombre del mismo.
  
#### Habilitación de la versión 1.1 de ASP.NET en servidores con una versión de 64 bits de Windows Server 2003
  
En el tema "Requisitos del sistema" de la ayuda de RMS se explica cómo instalar .NET Framework 1.1 y cómo habilitar ASP.NET 1.1 tras instalar los Servicios de Internet Information Server (IIS). Sin embargo, si .NET Framework 1.1 se ha instalado antes que IIS, ASP.NET 1.1, no aparecerá en las extensiones del servicio Web y el procedimiento documentado no será útil. Si IIS se ha instalado después de instalar .NET Framework 1.1, ejecute el comando siguiente en el símbolo del sistema para habilitar ASP.NET:
  
**%SystemRoot%\\Microsoft.NET\\Framework\\v1.1.4322\\aspnet\_regiis.exe -i –enable**
  
Al utilizar una versión de .NET Framework posterior a 1.1, sustituya **-i** por **-ir** en este comando para evitar restablecer cualquier asignación de secuencias de comando de IIS existentes.
  
#### La cuenta de servicio de RMS de bosque remoto debe añadirse a la canalización de ampliación de grupos local
  
Se ha solucionado un problema de seguridad que elimina BUILTIN\\users de ACL en la canalización de ampliación de grupos. Esto puede hacer que se descomponga la ampliación de grupos en los distintos bosques. Para solucionar este problema, siga estos pasos:
  
**Añada la cuenta del servicio RMS al bosque remoto**  
1.  En Forest1, donde Forest1 es el clúster raíz de RMS en el primer bosque, vaya a inetpub\\wwwroot\\\_wmcs.
  
2.  Haga clic con el botón derecho en la carpeta **GroupExpansion** y, a continuación, seleccione **Propiedades**.
  
3.  En la ventana **Propiedades de GroupExpansion**, haga clic en la pestaña **Seguridad**, añada la entrada para *Forest2\\RmsServiceAccount* (por ejemplo, rmil31\\rmsvc), donde Forest2 es el clúster raíz de RMS en el segundo bosque.
  
4.  Haga clic en **Aceptar**.
  
5.  Haga clic en **Ejecutar**, introduzca **iisreset** y, a continuación, haga clic en**Aceptar**.
  
#### La actualización de .NET Framework puede producir pérdida de datos
  
Si la versión 1.1 de .NET Framework (CLR) se actualiza después de instalar y establecer RMS, las raíces virtuales están configuradas para utilizar la versión 2.0 de .NET Framework. Si esto sucede, no se registra ningún dato en la base de datos de registro. Esto tendrá como resultado la pérdida de datos. Realice una de las siguientes acciones:
  
-   Actualice .NET Framework antes de instalar y establecer RMS.  
-   Restablezca las raíces virtuales de modo que utilicen la versión 1.1 después de actualizar .NET Framework.
  
Cambios en la documentación de esta versión  
-------------------------------------------
  
A continuación se presenta una lista de temas que se han modificado en esta versión:
  
-   Para confiar en certificados de cuenta de permisos basados en Passport ([http://go.microsoft.com/fwlink/?LinkId=70369](http://go.microsoft.com/fwlink/?linkid=70369))  
-   Requisitos de software para RMS ([http://go.microsoft.com/fwlink/?LinkId=70371](http://go.microsoft.com/fwlink/?linkid=70371))  
-   Como implementar el cliente de RMS ([http://go.microsoft.com/fwlink/?LinkId=70373](http://go.microsoft.com/fwlink/?linkid=70373))  
-   Instalación de RMS desde el símbolo del sistema ([http://go.microsoft.com/fwlink/?LinkId=70374](http://go.microsoft.com/fwlink/?linkid=70374))  
-   Tablas principales de la base de datos de configuración de RMS ([http://go.microsoft.com/fwlink/?LinkId=70375](http://go.microsoft.com/fwlink/?linkid=70375))  
-   Tablas principales de la base de datos de configuración de RMS ([http://go.microsoft.com/fwlink/?LinkId=70376](http://go.microsoft.com/fwlink/?linkid=70376))  
-   Tablas de la base de datos de registro de RMS ([http://go.microsoft.com/fwlink/?LinkId=70377](http://go.microsoft.com/fwlink/?linkid=70377))  
-   Evaluación de requisitos de escala [http://go.microsoft.com/fwlink/?LinkId=70378](http://go.microsoft.com/fwlink/?linkid=70378))  
-   Protección de la implementación de RMS ([http://go.microsoft.com/fwlink/?LinkId=70379](http://go.microsoft.com/fwlink/?linkid=70379))  
-   Habilitación del servicio de retiro ([http://go.microsoft.com/fwlink/?LinkId=70380](http://go.microsoft.com/fwlink/?linkid=70380))  
-   Planificación de usuarios externos de RMS [http://go.microsoft.com/fwlink/?LinkId=70381](http://go.microsoft.com/fwlink/?linkid=70381))  
-   Habilitación de la compatibilidad del servidor de RMS con dispositivos móviles y servicios de servidor ([http://go.microsoft.com/fwlink/?LinkId=70382](http://go.microsoft.com/fwlink/?linkid=70382))
  
#### Copyright
  
*La información que contiene este documento representa la visión actual de Microsoft Corporation sobre los temas tratados en la fecha de publicación. Dado que Microsoft debe responder a las condiciones cambiantes del mercado, no debe interpretarse como compromiso por parte de Microsoft, y Microsoft no puede garantizar la precisión de cualquier información presentada después de la fecha de publicación.*
  
*Este documento tiene únicamente fines informativos. MICROSOFT NO OTORGA NINGUNA GARANTÍA, EXPLÍCITA, IMPLÍCITA O ESTATUTARIA, A LA INFORMACIÓN INCLUIDA EN ESTE DOCUMENTO.*
  
*Es responsabilidad del usuario el cumplimiento de todas las leyes de derechos de autor aplicables. Sin limitar los derechos correspondientes de acuerdo con la ley de derechos de autor, ninguna parte de este documento puede ser reproducida, almacenada ni introducida en un sistema de recuperación, ni transmitida de ninguna forma, por ningún medio (ya sea electrónico, mecánico, mediante fotocopias, grabación u otros) y con ningún propósito sin la previa autorización por escrito de Microsoft Corporation.*
  
*Microsoft puede ser titular de patentes o tener solicitudes de patentes, marcas comerciales, derechos de autor y otros derechos sobre la propiedad intelectual acerca del contenido de este documento. La difusión del mismo no le otorga ninguna licencia sobre estas patentes, marcas comerciales, derechos de autor ni otros derechos sobre la propiedad intelectual, a menos que se indique por escrito en un contrato de licencia de Microsoft.*
  
*A menos que se indique lo contrario, los nombres de las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y eventos mencionados en los ejemplos son ficticios y no se pretende indicar, ni debe deducirse, ninguna asociación con compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares o eventos reales.*
  
*© 2006 Microsoft Corporation. Reservados todos los derechos.*
  
*Active Directory, Microsoft, MS-DOS, Visual Studio, Windows, Windows Server, SQL Server y Windows NT son marcas registradas o marcas comerciales de Microsoft Corporation en Estados Unidos y otros países.*
  
*Los nombres de compañías y productos reales mencionados en este documento pueden ser marcas comerciales de sus respectivos propietarios.*
