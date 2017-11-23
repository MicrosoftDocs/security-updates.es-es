---
TOCTitle: Kit de herramientas de cifrado de datos para equipos móviles
Title: Kit de herramientas de cifrado de datos para equipos móviles
ms:assetid: '01754723-3e94-4bec-8284-02e2a4e91593'
ms:contentKeyID: 20200201
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162802(v=TechNet.10)'
---

Kit de herramientas de cifrado de datos para equipos móviles: guía de implementación y planeación
=================================================================================================

### Capítulo 3: operaciones y escenarios de recuperación

Publicado: 29-05-2007

El funcionamiento y el mantenimiento continuos de equipos protegidos con el Cifrado de unidad BitLocker™ de Microsoft® (BitLocker) y/o con el Sistema de cifrado de archivos (EFS), como se describe en esta guía, requieren que planee un número de escenarios, algunos de los cuales son complejos. En este capítulo, se describen escenarios clave que es posible que su organización le exija que aplique, entre los que se incluyen:

-   La recuperación de datos de sistemas protegidos con EFS.

-   La recuperación de datos de sistemas protegidos con BitLocker.

##### En esta página

[](#edae)[Escenarios de Cifrado de unidad BitLocker](#edae)
[](#ecae)[Escenarios de uso del Sistema de cifrado de archivos](#ecae)
[](#ebae)[Más información](#ebae)

### Escenarios de Cifrado de unidad BitLocker

La recuperación de BitLocker depende totalmente de que se tenga acceso a la contraseña de recuperación. Por tanto, todos los escenarios de recuperación comienzan con la suposición de que se dispone de la contraseña de recuperación. La necesidad de recuperar datos de BitLocker podría derivar de alguna de las siguientes situaciones:

-   Instalación de la unidad protegida con BitLocker en un nuevo equipo.

-   Actualización de la placa base a una con un TPM nuevo.

-   Apagado, deshabilitación o eliminación del TPM.

-   Actualización de los componentes críticos que primero se ejecutan al arrancar y que hacen que el TPM genere un error en el proceso de validación.

-   Olvido del NIP después de habilitar el proceso de autenticación del NIP.

-   Pérdida de la unidad flash USB Plug and Play que contiene la clave de inicio después de habilitar la autenticación de la clave de inicio.

-   La reimplementación de escritorios o equipos portátiles en otros departamentos o para otros empleados de la organización. Estas reimplementaciones podrían ocurrir en el caso de usuarios con permisos de seguridad diferentes, que podrían requerir una funcionalidad de recuperación de datos para sus equipos antes de que pasar a utilizarse a un nuevo nivel de seguridad.

-   Asignación de nuevas tareas a los escritorios en uso. Por ejemplo, puede que un administrador de TI necesite volver a instalar el sistema operativo de forma remota sin perder los datos protegidos.

BitLocker cifra el volumen completo del sistema operativo y solo se puede descifrar después de desbloquear la clave del volumen. Si no se puede desbloquear la clave del volumen, el proceso de inicio se interrumpirá antes de que se pueda iniciar el sistema operativo. En esta parte del proceso de inicio, se debe proporcionar la contraseña de recuperación de una unidad flash USB o usar las teclas de función para escribir la contraseña de recuperación. Las teclas F1 a F9 representan los dígitos del 1 al 9, y F10 representa el 0.

![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

La recuperación tiene lugar en la primera fase del proceso de inicio, por lo que las características de accesibilidad de Microsoft Windows® (incluidos los lectores de pantalla y las pantallas de contraste alto) no están disponibles. Si necesita características de accesibilidad, tenga en cuenta formas en las que pueda establecer procedimientos de recuperación alternativos para usuarios que dependen de las características de accesibilidad.

#### Métodos y problemas de recuperación de BitLocker

La recuperación de BitLocker exige tener acceso a la contraseña de recuperación de BitLocker, que es exclusiva del equipo en el que se creó. Puede guardar la clave en papel, en un dispositivo de inicio USB, en el servicio de directorios de Active Directory® o en un archivo de la red. No obstante, el acceso a esta clave garantiza al portador la capacidad de desbloquear un volumen protegido con BitLocker y leer todos los datos que contiene. Por este motivo, es fundamental que la organización establezca procedimientos para controlar el acceso a las contraseñas de recuperación, y asegurarse de que se almacenen de forma segura e independiente de los equipos que protegen.

##### Métodos de desbloqueo

Existen tres formas diferentes de desbloquear un disco cifrado con BitLocker:

-   La consola de recuperación de BitLocker, que se ejecuta antes de que arranque Windows Vista™, está diseñada para ayudar a los usuarios a desbloquear un volumen del sistema operativo cifrado con BitLocker.

-   El Asistente para la recuperación incluido en el panel de control de BitLocker está diseñado para ayudar a los usuarios a desbloquear un volumen de datos cifrado con BitLocker (un volumen de un sistema no operativo, un volumen de un sistema operativo alternativo del mismo equipo o un volumen de un sistema operativo de otro equipo).

-   El Entorno de recuperación de Windows Vista (WinRE) incluye un asistente que puede usar para desbloquear volúmenes de datos o de sistemas operativos protegidos con BitLocker. WinRE está disponible en un DVD de Windows Vista o en una partición de recuperación que proporcionan algunos fabricantes de equipos.

En cualquiera de estos casos, puede usar la contraseña de recuperación de 48 dígitos para desbloquear el acceso a la unidad de disco cifrada. Esta contraseña puede recuperar información cifrada con BitLocker independientemente del método de protección usado (por ejemplo, TPM, TPM con NIP y TPM con clave de inicio). Esta funcionalidad conserva la capacidad de BitLocker de recuperar la información cifrada. Por ejemplo, si se pierde el NIP, los usuarios pueden volver a obtener acceso a la unidad cifrada mediante la escritura de la contraseña de recuperación.

En una recuperación, la consola de recuperación de BitLocker muestra dos datos:

-   **La etiqueta de la unidad de disco.** Esta información viene definida en una cadena de tres partes que está compuesta por el nombre del equipo, el nombre del volumen de la unidad de disco y la fecha de generación de la contraseña (por ejemplo, CATAPULT OS 1/15/2007).

-   **El identificador de la contraseña.** Esta información viene definida por una cadena hexadecimal de 32 dígitos que identifica de forma exclusiva cada contraseña de recuperación de BitLocker (por ejemplo, 4269744C-6F63-6B65-7220-697320537570).

Los usuarios y los profesionales de soporte técnico pueden usar estos identificadores para asegurarse de que proporcionan la contraseña de recuperación correcta. Estos datos son especialmente útiles cuando se recupera la contraseña de Active Directory.

##### Recuperación iniciada por el usuario

Los usuarios pueden recuperar sus propios datos mediante el uso de una contraseña de recuperación. No obstante, deben conocer o tener el acceso a la contraseña en una unidad flash USB o en otro formato accesible. Después de haber obtenido acceso a la contraseña correcta, pueden usar la consola de recuperación previa al arranque o herramientas del WinRE para desbloquear el volumen y reanudar las operaciones.

##### Recuperación asistida por el departamento de soporte técnico

A la hora de planear el proceso de recuperación de BitLocker, el primer paso es consultar los procedimientos recomendados actuales de la organización para recuperar información confidencial. Por ejemplo, ¿de qué forma administra la organización las contraseñas de Windows? ¿Qué procedimientos aplica la organización para administrar las solicitudes de restablecimiento del NIP de tarjetas inteligentes? Use estos procedimientos recomendados y los recursos relacionados (personal y herramientas) para ayudar a crear un modelo de recuperación de BitLocker.

###### Preparación de la recuperación

Antes de completar la implementación de BitLocker, debe tomar en consideración las solicitudes de recuperación para asegurarse de que las atiende de manera oportuna.

Comience por examinar la guía [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=67438), que describe la forma en que puede usar Active Directory para almacenar la información de recuperación de claves. En este documento, se incluyen una serie de herramientas y scripts que pueden ser útiles a la hora de establecer las operaciones de recuperación.

Microsoft ha desarrollado la herramienta BitLocker Recovery Password Viewer (una extensión del complemento MMC Usuarios y equipos de Active Directory) para proporcionar una forma de ver la información de recuperación de BitLocker como propiedad de un objeto de equipo. Esta funcionalidad hace que el personal del departamento de soporte técnico pueda obtener acceso a la información de recuperación más fácilmente. Debe examinar detalladamente las directivas operativas y la delegación de permisos de Active Directory de la organización para asegurarse de que se limita el acceso a la información de recuperación exclusivamente al personal de soporte técnico que necesita acceso.

Para obtener BitLocker Recovery Password Viewer, consulte las instrucciones en el artículo 928202 de Microsoft Knowledge Base, acerca de [cómo usar BitLocker Recovery Password Viewer para la herramienta Usuarios y equipos de Active Directory y ver contraseñas de recuperación de Windows Vista](http://support.microsoft.com/kb/928202). Después de obtener la herramienta, instálela según las instrucciones del artículo de Microsoft Knowledge Base. Deberá usar una cuenta que tenga permiso de administrador de empresa la primera vez que instale la herramienta en un dominio, pero para las instalaciones posteriores, solo necesitará que la cuenta de instalación tenga privilegios de administrador local sobre el equipo en el que instale la herramienta.

![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

Microsoft recomienda que establezca una directiva de identificación de usuarios para averiguar qué equipos de la empresa pertenecen a qué usuarios antes de emitir contraseñas de recuperación.

###### Ejecución de una recuperación

El personal del departamento de soporte técnico puede usar el siguiente procedimiento de recuperación.

**Para completar una recuperación correctamente**

1.  Pídale al usuario del equipo que le facilite el nombre del mismo. Si el usuario no sabe el nombre del equipo, puede derivarlo de la cadena de la etiqueta de la unidad de disco (si no se ha cambiado el nombre del equipo).

2.  Compruebe la identidad del usuario mediante un mecanismo de autenticación adecuado.

3.  Extraiga la contraseña de recuperación de BitLocker del objeto de equipo de Active Directory. Puede hacerlo con el script **Get-BitLockerRecoveryInfo.vbs**, que viene incluido en la guía [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=78953). También puede usar BitLocker Recovery Password Viewer (si está instalado) mediante las siguientes acciones:

    1.  Abra el complemento MMC Usuarios y equipos de Active Directory.

    2.  En el complemento MMC Usuarios y equipos de Active Directory, localice y haga clic en el contenedor en el que está ubicado el equipo. Por ejemplo, haga clic en el contenedor **Equipos**.

    3.  Haga clic con el botón secundario en el objeto de equipo y, a continuación, haga clic en **Propiedades**.

    4.  En el cuadro de diálogo **Propiedades**, haga clic en la ficha de **recuperación de BitLocker** para ver las contraseñas de recuperación de BitLocker asociadas al equipo específico.

4.  Si no está disponible el nombre del equipo, puede recuperar la contraseña escribiendo el identificador de la contraseña cuando ejecute el script **Get-BitLockerRecoveryInfoByID.vbs**, o puede usar BitLocker Recovery Password Viewer:

    1.  En la opción de usuarios y equipos de Active Directory, haga clic con el botón secundario en el contenedor del dominio y, a continuación, haga clic en la opción de **búsqueda de contraseña de recuperación de BitLocker**.

    2.  En el cuadro de diálogo de **búsqueda de contraseña de recuperación de BitLocker**, escriba los ocho primeros caracteres de la contraseña de recuperación en el cuadro de **Id. de contraseña (primeros 8 caracteres)** y, a continuación, haga clic en el botón de **búsqueda**.

5.  Facilite la contraseña de recuperación al usuario. Se solicitará la contraseña cada vez que se vuelva a arrancar el equipo a menos que se proporcione una clave de inicio o un NIP, o que el usuario desconecte BitLocker.

6.  Si el usuario no ha olvidado o perdido el NIP o la clave de inicio, tome las medidas necesarias para examinar el sistema y determinar la causa de la recuperación. Es importante identificar problemas con el TPM, los archivos de arranque y otras cuestiones que requieran la recuperación para asegurarse de que se administren correctamente y de que no afecten a otros sistemas.

Una vez identificada la causa que obligó a la recuperación, Microsoft recomienda el restablecimiento de la protección de BitLocker en la unidad de disco. Elija uno de los siguientes métodos en función de la causa de la recuperación:

-   **Restablecimiento de la contraseña de recuperación:** este método crea una contraseña de recuperación nueva y anula todas las contraseñas anteriores.

-   **Restablecimiento del NIP o de la clave de inicio USB:** este método sustituye un NIP o una clave de inicio USB perdidos. El vínculo **Administrar claves** del panel de control del Cifrado de unidad BitLocker permite restablecer un NIP perdido o duplicar una clave de inicio USB.

-   **Restablecimiento de medidas de validación del TPM:** este método renueva la captura de pantalla que el TPM usa para validar los archivos de arranque. Restablezca las medidas del TPM solo si conoce la razón por la que no se pudo realizar el proceso de validación y si ha determinado que dicho error es benigno (por ejemplo, una actualización de BIOS de un usuario conocido). Si no es así, considere el acoplamiento y la reconstrucción del equipo.

##### Uso de la herramienta de reparación de BitLocker

La herramienta de reparación de BitLocker (disponible en el artículo 928201 de Microsoft Knowledge Base, acerca de [cómo usar la herramienta de reparación de BitLocker para ayudar a recuperar datos de un volumen cifrado de Windows Vista](http://support.microsoft.com/kb/928201)) puede ayudar a obtener acceso a datos cifrados si el disco duro no está gravemente dañado. Esta herramienta puede reconstruir partes críticas de la unidad de disco y rescatar datos recuperables. Se necesita un paquete de contraseñas de recuperación o de claves de recuperación para descifrar los datos. La herramienta está diseñada para el uso en casos en los que no se puede iniciar Windows Vista o la consola de recuperación de BitLocker no se encuentra disponible. Si proporciona la contraseña de recuperación, la herramienta intentará leer la clave de cifrado específica del volumen. Si la clave específica del volumen está dañada o no se puede leer, puede que necesite usar directamente el paquete de claves de recuperación. Básicamente, la herramienta usa el paquete de contraseñas o de claves de recuperación que le proporciona para permitir el montaje del disco e intentar la recuperación de datos del mismo. Tenga en cuenta que la herramienta de recuperación solo es útil cuando los datos del disco aún se pueden leer. Si el error del disco es muy grave, la herramienta de recuperación no podrá leer los datos cifrados para descifrarlo.

Antes de ejecutar la herramienta de reparación de BitLocker, necesitará los siguientes elementos:

-   El volumen cifrado de BitLocker original.

-   Un volumen de disco con espacio suficiente para contener los datos del volumen cifrado. Microsoft recomienda que use un disco duro externo para guardar esta información.

-   Un disco de unidad flash USB u otro dispositivo de almacenamiento extraíble similar con la información de recuperación de BitLocker del volumen dañado.

-   La propia herramienta de reparación de BitLocker.

Las instrucciones completas para la ejecución de la herramienta de reparación de BitLocker están disponibles en el artículo de Microsoft Knowledge Base citado anteriormente en esta sección.

[](#mainsection)[Principio de la página](#mainsection)

### Escenarios de uso del Sistema de cifrado de archivos

La recuperación EFS depende de si se tiene acceso al material de clave usado para proteger la clave de cifrado de archivos (FEK). Este material podría ser el certificado EFS del usuario o un certificado del Agente de recuperación de datos (DRA). Existen tres escenarios principales para la recuperación de datos EFS:

-   Los datos cifrados del usuario que no deberían haberse cifrado. En este escenario, el modelo de recuperación es simple: la desactivación del cifrado de los datos específicos.

-   Un usuario pierde acceso al material de clave.

-   Una organización debe restaurar el acceso a datos cuando el usuario original (o el certificado asociado) no se encuentra disponible para hacerlo.

#### Métodos y problemas de recuperación EFS

Si la clave de descifrado EFS se pierde o se daña, no se podrá obtener acceso a los archivos protegidos con EFS hasta que se recupere la clave de descifrado. En esta sección, se proporciona información acerca de varios escenarios de recuperación EFS que dependen del método de recuperación original que se ha planeado e implementado.

##### Importación de claves EFS

Si un usuario pierde la clave de descifrado privada EFS, el método de recuperación más simple es la importación del certificado digital EFS (y la clave privada) desde una copia de seguridad conocida. En los capítulos anteriores, hay descripciones de algunos métodos para realizar copias de seguridad de claves EFS.

![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

Para una recuperación correcta, la copia de seguridad de la clave EFS del usuario debe incluir la clave de cifrado privada EFS. Además, el usuario debe recordar la contraseña de protección, que se estableció durante la exportación de claves.

**Para volver a importar una clave EFS que se exportó con anterioridad**

1.  Inicie la sesión en Windows con la cuenta del usuario que debe importar la clave EFS.

2.  Deje que el usuario tenga acceso a una copia del certificado digital EFS y a la clave privada. El nombre del archivo exportado debe finalizar en .pfx.

3.  Haga doble clic en el archivo EFS exportado.

4.  En el cuadro de diálogo **Asistente para importación de certificados**, haga clic en el botón **Siguiente**.

5.  Si es necesario, escriba la ubicación y el nombre del certificado digital EFS y, a continuación, haga clic en **Siguiente**.

6.  Escriba la contraseña de protección que se estableció durante la exportación de certificados EFS y, a continuación, haga clic en **Siguiente**.

    ![](images/Cc162802.3e3b1988-af31-480c-aae0-d594a200773b(es-es,TechNet.10).gif)

    **Figura 3.1. Petición de contraseña de certificado en el Asistente para importación de certificados**

7.  Para permitir que el Asistente para importación de certificados importe el certificado EFS al almacén predeterminado correcto, seleccione el botón de radio **Seleccionar automáticamente el almacén de certificados en base al tipo de certificado** y, a continuación, haga clic en **Siguiente**.

    ![](images/cc162802.IC271005(es-es,TechNet.10).gif)

    **Figura 3.2. Petición de ubicación del almacén de certificados en el Asistente para importación de certificados**

8.  En la pantalla final, haga clic en **Finalizar**.

Ahora el usuario debe intentar obtener acceso al archivo previamente protegido con EFS. Si lo consigue, se debe volver a colocar la clave EFS de la copia de seguridad del usuario en el lugar seguro en el que estaba antes. Se deben eliminar todas las copias que se hayan realizado, y se debe vaciar la Papelera de reciclaje.

##### Uso de agentes de recuperación de datos

Otro escenario de recuperación EFS común es el uso de un agente de recuperación de datos (DRA) EFS. Si configura correctamente el DRA antes de cifrar un archivo, se usará automáticamente el DRA con este archivo. También puede agregar DRA a archivos existentes después de su cifrado inicial.

**Para usar un agente de recuperación de datos**

1.  Inicie la sesión en Windows con la cuenta de usuario del DRA. Debe usar un equipo que pueda tener acceso a los archivos que desea recuperar.

    ![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

    Un DRA puede importar el certificado digital del DRA para EFS si aún no está instalado mediante el uso de las instrucciones de la sección anterior.

2.  Obtenga acceso a la ubicación de los archivos o las carpetas que desea recuperar.

3.  Quite el atributo EFS de los archivos o las carpetas mediante el uso del Explorador de Windows o del comando **Cipher.exe /D**.

4.  Cierre la sesión y deje que el usuario afectado vuelva a iniciarla.

5.  El usuario podrá volver a habilitar la protección EFS en los archivos, si lo desea. Windows volverá a generar un certificado EFS, si es necesario.

##### Recuperación de claves archivadas

Si una entidad de certificación (CA) participante ha archivado las claves privadas y el certificado digital EFS del usuario, la utilización de un escenario de recuperación de claves es pertinente. En esta sección, se analiza la recuperación de claves EFS mediante el uso de Servicios de Certificate Server de Windows Server® 2003.

![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

Para que la recuperación de claves esté disponible, la plantilla del certificado EFS que se usó para crear el certificado digital EFS y cifrar archivos y carpetas se debe configurar para que archive claves.

Existen tres pasos básicos para la recuperación de claves:

1.  El Administrador de certificados de los Servicios de Certificate Server recupera el certificado digital EFS del usuario del almacén que contiene las claves.

2.  El Administrador de certificados descifra la clave privada del usuario y, a continuación, la almacena en un archivo PXF.

3.  El usuario importa el archivo PFX, que vuelve a agregar el certificado digital EFS y la clave privada al almacén de certificados del equipo local.

El proceso de recuperación es sencillo pero requiere dos pasos intermedios: la identificación del número de serie del certificado digital EFS del usuario y la recuperación del propio certificado.

###### Identificación del número de serie del certificado digital EFS del usuario

El primer paso para la recuperación de claves es la identificación del número de serie del certificado digital EFS del usuario. Para los Servicios de Certificate Server, este número de serie debe determinar el certificado que se va a recuperar del archivo.

**Para identificar el número de serie del certificado de un usuario**

1.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.

2.  Abra la consola Entidad de certificación y establezca la conexión con un servidor autorizado de Servicios de Certificate Server.

3.  Expanda el nodo de la entidad de certificación y, a continuación, haga clic en el nodo **Certificados emitidos**.

4.  En el menú **Ver**, haga clic en **Agregar o quitar columnas**.

5.  En el cuadro de diálogo **Agregar o quitar columnas**, en la lista **Columnas disponible**s, haga clic en **Clave archivada** y, a continuación, haga clic en **Agregar**.

6.  Use los botones **Subir** o **Bajar** para subir o bajar el campo **Clave archivada** en la lista de la columna para facilitar la búsqueda de la clave y, a continuación, haga clic en **Aceptar**.

7.  El campo **Clave archivada** debe aparecer ahora en la lista de las columnas desplegadas e indicar las claves que se han archivado.

8.  Busque el certificado digital EFS correcto. Asegúrese de que se trata del certificado EFS emitido y archivado más reciente. Escriba el número de serie del certificado (es necesario para la recuperación).

9.  Cierre la consola Entidad de certificación.

###### Recuperación de la clave y el certificado EFS de un usuario

Cuando obtenga el número de serie del certificado de usuario, podrá recuperar el certificado real y el material de clave asociado desde el servidor de los Servicios de Certificate Server. Para ello, debe usar la herramienta de línea de comandos **Certutil** para consultar la CA y recuperar un archivo PKCS \#7 que contenga los certificados KRA y el certificado de usuario con la cadena de confianza del certificado completa. Su contenido es una estructura PKCS \#7 cifrada que contiene la clave privada (cifrada por los certificados KRA).

Para descifrar el archivo de salida PKCS \#7 cifrado, el usuario conectado debe hacer las veces de KRA o tener la clave privada de uno o más KRA del archivo de salida cifrado de destino. Si el usuario que recupera la clave del almacén de certificados no es funciona como KRA, deberá transferir el archivo de salida cifrado a un usuario que tenga una clave privada KRA para continuar con el proceso.

**Para recuperar el certificado y la clave privada de un usuario**

1.  Inicie la sesión en Windows con una cuenta de usuario que tenga permiso para administrar los Servicios de Certificate Server.

2.  Abra una ventana del símbolo del sistema. En el símbolo del sistema, escriba

    **Certutil -getkey** *&lt;número&gt;* *&lt;nombre&gt;*

    en el que *número* es el número de serie del certificado que debe recuperarse, y *nombre* es el nombre del archivo de salida donde desea almacenar el certificado.

    Este comando intenta realizar la recuperación de cualquier CA de la empresa disponible en el bosque. Si se va a seleccionar una CA específica en vez de todas las entidades de certificación de la empresa que haya en el bosque, use la siguiente sintaxis:

    **Certutil -config** *&lt;nombre del equipo*\\*nombre de CA*&gt; **-getkey** *&lt;número&gt;* *&lt;nombre&gt;*

3.  En el símbolo del sistema, escriba el comando siguiente:

    **Certutil -recoverkey** *&lt;nombre de archivo&gt; &lt;nombredearchivo.pfx&gt;* **–p*** &lt;contraseña&gt;*

    en el que *nombre de archivo* es el archivo de salida cifrado creado en el paso anterior, *nombredearchivo.pfx* es el nombre del archivo de salida nuevo para la clave privada EFS del usuario en formato PKCS \#12 y *contraseña* es la contraseña del archivo **nombredearchivo.pfx** resultante.

4.  Escriba y confirme una contraseña segura para el archivo cuando se le solicite.

5.  Proporcione al usuario esta contraseña a través de un mecanismo seguro que sea independiente del propio archivo para garantizar un alto nivel de seguridad en el proceso de recuperación.

6.  Haga llegar el archivo PFX al usuario a través de un mecanismo de entrega seguro.

7.  Proporcione al usuario las instrucciones de la sección “Importación de claves EFS”, incluida anteriormente en este capítulo.

##### Restauración de datos mediante el uso de un agente de recuperación sin conexión

Cuando deba recuperar datos y se usen agentes de recuperación sin conexión, debe restaurar el certificado del agente de recuperación sin conexión antes de ejecutar la recuperación. Este proceso es sencillo y se puede realizar mediante el uso de los pasos individuales descritos detalladamente en esta guía:

1.  Use el complemento MMC Usuarios y equipos de Active Directory para habilitar la cuenta de usuario de Active Directory usada por el agente de recuperación para que se pueda usar con objeto de iniciar la sesión en el equipo de recuperación.

2.  Use la cuenta de usuario del agente de recuperación para iniciar la sesión en el equipo en el que se llevará a cabo la recuperación.

3.  Importe la clave privada y el certificado digital del agente de recuperación.

4.  Recupere las carpetas y los archivos necesarios.

5.  Quite o vuelva a exportar la clave privada y el certificado del agente de recuperación. Si vuelve a exportar el certificado y la clave, quítelos de la red y almacene la versión exportada de forma segura.

6.  Deshabilite la cuenta de usuario de recuperación.

#### Migración a un nuevo equipo

Los usuarios suelen migrar los entornos de trabajo de un equipo a otro. Estas migraciones ocurren por muchas razones, incluidos la sustitución de hardware, las actualizaciones de equipos o los cambios de trabajo. Se deben aplicar medidas especiales cuando se migren datos de usuario de un equipo a otro para garantizar el acceso continuado a los datos protegidos con EFS. Para realizar este proceso básico, debe completar las siguientes tareas:

-   Migrar los certificados EFS y el material de claves asociado del equipo antiguo al nuevo.

-   Crear certificados de agente de recuperación de datos (DRA), si lo desea.

-   Migrar los archivos cifrados y otros datos de usuario al nuevo equipo.

-   Probar los archivos cifrados para comprobar que se pueden abrir.

##### Migración de los certificados EFS

La migración de los certificados EFS es una parte necesaria del traslado de datos de usuario de un equipo a otro. El método que use para conseguirlo depende del sistema operativo de Windows que esté usando.

###### Migración a Windows Vista

Puede usar la versión 3.0 de la Herramienta de migración de estado de usuario de Microsoft (USMT) para migrar automáticamente los certificados EFS de equipos basados en Windows XP a equipos que ejecutan Windows Vista. No obstante, de manera predeterminada, se produce un error en USMT si esta herramienta encuentra un archivo cifrado (a menos que use la opción /efs). Por tanto, debe usar el marcador /efs:copyraw con la herramienta USMT para migrar los archivos cifrados. Cuando ejecute USMT en el equipo de destino, el archivo cifrado y el certificado EFS migrarán automáticamente. También puede usar los métodos manuales descritos en la sección siguiente para trasladar datos EFS de Windows XP a Windows Vista.

###### Migración a Windows XP

Para migrar archivos cifrados a equipos que ejecutan Windows XP, también debe migrar el certificado EFS. A la hora de migrar certificados con USMT, se necesita la intervención del usuario antes y después de la migración.

También puede migrar certificados EFS de cualquiera de las siguientes formas:

-   Use la herramienta Cipher.exe.

-   Use el complemento MMC Certificados.

**Uso de la herramienta Cipher.exe para migrar certificados EFS**

Puede usar la herramienta de línea de comandos Cipher.exe para exportar el certificado EFS del usuario (tal como se describe en la sección “Recuperación ante problemas de EFS” de este capítulo) y, a continuación, importar el archivo PFX resultante en el nuevo equipo.

**Para migrar el certificado de un usuario con Cipher.exe**

1.  Inicie la sesión como usuario que posee el certificado.

2.  Abra el símbolo del sistema y escriba **Cipher /x:***&lt;archivoefs&gt;*** ***&lt;nombredearchivo&gt;*, donde *nombredearchivo* es un nombre de archivo sin extensiones y *archivoefs* es una ruta de acceso a un archivo cifrado. A continuación, presione Entrar.

    Si se facilita *&lt;archivoefs&gt;*, se realizará una copia de seguridad del certificado de usuario actual que se usa para cifrar el archivo. Si no es así, se realizará una copia de seguridad de las claves y el certificado EFS actuales del usuario. Cipher.exe creará un archivo .pfx protegido con contraseña en la ubicación que se especifique. Para obtener información adicional acerca de Cipher.exe, escriba **cipher /?**.

    ![](images/Cc162802.note(es-es,TechNet.10).gif)**Nota:**

    Hay dos problemas de seguridad importantes en este proceso. En primer lugar, el archivo PFX se debe almacenar en una ubicación a la que se pueda tener acceso desde un equipo de destino (por ejemplo, una carpeta compartida o un medio extraíble). En segundo lugar, el archivo no se debe almacenar en el mismo lugar que los archivos protegidos con EFS.

Después de exportar el archivo, el usuario puede importarlo al nuevo equipo mediante el procedimiento **Para importar el certificado al nuevo equipo** que se encuentra más adelante.

**Uso del complemento Certificados para migrar certificados EFS**

**Para exportar el certificado de un usuario con el complemento Certificados**

1.  Pida al usuario que posee el certificado que inicie la sesión en el equipo de origen.

2.  Abra Microsoft Management Console (MMC). Para ello, haga clic en **Inicio**, **Ejecutar**, escriba **mmc** y, a continuación, presione Entrar.

3.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**.

4.  En el cuadro de diálogo **Agregar o quitar complemento**, haga clic en **Agregar**.

5.  En la lista resultante, seleccione **Certificados**, haga clic en **Agregar** y, a continuación, seleccione **Mi cuenta de usuario**.

6.  Haga clic en **Finalizar**, en **Cerrar** y, a continuación, en **Aceptar**.

7.  Vaya a **Certificados: usuario actual\\Personal\\Certificados**.

8.  Haga clic con el botón secundario en el certificado que desea migrar.

9.  Haga clic en **Todas las tareas** y, a continuación, haga clic en **Exportar**.

10. El Asistente para exportación de certificados le ayudará a almacenar el certificado en algún lugar al que se pueda tener acceso desde un equipo de destino (por ejemplo, un disquete o una carpeta compartida). Cuando se le solicite, indique que desea exportar la clave privada y el certificado.

    Después de completar el proceso, aparecerá un mensaje que indica que la exportación se ha realizado correctamente.

**Para importar el certificado al nuevo equipo**

1.  Pida al usuario que posee el certificado que inicie la sesión en el nuevo equipo.

2.  Abra MMC tal como se describió en el procedimiento anterior.

3.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**.

4.  En el cuadro de diálogo **Agregar o quitar complemento**, haga clic en **Agregar**.

5.  Seleccione **Certificados** de la lista, haga clic en **Agregar** y, a continuación, seleccione **Mi cuenta de usuario**.

6.  Haga clic en **Finalizar**, en **Cerrar** y, a continuación, en **Aceptar**.

7.  Vaya a **Certificados: usuario actual\\Personal**.

8.  Haga clic con el botón secundario en **Personal**.

9.  Haga clic en **Todas las tareas** y, a continuación, haga clic en **Importar**.

10. Use el Asistente para importación de certificados con objeto de localizar el certificado que exportó. Cuando busque el certificado, seleccione Intercambio de información personal (\*.pfx; \*.p12) en el cuadro de lista desplegable **Archivos de tipo**. Deberá escribir la contraseña que proporcionó cuando exportó el certificado desde el equipo de destino.

    Después de completar el proceso, aparecerá un mensaje que indica que la importación se ha realizado correctamente.

##### Creación de certificados de DRA

Como parte de la migración, es posible que desee usar las instrucciones del [Capítulo 2: tareas de configuración e implementación](http://www.microsoft.com/spain/technet/security/guidance/clientsecurity/dataencryption/planandimplement/a69e5f04-8f25-43a6-86b9-e8279021d108.mspx) para asegurarse de que el nuevo equipo (junto con los certificados asociados) tiene el conjunto correcto de certificados de DRA asociados a él.

##### Migración de los archivos cifrados al nuevo equipo

Después de exportar el certificado, puede continuar con el traslado de otros datos de usuario, como archivos reales, al nuevo equipo.

Si usa USMT para trasladar datos cifrados de un equipo a otro, debe especificar el marcador **/efs:copyraw** para permitir que USMT lea la secuencia completa de datos cifrados de los archivos de origen. Si no especifica este marcador o si usa otras herramientas (como **xcopy** o **robocopy**) para trasladar los archivos, el equipo de origen los descifrará antes de que se copien.

##### Prueba de los archivos migrados

Una vez trasladados los certificados y los archivos al nuevo equipo, debe comprobar que la migración ha funcionado correctamente mediante la comprobación de dos elementos:

-   Compruebe que la cuenta de usuario que posee los archivos puede abrirlos.

-   Compruebe que los archivos siguen cifrados mediante la comprobación de sus atributos en el Explorador de Windows. Los iconos de los archivos cifrados aparecerán marcados en verde. También puede usar el cuadro de diálogo **Propiedades de archivo** para comprobar que el atributo **Cifrado** está habilitado.

#### Actualización de los certificados de DRA

Deberá actualizar los certificados de DRA en las siguientes circunstancias:

-   La organización va a migrar de DRA locales a una infraestructura de DRA centralizada.

-   Debe actualizar una directiva de DRA centralizada porque los certificados de DRA existentes han expirado (o expirarán pronto).

-   Debe actualizar una directiva de DRA centralizada porque el material de clave de DRA existente se ha perdido, no está en su sitio o ha perdido su carácter confidencial.

##### Consideraciones de actualización de los certificados de DRA

Para actualizar los certificados de DRA, primero debe solicitar o crear uno o más pares de claves y certificados de DRA nuevos. Según el entorno que tenga, podrá realizar esta tarea de una de las siguientes formas:

-   Uso del parámetro /R con Cipher.exe.

-   Uso de Web o de interfaces programáticas ofrecidas por los Servicios de Certificate Server de Microsoft.

-   Uso del mecanismo de solicitud de la entidad de certificación de terceros existente.

La solicitud debe usar una plantilla de DRA adecuada para que se pueda usar el certificado emitido como DRA.

Después de solicitar y obtener los nuevos certificados de DRA, debe enlazarlos a una directiva de grupo adecuada que se aplique a todos los equipos cuya información de DRA desee actualizar. Asegúrese de que el objeto de directiva de grupo que usa aplica correctamente los nuevos certificados de DRA a las diversas unidades organizativas, dominios de Active Directory y bosques de Active Directory. De manera predeterminada, es posible que pueda usar el GPO de la directiva de dominio predeterminada de Active Directory como base para la distribución de la nueva información de DRA.

Después de asignar los nuevos certificados de DRA a un GPO, puede eliminar los certificados de DRA existentes. No obstante, si lo hace, perderá la capacidad de recuperar archivos que se crearon con el certificado de DRA existente. Antes de eliminar un certificado de DRA, asegúrese de que tiene una copia utilizable que le permita recuperar archivos cifrados.

Los cambios de DRA no tienen lugar en los equipos individuales hasta que dichos equipos actualicen sus parámetros de directiva de grupo. Puede esperar a que se realice la próxima actualización de directiva de seguridad (que se realiza de manera predeterminada cada 90 minutos), ejecutar el comando **gpupdate /force** en los equipos afectados o volver a arrancarlos.

También debe archivar los pares de claves y los certificados de DRA para aumentar la seguridad de la clave privada. Después, debe eliminar el par de claves y el certificado del almacén de certificados de usuario de cualquier usuario que haya importado el certificado y el par de claves. Al hacerlo, asegúrese de seleccionar la casilla **Eliminar la clave privada si la exportación es satisfactoria** del Asistente para exportación.

Después de que se haya actualizado la información de DRA, puede continuar con la actualización de los archivos protegidos con EFS de los equipos de destino como se describe en la siguiente sección.

#### Actualización de archivos de certificados de DRA o de usuario nuevos

Después de cambiar o actualizar los DRA usados en la organización, debe actualizar todos los archivos que estuvieran protegidos con el DRA anterior. Puede hacerlo manualmente abriendo y guardando cada archivo, aunque este método lleva mucho tiempo y puede inducir a error. También puede usar el parámetro /U con el comando Cipher.exe, que recorrerá el disco local y actualizará la información de DRA de cada uno de los archivos cifrados que encuentre.

Como parte de este proceso, puede que desee realizar los siguientes pasos:

-   Capturar la salida de **Cipher /U** en un registro de errores y almacenarlo en una ubicación centralizada (como recurso compartido de red).

-   Considerar el uso del marcador /I para obligar a Cipher.exe a que omita los errores. Si no lo hace, cuando **Cipher /U** encuentre archivos bloqueados u ocupados, no podrá actualizarlos y no se podrá realizar el proceso de actualización.

-   Es posible que desee crear un script para realizar la actualización en vez de ejecutar **Cipher /U** desde la línea de comandos. La creación de este script podría llevar mucho tiempo, por lo que puede que no sea conveniente ejecutarlo durante el proceso de inicio de sesión. No obstante, puede programarlo para que se ejecute en los equipos del usuario o pedir a los usuarios que lo invoquen manualmente cuando sea oportuno.

[](#mainsection)[Principio de la página](#mainsection)

### Más información

-   [Configuración de Active Directory para la creación de copias de seguridad de la información de Cifrado de unidad BitLocker de Windows y de recuperación del Módulo de plataforma segura](http://go.microsoft.com/fwlink/?linkid=67438)

-   [Cómo usar BitLocker Recovery Password Viewer para la herramienta Usuarios y equipos de Active Directory y ver contraseñas de recuperación de Windows Vista](http://support.microsoft.com/kb/928202)

-   [Cómo usar la herramienta de reparación de BitLocker para ayudar a recuperar datos de un volumen cifrado de Windows Vista](http://support.microsoft.com/kb/928201)

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Consiga el Kit de herramientas de cifrado de datos para equipos móviles](http://go.microsoft.com/fwlink/?linkid=81666)

**Notificaciones de actualizaciones**

[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=kit%20de%20herramientas%20de%20cifrado%20de%20datos%20para%20equipos%20móviles,%20guía%20de%20implementación%20y%20planeación%20para%20el%20kit%20de%20herramientas%20de%20cifrado%20de%20datos)

[](#mainsection)[Principio de la página](#mainsection)
