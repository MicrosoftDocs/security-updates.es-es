---
TOCTitle: 'Guía fundamental de investigación informática para Windows: Capítulo 2: Obtener los datos'
Title: 'Guía fundamental de investigación informática para Windows: Capítulo 2: Obtener los datos'
ms:assetid: '89ae3bbe-057c-4d3e-99e1-f7356321c01f'
ms:contentKeyID: 20200208
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162837(v=TechNet.10)'
---

Guía fundamental de investigación informática para Windows
==========================================================

### Capítulo 2: Obtener los datos

Publicado: enero 11, 2007

Este capítulo trata sobre cómo obtener los datos necesarios para la investigación. Algunos datos de la investigación informática son frágiles, sumamente volátiles, y pueden ser modificados o dañados con facilidad. Por lo tanto, usted necesita garantizar que los datos se recopilen y se conserven correctamente antes del análisis. Utilice el proceso de tres pasos que se muestra en la figura siguiente.

![](images/Cc162837.fff0169f-2011-4eb8-870f-f83eedaa5942(es-es,TechNet.10).gif)

**Figura 2.1. La fase de obtención del modelo de investigación informática**

##### En esta página

[](#edaa)[Crea un kit de herramientas de investigación informática](#edaa)
[](#ecaa)[Recopilar los datos](#ecaa)
[](#ebaa)[Almacenar y archivar](#ebaa)

### Crea un kit de herramientas de investigación informática

Su organización necesitará una colección de herramientas de hardware y software para obtener los datos durante una investigación. Este kit de herramientas puede que contenga un equipo portátil con herramientas apropiadas de software, sistemas operativos y revisiones, medios de aplicación, dispositivos de copia de seguridad protegidos contra escritura, soportes vírgenes, equipo de red básico y cables. Idealmente, este kit de herramientas se creará con antelación, y los miembros del equipo estarán familiarizados con las herramientas antes de tener que realizar una investigación.

![](images/Cc162837.note(es-es,TechNet.10).gif)**Nota:**

Consulte las secciones "Preparación de su organización para una investigación informática" y "Herramientas" del [Apéndice: Recursos](https://technet.microsoft.com/es-es/library/a9a5c2a9-cce3-4edb-a92c-10983899240a(v=TechNet.10)) de esta guía para una lista de herramientas de software propuestas que pueden incluirse en el kit de herramientas de la investigación informática y para instrucciones en la creación de un kit de herramientas.

[](#mainsection)[Principio de la página](#mainsection)

### Recopilar los datos

La recopilación de datos de evidencia digital puede realizarse localmente o a través de una red. Obtener los datos localmente tiene la ventaja de poseer un mayor control sobre el equipo o equipos y los datos implicados. Sin embargo, no siempre es posible (por ejemplo, cuándo los equipos están en espacios cerrados u otras ubicaciones, o bien cuando hay implicados servidores de alta disponibilidad). Otros factores, como el secreto de la investigación, la naturaleza de la evidencia que debe reunirse y el marco temporal de la investigación determinarán en última instancia si la evidencia se recopila localmente o a través de la red.

![](images/Cc162837.important(es-es,TechNet.10).gif)**Importante:**

Cuando se usan herramientas para recopilar los datos, es importante determinar primero si se ha instalado o no un rootkit. Los rootkits son componentes de software que se encargan del control completo de un equipo y ocultan su existencia ante las herramientas de diagnóstico estándar. Debido a que los rootkits operan en un nivel muy bajo del hardware, pueden interceptar y modificar llamadas de sistema. Usted no puede encontrar un rootkit buscando su ejecutable, ya que el rootkit se elimina de la lista de resultados de búsqueda retornados. El examen de los puertos no revela que los puertos utilizados por el rootkit estén abiertos, porque el rootkit evita que el examen detecte el puerto abierto. Por lo tanto, es difícil asegurar que no existe ningún rootkit. Una herramienta disponible que puede utilizar es Microsoft® Windows® Sysinternals [RootkitRevealer.](http://go.microsoft.com/?linkid=6013255)

Al obtener los datos a través de una red, debe tener en cuenta el tipo de datos que deben recopilarse y la cantidad de esfuerzo que se va a emplear. Considere qué datos necesita obtener para apoyar la acusación de las partes causantes del conflicto. Por ejemplo, puede que sea necesario obtener datos de varios equipos a través de diferentes conexiones de red, o quizás sea suficiente copiar un volumen lógico de un sólo equipo.

El proceso recomendado para la obtención de datos es el siguiente:

1.  Cree documentación precisa que después le permita identificar y autenticar la evidencia que usted recopila. Asegúrese de tener en cuenta todos los artículos potencialmente interesantes y registre todas las actividades que puedan ser relevantes posteriormente en la investigación. La clave para una investigación satisfactoria es la documentación apropiada, incluida información como la siguiente:

    -   Quién realizó la acción y por qué. ¿Qué intentaban conseguir?

    -   Cómo realizaron la acción, incluidas las herramientas utilizadas y los procedimientos empleados.

    -   Cuándo realizaron la acción (la fecha y la hora) y sus resultados.

2.  Determine qué métodos de investigación deben utilizarse. Normalmente se utiliza una combinación de investigaciones sin conexión y en línea.

    -   En las investigaciones sin conexión, el análisis adicional es realizado mediante copia a nivel de bits de la evidencia original. (Una copia a nivel de bits es una copia completa de todos los datos del origen dirigido, incluida información como el sector de arranque, la partición y el espacio en disco sin asignar). Debería utilizar el método de investigación sin conexión siempre que sea posible, ya que mitiga el riesgo de dañar la evidencia original. Sin embargo, este método es sólo conveniente para situaciones en las que se puede crear una imagen, de modo que no puede ser utilizada para reunir algunos datos volátiles.

    -   En una investigación en línea, el análisis se realiza mediante la evidencia original en directo. Deberá ser especialmente cuidadoso al realizar el análisis en línea de datos debido al de alterar la evidencia que podría requerirse para demostrar un caso.

3.  Identifique y documente los orígenes de datos potenciales, incluidos los siguientes:

    -   Servidores. La información del servidor incluye la función de servidor, registros (como registro de eventos), archivos y aplicaciones.

    -   Registros de dispositivos de red con acceso interno y externo, tales como firewalls, enrutadores, servidores proxy, servidores de acceso a redes (NAS), y sistemas de detección de intrusos (IDS) que podrían utilizarse en la posible ruta del ataque.

    -   Componentes de hardware internos, como adaptadores de red, que incluyen información de dirección de Media Access Control (MAC) y tarjetas PCMCIA. Tenga en cuenta también tipos de puerto externos, tales como Firewire, USB y PCMCIA.

    -   Dispositivos de almacenamiento que deben obtenerse (internos y externos), incluidos discos duros, dispositivos de almacenamiento de red y dispositivos extraíbles. No se olvide de dispositivos móviles portátiles, como por ejemplo, Pocket PC, dispositivos de Smartphone y reproductores MP3, por ejemplo, Zune™.

4.  Cuándo tiene que capturar datos volátiles, estudie cuidadosamente el orden en el que recopila los datos. La evidencia volátil puede destruirse fácilmente. La información del tipo procesos de ejecución, datos cargados en la memoria, tablas de enrutamiento y archivos temporales, puede perderse para siempre cuando el equipo se apaga. La información acerca de herramientas y comandos que puede ayudar a reunir esta información está disponible en la sección "Herramientas" de [Apéndice: Recursos](https://technet.microsoft.com/es-es/library/a9a5c2a9-cce3-4edb-a92c-10983899240a(v=TechNet.10)) de esta guía.

5.  Utilice los métodos siguientes para recopilar información de configuración de medios de almacenamiento y de medios de almacenamiento mediante grabación:

    -   Si necesita eliminar algún dispositivo de almacenamiento interno, apague el equipo primero. Sin embargo, antes de apagar el equipo, deberá comprobar que todos datos volátiles se han capturado, siempre que sea posible.

    -   Determine si desea eliminar el dispositivo de almacenamiento del equipo sospechoso y utilizar su propio sistema para obtener los datos. Puede que no sea posible eliminar el dispositivo de almacenamiento debido a consideraciones e incompatibilidades de hardware. Normalmente no desconectará dispositivos de almacenamiento tales como dispositivos RAID, dispositivos de almacenamiento dependientes de hardware (por ejemplo, equipo heredado), ni dispositivos en sistemas de almacenamiento de red, como por ejemplo, redes de área de almacenamiento (SAN).

    -   Cree una copia a nivel de bits de la evidencia en un destino de copia de seguridad y asegúrese de que los datos originales están protegidos contra escritura. El análisis de datos posterior debe realizarse en esta copia y no en la evidencia original. Realizar un recorrido paso a paso para la imagen es algo que queda fuera del ámbito de esta guía, pero es una parte integral de la recopilación de la evidencia.

        ![](images/Cc162837.important(es-es,TechNet.10).gif)**Importante:**

        Las herramientas aceptadas habitualmente por la industria al obtener una copia a nivel de bits. Por ejemplo, EnCase, de [Guidance Software](http://www.guidancesoftware.com/) o FTK, de [AccessData.](http://www.accessdata.com/)

    -   Documente los dispositivos de almacenamiento internos y asegúrese de incluir información acerca de sus configuraciones. Por ejemplo, anote el fabricante y el modelo, la configuración de puente y el tamaño del dispositivo. Además, tenga en cuenta el tipo de interfaz y el estado de la unidad.

6.  Compruebe los datos recopilados. Cree sumas de comprobación y firmas digitales cuando sea posible con el fin de ayudar a establecer que los datos copiados son idénticos al original. En determinadas circunstancias (por ejemplo, si hay un sector dañado en el medio de almacenamiento) puede que no sea posible crear una copia perfecta. Asegúrese de obtener la mejor copia posible con las herramientas y recursos disponibles. Puede utilizar el [Microsoft File Checksum Integrity Verifier](http://www.microsoft.com/downloads/details.aspx?familyid=b3c93558-31b7-47e2-a663-7365c1686c08&displaylang=en) (FCIV) herramienta para calcular un hash de cifrado MD5 o SHA1 del contenido de un archivo.

[](#mainsection)[Principio de la página](#mainsection)

### Almacenar y archivar

Cuándo se ha recopilado la evidencia y está lista para su análisis, es importante almacenarla y archivarla de forma que se garantice su seguridad e integridad. Deberá seguir cualquier proceso de almacenamiento y archivado existente en su organización.

Las prácticas recomendadas para el almacenamiento y archivado de datos incluyen lo siguiente:

-   Proteja físicamente y almacene la evidencia en una ubicación inviolable.

-   Asegúrese de que el personal no autorizado no tenga acceso a la evidencia, ya sea a través de la red o de otro modo. Documente quién tiene acceso físico y de red a la información.

-   Proteja al equipo de almacenamiento de los campos magnéticos. Utilice soluciones de almacenamiento de control estático para proteger el equipo de almacenamiento de la electricidad estática.

-   Haga por lo menos dos copias de la evidencia recopilada y almacene una copia en una ubicación segura fuera del sitio.

-   Asegúrese de que la evidencia esté protegida físicamente (por ejemplo, colocando la evidencia en una caja de seguridad) y digitalmente (por ejemplo, asignando una contraseña a los medios del almacenamiento).

-   Documente claramente la cadena de custodia de la evidencia. Cree una lista de protección/desprotección que incluya información como el nombre de la persona que examina la evidencia, la fecha y hora exactas en que se desproteja la evidencia y la fecha y hora exacta en que se devuelva. Se incluye un documento de muestra **Hoja de cálculo: Documentación de registro de la cadena de custodia** con las hojas de cálculo mencionadas en el [Apéndice: Recursos](https://technet.microsoft.com/es-es/library/a9a5c2a9-cce3-4edb-a92c-10983899240a(v=TechNet.10)) de esta guía.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía fundamental de investigación informática para Windows](http://go.microsoft.com/fwlink/?linkid=80345)

**Notificaciones de actualización**

[Regístrese para recibir información acerca de actualizaciones y versiones nuevas](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=fundamental%20computer%20investigation%20guide%20for%20windows)

[](#mainsection)[Principio de la página](#mainsection)
