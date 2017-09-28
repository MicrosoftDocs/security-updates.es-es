---
TOCTitle: Servicio de subinscripción de RMS
Title: Servicio de subinscripción de RMS
ms:assetid: '6b05e71c-5e7d-467c-9e13-35ac14d3718a'
ms:contentKeyID: 18127835
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720289(v=WS.10)'
---

Servicio de subinscripción de RMS
=================================

El servicio de subinscripción sólo se ejecuta en el clúster raíz de RMS. Este servicio responde a las solicitudes de certificados emisores de licencias de servidor que envían los servidores de clústeres de sólo licencias durante el establecimiento de servicios en línea.

El archivo de aplicación del servicio de subinscripción, SubEnrollService.asmx, se encuentra en el directorio virtual Certification *sitio\_Web\_RMS*\\\_wmcs\\Certification\\, donde *sitio\_Web\_RMS* se reemplaza por el nombre del sito Web en el que haya establecido los servicios en línea de RMS.

De forma predeterminada, el acceso a este servicio está restringido a la cuenta del SISTEMA local. Para poner en servicio e inscribir un servidor subordinado en un clúster de sólo licencias, la cuenta de usuario del administrador del servidor de licencias se debe agregar a la lista de control de acceso discrecional (DACL) de SubEnrollService.asmx con privilegios de control totales.

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
<td style="border:1px solid black;">SYSTEM</td>
<td style="border:1px solid black;">Control total</td>
</tr>
</tbody>
</table>
