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
<th><p>Nombre de documento</p></th>
<th><p>Ubicación</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Hoja de cálculo: Chain of Custody Log Documentation.doc</p>
<p>Hoja de cálculo: Impact Analysis.doc</p>
<p>Muestra: Internal Investigation Report.doc</p></td>
<td style="border:1px solid black;"><p>Vínculo a la <a href="http://go.microsoft.com/fwlink/?linkid=80345">Guía fundamental de investigación de equipos para Windows</a> en el Centro de descarga de Microsoft.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Evidencia de equipo</p>
<p>Evidencia de disco duro</p>
<p>Removable media (Medios extraíbles)</p></td>
<td style="border:1px solid black;"><p>Apéndice C. Hojas de cálculo de muestra en <a href="http://www.ojp.usdoj.gov/nij/pubs-sum/199408.htm">Forensic Examination of Digital Evidence: A Guide for Law Enforcement</a> del Instituto Nacional de Justicia, una agencia del Departamento de Justicia de EE.UU.</p></td>
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
<th><p>Tipo de crimen</p></th>
<th><p>Organizaciones adecuadas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Asuntos de explotación de menores y fraude en Internet relacionados con el correo</p></td>
<td style="border:1px solid black;"><p><a href="http://www.usps.com/postalinspectors">Servicio de Inspección Postal de EE.UU.</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Explotación o pornografía de menores</p></td>
<td style="border:1px solid black;"><p>Policía local</p>
<p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Intrusión de equipos (piratería)</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p><a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Piratería de Copyright (software, películas, grabación de sonido)</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Falsificación de divisas</p></td>
<td style="border:1px solid black;"><p><a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Robo de identidad o datos de clientes</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p><a href="http://www.secretservice.gov/financial_crimes.shtml">Servicio Secreto de Estados Unidos (División de crímenes financieros)</a></p>
<p><a href="https://rn.ftc.gov/pls/dod/wsolcq$.startup?z_org_code=pu01">Formulario de quejas del consumidor FTC</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Amenazas de bomba en Internet</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Oficina local de la <a href="http://www.atf.gov/field/index.htm">división de ATF</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Fraude en Internet y correo no deseado</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p><a href="http://www.secretservice.gov/financial_crimes.shtml">Servicio Secreto de Estados Unidos (División de crímenes financieros)</a></p>
<p><a href="https://rn.ftc.gov/pls/dod/wsolcq$.startup?z_org_code=pu01">Formulario de quejas del consumidor FTC</a></p>
<p>Si se trata de fraude de títulos o correo electrónico no deseado relacionado con inversiones, <a href="http://www.sec.gov/complaint.shtml">Centro de reclamaciones de la SEC y consejos informativos</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Acoso de Internet</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Tráfico de contraseñas</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p><a href="http://www.secretservice.gov/">Servicio Secreto de Estados Unidos</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Robo de secretos comerciales</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Falsificación de marcas</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Si se trata de un crimen importado, <a href="http://www.ice.gov/">Oficina de Inmigración y Aduanas de EE.UU.</a></p>
<p><a href="http://www.ic3.gov/">Centro de Quejas sobre Crímenes en Internet</a></p>
<p>Unidad operativa o cuerpo policial local contra crímenes tecnológicos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Tráfico de explosivos, dispositivos incendiarios o armas de fuego en Internet</p></td>
<td style="border:1px solid black;"><p><a href="http://www.fbi.gov/contact/fo/fo.htm">Oficina local del FBI</a></p>
<p>Oficina local de la <a href="http://www.atf.gov/field/index.htm">división de ATF</a></p></td>
</tr>
</tbody>
</table>
<p> </p>

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
<th><p>Icono</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Este icono representa una herramienta de línea de comandos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Este icono representa una herramienta con una interfaz gráfica de usuario que requiere instalación y altera la unidad de disco de destino.</p></td>
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
<th><p>Tipo de herramienta</p></th>
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">AccessChk v2.0</a></p></td>
<td style="border:1px solid black;"><p>Muestra el acceso a archivos, claves de registro o servicios de Windows del usuario o el grupo que especifique.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">AccessEnum v1.3</a></p></td>
<td style="border:1px solid black;"><p>Muestra quién tiene acceso a qué directorios, archivos y claves de registro de un equipo. Utilícelo para encontrar los lugares donde los permisos no se han aplicado correctamente.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Autoruns v8.53</a></p></td>
<td style="border:1px solid black;"><p>Muestra los programas que están configurados para iniciarse automáticamente cuando se arranca un equipo y un usuario inicia una sesión (también muestra la lista completa de las ubicaciones de registro y archivo donde las aplicaciones pueden configurar los valores de inicio automático).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Autorunsc v8.53</a></p></td>
<td style="border:1px solid black;"><p>La versión de línea de comandos del programa Autoruns (descrita en la entrada anterior).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Diskmon</a></p></td>
<td style="border:1px solid black;"><p>Captura toda la actividad del disco duro. Actúa como una luz de actividad del disco de software en la bandeja del sistema.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">DiskView</a></p></td>
<td style="border:1px solid black;"><p>Utilidad gráfica del sector de disco; visor de disco.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Du v1.3</a></p></td>
<td style="border:1px solid black;"><p>Muestra el uso de disco por directorio.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Filemon v7.03</a></p></td>
<td style="border:1px solid black;"><p>Muestra toda la actividad del sistema de archivos en tiempo real.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Handle v3.2</a></p></td>
<td style="border:1px solid black;"><p>Muestra los archivos abiertos y el proceso que abrió dichos archivos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">ListDLLs v2.25</a></p></td>
<td style="border:1px solid black;"><p>Muestra todos los DLL cargados actualmente, así como dónde están cargados y los números de versión (imprime los nombres de ruta completos de los módulos cargados).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">LogonSessions v1.1</a></p></td>
<td style="border:1px solid black;"><p>Lista las sesiones de inicio activas</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PendMoves v1.1</a></p></td>
<td style="border:1px solid black;"><p>Muestra los comandos file rename y delete que se ejecutarán la próxima vez que se inicie el equipo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Portmon v3.02</a></p></td>
<td style="border:1px solid black;"><p>Muestra la actividad del puerto paralelo y serie (también muestra parte de los datos enviados y recibidos).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Process Explorer v10.2</a></p></td>
<td style="border:1px solid black;"><p>Muestra los archivos, claves de registro y otros objetos que han abiertos los procesos, los DLL que se han cargado, los propietarios de los procesos, etc.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsExec v1.72</a></p></td>
<td style="border:1px solid black;"><p>Ejecuta procesos de forma remota.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsFile v1.01</a></p></td>
<td style="border:1px solid black;"><p>Muestra los archivos abiertos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsInfo v1.71</a></p></td>
<td style="border:1px solid black;"><p>Muestra información acerca de un equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsList v1.27</a></p></td>
<td style="border:1px solid black;"><p>Muestra información acerca de procesos y subprocesos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsLoggedOn v1.32</a></p></td>
<td style="border:1px solid black;"><p>Muestra los usuarios que han iniciado sesión en un equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsLogList v2.63</a></p></td>
<td style="border:1px solid black;"><p>Vuelca los registros de eventos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">PsService v2.2</a></p></td>
<td style="border:1px solid black;"><p>Vista y control de servicios.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Regmon v7.03</a></p></td>
<td style="border:1px solid black;"><p>Muestra toda la actividad de registro en tiempo real.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">RootkitRevealer</a></p></td>
<td style="border:1px solid black;"><p>Busca código malintencionado basado en rootkit.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">ShareEnum v1.6</a></p></td>
<td style="border:1px solid black;"><p>Busca recursos compartidos de archivo en una red y muestra la configuración de seguridad para eliminar los valores aplicados incorrectamente.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Streams v1.53</a></p></td>
<td style="border:1px solid black;"><p>Revela secuencias de datos NTFS alternativas.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Strings v2.3</a></p></td>
<td style="border:1px solid black;"><p>Busca cadenas ANSI y UNICODE en imágenes binarias.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">TCPVcon v2.34</a></p></td>
<td style="border:1px solid black;"><p>Muestra los sockets activos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">TCPView v2.4</a></p></td>
<td style="border:1px solid black;"><p>Muestra todos los extremos TCP y UDP abiertos y el nombre del proceso que posee cada extremo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">TDIMon v1.01</a></p></td>
<td style="border:1px solid black;"><p>Muestra información de TCP/IP.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://go.microsoft.com/?linkid=6013259">Tokenmon v1.01</a></p></td>
<td style="border:1px solid black;"><p>Muestra la actividad relacionada con la seguridad, incluidos el inicio y cierre de sesión, el uso de privilegios y la suplantación.</p></td>
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
<th><p>Tipo de herramienta</p></th>
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Arp</p></td>
<td style="border:1px solid black;"><p>Muestra tablas de Protocolo de resolución de direcciones (ARP).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Date</p></td>
<td style="border:1px solid black;"><p>Muestra la configuración de fecha actual.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Dir</p></td>
<td style="border:1px solid black;"><p>Muestra una lista de archivos y subdirectorios.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Doskey</p></td>
<td style="border:1px solid black;"><p>Muestra el historial de comandos para un shell CMD.EXE abierto.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Ipconfig</p></td>
<td style="border:1px solid black;"><p>Muestra la configuración local del equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Net</p></td>
<td style="border:1px solid black;"><p>Actualiza, corrige o muestra la red o la configuración de red.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Netstat</p></td>
<td style="border:1px solid black;"><p>Muestra estadísticas de protocolo y la información de conexión actual.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Time</p></td>
<td style="border:1px solid black;"><p>Muestra la configuración de hora actual.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Find</p></td>
<td style="border:1px solid black;"><p>Busca en archivos para encontrar una cadena.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Schtasks</p></td>
<td style="border:1px solid black;"><p>Muestra las tareas programadas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Systeminfo</p></td>
<td style="border:1px solid black;"><p>Proporciona información general acerca del equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Vol</p></td>
<td style="border:1px solid black;"><p>Muestra la etiqueta de volumen de disco y el número de serie, si existen.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Hostname</p></td>
<td style="border:1px solid black;"><p>Muestra la parte del nombre de host del nombre completo del equipo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Openfiles</p></td>
<td style="border:1px solid black;"><p>Consulta, muestra o desconecta archivos abiertos o archivos abiertos por usuarios de la red.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://support.microsoft.com/kb/841290">FCIV</a></p></td>
<td style="border:1px solid black;"><p>Comprobador de Integridad de CHECKSUM de Archivo. Sirve para calcular un hash MD5 o SHA1 cifrado del contenido de un archivo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Bloc de notas</p></td>
<td style="border:1px solid black;"><p>Sirve para examinar los metadatos asociados con un archivo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Reg</p></td>
<td style="border:1px solid black;"><p>Sirve para ver, modificar, exportar, guardar o eliminar claves de registro, valores y subárboles.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://technet2.microsoft.com/windowsserver/en/library/7e8e71a0-16c2-46ce-bd40-fa8ea0dbeb5e1033.mspx?mfr=true">Netcap</a></p></td>
<td style="border:1px solid black;"><p>Recopila información de rastreo de red de la línea de comandos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Sc</p></td>
<td style="border:1px solid black;"><p>Sirve para comunicarse con el Controlador de servicio y los servicios. (La consulta de Sc es útil para volcar todos los servicios y sus estados).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Assoc</p></td>
<td style="border:1px solid black;"><p>Ve o modifica las asociaciones de extensión de nombre de archivo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Ftype</p></td>
<td style="border:1px solid black;"><p>Ve o modifica los tipos de archivo utilizados en asociaciones de extensión de nombre de archivo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Gpresult</p></td>
<td style="border:1px solid black;"><p>Determina el conjunto de directivas resultante.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Tasklist</p></td>
<td style="border:1px solid black;"><p>Lista los procesos en ejecución y los módulos cargados.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://www.microsoft.com/technet/security/tools/mbsahome.mspx">MBSA</a></p></td>
<td style="border:1px solid black;"><p>Determina el estado de la revisión de seguridad y otras vulnerabilidades conocidas.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">  <img src="images/Cc162853.4ca6dc59-46e6-4293-8352-95061fd425a9(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p>Rsop.msc</p></td>
<td style="border:1px solid black;"><p>Muestra el conjunto de directivas resultante.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">  <img src="images/Cc162853.60a80b39-03c6-486c-b4c4-86010954219c(es-es,TechNet.10).gif" /></td>
<td style="border:1px solid black;"><p><a href="http://technet2.microsoft.com/windowsserver/f/?en/library/e38acbb8-c414-4ac7-b301-be0293a157f91033.mspx">Rasdiag</a></p></td>
<td style="border:1px solid black;"><p>Recopila información diagnóstica acerca de servicios remotos y colóquela en un archivo.</p></td>
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
