---
TOCTitle: 'Data Encryption Toolkit for Mobile PCs: Capítulo 3: Sistema de archivos de cifrado'
Title: 'Data Encryption Toolkit for Mobile PCs: Capítulo 3: Sistema de archivos de cifrado'
ms:assetid: 'dc2cde72-a84d-4716-9a30-f62b608efda1'
ms:contentKeyID: 20200222
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162818(v=TechNet.10)'
---

Data Encryption Toolkit for Mobile PCs: análisis de seguridad
=============================================================

### Capítulo 3: Sistema de archivos de cifrado

Publicado: abril 4, 2007

Microsoft® Windows® XP y Windows Vista™ incluyen la capacidad de protección de datos y de recuperación de datos protegidos mediante el Sistema de archivos de cifrado (EFS). EFS es una tecnología de cifrado de datos que se puede aplicar a archivos individuales o a todos los archivos que residen en una carpeta específica. Los archivos de EFS no se pueden descifrar sin el material de claves correspondiente. También es importante tener en cuenta que a diferencia de Microsoft BitLocker™ Drive Encryption (BitLocker), EFS no se puede aplicar a los archivos que son necesarios para iniciar el sistema operativo.

Aunque BitLocker garantiza el cifrado de todos los datos en todo el volumen del sistema, EFS tiene la ventaja de ser más preciso y flexible a la hora de configurar el cifrado para uno o varios usuarios de un equipo. Por ejemplo, EFS se puede usar para cifrar archivos de datos en una red a la que tienen acceso muchos usuarios distintos, un escenario que supera la capacidad de BitLocker.

EFS proporciona un cifrado por usuario al proteger los archivos con una clave a la que sólo el usuario y los agentes de recuperación autorizados tienen acceso. Un atacante que obtenga copias de los archivos no podrá leerlos a menos que también obtenga el material de claves o copie los archivos directamente desde la ubicación original a otra ubicación habiendo iniciado sesión como el usuario que cifró los archivos.

##### En esta página

[](#egaa)[EFS en Windows XP](#egaa)
[](#efaa)[EFS en Windows Vista](#efaa)
[](#eeaa)[Opción de EFS: EFS con almacenamiento de claves de software](#eeaa)
[](#edaa)[Opción de EFS: EFS con tarjetas inteligentes](#edaa)
[](#ecaa)[Resumen de análisis de riesgos de EFS](#ecaa)
[](#ebaa)[Más información](#ebaa)

### EFS en Windows XP

Aunque EFS estaba disponible en Windows 2000, la implementación en Windows XP y Windows Server® 2003 ofrecía importantes características agregadas, como:

-   Capacidades de recuperación mejoradas.

-   Compatibilidad completa para la comprobación de revocación en certificados usados al compartir archivos cifrados.

-   La interfaz de usuario cambia en Windows Explorer para ubicar y comprobar fácilmente los archivos protegidos.

-   Compatibilidad con carpetas sin conexión cifradas en Windows XP.

-   Compatibilidad multiusuario para archivos cifrados.

-   Compatibilidad con proveedores de cifrado mejorado de Microsoft.

-   Cifrado de un extremo a otro mediante EFS sobre WebDAV.

Obtenga más información acerca de estas mejoras de Windows XP en el artículo [Sistema de cifrado de archivos en Windows XP y Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/deploy/cryptfs.mspx).

En todos los escenarios de EFS descritos en este capítulo, un usuario con sesión iniciada puede habilitar el cifrado en archivos y carpetas usando la interfaz **Atributos avanzados** en Windows Explorer.

![](images/Cc162818.c43d3fd1-4a4f-4ad0-8462-5a6eab0bfbb4(es-es,TechNet.10).gif)

**Figura 3.1. Cuadro de diálogo Atributos avanzados de Windows XP**

Cuando un archivo se cifra en una carpeta por primera vez, aparece un mensaje que pregunta al usuario si desea cifrar sólo el archivo seleccionado o toda la carpeta.

Para las organizaciones que necesiten un mayor control sobre el ámbito de la directiva de cifrado de EFS, éste también se puede administrar de forma central mediante objetos de directiva de grupo (GPO) para distribuir automáticamente scripts que usen la utilidad Cipher.exe para configurar el cifrado en la organización.

![](images/Cc162818.note(es-es,TechNet.10).gif)**Nota:**

El software y los modos basados en tarjetas inteligentes de EFS necesitan la existencia del certificado asociado para cada operación. Por ejemplo, EFS basado en tarjeta inteligente necesita la presencia de la tarjeta para cada cifrado o descifrado. Esta funcionalidad evita que los usuarios cifren archivos de forma accidental mediante un certificado para el que no tienen la clave privada asociada, ya que el certificado no se puede usar para el descifrado si la clave privada no se encuentra disponible.

[](#mainsection)[Principio de la página](#mainsection)

### EFS en Windows Vista

EFS está disponible en las ediciones Windows Vista Business, Enterprise y Ultimate y estará disponible en la versión Windows Server “Longhorn”. Windows Vista ofrece mejoras adicionales importantes para EFS, entre las que se incluyen:

-   Uso de claves criptográficas almacenadas directamente en tarjetas inteligentes para el cifrado de EFS.

-   Creación y selección basadas en asistentes de certificados usados para EFS .

-   Migración basada en asistentes de archivos desde una tarjeta inteligente antigua a una nueva.

-   Cifrado del archivo de paginación del sistema cuando EFS está habilitado.

-   Nuevas opciones de directiva de grupo que ayudan a los administradores a definir e implementar directivas organizativas para EFS. Estas opciones incluyen la capacidad de requerir tarjetas inteligentes para EFS, aplicar el cifrado de archivos de paginación, determinar la longitud mínima de claves para EFS y aplicar el cifrado de la carpeta Mis documentos del usuario.

-   Una mayor funcionalidad y capacidad para administrar con exhaustividad las posibilidades de EFS en Windows Vista se muestran en la nueva interfaz de usuario:

![](images/Cc162818.44c4c3c8-7669-4318-8847-1d5a56121c14(es-es,TechNet.10).gif)

**Figura 3.2. Interfaz de administración de EFS de Windows Vista**

El resto de este capítulo trata dos opciones de EFS y describe el nivel de protección que ofrece cada una.

[](#mainsection)[Principio de la página](#mainsection)

### Opción de EFS: EFS con almacenamiento de claves de software

Esta opción de EFS necesita únicamente un equipo con Windows XP o Windows Vista.

La secuencia lógica del proceso de cifrado de EFS en esta opción se muestra en la siguiente figura:

![](images/Cc162818.67dc08b1-9271-4491-b617-43ccb0020ebc(es-es,TechNet.10).gif)

**Figura 3.3. El proceso de cifrado de EFS**

Los pasos de la secuencia de cifrado son los siguientes:

1.  El usuario crea un nuevo archivo en una carpeta cifrada.

2.  Se genera una clave de cifrado de archivos simétrica (FEK) de forma aleatoria.

3.  El sistema operativo comprueba el almacenamiento del certificado del usuario en busca de un certificado que tenga las marcas de uso de las claves apropiadas. Si no hay un certificado adecuado, se genera uno automáticamente.

4.  La interfaz de programación de aplicaciones de protección de datos (DPAPI) se usa para cifrar y almacenar la clave privada asociada al certificado del usuario.

5.  La FEK se cifra mediante la clave pública del certificado y se almacena en los metadatos del archivo.

6.  La FEK se usa para cifrar cada bloque de datos.

7.  Los bloques cifrados se escriben en el disco.

La secuencia lógica del proceso de descifrado de EFS en esta opción se muestra en la siguiente figura:

![](images/Cc162818.8e90f3ca-64ed-456e-be71-29bf3388699b(es-es,TechNet.10).gif)

**Figura 3.4. El proceso de descifrado de EFS**

Los pasos de la secuencia de descifrado son los siguientes:

1.  El inicio de sesión del usuario se valida localmente o mediante un controlador de dominio.

2.  El usuario intenta obtener acceso a un archivo cifrado.

3.  La DPAPI se usa para recuperar la clave privada asociada al certificado X.509 del usuario y descifrarla mediante una clave derivada de la credencial de inicio de sesión del usuario.

4.  La FEK se recupera desde el archivo y se descifra con la clave privada obtenida en el paso anterior.

5.  La FEK se usa para descifrar cada bloque del archivo a medida que sea necesario.

6.  Los datos descifrados se pasan a la aplicación solicitante.

Se puede obtener información adicional acerca del comportamiento de la implementación de EFS en la [Referencia técnica del sistema de archivos de cifrado](http://technet.microsoft.com/es-es/library/cc721923.aspx)

#### Riesgos minimizados: EFS con almacenamiento de claves de software

Esta opción de EFS minimiza los siguientes riesgos para los datos:

-   **Usuario no autorizado puede leer datos cifrados**. Una ventaja específica de EFS en comparación con BitLocker es que las claves de cifrado se guardan en un almacenamiento de clave segura que está protegido con las credenciales del usuario. En esta configuración, la credencial es una contraseña. Por tanto, otros usuarios autorizados del equipo pueden iniciar sesión en el equipo ya sea de forma interactiva o a través de la red, pero no tendrán acceso a archivos confidenciales del equipo que otro usuario haya protegido con EFS, a menos que este usuario les conceda específicamente el acceso a los mismos.

-   **Detección de claves mediante ataque sin conexión**. Suponiendo que el atacante se centre en una clave como FEK o la clave maestra de DPAPI en vez de en la contraseña del usuario, la clave de recuperación de EFS (que es la clave privada de los certificados usados por EFS) o la clave maestra de DPAPI puede estar sometida a un ataque por fuerza bruta. Esta amenaza no debe preocupar demasiado a las organizaciones debido a la dificultad de obtener éxito con este tipo de ataque contra los tipos seguros de claves que EFS usa.

-   **Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema (Windows** **Vista sólo)**. Windows Vista ofrece la posibilidad de cifrar el contenido del archivo de paginación del sistema, que elimina un posible origen de pérdida de datos. Esta característica se implementó concretamente para proteger las claves de EFS de Windows Vista, como la clave de DPAPI maestra (consulte el tema siguiente) mientras el equipo la usa. Esta características también contribuye a controlar el riesgo en esta opción de EFS, donde es posible que se encuentren disponibles los datos de texto sin formato en un archivo de paginación si una aplicación los usa. Las claves de cifrado que se usan para cifrar el archivo de paginación son efímeras y se generan en la Autoridad de seguridad local (LSA). No derivan de la credencial de inicio de sesión del usuario ni del certificado X.509. Después de apagar el equipo (o si se bloquea), ningún método conocido podrá recuperar o leer los datos del archivo de paginación cifrados, excepto el ataque por fuerza bruta.

#### Riesgos residuales y minimizaciones: EFS con almacenamiento de claves de software

Esta opción de EFS no minimiza los siguientes riesgos sin controles y directivas adicionales:

-   **Equipo en modo de hibernación**. Como en las opciones de BitLocker, si un usuario no configura el equipo para solicitar la contraseña al reanudarse desde el modo de suspensión o hibernación, el sistema operativo no puede saber que el usuario actual no es el usuario adecuado. En esta situación, el atacante puede usar el portátil como si fuera el usuario autorizado. Un posible ataque sería copiar los datos interesantes en un dispositivo extraíble o en una ubicación de red. Sin embargo, si el equipo está configurado para solicitar las credenciales de usuario cuando se reanuda desde los modos de suspensión o hibernación, este riesgo queda minimizado.

-   **Equipo en modo de suspensión (en espera)**. Igual que la explicación anterior de minimización de riesgos.

-   **Equipo con sesión iniciada y escritorio desbloqueado**. Después de que el usuario inicie sesión en el equipo, las credenciales se encuentran disponibles para descifrar los certificados usados para EFS. A partir de ese momento, cualquier persona con acceso al teclado podrá tener acceso a los datos descifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la conciencia de seguridad de aquellos usuarios que puedan tener información confidencial en sus equipos.

-   **Detección de contraseña local o de dominio**. En esta configuración, las claves de EFS se descifran en una secuencia que comienza con una clave derivada de la contraseña del usuario. Por tanto, el cifrado de EFS estará comprometido si la contraseña del usuario también lo está. Este riesgo se puede minimizar implementado una directiva de contraseña segura para evitar ataques del tipo ataque de diccionario y educando a los usuarios acerca de la importancia de proteger sus contraseñas.

-   **Ataques sin conexión contra el sistema operativo**. EFS no ofrece protección para el sistema operativo del equipo o los archivos de configuración del sistema operativo en un escenario de ataque sin conexión.

-   **Ataques en línea contra el sistema operativo**. Esta opción no minimiza los ataques en línea contra el sistema operativo. Los atacantes que obtengan código de su elección para ejecutarlo en el sistema operativo pueden robar claves criptográficas.

-   **Pérdidas de datos de texto sin formato a través del archivo de hibernación**. EFS no ofrece protección para el archivo de hibernación del sistema. Este riesgo se puede minimizar actualizando a Windows Vista y usando BitLocker o deshabilitando el modo de hibernación.

    ![](images/Cc162818.important(es-es,TechNet.10).gif)**Importante:**

    La deshabilitación del modo de hibernación reduce las posibilidades de uso de los equipos móviles. Esta minimización puede ser adecuada para los equipos que almacenan activos muy valiosos, pero en general, otras minimizaciones de los riesgos resultan más adecuadas.

-   **Pérdidas de datos de texto sin formato a través del archivo de paginación del sistema (Windows** **XP sólo)**. EFS no se puede usar en Windows XP para cifrar los archivos del sistema, incluido el archivo de paginación del sistema. Esta limitación significa que si se obtiene acceso a los datos confidenciales a través de una aplicación, los datos se pueden escribir en un disco como parte típica de la operación de paginación de memoria. Este riesgo se puede minimizar actualizando a Windows Vista o configurando el equipo para no usar la paginación de memoria.

    ![](images/Cc162818.important(es-es,TechNet.10).gif)**Importante:**

    La deshabilitación de la paginación de memoria suele disminuir el rendimiento del equipo, a veces de forma significativa.

-   **Ataques a plataformas**. Los equipos configurados para usar EFS con el almacenamiento de claves de software mantendrán las claves de EFS en el disco y en la memoria. Los ataques a plataformas que usan el acceso directo a memoria u otras técnicas de manipulación de hardware pueden recuperar el material de claves.

-   **Factor de autenticación necesario dejado con el equipo**. En esta opción, no existe otro factor de autenticación. El único factor de autenticación es la contraseña del equipo del usuario o de la red.

-   **Error de usuario**. El usuario debe abstenerse de guardar archivos que contengan datos confidenciales en una ubicación donde EFS no esté habilitado. En Windows Vista este riesgo se minimiza parcialmente porque existe una opción de configuración de EFS que permite cifrar todos los archivos de la carpeta Mis documentos del usuario. Esta funcionalidad facilita a los usuarios poder garantizar que se cifran los archivos y los directorios adecuados. Este riesgo también se puede minimizar usando la herramienta Asistente del sistema de archivos de cifrado de Microsoft (el Asistente de EFS se proporciona como parte de Aceleradores de soluciones) para ayudar a automatizar el proceso de asegurar los archivos de usuario con EFS.

[](#mainsection)[Principio de la página](#mainsection)

### Opción de EFS: EFS con tarjetas inteligentes

Las distintas versiones de Windows proporcionan capacidades diferentes para mejorar las características de seguridad de EFS. Se ofrece información acerca de las distintas capacidades en las subsecciones siguientes.

#### Windows XP e inicio de sesión con tarjeta inteligente

**Requerir inicio de sesión de tarjeta inteligente** es un parámetro del usuario del dominio configurado a través del servicio de directorio Active Directory® que requiere el uso de una tarjeta inteligente por parte del usuario para iniciar sesión en su cuenta de dominio. El riesgo principal para EFS es que si la contraseña de un usuario se ve comprometida, un atacante puede iniciar sesión en el equipo con esa cuenta y obtener acceso a los datos del equipo, incluidos los datos protegidos con EFS.

La configuración de la directiva de Active Directory que requiere una tarjeta inteligente para iniciar sesión mejora significativamente la seguridad de la cuenta y, por extensión, la seguridad de los datos protegidos con EFS. Esta configuración también ayuda a proteger los datos cifrados frente a ataques sin conexión, ya que fortalece la clave que EFS usa para el cifrado de DPAPI. DPAPI funciona mediante la derivación de una clave a partir de las credenciales del usuario.

El inicio de sesión con tarjeta inteligente se puede requerir de dos formas diferentes: por usuario o por equipo. Se puede habilitar o aplicar en cada modo. Existen algunas diferencias de seguridad entre los modos, incluidas las siguientes:

-   Con el inicio de sesión de tarjeta inteligente por usuario aplicado, la clave inicial es bastante más segura que una contraseña normal. En vez de poder montar un ataque de diccionario contra la contraseña, es probable que un atacante monte un ataque por fuerza bruta contra una clave privada que puede ser lo suficientemente larga como para ser prácticamente irrompible usando las tecnologías actuales.

-   El inicio de sesión de tarjeta inteligente por equipo aplicado proporciona una mejor seguridad en varios sentidos que el inicio de sesión sólo con contraseña, ya que agrega un segundo factor de autenticación. Sin embargo, el inicio de sesión de tarjeta inteligente por equipo usa la tarjeta inteligente sólo para autenticar el inicio de sesión. Los atacantes que obtengan la clave maestra de DPAPI cifrada pueden montar un ataque por fuerza bruta en menos tiempo que el necesario para realizar un ataque por fuerza bruta contra una clave maestra de DPAPI protegida mediante inicio de sesión de tarjeta inteligente por usuario.

Si se habilita, pero no se aplica, cualquier tipo de inicio de sesión de tarjeta inteligente no agregará protección de seguridad eficaz porque permite que el usuario decida si se usa o no el inicio de sesión de tarjeta inteligente.

Para obtener más información acerca de DPAPI y cómo afecta el inicio de sesión de tarjeta inteligente a las claves de DPAPI, consulte el artículo de MSDN [Protección de datos de Windows](http://msdn2.microsoft.com/en-us/library/ms995355.aspx).

![](images/Cc162818.note(es-es,TechNet.10).gif)**Nota:**

Esta descripción de riesgos supone que las tarjetas inteligentes se usan junto con un NIP complejo y que la tarjeta inteligente implementa el bloqueo de NIP para evitar el descubrimiento del NIP.

El cifrado de EFS con la opción de inicio de sesión de tarjeta inteligente en Windows XP se muestra en la siguiente figura.

![](images/Cc162818.9106cca5-90c1-49dc-87f0-ec6605d165c9(es-es,TechNet.10).gif)

**Figura 3.5. Secuencia de cifrado de EFS con inicio de sesión de tarjeta inteligente en Windows XP.**

Los pasos de la secuencia de cifrado son los siguientes:

1.  El usuario crea un nuevo archivo en una carpeta cifrada.

2.  Se genera una FEK simétrica de forma aleatoria.

3.  El sistema operativo comprueba el almacenamiento del certificado del usuario en busca de un certificado que tenga las marcas de uso de las claves apropiadas. Si no hay un certificado adecuado, se genera uno automáticamente.

4.  DPAPI se usa para cifrar y almacenar la clave privada asociada al certificado del usuario. Este cifrado es mucho más seguro que la opción anterior porque la contraseña es mucho más segura que la usada cuando se requiere el inicio de sesión de tarjeta inteligente.

5.  La FEK se cifra mediante la clave pública del certificado y se almacena en los metadatos del archivo.

6.  La FEK se usa para cifrar cada bloque de datos.

7.  Los bloques cifrados se escriben en el disco.

El cifrado de EFS con la opción de inicio de sesión de tarjeta inteligente en Windows XP se muestra en la siguiente figura.

![](images/Cc162818.98911cc3-45af-44be-aa3b-ffa37b9e520d(es-es,TechNet.10).gif)

**Figura 3.5. Secuencia de cifrado de EFS con inicio de sesión de tarjeta inteligente en Windows XP.**

Los pasos de la secuencia de descifrado son los siguientes:

1.  El inicio de sesión de tarjeta inteligente del usuario se valida localmente o mediante un controlador de dominio.

2.  El usuario intenta obtener acceso a un archivo cifrado.

3.  La clave privada correcta se recupera del almacenamiento de DPAPI del usuario y DPAPI la descifra usando una clave derivada de la contraseña segura aleatoria del usuario que se aplica a la cuenta del usuario cuando **Requerir inicio de sesión de tarjeta inteligente** está habilitado en la cuenta.

4.  La FEK se recupera desde el archivo y se descifra con la clave privada obtenida en el paso anterior.

5.  Conforme la aplicación lee cada bloque del archivo, la FEK se usa para descifrar el bloque antes de pasar a la aplicación de solicitante.

#### Windows Vista y EFS con tarjeta inteligente

Windows Vista ofrece nuevas y eficaces características que mejoran la seguridad y la posibilidad de uso de EFS mediante una integración mayor con la tecnología de tarjeta inteligente. En Windows XP, el inicio de sesión con tarjeta inteligente se aprovecha indirectamente debido a la forma en que mejora las características de las claves de DPAPI. Sin embargo, en Windows Vista las tarjetas inteligentes se pueden usar directamente para cifrar archivos con EFS. Las nuevas características no necesitan que el usuario inicie sesión con la tarjeta inteligente, aunque la verdad es que este escenario también funciona. En su lugar, se solicita al usuario que inserte la tarjeta inteligente y proporcione un NIP si EFS se configura para requerir tarjetas inteligentes.

La implementación obvia de EFS y tarjetas inteligentes es cifrar directamente la FEK usando la clave pública y descifrar la FEK usando la clave privada que se corresponde con un certificado de la tarjeta inteligente. Aunque esta opción es muy sencilla y segura, afecta al rendimiento cuando se descifra cada archivo al que se ha obtenido acceso porque cada operación de descifrado de clave privada implica una comunicación con la tarjeta inteligente y la CPU de la tarjeta inteligente es muy lenta comparada con la CPU del equipo host.

Otro problema de la implementación obvia es que la tarjeta inteligente debe estar presente en todo momento, ya que cada intento de descifrar un archivo necesita que la clave privada descifre la FEK correctamente. Como forma de mejorar el rendimiento y también las posibilidades de uso de EFS con la opción de tarjeta inteligente, se puede configurar EFS de forma predeterminada para derivar una clave simétrica a partir de la clave privada de la tarjeta inteligente y usar esta clave para descifrar y cifrar las FEK asociadas a los archivos cifrados. En la configuración predeterminada, el sistema operativo almacenará en caché la clave simétrica derivada de forma que las operaciones de cifrado o descifrado de archivos siguientes no requieran el uso de la tarjeta inteligente y sus claves privadas o públicas asociadas.

La posibilidad de configurar si la clave simétrica se deriva y almacena en caché o no se representa en la **Figura 3.2. Interfaz de administración de EFS en Windows Vista EFS**, como la opción **Crear una clave de usuario con capacidad de almacenamiento en caché desde la tarjeta inteligente**. Si la opción se borra, la clave simétrica ni se deriva ni se almacena en caché y la FEK se cifra y se descifra usando directamente las claves de la tarjeta inteligente. Esta guía usa los términos *modo de clave en caché* y *modo de clave no en caché* para describir estos dos modos operativos diferentes que tienen características de seguridad exclusivas.

##### Modo de clave en caché

En el modo de clave en caché, el sistema operativo almacena en caché la clave simétrica derivada en la memoria de LSA protegida hasta que caduque el tiempo de espera en caché, que se puede configurar. El tiempo de espera en caché predeterminado es de ocho horas de tiempo de inactividad del sistema. Las operaciones que usen la clave derivada restablecerán el periodo de tiempo de inactividad de vaciado. El vaciado de la memoria caché de la clave de EFS también se puede configurar para que se produzca cuando el usuario bloquee el equipo o cuando quite la tarjeta inteligente. El modo de clave en caché mejora el rendimiento significativamente y permite que el administrador configure EFS de forma que los archivos cifrados se puedan cifrar y descifrar sin tener la tarjeta inteligente en el lector todo el tiempo.

![](images/Cc162818.note(es-es,TechNet.10).gif)**Nota:**

Para obtener más información acerca de cómo se implementa el modo en caché en Windows Vista, consulte la [Guía de seguridad de Windows Vista](http://www.microsoft.com/technet/windowsvista/security/guide.mspx).

El cifrado de EFS en el modo de clave en caché se muestra en la siguiente figura:

![](images/Cc162818.5cf0f6c0-5a9c-4c49-80da-5690297f89bc(es-es,TechNet.10).gif)

**Figura 3.7. Secuencia de cifrado de EFS con tarjeta inteligente en Windows Vista: modo de clave en caché**

Los pasos de la secuencia de cifrado son los siguientes:

1.  El usuario crea un nuevo archivo en una carpeta cifrada.

2.  Si una de las siguientes condiciones es verdadera, se solicitará al usuario que inserte la tarjeta inteligente y escriba el NIP:

    -   El usuario no ha iniciado sesión en el equipo con la tarjeta inteligente.

    -   El usuario no ha usado la tarjeta inteligente para obtener acceso a un archivo de EFS recientemente.

    -   El NIP de la tarjeta no se ha almacenado en caché a partir de una operación de EFS reciente o la memoria caché del NIP se ha borrado debido a la inactividad.

3.  Se genera una FEK de forma aleatoria.

4.  Se deriva una clave simétrica a partir de la clave privada de la tarjeta inteligente si una de las condiciones siguientes es verdadera:

    -   Cuando se cifra el primer archivo.

    -   Cuando la clave derivada no se encuentra en la memoria caché.

5.  La FEK se cifra mediante la clave simétrica derivada y se almacena en los metadatos del archivo.

6.  La clave simétrica derivada se almacena en caché en la memoria protegida por LSA.

7.  La FEK se usa para cifrar cada bloque de datos.

8.  Los bloques cifrados se escriben en el disco.

El cifrado de EFS en el modo de clave en caché se muestra en la siguiente figura:

![](images/Cc162818.9239422a-18b2-4d59-a9d4-3d6f7a0ffa8d(es-es,TechNet.10).gif)

**Figura 3.7. Secuencia de cifrado de EFS con tarjeta inteligente en Windows Vista: modo de clave en caché**

Los pasos de la secuencia de descifrado son los siguientes:

1.  El usuario intenta obtener acceso a un archivo cifrado.

2.  Si una de las siguientes condiciones es verdadera, se solicitará al usuario que inserte la tarjeta inteligente y escriba el NIP:

    -   El usuario no ha iniciado sesión en el equipo con la tarjeta inteligente.

    -   El usuario no ha usado la tarjeta inteligente para obtener acceso a un archivo de EFS recientemente.

    -   El NIP de la tarjeta no se ha almacenado en caché a partir de una operación de EFS reciente o la memoria caché del NIP se ha borrado debido a la inactividad.

3.  Se deriva una clave simétrica de la clave privada basada en tarjeta inteligente si no está almacenada en caché aún. Tras el primer uso, la clave derivada se almacena en caché en la memoria protegida por LSA.

4.  La FEK se recupera del archivo y se descifra usando la clave simétrica derivada.

5.  Conforme la aplicación lee cada bloque del archivo, la FEK se usa para descifrar el bloque antes de pasar a la aplicación de solicitante.

##### Modo de clave no en caché

El cifrado de EFS en Windows Vista con EFS funcionando en el modo de no en caché se muestra en la siguiente figura.

![](images/Cc162818.a1c07b9d-de1a-407a-8ce3-6177d8b91e27(es-es,TechNet.10).gif)

**Figura 3.7. Secuencia de cifrado de EFS con tarjeta inteligente en Windows Vista: modo de clave no en caché**

Los pasos de la secuencia de cifrado son los siguientes:

1.  El usuario crea un nuevo archivo en una carpeta cifrada.

2.  Si la tarjeta inteligente del usuario no se encuentra, se le solicitará al usuario que la inserte.

3.  Se genera una FEK simétrica de forma aleatoria.

4.  La FEK se cifra mediante la clave pública del certificado y se almacena en los metadatos del archivo.

5.  Conforme la aplicación escribe cada bloque de datos, se cifra con la FEK.

6.  El bloque cifrado se escribe en el disco.

El cifrado de EFS en el modo de clave no en caché se muestra en la siguiente figura:

![](images/Cc162818.b6906b39-323a-463c-aecc-2252dc8be65e(es-es,TechNet.10).gif)

**Figura 3.7. Secuencia de cifrado de EFS con tarjeta inteligente en Windows Vista: modo de clave no en caché**

Los pasos de la secuencia de descifrado son los siguientes:

1.  El usuario intenta obtener acceso a un archivo cifrado.

2.  Si la tarjeta inteligente del usuario no se encuentra, se le solicitará al usuario que la inserte. Si una de las condiciones siguientes es verdadera, se solicita al usuario que escriba el NIP:

    -   El usuario no ha iniciado sesión en el equipo con la tarjeta inteligente.

    -   El usuario no ha usado la tarjeta inteligente para obtener acceso a un archivo de EFS recientemente.

    -   El NIP de la tarjeta no se ha almacenado en caché a partir de una operación de EFS reciente o la memoria caché del NIP se ha borrado debido a la inactividad.

3.  Los metadatos de EFS para el archivo se recuperan desde el archivo y la FEK cifrada se pasa a la tarjeta inteligente.

4.  La tarjeta inteligente descifra los metadatos para obtener la FEK, que se devuelve a continuación al sistema operativo.

5.  Conforme la aplicación lee cada bloque del archivo, la FEK se usa para descifrar el bloque antes de pasar a la aplicación de solicitante.

#### Riesgos minimizados: EFS con tarjeta inteligente

La opción de EFS con tarjeta inteligente minimiza los siguientes riesgos para los datos:

-   **Equipo en modo de hibernación (sólo modo de clave no en caché de Windows Vista)**. Windows Vista puede requerir la autenticación de la tarjeta inteligente cada vez que se tenga acceso a un archivo protegido por EFS. Este modo de funcionamiento minimiza de forma eficaz este riesgo, aunque no así el modo de tarjeta inteligente de clave en caché predeterminado.

-   **Equipo en modo de suspensión (en espera) (sólo modo de clave no en caché de Windows Vista)**. Igual que la explicación anterior de minimización de riesgos (modo de hibernación).

-   **Equipo con sesión iniciada y escritorio desbloqueado (sólo modo de clave no en caché de Windows Vista)**. Windows Vista puede requerir la autenticación de la tarjeta inteligente cada vez que se tenga acceso a un archivo protegido por EFS. Esta funcionalidad, conocida como modo de clave no en caché, se describe anteriormente en este capítulo y minimiza de forma eficaz este riesgo al requerir la presencia de la tarjeta inteligente para todos los accesos a los archivos de EFS. Aunque este escenario puede implicar posibles problemas graves de posibilidades de uso, se considera una opción válida para las organizaciones que necesiten la solución de cifrado más segura para sus datos confidenciales y cruciales.

-   **Detección de contraseña local o de dominio**. Como se menciona en la sección "Riesgos de seguridad de los datos" en el Capítulo 1, un atacante inteligente siempre explota el eslabón más débil. Desafortunadamente para las personas responsables de asegurar los sistemas de TI, el eslabón más débil suele ser el usuario que elige contraseñas deficientes o que escribe una contraseña muy buena en un papel y la sitúa en el monitor. Después de que la organización implemente la autenticación de dos fases basada en tarjeta inteligente para la seguridad de red, debe poder aumentar la seguridad de EFS mediante el uso de la directiva “Tarjeta inteligente necesaria para el inicio de sesión interactivo”. En Windows Vista, la autenticación de dos fases se puede requerir para el acceso a datos confidenciales incluso en situaciones en que no se puede aplicar el inicio de sesión con tarjeta inteligente habilitando la configuración **Requerir tarjeta inteligente para EFS**.

-   **Usuario no autorizado puede leer datos cifrados**. La opción de EFS con tarjeta inteligente proporciona una minimización eficaz de este riesgo al agregar una factor de autenticación adicional.

-   **Detección de claves mediante ataque sin conexión**. Suponiendo que el atacante se centre en una clave como FEK o la clave maestra de DPAPI en vez de en la contraseña del usuario, la clave de recuperación de EFS (que es la clave privada de los certificados usados por EFS) o la clave maestra de DPAPI puede estar sometida a un ataque por fuerza bruta. Esta amenaza no debe preocupar demasiado a las organizaciones debido a la dificultad de tener éxito con este tipo de ataque contra los tipos seguros de claves que usa EFS.

-   **Pérdidas de datos de texto sin formato a través del archivo de paginación del sistema (Windows** **Vista sólo)**. Windows Vista se puede configurar para cifrar el archivo de paginación del sistema, que minimiza de forma eficaz este riesgo.

-   **Ataques a plataformas (sólo modo de clave no en caché de Windows Vista)**. En el modo de clave en caché, un equipo configurado para usar EFS con almacenamiento de clave de tarjeta inteligente mantendrá las claves de EFS en memoria y un ataque a plataforma puede tener éxito al intentar recuperarlas. El EFS usado con el almacenamiento de claves de tarjeta inteligente no en caché minimiza con eficacia este ataque al requerir un ataque directo contra la tarjeta inteligente para recuperar el material de claves.

-   **Factor de autenticación necesario dejado con el equipo**. En esta opción, el usuario debe proporcionar el NIP, así como el factor de autenticación física, que ofrece una verdadera minimización multifactor de este riesgo.

#### Riesgos residuales y minimizaciones: EFS con tarjeta inteligente

La opción de EFS con tarjeta inteligente no minimiza los siguientes riesgos sin controles y directivas adicionales:

-   **Equipo en modo de hibernación (sólo modo de clave en caché en Windows XP y Windows Vista)**. Si un usuario no configura el equipo para solicitar la contraseña al reanudarse desde el modo de suspensión o hibernación, el sistema operativo no puede saber que el usuario actual no es el usuario adecuado. En esta situación, el atacante puede usar el portátil como si fuera el usuario autorizado. Un posible ataque sería copiar los datos interesantes en un dispositivo extraíble o en una ubicación de red. Sin embargo, si el equipo está configurado para solicitar las credenciales de usuario cuando se reanuda desde los modos de suspensión o hibernación, este riesgo queda minimizado. En la opción de EFS con tarjeta inteligente, este riesgo se puede minimizar como se describe anteriormente cuando se usa Windows Vista.

-   **Equipo en modo de suspensión (en espera) (sólo modo de clave en caché en Windows XP y Windows Vista)**. Igual que la explicación anterior de riesgos residuales (modo de hibernación).

-   **Equipo con sesión iniciada y escritorio desbloqueado (sólo modo de clave en caché en Windows XP y Windows Vista)**. Después de que el usuario inicie sesión en el equipo, las credenciales se encuentran disponibles para descifrar los certificados usados para EFS. A partir de ese momento, cualquier persona con acceso al teclado podrá tener acceso a los datos descifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la conciencia de seguridad de aquellos usuarios que puedan tener información confidencial en sus equipos. En la opción de EFS con tarjeta inteligente, este riesgo se puede minimizar como se describe anteriormente cuando se usa Windows Vista.

-   **Ataques sin conexión contra el sistema operativo**. EFS no ofrece protección para el sistema operativo del equipo o los archivos de configuración del sistema operativo en un escenario de ataque sin conexión.

-   **Ataques en línea contra el sistema operativo (sólo modo de clave en caché en Windows XP y Windows Vista)**. Esta opción *no* minimiza los ataques en línea contra el sistema operativo. Sin embargo, el uso de Windows Vista con tarjetas inteligentes en el modo de clave no en caché minimiza parcialmente este riesgo al imposibilitar al atacante la recuperación de las claves de EFS porque no son accesibles para los programas que se ejecutan en el sistema operativo host.

-   **Pérdidas de datos de texto sin formato mediante el archivo de hibernación**. EFS no ofrece protección para el archivo de hibernación del sistema. Este riesgo se puede minimizar actualizando a Windows Vista y usando BitLocker o deshabilitando el modo de hibernación.

    ![](images/Cc162818.important(es-es,TechNet.10).gif)**Importante:**

    La deshabilitación del modo de hibernación reduce las posibilidades de uso de los equipos móviles. Esta minimización puede ser adecuada para los equipos que almacenan activos muy valiosos, pero en general, otras minimizaciones de los riesgos resultan más adecuadas.

-   **Pérdidas de datos de texto sin formato a través del archivo de paginación del sistema (Windows** **XP sólo)**. EFS no se puede usar en Windows XP para cifrar los archivos del sistema, incluido el archivo de paginación del sistema. Esta restricción significa que si se obtiene acceso a los datos confidenciales a través de una aplicación, los datos se pueden escribir en un disco como parte típica de la operación de paginación de memoria. Este riesgo se puede minimizar actualizando a Windows Vista o configurando el equipo para no usar la paginación de memoria.

    ![](images/Cc162818.important(es-es,TechNet.10).gif)**Importante:**

    La deshabilitación de la paginación de memoria suele disminuir el rendimiento del equipo, a veces de forma significativa.

-   **Ataques a plataformas (sólo modo de clave en caché de Windows XP y Windows Vista)**. En el modo de clave en caché, un equipo mantendrá las claves de EFS en memoria y es posible que un ataque contra la plataforma las recupere correctamente.

-   **Error de usuario**. El usuario debe abstenerse de guardar archivos que contengan datos confidenciales en una ubicación donde EFS no esté habilitado. En Windows Vista este riesgo se minimiza parcialmente porque existe una opción de configuración de EFS que permite cifrar todos los archivos de la carpeta Mis documentos del usuario. Esta funcionalidad facilita a los usuarios poder garantizar que se cifran los archivos y los directorios adecuados. Este riesgo también se puede minimizar usando la herramienta Asistente de EFS (que se proporciona como parte de Aceleradores de soluciones) para ayudar a automatizar el proceso de asegurar los archivos de usuario con EFS.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen de análisis de riesgos de EFS

La siguiente tabla enumera los riesgos para los datos e indica si las distintas opciones de EFS minimizan cada riesgo. En los equipos Windows XP, la configuración de usuario de dominio **Requerir inicio de sesión de tarjeta inteligente** está habilitada. En los equipos Windows Vista, las configuraciones de EFS **Requerir tarjeta inteligente para EFS** y **Habilitar cifrado de archivo de paginación** están habilitadas en los equipos.

Los riesgos que se pueden minimizar con opciones específicas están marcados con la letra **Y**. Los guiones **-** indican riesgos para los que la opción específica proporciona poca o ninguna minimización de riesgos.

**Tabla 3.1. Minimizaciones de riesgos de EFS**

![](images/Cc162818.0d76df62-1c23-49d8-beb0-9bd64db9f966(es-es,TechNet.10).gif)
[](#mainsection)[Principio de la página](#mainsection)

### Más información

-   [Referencia técnica del sistema de archivos de cifrado](http://technet.microsoft.com/es-es/library/cc721923.aspx)

-   [Protección de datos de Windows](http://msdn2.microsoft.com/en-us/library/ms995355.aspx)

-   [Guía de seguridad de Windows Vista](http://www.microsoft.com/technet/windowsvista/security/guide.mspx)

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
