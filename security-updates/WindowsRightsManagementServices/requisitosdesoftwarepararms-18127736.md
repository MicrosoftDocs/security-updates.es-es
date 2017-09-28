---
TOCTitle: Requisitos de software para RMS
Title: Requisitos de software para RMS
ms:assetid: '17faf2ad-2366-4a92-98a5-766e20a0f741'
ms:contentKeyID: 18127736
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720201(v=WS.10)'
---

Requisitos de software para RMS
===============================

Los requisitos de software para ejecutar servidores RMS aparecen en la siguiente tabla.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Software</th>
<th>Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Sistema operativo</p></td>
<td style="border:1px solid black;"><p>Cualquier edición de Microsoft Windows Server® 2003, excepto Web Edition.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Sistema de archivos</p></td>
<td style="border:1px solid black;"><p>Se recomienda el sistema de archivos NTFS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Componentes del sistema operativo</p></td>
<td style="border:1px solid black;"><ul>
<li>Message Queue Server (también conocido como MSMQ) con la integración con el servicio de directorio de Active Directory® habilitada.<br />
<br />
</li>
<li>Servicios de Internet Information Server (IIS) con ASP.NET habilitado.<br />
<br />
</li>
<li>Microsoft .NET Framework 1.1<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Servicio de directorio de Active Directory®</p></td>
<td style="border:1px solid black;"><p>RMS debe instalarse en un dominio de Active Directory donde los controladores del dominio ejecutan Windows Server 2000 con Service Pack 3 (SP3) o superior. Todos los usuarios y grupos que utilizan RMS para usar y publicar contenido deben tener una dirección de correo electrónico que esté configurada en Active Directory.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor de base de datos</p></td>
<td style="border:1px solid black;"><p>RMS necesita una base de datos y procedimientos almacenados para realizar operaciones. Puede utilizar Microsoft SQL Server 2000 con SP3a o posterior, o Microsoft SQL Server 2005. Para realizar pruebas u otra implementación de un solo equipo, se pueden utilizar Microsoft SQL Server Desktop Engine (MSDE 2000) con SP3 o Microsoft SQL Server 2005 Express Edition.</p></td>
</tr>
</tbody>
</table>
  
Si está implementando RMS en un entorno donde hay varios bosques de Active Directory, debe utilizar grupos universales de Active Directory, de modo que la pertenencia a grupos se replique a todos los catálogos globales. Para crear grupos universales, el nivel funcional de dominio se debe configurar como mínimo en Windows 2000 nativo y el nivel funcional del bosque se debe elevar a Windows Server 2003.
  
Se recomienda el uso de MSDE 2000 o Microsoft SQL Server 2005 Express Edition para las bases de datos de RMS únicamente en entornos de pruebas, puesto que MSDE 2000 o Microsoft SQL Server 2005 Express Edition no admiten ninguna interfaz de red. Además, las condiciones de uso de MSDE 2000 o Microsoft SQL Server 2005 Express Edition especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de MSDE 2000 o Microsoft SQL Server 2005 Express Edition. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración.
  
Si no tiene la versión 1.1 de ASP.NET instalada en el servidor, el proceso de instalación variará en función de si ejecuta la versión de 32 bits de Windows Server 2003 o la versión de 64 bits.
  
Si está ejecutando la versión de 32 bits de Windows Server 2003, siga estos pasos para instalar y habilitar la versión 1.1 de ASP.NET:
  
1.  Abra **Agregar o quitar programas** en el **Panel de control** y, a continuación, haga clic en **Agregar o quitar componentes de Windows**.  
2.  Haga clic en **Servidor de aplicaciones** y, a continuación, en **Detalles**.  
3.  En el asistente para componentes de Windows, seleccione **ASP.NET**.  
4.  Si ASP.NET 1.1 está instalado pero no se admite como extensión de servicio Web de IIS:  
    -   Abra Administrador de Servicios de Internet Information Server.  
    -   Haga clic en la opción correspondiente a **extensión de servicio Web de IIS**, seleccione ASP.NET v1.1.4322 y, a continuación, haga clic en **Permitir**.
  
Si está ejecutando la versión de 64 bits de Windows Server 2003, siga estos pasos para instalar y habilitar la versión 1.1 de ASP.NET:
  
1.  Instale .NET Framework 1.1, que instalará ASP.NET 1.1. Puede descargar el paquete redistribuible de Microsoft .NET Framework versión 1.1 del Centro de descarga de Microsoft ([http://go.microsoft.com/fwlink/?LinkID=69985](http://go.microsoft.com/fwlink/?linkid=69985)).  
2.  Abra Administrador de Servicios de Internet Information Server.  
3.  Haga clic en la opción correspondiente a extensión de servicio Web de IIS, seleccione ASP.NET v1.1.4322 y, a continuación, haga clic en Permitir.
  
Si está ejecutando RMS en una versión de 64 bits de Windows Server 2003, deberá seguir los pasos siguientes para habilitar IIS e interoperar con RMS:
  
1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.  
2.  En **Abrir**, escriba el siguiente comando y, a continuación, presione ENTRAR:
  
**"cscript %SystemDrive%\\inetpub\\AdminScripts\\adsutil.vbs set w3svc/AppPools/Enable32bitAppOnWin64 1"**
  
RMS no está diseñado para la versión 2.0 de .NET Framework. Aunque se admite una instalación en paralelo, debe asegurarse de que ASP.NET esté configurado para utilizar ASP.NET v1.1.4322. Tiene dos opciones para garantizar que una instalación en paralelo se realiza con éxito:
  
-   Asegúrese de instalar la versión 2.0 de .NET Framework antes de instalar el servidor RMSserver.  
-   Establezca la versión de ASP.NET de nuevo en la versión 1.1.4322 en el sitio Web predeterminado en IIS mediante la ejecución del siguiente comando:
  
**"%SystemRoot%\\Microsoft.NET\\Framework\\v1.1.4322\\aspnet\_regiis -s w3svc/1/root"**
  
Para obtener más información acerca de Active Directory, Message Queue Server e IIS, consulte en el Centro de ayuda y soporte técnico de Windows Server 2003.
  
| ![](images/Cc720201.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |  
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Puede establecer los servicios en línea del servidor de RMS en el sitio Web predeterminado o en cualquier sitio que haya definido previamente en IIS. Por motivos de seguridad, no debe utilizar este servidor para ejecutar servicios o sitios adicionales. Si lo hace, se pueden ejecutar varias aplicaciones y servicios con la misma cuenta que RMS (especialmente la cuenta del sistema local), lo que puede exponer las claves privadas a operaciones que pueden no ser seguras. No debe establecer los servicios en línea del servidor de RMS en el mismo sitio Web que Microsoft Office SharePoint Server 2007. No se puede usar RMS con la autenticación Kerberos. El establecimiento de servicios en línea del servidor de RMS en un sitio Web deshabilita la autenticación Kerberos para ese servidor. Si RMS no está configurado para utilizar ASP.NET v1.1.4322, no se registra información en la base de datos de registro, lo que provocará la pérdida de datos. |
  
Vea también  
-----------
  
####  
  
[Planeamiento de la infraestructura de servidor de base de datos](https://technet.microsoft.com/b12354bd-3143-4d1f-b5aa-450c4550653c)
