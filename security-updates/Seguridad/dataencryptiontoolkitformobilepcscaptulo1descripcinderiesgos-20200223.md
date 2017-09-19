---
TOCTitle: 'Data Encryption Toolkit for Mobile PCs: Capítulo 1: Descripción de riesgos'
Title: 'Data Encryption Toolkit for Mobile PCs: Capítulo 1: Descripción de riesgos'
ms:assetid: 'df2c6d71-98f7-4212-b3b7-b9eb2f501348'
ms:contentKeyID: 20200223
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162822(v=TechNet.10)'
---

Data Encryption Toolkit for Mobile PCs: análisis de seguridad
=============================================================

### Capítulo 1: Descripción de riesgos

Publicado: abril 4, 2007

Los datos confidenciales, como todos los datos, tienen un ciclo de vida complejo y normalmente se mueven de un sitio a otro conforme realizan su función empresarial. Es necesario asegurar los datos durante todo el ciclo de uso, pero se pueden aplicar muchas tecnologías y procesos en las distintas fases del ciclo de vida de los datos.

![](images/Cc162822.4e80aa2b-2eba-421f-aeb8-d6021778e75d(es-es,TechNet.10).gif)

**Figura 1.1. Ejemplo de ciclo de vida de los datos**

Esta guía se centra en el nivel de seguridad que se puede alcanzar mediante el uso de tecnologías de Microsoft para proteger los datos cuando se copian o crean en equipos móviles, como equipos portátiles.

Esta guía no incluye descripciones de la protección de datos para los siguientes escenarios, excepto si los datos se almacenan en caché de forma local:

-   Cuando los datos transitan por redes internas o externas.

-   Cuando los datos se presentan en aplicaciones web (cliente ligero).

-   Cuando los datos se usan en aplicaciones tras su descifrado.

##### En esta página

[](#efaa)[Riesgos de seguridad de los datos](#efaa)
[](#eeaa)[Conceptos criptográficos para la protección de datos](#eeaa)
[](#edaa)[Información sobre los riesgos para los datos](#edaa)
[](#ecaa)[Enfoques de la protección de datos](#ecaa)
[](#ebaa)[Más información](#ebaa)

### Riesgos de seguridad de los datos

Las dos tecnologías descritas en esta guía, el Sistema de archivos de cifrado (EFS) y Microsoft® BitLocker™ Drive Encryption (BitLocker), son ejemplos de dos enfoques del cifrado de datos que son al mismo tiempo diferentes y complementarios. EFS es un mecanismo de cifrado que protege los datos residentes en archivos y carpetas por usuario. BitLocker es un mecanismo de cifrado del volumen completo que cifra todos los sectores del volumen del sistema por equipo, incluidos el sistema operativo, las aplicaciones y los archivos de datos. BitLocker proporciona comprobación y cifrado de la integridad anterior al inicio, pero no ofrece autenticación de usuario. EFS complementa la protección de BitLocker al limitar el acceso a archivos cifrados a los usuarios autenticados correctamente en un equipo en ejecución.

Debido a sus diferencias fundamentales en términos de enfoque e implementación, EFS y BitLocker tienen sus propios puntos fuertes y débiles y ofrecen distintos niveles de seguridad en un conjunto común de escenarios de atacantes. Esta guía describe esos escenarios con detalle y examina cómo se aplican las dos tecnologías de cifrado entre sí.

#### Información sobre los tipos de datos

Existen distintos tipos de datos confidenciales y muchos escenarios diferentes que condicionan las causas y las formas en que se comprometen los datos. Esta guía describe las distintas tecnologías de cifrado en el contexto de los siguientes tipos de datos.

-   **Información de identificación personal (IIP)**. Información privada acerca de los clientes o empleados de una organización, incluidos los números de la seguridad social, números de tarjetas de crédito, información sobre salud, etc. Los datos de este tipo están protegidos por una o más normas gubernamentales o industriales, como la Ley de responsabilidad y portabilidad de seguros médicos (HIPAA), la Directiva de protección de datos de la Unión Europea y la Ley de California SB1386. La pérdida de este tipo de datos suele tener un efecto inmediato y a largo plazo para la organización, aunque nunca se pueda probar que los datos se leyeron desde un equipo.

-   **Propiedad intelectual (IP)**. Datos considerados como confidenciales por una organización, incluidos planes comerciales, investigaciones sobre nuevos productos anteriores a la patente, algoritmos de software, listas de clientes potenciales, etc. Si estos tipos de datos se pierden y son descubiertos por personas no adecuadas, o si se encuentran en un dispositivo que se ha robado deliberadamente, podría implicar una pérdida de ventaja competitiva u otros efectos negativos. Lo más importante que se debe recordar es que hay implicaciones económicas lógicas en el uso de datos de IP, por lo que el costo de la minimización del riesgo se puede equilibrar frente a las implicaciones económicas de no contar con la protección suficiente. Sin embargo, este tipo de cálculo no siempre resulta útil. La vergüenza pública también puede ser un factor de motivación, por lo que sería buena idea cifrar los datos en el equipo del presidente de la organización para evitar una publicidad negativa.

#### Escenarios de atacantes: Usuario no autorizado e intruso

Al describir los ataques y las tecnologías de minimización de riesgos, se suele distinguir entre amenazas procedentes de usuarios internos malintencionados y amenazas con origen en atacantes intrusos. Los usuarios no autorizados malintencionados tienen capacidades que están fuera del alcance de los atacantes intrusos. La lista parcial de diferencias incluye:

-   El usuario no autorizado puede iniciar sesión de forma legítima en el equipo usando su propia cuenta.

-   El usuario no autorizado puede tener acceso al equipo mediante una red durante un largo periodo de tiempo mientras otros usuarios legítimos usan el equipo. Esta oportunidad puede aumentar la probabilidad de encontrar un punto débil que explotar.

-   El usuario no autorizado tiene más probabilidades de realizar ataques de varias fases.

-   Es más probable que el usuario no autorizado pueda obtener con éxito la contraseña de un usuario (o parte de ella) mediante ataques de ingeniería social.

Para comparar los puntos fuertes y débiles de los distintos enfoques del cifrado de datos, es necesario tratar algunos conceptos criptográficos que se aplican al cifrado en general y a EFS y BitLocker en particular.

[](#mainsection)[Principio de la página](#mainsection)

### Conceptos criptográficos para la protección de datos

El cifrado se puede implementar de muchas formas. Por ejemplo, el cifrado se puede realizar en capas o en patrones complicados creados en algoritmos únicos. El uso de claves criptográficas se suele tratar en términos de longitud de clave, pero es mucho más importante cómo se calculan, almacenan y usan esas claves. El almacenamiento y la protección de claves criptográficas no se suele tratar en detalle en la documentación técnica del producto, pero estos problemas son esenciales para entender la parte más vulnerable de una tecnología de cifrado.

![](images/Cc162822.note(es-es,TechNet.10).gif)**Nota:**

Esta sección de la guía no pretender ser un tratado general sobre las tecnologías de datos. Si no dispone de conocimientos básicos sobre los fundamentos del cifrado, como el cifrado simétrico y asimétrico, debe revisar el artículo "[Criptografía para la seguridad de redes e información](http://www.microsoft.com/technet/prodtechnol/windows2000serv/reskit/distrib/dsch_key_rveg.mspx)".

Un algoritmo de cifrado óptimo está diseñado e implementado de manera que la única forma en que un atacante pueda romper el cifrado sea averiguar correctamente la clave concreta usada desde un posible *espacio de claves* grande, que es el intervalo de valores que una clave puede tener. Este tipo de ataque se denomina ataque *por fuerza bruta*.

Los algoritmos de clave simétrica suelen tener un espacio de claves entre 40 y 512 bits, lo que significa que el número de posibles valores para la clave es el máximo valor numérico que se puede expresar mediante el número de bits usados. 40 bits permite un máximo valor numérico de 1.099.511.627.775 (240 -1), que verdaderamente es un número grande, aunque los equipos disponibles actualmente pueden probar fácilmente todos los valores posibles de un espacio de claves de 40 bits como clave de cifrado para intentar descifrar datos. Sin embargo, cada bit agregado al espacio de claves dobla el número de claves posibles, por lo que un espacio de claves de 41 bits ofrecería 2.199.023.255.552 claves posibles. El aumento rápido del espacio de claves provoca que el número de claves posibles aumente hasta un punto en el que no sean factibles los ataques por fuerza bruta usando el hardware actual y las técnicas de ataque conocidas.

No obstante, las tecnologías de cifrado no suelen proporcionar este nivel de seguridad. Muchas implementaciones de cifrado presentan, como mínimo, una de las siguientes vulnerabilidades:

-   **El algoritmo de cifrado tiene errores**. A veces, se encuentra que los algoritmos de cifrado tienen errores tras la revisión por niveles o después de que hayan recibido ataques con éxito. A veces, estos errores se encuentran muchos años después de que el algoritmo se publique y se generalice su uso.

-   **La implementación no es correcta**. Los desarrolladores implementan algoritmos y, a veces, introducen errores de software que reducen la eficacia del algoritmo.

-   **Las claves tienen un nivel bajo de entropía**. Sólo porque un espacio de claves tenga 128 bits, por ejemplo, no significa que el proceso para generar el número de 128 bits sea realmente aleatorio o use todo el espacio de claves.

-   **Las claves se descubren fácilmente**. Las claves se tienen que almacenar en algún lugar. Si la ubicación se puede descubrir y la clave se puede recuperar, los datos cifrados se pueden ver comprometidos.

Si las tecnologías de cifrado están sujetas a estas vulnerabilidades, se puede preguntar por qué uno se preocupa por el cifrado. En la práctica, existen dos factores que ayudan a reducir la aparición de estas vulnerabilidades. Un factor es que Microsoft invierte enormemente en la validación y comprobación de la precisión de sus implementaciones de cifrado. Este proceso comienza eligiendo algoritmos maduros bien entendidos que proporcionan una resistencia innata ante algunos tipos de ataques y continúan con el compromiso constante de Microsoft de certificar sus implementaciones de algoritmos criptográficos como parte del cumplimiento de las normas de [Evaluación de los estándares federales de procesamiento de información (FIPS) 140](http://www.microsoft.com/technet/archive/security/topics/issues/fipseval.mspx) y de enviar sus sistemas operativos para el certificado de Criterio común. Para obtener más información acerca del certificado de Criterio común, consulte la página [Certificado de Criterio común de plataforma de Windows](http://www.microsoft.com/technet/security/prodtech/windowsxp/ccc/default.mspx) de Microsoft TechNet. Además, se ha integrado el proceso del[ciclo de vida de desarrollo de seguridad (SDL) de Trustworthy Computing](http://msdn2.microsoft.com/en-us/library/ms995349.aspx) en los procesos de desarrollo de Microsoft para garantizar que se ha incorporado la seguridad como componente central del desarrollo del producto.

El segundo factor es que el cifrado se puede realizar con suficiente resistencia ante ataques para proporcionar un grado de seguridad adecuado para los datos que se están protegiendo. Es decir, normalmente no importa si un gobierno puede aplicar todos sus recursos y romper con éxito el cifrado que protege la base de datos del cliente. Es posible que sólo necesite una solución de cifrado que evite descubrir los datos fácilmente si éstos quedaran de alguna manera a disposición de personas no autorizadas con recursos o conocimientos muy limitados. Otra forma de evaluar las necesidades de cifrado es asegurarse de que los datos que decide cifrar se evalúan para comprobar su validez y se comparan con los costos estimados para romper el cifrado. Por ejemplo, si la base de datos de un cliente vale 100.000 USD para la competencia y el costo estimado para romper el cifrado es de 1 millón USD, probablemente el nivel de cifrado usado es suficiente.

![](images/Cc162822.note(es-es,TechNet.10).gif)**Nota:**

Para obtener más información acerca de las formas de garantizar que la implementación criptográfica es segura, consulte el capítulo 19 de [Publicación especial 800-12 – Introducción a la seguridad de equipos: el cuaderno NIST](http://csrc.nist.gov/publications/nistpubs/800-12/), publicado por el Instituto Nacional de Estándares y Tecnología (NIST) de Estados Unidos.

Para evaluar los méritos relativos de los enfoques del cifrado, necesita examinar los detalles completos de la implementación del cifrado. La siguiente figura muestra una cadena típica de eventos que se producen cuando los datos se cifran y descifran.

![](images/Cc162822.a42ab380-80b9-41a7-8f54-50ad34a59ee1(es-es,TechNet.10).jpg)

**Figura 1.2. Cifrado y descifrado de datos**

Es importante comprender los siguientes factores a la hora de evaluar una tecnología de cifrado:

-   **Selección del algoritmo**. La seguridad de una implementación criptográfica depende de la calidad de la implementación y de los algoritmos que se implementan. Por este motivo, la mayoría de tecnologías comerciales implementan un conjunto relativamente pequeño de algoritmos maduros, probados correctamente, que se cree que son seguros frente a distintos tipos de ataques. Entre los ejemplos de estos algoritmos se encuentran 3DES (Triple Estándar de cifrado de datos), AES (Estándar de cifrado avanzado) y Blowfish, que son algoritmos simétricos; y RSA (Rivest-Shamir-Adelman) y ECC (Criptografía de curva elíptica), que son algoritmos de clave pública.

-   **Generación de claves**. Las tecnologías de cifrado suelen usar varias claves. Algunas de estas claves se generarán mediante hardware o software, algunas las proporcionan las personas y otras derivan de claves generadas, de claves proporcionadas por personas o de una combinación de ambas. El nivel de seguridad de las claves generadas depende de si se puede predecir el valor de la clave si se conocen los factores ambientales. En otras palabras, una clave debe ser lo suficientemente aleatoria y debe tener la suficiente longitud para ser eficaz.

-   **Derivación de claves**. Muchas implementaciones de cifrado derivan algunas de sus claves a partir de otras claves, como una contraseña proporcionada por usuario. El modo en que se deriva cada una de las claves es fundamental para la seguridad general de la implementación. Lo importante es recordar que no se pueden reforzar las claves a través de la derivación. Se puede crear una clave AES de 256 bits a partir de una clave DES (Estándar de cifrado de datos) de 56 bits, pero la seguridad resultante de la clave no es mayor que la seguridad de una clave DES de 56 bits, que puede derivar de una clave incluso más vulnerable.

-   **Almacenamiento de claves**. Cada tecnología de cifrado debe almacenar y usar material de claves. Es muy importante cómo se almacena el material de claves para la seguridad de la implementación. Los activos valiosos, como las claves de firmas de entidades de certificación raíz, normalmente están protegidos mediante módulos de hardware resistentes a alteraciones que ofrecen una gran resistencia a los ataques. Muchas organizaciones eligen implementar tarjetas inteligentes porque proporcionan una seguridad mayor para el almacenamiento de claves que las soluciones basadas en software, con la ventaja agregada de que el usuario no puede, ni siquiera involuntariamente, recuperar y revelar el material de claves de las tarjetas inteligentes. También se deben tener en cuenta los problemas prácticos del comportamiento de los usuarios como, por ejemplo, si protegen adecuadamente las contraseñas y el material de claves. Las tecnologías de cifrado que facilitan al usuario actuar correctamente son mucho más seguras y eficaces.

-   **Almacenamiento en caché de claves**. Las operaciones criptográficas son mucho más complejas en términos computacionales. Para mejorar el rendimiento, las tecnologías de cifrado suelen apoyarse en optimizaciones que implican el almacenamiento de claves en caché y el uso de productos intermedios de operaciones criptográficas. Estos elementos de datos son extremadamente confidenciales y si la tecnología no los protege correctamente pueden quedar expuestos a un atacante. Por ejemplo, una tecnología que almacena en caché una clave criptográfica en memoria puede permitir al atacante recuperar esta clave desde la memoria del sistema o el archivo de paginación si la memoria caché no está implementada y protegida correctamente.

-   **Eslabón más débil**. La seguridad general de una implementación de cifrado se debe basar en la seguridad del eslabón más débil. Por tanto, el aspecto más importante a la hora de evaluar una implementación de cifrado es conocer el eslabón más débil de una tecnología de cifrado. En muchos entornos, los eslabones más débiles son los usuarios y es fundamental complementar las medidas técnicas para proteger los datos de los equipos portátiles con la educación y formación adecuadas para los usuarios.

-   **Posibilidades de uso frente a seguridad**. En realidad, no hay una solución de cifrado perfecta. Todas las soluciones se pueden atacar por fuerza bruta. El problema es cuánto tiempo hay que invertir en realizar este ataque correctamente. Las implementaciones eficaces suelen tender a ser más o menos equivalentes al nivel de seguridad de la tecnología de cifrado subyacente. Sin embargo, el nivel de seguridad criptográfico no suele ser el factor más importante. También son muy importantes otros factores como la interacción del usuario. Las medidas de seguridad se pueden aumentar casi siempre hasta que resulte difícil para los usuarios obtener acceso a los datos, pero el grado de dificultad se debe analizar con atención para determinar si el costo de la implementación merece la pena a la organización. No se recomienda implementar una solución que sea tan compleja de usar que al final los usuarios decidan usar lápiz y papel.

#### Dificultad de los ataques

No todos los ataques contra una solución de cifrado son iguales. Como se ha mencionado anteriormente, un atacante inteligente normalmente atacará el eslabón más débil. Para estimar el nivel de seguridad de una solución de cifrado puede enumerar los posibles ataques contra las tecnologías de cifrado que implementa y, a continuación, clasificar los ataques por nivel de dificultad.

Un ataque de dificultad baja es uno en el que no se necesitan recursos para leer los datos de interés. Es decir, este tipo de ataque describe una situación en la que un atacante sólo tiene que abrir la tapa del equipo portátil y empezar a leer. La dificultad de un ataque suele estar asociada al contexto y a otros factores de una solución concreta.

[](#mainsection)[Principio de la página](#mainsection)

### Información sobre los riesgos para los datos

El objetivo de una solución de cifrado es cifrar todos los datos importantes para que ningún atacante (casual o determinado, principiante o experto) pueda tener acceso a los datos como texto sin formato. Sin embargo, las soluciones de cifrado se pueden subvertir a través de la aplicación masiva de recursos, encontrando una imperfección desconocida en una tecnología de cifrado específica o simplemente mediante un error de usuario. Las tecnologías de cifrado cuentan con características exclusivas de riesgos basadas en las decisiones de diseño e implementación y en cómo se usan. En las siguientes subsecciones se enumeran algunos riesgos potenciales y se hace referencia a ellos en las descripciones de escenarios más adelante en esta guía. Recuerde que no todos los riesgos enumerado son aplicables a todas las organizaciones. Debe considerar minimizar los riesgos que afectan a su organización tras determinar cuáles de ellos son importantes y justifican una acción adecuada.

#### Equipo en modo de hibernación

La mayoría de equipos portátiles cuentan con una característica denominada hibernación que permite a los usuarios apagar el sistema de forma que no consuma energía, pero que se reinicie exactamente en el mismo estado en que se encontraba antes de entrar en modo de hibernación. Sin embargo, dejar el equipo en modo de hibernación no seguro implica que un atacante puede tener acceso ilimitado a toda la información del equipo. Como en el modo de suspensión, los equipos se pueden configurar para que soliciten las credenciales de usuario al reanudarse desde el modo de hibernación. Puede encontrar detalles sobre cómo habilitar esta configuración en [Proteger el equipo mediante contraseña durante el modo de espera o de hibernación](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/pwrmn_passwordprotect_standby.mspx?mfr=true), que es parte de la documentación en línea de los productos Windows XP Professional.

![](images/Cc162822.important(es-es,TechNet.10).gif)**Importante:**

Microsoft recomienda encarecidamente que solicite el uso de credenciales para desbloquear un equipo en el modo de hibernación.

#### Equipo en modo de suspensión (de espera)

Es posible configurar un equipo portátil para que no solicite al usuario una contraseña o una tarjeta inteligente cuando se reanude desde el modo de suspensión, lo que significa que el equipo se deja activado y disponible para que lo use cualquier persona. Los usuarios que configuren sus equipos para usar el modo de suspensión se encuentran en riesgo máximo si el equipo no requiere inicio de sesión al reanudarse tras un tiempo en modo de suspensión. Puede encontrar detalles sobre cómo habilitar esta configuración en [Proteger el equipo mediante contraseña durante el modo de espera o de hibernación](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/pwrmn_passwordprotect_standby.mspx?mfr=true), que es parte de la documentación en línea de los productos Windows XP Professional.

![](images/Cc162822.important(es-es,TechNet.10).gif)**Importante:**

Microsoft recomienda encarecidamente que solicite el uso de credenciales para desbloquear un equipo tras un tiempo en modo de suspensión.

#### Equipo con sesión iniciada y escritorio desbloqueado

Muy pocas tecnologías de cifrado podrán ser eficaces si el equipo se deja en un lugar público mientras un usuario autorizado ha iniciado sesión. Algunos ataques pueden prosperar incluso en equipos con el escritorio bloqueado. El atacante tan sólo tiene que hacerse con el equipo, llevarlo a un lugar privado y empezar a leer o copiar sus datos. Algunas tecnologías de cifrado disponen de opciones que requieren una clave externa cada vez que se tiene acceso a un archivo, pero el impacto sobre las posibilidades de uso es tan espectacular que pocas organizaciones optan por soluciones tan restrictivas. Una minimización de riesgos más común es el uso de una clave externa o un token, como una tarjeta inteligente, con almacenamiento en caché que permita al equipo retener una copia cifrada de la clave para proporcionar mejores posibilidades de uso.

#### Detección de contraseña local o de dominio

Un atacante que obtenga las credenciales de un usuario podrá obtener acceso a los datos cifrados de dos formas distintas en función de la implementación del cifrado: las credenciales se pueden usar para descifrar el material directamente o para obtener acceso al material de claves mediante ataques contra las credenciales que están almacenadas en caché o en el sistema operativo.

En un sistema de seguridad, el eslabón más débil de la tecnología de cifrado es normalmente la contraseña del usuario porque las contraseñas seleccionadas por usuarios suelen ser mucho menos seguras que incluso las claves menos seguras usadas por los algoritmos de cifrado comunes. El autor de [Evitar productos de cifrado fantasmas: P+F sobre remedios milagrosos](http://www.faqs.org/faqs/cryptography-faq/snake-oil/) afirma que incluso una frase en inglés de 20 caracteres tan sólo tiene 40 bits de aleatoriedad en vez de los 20x8=160 bits de aleatoriedad que se puede esperar. Una contraseña de 8 caracteres tiene mucho menos de 40 bits de aleatoriedad, según declara este autor. Sin embargo, incluso este escenario no es tan preocupante como alguien que escriba su contraseña en un papel y lo pegue en su portátil, que efectivamente puede estropear cualquier solución de cifrado basada en la contraseña de usuario.

![](images/Cc162822.note(es-es,TechNet.10).gif)**Nota:**

Los ataques que descubren la contraseña de usuario mediante ingeniería social u otros métodos de ataque no técnicos no se incluyen en esta guía. Se considera que los ataques de descubrimiento de contraseñas implican principalmente ataques criptográficos por fuerza bruta u otros ataques técnicos contra almacenes de credenciales.

#### Usuario no autorizado puede leer datos cifrados

Este riesgo es diferente que los riesgos tratados anteriormente, ya que se supone que el atacante es un usuario no autorizado malintencionado en vez de un intruso. Este riesgo llama la atención sobre el hecho de que algunas tecnologías de cifrado, concretamente el cifrado por equipo descrito en la sección siguiente, permiten el acceso a datos cifrados por parte de cualquier usuario que inicie sesión correctamente en el equipo. La cuenta de usuario puede ser local para el equipo o una cuenta de usuario de red (por ejemplo, una cuenta en el servicio de directorio Active Directory®) y el inicio de sesión puede ser local o a través de la red.

#### Detección de claves mediante ataque sin conexión

En este tipo de ataque, el atacante crea un disco con datos cifrados en un sistema operativo diferente o modificado. Con un conocimiento detallado de la implementación, el atacante puede intentar aislar las claves usadas para cifrar datos e intentar un ataque por fuerza bruta contra el mecanismo de almacenamiento usado para las claves. En este tipo de ataque se aplica la ley del menor esfuerzo y el atacante intentará aislar y atacar el eslabón más débil del mecanismo de almacenamiento. Los ataques por fuerza bruta contra claves moderadamente seguras son muy difíciles y requieren cantidades extraordinarias de recursos computacionales. Si la solución de cifrado se implementa lo suficientemente bien como para que el ataque por fuerza bruta sea la única opción para el atacante, probablemente se hayan cumplido los objetivos de seguridad de los datos de la organización.

#### Ataques sin conexión contra el sistema operativo

Este tipo de ataques pretende modificar o cambiar los archivos o configuraciones del sistema cuando el sistema operativo se está ejecutando para facilitar el acceso a los datos cifrados. Estos ataques son técnicamente difíciles y requieren un conocimiento profundo del sistema operativo. En el contexto de una tecnología de cifrado del volumen completo, un posible ataque es que un atacante pueda cambiar algunos datos cifrados en el disco esperando que cambie un único valor del Registro o un valor codificado de forma rígida en un sistema operativo ejecutable para que aumente la vulnerabilidad del equipo.

#### Ataques en línea contra el sistema operativo

Este tipo de ataque pretende subvertir la protección del sistema operativo mientras se está ejecutando. Algunos ejemplos incluyen los ataques de extensión de privilegios o intentos de ejecutar código de forma remota. Si un atacante puede completar satisfactoriamente este tipo de ataque, podrá también recuperar los datos cifrados ejecutando un código de su elección en el equipo.

#### Datos de texto sin formato encontrados en el equipo

La existencia de datos confidenciales de texto sin formato es un riesgo básico que cualquier solución de cifrado puede minimizar. Casi todas las soluciones de cifrado minimizan este riesgo a menos que el algoritmo de cifrado que usen se pueda romper con poco o ningún esfuerzo. Las dos tecnologías de cifrado de Microsoft descritas en esta guía usan algoritmos de cifrado aprobados por la industria, por lo que se supone que este riesgo se minimiza en general para cada opción analizada. Sin embargo, en algunas situaciones, es posible que la tecnología de cifrado no se aplique a un archivo específico que contenga datos confidenciales. Muchas de las descripciones de riesgos que aparecen en el resto de esta guía analizan dichas situaciones.

#### Pérdidas de datos de texto sin formato mediante el archivo de hibernación

El concepto de hibernación es parecido al concepto de paginación del sistema, excepto en que el equipo realiza una instantánea de toda la memoria física y escribe los datos en el disco en un *archivo de hibernación*. Si algún dato confidencial se encuentra en la memoria física en el momento de realizar de la instantánea, se escribirá en el disco como parte del archivo de hibernación. Al igual que los ataques al archivo de paginación, los ataques contra el archivo de hibernación se suelen realizar sin conexión.

#### Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema

Los sistemas operativos modernos proporcionan grandes cantidades de memoria virtual para las aplicaciones cambiando los datos en memoria que no se usan a un archivo de paginación almacenado en la unidad de disco duro. Sin embargo, esta funcionalidad crea un riesgo, ya que una aplicación que se ejecuta en el equipo puede cargar datos cifrados desde el disco, descifrarlos en memoria para su uso y, a continuación, escribirlos como datos sin cifrar en la unidad de disco duro en forma de archivo de paginación. Algunos sistemas operativos eliminan el archivo de paginación durante las operaciones de apagado, pero existen formas conocidas de evitar la eliminación del archivo de paginación (incluido el bloqueo provocado del sistema operativo). También puede ser irrelevante recuperar el archivo de paginación y explorar su contenido. Los ataques contra el archivo de paginación casi siempre consisten en quitar la unidad de disco duro del equipo de destino y montarlo en otro equipo o iniciar otro sistema operativo en el equipo de destino. Estos ataques se denominan *ataques sin conexión*.

![](images/Cc162822.note(es-es,TechNet.10).gif)**Nota:**

El material confidencial, como claves criptográficas, puede perderse a través de otros mecanismos de almacenamiento en caché de aplicaciones o de sistemas operativos, incluidos archivos temporales escritos en el disco. Las medidas descritas en Data Encryption Toolkit for Mobile PCs se centran en la minimización del riesgo de pérdida de datos a través del archivo de paginación del sistema, pero también puede minimizar las pérdidas de otros mecanismos de almacenamiento en caché específicos de las aplicaciones.

#### Ataques a plataformas

Algunos ataque se dirigen a características de hardware o software de una plataforma concreta. Por ejemplo, algunos ataques usan la característica de acceso directo a memoria (DMA) ofrecida por la interfaz IEEE 1394 (FireWire) para intentar leer o escribir en la memoria del sistema sin que el sistema operativo lo sepa. Otros ataques incluyen la posibilidad de acceso a memoria basado en DMA realizado por un dispositivo PCI activo y ataques que aprovechan las características o vulnerabilidades de los chips de puente bus PCI o RAM. Los costos de implementación de estos ataques han sido tradicionalmente bastante importantes, pero están disminuyendo conforme aumenta la disponibilidad de las técnicas y los equipos necesarios.

#### Factor de autenticación necesario dejado con el equipo

Este riesgo se aplica a las tecnologías de cifrado que pueden usar un dispositivo externo, como una tarjeta inteligente o un dispositivo USB, para almacenar claves de cifrado. Los usuarios que no son conscientes de los riesgo de seguridad no prestan atención y dejan el dispositivo conectado al equipo o guardado en el mismo lugar de almacenamiento. Como este escenario es común, la mayoría de organizaciones no confiarán en un único factor físico para sus soluciones de cifrado. (Este riesgo afecta también a usuarios que anotan los NIP o frases de acceso en un papel, pero este comportamiento se debe abordar principalmente desde la educación del usuario, algo de lo que no se ocupa esta guía.)

#### Error de usuario

Los usuarios no siempre comprenden todo acerca de la tecnología que usan ni prestan tanta atención a las directivas como a los administradores de TI les gustaría. Este riesgo incluye usuarios que actúan incorrectamente porque no saben cómo activar el cifrado, porque olvidan cifrar un archivo concreto o porque no prestan atención a las directivas de seguridad de los datos.

[](#mainsection)[Principio de la página](#mainsection)

### Enfoques de la protección de datos

El diseño y la implementación de tecnologías de protección de datos implica realizar elecciones que afectan a la seguridad, a las posibilidades de uso y a la administración operativa de la tecnología a la hora de su implementación. Aunque no se trata de algo exhaustivo, la descripción de las tecnologías de la siguiente lista le ayudará a conocer el material presentado en esta guía. Estas tecnologías de protección de datos incluyen:

-   Cifrado basado en software

-   Cifrado basado en hardware

-   Cifrado anterior al inicio (anterior al sistema operativo)

-   Cifrado posterior al inicio (sistema operativo)

-   Cifrado a nivel de aplicación

-   Cifrado a nivel de archivos o carpetas

-   Cifrado del volumen completo

-   Cifrado por usuario

-   Cifrado por equipo

#### Cifrado basado en software

El cifrado basado en software es el estándar para la mayoría de tecnologías y productos de protección de datos. La alternativa, el cifrado basado en hardware, requiere hardware criptográfico especializado que tradicionalmente no ha estado disponible en los equipos personales. Con el cifrado basado en software, las operaciones criptográficas se realizan en la CPU del equipo. Si el equipo está apagado, en modo de hibernación o de suspensión, las claves de cifrado se suelen almacenar cifradas en el disco. Una opción típica es almacenar una clave inicial separada del equipo, por ejemplo, en un dispositivo USB, que se usa para descifrar el material de claves almacenado. Cuando el equipo está en funcionamiento, las claves de cifrado se suelen almacenar en memoria.

Los puntos fuertes del cifrado basado en software incluyen:

-   **La posibilidad de actualizar y revisar la implementación**. Las tecnologías basadas en software se pueden actualizar en cualquier momento para corregir imperfecciones de la implementación, agregar nuevas capacidades o aprovechar nuevos algoritmos.

-   **No hay requisitos especiales de hardware**. Como no es necesario un hardware especial, las tecnologías que dependen del cifrado basado en software se pueden aplicar normalmente a todos los equipos de la organización.

Los puntos débiles y problemas del cifrado basado en software incluyen:

-   **Puntos débiles de software**. En las implementaciones que se apoyan sólo en el software, es posible atacar al software en un intento de subvertir el modo seguro previsto de operación. Un ataque común será cambiar los archivos binarios del sistema operativo de forma que evite el cifrado, manipule las claves de alguna manera o debilite significativamente la operación de cifrado.

-   **Detección de claves**. Si se almacena alguna clave de cifrado en el equipo, un atacante puede descubrir el valor de la clave. Lo importante es saber cómo está protegida la clave. Si la clave se descifra usando únicamente otro material de claves que esté almacenado en el mismo equipo, asuma que un atacante con intenciones y habilidad puede descubrir la clave.

#### Cifrado basado en hardware

Algunos mecanismos de cifrado aprovechan el hardware criptográfico especial para aislar las operaciones criptográficas de la CPU principal con el objeto de proporcionar mayor seguridad para el almacenamiento de claves. Este hardware suele incluir un medio para almacenar de forma segura una o más claves criptográficas. Puede incluir igualmente funciones para realizar operaciones criptográficas en hardware, de forma que la clave nunca queda a disposición de otros componentes de hardware o de software.

Los puntos fuertes del cifrado basado en hardware incluyen:

-   **Las claves de cifrado están protegidas de los puntos débiles del software y del sistema operativo**. El cifrado basado en hardware normalmente asegura que las porciones privadas de los pares de claves se separan de la memoria que está controlada por el sistema operativo.

-   **Las operaciones criptográficas están protegidas de los puntos débiles del software y del sistema operativo.** El cifrado basado en hardware es independiente del sistema operativo host y no está expuesto a vulnerabilidades externas de software.

Los puntos débiles y problemas del cifrado basado en hardware incluyen:

-   **Disponibilidad limitada**. El hardware de cifrado no siempre está disponible. Por ejemplo, el módulo TPM usado por BitLocker no se puede instalar en equipos antiguos y no está disponible de forma generalizada en equipos más recientes.

-   **Difícil de actualizar**. Si se encuentra una imperfección en un sistema basado en hardware, por lo general se debe reemplazar. Sucede lo mismo si el fabricante desea agregar nuevas características o compatibilidad para nuevos algoritmos en el hardware.

#### Cifrado anterior al inicio (anterior al sistema operativo)

El firmware a nivel de BIOS se puede agregar a equipos de forma que todos los datos escritos en un volumen de disco duro se cifren y todos los datos leídos desde el disco se descifren. Esta operación puede ser transparente para el sistema operativo y, por tanto, se puede aplicar a los archivos del sistema operativo.

Si hay disponible un hardware criptográfico, como un TPM, se puede usar para reforzar la seguridad del cifrado y descifrado anterior al inicio. Los equipos que incorporan un TPM también pueden crear una clave que esté cifrada y unida a determinadas medidas de plataformas como el código de Registro de arranque maestro (MBR), el Sector de arranque de NTFS, el Bloque de arranque de NTFS y el Administrador de arranque de NTFS. Este tipo de clave sólo se puede descifrar cuando esas medidas de plataformas tienen los mismos valores que tenían cuando se creó la clave. Este proceso se denomina *sellado* de la clave en el TPM y su descifrado se denomina *quitar el sello*.

El TPM también puede sellar y quitar el sello de los datos generados fuera del TPM. El efecto práctico de esta característica es que la capacidad de descubrir la clave puede depender de si han cambiado algunas características de la plataforma, supuestamente a través de alteraciones malintencionadas que intentan vencer las medidas de seguridad, como el cifrado.

Como el cifrado se aplica a los archivos del sistema operativo, la clave para descifrar estos archivos se debe aplicar antes de la secuencia de inicio del sistema operativo. Es posible que la clave varíe entre las distintas soluciones y pueda derivar de un número de identificación personal (NIP) o de una clave almacenada en un dispositivo de hardware, como un token USB o una tarjeta inteligente.

Los puntos fuertes del cifrado anterior al inicio incluyen:

-   **Los archivos del sistema operativo están protegidos contra los ataques sin conexión**. Todos los archivos de configuración y del sistema están protegidos por la solución de cifrado del volumen completo. Aunque un atacante pueda montar un volumen protegido con un sistema operativo diferente (un *ataque sin conexión*), no podrá hacer nada excepto interrumpir el funcionamiento del sistema operativo.

-   **Protección aumentada para los archivos del sistema operativo**. El hardware criptográfico, como TPM versión 1.2 con actualizaciones de BIOS compatible proporciona la posibilidad de validar la integridad de componentes críticos de inicio anticipado.

Los puntos débiles y problemas del cifrado anterior al inicio incluyen:

-   **La estrategia de recuperación de datos es obligatoria**. Cualquier error de la BIOS, del TPM o del mecanismo de almacenamiento de claves dejará todos los datos del equipo ilegibles. Los errores de hardware suelen ser más difíciles de diagnosticar, clasificar y reparar que los errores de software. Las reparaciones tardan más tiempo si el hardware se debe devolver al fabricante o reparar en una instalación externa. Se debe desarrollar y probar con frecuencia una estrategia eficaz y confiable para la copia de seguridad y recuperación de claves.

-   **Las actualizaciones de software pueden ser más difíciles**. Como los archivos del sistema operativo y otros archivos están cifrados y validados con una firma, la actualización de estos archivos puede necesitar un proceso especial. Este requisito puede dar lugar a una sobrecarga operativa para los equipos que usen una tecnología de cifrado anterior al inicio.

#### Cifrado posterior al inicio (sistema operativo)

El cifrado posterior al inicio se puede realizar por parte del sistema operativo o por una aplicación que se ejecute en el equipo. EFS es un ejemplo de tecnología de cifrado posterior al inicio. Se crea en el sistema operativo Windows y, por tanto, no se puede usar para cifrar el propio sistema operativo. Sin embargo, es un medio eficaz para proteger los datos de los usuarios y las aplicaciones.

Los puntos fuertes del cifrado posterior al inicio incluyen:

-   **Los errores de cifrado no anulan la operabilidad del equipo**. Aunque se produzca un error en la tecnología de cifrado, el equipo seguirá operativo. Por tanto, se pueden recuperar los datos cifrados sin tener que usar un segundo equipo.

Los puntos débiles y problemas del cifrado posterior al inicio incluyen:

-   **No ofrece protección para la configuración ni para los archivos del sistema operativo**. Si se obtiene acceso al disco duro que contiene datos confidenciales mientras éste se monta en un equipo diferente o mientras el equipo móvil se inicia en un sistema operativo diferente, es posible alterar el sistema operativo original de forma que permita subvertir el cifrado.

-   **La estrategia de recuperación de datos es obligatoria**. Si se produce un error en el sistema operativo o en el software de la aplicación, los datos protegidos pueden quedar ilegibles. Se debe desarrollar y probar con frecuencia una estrategia eficaz y confiable para la copia de seguridad y recuperación de claves.

#### Cifrado a nivel de aplicación

El cifrado también se puede implementar a nivel de la aplicación, fuera de los niveles de la BIOS o del sistema operativo. Actualmente muchas aplicaciones ofrecen cierta capacidad para cifrar datos, como WinZip, Microsoft Office e Intuit Quicken.

Los puntos fuertes del cifrado a nivel de aplicación incluyen:

-   **Independencia de la plataforma**. Si la aplicación se ejecuta en sistemas operativos diferentes, los datos cifrados por la aplicación normalmente se pueden mover de una plataforma a otra y se pueden seguir descifrando si se dispone de la clave correcta.

-   **Movimiento de datos durante el cifrado**. Cuando los datos se cifran a nivel del sistema operativo, se suelen descifrar cuando se realizan las operaciones del sistema de archivos, como copiar y mover. Si la carpeta o el sistema de destino se configura para el cifrado, los datos se pueden cifrar con un conjunto completamente diferente de claves. El cifrado a nivel de aplicación normalmente permite al usuario mover los datos en su forma de cifrado original a otra ubicación.

Los puntos débiles y problemas del cifrado a nivel de aplicación incluyen:

-   **Dependencia de la aplicación**. Los datos movidos desde el formato o contenedor de una aplicación a otro formato o contenedor generalmente no pueden mantener el cifrado. Por ejemplo, un usuario puede extraer un archivo desde un archivo WinZip cifrado y el archivo extraído se puede descifrar. Si el usuario no elimina el archivo cuando termine con él, los datos se pueden ver comprometidos.

#### Cifrado a nivel de archivos o carpetas

El cifrado a nivel de archivo y carpeta es una forma de proteger determinados archivos y carpetas y los datos que contienen. Con dicha solución, sólo están protegidos los archivos configurados específicamente para cifrarlos. El resto de datos del equipo están sin cifrar. Un enfoque típico para el cifrado a nivel de archivo o carpeta es crear una clave de cifrado única para cada archivo o carpeta. Este enfoque tiene la ventaja agregada de posibilitar la implementación del cifrado por usuario, como se describe posteriormente en este capítulo.

Los puntos fuertes del cifrado a nivel de archivo o carpeta correctamente implementado incluyen:

-   **Mejor rendimiento que el cifrado del volumen completo**. El rendimiento del equipo no se debe ver afectado drásticamente. Sin embargo, se producirá inevitablemente algún tipo de efecto en el rendimiento del sistema. El cifrado de archivos o carpetas reduce el impacto sobre el rendimiento general del cifrado porque la sobrecarga adicional sólo se aplica a los archivos que se deban cifrar para cumplir la directiva de seguridad de datos de la organización.

-   **Cifrado selectivo**. Los controles exhaustivos de esta solución permitirán a los usuarios cifrar solamente datos confidenciales, al tiempo que los administradores podrán forzar o bloquear el cifrado de carpetas, archivos o tipos de datos específicos.

-   **Compatibilidad con varios usuarios**. Los propietarios de archivos pueden permitir a usuarios adicionales leer o modificar el archivo mientras se mantiene cifrado. Esta capacidad permite compartir de forma segura los archivos cifrados entre los usuarios.

Los puntos débiles del cifrado a nivel de archivo o carpeta incluyen:

-   **Los datos confidenciales se pueden perder a través de archivos generados por el sistema operativo o las aplicaciones**. Normalmente, el sistema operativo escribe datos de aplicación contenidos en memoria en los archivos del disco. Estos datos de aplicación pueden contener datos confidenciales. En el sistema operativo Windows, estos archivos incluyen el archivo de paginación del sistema y el archivo de hibernación. También es posible que el sistema operativo genere archivos de registro y otros archivos inocuos que puedan contener datos confidenciales.

-   **Los datos confidenciales se pueden perder a través del almacenamiento en caché de datos a nivel de aplicación**. Es posible que las aplicaciones implementen sus propios mecanismos de registro o de almacenamiento en caché, como archivos temporales, a través de los cuales los datos confidenciales se pueden perder. Los archivos de recuperación creados por Microsoft Word son un buen ejemplo. Este punto débil se puede minimizar hasta cierto punto configurando la aplicación para que siempre cree archivos temporales en un directorio específico y, a continuación, configurando la solución de cifrado para que cifre todos los archivos de esa carpeta.

-   **Los archivos se pueden copiar por accidente en un archivo o carpeta sin cifrar**. Como sólo se cifran determinados archivos y carpetas, es posible que un usuario pueda copiar por accidente el contenido de un archivo en otro archivo incluido en una carpeta que no esté configurada para el cifrado.

#### Cifrado del volumen completo

El cifrado del volumen completo mejora el cifrado a nivel de archivo o carpeta minimizando los problemas comunes del cifrado a nivel de archivo o carpeta. Si el volumen que se va a proteger contiene archivos del sistema operativo, el cifrado anterior al inicio es un requisito para el enfoque de cifrado del volumen completo. Si una organización elige configurar una solución de cifrado del volumen completo que contenga archivos del sistema operativo, se deben tener en cuenta los puntos débiles y fuertes del cifrado anterior al inicio.

Los siguientes puntos fuertes principales del cifrado del volumen completo son básicamente minimizaciones de los riesgos para los puntos débiles del cifrado a nivel de archivo o carpeta descritos anteriormente.

-   **Se cifran los archivos temporales del sistema operativo**. Como el volumen completo está cifrado, los archivos que se escriben en el volumen se cifran automáticamente, incluidos el archivo de paginación del sistema y el archivo de hibernación.

-   **Se cifran los archivos temporales de aplicaciones**. Los archivos temporales creados por una aplicación se escriben en el volumen cifrado y, por tanto, se cifran automáticamente.

-   **Todos los archivos creados por el usuario se cifran automáticamente**. Si el usuario copia un archivo en una carpeta distinta del volumen, se seguirá cifrando automáticamente. Con el cifrado completo de volúmenes resulta mucho más complicado que el usuario subvierta la solución de cifrado por error.

Los puntos débiles y problemas del cifrado del volumen completo incluyen:

-   **Rendimiento reducido**. Cada bloque de un volumen protegido se debe descifrar cuando se lee y si se vuelve a escribir en el disco, es necesario cifrarlo de nuevo. Esta funcionalidad se aplica a los archivos ejecutables y de configuración del sistema operativo, los archivos ejecutables y de configuración de aplicaciones y a todos los archivos de datos. Aunque el cifrado moderno es relativamente eficaz, se puede esperar una degradación del 5 al 15 por ciento en el rendimiento del sistema con el cifrado del volumen completo.

-   **Protección limitada frente a ataques de usuarios no autorizados**. El cifrado del volumen completo proporciona protección frente a una variedad de ataques sin conexión, pero en general proporciona protección limitada frente a ataques realizados por usuarios no autorizados malintencionados que normalmente tienen (o pueden tener) capacidad para iniciar sesión en un equipo de destino con una cuenta legítima.

#### Cifrado por usuario

El cifrado se puede implementar de forma que varios usuarios tengan la posibilidad de descifrar las claves necesarias para cifrar y descifrar los archivos de datos en el equipo usando su propia clave exclusiva, que puede ser una contraseña o una clave almacenada en un dispositivo USB o similar. Cuando este enfoque se combina con un cifrado a nivel de archivo o carpeta con clave individual, se puede proporcionar acceso a usuarios individuales archivo por archivo.

Los puntos fuertes del cifrado por usuario incluyen:

-   **Control exhaustivo sobre quién puede leer datos cifrados**. Otros usuarios del equipo no pueden leer datos cifrados a menos que el propietario del archivo conceda específicamente esa capacidad. Esta funcionalidad proporciona un nivel de control de acceso así como confidencialidad para los datos.

-   **La posibilidad de cifrar de forma selectiva sólo los datos confidenciales**. Con un sistema de cifrado por usuario implementado correctamente, puede seleccionar exactamente los archivos y carpetas que están protegidos.

-   **La posibilidad de cifrar archivos para varios usuarios**. Un sistema de cifrado por usuario implementado correctamente permite al propietario de un archivo cifrar un único archivo para varios usuarios, permitiendo el uso compartido mientras se mantiene un buen nivel de seguridad. Además, esta funcionalidad se puede usar para implementar la recuperación de datos permitiendo a un agente de recuperación autorizado descifrar los archivos protegidos.

Los puntos débiles y problemas del cifrado por usuario incluyen:

-   **Tan seguro como la clave o credencial menos segura**. Con este enfoque, se debe cifrar cada clave de cifrado o descifrado con varias claves (una para cada usuario exclusivo). Un atacante que busca una clave especialmente vulnerable puede atacar cada clave cifrada por separado, especialmente cuando se usan contraseñas de inicio de sesión local, de inicio de sesión de red o de no inicio de sesión para derivar el material de claves.

#### Cifrado por equipo

Algunas implementaciones de cifrado de datos no ofrecen la posibilidad a distintos usuarios, cada uno con una clave o contraseña diferente, de descifrar la(s) clave(s) maestras necesarias para descifrar los datos residentes en el equipo. En este tipo de implementación, existe una clave que se puede usar para obtener acceso al equipo, incluidos todos los datos cifrados.

Los puntos fuertes del cifrado por equipo incluyen:

-   **Secuencia de derivación de claves más simple**. Si sólo se puede usar una clave para iniciar la secuencia de derivación de claves, todo el mecanismo será sustancialmente menos complicado. Esta complejidad reducida puede, aunque no siempre, implicar una seguridad mayor.

Los puntos débiles y problemas del cifrado por equipo incluyen:

-   **No ofrece protección frente a usuarios no autorizados malintencionados**. Los usuarios a los que la directiva permita iniciar sesión en el equipo protegido pueden tener acceso a cualquier archivo del equipo sin cifrar.

[](#mainsection)[Principio de la página](#mainsection)

### Más información

-   [Criptografía para la seguridad de redes e información](http://www.microsoft.com/technet/prodtechnol/windows2000serv/reskit/distrib/dsch_key_rveg.mspx)

-   [Proteger el equipo con contraseña durante el modo en espera o modo de hibernación](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/pwrmn_passwordprotect_standby.mspx?mfr=true)

-   [Evitar productos de cifrado fantasmas: P+F sobre remedios milagrosos](http://www.faqs.org/faqs/cryptography-faq/snake-oil/)

-   [Publicación especial 800-12 – Introducción a la seguridad de equipos: el cuaderno NIST](http://csrc.nist.gov/publications/nistpubs/800-12/)

-   Normas de [Evaluación de los estándares federales de procesamiento de información (FIPS) 140](http://www.microsoft.com/technet/archive/security/topics/issues/fipseval.mspx)

-   [Certificado de Criterio común de plataforma de Windows](http://www.microsoft.com/technet/security/prodtech/windowsxp/ccc/default.mspx)

-   [Ciclo de vida de desarrollo de seguridad (SDL) de Trustworthy Computing](http://msdn2.microsoft.com/en-us/library/ms995349.aspx)

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
