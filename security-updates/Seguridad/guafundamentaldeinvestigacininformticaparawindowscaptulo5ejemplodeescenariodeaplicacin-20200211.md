---
TOCTitle: 'Guía fundamental de investigación informática para Windows: Capítulo 5: Ejemplo de escenario de aplicación'
Title: 'Guía fundamental de investigación informática para Windows: Capítulo 5: Ejemplo de escenario de aplicación'
ms:assetid: '959c31cd-216b-47fe-b821-7bb40d4156ae'
ms:contentKeyID: 20200211
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162849(v=TechNet.10)'
---

Guía fundamental de investigación informática para Windows
==========================================================

### Capítulo 5: Ejemplo de escenario de aplicación

Publicado: enero 11, 2007

Este escenario representa el acceso no autorizado a información confidencial interna dentro de una institución financiera nacional: el Banco de Woodgrove. El escenario es ficticio, al igual que las personas y las organizaciones mencionadas.

El escenario fue concebido para ofrecer una introducción de las herramientas y tecnologías utilizadas para la recopilación y el examen de datos. En una situación de infracción de seguridad real, deberá consultar con los grupos de administración, legales y de aplicación de la ley para pedirles consejo acerca de las técnicas de investigación apropiadas que debe utilizar. Además, a pesar de que los autores reconocen que imaginar una unidad de disco sospechosa es importante en el trabajo de investigación, es algo que escapa al ámbito de esta guía y sólo se menciona brevemente durante la fase de obtención de datos del escenario.

##### En esta página

[](#eiaa)[Escenario](#eiaa)
[](#ehaa)[Valorar la situación](#ehaa)
[](#egaa)[Obtener evidencia del acceso a datos confidenciales](#egaa)
[](#efaa)[Recopilación de evidencia remota](#efaa)
[](#eeaa)[Recopilación de evidencia local](#eeaa)
[](#edaa)[Analizar la evidencia recopilada](#edaa)
[](#ecaa)[Informar de la evidencia](#ecaa)
[](#ebaa)[Configuración de laboratorio del escenario de aplicación](#ebaa)

### Escenario

Ray Chow, Administrador de sistemas de la empresa, el Banco Nacional de Woodgrove, se ha fijado en que alguien se jactaba de conocer el salario de muchos empleados del banco. Ray averiguó el nombre del empleado que decía conocer dicha información: Mike Danseglio. Mike trabaja en el departamento de créditos y no debería tener acceso a ningún archivo de Recursos Humanos (RR.HH.).

El Banco Nacional de Woodgrove tiene una directiva relacionada con el uso correcto de los equipos bancarios. Esta directiva establece que no se permite el uso privado de equipos de la empresa en ningún caso, incluidos los servicios de correo electrónico y el acceso a sitios Web. La directiva también establece que no se cargará ningún programa en ninguno de los equipos sin la autorización por escrito del director de TI, y que cualquier intento de burlar las contraseñas u obtener acceso no autorizado a archivos del banco constituirá motivo de despido o de proceso judicial. La directiva también permite que el personal de TI instale cualquier tipo de dispositivos de supervisión de red, incluidos rastreadores u otros dispositivos de captura de paquetes, para mantener la seguridad de la red o investigar los posibles abusos.

Ray quiere asegurarse de que utiliza los procedimientos de investigación informática autorizados para investigar este tema e informar sobre sus conclusiones. Ray cree que esa información pudo obtenerse originalmente del servidor de archivos de RR.HH. y tiene previsto seguir el modelo de investigación informática de cuatro fases que se muestra en la figura siguiente:

![](images/Cc162849.80e07bd9-28f1-4bc8-b541-bc821af9f2a7(es-es,TechNet.10).gif)

**Figura 5.1. Introducción al modelo de investigación informática**

![](images/Cc162849.important(es-es,TechNet.10).gif)**Importante:**

Consulte la sección "Configuración de laboratorio del escenario de aplicación" al final de este capítulo para obtener más información sobre cómo emular este escenario y seguir sus pasos utilizando las herramientas.

[](#mainsection)[Principio de la página](#mainsection)

### Valorar la situación

Ray se reúne con la administración para valorar la situación. La administración indica que el acceso no autorizado y la distribución de información confidencial sobre salarios pueden ser motivo de despido, pero no iniciaran un proceso judicial contra un empleado por dichas acciones.

El Banco Nacional de Woodgrove declara que la administración consultará con el departamento legal interno para comprobar las leyes locales y determinar si existe alguna otra política que afecte a las investigaciones sobre el acceso inadecuado de los empleados a sistemas informáticos restringidos.

El departamento legal del Banco Nacional de Woodgrove proporciona una autorización por escrito a Ray para examinar el contenido del equipo de la empresa de Mike Danseglio. El equipo del departamento legal y administrativo solicitan que les informe del resultado de la investigación. También solicitan a Ray que realice un seguimiento para proteger los datos confidenciales de un modo más eficaz en el futuro si descubre que se ha producido una infracción.

La primera tarea de Ray es identificar los equipos implicados en la investigación y documentar la configuración del hardware de cada uno de ellos. Después de completar dicha tarea, Ray esboza un diagrama lógico de los equipos implicados, que se muestra siguiente.

![](images/Cc162849.1010ca24-547f-4899-9ad1-19ede8e19b12(es-es,TechNet.10).gif)

**Figura 5.2. Diagrama lógico de los equipos implicados en la investigación**

A continuación, Ray considera las diferentes opciones existentes para proceder con la investigación. Ya que parte de la información que necesita obtener son datos volátiles, Ray decide empezar la investigación informática interna analizando datos en tiempo real. Después creará una imagen de la unidad de Mike Danseglio y examinará la evidencia estática.

Ray crea una unidad USB que incluye las herramientas de investigación apropiadas para una investigación en tiempo real. (La sección "Herramientas" en el [Apéndice: Los recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) de esta guía describen las herramientas mencionadas en este capítulo).

La siguiente tarea de Ray es realizar un duplicado del disco duro de la parte sospechosa de forma que se proteja y se preserve la evidencia, en caso de localizar información que requiera para informar del caso al organismo encargado del cumplimiento de la ley.

Ray toma nota de los elementos de interés potencial, los documentos necesarios para identificar y autenticar la evidencia recopilada posteriormente en la investigación y crea un registro de auditoría de las acciones realizadas durante la investigación.

[](#mainsection)[Principio de la página](#mainsection)

### Obtener evidencia del acceso a datos confidenciales

La administración del Banco Nacional de Woodgrove autorizó a Ray para que examinara la estructura de directorios del servidor de archivos de RR.HH. (WNB-HQ-FS1) y los archivos de nóminas para determinar si un individuo no autorizado leyó los archivos. Ray podría dirigirse al equipo de Mike Danseglio inmediatamente y buscar la evidencia, o bien podría empezar con el servidor e intentar localizar la evidencia en los registros de auditoría. Ray también desea saber qué derechos de usuario posee Mike Danseglio en relación con las carpetas de RR.HH.

Ray decide utilizar el siguiente enfoque de dos pasos para obtener la evidencia:

1.  Examine el servidor de archivos de RR.HH. para buscar evidencia de un acceso no autorizado a archivos y carpetas confidenciales. Este examen puede que confirme o no la sospecha de la administración de que Mike Danseglio obtuvo acceso a estos archivos sin la autorización apropiada.

2.  Examine el contenido de unidad de disco de Mike Danseglio localmente y de forma remota para detectar cualquier tipo de dato confidencial. Ray tiene previsto utilizar una combinación de herramientas nativas de Microsoft® Windows® (incluidas Ipconfig, Systeminfo y Netstat) y herramientas de Windows Sysinternals (incluidas AccessChk, PsLoggedOn y PsFile).

Ray entrevista a miembros del equipo de RR.HH. y examina el servidor de archivos. Averigua que los archivos de nóminas se resumen una vez al mes en los archivos de hoja de cálculo que se almacenan en la carpeta RR.HH.\\Interno\\Nóminas. El grupo de gestión de recursos humanos es el único que debería tener permiso de lectura o escritura para esta carpeta, y Mike Danseglio no es un miembro de este grupo. Ray tiene que determinar si es posible que alguien obtenga acceso a la carpeta del departamento de RR.HH. que contiene la información de salarios de los empleados bancarios.

Ray visualiza los registros de sucesos para el servidor de archivos de RR.HH. Configuró previamente la auditoría de la carpeta RR.HH.\\Interno, para poder realizar un seguimiento de los accesos correctos y erróneos. Ray anota todos los pasos que realiza para abrir y visualizar el registro de sucesos de seguridad.

Varias de las entradas en el registro de sucesos destacan, como por ejemplo, la que se muestra en la captura de pantalla siguiente. Unas pocas entradas indican que una cuenta de usuario de mdanseglio obtuvo acceso al archivo **RR.HH.\\Interno\\Nóminas\\090806PR-A139.xls.**

![](images/Cc162849.2185f010-221f-41b9-bbf4-25c2591ef44d(es-es,TechNet.10).gif)

**Figura 5.3. Entradas del registro de sucesos de seguridad que indican que la cuenta de usuario de mdanseglio obtuvo acceso al archivo 090806PR-A139.xls de la carpeta RR.HH.\\Interno\\Nóminas**

Primero, Ray crea las carpetas nueva\\evidencia y \\herramientas en la unidad USB. Para garantizar la integridad de los archivos de evidencia que crea, Ray realizará un hash de cifrado MD-5 en todos los archivos que copie del equipo de Mike a la carpeta evidencia.

Los hash de cifrado MD-5 se crean ejecutando un algoritmo en un archivo para crear una "huella dactilar" única de 128 bits del contenido del archivo. Si alguien cuestiona la integridad de los datos recopilados por Ray (por ejemplo, para insinuar que el archivo podría haber sido editado posteriormente), Ray puede proporcionar el valor original de la suma de comprobación de MD-5 para su comparación y validación.

Ray exporta el conjunto de registros a una unidad USB etiquetada como HR01. Utilizará esta misma unidad USB para toda recopilación de evidencia.

![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

Al conectar una unidad USB a un equipo basado en Windows, se agrega una entrada al archivo **Setupapi.log** y se altera la clave de registro siguiente: **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Enum\\Storage\\RemovableMedia**

        ```
![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

La herramienta Sysinternals AccessChk requiere un proceso de instalación y dejará una huella en la unidad de disco local en la clave de registro siguiente: **HKEY\_CURRENT\_USER\\Software\\Sysinternals\\AccessChk**

Ray descubre que la cuenta de usuario de mdanseglio posee permiso de lectura y escritura para las subcarpetas \\Beneficios, \\Nóminas y \\Análisis de \\RR.HH.\\Interno, tal y como muestra la siguiente captura de pantalla:

![](images/Cc162849.89107cc0-71e0-4b6d-83d1-24e22c3e1521(es-es,TechNet.10).gif)

**Figura 5.4. Los resultados de AccessChk indican que la cuenta de usuario de mdanseglio posee permiso de lectura y escritura para las subcarpetas de RR.HH.\\Interno**

Ray sospecha que los errores de configuración de las autorizaciones del servidor de RR.HH. hicieron posible que Mike Danseglio obtuviera acceso a la carpeta RR.HH.\\Interno. Ray dedica algunos minutos en investigar los derechos de usuario de Mike Danseglio y se da cuenta de que es miembro de un grupo llamado branch01mgrs. Este grupo posee permisos de lectura y escritura para las carpetas de RR.HH.\\Interno.

        ```
Los resultados, que se muestran en la captura de pantalla siguiente, indican que Mike Danseglio tiene una sesión iniciada en WNB-HQ-FS1 en este momento.

![](images/Cc162849.0e12a08e-1f27-4852-81b2-6feb53b61773(es-es,TechNet.10).gif)

**Figura 5.5. Los resultados de Psloggedon indican que la cuenta de usuario de mdanseglio tiene una sesión iniciada en WNB-HQ-FS1**

Ray quita a Mike Danseglio del grupo branch01mgrs y reexamina sus derechos de usuario para la carpeta RR.HH.\\Interno.

Después revisar más los registros de sucesos de seguridad y los resultados de AccessChk para localizar otras posibles configuraciones de autorización incorrectas para la carpeta RR.HH.\\Interno, Ray empieza a investigar el contenido del equipo de Mike Danseglio utilizando técnicas de investigación remotas.

[](#mainsection)[Principio de la página](#mainsection)

### Recopilación de evidencia remota

Ray decide reunir información de forma remota del equipo de Mike Danseglio antes de intentar recopilar información localmente, y va a la oficina durante el fin de semana para realizar una copia forense del disco duro de Mike. En una situación real, Ray podría realizar toda su investigación forense en una imagen del disco duro del equipo de la parte sospechosa. Sin embargo, este escenario representa el uso de herramientas y técnicas para reunir evidencia volátil de forma local y remota.

Ray utiliza una unidad USB conectada a su propio equipo que contiene numerosas herramientas. La unidad USB almacenará toda la evidencia recopilada, así como un registro de archivos de texto de todos los comandos que escriba.

Ray utiliza el siguiente el procedimiento básico, que le permite marcar la hora en que empieza su examen, recopila la evidencia del equipo de Mike Danseglio a través de la red, registra todos los pasos de la investigación y crea un hash MD5 de la evidencia recopilada.

![](images/Cc162849.important(es-es,TechNet.10).gif) **Importante:**

Algunas herramientas de Sysinternals, incluidas PsExec, PsFile y PsLogList, las bloquea la configuración predeterminada del firewall de Windows. Para seguir este ejemplo aplicado y utilizar estas herramientas para examinar qué información puede reunirse a través de la red, tiene que hacer clic en la ficha **Excepciones** del firewall de Windows y habilitar **Compartir archivos e impresoras.** Sin embargo, usted NO necesita compartir nada.

En los equipos de destino con el firewall de Windows habilitado y Compartir archivos e impresoras deshabilitado (la configuración predeterminada), las herramientas Systeminfo, Ipconfig, Arp, Netstat, Schtasks, PsFile, PsList y PsLogList deberán ejecutarse directamente en el equipo de destino. En tal caso, ejecute cada una de estas herramientas directamente en el sistema de destino y canalice los resultados al archivo **evidence2.txt** creado en la sección "Recopilación de evidencia local" de este capítulo.

1.  Obtener acceso a la unidad USB.

    Ray obtiene acceso a la unidad USB y la carpeta \\herramientas, que contiene sus herramientas de línea de comandos (incluidas PsExec y la herramienta File Checksum Integrity Validator (FCIV)).

    
        ```
2.  Anotar la fecha y hora de inicio del examen.

    Ray canaliza los resultados de los comandos de fecha y hora para registrar la hora de inicio de su investigación en un nuevo archivo **mdevidence.txt** creado en la carpeta \\evidencia de su unidad USB. (Ray obtendrá la hora de sistema del equipo de Mike Danseglio en el paso 3.) Además, Ray buscará cualquier tipo de discrepancia entre la fecha y hora del BIOS y la fecha y hora real.

    
        ```
3.  Obtener información básica del equipo de destino.

    Ray ejecuta una serie de comandos nativos de Windows para obtener información sobre el equipo de Mike.

    
        ```
    ![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

    PsExec reúne información de forma remota utilizando los servicios ya existentes en el equipo de destino, como por ejemplo, Cmd y Ipconfig. PsExec también se puede utilizar para cargar servicios a través de la red para ejecutarlos en el equipo de destino. Ray no quiere instalar ninguna aplicación en el equipo de Mike; sólo ejecuta servicios compatibles con el sistema operativo Windows XP en el equipo de Mike

4.  Ejecutar herramientas remotas que utilizan interfaces de programación de aplicación local (API).

    Ray ejecuta ahora varias herramientas para determinar si otros equipos tienen los archivos abiertos en el equipo de Mike, los procesos en ejecución en el equipo, y obtener los registros de sucesos de seguridad del equipo.

    
        ```
    -   PsFile muestra archivos abiertos de forma remota Esta herramienta utiliza API remotas de Windows y no es preciso cargarlo en el equipo de destino.

    -   PsList muestra información acerca de los procesos y subprocesos en ejecución en un equipo. Esta herramienta utiliza API remotas de Windows y no es preciso cargarlo en el equipo de destino.

    -   PsLogList vuelca el contenido del registro de sucesos del equipo de forma predeterminada, no se precisa ningún parámetro adicional. Ray ejecuta este comando con el parámetro **sec** para obtener el registro de sucesos de seguridad.

5.  Crear un registro de todas las tareas.

    Windows realiza un seguimiento automático de todos los comandos ejecutados en un símbolo del sistema. Ray utiliza el comando Doskey para capturar este registro y canaliza la información de historial en un archivo llamado **mdevidence-doskey. txt.**

    
        ```
6.  Realice una suma de comprobación MD5 en los archivos de evidencia.

    Ray utiliza la herramienta FCIV para realizar una suma de comprobación MD5 en los archivos de evidencia.

    
        ```
![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

Las limitaciones de la pantalla podrían hacer que el comando anterior se muestre en más de una línea. Debe escribirse como una sola línea en el símbolo del sistema.

La herramienta FCIV calcula y comprueba los valores hash de cifrado. Esta herramienta está disponible a través del artículo de Microsoft Knowledge Base 841290.

        ```
Aunque se pide a todos los usuarios que conserven los documentos en el servidor de red, Ray advierte que Mike Danseglio tiene una carpeta personal en su equipo. Esta carpeta incluye una hoja de cálculo y una subcarpeta de \\xxxpixset.

Después de revisar de forma remota las carpetas del equipo de Mike, Ray está listo para informar sobre sus conclusiones y trasladarse al equipo de Mike para realizar la investigación de forma local.

Jill Shrader, el administrador del departamento de RR.HH., llama a Ray en su teléfono móvil y le pregunta sobre el estado de la investigación. Ray le explica que ha reunido la información siguiente:

-   La cuenta de usuario de Mike Danseglio poseía permisos de lectura y de escritura para la carpeta RR.HH.\\Interno porque había sido agregado por error al grupo branch01mgrs, que posee permisos para esta carpeta y sus subcarpetas.

-   El equipo de Mike posee una carpeta personal en su disco duro que contiene por lo menos una hoja de cálculo.

-   El equipo de Mike contiene dos programas no autorizados que le permiten supervisar el tráfico de la red y examinar la red en busca de servicios y equipos.

-   El equipo de Mike tiene una amplia colección de archivos de imagen en su disco duro y Ray sospecha que se trata de imágenes pornográficas.

[](#mainsection)[Principio de la página](#mainsection)

### Recopilación de evidencia local

Idealmente, las investigaciones informáticas deberían realizarse en imágenes de disco duro. En este ejemplo, sin embargo, Ray ejecuta una serie de herramientas directamente en el equipo de Mike Danseglio. Estas herramientas se ejecutan en una unidad USB y no requieren su instalación en el equipo local. Sin embargo, tal como se ha mencionado anteriormente en este capítulo, la inserción de la unidad USB dejará una huella en el registro.

![](images/Cc162849.important(es-es,TechNet.10).gif) **Importante:**

Si el equipo de Mike Danseglio hubiera tenido habilitado el firewall de Windows con Compartir archivos e impresoras deshabilitado, Ray debería haber ejecutado las herramientas Systeminfo, Ipconfig, Arp, Netstat, Schtasks, PsFile, PsList y PsLogList de forma local en equipo de Mike. Ray escribiría los comandos enumerados en la anterior sección de este capítulo, "Recopilación de evidencia remota", pero quitaría la referencia a \\\\hqloan164 antes de canalizar los resultados al archivo **evidence2.txt** creado en esta sección.

Ray tiene previsto realizar las siguientes tareas en el equipo de Mike:

-   Buscar evidencia de archivos confidenciales en la unidad de disco.

-   Obtener copias de cualquier archivo sospechoso.

-   Examinar los archivos.

Ray inicia sesión en el equipo de Mike mediante la cuenta de Administrador para obtener acceso a la carpeta personal de Mike. Ray utiliza el siguiente procedimiento básico después de conectar la unidad USB de recopilación de evidencia en el equipo de Mike:

1.  Obtener acceso a la carpeta personal de Mike Danseglio.

    Ray obtiene acceso a la carpeta personal de Mike con los comandos siguientes.

    
        ```
2.  Anotar la fecha y hora de inicio del examen.

    Ray canaliza los resultados de los comandos Fecha y Hora para registrar la hora de inicio de su investigación. Canaliza los resultados a un archivo **mdevidence2.txt** nuevo creado en la carpeta \\evidencia del disco USB.

    
        ```
    ![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

    La unidad USB se designa unidad F: en el equipo de Mike.

3.  Obtener información de la estructura de directorios.

    Ray utiliza el comando Dir para examinar el contenido de la carpeta personal de Mike. Primero, Ray canaliza los resultados a la pantalla para visualizar los resultados y advierte un archivo de hoja de cálculo y la carpeta \\xxxpixset. A continuación, Ray canaliza los resultados del comando Dir al archivo de evidencia utilizando tres parámetros diferentes: /tc, para mostrar la hora de creación, /ta para mostrar la última hora de acceso, y /tw, para mostrar la última hora de escritura.

    
        ```
4.  Obtener acceso a la unidad USB.

    Ray obtiene acceso a la unidad USB y a la carpeta \\herramientas que contiene sus herramientas de línea de comandos.

    
        ```
5.  Reunir información de archivo de Mike Danseglio.

    Ray utiliza la utilidad Du para examinar el contenido de la carpeta Mis documentos y de cualquier subcarpeta de Mike Danseglio. Utiliza el parámetro –I 5 para buscar a una profundidad de cinco carpetas. Ray examina primero los resultados en la pantalla (que se muestran en la captura de pantalla siguiente) antes de canalizar la evidencia al archivo **mdevidence2.txt.**

    
        ```
    ![](images/Cc162849.e08dd6a3-ffd8-41a9-bd1e-8f487f69508b(es-es,TechNet.10).gif)

    **Figura 5.6. Los resultados de ejecutar la utilidad Du**

6.  Copie los archivos sospechosos a la carpeta \\evidencia\_archivos.

    Aunque Ray creó una imagen de toda la unidad de disco de Mike Danseglio, decide copiar los archivos de la carpeta personal de Mike Danseglio en una carpeta nueva denominada **evidencia\_archivos** que ha creado en la unidad USB. Ray examinará la carpeta y los archivos durante el proceso del análisis.

    ![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

    Ray obtuvo una copia del archivo original durante el proceso de creación de imagen. Puede realizar un hash en el archivo original que encontró en la unidad de disco en tiempo real si desea comparar este archivo con la copia del archivo de su unidad USB.

    Ray utiliza el comando Xcopy con el parámetro /s para copiar subcarpetas, el parámetro /e para copiar subcarpetas, incluso si están vacías, el parámetro /k para retener el atributo de sólo lectura en los archivos de destino, si se encuentra en los archivos de origen, y el parámetro /v para comprobar cómo está escrito cada archivo en el archivo de destino, para cerciorarse de que los archivos de destino son idénticos a los archivos de origen.

    
        ```
7.  Examinar el contenido de la papelera de reciclaje.

    Ray hace una revisión rápida del contenido de la papelera de reciclaje del equipo de Mike Danseglio, que contiene numerosos archivos eliminados como se muestra en la figura siguiente. Ray sabe que el proceso de imagen de la unidad de disco obtuvo una copia de estos archivos, en caso de que desee revisar los archivos más tarde. Después de observar el contenido de la papelera de reciclaje, Ray está listo para revisar la evidencia que recopilada de forma remota y local.

    ![](images/Cc162849.1947d37b-f6aa-45d5-8899-e0de76cdb382(es-es,TechNet.10).gif)

    **Figura 5.7. Varios archivos de imagen localizados en la Papelera de reciclaje**

[](#mainsection)[Principio de la página](#mainsection)

### Analizar la evidencia recopilada

Ray tiene dos archivos de evidencia: **mdevidence.txt** y **mdevidence2.txt.** También tiene una copia de la carpeta personal de Mike Danseglio. Ray utiliza el procedimiento siguiente en su propio equipo para analizar la información contenida en estos archivos.

1.  Analizar la información del proceso.

    Ray revisa el archivo **mdevidence.txt.** Los resultados de PsList son muy interesantes, porque indican que Mike Danseglio ejecuta algunas aplicaciones no autorizadas, incluidas Wireshark y nMapWin, como se muestra en la captura de pantalla siguiente.

    Ray sabe que no es inusual encontrar infracciones que no están relacionadas al realizar una investigación en un equipo sospechoso. Ray entiende también que no todas aplicaciones se reconocerán fácilmente (como las enumeradas en este escenario) y que también es posible que fueran instaladas sin el conocimiento de Mike.

    ![](images/Cc162849.defe0f97-b28f-4300-9df3-d6fa832d1c59(es-es,TechNet.10).gif)

    **Figura 5.8. Resultados de Pslist ejecutado en el equipo de Mike Danseglio**

2.  Obtener acceso a la unidad USB.

    Ray obtiene acceso a la unidad USB y a la carpeta \\herramientas que contiene sus herramientas de línea de comandos.

    
        ```
3.  Buscar cadenas sospechosas en el archivo de hoja de cálculo.

    Ray busca la cadena "confidencial" en sus copias de los archivos de la carpeta personal de Mike. Para ello, utiliza el comando Buscar con el parámetro /I (este parámetro ignora este parámetro ignora si los caracteres están en mayúscula o minúscula al buscar la cadena) y el parámetro /c (este parámetro ofrece el número de líneas que contienen la cadena).

    Primero, Ray canaliza a la pantalla. Se muestra que el archivo **090806PR-A139.xls** contiene una coincidencia, tal como se muestra en la captura de pantalla siguiente. Por lo tanto, Ray ejecuta el comando por segunda vez para canalizar los resultados a un archivo **mdevidence-review.txt.**

    
        ```
    ![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

    Las limitaciones de la pantalla podrían hacer que el comando anterior se muestre en más de una línea. Debe escribirse como una sola línea en el símbolo del sistema.

    ![](images/Cc162849.2a056bdd-f29e-4327-b88c-add5b50ef92b(es-es,TechNet.10).gif)

    **Figura 5.9. Resultados de la búsqueda de "confidencial," encontrado en 090806PR-A139.XLS**

4.  Ray copia primero **090806PR-A139.xls** a la carpeta \\evidencia\_archivos y luego utiliza la herramienta de cadenas para enumerar las cadenas ASCII y Unicode incluidas en el archivo de hoja de cálculo.

    
        ```
    Los resultados (que se muestran en la captura de pantalla siguiente) indican que el archivo de hoja de cálculo contiene información sobre nóminas. Ray ejecuta la herramienta de cadenas otra vez y canaliza los resultados a su archivo **mdevidence-review.txt.**

    
        ```
    ![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

    Las limitaciones de la pantalla podrían hacer que el comando anterior se muestre en más de una línea. Debe escribirse como una sola línea en el símbolo del sistema.

    ![](images/Cc162849.ad4cc4e5-9d54-47f3-99cb-694d01db0e66(es-es,TechNet.10).gif)

    **Figura 5.10. Resultados de ejecutar la utilidad de cadenas en el archivo de hoja de cálculo**

    Ray está seguro de que ha localizado una copia no autorizada del archivo de salarios de RR.HH. en el equipo de Mike Danseglio.

[](#mainsection)[Principio de la página](#mainsection)

### Informar de la evidencia

Ray analiza y ordena la evidencia y luego escribe un informe donde resume sus conclusiones. Hay un modelo de informe disponible en los materiales que acompañan esta guía, mencionados en la sección "Hojas de cálculo" del [Apéndice: Recursos](http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx) En este informe, Ray incluye recomendaciones para proteger los datos confidenciales de futuras infracciones- Ray realiza también una comprobación de la integridad de los datos en los archivos de evidencia y luego almacena los archivos adecuadamente grabándolos junto al informe final en un CD.

El informe de Ray incluye la información siguiente:

-   **Objetivo del informe.** El objetivo del informe es aconsejar a la administración del Banco de Woodgrove acerca del incidente y explicar de qué modo los resultados de la investigación pueden ser utilizados para evitar futuras infracciones de seguridad.

-   **Autor del informe.** Ray se identifica, proporciona su cargo, y declara que se ha atenido a su responsabilidad de directivo técnico.

-   **Resumen del incidente.** Esta sección enumera las sospechas iniciales y la repercusión empresarial del incidente.

-   **Evidencia.** Esta sección incluye la lista de procesos ejecutados, el directorio personal encontrado en el equipo de Mike Danseglio, las imágenes explícitas encontradas, la lista de aplicaciones inaceptables ejecutadas y la ubicación de un archivo confidencial que contiene información de nóminas.

-   **Análisis.** Esta sección incluye los resultados de las investigaciones locales y remotas, que demuestra que se descargaron imágenes sexualmente explícitas, se configuraron incorrectamente los permisos y que se obtuvo acceso a un archivo confidencial que contiene información de nóminas.

-   **Conclusión** Esta sección resume el resultado de la investigación e incluye las recomendaciones para evitar incidentes similares en el futuro.

-   **Documentos de soporte.** Esta sección incluye diagramas de red y una lista de los procedimientos de investigación informática y tecnologías utilizadas en la investigación.

Después de presentar su informe, Ray espera la autorización necesaria para realizar pasos adicionales en la investigación, o cualquier otro tipo de acciones que pueda solicitar la administración.

![](images/Cc162849.note(es-es,TechNet.10).gif)**Nota:**

Cada investigación puede ser diferente. Deberá utilizar herramientas apropiadas para la tarea necesaria y que le ayuden a obtener la información que busca, pero siempre es una idea buena reunir más evidencia de la que podría ser necesaria.

[](#mainsection)[Principio de la página](#mainsection)

### Configuración de laboratorio del escenario de aplicación

Para emular este escenario de aplicación en un entorno de laboratorio de pruebas, deberá completar los pasos siguientes:

1.  Implementar equipos y crear un dominio de servicio de directorio de Active Directory®.

2.  Crear usuarios y grupos en Active Directory.

3.  Crear carpetas y archivos en equipos específicos.

4.  Asignar recursos compartidos y permisos.

5.  Configurar auditorías.

#### Implementar equipos y crear dominio

La tabla siguiente muestra una lista de los equipos y los sistemas operativos que necesitará:

**Tabla 5.1. Equipos y sistemas operativos utilizados en el laboratorio del escenario de aplicación**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del equipo</th>
<th style="border:1px solid black;" >Sistema operativo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">WNB-HQ-DC</td>
<td style="border:1px solid black;">Windows Server® 2003 R2</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WNB-HQ-FS1</td>
<td style="border:1px solid black;">Windows Server 2003 R2</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">HQ-IT-PC10</td>
<td style="border:1px solid black;">Windows XP Profesional SP2</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">HQLOAN164</td>
<td style="border:1px solid black;">Windows XP Profesional SP2</td>
</tr>
</tbody>
</table>
  
Después que instalar el sistema operativo en cada equipo, ejecute Dcpromo en WNB-HQ-DC para instalar Active Directory y DNS.
  
#### Crear usuarios y grupos
  
La tabla siguiente muestra una lista de los grupos y los usuarios que deberán definirse en Usuarios y equipos de Active Directory de Microsoft Management Console (MMC):
  
**Tabla 5.2. Grupos y usuarios mencionados en el laboratorio del escenario de aplicación**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupos</th>
<th style="border:1px solid black;" >Usuarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administrador de sistemas de la empresa</td>
<td style="border:1px solid black;">Ray Chow</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Administradores del dominio</td>
<td style="border:1px solid black;">Ray Chow</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Administradores de RR.HH.</td>
<td style="border:1px solid black;">Hembra Gottfried, Roland Winkler, Jill Shrader</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Branch01Mgrs</td>
<td style="border:1px solid black;">Mike Danseglio, Nuria Gonzalez</td>
</tr>
</tbody>
</table>
  
En el servidor de archivos WNB-HQ-FS1, el grupo de administradores del dominio está agregado como miembro del grupo de administradores local.
  
#### Crear carpetas y archivos
  
La tabla siguiente muestra una lista de los nombres de dispositivo, las estructuras de directorios y los archivos incluidos que necesitará:
  
**Tabla 5.3. Dispositivos, carpetas y archivos utilizados en el laboratorio del escenario de aplicación**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Dispositivo (equipo o lápiz USB)</th>
<th style="border:1px solid black;" >Carpetas</th>
<th style="border:1px solid black;" >Archivos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">WNB-HQ-FS1 (servidor de archivos)</td>
<td style="border:1px solid black;">\RR.HH.\Interno\Beneficios
\RR.HH.\Interno\Nóminas
\RR.HH.\Interno\Análisis
\Herramientas</td>
<td style="border:1px solid black;">090806PR-A139.xls
(Esta carpeta contiene todas las herramientas SysInternal y la herramienta FCIV, tal como se enumeran en la sección &quot;Herramientas&quot; del <a href="http://www.microsoft.com/spain/technet/security/guidance/disasterrecovery/computer_investigation/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx">Apéndice: Recursos</a>.)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">HQLOAN164 (equipo de Mike Danseglio)</td>
<td style="border:1px solid black;">Documents and Settings\mdanseglio\Mis Documentos\Personal
Documents and Settings\mdanseglio\Mis Documentos\Personal\xxxpixset</td>
<td style="border:1px solid black;">090806PR-A139.xls
(Esta carpeta contiene varios archivos .jpg que incluyen xxx como parte del nombre de archivo. Varios archivos xxx*.* fueron eliminados de esta carpeta y se encuentran en la papelera de reciclaje).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">HQ-IT-PC10 (equipo de Ray Chow)</td>
<td style="border:1px solid black;">\Herramientas</td>
<td style="border:1px solid black;">(Esta carpeta contiene todas las herramientas SysInternal y la herramienta FCIV, tal como se enumeran en la sección &quot;Herramientas&quot; del <a href="http://www.microsoft.com/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx">Apéndice: Recursos</a>.)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Lápiz USB (lápiz USB de Ray Chow)</td>
<td style="border:1px solid black;">\Evidencia
\Evidencia_archivos
\Herramientas</td>
<td style="border:1px solid black;">(Esta carpeta contiene todas las herramientas SysInternal y la herramienta FCIV, tal como se enumeran en la sección &quot;Herramientas&quot; del<a href="http://www.microsoft.com/a9a5c2a9-cce3-4edb-a92c-10983899240a.mspx">Apéndice: Recursos</a>.)</td>
</tr>
</tbody>
</table>
  
#### Asignar recursos compartidos y permisos
  
La tabla siguiente muestra una lista de las carpetas de archivo y comparte los permisos necesarios para el servidor de archivos WNB-HQ-FS1:
  
**Tabla 5.4. Carpetas y permisos de recursos compartidos del laboratorio del escenario de aplicación**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Carpeta</th>
<th style="border:1px solid black;" >Permisos de recursos compartidos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">\RR.HH.</td>
<td style="border:1px solid black;">Branch01Mgrs (control total, de modificación, de lectura)
HR MGRS (control total, de modificación, de lectura)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">\Herramientas</td>
<td style="border:1px solid black;">No compartido; sólo para uso local por usuarios que tienen credenciales administrativas del servidor.</td>
</tr>
</tbody>
</table>
  
#### Configurar auditorías.
  
En el controlador de dominio WNB-HQ-DC, la política **Acceso a objetos de auditoría** está configurada para auditar tanto los casos correctos como los erróneos. Esta configuración se establece a través de la Domain Security Policy MMC y de la Domain Controller Security Policy MMC.
  
En el servidor de archivos WNB-HQ-FS1, la auditoría está configurada para el grupo de usuarios de dominio en la carpeta RR.HH.\\Interno. Para lograr esta configuración, haga clic con el botón secundario en la carpeta y seleccione **Propiedades, Seguridad, Avanzado** y, a continuación **Auditoría.** Luego introduzca el grupo **Usuarios de dominio.**
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía fundamental de investigación de equipos para Windows](http://go.microsoft.com/fwlink/?linkid=80345)
  
**Notificaciones de actualización**
  
[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)
  
[](#mainsection)[Principio de la página](#mainsection)
