---
TOCTitle: Servicio de certificación preliminar de RMS
Title: Servicio de certificación preliminar de RMS
ms:assetid: '09957294-167f-4f98-88e9-ae90fbeb26c1'
ms:contentKeyID: 18127720
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720191(v=WS.10)'
---

Servicio de certificación preliminar de RMS
===========================================

El servicio de certificación preliminar sólo se ejecuta en el clúster raíz de RMS. Este servicio habilita a un servidor para solicitar un certificado de cuenta de permisos en nombre de un usuario, y puede utilizarse para desarrollar aplicaciones personalizadas. Algunos ejemplos que usan este servicio son Microsoft Exchange Server 2007 y Microsoft Office SharePoint Server 2007.

El archivo de aplicación del servicio de certificación preliminar, Precertification.asmx, está ubicado en el directorio virtual Certification, que se encuentra en IIS.

Para obtener más información sobre el desarrollo de aplicaciones personalizadas, consulte la documentación de tecnología de Servicios de Windows Rights Management en MSDN Library [http://go.microsoft.com/fwlink/?LinkId=32972](http://go.microsoft.com/fwlink/?linkid=32972).

La lista de control de acceso predeterminada de este servicio se muestra en la siguiente tabla:

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Usuario o grupo</th>
<th>Permiso predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Control total</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Grupo de servicio RMS</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SYSTEM</td>
<td style="border:1px solid black;">Control total</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
</tbody>
</table>
