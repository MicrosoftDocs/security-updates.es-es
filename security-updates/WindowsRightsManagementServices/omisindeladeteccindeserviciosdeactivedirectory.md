---
TOCTitle: Omisión de la detección de servicios de Active Directory
Title: Omisión de la detección de servicios de Active Directory
ms:assetid: '9d97e7fb-5b05-4853-ad7b-6cc82b9729f0'
ms:contentKeyID: 18127944
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747614(v=WS.10)'
---

Omisión de la detección de servicios de Active Directory
========================================================

Los servicios y los clientes de RMS descubren las ubicaciones de servicio con la búsqueda en primer lugar en el Registro local. Si determinadas claves del Registro no tienen un valor, los servicios y los clientes de RMS buscan en Active Directory el punto de conexión de servicio (SCP). Esto significa que puede anular la configuración de descubrimiento de Active Directory predeterminado si escribe determinadas claves en el Registro del servidor o del cliente.

> [!NOTE]
> Si el clúster raíz de RMS está configurado de un modo que el SCP no se publique en Active Directory, puede usar estas claves para dirigir los clientes de RMS a la ubicación correcta. 

En esta sección se describen las entradas del Registro y se proporcionan detalles acerca de cómo crearlas.

Anulación del descubrimiento de servicios para la subinscripción de clúster de sólo licencias
---------------------------------------------------------------------------------------------

Si está realizando el aprovisionamiento de un clúster de sólo licencias y desea subinscribirlo con un clúster raíz distinto del clúster raíz que ha implementado en el bosque de Active Directory del clúster de sólo licencias, debe anular el descubrimiento de los servicios de subinscripción y de certificación de cuentas.

#### Descripciones de las entradas del Registro

Las siguientes entradas del Registro se usan para anular los servicios de subinscripción y de certificación de cuentas.

-   **SubEnrollmentURL**. Esta entrada especifica la ruta de acceso al clúster raíz que el servidor de licencias usa al solicitar su certificado de emisor de licencias.
-   **GicURL**. Esta entrada especifica la ruta de acceso al servicio de certificación de cuentas para este clúster de sólo licencias.

#### Detalles de la entrada

En los equipos que ejecutan la versión de 32 bits de Windows Server 2003, la ruta de acceso completa a la subclave del Registro de las entradas de descubrimiento de servicios para la subinscripción de clúster de sólo licencias es:

**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DRMS\\1.0**

En los equipos que ejecutan la versión de 64 bits de Windows Server 2003, la ruta de acceso completa a la subclave del Registro de las entradas de descubrimiento de servicios para la subinscripción de clúster de sólo licencias es:

**HKEY\_LOCAL\_MACHINE\\SoftwareWOW6432Node\\Microsoft\\DRMS\\1.0**

En la siguiente tabla se enumeran las entradas que puede agregar para anular el descubrimiento de servicios.

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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo</th>
<th style="border:1px solid black;" >valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">SubEnrollmentURL</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">http(o https)://<em>nombre_de_servidor</em>/_wmcs/certification/subenrollservice.asmx</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GicURL</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">http(o https)://<em>nombre_de_servidor</em>/_wmcs/certification/certification.asmx</td>
</tr>
</tbody>
</table>
  
Anulación del descubrimiento de servicios en el cliente para la publicación  
---------------------------------------------------------------------------
  
Si los usuarios van a publicar contenido desde sus equipos, puede anular las ubicaciones de los servidores usadas para la publicación según la topología empleada en su empresa. Las ubicaciones de los servidores usados para la publicación normalmente las descubre el cliente con Active Directory. Al agregar las claves del Registro adecuadas en los equipos cliente, los clientes omitirán estos métodos y, en su lugar, usarán las direcciones URL que especifique en el valor de entrada del Registro.
  
> [!NOTE]
> Las anulaciones enumeradas en estas secciones se deben crear como claves y no como entradas individuales. El valor de estas claves se debe crear en la entrada predeterminada de cada clave.
  
#### Descripciones de las claves del Registro
  
Las siguientes claves del Registro se pueden usar para anular el descubrimiento automático del clúster de RMS.
  
-   **Activation**. Esta clave del Registro define la dirección URL del servicio de activación de equipo. Si ejecuta el cliente de RMS con Service Pack 1 o posterior, esta entrada del Registro ya no se usa.  
-   **EnterprisePublishing**. Esta clave del Registro define la dirección URL de una instalación de RMS que desea que use este cliente para las solicitudes de licencia.  
-   **CloudPublishing**. Esta clave del Registro define la dirección URL del servicio de licencias hospedado por Microsoft que se puede usar si el cliente no tiene acceso a una instalación de RMS pero sí a Internet.
  
#### Detalles de la clave
  
La ruta de acceso completa a la subclave del Registro para las entradas de descubrimiento de servicios en el cliente es:
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MSDRM\\ServiceLocation\\**
  
En la siguiente tabla se enumeran las claves del Registro que puede agregar en un equipo cliente de RMS para anular el descubrimiento de servicios.
  
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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo</th>
<th style="border:1px solid black;" >valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Activation</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">http(o https)://<em>nombre_del_clúster_RMS</em>/_wmcs/Certification donde <em>nombre_del_clúster_RMS</em> es el nombre del clúster de RMS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">EnterprisePublishing</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">http(o https)://<em>nombre_del_clúster_RMS</em>/_wmcs/Licensing donde <em>nombre_del_clúster_RMS</em> es el nombre del clúster de RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CloudPublishing</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">http(o https)://<em>nombre_de_clúster_completo</em>/_wmcs/Licensing donde <em>nombre_de_clúster_completo</em> es el nombre de dominio completo del clúster de RMS.</td>
</tr>
</tbody>
</table>
  
Se recomienda implementar estas claves del Registro con Systems Management Server o Directiva de grupo para garantizar que todos los clientes de la empresa usan los servidores de publicación correctos.
  
> [!CAUTION]
> La modificación incorrecta del Registro puede dañar gravemente el sistema. Antes de realizar cambios en el Registro, debe hacer una copia de seguridad de los datos de valor que contenga el equipo. 
  
Se puede usar un archivo de Registro de ejemplo (.reg) para importar las claves del Registro adecuadas en cada servidor del clúster de RMS.
  
**Para importar las claves del Registro adecuadas en cada servidor del clúster de RMS**  
1.  Copie el siguiente archivo de Registro de ejemplo en Bloc de notas.
  
    `Windows Registry Editor Version 5.00`
  
    `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation]`
  
    `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\Activation]`
  
    `@="http://<RMS_cluster_name>/_wmcs/certification"`
  
    `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing]`
  
    `@="http://<RMS_cluster_name>/_wmcs/licensing"`
  
2.  Reemplace &lt;RMS\_cluster\_name&gt; por el nombre de su clúster de RMS.
  
3.  Guarde el archivo con la extensión de nombre de archivo .reg.
  
4.  Haga doble clic en el nombre del archivo en el Explorador de Windows.
  
5.  Si aparece el cuadro de diálogo **Control de cuentas de usuario**, confirme que la acción que muestra es la que desea y, a continuación, haga clic en **Continuar**.. Cuando aparezca una solicitud en la que se le pregunta si desea agregar la información al Registro, haga clic en **Sí**.
