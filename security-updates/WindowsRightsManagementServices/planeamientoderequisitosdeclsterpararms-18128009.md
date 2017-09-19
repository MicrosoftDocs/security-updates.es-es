---
TOCTitle: Planeamiento de requisitos de clúster para RMS
Title: Planeamiento de requisitos de clúster para RMS
ms:assetid: 'ec4023eb-4d39-4551-9789-c8a2d973a55b'
ms:contentKeyID: 18128009
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747792(v=WS.10)'
---

Planeamiento de requisitos de clúster para RMS
==============================================

Si utiliza RMS en una implementación de clúster, asegúrese de tener en cuenta cómo tratar las siguientes condiciones que se pueden dar en la organización.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Condición</th>
<th>Recomendación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Un gran número de escritorios utilizan RMS.</p></td>
<td style="border:1px solid black;"><p>Puede utilizar Windows Update, una secuencia de comandos o un método de distribución de software como Systems Management Server (SMS) o Directiva de grupo para instalar y activar el software de cliente de los Servicios de Microsoft Windows Rights Management.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Gran número de solicitudes de clientes.</p></td>
<td style="border:1px solid black;"><p>Utilice un servidor de equilibrio de carga, el servicio de equilibrio de carga (NLB) o equilibrio de carga de hardware para distribuir las solicitudes por el clúster.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Dos adaptadores de red que utilizan direcciones IP virtuales para prestar servicio a solicitudes de la extranet y de la intranet.</p></td>
<td style="border:1px solid black;"><p>Asegúrese de que todo registro de DNS que se haga para exponer la dirección IP virtual a la extranet también se hace para exponer la dirección a la intranet.</p>
<p>Si no se realiza el registro de DNS para la intranet, no se aceptarán las solicitudes internas de licencia de uso. Si no puede modificar los registros de recursos de DNS, puede modificar la tabla de hosts de cada servidor del clúster para asignar la URL del clúster a la dirección IP virtual del clúster. Debe realizarse el registro de DNS antes de establecer los servicios en línea de RMS. Si ya ha establecido servicios en línea de RMS, debe anularlos y repetir el proceso de establecimiento.</p></td>
</tr>
</tbody>
</table>
