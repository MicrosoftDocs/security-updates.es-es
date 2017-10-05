---
TOCTitle: Información general del sistema RMS
Title: Información general del sistema RMS
ms:assetid: 'cbd14635-e17e-42b8-9fd8-6fdce42ffe07'
ms:contentKeyID: 18127960
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747671(v=WS.10)'
---

Información general del sistema RMS
===================================

En este tema se proporciona información sobre cómo funcionan conjuntamente los servicios Web de RMS y las tecnologías de cliente de RMS en un sistema RMS.

En la tabla siguiente se muestran los tipos de servidores que intervienen en una implementación de RMS y se describen sus funciones. Para obtener información detallada sobre la implementación, vea "Implementación de un sistema RMS", en esta recopilación de documentación.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Servidor o clúster</th>
<th style="border:1px solid black;" >Función</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Certificación raíz</td>
<td style="border:1px solid black;">Ejecuta los siguientes servicios de RMS:
<ul>
<li><strong>Subinscripción</strong>. Subinscribe servidores de licencias.<br />
<br />
</li>
<li><strong>Proxy de activación</strong>. Actúa como un proxy de Internet para solicitudes de clientes de cajas de seguridad y certificados de equipo de RMS.<br />
<br />
</li>
<li><strong>Certificación</strong>. Emite certificados de cuenta de permisos.<br />
<br />
</li>
<li><strong>Publicación</strong>. Emite licencias de publicación.<br />
<br />
</li>
<li><strong>Licencias</strong>. Emite licencias de uso.<br />
<br />
</li>
</ul>
En todas las instalaciones se deberá contar al menos con un servidor o clúster de certificación raíz. Sólo puede haber un clúster de certificación raíz en cada bosque de Active Directory.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Licencias (opcional)</td>
<td style="border:1px solid black;">Ejecuta los siguientes servicios de RMS:
<ul>
<li><strong>Publicación</strong>. Emite licencias de publicación.<br />
<br />
</li>
<li><strong>Licencias</strong>. Emite licencias de uso.<br />
<br />
</li>
</ul>
Con frecuencia, los servidores de licencias se implementan para cubrir las necesidades de pequeños departamentos o para descargar solicitudes de licencias del clúster de certificación raíz. Los servidores de licencias son opcionales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de base de datos, como SQL Server</td>
<td style="border:1px solid black;"><ul>
<li>Ejecuta las bases de datos de configuración, registro y servicios de directorio de RMS.<br />
<br />
</li>
<li>Almacena certificados de cuenta de permisos en la base de datos de configuración del clúster de certificación raíz.<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Controlador de dominio y catálogo global</td>
<td style="border:1px solid black;"><ul>
<li>Proporciona autenticación de usuarios y servicios de directorio.<br />
<br />
</li>
<li>Almacena la ubicación de detección de servicios del clúster de certificación raíz.<br />
<br />
</li>
</ul></td>
</tr>
</tbody>
</table>
 

RMS utiliza los servicios de subinscripción y de activación alojados por Microsoft para proporcionar una raíz común de confianza al sistema. Para obtener más información, vea "[Jerarquía de confianza de RMS](https://technet.microsoft.com/2d44182f-a653-4383-aba1-dade53f7cf9a)", más adelante en este tema.

En el diagrama siguiente se muestran los diferentes componentes de un sistema RMS y sus funciones en el sistema. Las flechas representan las solicitudes y respuestas que circulan entre los distintos componentes.

![](images/Cc747671.29138741-d45c-459b-8ead-b9bc3f708dd5(WS.10).gif)

Para obtener más información sobre cada componente, vea "[Componentes de software de RMS](https://technet.microsoft.com/e38a840e-f390-48fd-8354-50108a64f5ca)", más adelante en este tema.
