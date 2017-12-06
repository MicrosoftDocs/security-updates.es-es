---
TOCTitle: Protección de una red frente a clientes no administrados
Title: Protección de una red frente a clientes no administrados
ms:assetid: '9a90dd07-0efb-4151-bf99-629448130645'
ms:contentKeyID: 20200270
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875843(v=TechNet.10)'
---

Protección de una red frente a clientes no administrados
========================================================

### En esta página

Publicado: 29/08/2006

[](#efaa)[Introducción](#efaa)  
[](#eeaa)[Definición](#eeaa)  
[](#edaa)[Desafíos](#edaa)  
[](#ecaa)[Soluciones](#ecaa)  
[](#ebaa)[Resumen](#ebaa)  
[](#eaaa)[Apéndice A: Protección de acceso a redes](#eaaa)

### Introducción

Bienvenido a este documento de la colección Guías de seguridad para medianas empresas. Microsoft espera que esta información le ayude a crear un entorno informático más seguro y productivo.

### Resumen ejecutivo

En el contexto actual de preocupación por la seguridad, el conseguir un tratamiento en profundidad sobre la protección de las redes de las medianas empresas y los datos que residen en ellas es un asunto muy complejo. Ya no basta con confiar en defensas perimetrales y antivirus exclusivamente para proteger los activos de la red y la información confidencial. Las organizaciones y los profesionales de seguridad ya saben que los riesgos de las redes internas, ya sean intencionados o accidentales, pueden ser incluso más peligrosos que las amenazas externas.

Para hacer frente al gran número de vulnerabilidades que suponen un riesgo para las medianas empresas, se realizan importantes inversiones tanto de tiempo como de recursos en áreas como la administración de revisiones, las soluciones antimalware y las iniciativas de administración de identidad. Para garantizar que estas inversiones se usan en toda la empresa con el fin de maximizar la efectividad de la inversión, la empresa debe encontrar la forma de aplicar directivas de seguridad de forma eficiente.

Los equipos independientes son sistemas que no se consideran como riesgos sustanciales, ya que no hay forma de determinar si cumplen con las directivas de seguridad establecidas. Estos equipos pueden suponer un problema tanto para los administradores de sistemas como para los profesionales de la seguridad. Los sistemas que no cumplen las directivas de seguridad establecidas implican una serie de riesgos, desde que son vulnerables a una infección por malware hasta que constituyen posibles plataformas para un ataque. No ha sido fácil administrar estos sistemas ni conseguir que cumplan con las directivas de seguridad.

En este documento se tratan algunos métodos efectivos que pueden ayudar a conseguir la conformidad con las directivas de seguridad. En este enfoque se maximizan las ventajas de los esfuerzos dedicados a la administración de riesgos y se agrega un nivel de seguridad adicional a las redes de medianas empresas, que le ayudarán a reducir los riesgos relacionados con los equipos que no sean de confianza y no administrados.

### Información general

Este documento consta de cuatro secciones principales que se centran en detalles para ayudar al lector a entender mejor los conceptos y principios relacionados con intentar proteger la red de una mediana empresa de los equipos no administrados. Estas cuatro secciones principales se resumen de la siguiente manera:

### Introducción

Esta sección proporciona un resumen ejecutivo del documento junto con información general de la estructura del mismo e información sobre la audiencia a quien va dirigido el documento.

### Definición

Esta sección proporciona algunos detalles y definiciones que resultarán útiles para comprender las soluciones explicadas en el documento.

### Desafíos

Esta sección describe algunos de los problemas comunes a los que una mediana empresa tendría que enfrentarse a la hora de determinar cómo conseguir protección frente a equipos no administrados y que no son de confianza. Sienta las bases generales sobre los problemas que trata este documento.

### Soluciones

En esta sección se tratan soluciones que ayudan a hacer frente al desafío que suponen los equipos no administrados al valorar los posibles métodos y tratar los problemas relacionados con el desarrollo de planes para solucionar el problema. También proporciona información acerca de los métodos de implementación y administración.

### Quién debería leer esta guía

El objetivo de este documento técnico es ayudar a los profesionales de la tecnología y a los administradores técnicos a comprender y tomar decisiones bien fundamentadas acerca de cómo proteger la red de una mediana empresa frente a las amenazas que suponen los dispositivos no administrados. Si bien los destinatarios no técnicos pueden usar este documento para comprender mejor este problema de seguridad concreto, resulta útil tener conocimientos básicos de los siguientes aspectos para poder comprender y aplicar totalmente el contenido de este documento.

Entre las tecnologías específicas tratadas se incluyen:

-   Autenticación IEEE 802.1X

-   Directivas IPsec

-   Seguridad de red

-   Microsoft® Systems Management Server 2003

-   Microsoft Windows Server™ 2003

-   Servicio de directorio Active Directory®

-   Microsoft Operations Management Server

-   Servicio de autenticación de Internet de Microsoft

-   Autenticación RADIUS

[](#mainsection)[Principio de la página](#mainsection)

### Definición

Esta guía está diseñada para usar el modelo de proceso de Microsoft Operations Framework (MOF), además de las funciones de administración de servicio (SMF) de administración de seguridad de MOF.

Específicamente, las soluciones presentadas en este documento recomiendan el uso de un proceso continuo en lugar de una implementación lineal para ayudar a mejorar la seguridad de la red frente a las amenazas de equipos no administrados.

En concreto, la aplicación de estas soluciones debe conllevar los pasos que se incluyen en la siguiente figura:

![](images/Cc875843.PNFUC01(es-es,TechNet.10).gif)

**Figura 1. Aplicación de MOF**

Como muestra la figura, cualquier respuesta a los problemas de seguridad que presenten los sistemas no administrados debe suponer procesos continuos de pruebas y ajustes, y no sólo problemas de planificación e implementación. Las amenazas que pueden afectar a una red de una mediana empresa están en constante cambio y los sistemas que protegen la red de una empresa deben adaptarse de forma continua a dichas amenazas.

La aplicación de las soluciones tratadas en este documento se ajusta a las funciones de administración de servicios (SMF) de administración de seguridad, que se describe a continuación:

-   Evaluar la exposición de la empresa e identificar los activos que se deben proteger.

-   Identificar las formas de reducir los riesgos que suponen los dispositivos desprotegidos a niveles aceptables.

-   Diseñar un plan para mitigar los riesgos para la seguridad.

-   Supervisar la eficiencia de los mecanismos de seguridad.

-   Volver a evaluar la efectividad y los requisitos de seguridad regularmente.

Para obtener más información acerca de MOF, consulte el sitio web de [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) en Microsoft TechNet en la dirección www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx.

Para obtener más información sobre la función SMF de administración de seguridad, consulte la página [Funciones de administración de seguridad](http://go.microsoft.com/fwlink/?linkid=37696) en http://go.Microsoft.com/fwlink/?LinkId=37696 (puede estar en inglés).

La administración de riesgos es el proceso mediante el cual se determina el nivel de riesgo aceptable de una organización, se evalúan los riesgos actuales, se buscan formas de alcanzar ese nivel de riesgo aceptable y se administra el riesgo. Si bien en este documento se tratan algunos conceptos de la administración de riesgos, un tratamiento en profundidad de la administración de riesgos supone un asunto independiente y, por tanto, merece un tema en exclusiva. Para obtener más información acerca del análisis y las evaluaciones de riesgos, consulte la [*Guía de administración de riesgos de seguridad*](http://go.microsoft.com/fwlink/?linkid=30794) en http://go.microsoft.com/fwlink/?linkid=30794 (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Desafíos

Entre algunos de los desafíos implicados en la protección frente a los equipos no administrados se incluyen:

-   Cómo evitar que los equipos no administrados tengan acceso a recursos de la red.

-   Cómo conseguir que los equipos itinerantes cumplan con las actualizaciones y las directivas.

-   Cómo aplicar directivas de seguridad establecidas en equipos que se conectan a la red en modo remoto.

-   Cómo proteger una red frente a dispositivos inalámbricos independientes.

-   Cómo detectar sistemas no administrados, como portátiles de proveedores o dispositivos personales, cuando se vayan a conectar a la red.

-   Cómo protegerse frente a otros dispositivos móviles como equipos y dispositivos de mano.

[](#mainsection)[Principio de la página](#mainsection)

### Soluciones

En la sección "Desafíos" se enumeran una serie de factores que se deben tener en cuenta al considerar cómo protegerse frente a las amenazas que suponen los equipos independientes no administrados para una red. Además de defender la red con cable interna tradicional, también se deben realizar pasos para ayudar a proteger la red inalámbrica y cualquier ruta de acceso remoto. Para cubrir todas las posibles formas en las que un dispositivo independiente se puede conectar a una red, la solución debe ser lo más completa posible.

En la siguiente sección se enumeran los desafíos mediante los siguientes métodos:

-   Uso del aislamiento de dominios y redes IPsec para evitar que los equipos no administrados tengan acceso a los recursos de la red.

-   Uso de la cuarentena de VPN para aplicar directivas de seguridad en equipos que se conectan a la red en modo remoto.

-   Uso de la autenticación 802.1X para protegerse frente a dispositivos inalámbricos que no sean de confianza.

-   Uso de SMS para detectar equipos no administrados cuando se conectan a la red.

**Nota**   En este documento se asume que el lector ya implementó procesos para asegurar que los equipos miembros que residen en las estructuras del dominio de la mediana empresa cumplen con los requisitos de revisiones y seguridad establecidos; además, en él se investigan métodos para aplicar la conformidad y protegerse frente a dispositivos que no cumplen estos requisitos. No es el objeto de este documento tratar cómo conseguir que los equipos cumplan o usen mecanismos de actualización de seguridad automáticos, como WSUS o las funciones de administración de revisiones de SMS.

### Evaluación

En esta sección se presentan algunas de las posibles respuestas que le ayudarán a enfrentarse al problema que suponen los equipos no administrados para las medianas empresas. También se incluyen algunas de las decisiones que se deben tomar antes de decidirse por alguna de estas respuestas. Cualquiera de las respuestas tratadas deberían servir para mejorar el nivel de seguridad de una red de una mediana empresa. Sin embargo, cuando se implementa como parte de un método de defensa en profundidad, las respuestas combinadas pueden suponer una respuesta más sofisticada a los problemas que aparecen en la sección "Desafíos".

### Uso de IPsec para aislar dominios y servidores

El aislamiento físico de equipos y redes no es un concepto nuevo. Se ha venido usando de varias formas durante años, principalmente cuando la implementación y prueba de las redes suponía un problema. Sin embargo, los antiguos métodos de aislamiento físico no se prestaban bien a la tarea de proteger los sistemas administrados frente a dispositivos no administrados potencialmente en riesgo. Esto resulta especialmente cierto en los entornos de red de negocios modernos donde los sistemas móviles están ganando terreno y está aumentando la demanda de soluciones automatizadas y flexibles. La siguiente tabla describe los métodos de aislamiento más comunes usados, junto con las dificultades relacionadas con su uso en esta capacidad.

**Tabla 1. Métodos de aislamiento de la red**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nivel OSI</th>
<th style="border:1px solid black;" >Método</th>
<th style="border:1px solid black;" >Problemas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nivel 1</td>
<td style="border:1px solid black;">Use un cableado distinto para los segmentos que se deben aislar de la red de confianza.</td>
<td style="border:1px solid black;"><ul>
<li>Costos asociados al uso de un nuevo cable para cada nueva conexión.</li>
<li>Mayor trabajo administrativo por el tendido de nuevos cables cuando se trasladen los usuarios.</li>
<li>Falta de flexibilidad y difícil administración si la empresa crece.</li>
<li>Mayor posibilidad de descuidos y errores debido a los mayores requisitos de administración.</li>
</ul>
<br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nivel 2</td>
<td style="border:1px solid black;">Use VLAN para crear subredes lógicas aisladas de la red de confianza.</td>
<td style="border:1px solid black;"><ul>
<li>Mayor costo relacionado con la actualización de las redes de conmutadores (switch fabric) para admitir las redes VLAN.</li>
<li>Más trabajo administrativo resultante del seguimiento de los cambios de red, los traslados de usuarios y las respuestas a las peticiones de conexiones de invitados.</li>
<li>Posibilidad de descuidos y errores cuando se trasladan varios usuarios o se usan dispositivos móviles.</li>
</ul>
<br />
</td>
</tr>
</tbody>
</table>
 

Como demuestra esta tabla, las redes de las empresas modernas necesitan una solución más flexible que les permita cumplir los estándares de seguridad que facilitan la protección frente a los sistemas no administrados. Si bien existen algunas soluciones de terceros para este problema, suponen la instalación del cliente en todas las estaciones de trabajo administradas y un grado adicional de complejidad para la red. Afortunadamente, las versiones actuales de Microsoft Windows tienen funciones integradas que permiten resolver este problema sin necesidad de software ni curvas de aprendizaje administrativas adicionales.

El aislamiento de dominios y servidores de Microsoft permite a los administradores de TI restringir la comunicación TCP/IP al aprovechar la directiva de grupo de Active Directory integrada e IPsec, lo que aporta las siguientes ventajas:

-   Usa el nivel de red del modelo OSI, lo que significa que puede traspasar los límites de los conmutadores y enrutadores.

-   Independiente de las limitaciones de redes físicas y redes de conmutadores.

-   Reduce el costo al aprovechar las funciones de autenticación integradas de los equipos basados en Windows.

-   Se trata de un proceso automatizado que no necesita el mantenimiento continuado que implican los cambios de red y los traslados de usuarios.

-   Permite no sólo autenticar los equipos de confianza sino también cifrar las comunicaciones entre los sistemas de confianza.

-   Aplica las directivas de seguridad al rechazar las conexiones de dispositivos no administrados.

-   Mejora la administración de recursos y la auditoría.

-   Permite aislar rápidamente recursos específicos si se produce un ataque.

Avances recientes realizados como respuesta a estos problemas tratan las preocupaciones habituales que rodean el uso de IPsec para proteger las comunicaciones. En concreto, la traducción de direcciones de red (NAT) ya no supone un problema gracias a las capacidades de NAT Traversal disponibles en las versiones actuales de Microsoft Windows, como Windows Server 2003 y Microsoft Windows XP con Service Pack 2 (SP2). Además, se admiten las plataformas que no son IPsec mediante listas de exención configurables y/o una excepción de reserva para permitir la comunicación de texto sin cifrar con dichos sistemas.

Las soluciones de aislamiento de dominio y servidores, tal y como se presentan en este documento, incluso se usan en la propia red interna de Microsoft. Además de recomendar estas soluciones a los clientes, Microsoft depende del nivel de seguridad adicional que proporciona esta solución y tiene un compromiso a largo plazo de contribuir a que, con este método, se consiga que las redes sean más seguras y fáciles de administrar para lograr una informática de confianza.

### Consideraciones acerca del aislamiento de dominios y servidores

En resumen, la creación de una red aislada implica la separación de los distintos tipos de equipos de la red de una empresa según el tipo de acceso que deban tener. En este caso, hay dos tipos: administrados y no administrados. Se deben cumplir dos condiciones básicas para lograr un nivel funcional de aislamiento de red. Estas condiciones son:

-   Los equipos que residen en la red aislada pueden iniciar la comunicación con todos los equipos de la red completa, incluidos los que residen fuera de la red de confianza.

-   Los equipos que residen fuera de la red aislada sólo pueden iniciar la comunicación con otros equipos situados fuera de la red de confianza; no pueden iniciar la comunicación con equipos de la red de confianza.

El aislamiento de dominios y servidores IPsec aprovecha las estructuras de los dominios existentes mediante el uso de la configuración de la directiva de grupo. Todo lo necesario para crear una red aislada ya está incluido en los equipos que usan Windows XP, Windows 2000 Server y Windows Server 2003. Cuando se configure la directiva de grupo necesaria, para incluir un nuevo equipo en la red aislada sólo hay que agregar dicho equipo al dominio.

![](images/Cc875843.PNFUC02(es-es,TechNet.10).gif)

**Figura 2. Aislamiento de red mediante los dominios de Active Directory**

Como se ilustra en la figura anterior, cualquier equipo que no sea miembro del dominio se considera como un equipo que no es de confianza y, por tanto, reside fuera de la red aislada. Cualquier sistema que resida fuera de la red aislada no puede iniciar la comunicación IPsec y, por tanto, no puede establecer una conexión con ningún sistema del dominio aislado. Sin embargo, los miembros del dominio aislado sí pueden establecer una comunicación de texto sin cifrar con los dispositivos situados fuera de la red aislada.

Está claro que muchas organizaciones tienen equipos y servidores que, si bien están administrados y son de confianza, no forman parte del dominio de Active Directory o no pueden usar IPsec por una serie de motivos, pero siguen teniendo que comunicarse con sistemas de la red aislada. Para resolver este dilema, se puede crear otro grupo aislado (o grupo de límites) mediante listas de exención, como se muestra en la siguiente figura.

[![](images/Cc875843.PNFUC03(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875843.pnfuc03_big(es-es,technet.10).gif)

**Figura 3. Aislamiento de red y grupos de límites**

Un modelo de aislamiento de red como éste permite reducir la huella de seguridad de la red de una empresa. Sin embargo, esta solución por sí sola no puede garantizar que los sistemas de confianza sigan cumpliendo los estándares que los convierten en sistemas de confianza. Esta solución no es una solución completa de seguridad para la red en sí misma. Es una parte útil de un proceso de seguridad más global que, junto con otras soluciones, puede ayudar a reducir los riesgos a los que se enfrentan las redes modernas de las medianas empresas. En concreto, cuando se usa con otras soluciones de seguridad como WSUS, SMS, MOM, entre otras, se puede usar este método de aislamiento para ayudar a aplicar la conformidad con la directiva de seguridad en la red aislada.

Otras soluciones de seguridad basadas en Active Directory permiten automatizar tareas que ayudan a garantizar un cumplimiento continuado con la directiva de seguridad en la red aislada de confianza. Sin embargo, un grupo de límites tendrá que basarse en distintos métodos para garantizar que los equipos que contiene no se conviertan en puntos débiles de la solución de red aislada. Dichos equipos se deben validar como equipos que cumplen los requisitos antes de agregarse al grupo de límites; además, deben tener directivas y métodos específicos asociados que garanticen su cumplimiento continuado con los requisitos de directivas de seguridad de los sistemas de confianza.

### Consideraciones acerca de IPsec

IPsec es un estándar de seguridad del protocolo de Internet que proporciona un mecanismo general de seguridad de nivel IP basado en directivas que resulta ideal para proporcionar autenticación de host a host. Las directivas IPsec se definen como directivas que incluyen configuración y reglas de seguridad que controlan el flujo del tráfico entrante y saliente en un sistema host. Estas directivas se administran de forma central en Active Directory mediante objetos de directiva de grupo (GPO) para asignar las directivas a los miembros del dominio. Facilitan el establecimiento de comunicaciones seguras entre los miembros del dominio, lo que supone la base de esta solución.

IPsec usa el protocolo de negociación de Intercambio de claves por red (IKE) para negociar las opciones entre dos hosts y poder determinar el método de comunicación segura con IPsec. Los acuerdos realizados entre dos hosts y los distintos parámetros que definen este método de negociación se denominan asociaciones de seguridad o SA. Microsoft Windows puede usar uno de los tres métodos IKE siguientes:

-   Protocolo de autenticación Kerberos versión 5

-   Certificados digitales X.509 con los pares de claves RSA correspondientes

-   Claves precompartidas con frases de contraseña

**Nota**   Si bien se puede usar PKI como método de autenticación, la integración de la autenticación (Kerberos) de dominios de Windows 2000 en el protocolo de negociación IKE convierte a PKI en un método no recomendado.

La negociación IKE de Windows se puede configurar para permitir la comunicación con equipos que no responden a la petición de negociación IKE. Esta funcionalidad se denomina reserva para texto sin cifrar y, además de ser fundamental durante una instalación distribuida, también resulta útil en este contexto porque permite a los sistemas del grupo de límites comunicarse con miembros de la red aislada. Cualquier comunicación que IPsec no pueda proteger se conoce como asociación de seguridad parcial y se registra correctamente como evento de auditoría en el registro de seguridad.

IPsec puede realizar otras funciones útiles además de la autenticación, incluida la posibilidad de controlar la integridad y el cifrado del tráfico de la red mediante el uso de las opciones de encabezados de autenticación (AH) y carga de seguridad encapsulada (ESP). Si bien los encabezados de autenticación se pueden usar para conseguir que un paquete no se modifique durante el transporte, el uso de encabezados para realizar esta tarea hace que sea incompatible con la traducción de direcciones de red (NAT). El uso de ESP, que se suele usar para cifrar tráfico, puede servir en el modo de cifrado nulo (ESP/null), que permite la comprobación de la integridad de datos que sea compatible con NAT.

IPsec también se puede usar en dos modos distintos: transporte o túnel. El modo de transporte IPsec es el método recomendado para proteger el tráfico entre dos hosts. Funciona simplemente mediante la inserción de un encabezado después del encabezado IP original y, a continuación, mediante el cifrado del resto del paquete con AH o ESP. El modo de túnel se suele usar para los túneles VPN de puerta de enlace a puerta de enlace en los que los paquetes originales y los encabezados IP se encapsulan por completo y un nuevo encabezado IPsec reemplaza el encabezado IP original.

Para obtener más información, consulte la página [Aislamiento de dominios y servidores](http://www.microsoft.com/technet/itsolutions/network/sdiso/default.mspx) de Microsoft en www.microsoft.com/technet/itsolutions/network/sdiso/default.mspx (puede estar en inglés).

### Defensa en profundidad

![](images/Cc875843.PNFUC04(es-es,TechNet.10).gif)

**Figura 4. Modelo de defensa en profundidad con aislamiento lógico**

En la figura anterior se demuestra cómo el aislamiento lógico encaja en el modelo de defensa en profundidad. Si bien el aislamiento de dominios y servidores parece centrarse en la protección del equipo host, como haría un firewall basado en host, reside en el territorio de las comunicaciones de red con su uso de IPsec. Aunque esta solución cubre el hueco entre el host y la red interna, no reside completamente en ninguno de ellos porque se trata de una solución de ‘aislamiento lógico’. Por tanto, la siguiente funcionalidad queda fuera de su ámbito:

-   El aislamiento lógico no puede proteger los dispositivos de red como los enrutadores.

-   El aislamiento lógico no puede proteger los vínculos de red, como hacen 802.11i WPA para el cifrado inalámbrico y 802.1x EAP-TLS para el control de acceso inalámbrico.

-   El aislamiento lógico no puede proporcionar seguridad para todos los hosts de la red, ya que sólo controla los sistemas que tengan una credencial de equipo de confianza y una directiva IPsec basada en dominios.

-   El aislamiento lógico no está recomendado y no tiene un método con configuración automática que pueda proteger las rutas de nivel de aplicación, como hacen HTTPS y SSL para las aplicaciones web.

Es importante comprender y tener en cuenta qué parte desempeña el aislamiento lógico dentro de una solución completa de una defensa en profundidad. Por sí sola, esta solución no puede proteger todos los aspectos de una infraestructura de mediana empresa. Sin embargo, cuando se usa como parte de una solución completa, puede desempeñar un papel muy valioso.

### Uso de los servicios de cuarentena de VPN para protegerse frente a equipos remotos no administrados

Los sistemas remotos que usan soluciones VPN para tener acceso a la red de una empresa representan problemas concretos desde una perspectiva de directiva de seguridad. La mayoría de las soluciones de acceso remoto sólo validan las credenciales de un usuario remoto, pero no comprueban que el equipo remoto cumpla con las directivas de seguridad. Este método de validación supone un problema, ya que puede negar los esfuerzos para proteger una red de las amenazas relacionadas con problemas como archivos de firma antimalware obsoletos, niveles de seguridad obsoletos, configuración inadecuada de enrutamiento y una falta de protección por firewall adecuada.

El control de cuarentena de acceso a la red de Microsoft Windows Server 2003 permite solucionar este problema al retrasar el acceso remoto a una red VPN hasta que se pueda comprobar que el estado de configuración del equipo que se conecta cumple con los estándares de la directiva de seguridad actual.

### Consideraciones acerca de los servicios de cuarentena de VPN

El control de cuarentena de acceso a la red es una función que proporciona la familia de productos Windows Server 2003 que retrasa los servicios de acceso remoto normales hasta que se examinan y validan los equipos remotos que se conectan mediante un script configurado por el administrador. Normalmente, cuando se inicia una sesión remota, el usuario se autentica y al equipo remoto se le proporciona una dirección IP pero, en este momento, la conexión se coloca en modo de cuarentena; en dicho modo, el acceso a la red está limitado hasta que se ejecute el script del administrador en el equipo remoto. Después de haberlo ejecutado y de notificar al servidor de acceso remoto que el equipo remoto cumple con las directivas de red configuradas, se elimina el modo de cuarentena y al equipo remoto se le otorga acceso a la red.

Mientras una conexión remota se encuentra en modo de cuarentena, se pueden aplicar las siguientes restricciones en dicha conexión:

-   Se puede configurar un conjunto de filtros de paquetes de cuarentena para restringir el tipo de tráfico que el cliente puede iniciar o recibir.

-   Se puede configurar un temporizador de sesión de cuarentena para restringir el tiempo que un cliente puede estar conectado mientras se encuentra en modo de cuarentena.

El control de cuarentena de acceso a la red se puede usar como parte de una solución de seguridad completa que le ayuda a aplicar las directivas de seguridad y a garantizar que los sistemas que no sean de confianza no se puedan conectar a una red de confianza. Sin embargo, no se trata de una solución de seguridad en sí misma y no puede evitar las conexiones de usuarios malintencionados que obtengan un conjunto válido de credenciales.

**Nota**   El control de cuarentena de acceso a la red no es igual que la Protección de acceso a redes (NAP), una nueva plataforma de aplicación de directivas que se incluirá en la próxima familia de sistemas operativos Windows Server Longhorn. Para obtener más información acerca de NAP, consulte el "Apéndice A: Protección de acceso a redes" al final de este documento.

### Componentes del control de cuarentena de acceso a la red

[![](images/Cc875843.PNFUC05(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875843.pnfuc05_big(es-es,technet.10).gif)

**Figura 5. Componentes del control de cuarentena de acceso a la red de Windows**

En la figura anterior se muestran los componentes habituales de una solución de acceso remoto de Windows que usa el control de cuarentena de acceso a la red. Estos componentes incluyen:

-   **Cliente de acceso remoto compatible en cuarentena**. Este componente es un equipo que ejecuta una versión de Windows capaz de admitir perfiles CM creados con el kit de administración de Connection Manager (CMAK), que se proporciona con Windows Server 2003. Las versiones de Windows que ofrecen esta compatibilidad incluyen Windows 98 Second Edition y posteriores. Estos equipos cliente deben tener instalado un componente notificador, un script de requisitos de directivas de red y se pueden configurar para ejecutar el script como acción posterior a la conexión.

-   **Servidor de acceso remoto compatible en cuarentena**. Este componentes es un equipo con Windows Server 2003 que ejecuta Enrutamiento y acceso remoto, que admite el uso de un componente de escucha y los atributos del proveedor (VSA) de RADIUS MS-Quarantine-IPFilter y MS-Quarantine-Session-Timeout, junto con un componente de escucha instalado.

-   **Servidor RADIUS compatible en cuarentena**. Este componente es opcional y se usa cuando se configura la autenticación RADIUS en el servidor de acceso remoto que ejecuta Windows Server 2003 e IAS para admitir los VSA de RADIUS MS-Quarantine-IPFilter y MS-Quarantine-Session-Timeout.

-   **Recursos de cuarentena**. Estos componentes son los servidores y los servicios a los que el cliente remoto puede tener acceso mientras se encuentra en modo de cuarentena. Normalmente, suelen incluir servidores que proporcionan servicios DNS, perfiles CM o proveedores de actualización de seguridad para conseguir la conformidad de los clientes.

-   **Base de datos de la cuenta**. Normalmente, este componente sería un dominio de Active Directory donde la cuenta del usuario remoto se almacena y se buscan las propiedades de conexión.

-   **Directiva de acceso remoto de cuarentena**. Esta directiva es necesaria para proporcionar las condiciones necesarias para que se produzcan las conexiones de acceso remoto y para especificar los atributos MS-Quarantine-IPFilter o MS-Quarantine-Session-Timeout.

### Defensa en profundidad

![](images/Cc875843.PNFUC06(es-es,TechNet.10).gif)

**Figura 6. Defensa en profundidad y control de cuarentena de acceso a la red**

Como muestra esta adaptación del modelo de defensa en profundidad de Microsoft, la cuarentena de VPN ocupa tres niveles del modelo: el host, la red interna y el perímetro. Si bien esta solución no protege directamente al cliente, protege los servidores frente a amenazas que podrían introducir los clientes remotos que no cumplen las directrices de seguridad. También protege de forma indirecta a los clientes remotos, al asegurar que cumplan los requisitos de directivas para que funcionen correctamente y fomentar las actualizaciones periódicas.

Asimismo, esta solución mejora la protección de la propia red frente a los efectos negativos que pueden crear los equipos remotos independientes sin no están bien configurados, incluida la propagación de malware, que puede tener efectos nocivos en el rendimiento de la red. Si bien el perímetro puede parecer que no está relacionado porque esta solución no evita directamente los ataques en la VPN (que reside en el perímetro), ofrece otro nivel de seguridad al que tendría que enfrentarse un atacante para obtener acceso directo a los recursos de la red interna, incluso aunque el atacante obtuviera las credenciales de autenticación.

### Uso de la autenticación 802.1X para protegerse frente a clientes inalámbricos no administrados

El uso del estándar 802.1X del Instituto de ingenieros de electricidad y electrónica (IEEE) se adapta bien a la tarea de ayudar a defender las redes inalámbricas frente al uso no autorizado. En resumen, a menos que un equipo esté configurado para poder comunicarse en la red, sencillamente no se podrá comunicar. Si bien esta solución funciona bien en las redes inalámbricas, no es tan efectiva en las redes con cable, aunque se puede usar el estándar de esta forma. Su efectividad limitada es lo que hace que este documento de recomendaciones sugiera un método combinado para proteger la red de una mediana empresa. Al usar una combinación de las soluciones más efectivas que ayudan a tratar todos los aspectos de una red típica de un negocio, se puede implementar una solución eficaz de defensa en profundidad.

### Consideraciones acerca de la autenticación IEEE 802.1X

La autenticación IEEE 802.1X es un mecanismo de control de acceso basado en puertos que se puede configurar para exigir la autenticación mutua entres clientes y una red. Cuando se implementa, cualquier dispositivo que no se autentique no podrá participar en ninguna comunicación que se establezca con la red en cuestión.

802.1X admite el protocolo de autenticación extensible (EAP), que tiene una serie de variantes, entre las que se incluyen tres admitidas por las versiones actuales de Microsoft Windows:

-   **EAP-MD5**. Con MD5, un servidor de autenticación envía un desafío a un cliente (suplicante) y el suplicante combina esta petición de desafío con su propio identificador y frase de contraseña. Esta respuesta se convierte en un algoritmo hash MD5 y se devuelve al servidor de autenticación, que descifra y hace coincidir la respuesta con el desafío original. Si la respuesta coincide, se produce la autenticación. Este método no es seguro en la mayoría de las implementaciones porque se envía la propia contraseña, que puede ser interceptada y descifrada por terceros.

-   **EAP protegido**. EAP protegido (PEAP) usa la información de autenticación y certificado del servidor del cliente (como los nombres de usuario y las contraseñas) para establecer la autenticación mutua. La implementación de Microsoft de este estándar usa MS-CHAPv2, que se basa en la información de contraseña y cuenta tradicional y en un servidor RADIUS para establecer esta autenticación. Este método se suele considerar lo suficientemente seguro para pequeños entornos que no se pueden permitir los requisitos administrativos y de infraestructura que implica el método EAP-TLS.

-   **EAP-TLS**. Con este método, un servidor de autenticación configura una sesión de seguridad del nivel de transporte (TLS) con el suplicante para enviar al cliente un certificado digital. El suplicante valida este certificado cuando lo recibe y, a continuación, envía su propio certificado como respuesta, certificado que a su vez valida el servidor de autenticación. Siempre que ambas partes confíen en los certificados de la otra parte, se produce la autenticación. Este método está recomendado para redes que puedan admitir una infraestructura PKI y servidores de autenticación RADIUS. También es la opción más segura que hay disponible para redes inalámbricas, especialmente cuando se combinan con el uso del estándar 802.11i WPA2.

Antes de que un cliente se autentique, debe confiar en el autenticador (un punto de acceso inalámbrico o un conmutador de red) hasta que se autentique mediante el servidor que realiza la autenticación. Por tanto, durante el protocolo de enlace de autenticación inicial, el autenticador reenvía todas las comunicaciones entre el suplicante y el servidor de autenticación. Cuando la autenticación finaliza, el suplicante puede tener acceso directo a la red.

### Por qué 802.1X no es efectivo en el caso de redes con cable

Si bien 802.1X suele ayudar a controlar la seguridad de las redes inalámbricas, existen algunos problemas relacionados con la implementación de este método para proteger las redes con cable. El primer problema consiste en que, si bien 802.1X tiene varios objetos de directiva de grupo de Active Directory que admiten su implementación en redes inalámbricas, no admite la autenticación 802.1X en las redes con cable. Por tanto, 802.1X supondría un grado importante de sobrecarga administrativa para dicha implementación. Además, muchos conmutadores, dispositivos de impresión de red, así como otros dispositivos de la infraestructura de la red con cable no admiten 802.1X, por lo que es muy probable que se tuvieran que realizar costosas actualizaciones para admitir esta implementación en la mayoría de las redes de las medianas empresas.

Además de los costos administrativos y de infraestructura relacionados con dicha implementación, existen algunos defectos de seguridad que surgen cuando se usa este estándar pensado para el entorno inalámbrico en redes con cable. Por ejemplo, como la autenticación 802.1X sólo se produce cuando se establece una conexión y 802.1X no puede ver los concentradores, lo único que tendría que hacer un atacante sería conectar un concentrador a la red interna, junto con un equipo autenticado y otro “a la sombra” en el que podría realizar un ataque.

**Nota**   Estas desventajas y vulnerabilidades específicas no afectan a las redes inalámbricas. Estos problemas con la seguridad 802.1X sólo se presentan cuando se usa en redes con cable.

Estos problemas son los que hacen que se recomiende IPsec para el aislamiento de dominios y servidores en lugar de 802.1X. Sin embargo, esta recomendación no significa que la autenticación 802.1X no se pueda aplicar en una red de una mediana empresa. Tal como se ha mencionado con anterioridad, 802.1X es una valiosa herramienta que ayuda a solucionar los problemas de la seguridad inalámbrica y cuya seguridad aumenta si se agrega una solución de aislamiento de red basada en IPsec.

### Defensa en profundidad

![](images/Cc875843.PNFUC07(es-es,TechNet.10).gif)

**Figura 7. Defensa en profundidad con seguridad inalámbrica 802.1X**

Como se ilustra en la figura anterior, la seguridad inalámbrica que usa la autenticación 802.1X ocupa el nivel de red del modelo de defensa en profundidad. Si bien podría parecer que la seguridad inalámbrica también va más allá del perímetro, las redes inalámbricas en realidad son una parte de la red local, mientras que el perímetro se encarga más de las redes externas como Internet. Algunas partes de los métodos de seguridad inalámbrica tienen componentes host, pero la seguridad inalámbrica no está diseñada para proteger directamente el host.

### Uso de SMS para detectar y tratar los sistemas no administrados

Microsoft Systems Management Server (SMS) 2003 se suele usar para administrar equipos de la red, mantener la información de inventario de activos, así como ofrecer software y actualizaciones para conseguir que se cumplan las directivas de seguridad y mantener la compatibilidad de la instalación de plataformas y software. La funcionalidad de inventario y detección de redes de SMS 2003 entra en el ámbito de este documento porque proporciona un método que puede ayudar a detectar los sistemas que no son de confianza cuando se conectan a la red. Esta funcionalidad también ofrece un método que facilita el tratamiento, dependiendo de las directivas que se implementan como respuesta al uso de equipos no administrados.

En este documento se asume que el lector ha usado SMS y otros métodos para conseguir que los equipos miembros del dominio cumplan las directivas de seguridad, lo que incluiría que cuenten con todas las actualizaciones de seguridad actuales. Por tanto, los debates sobre la administración de revisiones mediante SMS 2003 y otras herramientas no son objeto de este documento. Para obtener más información acerca de estos temas e información adicional relacionada con SMS, consulte el acelerador de solución [Administración de revisiones mediante Systems Management Server 2003](http://www.microsoft.com/technet/itsolutions/cits/mo/swdist/pmsms/2003/pmsms031.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/swdist/pmsms/2003/pmsms031.mspx o la página principal de [Microsoft Systems Management Server](http://www.microsoft.com/smserver/default.mspx) en www.microsoft.com/smserver/default.mspx (puede estar en inglés).

### Detección y documentación de activos existentes

Para negocios que implementaron SMS, la documentación de los activos existentes posiblemente ya se habría realizado y existiría un inventario de los sistemas administrados y no administrados. Dicho inventario debe contener información acerca de los requisitos y procedimientos de actualización de seguridad para equipos que no administre SMS, ya sea por diseño o porque no sean agentes activos para ese tipo de cliente. Estos equipos no administrados pueden incluir dispositivos de un perímetro de seguridad (también conocido como DMZ, zona desmilitarizada y subred apantallada), equipos de prueba o dispositivos independientes.

Es importante contar con una lista de dispositivos bien documentada que no administre SMS, no sólo debido a los requisitos de seguridad, sino también porque dicha lista se debe usar para compararla con cualquier información de inventario nueva con el fin de determinar si los sistemas que se acaban de detectar están autorizados o son desconocidos. Para mantener actualizadas dichas listas, es importante aplicar un proceso para agregar nuevos sistemas no administrables a la red del negocio y que incluya no sólo información de identificación, sino también el proceso que se realiza para conseguir que dichos sistemas estén protegidos, junto con asignaciones de propiedad.

Aunque SMS tal vez no pueda recopilar mucha información sobre estos sistemas no administrados, aparte de la dirección IP y el nombre, esta información suele bastar para determinar si los nuevos dispositivos de red están autorizados o no.

### Desarrollo

La sección "Evaluación" explica que una combinación de distintas soluciones que trate las funciones específicas en una red de una mediana empresa es el método más completo para ayudarle a defender dicha red. El aislamiento de dominios y servidores en la red con cable garantiza que sólo los equipos conocidos y administrados pueden tener acceso a los recursos de confianza. La cuarentena de VPN garantiza que los sistemas remotos que sólo se conectan en ocasiones a la red remota sigan cumpliendo las directivas de seguridad. La autenticación 802.1X protege la red inalámbrica para que sólo los equipos autorizados puedan establecer conexiones. Finalmente, se usa SMS para ayudar a que los equipos de confianza sigan cumpliendo las directivas de seguridad y detectar equipos independientes que no son de confianza cuando se conecten a la red. Todas estas soluciones se combinan para ayudar a proteger una red frente a conexiones no autorizadas y equipos independientes.

Además de tratar los requisitos para implementar estas soluciones, esta sección también incluye algunos de los posibles problemas que se deben solucionar para permitir que cada solución sea el método más adecuado para cada entorno de mediana empresa.

### Uso de IPsec para aislar dominios y servidores

Desarrollar un plan para implementar el aislamiento de dominios y servidores basado en IPsec implica el determinar si esta solución es o no factible para un determinado entorno de red, así como recopilar la información de requisitos previos necesaria para desarrollar un plan de implementación. El concepto de aislamiento de red IPsec se presentó en la sección "Evaluación" de este documento. Ahora que ya se conocen las ventajas de este método, se pueden sopesar los posibles problemas relacionados con dicha implementación. En esta sección se tratarán algunos problemas relacionados con la implementación del aislamiento de redes basado en IPsec, junto con los requisitos de dicha implementación para facilitar ese proceso de toma de decisiones.

### Identificación de la arquitectura de red

Debido a que IPsec se basa en el propio protocolo de Internet, se necesita un conocimiento profundo de la infraestructura y el flujo de tráfico de la red actual para conseguir implementar dicha solución. Si bien la información sobre los esquemas de direcciones IP, diseños de subredes y patrones de tráfico de red son componentes importantes que se deben identificar, una documentación detallada de la segmentación de la red y un modelo de flujo de tráfico de la red actual son absolutamente esenciales para implementar con éxito un plan de aislamiento de red eficaz.

**Nota**   No es el objeto de este documento tratar los detalles de la documentación del entorno de red. La creación de dicha documentación es fundamental para que cualquier iniciativa completa de seguridad de la red tenga éxito, incluida una como ésta. Por tanto, si no existe dicha documentación, proyectos de este tipo se deberían considerar como un riesgo innecesario y no se implementarán eficazmente hasta que se realicen dichas iniciativas de documentación.

La documentación de arquitectura de red debe reflejar de forma precisa los detalles actuales con respecto a la siguiente información:

-   Ubicaciones y detalles de equilibrio de carga y firewall

-   Información de los dispositivos de red, como el tamaño de RAM, el fabricante/modelo y la configuración MTU

-   Informes de uso y tráfico de red

-   Uso de NAT

-   Segmentación de VLAN

-   Vínculos de red de dispositivos

-   Información de sistemas de detección de intrusiones (IDS)

### Identificación del flujo de tráfico de red

Además de la información acerca de los dispositivos y las configuraciones que pueden afectar al aislamiento de red basado en IPsec, es importante examinar los patrones de tráfico de red. Cuando recopile este tipo de información, es importante que considere factores como la forma en la que los dispositivos que no son de Windows (como equipos Linux) o los dispositivos que usan versiones de Windows anteriores a Windows 2000 SP4 se comunican con otros sistemas basados en Windows. Otras consideraciones:

-   ¿Están las subredes dedicadas a tipos específicos de tráfico, como las comunicaciones con grandes sistemas (mainframes)?

-   ¿Se debe separar el tráfico entre las ubicaciones?

-   ¿Hay algún tipo de tráfico que necesite el alto nivel de seguridad que proporciona el cifrado, como la comunicación con una base de datos de RRHH?

-   ¿Hay algún dispositivo de seguridad o reglas de firewall que puedan afectar a la implementación, como el bloqueo del puerto UDP 500?

-   ¿Qué método de comunicación existe entre las aplicaciones? Por ejemplo, ¿usan la llamada a procedimiento remoto (RPC)? Esto podría requerir más atención.

-   ¿Cómo se comunican los hosts y los servidores entre sí? ¿Usan conexiones de puerto/protocolo o establecen varias sesiones en una amplia gama de protocolos?

### Identificación de la estructura de Active Directory

Para comprender el impacto que la implementación de IPsec puede tener en una estructura de Active Directory, es importante recopilar información sobre la estructura de bosques de Active Directory, el diseño de dominios, el diseño de la unidad organizativa (OU) y la topología del sitio, además de la información de red identificada anteriormente. Esta información debe incluir lo siguiente:

-   Número de bosques

-   Número de nombres de dominio

-   Número y tipos de relaciones de confianza

-   Número y nombres de sitios

-   Estructura de directiva de grupo y unidad organizativa

-   Cualquier información de directiva IPsec existente (si se usa IPsec actualmente)

### Identificación de hosts

Entre la información de host importante que se debe recopilar se incluyen:

-   Nombres de equipo

-   Direcciones IP, especialmente las direcciones estáticas

-   Direcciones MAC

-   Versión del sistema operativo, incluido Service Pack y niveles de revisión

-   Miembros del dominio

-   Ubicación física

-   Tipo y función del hardware

### Identificación de las consideraciones de la función IPsec

Hay varias consideraciones sobre planificación de capacidad que se deben tener en cuenta al desarrollar un plan para implementar IPsec, sobre todo, al contemplar el uso del cifrado IPsec, porque necesita una determinada cantidad de uso de host y sobrecarga de la red. Algunas consideraciones:

-   **Uso de memoria de servidor**. Cada sesión puede usar 5 KB de RAM.

-   **Uso de CPU** **de servidores,** **estaciones de trabajoy** **dispositivos de la infraestructura**. Esta información es especialmente importante para los servidores. Asegúrese de que el uso de los dispositivos no sea ya excesivo.

-   **Latencia y uso de la red**. La latencia se puede aumentar cuando se usa IPsec. Cuando Microsoft implementó IPsec, el uso de la red aumentó del 1% al 3%.

-   **Uso de NAT y tipo de cifrado**. La comunicación AH no puede atravesar NAT. Por tanto, habrá que usar ESP para cifrar las comunicaciones. ESP supone una mayor sobrecarga que el cifrado AH, a menos que se use el cifrado ESP nulo.

-   **Impacto de las directivas de grupo**. Los GPO IPsec afectan a los tiempos de conexión y arranque del equipo. Se deben tomar líneas de base antes y después de las implementaciones de prueba para determinar el efecto real en dichos tiempos.

### Identificación de los niveles de confianza

Otra importante consideración consiste en determinar los hosts que participan en esta solución y en qué medida. Para decidir esto, es necesario establecer una definición clara de las condiciones que se deben cumplir para ser de confianza y los grados de confianza que pueden existir. La siguiente información puede ayudarle a realizar este proceso al ofrecer algunas definiciones claras sobre confianza, los criterios necesarios para cumplir determinados niveles de confianza y cómo esto afecta al proceso de planificación.

Hay cuatro estados básicos que se pueden aplicar a un host con respecto a los niveles de confianza. En el orden de mayor o menor grado de confianza, estos estados son:

-   **De confianza**. Un estado de confianza implica que se administran los riesgos de seguridad de un host y que otros hosts de confianza pueden suponer de forma razonable que no se va a realizar un acto malintencionado desde dicho host. Aunque este estado no implica necesariamente que este host sea completamente seguro, significa que el estado de dicho host es responsabilidad de un departamento de TI y que está administrado por algún mecanismo, ya sea un proceso automático o documentado.

    Puesto que este host es de confianza, la comunicación entre este host y otros hosts de confianza no debe verse impedida por la infraestructura de red. Puesto que se puede asumir con seguridad que no se va a iniciar un acto malintencionado desde este host, no es necesario bloquear ni filtrar el tráfico del host mediante firewalls u otras medidas similares.

-   **De próxima confianza**. Un estado de próxima confianza indica que, si bien un equipo puede convertirse en un dispositivo de confianza, aún es necesario realizar algunos cambios adicionales de configuración o algún tipo de actualización para poder certificarlo como de confianza. La identificación de dichos equipos es especialmente importante durante la fase de diseño, ya que proporcionan algún tipo de indicación sobre la cantidad de esfuerzo y el costo necesarios para establecer una red aislada.

-   **Conocido,** **no de confianza**. Hay una serie de motivos por los que un equipo conocido tal vez no pueda convertirse en un activo de confianza, desde limitaciones financieras, requisitos de negocio o incluso requisitos funcionales. Por ejemplo, la financiación de un proyecto tal vez no sea suficiente para actualizar todos los equipos, algunas unidades de negocio tal vez posean sus propios dominios o una aplicación más antigua tal vez no sea compatible con los sistemas operativos actualmente admitidos y, por tanto, no se pueda ejecutar en un equipo protegido.

    Independientemente del motivo, se debe consultar a los propietarios de empresas de equipos conocidos pero que no son de confianza para que determinen si hay algo que se pueda hacer para que un equipo pueda cumplir los requisitos y para determinar cómo resolver esta situación a la vez que se mantiene un perfil de riesgo aceptable.

-   **Desconocido,** **no de confianza**. El estado desconocido y no de confianza debe ser el estado predeterminado para todos los hosts. Los hosts con este estado no están administrados y sus configuraciones son desconocidas, por lo que no se les puede asignar otro estado de confianza. Se debe asumir que estos hosts se pueden poner en riesgo y se pueden usar como plataformas para actividades malintencionadas, por lo que suponen un nivel de riesgo inaceptable para la compañía. Esta solución está diseñada para reducir el posible impacto de dichos sistemas.

### Uso de la información recopilada

Cuando se haya recopilado toda la información importante, se podrá implantar un plan de implementación y determinar la solución de aislamiento de red basada en IPsec adecuada para el entorno de red actual. Algunas de las consideraciones que pueden influir en la implementación de esta solución son:

-   El costo de las actualizaciones necesarias para que los hosts cumplan con un estado de confianza y sean compatibles con los requisitos IPsec.

-   El costo de las actualizaciones y reemplazos de infraestructura si los dispositivos de la red actual no admiten IPsec.

-   Equilibrar la posible pérdida de QOS basada en enrutador y las ventajas de seguridad del aislamiento de red, ya que el establecimiento de prioridades basado en puertos no funcionará cuando se implemente IPsec pero el QOS basado en direcciones IP continuará funcionando.

-   Los monitores de red y los dispositivos IDS pueden dar error cuando se implementa IPsec, especialmente, cuando se usa el cifrado ESP. Se pueden usar analizadores para superar este problema si el dispositivo tiene un analizador IPsec.

-   La implementación de IPsec puede conllevar actualizaciones de hardware debido a la mayor sobrecarga y demandas que soportan la CPU y memoria de los servidores y dispositivos de red.

-   La administración de expectativas puede suponer un problema, ya que puede aumentar la latencia de la red.

-   La administración de usuarios invitados y proveedores también puede generar costos excesivos porque estos usuarios tienen dispositivos que no son de confianza y pueden tener motivos comerciales para tener acceso a recursos de la red aislada. Estas excepciones pueden ser difíciles de administrar conforme aumentan en número y frecuencia, pero se pueden mitigar mediante el uso de una zona de límites entre las redes de confianza y las que no son de confianza.

Estos problemas muestran el motivo por el que es necesario planear y probar exhaustivamente los cambios que puedan afectar a toda la red antes de implementarlos, como la implementación de aislamiento de la red e IPsec. Se debe prestar especial atención para determinar no sólo cómo implementar esta solución, sino también si se puede implementar debido al estado actual de la red y a los costos financieros y políticos de conseguir que la red cumpla los requisitos. Además, las implementaciones limitadas o incrementales que sólo aíslan determinados recursos se deben considerar como una posible estrategia de mitigación que ayude a resolver estos problemas.

De nuevo, el aislamiento de la red basado en IPsec sólo supone una parte de una solución completa. Cada una de las soluciones de esta guía ayuda a defenderse frente a dispositivos no administrados que se pueden conectar a la red, pero cada parte de esta solución puede aplicarse por separado y aumentar aun así el nivel de seguridad de determinada red. Por tanto, incluso aunque el aislamiento de dominios y servidores IPsec no es una solución aceptable en este momento, aún puede resultar útil implementar las demás soluciones que se enumeran aquí y, tal vez, volver al aislamiento de la red cuando ésta se encuentre más madura y sea más compatible con los requisitos señalados en este documento.

### Uso de los servicios de cuarentena de VPN para protegerse frente a equipos remotos no administrados

En una sesión de servidor de acceso remoto estándar de Windows, el servidor realizará las siguientes acciones cuando un cliente de acceso remoto inicie sesión:

1.  El servidor de acceso remoto realiza comprobaciones en las directivas de acceso remoto configuradas y permite la conexión.

2.  El servidor comprueba los permisos de acceso remoto del usuario.

3.  A continuación, el servidor autentica las credenciales del usuario en Active Directory o en algún otro servicio de autenticación.

4.  El servidor asigna una dirección IP al cliente remoto.

En este momento, el cliente remoto tiene acceso completo a la red y no se tienen que realizar comprobaciones para comprobar los niveles de actualización, la existencia o estado de actualización del software antivirus o cualquier otra información relacionada con la directiva de seguridad. Esta funcionalidad es menos adecuada porque a veces significa que las actualizaciones, cambios de configuración o revisiones no se aplican a los usuarios remotos o a los equipos en itinerancia.

Sin embargo, como se muestra en la siguiente figura y lista numerada, la conexión de cuarentena de VPN es distinta:

[![](images/Cc875843.PNFUC08(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875843.pnfuc08_big(es-es,technet.10).gif)

**Figura 8. Proceso de cuarentena de VPN**

1.  El cliente remoto ejecuta un script previo a la conexión de Connection Manager que comprueba los requisitos previos de conexión básicos (como el nivel de actualización de seguridad y la fecha del archivo de firma de virus) y almacena los resultados. Después de ejecutar este script, el cliente establece una sesión de acceso remoto mediante un túnel VPN.

2.  El servidor de acceso remoto autentica las credenciales del usuario mediante RADIUS, que comprueba Active Directory para verificar las credenciales.

3.  Cuando Active Directory autentica al usuario, el servidor de acceso remoto coloca al cliente en estado de cuarentena mediante la aplicación de una directiva de acceso remoto. Mientras se encuentra en cuarentena, el acceso a la red está limitado a lo que especifique la directiva de cuarentena. Este acceso limitado se puede conseguir mediante un filtro IP que restrinja el acceso a determinados recursos que se pueden usar para conseguir que el cliente cumpla los requisitos o mediante la especificación de un período de tiempo de espera, tras el cual, se desconectará al cliente.

4.  Un script posterior a la conexión notifica al servidor de acceso remoto si el cliente cumple o no con los requisitos especificados. Si la conexión no cumple los requisitos en el período de tiempo de espera, al usuario se le notifican los detalles del error y se cierra la conexión.

5.  Si el script posterior a la conexión indica que el cliente cumple los requisitos especificados, el servidor de acceso remoto elimina el cliente del modo de cuarentena. Para ello, quita las restricciones del filtro IP y, por tanto, le otorga permiso de acceso a los recursos de la red especificados por la directiva de acceso remoto.

Un cliente de acceso remoto sólo puede tener acceso a los recursos situados en la red de cuarentena especificada, tanto si dicha red es una subred independiente como si se trata de un conjunto definido de servidores de Internet. Una red de cuarentena debe proporcionar recursos que permitirían a un cliente remoto realizar actividades para conseguir que un equipo remoto cumpla con los estándares de seguridad. En general, estos recursos incluirían el acceso a un servidor DNS para resolver los nombres, a un servidor de archivos para recuperar actualizaciones y, tal vez, a un servidor web para obtener instrucciones o actualizaciones basadas en Web.

El uso de una subred de cuarentena en este proceso implicaría una configuración más prolongada de tiempo de espera de sesión para garantizar que hubiera suficiente tiempo para descargar e instalar las actualizaciones en el equipo del cliente remoto. Para evitar este problema, se podría dirigir el equipo cliente para que use otras fuentes o usar servidores de actualización de Internet situados fuera de la sesión VPN, si bien este método implicaría un script más complejo y podría suponer otros problemas de seguridad. En cualquier caso, es el script el que determina el comportamiento de cuarentena y no la propia red.

**Nota**   Las directivas IPsec se pueden incluir en un script si la solución de cuarentena tiene que contener sistemas no unidos a un dominio. En estos casos, se pueden usar netsh o lpseccmd.exe para aplicar directivas sencillas con certificados para admitir la autenticación IPsec. IPsec también puede funcionar para sistemas unidos a un dominio en configuraciones de cuarentena de VPN, así como una solución de niveles.

### Componentes del cliente de cuarentena de VPN

Como se indicó en la sección anterior, el primer paso del proceso de cuarentena de VPN empieza con el cliente, en concreto, con el script previo a la conexión de Connection Manager. Connection Manager forma parte del kit de administración de Connection Manager (CMAK) que centraliza y automatiza el establecimiento y la administración de conexiones de red y admite varias áreas clave de una configuración de cuarentena de VPN, entre ellas:

-   Comprobaciones de seguridad previas a la conexión para administrar automáticamente las configuraciones de equipos cliente.

-   Comprobaciones posteriores a la conexión y validaciones de inicio de sesión.

Connection Manager permite que los administradores establezcan acciones personalizadas mediante perfiles que se pueden distribuir a varios equipos. Esta capacidad simplifica el proceso de conexión para los usuarios remotos mediante la limitación del número de valores que se pueden cambiar. Algunos de los valores que se pueden cambiar son:

-   Establecimiento de listas de números de teléfono que se pueden usar para conexiones telefónicas.

-   Personalización de gráficos, iconos, mensajes y texto de Ayuda.

-   Ejecución de acciones personalizadas previas y posteriores a la conexión, que pueden incluir actividades como el restablecimiento del perfil de marcador de teléfono o la configuración de reglas de filtro de paquetes del Firewall de Windows.

Otro componente de CMAK es el agente cliente (RQC.exe), que se comunica con el Servicio de cuarentena de acceso remoto (RQS.exe) en el servidor de acceso remoto mediante el puerto TCP 7250. Cuando se establece una conexión de cuarentena, RQS envía a RQC una clave compartida secreta. Si el cliente cumple las condiciones necesarias, RQC envía la clave compartida para liberar al cliente de la cuarentena.

Los perfiles de Connection Manager son paquetes de marcador de teléfono del cliente Connection Manager personalizados autoextraíbles que se pueden crear y configurar mediante CMAK. El asistente de CMAK guía a los administradores por el proceso de configuración del perfil que, a continuación, se puede distribuir mediante una serie de mecanismos que van desde la directiva de grupo hasta la distribución del software Microsoft Systems Management Server (SMS) 2003. Cuando se ejecuta el archivo ejecutable creado en el equipo cliente, instala el perfil en el equipo local junto con la configuración necesaria para establecer la comunicación con los servidores de acceso remoto. Cuando finaliza la instalación, el usuario sólo tiene que iniciar el nombre del perfil en el menú **Conectar a** de Windows XP para establecer una conexión.

Para obtener más información acerca de CMAK, consulte la página [Kit de administración de Connection Manager](http://technet2.microsoft.com/windowsserver/en/library/be5c1c37-109e-49bc-943e-6595832d57611033.mspx?mfr=true) en Microsoft TechNet en http://technet2.microsoft.com/WindowsServer/en/library/be5c1c37-109e-49bc-943e-6595832d57611033.mspx?mfr=true (puede estar en inglés).

### Componentes del servidor de cuarentena de VPN

El servidor de acceso remoto VPN es la parte central de esta solución y realiza las siguientes funciones:

-   Ejecuta el Servicio de cuarentena de acceso remoto (RQS.exe).

-   Aplica directivas de acceso remoto para la configuración de acceso de cuarentena.

-   Negocia la comunicación con el agente del cliente.

-   Recibe información de cumplimiento de directivas del agente del cliente.

-   Aplica directivas de acceso remoto para determinar los permisos de acceso a los recursos de la red.

El Servicio de cuarentena de acceso remoto es un componente opcional en Windows Server 2003 con Service Pack 1 y admite las API necesarias para poner los equipos de cliente remoto en cuarentena y, a continuación, eliminarlos del modo de cuarentena cuando el agente del cliente envíe una notificación de cumplimiento de directivas. Este servicio (RQS.exe) espera en el puerto TCP 7250 la notificación por parte del componente del cliente (RQC.exe) de que el equipo cliente cumple los requisitos de la directiva. Esta funcionalidad significa que cualquier firewall, incluidos los firewalls basados en host, deben permitir el tráfico en el puerto TCP 7250 para que esta solución funcione.

### Componentes de la red de cuarentena de VPN

Los siguientes componentes de red incluyen tanto las partes necesarias como las opcionales que pueden formar parte de una solución de red de cuarentena de VPN.

-   **Servidor RADIUS del Servicio de autenticación de Internet (IAS) (recomendado)**. Aunque los servidores IAS sólo son necesarios si se usa RADIUS como proveedor de autenticación, tienen algunas ventajas indiscutibles con respecto a otras soluciones de autenticación, incluida la compatibilidad con el protocolo de autenticación extensible para admitir la autenticación en dos fases basada en certificados y tarjetas inteligentes. Si se usa RADIUS, se recomienda usar el servicio IAS que se incluye con Windows Server 2003 como proveedor RADIUS, ya que admite los VSA MS-Quarantine Session Timeout y MS-Quarantine-IPFilter; otros servidores RADIUS tal vez no.

-   **Active Directory (recomendado)**. Active Directory actúa como base de datos de autenticación de la cuenta de usuario para RADIUS y se integra con IAS y otros servicios. Cuando se usa junto con IAS, puede admitir la autenticación en dos fases con certificados y otros métodos.

-   **Servidor DHCP (recomendado)**. Los servidores DHCP se usan para proporcionar direcciones IP a los clientes remotos.

-   **Servidor DNS (recomendado)**. Un servidor DNS proporciona servicios de resolución de nombres para que los clientes de la red de cuarentena puedan conectarse a otros servidores (si se proporcionaran) para poder conseguir que los equipos clientes remotos puedan cumplir los requisitos.

-   **Servidor Windows Software Update Service (WSUS) (opcional)**. Los servidores WSUS pueden suministrar las actualizaciones y revisiones de seguridad necesarias que los equipos remotos pueden necesitar para cumplir los requisitos para poder salir del estado de cuarentena. También se podrían usar otros métodos, incluido SMS 2003 o incluso los servicios estándar de Windows Update si los equipos se tuvieran que dirigir a fuentes externas para realizar las actualizaciones.

-   **Servidor de archivos (opcional)**. Los servidores de archivos se pueden usar para proporcionar recursos compartidos cuando los equipos en cuarentena pueden tener acceso a actualizaciones de software y archivos de firma de antivirus para cumplir los requisitos de directiva.

-   **Servidor web (opcional)**. Los servidores web se pueden usar en cuarentena para proporcionar instrucciones al usuario para poder quitar a sus equipos del estado de cuarentena. Algunos paquetes de actualización también usan componentes web para la entrega, como algunos productos antivirus.

### Uso de la autenticación 802.1X para protegerse frente a clientes inalámbricos no administrados

En la sección anterior se presentó la autenticación 802.1X como la opción más efectiva disponible para proteger las redes inalámbricas de equipos que no son de confianza. Se describieron los distintos métodos 802.1X que se admiten de forma nativa en las versiones actuales de Microsoft Windows, además de darse una explicación del motivo por el que la autenticación 802.1X no es tan efectiva para las redes con cable (aunque es muy efectiva para las redes inalámbricas). Con esta información, se puede hablar de las diferencias entre los métodos admitidos y determinar cuál puede ser el más indicado para los distintos tipos de entornos de red de las medianas empresas.

### Comparaciones de 802.1X

Como se ha indicado, hay tres métodos 802.1X admitidos en las versiones actuales de Microsoft Windows, que son:

-   EAP-MD5

-   EAP protegido (PEAP)

-   EAP-TLS

De estos tres métodos, el primero (EAP-MD5) se considera el menos seguro porque las frases de contraseña usadas en él se transmiten por aire y, por tanto, se podrían interceptar. Las otras dos opciones (PEAP y EAP-TLS) merecen ser tenidas en cuenta para su implementación en redes de medianas empresas.

La implementación de Microsoft de PEAP usa el Protocolo de autenticación por desafío mutuo versión 2 de Microsoft (MS-CHAP v2), originalmente diseñado como método de autenticación VPN de acceso telefónico, pero que se puede usar también con PEAP porque puede admitir las estrictas directivas de contraseñas de usuario disponibles en Active Directory. Este método es más sencillo de implementar que EAP-TLS y su costo es inferior en recursos y costo inicial, ya que no es necesario implementar muchos servidores y servicios adicionales. Si bien esta solución no necesita certificados para los servidores de autenticación, estos certificados los podrían generar proveedores de certificados de terceros porque no son muchos los que se necesitan para la implementación.

Sin embargo, EAP-TLS se considera como la implementación más segura de 802.1X que hay disponible, ya que necesita certificados tanto en el cliente como en el servidor de autenticación para realizar la autenticación mutua. Debido a que sería necesario un gran número de certificados para dicha implementación, se sugiere que se implemente una infraestructura de clave pública si no existe aún. Por tanto, se considera que EAP-TLS tiene unos mayores costos de compatibilidad e implementación en comparación con PEAP con MS-CHAP v2.

### Proceso de decisión de 802.1X

Para facilitar el proceso de decisión sobre qué implementación de 802.1X es mejor para un entorno de red concreto, Microsoft diseñó el siguiente árbol de decisiones de 802.1X.

![](images/Cc875843.PNFUC09(es-es,TechNet.10).gif)

**Figura 9. Árbol de decisiones de 802.1X**

Este gráfico puede crear alguna confusión porque en él se usa el término “gran empresa”. Este término se debe entender como que se refiere en general a cualquier empresa con al menos 500 empleados y un personal de TI de apoyo de al menos 5 profesionales técnicos. Teniendo en cuenta esta información, está claro que cualquiera de las soluciones sería recomendada para un entorno de red de una mediana empresa. Por tanto, el proceso de decisión evoluciona más en la línea de ganas de asumir riesgos y rentabilidad.

La diferencia principal entre PEAP y EAP-TLS incluye la necesidad de una infraestructura de certificados, motivo por el que normalmente EAP-TLS se suele considerar la opción más adecuada para las necesidades de empresas más grandes y PEAP se suele considerar como un método suficiente para empresas más pequeñas si no existen requisitos normativos que exijan estándares de seguridad más estrictos. Al margen de las consideraciones de costos, en ocasiones las organizaciones tienen necesidades adicionales de una infraestructura de certificados, lo cual proporciona una justificación adicional para invertir en PKI. Después de todo, si se necesitan muchos certificados para las firmas de código o contenido web, sólo sería razonable usar la inversión en infraestructura para implementar la forma más segura de autenticación 802.1X.

### Requisitos de 802.1X PEAP

Una implementación PEAP basada en Microsoft con MS-CHAP v2 necesita al menos dos servidores IAS RADIUS para funcionar como servidores de autenticación y autenticar los clientes inalámbricos en una base de datos de cuenta de Active Directory. El número de servidores RADIUS puede tener que ajustarse según el número de sitios remotos o para aceptar un número mayor de intentos de autenticación de usuarios.

La existencia de ubicaciones remotas no hace necesario automáticamente servidores RADIUS IAS adicionales. Sin embargo, si las ubicaciones remotas no tienen conexiones redundantes de gran ancho de banda o ya tienen sus propios controladores de dominio y otros recursos locales, se deberían agregar servidores de autenticación adicionales para tales sitios.

### Requisitos de 802.1X EAP-TLS

Como se mencionó anteriormente, EAP-TLS necesita más recursos que las implementaciones PEAP debido a los requisitos de certificados adicionales. Por supuesto, se pueden usar proveedores de terceros para emitir los certificados de requisitos para todos los clientes inalámbricos y servidores de autenticación, pero este método es más costoso que implementar una infraestructura de certificados, excepto cuando el número de clientes inalámbricos está limitado estrictamente a unos pocos usuarios.

En total, un sencilla implementación de EAP-TLS necesitaría al menos cuatro servidores, más en el caso de compañías más grandes o de redes con distribución geográfica. Dos de los cuatro servidores actuarán como servidores RADIUS IAS redundantes y los otros dos como la infraestructura de certificados. De los dos servidores de certificados, se recomienda que uno (el servidor de certificados raíz) esté separado de la red y desconectado de ésta, lo que puede significar que se puede reducir el número de servidores en uno en determinadas circunstancias.

### Uso de WEP o WPA

Otro problema con respecto a la seguridad inalámbrica que se debe tener en cuenta es si se va a usar o no el cifrado inalámbrico y, en caso afirmativo, qué estándar se debe usar. Para un entorno de mediana empresa, hay muy pocos motivos por los que se deba tener en cuenta la falta de cifrado inalámbrico, motivos relacionados con empresas que ofrecen conexiones a Internet inalámbricas de acceso público. De lo contrario, para proteger la seguridad de una red inalámbrica es fundamental que se implemente alguna forma de cifrado inalámbrico junto con la autenticación 802.1X.

El cifrado inalámbrico se presenta en las dos formas siguientes, con una variante adicional:

-   **WEP**. El estándar Privacidad equivalente por cable formaba parte del estándar IEEE 802.11 original que usa el cifrado RC4 de 64 o de 128 bits para proteger las comunicaciones inalámbricas. Se detectaron graves defectos que hacen que este método de cifrado sea extremadamente vulnerable a los ataques de escucha pasiva. Hay disponibles una serie de herramientas que permiten descodificar las transmisiones WEP en un período de tiempo relativamente corto, en ocasiones incluso en cuestión de minutos. En general, el uso de WEP no está recomendado para los entornos de negocios, pero se puede proteger en cierta forma mediante el uso de distintos métodos, incluida la autenticación 802.1X.

-   **WPA**. Como respuesta a la debilidad inherente en el estándar WEP, un consorcio de líderes del sector que incluía a Microsoft y al Wi-Fi Institute creó el estándar Wi-Fi Protected Access (WPA, Acceso protegido de fidelidad inalámbrica) como implementación parcial del estándar 802.11i que estaba en ese momento aún en desarrollo. Este estándar proporciona un cifrado mucho más seguro al usar el protocolo de integridad de clave temporal para el cifrado de los datos, que resulta mucho mejor que el deficiente estándar WEP. La mayoría de los puntos de acceso inalámbricos (WAP) actuales del mercado admiten el estándar WPA, al igual que las versiones actuales del sistema operativo Microsoft Windows.

-   **WPA2**. En septiembre de 2004 Wi-Fi Alliance creó el estándar Wireless Protected Access 2 (WPA2, Acceso protegido inalámbrico). Está certificado como implementación completa de la especificación IEEE 802.11i, ratificada en junio de 2004. Este estándar admite los métodos de autenticación EAP basados en 802.1X o la tecnología PSK (a los que en ocasiones también se conoce como WPA de modo personal), pero presenta el mecanismo de cifrado avanzado que usa Counter-Mode/CBC-MAC Protocol (CCMP) denominado Estándar de cifrado avanzado (AES, del inglés Advanced Encryption Standard). Esta implementación de cifrado inalámbrico es extremadamente segura. La mayoría de los proveedores admiten WPA2 en cierta forma, incluidas las versiones actuales del sistema operativo Microsoft Windows.

Si fuera posible, se debería usar WPA2 o WPA para ayudar a proteger los datos inalámbricos. Sin embargo, tal vez esto no se pueda porque estos estándares son más nuevos, especialmente si ya se realizaron importantes inversiones inalámbricas que no las admiten. Como se mencionó anteriormente, se puede aumentar el nivel de seguridad que ofrece el estándar WEP mediante la configuración de autenticación 802.1X y los cambios frecuentes de los pares de claves. Sin embargo, incluso así, el uso de WEP se debe reservar para las redes inalámbricas que se encuentren en transición al estándar WPA o WPA 2.

### Uso de SMS para detectar sistemas no administrados

Microsoft Systems Management Server (SMS) 2003 es una herramienta de administración muy versátil en una red de Microsoft. Con SMS se pueden centralizar varias funciones de administración, incluida la entrega de software, la implementación de actualización de seguridad y la auditoría de sistemas. Es fundamental para estas funciones contar con un inventario de sistemas automatizado y centralizado desde el cual poder implementar estas herramientas increíblemente útiles, motivo por el que la detección de sistemas no administrados entra en juego.

SMS 2003 proporciona distintos métodos de detección que los administradores pueden usar para crear la base de datos de recopilación de equipos, que contiene información sobre todos los equipos de la red. Estos métodos de detección varían desde el método de detección de Active Directory (que actualiza la recopilación con los detalles que proporcionan las listas de cuentas de los equipos de Active Directory) hasta el método de detección de la red (que supervisa de forma activa si hay dispositivos conectados en la red). Estos métodos de detección se pueden configurar para que se produzca de forma automática a intervalos predefinidos y que actualicen las base de datos de recopilaciones cuando terminen.

Para responder a la necesidad de detectar sistemas no administrados cuando se conectan a la red, se puede configurar la detección de la red para que se produzca de forma más frecuente y, posteriormente, revisar los resultados a intervalos regulares para determinar cuándo se conectó un nuevo sistema a la red. Cuando se producen estas conexiones de sistemas, se pueden comprobar con respecto a una lista establecida de nuevos equipos o peticiones de conexión a la red con el fin de confirmar que el nuevo sistema está autorizado para su uso en la red.

### Proceso de detección de la red

Uno de los inconvenientes de este método de detección de los sistemas no administrados es que SMS puede tener dificultades a la hora de detectar los detalles de los equipos que usan sistemas operativos que no sean Microsoft Windows. De hecho, incluso las versiones anteriores a Microsoft Windows 98 SE pueden no ser detectadas por los métodos de detección de SMS 2003, ya que no admiten las implementaciones de la interfaz de administración de Windows (WMI). En consecuencia, es necesario agregar scripts a este proceso de solución para que se pueda detectar cualquier dispositivo cuando se conecte a la red. En la siguiente figura se muestra cómo funcionaría dicho proceso.

![](images/Cc875843.PNFUC10(es-es,TechNet.10).gif)

**Figura 10. Proceso de detección de un equipo no administrado con SMS**

Esta figura muestra los métodos de detección que se podrían usar para agregar distintos tipos de equipos a la base de datos de recopilación de SMS. Hay tres tipos distintos de equipos a los que hay que enfrentarse, incluidos los siguientes:

-   **Sistemas administrados accesibles mediante SMS**. SMS puede administrar estos equipos y, de hecho, ya los administra. Ya están incluidos en la base de datos de recopilación de SMS y se deben configurar para su administración automática. Probablemente se considerarán parte de la red de confianza y no necesitan más atención.

-   **Sistemas no administrados con accesibilidad SMS**. Estos equipos pueden ser administrados por SMS pero no se han puesto bajo la administración de SMS. SMS los puede detectar o no, según su ubicación en la red (por ejemplo, detrás de firewalls o no), y pueden incluir equipos administrados por otros medios. Estos equipos deben estar incluidos en una lista de exenciones que incluya detalles de administración. Si no lo están, se deben considerar como que no son de confianza y se deben investigar más profundamente. Pueden ser detectados por SMS, a menos que haya cualquier dispositivo de red que bloquee dicha actividad.

-   **Sistemas no administrados sin accesibilidad SMS**. Estos equipos no se pueden administrar mediante SMS por lo que quedan fuera del control de SMS. Pueden o no incluir sistemas conocidos administrados por otros medios. Estos equipos deben estar incluidos en una lista de exención que incluya detalles de administración. Si no lo están, se deben considerar como desconocidos y que no son de confianza y se deben investigar más profundamente. Estos equipos sólo se pueden detectar mediante el uso de procesos que no sean la detección de SMS, incluidos los scripts de detección personalizados.

En este momento, debe quedar claro que el proceso de detección de sistemas no administrados de la red depende del establecimiento de procesos que documenten los detalles de cada una de las conexiones de equipos autorizados en la red. Dicha documentación debe incluir detalles sobre el equipo, si está o no administrado por métodos automatizados (como SMS) y, en caso contrario, qué proceso se usa para conseguir que el equipo cumpla con las directivas de seguridad establecidas, si existe alguno. Por supuesto, podría existir un equipo autorizado en una red al que no se le exigiera que cumpliera los estándares de seguridad, pero a estos equipos se les debe forzar a permanecer en un segmento de red que no sea de confianza que esté aislado de la red de confianza.

Cuando se aplica un proceso de “adición de equipos” documentado que detalla todos los equipos que se sabe que existen en la red y que están autorizados, se puede usar esta información para determinar lo que está autorizado y lo que no. Cualquier equipo detectado en la red que no exista en esta lista se debe considerar como sospechoso y se debe investigar de forma inmediata.

### Implementación y administración

La sección "Desarrollo" ofrece información acerca de los detalles necesarios para crear planes de implementación. En esta sección se detallan algunos de los problemas de implementación comunes y los procesos que pueden servir a los implementadores de la tecnología cuando apliquen estas soluciones o a las personas que toman las decisiones a comprender mejor lo que estas soluciones implican para que puedan tomar una decisión bien fundamentada acerca de si son adecuadas para un entorno concreto.

### Uso de IPsec para aislar dominios y servidores

Debido a la complejidad asociada al aislamiento de redes basado en IPsec, se recomienda a los implementadores adoptar un método en fases para la implementación de esta solución en una red de producción. Hay varios métodos que sirven para conseguir esa implementación en fases y se basan en cómo se aplican las directivas IPsec: por grupos o por directiva.

Independientemente del método que se use, es importante usar ejemplos piloto de cada grupo durante las fases iniciales de la implementación, además de probar el impacto de esta solución en un entorno de prueba, si es posible. La implementación de IPsec debe seguir un proceso de petición de control de cambios formal que detalle los planes de reversión, junto con la compra informada por parte de los propietarios de los procesos de negocio afectados y la tecnología.

### Implementación de IPsec por grupo

El método de implementación del aislamiento de redes IPsec por grupo usa directivas IPsec totalmente definidas que controlan la implementación mediante el uso de listas ACL en los GPO que entregan las directivas. Todas las directivas IPsec tendrán totalmente definidas todas las exenciones y subredes de protección con todas las acciones de filtro adecuadas activadas antes de que se produzca la implementación.

Cuando finaliza la configuración, los administradores crean GPO para cada directiva IPsec y grupos de equipos para administrar esos GPO. Cuando se crean, las directivas IPsec adecuadas se asignan a su GPO correspondiente y los GPO se vinculan a los objetos adecuados de Active Directory. En ese momento del proceso no se debe entregar ninguna de las directivas, ya que las ACL que controlan la asignación de GPO están vacías.

Cuando se identifican los equipos piloto, las cuentas de equipo correspondientes se pueden colocar en los grupos de equipos adecuados y se aplicará la directiva IPsec cuando pase el próximo intervalo de sondeo de GPO. Conforme se agregan más equipos a la lista de implementación en fases, sus cuentas correspondientes se pueden colocar en los grupos adecuados para la entrega de directivas.

Este método requiere especial cuidado en el planificación para garantizar que no se interrumpan las comunicaciones. Por ejemplo, si un servidor que incluye una aplicación usada por todos los hosts se colocara en un grupo protegido que necesite comunicación cifrada con IPsec, se interrumpiría la comunicación de los equipos que aún no se hubieran agregado a los grupos, así como cualquier host que no pudiera usar el cifrado IPsec.

### Implementación de IPsec por directiva

En este método crea las directivas IPsec desde cero durante la implementación, en lugar de antes de la implementación de producción real. Con este método, las directivas IPsec iniciales sólo incluyen listas de excepción sin reglas establecidas para que los equipos negocien la seguridad. Después de entregar la directiva inicial, los administradores pueden crear una regla de seguridad con un filtro que sólo afecte a una subred. Conforme avanza la implementación, las subredes adicionales se pueden agregar a la regla de protección hasta que la directiva alcance el estado de implementación final.

Las ventajas del uso de este método de implementación por fases son que IPsec se negocia sólo para un pequeño porcentaje del tráfico TCP/IP total, en lugar de para todas las subredes, como ocurre con un método de grupo a grupo. Asimismo, este método permite probar todas las rutas de acceso de las redes de una sola subred, por lo que se reduce el número de clientes afectados si se produce algún problema. Sin embargo, el problema con este método es que se aplica a todos los equipos del dominio o grupo de aislamiento, y no sólo a equipos concretos como con el método de grupo a grupo. Asimismo, todos los equipos sufrirán el retraso de tres segundos para recuperarse en algún momento cuando inicien las conexiones con las subredes especificadas.

Este método funciona bien en el caso de redes complejas con varias subredes, pero es poco recomendado para redes más pequeñas con un número relativamente reducido de subredes.

### Listas de exención

Incluso el modelo de aislamiento de red con el mejor diseño posible encontrará algunas restricciones cuando se implemente en un entorno de producción. Normalmente, los componentes clave de un entorno de red como los servidores DNS y los controladores de dominio suponen algunos desafíos que se deben tratar. Dichos sistemas se deben proteger pero también deben estar disponibles para todos los sistemas de una red. Por tanto, deben estar abiertos a las peticiones de conexión entrantes. También se pueden manifestar otros problemas cuando se aplica el plan, pero hay un método que permite resolver estos problemas: las listas de exención

Una lista de exención está compuesta por una lista de equipos que no se pueden proteger con IPsec y que se tendrá que implementar en cada directiva IPsec diseñada. Debido a que IPsec sólo admite el filtrado estático, cualquier host que se agregue a una lista de exención permitirá tanto el tráfico saliente como entrante de todas las partes de la red, ya sean de confianza o no. Por este motivo, la lista de exención debe ser lo más reducida posible, ya que estos hosts necesitarán una protección adicional mediante la protección del servidor y el filtrado con firewall de estado del host para mitigar los riesgos a que se enfrentan de dispositivos no administrados. También puede resultar útil colocar en la lista de exención los hosts de una sola subred o VLAN para facilitar la administración o consolidar las funciones del servidor con el fin de reducir el número de hosts exentos.

Algunos de los hosts que tal vez se tengan que agregar a una lista de exención son:

-   Controladores de dominio que no admiten la comunicación IPsec con los miembros de dominio, incluso aunque proporcionen las directivas IPsec a los miembros del dominio y realicen la autenticación Kerberos en la que se basa el aislamiento de la red.

-   Hosts que puedan sufrir un impacto inaceptable en el rendimiento, lo cual se puede producir en los hosts que tengan que administrar miles de clientes de forma simultánea, así como hosts que se vean afectados por el retraso de tres segundos para recuperarse, como los servidores DHCP.

-   Hosts que no tengan una implementación de IPsec compatible o que proporcionarán servicios a equipos de confianza y de no confianza, pero que no usarán IPsec.

Al igual que con el grupo de límites, debe existir un proceso de aprobación formal de los hosts que se deben agregar a las listas de exención.

**Nota**   Hay una revisión de “directiva sencilla” para Microsoft Windows XP y Windows Server 2003 que hace que no sean necesarias las listas de exención. Para obtener más información, consulte el artículo de Knowledge Base [914841](http://support.microsoft.com/?kbid=914841) en http://support.microsoft.com/?kbid=914841.

### Consideraciones acerca de la administración de IPsec

Una vez implementadas, las directivas IPsec afectan a la comunicación entre muchos hosts de la red. Por tanto, los cambios que se producen después de cada implementación pueden tener un profundo efecto en muchos usuarios. Por este motivo, todos los cambios realizados en una red de aislamiento basada en IPsec debe seguir un proceso de administración de cambios MOF estandarizado que incluye lo siguiente:

-   Cambiar la petición (RFC)

-   Cambiar la clasificación

-   Cambiar la autorización

-   Cambiar el plan de desarrollo

-   Cambiar el plan de publicación

-   Cambiar la revisión

Microsoft recomienda que se use Windows Server 2003 como plataforma de administración de IPsec. Para facilitar las tareas de administración, los administradores puede usar el complemento MMC de la directiva de seguridad IP o la herramienta de la línea de comandos Netsh en la consola de Windows Server 2003. De lo contrario, la administración de directivas IPsec será una tarea bastante sencilla porque se realiza mediante la directiva de grupo. Por tanto, la adición de nuevos equipos a la red de confianza se puede automatizar si se usa un proceso de "adición de equipos" establecido.

Sin embargo, se deben tener en cuenta algunos factores para cuando se deban realizar cambios, entre ellos:

-   Cualquier cambio en una acción de filtro que se usara para un SA IPsec hará que se eliminen los SA establecidos en esa configuración de directiva. Esta funcionalidad crea un nuevo intento de modo rápido si hay algún tráfico en ruta, lo que puede provocar una caída del tráfico de red.

-   El cambio del método de autenticación o del método de seguridad del modo principal hará que IKE elimine los modos principales existentes. En algunas circunstancias, esta funcionalidad puede hacer que fallen las negociaciones del modo principal de IKE del lado servidor con los clientes.

-   Cuando cambien las directivas IPsec de un GPO, se producirán determinados retrasos (incluido el retraso de replicación de Active Directory y el retraso de sondeo de GPO), que pueden ir desde minutos hasta horas, según el tamaño y la complejidad del entorno.

Otra consideración de administración es la forma de aislar los equipos sospechosos cuando se produzcan infecciones. Hay una serie de formas distintas de dar respuesta a las actividades malintencionadas, entre ellas:

-   **Aislamiento del dominio de aislamiento**. Al modificar el filtro IPsec de modo de petición seguro para deshabilitar la comunicación desprotegida, la red aislada puede quedar totalmente desconectada de la red desprotegida cuando se sospeche que un dispositivo que no sea de confianza es una plataforma de actividades malintencionadas.

-   **Bloqueo de puertos sospechosos**. Al crear listas de filtros con dos filtros unidireccionales, se puede bloquear el tráfico por puertos. Este método se debe usar con precaución, ya que puede bloquear el tráfico necesario, como DNS, lo que dificultaría la realización de más cambios o reversiones IPsec.

-   **Aislamiento en dominios secundarios**. Al cambiar las directivas de un dominio para usar una clave precompartida en lugar del protocolo Kerberos para la autenticación IPsec, se puede aislar un dominio del resto de dominios de un bosque.

-   **Aislamiento en grupos predefinidos**. Al usar claves precompartidas o certificados para la autenticación IPsec en lugar del protocolo Kerberos, se pueden crear grupos de aislamiento que usen distintas claves o certificados que sirvan para realizar el mismo tipo de funcionalidad de aislamiento.

### Uso de los servicios de cuarentena de VPN para protegerse frente a equipos remotos no administrados

La implementación real del control de cuarentena de VPN conlleva seis pasos más allá de cualquier otro proceso de solicitud de administración de cambios y procesos de prueba previa a la implementación que se puedan producir en una determinada organización. Estos seis pasos son:

1.  Crear recursos de cuarentena.

2.  Crear scripts para validar las configuraciones de los clientes.

3.  Instalar el componente de escucha Rqs.exe en servidores de acceso remoto.

4.  Crear perfiles de Connection Manager (CM) de cuarentena con CMAK de Windows Server 2003.

5.  Distribuir los perfiles CM en equipos cliente de acceso remoto.

6.  Configurar la directiva de acceso remoto de cuarentena.

### 1. Crear recursos de cuarentena

Si los clientes en cuarentena van a usar recursos internos para permitir que tengan un estado que cumpla las directivas de seguridad establecidas, tendrá que haber un conjunto de recursos accesibles que se puedan usar para instalar las actualizaciones de requisitos y otro software necesario para conseguir que sean seguros. Como se detalló en la sección anterior, estos recursos suelen incluir un servidor de nombres, servidores de archivos y, en ocasiones, también servidores web. Se pueden usar un par de métodos al diseñar estos recursos de cuarentena, incluido el diseño de servidores existentes que residan en la red interna y la colocación de los recursos necesarios en su propia subred independiente.

El primer método de diseño de servidores individuales puede reducir los costos relacionados con la agregación de dichos servidores para entregar actualizaciones, porque se usarán los servidores existentes. Sin embargo, para este método se necesitan filtros de paquetes más complejos porque cada recurso tendrá su propio conjunto de filtros en el atributo MS-Quarantine-IPFilter de la directiva de acceso remoto de cuarentena.

Colocar todos los recursos de cuarentena en una sola subred destinada a servicios de cuarentena puede implicar la adición de más servidores al entorno de red, pero sólo se necesita un filtro de paquetes de entrada y salida para todos los recursos de cuarentena.

### 2. Crear scripts de validación

Los scripts de cuarentena realizan un conjunto de pruebas que garantizan la conformidad de los equipos de acceso remoto de las directivas de seguridad. Cuando se realizan estas pruebas, el script tendrá que iniciar el componente de cliente RQC.exe (si es correcto) o dirigir el equipo cliente a los recursos adecuados para conseguir que cumpla los requisitos. Por supuesto, el script también podría simplificar la aplicación de un tiempo de espera de red junto con un mensaje de error si las directivas de red determinan este método en su lugar. Estos scripts puede ser tan sencillos como un archivo por lotes de la línea de comandos o archivos ejecutables complejos.

Se pueden revisar y descargar algunos scripts de ejemplo en la página* *[Scripts de ejemplo de cuarentena de VPN](http://www.microsoft.com/downloads/details.aspx?familyid=a290f2ee-0b55-491e-bc4c-8161671b2462&displaylang=en) en el centro de descarga de Microsoft en la dirección www.microsoft.com/downloads/details.aspx?FamilyID=a290f2ee-0b55-491e-bc4c-8161671b2462&displaylang=en (puede estar en inglés).

### 3. Instalar RQS.exe en servidores de acceso remoto

El proceso de instalación del servicio Agente de cuarentena de acceso remoto (Rqs.exe) en un equipo con Microsoft Windows Server 2003 es distinto para los servidores con el Service Pack 1 (SP1). Por brevedad, esta sección sólo describe la instalación en Windows Server 2003 con SP1, porque se asume que todos los sistemas tienen los Service Pack y las actualizaciones de seguridad más recientes.

**Para instalar Rqs.exe en un servidor con Windows Server 2003 con SP1**

1.  Haga clic en **Inicio** y, a continuación, en **Panel de control**.

2.  Haga clic en **Agregar o quitar programas**.

3.  Haga clic en **Agregar o quitar componentes de Windows**.

4.  Seleccione **Componentes** y, a continuación, **Servicios de red**.

5.  Haga clic en **Detalles**.

6.  Seleccione **Subcomponentes de Servicios de red**, haga clic en **Servicio de cuarentena de acceso remoto** y, a continuación, haga clic en **Aceptar**.

Este proceso instala pero no inicia el servicio de cuarentena, que el administrador debe iniciar manualmente cuando la solución esté completamente configurada y el entorno esté preparado para la implementación.

Un paso adicional en el proceso de instalación incluye la modificación de las cadenas de versión de script para que coincidan con la cadena de versión configurada para Rqc.exe en el script de cuarentena. Se puede configurar Rqs.exe para que acepte varias cadenas de versión de script que, a su vez, se escriben en el Registro del servidor de acceso remoto en **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\rqs\\AllowedSet**, que es el lugar donde se deben aplicar estos valores mediante el tipo de valor REG\_MULTI\_SZ. Normalmente, el valor **Allowed Set** está establecido en **RASQuarantineConfigPassed**, pero se pueden agregar más valores de cadena.

### 4. Crear perfiles CM de cuarentena

Un perfil CM de cuarentena es simplemente un perfil CM de acceso remoto con los siguientes elementos adicionales:

-   Una acción posterior a la conexión que ejecuta el script creado para comprobar la conformidad con la directiva de red y el propio script. Esto se realiza mediante la página Acciones personalizadas del asistente CMAK.

-   También se debe agregar un componente de notificación al perfil, como se hace en la pantalla **Archivos adicionales** del asistente CMAK.

### 5. Distribuir perfiles CM

Se deben distribuir los perfiles CM de cuarentena que se acaban de crear e instalar en todos los equipos cliente de acceso remoto. Un perfil se presenta como un archivo ejecutable que se tiene que ejecutar en cada cliente de acceso remoto para que instale el perfil y configure la conexión de red de cuarentena.

La distribución de estos perfiles puede ser un proceso manual, en el que se envían como archivos adjuntos a los usuarios junto con instrucciones, por ejemplo. O bien, se podría automatizar la distribución con herramientas como la distribución del software SMS 2003. Hay una serie de métodos que se podrían usar y el mejor método varía para cada entorno.

### 6. Configurar una directiva de acceso remoto de cuarentena

El procedimiento de configuración de una directiva de acceso remoto de cuarentena varía en función de si está o no configurada en un servidor IAS o en otro proveedor de autenticación, de la siguiente manera:

-   Si se configura en un servidor RADIUS IAS, use el complemento Servicio de autenticación de Internet.

-   Si se configura en un proveedor de autenticación de Windows, use el complemento Enrutamiento y acceso remoto.

Al crear una directiva, se debe realizar primero una directiva de acceso remoto en modo normal. A continuación, se deben agregar los atributos MS-Quarantine-Session-Timeout y MS-Quarantine-IPFilter en la ficha **Opciones avanzadas** de las propiedades del perfil de la directiva de acceso remoto.

Si se usa RADIUS, la directiva de acceso remoto de cuarentena se tiene que replicar en los demás servidores RADIUS mediante la copia de la configuración o la creación manual de ésta en cada servidor.

### Uso de la autenticación 802.1X para protegerse frente a clientes inalámbricos no administrados

Como se describe en las secciones anteriores, las opciones que recomienda Microsoft, de la más a la menos segura, para proteger la red inalámbrica de una mediana empresa son:

-   WPA2/AES y EAP-TLS

-   WPA2/AES y PEAP-MS-CHAP v2

-   WPA/TKIP y EAP-TLS

-   WPA/TKIP y PEAP-MS-CHAP v2

Si bien EAP-TLS o PEAP-MS-CHAP v2 pueden hacer que WEP sea más seguro, el uso de WEP como parte de una de estas soluciones sólo se recomienda durante una transición a los estándares más seguros WPA o WPA2.

Los procesos de implementación de EAP-TLS y PEAP-MS-CHAP v2 comparten algunas similitudes. En ambos se deben usar servidores RADIUS IAS de Microsoft como parte de la solución y ambos necesitan certificados de algún tipo, pero para EAP-TLS se necesitan certificados en el equipo cliente y el servidor, mientras que para PEAP-MS-CHAP v2 sólo se necesitan para los servidores de autenticación. Éste es el motivo por el que una infraestructura de certificados es muy recomendable cuando se implementa EAP-TLS, debido a que el costo de adquirir certificados de terceros proveedores para todos los clientes puede ser prohibitivo.

### Autenticación inalámbrica con EAP-TLS y PEAP-MS-CHAP v2

Los procesos de implementación de EAP-TLS y PEAP-MS-CHAP v2 incluyen una serie de detalles que no son objeto de este documento. Sin embargo, existen algunos recursos excelentes para ayudarle a diseñar e implementar soluciones para proteger las redes inalámbricas, como:

-   La página [Implementación de redes 802.11 protegidas mediante Microsoft Windows](http://www.microsoft.com/technet/prodtechnol/winxppro/deploy/ed80211.mspx) de Microsoft TechNet, que suministra información sobre la implementación para ambos métodos de autenticación IEEE 802.1X, se encuentra en www.microsoft.com/technet/prodtechnol/winxppro/deploy/ed80211.mspx (puede estar en inglés).

-   En la página [Protección de LAN inalámbricas con Servicios de Certificate Server](http://go.microsoft.com/fwlink/?linkid=14844) que se encuentra en la dirección http://go.Microsoft.com/fwlink/?LinkId=14844 (puede estar en inglés), encontrará recursos e información detallada acerca de la implementación de EAP-TLS en redes Microsoft.

-   En la página [Protección de LAN inalámbricas con PEAP y contraseñas](http://go.microsoft.com/fwlink/?linkid=23481) en la dirección http://go.Microsoft.com/fwlink/?LinkId=23481 (puede estar en inglés), encontrará información detallada acerca de la implementación de PEAP-MS-CHAP v2 en redes Microsoft.

-   Es necesaria la [actualización de Wi-Fi Protected Access 2 (WPA2) o Wireless Provisioning Services Information Element (WPS IE) para Windows XP con SP2](http://support.microsoft.com/default.aspx?scid=kb;en-us;893357), que encontrará en la dirección http://support.microsoft.com/default.aspx?scid=kb;en-us;893357 para que Microsoft Windows XP con SP2 admita el estándar WPA2.

### Uso de SMS para detectar y tratar los sistemas no administrados

Como se explica en la sección "Desarrollo", el proceso de detección de SMS es muy útil para encontrar equipos que se acaban de conectar a la red cuando SMS los puede administrar. También se menciona el hecho de que SMS tiene dificultades para detectar algunos sistemas no administrables durante el proceso de detección, por lo que tal vez se necesite otro mecanismo para rellenar este hueco.

Puede haber varios motivos por los que SMS no pudiera detectar los equipos conectados a una red. Entre ellos:

-   El equipo está conectado pero no se está ejecutando en el momento de la detección y no tiene una cuenta de equipo en el dominio.

-   El equipo está conectado a una subred donde un firewall u otro dispositivo de red evita la comunicación entre el servidor de SMS y dicha subred.

-   El equipo está conectado a una red accesible pero usa un sistema operativo que SMS no puede detectar.

Para tratar dichas eventualidades, se necesita una solución personalizada que combine la utilidad de SMS con scripts que traten las excepciones a lo que SMS puede administrar. Se pueden usar scripts personalizados para explorar la red a intervalos regulares con un proceso de administrador, lo que significa que pueden detectar dispositivos que puede que sólo estén activos durante breves períodos de tiempo. También se pueden ejecutar dichos scripts desde estaciones de trabajo o servidores de subredes aisladas con otro método, lo que significa que se pueden detectar cuando se conecten sistemas no administrados a estos segmentos de red sin supervisar con otros métodos. Esos scripts no intentan realizar procesos de detección basados en WMI y, por tanto, no se ven afectados por el sistema operativo que pudieran estar usando los clientes no administrados.

Para obtener más información acerca de cómo usar SMS para detectar dispositivos en la red, consulte el acelerador de solución [Administración de revisiones mediante Systems Management Server 2003](http://www.microsoft.com/technet/itsolutions/cits/mo/swdist/pmsms/2003/pmsms031.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/swdist/pmsms/2003/pmsms031.mspx (puede estar en inglés) o la página principal de [Microsoft Systems Management Server](http://www.microsoft.com/smserver/default.mspx) en www.microsoft.com/smserver/default.mspx para obtener más vínculos, incluidos los vínculos a recursos sobre las soluciones de scripting SMS.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

Este documento ha demostrado que es posible usar un método completo que permita solucionar los problemas relacionados con los sistemas no administrados. El aislamiento de redes IPsec se ha usado para evitar que los sistemas no administrados tuvieran acceso a recursos de red de confianza y para contribuir a la aplicación de los requisitos de seguridad mediante la denegación de servicio a los equipos que no los cumplen. Se pueden usar servicios de cuarentena de VPN para exigir la conformidad con los requisitos en equipos móviles que usan una solución de acceso remoto pero que se conectan con poca frecuencia a la red local. Se pueden usar IEEE 802.1X y WPA/WPA2 para defenderse frente a dispositivos independientes en LAN inalámbricas. Finalmente, se pueden usar SMS y scripts de detección para facilitar la detección de sistemas no administrados, así como ayudar a mantener actualizados los equipos administrados con todas las revisiones y actualizaciones de seguridad.

Si bien estas soluciones técnicas ayudan a resolver muchos problemas relacionados con los dispositivos no administrados e independientes, dichas soluciones sólo se pueden mejorar cuando se crean directivas de seguridad sólidas y también se establecen estrictos procesos de administración de cambios. Cuando se combinan todas estas soluciones, directivas y procesos, el resultado es una infraestructura de mediana empresa administrable que puede reducir los costos administrativos y los riesgos de seguridad a niveles aceptables.

[](#mainsection)[Principio de la página](#mainsection)

### Apéndice A: Protección de acceso a redes

Protección de acceso a redes (NAP) es una nueva función que formará parte de la próxima generación de Windows (Microsoft Windows Server Longhorn y Windows Vista™) y que permitirá exigir la conformidad con las directivas de mantenimiento de los equipos. Con NAP, los administradores pueden establecer umbrales de directivas de validación de estado mediante una interfaz de programación de aplicación (API) que limite el acceso de red para los equipos que no cumplen los requisitos de mantenimiento cuando se conectan a la red.

La flexibilidad de NAP permite a los administradores configurar soluciones personalizadas para los requisitos de su entorno, ya sea simplemente para registrar el estado de los equipos que se conectan a la red, implementar automáticamente actualizaciones de software o limitar la conectividad de sistemas que no cumplen los requisitos de mantenimiento. Además, NAP es lo suficientemente flexible como para permitir la integración con aplicaciones de terceros y soluciones de programas personalizadas para que la implementación de directivas de mantenimiento de los equipos sea completa. NAP también será una solución completa; sus componentes de exigencia permitirán a los administradores forzar la conformidad con las directivas de mantenimiento mediante DHCP, VPN y redes inalámbricas 802.1X, y es compatible con IPsec.

Para obtener más información acerca de NAP, consulte la página principal [Protección de acceso a redes](http://www.microsoft.com/technet/itsolutions/network/nap/default.mspx) en www.microsoft.com/technet/itsolutions/network/nap/default.mspx (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener el artículo Protección de una red frente a clientes no administrados](http://go.microsoft.com/fwlink/?linkid=71713)

[](#mainsection)[Principio de la página](#mainsection)
