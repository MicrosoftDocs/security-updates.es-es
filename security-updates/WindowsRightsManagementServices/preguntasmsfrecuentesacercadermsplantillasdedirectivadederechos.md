---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Plantillas de directiva de derechos'
Title: 'Preguntas más frecuentes acerca de RMS: Plantillas de directiva de derechos'
ms:assetid: '01515f08-9844-4c1a-9ab5-a5a60a901b50'
ms:contentKeyID: 18127679
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720175(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Plantillas de directiva de derechos
===========================================================================

Preguntas más frecuentes acerca de las plantillas de RMS
--------------------------------------------------------

-   [¿Puedo imponer una plantilla predeterminada de RMS sobre todo el contenido creado dentro de una organización para que una empresa pueda asegurar un conjunto de permisos mínimo?](#bkmk_57)
-   [¿Dónde están ubicadas las plantillas de directiva de RMS?](#bkmk_58)
-   [Cuando se crean las plantillas, los alias de usuario y las listas de distribución (DL) quedan vinculados a ellas. ¿Cómo puede una organización con múltiples departamentos proporcionar plantillas con los mismos permisos básicos pero conceder esos permisos a grupos diferentes en función del contenido?](#bkmk_59)
-   [¿Se aplican los permisos a un documento estático? Si se envía un archivo y hay que modificar los permisos más adelante, ¿puede modificarse, teniendo en cuenta que la licencia de publicación está incrustada en el archivo y no en el servidor de "directivas" de RMS?](#bkmk_60)

#### ¿Puedo imponer una plantilla predeterminada de RMS sobre todo el contenido creado dentro de una organización para que una empresa pueda asegurar un conjunto de permisos mínimo?

Sí. Utilizando el SDK de los Servicios de Rights Management, puede desarrollarse una aplicación personalizada que pueda imponer las plantillas necesarias. Sin embargo, la implementación de Information Rights Management en Office 2003 y posterior no admite la aplicación de plantillas sobre el contenido.

#### ¿Dónde están ubicadas las plantillas de directiva de RMS?

La ubicación de la plantilla está determinada por la aplicación compatible con RMS. En Office 2003 y posterior, se almacena como configuración de usuario en la siguiente ubicación del Registro:

**HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\11.0\\Common\\DRM\\AdminTemplatePath**

O bien

**HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\12.0\\Common\\DRM\\AdminTemplatePath** para Microsoft Office 2007.

> [!NOTE]
> Si esta entrada apunta a una carpeta local en el cliente, los archivos de plantilla deben copiarse en el cliente. Si apunta a una carpeta compartida de red, no estará disponible cuando el usuario no esté conectado. 

#### Cuando se crean las plantillas, los alias de usuario y las listas de distribución (DL) quedan vinculados a ellas. ¿Cómo puede una organización con múltiples departamentos proporcionar plantillas con los mismos permisos básicos pero conceder esos permisos a grupos diferentes en función del contenido?

Hay dos soluciones para este caso:

-   Cree una única plantilla confidencial de la compañía, con licencia para todos los empleados de la unidad de negocio, utilice esa plantilla en un mensaje de correo electrónico y envíe el mensaje a personas concretas. La ventaja es que requiere una única plantilla para cada unidad de negocio para correo electrónico, y puede restringirse a los usuarios en función del destinatario. La desventaja es que cualquier persona de fuera del grupo al que se le mandó originalmente todavía podrá leerlo.

-   Como alternativa, cree múltiples plantillas, incluida una para cada lista de distribución. Aunque esto proporciona un control mucho más preciso, también significa que el departamento de TI debe permitir plantillas múltiples.

#### ¿Se aplican los permisos a un documento estático? Si se envía un archivo y hay que modificar los permisos más adelante, ¿puede modificarse, teniendo en cuenta que la licencia de publicación está incrustada en el archivo y no en el servidor de "directivas" de RMS?

Sí, esto es posible cuando se utiliza una plantilla de directiva de RMS: Cuando se publica contenido utilizando una plantilla de directiva de RMS, la definición de la directiva se mantiene en el servidor, y puede ser modificada por un administrador una vez publicado el contenido. Cuando un usuario solicita una licencia para el contenido, la licencia concede permisos de acuerdo con la directiva actual definida en el servidor. Si se modifican los permisos después de conceder una licencia a un usuario, éste seguirá teniendo los permisos vigentes en el momento de concederle la licencia. Para permitir que aplique una nueva plantilla de directiva de permisos una vez publicado el contenido, habilite una directiva de caducidad para la plantilla y especifique la opción **Las licencias de uso del contenido deben renovarse cada: n días**. Para n, especifique el número de días después del cual un usuario debe solicitar una nueva licencia de uso.