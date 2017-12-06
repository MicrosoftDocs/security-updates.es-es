---
TOCTitle: Protección de los equipos cliente contra los ataques de red
Title: Protección de los equipos cliente contra los ataques de red
ms:assetid: 'f3e96a10-4eb6-4a41-8040-d5af55edf694'
ms:contentKeyID: 20200233
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875823(v=TechNet.10)'
---

Protección de los equipos cliente contra los ataques de red
===========================================================

Actualizado: julio 21, 2006

##### En esta página

[](#efaa)[Introducción](#efaa)  
[](#eeaa)[Antes de comenzar](#eeaa)  
[](#edaa)[Windows Live OneCare](#edaa)  
[](#ecaa)[Windows Defender](#ecaa)  
[](#ebaa)[Firewall de Windows](#ebaa)  
[](#eaaa)[Información relacionada](#eaaa)

### Introducción

Muchas organizaciones dependen en gran medida de los servidores de seguridad de red para proteger sus estaciones de trabajo y servidores de las amenazas de Internet. Este enfoque se conoce como “duro por fuera, blando por dentro”. Microsoft recomienda el uso de un servidor de seguridad de red y de las características de seguridad de la estación de trabajo descritas en este documento. Este enfoque proporciona un tipo de seguridad “duro por dentro y por fuera” más adecuado. El hecho de que se hayan detectado gusanos que hayan logrado franquear los servidores de seguridad de las organizaciones demuestra que la utilización de dichos servidores no basta.

Los atacantes crean gusanos y virus que pueden destruir los datos almacenados en los equipos cliente, o provocar la pérdida o el robo de la información que contienen. Estos ataques pueden causar la pérdida de información privada y secretos empresariales, impedir que los equipos puedan iniciarse e incluso servir de plataforma para el lanzamiento de ataques a otros equipos. En consecuencia, constituyen una amenaza muy real para los equipos conectados a Internet.

La mayoría de los métodos de ataque intentan aprovecharse de los problemas de seguridad más conocidos de los equipos. La aplicación de las siguientes características puede proporcionar un nivel de protección más elevado para los equipos cliente con el sistema operativo Microsoft® Windows® XP con Service Pack 2 (SP2):

-   Servidor de seguridad personal (Firewall de Windows)

-   Actualización de Service Packs y revisiones (Actualización automática)

-   Software antivirus con firmas actualizadas (Windows Live OneCare)

-   Software contra el spyware con firmas actualizadas (Windows Defender)

#### Objetivo de este documento

Una vez leído este documento, el lector debería estar lo suficientemente familiarizado con las herramientas y características disponibles de Microsoft para aumentar el nivel de seguridad de los equipos cliente con Windows XP SP2 dentro de una red SMB.

[](#mainsection)[Principio de la página](#mainsection)

### Antes de comenzar

Deberá tener en cuenta la siguiente información antes de aplicar las recomendaciones que se detallan en este documento.

#### Credenciales necesarias

La mayoría de las tareas descritas en este documento requieren una cuenta administrativa. Un usuario normal no podrá ejecutar dichas tareas.

#### Recomendaciones

Microsoft recomienda la actualización de todas las estaciones de trabajo de Windows a Windows XP SP2. Este sistema operativo contiene las características de seguridad más actuales; de hecho, muchas de ellas ya están habilitadas de forma predeterminada.

Además, Microsoft recomienda la actualización de todas las versiones de las instalaciones existentes de Internet Explorer a la versión más actual.

#### Valores predeterminados

Los valores predeterminados de los parámetros de seguridad de las herramientas que aparecen en este documento son los valores recomendados por Microsoft. Estas recomendaciones se realizaron para equilibrar los niveles de funcionalidad y seguridad de Windows XP SP2. Muchas organizaciones cuentan con requisitos de seguridad específicos; todas estas características de seguridad pueden configurarse o deshabilitarse.

[](#mainsection)[Principio de la página](#mainsection)

### Windows Live OneCare

Microsoft ha elaborado Windows Live OneCare, un servicio de protección de actualización automática para equipos que se ejecuta en un segundo plano. Dicho servicio proporciona una protección constante contra virus, piratas informáticos y otras amenazas, y ayuda a mantener el equipo a punto y a realizar copias de seguridad para documentos importantes. Para obtener más detalles, consulte [Windows Live OneCare](http://www.microsoft.com/spain/athome/security/update/onecare_live.mspx) en www.microsoft.com/spain/athome/security/update/onecare\_live.mspx.

Windows Live OneCare proporciona una única consola para la comprobación del estado de varios servicios relacionados con la seguridad de su estación de trabajo de Windows XP. La pantalla única describe el estado de la protección antivirus, del sistema, de los niveles de revisión y de la última copia de seguridad de datos.

#### Protección antivirus

Los virus informáticos son programas de software diseñados con el objeto de interferir de forma deliberada en las operaciones del equipo. Pueden registrar, dañar o eliminar datos, propagarse a otros equipos y extenderse por Internet, y, además, suelen ralentizar las operaciones, así como causar otros problemas en el proceso.

Al igual que los virus humanos, que tienen distintos grados de gravedad desde el Ébola hasta la gripe de 24 horas, los virus informáticos varían desde los ligeramente molestos a los altamente destructivos. Además, adoptan nuevas y diferentes formas. La parte positiva es que, con un poco de prevención y unos conocimientos mínimos, tendrá menos probabilidades de ser víctima de los virus y podrá reducir su impacto.

Con Windows Live OneCare, las firmas antivirus y las revisiones de seguridad del sistema operativo se actualizan automáticamente, con lo que su equipo queda actualizado sin necesidad de llevar a cabo una intervención manual.

Para obtener una [lista de los proveedores de software](http://support.microsoft.com/kb/49500) que, además, proporcionen software antivirus compatible con Windows XP, consulte http://support.microsoft.com/kb/49500.

#### Supervisión del servidor de seguridad

Firewall de Windows trabaja en un único equipo y le ayuda a protegerlo del ataque de piratas informáticos al enviar o recibir archivos. Windows Live OneCare supervisa continuamente las acciones del Firewall de Windows.  

#### Windows Defender

Windows Defender, que puede descargarse de Microsoft, es un programa que ayuda a proteger la información privada de los equipos de ataques provenientes de Internet. Windows Live OneCare supervisa el estado de Windows Defender.

#### Actualizaciones

Windows Live OneCare se actualiza automáticamente para garantizar que la protección antivirus, la protección del servidor de seguridad y la protección contra spyware esté siempre actualizada y lista para ayudarle a proteger su equipo de las últimas amenazas.

#### Copia de seguridad y restauración de archivos

Con Windows Live OneCare puede hacer copias de archivos y documentos importantes, y almacenarlos en un CD, DVD o disco duro externo en caso de emergencia. Tendrá la opción de hacerlo manualmente o dejar que Windows Live OneCare lo haga de forma automática para que no tenga que acordarse de realizar copias de seguridad de sus archivos y documentos periódicamente. Además, Windows Live OneCare le ayudará a restaurar los archivos con copia de seguridad en su equipo en caso de que ocurra algún problema.

[](#mainsection)[Principio de la página](#mainsection)

### Windows Defender

El spyware suele asociarse con el software que muestra anuncios publicitarios (llamado adware) o con el que hace seguimientos de la información personal o confidencial. No obstante, esto no quiere decir que todo el software que proporcione anuncios o realice seguimientos de las actividades en línea sea nocivo. Por ejemplo, es posible inscribirse para recibir servicios musicales gratuitos y "pagar" por esto aceptando la recepción de los anuncios pertinentes. Si el usuario entiende y acepta los términos del contrato, se supondrá que éste considera que es un intercambio justo. Además, es posible que el usuario permita que la empresa en cuestión realice un seguimiento de sus actividades en línea para determinar qué tipo de anuncios debe mostrarle.

Otros tipos de software no deseado pueden realizar cambios en el equipo que pueden resultar molestos y provocar que éste se ralentice o se bloquee. Estos programas tienen la capacidad de cambiar la página de inicio o la de búsqueda del explorador Web o de añadir componentes adicionales al explorador que ni se necesitan ni se desean. Además, suelen dificultar el restablecimiento de la configuración inicial tal y como estaba antes. Estos programas no deseados suelen llamarse también spyware.

Windows Defender (Beta2) es una tecnología de seguridad que ayuda a proteger a los usuarios de Windows del spyware y de otros tipos de software potencialmente no deseados. El spyware conocido que obtenga acceso a su equipo puede detectarse y eliminarse, lo que contribuye a reducir sus efectos negativos, incluida la ralentización del equipo, la aparición de anuncios emergentes molestos, los cambios no deseados de la configuración de Internet y el uso no autorizado de la información privada. La protección continua mejora la seguridad de la exploración de Internet mediante la protección de más de 50 vías por las que el spyware puede introducirse en el equipo. Los integrantes de la comunidad de ámbito mundial SpyNet™ desempeñan una labor clave a la hora de determinar qué programas sospechosos pueden clasificarse como spyware. En consecuencia, los investigadores de Microsoft desarrollan rápidamente métodos para contrarrestar dichas amenazas y las actualizaciones resultantes se descargan automáticamente en los equipos para que estén totalmente al día.

Puede descargarse [Windows Defender](http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx) desde http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx. La versión actual es la Beta 2. El nombre del archivo es WindowsDefender.msi y ocupa unos 5,5 MB. (El nombre y el tamaño del archivo pueden modificarse tras el lanzamiento de la versión completa.)

Siga los pasos que se indican a continuación para instalar Windows Defender (Beta 2) una vez descargado.

1.  Al descargar Windows Defender (Beta 2), aparecerá el siguiente cuadro de diálogo. Haga clic en **Ejecutar**.

    ![](images/Cc875823.PCNA01(es-es,TechNet.10).gif)

2.  A continuación, aparecerá la pantalla **Éste es el Asistente para la instalación de Windows Defender**. Haga clic en **Siguiente**.

    ![](images/Cc875823.PCNA02(es-es,TechNet.10).gif)

3.  Aparecerá el **Contrato de licencia de Windows Defender** (que se muestra en la siguiente captura de pantalla). Revise los términos del contrato.

    Para continuar con la instalación, seleccione **Acepto los términos del contrato de licencia** y haga clic en **Siguiente**.

    ![](images/Cc875823.PCNA03(es-es,TechNet.10).gif)

4.  En la pantalla **Ayudar a proteger Windows** (que se muestra en la siguiente captura de pantalla), seleccione **Utilizar la configuración recomendada**. Haga clic en el botón **Declaración de privacidad** si desea leerla. A continuación, haga clic en **Siguiente**.

    ![](images/Cc875823.PCNA04(es-es,TechNet.10).gif)

5.  En la pantalla **Tipo de instalación** (que se muestra en la siguiente captura de pantalla), seleccione **Completa** y haga clic en **Siguiente**.

    ![](images/Cc875823.PCNA05(es-es,TechNet.10).gif)

6.  Cuando se muestre la pantalla **Preparado para instalar Windows Defender**, haga clic en el botón **Instalar** para comenzar la instalación.

    ![](images/Cc875823.PCNA06(es-es,TechNet.10).gif)

7.  Una vez finalizado el proceso de instalación, debería aparecer la pantalla **Instalación finalizada de Windows Defender**.

    Asegúrese de que la opción **Buscar definiciones actualizadas y realizar una exploración rápida ahora** esté seleccionada, y haga clic en **Finalizar**.

    **Nota**   Se requiere una conexión a Internet para este paso.

    ![](images/Cc875823.PCNA07(es-es,TechNet.10).gif)

8.  Cuando aparezca la siguiente pantalla, haga clic en el botón **Comprobar actualizaciones** para obtener las actualizaciones más recientes.

    [![](images/Cc875823.PCNA08(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875823.pcna08_big(es-es,technet.10).gif)

Para más información sobre esto y sobre las características avanzadas de Windows Defender (Beta 2), consulte el sitio Web de [Windows Defender (Beta 2)](http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx) en http://www.microsoft.com/spain/athome/security/spyware/software/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Firewall de Windows

Un servidor de seguridad es un sistema de seguridad que actúa como frontera protectora entre una red y el mundo exterior. Windows XP SP2 incluye el Firewall de Windows, un software que funciona prácticamente de la misma manera en todos los equipos cliente individuales.

Firewall de Windows viene instalado en Windows XP Professional SP2 y cuenta con múltiples opciones de configuración. Se habilita de forma predeterminada y ayuda a proteger el equipo contra los ataques de red. Además, Windows Live OneCare también se encarga de la supervisión de Firewall de Windows y proporciona una única consola para la comprobación del estado global de la seguridad del equipo. A continuación, le mostraremos la manera de cambiar la configuración del Firewall de Windows a través del Centro de seguridad de Windows, que se encuentra en el Panel de control.

**Nota**   Firewall de Windows no está diseñado para sustituir a la funcionalidad del servidor de seguridad de la red. La red de Windows está habilitada y permite pasar el Firewall de Windows, lo que implica que el usuario podrá seguir comunicándose con otros equipos de la red, imprimir y obtener acceso a recursos compartidos de red. No obstante, se recomienda contar con un servidor de seguridad de la red para proteger los puertos que se abren con estas funciones.

#### Configuración general

Los parámetros generales de Firewall de Windows permiten configurar estas opciones:

-   **Activado** (recomendado).

-   **Desactivado** (no se recomienda). Si desactiva Firewall de Windows, su equipo será más vulnerable frente a ataques de virus, gusanos o intrusos.

1.  Para abrir el Centro de seguridad de Windows, haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**. Aparecerá la siguiente pantalla.

    [![](images/Cc875823.PCNA09(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875823.prot_clients_net_attacks_01(es-es,technet.10).jpg)

2.  En la sección **Elija una categoría**, haga clic en **Centro de seguridad**. Aparecerá la pantalla **Centro de seguridad de Windows** (que se muestra en la siguiente captura de pantalla).

    [![](images/Cc875823.PCNA10(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875823.cfgfwa02_big(es-es,technet.10).gif)

#### Notificaciones de configuración

Firewall de Windows muestra un cuadro de diálogo de notificación de forma predeterminada siempre que éste bloquee un programa que intente establecer una comunicación desde su equipo a otro. El cuadro de diálogo es similar al que se muestra en la siguiente captura de pantalla:

![](images/Cc875823.PCNA11(es-es,TechNet.10).gif)

Dicho cuadro de diálogo indica qué programa se ha bloqueado y permite seleccionar si se desea admitirlo o no. Las opciones disponibles son las siguientes:

-   **Mantener el bloqueo**. Utilice esta opción para que el programa no acepte las conexiones desde Internet o desde la red sin permiso.

-   **Desbloquear**. Utilice esta opción para incluir el programa en la lista de excepciones de Firewall de Windows.

-   **Preguntar más tarde**. Utilice esta opción si no sabe si bloquear el programa o no. Esta opción mantiene bloqueado el programa para una mayor seguridad. La próxima vez que se bloquee el programa, volverá a aparecer este mensaje.

#### Descripción de los puertos de aplicaciones

Un puerto es un punto de conexión que utiliza un programa para comunicarse con otros programas, especialmente con programas que se ejecutan en otros equipos. Los puertos se identifican mediante la combinación de un número de puerto y un transporte. Existen puertos específicos asociados a cada tipo de aplicación o servicio. Por ejemplo, el puerto estándar para un servidor Web es el puerto TCP 80, el puerto estándar para un servidor de Protocolo de transferencia de archivos (FTP) es el puerto TCP 21 y el servicio de Windows Server que permite compartir archivos e impresión recibe los mensajes en cuatro puertos: los puertos UDP 137 y 138, y los puertos TCP 139 y 445.

Firewall de Windows activa el bloqueo de todos los puertos para evitar la recepción de mensajes entrantes no solicitados. Esta función protege al equipo, ya que bloquea los mensajes que suele utilizar el código malicioso para obtener acceso a él. Firewall de Windows no interfiere con la mayoría del software comercial legítimo, ya que, como norma general, este tipo de software no envía mensajes no solicitados a los equipos cliente.

Dado que los servidores de seguridad restringen la comunicación entre Internet y el equipo, es posible que deba realizar ajustes en la configuración para otros programas que requieran una conexión abierta. Además, pueden realizarse excepciones para estos programas de manera que puedan comunicarse a través del Firewall de Windows.

#### Riesgos de la admisión de excepciones

Cada vez que se admite una excepción para que un programa pueda comunicarse atravesando el Firewall de Windows, el equipo se va haciendo más y más vulnerable. De hecho, cuantas más excepciones se admitan, menor será la eficacia del servidor de seguridad. Los piratas informáticos suelen utilizar programas de software que exploran la red en busca de equipos con conexiones desprotegidas. Si su equipo admite muchas excepciones y tiene muchos puertos abiertos, será cada vez más vulnerable.

Para reducir el riesgo de ataques, haga lo siguiente:

-   Admita una excepción sólo si la necesita.

-   No admita nunca una excepción para un programa que no reconozca.

-   Elimine las excepciones que ya no necesite.

#### Admisión de excepciones a pesar de los riesgos

Es posible que, en ocasiones, desee admitir que alguien se conecte a su equipo a pesar del riesgo que supone, como, por ejemplo, si desea recibir un archivo enviado a través de un programa de mensajería instantánea de Internet.

Si está intercambiando mensajes instantáneos con alguien que quiera enviarle un archivo (por ejemplo, una hoja de cálculo), Firewall de Windows mostrará un mensaje que le preguntará si desea desbloquear la conexión y permitir la transferencia de archivos. De la misma manera, también podrá agregar el programa de mensajería instantánea como una excepción, de manera que Firewall de Windows admita la conexión a su equipo.

Para agregar un programa a la lista de excepciones, lleve a cabo los pasos que se especifican en el siguiente procedimiento.

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Panel de control**.

2.  En Panel de control, haga clic en **Centro de seguridad** y, a continuación, haga clic en **Firewall de Windows**.

3.  En la ficha **Excepciones**, que aparece en **Programas y servicios** (y que se muestra en la siguiente captura de pantalla), active la casilla de verificación del programa o servicio que desee permitir. A continuación, haga clic en **Aceptar**.

    ![](images/Cc875823.PCNA12(es-es,TechNet.10).gif)

Si el programa (o servicio) que desea admitir no aparece en la lista, haga lo siguiente:

1.  Haga clic en **Agregar programa**.

2.  En el cuadro de diálogo **Agregar programa**, seleccione el programa que desea agregar y haga clic en **Aceptar**.

3.  Haga clic en **Aceptar**.

**Sugerencia**   Si el programa (o servicio) que desea admitir no aparece en el cuadro de diálogo **Agregar programa**, haga clic en **Examinar**, localice el programa que desea agregar y haga doble clic sobre él. (Los programas suelen almacenarse en la carpeta Archivos de programa del equipo.) El programa aparecerá en **Programas** en el cuadro de diálogo **Agregar programa**.

#### Apertura de puertos como último recurso

Si sigue sin encontrar el programa, puede abrir un puerto. Los puertos son como pequeñas puertas dentro del servidor de seguridad que permiten el paso de las comunicaciones. Para especificar qué puerto deberá abrirse, haga clic en **Agregar puerto** en la ficha **Excepciones**. (Recuerde cerrar los puertos abiertos cuando ya no necesite utilizarlos.)

A continuación, se exponen las razones por las que es preferible agregar una excepción en lugar de abrir un puerto:

-   Es más fácil de hacer.

-   No necesita saber el número de puerto que tiene que utilizarse.

-   Agregar una excepción es más seguro que abrir un puerto, ya que el servidor de seguridad sólo se abre cuando el programa espera recibir una conexión.

#### Opciones avanzadas

Los usuarios expertos pueden abrir puertos para conexiones individuales y configurar su alcance para reducir las posibilidades de que haya intrusos que puedan conectarse al equipo o la red. Para ello, abra Firewall de Windows, haga clic en la ficha **Opciones avanzadas** y utilice los parámetros que se hallan en **Configuración de conexión de red**.

Para obtener más información sobre las características avanzadas, consulte "[Understanding Windows Firewall](http://www.microsoft.com/spain/windowsxp/using/security/internet/sp2_wfintro.mspx)" en www.microsoft.com/spain/windowsxp/using/security/internet/sp2\_wfintro.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Información relacionada

Si desea obtener más información acerca de la apertura de puertos, consulte:

-   “[Puertos de red clave utilizados por productos de servidor de Microsoft](http://www.microsoft.com/spain/empresas/seguridad/articulos/ref_net_ports_ms_prod.mspx)” en el sitio Web de Centro para Empresas y Profesionales de Microsoft, en http://www.microsoft.com/spain/empresas/seguridad/articulos/ref\_net\_ports\_ms\_prod.mspx.

-   "[Números de puerto](http://www.iana.org/assignments/port-numbers)", un documento del sitio Web de Internet Assigned Numbers Authority que puede encontrarse en www.iana.org/assignments/port-numbers.

Si desea obtener información general adicional acerca de los servidores de seguridad, consulte:

-   "[Cambios de funcionalidad en Service Pack 2 de Microsoft Windows XP - Parte 2: Tecnologías para la protección de redes](http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx)" en el sitio Web de Microsoft TechNet en http://www.microsoft.com/technet/prodtechnol/winxppro/es/maintain/sp2netwk.mspx.

Para obtener más información sobre la seguridad de Windows XP SP2, consulte:

-   [*Guía de seguridad de Windows XP*](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc) en el sitio Web del Centro de descarga de Microsoft en http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/GuideforWinXPProSP2inSMB.doc.

Para obtener definiciones de los términos relacionados con la seguridad, consulte:

-   El [Glosario de seguridad de Microsoft](http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx) del sitio Web de Microsoft en http://www.microsoft.com/spain/technet/seguridad/recursos/glosario/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener Protección de los equipos cliente contra los ataques de red](http://download.microsoft.com/download/a/e/2/ae21ee34-b553-44e6-9160-d0addca7f3ae/guideforwinxpprosp2insmb.doc)

[](#mainsection)[Principio de la página](#mainsection)
