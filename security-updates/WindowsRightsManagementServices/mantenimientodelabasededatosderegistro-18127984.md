---
TOCTitle: Mantenimiento de la base de datos de registro
Title: Mantenimiento de la base de datos de registro
ms:assetid: 'de55058b-0d1a-4997-8a45-e14678ddd13f'
ms:contentKeyID: 18127984
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747691(v=WS.10)'
---

Mantenimiento de la base de datos de registro
=============================================

Las entradas de registro también incluyen copias de las licencias emitidas para diversas operaciones de RMS, como la inscripción de usuarios o la asignación de licencias de usuario. En el peor de los casos (en el que todas las entradas de registro son una inscripción de usuario correcta o un intento correcto de adquirir una licencia de uso) cada entrada de registro añadirá unos 200 KB al tamaño de la base de datos de registro.

Por ejemplo, supongamos que un mensaje de correo electrónico protegido con RMS se ha enviado a todos los empleados de una compañía con 50.000 usuarios y que todos los empleados lo abren. Si cada uno de los empleados abre el mensaje de correo electrónico en un período de un día, la base de datos de registro crecerá unos 10 GB. Es posible configurar el servicio de escucha para que no registre los datos XrML, lo cual reducirá la cantidad de información registrada.

Considere crear comandos para archivar la información antigua de la base de datos de registro en una base de datos secundaria. Podrá encontrar ejemplos de comandos de registro en el kit de herramientas de RMS, que está disponible como descarga gratuita en el [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=26724) (http://go.microsoft.com/fwlink/?LinkId=26724).

Variables que afectan al crecimiento de la base de datos de registro
--------------------------------------------------------------------

Predecir el tamaño de una base de datos de registro depende del entorno. Pueden predecirse numerosas entradas de "inicio" dentro del registro, entre las cuales:

-   Inscripción del servidor de RMS
-   Inscripción de usuario (una única solicitud para cada equipo utilizado por cada usuario)
-   Solicitudes de usuario automatizadas para certificados de publicación sin conexión

El volumen de entradas en la base de datos de registro después de las entradas iniciales depende de la emisión de licencias de uso para contenido protegido. Hay varias condiciones que afectan al crecimiento de esta base de datos:

-   Se requiere una licencia nueva cada vez que un usuario obtiene acceso a contenido protegido. Este no es el método predeterminado para documentos protegidos, sino una configuración opcional. Si elige implementar este requisito, sus bases de datos crecerán a un ritmo más rápido.
-   Número previsto de mensajes de correo electrónico protegidos que recibirá cada persona al día.
-   Número previsto de usuarios únicos que leerán estos mensajes de correo electrónico protegidos.
-   Número previsto de documentos protegidos de Microsoft Office 2003 (Word, PowerPoint y Excel) producidos por persona al día.
-   Destinatarios previstos de los documentos protegidos.

El tamaño inicial de la base de datos de registro será de 1,7 MB aproximadamente, incluida la solicitud de un certificado del servidor de RMS. Cada vez que se inscribe un usuario nuevo, éste obtiene un certificado de cuenta de permisos (RAC) y un certificado emisor de licencias de cliente (CLC). Se registran estas dos acciones, y entre las dos aumentan la base de datos en 0,06 MB. Cada vez que un usuario adquiere correctamente una licencia para contenido protegido, la base de datos crece en 0,19 MB.

Para saber cómo funciona esta estimación, supongamos que una organización de 5.000 usuarios implementa RMS para uso de todos. Cada usuario tiene un equipo, y la organización utiliza dos servidores de RMS. Después de la implementación, cada usuario crea por término medio un mensaje de correo electrónico protegido con RMS al día, y lo envía a cinco usuarios. Cada usuario crea también un documento protegido con RMS al día, al que obtienen acceso tres usuarios más. En la siguiente tabla, se muestra una estimación de cómo esta actividad aumenta el tamaño de la base de datos de registro.

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
<th>Acción</th>
<th>Crecimiento del registro</th>
<th>Tamaño acumulativo del registro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Se han establecido correctamente los servicios en línea del servidor de RMS</p></td>
<td style="border:1px solid black;"><p>1,7 MB</p></td>
<td style="border:1px solid black;"><p>1,7 MB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Se inscriben 5.000 empleados (5.000*0,06)</p></td>
<td style="border:1px solid black;"><p>300 MB</p></td>
<td style="border:1px solid black;"><p>301,7 MB</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mensajes de correo electrónico protegidos a los que se ha obtenido acceso (25.000*0,19)</p></td>
<td style="border:1px solid black;"><p>4.750 MB</p></td>
<td style="border:1px solid black;"><p>5.051,7 MB</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Documentos protegidos a los que se ha obtenido acceso (15.000*0,19)</p></td>
<td style="border:1px solid black;"><p>2.850 MB</p></td>
<td style="border:1px solid black;"><p>7.901,7 MB</p></td>
</tr>  
</tbody>  
</table>
  
Por lo tanto, después de la inscripción, la base de datos de registro tiene un tamaño estático de aproximadamente 300 MB. No obstante, el crecimiento diario en este ejemplo es de 7,6 GB, cerca del límite de 8 GB de la instalación predeterminada de los Servicios de Message Queue Server. Si la base de datos de registro dejara de estar disponible durante un periodo superior a un día, empezarían a perderse entradas de registro.
  
Control del tamaño de la base de datos de registro  
--------------------------------------------------
  
El plan de implementación debe incluir un método para administrar la base de datos de registro. A continuación se muestran los métodos más habituales.
  
-   **Eliminar y archivar**  
    Este método consiste en utilizar comandos de SQL Server para archivar la información seleccionada de la base de datos de registro en una base de datos secundaria una vez las entradas de registro alcanzan cierta antigüedad. También implica filtrar las bases de datos de información irrelevante para que no se desperdicie el espacio.  
-   **Limitar la información registrada**  
    La base de datos de registro está formada por tres tablas principales. Una de ellas es **DRMS\_Log\_Filter**, que identifica qué campo de la tabla principal deberá registrarse cuando esté habilitado el filtrado de registro.  
    Las entradas de tabla activado/desactivado dictan qué campos de la tabla principal registra el servicio de escucha de registro en el servidor de RMS. Dos de estos campos (relacionados con XrML) ya se han establecido en 0 para deshabilitar el registro, ya que estos dos campos suponen aproximadamente un 99% del tamaño de cada una de las filas de solicitud de licencia.  
    Otra tabla de la base de datos **DRMS\_Config\_ServerName\_Port**, llamada **DRMS\_ClusterPolicies**, contiene un **PolicyName** de **LoggingFiltering**. **LoggingFiltering** no está habilitado de forma predeterminada. Si establece el valor de **LoggingFiltering** en 1 y reinicia el servicio de escucha de registro, el crecimiento diario de la base de datos en el ejemplo anterior caería de 7,6 GB cada día a aproximadamente 160 MB cada día.  
-   **Traslado de la base de datos de registro**  
    Otra opción para administrar una base de datos de registro creciente es simplemente trasladarla a un servidor con más espacio en disco. La base de datos de registro puede existir en un servidor de base de datos distinto que la base de datos de configuración. Para trasladar la base de datos a un servidor diferente, siga estos pasos:  
    1.  Detenga el servicio de escucha de registro de cada servidor de RMS.  
    2.  Copie la base de datos (o cree una nueva) en un servidor diferente.  
    3.  Edite la base de datos **DRMS\_Config\_ServerName\_Port** de RMS seleccionando la tabla **DRMS\_ClusterPolicies** y modificando los valores de **LoggingDatabaseName** (nombre del servidor de base de datos) y **LoggingDatabaseServer** (nombre de la base de datos).  
    4.  Reinicie IIS ejecutando IISRESET.exe desde la línea de comandos.
