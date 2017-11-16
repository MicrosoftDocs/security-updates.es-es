---
TOCTitle: 'Guía fundamental de investigación de equipos para Windows: Apéndice: Recursos'
Title: 'Guía fundamental de investigación de equipos para Windows: Apéndice: Recursos'
ms:assetid: 'a9a5c2a9-cce3-4edb-a92c-10983899240a'
ms:contentKeyID: 20200214
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162853(v=TechNet.10)'
---

Guía fundamental de investigación de equipos para Windows
=========================================================

### Apéndice: Recursos

Publicado: enero 11, 2007

En este apéndice se ofrece información acerca de varios recursos que puede utilizar para realizar una investigación de equipo.

##### En esta página

[](#efaa)[Preparación de la organización para una investigación de equipo](#efaa)
[](#eeaa)[Hojas de cálculo y Muestras](#eeaa)
[](#edaa)[Informar de crímenes relacionados con equipos](#edaa)
[](#ecaa)[Aprendizaje](#ecaa)
[](#ebaa)[Tools](#ebaa)

### Preparación de la organización para una investigación de equipo

Para preparar a su organización para una investigación interna de equipo, debe reunir un kit de herramientas de investigación de equipos disponible cómodamente que incluya software y dispositivos que se puedan utilizar para obtener evidencias. Este kit de herramientas puede contener un equipo portátil con herramientas de software adecuadas, diferentes sistemas operativos y revisiones, medios de aplicación, dispositivos de copia de seguridad, medios en blanco, equipos de red básicos y cables. La preparación de este kit de herramientas puede ser un proceso continuo, a medida que se vayan necesitando diferentes herramientas y recursos, en función de las investigaciones que deba llevar a cabo.

Utilice las instrucciones siguientes para crear y usar un kit de herramientas de investigación de equipo:

-   Decida qué herramientas prevé utilizar antes de iniciar la investigación. Además de Microsoft® Windows® Sysinternals y otras herramientas de Windows mencionadas en este documento, el kit de herramientas incluirá software forense dedicado, como Encase de [Guidance Software](http://www.guidancesoftware.com), Forensic Toolkit (FTK) de [AccessData](http://www.accessdata.com) o ProDiscover de [Technology Pathways](http://www.techpathways.com/).

-   Asegúrese de archivar y conservar las herramientas. Es posible que necesite una copia de seguridad de las herramientas de investigación de equipo y el software que utilice en la investigación para demostrar cómo recopiló y analizó los datos.

-   Haga una lista de todos los sistemas operativos que probablemente examinará, y asegúrese de que tiene las herramientas necesarias para examinarlos todos. Por ejemplo, puede utilizar herramientas de Windows Sysinternals (descritas más adelante en este apéndice) como PsInfo, PsLogList y ProcessExplorer para examinar equipos que ejecuten Windows XP y Windows Server® 2003.

-   Incluya una herramienta para recopilar y analizar metadatos.

-   Incluya una herramienta para crear copias bit a bit y lógicas.

-   Incluya herramientas para reunir y examinar datos volátiles, como el estado del sistema. Algunos ejemplos de herramientas de Windows Sysinternals son ListDLLs, LogonSessions, PendMoves, Autoruns y ProcessExplorer. Las herramientas de Windows son Systeminfo, Ipconfig, Netstat y Arp.

-   Incluya una herramienta para generar sumas de comprobación y firmas digitales en archivos y otros datos, como la herramienta Comprobador de Integridad de CHECKSUM de Archivo (FCIV). Esta herramienta está disponible en el artículo 841290 de Microsoft Knowledge Base, [Disponibilidad y descripción de la herramienta Comprobador de Integridad de CHECKSUM de Archivo](http://support.microsoft.com/default.aspx?scid=841290).

-   Si necesita reunir evidencias físicas, incluya una cámara digital en el kit de herramientas.

Además, compruebe que el kit de herramientas cumple los criterios siguientes:

-   Las herramientas de obtención de datos se muestran con fines de precisión. Normalmente, resulta más fácil demostrar la precisión si se utiliza un software forense conocido.

-   Las herramientas no modifican el tiempo de acceso de los archivos.

-   El dispositivo de almacenamiento del examinador es estéril desde un punto de vista forense, es decir, que la unidad de disco no contiene datos antes de utilizarse. Para determinar si un dispositivo de almacenamiento es estéril desde un punto de vista, ejecute una suma de comprobación en el dispositivo. Si la suma de comprobación devuelve todo ceros, la unidad no contiene datos.

-   El hardware y las herramientas del examinador sólo se utilizan para el proceso de investigación de equipos, no para otras tareas.

[](#mainsection)[Principio de la página](#mainsection)

### Hojas de cálculo y Muestras

En la tabla siguiente se proporciona una lista de hojas de cálculo y muestras que se pueden utilizar durante la investigación de equipo. Algunos de estos recursos están disponibles como documentos de Word separados y se incluyen en el archivo del Centro de descarga de Microsoft del que extrajo esta guía. Los otros están disponibles a través de un vínculo al sitio Web del Instituto Nacional de Justicia.

**Tabla A.1. Hojas de cálculo y Muestras**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de documento</th>
<th style="border:1px solid black;" >Ubicación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Hoja de cálculo: Chain of Custody Log Documentation.doc
Hoja de cálculo: Impact Analysis.doc
Muestra: Internal Investigation Report.doc</td>
<td style="border:1px solid black;">Vínculo a la <a href="http://go.microsoft.com/fwlink/?linkid=80345">Guía fundamental de investigación de equipos para Windows</a> en el Centro de descarga de Microsoft.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Evidencia de equipo
Evidencia de disco duro
Removable media (Medios extraíbles)</td>
<td style="border:1px solid black;">Apéndice C. Hojas de cálculo de muestra en <a href="http://www.ojp.usdoj.gov/nij/pubs-sum/199408.htm">Forensic Examination of Digital Evidence: A Guide for Law Enforcement</a> del Instituto Nacional de Justicia, una agencia del Departamento de Justicia de EE.UU.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Informar de crímenes relacionados con equipos
  
![](images/Cc162853.note(es-es,TechNet.10).gif)**Nota:**
  
Gran parte de la información de esta sección procede de la página [Reporting Computer, Internet-Related, or Intellectual Property Crime](http://www.cybercrime.gov/reporting.htm) (Informar de crímenes informáticos, relacionados con Internet o de propiedad intelectual) de la sección Computer Crime & Intellectual Property (Crimen informático y propiedad intelectual) del sitio Web del Departamento de Justicia de los Estados Unidos.
  
Consulte primero con sus abogados para determinar si es necesario informar de crímenes informáticos específicos a las autoridades competentes del ámbito local, estatal, federal o internacional, en función del alcance del crimen. Los más probable es que las autoridades locales o estatales sean las primeras con las que deba ponerse en contacto. Si se trata de un crimen informático federal, es posible que deba notificar el crimen a las oficinas locales del cuerpo de seguridad federal. Tal como se ha mencionado previamente, esta guía está diseñada para el uso en los Estados Unidos.
  
Las autoridades judiciales competentes de los Estados Unidos que investigan crímenes relacionados con Internet son las siguientes:
  
-   [Oficina Federal de Investigación (FBI)](http://www.fbi.gov/)
  
-   [Servicio Secreto de Estados Unidos (USSS)](http://www.secretservice.gov)
  
-   [Oficina de Inmigración y Aduanas de EE.UU. (ICE)](http://www.ice.gov/)
  
-   [Servicio de Inspección Postal de EE.UU.](http://www.usps.com/postalinspectors)
  
-   [Oficina de Alcohol, Tabaco, Armas de Fuego y Explosivos (ATF)](http://www.atf.gov/)
  
-   [Administración de Control de Drogas (DEA)](http://www.dea.gov/)
  
Estas organizaciones tienen oficinas en varios puntos de los Estados Unidos. Encontrará la información de contacto en los directorios telefónicos locales o en Internet. Generalmente, los crímenes federales se pueden notificar por teléfono en la oficina local de una autoridad judicial competente a un agente de reclamación de obligaciones. Si la organización se ha unido a la ElectrInic Crimes Task Force (ECTF), [InfraGard](http://www.infragard.net/) o la [Asociación Internacional contra el crimen tecnológico (HTCIA)](http://www.htcia.org/), puede que ya conozca a la persona de contacto adecuada. El contacto con una persona conocida y que conoce a la organización simplifica el proceso de informe.
  
Muchas agencias cuentan con agentes formados especializados en casos de piratería informática.
  
#### Autoridades judiciales locales competentes
  
En algunas situaciones, la mejor opción es ponerse en contacto con una autoridad judicial local competente. Es posible que estas organizaciones o unidades operativas contra crímenes tecnológicos tengan personal formado que pueda investigar un incidente. Las organizaciones que cuentan con personal formado son [REACT Task Force](http://www.reacttf.org), que trabaja en el área de la bahía de San Francisco, [CATCH Team](http://www.catchteam.org), que opera en la región de San Diego, y otros cuerpos policiales.
  
La información de la tabla siguiente le puede ayudar a determinar la autoridad federal con la que debe ponerse en contacto para ciertos tipos de crimen.
  
**Tabla A.2. Autoridades judiciales competentes para diferentes tipos de crímenes**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de crimen</th>
<th style="border:1px solid black;" >Organizaciones adecuadas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Asuntos de explotación de menores y fraude en Internet relacionados con el correo</td>
<td style="border:1px solid black;"><a href="http://www.usps.com/postalinspectors">Servicio de Inspección Postal de EE.UU.</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Explotación o pornografía de menores</td>
<td style="border:1px solid black;">Policía local
<a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Intrusión de equipos (piratería)</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
<a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Piratería de Copyright (software, películas, grabación de sonido)</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Falsificación de divisas</td>
<td style="border:1px solid black;"><a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Robo de identidad o datos de clientes</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
<a href="http://www.secretservice.gov/financial_crimes.shtml">Servicio Secreto de Estados Unidos (División de crímenes financieros)</a>
<a href="https://rn.ftc.gov/pls/dod/wsolcq$.startup?z_org_code=pu01">Formulario de quejas del consumidor FTC</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Amenazas de bomba en Internet</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Oficina local de la <a href="http://www.atf.gov/field/index.htm">división de ATF</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Fraude en Internet y correo no deseado</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
<a href="http://www.secretservice.gov/financial_crimes.shtml">Servicio Secreto de Estados Unidos (División de crímenes financieros)</a>
<a href="https://rn.ftc.gov/pls/dod/wsolcq$.startup?z_org_code=pu01">Formulario de quejas del consumidor FTC</a>
Si se trata de fraude de títulos o correo electrónico no deseado relacionado con inversiones, <a href="http://www.sec.gov/complaint.shtml">Centro de reclamaciones de la SEC y consejos informativos</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acoso de Internet</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tráfico de contraseñas</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
<a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Robo de secretos comerciales</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Falsificación de marcas</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a>
<a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a>
Unidad operativa o cuerpo policial local contra crímenes tecnológicos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tráfico de explosivos, dispositivos incendiarios o armas de fuego en Internet</td>
<td style="border:1px solid black;"><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a>
Oficina local de la <a href="http://www.atf.gov/field/index.htm">división de ATF</a></td>
</tr>
</tbody>
</table>
 

[](#mainsection)[Principio de la página](#mainsection)

### Aprendizaje

Es recomendable que algunos de los miembros del equipo de respuesta a incidentes asistan a un curso de formación formal sobre investigación de equipos. Sin la formación pertinente, es improbable que el equipo lleve a cabo una investigación eficaz. De hecho, los examinadores sin conocimientos podrían afectar negativamente a la investigación por destrucción accidental de evidencias volátiles.

Para obtener una lista de organizaciones no lucrativas, organizaciones, autoridades judiciales federales e instituciones académicas que ofrecen formación sobre análisis forense de equipos, consulte el "Appendix G. Training Resources List" (Apéndice G. Lista de recursos de formación) de [Forensic Examination of Digital Evidence: A Guide for Law Enforcement](http://www.ojp.usdoj.gov/nij/pubs-sum/199408.htm) del Instituto Nacional de Justicia, una agencia del Departamento de Justicia de EE.UU.

[](#mainsection)[Principio de la página](#mainsection)

### Tools

Cada investigación será diferente. Las herramientas que utilice deben ser apropiadas para obtener la información que busca, pero siempre es recomendable recoger más evidencias de las necesarias.

En esta sección se proporciona información acerca de las herramientas de [Windows Sysinternals](http://go.microsoft.com/?linkid=6013259) y otras herramientas de Windows que pueden ayudarle a realizar una investigación de equipos interna. Los tipos de herramientas se representan mediante iconos en la primera columna de la tabla siguiente:

**Tabla A.3. Tipos de herramienta**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Icono</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Este icono representa una herramienta de línea de comandos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Este icono representa una herramienta con una interfaz gráfica de usuario que requiere instalación y altera la unidad de disco de destino.</td>
</tr>
</tbody>
</table>
  
En las tablas siguientes se proporciona información acerca de varias herramientas que puede utilizar en investigaciones de equipos.
  
#### Herramientas de Windows Sysinternals
  
**Tabla A.4. Información sobre herramientas de Windows Sysinternals**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de herramienta</th>
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">AccessChk v2.0</a></td>
<td style="border:1px solid black;">Muestra el acceso a archivos, claves de registro o servicios de Windows del usuario o el grupo que especifique.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">AccessEnum v1.3</a></td>
<td style="border:1px solid black;">Muestra quién tiene acceso a qué directorios, archivos y claves de registro de un equipo. Utilícelo para encontrar los lugares donde los permisos no se han aplicado correctamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Autoruns v8.53</a></td>
<td style="border:1px solid black;">Muestra los programas que están configurados para iniciarse automáticamente cuando se arranca un equipo y un usuario inicia una sesión (también muestra la lista completa de las ubicaciones de registro y archivo donde las aplicaciones pueden configurar los valores de inicio automático).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Autorunsc v8.53</a></td>
<td style="border:1px solid black;">La versión de línea de comandos del programa Autoruns (descrita en la entrada anterior).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Diskmon</a></td>
<td style="border:1px solid black;">Captura toda la actividad del disco duro. Actúa como una luz de actividad del disco de software en la bandeja del sistema.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">DiskView</a></td>
<td style="border:1px solid black;">Utilidad gráfica del sector de disco; visor de disco.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Du v1.3</a></td>
<td style="border:1px solid black;">Muestra el uso de disco por directorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Filemon v7.03</a></td>
<td style="border:1px solid black;">Muestra toda la actividad del sistema de archivos en tiempo real.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Handle v3.2</a></td>
<td style="border:1px solid black;">Muestra los archivos abiertos y el proceso que abrió dichos archivos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">ListDLLs v2.25</a></td>
<td style="border:1px solid black;">Muestra todos los DLL cargados actualmente, así como dónde están cargados y los números de versión (imprime los nombres de ruta completos de los módulos cargados).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">LogonSessions v1.1</a></td>
<td style="border:1px solid black;">Lista las sesiones de inicio activas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PendMoves v1.1</a></td>
<td style="border:1px solid black;">Muestra los comandos file rename y delete que se ejecutarán la próxima vez que se inicie el equipo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Portmon v3.02</a></td>
<td style="border:1px solid black;">Muestra la actividad del puerto paralelo y serie (también muestra parte de los datos enviados y recibidos).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Process Explorer v10.2</a></td>
<td style="border:1px solid black;">Muestra los archivos, claves de registro y otros objetos que han abiertos los procesos, los DLL que se han cargado, los propietarios de los procesos, etc.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsExec v1.72</a></td>
<td style="border:1px solid black;">Ejecuta procesos de forma remota.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsFile v1.01</a></td>
<td style="border:1px solid black;">Muestra los archivos abiertos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsInfo v1.71</a></td>
<td style="border:1px solid black;">Muestra información acerca de un equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsList v1.27</a></td>
<td style="border:1px solid black;">Muestra información acerca de procesos y subprocesos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsLoggedOn v1.32</a></td>
<td style="border:1px solid black;">Muestra los usuarios que han iniciado sesión en un equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsLogList v2.63</a></td>
<td style="border:1px solid black;">Vuelca los registros de eventos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">PsService v2.2</a></td>
<td style="border:1px solid black;">Vista y control de servicios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Regmon v7.03</a></td>
<td style="border:1px solid black;">Muestra toda la actividad de registro en tiempo real.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">RootkitRevealer</a></td>
<td style="border:1px solid black;">Busca código malintencionado basado en rootkit.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">ShareEnum v1.6</a></td>
<td style="border:1px solid black;">Busca recursos compartidos de archivo en una red y muestra la configuración de seguridad para eliminar los valores aplicados incorrectamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Streams v1.53</a></td>
<td style="border:1px solid black;">Revela secuencias de datos NTFS alternativas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Strings v2.3</a></td>
<td style="border:1px solid black;">Busca cadenas ANSI y UNICODE en imágenes binarias.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">TCPVcon v2.34</a></td>
<td style="border:1px solid black;">Muestra los sockets activos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">TCPView v2.4</a></td>
<td style="border:1px solid black;">Muestra todos los extremos TCP y UDP abiertos y el nombre del proceso que posee cada extremo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">TDIMon v1.01</a></td>
<td style="border:1px solid black;">Muestra información de TCP/IP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/?linkid=6013259">Tokenmon v1.01</a></td>
<td style="border:1px solid black;">Muestra la actividad relacionada con la seguridad, incluidos el inicio y cierre de sesión, el uso de privilegios y la suplantación.</td>
</tr>
</tbody>
</table>
  
#### Herramientas de Windows
  
**Tabla A.5. Información de herramientas de Windows**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de herramienta</th>
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Arp</td>
<td style="border:1px solid black;">Muestra tablas de Protocolo de resolución de direcciones (ARP).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Date</td>
<td style="border:1px solid black;">Muestra la configuración de fecha actual.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Dir</td>
<td style="border:1px solid black;">Muestra una lista de archivos y subdirectorios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Doskey</td>
<td style="border:1px solid black;">Muestra el historial de comandos para un shell CMD.EXE abierto.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Ipconfig</td>
<td style="border:1px solid black;">Muestra la configuración local del equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Net</td>
<td style="border:1px solid black;">Actualiza, corrige o muestra la red o la configuración de red.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Netstat</td>
<td style="border:1px solid black;">Muestra estadísticas de protocolo y la información de conexión actual.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Time</td>
<td style="border:1px solid black;">Muestra la configuración de hora actual.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Find</td>
<td style="border:1px solid black;">Busca en archivos para encontrar una cadena.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Schtasks</td>
<td style="border:1px solid black;">Muestra las tareas programadas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Systeminfo</td>
<td style="border:1px solid black;">Proporciona información general acerca del equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Vol</td>
<td style="border:1px solid black;">Muestra la etiqueta de volumen de disco y el número de serie, si existen.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Hostname</td>
<td style="border:1px solid black;">Muestra la parte del nombre de host del nombre completo del equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Openfiles</td>
<td style="border:1px solid black;">Consulta, muestra o desconecta archivos abiertos o archivos abiertos por usuarios de la red.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://support.microsoft.com/kb/841290">FCIV</a></td>
<td style="border:1px solid black;">Comprobador de Integridad de CHECKSUM de Archivo. Sirve para calcular un hash MD5 o SHA1 cifrado del contenido de un archivo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Bloc de notas</td>
<td style="border:1px solid black;">Sirve para examinar los metadatos asociados con un archivo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Reg</td>
<td style="border:1px solid black;">Sirve para ver, modificar, exportar, guardar o eliminar claves de registro, valores y subárboles.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://technet2.microsoft.com/windowsserver/en/library/7e8e71a0-16c2-46ce-bd40-fa8ea0dbeb5e1033.mspx?mfr=true">Netcap</a></td>
<td style="border:1px solid black;">Recopila información de rastreo de red de la línea de comandos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Sc</td>
<td style="border:1px solid black;">Sirve para comunicarse con el Controlador de servicio y los servicios. (La consulta de Sc es útil para volcar todos los servicios y sus estados).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Assoc</td>
<td style="border:1px solid black;">Ve o modifica las asociaciones de extensión de nombre de archivo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Ftype</td>
<td style="border:1px solid black;">Ve o modifica los tipos de archivo utilizados en asociaciones de extensión de nombre de archivo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Gpresult</td>
<td style="border:1px solid black;">Determina el conjunto de directivas resultante.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Tasklist</td>
<td style="border:1px solid black;">Lista los procesos en ejecución y los módulos cargados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/technet/security/tools/mbsahome.mspx">MBSA</a></td>
<td style="border:1px solid black;">Determina el estado de la revisión de seguridad y otras vulnerabilidades conocidas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;">Rsop.msc</td>
<td style="border:1px solid black;">Muestra el conjunto de directivas resultante.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><a href="http://technet2.microsoft.com/windowsserver/f/?en/library/e38acbb8-c414-4ac7-b301-be0293a157f91033.mspx">Rasdiag</a></td>
<td style="border:1px solid black;">Recopila información diagnóstica acerca de servicios remotos y colóquela en un archivo.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía fundamental de investigación de equipos para Windows](http://go.microsoft.com/fwlink/?linkid=80345)
  
**Notificaciones de actualización**
  
[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)
  
[](#mainsection)[Principio de la página](#mainsection)
