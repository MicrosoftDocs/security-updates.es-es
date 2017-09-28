---
TOCTitle: Descripción general de la Guía de defensa en profundidad antivirus
Title: Descripción general de la Guía de defensa en profundidad antivirus
ms:assetid: 'ee1fbdef-bf95-4c01-8963-905cac1c7ab9'
ms:contentKeyID: 20200219
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162791(v=TechNet.10)'
---

Guía de defensa en profundidad antivirus
========================================

### Descripción general

Publicado: mayo 20, 2004

##### En esta página

[](#abcd)[Introducción](#abcd)
[](#abce)[Resumen de los capítulos de la guía](#abce)
[](#abcf)[Envíenos sus comentarios](#abcf)
[](#afcb)[Capítulo 1: Introducción](#afcb)
[](#aflg)[Capítulo 2: Amenazas de software malintencionado](#aflg)
[](#flag)[Capítulo 3: Defensa en profundidad antivirus](#flag)
[](#emts)[Capítulo 4: Control y recuperación de los ataques de virus](#emts)
[](#qotg)[Reconocimientos](#qotg)

### Introducción

A pesar de que muchas organizaciones han instalado programas antivirus en sus equipos, el software malintencionado como virus, gusanos y troyanos continúa infectando sistemas informáticos en todo el mundo. No hay nada que explique esta aparente contradicción, pero la situación actual indica que el enfoque estándar consistente en instalar software antivirus en cada equipo del entorno puede no ser suficiente.

La *Guía de defensa en profundidad antivirus* proporciona una descripción general de fácil comprensión de los diferentes tipos de software malintencionado o "malware", además de información sobre los riesgos que suponen estos programas, sus características, formas de réplica y cargas. En esta guía se detallan las consideraciones que deberá tener en cuenta al planear e implementar un sistema de defensa antivirus completo para su organización, y se facilita información sobre el método de defensa en profundidad y otras herramientas relacionadas que le permitirán reducir las posibilidades de infección de los sistemas. En el capítulo final de la guía se ofrece una completa metodología que le ayudará a saber responder y recuperarse de forma rápida y eficaz de los ataques e incidencias provocados por el software malintencionado.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen de los capítulos de la guía

La *Guía de defensa en profundidad antivirus* se compone de cuatro capítulos:

**Capítulo 1: Introducción**
En este capítulo se ofrece una breve introducción a la guía y una descripción general de cada capítulo, y se indican los destinatarios a los que va dirigida.

**Capítulo 2: Amenazas de software malintencionado**
En este capítulo se definen los tipos principales de software malintencionado y se especifica qué programas se incluyen y excluyen de esta categoría. Asimismo, se proporciona información sobre las características del software malintencionado, los vectores de ataque, los medios de propagación y las cargas.

**Capítulo 3: Defensa en profundidad antivirus**
En este capítulo se detallan las consideraciones que deberá tener en cuenta al establecer un sistema de defensa antivirus completo para clientes, servidores y la infraestructura de red. También se abordan directivas de usuario y medidas de seguridad generales que Microsoft recomienda tener en cuenta al elaborar un plan de seguridad global.

**Capítulo 4: Control y recuperación de los ataques de virus**
En este capítulo se ofrece una descripción detallada del proceso de resolución y recuperación de los ataques de software malintencionado cuyas fuentes son las prácticas más recomendadas del sector y las operaciones internas de Microsoft.

[](#mainsection)[Principio de la página](#mainsection)

### Envíenos sus comentarios

Agradecemos cualquier comentario que desee realizar sobre esta guía. En particular, nos interesaría conocer su opinión sobre los siguientes temas:

-   ¿En qué medida le ha resultado útil la información que le hemos facilitado?

-   ¿Han sido los procedimientos detallados lo suficientemente precisos?

-   ¿Le han parecido los capítulos interesantes y de fácil lectura?

-   En general, ¿cómo valoraría la guía?

Envíenos sus comentarios a [](mailto:secwish@microsoft.com)[secwish@microsoft.com.](mailto:secwish@microsoft.com)</a> Esperamos con gran interés sus opiniones.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

A pesar de que muchas organizaciones han instalado programas antivirus en sus equipos, los nuevos virus, gusanos y otras formas de *software malintencionado* continúan infectando con rapidez a una gran cantidad de sistemas informáticos. No hay nada que explique esta aparente contradicción, pero las tendencias principales se hacen patentes en los comentarios que ha recibido Microsoft de los profesionales de TI y el personal de seguridad de organizaciones cuyos sistemas han sido infectados. Algunos de estos comentarios son los siguientes:

-   "El usuario ejecutó el archivo adjunto desde su programa de correo electrónico a pesar de que le indicamos reiteradamente que no debía hacerlo...".

-   "El software antivirus debería haberlo detectado, pero aún no se había instalado la firma de este virus".

-   "Este virus nunca debería haber pasado a través de nuestro servidor de seguridad; ni siquiera nos dimos cuenta de que esos puertos podrían ser atacados".

-   "No sabíamos que nuestros servidores se debían haber revisado".

El éxito de los últimos ataques demuestra que el enfoque estándar consistente en instalar software antivirus en cada equipo de la organización puede no ser suficiente. Los recientes ataques de virus se han propagado a una velocidad alarmante, de tal modo que la industria de software no puede detectar, identificar y facilitar herramientas antivirus capaces de ofrecer protección antes de que se produzcan. Las técnicas utilizadas por las últimas formas de software malintencionado también han resultado ser sustancialmente más avanzadas, lo que ha posibilitado que los últimos ataques de virus hayan escapado a la detección y se hayan propagado sin problemas. Entre estas técnicas se incluyen:

-   **Ingeniería social**. Muchos ataques pretenden hacer creer que provienen de un administrador del sistema o un servicio oficial, lo que aumenta las probabilidades de que los usuarios finales los ejecuten e infecten de este modo sus sistemas.

-   **Creación de una puerta trasera**. La mayoría de los últimos ataques de virus ha intentado abrir alguna forma de acceso no autorizado a los sistemas ya infectados, lo que permite al intruso obtener repetidamente acceso a ellos. Esta capacidad de acceso continuado se utiliza para infectar sistemas con nuevo software malintencionado, que actúan como "zombies" en ataques coordinados de denegación de servicio, o bien, para ejecutar el código que el intruso desee.

-   **Robo de direcciones de correo electrónico**. Los programas de software malintencionado utilizan las direcciones de correo electrónico obtenidas de los sistemas infectados para reenviarse a otras víctimas, al tiempo que los autores de este software pueden hacer una recopilación de las mismas. A continuación, pueden utilizarlas para enviar nuevas variantes de software malintencionado, facilitárselas a otros autores de este tipo de software a cambio de herramientas o código fuente de virus, o venderlas a todos aquellos que estén interesados en utilizarlas para generar correo no deseado.

-   **Motores de correo electrónico incrustados**. El correo electrónico es el principal medio de propagación de software malintencionado. Muchas formas de software malintencionado integran ahora un motor de correo electrónico que posibilita que el código malintencionado se propague mucho más rápidamente y con menos probabilidades de crear una actividad poco corriente que se pueda detectar con facilidad. El correo masivo ilícito aprovecha las puertas traseras de los sistemas infectados para beneficiarse de las oportunidades que brinda el uso de estos motores de correo electrónico. Como resultado, se cree que la mayoría del correo no deseado que se generó el año pasado se envió a través de estos sistemas infectados.

-   **Aprovechamiento de las vulnerabilidades de los productos**. El software malintencionado aprovecha cada vez con más frecuencia las vulnerabilidades de los productos para propagarse, lo que le permite extenderse a una velocidad muy superior.

-   **Aprovechamiento de las nuevas tecnologías de Internet**. A medida que surgen nuevas herramientas de Internet, los autores del software malintencionado las analizan con rapidez para determinar cómo pueden sacar provecho de ellas. Recientemente, la mensajería instantánea y las redes de igual a igual (P2P) se han convertido en vectores de ataque para tal fin.

    Estas técnicas y particularidades del software malintencionado se analizan en detalle en los capítulos siguientes de esta guía.

Microsoft mantiene su firme compromiso de garantizar la seguridad de las aplicaciones que produce y de colaborar con los socios de la empresa para hacer frente a las amenazas del software malintencionado. Entre los últimos esfuerzos realizados por Microsoft para reducir el impacto de estas amenazas se incluyen:

-   Estrecha colaboración con los proveedores de software antivirus para formar la Virus Information Alliance (VIA). Los miembros de la alianza intercambian información técnica sobre el software malintencionado descubierto recientemente. De este modo, pueden comunicar con rapidez a los clientes la información sobre el objetivo del software, su impacto y la recuperación. Para obtener más información sobre VIA, consulte la página "Virus Information Alliance (VIA)" en Microsoft® TechNet: [http://www.microsoft.com/technet/security/topics/virus/via.mspx](http://technet.microsoft.com/es-es/security/bb977553.aspx) (en inglés).

-   Investigación de nuevas tecnologías de seguridad, como la tecnología de protección activa y la protección de sistemas dinámicos, con las que se contribuye a garantizar la seguridad de la plataforma Microsoft Windows®. Para obtener más información sobre los esfuerzos realizados en este campo, consulte las declaraciones de Bill Gates en la RSA Conference 2004 que se incluyen en Microsoft.com:
    <http://www.microsoft.com/billgates/speeches/2004/02-24rsa.asp> (en inglés).

-   Apoyo a la legislación con el objetivo de eliminar el correo no deseado y de trabajar con los responsables del cumplimiento de las leyes y los proveedores de servicios de Internet (ISP) para conseguir que se emprendan acciones judiciales contra las operaciones de correo no deseado. Para obtener información sobre las alianzas que se han creado con este fin, consulte "America Online, Microsoft and Yahoo! Join Forces Against Spam" en Microsoft.com: [http://www.microsoft.com/presspass/press/2003/apr03/04-28JoinForcesAntispamPR.asp](http://www.microsoft.com/presspass/press/2003/apr03/04-28joinforcesantispampr.asp) (en inglés).

-   Presentación del programa de recompensa antivirus (Antivirus Reward Program) y estrecha colaboración con las instituciones responsables del cumplimiento de las leyes para reducir las amenazas que suponen los autores de software malintencionado. Para obtener más información sobre este programa, consulte la página "Microsoft Announces Anti-Virus Reward Program" en Microsoft.com: [http://www.microsoft.com/presspass/press/2003/nov03/11-05AntiVirusRewardsPR.asp](http://www.microsoft.com/presspass/press/2003/nov03/11-05antivirusrewardspr.asp) (en inglés).

Microsoft ha elaborado esta guía de seguridad con el fin de ayudarle a identificar todos los puntos de su infraestructura en los que debería considerar la implementación de sistemas de defensa antivirus. Asimismo, se facilita información sobre cómo recuperarse si el entorno resulta infectado.

##### En esta página

[](#bcde)[Descripción general](#bcde)
[](#bcdf)[Destinatarios de la guía](#bcdf)
[](#bcdg)[Convenciones de estilo utilizadas en esta guía](#bcdg)

### Descripción general

La *Guía de defensa en profundidad antivirus* se compone de los siguientes capítulos:

#### Capítulo 1: Introducción

En este capítulo se ofrece una breve introducción a la guía y se presentan las técnicas y mecanismos utilizados por el software malintencionado; asimismo se incluye una descripción general en cada capítulo y se indican los destinatarios de la guía.

#### Capítulo 2: Amenazas de software malintencionado

En este capítulo se definen distintos tipos de software malintencionado y se especifica qué programas se incluyen y excluyen de esta categoría. Además, se proporciona información sobre las características del software malintencionado, los vectores de ataque y los medios de propagación.

#### Capítulo 3: Defensa en profundidad antivirus

En este capítulo se detallan las consideraciones que recomienda Microsoft al establecer un sistema de defensa antivirus completo para clientes, servidores y la infraestructura de red. También se abordan directivas de usuario y otras medidas de seguridad generales que Microsoft recomienda tener en cuenta al elaborar un plan de seguridad global.

#### Capítulo 4: Control y recuperación de los ataques de virus

En este capítulo se ofrece una descripción detallada del proceso de resolución de los ataques de software malintencionado cuyas fuentes son las prácticas más recomendadas del sector y las operaciones internas de Microsoft.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Con esta guía se pretende principalmente ayudar al personal de TI y de seguridad a comprender mejor las amenazas que supone el software malintencionado, defenderse de ellas y responder con rapidez y eficacia cuando tenga lugar un ataque de software malintencionado.

Aunque se detallan las consideraciones relativas a la defensa mediante software antivirus en entornos de muchos clientes y servidores, el contenido de la guía también es aplicable a las organizaciones que utilizan un único servidor para realizar toda su actividad. Con cada una de estas consideraciones de defensa se pretende proteger al entorno frente a cualquier tipo de amenaza que suponga un ataque de software malintencionado, lo que hace que cobren un gran valor en cualquier organización, independientemente de su tamaño. Puede parecer que algunas de las medidas recomendadas, como la administración y la supervisión de sistemas, van más allá del alcance o las necesidades de algunas organizaciones. Sin embargo, el equipo que elaboró esta guía cree firmemente que por su propio interés debería revisarlas con detenimiento para comprender mejor la naturaleza de los riesgos que supone el software malintencionado hoy en día para los sistemas informáticos de todo el mundo.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo utilizadas en esta guía

En la tabla siguiente se indican las convenciones de estilo que se utilizan en la *Guía* *de defensa en profundidad antivirus*.

**Tabla 1.1: Convenciones de estilo**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Negrita</strong></p></td>
<td style="border:1px solid black;"><p>Los nombres de archivo y los elementos de la interfaz de usuario aparecen en negrita.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><em>Cursiva</em><br />
o<br />
<em>&lt;Cursiva&gt;</em></p></td>
<td style="border:1px solid black;"><p>La cursiva se aplica a caracteres que escribe el usuario y que pueden cambiar. Los caracteres en cursiva que aparecen entre corchetes angulares representan marcadores de posición variables en los que el usuario debe facilitar valores específicos. Ejemplo:</p>
<p><em>  &lt;Nombredearchivo.ext&gt;</em> indica que debería sustituir el texto<em> </em><br />
<em>Nombredearchivo.ext</em> en cursiva por otro nombre de archivo que sea adecuado para la<br />
configuración.<br />
</p>
<p>La cursiva también se utiliza para representar nuevos términos. Ejemplo:</p>
<p><em>  Identidad digital:</em> atributos descriptivos e identificador único de<br />
  una persona, grupo, dispositivo o servicio.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Fuente de texto de la pantalla</p></td>
<td style="border:1px solid black;"><p>Esta fuente define el texto de salida que se muestra en la pantalla.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><pre><code>Fuente de código Monospace</code></pre>
<br />
</td>
<td style="border:1px solid black;"><p>Esta fuente se utiliza para definir ejemplos de código. Ejemplo:<br />
  public override void Install(IDictionary savedState)</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><pre><code>Fuente de comandos Monospace</code></pre>
<br />
</td>
<td style="border:1px solid black;"><p>Esta fuente se utiliza para definir comandos, modificadores y atributos que el usuario escribe en un símbolo del sistema. Ejemplo:<br />
  En el símbolo del sistema, escriba lo siguiente:<br />
  CScript SetUrlAuth.vbs</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>%SystemRoot%</p></td>
<td style="border:1px solid black;"><p>La carpeta en la que se ha instalado el sistema operativo Windows.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Nota</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>Importante</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional que resulta esencial para completar una tarea.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Precaución</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que si no se realiza o pasa por alto una determinada acción, se podrá producir una pérdida de datos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>Advertencia</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que si no se realiza o pasa por alto una determinada acción, el usuario o el hardware podría resultar dañado físicamente.</p></td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 2: Amenazas de software malintencionado
  
[](#cdef)[Introducción](#cdef)  
[](#cdeg)[Evolución de los virus informáticos](#cdeg)  
[](#cdeh)[Definición del software malintencionado](#cdeh)  
[](#cdei)[Características del software malintencionado](#cdei)  
[](#cdej)[¿Qué no se considera software malintencionado?](#cdej)  
[](#cdek)[Software antivirus](#cdek)  
[](#cdel)[Ciclo de vida típico del software malintencionado en circulación](#cdel)  
[](#cdem)[Resumen](#cdem)
  
### Introducción
  
En este capítulo de la *Guía* *de defensa en profundidad antivirus* se describe de forma concisa la evolución de los virus informáticos, desde los primeros virus relativamente simples hasta la gran diversidad de software malintencionado o *malware* que existe hoy en día. Asimismo, se definen distintos tipos y técnicas comunes de software malintencionado, se proporciona información sobre su propagación y se analizan los riesgos que suponen para cualquier tipo de organización.
  
Dada la continua evolución de los virus informáticos, sería imposible incluir y explicar en esta guía todos los tipos de software malintencionado junto con sus posibles variaciones. No obstante, este documento constituye un primer paso muy importante hacia el entendimiento de la naturaleza de los distintos elementos que componen este tipo de software. En esta guía también se presentan y definen otros ejemplos que no pertenecen a la categoría de software malintencionado, como *spyware* (programas espía que realizan ciertas actividades en un equipo determinado sin el consentimiento del usuario), *spam* (correo electrónico no deseado o solicitado) y *adware* (publicidad no deseada integrada en software).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Evolución de los virus informáticos
  
Los primeros virus informáticos aparecieron a principios de los 80. Se trataba, en su mayoría, de archivos relativamente simples de replicación automática que mostraban burlas o bromas cuando se los ejecutaba.
  
**Nota**: es necesario señalar que resulta prácticamente imposible ofrecer un historial definitivo de la evolución de los virus informáticos. La propia naturaleza ilegal del software malintencionado hace que los responsables de los ataques intenten ocultar su origen. En esta guía se describe la historia del software malintencionado comúnmente aceptada y avalada por los investigadores de virus informáticos y los proveedores de productos antivirus.
  
En 1986 aparecieron los primeros casos de ataques de virus informáticos a equipos Microsoft® MS-DOS®, de los cuales se identificó al virus Brain como el primero de todos. Sin embargo, en 1986 aparecieron otros virus: Virdem (el primer virus de archivos) y PC-Write (el primer *troyano*; un programa aparentemente útil o inofensivo que en realidad contiene código oculto diseñado para dañar o beneficiarse del sistema en el que se ejecuta). En el caso de PC-Write, se trataba de un troyano oculto que utilizaba el mismo nombre que una conocida aplicación de procesamiento de textos que se distribuía como "shareware".
  
A medida que más usuarios se iniciaban en la tecnología de creación de virus informáticos, comenzó a aumentar considerablemente su número, la complejidad y diversidad de los virus informáticos y las plataformas susceptibles de ser atacadas. Durante un tiempo, los ataques se centraron en los sectores de inicio. Más tarde pasaron a infectar los archivos ejecutables. En 1988 apareció el primer *gusano* de Internet (un tipo de software malintencionado que utiliza código malintencionado de propagación automática capaz de distribuirse de un equipo a otro a través de las conexiones de red). El gusano Morris, por ejemplo, consiguió ralentizar considerablemente las comunicaciones de Internet. En respuesta a esta situación y al creciente número de ataques de virus registrados, se fundó el Centro de coordinación de CERT: <http://www.cert.org/> (en inglés). Su objetivo era garantizar la estabilidad de Internet prestando asistencia para coordinar las respuestas a ataques de virus y otro tipo de incidencias.
  
En 1990 apareció en Internet la primera BBS de intercambio de virus, que utilizaban los creadores de virus para colaborar y compartir sus conocimientos. También en esta época se publicó el primer libro sobre creación de virus y se desarrolló el primer virus *polimórfico* (conocido comúnmente como Camaleón o Casper). Un virus polimórfico es un tipo de software malintencionado que utiliza un número ilimitado de rutinas de cifrado para evitar ser detectado. Este tipo de virus tiene la capacidad de modificarse cada vez que se replica, lo que dificulta su detección mediante programas antivirus basados en *firmas*, diseñados para "reconocer" virus. Poco después hizo su aparición Tequila, el primer gran virus polimórfico. En 1992 apareció el primer motor de virus polimórficos y los primeros kits de herramientas para la creación de virus.
  
Desde entonces, el nivel de sofisticación de los virus ha aumentado considerablemente: aparecieron virus informáticos capaces de obtener acceso a las libretas de direcciones de correo electrónico y enviarse a sí mismos a los contactos; virus de macro que se adjuntaban por sí solos y atacaban distintos archivos de aplicaciones tipo Office; y virus creados específicamente para aprovechar las vulnerabilidades de los sistemas operativos y aplicaciones. Los virus informáticos aprovechan las vulnerabilidades del correo electrónico, de las redes de uso compartido de archivos de igual a igual (P2P), de los sitios Web, de las unidades compartidas y de los productos para replicarse y atacar. Asimismo, crean *puertas traseras* (puntos de entrada de red secretos u ocultos a través de los cuales penetra el software malintencionado) en los sistemas infectados para permitir a los creadores de virus, o *intrusos*, regresar y ejecutar el software que deseen. En el contexto de esta guía, un intruso es un programador o usuario de un equipo que intenta obtener acceso a un sistema o una red informática de forma ilegal. En la sección siguiente de este capítulo se trata el software malintencionado en profundidad.
  
Determinados virus informáticos incorporan su propio motor de correo electrónico incrustado, a través del cual pueden propagarse directamente por correo electrónico desde un sistema infectado, obviando la configuración del cliente o servidor de correo electrónico del usuario. Los creadores de virus también han comenzado a estructurar cuidadosamente sus ataques y a utilizar la ingeniería social para desarrollar mensajes de correo electrónico con aspecto y diseño auténticos. Con ello se pretende engañar a los usuarios para que abran el archivo con el virus adjunto, aumentando, de este modo, la posibilidad de que tenga lugar una infección a gran escala.
  
Al tiempo que el software malintencionado ha evolucionado, se ha desarrollado también software antivirus para contrarrestarlo. No obstante, la mayoría del software antivirus actual se basa casi por completo en las *firmas* de virus (características de identificación de software malintencionado) para detectar el código potencialmente dañino. Esto beneficia a los creadores de virus en tanto que aprovechan el período que va desde el lanzamiento del virus hasta que los proveedores de software antivirus distribuyen a gran escala los archivos de firma. Por ello la norma general es que la tasa de infección del virus sea tremendamente elevada durante los primeros días, y que se produzca un declive pronunciado una vez que se distribuyen los archivos de firma.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Definición del software malintencionado
  
En esta guía se utiliza el término software malintencionado o *malware* (procedente del término inglés "malicious software") como denominación colectiva para hacer referencia a los virus, gusanos y troyanos que realizan tareas malintencionadas en un sistema informático con total premeditación.
  
Por tanto, ¿qué es exactamente un virus o un gusano informático? ¿En qué se diferencian de los troyanos? ¿Actúan las aplicaciones antivirus sólo frente a gusanos y troyanos, o sólo ante virus?
  
Estas preguntas surgen dada la gran confusión, y a menudo la distorsión, que acompaña al concepto de código malintencionado. La gran cantidad y variedad de código malintencionado existente hace difícil proporcionar una definición exacta de cada una de sus categorías.
  
A continuación se muestran varias definiciones simples de carácter general de categorías de software malintencionado:
  
-   **Troyano**. Programa aparentemente útil o inofensivo que en realidad contiene código oculto diseñado para dañar o beneficiarse del sistema en el que se ejecuta. Los troyanos se envían normalmente a través de mensajes de correo electrónico que falsean el objetivo y la función del programa. También se denominan códigos troyanos. El troyano deja una *carga* o realiza una tarea malintencionada cuando se ejecuta.
  
-   **Gusano**. Los gusanos utilizan código malintencionado de propagación automática capaz de distribuirse de un equipo a otro a través de las conexiones de red. Los gusanos pueden realizar acciones dañinas, como consumir los recursos de la red o del sistema local, dando lugar probablemente a un ataque de denegación de servicio. Determinados tipos de gusanos se pueden ejecutar y propagar sin la intervención del usuario, mientras que otros requieren que éste ejecute directamente el código para su propagación. Además de replicarse, los gusanos también pueden dejar una carga.
  
-   **Virus**. Los virus ejecutan código escrito con la intención expresa de replicarse. Se intentan propagar de un equipo a otro adjuntándose a un programa host. Pueden dañar elementos de hardware, software o datos. Cuando el host se ejecuta, también lo hace el código del virus, infectando nuevos hosts y, en ocasiones, dejando una carga adicional.
  
A efectos de esta guía, *carga* es un término colectivo que hace referencia a las acciones que realiza el software malintencionado en un equipo infectado. Estas definiciones de las distintas categorías de software malintencionado permiten presentar las diferencias entre ellas en un simple gráfico de flujo. En la ilustración siguiente se muestran los elementos que permiten determinar si un programa o una secuencia de comandos se incluye dentro de alguna de las categorías:
  
![](images/Cc162791.AVFG0201(es-es,TechNet.10).gif)
  
**Figura 2.1 Árbol de decisión para determinar si se trata de código malintencionado**
  
La ilustración nos permite distinguir las categorías de código malintencionado más comunes según se presentan en esta guía. No obstante, es importante señalar que un mismo ataque puede introducir código que se ajuste a varias de estas categorías. Estos tipos de ataque (conocidos como *amenazas mixtas* porque constan de más de un tipo de software malintencionado y utilizan varios vectores de ataque) se pueden propagar muy rápidamente. Un *vector de* *ataque* es la ruta que el software malintencionado puede utilizar para realizar un ataque. Por ello, la defensa frente a las amenazas mixtas puede resultar especialmente difícil.
  
En las secciones siguientes se ofrece una explicación más detallada de cada categoría de software malintencionado y de algunos de los elementos clave que lo componen.
  
#### Troyanos
  
Los troyanos no se consideran virus informáticos ni gusanos porque no se pueden propagar por sí mismos. No obstante, se puede utilizar un virus o un gusano para copiar un troyano en el sistema que se desea atacar como parte de una carga de ataque. Este proceso se denomina *colocación*. Normalmente, los troyanos tienen como objetivo interrumpir el trabajo del usuario o el funcionamiento normal del sistema. Por ejemplo, los troyanos pueden crear una puerta trasera en el sistema para que los atacantes puedan robar datos o cambiar la configuración.
  
Hay otros dos términos que se suelen utilizar al hablar de troyanos o actividades troyanas; se identifican y explican a continuación:
  
-   **Troyanos de acceso remoto**. Algunos programas troyanos permiten al atacante o ladrón de datos hacerse con el control de un sistema de forma remota. Estos programas se denominan *troyanos de acceso remoto* (RAT) o puertas traseras. Varios ejemplos de RAT son: Back Orifice, Cafeene y SubSeven.
  
    Para obtener una explicación detallada de este tipo de troyano, consulte el artículo "Danger: Remote Access Trojans" en Microsoft TechNet:  
    [http://www.microsoft.com/technet/security/topics/virus/virusrat.mspx](http://technet.microsoft.com/es-es/security/bb977553.aspx) (en inglés).
  
-   **Rootkits**. Se trata de colecciones de programas de software que los atacantes utilizan para obtener acceso remoto no autorizado a un equipo y ejecutar ataques adicionales. Pueden utilizar varias técnicas diferentes, entre las que se incluyen el seguimiento de las pulsaciones de teclas, el cambio de los archivos de registro o de las aplicaciones existentes en el sistema, la creación de puertas traseras y el ataque a otros equipos de la red. Por lo general, los rootkits se organizan como un conjunto de herramientas que se adaptan específicamente para atacar a un sistema operativo determinado. Los primeros aparecieron a principios de los 90, siendo sus principales objetivos los sistemas operativos Sun y Linux. Actualmente son muchos los sistemas operativos objetivo, entre ellos la plataforma Microsoft® Windows®.
  
    **Nota**: no hay que olvidar que tanto los RAT como determinadas herramientas que forman los rootkits pueden tener usos legítimos de control remoto y seguimiento. No obstante, se trata de herramientas que pueden suponer problemas para la seguridad y privacidad, lo que aumenta los riesgos globales de los entornos en los que se utilizan.
  
#### Gusanos
  
Si el código malintencionado se replica, no se trata de un troyano. Por tanto, la cuestión que debe plantearse para definir más claramente el software malintencionado es la siguiente: "¿Puede el código replicarse sin necesidad de un portador?". Es decir, ¿puede replicarse sin necesidad de infectar un archivo ejecutable? Si la respuesta a esta pregunta es "Sí", el código se considera un tipo de gusano.
  
La mayoría de los gusanos intentan copiarse a sí mismos en un equipo host para, a continuación, utilizar sus canales de comunicación y replicarse. El gusano Sasser, por ejemplo, se aprovecha inicialmente de la vulnerabilidad de un servicio para infectar un sistema y, a continuación, utiliza la conexión de red del mismo para intentar replicarse. Si ha instalado las últimas actualizaciones de seguridad (para detener la infección) o ha habilitado los servidores de seguridad de su entorno para bloquear los puertos de red utilizados por el gusano (para detener la replicación), el ataque no tendrá éxito.
  
#### Virus
  
Si el código malintencionado agrega una copia de sí mismo a un archivo, documento o sector de inicio de una unidad de disco con el fin de replicarse, estaremos frente a un virus. Puede ser una copia directa del virus original o una versión modificada del mismo. Para obtener información más detallada al respecto, consulte la sección "Mecanismos de defensa" que aparece más adelante en este capítulo. Como se mencionó anteriormente, los virus contienen a menudo cargas que pueden colocar en un equipo local, por ejemplo, un troyano, que realizará una o varias acciones malintencionadas, como la eliminación de datos del usuario. No obstante, aunque el virus sólo se replique y no contenga carga, seguimos estando frente a un problema de software malintencionado, ya que el virus es capaz de dañar datos, utilizar recursos del sistema y consumir ancho de banda de red a medida que se replica.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Características del software malintencionado
  
Las características de las distintas categorías de software malintencionado son a menudo muy similares. Por ejemplo, los virus y los gusanos pueden utilizar la red como mecanismo de transporte. No obstante, mientras que el virus buscará archivos que infectar, el gusano sólo intentará copiarse a sí mismo. En la sección siguiente se explican las características típicas del software malintencionado.
  
#### Entornos objetivo
  
Para que el ataque del software malintencionado a un sistema host tenga éxito, es necesario que disponga de una serie de componentes específicos. A continuación se muestran varios ejemplos típicos de componentes que requiere el software malintencionado para lanzar un ataque a un sistema host:
  
-   **Dispositivos**. Ciertos tipos de software malintencionado se dirigen específicamente a un tipo de dispositivo determinado, como un PC, un equipo Apple Macintosh o incluso un dispositivo PDA, aunque este último caso es muy poco común en la actualidad.
  
-   **Sistemas operativos**. En determinadas ocasiones, el software malintencionado requiere un sistema operativo determinado para ser efectivo. Por ejemplo, los virus CIH o Chernobyl de finales de los 90 sólo podían atacar equipos Microsoft Windows® 95 o Windows® 98.
  
-   **Aplicaciones**. También puede que el software malintencionado requiera que en el equipo al que va a atacar esté instalada una aplicación determinada para poder dejar una carga o replicarse. Por ejemplo, el virus LFM.926 de 2002 sólo podía atacar si los archivos Shockwave Flash (.swf) se ejecutaban en el equipo local.
  
#### Portadores
  
Cuando el software malintencionado es un virus, intenta atacar a un portador (también conocido como host) e infectarlo. El número y tipo de portadores susceptibles de ser atacados varía considerablemente, no obstante, en la lista siguiente se muestran algunos ejemplos de los portadores que suelen ser objeto de ataques con mayor frecuencia:
  
-   **Archivos ejecutables**. Se trata del objetivo del virus "clásico", que se replica adjuntándose a un programa host. Además de los archivos ejecutables típicos que utilizan la extensión .exe, también pueden ser objeto de ataques archivos con las siguientes extensiones: .com, .sys, .dll, .ovl, .ocx y .prg.
  
-   **Secuencias de comandos**. Los ataques que utilizan secuencias de comandos como portadores se dirigen a archivos que utilizan un lenguaje de secuencias de comandos como Microsoft Visual Basic® Script, JavaScript, AppleScript o Perl Script. Entre las extensiones de este tipo de archivos se encuentran: .vbs, .js, .wsh y .prl.
  
-   **Macros**. Estos portadores son archivos que admiten el lenguaje de secuencias de comandos con macros de una aplicación determinada, como una aplicación de procesamiento de textos, de hoja de cálculo o de base de datos. Por ejemplo, los virus pueden utilizar los lenguajes de macro de Microsoft Word y Lotus Ami Pro para producir una serie de efectos, desde pequeñas malas pasadas (cambio de palabras en el documento o de colores) hasta acciones malintencionadas (formateo del disco duro del equipo).
  
-   **Sector de inicio**. Otras áreas específicas del disco del equipo (discos duros y medios extraíbles de inicio), como el registro de inicio maestro (MBR) o el registro de inicio de DOS, también se pueden considerar portadores, dada su capacidad de ejecutar código malintencionado. Una vez que el disco se ha infectado, la replicación tiene lugar cuando éste se utiliza para iniciar otros sistemas.
  
    **Nota**: si el virus intenta infectar tanto a archivos como a sectores de inicio, hablamos de un virus *multipartite*.
  
#### Mecanismos de transporte
  
La replicación de los ataques de virus en distintos sistemas informáticos se puede llevar a cabo a través de uno o varios métodos diferentes. En esta sección se proporciona información sobre algunos de los mecanismos de transporte más comunes utilizados por el software malintencionado.
  
-   **Medios extraíbles**. La transferencia de archivos es el primer y probablemente más utilizado método de transmisión de virus informáticos y otro tipo de software malintencionado (al menos, hasta el momento). Se inició con los disquetes, luego pasó a las redes y, en la actualidad, utiliza nuevos medios, como los dispositivos de bus serie universal (USB) y los servidores de seguridad. Aunque la tasa de infección no es tan alta como la del software malintencionado transmitido a través de redes, la amenaza siempre está presente. Resulta difícil de erradicar completamente dada la necesidad de intercambiar datos entre sistemas.
  
-   **Recursos compartidos de red**. Cuando los equipos dispusieron de un método que les permitía conectarse entre sí directamente a través de una red, se abrió ante los creadores de software malintencionado un nuevo mecanismo de transporte que superaba a los medios extraíbles en cuanto a capacidad de propagar código malintencionado. Cuando el sistema de seguridad de los recursos compartidos de red está mal implementado, se obtiene como consecuencia un entorno apto para la replicación de software malintencionado a un gran número de equipos conectados. El uso de los recursos compartidos ha reemplazado en gran medida al de los medios extraíbles.
  
-   **Exploración de la red**. Los creadores de software malintencionado utilizan este mecanismo para explorar redes en busca de equipos vulnerables o para atacar de forma aleatoria direcciones IP. Con este mecanismo, por ejemplo, se puede enviar un paquete utilizando un puerto de red específico a un intervalo determinado de direcciones IP en busca de un equipo vulnerable al que poder atacar.
  
-   **Redes de igual a igual (P2P)**. Para que tenga lugar una transferencia de archivos P2P, es necesario que el usuario instale previamente un componente cliente de la aplicación P2P que utilice uno de los puertos autorizados en el servidor de seguridad de la organización, por ejemplo, el puerto 80. Las aplicaciones utilizan este puerto para atravesar el servidor de seguridad y transferir archivos directamente de un equipo a otro. Estas aplicaciones se pueden obtener fácilmente en Internet y proporcionan un mecanismo de transporte que los creadores de software malintencionado utilizan directamente para propagar un archivo infectado en el disco duro de un cliente.
  
-   **Correo electrónico**. El correo electrónico se ha convertido en el mecanismo de transporte utilizado por muchos creadores de software malintencionado. La facilidad con la que se puede llegar a cientos de miles de personas a través del correo electrónico sin necesidad de que los responsables del ataque abandonen sus equipos ha hecho de este mecanismo un método de transporte muy efectivo. Resulta relativamente sencillo engañar a los usuarios para que abran archivos adjuntos al correo electrónico (utilizando técnicas de ingeniería social). No es de extrañar, por tanto, que muchos de los ataques de software malintencionado más prolíficos hayan utilizado el correo electrónico como transporte. Existen dos tipos básicos de software malintencionado que lo utilizan de forma específica:
  
    -   **Servicio de envío de correo**. Este tipo de software malintencionado se envía a sí mismo por correo a un número limitado de direcciones, bien utilizando el software de correo instalado en el host (por ejemplo, Microsoft Outlook® Express), bien empleando su propio motor integrado de protocolo simple de transferencia de correo (SMTP).
  
    -   **Servicio de envío de correo masivo**. Este tipo de software malintencionado busca en el equipo infectado direcciones de correo electrónico y, a continuación, se envía a sí mismo de forma masiva a dichas direcciones, utilizando el software de correo instalado en el host o su propio motor integrado SMTP.
  
-   **Aprovechamiento remoto**. El software malintencionado puede intentar aprovechar una vulnerabilidad determinada de un servicio o aplicación para replicarse. Este comportamiento se observa a menudo en los gusanos; por ejemplo, el gusano Slammer aprovechó una de las vulnerabilidades de Microsoft SQL Server™ 2000 para generar una saturación de búfer que permitió que se sobrescribiera una parte de la memoria del sistema con código que se podía ejecutar en el mismo contexto de seguridad que el servicio SQL Server. Las saturaciones de búfer se producen al agregar una cantidad de información superior a la que el búfer es capaz de contener. Se trata de una vulnerabilidad muy aprovechada por los atacantes para hacerse con un sistema. Aunque Microsoft ya había identificado y solucionado esta vulnerabilidad meses antes de que apareciera Slammer, pocos sistemas se habían actualizado, por lo que el gusano se pudo propagar.
  
#### Cargas
  
Una vez el software malintencionado ha alcanzado el equipo host a través del transporte, generalmente realizará una acción denominada *carga*, que puede adoptar diferentes formas. En esta sección se identifican algunos de los tipos de carga más habituales:
  
-   **Puerta trasera**. Este tipo de carga permite el acceso no autorizado a un equipo. Aunque puede proporcionar acceso completo, también se puede limitar, por ejemplo, a habilitar el acceso mediante el protocolo de transferencia de archivos (FTP) a través del puerto 21 del equipo. Si el ataque se produjo para habilitar Telnet, un intruso podría utilizar el equipo infectado como área de almacenamiento temporal para los ataques a través de Telnet en otros equipos. Como se ha mencionado anteriormente, una puerta trasera en ocasiones se conoce como troyano de acceso remoto.
  
-   **Daños o eliminación de datos**. Uno de los tipos de carga más destructivos puede ser un código malintencionado que daña o elimina los datos, y deja inservible la información del equipo del usuario. El creador del software malintencionado tiene dos opciones: la primera consiste en crear la carga de modo que se ejecute con rapidez. Aunque es potencialmente desastroso para el equipo que infecta, el diseño del software malintencionado permite descubrirlo antes y esto favorece que se reduzcan las posibilidades de que se replique sin ser detectado. La otra opción consiste en dejar la carga en el sistema local (a modo de troyano) durante un período de tiempo (consulte la sección "Mecanismos de activación" más adelante en este capítulo para ver ejemplos) para que el software malintencionado se extienda antes de que se intente entregar la carga y, por lo tanto, se alerte al usuario de su presencia.
  
-   **Robo de información**. Un tipo de carga de software malintencionado especialmente preocupante es el que se ha diseñado para robar información. Si una carga compromete la seguridad de un equipo host, podrá proporcionar un mecanismo para pasar información a los atacantes. Esto puede ocurrir de diferentes formas; por ejemplo, la carga de software malintencionado puede automatizar una transferencia con el objetivo de capturar archivos locales o información tal como las teclas que el usuario presiona (con el fin de intentar obtener el nombre y la contraseña del usuario). Otro mecanismo consiste en proporcionar un entorno en el host local que permita al atacante controlarlo de forma remota u obtener acceso a los archivos del sistema directamente.
  
-   **Denegación de servicio (DoS)**. Uno de los tipos de carga de aplicación más sencilla es el ataque de denegación de servicio, que consiste en un asalto computerizado que inicia un atacante para sobrecargar o detener un servicio de red, por ejemplo un servidor Web o de archivos. El objetivo de los ataques DoS es simplemente dejar inutilizable un servicio determinado durante un período de tiempo.
  
    -   **Denegación de servicio distribuida (DDoS)**. Estos tipos de ataques utilizan habitualmente clientes infectados que desconocen por completo que participan en el ataque. Un ataque DDoS es un tipo de denegación de servicio en el que un usuario utiliza código malintencionado instalado en varios equipos para alcanzar un único objetivo. Con este método se puede conseguir un efecto mayor en el objetivo de lo que se podría obtener si se usara un único equipo. La semántica del ataque varía de unos a otros, si bien generalmente implica el envío de grandes cantidades de datos a un host o un sitio Web específico, que hacen que éste deje de responder (o se vuelva incapaz de responder) al tráfico legítimo. De este modo, inunda el ancho de banda disponible en el sitio de la víctima y hace que se quede sin conexión.
  
        Puede resultar extremadamente difícil defenderse de este tipo de ataque, puesto que los hosts responsables son de hecho víctimas involuntarias. Los ataques DDoS generalmente se llevan a cabo mediante *bots* (programas que realizan tareas repetitivas), como *Eggdrop* de Internet Relay Chat (IRC), que un intruso puede utilizar para controlar los equipos "víctimas" a través de un canal IRC. Una vez que esos equipos quedan bajo el control del intruso, se convierten en *zombies* que pueden atacar a un objetivo bajo las órdenes del intruso y sin el conocimiento de sus propietarios.
  
    Los ataques DoS y DDoS pueden implicar distintas técnicas, entre las que se incluyen:
  
    -   **Cierres del sistema**. Si el software malintencionado consigue apagar o bloquear el sistema host, puede ocasionar problemas en uno o varios servicios. Para poder atacar el sistema host y hacer que se apague, el software malintencionado debe encontrar un punto débil en una aplicación o en el sistema operativo.
  
    -   **Inundación del ancho de banda**. La mayor parte de los servicios que se proporcionan en Internet están vinculados a través de una conexión de red de banda ancha limitada que los conecta a sus clientes. Si un creador de software malintencionado puede entregar una carga que ocupe este ancho de banda con tráfico de red falso, puede producir una denegación de servicio simplemente impidiendo que los clientes puedan conectarse directamente al mismo.
  
    -   **Denegación de servicio de red**. Este tipo de carga intenta sobrecargar los recursos disponibles para el host local. Recursos como el microprocesador y la capacidad de la memoria quedan saturados por los ataques del tipo *inundación de paquetes SYN*, en los que un atacante utiliza un programa para enviar múltiples solicitudes de SYN de TCP con el fin de llenar la cola de conexión pendiente en el servidor e impedir el tráfico de red legítimo a y desde el host. Los ataques del tipo *bomba de correo* también saturan los recursos de almacenamiento para crear un ataque DoS, en el que se envía a una dirección una cantidad excesiva de datos de correo electrónico en un intento de ocasionar problemas en el programa de correo electrónico o de impedir que el destinatario reciba otros mensajes legítimos.
  
    -   **Problemas en los servicios**. Este tipo de carga también puede ocasionar una denegación de servicio. Por ejemplo, esta técnica de ataque DoS tiene éxito cuando el ataque en un servidor de Sistema de nombres de dominio (DNS) deshabilita el servicio DNS. Sin embargo, puede que todos los demás servicios del sistema no resulten afectados.
  
#### Mecanismos de activación
  
Los mecanismos de activación son una característica que el software malintencionado utiliza para iniciar la replicación o la entrega de la carga. Entre los mecanismos de activación típicos se encuentran los siguientes:
  
-   **Ejecución manual**. Consiste simplemente en la ejecución del software malintencionado por parte de la propia víctima.
  
    -   **Ingeniería social**. El software malintencionado utilizará con frecuencia alguna forma de ingeniería social para tratar de engañar a una víctima y conseguir que ejecute manualmente el código malintencionado. El enfoque puede resultar relativamente sencillo, como el de los gusanos de correo masivo, en los que el elemento de ingeniería social se centra en seleccionar el texto del campo Asunto del mensaje de correo electrónico que tenga más posibilidades de ser abierto por una víctima potencial. Los creadores de software malintencionado pueden utilizar asimismo la *suplantación* de correo electrónico para intentar hacer creer a la víctima que un mensaje proviene de un remitente de confianza. La suplantación es el acto de imitar un sitio Web o una transmisión de datos para hacer que parezcan auténticos. Por ejemplo, el gusano Dumaru original que apareció por primera vez en 2003 modificaba el campo **De:** de los mensajes de correo electrónico para hacer creer que se enviaban desde security@microsoft.com. (Consulte la sección "Mensajes de virus falsos" en el siguiente apartado de este capítulo para obtener más información sobre esta característica.)
  
-   **Ejecución semiautomática**. Este tipo de mecanismo de activación lo inicia primero la propia víctima y a partir de ahí se ejecuta automáticamente.
  
-   **Ejecución automática**. Este mecanismo de activación no requiere de ninguna ejecución manual. El software malintencionado lleva a cabo su ataque sin necesidad de que la víctima ejecute un código malintencionado en el equipo de destino.
  
-   **Bomba de tiempo**. Este tipo de mecanismo realiza una acción tras un determinado período de tiempo. Este período puede ser un retraso desde la primera ejecución de la infección o una fecha o intervalo de fechas previamente establecidos. Por ejemplo, el gusano MyDoom.B únicamente inició sus rutinas de carga contra el sitio Web de Microsoft.com el día 3 de febrero de 2004, e hizo lo propio contra el sitio Web del grupo SCO el 1 de febrero de 2004. Después, detuvo toda replicación el 1 de marzo de ese mismo año, aunque el componente de puerta trasera de la bomba de tiempo continuaba activo después de esta fecha.
  
-   **Activación condicional**. Este mecanismo utiliza alguna condición predeterminada para entregar la carga. Por ejemplo, un archivo con un nombre nuevo, una serie de pulsaciones de teclas o el inicio de una aplicación. El software malintencionado que emplea esta activación se denomina en ocasiones *bomba lógica*.
  
#### Mecanismos de defensa
  
Numerosos ejemplos de software malintencionado utilizan algún tipo de mecanismo de defensa para reducir la probabilidad de ser detectados y eliminados. En la siguiente lista se ofrecen algunos ejemplos de las técnicas empleadas:
  
-   **Armadura**. Este tipo de mecanismo de defensa emplea técnicas que intentan impedir el análisis del código malintencionado, por ejemplo, detectar cuándo se ejecuta un depurador e intentar evitar que funcione correctamente, o agregar grandes cantidades de código sin sentido para ocultar el objetivo del código malintencionado.
  
-   **Ocultación**. El software malintencionado utiliza esta técnica para ocultarse mediante la interceptación de solicitudes de información y la devolución de datos falsos. Por ejemplo, un virus puede almacenar una imagen del sector de inicio no infectado y mostrarla cuando se intente visualizar el sector de inicio afectado. El virus informático más antiguo conocido, denominado “Brain”, utilizó esta técnica en 1986.
  
-   **Cifrado**. El software malintencionado que utiliza este mecanismo de defensa realiza un cifrado de sí mismo o de la carga (y en ocasiones incluso de otros datos del sistema) para evitar la detección o la recuperación de datos. El software malintencionado cifrado contiene una rutina de descifrado estática, una clave de cifrado y el código malintencionado cifrado (que incluye una rutina de cifrado). Cuando se ejecuta, utiliza la rutina de descifrado y la clave para descifrar el código malintencionado. A continuación, crea una copia del código y genera una nueva clave de cifrado. Emplea esa clave y la rutina de cifrado para cifrar la copia nueva de sí mismo, agregando la clave nueva con la rutina de descifrado al inicio de la copia nueva. A diferencia de los virus polimórficos, el software malintencionado de cifrado utiliza siempre las mismas rutinas de descifrado, así que aunque el valor de la clave (y, por tanto, la firma de los códigos malintencionados cifrados) generalmente cambia de una infección a otra, los programas antivirus pueden buscar la rutina de descifrado estática para detectar el software malintencionado que utiliza este mecanismo de defensa.
  
-   **Software malintencionado oligomórfico**. Se trata de software que utiliza el cifrado como mecanismo para defenderse y puede cambiar la rutina de cifrado únicamente un número determinado de veces (generalmente una cantidad reducida). Por ejemplo, un virus que puede generar dos rutinas de descifrado diferentes se clasificaría como *oligomórfico*.
  
-   **Software malintencionado polimórfico**. Utiliza el cifrado como mecanismo de defensa para cambiarse con el fin de evitar ser detectado, generalmente mediante el cifrado del propio software malintencionado con una rutina de cifrado para, a continuación, proporcionar una clave de descifrado diferente para cada mutación. De este modo, el software malintencionado *polimórfico* utiliza un número ilimitado de rutinas de cifrado para evitar la detección. Cuando el software se replica, una parte del código de descifrado se modifica. En función del tipo específico de código, la carga u otras acciones llevadas a cabo pueden utilizar o no el cifrado. Generalmente existe un *motor de mutación*, que es un componente incorporado del código malintencionado de cifrado que genera rutinas de cifrado aleatorias. Este motor y el software malintencionado quedan cifrados y la nueva clave de descifrado se pasa con ellos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### ¿Qué no se considera software malintencionado?
  
Existe una serie de amenazas que no se consideran software malintencionado puesto que no son programas informáticos escritos con intención de hacer daño. No obstante, estas amenazas pueden afectar a la seguridad y a los aspectos financieros de una organización. Por estos motivos se recomienda que conozca las amenazas que representan para la infraestructura de TI de su organización y para la productividad de los usuarios de TI.
  
#### Software de humor
  
Las aplicaciones de humor están diseñadas para conseguir una sonrisa o, en el peor de los casos, una pérdida de tiempo para el usuario. Estas aplicaciones son tan antiguas como los propios equipos informáticos. Como no se han creado con una intención maliciosa y se pueden identificar fácilmente como bromas, no se consideran software malintencionado en esta guía. Existen numerosos ejemplos de aplicaciones de humor, que ofrecen desde interesantes efectos de pantalla hasta divertidas animaciones o juegos.
  
#### Mensajes de virus falsos
  
Generalmente, resulta más sencillo engañar a alguien para que realice la acción que uno desea que escribir software que la lleve a cabo sin que éste lo advierta. Por lo tanto, en la comunidad de TI existe una gran cantidad de mensajes de virus falsos.
  
Al igual que otras formas de software malintencionado, un *mensaje de virus falso* utiliza la ingeniería social con el fin de intentar engañar a los usuarios de los equipos para que realicen una acción. No obstante, en el caso de un mensaje de virus falso, no se ejecuta ningún código; su creador habitualmente sólo intenta engañar a la víctima. A lo largo de los años, estos mensajes han adoptado formas muy diversas. Sin embargo, un ejemplo muy común consiste en un mensaje de correo electrónico en el que se anuncia la aparición de un nuevo tipo de virus y se aconseja reenviar el mensaje a los contactos para ponerles sobre aviso. Estos mensajes de virus falsos suponen una pérdida de tiempo, ocupan los recursos de los servidores de correo electrónico y consumen ancho de banda de red.
  
#### Fraudes
  
Prácticamente toda forma de comunicación se ha utilizado en algún momento por parte de delincuentes para intentar engañar a sus víctimas y conseguir que realicen acciones que les reporten un beneficio económico. Internet, los sitios Web y los mensajes de correo electrónico no son una excepción. Un ejemplo típico consiste en un mensaje de correo electrónico que intenta engañar al destinatario para que revele información personal que se pueda utilizar con objetivos ilegales (por ejemplo, información sobre cuentas bancarias). Un tipo especial de fraude es el denominado *phishing*, que se pronuncia igual que “fishing”, ("pesca", en inglés) y que también se conoce como *suplantación de marca* o *carding*.
  
Como ejemplos de "phishing" se pueden mencionar los casos en los que los remitentes suplantan a compañías de gran prestigio, como por ejemplo eBay, para intentar obtener acceso a la información de la cuenta del usuario. Este tipo de mensajes utiliza con frecuencia un sitio Web que imita el aspecto del sitio Web oficial de una compañía. El mensaje de correo electrónico se utiliza para redirigir al usuario al sitio Web falso y conseguir que escriba la información de su cuenta de usuario, que se guarda y usa con fines ilícitos. Estos casos se deben tratar con total seriedad y poner en conocimiento de las autoridades legales.
  
#### Correo no deseado
  
También conocido como *spam*, se trata de correo electrónico no deseado que se genera para hacer publicidad de un servicio o producto. Aunque generalmente se considera una molestia, no se trata de software malintencionado. Sin embargo, el enorme incremento en la cantidad de mensajes de este tipo constituye un problema para la infraestructura de Internet, con el resultado de pérdida de productividad para los empleados, que se ven obligados a descartar y eliminar estos mensajes a diario.
  
Aunque no existe acuerdo sobre el origen del término "spam", no hay duda de que éste se ha convertido en una de las molestias más constantes en las comunicaciones basadas en Internet. Muchos consideran que constituye un problema de tal gravedad que actualmente representa una amenaza para el funcionamiento de las comunicaciones a través de correo electrónico en el mundo. Sin embargo, es preciso mencionar que salvo por la carga que soportan los servidores de correo electrónico y los programas anti-spam, los mensajes no deseados no se pueden replicar o amenazar el correcto estado y funcionamiento de los sistemas de TI de una organización.
  
Los creadores de correo no deseado (conocidos con el término inglés *spammers*) han utilizado a menudo software malintencionado para instalar un servicio de servidor de correo electrónico SMTP de pequeño tamaño en un equipo host que, a continuación, utilizan para enviar este tipo de mensajes a otros destinatarios de correo electrónico.
  
#### Programas espía
  
Este tipo de software se denomina en ocasiones *spybot* o *software de seguimiento*. Los *programas espía* utilizan otras formas de software y programas engañosos que realizan algunas acciones en un equipo sin el consentimiento del usuario. Entre ellas se incluyen la recopilación de información personal y el cambio de los parámetros de configuración del explorador de Internet. Además de ser una molestia, los programas espía pueden causar problemas que abarcan desde la reducción del rendimiento general del equipo hasta la violación de la privacidad personal.
  
Los sitios Web que distribuyen estos programas utilizan una gama de trucos para conseguir que los usuarios los descarguen e instalen en sus equipos. Entre estos trucos se incluye la creación de experiencias de usuario engañosas y la inclusión de programas espía junto con otro software en el que los usuarios pueden estar interesados, por ejemplo los programas gratuitos para compartir archivos.
  
#### Publicidad no deseada
  
La *publicidad no deseada* se combina con frecuencia con una aplicación host que se ofrece de modo gratuito a condición de que el usuario acepte dicha publicidad. Como las aplicaciones de publicidad no deseada generalmente se instalan después de que el usuario haya aceptado un contrato de licencia en el que se advierte del objetivo de la aplicación, no se comete ningún delito. No obstante, los mensajes de publicidad emergentes se pueden convertir en una molestia y, en algunos casos, afectar al rendimiento del sistema. Asimismo, la información que recopilan algunas de estas aplicaciones puede plantear problemas de privacidad a los usuarios que no eran totalmente conscientes de los términos del contrato de licencia.
  
**Nota**: aunque los términos *spyware (programa espía)* y *adware (publicidad no deseada)* se utilizan con frecuencia como sinónimos, únicamente la publicidad no deseada que el usuario no ha autorizado se puede equiparar a los programas espía. La publicidad no deseada que advierte a los usuarios y les ofrece la posibilidad de elección y el control no es engañosa y no se debe clasificar como programa espía. Por otra parte se debe tener en cuenta que una aplicación espía que afirma realizar una función específica y que, en realidad, lleva a cabo otra diferente, actúa como un troyano.
  
#### Cookies de Internet
  
Las cookies de Internet son archivos de texto que los sitios Web colocan en el equipo de un usuario cuando éste los visita. Contienen y proporcionan información de identificación acerca del usuario a los sitios Web que las han colocado en su equipo, además de otra información que los sitios deseen conservar acerca de su visita.
  
Son herramientas legales que numerosos sitios Web utilizan para realizar un seguimiento de la información de los visitantes. Por ejemplo, un usuario adquiere un artículo en una tienda en línea, pero una vez que ha colocado el producto en su carro de la compra, puede que desee visitar otro sitio Web por alguna razón. La tienda en línea puede elegir guardar en una cookie en el equipo del usuario la información de los productos seleccionados, para que, cuando éste vuelva al sitio, sigan en el carro de la compra listos para que el usuario los adquiera si así lo decide.
  
Los desarrolladores de sitios Web sólo deberían poder recuperar la información almacenada en las cookies que ellos han creado. Este enfoque debería garantizar la privacidad evitando que otras personas que no sean los desarrolladores de estos sitios puedan tener acceso a las cookies que se han dejado en los equipos de los usuarios.
  
Por desgracia, se sabe que algunos desarrolladores de sitios Web utilizan cookies para recopilar información sin el conocimiento del usuario. Algunos pueden engañar a los usuarios o no respetar las directivas que han establecido. Por ejemplo, pueden realizar un seguimiento de los hábitos de visita a diferentes sitios Web sin informar al usuario y utilizar esta información para personalizar la publicidad que éste ve en un sitio Web, algo que se considera una invasión de la privacidad. Resulta difícil identificar esta forma de publicidad orientada al usuario y otras formas de "uso indebido de las cookies", con lo que es complicado decidir si se deben bloquear las cookies en el equipo y cuándo y cómo hacerlo. Además, el nivel aceptable de información compartida varía de unos usuarios a otros, por lo que también resulta complicado crear un programa "anti-cookies" que satisfaga las necesidades de todos los usuarios informáticos de un entorno.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Software antivirus
  
El software antivirus se crea específicamente para defender un sistema frente a las amenazas del software malintencionado. Microsoft recomienda encarecidamente el uso de este tipo de programas para proteger el equipo de cualquier forma de software malintencionado, no únicamente de los virus.
  
El software antivirus utiliza diferentes técnicas para detectar el software malintencionado. En esta sección se explicará el funcionamiento de algunas de ellas, entre las que se incluyen:
  
-   **Análisis de firma**. La mayor parte de los programas antivirus utilizan actualmente esta técnica, que se centra en analizar el objetivo (equipo host, unidad de disco o archivos) en busca de un patrón que pueda tratarse de software malintencionado. Estos patrones se almacenan generalmente en archivos denominados archivos de firma, que los proveedores del software actualizan con regularidad con el fin de garantizar que los escáneres antivirus reconocen todos los ataques de código malintencionado posibles. El principal problema de esta técnica radica en que el software antivirus ya debe estar actualizado para que el escáner lo pueda reconocer.
  
-   **Análisis heurístico**. Esta técnica intenta detectar las variantes nuevas y conocidas de software malintencionado mediante la búsqueda de características generales en dicho software. La principal ventaja de esta técnica consiste en que no depende de los archivos de firma para identificar y hacer frente al software malintencionado. No obstante, el análisis heurístico muestra una serie de problemas específicos, entre los que se incluyen los siguientes:
  
    -   **Positivos falsos**. Esta técnica utiliza características generales y, por tanto, es susceptible de confundir el software legítimo con el malintencionado si una característica fuera similar en ambos.
  
    -   **Lentitud del análisis**. El proceso de búsqueda de características resulta una tarea más laboriosa que la de buscar un patrón de software malintencionado ya conocido. Por este motivo, el software antivirus puede tardar más tiempo en realizar un análisis heurístico que un análisis de firma.
  
    -   **Es probable que se pasen por alto características nuevas**. Si el ataque de un nuevo software malintencionado presenta una característica que no se ha identificado previamente, probablemente el analizador heurístico no la detecte hasta que se actualice.
  
-   **Bloqueo del comportamiento**. Esta técnica se centra en el comportamiento de un ataque en lugar de en el propio código. Por ejemplo, si una aplicación intenta abrir un puerto de red, un programa antivirus de bloqueo del comportamiento podría detectarlo como una acción típica de software malintencionado y, a continuación, clasificar este comportamiento como posible ataque.
  
Numerosos proveedores de antivirus utilizan actualmente una combinación de estas técnicas en sus soluciones antivirus en un intento de mejorar el nivel de protección general de los equipos informáticos de sus clientes.
  
Muchos socios de Microsoft ofrecen programas antivirus. Para obtener una lista completa y actualizada, consulte la página "Microsoft Antivirus Partners" en Microsoft.com: <http://www.microsoft.com/security/partners/antivirus.asp> (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Ciclo de vida típico del software malintencionado en circulación
  
Se ha establecido un patrón que define el ciclo de vida de los nuevos ataques de software malintencionado presente en las redes públicas o que está actualmente en circulación o *in the Wild*. El examen de este patrón ayuda a comprender el riesgo que representan los nuevos ataques tras su aparición.
  
Un nuevo ciclo de vida se inicia con el desarrollo del software malintencionado y finaliza cuando se elimina por completo de las redes supervisadas. Las etapas del ciclo de vida son las siguientes:
  
1.  **Creación**. El desarrollo del software malintencionado se inicia con frecuencia cuando se sugiere y comparte entre las comunidades de piratas informáticos la posibilidad de una nueva forma de ataque o aprovechamiento. Durante un tiempo, se estudian y analizan estos métodos hasta que se descubre un enfoque que se puede convertir en ataque.
  
2.  **Desarrollo**. Anteriormente, la creación de software malintencionado requería un conocimiento del lenguaje del ensamblado del equipo así como del complejo funcionamiento del sistema contra el que se dirigía el ataque. Sin embargo, la aparición de los kits de herramientas y de los salones de chat de Internet ha hecho posible que casi cualquier persona que lo desee pueda crear software malintencionado.
  
3.  **Replicación**. Una vez que el nuevo software se ha desarrollado y puesto en circulación, normalmente busca replicarse en los dispositivos host potenciales durante un tiempo antes de poder llevar a cabo su función principal o entregar su carga.
  
    **Nota**: aunque existen decenas de miles de programas de software malintencionado conocidos, únicamente una pequeña parte está en circulación actualmente. La mayor parte de estos programas nunca se han expuesto al público y a menudo se conocen como *virus de zoo*.
  
4.  **Entrega de la carga**. Una vez el software malintencionado ha infectado un host, puede entregar una carga. Si el código contiene una activación condicional para su carga, es en este momento cuando se cumplen las condiciones para el mecanismo de entrega. Por ejemplo, algunas cargas se activan cuando un usuario realiza determinada acción o cuando el reloj del equipo host llega a una fecha específica. Si el software malintencionado contiene una activación de acción directa, simplemente comenzará a entregar la carga en el momento en que se complete la infección. Por ejemplo, en el caso de las cargas de registro de datos, el programa de software malintencionado simplemente comenzará a registrar los datos requeridos.
  
5.  **Identificación**. En este momento de su ciclo de vida, las comunidades antivirus identifican el software malintencionado. En la mayor parte de los casos, este paso ocurrirá antes de la etapa 4 o incluso antes de la 3, aunque no siempre es así.
  
6.  **Detección**. Una vez identificada la amenaza, los desarrolladores de software antivirus deben analizar el código para hallar un método de detección apropiado. Cuando han determinado el método, pueden actualizar los archivos de firma antivirus para permitir que las aplicaciones antivirus existentes detecten el nuevo software malintencionado. La duración de este proceso es fundamental para controlar un ataque.
  
7.  **Eliminación**. Cuando la actualización está disponible para el público, es responsabilidad de los usuarios de las aplicaciones antivirus aplicar la actualización periódicamente para proteger sus equipos del ataque (o limpiar los equipos ya infectados).
  
    **Nota**: si no se actualizan los archivos de firma locales con regularidad los riesgos pueden ser muy altos, ya que los usuarios creen que están protegidos mediante sus productos antivirus, cuando en realidad no lo están.
  
Cuantos más usuarios actualicen sus programas antivirus, el software malintencionado irá dejando de constituir una amenaza. Este proceso en pocas ocasiones elimina todas las instancias del software en circulación, puesto que éste puede seguir residiendo en los equipos conectados a Internet con escasa o nula protección antivirus. No obstante, se reduce la amenaza de un ataque generalizado.
  
Aunque este ciclo de vida se repite con cada nuevo ataque diseñado, no es típico de todos los ataques. Muchos de ellos son simplemente versiones modificadas de una parte de un código malintencionado original. Por lo tanto, el código básico y el enfoque del software malintencionado son idénticos, pero se realizan pequeñas modificaciones para impedir que se detecte y elimine. Típicamente, un ataque que haya tenido éxito generará diferentes versiones durante las semanas y meses siguientes. Esta situación lleva a una especie de "carrera armamentística" en la que los creadores de este tipo de software intentan evitar la detección para su propio provecho, ya se trate de obtener beneficio económico, fama o simplemente satisfacer su curiosidad. Las defensas antivirus se actualizan de nuevo, se revisan o modifican según sea necesario para reducir la renovada amenaza.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
El software malintencionado es un área compleja y en constante evolución dentro del ámbito de la tecnología informática. De todos los problemas que se encuentran en la TI, pocos están tan extendidos y resultan tan engorrosos como los ataques de este tipo de software y los costes derivados de su tratamiento. Comprender su funcionamiento, el modo en que evolucionan a lo largo del tiempo y los vectores de ataque que aprovechan, puede ayudar a tratar este asunto de un modo activo. Este conocimiento puede, a su vez, propiciar un proceso de reacción más efectivo cuando afecten a su organización.
  
Como este tipo de software utiliza tantas técnicas para generarse, distribuirse y explotar los equipos informáticos, puede resultar difícil saber cómo se puede asegurar un equipo lo suficiente como para resistir a tales ataques. No obstante, una vez se conocen los riesgos y vulnerabilidades, se puede administrar un sistema de modo que la posibilidad de que un ataque tenga éxito se reduzca en gran medida.
  
El siguiente paso consiste en analizar los riesgos en diferentes puntos de la infraestructura de TI con el fin de diseñar una defensa eficaz, cuestión que se tratará en el siguiente capítulo. El diseño de un plan de recuperación eficaz es el tema principal en el que se centra el último capítulo de esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 3: Defensa en profundidad antivirus
  
[](#efhg)[Introducción](#efhg)  
[](#efhm)[Vectores de amenazas de software malintencionado](#efhm)  
[](#efhn)[Enfoque de defensa contra software malintencionado](#efhn)  
[](#efhi)[Defensas del cliente](#efhi)  
[](#efhj)[Defensas del servidor](#efhj)  
[](#efhk)[La capa de defensa de la red](#efhk)  
[](#efhl)[Seguridad física](#efhl)  
[](#efhp)[Directivas, procedimientos y concienciación](#efhp)  
[](#efhq)[Resumen](#efhq)
  
### Introducción
  
Todas las organizaciones deberían desarrollar una solución antivirus que les proporcionara un elevado nivel de protección. No obstante, a pesar de seguir esta recomendación e instalar software antivirus, gran parte de ellas aún se infectan. Esta guía propone un acercamiento distinto al problema del *software malintencionado*. Como diseño de seguridad de la red, Microsoft recomienda una solución antivirus realizada con un enfoque de defensa en profundidad que asegure que se mantienen las medidas preventivas adoptadas por la organización.
  
Tal enfoque es vital para la seguridad de los equipos de cualquier organización, puesto que, por desgracia, y a pesar de la gran cantidad de características y servicios prácticos que ofrece un sistema informático, siempre existe alguien que por los motivos que sean intenta encontrar una vulnerabilidad de la que aprovecharse malintencionadamente.
  
La colaboración con consultores e ingenieros de sistemas que han implementado Microsoft® Windows Server™ 2003, Windows® XP Professional y Windows® 2000 en distintos entornos ha servido para establecer las prácticas más útiles y actualizadas para proteger del software malintencionado a los clientes y servidores que ejecutan estos sistemas operativos. En este capítulo se facilita toda esta información.
  
Además, se proporcionan instrucciones que le ayudarán a utilizar un método de defensa en profundidad al diseñar una solución de seguridad antivirus para su organización. El objetivo de este enfoque es que comprenda las particularidades de cada capa del modelo y que conozca las amenazas concretas a las que cada una de ellas se expone, a fin de que pueda utilizar esa información cuando implemente las defensas antivirus.
  
**Nota**: Microsoft recomienda incluir algunos de los pasos de esta guía en las directivas y procedimientos generales de seguridad de su organización. Cuando aparecen, la guía los identifica como pasos necesarios que debe definir el equipo de seguridad.
  
**Importante**: si sospecha que su organización es actualmente víctima de un ataque, consulte el capítulo 4 de esta guía, "Control y recuperación de los ataques de virus", antes de leer el presente capítulo.
  
Si consulta esta guía después de haber sufrido un ataque de software malintencionado y haberse recuperado del mismo, la información proporcionada le ayudará a impedir que vuelva a suceder y comprender cómo tuvo lugar.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Vectores de amenazas de software malintencionado
  
El software malintencionado puede comprometer la seguridad de una organización con distintos métodos. Estos se denominan en ocasiones *vectores de amenazas* y representan las zonas del entorno que exigen mayor atención durante la elaboración de una solución antivirus eficaz. En la siguiente lista se incluyen las zonas de una organización típica que corren el mayor riesgo de sufrir un ataque de software malintencionado:
  
-   **Redes externas**. Toda red que no se encuentre bajo el control directo de una organización se debe considerar como posible origen de software malintencionado. Internet supone, con diferencia, la mayor amenaza de software malintencionado; el anonimato y la conectividad que proporciona permiten que los intrusos obtengan acceso rápido y eficaz a muchos objetivos para establecer ataques a través de código malintencionado.
  
-   **Clientes invitados**. A medida que el uso de equipos portátiles y dispositivos móviles se hace más frecuente en los negocios, los propios dispositivos entran y salen de otras infraestructuras empresariales con mayor asiduidad. Si los clientes invitados no cuentan con una defensa antivirus eficaz, representan una amenaza de software malintencionado para la organización.
  
-   **Archivos ejecutables**. Todo código con capacidad para ejecutarse puede actuar como software malintencionado. En esta categoría no sólo se incluyen programas, sino también secuencias de comandos, archivos por lotes y objetos activos como los controles de Microsoft ActiveX®.
  
-   **Documentos**. Debido al aumento de la popularidad de los procesadores de texto y las hojas de cálculo, este tipo de aplicaciones se ha convertido en objetivo para los autores de software malintencionado, que aprovechan los lenguajes de macro que admiten muchas aplicaciones.
  
-   **Correo electrónico**. Los autores de software malintencionado pueden utilizar los archivos adjuntos y el código de lenguaje de marcado de hipertexto (HTML) activo en los mensajes de correo electrónico como formas de ataque.
  
-   **Medios extraíbles**. La transferencia de archivos a través de un medio extraíble es una cuestión que las organizaciones deben tratar como parte de su defensa antivirus. Entre los medios extraíbles más habituales se incluyen:
  
    -   **Discos CD-ROM o DVD-ROM**. El abaratamiento de los dispositivos de grabación de CD y DVD ha facilitado el acceso a estos medios de todos los usuarios, incluidos los autores de software malintencionado.
  
    -   **Disquetes y unidades Zip**. A pesar de que estos medios se utilizan cada vez menos debido a la velocidad y capacidad limitadas que tienen, constituyen un riesgo si el software malintencionado consigue tener acceso a ellos.
  
    -   **Unidades USB**. Estos dispositivos adquieren muchas formas, desde el clásico dispositivo del tamaño de un llavero hasta un reloj de pulsera. Todos ellos se pueden utilizar para introducir software malintencionado en el puerto bus serie universal (USB) de un host.
  
    -   **Tarjetas de memoria**. Las cámaras digitales y los dispositivos móviles, como los PDA y teléfonos móviles, han contribuido al establecimiento de las tarjetas de memoria digitales. Los lectores de tarjetas se están convirtiendo prácticamente en dispositivos de serie en los equipos, ya que facilitan el proceso de transferencia de datos. Dado que dichos datos llegan en forma de archivo, las tarjetas también pueden transferir software malintencionado a un sistema host.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Enfoque de defensa contra software malintencionado
  
Antes de intentar organizar una defensa eficaz contra el software malintencionado, resulta esencial comprender las distintas partes de la infraestructura de la organización que pueden resultar amenazadas, así como la importancia del riesgo en cada una de ellas. Microsoft recomienda que se realice una evaluación completa de los riesgos para la seguridad antes de iniciar el diseño de una solución antivirus, ya que de ella podrá obtener toda la información que necesita para optimizar el diseño de la solución.
  
Para obtener información e instrucciones sobre la forma de realizar este tipo de evaluación, consulte la guía *Microsoft Solution for Securing Windows 2000 Server* en:  
<http://www.microsoft.com/technet/security/prodtech/win2000/secwin2k/default.mspx> (en inglés). En ella se proporciona una introducción a la disciplina de administración de riesgos de seguridad (SRMD), con la que podrá comprender la naturaleza de la exposición de la organización a las amenazas.
  
#### Modelo de seguridad de defensa en profundidad
  
Una vez haya conocido y documentado los riesgos a los que la organización hace frente, el siguiente paso consiste en examinar y organizar la defensa que utilizará para la solución antivirus. El modelo de seguridad de defensa en profundidad constituye un punto de partida excelente para ello, ya que identifica siete niveles de defensas de seguridad diseñados para bloquear cualquier intento de comprometer la seguridad de una organización. Cada conjunto de defensas es capaz de desviar ataques en muchas y distintas escalas. Si no conoce el modelo de seguridad de defensa en profundidad, Microsoft le recomienda que visite la página "Security Content Overview" en Microsoft TechNet:  
<http://www.microsoft.com/technet/security/bestprac/overview.mspx> (en inglés).
  
También puede encontrar información adicional y ejemplos de diseño prácticos para este proceso en *MSA Reference Architecture Kit* en TechNet:  
<http://www.microsoft.com/resources/documentation/msa/2/all/solution/en-us/msa20rak/vmhtm1.mspx> (en inglés).
  
En la siguiente ilustración se describen las capas definidas para el modelo de seguridad de defensa en profundidad:
  
[![](images/Cc162791.AVFG0301(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0301_big(es-es,technet.10).gif)
  
**Figura 3.1 Capas del modelo de seguridad de defensa en profundidad**
  
Las capas incluidas en la ilustración ofrecen una vista de cada área del entorno que se debe tener en cuenta durante el diseño de defensas de seguridad para la red.
  
Las definiciones detalladas de cada capa se pueden modificar según los requisitos y las prioridades de seguridad de su organización. En esta guía, las siguientes definiciones sencillas definen las capas del modelo:
  
-   **Datos**. El riesgo en esta capa se debe a las vulnerabilidades que un atacante podría aprovechar para obtener acceso a los datos de configuración y organización, o cualquier dato que sea exclusivo de un dispositivo que utiliza la empresa. Por ejemplo, los datos empresariales confidenciales, los datos de los usuarios o la información privada de los clientes se incluirían en esta capa. Lo que más preocupa a una organización en esta capa del modelo son los problemas legales y empresariales que se pueden derivar de la pérdida o el robo de datos, así como los problemas operativos que las vulnerabilidades pueden descubrir en el host o en las aplicaciones.
  
-   **Aplicación**. El riesgo en esta capa se debe a las vulnerabilidades que un atacante podría aprovechar para obtener acceso a las aplicaciones en ejecución. Todo código ejecutable que un autor de software malintencionado pueda reunir fuera de un sistema operativo se puede utilizar para atacar un sistema. Las principales preocupaciones de la organización en esta capa son el acceso a los archivos binarios que componen las aplicaciones, el acceso al host a través de las vulnerabilidades en los servicios de escucha de la aplicación o la recopilación ilícita de datos concretos del sistema para transferirlos a alguien que pueda utilizarlos en beneficio propio.
  
-   **Host**. Por norma general, esta es la capa en la que se centran los proveedores que ofrecen Service Packs y revisiones con el objetivo de tratar las amenazas de software malintencionado. En ella, el riesgo proviene de los atacantes que se aprovechan de las vulnerabilidades en los servicios que ofrecen el host o el dispositivo. Los atacantes los utilizan de distintas formas para organizar ataques contra el sistema. Un desbordamiento de búfer, que se produce como resultado de agregar a un búfer más información de la que puede contener, es un buen ejemplo. En este caso, en lo que las organizaciones ponen más empeño es en impedir el acceso a los archivos binarios que componen el sistema operativo, así como el acceso al host a través de vulnerabilidades en los servicios de escucha.
  
-   **Red interna**. Los riesgos para las redes internas de las organizaciones están relacionados con los datos confidenciales que se transmiten a través ellas. Los requisitos de conectividad para las estaciones de trabajo clientes en estas redes internas también suponen algunos riesgos asociados.
  
-   **Red perimetral**. Los riesgos de la capa de red perimetral (también denominada zona desmilitarizada, DMZ o subred protegida) tienen su origen en el posible acceso por parte de un atacante a las redes de área extensa (WAN) y los niveles de red que conectan. Los principales problemas se centran en los puertos TCP (protocolo de control de transmisión) y UDP (protocolo de datagrama de usuario) disponibles que utiliza la red.
  
-   **Seguridad física**. Los riesgos se encuentran en el acceso físico de un atacante a un activo físico. Esta capa integra todas las anteriores, puesto que el acceso físico a un activo puede permitir el acceso a las demás capas del modelo de defensa en profundidad. Aquí, la preocupación principal para las organizaciones que utilizan sistemas antivirus es impedir que los archivos infectados salten las defensas de las redes perimetral e interna. Los atacantes pueden intentar hacerlo con tan sólo copiar un archivo infectado directamente en el equipo host a través de algún medio extraíble físico, como un dispositivo de disco USB.
  
-   **Directivas, procedimientos y concienciación**. Rodeando todas las capas del modelo de seguridad se encuentran las directivas y procedimientos que la organización necesita establecer a fin de cumplir y admitir los requisitos de cada nivel. Por último, resulta importante que se estimule la concienciación en la organización de todas las partes interesadas. En muchos casos, el desconocimiento de un riesgo puede llevar consigo infracciones en la seguridad, por lo que el aprendizaje también debe formar parte integrante de cualquier modelo de seguridad.
  
El uso de las capas de seguridad del modelo como base del método de defensa en profundidad antivirus le permitirá replantearse la perspectiva y optimizarlas en grupos para aplicar las defensas antivirus en su organización. La forma en que se lleve a cabo esta optimización dependerá completamente de las prioridades de la propia empresa, así como de las aplicaciones de defensa concretas que utilice. Lo importante es evitar un diseño antivirus incompleto y débil. Para ello, es preciso asegurase de que no se excluya ninguna de las capas de las defensas. En la siguiente ilustración se muestra la vista de una defensa en profundidad antivirus más específica:
  
[![](images/Cc162791.AVFG0302(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0302_big(es-es,technet.10).gif)
  
**Figura 3.2 Vista de una defensa en profundidad antivirus específica**
  
Las capas Datos, Aplicación y Host se pueden combinar en dos estrategias defensivas para proteger los clientes y servidores de la organización. Aunque estas defensas comparten determinadas estrategias, las diferencias al implementarlas en el cliente y en el servidor son suficientes para hacer necesario un único enfoque defensivo en cada una de ellas.
  
Las capas Red interna y Red perimetral también se pueden combinar en una estrategia de defensas de red común, ya que las tecnologías implicadas son las mismas para ambas. Sin embargo, los detalles de la implementación diferirán en cada capa, según la posición de los dispositivos y las tecnologías de la infraestructura de la organización.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Defensas del cliente
  
Cuando software malintencionado llega a un equipo host, los sistemas de defensa se deben centrar en proteger el sistema y los datos que contiene, y detener la propagación de la infección. Estas defensas no son menos importantes que las físicas y de red del entorno. Se deben diseñar partiendo de la base de que el software malintencionado ha sido capaz de superar todas las anteriores capas de defensa para llegar al host. Este método es la mejor forma de lograr el máximo nivel de protección.
  
#### Pasos de la protección antivirus del cliente
  
Son varios los métodos y tecnologías que se pueden utilizar para las configuraciones antivirus de los clientes. En las siguientes secciones se proporcionan detalles que Microsoft recomienda tener en cuenta.
  
##### Paso 1: Reducir el ámbito de ataque
  
La primera línea de defensa en la capa de aplicación consiste en reducir el ámbito de ataque del equipo. Será necesario quitar o deshabilitar todas las aplicaciones o servicios innecesarios para minimizar las vías desde las que atacante podría aprovechar el sistema de forma malintencionada.
  
Encontrará la configuración predeterminada para los servicios de Windows XP Professional en la página "Default settings for services" de la documentación del producto Windows XP Professional en Microsoft.com: <http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/sys_srv_default_settings.mspx> (en inglés).
  
Una vez que el ámbito de ataque se ha reducido al mínimo sin afectar a la funcionalidad necesaria del sistema, la defensa fundamental que se debe utilizar en esta capa es un escáner antivirus. La función primordial del escáner consiste en detectar y evitar un ataque para, a continuación, notificar al usuario y quizás también a los administradores del sistema de la organización.
  
##### Paso 2: Aplicar actualizaciones de seguridad
  
La gran cantidad y variedad de equipos cliente que puede haber conectados en las redes de una organización puede dificultar la utilización de un servicio confiable de administración de actualizaciones de seguridad. Microsoft y otras empresas de software han desarrollado distintas herramientas que se pueden utilizar para solventar este problema. Las siguientes herramientas de actualizaciones de seguridad y administración de revisiones se encuentran disponibles en Microsoft:
  
-   **Windows Update**. Ideal para pequeñas empresas o particulares, el servicio Windows Update ofrece un proceso, que puede ser automático o manual, que permite detectar y descargar las más recientes modificaciones de la seguridad y las características de la plataforma Windows. Entre las desventajas de este método para algunas organizaciones se incluye la falta de soporte para probar las actualizaciones antes de implementarlas, así como la cantidad de ancho de banda de la red que pueden llegar a consumir los clientes de la organización al descargar el mismo paquete a la vez. Para obtener información sobre el uso de este servicio, visite la página principal de Windows Update en:  
    [www.windowsupdate.com](http://www.windowsupdate.com/) (en inglés).
  
-   **Software Update Service**. Este servicio se ha diseñado para ofrecer una solución de actualizaciones de seguridad a los clientes Windows en la empresa. Soluciona las deficiencias que las actualizaciones de Windows Update suponían para las organizaciones de mayor tamaño, permitiendo las pruebas internas y la administración distribuida de las actualizaciones de seguridad. Para obtener información sobre el uso de este servicio para desarrollar una solución para su organización, consulte la página principal de Software Update Services en Microsoft.com:  
    [http://www.microsoft.com/windowsserversystem/sus/](http://technet.microsoft.com/es-es/wsus/bb466186.aspx) (en inglés).
  
-   **Systems Management Server 2003**. Microsoft Systems Management Server 2003 es una completa solución de administración empresarial que puede ofrecer servicios de actualizaciones de seguridad, entre otras muchas cosas. Para obtener más información sobre esta solución, consulte la página principal de Systems Management Server en Microsoft.com:  
    <http://www.microsoft.com/smserver/default.asp> (en inglés).
  
Cada una de estas herramientas de actualizaciones de seguridad de Microsoft tiene ventajas y objetivos concretos. Probablemente la mejor alternativa sea utilizar más de una. Para ayudarle a evaluar las soluciones de actualizaciones de seguridad disponibles, consulte la comparación de características proporcionada en la página "Choosing a Security Update Management Solution" en Microsoft.com:  
<http://www.microsoft.com/windowsserversystem/sus/suschoosing.mspx> (en inglés).
  
##### Paso 3: Habilitar un servidor de seguridad basado en host
  
El servidor de seguridad personal o basado en host representa una capa relevante para la defensa del cliente que se debe habilitar, especialmente en los equipos portátiles que los usuarios pueden utilizar fuera de las habituales defensas físicas y de red de la organización. Estos servidores de seguridad filtran todos los datos que intentan entrar o salir de un determinado equipo host.
  
Windows XP incluye un sencillo servidor de seguridad personal denominado Servidor de seguridad de conexión a Internet (ICF). Una vez habilitado, ICF supervisa todos los aspectos de la comunicación. Además, ICF inspecciona las direcciones de origen y destino de cada paquete de datos para garantizar que se permiten todas las comunicaciones. Para obtener más información sobre ICF, consulte el sistema de Ayuda de Windows XP y la página "Use the Internet Connection Firewall" en Microsoft.com:  
<http://www.microsoft.com/windowsxp/pro/using/howto/networking/icf.asp> (en inglés).
  
Windows XP Service Pack 2 introduce algunas mejoras significativas en ICF (ahora denominado *Windows Firewall*), así como mejoras orientadas a la seguridad. Un Service Pack es un conjunto probado de todas las revisiones, actualizaciones de seguridad, actualizaciones fundamentales y actualizaciones creadas para los defectos detectados internamente que se han generado desde la salida de un producto. Los Service Packs pueden además incluir un número limitado de características o cambios en el diseño solicitados por el propio cliente. Para obtener información sobre esta actualización para Windows XP, consulte la página de Windows XP Service Pack 2 en Microsoft TechNet:  
<http://www.microsoft.com/technet/prodtechnol/winxppro/sp2preview.mspx> (en inglés).
  
Las versiones anteriores a Windows XP no se suministraban con un servidor de seguridad integrado. Existen soluciones de servidor de seguridad basado en host de terceros que se pueden instalar tanto para ofrecer estos servicios a las versiones anteriores de Windows como para mejorarlos en clientes Windows XP. Para obtener información sobre estos productos de servidor de seguridad, consulte la página "Frequently Asked Questions About Internal Firewalls" en el sitio Web Protect Your PC de Microsoft:  
<http://www.microsoft.com/security/protect/firewall.asp> (en inglés).
  
##### Paso 4: Instalar software antivirus
  
Gran cantidad de empresas fabrican aplicaciones antivirus con las que intentan proteger el equipo host sin suponer molestias para los usuarios y teniendo la menor interacción posible con ellos. La mayoría de estas aplicaciones han resultado muy eficaces en la protección, aunque todas exigen actualizaciones frecuentes para estar al día sobre el nuevo software malintencionado. Toda solución antivirus debe ofrecer un mecanismo rápido y directo que garantice que se reciben lo antes posible las actualizaciones de los *archivos de firma* necesarias para tratar el software malintencionado tanto nuevo como con variantes. Un archivo de firma contiene información que los programas antivirus utilizan para detectar software malintencionado durante una comprobación. Se han diseñado de forma que los proveedores de la aplicación antivirus los actualicen con regularidad y se descarguen en el equipo cliente.
  
**Nota**: estas actualizaciones también pueden presentar un riesgo de seguridad, ya que los archivos de firma se envían desde el sitio de soporte de la aplicación antivirus a la aplicación host (normalmente, a través de Internet). Por ejemplo, si el mecanismo de transferencia utiliza el protocolo de transferencia de archivos (FTP) para obtener el archivo, los servidores de seguridad perimetrales de la organización deben permitir el acceso con este protocolo al servidor FTP en Internet. Asegúrese de revisar el mecanismo de actualización durante el proceso de evaluación de riesgos antivirus y comprobar que cumple los requisitos de seguridad de su organización.
  
Debido a que las técnicas y patrones del software malintencionado se encuentran en continuo cambio, algunas organizaciones han adoptado un método que recomienda que algunos usuarios de "alto riesgo" ejecuten más de un paquete antivirus en el mismo equipo para minimizar el riesgo de que no se detecte la presencia de software malintencionado. En esta categoría se incluyen los siguientes tipos de usuarios:
  
-   Administradores Web o cualquier individuo que administre el contenido en Internet o en una intranet.
  
-   Empleados de los laboratorios de versiones o cualquiera que produzca medios electrónicos, como CD-ROM.
  
-   Miembros del equipo de desarrollo que crean o compilan archivos comprimidos u otro producto de software.
  
Hay que tener en cuenta que la ejecución de aplicaciones antivirus de varios proveedores de aplicaciones en el mismo equipo puede causar problemas debido a la interoperabilidad entre las aplicaciones antivirus. Algunos de los problemas más comunes que pueden surgir en un entorno en el que se ejecute más de un producto antivirus son:
  
-   **Sobrecarga de la memoria**. Muchas aplicaciones antivirus utilizan agentes activos que permanecen residentes en la memoria, reduciendo así la cantidad de memoria disponible en el sistema.
  
-   **Bloqueos del sistema o errores de detención**. Estos bloqueos y errores se pueden deber a que las aplicaciones antivirus intentan comprobar el mismo archivo a la vez.
  
-   **Pérdida del rendimiento**. A medida que las aplicaciones antivirus exploran los archivos para comprobar si existe código malintencionado, el rendimiento del sistema puede disminuir. Con varias aplicaciones antivirus, las comprobaciones se realizan varias veces, lo que puede reducir el rendimiento del sistema hasta llegar a un nivel inaceptable.
  
-   **Pérdida de acceso al sistema**. Cuando se intentan ejecutar a la vez varias aplicaciones antivirus, puede que el sistema se detenga durante el inicio. Este problema es más habitual en versiones anteriores de Windows, como Microsoft Windows® NT y Windows 9*x*.
  
Por todo ello, el uso de varias aplicaciones antivirus en el mismo equipo no es una práctica aconsejable y se debe evitar en la medida de lo posible.
  
Un método alternativo consiste en utilizar software antivirus de distintos proveedores para la defensa del cliente, del servidor y de la red de la organización. De este modo, se realiza una comprobación coherente de las distintas zonas de la infraestructura con diferentes motores de comprobación, lo que debe contribuir a reducir el riesgo que correrían todas las defensas antivirus si el producto de un único proveedor no detectase un ataque.
  
Para obtener más información sobre proveedores de antivirus, consulte "Microsoft Antivirus Partners" en Microsoft.com:  
<http://www.microsoft.com/security/partners/antivirus.asp> (en inglés).
  
Para obtener más información sobre software antivirus diseñado para Windows XP, consulte la página de antivirus de "Microsoft Windows Catalog" en Microsoft.com: [http://go.microsoft.com/fwlink/?LinkId=28506](http://go.microsoft.com/fwlink/?linkid=28506) (en inglés).
  
##### Paso 5: Realizar pruebas con un escáner de vulnerabilidades
  
Una vez configurado un sistema, se debe comprobar periódicamente para garantizar que no aparecen puntos débiles para la seguridad. Para ayudarle con este proceso, determinadas aplicaciones actúan de escáner y buscan los puntos débiles de los que software malintencionado e intrusos se pueden intentar aprovechar. La mejor de estas herramientas actualiza las propias rutinas de exploración para defender el sistema contra los puntos débiles más recientes.
  
Microsoft Baseline Security Analyzer (MBSA) supone un ejemplo de escáner de vulnerabilidades, capaz de comprobar los problemas habituales de la configuración de seguridad. Este escáner también garantiza que el host se ha configurado con las actualizaciones de seguridad más recientes.
  
Para obtener más información sobre esta herramienta de configuración gratuita, consulte la página de Microsoft Baseline Security Analyzer V1.2 en TechNet: <http://www.microsoft.com/technet/security/tools/mbsahome.mspx> (en inglés).
  
##### Paso 6: Usar directivas de privilegio mínimo
  
Otra zona de las defensas del cliente que no se debe pasar por alto es la de los privilegios asignados a los usuarios en funcionamiento normal. Microsoft recomienda adoptar una directiva que ofrezca la menor cantidad de privilegios posible, a fin de reducir al mínimo el impacto del software malintencionado que se aprovecha de los privilegios al ejecutarse. Dicha directiva resulta especialmente importante para los usuarios que suelen contar con privilegios administrativos locales. Contemple la posibilidad de quitar esos privilegios para las operaciones diarias y, en su lugar, utilizar el comando **RunAs** para abrir las herramientas de administración pertinentes cuando resulte necesario.
  
Por ejemplo, un usuario que necesita instalar una aplicación que requiere privilegios de administración puede ejecutar el siguiente comando de instalación en el símbolo del sistema para abrir el programa de instalación con los privilegios correspondientes:
  
```  
runas /user:mi\_dominio\\admin "setup.exe"   
```  
También puede obtener acceso directo a esta característica en el Explorador de Windows, mediante los siguientes pasos:
  
**Para ejecutar un programa con privilegios administrativos**
  
1.  En el Explorador de Windows, seleccione el programa o herramienta que desea abrir (como un complemento de Microsoft Management Console (MMC) o el Panel de control).
  
2.  Haga clic con el botón secundario en el programa o herramienta y seleccione **Ejecutar como**.
  
    **Nota**: si **Ejecutar como** no aparece como opción, mantenga presionada la tecla **Mayús** mientras hace clic con el botón secundario en la herramienta.
  
3.  En el cuadro de diálogo **Ejecutar como**, elija la opción **El siguiente usuario:**.
  
4.  En los cuadros **Nombre de usuario** y **Contraseña**, escriba el nombre de usuario y la contraseña para la cuenta de administrador que desea utilizar.
  
##### Paso 7: Restringir aplicaciones no autorizadas
  
Si una aplicación proporciona un servicio a la red, como mensajería instantánea de Microsoft o un servicio Web, en teoría se podría convertir en el objetivo de un ataque de software malintencionado. Como parte de la solución antivirus, se puede plantear producir una lista de aplicaciones autorizadas para la organización. Si se intenta instalar una aplicación no autorizada en cualquiera de los equipos cliente, se podría exponer a éstos y los datos que contienen a un mayor riesgo de software malintencionado.
  
Si la organización desea restringir las aplicaciones no autorizadas, puede utilizar Directiva de grupo de Windows para limitar la capacidad de los usuarios de ejecutar software no autorizado. El uso de Directiva de grupo ya se ha documentado ampliamente y podrá encontrar información detallada sobre el mismo en [Windows Server 2003 Group Policy Technology Center](http://www.microsoft.com/windowsserver2003/technologies/management/grouppolicy/default.mspx) en Microsoft.com:  
www.microsoft.com/windowsserver2003/technologies/management/grouppolicy/ (en inglés).
  
El área específica de Directiva de grupo que trata esta característica se denomina Directiva de restricción de software, a la que se puede obtener acceso a través del complemento estándar Directiva de grupo de la consola de administración de MMC (GPMC). La siguiente ilustración muestra una pantalla GPMC con la ruta en donde puede establecer las directivas de restricción de software para los equipos y usuarios:
  
[![](images/Cc162791.AVFG0303(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0303_big(es-es,technet.10).gif)
  
**Figura 3.3 Ruta a las carpetas de las directivas de restricción de software en el complemento Directiva de grupo de MMC**'
  
Para obtener acceso directo a este complemento desde un cliente con Windows XP, realice los pasos siguientes:
  
1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.
  
2.  Escriba secpol.msc y haga clic en **Aceptar**.
  
Aunque no forma parte de la finalidad principal de esta guía dar una explicación detallada de todas las posibilidades de valores, el artículo "Using Software Restriction Policies to Protect Against Unauthorized Software" en TechNet:  
<http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx> (en inglés) le ofrecerá instrucciones paso a paso sobre el uso de esta eficaz característica del sistema operativo Windows XP Professional.
  
**Advertencia**: Directiva de grupo es una tecnología de extrema eficacia que necesita una configuración cuidadosa, además de conocimientos profundos, para implementarla correctamente. No intente cambiar la configuración directamente si no conoce en profundidad los valores de la directiva y no ha probado los resultados en un sistema no que sea de producción.
  
#### Configuración antivirus en aplicaciones clientes
  
En las siguientes secciones, se ofrecen directrices para configurar determinadas aplicaciones clientes que pueden ser objetivos del software malintencionado.
  
##### Clientes de correo electrónico
  
Si software malintencionado consigue traspasar las defensas antivirus en la red y el servidor de correo electrónico, deben existir algunos valores que se puedan configurar para ofrecer mayor protección al cliente de correo electrónico.
  
Por lo general, la posibilidad que tiene un usuario de abrir directamente documentos adjuntos desde el mensaje de correo electrónico supone una de las principales formas de propagación de software malintencionado en el cliente. Si puede, limite esta capacidad en los sistemas de correo electrónico de la organización. De no ser posible, algunos clientes permiten configurar pasos adicionales que los usuarios deberán realizar antes de abrir un archivo adjunto. Por ejemplo, en Microsoft Outlook® y Outlook Express, se puede realizar lo siguiente:
  
-   Utilizar las zonas de seguridad de Internet Explorer para deshabilitar contenido activo en los mensajes de correo electrónico en HTML.
  
-   Habilitar una opción de forma que los usuarios sólo puedan leer los mensajes en texto.
  
-   Impedir que los programas envíen mensajes de correo electrónico sin especificar la aprobación del usuario.
  
-   Bloquear archivos adjuntos en los mensajes no seguros.
  
Para obtener información sobre la forma de configurar estas características, consulte el artículo de Microsoft Knowledge Base "291387 - OLEXP: Using Virus Protection features in Outlook Express 6" en:  
<http://support.microsoft.com/?kbid=291387>
  
Microsoft Outlook 2003 incluye características adicionales para proteger contra software malintencionado y correo no deseado. Para encontrar información sobre la configuración de estas características, consulte la página "[Customizing Outlook 2003 to Help Prevent Viruses](http://www.microsoft.com/office/ork/2003/three/ch12/default.htm)" en Microsoft.com:  
www.microsoft.com/office/ork/2003/three/ch12/ (en inglés).
  
##### Aplicaciones de escritorio
  
A medida que las aplicaciones de escritorio se consolidan, también se convierten en objetivos del software malintencionado. Los virus de macro utilizan los archivos creados en el procesador de texto, hoja de cálculo u otra aplicación habilitada por macros para replicarse.
  
Siempre que sea posible, debe tomar medidas que aseguren que se ha habilitado la configuración de seguridad más apropiada en todas las aplicaciones del entorno que trabajan con estos archivos. Para obtener información sobre la seguridad de las aplicaciones de Microsoft Office 2003, consulte la página "Best practices for protection from viruses" en Microsoft.com:  
[http://go.microsoft.com/fwlink/?LinkId=28509](http://go.microsoft.com/fwlink/?linkid=28509) (en inglés).
  
##### Aplicaciones de mensajería instantánea
  
El fenómeno de la mensajería instantánea ha servido para mejorar la comunicación entre usuarios de todo el mundo. Por desgracia, también tiene el potencial de permitir que software malintencionado se introduzca en el sistema. Aunque los mensajes de texto no presentan una amenaza directa de software malintencionado, la mayoría de los clientes de mensajería instantánea ofrecen la posibilidad de transferencia de archivos, para mejorar la comunicación entre los usuarios. Al permitir esta transferencia, se presenta ante los posibles ataques por software malintencionado una ruta directa a la red de la organización.
  
Los servidores seguros de la red pueden bloquear este tipo de transferencias de archivos con tan solo filtrar los puertos utilizados para esta comunicación. Por ejemplo, los clientes con Microsoft Windows y MSN® Messenger utilizan un intervalo de puertos TCP entre 6891 y 6900 para la transferencia de archivos, por lo que, si el servidor de seguridad perimetral los bloquea, no se producirá la transferencia de archivos a través de la mensajería instantánea. No obstante, los equipos cliente móviles sólo estarán protegidos mientras se encuentren en la red de la organización. Por todo ello, se aconseja configurar en los clientes el servidor de seguridad basado en host para bloquear estos puertos y proteger los clientes móviles de la organización cuando se encuentren fuera de las defensas de la red.
  
Si la organización no puede bloquear estos puertos porque otras aplicaciones necesarias los requieren o porque la transferencia de archivos es precisa, se debe asegurar de que se comprueban todos los archivos antes la transferencia. Si las estaciones de trabajo clientes no utilizan un escáner antivirus en tiempo real, configure la aplicación de mensajería instantánea para que los archivos transferidos pasen automáticamente a una aplicación antivirus y se comprueben en cuanto se hayan recibido. Por ejemplo, puede configurar MSN Messenger para comprobar automáticamente los archivos transferidos. En los siguientes pasos, se muestra la forma de habilitar esta característica de seguridad:
  
**Nota**: la aplicación Windows Messenger incluida en Windows XP no admite esta característica, por lo que se debe utilizar un escáner antivirus con ella.
  
**Para comprobar archivos transferidos a través de MSN Messenger**
  
1.  En la ventana principal de MSN Messenger, haga clic en el menú **Herramientas** y, a continuación, en **Opciones**.
  
2.  Seleccione la ficha **Mensajes**.
  
3.  En **Transferencia de archivos**, active la casilla de verificación **Examinar los archivos en busca de virus usando:**.
  
4.  Haga clic en **Examinar**, seleccione el software antivirus que esté utilizando y elija **Aceptar**.
  
    **Nota**: para encontrar el archivo ejecutable correcto y el parámetro de comandos que incluir aquí, puede que sea necesario obtener más información del proveedor de software antivirus.
  
Una vez realizados estos pasos, el software antivirus comprobará todos los archivos recibidos a través de MSN Messenger en el cliente.
  
**Nota**: puede que la herramienta de comprobación antivirus que esté utilizando necesite pasos adicionales de configuración. Compruebe las instrucciones del software para obtener más información.
  
##### Exploradores Web
  
Antes de descargar o ejecutar código de Internet, se debe asegurar de que proviene de una fuente conocida y confiable. Los usuarios no pueden confiar únicamente en el aspecto o la dirección del sitio, ya que tanto las páginas como las direcciones Web se pueden falsificar.
  
Existen varias técnicas y tecnologías que se han desarrollado para ayudar al explorador Web de un usuario a determinar la confiabilidad del sitio Web que se están examinando. Por ejemplo, Microsoft Internet Explorer utiliza la tecnología Microsoft Authenticode® para comprobar la identidad del código descargado. Esta tecnología comprueba que el código tiene un certificado válido, que la identidad del fabricante de software coincide con el certificado y que éste sigue siendo válido. Si se superan todas estas pruebas, se habrán reducido las posibilidades de que un atacante haya introducido código malintencionado en el sistema.
  
La mayoría de los principales exploradores Web admiten la posibilidad de restringir el nivel de acceso automatizado disponible a código que se ejecuta desde un servidor Web. Internet Explorer utiliza zonas de seguridad que reducen la posibilidad de que el contenido Web realice operaciones que puedan resultar perjudiciales en el cliente. Estas zonas de seguridad se basan en la ubicación (zona) del contenido Web.
  
Por ejemplo, si confía en que todo lo descargado en la intranet de la organización es seguro, puede establecer la configuración de seguridad de los clientes de la zona de intranet en un nivel bajo, de modo que los usuarios puedan descargar contenido de la intranet con pocas o ninguna restricción. Sin embargo, si el origen de la descarga se encuentra en la zona de Internet o la zona de los sitios restringidos, debe establecer la configuración de seguridad del cliente en un nivel medio o elevado. De este modo, los exploradores de los clientes enviarán al usuario información sobre el certificado del contenido antes de descargarlo o impedirán que lo haga.
  
Para obtener más información sobre temas relacionados con la seguridad, consulte la página "[Internet Explorer Security Center](http://www.microsoft.com/technet/security/prodtech/ie/default.mspx)" en Microsoft.com:  
http://www.microsoft.com/technet/security/prodtech/ie/default.mspx (en inglés).
  
##### Aplicaciones de igual a igual
  
Con la llegada de las aplicaciones de igual a igual (P2P) para Internet, se ha favorecido más que nunca la tarea de encontrar e intercambiar archivos con otros individuos. Por desgracia, esta situación ha llevado a diversos ataques de software malintencionado que intentan utilizar dichas aplicaciones para replicar archivos en los equipos de otros usuarios. Gusanos como W32.HLLW.Sanker han apuntado a las aplicaciones P2P, como Kazaa, para realizar las mencionadas replicaciones. Existen muchos más ejemplos de software malintencionado que intentan utilizar esas aplicaciones, como Morpheus y Grokster.
  
Los problemas de seguridad que afectan a las aplicaciones P2P tienen poco que ver con los propios programas clientes. Por el contrario, guardan más relación con la capacidad de estas aplicaciones de ofrecer rutas directas de un equipo a otro a través de las cuales se puede transmitir contenido sin las comprobaciones de seguridad correspondientes.
  
En la medida de lo posible, Microsoft recomienda limitar la cantidad de clientes de la organización que utilizan estas aplicaciones. Se pueden utilizar las directivas de restricción de software de Windows tratadas anteriormente en este capítulo para bloquear a los usuarios que las utilicen. De no ser posible en el entorno, asegúrese de que las directivas antivirus tienen en cuenta que los clientes corren mayor riesgo debido a estas aplicaciones.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Defensas del servidor
  
Las defensas del servidor en el entorno tienen mucho en común con las defensas del cliente: ambas intentan proteger el mismo entorno del equipo básico. La diferencia principal entre ellas radica en que, por lo general, hay expectativas mucho mayores puestas en las defensas del servidor, en cuanto a confiabilidad y rendimiento. Además, las funciones dedicadas que muchos servidores realizan en la infraestructura de una organización a menudo conducirán a una solución de defensa especializada. La información de las siguientes secciones se centra en las principales diferencias entre las defensas del servidor y las defensas del cliente anteriormente mencionadas.
  
#### Pasos de protección antivirus del servidor
  
Las configuraciones antivirus del servidor varían en gran medida, según la función del servidor concreto y los servicios que, según su diseño, debe ofrecer. El proceso de minimizar el ámbito de ataque de un servidor se denomina a veces *consolidación*. Hay excelentes instrucciones disponibles sobre la consolidación de Windows Server 2003 cuando se utiliza con varias funciones habituales en una organización. Para obtener más información sobre este tema, consulte la página "Server Security Index" en Microsoft.com:  
[http://www.microsoft.com/security/guidance/topics/ServerSecurity.mspx](http://technet.microsoft.com/es-es/security/bb977553.aspx) (en inglés).
  
Entre los pasos para defender los servidores en la organización, cuatro de los básicos son los mismos que para los clientes.
  
1.  **Reducir el ámbito de ataque**. Elimine servicios y aplicaciones no deseados de los servidores para minimizar el ámbito de ataque.
  
2.  **Aplicar actualizaciones de seguridad**. Asegúrese de que todos los equipos servidores ejecutan las actualizaciones de seguridad más recientes, si es posible. Lleve a cabo las pruebas adicionales que sean necesarias para garantizar que los servidores que realizan misiones críticas no se ven perjudicados por las nuevas actualizaciones.
  
3.  **Habilitar el servidor de seguridad basado en host**. Windows Server 2003 incluye un servidor de seguridad basado en host que se puede utilizar para reducir el ámbito de ataque en los servidores, así como para quitar servicios y aplicaciones no deseados.
  
4.  **Realizar pruebas con escáneres de vulnerabilidades**. Utilice MBSA en Windows Server 2003 para identificar las posibles vulnerabilidades en la configuración de un servidor. Microsoft recomienda utilizar ésta y otras comprobaciones de vulnerabilidades especializadas para garantizar una configuración lo más sólida posible.
  
Además de estos pasos antivirus habituales, puede utilizar el siguiente software específico de servidor como parte de las defensas antivirus generales del servidor.
  
##### Software antivirus general para el servidor
  
La diferencia principal entre las aplicaciones antivirus diseñadas para los entornos clientes (como Windows XP) y las diseñadas para los servidores (como Windows Server 2003) ha sido el nivel de integración entre el escáner basado en servidor y cualquier servicio basado en servidor, como los servicios de mensajería de bases de datos. Gran cantidad de aplicaciones antivirus basadas en el servidor también ofrecen capacidad de administración remota para minimizar la necesidad de acceso físico a la consola de éste.
  
Entre los demás asuntos importantes que se deben tener en cuenta al evaluar software antivirus para el entorno de servidores se incluyen:
  
-   **Utilización de la CPU durante la comprobación**. En un entorno de servidor, el uso de la CPU representa un componente crítico de la capacidad del servidor de realizar su función principal para la organización.
  
-   **Confiabilidad de la aplicación**. Un bloqueo del sistema en un importante servidor de centro de datos causa un impacto mucho mayor que el bloqueo de una única estación de trabajo. Por tanto, Microsoft recomienda probar exhaustivamente todas las aplicaciones antivirus basadas en servidor para garantizar la confiabilidad del sistema.
  
-   **Carga de la administración**. La capacidad de la aplicación antivirus de administrarse a sí misma puede servir para reducir la carga administrativa de los equipos de administración del servidor en la organización.
  
-   **Interoperabilidad de la aplicación**. Se debe probar la aplicación antivirus con los mismos servicios y las mismas aplicaciones basados en el servidor que el servidor de producción ejecutará para asegurar que no se producen problemas de interoperabilidad.
  
##### Software y configuraciones antivirus específicos de la función
  
Actualmente hay aplicaciones, herramientas y configuraciones antivirus especializadas disponibles para funciones específicas del servidor de la empresa. Entre los ejemplos de funciones del servidor que pueden sacar provecho de este tipo de defensa antivirus especializada se incluyen:
  
-   **Servidores Web**, como Servicios de Internet Information Server (IIS) de Microsoft.
  
-   **Servidores de mensajería**, como Microsoft Exchange 2003.
  
-   **Servidores de bases de datos**, como los que ejecutan Microsoft SQL Server™ 2000.
  
-   **Servidores de colaboración**, como los que ejecutan Microsoft Windows SharePoint™ Services y Microsoft Office SharePoint Portal Server™ 2003.
  
Las soluciones antivirus específicas de la aplicación ofrecen mayor protección y rendimiento puesto que se han diseñado para integrarse con un servicio concreto en lugar de intentar funcionar de forma subyacente al servicio en el nivel del sistema de archivos. Todas las funciones de servidor abordadas en esta sección son responsables de la información que no sería accesible a un escáner antivirus que funcione en el nivel del sistema de archivos. También se facilita información sobre cada una de dichas funciones del servidor y sobre cómo Microsoft recomienda utilizar aplicaciones, herramientas y configuraciones antivirus específicas con ellas.
  
##### Servidores Web
  
Los servidores Web de todo los tipos de organización han sido objetivo de ataques de seguridad durante cierto tiempo. Independientemente de que un ataque provenga de software malintencionado como CodeRed o un intruso que intenta dañar el sitio Web de una organización, resulta importante que la configuración de seguridad en los servidores Web se configuren lo bastante para maximizar las defensas contra dichos ataques. Microsoft ha elaborado instrucciones específicas para los administradores de sistemas responsables de proteger los servidores con IIS en la red en "Chapter 8 - Hardening IIS Servers" de *Windows Server 2003 Security Guide* en Microsoft.com:  
<http://www.microsoft.com/technet/security/prodtech/win2003/w2003hg/sgch08.mspx> (en inglés).
  
Además de estas instrucciones, existen algunas herramientas gratuitas que se pueden descargar y que realizarán automáticamente algunas configuraciones de seguridad en IIS. Por ejemplo, la herramienta IIS Lockdown Tool se encuentra disponible en Microsoft.com:  
<http://www.microsoft.com/technet/security/tools/locktool.mspx> (en inglés).
  
Esta herramienta se utiliza para ajustar el servidor Web de modo que ofrezca sólo los servicios inherentes a su función y reduciendo, por tanto, el ámbito de ataque del servidor ante cualquier software malintencionado.
  
UrlScan es otra herramienta de seguridad que limita los tipos de solicitudes HTTP que IIS procesará. De este modo, UrlScan impide que solicitudes potencialmente perjudiciales lleguen al servidor. Ya puede instalar fácilmente UrlScan 2.5 en los servidores con IIS 4.0 o posterior. Para obtener más información sobre UrlScan, consulte la página "UrlScan Security Tool" en Microsoft.com:  
<http://www.microsoft.com/technet/security/tools/urlscan.mspx> (en inglés).
  
###### Servidores de mensajería
  
Hay dos objetivos que se deben tener en cuenta al diseñar una solución antivirus eficaz para los servidores de correo electrónico en la organización. El primero consiste en proteger los propios servidores de software malintencionado. El segundo consiste en impedir que cualquier software malintencionado se introduzca en el sistema de correo electrónico hasta los buzones de los usuarios en la organización. Resulta fundamental garantizar que la solución antivirus instalada en los servidores de correo pueda lograr ambos objetivos.
  
En términos generales, las soluciones antivirus de comprobación de archivos no pueden evitar que un servidor de correo envíe software malintencionado a los clientes en forma de archivo adjunto. Hasta los servicios de correo electrónico más sencillos almacenan los mensajes en una base de datos de algún tipo, lo que se conoce algunas veces como el *almacén de mensajes*. Una solución antivirus de comprobación de archivos habitual no puede obtener acceso al contenido de tal base de datos. De hecho, este tipo de solución podría dañar un almacén de mensajes si tuviese permiso para intentar realizar comprobaciones a través de una asignación de unidades (como la unidad M: en Exchange Server 5.5 y Exchange Server 2000).
  
Resulta importante que la solución antivirus corresponda con la solución de correo electrónico actual. Gran cantidad de proveedores de software antivirus ya ofrecen versiones dedicadas para servidores de correo específicos y que se han diseñado para comprobar la existencia de software malintencionado en los mensajes que entran en el sistema de correo. En general, existen dos tipos básicos de soluciones antivirus para correo electrónico:
  
-   **Escáneres de puerta de enlace SMTP**. Estas soluciones de comprobación de correo basadas en el protocolo simple de transferencia de correo (SMTP) se suelen conocer como soluciones antivirus de "puerta de enlace". Tienen la ventaja de que trabajan con todos los servicios de correo electrónico SMTP, en lugar de estar vinculado a un producto de servidor de correo concreto. Sin embargo, estas soluciones están limitadas en algunas de las características más avanzadas que pueden ofrecer, debido a su dependencia del protocolo de correo SMTP.
  
-   **Escáneres de servidor integrados**. Estas aplicaciones antivirus especializadas funcionan directamente con un producto de servidor de correo concreto. Aportan varias ventajas. Por ejemplo, se pueden integrar directamente con funciones avanzadas del servidor, ya que se han diseñado para utilizar el mismo hardware que el servidor de correo.
  
Microsoft Exchange proporciona una interfaz de programación de aplicaciones (API) antivirus específica denominada API de virus (VAPI), a la que también se conoce como API antivirus (AVAPI) o API de comprobación de virus (VSAPI). Aplicaciones antivirus especializadas de Exchange Server utilizan esta API para ofrecer protección total de los mensajes de forma segura y confiable en servidores de correo Exchange. Para obtener más información sobre esta API, consulte el artículo de Microsoft Knowledge Base "328841 – XADM: Exchange and Antivirus Software" en Microsoft.com:  
<http://support.microsoft.com/?kbid=328841>
  
###### Servidores de bases de datos
  
Al considerar las defensas antivirus de un servidor de bases de datos, hay cuatro elementos principales que se deben proteger:
  
-   **Host**. El servidor o servidores que ejecutan la base de datos.
  
-   **Servicios de bases de datos**. Las distintas aplicaciones del host que proporcionan el servicio de base de datos en la red.
  
-   **Almacén de datos**. La información almacenada en la base de datos.
  
-   **Comunicación de datos**. Las conexiones y los protocolos que se utilizan entre el host de la base de datos y los demás hosts en la red.
  
Puesto que la información incluida en el almacén de datos no se puede ejecutar, se suele pensar que no es necesario comprobar los almacenes de datos. Actualmente, no existen aplicaciones antivirus importantes diseñadas especialmente para los almacenes de datos. No obstante, se deben tener en cuenta al host, los servicios de bases de datos y la comunicación de datos en el servidor de bases de datos para las configuraciones antivirus.
  
Se deben revisar la ubicación y configuración del host contra amenazas de software malintencionado. Como norma general, Microsoft no recomienda ubicar los servidores de bases de datos en la red perimetral de la infraestructura de una organización, especialmente si los servidores almacenan información confidencial. Pero si es necesario ubicarlo en la red perimetral, asegúrese de que el servidor de bases de datos se ha configurado para reducir al mínimo el riesgo de una infección por software malintencionado.
  
Si su organización utiliza SQL Server, consulte las siguientes instrucciones para obtener más información sobre las directrices específicas de configuración de ataques por software malintencionado:
  
-   El artículo de Microsoft Knowledge Base "309422 – INF: Consideration for a Virus Scanner On a Computer That Is Running SQL Server" en Microsoft.com:  
    <http://support.microsoft.com/?kbid=309422>
  
-   La página "[Security Resources](http://www.microsoft.com/sqlserver/2005/en/us/security.aspx)" de Microsoft SQL Server en Microsoft.com:  
    www.microsoft.com/sql/techinfo/administration/2000/security/ (en inglés).
  
El reciente ataque del gusano "Slammer" apuntó directamente a SQL Server. Este ataque demostró la importancia de proteger los equipos con bases de datos SQL Server, independientemente de si residen en la red interna o perimetral.
  
Para obtener información y software que le garantice que los sistemas SQL Server están protegidos contra el gusano Slammer, consulte la página "Finding and Fixing Slammer Vulnerabilities" en Microsoft.com:  
[http://www.microsoft.com/security/incident/slammer.mspx](http://www.microsoft.com/spain/technet/seguridad/herramientas/msrtool.mspx) (en inglés).
  
###### Servidores de colaboración
  
La misma naturaleza de los servidores de colaboración los convierte en vulnerables a software malintencionado. Cuando los usuarios copian archivos a y desde los servidores, pueden dejar expuestos a los servidores y otros usuarios de la red ante un ataque de software malintencionado. Microsoft recomienda proteger los servidores de colaboración del entorno (como los que ejecutan SharePoint Services y SharePoint Portal Server 2003) con una aplicación antivirus que pueda comprobar todos los archivos copiados a y desde el almacén de colaboración. Para obtener información paso a paso detallada sobre la protección de estos servicios, consulte la página "Configuring Antivirus Protection" de *Administrators Guide for Windows SharePoint Services* en Microsoft.com:  
<http://www.microsoft.com/resources/documentation/wss/2/all/adminguide/en-us/stse11.mspx> (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### La capa de defensa de la red
  
Los ataques que tienen lugar a través de la red representan el mayor número de incidencias registradas de software malintencionado. Normalmente, los ataques de este tipo de software comenzarán por aprovechar los puntos débiles en las defensas del perímetro de la red a fin de tener acceso a los dispositivos host dentro de la infraestructura de TI de la organización. Estos dispositivos podrían ser clientes, servidores, enrutadores o incluso servidores de seguridad. Uno de los problemas más difíciles a los que se enfrentan las defensas antivirus en esta capa consiste en buscar el equilibrio entre los requisitos de características de los usuarios de los sistemas de TI y las limitaciones necesarias para establecer una defensa eficaz. Por ejemplo, al igual que numerosos ataques recientes, el gusano MyDoom utilizaba un archivo adjunto de correo electrónico para replicarse. Desde la perspectiva de la infraestructura de TI, la opción más sencilla y segura consiste en bloquear todos los archivos adjuntos entrantes. Sin embargo, puede que los requisitos de los usuarios de correo electrónico de su organización no permitan que sea una opción viable. Por tanto, es necesario llegar a un compromiso que consiga un equilibrio entre los requisitos de la organización y el nivel de riesgo que ésta puede aceptar.
  
Muchas organizaciones han adoptado un enfoque multicapa en relación al diseño de sus redes que utiliza tanto estructuras de red interna como externa. Microsoft recomienda este método porque se adapta directamente al modelo de seguridad de defensa en profundidad.
  
**Nota**: hay una tendencia creciente a dividir la red interna en zonas de seguridad para establecer un perímetro en cada una de ellas. Microsoft recomienda también este enfoque, ya que ayuda a reducir la exposición general a un ataque de software malintencionado que busca obtener acceso a la red interna. Sin embargo, en relación a la finalidad de esta guía, sólo se describe la defensa de una única red. Si tiene pensado utilizar un perímetro y varias redes internas, puede aplicar esta instrucción directamente a cada una.
  
Las primeras defensas de la red de la organización se denominan defensas de la red perimetral. Se han diseñado para evitar que se introduzca software malintencionado en la organización a partir de un ataque externo. Como se ha mencionado anteriormente en este capítulo, un ataque normal de software malintencionado se centra en copiar archivos en un equipo de destino. Por tanto, las defensas antivirus deben trabajar en combinación con las medidas de seguridad generales de la organización para garantizar que el acceso a los datos de la empresa sólo se permite a personal autorizado y de forma segura (por ejemplo, a través de una conexión de red privada virtual (VPN) cifrada). Para obtener más información sobre la creación de un diseño de red perimetral seguro, consulte las instrucciones de Microsoft Systems Architecture 2.0 en TechNet:  
<http://www.microsoft.com/resources/documentation/msa/2/all/solution/en-us/default.mspx> (en inglés).
  
**Nota**: también se pueden tener en cuenta todas las redes de área local (LAN) inalámbricas y VPN como redes perimetrales. Si su organización cuenta con estas tecnologías, es importante garantizar su seguridad. Si no lo hace, podría permitir el acceso directo de un intruso a la red interna (saltándose las defensas perimetrales estándar) para provocar un ataque.
  
Para obtener más información sobre la seguridad de las redes WLAN, consulte los siguientes artículos en TechNet:
  
-   "Planning a Secure Wireless LAN using Windows Server 2003 Certificate Services" en:  
    [http://www.microsoft.com/technet/security/guidance/secmod167.mspx](http://technet.microsoft.com/es-es/security/bb977553.aspx) (en inglés).
  
-   "Securing Wireless LANs - A Windows Server 2003 Certificate Services Solution" en:  
    <http://www.microsoft.com/technet/security/prodtech/win2003/pkiwire/swlan.mspx> (en inglés).
  
Para obtener instrucciones sobre la seguridad de las redes VPN, consulte el siguiente artículo en Microsoft.com:
  
-   "MSA Enterprise Design for Remote Access" en:  
    <http://www.microsoft.com/resources/documentation/msa/2/all/solution/en-us/msa20rak/vmhtm128.mspx> (en inglés).
  
En esta guía, se asume que el diseño de seguridad de la red proporciona a la organización el nivel de identificación, autorización, cifrado y protección necesario para defenderse contra la intrusión directa de un atacante no autorizado. Sin embargo, en este punto las defensas antivirus no están completas. El siguiente paso consiste en configurar las defensas de las capas de la red a fin de detectar y filtrar los ataques de software malintencionado que utilizan las comunicaciones de red permitidas, como el correo electrónico, la exploración Web y la mensajería instantánea.
  
#### Configuración antivirus de la red
  
Existen varias configuraciones y tecnologías que están diseñadas específicamente para proporcionar seguridad de red a las organizaciones. Aunque se trata de partes esenciales en el diseño de seguridad de una organización, esta sección sólo se centrará en las áreas que tienen relación directa con la defensa antivirus. Los equipos que se ocupan del diseño y de la seguridad de la red deberán determinar cómo se utilizarán cada una de las siguientes técnicas en su organización.
  
##### Sistema de detección de intrusos en la red
  
Debido a que la red perimetral constituye una parte altamente expuesta, resulta de vital importancia que los sistemas de administración de la red puedan detectar e informar lo antes posible de un ataque. La función que cumple el sistema de detección de intrusos en la red (NID) es básicamente esa: permitir un proceso rápido de detección e información de ataques externos. Aunque el sistema NID forma parte del diseño de seguridad del sistema general y no de una herramienta antivirus concreta, muchos de los primeros signos son comunes tanto a los ataques del software malintencionado como al sistema. Por ejemplo, algunos tipos de software malintencionado utilizan la exploración de IP para encontrar sistemas que puedan infectar. Por este motivo, el sistema NID se debe configurar para que funcione con los sistemas de administración de la red de la organización a fin de enviar advertencias directamente al personal de seguridad de la misma ante cualquier comportamiento extraño.
  
Un aspecto clave es que con cualquier implementación de NID, la efectividad de su protección es comparable al proceso que se sigue una vez que se detecta una intrusión. Este proceso debe activar defensas, controladas constantemente en tiempo real, que se puedan utilizar para bloquear un ataque. Sólo entonces se puede considerar el proceso como parte de una estrategia de defensa. Si no es así, el sistema NID es más bien una herramienta que proporciona una pista de auditoría después de que se produce un ataque.
  
Hay distintos sistemas de detección de intrusos en la red de clase empresarial disponibles para los diseñadores de redes. Pueden ser dispositivos independientes u otros sistemas que se integran en otros servicios de red, como los servicios de servidor de seguridad de la organización. Por ejemplo, los productos Microsoft Internet Security and Acceleration (ISA) Server 2000 y 2004 contienen capacidades NID, así como servicios de proxy y servidores de seguridad.
  
Para obtener una lista de los socios de Microsoft ISA Server que ofrecen servicios NID adicionales para ISA Server, consulte la página "Intrusion Detection" en Microsoft.com:  
[http://www.microsoft.com/isaserver/partners/intrusiondetection.asp](http://www.microsoft.com/forefront/edgesecurity/isaserver/en/us/isa-solution-partners.aspx) (en inglés).
  
##### Filtrado de aplicaciones
  
Las organizaciones encuentran no sólo útiles sino también necesarias las tecnologías de filtrado de Internet para supervisar y examinar las comunicaciones de la red en busca de contenido no legítimo, por ejemplo, virus. Tradicionalmente se ha realizado utilizando el filtrado de paquetes que proporcionan los servicios del servidor de seguridad, que sólo permite filtrar el tráfico de la red según una dirección IP de origen o destino o de un puerto de red TCP o UDP específico. El filtrado de aplicaciones (ALF) funciona a nivel de la capa de aplicaciones del modelo de redes OSI, por lo que permite que se examinen y se filtren los datos según su contenido. Si se utiliza ALF además del filtrado de la capa de paquetes estándar, se puede lograr una mayor seguridad. Por ejemplo, el uso del filtrado de paquetes permite filtrar el tráfico de red del puerto 80 a través del servidor de seguridad de la organización para que sólo pueda pasar a sus servidores Web. Sin embargo, este método puede que no aporte suficiente seguridad. Agregar ALF a la solución le permitiría comprobar todos los datos que pasan a los servidores Web en el puerto 80 para asegurarse de que son válidos y no contienen código sospechoso.
  
ISA Server puede proporcionar ALF en los paquetes de datos cuando pasan por un servidor de seguridad de la organización. La exploración Web y el correo electrónico se pueden analizar para garantizar que determinado contenido no incluye datos sospechosos, como correo no deseado o software malintencionado. La capacidad ALF en ISA Server posibilita un análisis en profundidad del contenido que incluye la detección, la inspección y la validación del tráfico con cualquier puerto o protocolo. Para obtener una lista de proveedores que fabrican filtros que mejoran la seguridad y la interoperabilidad de distintos protocolos y tráfico Web, consulte la página "Partner Application Filters" en Microsoft.com:  
[http://www.microsoft.com/isaserver/partners/applicationfilters.asp](http://www.microsoft.com/forefront/edgesecurity/isaserver/en/us/isa-solution-partners.aspx) (en inglés).
  
Para obtener una descripción detallada de cómo funciona ALF en ISA Server 2000, consulte la página "Introducing the ISA Server 2000 Application Layer Filtering Kit" en:  
[www.isaserver.org/articles/spamalfkit.html](http://www.isaserver.org/articles/spamalfkit.html) (en inglés).
  
##### Exploración de contenido
  
La exploración de contenido se encuentra disponible como característica en soluciones más avanzadas de servidores de seguridad o como un componente de un servicio independiente, por ejemplo, el correo electrónico. La exploración de contenido analiza los datos que tienen permiso para entrar o salir de la red de la organización a través de los canales de datos válidos. Si se realiza en el correo electrónico, generalmente funciona con los servidores de correo electrónico para comprobar determinadas características del correo, como los archivos adjuntos. Esta técnica puede explorar e identificar contenido de software malintencionado en tiempo real a medida que los datos pasan a través del servicio. Microsoft colabora con distintos socios para ofrecer características de seguridad mejoradas, como la exploración de contenido antivirus en tiempo real, para Microsoft Exchange Server e ISA Server.
  
Para obtener más detalles sobre los productos antivirus de nuestros socios disponibles para Microsoft Exchange Server 2003, consulte el artículo de Microsoft Knowledge Base, "823166 "Overview of Exchange Server 2003 and Antivirus Software" en Microsoft.com:  
<http://support.microsoft.com/?kbid=823166> (en inglés).
  
Para obtener una lista de los socios de Microsoft que han desarrollado productos de exploración de contenido para ISA Server, consulte la página "Partners" en Microsoft.com:  
<http://www.microsoft.com/isaserver/partners/> (en inglés).
  
##### Filtrado de URL
  
Otra opción disponible para los administradores de redes es el filtrado de URL, que se puede utilizar para bloquear sitios Web problemáticos. Por ejemplo, podría utilizar el filtrado de URL para bloquear sitios Web, servidores de descarga y servicios de correo electrónico HTTP personales de intrusos conocidos.
  
**Nota**: los principales sitios de servicios de correo electrónico HTTP (como Hotmail y Yahoo) ofrecen servicios de exploración antivirus, pero existen muchos otros sitios más pequeños que no disponen de esta característica. Este es un grave inconveniente para las defensas de una organización, ya que dichos servicios proporcionan una ruta directa desde Internet a los clientes.
  
Los administradores de red pueden adoptar dos enfoques básicos para el filtrado de URL:
  
-   **Listas de bloqueados**. El servidor de seguridad comprueba una lista predefinida de sitios problemáticos antes de permitir la conexión. Sólo se permite a los usuarios conectarse con sitios que no están en dicha lista.
  
-   **Listas de admitidos**. Este método sólo permite comunicaciones con sitios incluidos en una lista predefinida de sitios Web que han sido aprobados por la organización.
  
El primer enfoque se basa en un proceso activo de identificación de sitios Web que puedan resultar problemáticos y su posterior incorporación a la lista. Debido al tamaño y naturaleza variable de Internet, este método exige una solución automatizada o una carga de administración significativa, y normalmente resulta útil solamente para bloquear un pequeño número de sitios problemáticos conocidos en lugar de aportar una solución de protección general. El segundo enfoque proporciona una mayor protección debido a que su naturaleza restrictiva permite controlar los sitios disponibles para los usuarios del sistema. Sin embargo, a menos que se lleve a cabo una investigación adecuada que identifique todos los sitios que solicitan los usuarios, puede resultar demasiado restrictivo para muchas organizaciones.
  
Microsoft ISA Server admite la creación manual de ambas listas a través de sus reglas de contenido y de sitios. No obstante, existen soluciones mejoradas y automatizadas de los socios de Microsoft que trabajan directamente con ISA Server para garantizar que las direcciones URL se pueden bloquear o autorizar según sea necesario con un mínimo de carga de administración. Una lista de estas soluciones se encuentra disponible en la página "Microsoft Internet Security and Acceleration (ISA) Server Partners URL Filtering" en Microsoft.com:  
[http://www.microsoft.com/isaserver/partners/accesscontrol.asp](http://www.microsoft.com/forefront/edgesecurity/isaserver/en/us/isa-solution-partners.aspx) (en inglés).
  
Ambos enfoques sólo proporcionan protección mientras el cliente está dentro de las defensas de la organización. No está disponible cuando un cliente móvil se conecta directamente a Internet mientras está fuera de la oficina, lo que significa que la red será susceptible de un posible ataque. Si precisa una solución de filtrado de URL para los clientes móviles de su organización, debe considerar el uso de un sistema de defensa basado en clientes. Sin embargo, este enfoque puede suponer una carga de administración importante, especialmente en entornos con un gran número de clientes móviles.
  
##### Redes de cuarentena
  
Otra técnica que puede utilizar para asegurar redes es la de establecer una red de cuarentena para equipos que no cumplan los requisitos de seguridad mínimos de su organización.
  
**Nota**: esta técnica no se debe confundir con la característica de cuarentena disponible en algunas aplicaciones antivirus, que mueve un archivo infectado a un área segura del equipo hasta que se pueda limpiar.
  
Una red de cuarentena debe restringir, o incluso bloquear, el acceso interno a los recursos de la organización, pero proporcionar al mismo tiempo un nivel de conectividad (en el que se incluya Internet) que permita a los equipos de visitantes temporales trabajar de forma productiva sin poner en riesgo la seguridad de la red interna. Si el equipo portátil de un visitante está infectado con software malintencionado y se conecta a la red, su capacidad de infectar los demás equipos de la red interna se verá restringida por la red de cuarentena.
  
Un método similar a éste lleva aplicándose con éxito desde hace algún tiempo a las conexiones remotas del tipo VPN. Los clientes de VPN son desviados a una red de cuarentena temporal mientras se realizan las pruebas del sistema. Si el cliente pasa las pruebas, por ejemplo porque dispone de las actualizaciones de seguridad y los archivos de firmas antivirus necesarios, se le concede acceso a la red interna de la organización. Si, por el contrario, el cliente no cumple estos requisitos, se lo desconectará o se permitirá el acceso a la red de cuarentena, que se puede utilizar para obtener las actualizaciones necesarias para pasar las pruebas. Los diseñadores de redes están estudiando esta tecnología para ayudar a mejorar la seguridad en las redes internas.
  
Para obtener más información sobre esta técnica, consulte la página "Planning for Network Access Quarantine Control" del *kit de implementación de Microsoft Windows Server 2003* en Microsoft.com:  
<http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbf_vpn_aosh.asp> (en inglés).
  
##### ISA Server Feature Pack
  
Si su organización utiliza ISA Server 2000, Microsoft recomienda que lo complemente con las características adicionales que se proporcionan en ISA Server Feature Pack 1. Este complemento gratuito proporciona características de seguridad que podrá utilizar para mejorar la seguridad de las comunicaciones (incluido el correo electrónico) a través de los servidores de seguridad en las defensas de su organización. Entre las características que puede emplear para mejorar las defensas antivirus de la red se incluyen:
  
-   **Un** **filtro SMTP mejorado**. Esta característica ayuda a filtrar mensajes de correo electrónico con un mayor grado de confiabilidad y seguridad. El filtrado se basa en el nombre, el tamaño o la extensión de un archivo adjunto, así como en el remitente, dominio, palabra clave y cualquier comando SMTP y su longitud.
  
-   **Un** **filtro mejorado de llamadas a procedimientos remotos (RPC) de Exchange**. Esta característica protege la comunicación del correo electrónico de Outlook con los equipos Exchange Server en redes que no son de confianza sin que sea necesario configurar una red privada virtual (VPN). Para lograrlo, también se incluyen en ISA Server Feature Pack 1 las siguientes características:
  
    -   Capacidad para que los administradores puedan aplicar el cifrado de RPC entre Outlook y Exchange Server.
  
    -   Capacidad para que la comunicación RPC saliente pase de forma segura a través de ISA Server que, a su vez, permite a los clientes de Outlook conectarse a un equipo ISA Server para tener acceso a equipos Exchange Server externos.
  
-   **UrlScan 2.5**. Esta herramienta ayuda a detener solicitudes Web malintencionadas en el equipo ISA Server antes de que puedan entrar en la red y tener acceso a un servidor Web.
  
-   **Asistente de Outlook Web Access (OWA)**. Puede utilizar este asistente para configurar ISA Server de forma fácil y rápida para proteger una implementación de OWA.
  
-   **Asistente de configuración del filtro de RPC**. Puede utilizar este asistente para permitir solamente un nivel preciso de acceso a los servicios de RPC de la red interna en lugar de todo el tráfico de RPC.
  
Para obtener el paquete de características, consulte la página "How to Obtain Feature Pack 1" en Microsoft.com:  
[http://www.microsoft.com/isaserver/featurepack1/howtogetfp1.asp](http://www.microsoft.com/forefront/edgesecurity/isaserver/en/us/isa-solution-partners.aspx) (en inglés).
  
Para obtener más información sobre el uso de estas características a fin de asegurar un servidor de seguridad ISA Server perimetral, consulte la página "ISA Server Feature Pack 1" en Microsoft.com:  
<http://www.microsoft.com/isaserver/featurepack1/> (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Seguridad física
  
Aunque la seguridad física es más un problema de seguridad general que un problema específico de software malintencionado, es imposible protegerse contra este tipo de software sin contar con un plan de defensa física eficaz para todos los clientes, servidores y dispositivos de red de la infraestructura de la organización. Algunos de los elementos esenciales en un plan eficaz de defensa física son los siguientes:
  
-   Seguridad del edificio
  
-   Seguridad del personal
  
-   Puntos de acceso a la red
  
-   Servidores
  
-   Estaciones de trabajo
  
-   Equipos y dispositivos móviles
  
Se deben considerar cada uno de estos elementos en una evaluación de los riesgos de seguridad de la organización. Si un atacante pone en peligro cualquiera de ellos, existe un mayor riesgo de que el software malintencionado pueda saltarse las defensas de las redes interna y externa para infectar un host.
  
El acceso protegido a sus instalaciones y sistemas informáticos debe constituir un elemento fundamental en la estrategia de seguridad general. La explicación detallada de estas consideraciones no entra dentro del ámbito de esta guía. Sin embargo, hay disponible información sobre los elementos básicos de un plan de seguridad física en el artículo "5-Minute Security Advisor - Basic Physical Security" en Microsoft TechNet:  
<http://www.microsoft.com/technet/community/columns/5min/5min-203.mspx> (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directivas, procedimientos y concienciación
  
Las directivas y procedimientos operativos de redes, clientes y servidores constituyen aspectos esenciales de las capas de defensa antivirus de la organización. Microsoft recomienda que considere las siguientes directivas y procedimientos como parte de la solución de defensa en profundidad antivirus:
  
-   **Rutinas de comprobación antivirus**. Lo ideal es que la aplicación antivirus que utilice permita exploraciones automatizadas o en tiempo real. Sin embargo, si no es el caso, debe implementar un proceso que proporcione instrucciones a los usuarios de su organización sobre el momento preciso en el que deben realizar una exploración completa del sistema.
  
-   **Rutinas de actualización de firmas de antivirus**. Prácticamente todas las aplicaciones antivirus actuales incluyen un método automatizado para la descarga de actualizaciones de firmas de virus, que se recomienda que implemente de forma regular. Sin embargo, si en su organización se ha establecido que se prueben estas actualizaciones antes de implementarlas, no podrá utilizar normalmente este sistema. En este caso, asegúrese de que el personal de soporte técnico identifica, descarga, prueba y actualiza lo antes posible los archivos de firmas.
  
-   **Directivas sobre aplicaciones y servicios autorizados**. Debe existir una directiva claramente especificada que determine qué aplicaciones se permiten en los equipos de su organización y en los que tengan acceso a los recursos de la misma. Entre los ejemplos de aplicaciones que pueden causar problemas se incluyen aplicaciones de redes de igual a igual y aplicaciones que los usuarios pueden descargar directamente de sitios Web malintencionados.
  
Como mínimo, Microsoft recomienda las siguientes directivas y procedimientos para todos los dispositivos de la capa de defensa de la red de su organización.
  
-   **Control de cambios**. Un proceso de seguridad clave para los dispositivos de red es controlar los cambios que les pueden afectar. Lo ideal es que todos los cambios se propongan, prueben e implementen de una forma documentada y controlada. Es probable que los cambios espontáneos en los dispositivos de la red perimetral introduzcan errores o problemas de configuración de los que un ataque podría sacar provecho.
  
-   **Supervisión** **de la red**. La configuración correcta de los dispositivos de red a fin de optimizarlos para la seguridad no significa que deban dejarse de lado los demás procedimientos antivirus. La supervisión continua de todos los dispositivos de la red resulta esencial para detectar lo antes posible ataques de software malintencionado. Esta supervisión constituye un proceso complejo que requiere reunir información de una serie de fuentes (como servidores de seguridad, enrutadores y conmutadores) para compilar una línea de base de comportamiento "normal" que se pueda utilizar para identificar el comportamiento anormal.
  
-   **Proceso de detección de ataques**. Si se detecta un ataque de software malintencionado, su organización debe disponer del conjunto de pasos bien documentados y definidos que se deberán seguir para garantizar que se confirma, controla y limpia el ataque con el mínimo trastorno para los usuarios finales. Consulte el capítulo 4, "Control y recuperación de los ataques de virus", para obtener más información sobre este tema.
  
-   **Directiva de acceso a redes de equipos domésticos**. Se deben establecer y cumplir una serie de requisitos mínimos antes de que un empleado pueda conectar una red o equipo doméstico a la red de su organización a través de una conexión de VPN.
  
-   **Directiva de acceso a redes de visitantes**. Se deben establecer y cumplir una serie de requisitos mínimos por parte de los visitantes antes de que se les permita conectarse a la red de su organización. Estos requisitos se deben aplicar tanto a la conectividad inalámbrica como a la normal.
  
-   **Directiva de redes inalámbricas**. Todos los dispositivos inalámbricos que se conecten a la red interna deben cumplir los requisitos mínimos de seguridad para que se puedan conectar. Esta directiva debe especificar la configuración mínima necesaria para la organización.
  
Existen muchas más directivas y procedimientos que podría implementar para mejorar la seguridad de los dispositivos de red; los que se mencionan en esta sección son un punto de partida. Sin embargo, puesto que las directivas adicionales proporcionan configuraciones de seguridad generales en lugar de específicas contra virus, quedan fuera del ámbito de esta guía.
  
#### Directiva de actualizaciones de seguridad
  
Debería existir algún sistema de administración de actualizaciones de seguridad para la defensa de la red, los clientes y los servidores. Dicho sistema se podría proporcionar como parte de una solución más amplia de administración de revisiones de la empresa. Es necesario comprobar de forma periódica si existen actualizaciones para los sistemas operativos de hosts y dispositivos. La directiva de actualizaciones de seguridad debe ofrecer también criterios operativos para el proceso que permite distribuir actualizaciones de seguridad a los sistemas de su organización. Este proceso debe incluir las siguientes fases:
  
1.  **Búsqueda de actualizaciones**. Se debe establecer algún tipo de proceso de notificación automatizado para avisar a los usuarios de las actualizaciones disponibles.
  
2.  **Descarga de actualizaciones**. El sistema debe poder descargar las actualizaciones con un mínimo impacto en los usuarios y la red.
  
3.  **Prueba de las actualizaciones**. Si las actualizaciones son para hosts con funciones esenciales, debe asegurarse de que cada actualización se prueba en un sistema adecuado que no sea el de producción antes de implementarlo en el propio entorno de producción.
  
4.  **Implementación de las actualizaciones**. Una vez que se ha probado la actualización, se debe ofrecer un mecanismo sencillo de implementación que permita distribuirla.
  
Si los sistemas que se están actualizando en su entorno no requieren la fase de prueba de esta lista, su organización puede optar por la automatización de todo el proceso. Por ejemplo, la opción **Actualizaciones automáticas** del sitio Web de Microsoft Windows Update permite que se notifiquen y actualicen los equipos cliente sin la intervención del usuario. Con ello los sistemas pueden ejecutar lo antes posible las actualizaciones de seguridad más recientes. Sin embargo, este método no prueba la actualización antes de instalarla, por lo que si se trata de un requisito para su organización, no se recomienda esta opción.
  
Comprobar que los sistemas disponen siempre de las últimas actualizaciones de seguridad se deberá convertir en parte rutinaria de la administración del sistema de su organización.
  
#### Directivas basadas en riesgos
  
Con tantos dispositivos de red, clientes y servidores conectados a las capas de red interna y perimetral del modelo de defensa en profundidad antivirus, puede resultar difícil crear una directiva de seguridad única y eficaz que administre todos los requisitos y configuraciones de su organización. Un método que puede emplear para organizar la directiva consiste en agrupar los hosts en categorías basadas en el tipo y exposición al riesgo.
  
Para poder determinar el nivel de riesgo que se asigna a un host o dispositivo puede realizar una evaluación de riesgos de cada uno de ellos. Podrá encontrar un conjunto detallado de instrucciones sobre la realización de estas evaluaciones de riesgos en la sección "Chapter 3: Understanding the Security Risk Management Discipline" de *Microsoft Solution for Securing Windows 2000 Server* en TechNet:  
<http://www.microsoft.com/technet/security/prodtech/win2000/secwin2k/03secrsk.mspx> (en inglés).
  
Microsoft recomienda que tenga en cuenta las siguientes categorías de configuración para las directivas de evaluación de riesgos centrada en los clientes de su organización:
  
-   **Configuración de clientes estándar**. Esta categoría de configuración se suele aplicar a los equipos de escritorio que permanecen físicamente instalados en un edificio. Estos clientes de escritorio se encuentran protegidos continuamente por la existencia de defensas de redes internas y externas y al hallarse dentro de las dependencias de la organización.
  
-   **Configuración de clientes de alto riesgo**. Esta categoría de configuración se ha diseñado para satisfacer las necesidades de los usuarios de equipos y dispositivos móviles, como los asistentes personales digitales (PDA) o los teléfonos móviles. Estos dispositivos normalmente salen del ámbito de protección de las defensas de red de la organización y se encuentran, por tanto, ante un nivel de riesgo mayor.
  
-   **Configuración de clientes invitados**. Esta categoría de configuración se ha diseñado para equipos cliente que no pertenecen o no tienen soporte técnico por parte de su organización. Puede que no sea posible administrar la configuración de estos equipos, ya que lo más probable es que no tenga control sobre su configuración. Sin embargo, puede establecer directivas que limiten la capacidad de estos equipos de conectarse a las redes de su organización. Los equipos cliente invitados suelen incluirse en uno de los siguientes tipos:
  
    -   Equipos domésticos de los empleados.
  
    -   Equipos de socios o proveedores.
  
    -   Equipos invitados.
  
Microsoft también recomienda que establezca categorías de riesgos para las funciones de servidor, y que aplique la misma evaluación de riesgos tanto para servidores como para clientes. Como punto de partida para las directivas de servidor, podría considerar las siguientes categorías de configuración:
  
-   **Configuración de servidores estándar**. Esta categoría de configuración está diseñada para que sea un denominador común para la mayoría de las configuraciones de los servidores de su entorno. Proporciona un nivel de seguridad mínimo, pero sin restringir los servicios que se utilizan normalmente. Después puede modificar las directivas de las categorías de configuración específicas de funciones y de alto riesgo para cubrir todos los requisitos de directivas en un nivel adecuado.
  
-   **Configuración de servidores de alto riesgo**. Los servidores que se encuentran en la red perimetral o expuestos directamente a archivos y conexiones externas se deben considerar en esta categoría de configuración. Por ejemplo, en ella se podrían incluir servidores Web, servidores de seguridad y de mensajería perimetrales. Un servidor que contenga datos especialmente confidenciales, como el servidor de la base de datos de recursos humanos, podría justificar esta configuración independientemente de su ubicación en la red.
  
-   **Configuraciones específicas de funciones**. Puede que su empresa decida organizar funciones específicas de servidor en distintas configuraciones para cumplir con mayor precisión los requisitos de las aplicaciones del servidor. Por ejemplo, puede emplear configuraciones de funciones para los servidores de mensajería, de base de datos o de seguridad. Este método se podría combinar con la categoría de configuración estándar o de alto riesgo si fuera necesario.
  
El uso de directivas basadas en riesgos es la opción por la que deben optar los equipos de planeación de su organización; después se pueden emplear las clasificaciones de configuración mencionadas como base para el posterior desarrollo. El objetivo es reducir el número de configuraciones que se deben gestionar los sistemas de administración. Por lo general, es más probable que un enfoque estandarizado propicie una configuración segura que configurar de forma independiente la seguridad de cada host del entorno.
  
#### Directivas de supervisión y generación de informes automatizadas
  
Si su organización utiliza un sistema de supervisión automatizada o una aplicación antivirus que informe de las posibles infecciones de software malintencionado a una ubicación central, tiene la posibilidad de automatizar este proceso para que cualquier alerta notifique automáticamente las incidencias a todos los usuarios de la infraestructura de TI. Un sistema de alertas automatizado reducirá al mínimo la demora entre una alerta inicial y el momento en que los usuarios son conscientes de la amenaza del software malintencionado; sin embargo, el problema que tiene este enfoque es que puede generar numerosos "positivos falsos". Si nadie controla las alertas y revisa la lista de comprobación de informes sobre actividades inusuales, es probable que las alertas avisen de software malintencionado que no está presente. Esta situación puede resultar contraproducente porque puede generar falta de interés en los usuarios al generarse las alertas con demasiada frecuencia.
  
Microsoft recomienda que asigne a miembros del equipo de administración de la red la responsabilidad de recibir todas las alertas automatizadas de software malintencionado de todos los paquetes antivirus o software de supervisión de sistemas que emplee su organización. El equipo podrá filtrar las falsas alarmas de los sistemas automatizados antes de enviar las alertas a los usuarios. Para que este método se pueda aplicar con éxito, el equipo debe supervisar las alertas 24 horas al día, los 7 días de la semana, a fin de garantizar que se comprueban todas las alertas y que las auténticas se envían a los usuarios de la red.
  
#### Concienciación de los usuarios y del equipo de soporte técnico
  
La concienciación y el entrenamiento deben estar dirigidos a los equipos de administración y de soporte de su organización. El entrenamiento de profesionales de TI esenciales constituye un requisito fundamental en todas las áreas de TI, pero resulta especialmente importante para la defensa antivirus, ya que la naturaleza de los ataques de software malintencionado y las defensas suelen cambiar con regularidad. Un nuevo ataque de este tipo de software podría poner en peligro un sistema de defensa eficaz casi de la noche a la mañana, y las defensas de su organización verse amenazadas. Si el personal de soporte técnico responsable de estas defensas no cuenta con el entrenamiento adecuado para saber detectar y responder a las nuevas amenazas de software malintencionado, es sólo cuestión de tiempo que se produzca una infracción grave en el sistema de defensa antivirus.
  
##### Concienciación del usuario
  
La educación del usuario es a menudo una de las últimas consideraciones que tiene en cuenta la organización a la hora de diseñar su defensa antivirus. Ayudar a los usuarios a comprender algunos de los riesgos relacionados con los ataques de software malintencionado constituye un elemento importante en la reducción de dichos riesgos, ya que todos los usuarios de la organización que utilizan recursos de TI desempeñan una función en la seguridad de la red. Por este motivo, es importante educar a los usuarios sobre los riesgos más frecuentes que pueden ayudar a reducir, por ejemplo:
  
-   Abrir archivos adjuntos al correo electrónico.
  
-   Utilizar contraseñas poco seguras.
  
-   Descargar aplicaciones y controles ActiveX de sitios Web que no son de confianza.
  
-   Ejecutar aplicaciones desde medios extraíbles no autorizados.
  
-   Permitir el acceso a los datos y redes de su organización.
  
A medida que cambian las técnicas de software malintencionado, deben actualizarse las defensas antivirus. Tanto si es para actualizar el archivo de firma del programa antivirus como el propio programa, el proceso de creación e implementación de las actualizaciones lleva su tiempo. En los últimos años, el tiempo que se tarda en crear actualizaciones se ha reducido considerablemente y éstas normalmente se encuentran disponibles en cuestión de horas. Sin embargo, en casos más raros, aún pueden pasar días desde el momento en que se produce el nuevo ataque de software malintencionado hasta que se crea una defensa antivirus efectiva.
  
Durante este período, la mejor defensa con la que puede contar su organización es que los usuarios sean conscientes del problema del software malintencionado y sus riesgos. Proporcionar a los usuarios instrucciones antivirus básicas y un entrenamiento al respecto puede ayudar a evitar que una nueva variante de software malintencionado que haya traspasado las defensas de TI se propague por todo el entorno.
  
El entrenamiento de los usuarios no tiene por qué ser un proceso complejo. Las instrucciones antivirus básicas se basan fundamentalmente en principios de sentido común, pero la tarea de asegurarse de que dichas instrucciones se apliquen y se comuniquen de forma clara puede resultar algo más difícil. En la página "Windows XP Baseline Security Checklists" de Microsoft TechNet:  
[http://www.microsoft.com/technet/Security/chklist/xpcl.mspx](http://www.microsoft.com/technet/security/chklist/xpcl.mspx) (en inglés) podrá encontrar unas listas de comprobación que pueden ayudarle a identificar los problemas relacionados con la seguridad y la protección antivirus de los que deberá informar a sus usuarios.
  
Los usuarios responsables de dispositivos móviles es probable que necesiten entrenamiento adicional a fin de que sean conscientes de los riesgos que supone sacar un dispositivo fuera de las defensas físicas y de red de la organización. Puede que sean necesarias defensas especiales para salvaguardar específicamente dichos dispositivos móviles. Por este motivo, es probable que los usuarios que administran este tipo de dispositivos precisen información y directrices de configuración adicionales.
  
**Nota**: encontrará información útil sobre la configuración de los usuarios finales en las instrucciones [Protect your PC](http://www.microsoft.com/security/protect/default.asp) en Microsoft.com:  
www.microsoft.com/security/protect/ (en inglés). Este sitio constituye una buena fuente de información que puede ayudar a que los usuarios se documenten sobre cómo garantizar la seguridad de las redes y los equipos domésticos.
  
##### Concienciación del equipo de soporte técnico
  
Los profesionales de TI responsables de la configuración y el soporte técnico de los servidores, clientes y dispositivos de red de la organización necesitarán un entrenamiento antivirus para ayudarles a garantizar que los sistemas se configuran y mantienen de forma óptima para detener ataques de software malintencionado. Los errores en la configuración de cualquiera de estos equipos o dispositivos pueden abrir un camino para el ataque de un software malintencionado. Por ejemplo, si un administrador de servidor de seguridad con poca información abre todos los puertos de red de forma predeterminada en un dispositivo de servidor de seguridad perimetral, se podría producir un grave riesgo para la seguridad con la posible entrada de software malintencionado. Los administradores responsables de los dispositivos que se conectan a la red perimetral de su organización deben recibir entrenamiento de seguridad específico para que sean conscientes de los distintos ataques que pueden afectar a los dispositivos de red.
  
Puede encontrar numerosos eventos, prácticas de laboratorio y Webcasts sobre temas de seguridad directamente en Microsoft. Para obtener más información sobre estos temas, consulte "Your Security Program Guide" en Microsoft.com:  
<http://www.microsoft.com/seminar/events/security.mspx> (en inglés).
  
También se encuentran disponibles información y libros sobre seguridad en Microsoft Learning. Para obtener más información sobre estas publicaciones, consulte la página "Microsoft Learning Security Resources" en Microsoft.com:  
<http://www.microsoft.com/learning/centers/security.asp> (en inglés).
  
##### Comentarios de los usuarios
  
Los usuarios conscientes del problema del software malintencionado pueden constituir un primer sistema de advertencia excelente si se les proporciona un mecanismo sencillo y eficaz para informar de comportamientos inusuales en los sistemas que utilicen. Dicho mecanismo puede adoptar la forma de un número directo de teléfono, un alias de correo electrónico o un proceso de ascenso rápido desde el servicio de soporte técnico de la organización.
  
##### Comunicaciones internas proactivas
  
Si es posible, los miembros del departamento de TI deben crear un equipo de respuesta antivirus proactiva que sea responsable de supervisar los sitios externos de alertas de software malintencionado de modo que puedan conocer los primeros avisos de este tipo de ataques. Algunos buenos ejemplos de este tipo de sitios son:
  
-   Sitios Web de proveedores de aplicaciones antivirus.
  
-   El sitio Web de la red de intercambio de información antivirus (AVIEN) en: [www.avien.org](http://www.avien.org/) (en inglés).
  
-   Servicios de alerta antivirus, como el sistema "Antivirus Information Early Warning System" (AVI-EWS) de AVIEN (a los que se puede suscribir).
  
-   El sitio Web de información de protección frente a virus en Microsoft.com: <http://www.microsoft.com/security/antivirus/> (en inglés).
  
Una comprobación regular de sitios de referencia como los mencionados anteriormente permitirán al personal de soporte técnico notificar a los administradores de sistemas y usuarios las amenazas de software malintencionado antes de que se introduzcan en la red de la organización. La regularidad de estas comprobaciones resulta esencial. Garantizar que los usuarios del sistema reciben advertencias proactivas antes de comprobar el correo electrónico de la mañana puede marcar la diferencia entre administrar la eliminación de algunos mensajes de correo electrónico sospechosos e intentar contener un ataque de software malintencionado. Si la mayoría de los usuarios de su sistema inician sesión a las 9 de la mañana, establecer una forma de comunicar nuevas amenazas de software malintencionado a esta hora se consideraría la mejor práctica.
  
###### Alertas internas de software malintencionado
  
Hallar el mecanismo más eficaz de informar a todos los usuarios del posible ataque de software malintencionado de forma oportuna y exhaustiva resulta fundamental. Los sistemas de comunicaciones disponibles varían en gran medida dependiendo de la infraestructura de la organización, lo que hace imposible proporcionar un sistema de alerta de este tipo de software que funcione para todas las organizaciones. Sin embargo, en esta sección se ofrecen los siguientes ejemplos de mecanismos que puede que desee tener en cuenta.
  
-   **Tablones de anuncios de la organización**. Un enfoque muy poco técnico pero que no por ello se debe olvidar es el uso de las puertas interiores de la oficina, tablones de anuncios o puntos de información impresa en papel que sean evidentes para los empleados. Aunque este proceso implica cierta labor de mantenimiento, tiene la importante ventaja de comunicar información esencial a los usuarios cuando las áreas de la red no están disponibles debido a un ataque.
  
-   **Sistemas de correo de voz**. Si lo permite el sistema de correo de voz de su organización, la posibilidad de dejar un único mensaje para todos los usuarios puede resultar un mecanismo eficaz de comunicar una alerta de software malintencionado. Sin embargo, debe tener en cuenta que este método obliga a que los usuarios tengan acceso al correo de voz antes que al correo electrónico para recibir la alerta de una posible amenaza.
  
-   **Mensajes de inicio de sesión**. Puede configurar el sistema operativo Windows para que envíe un mensaje directamente a las pantallas de los usuarios durante el proceso de inicio de sesión. Este mecanismo proporciona una forma eficaz de llamar la atención de los usuarios ante las alertas de software malintencionado.
  
-   **Portales de intranet**. Se puede utilizar un portal de la intranet que los usuarios tengan establecido como página de inicio para enviar alertas de software malintencionado. Se deberá indicar a los usuarios que consulten este portal antes de tener acceso a su correo electrónico para que este tipo de mecanismo de alerta resulte eficaz.
  
-   **Sistemas de correo electrónico**. Se debe prestar especial cuidado cuando se utilice el sistema de correo electrónico para comunicar alertas de software malintencionado a los usuarios. Debido a que un ataque podría afectar a los servidores de correo electrónico, puede que este mecanismo no sea efectivo en todos los casos. Asimismo, la existencia de una cola de mensajes en la bandeja de entrada podría hacer que se entregara una advertencia de software malintencionado después de que se hubiera recibido el correo electrónico que lo contiene. Por este motivo, conviene aconsejar a los usuarios que lean las advertencias de software malintencionado de alta prioridad cuando inicien sus equipos antes de revisar cualquier otro mensaje de correo electrónico.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
La defensa antivirus ya no se basa simplemente en instalar una aplicación. Los ataques de software malintencionado más recientes han demostrado que es necesario un método defensivo más exhaustivo. Este capítulo se ha centrado en la forma de aplicar el modelo de seguridad de defensa en profundidad para formar la base de un método de defensa en profundidad que cree una solución antivirus eficaz para su organización. Es importante entender que los creadores de software malintencionado están continuamente actualizando sus métodos para atacar las nuevas tecnologías de TI que pueda estar utilizando su organización, y que las tecnologías antivirus están en continua evolución para mitigar estas nuevas amenazas.
  
El método de defensa en profundidad antivirus debe ayudar a asegurar que su infraestructura de TI abarcará todos los posibles vectores de ataque del software malintencionado. Con este método de capas resulta más fácil reconocer cualquier punto débil que haya en el sistema, desde la red perimetral hasta los individuos que trabajan en los equipos de su entorno. No abarcar alguna de estas capas descritas en el método de defensa en profundidad antivirus podría dejar abiertos los sistemas a un posible ataque.
  
Debe revisar constantemente la solución antivirus para poder actualizarla cada vez que sea necesario. Todos los aspectos de la protección antivirus son importantes, desde las sencillas descargas automatizadas de firmas de virus hasta los cambios completos en la directiva de funcionamiento.
  
De la misma forma, debido a que la información proporcionada en esta guía está sujeta a actualizaciones, es importante consultar continuamente el sitio Web de información de protección frente a virus en Microsoft.com <http://www.microsoft.com/security/antivirus/> (en inglés) para recibir la información e instrucciones antivirus más recientes.
  
Microsoft reconoce lo perjudicial y costoso que puede llegar a ser el ataque de software malintencionado, por lo que ha invertido mucho esfuerzo en hacérselo más difícil a aquellos que crean y distribuyen este tipo de software. Microsoft también está trabajando para facilitar a los diseñadores de redes, profesionales de TI y usuarios finales la tarea de configurar los sistemas de modo que cumplan sus requisitos de seguridad con un mínimo impacto en las transacciones comerciales.
  
Aunque puede que no sea posible erradicar totalmente el código malintencionado, centrar la atención sistemáticamente en las áreas señaladas en este enfoque de defensa en profundidad antivirus ayudará a minimizar el efecto que pueda producir un ataque de software malintencionado en las actividades empresariales de su organización.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Control y recuperación de los ataques de virus
  
Publicado: mayo 20, 2004
  
##### En esta página
  
[](#agae)[Introducción](#agae)  
[](#azae)[Paso 1: Confirmación de la infección](#azae)  
[](#mnbv)[Paso 2: Respuesta a la incidencia](#mnbv)  
[](#ngba)[Paso 3: Análisis del software malintencionado](#ngba)  
[](#rtyu)[Paso 4: Recuperación del sistema](#rtyu)  
[](#ling)[Paso 5: Postrecuperación](#ling)  
[](#asfd)[Resumen](#asfd)
  
### Introducción
  
En este capítulo se presenta un conjunto detallado de consideraciones que son de utilidad para identificar y contener una infección ocasionada por un software malintencionado o un ataque de virus, y posteriormente remediar los efectos que hayan podido tener en los sistemas afectados del entorno. No conviene subestimar la necesidad de disponer de un enfoque coherente y directo que permita dar respuesta a las incidencias y recuperar los sistemas; los problemas ocasionados por el software malintencionado suelen crear una sensación de urgencia que no es muy propicia para iniciar procedimientos bien pensados que resulten eficaces a largo plazo.
  
También es importante recalcar un hecho: los ataques del software malintencionado se han hecho cada vez más complejos al utilizar muchas cargas distintas, por lo que ya no existe un único proceso que se pueda aplicar a todos los sistemas para eliminarlo. Lo más probable es que cada ataque de software malintencionado precise su propio remedio. Sin embargo, esto no resta importancia a la recomendación de definir un proceso coherente para identificar y contener un ataque de virus y recuperar el sistema.
  
A grandes rasgos, los principales pasos que debe seguir un proceso de recuperación ante un ataque de virus son los siguientes:
  
1.  Confirmación de la infección
  
2.  Respuesta a la incidencia
  
3.  Análisis del software malintencionado
  
4.  Recuperación del sistema
  
5.  Postrecuperación
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Paso 1: Confirmación de la infección
  
La capacidad de determinar con rapidez si un sistema se ha infectado resulta esencial para que la organización pueda minimizar el impacto de los virus. Si se puede confirmar una infección e identificar las características sospechosas del virus rápidamente, se podrá reducir significativamente su expansión e impacto en los usuarios.
  
Existen muchos tipos distintos de funcionamientos incorrectos de los sistemas que se pueden confundir con el comportamiento de un virus. Al recibir una llamada telefónica o un correo electrónico de un usuario informando de que tiene un virus en el sistema, el personal de soporte primero debe determinar si el comportamiento efectivamente puede deberse a algún tipo de código malintencionado. La lista siguiente proporciona algunos ejemplos de los síntomas típicos de los que puede informar un usuario como comportamientos similares a los de un virus:
  
-   "He abierto los datos adjuntos a un mensaje de correo electrónico y no ha pasado nada, pero el equipo se comporta de forma extraña".
  
-   "He recibido respuestas de mis contactos preguntándome por qué les había enviado datos adjuntos con la extensión .exe, .zip u otra, cuando en realidad nunca les he enviado tales datos adjuntos".
  
-   "Mi software antivirus ha dejado de funcionar y el equipo se apaga constantemente".
  
-   "Los programas no funcionan correctamente y van todos *muy* lentos".
  
-   "Un grupo de archivos que nunca había visto ha aparecido en la carpeta **Mis** **documentos**".
  
-   "Algunos archivos no se abren o han desaparecido".
  
Las observaciones y los comentarios que puedan proporcionar los usuarios son fundamentales, ya que ellos son los primeros en detectar una actividad inusual. Como la velocidad a la que se propaga un virus es cada vez mayor, el intervalo de tiempo entre la infección inicial y la disponibilidad de una defensa eficaz es un factor cada vez más importante. La mayoría de las infecciones se producen en este intervalo, por lo que es crucial que una organización pueda identificarlas y confirmarlas con rapidez para minimizar tanto la expansión de un ataque de virus como el daño que puede ocasionar.
  
En la siguiente sección se describen los pasos que permiten confirmar con prontitud si un comportamiento inusual es realmente un ataque de virus o de software malintencionado.
  
Si un nuevo tipo de software malintencionado infecta un sistema, el usuario del mismo será el primero en detectar el comportamiento inusual. Como se expuso en el capítulo 3 de esta guía, "Defensa en profundidad antivirus", normalmente se produce un retraso desde que se libera el software malintencionado hasta el momento en que la aplicación de búsqueda de virus se actualiza para poder detectarlo y tomar las medidas para eliminarlo. La mejor forma de ofrecer un sistema de advertencia rápido es informar a los usuarios para que reconozcan las señales de un posible ataque de software malintencionado y proporcionarles un vínculo de comunicaciones que les permita notificar esta circunstancia lo antes posible.
  
#### Elaboración de informes de la infección
  
Al recibir una llamada o generarse una alerta sobre un posible ataque de software malintencionado, es muy conveniente que el personal de soporte disponga de un proceso definido para determinar con la mayor rapidez posible si la alerta está relacionada con un nuevo ataque. El siguiente gráfico de flujo ilustra los principales pasos que implica el proceso:
  
![](images/Cc162791.AVFG0401(es-es,TechNet.10).gif)
  
**Figura 4.1 Proceso de elaboración de informes de una infección de software malintencionado**
  
##### Informes de actividad inusual
  
Las preguntas que se presentan a continuación permiten determinar si la actividad inusual que ha provocado la alerta es un ataque de software malintencionado. Se trata de preguntas que el miembro del soporte técnico de la organización debe realizar al usuario no técnico.
  
**Recopilación de la información básica**  
Las cuestiones iniciales se deben diseñar para generar respuestas que ayuden a determinar con la mayor rapidez posible la verdadera naturaleza de la alerta y la probabilidad de que se trate de un nuevo ataque de software malintencionado. Puede emplear las siguientes preguntas de ejemplo como punto de partida del proceso; deberían modificarse para que se adecuaran a los requisitos de su organización:
  
-   ¿Qué fecha y hora tiene el informe?
  
-   ¿Cuál fue la actividad inusual que generó el informe?
  
-   ¿Qué actividad se estaba realizando en el momento anterior a que se produjera la actividad inusual?
  
    -   ¿Ha visitado recientemente algún sitio Web que no visite normalmente?
  
    -   ¿Ha utilizado el sistema fuera de la red de la organización recientemente (por ejemplo, en un aeropuerto, en la red de su casa, en una zona activa Wi-Fi o en un hotel?
  
    -   ¿Ha visto alguna ventana emergente o anuncio poco habituales en pantalla?
  
-   ¿Qué procesos inusuales o inesperados se ejecutan en este momento?
  
-   ¿Es el equipo una estación de trabajo o un servidor? ¿Qué sistema operativo utiliza y qué actualizaciones de seguridad se le han aplicado?
  
-   ¿Contiene el equipo u otros dispositivos conectados a él datos esenciales?
  
-   ¿Inicia sesión en el equipo con una cuenta de usuario con privilegios administrativos?
  
-   ¿Utiliza el usuario una contraseña o clave segura?
  
-   ¿Ha sufrido este sistema algún otro ataque de software malintencionado anteriormente?
  
Esta última pregunta es muy importante, ya que los ataques previos a menudo crean vulnerabilidades que pueden llevar a ataques posteriores a menos que se eliminen. Si la respuesta a esta pregunta es "Sí", se pueden formular las siguientes preguntas adicionales:
  
-   ¿Cuándo tuvo lugar ese ataque previo?
  
-   ¿Quién se encargó del caso y, si se conociera, cuál era el número de caso?
  
-   ¿Dispone de información sobre las medidas tomadas en aquel momento?
  
**Evaluación de los datos**  
Una vez recopiladas las respuestas a estas preguntas, el técnico de soporte debe evaluar los datos obtenidos teniendo en cuenta las siguientes preguntas para determinar si la causa probable del informe es un ataque de software malintencionado:
  
-   ¿Podría el informe ser resultado de la incorporación o actualización legítimas de una característica del sistema?
  
-   ¿Se podría deber a las actividades de un usuario no autorizado (en lugar de un intruso)?
  
-   ¿Se podría justificar como producido por una actividad del sistema conocida?
  
-   ¿Se podría deber a cambios no autorizados en programas o sistemas?
  
Por último, se debe realizar una comprobación con fuentes antivirus externas (identificadas en la sección "Comunicaciones internas proactivas" del capítulo 3 de esta guía, "Defensa en profundidad antivirus") a fin de determinar si el informe coincide con algún virus o alerta de gusano existente.
  
**Recopilación de los detalles**  
En este punto ya se podría establecer si la causa del problema es un ataque de software malintencionado. Si no fuera así, sería necesario un nivel mayor de información técnica y que el técnico de soporte visitara físicamente o, si fuera posible, que obtuviera acceso remoto al sistema sospechoso. Puede emplear las siguientes preguntas técnicas para recopilar información más detallada y determinar categóricamente si un sistema ha sufrido el ataque de un virus o un código malintencionado:
  
-   ¿Tiene habilitado o está protegido el dispositivo por un servidor de seguridad? Si es así, ¿qué puertos están abiertos a Internet?
  
-   Si las aplicaciones dan error, póngase en contacto con el proveedor de la aplicación directamente para establecer la causa raíz (por ejemplo, las aplicaciones actuales de Microsoft ofrecen herramientas de elaboración de informes de error que se pueden utilizar para enviar un informe de errores).
  
-   ¿Existe alguna nueva actualización de seguridad para el sistema que no se haya instalado?
  
-   ¿Con qué tipo de directiva de contraseñas cuenta el sistema? ¿Cuál es la longitud máxima de las contraseñas? ¿Qué requisitos de complejidad tienen?
  
-   ¿Existe algún/alguna:
  
    -   cuenta nueva o sospechosa en el equipo local?
  
    -   cuenta nueva o sospechosa en el grupo del administrador?
  
    -   servicio nuevo o sospechoso en la consola de administración de los servicios?
  
    -   suceso nuevo o sospechoso en los registros de sucesos?
  
-   ¿Ha informado la utilidad **netstat** de conexiones de red a direcciones IP externas o sospechosas?
  
##### Respuesta a la actividad inusual
  
Una vez que se ha recopilado la información inicial y se ha empleado para determinar la naturaleza de la alerta, debería resultar sencillo para el soporte técnico tomar una decisión sobre si se ha producido una falsa alarma, si se trata de un mensaje de virus falso o por el contrario de un ataque de software malintencionado real.
  
Crear un informe de software malintencionado falso es mucho más sencillo que desarrollar un virus o un gusano, pero desgraciadamente hace que se generen muchas alertas falsas de este tipo de amenazas. Estos mensajes de virus falsos y las llamadas y advertencias que producen hacen que se pierda mucho tiempo y dinero. También suelen molestar a los usuarios y hacerles cuestionarse la utilidad de informar de ataques potenciales. Se deben tener en cuenta las siguientes consideraciones para garantizar que la alerta se gestiona de forma correcta.
  
-   **Falsa alarma**. Si el informe es una falsa alarma, la información de la llamada debería registrarse para que la revisión periódica de estos datos ayude a establecer si el usuario requiere directrices adicionales.
  
-   **Mensaje de virus falso**. Resulta igual de importante registrar las alertas de software malintencionado falsas como la actividad de un virus real, puesto que las primeras también son ejemplos de ataques, aunque no utilicen código malintencionado. Informar a los usuarios de las alertas falsas y de las amenazas reales debe formar parte del protocolo antivirus de su organización. Esta información podrá ayudarles a reconocer los mensajes de virus falsos de antemano y en consecuencia contribuirá a reducir las pérdidas en la productividad.
  
-   **Infección conocida**. Si el sistema parece realmente infectado, el soporte técnico debe tomar medidas para determinar si la infección es un ataque conocido que se puede solucionar con una aplicación antivirus existente. Dicha aplicación debe estar siempre operativa y actualizada. Se debe realizar una búsqueda completa en el sistema para intentar limpiarlo. Si esta búsqueda logra identificar y limpiar la infección, se deberá registrar la llamada y enviar una advertencia a todos los usuarios para que comprueben que sus sistemas antivirus se ejecutan correctamente y que están actualizados. Si la búsqueda no puede identificar una forma concreta de software malintencionado, el virus se deberá considerar una infección nueva y se deberá tratar según las directrices establecidas en la sección "Respuesta a la incidencia".
  
-   **Nueva infección**. Cuando el sistema parezca estar infectado por un nuevo tipo de software malintencionado, se deben tomar una serie de medidas previas para garantizar que el problema se pone en conocimiento de los usuarios de la forma correcta. Estas medidas iniciales se han diseñado para que el personal de soporte de TI pueda seguir un proceso de aplicación coherente. Las respuestas a las preguntas iniciales mencionadas anteriormente permitirán establecer cuáles de las siguientes medidas se deben tomar en esta fase:
  
    -   Ponerse en contacto con el miembro asignado del equipo de respuesta a emergencias y facilitarle los detalles de la alerta.
  
    -   Si el sistema sospechoso es un servidor, ponerse en contacto con el administrador del mismo para determinar la viabilidad y las consecuencias de eliminarlo de la red.
  
    -   Si el sistema sospechoso es una estación de trabajo, ponerse en contacto con el usuario que la utiliza para determinar la viabilidad y las consecuencias de eliminarlo de la red.
  
    -   Considerar la posibilidad de activar una advertencia o alerta de alto nivel para notificar a los usuarios del sistema de TI del ataque detectado.
  
En este punto, la función del personal de soporte habrá concluido. La responsabilidad del ataque de virus se deriva al proceso de respuesta a incidencias y será necesario informar de su existencia a los miembros del equipo de respuesta a incidencias de seguridad (CSIRT).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Paso 2: Respuesta a la incidencia
  
Como se expuso en el capítulo 3 de esta guía, "Defensa en profundidad antivirus", el CSIRT deberá convocar una reunión de emergencia lo antes posible para organizar la fase siguiente del proceso de respuesta a incidencias de la organización. Para obtener explicaciones detalladas sobre la creación de un equipo de respuesta a incidencias y los procesos de recuperación de desastres y seguridad en general, consulte el mismo capítulo de la guía.
  
En esta guía se presupone que ya existe un CSIRT. El objetivo principal en este momento debe ser determinar el mecanismo de control del ataque de virus inmediato. En la siguiente sección se ofrece información que permite establecer las distintas opciones disponibles de dicho mecanismo y sus componentes.
  
#### Control de ataques de virus de emergencia
  
Una vez se ha confirmado el ataque de software malintencionado, el primer paso para controlarlo es aislar los equipos infectados del resto de dispositivos. Este aislamiento es esencial para evitar la propagación del código malintencionado. Los diferentes mecanismos que se pueden utilizar para ello tendrán un impacto en el funcionamiento normal de la organización.
  
**Importante**: si piensa que su organización puede tomar medidas legales e iniciar un proceso criminal o civil, Microsoft recomienda que consulte a los representantes legales antes de realizar otras acciones.
  
Si el ataque de virus se hubiera detectado en la comunidad de proveedores de antivirus, siga las indicaciones del proveedor de su producto antivirus para determinar su gravedad.
  
Si el ataque no fuera conocido por la comunidad de proveedores de productos antivirus, deberá ponerse en contacto con su proveedor lo antes posible. Probablemente le solicite que envíe algunos ejemplos del software malintencionado en un archivo comprimido y protegido por contraseña para que puedan analizarlo. El proceso de búsqueda de estos ejemplos no siempre es sencillo y lo ideal es que se prepare por anticipado. Consulte la sección "Paso 3: Análisis del software malintencionado" de este capítulo para conocer cómo preparar los ejemplos.
  
El siguiente paso es contener el ataque. Existen tres opciones básicas a considerar:
  
-   Desconectar el sistema o sistemas afectados de la red local.
  
-   Si fuera posible, aislar la red o redes que contengan los hosts infectados.
  
-   Si toda la red está afectada o puede verse afectada, desconectarla por completo de todas las redes externas.
  
Se podrían seguir muchos otros pasos técnicos más detallados como controlar la red para intentar identificar los puertos y direcciones IP que se han visto implicados en el ataque. Sin embargo, si no se completa el análisis detallado del software malintencionado, el riesgo de pasar por alto un vector de ataque que podría conducir a una infección mayor es significativo. El único mecanismo disponible en su organización para determinar si el riesgo es aceptable o no sería realizar un informe de evaluación de riesgos de seguridad. Este informe permitiría analizar los riesgos que implica no detener el ataque e infectar potencialmente o utilizar sin advertirlo el software malintencionado para iniciar un ataque en los equipos de clientes o socios de la organización. Si no ha completado el análisis de riesgos antes de que se produzca un ataque, se recomienda que su organización peque de cautela y minimice la posibilidad de propagación del ataque seleccionando el nivel de aislamiento más alto posible.
  
Las opciones enumeradas aquí son únicamente unas directrices. La acción específica que emprenda puede ser distinta dependiendo de factores como las necesidades empresariales, el escenario, el impacto y la gravedad entre otros, que pueden ser aplicables sólo a su organización y a las circunstancias del ataque.
  
#### Preparación de la recuperación
  
Después de activar el mecanismo de control del ataque de virus deberá iniciar el proceso de recuperación activa. El objetivo general de dicho proceso es garantizar que se logra lo siguiente:
  
-   Trastorno mínimo de la actividad empresarial de la organización.
  
-   Recuperación del ataque en el menor tiempo posible.
  
-   Captura de información para las posibles acciones legales que se puedan emprender.
  
-   Recopilación de información para que se puedan desarrollar medidas de seguridad adicionales, si fueran necesarias.
  
-   Prevención de nuevos ataques del mismo tipo en los sistemas recuperados.
  
Desgraciadamente, a diferencia de los primeros dos objetivos, que requieren una solución rápida, los tres restantes precisan más tiempo para recopilar información sobre el ataque que permita identificarlo completamente. Para lograr los objetivos de estos dos grupos, es decir, resolver rápidamente el problema y recopilar todos los datos relevantes necesarios, puede utilizar el proceso que se muestra en la figura siguiente. Este proceso se ha diseñado para garantizar que el sistema infectado se prepara para la recuperación tan rápido como sea posible y al mismo tiempo para asegurar que los datos de análisis necesarios no se pierden. Esos datos son importantes, ya que la organización los utilizará para determinar si los sistemas recuperados están a salvo de futuros ataques, y como pruebas en caso de que se deseen emprender acciones legales en el futuro.
  
Los procesos de recuperación del sistema y de análisis de virus se deben ejecutar de forma paralela para que la recuperación tenga lugar lo más rápidamente posible.
  
[![](images/Cc162791.AVFG0402(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0402_big(es-es,technet.10).gif)
  
**Figura 4.2 Pasos de la recuperación previos al análisis**
  
La forma más rápida de preparar todos los sistemas para su recuperación es determinar si se puede emplear un sistema infectado para el análisis. Si es así, este sistema deberá ponerse en cuarentena y analizarse. (Las instrucciones de este proceso de análisis se facilitan en la sección "Paso 3: Análisis del software malintencionado" de este capítulo.) Cuando no es posible poner en cuarentena o analizar el sistema, la mejor opción es crear un clon del sistema utilizando un software de creación de imágenes. Si esta opción está disponible, puede crear una imagen del sistema, preparar el equipo original para la recuperación y crear un clon del sistema.
  
En aquellos casos en los que se desee recopilar pruebas y realizar un análisis más detallado, es fundamental crear una imagen de los equipos afectados lo antes posible (antes de que se inicien las actividades de recuperación) para que la infección se pueda identificar, clasificar y tratar de la forma más rápida y conveniente posible.
  
Por último, si no se puede crear una imagen, se debe recopilar un conjunto de datos de análisis mínimos antes preparar el sistema para la recuperación. Lo ideal es que el equipo de seguridad de la organización desarrolle y utilice algún tipo de kit de herramientas de respuesta a incidencias. Estas herramientas pueden servir para recopilar datos volátiles y no volátiles para facilitar información de análisis del sistema. Se podría emplear un subconjunto de un grupo de herramientas de análisis de software malintencionado más completo que el utilizado en la sección siguiente de este capítulo para descubrir y documentar todos los elementos del virus. Sin embargo, el principal diferenciador de un kit de herramientas de respuesta a incidencias es que debe capturar el nivel mínimo de información del sistema necesaria en el menor tiempo posible para permitir que el sistema se pueda preparar para la recuperación a la mayor brevedad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Paso 3: Análisis del software malintencionado
  
Tan pronto como se logre contener el ataque del software malintencionado, es importante detenerse a descubrir su naturaleza y realizar un análisis más detallado del mismo. Si no se hace así, las probabilidades de que se produzca una nueva infección son altas; por otra parte, si se desconoce el funcionamiento del software malintencionado no habrá garantías de que los sistemas están realmente limpios y seguros antes nuevos ataques.
  
Lo ideal es que el análisis del software malintencionado lo lleve a cabo un miembro del equipo de seguridad con un conjunto de aplicaciones y utilidades dedicadas que puede emplear para recopilar la información necesaria de la forma más automatizada posible. Los pasos siguientes permitirán conocer la naturaleza del ataque.
  
#### Examen de los elementos del sistema operativo
  
Intente determinar qué archivos del sistema operativo introdujo o modificó el ataque. Como parte del análisis, examine los cambios en las siguientes áreas:
  
-   Los procesos y servicios activos.
  
-   El Registro local.
  
-   Los archivos de las carpetas del sistema Microsoft® Windows®.
  
-   Las nuevas cuentas de usuarios o grupos, en especial aquellas con privilegios de administrador.
  
-   Las carpetas compartidas (incluidas las ocultas).
  
-   Los archivos de reciente creación que tengan nombres de archivo comunes pero en ubicaciones poco habituales.
  
-   Los puertos de red abiertos.
  
Las técnicas que se pueden emplear para comprobar todos estos elementos del sistema operativo se presentan en las secciones siguientes.
  
##### Comprobación de los procesos y servicios activos
  
Lo más probable es que se hayan introducido nuevos procesos en la memoria de los sistemas infectados.
  
Se recomienda utilizar herramientas de enumeración de procesos especializadas como PsTools o el programa gratuito Process Explorer para contar con una interfaz de usuario más descriptiva. Estas herramientas, disponibles en el sitio Web de Sysinternals en [http://www.sysinternals.com](http://www.sysinternals.com/) (en inglés), permiten no sólo ver la ruta al archivo de imagen, sino también el árbol del proceso.
  
Para minimizar el número de entradas de la lista de procesos y facilitar la identificación de los procesos falsos, será necesario cerrar todas las aplicaciones válidas, incluidas las que se ejecuten en un segundo plano, como Instant Messenger, los monitores de correo electrónico o las utilidades de terceros residentes en memoria.
  
Si no se dispusiera de ninguna herramienta especializada, se puede emplear la herramienta Administrador de tareas de Windows, presente en todos los sistemas Microsoft Windows, para realizar una comprobación rápida de los procesos activos que se estén ejecutando en el sistema. No obstante, el Administrador de tareas de Windows no muestra la ruta a la imagen que inició el proceso, por lo que resulta imposible determinar si un ataque de software malintencionado que se inició como "svrhost" es un proceso legítimo o no.
  
Siga los pasos siguientes para analizar los procesos activos con el Administrador de tareas:
  
**Para analizar los procesos activos en un equipo con Windows**
  
1.  Presione las teclas **CTRL**+**ALT**+**Supr** simultáneamente para que se muestre la ventana **Seguridad de Windows** y seleccione **Administrador de tareas**.
  
    **Nota**: en los equipos Windows 9*x* podrá ver una lista de los programas que se están ejecutando en lugar de la aplicación Administrador de tareas.
  
2.  Haga clic en la ficha **Procesos**.
  
3.  Amplíe la ventana Administrador de tareas de Windows para mostrar en pantalla tantos procesos activos como sea posible.
  
4.  Seleccione la opción **Ver** en la barra de menús y haga clic en **Seleccionar columnas...**
  
5.  Active las casillas de verificación de las siguientes columnas:
  
    -   Identificador de proceso (PID)
  
    -   Uso de CPU
  
    -   Tiempo de CPU
  
    -   Uso de memoria
  
    -   Uso máximo de la memoria
  
    -   Lecturas de E/S
  
    -   Escrituras de E/S
  
6.  Haga clic en **Aceptar** y amplíe la ventana para mostrar tantas columnas como sea posible.
  
Puede ordenar las columnas haciendo clic en el título de cualquiera de ellas. Utilice este método de ordenación en cada una de las columnas enumeradas y determine los recursos que utiliza cada proceso.
  
**Nota**: para guardar una copia impresa de la lista para referencia futura, haga que Process Explorer o el Administrador de tareas de Windows aparezcan en una ventana activa y presione **ALT+Impr Pant** en el teclado. Se creará una captura de pantalla de la lista en el portapapeles del equipo y podrá pegarla en la aplicación Paint de Windows o en Microsoft Word para imprimirla.
  
La siguiente figura muestra los detalles del gusano Blaster como proceso activo en el Administrador de tareas de Microsoft Windows 2000® Server.
  
[![](images/Cc162791.AVFG0403(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0403_big(es-es,technet.10).gif)
  
**Figura 4.3 Pantalla Administrador de tareas de Windows 2000 con el gusano Blaster como proceso activo**
  
**Nota**: algunos tipos de software malintencionado intentarán bloquear el Administrador de tareas e impedir que se inicie como mecanismo de defensa. En este caso se puede emplear la utilidad de la línea de comandos **Tasklist** en los equipos Microsoft Windows® XP y Windows Server™ 2003 (o **TList** en equipos Windows 2000) para generar una lista de archivos de texto simple que se puede copiar a un medio extraíble para su análisis posterior. Utilice la siguiente sintaxis de la línea de comandos para generar el archivo de texto con la lista de todos los procesos activos:
  
```  
 tasklist /v &gt;TaskList.txt  
```  
Con ella podrá crear un archivo llamado **TaskList*.*txt** en el directorio de trabajo actual.
  
Siga las siguientes sugerencias para comprobar los procesos que se ejecutan en un equipo en el que se sospecha que existe un software malintencionado:
  
-   Compruebe todas las instancias de los servicios Telnet o protocolo de transferencia de archivos (FTP) en ejecución.
  
-   Si no está seguro de la legitimidad de un proceso, utilice un motor de búsqueda en Internet como Google para buscar información sobre el mismo.
  
-   Compruebe en la ruta al archivo de imagen los procesos cuyo nombre de imagen reconozca.
  
-   Busque servicios que estén tanto en ejecución como detenidos.
  
Además del proceso msblast.exe que se mostraba en la figura anterior, otros procesos sospechosos posibles serían los siguientes:
  
-   ServuFTP
  
-   Ocxdll.exe
  
-   Kill.exe
  
-   Mdm.exe
  
-   Mdm.scr
  
-   Mt.exe
  
-   Ncp.exe
  
-   Psexec.exe
  
-   Win32load.exe
  
**Comprobación de las carpetas de inicio**  
Es posible que el software malintencionado haya intentado ejecutarse modificando las carpetas de inicio del sistema.
  
**Nota**: la ruta precisa a estas carpetas depende del sistema operativo que se analice. La siguiente información corresponde a los sistemas operativos Windows XP, Windows Server 2003 o Windows 2000.
  
Son dos las áreas de la carpeta de inicio que se recomienda comprobar. La primera es la carpeta **All Users**, que se encuentra en la siguiente ubicación predeterminada:
  
C:\\Documents and Settings\\All Users\\Menú Inicio
  
La segunda área es la ruta al perfil de usuario de la cuenta conectada en ese momento, si bien resulta recomendable comprobar todos los perfiles que se hayan creado en el sistema. Podrá encontrar esta información en C:\\Documents and Settings\\*&lt;Nombre\_usuario&gt;*\\Menú Inicio, donde *&lt;Nombre\_usuario&gt;* es el Id. de inicio de sesión en el sistema que se está comprobando.
  
**Nota**: en los sistemas Microsoft Windows® 95 y Windows® 98 puede ocurrir que el software malintencionado cambie el nombre de la carpeta de inicio. Para obtener más información sobre este tema, consulte el artículo de Microsoft Knowledge Base "141900: "Folder Other Than StartUp Launches Programs" en Microsoft.com: <http://support.microsoft.com/?kbid=141900>
  
Compruebe las entradas de cada una de las carpetas de inicio para asegurarse de que ningún tipo de software malintencionado se intenta ejecutar durante el inicio del sistema.
  
**Comprobación de las aplicaciones programadas**  
Aunque resulta menos frecuente, en ocasiones el software malintencionado intenta utilizar el servicio de programador de Windows para iniciar una aplicación no autorizada. Para asegurarse de que no es el caso basta con realizar una simple comprobación de la cola del programador como se describe en estos pasos:
  
**Para comprobar la cola del programador**
  
1.  Haga clic en **Inicio**, seleccione **Ejecutar**, escriba **at** y presione **ENTRAR**
  
2.  Revise la lista. Si mostrara alguna aplicación no autorizada o sospechosa, cree un informe para un análisis posterior con el siguiente comando:
  
    -   Haga clic en **Inicio**, seleccione **Ejecutar**, escriba at &gt;C:\\AT\_Queue\_Report.txt y presione **ENTRAR**.
  
Con la ejecución de este comando se creará un archivo de texto en la raíz de la unidad C: que deberá copiarse a un disco extraíble para un análisis posterior. Revise el archivo de texto para determinar si hay programada alguna aplicación no autorizada en la cola.
  
Una vez haya completado el análisis de todos los procesos activos y programados, podrá identificar los procesos que introdujo el ataque. Después de documentarlos, deberá reiniciar el sistema y repetir el análisis para asegurarse de que el ataque de virus no ha comprometido otras áreas del sistema o permitido que se ejecuten procesos falsos al iniciar. Si fuera así, deberá realizar un análisis de los archivos de inicio del sistema y del Registro para intentar hallar el mecanismo utilizado para mantener los procesos falsos.
  
##### Análisis del Registro local
  
Al ser el Registro del sistema un almacén de datos complejo y extenso, puede que resulte recomendable realizar una copia de seguridad completa del mismo para poder llevar a cabo un análisis detallado de su contenido después de completar el proceso de recuperación.
  
La utilidad de copia de seguridad que se incluye en todas las versiones de Windows se puede emplear para realizar una copia de seguridad y la restauración de todo el Registro. Si ya utiliza esta utilidad para realizar copias de seguridad regulares del disco duro no le resultará complicado incluir el Registro en esta rutina. Para realizar la copia de seguridad del Registro con la aplicación de copia de seguridad, seleccione **Estado del sistema** cuando elija las unidades, archivos y carpetas que desea incluir en el conjunto de copia de seguridad.
  
Como Estado del sistema incluye, además del Registro, otra información específica del sistema, los archivos de copia de seguridad tendrán un tamaño considerable. Otra alternativa es usar las utilidades del Editor del Registro que se facilitan con todas las versiones de Windows. Estas utilidades son idóneas para realizar copias del Registro. Windows XP y Windows Server 2003 disponen de dos grupos de herramientas del Editor del Registro, **Regedit.exe** y la herramienta de la línea de comandos **Reg.exe**.
  
**Nota**: los sistemas operativos Windows 2000 y Windows NT® emplean **Regedt32.exe** y requieren las herramientas **RegBack.exe** *y* **RegRest.exe** del kit de recursos para proporcionar la misma funcionalidad que **Regedit.exe**y **Reg.exe**. Para obtener más información sobre estas herramientas, consulte la página "Backing up and Restoring the Windows 2000 Registry" del *kit de recursos de Windows 2000* en Microsoft.com:  
[http://www.microsoft.com/windows2000/techinfo/reskit/en-us/regentry/RegistryBackup.asp](http://www.microsoft.com/windows2000/techinfo/reskit/en-us/regentry/registrybackup.asp) (en inglés).
  
**Para realizar una copia de seguridad del Registro con Regedit**
  
1.  Haga clic en **Inicio**, seleccione **Ejecutar**, escriba regedit y presione **ENTRAR**.
  
2.  En el panel de la izquierda, seleccione **Mi PC** y, a continuación, en el menú **Archivo**, seleccione **Exportar**.
  
3.  Escriba un nombre en el cuadro **Nombre de archivo** y especifique una ubicación para la copia del archivo del Registro.
  
4.  En **Intervalo de exportación**, seleccione **Todo** y haga clic en **Guardar**.
  
Puede encontrar información detallada sobre el uso de **Regedit.exe** y **Reg.exe** en "Registry Reference for Windows Server 2003" de la guía de implementación de Windows Server 2003 en:  
[http://www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/RegistryBackup.asp](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/registrybackup.asp) (en inglés).
  
**Importante**: como este disco puede estar expuesto al software malintencionado, asegúrese de que no entra en contacto con otros sistemas hasta que se haya establecido un método de control eficaz.
  
Una vez haya realizado la copia de seguridad del Registro, compruebe en las siguientes áreas las posibles referencias de archivo inusuales:
  
```  
  HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\SessionManager\\KnownDLLs   HKEY\_LOCAL\_MACHINE\\System\\ControlSet001\\Control\\Session Manager\\KnownDLLs    HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Current Version\\Run    HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Current Version\\RunOnce    HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Current Version\\RunOnceEx HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServices    HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows ("run="     line) HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\Current Version\\Run    HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\Current Version\\RunOnce    HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\Current Version\\RunOnceEx HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\RunServices    HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows ("run="     value)   
```  
Estas áreas del Registro suelen ser el objetivo del código malintencionado porque le permiten ejecutarse al iniciar el sistema. Por ejemplo, el gusano W32@.Mydoom.G@mm agregó el valor:
  
```  
   "(Default)" = "%System%\\&lt;nombre\_archivo\_aleatorio&gt;"  
```  
a las claves del Registro:
  
```  
   HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run   HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run  
```  
Otra área que se ha visto afectada recientemente es la siguiente clave:
  
```  
   HKEY\_CLASSES\_ROOT\\CLSID\\{E6FB5E20-DE35-11CF-9C87-00AA005127ED}\\InProcServer32  
```  
Esta clave controla los archivos .dll que carga Microsoft Internet Explorer (**Explorer.exe**). Por ejemplo, el gusano Mydoom y sus variantes podrían agregar una entrada a esta clave para cargar un archivo .dll que crearía una vulnerabilidad y establecería una puerta trasera para un ataque.
  
El gusano W32.Netsky.D@mm eliminaría la clave y agregaría todo este conjunto de claves:
  
```  
  HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\PINF   HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\WksPatch  
```  
##### Comprobación de la existencia de software malintencionado y de archivos dañados
  
La mayoría de los tipos de software malintencionado modifican uno o más archivos del disco duro de un equipo, por lo que encontrar cuáles son los que se han visto afectados puede resultar complicado. Si el sistema se creó a partir de una imagen, se puede comparar el sistema infectado directamente con un sistema nuevo creado a partir de dicha imagen.
  
Si esta alternativa no estuviera disponible, otro método que permite determinar qué archivos se han modificado consiste en utilizar una herramienta de búsqueda en el sistema para localizar todos los archivos que hayan cambiado desde que el software malintencionado se introdujo en el sistema. Una búsqueda de estas características se puede realizar con la herramienta Buscar de Windows; la siguiente captura de pantalla muestra cómo acotar la búsqueda de archivos infectados con las opciones avanzadas del panel **Resultados de la búsqueda**.
  
[![](images/Cc162791.AVFG0404(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162791.avfg0404_big(es-es,technet.10).gif)
  
**Figura 4.4 Opciones avanzadas del cuadro de diálogo Resultados de la búsqueda**
  
Si establece las opciones tal como se muestra en la figura, aparecerán todos los archivos que se hayan creado el día en el que el software malintencionado se introdujo en el host (en este ejemplo, el 27 de abril de 2004).
  
También se puede crear un archivo de texto que contenga una lista de todos los archivos presentes en el directorio actual y sus subdirectorios, aunque advertimos que la lista puede ser extensa.
  
**Para crear una lista de todos los archivos de un directorio y sus subdirectorios**
  
1.  Haga clic en **Inicio**, seleccione **Ejecutar**, escriba cmd y presione **ENTRAR**.
  
2.  Cambie al directorio que desea documentar.
  
3.  En el símbolo del sistema, escriba dir /s /-c /o:-d /t:c /q &gt; FileList.txt y presione **ENTRAR**.
  
Al ejecutar este comando se creará en el directorio actual un archivo de texto de nombre **FileList.txt**, que podrá copiar a un medio extraíble para realizar un análisis posterior.
  
**Nota**: existen muchas otras formas de crear una lista de estas características con otras herramientas y secuencias de comandos. Sin embargo, el objetivo de esta sección es ayudar a recopilar información rápidamente con herramientas que fácilmente pueden estar disponibles en cualquier equipo. Si dispone de tiempo para preparar un kit de herramientas de respuesta ante una emergencia que contenga una secuencia de comandos más avanzada, utilícelo en lugar del procedimiento descrito aquí.
  
Después de completar la búsqueda, los resultados se pueden ordenar por tipo para simplificar la identificación de los archivos ejecutables, que por regla general son el objetivo del software malintencionado. La siguiente lista ofrece ejemplos de algunos de los tipos de archivos más comunes que pueden contener código ejecutable:
  
\*.exe        \*.html        \*.cmd        \*.htm
  
\*.bat        \*.cpl        \*.pif        \*.pot
  
\*.vbs        \*.vbe         \*.js        \*.jse
  
\*.scr        \*.jpg         \*.doc        \*.xls
  
\*.mdb        \*.com        \*.ocx
  
**Nota**: la lista de búsqueda puede contener muchas entradas y es probable que no disponga de tiempo para revisar todas las modificaciones en esta fase del proceso. No obstante, se recomienda guardar una copia o imprimir la lista para cuando tenga tiempo de revisar los archivos que serán el objetivo más probable de los ataques.
  
Los siguientes archivos pueden indicar la presencia de un software malintencionado en el sistema:
  
-   DLL16.ini
  
-   DLL32.hlp
  
-   DLL32NT.hlp
  
-   Gates.txt
  
-   Gg.bat
  
-   Httpsearch.ini
  
-   Seced.bat
  
-   Xvpll.hlp
  
-   Psexec.bat
  
-   Lcp\_netbios.dll
  
Tradicionalmente estos archivos los ha utilizado el software malintencionado y se facilitan aquí como ejemplo de las técnicas de asignación de nombres que se han empleado para ocultar archivos de software malintencionado. Si no está seguro de la legitimidad de un nombre de archivo concreto, puede realizar una búsqueda en Internet para conocer la naturaleza del archivo y saber si se ha vinculado a software malintencionado. No obstante, conviene señalar que la búsqueda no se debe realizar desde el sistema infectado, ya que si se hace así, el software malintencionado podría modificar el comportamiento de la búsqueda en Internet.
  
También es necesario saber que algunos ataques de software malintencionado han utilizado nombres de archivo válidos pero colocando el archivo en una carpeta distinta para evitar que lo detecte el servicio de protección de archivos de Windows. Por ejemplo, un archivo utilizado por software malintencionado en el pasado es **Svchost.exe**, que normalmente se instala y está protegido en la carpeta %WINDIR%\\System32. Pero también se han descubierto ejemplos de código malintencionado que ha podido crear un archivo con el mismo nombre en la carpeta %WINDIR%. Por ello es importante comprobar la ruta completa así como los nombres de archivo.
  
Algunas de las áreas comunes en las que los ataques de software malintencionado suelen colocar y modificar archivos son las siguientes:
  
-   **%Windir%**. Es la variable asignada a la carpeta de instalación predeterminada del sistema operativo Windows. Esta carpeta contiene varios archivos ejecutables y de configuración importantes. De forma predeterminada, la variable señalará a otras rutas de carpeta:
  
    -   C:\\Windows (para los sistemas Windows 95/98/ME/XP y Windows Server 2003).
  
    -   C:\\Winnt\\ (para los sistemas Windows NT/2000).
  
-   **%System%**. Es la variable asignada a la carpeta del sistema situada debajo de la carpeta de instalación predeterminada del sistema operativo Windows. Esta carpeta contiene los archivos de sistema del sistema operativo host. De forma predeterminada, la variable señalará a otras rutas de carpeta:
  
    -   C:\\Windows\\System (para sistemas Windows 95/98/ME).
  
    -   C:\\Winnt\\System32 (para sistemas Windows NT/2000).
  
    -   C:\\Windows\\System32 (para sistemas Windows XP y Windows Server 2003).
  
-   **%Temp%**. Es la variable asignada a la ruta que utilizan las aplicaciones para escribir archivos temporales. De forma predeterminada, la variable se asigna a las siguientes rutas:
  
    -   C:\\Windows\\TEMP (para sistemas Windows 95/98/ME).
  
    -   C:\\WINNT\\Temp (para sistemas Windows NT/2000).
  
    -   C:\\Document and Settings\\*&lt;Nombre\_usuario&gt;*\\Configuración local\\Temp (para Windows XP y Windows Server 2003).
  
-   **%Temporary Internet Files%**. Es la variable utilizada por las aplicaciones de exploración en Internet para almacenar los archivos temporales durante la exploración Web. De forma predeterminada, la variable señalará a las siguientes rutas:
  
    -   C:\\Windows\\Archivos temporales de Internet (para sistemas Windows 95/98/ME).
  
    -   C:\\Document and Settings\\*&lt;Nombre\_usuario&gt;*\\Configuración local\\Archivos temporales de Internet (para sistemas Windows NT/2000/XP y Windows Server 2003).
  
Si al analizar los archivos del sistema descubre archivos infectados, se recomienda copiarlos a un medio extraíble para un análisis posterior. Obviamente, como estos archivos están infectados, deberá asegurarse de que no los utiliza ningún otro proceso que el previsto. Algunos de los pasos que puede seguir para proteger estas copias son los siguientes:
  
-   **Cambiar la extensión del nombre de archivo**. Si cambia la extensión del nombre de archivo a un nombre que desconozca el sistema operativo, éste no podrá ejecutar el archivo si por descuido se hace clic en él. Por ejemplo, podría reemplazar la última letra del archivo **Avirus.exe** por un guión bajo para que se muestre así: **Avirus.ex\_**.
  
-   **Almacenar los archivos infectados en un archivo de almacenamiento protegido**. Podría comprimir los archivos y utilizar una contraseña para proteger el archivo comprimido.
  
-   **Medios especializados**. Asegúrese de que los medios extraíbles se pueden identificar físicamente con claridad de los medios estándar utilizando discos de colores o etiquetas no estándar.
  
-   **Bloquear los archivos en una ubicación segura**. Coloque todos los medios de ejemplo de software malintencionado en una ubicación o medio de almacenamiento seguros.
  
-   **Enviar por correo electrónico sólo archivos de almacenamiento protegidos**. Si precisa enviar por correo electrónico el archivo sospechoso de contener software malintencionado (por ejemplo a un proveedor de antivirus), envíelo siempre en un archivo de almacenamiento protegido por contraseña. Las puertas de enlace del correo electrónico podrán buscar y detectar el software malintencionado si se envía como dato adjunto no protegido.
  
    **Nota**: algunos ataques de software malintencionado han utilizado archivos de almacenamiento protegidos para escapar de las técnicas de búsqueda antivirus. Como resultado, algunas organizaciones también bloquean o ponen en cuarentena todos los archivos de almacenamiento entrantes. Por ello, antes de enviar el archivo, compruebe que el destinatario del mismo permite los archivos de almacenamiento protegidos.
  
##### Comprobación de los usuarios y grupos
  
Algunos ataques de software malintencionado intentarán elevar los privilegios de los usuarios existentes en el sistema o agregar nuevas cuentas a grupos que dispongan de derechos de administrador. Compruebe la siguiente configuración inusual:
  
-   Cuentas de usuario y grupos extraños.
  
-   Nombres de usuario que no parecen corresponderse a ningún usuario existente.
  
-   Grupos que contengan miembros no válidos.
  
-   Derechos de usuario no válidos.
  
-   Privilegios elevados recientemente para una cuenta de usuario o grupo.
  
-   Por último, confirme que todos los miembros del grupo Administrador son válidos.
  
Utilice el complemento de usuarios y grupos locales de Microsoft Management Console (MMC) para comprobar las incorporaciones inusuales al grupo de administradores local. Asimismo, consulte el registro de seguridad del equipo local para saber si hay entradas inusuales. Por ejemplo, las entradas de la categoría "Administración de cuentas" como el suceso 636 indican que se ha agregado un nuevo miembro al grupo local. Estos registros también facilitan la fecha y la hora del cambio.
  
Si el sistema que se analiza es un servidor Windows, utilice el complemento de usuarios y grupos de Active Directory de MMC para examinar también la pertenencia al grupo del dominio. Para obtener más información sobre los usuarios y grupos predeterminados para Windows 2000, consulte la página "Default User Accounts and Groups" en Microsoft TechNet:  
<http://www.microsoft.com/technet/prodtechnol/windows2000serv/evaluate/featfunc/07w2kadb.mspx> (en inglés) y el artículo de Knowledge Base "243330: Well Known Security Identifiers in Windows Server Operating Systems", que ofrece información sobre los identificadores de seguridad (SID) conocidos y la información de usuarios y grupos asociada, en Microsoft.com:  
<http://support.microsoft.com/?kbid=243330>
  
**Nota**: aunque los artículos describen el sistema operativo Windows 2000, la información también se aplica a Windows 2003, ya que los grupos predeterminados básicos no han cambiado de una versión a otra. Sin embargo, sí se han introducido en Windows Server 2003 grupos predeterminados adicionales, como los grupos especiales Servicio de red y Servicio local. Consulte la configuración predeterminada del sistema para ver detalles.
  
##### Comprobación de las carpetas compartidas
  
Otro comportamiento común del software malintencionado es el uso de carpetas compartidas para extender la infección. Compruebe el estado de las carpetas compartidas en el sistema infectado con el complemento Administración de equipos de MMC o desde la línea de comandos con el comando **NetShare***. Las tablas que se muestran a continuación ilustran los recursos compartidos predeterminados presentes en los clientes y servidores Windows.*
  
**Nota**: de forma predeterminada, los equipos Windows 9*x* no comparten archivos o carpetas a menos que se habilite el uso compartido de archivos. Asimismo, los clientes Windows 9*x* no disponen de recursos compartidos "admin$" o equivalentes; únicamente las carpetas o volúmenes que se han compartido específicamente están disponibles en la red (salvo el sistema comprometido o algún software de control remoto instalado en el mismo).
  
**Tabla 4.1: Recursos compartidos de carpeta predeterminados de Windows XP**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Carpeta compartida</p></th>
<th><p>Ruta compartida</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>ADMIN$</p></td>
<td style="border:1px solid black;"><p>C:\Windows</p></td>
<td style="border:1px solid black;"><p>Administración remota</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>C$</p></td>
<td style="border:1px solid black;"><p>C:\</p></td>
<td style="border:1px solid black;"><p>Recurso compartido predeterminado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>&lt;n&gt;$</p></td>
<td style="border:1px solid black;"><p>&lt;n:&gt;\</p></td>
<td style="border:1px solid black;"><p>Representa un recurso compartido para la raíz de cada unidad fija del sistema.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SharedDocs</p></td>
<td style="border:1px solid black;"><p>C:\Documents and Settings\All Users\Documents</p></td>
<td style="border:1px solid black;"><p>Se agregará si se ha habilitado el uso compartido de archivos locales.</p></td>
</tr>
</tbody>
</table>
  
**Tabla 4.2: Recursos compartidos de carpeta predeterminados de Windows Server 2003 y Windows 2000 Server**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Carpeta compartida</p></th>
<th><p>Ruta compartida</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>ADMIN$</p></td>
<td style="border:1px solid black;"><p>C:\Windows</p></td>
<td style="border:1px solid black;"><p>Administración remota</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>C$</p></td>
<td style="border:1px solid black;"><p>C:\</p></td>
<td style="border:1px solid black;"><p>Recurso compartido predeterminado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>&lt;n&gt;$</p></td>
<td style="border:1px solid black;"><p>&lt;n:&gt;\</p></td>
<td style="border:1px solid black;"><p>Representa un recurso compartido para la raíz de cada unidad fija del sistema.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SharedDocs</p></td>
<td style="border:1px solid black;"><p>C:\Documents and Settings\All Users\Documents</p></td>
<td style="border:1px solid black;"><p>Se agregará si se ha habilitado el uso compartido de archivos locales.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Wwwroot$</p></td>
<td style="border:1px solid black;"><p>C:\inetpub\wwwroot</p></td>
<td style="border:1px solid black;"><p>Se configurará si Servicios de Internet Information Server (IIS) se ha instalado como servidor Web.</p></td>
</tr>
</tbody>
</table>
  
También puede examinar los permisos en estos recursos compartidos con la herramienta de la línea de comandos **SrvCheck** de la página "Windows Server 2003 Resource Kit Tools" en Microsoft.com: [http://go.microsoft.com/fwlink/?LinkId=4544](http://go.microsoft.com/fwlink/?linkid=4544) (en inglés).
  
O bien utilizar otras utilidades de terceros como **Dumpsec**, que puede descargar desde el sitio Web de SystemTools.com: [http://www.somarsoft.com](http://www.somarsoft.com/) (en inglés), para generar estos informes.
  
##### Comprobación de los puertos de red abiertos
  
Muchos ataques de software malintencionado intentan debilitar los sistemas afectados para preparar el camino para ataques futuros. Una técnica que suelen emplear los atacantes consiste en abrir puertos de red en el host para posteriormente utilizarlos como ruta adicional al mismo.
  
Existen distintas herramientas que se pueden emplear para exportar una lista de la configuración actual de los puertos de la red, entre las que se incluye **PortQRY**, perteneciente a las herramientas de soporte de Microsoft Windows Server 2003. Para obtener más información sobre esta herramienta, consulte el artículo de Microsoft Knowledge Base "832919: New features and functionality in PortQry version 2.0" en Microsoft.com: <http://support.microsoft.com/?kbid=832919>
  
Otra herramienta para este propósito es la utilidad de la línea de comandos **FPort** de Foundstone, que se encuentra disponible en: [http://www.foundstone.com](http://www.foundstone.com/) (en inglés).
  
Por último, también se puede hacer uso de la utilidad de la línea de comandos **NetStat**, que se proporciona con Windows, para documentar el estado de las conexiones y puertos de red a la escucha e imprimir una copia del mismo si así se desea.
  
**Para crear un informe de NETSTAT**
  
-   En el host infectado, haga clic en **Inicio**, **Ejecutar**, escriba **Netstat -an** &gt;c:\\netstat\_report.txt y presione **ENTRAR**.
  
    **Nota**: si Netstat se ejecuta en Windows XP o posterior, también puede utilizar el siguiente comando, con el que se incluirá el identificador de proceso (PID) asociado en el informe:
  
    Netstat -ano &gt;c:\\netstat\_report.txt
  
Se creará un archivo de texto llamado **netstat\_report.txt** (nombre al que puede agregar la fecha si así lo desea) en la raíz de la unidad C:. Este archivo se debe guardar en un medio extraíble para un análisis posterior.
  
##### Uso de un analizador de protocolos de red
  
Esta herramienta se puede emplear para crear un registro de los datos de tráfico en la red que se trasmiten a y desde el host infectado. El archivo de seguimiento de la red que se obtenga se debe guardar como parte de un conjunto de archivos de información para análisis posteriores.
  
Entre los ejemplos de analizadores que permiten crear este tipo de archivos se encuentra el componente Monitor de red de Microsoft Systems Management Server (SMS) y otras herramientas de terceros como el analizador Ethereal, disponible en el sitio Web de Ethereal en: <http://www.ethereal.com/> (en inglés).
  
##### Comprobación y exportación de los registros de sucesos del sistema
  
Los registros de sucesos del sistema de Windows pueden servir para localizar una amplia gama de comportamientos inusuales que permiten identificar los cambios realizados por el software malintencionado, así como el momento en que se produjeron. La consola de administración Visor de sucesos se puede utilizar para guardar cada tipo de archivo del registro de sucesos (aplicación, seguridad y sistema) en medios extraíbles para un análisis posterior. De forma predeterminada, estos archivos, que se almacenan en el directorio C:\\Winnt\\System32\\Config\\, se llaman **AppEvent.evt**, **SecEvent.evt** y **SysEvent.evt**. No obstante, tenga en cuenta que mientras el sistema está activo, estos archivos se encuentran bloqueados y se deben exportar con la herramienta de administración Visor de sucesos.
  
Las siguientes sugerencias proporcionan información sobre el modo en que estos registros se pueden utilizar para determinar los efectos de los ataques de software malintencionado:
  
-   Busque los cambios realizados en el momento que se produjo el posible ataque.
  
-   Compare las horas de los registros de sucesos con las horas de creación y modificación de los archivos.
  
-   Busque las cuentas que se hayan creado o cuyas contraseñas se hubieran modificado en el momento de la posible intrusión.
  
Después de completar el proceso de análisis del software malintencionado, puede intentar volver a conectar las redes aisladas, siempre teniendo en cuenta si la naturaleza del ataque lo permite. Por ejemplo, si el análisis determina que el software malintencionado sólo se transmite a través de una aplicación de igual a igual (P2P) concreta, podrá restaurar las redes y otros servicios con un simple cambio de los filtros del servidor de seguridad perimetral para bloquear los puertos de red utilizados por dicha aplicación. Esta solución puede restaurar las comunicaciones de una organización a un nivel prácticamente normal mientras se lleva a cabo el proceso de recuperación del sistema.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Paso 4: Recuperación del sistema
  
Una vez que ha recopilado toda la información necesaria sobre el ataque y ha comprendido su naturaleza, puede iniciar el proceso de eliminación del software malintencionado y de recuperación de los datos dañados en los equipos infectados.
  
**Importante**: aunque disponga de una aplicación antivirus que pueda reconocer y limpiar un equipo que ha sufrido un ataque de software malintencionado, Microsoft recomienda que determine la fecha y la hora de la infección, así como el modo en que se produjo. Sin esta información resulta difícil determinar qué otros sistemas, medios de copia de seguridad o medios extraíbles estuvieron expuestos.
  
La forma en que complete este proceso dependerá en gran medida de la naturaleza del ataque en concreto. No obstante, puede utilizar el siguiente proceso de alto nivel para garantizar la completa recuperación de los datos y los sistemas:
  
1.  Restaurar los datos perdidos o dañados.
  
2.  Eliminar o limpiar los archivos infectados.
  
3.  Confirmar que en los equipos no hay software malintencionado.
  
4.  Volver a conectar los equipos a la red.
  
La confirmación de que el sistema está libre de software malintencionado es un paso esencial que no debe omitirse, ya que muchas amenazas están diseñadas para permanecer en la sombra durante largos períodos de tiempo. Asimismo, las imágenes de copia de seguridad o los puntos de restauración del sistema pueden incluir archivos de sistema infectados, lo que puede producir otra infección si una imagen infectada se utiliza como origen para la recuperación. Por estos motivos, resulta vital determinar la fecha y la hora de la primera instancia del ataque, si es posible. Una vez que disponga de una marca de tiempo como referencia, mediante las fechas de las imágenes de copia de seguridad puede determinar si es probable que alguna de ellas incluya el mismo tipo de amenaza.
  
#### ¿Limpieza o reconstrucción?
  
Son las dos opciones disponibles cuando se trata de decidir cómo recuperar el sistema. La primera de ellas, la limpieza del sistema, se basa en las características conocidas del ataque para intentar deshacer de forma sistemática el daño que ha causado cada una de ellas en el sistema. La segunda opción se suele denominar reconstrucción o *acoplamiento* de un sistema. Sin embargo, la dificultad radica en decidir cuál de ellas utilizar.
  
La limpieza del sistema únicamente se debe seleccionar si se está completamente seguro de que todos los elementos del ataque se han documentado debidamente y que el proceso solucionará todos los problemas de forma satisfactoria. Los proveedores de antivirus suelen proporcionar la documentación necesaria, pero pueden tardar varios días en analizar y comprender la naturaleza del ataque. Se suele preferir la opción de limpieza del sistema porque lo devuelve a su estado anterior con las aplicaciones y los datos intactos. Este enfoque también suele suponer una vuelta más rápida a las operaciones normales si se compara con la opción de reconstrucción. No obstante, si no se realiza un análisis detallado del código malintencionado, puede que la limpieza no elimine el problema por completo.
  
El riesgo fundamental de la limpieza del sistema radica en la posibilidad de que no se haya detectado o documentado algún elemento de la infección inicial o una posible segunda infección, por lo que el sistema puede continuar infectado o ser susceptible de un sufrir un ataque de software malintencionado. Debido a este riesgo, muchas organizaciones seleccionan simplemente la reconstrucción de sus sistemas infectados para tener la total seguridad de que el software malintencionado ya no está presente en ellos.
  
En líneas generales, Microsoft recomienda la reconstrucción siempre que un sistema haya sufrido un ataque donde se hayan instalado una puerta trasera o un rootkit. Para obtener más información sobre este tipo de ataques, consulte el capítulo 2 de esta guía, "Amenazas de software malintencionado". Los distintos componentes de estos ataques son difíciles de detectar con seguridad y suelen volver a aparecer tras varios intentos de eliminación. Normalmente su objetivo es obtener acceso no autorizado a los sistemas infectados para posteriormente iniciar otros ataques que les permitan elevar sus privilegios o instalar su propio software. Por ello, la única forma de estar completamente seguro de que el equipo está libre de software malintencionado es la reconstrucción a partir de medios de confianza y el establecimiento de opciones de configuración que solucionen las vulnerabilidades que permitieron que se produjera el ataque inicial, por ejemplo, no haber aplicado las actualizaciones de seguridad o haber utilizado contraseñas poco seguras.
  
Este proceso también requiere una cuidadosa recopilación y evaluación de todos los datos importantes del usuario del sistema infectado, la reparación de los elementos dañados, la comprobación de los datos para confirmar que no contienen software malintencionado y finalmente la restauración de los datos limpios en el sistema reconstruido.
  
La reconstrucción del sistema también implica la reinstalación de las aplicaciones disponibles anteriormente y su adecuada configuración. Por lo tanto, aunque la reconstrucción proporciona el máximo nivel de seguridad en cuanto a la eliminación de la infección o ataque, suele resultar un proceso mucho más largo que la limpieza.
  
El factor principal a considerar en la elección de una opción u otra es el nivel de confianza que tenga en cada una de ellas para eliminar completamente y resolver la infección o el ataque. El tiempo de inactividad necesario durante la reparación debe ser una consideración secundaria, ya que lo que se persigue es la integridad y la estabilidad del sistema.
  
**Tabla 4.3: Ventajas y desventajas de la limpieza y la reconstrucción del sistema**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Limpieza</p></th>
<th><p>Reconstrucción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Proceso sencillo, si se dispone de herramientas de limpieza.</p></td>
<td style="border:1px solid black;"><p>Proceso más complejo, especialmente si no se cuenta con una solución de copia de seguridad o recuperación antes de la infección.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>La limpieza de los datos se realiza en menos pasos.</p></td>
<td style="border:1px solid black;"><p>Los pasos a seguir son más numerosos: capturar, realizar copias de seguridad, limpiar, examinar y restaurar los datos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Las herramientas de eliminación utilizan menos recursos que la reconstrucción completa del sistema.</p></td>
<td style="border:1px solid black;"><p>El proceso de reconstrucción puede requerir una cantidad de tiempo significativa y consumir muchos recursos.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Existe el riesgo de que el sistema aún esté infectado.</p></td>
<td style="border:1px solid black;"><p>Escaso riesgo de que el sistema aún esté infectado si se restaura a partir de medios limpios y datos administrados de forma correcta.</p></td>
</tr>
</tbody>
</table>
  
**Nota**: si se opta por la limpieza de un sistema infectado, los equipos legales y de administración de la organización deben llevar a cabo un análisis de riesgos para determinar si están dispuestos a aceptar la posibilidad de un futuro ataque si el proceso de limpieza no elimina parte del código malintencionado.
  
#### Limpieza del sistema
  
Esta opción resultará viable únicamente si los ataques y el comportamiento del software malintencionado se encuentran documentados y la confiabilidad de los procedimientos de limpieza se ha comprobado. Microsoft y otros proveedores de antivirus pueden proporcionar a los administradores la documentación sobre los pasos a seguir o facilitarles herramientas automatizadas que limpien la infección del sistema. Ambas opciones pretenden deshacer cada una de las acciones realizadas durante la infección para devolver el sistema a su estado operativo original. Generalmente, estos procedimientos sólo están disponibles para hacer frente a virus o gusanos muy graves y varios días después de la infección inicial.
  
**Nota**: como los ataques de software malintencionado se suelen producir en cadena, por ejemplo, MyDoom@A, MyDoom@B, etc, es muy importante utilizar solamente procedimientos o herramientas de limpieza que eliminen la versión específica del software malintencionado del sistema.
  
Si no se puede contar con una herramienta automatizada para el contrarrestar el ataque, algunos de los pasos básicos que se deben considerar si se opta por la limpieza manual son los siguientes:
  
1.  Detener los procesos de ejecución del software malintencionado. Es necesario finalizar todos los procesos relacionados con el ataque que se estén ejecutando en ese momento, así como las entradas de ejecución automática o tareas programadas asociadas al software malintencionado que se pretende eliminar.
  
2.  Eliminar los archivos introducidos por el software malintencionado. Para este paso será necesario realizar un análisis detallado de los archivos de las unidades de disco del host para determinar cuáles están afectados.
  
3.  Aplicar las actualizaciones o revisiones de seguridad más recientes para solucionar las vulnerabilidades aprovechadas por el ataque original. Este paso puede obligar a reiniciar el sistema en varias ocasiones y visitar el sitio Web de Windows Update varias veces para comprobar que se han aplicado todas las actualizaciones de seguridad.
  
4.  Cambiar las contraseñas (de dominio o locales) que se puedan haber visto comprometidas o las que resulten poco seguras o fáciles de averiguar. Para obtener información sobre la configuración de contraseñas seguras, consulte la página "Strong Passwords" en Microsoft.com:  
    [http://www.microsoft.com/resources/documentation/WindowsServ/2003/enterprise/proddocs/en-us/windows\_password\_tips.asp](http://www.microsoft.com/resources/documentation/windowsserv/2003/enterprise/proddocs/en-us/windows_password_tips.asp) (en inglés).
  
5.  Deshacer los cambios realizados por el software malintencionado en el sistema. Este paso puede implicar la restauración de las configuraciones del servidor de seguridad y los archivos del host local del equipo.
  
6.  Restaurar los archivos de usuario modificados o eliminados por el software malintencionado.
  
Si opta por realizar manualmente estos pasos, tenga en cuenta que será necesario compararlos posteriormente con procedimientos de limpieza publicados para asegurarse de que los ha realizado todos y que pueden solucionar la infección. O bien, si su organización cuenta con un equipo de soporte antivirus, también será preciso que compruebe que los procedimientos de inspección y recuperación utilizados para identificar y reparar todos los posibles vectores de ataque resultan adecuados. Si no se hace así, la infección podría volver a producirse.
  
#### ¿Restauración o reinstalación?
  
Si decide que el mejor enfoque es reconstruir el sistema, la restauración se puede llevar a cabo utilizando una imagen o copia de seguridad anterior del sistema que esté libre de software malintencionado, o bien, volviendo a instalar el sistema a partir de los medios originales.
  
Si opta por la opción de la imagen anterior, guarde los datos más recientes del usuario del sistema infectado para evitar la pérdida de las actualizaciones o cambios aplicados desde la fecha en la que se realizó la copia de seguridad. Con la segunda opción, la reconstrucción a partir de los medios originales en lugar de con una copia de seguridad, la única forma de evitar la pérdida de los datos del sistema infectado es almacenarlos.
  
##### Recuperación de los datos del sistema infectado
  
Probablemente el activo más importante con el que cuente el sistema sean los datos que residen en él. Por ello, es fundamental diseñar una estrategia que permita almacenarlos, repararlos, realizar una copia de seguridad de ellos y posteriormente restaurarlos en el sistema reconstruido.
  
Asegúrese de guardar correctamente los siguientes tipos de datos para poder restaurar el sistema por completo:
  
-   **Datos de configuración del sistema operativo**. Esta información incluye todas las opciones de configuración necesarias para restaurar el sistema operativo del host a su estado original y garantizar que todos sus servicios funcionan correctamente.
  
-   **Datos de aplicaciones**. Se incluyen todos los datos utilizados y almacenados en las aplicaciones que se encuentran instaladas en el dispositivo host.
  
-   **Datos de los usuarios**. Se incluyen todos los datos de configuración, por ejemplo, perfiles y archivos generados por los usuarios.
  
    **Nota**: obviamente, estos datos que se guardan representan un riesgo de infección, por lo que se debe prestar especial atención a cómo se trabaja con ellos hasta que se haya identificado un método confiable que permita determinar si están infectados.
  
Realice una copia de seguridad de todos los datos en un medio o ubicación seguros donde no puedan ejecutarse ni estar a disposición de sistemas o usuarios no autorizados. Utilice las herramientas o medios necesarios de los que disponga para restaurar y almacenar los datos y, posteriormente, restaurarlos en el sistema una vez reconstruido.
  
##### Restauración desde una imagen o copia de seguridad
  
Para poder restaurar los datos a partir de una imagen o copia de seguridad, será necesario haberlos capturado previamente con una herramienta de recuperación antes de que la infección comprometiera el sistema. Existe una gran variedad de herramientas que pueden simplificar en gran medida la tarea de copia de seguridad y recuperación de datos de los sistemas. Estas herramientas ofrecen un alto nivel de garantía en la protección de los sistemas no sólo frente a infecciones de software malintencionado, sino también frente a errores del hardware y otras posibles amenazas. La configuración de una infraestructura de recuperación completa no entra dentro del ámbito de esta guía. No obstante, en las siguientes secciones se analizan algunas tecnologías clave pertenecientes a este área que se pueden utilizar para tratar problemas relacionados con los virus.
  
**Restauración del sistema de Windows**  
La restauración del sistema de Windows (WSR) protege archivos de aplicaciones y del sistema de vital importancia mediante el control, el registro y, en ciertos casos, la copia de seguridad de los mismos antes de que se modifiquen. Es importante saber si su aplicación antivirus es compatible con WSR, ya que esta utilidad puede crear un punto de restauración que podría infectarse con software malintencionado si se utiliza para limpiar el sistema en cualquier momento tras el ataque inicial. El software malintencionado podría volver a introducirse en el sistema mediante el punto de restauración infectado. Por suerte, una aplicación antivirus compatible con WSR detectará el problema durante un proceso de restauración. Si se detectan archivos infectados, la solución antivirus intentará modificarlos, moverlos o eliminarlos. Si los archivos se limpian correctamente, WSR se encargará de restaurarlos. Sin embargo, si algún archivo no se puede limpiar y se elimina o pone en cuarentena, el proceso de restauración generará un error al producir este aislamiento un estado de restauración incoherente. Si es el caso, WSR devolverá el sistema a su estado anterior (antes de que comience la operación de restauración).
  
Para obtener más información sobre el funcionamiento de las aplicaciones antivirus con este servicio, consulte el artículo de Knowledge Base "831829: How antivirus software and System Restore work together" en Microsoft.com: <http://support.microsoft.com/?kbid=831829>
  
**Nota**: como los archivos de firma de virus se actualizan para evitar un ataque de software malintencionado, puede que una restauración que generara error días atrás funcione ahora correctamente (una vez actualizada la aplicación antivirus). Y al contrario, si la restauración se ha realizado a un punto que resultó adecuado anteriormente pero un nuevo archivo de firma activa la detección de un ataque en un archivo de copia de seguridad que no se puede limpiar, puede se genere un error en el proceso de restauración.
  
Para obtener más información sobre WSR, consulte la página "How to Restore Windows XP to a Previous State" en Microsoft.com:  
<http://www.microsoft.com/windowsxp/pro/using/itpro/managing/restore.asp> (en inglés).
  
**Recuperación automatizada del sistema**  
La recuperación automatizada del sistema (ASR) permite, de una forma sencilla y rápida, realizar copias de seguridad de los volúmenes de inicio y del sistema en el equipo, lo que propiciará una restauración más pronta en caso de error o infección. No obstante, al igual que sucede con cualquier otro medio de copia de seguridad, es posible que los archivos de copia de ASR resulten infectados por software malintencionado. Para obtener más información sobre ASR y su uso, consulte las notas del producto "How ASR Works" en Microsoft.com: [http://www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/sdcbc\_sto\_axho.asp](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/sdcbc_sto_axho.asp) (en inglés).
  
**Solución de copia de seguridad de Windows**  
La solución de copia de seguridad que se proporciona como parte de la familia de sistemas operativos Windows ofrece un sencillo mecanismo de copia para entornos empresariales de pequeño y mediano tamaño. No obstante, al igual que sucede con WSR y ASR, los propios archivos de copia de seguridad pueden contener software malintencionado. Por ello, si emplea esta solución, compruebe que el software malintencionado no se restaura en el sistema y que no se reinicia el ataque. Todos los archivos de copia de seguridad se deben comprobar y examinar con una aplicación antivirus actualizada que sea capaz de detectar y eliminar la infección antes de que se utilice una imagen de copia de seguridad para restaurar el sistema. Para obtener documentación detallada sobre la recuperación de desastres, incluidas las operaciones de copia de seguridad y restauración, consulte la sección "Planning for Disaster Recovery" de *Windows Server 2003 Deployment Kit* en Microsoft.com: [http://www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/sdcbc\_sto\_gqda.asp](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/sdcbc_sto_gqda.asp) (en inglés).
  
##### Reinstalación del sistema
  
Una vez que haya comprobado la seguridad de los datos de copia de seguridad, puede iniciar el proceso de reconstrucción del sistema. Este punto del proceso resulta idóneo para dar formato a las unidades, cambiar los tamaños de las particiones y realizar otras tareas de mantenimiento del sistema necesarias para asegurar un rendimiento óptimo tras la restauración. Si es posible, reconstruya los servidores con un recurso compartido integrado totalmente actualizado. Para obtener más información sobre la creación de este tipo de instalaciones de Windows, consulte:
  
-   La sección "The Combination Installation" de *Microsoft Windows XP Hotfix Installation and Deployment Guide* en Microsoft.com:
  
    [http://www.microsoft.com/WindowsXP/pro/downloads/servicepacks/sp1/hfdeploy.asp\#the\_combination\_installation\_gxsi](http://www.microsoft.com/windowsxp/pro/downloads/servicepacks/sp1/hfdeploy.asp#the_combination_installation_gxsi) (en inglés).
  
-   La sección "Installing Windows 2000 with the Service Pack and Hotfixes" de *Windows 2000 Hotfix Installation and Deployment Guide* en Microsoft.com:
  
    [http://www.microsoft.com/windows2000/downloads/servicepacks/sp3/HFDeploy.htm\#installing\_windows\_2000\_with\_hotfixes\_ykot](http://www.microsoft.com/windows2000/downloads/servicepacks/sp3/hfdeploy.htm#installing_windows_2000_with_hotfixes_ykot) (en inglés).
  
Si no se puede realizar la reconstrucción con este origen, existe el riesgo de que el sistema se infecte con software malintencionado basado en la red antes de que se pueda realizar la conexión al sitio Web de Windows Update para descargar las actualizaciones de seguridad y los Service Packs necesarios. Si fuera así, siga los siguientes pasos para llevar a cabo la reinstalación:
  
1.  Desconecte el sistema de la red. La desconexión física del equipo de la red es el método más seguro.
  
2.  Instale el sistema operativo desde el medio de instalación del sistema original. Durante este proceso resulta fundamental crear contraseñas de administrador local seguras en cada equipo. Estas contraseñas deben ser exclusivas para cada sistema.
  
3.  Inicie el sistema y conéctese utilizando la cuenta de administrador local.
  
4.  Active un servidor de seguridad basado en host en el sistema, por ejemplo, el servidor de seguridad de conexión a Internet (ICF) de Windows XP.
  
    **Nota**: en Windows XP Service Pack 2, ICF ha cambiado de nombre para denominarse *Windows Firewall* y se habilita de forma predeterminada en todas las conexiones de red. Si el sistema se basa en Windows 2000 o una versión anterior, se recomienda la instalación de un servidor de seguridad basado en host de terceros.
  
5.  Vuelva a conectar el sistema a la red. En este momento es importante realizar los siguientes pasos con la mayor rapidez posible para reducir el riesgo del sistema que se desea reconstruir.
  
6.  Instale en el sistema las actualizaciones de software más recientes. Es importante tener en cuenta que no todas las actualizaciones de seguridad se incluyen en el sitio Web de Windows Update. Windows Update sólo proporciona las actualizaciones de seguridad más importantes del sistema operativo y no actualizaciones para otros productos como SQL Server™, Front Page, Commerce Server, etc. Por este motivo, consulte la página "Security Bulletin Search" en Microsoft TechNet: <http://www.microsoft.com/technet/security/default.mspx> (en inglés) para buscar actualizaciones específicas de productos.
  
7.  Instale un paquete antivirus, compruebe que utiliza la versión más reciente del archivo de firma de virus y realice una exploración antivirus completa del sistema.
  
8.  Refuerce la configuración del sistema con las instrucciones de blindaje más recientes de la organización. Consulte el capítulo 3 de esta guía, "Defensa en profundidad antivirus", para obtener información sobre este proceso.
  
9.  Compruebe si queda alguna vulnerabilidad en el sistema utilizando un examinador de vulnerabilidades como Microsoft Baseline Security Analyzer (MBSA). La descarga de esta herramienta gratuita se puede realizar en Microsoft.com:  
    <http://www.microsoft.com/technet/security/tools/mbsahome.mspx> (en inglés).
  
Tras la reconstrucción y examen del sistema para comprobar que ya no existe ningún archivo infectado, la restauración de los datos de usuario se podrá realizar con seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Paso 5: Postrecuperación
  
En esta sección se proporcionan instrucciones sobre los pasos concretos que se deben realizar tras el control y la recuperación de un primer ataque. Es importante completar esta fase para ayudar al fortalecimiento de las directivas generales de su organización en cuanto a usuarios, procesos y tecnologías.
  
#### Reunión de revisión posterior al ataque
  
A esta reunión deben acudir todas las partes afectadas, que deberían intercambiar las experiencias aprendidas en beneficio de todos. Concretamente, los participantes deben considerar los siguientes puntos:
  
-   Trabajar con los asesores jurídicos para determinar si la organización debe adoptar medidas legales frente a los atacantes.
  
-   Consultar con los asesores jurídicos para decidir si la organización debe informar del ataque a las autoridades correspondientes si se pusieron en peligro datos importantes. Por ejemplo, información sobre tarjetas de crédito.
  
-   Evaluar económicamente los daños sufridos para generar un informe interno que incluya los siguientes elementos:
  
    -   Las horas empleadas en la recuperación.
  
    -   El coste de reparación del equipo dañado.
  
    -   La pérdida de beneficios.
  
    -   Los costes o daños causados a clientes y socios comerciales.
  
    -   La pérdida de productividad de los trabajadores afectados.
  
    -   El valor de los datos perdidos.
  
-   Identificar las vulnerabilidades del sistema aprovechadas por el software malintencionado para fines ilícitos.
  
-   Recomendar cambios en la directiva de defensa en profundidad antivirus de la organización.
  
-   Recomendar modificaciones en la directiva de seguridad de la organización, incluyendo:
  
    -   Una directiva más exhaustiva de contraseñas predeterminada.
  
    -   Directivas de auditoría.
  
    -   Directiva de actualizaciones de seguridad.
  
    -   Directivas de servidor de seguridad.
  
#### Actualizaciones posteriores al ataque
  
Se deben revisar y evaluar las recomendaciones resultantes de la reunión para asegurar su pronta implementación en la organización. Una vez expuesta una vulnerabilidad específica, existen distintos enfoques disponibles que se pueden emplear de forma simultánea para solventarla.
  
Es importante tener en cuenta que estos cambios pueden afectar a usuarios, procesos y tecnologías de la organización. La revisión del coste calculado del ataque debe servir para subrayar los beneficios futuros que puede obtener la organización al contar con una estrategia activa que evite la nueva aparición de los ataques.
  
Llegados este punto, si su organización aún no ha implementado un enfoque de defensa en profundidad antivirus, consulte el capítulo 3 de esta guía, "Defensa en profundidad antivirus", para revisar qué elementos de dicho enfoque pueden suponer mayores beneficios para su empresa.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se ofrecen instrucciones y recomendaciones que se pueden utilizar para la recuperación de un ataque de software malintencionado de manera planeada y coherente. Es importante seguir cada uno de los pasos sugeridos, ya la omisión o la mala interpretación de alguno de ellos podría suponer un nuevo riesgo de ataque para su organización. Asimismo, esto podría dificultar o impedir que su organización tomara medidas legales contra al atacante.
  
Si implementa una solución de defensa en profundidad antivirus, es muy probable que el número de veces que tenga que hacer frente a los ataques con ella se reduzca al mínimo. Sin embargo, si no dispone de una solución anticipada que esté preparada para hacer frente a los peores escenarios, las probabilidades de cometer errores más graves cuando un ataque real anule sus defensas son bastante altas.
  
Es preciso estar preparado para cualquier eventualidad de antemano ofreciendo al personal encargado de la seguridad toda la información sobre las técnicas utilizadas más comúnmente por el software malintencionado (como las descritas en este capítulo). Asimismo, una sugerencia muy útil es crear un kit de herramientas de análisis de software malintencionado que incluya algunas de las mencionadas aquí, así como secuencias de comandos y otras utilidades que se puedan emplear para capturar y documentar con rapidez la información importante de los sistemas infectados. Esta preparación contribuirá a reducir el impacto de los ataques de software malintencionado en las operaciones de su organización si los sistemas se ven afectados.
  
Cada nuevo ataque puede introducir distintos métodos para comprometer o dañar los sistemas. Por ello, Microsoft recomienda la consulta del sitio Web de información de protección frente a virus en: <http://www.microsoft.com/security/antivirus/> (en inglés). En este sitio se ofrecen información antivirus actualizada e instrucciones sobre cómo hacer frente a los ataques de software malintencionado más recientes. El uso de los recursos presentados en este capítulo le ayudará a controlar de manera eficaz el impacto de los ataques en su organización y a realizar la recuperación de forma eficaz y segura.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Reconocimientos
  
El grupo Microsoft Solutions for Security (MSS) desea agradecer y reconocer la labor realizada por el equipo que elaboró la *Guía* *de defensa en profundidad antivirus*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, elaboración y comprobación de esta solución.
  
[](#safd)[Autor](#safd)  
[](#sytd)[Editores](#sytd)  
[](#ystd)[Evaluadores](#ystd)  
[](#tsyd)[Comité de revisión del contenido sobre seguridad](#tsyd)  
[](#tsir)[Director del programa](#tsir)  
[](#tupl)[Revisores (en orden alfabético)](#tupl)  
[](#trwq)[Colaboradores (en orden alfabético)](#trwq)
  
### Autor
  
Richard Harrison – Content Master Ltd
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Editores
  
John Cobb – Volt Information Sciences
  
Steve Wacker – Volt Information Sciences
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Evaluadores
  
Gaurav Singh Bora – Infosys Technologies Ltd
  
Balkrishnan Venkiteswaran – Infosys Technologies Ltd
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comité de revisión del contenido sobre seguridad
  
Rich Benack, Security Support Engineer – Microsoft Product Support Services (PSS)
  
Matt Braverman, Program Manager – Microsoft Security Business and Technology Unit (SBTU)
  
Martin Fallenstedt, Development Lead – Microsoft Windows Security Core
  
Robert Hensing, Technical Lead – Microsoft Product Support Services (PSS)
  
Daryl Pecelj, Senior Antivirus Technician – Microsoft IT
  
Randy Treit, Program Manager – Microsoft SBTU
  
Jeff Williams, Security Privacy Officer – Microsoft PSS (revisor principal)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Director del programa
  
Jeff Coon – Volt Information Sciences
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Revisores (en orden alfabético)
  
Ken Anderson, Security Solutions Technical Account Manager – Microsoft Consulting
  
Ignacio Ayerbe, Director of Strategic Alliances – Panda Software
  
Steve Clark, Systems Design Engineer – MSS
  
J.P. Duan, Group Manager of Antivirus Security Response – Microsoft SBTU
  
Marius Gheorghescu, Software Design Engineer – Microsoft SBTU
  
Yolanda Ruiz Hervas – Panda Software
  
Mikko Hypponen, Director of Antivirus Research – F-Secure Corporation
  
Maxim Kapteijns, Senior Program Manager – Microsoft Consulting
  
Mady Marinescu, Development Lead – Microsoft SBTU
  
Brian May, Systems Design Engineer – MSS
  
Sami Rautiainen, Antivirus Researcher – F-Secure Corporation
  
Anil Francis Thomas, Development Manager – Microsoft SBTU
  
Jessica Zahn, International Program Manager – Microsoft Publications
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Colaboradores (en orden alfabético)
  
Eric Cameron, SCRB Program Manager – Volt Information Sciences
  
Philippe Goetschel – Product Unit Manager SBTU
  
Joanne Kennedy, Group Program Manager – MSS
  
Kelly McMahon, User Experience – Content Master Ltd
  
Jeff Newfeld, Product Unit Manager – MSS
  
Rob Oikawa, Architect – MSS
  
Adrien Ransom, Business Development Manager – Microsoft SBTU
  
Bill Reid, Group Product Manager – MSS
  
Bomani Siwatu, Test Lead – MSS
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar la solución completa**
  
[**Guía de defensa en profundidad antivirus**](http://go.microsoft.com/fwlink/?linkid=28734&clcid=0x409)
  
[Ver todos los temas sobre instrucciones de seguridad](http://technet.microsoft.com/es-es/security/bb977553.aspx)
  
[](#mainsection)[Principio de la página](#mainsection)
