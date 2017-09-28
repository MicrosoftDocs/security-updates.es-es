---
TOCTitle: Servicios Web de RMS
Title: Servicios Web de RMS
ms:assetid: 'ed8dbb2e-0590-4502-afc4-54f66b96d515'
ms:contentKeyID: 18128012
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747728(v=WS.10)'
---

Servicios Web de RMS
====================

RMS proporciona el componente de servidor de un sistema RMS. Sus funciones principales se implementan como conjunto de servicios web de Microsoft® ASP.NET que se ejecutan en Microsoft® Internet Information Services (IIS). Los servicios web de RMS se exponen mediante la interfaz de SOAP o mediante .NET Remoting.

Los servicios web proporcionan:

-   Subinscripción de servidores
-   Certificación de cuenta de las entidades de confianza
-   Licencias de la información protegida por derechos
-   Funciones de administración de RMS

En la siguiente tabla se describen los servicios web de RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Servicio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Subinscripción</p></td>
<td style="border:1px solid black;"><p>Proporciona certificados de emisor de licencias de servidor subordinado a los servidores en clústeres de sólo licencias. Estos certificados permiten que el clúster de sólo licencias pueda emitir licencias de publicación y de uso.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Certificación de cuenta</p></td>
<td style="border:1px solid black;"><p>Proporciona certificados de cuenta de derechos a los usuarios. Estos certificados son necesarios para que los usuarios obtengan licencias de publicación y uso con el fin de crear y usar contenido protegido por derechos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Proxy de activación</p></td>
<td style="border:1px solid black;"><p>Este servicio se retiene por compatibilidad con el cliente de la versión 1 de RMS. Pasa solicitudes de activación de equipo al servicio de activación de Microsoft y devuelve cajas de seguridad y certificados de equipo de RMS a los clientes de la versión 1 de RMS. Este servicio no lo usan los clientes de RMS Service Pack 1 (SP1) o posterior.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Publicar</p></td>
<td style="border:1px solid black;"><p>Emite licencias de publicación, que permiten a los autores crear y distribuir contenido protegido por derechos. También emite certificados de emisor de licencias de cliente, que permiten a los usuarios publicar contenido protegido por derechos sin estar conectados a la red interna que hospeda RMS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Licencias</p></td>
<td style="border:1px solid black;"><p>Emite licencias de uso, que permiten a los usuarios usar contenido protegido por derechos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Administración</p></td>
<td style="border:1px solid black;"><p>Permite al administrador administrar RMS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DrmRemote</p></td>
<td style="border:1px solid black;"><p>Permite que los servicios web se comuniquen entre sí y con otros componentes del sistema RMS mediante la exposición de .NET Remoting.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Retiro</p></td>
<td style="border:1px solid black;"><p>Desprotege el contenido protegido por derechos anteriormente y lo devuelve al cliente. Este servicio se instala con RMS, pero el servicio no tiene una raíz virtual correspondiente en IIS hasta que lo habilita el administrador. Al habilitar este servicio se deshabilitan los demás.</p></td>
</tr>
</tbody>
</table>
  
Además de los servicios web, RMS instala un servicio de escucha de registro. Cada servicio web envía datos registrados a la cola de mensajes de registro. A continuación, el servicio de escucha de registro transfiere los datos de registro de la cola de mensajes a la base de datos de registro.
  
Las aplicaciones de servicio web se encuentran en los directorios virtuales de IIS. Estos directorios virtuales se instalan en cada servidor RMS, en el sitio web que ha seleccionado durante el aprovisionamiento.
  
La autenticación y el acceso se configuran de forma independiente para cada directorio virtual. Además, el acceso se configura independientemente para cada servicio web. Para obtener más información acerca de la configuración de seguridad en los directorios virtuales y los archivos de servicios web, vea [Compatibilidad con los Servicios de Internet Information Server para RMS](https://technet.microsoft.com/bd4dc69f-1e4e-4e95-9ae2-c925d8a14d4c) más adelante en este tema.
  
Para obtener más información acerca de cada servicio web, vea [Componentes de software de RMS](https://technet.microsoft.com/e38a840e-f390-48fd-8354-50108a64f5ca) más adelante en este tema.
