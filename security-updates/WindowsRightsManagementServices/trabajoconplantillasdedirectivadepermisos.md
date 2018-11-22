---
TOCTitle: Trabajo con plantillas de directiva de permisos
Title: Trabajo con plantillas de directiva de permisos
ms:assetid: 'ff4f1143-f6b9-4dd8-aa4c-c2cbbf6fdf06'
ms:contentKeyID: 18128039
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747804(v=WS.10)'
---

Trabajo con plantillas de directiva de permisos
===============================================

Después de crear una plantilla de directiva de permisos, puede administrar cómo se aplicará en la organización controlando su distribución a los autores.

RMS almacena plantillas de directiva de permisos en la base de datos de configuración. Además, mantiene una copia de todas las plantillas de directiva de permisos en la carpeta compartida que especifique, como se describe en “[Para especificar la ubicación de las plantillas de directiva de permisos](https://technet.microsoft.com/e1bee46d-33db-424f-ba45-1dcedcb883ab)”, más adelante en este tema. Asegúrese de que las plantillas estén almacenadas en una ubicación accesible de la red que cumpla las instrucciones de seguridad de la organización. No debe crear carpetas compartidas para plantillas en las carpetas principales que utiliza RMS, como las carpetas Archivos de programa o IISRoot.

Cuando publica contenido protegido, el autor selecciona la plantilla de directiva de permisos que desea aplicar entre las plantillas que haya disponibles en el equipo local. Para hacer que las plantillas de directiva de permisos estén disponibles para su uso, el administrador debe implementarlas en los equipos de los usuarios desde una carpeta compartida.

Cuando un usuario intenta utilizar contenido protegido, la aplicación compatible con RMS obtiene de la base de datos de configuración la versión más reciente de la plantilla de directiva de permisos que se haya utilizado para publicar el contenido. A continuación, la aplicación compatible con RMS aplica su configuración al contenido. Al modificar una plantilla de directiva de permisos en el servidor de RMS, RMS actualiza la plantilla tanto en la base de datos de configuración como en la carpeta compartida (si el servidor de RMS está configurado para especificar una ubicación de archivo para almacenar copias de plantillas de directiva de permisos). Es aconsejable implementar de nuevo la plantilla de directiva de permisos en los sistemas cliente cuando se haya modificado para que la versión más reciente esté disponible en los equipos de los usuarios.

Si elimina una plantilla de directiva de permisos, se quita de la base de datos de configuración y también de la carpeta compartida (que esté especificada como ubicación para almacenar copias de plantillas) cuando la elimine. De todos modos, no se elimina de los equipos de los usuarios. Se deben eliminar manualmente desde esta ubicación. Debe quitar las plantillas de directiva de permisos eliminadas de los equipos de todos los usuarios. Si no lo hace y se utiliza la plantilla de directiva de permisos eliminada para publicar contenido, RMS no podrá emitir licencias de uso para el contenido, ya que no podrá ubicar la plantilla especificada en la base de datos de configuración.

Cuando trabaje con plantillas de directiva de permisos, realice las siguientes tareas:

-   **Especificar una carpeta compartida** Antes de crear la primera plantilla de directiva de permisos, debe especificar la carpeta compartida donde se almacenarán todas las plantillas de directiva de permisos. Para obtener más información, vea “[Para especificar la ubicación de las plantillas de directiva de permisos](https://technet.microsoft.com/e1bee46d-33db-424f-ba45-1dcedcb883ab)”, más adelante en este tema.
-   **Crear y editar plantillas de directiva de permisos** Puede crear tantas plantillas de directiva de permisos como necesite para gestionar permisos en su organización. Cuando se crea una plantilla de directiva de permisos, se definen los usuarios y los permisos que se aplican. También se define cómo se aplicará la plantilla de directiva de permisos al contenido. Más adelante, puede editar las plantillas de directiva de permisos cuando necesite actualizarlas. Para obtener más información, vea “[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)”, más adelante en este tema.
-   **Distribuir plantillas de directiva de permisos** Para que un autor pueda aplicar una determinada plantilla de directiva de permisos al contenido, debe existir una copia de esta en el equipo del autor. Puede controlar las plantillas de directiva de permisos que determinados autores podrán aplicar mediante la administración de la distribución de plantillas. Para obtener más información, vea “[Distribución de plantillas de directiva de permisos](https://technet.microsoft.com/ae6fa26f-d744-4ac9-9eb1-728ffab87bfe)”, más adelante en este tema.
-   **Retirar plantillas de directiva de permisos**. Cuando ya no sea adecuada, puede eliminar una plantilla de directiva de permisos. Cuando lo haga, debe quitarla también de los equipos de los usuarios para que éstos no experimenten problemas cuando intenten utilizar contenido que se publicó con la plantilla de directiva de permisos retirada. Para obtener más información, vea “[Retiro de plantillas de directiva de permisos](https://technet.microsoft.com/32bf98c7-edda-4507-a4b8-4c11bddd6e60)”, más adelante en este tema.
