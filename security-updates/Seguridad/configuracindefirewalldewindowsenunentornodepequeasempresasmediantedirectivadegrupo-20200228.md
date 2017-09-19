---
TOCTitle: Configuración de Firewall de Windows en un entorno de pequeñas empresas mediante Directiva de grupo
Title: Configuración de Firewall de Windows en un entorno de pequeñas empresas mediante Directiva de grupo
ms:assetid: 'be4467be-5a2c-4ae2-925a-c2e1f6e33e4b'
ms:contentKeyID: 20200228
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875816(v=TechNet.10)'
---

Cómo configurar Firewall de Windows en un entorno de pequeñas empresas mediante Directiva de grupo
==================================================================================================

Publicado: diciembre 9, 2004 | Actualizado: julio 21, 2006

##### En esta página

[](#ehaa)[Introducción](#ehaa)
[](#egaa)[Antes de comenzar](#egaa)
[](#efaa)[Adición de revisiones a estaciones de trabajo administrativas y Windows Small Business Server 2003](#efaa)
[](#eeaa)[Crear un objeto de directiva de grupo y actualizarlo](#eeaa)
[](#edaa)[Configuración de los parámetros de Firewall de Windows mediante Directiva de grupo](#edaa)
[](#ecaa)[Aplicación de la configuración con GPUpdate](#ecaa)
[](#ebaa)[Comprobación de la aplicación de la configuración de Firewall de Windows](#ebaa)
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

En este documento se explica cómo configurar las características de Firewall de Windows en equipos en los que se ejecuta Microsoft® Windows® XP Professional Service Pack 2 (SP2) en un entorno de pequeñas y medianas empresas (PYMES). El entorno puede incluir controladores de dominio en los que se ejecuta Microsoft Windows Small Business Server 2003, Microsoft Windows Server™ 2003 o Microsoft Windows 2000 Server.

El modo más eficaz de administrar la configuración de Firewall de Windows en la red de una organización es utilizar el servicio de directorio Active Directory® y configurar los parámetros de Firewall de Windows en Directiva de grupo. Active Directory y Directiva de grupo permiten configurar de un modo centralizado los parámetros de Firewall de Windows y aplicarlos a todos los equipos cliente con Windows XP SP2.

Windows XP SP2 incluye nuevas plantillas administrativas para los objetos de directiva de grupo (GPO) a fin de mejorar la seguridad para el equipo cliente y el dominio que incluye la funcionalidad para Firewall de Windows. Para aplicar estas plantillas, es posible que tenga que instalar revisiones, en función del sistema operativo de la estación de trabajo o del servidor de dominio que se utilice.

Después de aplicarlas, todas las actualizaciones de Directiva de grupo incluirán parámetros de configuración para Firewall de Windows. Las actualizaciones de Directiva de grupo se envían del controlador de dominio a todos los miembros del dominio; asimismo, un miembro del dominio también puede solicitarlas mediante la utilidad GPUpdate.

Para configurar Firewall de Windows, inicie sesión como miembro del grupo de seguridad del propietario/creador de directivas de grupo o del grupo Admins. del dominio y utilice el Editor de objetos de directiva de grupo.

En la tabla siguiente, se especifica la configuración predeterminada de Firewall de Windows.

**Tabla 1. Configuración predeterminada de Firewall de Windows**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Opción</p></th>
<th><p>Configuración predeterminada</p></th>
<th><p>Supuesto de modificación</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Configuración de conexión de red</p></td>
<td style="border:1px solid black;"><p>Todas las conexiones</p></td>
<td style="border:1px solid black;"><p>La protección de Firewall de Windows en una conexión de red específica deja de ser necesaria o cada una de las conexiones de red requiere una configuración individual.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Excepciones de programa</p></td>
<td style="border:1px solid black;"><p>Sólo asistencia remota</p></td>
<td style="border:1px solid black;"><p>Resulta necesario recibir en su equipo conexiones de otros programas o servicios.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Excepciones de puerto</p></td>
<td style="border:1px solid black;"><p>Ninguna</p></td>
<td style="border:1px solid black;"><p>Resultan necesarias conexiones de otro equipo que utiliza puertos específicos de su equipo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Excepciones ICMP</p></td>
<td style="border:1px solid black;"><p>Ninguna</p></td>
<td style="border:1px solid black;"><p>Es necesario que otros equipos comprueben que el suyo está en ejecución y TCP/IP se ha configurado correctamente.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Notificaciones</p></td>
<td style="border:1px solid black;"><p>Activadas</p></td>
<td style="border:1px solid black;"><p>No se desea recibir más notificaciones cuando otros equipos intentan conectarse al suyo sin conseguirlo.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Registro</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
<td style="border:1px solid black;"><p>Se necesita un registro de conexiones o de intentos de conexión efectuados por su equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>No se permiten excepciones</p></td>
<td style="border:1px solid black;"><p>Desactivado</p></td>
<td style="border:1px solid black;"><p>Se ha descubierto una vulnerabilidad de seguridad en el equipo o éste se utiliza en un entorno de menos seguro, como la sala de espera de un aeropuerto.</p></td>
</tr>  
</tbody>  
</table>
  
Las tareas que se deben realizar para configurar Firewall de Windows mediante Directiva de grupo son las siguientes:
  
-   Agregar revisiones a las estaciones de trabajo administrativas de GPO y Windows Small Business Server 2003.
  
-   Crear GPO y actualizarlos.
  
-   Configurar los parámetros de Firewall de Windows con Directiva de grupo.
  
-   Aplicar la configuración mediante GPUpdate.
  
-   Comprobar que la configuración de Firewall de Windows se ha aplicado.
  
Complete las tareas que se describen en este documento para mantener su equipo a salvo de gusanos y de otros tipos de código malicioso, mientras sigue permitiendo las conexiones a Internet y desde Internet.
  
Microsoft recomienda que pruebe todos los parámetros de configuración de Directiva de grupo de Firewall de Windows en un entorno de prueba antes de implementarlos en el entorno de producción; con ello, se garantiza que la configuración de Directiva de grupo no dará lugar a tiempo de inactividad o a una pérdida de productividad.
  
Para obtener definiciones acerca de términos relacionados con la seguridad, consulte el documento siguiente:
  
-   [Glosario de seguridad de Microsoft](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx), disponible en el sitio Web de Microsoft, en http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx.
  
#### Objetivo de este documento de seguridad
  
Al llevar a cabo los procesos que se detallan en este documento, protegerá a los equipos cliente con Windows XP Professional del acceso de usuarios no autorizados y de software malicioso mediante un servidor de seguridad basado en host. Además, con estos pasos, habilitará la administración de seguridad avanzada mediante Active Directory.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Antes de comenzar
  
**Importante**   Las instrucciones de este documento se han desarrollado con el menú predeterminado que se visualiza al hacer clic en el botón **Inicio**. Si ha modificado dicho menú, puede que los pasos varíen ligeramente.
  
Windows XP con SP2 puede utilizarse en equipos cliente en un dominio de Active Directory mediante controladores de dominio en los que se ejecuta una de las siguientes aplicaciones:
  
-   Windows Server 2003
  
-   Windows Small Business Server 2003
  
-   Windows 2000 Server SP4 o posterior
  
En la mayor parte de las redes, el servidor de seguridad del hardware de la red, así como otros sistemas de seguridad, proporcionan cierto nivel de protección frente a Internet a los equipos de la red.
  
Si no tiene un servidor de seguridad de host (un servidor de seguridad de software instalado de forma local), como Firewall de Windows, para las conexiones de red del equipo, será vulnerable a programas maliciosos que podrían introducir otros equipos al incorporarse a la red. Además, será vulnerable al utilizar el equipo en un lugar ajeno a su red, como al usar un equipo portátil en casa o al conectarlo a una red aeroportuaria o a la de un hotel.
  
Antes de instalar alguna revisión, asegúrese de contar con una buena copia de seguridad del equipo, incluida una copia de seguridad del Registro.
  
Para obtener más información acerca de cómo realizar una copia de seguridad del Registro, consulte el documento siguiente:
  
-   Artículo 322756 de Microsoft Knowledge Base, "[Cómo realizar una copia de seguridad, modificar y restaurar el Registro en Windows XP y Windows Server 2003](http://support.microsoft.com/?id=322756)", disponible en el sitio Web de ayuda y soporte técnico de Microsoft, en http://support.microsoft.com/?id=322756.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Adición de revisiones a estaciones de trabajo administrativas y Windows Small Business Server 2003
  
Si administra la configuración de GPO en equipos en los que se ejecutan versiones anteriores de sistemas operativos o Service Packs (por ejemplo, Windows XP con SP1 o Windows Server 2003), debe instalar una revisión ([KB842933](http://support.microsoft.com/?kbid=842933)) a fin de que la configuración de la directiva aparezca correctamente en el Editor de objetos de directiva de grupo.
  
Si utiliza Small Business Server 2003, tendrá que instalar una revisión adicional ([KB872769](http://support.microsoft.com/?kbid=872769)). De forma predeterminada, Small Business Server 2003 deshabilita Firewall de Windows. La revisión resuelve este problema.
  
**Nota**   Las revisiones enumeradas no se incluyen como parte de Microsoft Update y, por lo tanto, deben instalarse de forma independiente. Estas revisiones deben aplicarse a todos los equipos afectados individualmente.
  
La revisión KB842933 se aplica a los siguientes productos:
  
-   Microsoft Windows Server 2003, Web Edition
  
-   Microsoft Windows Server 2003, Standard Edition (x86 de 32 bits)
  
-   Microsoft Windows Server 2003, Enterprise Edition (x86 de 32 bits)
  
-   Microsoft Windows Server 2003, Enterprise Edition para sistemas basados en Itanium
  
-   Microsoft Windows XP Professional SP1
  
-   Microsoft Windows Small Business Server 2003 Premium Edition
  
-   Microsoft Windows Small Business Server 2003 Standard Edition
  
-   Microsoft Windows 2000 Advanced Server
  
-   Microsoft Windows 2000 Server
  
-   Microsoft Windows 2000 Professional Edition
  
La revisión KB872769 se aplica a los siguientes productos:
  
-   Microsoft Windows Small Business Server 2003 Standard Edition
  
-   Microsoft Windows Small Business Server 2003 Premium Edition
  
Para obtener más información o para obtener estas revisiones, consulte los documentos siguientes:
  
-   Artículo de Microsoft Knowledge Base [842933](http://support.microsoft.com/?kbid=842933), disponible en el sitio Web de ayuda y soporte técnico de Microsoft, en http://support.microsoft.com/?kbid=842933.
  
-   Artículo de Microsoft Knowledge Base [872769](http://support.microsoft.com/?kbid=872769), disponible en el sitio Web de ayuda y soporte técnico de Microsoft, en http://support.microsoft.com/?kbid=872769.
  
Para obtener información adicional acerca de cómo descargar archivos de soporte técnico de Microsoft, consulte el siguiente documento:
  
-   "[Cómo obtener Archivos de soporte técnico de Microsoft desde los servicios en línea](http://support.microsoft.com/kb/119591)", disponible en el sitio Web de ayuda y soporte técnico de Microsoft, en http://support.microsoft.com/kb/119591.
  
#### Requisitos para llevar a cabo esta tarea
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Tendrá que iniciar sesión en el equipo cliente con una cuenta que sea miembro del grupo de seguridad de administradores locales o Admins. del dominio.
  
-   **Herramientas**. La revisión descargada, adecuada para su sistema operativo, tal como se explica en los artículos de Knowledge Base 842933 y 872769.
  
#### Cómo agregar revisiones
  
**Para agregar la revisión 842933 a Windows Small Business Server 2003,** **Windows 2000 Server SP4 o posterior,** **Windows XP SP1** **o Windows Server 2003**
  
1.  En el escritorio de Windows, haga clic en **Inicio** y en **Ejecutar**; a continuación, escriba la ruta y el nombre del archivo de la revisión descargada; por último, haga clic en **Aceptar**.
  
2.  En la pantalla **Éste es el Asistente para instalación de KB842933**, haga clic **Siguiente**.
  
3.  En la página **Licencia**, revise los términos del contrato de licencia. Para continuar, haga clic en **Acepto** y, a continuación, haga clic en **Siguiente**.
  
4.  En la pantalla **Finalización del Asistente para instalación de KB842933**, haga clic en **Finalizar** para completar la instalación de la revisión y reiniciar el equipo.
  
5.  Repita los pasos del 1 al 4 para todos los equipos a los que afecte la revisión (servidores y estaciones de trabajo de administración).
  
**Para agregar la revisión 872769 a Windows Small Business Server 2003**
  
1.  En el escritorio de Windows, haga clic en **Inicio** y en **Ejecutar**; a continuación, escriba la ruta y el nombre de archivo de la revisión 872769 descargada; por último, haga clic en **Aceptar**.
  
2.  En la página **Éste es el Asistente para instalación de KB872769**, haga clic en **Siguiente**.
  
3.  En la página **Licencia**, revise los términos del contrato de licencia. Para continuar, haga clic en **Acepto** y, a continuación, haga clic en **Siguiente**.
  
4.  En la página **Finalizando el Asistente para instalación de KB872769**, haga clic en **Finalizar** para completar la instalación de la revisión y reiniciar el equipo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Crear un objeto de directiva de grupo y actualizarlo
  
Windows XP SP2 agrega parámetros de configuración a las plantillas administrativas. Para configurar estos nuevos parámetros, debe actualizar cada uno de los GPO con las nuevas plantillas administrativas que se encuentren en Windows XP SP2. Si no actualiza los GPO, la configuración de Firewall de Windows no estará disponible.
  
En un equipo con Windows XP SP2, puede utilizar Microsoft Management Console (MMC) con el complemento Editor de objetos de directiva de grupo para actualizar GPO con sólo abrir un GPO existente.
  
Después de actualizar un GPO, podrá configurar los parámetros de protección de la red apropiados para los equipos en los que se ejecute Windows XP SP2. En el siguiente ejercicio, se creará un nuevo GPO que incorporará de forma inmediata estos parámetros de protección de red actualizados.
  
#### Requisitos para llevar a cabo esta tarea
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Tendrá que iniciar sesión en un equipo con Windows XP SP2 que sea un equipo cliente del dominio de Active Directory; además, deberá utilizar una cuenta que sea miembro del grupo de seguridad del propietario/creador de directivas de grupo o del grupo Admins. del dominio.
  
-   **Herramientas**. Microsoft Management Console (MMC) con el complemento Editor de objetos de directiva de grupo instalado.
  
#### Creación y actualización de objetos de directiva de grupo
  
**Para actualizar objetos de directiva de grupo con nuevas plantillas administrativas de Windows XP SP2**
  
1.  En el escritorio de Windows XP SP2, haga clic en **Inicio** y en **Ejecutar**; a continuación, escriba **mmc** y, seguidamente, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**.
  
3.  En la ficha **Independiente**, haga clic en **Agregar**.
  
4.  En la lista **Complementos independientes disponibles**, busque la opción **Editor de objetos de directiva de grupo** y haga clic en ella; seguidamente, haga clic en **Agregar**.
  
5.  En el cuadro de diálogo **Seleccionar un objeto de directiva de grupo**, haga clic en **Examinar**.
  
6.  En el cuadro de diálogo **Buscar un objeto directiva de grupo** (que se muestra en la siguiente captura de pantalla), haga clic en **Crear nuevo objeto de directiva de grupo** y asigne el nombre **Probar directiva de Firewall de Windows cliente** al nuevo GPO.
  
    ![](images/Cc875816.WFGP01(es-es,TechNet.10).gif)
  
7.  Haga clic en **Aceptar** y, seguidamente, en **Finalizar** para cerrar el Asistente para directivas de grupo y aplicar la nueva plantilla administrativa al GPO seleccionado.
  
8.  En el cuadro de diálogo **Agregar un complemento independiente**, haga clic en **Cerrar**.
  
9.  En el cuadro de diálogo **Agregar o quitar complemento**, haga clic en **Aceptar**.
  
10. Cierre MMC, haga clic en **Archivo** y en **Salir**. No guarde los cambios efectuados en la configuración de la consola.
  
    **Nota**   Aunque no guarden los cambios de la consola, este procedimiento importa en el GPO las nuevas plantillas administrativas desde Windows XP SP2. Las plantillas deben importarse en cada uno de los GPO que se definan.
  
11. Repita los pasos anteriores para todos los GPO que se utilicen para aplicar la directiva de grupo a los equipo basados en Windows XP SP2.
  
Para actualizar los GPO para entornos de red mediante Active Directory y Windows XP SP2, Microsoft recomienda utilizar la consola de administración de directivas de grupo, que está disponible como descarga gratuita. Para obtener más información, consulte los siguientes documentos:
  
-   "[Enterprise Management with the Group Policy Console](http://www.microsoft.com/spain/servidores/windowsserver2003/technologies/management/grouppolicy/gpmc.aspx)", disponible en el sitio Web de Microsoft Windows Server 2003, en http://www.microsoft.com/spain/servidores/windowsserver2003/technologies/management/grouppolicy/gpmc.aspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de los parámetros de Firewall de Windows mediante Directiva de grupo
  
Hay dos grupos de parámetros de Firewall de Windows que se pueden configurar:
  
-   **Perfil de dominio**. Estos parámetros de configuración los utilizan los equipos conectados a una red que contiene controladores de dominio para el dominio del que tales equipos son miembros.
  
-   **Perfil estándar**. Estos parámetros de configuración los utilizan los equipos que no están conectados a una red, como, por ejemplo, cuando se viaja con un equipo portátil.
  
Si no configura los parámetros de perfil estándar, los valores predeterminados no experimentan cambio alguno. Microsoft recomienda que configure los parámetros de perfil estándar y de dominio, y que habilite Firewall de Windows para ambos perfiles. La única excepción la constituyen las situaciones en las que ya está usando un producto de servidor de seguridad de host de terceros (un servidor de seguridad de software instalado localmente). Microsoft recomienda deshabilitar Firewall de Windows si ya está utilizando un producto de servidor de seguridad de host de terceros.
  
De forma típica, la configuración de perfil estándar es más restrictiva que la de perfil de dominio, puesto que la primera no incluye aplicaciones y servicios que se utilizan únicamente en un entorno de dominio administrado.
  
En un GPO, tanto el perfil de dominio como el estándar contienen el mismo conjunto de parámetros de configuración de Firewall de Windows. Windows XP SP2 se basa en la determinación de la red para aplicar la configuración de perfil correcta.
  
**Nota**   Para obtener más información acerca de la determinación de red, consulte "[Network Determination Behavior for Network-Related Group Policy Settings](http://www.microsoft.com/spain/technet/recursos/articulos/cg1204.mspx)", disponible en el sitio Web de TechNet, en http://www.microsoft.com/spain/technet/recursos/articulos/cg1204.mspx.
  
En esta sección, se describen las posibles configuraciones de Firewall de Windows en un GPO y la configuración recomendada para un entorno de SMB. Además, se muestra cómo configurar los cuatro tipos principales de parámetros de configuración de GPO.
  
#### Requisitos para llevar a cabo esta tarea
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Tendrá que iniciar sesión en un equipo con Windows XP SP2 que sea un equipo cliente del dominio de Active Directory; además, deberá utilizar una cuenta que sea miembro del grupo de seguridad del propietario/creador de directivas de grupo o del grupo Admins. del dominio.
  
-   **Herramientas**. Microsoft Management Console (MMC) con el complemento Editor de objetos de directiva de grupo instalado.
  
**Nota**   Para abrir un GPO, utilice una MMC con el complemento Editor de objetos de directiva de grupo o la consola Usuarios y equipos de Active Directory. Para utilizar la consola Usuarios y equipos de Active Directory en un equipo cliente con Windows XP, primero debe ejecutar Aadminpak.msi desde el CD de Windows Server 2003.
  
#### Configuración de los parámetros de Firewall de Windows mediante Directiva de grupo
  
Utilice el complemento Directiva de grupo para modificar la configuración de Firewall de Windows en los GPO que corresponda.
  
Tras completar los pasos siguientes para configurar los parámetros de Firewall de Windows, espere a que la configuración se aplique a los equipos cliente mediante los ciclos de actualización estándar o sírvase de la utilidad GPUpdate en el equipo cliente. De forma predeterminada, estos ciclos de actualización tienen una periodicidad de 90 minutos, con una variación aleatoria de +/- 30 minutos. Con la siguiente actualización de Directiva de grupo de Configuración del equipo, se descargará la nueva configuración de Firewall de Windows y ésta se aplicará a los equipos en los que se ejecute Windows XP SP2.
  
**Para configurar los parámetros de Firewall de Windows mediante Directiva de grupo**
  
1.  En el escritorio de Windows XP SP2, haga clic en **Inicio** y en **Ejecutar**; a continuación, escriba **mmc** y, seguidamente, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**.
  
3.  En la ficha **Independiente**, haga clic en **Agregar**.
  
4.  En la lista **Complementos independientes disponibles**, busque la opción **Editor de objetos de directiva de grupo** y haga clic en ella; seguidamente, haga clic en **Agregar**.
  
5.  En el cuadro de diálogo **Seleccionar objeto de directiva de grupo**, haga clic en **Examinar**.
  
6.  Seleccione **Probar directiva de Firewall de Windows cliente**, haga clic en **Aceptar** y, a continuación, en **Finalizar**.
  
7.  Haga clic en **Cerrar** para cerrar el cuadro **Agregar complemento independiente**; seguidamente, en el cuadro **Agregar o quitar complemento**, haga clic en **Aceptar**.
  
8.  En el árbol de consola del Editor de objetos de directiva de grupo, abra **Configuración del equipo**, **Plantillas administrativas**, **Red**, **Conexiones de red** y, a continuación,**Firewall de Windows** (que se muestra en la siguiente captura de pantalla).
  
    ![](images/Cc875816.WFGP02(es-es,TechNet.10).gif)
  
9.  Seleccione **Perfil de dominio** (que se muestra en la siguiente captura de pantalla) o **Perfil estándar**.
  
    ![](images/Cc875816.WFGP03(es-es,TechNet.10).gif)
  
    En la siguiente tabla, se resume la configuración recomendada de Directiva de grupo de Firewall de Windows para los perfiles de dominio y estándar.
  
    **Tabla 2. Recomendaciones de configuración de Firewall de Windows**

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
    <th><p>Configuración</p></th>  
    <th><p>Descripción</p></th>  
    <th><p>Perfil de dominio</p></th>  
    <th><p>Perfil estándar</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Proteger todas las conexiones de red</p></td>
    <td style="border:1px solid black;"><p>Especifica que todas las conexiones de red tienen habilitado Firewall de Windows.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>No permitir excepciones</p></td>
    <td style="border:1px solid black;"><p>Especifica que todo el tráfico entrante no solicitado se descarta, incluido el tráfico permitido.</p></td>
    <td style="border:1px solid black;"><p>No configurado.</p></td>
    <td style="border:1px solid black;"><p>Habilitado, a menos que deba configurar excepciones de programa.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Definir excepciones de programa</p></td>
    <td style="border:1px solid black;"><p>Define el tráfico permitido en términos de nombres de archivos de programa.</p></td>
    <td style="border:1px solid black;"><p>Habilitado y configurado con los programas (aplicaciones y servicios) que usan los equipos de la red en los que se ejecuta Windows XP SP2.</p></td>
    <td style="border:1px solid black;"><p>Habilitado y configurado con los programas (aplicaciones y servicios) que usan los equipos de la red en los que se ejecuta Windows XP SP2.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Permitir excepciones de programa locales</p></td>
    <td style="border:1px solid black;"><p>Habilita la configuración local de excepciones de programa.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado, a menos que desee que los administradores locales configuren las excepciones de programa de forma local.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Permitir excepción de administración remota</p></td>
    <td style="border:1px solid black;"><p>Permite efectuar la configuración remota mediante el uso de herramientas.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado, a menos que desee poder administrar los equipos de forma remota con complementos MMC.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Permitir excepción de impresión y archivos compartidos</p></td>
    <td style="border:1px solid black;"><p>Especifica si se permite el tráfico generado al compartir impresoras y archivos.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado, a menos que los equipos en los que se ejecute Windows XP SP2 constituyan recursos locales de carácter compartido.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Permitir excepciones ICMP</p></td>
    <td style="border:1px solid black;"><p>Especifica los tipos de mensaje ICMP permitidos.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado, a menos que quiera utilizar el comando ping para solucionar problemas.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Permitir excepción de escritorio remoto</p></td>
    <td style="border:1px solid black;"><p>Especifica si el equipo puede aceptar una solicitud de conexión basada en escritorio remoto.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Permitir excepción del marco UPnP</p></td>
    <td style="border:1px solid black;"><p>Especifica si el equipo puede recibir mensajes UPnP no solicitados.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Prohibir notificaciones</p></td>
    <td style="border:1px solid black;"><p>Deshabilita las notificaciones.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Habilitar registro</p></td>
    <td style="border:1px solid black;"><p>Permite los registros de tráfico y configura los parámetros de los archivos de registro.</p></td>
    <td style="border:1px solid black;"><p>No configurado.</p></td>
    <td style="border:1px solid black;"><p>No configurado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Prohibir respuesta de unidifusión para solicitudes de difusión o multidifusión</p></td>
    <td style="border:1px solid black;"><p>Descarta los paquetes de unidifusión recibidos como respuesta a un mensaje de solicitud de difusión o de multidifusión.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    <td style="border:1px solid black;"><p>Habilitado.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Definir excepciones de puerto</p></td>
    <td style="border:1px solid black;"><p>Especifica el tráfico permitido en términos de TCP y UDP.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Permitir excepciones locales de puerto</p></td>
    <td style="border:1px solid black;"><p>Habilita la configuración local de excepciones de puerto.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    <td style="border:1px solid black;"><p>Deshabilitado.</p></td>
    </tr>  
    </tbody>  
    </table>
  
10. Haga doble clic en cada uno de los parámetros enumerados en la Tabla 2, haga clic en **Habilitado**, **Deshabilitado** o **No configurado** y, a continuación, haga clic en **Aceptar**.
  
#### Habilitación de excepciones para puertos
  
**Para habilitar excepciones para puertos**
  
1.  En el área de configuración de **Perfil de dominio** o de **Perfil estándar**, haga doble clic en **Firewall de Windows: Definir excepciones de puerto**. Aparecerá el siguiente cuadro de diálogo.
  
    ![](images/Cc875816.WFGP04(es-es,TechNet.10).gif)
  
2.  Seleccione **Habilitado** y, seguidamente, haga clic en **Mostrar**. Aparecerá el cuadro de diálogo **Mostrar contenido** (que se ilustra en la siguiente captura de pantalla).
  
    [![](images/Cc875816.WFGP05(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp06(es-es,technet.10).gif)
  
3.  Haga clic en **Agregar** y, seguidamente, aparecerá el cuadro de diálogo **Agregar elemento**. Escriba la información relativa al puerto que desee bloquear o habilitar. La sintaxis es la siguiente:
  
    puerto:transporte:ámbito:estado:nombre
  
    -   **puerto** es el número del puerto
  
    -   **transporte** es TCP o UDP
  
    -   **ámbito** es \* (para todos los equipos) o una lista de los equipos a los que se permite el acceso al puerto
  
    -   **estado** es "enabled" (para "habilitado") o "disabled" (para "deshabilitado")
  
    -   **nombre** es una cadena de texto que se utiliza como etiqueta de esta entrada
  
    El ejemplo que se muestra en la siguiente captura de pantalla se denomina WebTest y habilita el puerto TCP 80 para todas las conexiones.
  
    ![](images/Cc875816.WFGP06(es-es,TechNet.10).gif)
  
4.  Tras especificar la información, haga clic en **Aceptar** para cerrar el cuadro de diálogo **Agregar elemento**. Aparecerá el cuadro de diálogo **Mostrar contenido** (que se ilustra en la siguiente captura de pantalla).
  
    [![](images/Cc875816.WFGP07(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp08(es-es,technet.10).gif)
  
5.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Mostrar contenido**.
  
6.  Haga clic en **Aceptar** para cerrar **Propiedades de Firewall de Windows: Definir excepciones de puerto**.
  
#### Habilitación de excepciones para programas
  
**Para habilitar excepciones para programas**
  
1.  En el área de configuración de **Perfil de dominio** o de **Perfil estándar**, haga doble clic en **Firewall de Windows: Definir excepciones de programas**. Aparecerá el siguiente cuadro de diálogo.
  
    ![](images/Cc875816.WFGP08(es-es,TechNet.10).gif)
  
2.  Seleccione **Habilitado** y, seguidamente, haga clic en **Mostrar**. Aparecerá el cuadro de diálogo **Mostrar contenido** (que se ilustra en la siguiente captura de pantalla).
  
    [![](images/Cc875816.WFGP09(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp06(es-es,technet.10).gif)
  
3.  Haga clic en **Agregar** y, seguidamente, aparecerá el cuadro de diálogo **Agregar elemento**. Escriba la información relativa al programa que desee bloquear o habilitar. La sintaxis es la siguiente:
  
    ruta:ámbito:estado:nombre
  
    -   **ruta** es la ruta del programa y el nombre del archivo
  
    -   **ámbito** es \* (para todos los equipos) o una lista de los equipos a los que se permite el acceso al programa
  
    -   **estado** es "enabled" (para "habilitado") o "disabled" (para "deshabilitado")
  
    -   **nombre** es una cadena de texto que se utiliza como etiqueta de esta entrada
  
    El ejemplo que se muestra en la siguiente captura de pantalla se denomina Messenger y habilita el programa Windows Messenger, ubicado en %program files%\\messenger\\msmsgs.exe, para todas las conexiones.
  
    ![](images/Cc875816.WFGP10(es-es,TechNet.10).gif)
  
4.  Tras especificar la información, haga clic en **Aceptar** para cerrar el cuadro de diálogo **Agregar elemento**. Aparecerá el cuadro de diálogo **Mostrar contenido** (que se ilustra en la siguiente captura de pantalla).
  
    [![](images/Cc875816.WFGP11(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp12(es-es,technet.10).gif)
  
5.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Mostrar contenido**.
  
6.  Haga clic en **Aceptar** para cerrar **Propiedades de Firewall de Windows: Definir excepciones de programa**.
  
#### Configuración de opciones básicas de ICMP
  
**Para configurar opciones básicas de ICMP**
  
1.  En el área de configuración de **Perfil de dominio** o de **Perfil estándar**, haga doble clic en **Firewall de Windows: Permitir excepciones ICMP**. Aparecerá el siguiente cuadro de diálogo.
  
    ![](images/Cc875816.WFGP12(es-es,TechNet.10).gif)
  
2.  Seleccione **Habilitado** y, a continuación, la excepción o las excepciones ICMP adecuadas que desee habilitar. En el ejemplo de esta instantánea de pantalla se selecciona **Permitir petición de eco entrante**.
  
    También puede seleccionar **Deshabilitado** para deshabilitar una excepción ICMP o varias.
  
3.  Haga clic en **Aceptar** para cerrar **Propiedades de Firewall de Windows: Permitir excepciones ICMP**.
  
#### Registro de paquetes perdidos y conexiones efectuadas correctamente
  
**Para elaborar un registro de los paquetes perdidos y de las conexiones efectuadas correctamente**
  
1.  En el área de configuración de **Perfil de dominio** o de **Perfil estándar**, haga doble clic en **Firewall de Windows: Habilitar registro**. Aparecerá el siguiente cuadro de diálogo.
  
    ![](images/Cc875816.WFGP13(es-es,TechNet.10).gif)
  
2.  Seleccione **Habilitado**, **Registro de paquetes perdidos** y, seguidamente, **Registrar conexiones correctas**. Escriba un **nombre y una ruta del archivo de registro**; a continuación, deje **Límite de tamaño (KB)** para el tamaño del archivo de registro. Seguidamente, haga clic en **Aceptar**.
  
    **Nota**   Asegúrese de que el archivo de registro se guarda en una ubicación protegida para evitar la modificación deliberada o accidental.
  
3.  Cuando haya terminado de efectuar los cambios en la configuración de Firewall de Windows, cierre la consola.
  
    **Nota**   Cuando cierre la consola, se le preguntará si desea guardarla. Independientemente de si guarda la consola, se guardará la configuración de GPO.
  
4.  Si se le pregunta si desea guardar la configuración de la consola, haga clic en **No**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Aplicación de la configuración con GPUpdate
  
La utilidad GPUpdate actualiza la configuración de Directiva de grupo basada en Active Directory. Tras configurar Directiva de grupo, puede esperar a que se aplique la configuración a los equipos cliente mediante los ciclos de actualización estándar. De forma predeterminada, estos ciclos de actualización tienen una periodicidad de 90 minutos, con una variación aleatoria de +/- 30 minutos. Para actualizar inmediatamente Directiva de grupo, puede utilizar la utilidad GPUpdate.
  
#### Requisitos para llevar a cabo esta tarea
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión en un equipo con Windows XP SP2 que sea cliente del dominio de Active Directory; además, tendrá que utilizar una cuenta que sea miembro del grupo Usuarios de dominio.
  
#### Ejecución de GPUpdate
  
**Para ejecutar GPUpdate**
  
1.  En el escritorio de Windows XP SP2, haga clic en **Inicio** y, a continuación, en **Ejecutar**.
  
2.  En el cuadro de diálogo **Ejecutar**, escriba **cmd** y, a continuación, haga clic en **Aceptar**.
  
3.  En el símbolo del sistema, escriba **GPUpdate** y, a continuación presione Entrar. Aparecerá una pantalla similar a la siguiente:
  
    [![](images/Cc875816.WFGP14(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp15(es-es,technet.10).gif)
  
4.  Para cerrar el símbolo del sistema, escriba **Exit** y, a continuación, presione Entrar.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comprobación de la aplicación de la configuración de Firewall de Windows
  
**Nota**   Al utilizar Directiva de grupo para configurar Firewall de Windows, puede impedir que los administradores locales tengan acceso a algunos elementos de la configuración. Si ha impedido el acceso, algunas fichas y opciones del cuadro de diálogo de Firewall de Windows no estarán disponibles en equipos locales del usuario.
  
#### Requisitos para llevar a cabo esta tarea
  
Para completar esta tarea, necesitará lo que se especifica a continuación:
  
-   **Credenciales**. Debe haber iniciado sesión en un equipo con Windows XP SP2 que sea cliente del dominio de Active Directory; además, tendrá que utilizar una cuenta que sea miembro del grupo Usuarios de dominio.
  
**Para comprobar que la configuración de Firewall de Windows se ha aplicado**
  
1.  En el escritorio de Windows XP SP2, haga clic en **Inicio** y, a continuación, en **Panel de control**.
  
2.  En **Elija una categoría**, haga clic en **Centro de seguridad**. Aparecerá una pantalla similar a la siguiente.
  
    [![](images/Cc875816.WFGP15(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875816.fwgrpp16(es-es,technet.10).gif)
  
3.  En **Administrar la configuración de seguridad para**, haga clic en **Firewall de Windows**.
  
4.  Haga clic en las fichas **General**, **Excepciones** y **Opciones avanzadas**, y compruebe que la configuración de Directiva de grupo también se aplica a Firewall de Windows en el equipo cliente.
  
Si los parámetros de configuración no se han aplicado, debe solucionar los problemas de la aplicación de Directiva de grupo. Para ello, consulte el siguiente documento:
  
-   "[Troubleshooting Group Policy in Microsoft Windows Server](http://go.microsoft.com/fwlink/?linkid=35481)", disponible en el Centro de descarga de Microsoft, en http://go.microsoft.com/fwlink/?linkid=35481.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información relacionada
  
Para obtener más información acerca del servidor de seguridad de Windows XP SP2, consulte los siguientes documentos:
  
-   "[Deploying Firewall de Windows Settings for Microsoft Windows XP with Service Pack 2](http://go.microsoft.com/fwlink/?linkid=35303)", disponible en el Centro de descarga de Microsoft, en http://go.microsoft.com/fwlink/?linkid=35303.
  
-   "[Understanding Windows Firewall, Introduction](http://www.microsoft.com/spain/windowsxp/using/security/internet/sp2_wfintro.mspx)", disponible en el sitio Web de Microsoft Windows XP, en http://www.microsoft.com/spain/windowsxp/using/security/internet/sp2\_wfintro.mspx.
  
Para obtener más información acerca de la seguridad de Windows XP SP2, consulte el siguiente documento:
  
-   La guía [*Guía de seguridad de Windows XP*](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc), disponible en el sitio Web del Centro de descarga de Microsoft, en http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/GuideforWinXPProSP2inSMB.doc.
  
Para obtener definiciones de términos relacionados con la seguridad, consulte el siguiente documento:
  
-   El [Glosario de seguridad de Microsoft](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx), disponible en el sitio Web de Microsoft, en http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener Cómo configurar Firewall de Windows en un entorno de pequeñas empresas mediante Directiva de grupo](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx)
  
[](#mainsection)[Principio de la página](#mainsection)
