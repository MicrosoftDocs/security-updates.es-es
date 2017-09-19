---
TOCTitle: Plantillas de directiva de permisos
Title: Plantillas de directiva de permisos
ms:assetid: 'eee931c8-7c98-48e9-9e2c-d0b7bd4f2b96'
ms:contentKeyID: 18128031
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747732(v=WS.10)'
---

Plantillas de directiva de permisos
===================================

Las plantillas de directiva de permisos describen un conjunto estándar de usuarios, permisos y condiciones que puede aplicarse a contenido protegido con RMS. Cuando un usuario aplica una plantilla de directiva de permisos a un fragmento de contenido, los permisos que describe se convierten en parte de la licencia de publicación.

En el sitio Web de administración de RMS, se pueden crear plantillas de directiva de permisos, así como eliminar o modificar las existentes. Las plantillas de directiva de permisos pueden incluir diversas condiciones, como destinatarios o grupos de Active Directory determinados, el período de validez de una licencia de uso para el contenido, cuánto tiempo después de la publicación se puede utilizar el contenido e, incluso, valores personalizados que resulten significativos para una aplicación compatible con RMS determinada. Una plantilla puede requerir una lista de revocaciones. Si es así, la plantilla especifica la dirección URL al archivo de la lista y el número de días que dicha lista es válida. Cuando un destinatario solicita una licencia de uso que se basa en la plantilla, el sistema comprueba la lista de revocaciones antes de que el usuario utilice el contenido protegido con RMS. Para obtener más información, vea "[Revocación de RMS](https://technet.microsoft.com/72689f90-f3c5-4b61-94ea-d825f3199b3b)", más adelante en este tema.

A continuación, se muestran algunos ejemplos de los permisos que se pueden establecer en una plantilla de directiva de permisos:

-   Cualquiera puede ver el contenido, pero sólo el autor puede modificarlo.
-   Cualquiera en la empresa puede ver el contenido, pero sólo durante un mes tras la publicación.
-   Cualquiera en la empresa puede ver el contenido, pero ningún socio o cliente externo puede verlo.
-   Sólo los destinatarios especificados pueden ver el contenido.
-   Sólo el destinatario especificado puede ver o modificar el contenido.

Las plantillas pueden incluir diversas condiciones, tales como:

-   Destinatarios o grupos de Active Directory específicos que tienen permisos sobre el contenido.
-   Período de vigencia de una licencia de uso sobre el contenido.
-   Período de tiempo tras la publicación que se puede utilizar el contenido.
-   Si la licencia de uso requiere una lista de revocaciones y con qué frecuencia se debe actualizar dicha lista.
-   Valores personalizados que resultan significativos para una aplicación compatible con RMS determinada.

Las plantillas de directiva de permisos se almacenan tanto en la base de datos de configuración como en una carpeta compartida. El administrador de RMS es responsable de distribuir las plantillas de directiva de permisos desde la carpeta compartida a los equipos cliente, para que los autores puedan utilizarlas. Para obtener más información, vea "Distribución de plantillas de directiva de permisos" en "Operación de un servidor de RMS", en esta recopilación de documentación.

En una aplicación compatible con RMS, los autores pueden seleccionar una plantilla de directiva de permisos para aplicarla, lo que normalmente especifica el grupo cuyos integrantes pueden utilizar el contenido. Cuando un destinatario solicita una licencia de uso, el servidor aplica la plantilla de directiva de permisos de la base de datos, lo que garantiza que los términos de una licencia de uso siempre reflejan la versión más actual de la plantilla.
