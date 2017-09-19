---
TOCTitle: 'Apéndice D: Compatibilidad con WPA'
Title: 'Apéndice D: Compatibilidad con WPA'
ms:assetid: 'a622f7a6-cb43-4b4f-ae2a-1b710b056f7d'
ms:contentKeyID: 20112543
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458721(v=TechNet.10)'
---

Apéndice D: Compatibilidad con WPA
==================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

### Introducción

La solución *Seguridad en LAN inalámbricas con Servicios de Certificate Server* por diseño es compatible con la seguridad WPA (acceso protegido de Wi-Fi) para LAN inalámbricas (WLAN). La compatibilidad con WPA se ha probado correctamente en un laboratorio configurado según los pasos de esta guía. En este documento se describen varios elementos que se deben tener en cuenta al evaluar el modo en que se puede utilizar WPA con esta solución.

#### Información general de WEP y WPA

WEP (privacidad equivalente por cable) se definió como parte del estándar de red inalámbrica 802.11 del instituto Institute for Electrical Engineers (IEEE) de 1999 para proporcionar un nivel de protección equivalente a un sistema con cables. WEP básica (o estática) proporciona codificación y control de acceso para el tráfico inalámbrico en función de una clave precompartida. Se ha demostrado que WEP adolece de varias vulnerabilidades que pueden permitir que un atacante eluda este control de seguridad 802.11 nativo.

El sector de WLAN ha respondido a las vulnerabilidades de WEP mediante la oferta de una solución de seguridad más robusta denominada WPA. WPA incrementa el nivel de protección de datos y el control de acceso de los sistemas WLAM mediante una especificación de seguridad basada en estándares e interoperable. La primera versión de WPA es un subconjunto inicial del estándar 802.11i y se prevé que mantenga la compatibilidad en el futuro. Actualmente está previsto que 802.11i se publique como WPA 2.0.

En el momento de la publicación, numerosas organizaciones tenían una gran cantidad de hardware de WLAN implementado que no admitía WPA. Es importante que esta solución admita tanto este hardware como el nuevo equipo compatible con WPA. Aunque WPA proporciona un mayor nivel de seguridad que WEP dinámica, esta última todavía constituye una solución viable hasta que todo el hardware se pueda actualizar para ser compatible con WPA.

#### Consecuencias de WPA en esta solución

WPA se puede considerar como un sustituto de WEP en esta solución *Seguridad en LAN inalámbricas* *con Servicios de Certificate Server*. La mayoría de los componentes de la solución no se ven afectados por la introducción de WPA. Se ha probado correctamente la compatibilidad de la solución con WPA mediante la configuración de equipo de red habilitado par WPA de un modo similar al equipo basado en WEP y la realización de cambios en los equipos cliente.

Debido a que WPA utiliza el protocolo 802.1X para la autenticación de red, el servicio de usuario de acceso telefónico de autenticación remota (RADIUS), Servicios de Microsoft® Certificate Server y la mayoría de los valores del servicio de directorio de Active Directory® funcionan del modo en que se han configurado. Una consideración importante es que sólo se pueden configurar los valores específicos de WPA mediante Directiva de grupo si hay al menos un controlador de dominio con Windows Server 2003 Service Pack 1 (también se pueden configurar los valores de Directiva de grupo en un miembro de dominio con Windows Server 2003 que no sea un controlador de dominio). Más adelante en este apéndice encontrará más información al respecto. En la siguiente tabla se enumeran los elementos que se deben tener en cuenta al utilizar WPA con esta solución.

**Tabla D.1: Componentes de la solución que se deben tener en cuenta**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento de la solución</p></th>
<th><p>Consideración</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Controladores de hardware de Microsoft Windows® XP</p></td>
<td style="border:1px solid black;"><p>Debe ponerse en contacto con el proveedor de la tarjeta de interfaz de red (NIC) para evaluar las tarjetas que puede actualizar para compatibilidad con WPA y la disponibilidad de controladores de cliente para Windows XP.</p></td>
<td style="border:1px solid black;"><p>Busque controladores que hayan pasado las pruebas de los laboratorios de calidad de hardware de Windows (WHQL). La compatibilidad de controladores para el Servicio Configuración inalámbrica cero para Windows habilita el firmware de tarjeta para que se actualice dinámicamente con el fin de admitir WPA. Confirme la compatibilidad de controladores para el servicio Configuración inalámbrica cero con el proveedor.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Configuración de cliente Windows XP</p></td>
<td style="border:1px solid black;"><p>Se deberán cambiar los valores de configuración del cliente. Esta solución se ha probado mediante la selección de WPA como método de autenticación y TKIP (Protocolo de integridad de claves temporales) como el protocolo de cifrado.</p></td>
<td style="border:1px solid black;"><p>TKIP reemplaza a WEP como el método de cifrado y WPA impone 802.1X como el método de autenticación.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Reautenticación de cliente temporizada</p></td>
<td style="border:1px solid black;"><p>Esta solución utiliza la configuración de RADIUS para garantizar que los clientes realizan una reautenticación cada 10 minutos de modo que se regeneren las claves WEP.</p></td>
<td style="border:1px solid black;"><p>TKIP vuelve a crear claves para cada paquete; por lo tanto, convierte en obsoleto el requisito de reautenticación de cliente para la clave WEP. Si se deja esta configuración en 10 minutos, se agrega una carga innecesaria a los servidores de Servicio de autenticación de Internet (IAS) de Microsoft. Cuando utilice WPA, puede cambiar el tiempo de espera de sesión a 10 horas.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva de grupo de red inalámbrica</p></td>
<td style="border:1px solid black;"><p>La directiva de grupo de red inalámbrica existente que se incluían con Windows Server 2003 antes de SP1 se había desarrollado con anterioridad a la disponibilidad de WPA y, por lo tanto, no puede configurar valores de WPA de cliente.</p></td>
<td style="border:1px solid black;"><p>Debe utilizar Windows Server 2003 SP1 para configurar los valores de WPA de la directiva de grupo.<br />
De lo contrario, debe configurar manualmente los valores de cliente inalámbrico.</p></td>
</tr>
</tbody>
</table>
<p> </p>

#### Configuración de la solución de seguridad en LAN inalámbricas con WPA

Puede llevar a cabo los siguientes pasos de alto nivel para configurar la solución con el fin de que utilice WPA:

1.  Actualice el firmware de los puntos de acceso inalámbricos existentes para que admitan WPA o implemente nuevos puntos de acceso inalámbricos que admitan WPA. Asegúrese de agregar nuevos puntos de acceso inalámbricos como clientes RADIUS al servidor IAS según las instrucciones de esta guía. Configure los valores de WPA en los puntos de acceso inalámbrico según las especificaciones del proveedor.

2.  Actualice la tarjeta de interfaz de red (NIC) de WLAN a una versión que admita WPA. Microsoft está trabajando con numerosos proveedores de tarjetas de WLAN para admitir la actualización de firmware mediante el controlador de la tarjeta adaptadora.

3.  Quite el equipo inalámbrico del grupo de seguridad al que se aplica la directiva de grupo de red inalámbrica. Cree un nuevo objeto de directiva de grupo (GPO) mediante Windows Server 2003 SP1 y configure los valores de cliente inalámbrico para WPA. Especifique WPA como el tipo de autenticación y TKIP como el tipo de codificación. Cree un grupo de seguridad adicional y concédale permisos para aplicar directiva en el GPO de WPA. Utilice este grupo para controlar los clientes que reciben la configuración de WPA. Si no ha implementado el Service Pack 1 de Windows Server 2003, debe configurar manualmente los valores de cliente inalámbrico para WPA.

4.  Pruebe la autenticación para la WLAN mediante WPA. IAS debe registrar un mensaje del registro de sucesos del sistema con **IAS** como origen y **1** como Id. de suceso. Esto indica una autenticación correcta.  

#### Información adicional

Utilice los siguientes recursos para encontrar más información acerca de los temas tratados en este apéndice:

-   [The Cable Guy — March 2003, Wi – Fi Protected Access (WPA) Overview](http://www.microsoft.com/technet/community/columns/cableguy/cg0303.mspx) en Microsoft TechNet en http://www.microsoft.com/technet/community/columns/cableguy/cg0303.mspx.

-   Artículo 815485 de Microsoft Knowledge Base, “[Overview of the WPA Wireless Security Update in Windows XP](http://support.microsoft.com/?kbid=815485)”, en http://support.microsoft.com/?kbid=815485.

-   La publicación [Microsoft Press Pass Announcement](http://www.microsoft.com/presspass/press/2003/mar03/03-31wifiprotectedaccesspr.asp) acerca de la disponibilidad de WPA en http://www.microsoft.com/presspass/press/2003/mar03/03-31WiFiProtectedAccessPR.asp.

-   [IEEE 802.11 Wireless LAN Security with Microsoft Windows XP](http://www.microsoft.com/downloads/details.aspx?familyid=67fdeb48-74ec-4ee8-a650-334bb8ec38a9&displaylang=en) en http://www.microsoft.com/downloads/details.aspx?FamilyID=67fdeb48-74ec-4ee8-a650-334bb8ec38a9&displaylang=en.

[](#mainsection)[Principio de la página](#mainsection)
