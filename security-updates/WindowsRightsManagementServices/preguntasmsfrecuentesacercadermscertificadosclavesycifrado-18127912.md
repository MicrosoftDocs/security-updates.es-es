---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Certificados, claves y cifrado'
Title: 'Preguntas más frecuentes acerca de RMS: Certificados, claves y cifrado'
ms:assetid: 'ad8cc088-1dea-44c2-be68-9091129f0f12'
ms:contentKeyID: 18127912
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747725(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Certificados, claves y cifrado
======================================================================

Preguntas más frecuentes acerca de certificados, claves y cifrado de RMS
------------------------------------------------------------------------

-   [¿Qué algoritmos de cifrado se utilizan en RMS?](#bkmk_10)
-   [¿Utiliza RMS cifrado certificado por FIPS?](#bkmk_11)
-   [Para plantillas o licencias de publicación que conceden permisos a una lista de distribución en lugar de usuarios individuales, ¿se manejan de forma diferente las licencias de uso para evaluar dinámicamente a los miembros?](#bkmk_12)
-   [Cuando se utiliza RMS desde un quiosco, se emite un certificado de cuenta de permisos (RAC) temporal. ¿En qué se diferencian un RAC temporal y un RAC estándar? ¿Cómo detecta RMS que está siendo utilizado en un quiosco?](#bkmk_13)
-   [¿Cuándo se utiliza un RAC temporal?](#bkmk_14)
-   [¿Emite RMS certificados X.509v3?](#bkmk_15)
-   [¿Dónde se almacenan los certificados XrML?](#bkmk_16)
-   [¿Dónde se almacena el par de claves privada/pública del equipo?](#bkmk_17)
-   [¿Dónde se almacena el par de claves privada/pública del cliente?](#bkmk_18)
-   [AES es un algoritmo simétrico. ¿Cómo se pasan las claves entre el servidor y el usuario de forma segura?](#bkmk_19)

#### ¿Qué algoritmos de cifrado se utilizan en RMS?

RMS utiliza claves de 2048 bits de RSA para el servidor de RMS y claves de 1024 bits de RSA para el par de claves del usuario y el equipo.

#### ¿Utiliza RMS cifrado certificado por FIPS?

En RMS con Service Pack 1 y posterior, las cajas de seguridad generadas por la aplicación cliente de RMS usan cifrado AES certificado por FIPS cuando el cliente está instalado en un equipo con Windows XP o Windows Server 2003. Sin embargo, si el cliente de RMS está instalado en equipos con Windows 2000, no se instala una biblioteca AES certificada por FIPS, de modo que las cajas de seguridad no son compatibles con FIPS.

#### Para plantillas o licencias de publicación que conceden permisos a una lista de distribución en lugar de usuarios individuales, ¿se manejan de forma diferente las licencias de uso para evaluar dinámicamente a los miembros?

Las licencias de uso siempre se conceden a usuarios individuales. Si una plantilla o licencia de publicación nombra a un grupo, RMS evalúa la pertenencia a grupos en el momento de emisión de licencias de uso. Si el usuario que solicita la licencia es miembro del grupo especificado, se emite la licencia de uso para la identidad del usuario.

#### Cuando se utiliza RMS desde un quiosco, se emite un certificado de cuenta de permisos (RAC) temporal. ¿En qué se diferencian un RAC temporal y un RAC estándar? ¿Cómo detecta RMS que está siendo utilizado en un quiosco?

La aplicación compatible con RMS debe determinar si el cliente de RMS necesita solicitar un RAC temporal o estándar para el usuario. No hay método de detección para esta situación. Microsoft Office 2003 es un ejemplo de aplicación compatible con RMS que permite al usuario seleccionar el RAC adecuado.

La principal diferencia entre un RAC temporal y un RAC estándar es la presencia de un identificador de seguridad de usuario y la especificación de un período de validez. Los RAC temporales no incluyen el SID de usuario y tienen un período de validez especificado en un número de minutos. El período de validez predeterminado de un RAC temporal es de 15 minutos. Sin embargo, los RAC estándar no incluyen el SID de usuario, y tienen un período de validez especificado en un número de días. El período de validez predeterminado de un RAC estándar es de 365 días.

#### ¿Cuándo se utiliza un RAC temporal?

Un RAC temporal está diseñado para permitir a un usuario utilizar contenido protegido con RMS en equipos que cumplan con las condiciones siguientes:

-   Un equipo que no forme parte del mismo bosque que la instalación de RMS desde la que se obtuvo el RAC.
-   Un equipo que forme parte de un bosque distinto del que contiene la cuenta de usuario.
-   El usuario no está seguro de si utilizará el mismo equipo más tarde.

Cumplen con estas condiciones los equipos que se encuentran en terminales de aeropuerto, bibliotecas públicas o cafés Internet, por ejemplo.

#### ¿Emite RMS certificados X.509v3?

No. RMS emite certificados XrML para representar a los usuarios y una expresión de directiva que está más allá del ámbito de los certificados X.509v3.

#### ¿Dónde se almacenan los certificados XrML?

Un sistema RMS utiliza los siguientes certificados y licencias guardados en XrML en el equipo cliente.

-   Certificado de equipo
    Nombre de archivo: Archivo CERT-Machine.drm
    Ubicación: %USERPROFILE%\\Configuración local\\Datos de programa\\Microsoft\\DRM\\
-   Certificado de cuenta de permisos
    Prefijo del nombre de archivo: GIC
    Ubicación: %USERPROFILE%\\Configuración local\\Datos de programa\\Microsoft\\DRM\\
-   Certificado emisor de licencias de cliente
    Prefijo del nombre de archivo: CLC
    Ubicación: %USERPROFILE%\\Configuración local\\Datos de programa\\Microsoft\\DRM\\
-   Licencia de uso
    Prefijo del nombre de archivo: EUL
    Ubicación: %USERPROFILE%\\Configuración local\\Datos de programa\\Microsoft\\DRM\\

> [!NOTE]
> Una cuenta de usuario tiene un único certificado de equipo, un archivo GIC y un archivo CLC, pero múltiples archivos EUL para cada elemento de contenido al que se obtiene acceso. 

> [!NOTE]
> Para el cliente de RMS integrado con Windows Vista®, la ubicación es %USERPROFILE%\\AppData\\Local\\Microsoft\\DRM. 

#### ¿Dónde se almacena el par de claves privada/pública del equipo?

La clave privada del equipo está almacenada de forma segura, protegida por claves criptográficas vinculadas a las credenciales de inicio de sesión del usuario y a la configuración del equipo.

#### ¿Dónde se almacena el par de claves privada/pública del cliente?

El par de claves de una cuenta de usuario se almacena en el certificado de cuenta de permisos.

#### AES es un algoritmo simétrico. ¿Cómo se pasan las claves entre el servidor y el usuario de forma segura?

En el sistema se utilizan tanto claves simétricas como públicas/privadas. El contenido está cifrado con una clave simétrica, pero las demás claves del sistema (usuario, equipo y servidor) son claves públicas/privadas de RSA. La clave de contenido simétrica siempre está cifrada en las distintas licencias, ya sea la clave pública de RSA del servidor de RMS en la licencia de publicación o la clave pública de RSA del usuario en la licencia de uso.
