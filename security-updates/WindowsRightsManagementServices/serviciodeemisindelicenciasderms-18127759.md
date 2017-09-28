---
TOCTitle: Servicio de emisión de licencias de RMS
Title: Servicio de emisión de licencias de RMS
ms:assetid: '5cad1baf-0304-4e82-b62d-83a4aac2140b'
ms:contentKeyID: 18127759
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720278(v=WS.10)'
---

Servicio de emisión de licencias de RMS
=======================================

El servicio de licencias, que emite licencias de publicación, se ejecuta en el clúster raíz de RMS y en cualquier clúster de sólo licencias. Las licencias de uso permiten a los usuarios usar contenido protegido con derechos.

El archivo de aplicación del servicio de emisión de licencias, License.asmx, está ubicado en el directorio virtual Licensing, que se encuentra en IIS.

| ![](images/Cc720278.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Se puede implementar un clúster de sólo licencias independiente para descargar solicitudes de licencia del clúster raíz. Asimismo, es posible implementar un servidor o clúster de licencias independiente para un departamento, de forma que éste pueda, por ejemplo, establecer sus propias directivas de permisos. Para obtener más información acerca de estas consideraciones, consulte "Identificación de los componentes principales" en "RMS: planeamiento y arquitectura" en esta recopilación de documentación. |

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
