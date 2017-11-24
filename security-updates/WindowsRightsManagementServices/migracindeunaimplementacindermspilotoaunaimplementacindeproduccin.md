---
TOCTitle: Migración de una implementación de RMS piloto a una implementación de producción
Title: Migración de una implementación de RMS piloto a una implementación de producción
ms:assetid: 'ea151946-22fb-4cba-a3ef-fd7a4bf0d292'
ms:contentKeyID: 18128002
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747789(v=WS.10)'
---

Migración de una implementación de RMS piloto a una implementación de producción
================================================================================

Muchas organizaciones prefieren realizar una implementación piloto de RMS antes de implementar la tecnología en la organización. El programa piloto suele tener un número limitado de usuarios, y un administrador dedicado puede mantener localmente el servidor en lugar de formar parte de un centro de datos mantenido por un grupo de informática. Cuando la organización implementa RMS en el centro de datos para todos los clientes una vez completada la implementación piloto, se implementan nuevos servidores de RMS a fin de admitir el mayor número de posibles usuarios.

No obstante, el contenido protegido con RMS está vinculado al servidor de RMS que se utilizó para crearlo, por lo que si se quita o reemplaza un servidor, deberán seguirse los pasos necesarios para que el contenido que se cifró utilizando los servidores de RMS piloto pueda descifrarse y obtener licencia con los servidores de RMS de producción.

Si ha implementado RMS como programa piloto y desea trasladar el servidor de RMS al entorno de producción de la organización y, además, mantener la integridad del contenido protegido con el servidor de RMS piloto, deberá crear un plan de migración que garantice una transición fluida y que permita volver al programa piloto en caso necesario para recuperar datos.

Los pasos siguientes se indican como ejemplo de algunos de los elementos que debe incluir un plan de migración; es posible que su implementación tenga requisitos adicionales.

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
<th style="border:1px solid black;" >Servidor</th>
<th style="border:1px solid black;" >Paso</th>
<th style="border:1px solid black;" >Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Piloto</td>
<td style="border:1px solid black;">Realice una copia de seguridad de la base de datos de configuración de RMS.</td>
<td style="border:1px solid black;">Esto le permitirá restaurar el servidor piloto en caso necesario.
La base de datos de configuración incluye la clave privada de RMS.
Asegúrese de saber la contraseña de la clave privada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Piloto</td>
<td style="border:1px solid black;">Si utilizó un módulo de seguridad de hardware (HSM) para proteger la clave privada de RMS, realice una copia de seguridad del HSM siguiendo las indicaciones del fabricante.</td>
<td style="border:1px solid black;">Así restaurará el HSM en el nuevo servidor.
Asegúrese de tener todos los componentes necesarios para instalar y configurar el HSM.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Piloto</td>
<td style="border:1px solid black;">Exporte el archivo de dominio de publicación de confianza.</td>
<td style="border:1px solid black;">Esto permite que otro servidor de RMS pueda descifrar licencias de publicación creadas por este servidor y emitir licencias de uso para el contenido protegido.
El dominio de publicación de confianza incluye el certificado emisor de licencias de servidor, la clave privada de RMS y las plantillas de directiva de permisos que haya establecido este servidor.
El archivo de dominio de publicación de confianza es un archivo XML cifrado con una contraseña segura que se especifica al crear el archivo. También deberá tener esta contraseña para importar el archivo de dominio de publicación de confianza.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Piloto</td>
<td style="border:1px solid black;">Exporte el dominio de usuario de confianza.</td>
<td style="border:1px solid black;">Esto permite a otro servidor de RMS conceder licencias de uso a los usuarios cuyos certificados de cuenta de permisos (RAC) habían sido concedidos por el servidor de RMS piloto.
El dominio de usuario de confianza se establece importando el certificado emisor de licencias de servidor de este servidor al otro servidor de RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Prepare el nuevo servidor para que sea el servidor de certificación raíz.</td>
<td style="border:1px solid black;">Asegúrese de que puede obtener acceso al servidor de base de datos, así como de que IIS y Message Queue Server estén instalados.
Si es posible, utilice el mismo nombre de servidor para este servidor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Si utiliza un HSM, instálelo y restaure la configuración a partir de la copia de seguridad que creó en el servidor piloto.</td>
<td style="border:1px solid black;">Establece las credenciales necesarias para descifrar la clave privada de RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Instale RMS.</td>
<td style="border:1px solid black;">RMS comprobará que todos los servicios que son requisitos previos estén instalados y configurados correctamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Establezca los servicios en línea de RMS utilizando una clave privada nueva. Si utiliza la inscripción en línea, su servidor se inscribirá durante el proceso de establecimiento de servicios en línea utilizando Internet para conectarse al servicio de inscripción de Microsoft. Si no dispone de conexión a Internet desde este servidor, deberá utilizar la inscripción sin conexión.</td>
<td style="border:1px solid black;">Si el nombre de este servidor es diferente del nombre del servidor piloto, podrá modificar la configuración de la dirección URL de clúster para que sea la misma dirección URL que la del servidor piloto.
Si no lo hace, deberá configurar un redireccionamiento de la dirección URL de clúster anterior a la nueva dirección URL de clúster para permitir que los usuarios con contenido preexistente puedan obtener licencias de uso.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Si utiliza la inscripción sin conexión, complete el proceso de inscripción manual para el nuevo servidor de RMS. Para obtener más información, vea “Para inscribir manualmente un servidor de certificación raíz” en “Operación de un servidor RMS” en esta recopilación de documentación.</td>
<td style="border:1px solid black;">El servidor de RMS no se puede utilizar hasta que se haya inscrito.
Además, no es posible obtener acceso a las páginas de administración de RMS hasta que se haya inscrito el servidor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Importe el archivo de dominio de publicación de confianza que exportó en el paso 3.</td>
<td style="border:1px solid black;">La cuenta de servicio de RMS debe tener permisos de lectura para la ubicación donde está almacenado el archivo a fin de que el archivo se importe correctamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Vuelva a firmar cada una de las plantillas importadas con el dominio de publicación de confianza.</td>
<td style="border:1px solid black;">Las plantillas están firmadas con la clave privada del servidor. Dado que este servidor tiene una clave privada nueva, para que sean válidas, las plantillas deben volver a firmarse. Para obtener más información, vea “Para volver a firmar una plantilla de directiva de permisos” en “Operación de un servidor RMS” en esta recopilación de documentación.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Redistribuya las plantillas a los equipos cliente que participaron en la implementación piloto.</td>
<td style="border:1px solid black;">Es preciso quitar las viejas plantillas y reemplazarlas por las plantillas firmadas por este servidor.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Producción</td>
<td style="border:1px solid black;">Importe el archivo de dominio de usuario de confianza que exportó en el paso 4.</td>
<td style="border:1px solid black;">Permite utilizar certificados emisores de licencias de cliente y RAC antiguos.
Si se están moviendo cuentas de usuario entre bosques como parte de esta migración, tenga en cuenta que las cuentas deben tener proxy SMTP coincidentes.</td>
</tr>
</tbody>
</table>
 

Cuando haya terminado de configurar el servidor de producción, compruebe que los usuarios piloto pueden seguir creando y leyendo correo previamente protegido. Luego podrá agregar al clúster tantos servidores de RMS como necesite para admitir el número de usuarios de su organización.
