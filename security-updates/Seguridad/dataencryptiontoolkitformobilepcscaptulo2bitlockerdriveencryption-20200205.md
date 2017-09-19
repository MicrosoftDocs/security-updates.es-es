---
TOCTitle: 'Data Encryption Toolkit for Mobile PCs: Capítulo 2: BitLocker Drive Encryption'
Title: 'Data Encryption Toolkit for Mobile PCs: Capítulo 2: BitLocker Drive Encryption'
ms:assetid: '4e6ce820-fcac-495a-9f23-73d65d846638'
ms:contentKeyID: 20200205
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162804(v=TechNet.10)'
---

Data Encryption Toolkit for Mobile PCs: análisis de seguridad
=============================================================

### Capítulo 2: BitLocker Drive Encryption

Publicado: abril 4, 2007

Microsoft® BitLocker™ Drive Encryption es una nueva característica de seguridad integral en las versiones Enterprise y Ultimate del sistema operativo Windows Vista™. Proporciona una protección notable para los datos sin conexión y para el sistema operativo del equipo.

BitLocker es una tecnología de cifrado completo de volúmenes que asegura la no revelación de los datos almacenados en un equipo con Windows Vista si éste sufre alteraciones cuando el sistema operativo instalado se encuentra sin conexión. Está diseñado para sistemas que cuentan con una BIOS y un microchip de Módulo de plataforma segura (TPM). Si estos componentes existen, BitLocker los usa para proporcionar una protección mejorada para los datos y para asegurar la integridad de los componentes de inicio anticipado. Al cifrar todo el volumen, esta funcionalidad ayuda a proteger los datos frente a robos o visualizaciones no autorizadas.

El TPM normalmente se encuentra instalado en la placa base del equipo y usa un bus de hardware para comunicarse con el resto del equipo. Los equipos que incluyen un TPM tienen la posibilidad de crear claves criptográficas y cifrarlas de forma que sólo el TPM las pueda descifrar. Este proceso, a menudo denominado *ajuste* o *enlace* de una clave, puede ayudar a proteger la clave de divulgaciones. Cada TPM tiene una clave de ajuste maestra, denominada clave raíz de almacenamiento (SRK), que se almacena con el propio TPM. La porción privada de un par de claves creada en un TPM nunca se expone a otras personas, componentes, software o procesos.

BitLocker proporciona dos capacidades principales:

-   Proporciona un cifrado por equipo al cifrar el contenido del volumen del sistema operativo. Los atacantes que quiten el volumen no podrán leerlo a menos que obtengan las claves, lo que a su vez requiere atacar la infraestructura de recuperación o el TPM del equipo original.

-   Proporciona un cifrado completo de volúmenes al cifrar todo el contenido de los volúmenes protegidos, incluidos los archivos usados por Windows Vista, el sector de inicio y el espacio de margen asignado en un principio a los archivos en uso. Por tanto, se evita que un atacante recupere información útil al analizar las porciones del disco sin recuperar la clave.

Existen mecanismos de recuperación para usuarios autorizados que se encuentren en situaciones legítimas que requieran recuperación. Por ejemplo, si el TPM no obtiene la validación debido a una actualización necesaria, porque se ha sustituido la placa base que contiene el TPM o porque la unidad de disco duro que contiene el volumen del sistema operativo se ha movido a otro equipo, el sistema entra en modo de recuperación y el usuario debe usar una clave de recuperación que se almacena en un dispositivo USB o en el servicio de directorio Active Directory® para recuperar el acceso al volumen.

El proceso de recuperación es el mismo para todos los escenarios de BitLocker. Si la clave de recuperación está separada físicamente del equipo (y consecuentemente no se ha perdido con el equipo) y el ataque no tiene un origen interno como, por ejemplo, por parte de alguien como un administrador de dominios, los ataques contra la clave de recuperación resultarán muy difíciles.

Después de que BitLocker autentique el acceso a un volumen del sistema operativo protegido, el controlador del filtro del sistema operativo del archivo de BitLocker usará una clave de cifrado del volúmen completo (FVEK) para cifrar y descifrar de forma transparente los sectores de disco conforme los datos se escriban en y se lean desde el volumen protegido. Cuando el equipo hiberna, se guarda un archivo de hibernación cifrado en el volumen protegido. Con la autenticación del acceso pendiente, este archivo guardado se descifra cuando el equipo se reanuda desde el modo de hibernación.

BitLocker admite varias opciones diferentes, dependiendo de la capacidad del hardware del dispositivo y del nivel deseado de seguridad. Estas opciones incluyen:

-   BitLocker con TPM

-   BitLocker con dispositivo de bus serie universal (USB)

-   BitLocker con TPM y número de identificación personal (NIP)

-   BitLocker con TPM y USB

##### En esta página

[](#egaa)[Opción de BitLocker: BitLocker con TPM](#egaa)
[](#efaa)[Opción de BitLocker: BitLocker con dispositivo USB](#efaa)
[](#eeaa)[Opción de BitLocker: BitLocker con TPM y NIP](#eeaa)
[](#edaa)[Opción de BitLocker: BitLocker con TPM y dispositivo USB](#edaa)
[](#ecaa)[Resumen de análisis de riesgos de BitLocker](#ecaa)
[](#ebaa)[Más información](#ebaa)

### Opción de BitLocker: BitLocker con TPM

BitLocker con TPM requiere un equipo con hardware TPM versión 1.2. Esta opción es transparente para el usuario porque el proceso de inicio no se altera de ninguna forma y no es necesario hardware ni contraseñas adicionales.

La experiencia de usuario más transparente para organizaciones que necesitan un nivel de línea de base de protección de datos para cumplir las directivas de seguridad se logra con el modo de autenticación de TPM sólo. Este modo de autenticación es el más sencillo de implementar, administrar y usar. El modo de TPM sólo resulta más adecuado para equipos que estén desatendidos o que se deban reiniciar mientras están desatendidos.

Sin embargo, el modo de TPM sólo ofrece el menor grado de protección de datos. Este modo ofrece protección frente a algunos ataques que modifican los componentes de inicio anticipado, pero el nivel de protección se puede ver afectado por posibles vulnerabilidades en el hardware o en los componentes de inicio anticipado. Los modos de autenticación multifactor de BitLocker pueden minimizar muchos de esos ataques.

Si algunos sectores de su organización cuentan con datos en equipos móviles que se consideren extremadamente confidenciales, considere la recomendación de implementar BitLocker con autenticación multifactor en esos equipos. Solicitar a los usuarios que escriban un NIP o inserten una clave de inicio USB reduce significativamente la posibilidad de ataques contra datos confidenciales.

La figura siguiente muestra el flujo lógico del proceso de descifrado en esta opción.

![](images/Cc162804.d118f78b-f599-4be8-a53e-f1d62b9cad8c(es-es,TechNet.10).gif)

**Figura 2.1. Proceso de descifrado de BitLocker con TPM**

Los pasos de la secuencia son los siguientes:

1.  La BIOS se inicia e inicializa el TPM. Los componentes de confianza/medidos interactúan con el TPM para almacenar medidas de componentes en los Registros de configuración de la plataforma (PCR) del TPM.

2.  Si los valores de PCR coinciden con los valores esperados, el TPM usa la clave raíz de almacenamiento (SRK) para descifrar la clave maestra de volumen (VMK).

3.  La lectura de la FVEK cifrada se realiza desde el volumen y la VMK descifrada se usa para descifrarla.

4.  Los sectores del disco se descifran con la FVEK a medida que se accede a ellos.

5.  Los datos de texto sin formato se proporcionan a aplicaciones y a procesos.

Asegurar la VMK es una forma indirecta de proteger los datos en el volumen de disco. La adición de la VMK permite al sistema regenerar claves de forma sencilla cuando las claves precedentes en la cadena de confianza se pierden o se ven comprometidas, ya que descifrar y volver a cifrar todo el volumen de disco puede resultar costoso.

Como se describe en el proceso anterior, BitLocker evita que el volumen se descifre y que el sistema operativo se cargue si detecta cambios en el Código de Registro de inicio maestro (MBR), el Sector de inicio de NTFS, el Bloque de arranque de NTFS, el Administrador de inicio y otros componentes críticos.

#### Riesgos minimizados: BitLocker con TPM

La opción de BitLocker con TPM minimiza los siguientes riesgos para los datos:

-   **Detección de claves mediante ataque sin conexión**. La VMK se cifra usando la SRK, una clave que se guarda en el hardware del TPM. Entonces, la VMK se usa para cifrar la FVEK. Para descifrar los datos del volumen cifrado, el atacante necesitará realizar un ataque por fuerza bruta para determinar el valor de la FVEK.

    ![](images/Cc162804.note(es-es,TechNet.10).gif)**Nota:**

    De forma predeterminada, BitLocker usa un algoritmo AES-128 (Estándar de cifrado avanzado) más la seguridad de 128 bits del difusor elefante. (Para obtener más información sobre el papel del difusor en el refuerzo de la seguridad de BitLocker, consulte la nota del producto [AES-CBC + Elephant diffuser](http://www.microsoft.com/downloads/details.aspx?familyid=131dae03-39ae-48be-a8d6-8b0034c92555&displaylang=en) para el cifrado de la unidad de BitLocker) También puede configurar BitLocker para usar AES-256 más la versión de 256 bits de Elephant, AES-128 plano o AES-256 plano. Consulte la documentación de Windows Vista para obtener más información acerca de la selección de estos refuerzos de cifrado para BitLocker.

-   **Ataques sin conexión contra el sistema operativo**. Los ataques sin conexión contra el sistema operativo se minimizan porque un atacante debe recuperar correctamente la SRK del TPM y usarla para descifrar la VMK, o realizar un ataque por fuerza bruta en la FVEK. Además, BitLocker configurado con la tecnología de difusor (habilitada de forma predeterminada) minimiza con precisión los ataques localizados de esta naturaleza, ya que las pequeñas modificaciones en el texto cifrado se propagan a través de un área mayor.

-   **Pérdidas de datos de texto sin formato mediante el archivo de hibernación**. El objetivo principal de BitLocker es proteger los datos del volumen del sistema operativo de la unidad de disco duro cuando el equipo se apaga o se encuentra en modo de hibernación. Cuando BitLocker está habilitado, el archivo de hibernación se cifra.

-   **Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema**. Cuando BitLocker está habilitado, el archivo de paginación del sistema se cifra.

-   **Error de usuario**. Como BitLocker es una tecnología de cifrado completo de volúmenes, cifra todos los archivos almacenados en el volumen del sistema operativo Windows Vista. Esta funcionalidad ayuda a evitar errores por parte de los usuarios que toman decisiones incorrectas acerca de la aplicación o no del cifrado.

#### Riesgos residuales y minimizaciones: BitLocker con TPM

BitLocker con la opción de TPM no minimiza los siguientes riesgos sin controles y directivas adicionales:

-   **Equipo en modo de hibernación**. El estado de las claves de cifrado del equipo portátil y de BitLocker no cambia cuando el portátil entra en modo de hibernación. Este riesgo se puede minimizar habilitando la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

-   **Equipo en modo de suspensión (en espera)**. Como en el modo de hibernación, el estado de las claves de cifrado del equipo portátil y de BitLocker no cambia cuando el portátil entra en modo de suspensión. Cuando se reanuda desde el modo de suspensión, la FVEK permanece accesible para el equipo. Este riesgo se puede minimizar habilitando la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

-   **Equipo con sesión iniciada y escritorio desbloqueado**. Después de iniciar el equipo y quitar el sello de la VMK, cualquier persona con acceso al teclado puede obtener acceso a los datos cifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la conciencia de seguridad de aquellos usuarios que puedan tener información confidencial en sus equipos.

-   **Detección de contraseña local o de dominio**. Como el TPM está asociado de forma permanente al equipo del usuario, no se considera una segunda credencial para la autenticación o el acceso a los archivos cifrados. Si la contraseña de un usuario está comprometida, también lo estará la solución de cifrado. Este riesgo se puede minimizar formando a los usuarios para crear buenas contraseñas y no compartirlas con nadie ni escribirlas en un lugar obvio. Las directivas de contraseñas de red seguras pueden evitar de forma eficaz un ataque de diccionario contra una contraseña a manos de un atacante que use herramientas ampliamente disponibles.

-   **Usuario no autorizado puede leer datos cifrados**. BitLocker con TPM tan sólo necesita como credencial una contraseña de cuenta de usuario para tener acceso a todos los datos cifrados del equipo. Por tanto, las cuentas de usuario que puedan iniciar sesión en el equipo también pueden obtener acceso a algunos o a todos los archivos cifrados por BitLocker, como si BitLocker no estuviera habilitado. La forma más eficaz de minimizar este riesgo es requerir un factor de autenticación adicional para usar el equipo (que es posible con otras opciones de BitLocker) o para controlar estrechamente la directiva de cada equipo en función de quién esté autorizado para iniciar sesión. Además, la implementación adecuada de EFS puede minimizar significativamente el riesgo.

-   **Ataques en línea contra el sistema operativo**. Esta opción *no* minimiza los ataques en línea contra el sistema operativo. Si un atacante puede quitar el sello del volumen y realizar un inicio normal, el sistema operativo puede ser susceptible de recibir numerosos ataques, incluidos la extensión de privilegios y los ataques de ejecución de código remoto.

-   **Ataques a plataformas**. Los equipos configurados con BitLocker en modo básico (de TPM sólo) iniciarán y cargarán el sistema operativo hasta la interfaz de credencial de usuario de Microsoft Windows® (el servicio Winlogon) sin solicitar ningún elemento de autenticación de BitLocker adicional. Para cargar el sistema operativo desde el volumen cifrado, el equipo debe obtener acceso con privilegios a las claves de descifrado. Esto se realiza de forma segura porque opera dentro de una Trusted Computing Base (TCB) que valida usando un TPM. Los ataques contra la plataforma, como el acceso directo a la memoria (DMA) a través del bus PCI, puede provocar la divulgación de material de claves.

-   **Factor de autenticación necesario dejado con el equipo**. El TPM proporciona una capa de seguridad adicional, ya que sin ella, un volumen sellado no se puede descifrar. Esta funcionalidad ofrece protección frente a ataques que mueven el volumen cifrado de un equipo a otro. Sin embargo, como el TPM no se puede quitar del equipo, está necesariamente presente y no proporciona la misma seguridad que un factor de autenticación completamente independiente. El TPM no proporciona protección si un atacante descubre autenticadores adicionales, como la contraseña de cuentas del equipo del usuario (para BitLocker con TPM sólo), el token de USB del usuario o el NIP de BitLocker del usuario.

[](#mainsection)[Principio de la página](#mainsection)

### Opción de BitLocker: BitLocker con dispositivo USB

BitLocker admite el cifrado completo de volúmenes en equipos que no tengan el chip de TPM versión 1.2. Aunque la protección adicional que el TPM proporciona no existe con esta opción, muchas organizaciones que requieren una solución de cifrado básica pueden considerar satisfactoria la opción de BitLocker con dispositivo USB si se combina con directivas como contraseñas de cuentas de usuario seguras y la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

Como no existe el TPM en esta opción, no hay ninguna operación para sellar o quitar de sello en la VMK. En vez de esto, la VMK se cifra y descifra mediante los mecanismos de software tradicionales que usan una clave simétrica que se encuentra en el dispositivo USB. Después de insertar el dispositivo USB en el equipo, BitLocker recupera la clave y descifra la VMK. La VMK se usa para descifrar la FVEK, como se muestra en la siguiente figura.

![](images/Cc162804.5cc88486-b6fc-4393-9159-596ad2187ec5(es-es,TechNet.10).gif)

**Figura 2.2. Proceso de descifrado de BitLocker con dispositivo USB**

Los pasos de la secuencia son los siguientes:

1.  El sistema operativo se inicia y solicita al usuario que inserte el dispositivo USB que contiene la clave USB.

2.  La VMK se descifra con la clave del dispositivo USB.

3.  La lectura de la FVEK cifrada se realiza desde el volumen y la VMK descifrada se usa para descifrarla.

4.  Los sectores del disco se descifran con la FVEK a medida que se accede a ellos.

5.  Los datos de texto sin formato se proporcionan a aplicaciones y a procesos.

#### Riesgos minimizados: BitLocker con dispositivo USB

La opción de BitLocker con dispositivo USB minimiza los siguientes riesgos para los datos:

-   **Equipo en modo de hibernación**. Tras la hibernación, BitLocker solicitará la autenticación de nuevo con el dispositivo USB.

-   **Detección de contraseña local o de dominio**. BitLocker con un dispositivo USB requiere un factor de autenticación distinto de una contraseña de cuentas del equipo válida para obtener acceso a los datos cifrados del equipo.

-   **Usuario no autorizado puede leer datos cifrados**. Igual que la explicación anterior de minimización de riesgos.

-   **Detección de claves mediante ataque sin conexión**. La VMK se cifra usando una clave en el dispositivo USB. Si el dispositivo USB no se encuentra disponible, el atacante necesitará realizar un ataque por fuerza bruta para determinar el valor de la FVEK.

-   **Ataques sin conexión contra el sistema operativo**. La VMK se cifra usando una clave en el dispositivo USB. Si el dispositivo USB no se encuentra disponible, el atacante necesitará manipular correctamente miles de sectores que contengan módulos del sistema operativo (equivalente a un ataque por fuerza bruta) para determinar el valor de la FVEK. Además, BitLocker configurado con la tecnología de difusor (habilitada de forma predeterminada) minimiza con precisión los ataques localizados de esta naturaleza, ya que las pequeñas modificaciones en el texto cifrado se propagan a través de un área mayor.

-   **Pérdidas de datos de texto sin formato mediante el archivo de hibernación**. El objetivo principal de BitLocker es proteger los datos del volumen del sistema operativo de la unidad de disco duro cuando el equipo se apaga o se encuentra en modo de hibernación. Cuando BitLocker está habilitado, el archivo de hibernación se cifra.

-   **Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema**. Cuando BitLocker está habilitado, el archivo de paginación del sistema se cifra.

-   **Error de usuario**. Como BitLocker es una tecnología de cifrado completo de volúmenes, cifra todos los archivos almacenados en el volumen del sistema operativo Windows Vista. Esta funcionalidad ayuda a evitar errores por parte de los usuarios que toman decisiones incorrectas acerca de la aplicación o no del cifrado.

#### Riesgos residuales y minimizaciones: BitLocker con dispositivo USB

La opción de BitLocker con dispositivo USB no minimiza los siguientes riesgos sin controles y directivas adicionales

-   **Equipo en modo de suspensión (en espera)**. El estado de las claves de cifrado del equipo portátil y de BitLocker no cambian cuando el portátil entra en modo de suspensión. Cuando se reanuda desde el modo de suspensión, la FVEK permanece accesible para el equipo. Este riesgo se puede minimizar habilitando la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

-   **Equipo con sesión iniciada y escritorio desbloqueado**. Después de iniciar el equipo y quitar el sello de la VMK, cualquier persona con acceso al teclado puede obtener acceso a los datos cifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la conciencia de seguridad de aquellos usuarios que puedan tener información confidencial en sus equipos.

-   **Ataques en línea contra el sistema operativo**. Esta opción *no* minimiza los ataques en línea contra el sistema operativo. Si un atacante puede causar un inicio normal proporcionando el dispositivo USB en el momento del inicio, el sistema operativo puede ser susceptible de recibir numerosos ataques, incluidos la extensión de privilegios y ataques de ejecución de código remoto.

-   **Ataques a plataformas**. Los equipos configurados con BitLocker y un dispositivo USB iniciarán y cargarán el sistema operativo hasta la interfaz de credencial de usuario de Windows (Winlogon) usando la clave contenida en el dispositivo USB. Los ataques contra la plataforma, como DMA a través del bus PCI o por medio de las interfaces IEEE 1394, pueden provocar la divulgación de material de claves.

-   **Factor de autenticación necesario dejado con el equipo**. El dispositivo USB es un factor de autenticación física único y la solución de cifrado depende de él. Es posible que los usuarios descuidados o desinformados guarden el dispositivo USB en el maletín con el PC móvil, lo que deja el dispositivo a disposición de los ladrones. El riesgo de que los usuarios pierdan el equipo y el dispositivo USB a la vez se puede minimizar usando un enfoque de minimización de riesgos que requiera un segundo factor de autenticación no física, como el número de identificación personal (NIP) o una contraseña.

[](#mainsection)[Principio de la página](#mainsection)

### Opción de BitLocker: BitLocker con TPM y NIP

Un equipo con un chip de TPM versión 1.2 y una BIOS que admita BitLocker se puede configurar para requerir dos factores para descifrar datos cifrados con BitLocker. El primer factor es el TPM y el segundo factor es un NIP.

![](images/Cc162804.note(es-es,TechNet.10).gif)**Nota:**

Microsoft recomienda a las organizaciones que se preocupan por la seguridad el uso de BitLocker con TPM y NIP como opción preferida, ya que no hay token externo alguno que perder o atacar.

Agregar un requisito de NIP a un equipo habilitado con BitLocker mejora significativamente la seguridad de la tecnología BitLocker en términos de capacidad de uso y de administración. En esta opción, al usuario se le solicitan dos contraseñas para usar el equipo, una para BitLocker (en el inicio) y otra para el equipo o el dominio en el inicio de sesión. Las dos contraseñas deberán ser diferentes, ya que el NIP está restringido a caracteres numéricos introducidos mediante las teclas de función y la mayoría de directivas de contraseñas de dominio rechazan contraseñas completamente numéricas.

Aunque el NIP proporciona seguridad adicional, es vulnerable a los ataques de cualquier persona paciente y determinada. BitLocker procesa el NIP antes de que se encuentre disponible la compatibilidad del teclado localizado. Por tanto, sólo se pueden usar las teclas de función (F0 - F9). Esta funcionalidad limita la entropía de la clave y posibilita los ataques por fuerza bruta, aunque no es especialmente rápida. Afortunadamente, el mecanismo del NIP del TPM está diseñado para resistir ante ataques de diccionario. Los detalles varían dependiendo del proveedor, pero cada uno agrega un retraso en aumento geométrico antes de permitir la provisión de un nuevo número tras proporcionar un NIP incorrecto. El resultado de este retraso es la ralentización de un posible ataque por fuerza bruta, que hace el ataque inefectivo. Este retraso de entrada se conoce como *protección contra ataques de repetición (hammering)*. Los usuarios pueden ayudar a minimizar los posibles ataques por fuerza bruta contra el NIP seleccionando unos NIP relativamente seguros con siete dígitos y al menos cuatro valores únicos. Se puede encontrar más información acerca de la selección de NIP seguros en el [Blog System Integrity Team](http://blogs.msdn.com/si_team/archive/2006/04/10/572888.aspx) de MSDN.

La versión actual de BitLocker no proporciona compatibilidad directa para la copia de seguridad del NIP. Como el usuario debe recordar dos contraseñas, es incluso más importante crear una clave de recuperación de BitLocker que se puede usar si el usuario olvida su NIP de BitLocker.

La siguiente figura muestra el flujo lógico del proceso de descifrado en BitLocker con la opción de TPM y NIP.

![](images/Cc162804.11056951-8e9f-4482-9ac4-bc7dac6e48a6(es-es,TechNet.10).jpg)

**Figura 2.3. Proceso de descifrado de BitLocker con TPM y NIP**

Los pasos de la secuencia son los siguientes:

1.  La BIOS se inicia e inicializa el TPM. Los componentes de confianza o medidos interactúan con el TPM para almacenar medidas de componentes en los Registros de configuración de la plataforma (PCR) del TPM. Se le solicita un NIP al usuario.

2.  El TPM descifra la VMK usando la SRK si los valores de PCR coinciden con los valores esperados *y* el NIP es correcto.

3.  La lectura de la FVEK cifrada se realiza desde el volumen y la VMK descifrada se usa para descifrarla.

4.  Los sectores del disco se descifran con la FVEK a medida que se accede a ellos.

5.  Los datos de texto sin formato se proporcionan a aplicaciones y a procesos.

Una diferencia interesante entre esta opción y el BitLocker básico con la opción de TPM es que el NIP se combina con la clave de TPM para quitar el sello de la VMK. Después de haber quitado el sello correctamente, BitLocker actúa de la misma forma que en la opción básica.

#### Riesgos minimizados: BitLocker con TPM y NIP

La opción de BitLocker con TPM y NIP minimiza los siguientes riesgos para los datos:

-   **Equipo en modo de hibernación**. BitLocker con TPM y NIP minimiza este riesgo porque se le pide al usuario que proporcione el NIP cuando el portátil se reanuda tras un tiempo de hibernación.

-   **Detección de contraseña local o de dominio**. La ventaja principal de BitLocker con la opción de TPM y NIP es que la solución introduce otro factor o credencial que son necesarios para iniciar el equipo o reanudarlo tras un tiempo de hibernación. Esta ventaja es importante para los usuarios que se encuentren en riesgo de recibir ataques de ingeniería social o que tengan malos hábitos de contraseñas, como usar la contraseña de Windows en equipos que no sean de confianza.

-   **Usuario no autorizado puede leer datos cifrados**. Un usuario que tenga una cuenta de dominio autorizada debe iniciar sesión en el equipo, que debe ser iniciado. Un usuario con una cuenta de dominio autorizada que no disponga de un factor de autenticación adicional no podrá iniciar el equipo para iniciar sesión. Un usuario que no conozca el NIP no puede tener acceso a los datos del portátil, ni siquiera un usuario de dominio al que se le permita iniciar sesión en el equipo debido a una directiva de dominio.

-   **Detección de claves mediante ataque sin conexión**. La VMK se cifra mediante una clave dentro del hardware de TPM que se combina con un NIP. Si se desconoce el NIP, el atacante necesitará realizar un ataque por fuerza bruta para determinar el valor de la FVEK.

-   **Ataques sin conexión contra el sistema operativo**. La VMK se cifra mediante una clave dentro del hardware de TPM que se combina con un NIP. Si se desconoce el NIP, el atacante necesitará realizar un ataque sin conexión por fuerza bruta para determinar el valor de la FVEK y usarla para descifrar el volumen y atacar los archivos del sistema operativo.

-   **Pérdidas de datos de texto sin formato mediante el archivo de hibernación**. El objetivo principal de BitLocker es proteger los datos del volumen del sistema operativo del disco duro cuando el equipo se apaga o se encuentra en modo de hibernación. Cuando BitLocker está habilitado, el archivo de hibernación se cifra.

-   **Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema**. Cuando BitLocker está habilitado, el archivo de paginación del sistema se cifra.

-   **Factor de autenticación necesario dejado con el equipo**. El NIP es un segundo factor de autenticación no física que no se puede perder con el equipo a menos que se escriba en algún lugar, como en un papel.

-   **Error de usuario**. Como BitLocker es una tecnología de cifrado completo de volúmenes, cifra todos los archivos almacenados en el volumen del sistema operativo Windows Vista. Esta funcionalidad ayuda a evitar errores por parte de los usuarios que tomen decisiones incorrectas sobre la aplicación o no aplicación del cifrado.

#### Riesgos residuales y minimizaciones: BitLocker con TPM y NIP

La opción de BitLocker con TPM y NIP no minimiza los siguientes riesgos sin controles y directivas adicionales:

-   **Equipo en modo de suspensión (en espera)**. El estado de las claves de cifrado del equipo portátil y de BitLocker no cambian cuando el portátil entra en modo de suspensión. Cuando se reanuda desde el modo de suspensión, la FVEK permanece accesible para el equipo. Este riesgo se puede minimizar habilitando la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

-   **Equipo con sesión iniciada y escritorio desbloqueado**. Después de iniciar el equipo y quitar el sello de la VMK, cualquier persona con acceso al teclado puede obtener acceso a los datos cifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la conciencia de seguridad de aquellos usuarios que puedan tener información confidencial en sus equipos.

-   **Ataques en línea contra el sistema operativo**. Esta opción *no* minimiza los ataques en línea contra el sistema operativo.

-   **Ataques a plataformas**. Un equipo configurado con BitLocker, un TPM y un NIP de usuario iniciará y cargará el sistema operativo hasta la interfaz de credencial de usuario (Winlogon) tras haber proporcionado el NIP de usuario. Hasta que el usuario no proporcione el NIP, los ataques a plataformas no podrán recuperar el material de claves. Después de proporcionar el NIP, estos ataques pueden dar lugar a la divulgación del material de claves.

[](#mainsection)[Principio de la página](#mainsection)

### Opción de BitLocker: BitLocker con TPM y dispositivo USB

En la opción anterior, BitLocker se configuró para usar un NIP como segundo factor de autenticación con el TPM. También se puede usar un dispositivo USB como alternativa al NIP. En esta opción, se solicita al usuario que inserte el dispositivo USB en el momento del inicio o cuando se active tras un tiempo de hibernación.

La siguiente figura muestra el flujo lógico del proceso de descifrado en BitLocker con la opción de TPM y USB.

![](images/Cc162804.da7b15a1-1d74-4a40-86b4-adb3720183c5(es-es,TechNet.10).jpg)

**Figura 2.4. Proceso de descifrado de BitLocker con TPM y dispositivo USB**

Los pasos de la secuencia son los siguientes:

1.  La BIOS se inicia e inicializa el TPM. Los componentes de confianza o medidos interactúan con el TPM para almacenar medidas de componentes en los Registros de configuración de la plataforma (PCR) del TPM.

2.  Se solicita al usuario el dispositivo USB que contiene la clave de BitLocker.

3.  El TPM descifra una clave intermedia usando la SRK si los valores de PCR coinciden con los valores esperados. Esta clave intermedia se combina con la clave del dispositivo USB para producir otra clave intermedia que se usa para descifrar la VMK.

4.  La lectura de la FVEK cifrada se realiza desde el volumen y la VMK descifrada se usa para descifrarla.

5.  Los sectores del disco se descifran con la FVEK a medida que se accede a ellos.

6.  Los datos de texto sin formato se proporcionan a aplicaciones y a procesos.

Esta opción es diferente de BitLocker básico con TPM o de BitLocker con las opciones TPM y NIP, ya que el material de claves almacenado en el dispositivo USB se combina con la clave de TPM para descifrar la VMK. Una vez quitado el sello correctamente, BitLocker actúa igual que en la opción básica.

#### Riesgos minimizados: BitLocker con TPM y dispositivo USB

La opción de BitLocker con TPM y dispositivo USB minimiza los siguientes riesgos para los datos:

-   **Equipo en modo de hibernación**. Tras la hibernación, BitLocker solicitará la autenticación de nuevo con el dispositivo USB.

-   **Detección de contraseña local o de dominio**. Como en la opción anterior, la ventaja principal de BitLocker con la opción de TPM y USB es que la solución introduce otro factor o credencial, que son necesarios para iniciar el equipo o activarlo tras un tiempo de hibernación.

-   **Usuario no autorizado puede leer datos cifrados**. Como esta opción agrega un factor de autenticación, reduce el riesgo de que un usuario no autorizado con una cuenta válida pueda iniciar el equipo, iniciar sesión y leer los datos cifrados.

-   **Detección de claves mediante ataque sin conexión**. Si no existe el dispositivo USB, el atacante necesitará realizar un ataque por fuerza bruta contra la clave contenida en el dispositivo USB para determinar el valor de la FVEK.

-   **Ataques sin conexión contra el sistema operativo**. Si no existe el dispositivo USB, el atacante necesitará realizar un ataque por fuerza bruta contra la clave contenida en el dispositivo USB para atacar con éxito el sistema operativo.

-   **Pérdidas de datos de texto sin formato mediante el archivo de hibernación**. El objetivo principal de BitLocker es proteger los datos del volumen del sistema operativo del disco duro cuando el equipo se apaga o se encuentra en modo de hibernación. Cuando BitLocker está habilitado, el archivo de hibernación se cifra.

-   **Pérdidas de datos de texto sin formato mediante el archivo de paginación del sistema**. En Windows Vista, el archivo de paginación se cifra usando una clave simétrica temporal que se genera en el momento del inicio, pero que nunca se escribe en el disco. Esta clave se descarta después de apagar el sistema, por lo que la recuperación de datos del archivo de paginación necesitará un ataque por fuerza bruta para encontrar la clave simétrica usada para cifrar el archivo de paginación.

-   **Error de usuario**. Como BitLocker es una tecnología de cifrado completo de volúmenes, cifra todos los archivos almacenados en el volumen del sistema operativo Windows Vista. Esta funcionalidad ayuda a evitar errores por parte de los usuarios que toman decisiones incorrectas acerca de la aplicación o no del cifrado.

#### Riesgos residuales y minimizaciones: BitLocker con TPM y dispositivo USB

La opción de BitLocker con TPM y dispositivo USB no minimiza los siguientes riesgos sin controles y directivas adicionales:

-   **Equipo en modo de suspensión (en espera)**. El estado de las claves de cifrado del equipo portátil y de BitLocker no cambian cuando el portátil entra en modo de suspensión. Cuando se reanuda desde el modo de suspensión, la FVEK permanece accesible para el equipo. Este riesgo se puede minimizar habilitando la configuración **Solicitar una contraseña cuando el equipo se active tras un tiempo de suspensión**.

-   **Equipo con sesión iniciada y escritorio desbloqueado**. Después de iniciar el equipo y descifrar la VMK, cualquier persona con acceso al teclado puede obtener acceso a los datos descifrados. El método más eficaz para minimizar este riesgo es un proceso de formación de la concienciación de los usuarios que puedan tener información confidencial en sus equipos.

-   **Ataques en línea contra el sistema operativo**. Un atacante que pueda completar un inicio normal mediante la provisión del dispositivo USB como parte del proceso de inicio, podrá también realizar varios ataques, incluidos la extensión de ataques de privilegios y ataques que se puedan explotar de forma remota.

-   **Ataques a plataformas**. Un equipo configurado con BitLocker, un TPM y un dispositivo USB iniciará y cargará el sistema operativo hasta la interfaz de credencial de usuario de Windows (Winlogon). Los ataques a plataformas pueden dar lugar a la divulgación de material de claves.

-   **Factor de autenticación necesario dejado con el equipo**. El dispositivo USB es un factor de autenticación física único y la solución de cifrado depende de él. El riesgo de que los usuarios pierdan el equipo y el dispositivo USB al mismo tiempo se puede minimizar requiriendo un segundo factor de autenticación no física, como un NIP o una contraseña.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen de análisis de riesgos de BitLocker

La siguiente tabla enumera los riesgos para los datos e indica si las distintas opciones de BitLocker minimizan cada riesgo. Los riesgos que se pueden minimizar con opciones específicas están marcados con la letra **Y**. Los guiones **-** indican riesgos para los que la opción específica proporciona poca o ninguna minimización de riesgos.

**Tabla 2.1. Minimizaciones de riesgos de BitLocker**

![](images/Cc162804.fd057821-a2d0-48df-a0b1-5b07eaa7c90a(es-es,TechNet.10).gif)
[](#mainsection)[Principio de la página](#mainsection)

### Más información

-   [Blog System Integrity Team](http://blogs.msdn.com/si_team/archive/2006/04/10/572888.aspx)

-   Nota del producto [AES-CBC + Elephant diffuser](http://www.microsoft.com/downloads/details.aspx?familyid=131dae03-39ae-48be-a8d6-8b0034c92555&displaylang=en) para el cifrado de la unidad de BitLocker

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
