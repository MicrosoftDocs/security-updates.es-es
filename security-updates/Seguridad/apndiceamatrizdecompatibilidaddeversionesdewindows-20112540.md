---
TOCTitle: 'Apéndice A: Matriz de compatibilidad de versiones de Windows'
Title: 'Apéndice A: Matriz de compatibilidad de versiones de Windows'
ms:assetid: 'bcdf1e01-a054-4bd4-bd6c-eb9b2df03e7c'
ms:contentKeyID: 20112540
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458718(v=TechNet.10)'
---

Apéndice A: Matriz de compatibilidad de versiones de Windows
============================================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

### Introducción

En la tabla de este apéndice se muestra el estado de distintas versiones de sistema operativo Microsoft® Windows® de cliente y servidor. En la tabla se muestra la función del sistema en la guía de la solución para *Seguridad en LAN inalámbricas con Servicios de Certificate Server*, las distintas versiones de sistema operativo que se pueden utilizar en dicha función y el estado de compatibilidad para cada sistema operativo. En la columna final de la tabla se incluyen notas explicativas o precauciones adicionales.

El estado de compatibilidad de cada función de servidor se clasifica como uno de los siguientes:

-   **Compatible y probado**: la versión de sistema operativo se ha utilizado en el laboratorio de prueba de Microsoft Solutions for Security (MSS) para generar la solución y se ha probado que funciona como parte de la solución.

-   **Compatible**: la versión de sistema operativo no se ha probado como parte de la solución, pero Microsoft admite su uso en esta función. Es posible que tenga que efectuar operaciones de configuración o personalización adicionales aparte de la guía incluida con esta solución.

-   **No compatible**: la versión de sistema operativo no funcionará en la solución del modo descrito. Es posible configurar el sistema no compatible para que funcione correctamente, pero es muy probable que hacerlo implique un esfuerzo considerable.

-   **Desconocido**: la versión de sistema operativo puede funcionar en esta función (no hay motivos técnicos para que no lo haga), pero asegurarse de que funcionará dependerá de su propia comprobación y pruebas.

Donde una versión de sistema operativo no se muestre en una función, no funcionará (**No compatible**) o se desconoce si funcionará (**Desconocido**).

**Tabla A.1: Estado de compatibilidad de las versiones de sistema operativo de la solución**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Función</p></th>
<th><p>Versión del sistema operativo</p></th>
<th><p>Estado</p></th>
<th><p>Notas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Cliente inalámbrico</p></td>
<td style="border:1px solid black;"><p>-Windows XP Professional</p>
<p>-Windows XP Professional Tablet Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Microsoft Windows 2000</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p>Se necesita obtener el cliente 802.1X de Microsoft.com.</p>
<p>Los certificados de usuario se implementan manualmente o mediante secuencias de comandos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>-Microsoft Windows NT® versión 4.0</p>
<p>-Windows 9<em>x</em></p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p>Se necesita obtener el cliente 802.1X mediante soporte técnico Premier.</p>
<p>Los certificados se implementan manualmente o mediante secuencias de comandos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Otras plataformas</p></td>
<td style="border:1px solid black;"><p>Desconocido</p></td>
<td style="border:1px solid black;"><p>Los clientes necesitan admitir 802.1X y el protocolo EAP – TLS (Protocolo de autenticación extensible - Protocolo de seguridad de la capa de transporte).</p>
<p>Los certificados se implementan manualmente o mediante secuencias de comandos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Entidad emisora de certificados (CA) raíz</p></td>
<td style="border:1px solid black;"><p>Microsoft Windows Server™ 2003, Standard Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>-Windows Server 2003, Enterprise Edition</p>
<p>-Windows 2000 Server</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Entidad emisora de certificados de otros fabricantes</p></td>
<td style="border:1px solid black;"><p>Desconocido</p></td>
<td style="border:1px solid black;"><p>Debe admitir la revocación.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Entidad emisora de certificados</p></td>
<td style="border:1px solid black;"><p>Windows Server 2003, Enterprise Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>-Otras versiones de Windows Server</p>
<p>-Entidades emisoras de certificados de otros fabricantes</p></td>
<td style="border:1px solid black;"><p>No compatibles</p></td>
<td style="border:1px solid black;"><p>Se pueden generar certificados utilizables.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidor RADIUS</p></td>
<td style="border:1px solid black;"><p>Windows Server 2003, Standard Edition o Enterprise Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p>Standard Edition sólo admite hasta 50 puntos de acceso inalámbricos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Windows 2000 Server</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p>Se puede utilizar el Servicio de autenticación de Internet (IAS) de Windows 2000 para 802.1X inalámbrico con pérdida de funcionalidad.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Otras plataformas</p></td>
<td style="border:1px solid black;"><p>No compatibles</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Controladores de dominio</p></td>
<td style="border:1px solid black;"><p>Windows Server 2003, Standard Edition o Enterprise Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p>El servicio de directorio Active Directory® debe tener esquema de Windows 2003 y un dominio en modo nativo de Windows 2000 o superior.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Windows 2000 Server</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p>Active Directory debe tener esquema de Windows 2003 y un dominio en modo nativo de Windows 2000 o superior.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor Web</p></td>
<td style="border:1px solid black;"><p>Servicios de Internet Information Server (IIS): Windows Server 2003</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>IIS: Windows 2000</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Otras plataformas</p></td>
<td style="border:1px solid black;"><p>No compatibles</p></td>
<td style="border:1px solid black;"><p>La mayoría de los servidores Web funcionarán para la lista de revocación de certificados (CRL) y la publicación de certificados de entidad emisora. Se requiere la compatibilidad con Páginas Active Server (ASP) para las páginas de inscripción de entidad emisora.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidores de infraestructura, como DNS (sistema de nombres de dominio) y DHCP (protocolo de configuración dinámica de host)</p></td>
<td style="border:1px solid black;"><p>Windows Server 2003, Standard Edition o Enterprise Edition</p></td>
<td style="border:1px solid black;"><p>Compatible y probado</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Windows 2000 Server</p></td>
<td style="border:1px solid black;"><p>Compatible</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Otras plataformas</p></td>
<td style="border:1px solid black;"><p>Desconocido</p></td>
<td style="border:1px solid black;"><p>Las soluciones de DHCP, DNS y de administración de otros fabricantes funcionarán correctamente con esta solución siempre que cumplan los requisitos básicos para cliente de Windows y Active Directory.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
