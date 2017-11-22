---
TOCTitle: 'Guía fundamental de investigación de equipos para Windows: Capítulo 3: Analizar los datos'
Title: 'Guía fundamental de investigación de equipos para Windows: Capítulo 3: Analizar los datos'
ms:assetid: 'ac7d2cc4-6cd9-4525-898c-613cf8a53fd6'
ms:contentKeyID: 20200216
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162856(v=TechNet.10)'
---

Guía fundamental de investigación de equipos para Windows
=========================================================

### Capítulo 3: Analizar los datos

Publicado: enero 11, 2007

En este capítulo se describen diferentes enfoques y las recomendaciones aceptados del sector para analizar la evidencia reunida durante la fase Obtener los datos de una investigación interna. Utilice el proceso de tres pasos que se muestra en la figura siguiente.

![](images/Cc162856.3418ca95-8ff6-443f-9690-d85ed84a0e98(es-es,TechNet.10).gif)

**Figura 3.1. Fase de análisis del modelo de investigación de equipos**

![](images/Cc162856.important(es-es,TechNet.10).gif) **Importante:**

A veces, es necesario el análisis de datos en línea, que examina un equipo directamente mientras se ejecuta. El análisis en línea suele realizarse debido a restricciones de tiempo en una investigación o para capturar los datos volátiles. Debe ser especialmente cuidadoso cuando realice el análisis en línea para garantizar que minimiza el riesgo de otra evidencia.

##### En esta página

[](#edaa)[Analizar los datos de la red](#edaa)  
[](#ecaa)[Analizar los datos del host](#ecaa)  
[](#ebaa)[Analizar los medios de almacenamiento](#ebaa)

### Analizar los datos de la red

En muchas investigaciones, no es necesario analizar los datos de la red. En vez de eso, las investigaciones examinan y se centran en las imágenes de los datos. Si es necesario un análisis de la red, utilice el procedimiento siguiente:

1.  Busque en los registros de servicios de red eventos de interés. Generalmente, habrá grandes cantidades de datos, por lo que debe centrarse en criterios específicos para eventos de interés, como el nombre de usuario, la fecha y la hora o el recurso al que se está accediendo.

2.  Examine el servidor de seguridad, el servidor proxy, el sistema de detección de intrusos (IDS) y los registros de servicios de acceso remoto. Muchos de estos registros contienen información de conexiones entrantes y salientes supervisadas e incluyen información de identificación, como la dirección IP, la hora del evento e información de autenticación. Es recomendable examinar los datos de registro en una herramienta adecuada para el análisis de datos, como Microsoft® SQL Server™ 2005.

3.  Consulte los detectores de paquetes o los registros del monitor de red para ver datos que pueden ayudarle a determinar las actividades que se realizaron en la red. Determine, además, si las conexiones que examina están cifradas, puesto que no podrá leer el contenido de una sesión cifrada. Sin embargo, puede derivar la hora de la conexión y si un sospechoso ha establecido una sesión con un servidor específico.

[](#mainsection)[Principio de la página](#mainsection)

### Analizar los datos del host

Los datos del host incluyen información acerca de componentes como el sistema operativo y las aplicaciones. Utilice el procedimiento siguiente para analizar la copia de los datos del host que obtuvo en la fase Obtener los datos.

1.  Identifique lo que busca. Es probable que haya una gran cantidad de datos del host, y que sólo parte de los datos sean pertinentes para el incidente. Por lo tanto, debe intentar crear criterios de búsqueda para eventos de interés. Por ejemplo, puede utilizar la herramienta Microsoft Windows® Sysinternals Strings para buscar los archivos ubicados en la carpeta \\Windows\\Prefetch. Esta carpeta contiene información como cuándo y dónde se iniciaron las aplicaciones. Para obtener información acerca de cómo utilizar la herramienta Strings y enviar o canalizar los resultados a un archivo de texto, consulte el [Capítulo 5: Ejemplo de escenario aplicado](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/959c31cd-216b-47fe-b821-7bb40d4156ae.mspx) de esta guía.

2.  Examine los datos del sistema operativo, incluida la información de deriva del reloj, y los datos cargados en la memoria del equipo host para intentar determinar si se están ejecutando o está programada la ejecución de aplicaciones o procesos malintencionados. Por ejemplo, puede utilizar la herramienta Windows Sysinternals AutoRuns para ver los programas que están configurados para ejecutarse durante el proceso de arranque o el inicio de sesión.

3.  Examine las aplicaciones, los procesos y las conexiones de red ejecutados. Por ejemplo, puede buscar procesos en ejecución que tengan un nombre apropiado pero se estén ejecutando desde ubicaciones no estándar. Use herramientas como Windows Sysinternals ProcessExplorer, LogonSession y PSFile para realizar estas tareas. Consulte la sección "Herramientas" del [Apéndice: Recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) de esta guía para obtener información acerca de estas herramientas.

[](#mainsection)[Principio de la página](#mainsection)

### Analizar los medios de almacenamiento

Los medios de almacenamiento que reunió durante la fase Obtener los datos contendrán muchos archivos. Debe analizar estos archivos para determinar su relevancia en el incidente. Puede tratarse de una tarea ardua, ya que los medios de almacenamiento como los discos duros y las cintas de copia de seguridad suelen contener miles de archivos.

Identifique los archivos que probablemente sean relevantes para analizarlos más a fondo. Utilice el procedimiento siguiente para extraer y analizar los datos de los medios de almacenamiento que reunió:

1.  Siempre que sea posible, realice el análisis sin conexión en una copia bit a bit de la evidencia original.

2.  Determine si se utilizó cifrado de datos, como EFS (Sistema de archivos de cifrado) en Microsoft Windows. Se pueden examinar varias claves de registro para determinar si EFS se utilizó alguna vez en el equipo. Para ver una lista de las claves de registro específicas, consulte la sección "Determinación de si EFS se está utilizando en un equipo" del artículo "[Sistema de archivos de cifrado en Windows XP y Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/deploy/cryptfs.mspx)" (en inglés) de Microsoft TechNet. Si cree que se ha utilizado cifrado de datos, debe determinar si realmente puede recuperar y leer los datos cifrados. Su capacidad para hacerlo dependerá de diferentes circunstancias, como la versión de Windows, si es un equipo unido al dominio y cómo se implementó EFS. Para obtener más información acerca de EFS, consulte "[Sistema de cifrado de archivos](http://www.microsoft.com/technet/security/guidance/cryptographyetc/efs.mspx)" en Microsoft TechNet. Las herramientas externas de recuperación EFS también están disponibles, como [Recuperación avanzada de datos EFS](http://www.elcomsoft.com/aefsdr.html) de Elcomsoft.

3.  Si es necesario, descomprima los archivos comprimidos. Aunque la mayoría del software forense puede leer archivos comprimidos de una imagen de disco, es posible que necesite descomprimir los archivos de almacenamiento para examinar todos los archivos de los medios que está analizando.

4.  Cree un diagrama de la estructura de directorios. Puede serle útil representar gráficamente la estructura de directorios y archivos de los medios de almacenamiento para analizar de forma eficaz los archivos.

5.  Identifique los archivos de interés. Si sabe a qué archivos afectó el incidente de seguridad, puede centrar la investigación en estos archivos primero. Los conjuntos hash creados por la [National Software Reference Library](http://www.nsrl.nist.gov/) se pueden utilizar para comparar los archivos conocidos (como los archivos de sistema operativo y de aplicación) con los originales. Normalmente, los archivos coincidentes pueden eliminarse de la investigación. También puede utilizar sitios de información como , [Wotsit's Format](http://www.wotsit.org/), [ProcessLibrary.com](http://www.processlibrary.com/) y [Ayuda de DLL](http://support.microsoft.com/dllhelp/default.aspx) de Microsoft para categorizar y reunir información sobre formatos de archivo existentes y para identificar archivos.

6.  Examine el registro, la base de datos que contiene la información de configuración de Windows, para obtener información acerca del proceso de arranque de equipo, las aplicaciones instaladas (incluidas las que se cargan durante el inicio) e información de inicio de sesión, como el nombre de usuario y el dominio de inicio de sesión. Para obtener información general del registro y descripciones detalladas del contenido del registro, consulte la [Referencia de registro del kit de recursos de Windows Server 2003](http://technet2.microsoft.com/windowsserver/en/library/56a33a88-a7b2-4f21-ab5e-5c62d728619f1033.mspx?mfr=true) (en inglés). Están disponibles varias herramientas para analizar el registro, como RegEdit, que se proporciona con el sistema operativo Windows, [Windows Sysinternals RegMon para Windows](http://go.microsoft.com/?linkid=6013256) y [Registry Viewer](http://www.accessdata.com/products/) de AccessData.

7.  Busque el contenido de todos los archivos recopilados para identificar los archivos que pueden se interesantes. Se pueden realizar varias búsquedas inteligentes con las herramientas descritas en la sección "Herramientas" del [Apéndice: Recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) de esta guía. Por ejemplo, puede utilizar la herramienta Windows Sysinternals Streams para ver si se han utilizado secuencias de datos NTFS alternativas en los archivos o carpetas. Las secuencias de datos NTFS alternativas pueden ocultar información dentro de un archivo aparentando que contiene cero bytes de datos cuando se ve en el Explorador de Windows, aunque el archivo contenga datos ocultos.

8.  Estudie los metadatos de los archivos de interés mediante herramientas como Encase de [Guidance Software](http://www.guidancesoftware.com/), Forensic Toolkit (FTK) de [AccessData](http://www.accessdata.com/) o ProDiscover de [Technology Pathways](http://www.techpathways.com/). Los atributos de archivo como las marcas de tiempo pueden mostrar las fechas de creación, del último acceso y la última escritura, que a menudo pueden resultar útiles al investigar un incidente.

9.  Utilice visores de archivos para ver el contenido de los archivos identificados que le permitan explorar y obtener una vista preliminar de determinados archivos sin la aplicación original que los creó. Este enfoque protege los archivos de daños accidentales y, a menudo, es más rentable que utilizar la aplicación nativa. Tenga en cuenta que los visores de archivos son específicos de cada tipo de archivo; si un visor no está disponible, utilice la aplicación nativa para examinar el archivo.

Después de analizar toda la información disponible, puede llegar a una conclusión. Sin embargo, es importante ser muy cauteloso en esta fase y asegurarse de que no se culpa a la parte equivocada de ningún daño. No obstante, si está seguro de sus conclusiones, puede iniciar la fase Informar acerca de la investigación.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía fundamental de investigación de equipos para Windows](http://go.microsoft.com/fwlink/?linkid=80345)

**Notificaciones de actualización**

[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)

[](#mainsection)[Principio de la página](#mainsection)
