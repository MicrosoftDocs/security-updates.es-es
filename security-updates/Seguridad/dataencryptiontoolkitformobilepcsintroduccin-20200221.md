---
TOCTitle: 'Data Encryption Toolkit for Mobile PCs: Introducción'
Title: 'Data Encryption Toolkit for Mobile PCs: Introducción'
ms:assetid: 'abfc4696-a39a-43df-b559-133633e4bd5e'
ms:contentKeyID: 20200221
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162811(v=TechNet.10)'
---

Data Encryption Toolkit for Mobile PCs: análisis de seguridad
=============================================================

### Introducción

Publicado: abril 4, 2007

Hasta hace unos años, los equipos portátiles seguían siendo relativamente escasos en la mayoría de organizaciones. Los portátiles sólo se cedían a trabajadores que viajaban con frecuencia y a ejecutivos. Actualmente, los portátiles son más eficaces que nunca, y también son ubicuos. Ya no se asignan a unos pocos, incluso superan el número de equipos de escritorio en algunas organizaciones. Y conforme aumenta su capacidad de almacenamiento, se consideran cada vez más repositorios de gran valor para todo tipo de datos confidenciales.

El tremendo aumento del número de portátiles viene acompañado del aumento correspondiente en el número de portátiles robados o perdidos. La seguridad de los portátiles es un problema serio para la mayoría de organizaciones de tamaño medio a grande. Un estudio reciente realizado por el Ponemon Institute, "[Datos confidenciales en peligro](http://www.csoonline.com/read/080106/col_ponemon.html)" (en inglés), establece que "el 81 por ciento de los 484 encuestados notifican que sus organizaciones han experimentado una o más pérdidas o desapariciones de equipos portátiles que contenían información empresarial confidencial en los últimos 12 meses." Aunque los costos de sustitución son importantes, los costos directos e indirectos de una infracción de seguridad cuando un portátil robado tiene datos importantes o confidenciales en la unidad de disco duro pueden ser significativamente mayores.

Algunos tipos de información están protegidos por leyes nacionales o federales, otros por leyes estatales, provinciales o regionales y otros por normas industriales. El número de leyes, jurisdicciones y clasificaciones de confidencialidad crece a medida que aumenta el número de portátiles. La pérdida de un equipo portátil puede exponer a la organización a multas importantes y responsabilidad civil, dependiendo del esfuerzo realizado para implementar medidas de seguridad preferenciales. Los costos directos e indirectos tras una infracción de seguridad pueden implicar la dificultad para retener clientes y la pérdida de credibilidad y reputación.

Microsoft proporciona herramientas para tratar los problemas de seguridad de los equipos portátiles. El cifrado adecuado de los datos de un equipo portátil puede dificultar mucho más la recuperación de los datos confidenciales si el portátil se roba o se pierde. Mediante el uso adecuado de Microsoft® BitLocker™ Drive Encryption (BitLocker) y el Sistema de archivos de cifrado (EFS), los datos confidenciales se pueden proteger frente a una gran variedad de vectores de ataques comunes.

La guía *Análisis de seguridad de Microsoft Data Encryption Toolkit for Mobile PCs* proporciona detalles específicos acerca de los niveles de seguridad que se pueden alcanzar mediante BitLocker y EFS. Las ediciones Enterprise y Ultimate de Windows Vista™ admiten la gama completa de características de seguridad descritas en esta guía y un subconjunto importante y útil se encuentra disponible en Microsoft Windows® XP. Existen varios niveles de protección disponibles dependiendo de las características y configuraciones aplicadas. En las configuraciones más seguras, un atacante malévolo puede requerir una cantidad extraordinaria de recursos para descifrar los datos de la unidad de disco duro.

El *Análisis de seguridad* le ayuda a entender cómo pueden contribuir las características de Windows Vista y Windows XP a minimizar los riesgos de seguridad específicos de su organización: Esta guía le ayudará a:

-   Identificar riesgos y vectores de amenazas comunes en su entorno.

-   Entender cómo se pueden minimizar los riesgos y amenazas específicos mediante BitLocker y EFS, de forma independiente o en conjunto.

-   Prepararse para minimizar las amenazas de seguridad que BitLocker o EFS no tratan.

-   Entender las características de seguridad seleccionadas y la tecnología disponible en Windows Vista.

Las características de seguridad descritas en esta guía se han desarrollado con tecnologías aprobadas por la industria. Por ejemplo, la implementación de Microsoft de algoritmos criptográficos usados para BitLocker y EFS se certifican según los estándares federales de procesamiento de información (FIPS) 140-1 del gobierno federal de Estados Unidos. De este modo, los algoritmos implementados han madurado. Este cumplimiento de la tecnología aprobada por la industria es importante, ya que algunas leyes de privacidad de datos estatales y nacionales ofrecen exenciones o factores mitigantes para las organizaciones que muestren que realizan esfuerzos de buena fe para seguir las recomendaciones sobre seguridad de los datos.

##### En esta página

[](#egaa)[Quién debería leer esta guía](#egaa)
[](#efaa)[Contenidos de los capítulos](#efaa)
[](#eeaa)[Convenciones de estilo](#eeaa)
[](#edaa)[Más información](#edaa)
[](#ecaa)[Soporte técnico y comentarios](#ecaa)
[](#ebaa)[Agradecimientos](#ebaa)

### Quién debería leer esta guía

Esta guía está dirigida a los especialistas en seguridad que son responsables de las decisiones o recomendaciones tecnológicas y de directivas que afectan miles de equipos cliente, especialmente portátiles. Las amenazas tecnológicas y relacionadas no son aplicables por lo general a redes o usuarios domésticos. Debe leer esta guía si sus responsabilidades incluyen:

-   Tomar decisiones o realizar recomendaciones acerca de las directivas de seguridad y la tecnología.

-   Implementar directivas de seguridad de servidores o clientes.

-   Evaluar las tecnologías de seguridad.

-   Integrar las directivas de seguridad con otras tecnologías o directivas de administración de equipos.

La información que contiene esta guía es avanzada y detallada, pero no pretende ser un tratado sobre seguridad, cifrado, sistemas de archivos u otros temas fundamentales de seguridad y administración de sistemas.

[](#mainsection)[Principio de la página](#mainsection)

### Contenidos de los capítulos

Esta sección ofrece una introducción a los capítulos de esta guía.

[Capítulo 1: Descripción de riesgos](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/analysis/df2c6d71-98f7-4212-b3b7-b9eb2f501348.mspx) presenta las amenazas de seguridad que BitLocker y EFS pueden tratar. También incluye una descripción de los escenarios usados en el resto de *Análisis de seguridad* para proporcionar un marco más concreto donde presentar los riesgos y las ventajas.

[Capítulo 2: BitLocker Drive Encryption](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/analysis/4e6ce820-fcac-495a-9f23-73d65d846638.mspx) se centra en la tecnología BitLocker Drive Encryption introducida en Windows Vista. Describe cómo se puede usar BitLocker para minimizar las amenazas de seguridad específicas descritas en el Capítulo 1 e incluye ejemplos de configuraciones que se pueden usar como punto de partida para desarrollar una implementación sólida de BitLocker en su organización.

[Capítulo 3: Sistema de archivos de cifrado](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/analysis/dc2cde72-a84d-4716-9a30-f62b608efda1.mspx) describe cómo funciona EFS y cómo se puede usar para ayudar a minimizar las amenazas de su entorno.

[Capítulo 4: Combinación de BitLocker y EFS](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/analysis/80c0d0af-2c2e-45d6-9b29-f850926296bb.mspx) muestra cómo combinar BitLocker y EFS para minimizar las amenazas de forma más eficaz que cualquier tecnología por sí sola.

[Capítulo 5: Elección de la solución correcta](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/analysis/b77d6369-10e9-4e66-8c67-c9f8cb073ced.mspx) ofrece descripciones y herramientas para ayudar a los especialistas en seguridad a elegir la combinación adecuada de características y elementos de configuración para sus organizaciones.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

Esta guía usa las convenciones de estilo descritas en la tabla siguiente.

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Negrita</strong></td>
<td style="border:1px solid black;">Significa caracteres escritos exactamente como se muestran, incluidos comandos, modificadores y nombres de archivos. Los elementos de la interfaz de usuario también se muestran en negrita.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>Cursiva</em></td>
<td style="border:1px solid black;">Los títulos de libros y otras publicaciones importantes aparecen en <em>cursiva</em>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><em>&lt;Cursiva&gt;</em></td>
<td style="border:1px solid black;">Los marcadores de posición en cursiva y entre corchetes angulares – <em>&lt;nombre de archivo&gt;</em> – representan variables.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><pre><code>Fuente monoespaciada</code></pre>
<br />
</td>
<td style="border:1px solid black;">Muestra ejemplos de códigos y scripts.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Nota</strong></td>
<td style="border:1px solid black;">Avisa al lector de que hay información adicional.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Importante</strong></td>
<td style="border:1px solid black;">Avisa al lector de que hay información adicional fundamental.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Más información
  
Además de este *Análisis de seguridad*, [Data Encryption Toolkit for Mobile PCs](http://go.microsoft.com/fwlink/?linkid=86127) (en inglés) incluye otros documentos y herramientas que pueden resultar útiles:
  
-   La *Guía de planeación e implementación* describe cómo realizar planes para implementar BitLocker y EFS con el objeto de proteger sus equipos móviles.
  
-   La herramienta Asistente del sistema de archivos de cifrado de Microsoft (Asistente para EFS) le ayuda a automatizar el proceso para encontrar y cifrar archivos confidenciales en equipos que ejecutan Windows XP y Windows Vista.
  
-   La *Guía del administrador del Asistente de EFS* explica cómo los administradores pueden implementar y administrar el Asistente para EFS en equipos de dominio combinados para proporcionar una protección coherente en las unidades de negocio o en toda la empresa.
  
Existen muchos recursos valiosos disponibles para ayudar a los responsables de la toma de decisiones a lograr un contexto más amplio o un conocimiento más profundo de los problemas de seguridad en las redes de Microsoft Windows. Un punto de partida perfecto es la página [Guía de seguridad](http://www.microsoft.com/technet/security/guidance/default.mspx) de Microsoft TechNet.
  
Se pueden encontrar consejos específicos para tratar los requisitos de seguridad de la administración de dominios en la [Guía de procedimientos recomendados para asegurar las instalaciones de Windows Server Active Directory](http://www.microsoft.com/windowsserver2003/techinfo/overview/adsecurity.mspx).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Soporte técnico y comentarios
  
El equipo Aceleradores de soluciones: seguridad y conformidad (SASC) agradece sus ideas acerca de éste y otros aceleradores de soluciones. Contribuya con sus comentarios y experiencias en [secwish@microsoft.com](mailto:secwish@microsoft.com?subject=data%20encryption%20toolkit%20for%20mobile%20pcs%20security%20analysis%20on%20technet). Esperamos obtener noticias suyas.
  
Aceleradores de soluciones proporciona una orientación prescriptiva y automatización para la integración en todos los productos. Presenta herramientas y contenidos probados para que pueda planear, crear, implementar y usar tecnología de información con confianza. Para ver la amplia gama de Aceleradores de soluciones y obtener información adicional, visite la página [Aceleradores de soluciones](http://go.microsoft.com/fwlink/?linkid=51571) de Microsoft TechNet.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Agradecimientos
  
Al equipo de Aceleradores de soluciones: seguridad y conformidad (SASC) le gustaría ofrecer su reconocimiento y dar las gracias al equipo que realizó *Análisis de seguridad de Data Encryption Toolkit for Mobile PCs*. Las siguientes personas fueron responsables directamente de la escritura, el desarrollo y la prueba de la solución, o bien realizaron una contribución importante a estas tareas.
  
**Jefes de desarrollo**
  
Mike Smith-Lonergan - *Microsoft*
  
David Mowers - *Securitay, Inc.*
  
**Administrador del programa**
  
Bill Canning - *Microsoft*
  
**Desarrolladores de contenido**
  
Paul Flynn - *3Sharp, LLC*
  
Tommy Phillips - *Butternut Software*
  
Paul Robichaux - *3Sharp, LLC*
  
**Editor**
  
Steve Wacker - *Wadeware LLC*
  
**Revisores**
  
Vijay Bharadwaj - *Microsoft*
  
Tom Daemen - *Microsoft*
  
Mike Danseglio - *Microsoft*
  
Kurt Dillard - *Microsoft*
  
Jeff Hatfield - *Wireless Ink Inc.*
  
Erik Holt - *Microsoft*
  
Russell Humphries - *Microsoft*
  
David Kennedy - *Microsoft*
  
Douglas MacIver - *Microsoft*
  
Josh Phillips
  
Greg Petersen - *Avanade Inc.*
  
Ben Wilson - *ASG Group*
  
**Jefes de producto**
  
Alain Meeus - *Microsoft*
  
Jim Stuart - *Microsoft*
  
**Jefe de lanzamiento**
  
Karina Larson - *Microsoft*
  
**Personal encargado de pruebas**
  
Gaurav Singh Bora - *Microsoft*
  
Sumit Ajitkumar Parikh - *Infosys Technologies Ltd.*
  
Swaminathan Viswanathan - *Infosys Technologies Ltd.*
  
Swapna Rangachari Jagannathan - *Infosys Technologies Ltd.*
  
Neethu Thomas - *Infosys Technologies Ltd.*
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener Data Encryption Toolkit for Mobile PCs](http://go.microsoft.com/fwlink/?linkid=81666)
  
**Participar**
  
[Suscríbase para participar en el programa beta de Data Encryption Toolkit](https://connect.microsoft.com/invitationuse.aspx?programid=790&invitationid=desa-r7gd-3f73&siteid=14)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=data%20encryption%20toolkit%20for%20mobile%20pcs%20security%20analysis%20on%20technet)
  
[](#mainsection)[Principio de la página](#mainsection)
