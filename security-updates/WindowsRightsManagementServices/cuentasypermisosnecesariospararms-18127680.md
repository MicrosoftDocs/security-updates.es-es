---
TOCTitle: Cuentas y permisos necesarios para RMS
Title: Cuentas y permisos necesarios para RMS
ms:assetid: '07a51daa-6823-41e6-b453-92f1a0592361'
ms:contentKeyID: 18127680
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720178(v=WS.10)'
---

Cuentas y permisos necesarios para RMS
======================================

En la siguiente tabla, se especifican los permisos de usuario necesarios para llevar a cabo acciones específicas de RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Actividad</th>
<th>Cuenta de usuario y permisos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Instalación de RMS</p></td>
<td style="border:1px solid black;"><p>Iniciar sesión con una cuenta de dominio que es miembro del grupo Administradores local.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Establecimiento de los servicios en línea de RMS</p></td>
<td style="border:1px solid black;"><p>Iniciar sesión con una cuenta de dominio que es miembro del grupo Administradores local. Además, la cuenta que se utiliza debe tener un inicio de sesión de SQL con la función de administrador del sistema en la base de datos de SQL Server, para que RMS pueda configurar las bases de datos.</p>
<p>Durante el establecimiento de servicios en línea, debe especificar la cuenta de servicio de RMS, que ya debe haber creado. Debe ser una cuenta de usuario de dominio estándar sin permisos adicionales. Esta cuenta se convierte en miembro del grupo de servicio de RMS y es la cuenta en la que se ejecutará RMS durante el funcionamiento normal.</p>
<p>Para implementaciones de un solo servidor en las que la base de datos reside en el mismo equipo que el servidor de certificación raíz, puede especificar de forma alternativa la cuenta del sistema local. No obstante, por motivos de seguridad, se recomienda especificar siempre la cuenta de servicio de RMS en lugar de la cuenta del sistema local. Cuando la base de datos se encuentra en un servidor diferente, debe especificar la cuenta de servicio de RMS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Administración de RMS</p></td>
<td style="border:1px solid black;"><p>Iniciar sesión con una cuenta de dominio que es miembro del grupo Administradores local. Puede personalizar la configuración de seguridad para administrar el acceso a las páginas Web de administración.</p></td>
</tr>
</tbody>
</table>
  
| ![](images/Cc720178.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                |  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| La cuenta utilizada para iniciar sesión en el servidor de RMS no requiere que se pertenezca a ningún grupo de dominio adicional, como Administradores del dominio. Sin embargo, algunas tareas administrativas específicas, como el registro del punto de conexión de servicio y la modificación de directivas de seguridad, requieren una cuenta que tenga privilegios adicionales. |
