---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Cuestiones de seguridad'
Title: 'Preguntas más frecuentes acerca de RMS: Cuestiones de seguridad'
ms:assetid: 'ff433834-79aa-481f-bd39-3393be12a26f'
ms:contentKeyID: 18128034
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747757(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Cuestiones de seguridad
===============================================================

Preguntas más frecuentes acerca de la seguridad de RMS
------------------------------------------------------

-   [¿Qué es la cuenta de superusuario?](#bkmk_43)
-   [¿Es RMS una solución de seguridad?](#bkmk_44)
-   [¿Qué mecanismos existen para evitar que los destinatarios atrasen el reloj del equipo cliente para prolongar el acceso a un documento protegido por derechos cuando haya expirado la licencia de uso?](#bkmk_45)
-   [¿Es posible que los miembros del grupo de administradores del dominio lean documentos destinados a otra persona de su dominio?](#bkmk_46)
-   [Entiendo que cada caja de seguridad puede autenticar cada certificado o licencia que se genera en el sistema, proviniendo de un servicio registrado con Microsoft. ¿Contra qué amenaza protege esto?](#bkmk_47)
-   [Si alguien consigue abrir un documento mediante un ataque de fuerza bruta, ¿podrá abrir otros documentos con la misma clave?](#bkmk_48)
-   [Debido a las restricciones de exportación sobre las tecnologías de cifrado, ¿hay alguna parte de las claves que quede expuesta fuera de la empresa que la implementó?](#bkmk_49)
-   [¿Cómo se evita que un pirata informático malintencionado active la función de retiro de forma remota?](#bkmk_50)
-   [¿Puede un usuario realizar capturas de pantalla de contenido protegido por derechos?](#bkmk_51)
-   [¿Pueden los administradores que realizan copias de seguridad de archivos relacionados con RMS tener acceso a contenido protegido por derechos?](#bkmk_52)
-   [¿Contiene en algún momento el archivo de intercambio utilizado por Windows el contenido descrifrado, de modo que pueda dejar el contenido “abierto”?](#bkmk_53)
-   [¿Es posible limitar qué administradores pueden tener acceso a las diferentes opciones administrativas de RMS?](#bkmk_54)
-   [¿Puede RMS proteger documentos individuales justo después de crearlos, en el disco duro del usuario o en una carpeta compartida?](#bkmk_55)
-   [Al abrir un archivo, ¿están cifrados el archivo de guardado automático y los archivos temporales?](#bkmk_56)
-   [Cuando recibo un mensaje de correo electrónico protegido por derechos, parece que el mensaje incluye datos adjuntos. Puedo guardar los datos adjuntos, a pesar de que se supone que el mensaje no se puede guardar; ¿significa eso que RMS no funciona bien?](#bkmk_562)

#### ¿Qué es la cuenta de superusuario?

RMS usa un grupo especial de superusuarios que tiene control completo sobre todo el contenido protegido por derechos. Se conceden permisos de propiedad completos a los miembros del grupo de superusuarios en todas las licencias de uso emitidas para ellos por el clúster de RMS donde esté configurado el grupo de superusuarios. Esto quiere decir que los miembros de este grupo pueden descifrar todos los archivos protegidos y quitar esta protección. Por ejemplo, un miembro de este grupo puede quitar la protección de archivos que un antiguo empleado haya publicado, de forma que el nuevo propietario pueda publicarlos y administrarlos.

#### ¿Es RMS una solución de seguridad?

No, RMS no es una solución de seguridad. Cuando se usa con una aplicación habilitada para RMS, como Office 2007, puede considerarse una “solución de imposición de directivas”. Si el usuario no está autorizado para ver los datos, podrá utilizar un ataque de fuerza bruta para intentar quebrar el cifrado. Aunque el cifrado es robusto, como todos los esquemas de cifrado de software, puede ser quebrado. Sin embargo, si el usuario tiene acceso a los datos, puede copiarlo a mano o sacar una fotografía digital y hacer llegar la información a usuarios no autorizados.

#### ¿Qué mecanismos existen para evitar que los destinatarios atrasen el reloj del equipo cliente para prolongar el acceso a un documento protegido por derechos cuando haya expirado la licencia de uso?

RMS detecta si el reloj de un sistema cliente se ha atrasado o adelantado, y evita que el usuario utilice el contenido. Además, RMS detecta si hay una diferencia considerable de hora entre el servidor y el cliente de RMS.

#### ¿Es posible que los miembros del grupo de administradores del dominio lean documentos destinados a otra persona de su dominio?

Los miembros del grupo de administradores del dominio pueden leer contenido protegido para una cuenta de usuario si son miembros del grupo de superusuarios de RMS o si están suplantando la cuenta del usuario. Dado que los miembros del grupo de administradores del dominio tienen control sobre las cuentas de usuario del dominio, no existen atenuantes en caso de que haya un miembro no confiable del grupo de administradores del dominio.

Es recomendable agregar sólo a los miembros del grupo de administradores del dominio al grupo de superusuarios si necesitan tener acceso a contenido protegido por derechos. Cuando se le otorga una licencia a un miembro del grupo de superusuarios, se registra un Id. de suceso 49 en el registro de sucesos de aplicación del servidor de RMS. El Id. de suceso 49 afirma que **“Se otorgó una licencia a un usuario que pertenece al grupo de superusuarios. El usuario tiene la siguiente dirección de correo electrónico: &lt;Alias de usuarios&gt;”** donde **Alias de usuarios** se reemplaza por la cuenta de correo electrónico del usuario.

Como con otros grupos que se utilizan para limitar el acceso a los recursos, deberá definir las alertas y realizar comprobaciones de seguridad para ayudar a evitar que alguien se una al grupo de superusuarios sin autorización.

#### Entiendo que cada caja de seguridad puede autenticar cada certificado o licencia que se genera en el sistema, proviniendo de un servicio registrado con Microsoft. ¿Contra qué amenaza protege esto?

Sin ser capaz de comprobar la integridad de los certificados, un usuario puede falsificar un certificado de cuenta de permisos (RAC) concedido a otro usuario y obtener una licencia de uso para contenido, o crear una aplicación que eliminara la protección de un documento.

#### Si alguien consigue abrir un documento mediante un ataque de fuerza bruta, ¿podrá abrir otros documentos con la misma clave?

Cada elemento de contenido protegido por derechos está cifrado con una clave simétrica diferente, generada aleatoriamente. Por tanto, la clave de cada documento es única y no sirve para descifrar otros documentos.

#### Debido a las restricciones de exportación sobre las tecnologías de cifrado, ¿hay alguna parte de las claves que quede expuesta fuera de la empresa que la implementó?

Las aplicaciones firmadas en la raíz de Microsoft están sujetas a la clave raíz de firma de Microsoft, pero a partir de ese punto, no se revelan más claves por parte de Microsoft o por parte de la implementación de un cliente.

#### ¿Cómo se evita que un pirata informático malintencionado active la función de retiro de forma remota?

El pirata informático necesitará las credenciales de una cuenta de usuario que tenga derechos administrativos en el clúster de RMS. De forma predeterminada, la interfaz de administración de RMS está disponible sólo localmente en el servidor de RMS. Asegurarse de que esto sigue siendo así, que el protocolo de escritorio remoto (RDP) está deshabilitado y que el servidor está seguro físicamente ayudará a mitigar el riesgo.

#### ¿Puede un usuario realizar capturas de pantalla de contenido protegido por derechos?

Si los permisos de RMS están establecidos para no permitir la función de copia, RMS deshabilita la combinación ALT+IMPR PANT. Sin embargo, en un entorno con escritorios no administrados, un usuario puede utilizar productos que no son de Microsoft para capturar contenido.

#### ¿Pueden los administradores que realizan copias de seguridad de archivos relacionados con RMS tener acceso a contenido protegido por derechos?

No, pueden realizar la copia de seguridad pero no tienen acceso.

#### ¿Contiene en algún momento el archivo de intercambio utilizado por Windows el contenido descrifrado, de modo que pueda dejar el contenido “abierto”?

Cuando el cliente de RMS vuelve a enviar contenido descifrado a la aplicación, puede aparecer en el archivo de intercambio. Parte de las recomendaciones de desarrollo de aplicaciones RMS del kit de desarrollo de software (SDK) de Servicios de Microsoft Rights Management (RMS) incluyen instrucciones para evitar que esto ocurra, pero la responsabilidad de hacerlo es de la aplicación compatible con RMS.

#### ¿Es posible limitar qué administradores pueden tener acceso a las diferentes opciones administrativas de RMS?

Sí, puede crear un grupo de administradores de RMS diferente en Active Directory, agregar usuarios y crear la lista de control de acceso (ACL) adecuada para las páginas de administración. Por ejemplo, la configuración predeterminada de las listas de control de acceso de la página Web de administración de RMS especifica que la página de configuración de seguridad está accesible sólo para el usuario que estableció los servicios en línea del servidor.

#### ¿Puede RMS proteger documentos individuales justo después de crearlos, en el disco duro del usuario o en una carpeta compartida?

Aunque puede utilizarse RMS para proteger documentos almacenados en el equipo local de un usuario, la opción recomendada es el Sistema de archivos de cifrado (EFS). EFS protege los documentos de forma transparente, mientras que RMS requiere intervención manual (un par de clics con el mouse) para proteger el documento.

#### Al abrir un archivo, ¿están cifrados el archivo de guardado automático y los archivos temporales?

Sí, todos los documentos temporales están cifrados.

#### Cuando recibo un mensaje de correo electrónico protegido por derechos, parece que el mensaje incluye datos adjuntos. Puedo guardar los datos adjuntos, a pesar de que se supone que el mensaje no se puede guardar; ¿significa eso que RMS no funciona bien?

No. Este es el comportamiento normal. Los datos adjuntos son el mensaje cifrado antes de que el cliente de RMS lo haya descifrado. Sigue estando protegido por derechos y no puede guardarse una vez descifrado.
