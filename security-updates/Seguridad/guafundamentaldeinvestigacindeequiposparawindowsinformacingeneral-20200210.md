---
TOCTitle: 'Guía fundamental de investigación de equipos para Windows: Información general'
Title: 'Guía fundamental de investigación de equipos para Windows: Información general'
ms:assetid: '9545b739-1ef9-415f-a1c4-3ca29f0ce5af'
ms:contentKeyID: 20200210
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162846(v=TechNet.10)'
---

Guía fundamental de investigación de equipos para Windows
=========================================================

### Información general

Publicado: enero 11, 2007

La conexión a Internet y los avances tecnológicos exponen los equipos y las redes informáticas a actividades criminales como la intrusión no autorizada, el fraude financiero y el robo de la identidad y la propiedad intelectual. Los equipos se pueden utilizar para lanzar ataques contra redes informáticas y destruir datos. El correo electrónico se puede utilizar para acosar a personas, transmitir imágenes con claro contenido sexual y realizar otras actividades malintencionadas. Dichas actividades exponen a las organizaciones a riesgos éticos, legales y financieros y, a menudo, las obligan a realizar investigaciones de equipos internas.

En esta guía se describen los procesos y las herramientas para el uso en investigaciones de equipos internas. Introduce un modelo de varias fases basado en procedimientos aceptados por la comunidad de investigación de equipos. También presenta un ejemplo de escenario aplicado de una investigación interna realizada en un entorno con equipos basados en Microsoft® Windows®. La investigación utiliza herramientas [Windows Sysinternals](http://go.microsoft.com/?linkid=6013253) (utilidades avanzadas que se pueden utilizar para examinar equipos basados en Windows), así como los comandos y herramientas de Windows disponibles normalmente.

Algunas de las directivas y los procedimientos invocados en las investigaciones derivadas de incidentes de seguridad de equipos también pueden existir en los planes de recuperación de desastres. Aunque esta guía no trata sobre dichos planes, es importante que las organizaciones establezcan procedimientos que se puedan utilizar en situaciones de emergencia y desastre. Las organizaciones también deben identificar y administrar los riesgos de seguridad donde sea posible. Para obtener más información, consulte la [Guía de Administración de riesgos de seguridad](http://go.microsoft.com/fwlink/?linkid=30794).

##### En esta página

[](#eiaa)[Modelo de investigación informática](#eiaa)
[](#ehaa)[Proceso inicial de toma de decisiones](#ehaa)
[](#egaa)[Resumen del capítulo](#egaa)
[](#efaa)[Destinatarios](#efaa)
[](#eeaa)[Advertencias y Renuncias](#eeaa)
[](#edaa)[Referencias y créditos](#edaa)
[](#ecaa)[Convenciones de estilo](#ecaa)
[](#ebaa)[Soporte y comentarios](#ebaa)

### Modelo de investigación informática

Según Warren G. Kruse II y Jay G. Heiser, autores de *Computer Forensics: Incident Response Essentials*, el examen forense informática es "la preservación, identificación, extracción, documentación e interpretación de medios informáticos para el análisis de evidencias o de la causa raíz." El modelo de investigación de equipos que se muestra en la figura siguiente organiza los diferentes elementos forenses informáticos en un flujo lógico.

![](images/Cc162846.80e07bd9-28f1-4bc8-b541-bc821af9f2a7(es-es,TechNet.10).gif)

Las cuatro fases de investigación y los procesos adjuntos de la figura deben aplicarse cuando se trabaja con evidencias digitales. Las fases se pueden resumir de la siguiente manera:

-   **Valorar la situación.** Analizar el ámbito de la investigación y la acción a emprender.

-   **Obtener los datos.**Reunir, proteger y conservar la evidencia original.

-   **Analizar los datos.**Examinar y establecer una correlación entre la evidencia digital y los eventos de interés que le ayudarán a crear el caso.

-   **Informar acerca de la investigación.**Reunir y organizar la información recopilada y escribir el informe final.

En los capítulos de esta guía se proporciona información detallada acerca de todas las fases.

[](#mainsection)[Principio de la página](#mainsection)

### Proceso inicial de toma de decisiones

Antes de iniciar cada una de las fases generales de la investigación, debe aplicar el proceso inicial de toma de decisiones que se muestra en la figura siguiente.

![](images/Cc162846.d4021970-fc6b-4e84-901d-0a4f49aca671(es-es,TechNet.10).gif)

Debe determinar si debe aplicarse la ley con la ayuda de abogados. Si decide que es necesario aplicar la ley, debe continuar con la investigación interna, a menos que la autoridad judicial competente le indique lo contrario. Es posible que los cuerpos de seguridad no estén disponibles para ayudarle en la investigación del incidente, de modo que debe continuar administrando el incidente y la investigación para su posterior sumisión a los cuerpos de seguridad.

En función del tipo de incidente que se esté investigando, lo principal debe ser evitar que las personas que causaron el incidente inflijan daños adicionales a la organización. La investigación es importante, pero la protección de la organización es primordial, a menos que haya problemas de seguridad nacionales.

Si no es necesario aplicar la ley, la organización puede tener directivas y procedimientos de funcionamiento estándar existentes que le guíen en el proceso de investigación. Consulte la sección "Informar de crímenes relacionados con equipos" del [Apéndice: Recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) de esta guía para ver los tipos de crímenes que deben notificarse a los cuerpos de seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen del capítulo

Esta guía consta de cinco capítulos y un apéndice, que se describen brevemente en la lista siguiente. Los primeros cuatro capítulos ofrecen información acerca de las cuatro fases del proceso de investigación interno:

-   [Capítulo 1: Valorar la situación](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/08013562-8f01-4ad5-a5de-a8901f590df3.mspx) explica cómo llevar a cabo una evaluación completa de la situación y prepararse para la investigación interna.

-   [Capítulo 2: Obtener los datos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/89ae3bbe-057c-4d3e-99e1-f7356321c01f.mspx) proporciona instrucciones acerca de cómo reunir evidencias digitales.

-   [Capítulo 3: Analizar los datos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/ac7d2cc4-6cd9-4525-898c-613cf8a53fd6.mspx) examina las técnicas estándar de análisis de evidencias.

-   [Capítulo 4: Informar acerca de la investigación](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/7dad6334-2d4a-4c9d-9648-165db9634835.mspx) explica cómo escribir el informe de resultados de la investigación.

-   [Capítulo 5: Ejemplo de escenario aplicado](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/959c31cd-216b-47fe-b821-7bb40d4156ae.mspx) describe un escenario ficticio que representa un acceso no autorizado a información confidencial.

-   [Apéndice: Recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) incluye información acerca de cómo prepararse para una investigación de equipos, información de contacto para informar de crímenes relacionados con equipos y dónde obtener formación sobre investigación de equipos, hojas de cálculo que se pueden utilizar en investigaciones de equipos y listas de determinadas herramientas de investigación de equipos.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios

Esta guía está dirigida a profesionales de TI de Estados Unidos que necesiten conocimientos generales sobre investigaciones de equipos, incluidos muchos de los procedimientos que se pueden utilizar en dichas investigaciones y los protocolos para crear informes de incidentes.

[](#mainsection)[Principio de la página](#mainsection)

### Advertencias y Renuncias

Esta guía no pretende ofrecer asesoramiento jurídico y no sustituye los consejos legales individualizados ni de otro tipo que pueda proporcionar un abogado. Siempre debe consultar a sus abogados antes de decidir si debe implementar alguno de los procesos descritos. Las herramientas y las tecnologías descritas en esta guía son actuales en el momento de su publicación y pueden cambiar en el futuro.

También es importante entender que las restricciones legales pueden limitar su capacidad a la hora de implementar estos procedimientos. Por ejemplo, Estados Unidos tiene muchas leyes relacionadas con los derechos de las personas sospechosas de haber cometido actos ilícitos. A menos que las restricciones legales se mencionen específicamente en las directivas y los procedimientos existentes establecidos por la organización, es importante que obtenga aprobaciones legales por escrito de los abogados, la administración y los principales participantes en la investigación interna.

![](images/Cc162846.note(es-es,TechNet.10).gif)**Nota:**

Esta guía no incluye información acerca de la directiva de respuesta a incidentes y el desarrollo de procedimientos, instrucciones específicas de productos de implementación de imágenes de datos, instrucciones acerca de la creación de un laboratorio forense o acerca de las investigaciones de equipos en entornos de que no sean Windows. Para obtener información acerca de la directiva de respuesta a incidentes y el desarrollo de procedimientos, consulte el sitio Web de [Microsoft Operations Framework (MOF)](http://go.microsoft.com/fwlink/?linkid=42590).

[](#mainsection)[Principio de la página](#mainsection)

### Referencias y créditos

La información de esta guía se basa en información ofrecida por expertos reconocidos del sector y otras fuentes, incluidas las publicaciones siguientes:

-   [Forensic Examination of Digital Evidence: A Guide for Law Enforcement](http://www.ojp.usdoj.gov/nij/pubs-sum/199408.htm) del Instituto Nacional de Justicia, una agencia del Departamento de Justicia de EE.UU.

-   [Guide to Integrating Forensic Techniques into Incident Response](http://csrc.nist.gov/publications/nistpubs/800-86/sp800-86.pdf) Documento en formato PDF del Instituto Nacional de Normas y Tecnología.

-   "[RFC3227 - Guidelines for Evidence Collection and Archiving](ftp://ftp.rfc-editor.org/in-notes/rfc3227.txt)" de D. Brezinski y T. Killalea.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

En esta guía se utilizan las convenciones de estilo descritas en la tabla siguiente.

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Fuente negrita</strong></td>
<td style="border:1px solid black;">Denota los caracteres escritos tal como se muestra, incluidos comandos, conmutadores y nombres de archivo. Los elementos de la interfaz de usuario también se muestran en negrita.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>Fuente cursiva</em></td>
<td style="border:1px solid black;">Los títulos de libros y otras publicaciones importantes se muestran en cursiva.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><em>&lt;Cursiva&gt;</em></td>
<td style="border:1px solid black;">Los marcadores de posición destacados en cursiva y entre corchetes angulares &lt;Cursiva&gt; representan variables.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><pre><code>Monospace font </code></pre>
<br />
</td>
<td style="border:1px solid black;">Define ejemplos de código y secuencias de comandos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Nota</strong></td>
<td style="border:1px solid black;">Informa al lector de la información suplementaria.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Importante</strong></td>
<td style="border:1px solid black;">Informa al lector de la información suplementaria fundamental.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Soporte y comentarios
  
El equipo Aceleradores de soluciones – Seguridad y Cumplimiento (SASC) estará encantado de recibir su opinión acerca de este y otros aceleradores de soluciones. Envíe sus opiniones y comentarios a [secwish@microsoft.com](mailto:secwish@microsoft.com?subject=the%20fundamental%20computer%20investigation%20guide%20for%20windows). Esperamos su contribución.
  
Los aceleradores de soluciones ofrecen instrucciones prescriptivas y automatización para la integración cruzada de productos. Presentan herramientas y contenido probados que le permiten planear, construir, implementar y utilizar la tecnología de la información con seguridad. Para ver el amplio abanico de aceleradores de soluciones e información adicional, visite la página [Aceleradores de soluciones](http://go.microsoft.com/fwlink/?linkid=51571) de Microsoft TechNet.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía fundamental de investigación de equipos para Windows](http://go.microsoft.com/fwlink/?linkid=80345)
  
**Notificaciones de actualización**
  
[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)
  
[](#mainsection)[Principio de la página](#mainsection)
