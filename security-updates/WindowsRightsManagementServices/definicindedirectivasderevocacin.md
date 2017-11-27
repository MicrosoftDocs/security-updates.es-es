---
TOCTitle: Definición de directivas de revocación
Title: Definición de directivas de revocación
ms:assetid: 'e2fffe9f-def7-439b-a8aa-43f8a065813d'
ms:contentKeyID: 18127987
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747782(v=WS.10)'
---

Definición de directivas de revocación
======================================

Para definir directivas de revocación para una organización, es necesario considerarlas y planearlas cuidadosamente, ya que si bien la implementación de revocaciones proporciona mayor seguridad para el contenido protegido, puede afectar a la capacidad de los usuarios de utilizar contenido. Las directivas de revocación para la implementación de RMS pueden definirse desde el sitio Web de administración.

Revocación de terceros
----------------------

Puesto que el servicio de inscripción de Microsoft es el emisor del certificado emisor de licencias del servidor de certificación raíz para la implementación de RMS, Microsoft puede revocar el certificado emisor de licencias de servidor. No obstante, Microsoft sólo revocará un certificado emisor de licencias de servidor cuando un tribunal así se lo ordene.

Además del servicio de inscripción de Microsoft, puede especificar una entidad de terceros que pueda revocar el certificado emisor de licencias del servidor de RMS. Esta entidad tercera puede ser una entidad externa o un par de claves públicas o privadas que el administrador genere en nombre de la organización. La clave privada de la entidad tercera que se especifica puede firmar una lista de revocaciones que revoque el certificado emisor de licencias de servidor. Esta entidad de terceros se especifica mediante su clave pública durante el establecimiento de los servicios en línea de RMS. Las plantillas de directiva de permisos del servidor también pueden configurarse para permitir a terceros revocar contenido, manifiestos de aplicaciones, licencias y certificados emitidos por la instalación de RMS. Para obtener más información, vea “[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)”, más adelante en este tema.

> [!IMPORTANT]
> Si decide generar su propio par de claves para utilizarlo a fin de revocar el certificado emisor de licencias de servidor del servidor de certificación raíz, asegúrese de guardarlo en una ubicación segura. 

La revocación de un certificado emisor de licencias de servidor es una decisión importante, ya que todos los certificados y licencias emitidos por su instalación de RMS quedarán invalidados cuando se revoque este certificado. Para obtener más información acerca de la revocación de certificados emisores de licencias de servidor, vea “[Revocación de certificados emisores de licencias de servidor](https://technet.microsoft.com/8020861d-d196-4431-8282-044675ef5616)”, más adelante en este tema.

Consideración de los efectos de las listas de revocaciones
----------------------------------------------------------

Una vez que se requiera la revocación para un contenido protegido concreto, se utilizarán todas las listas de revocaciones registradas en los equipos cliente y surtirá efecto si se cumple una condición especificada. Por tanto, utilice su criterio cuando implemente la revocación, ya que las listas de revocaciones se registran en los equipos cliente y es posible que se apliquen más ampliamente de lo que desee. Para obtener más información acerca de la configuración de esta opción, vea “[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)”, más adelante en este tema.

Equilibrio entre seguridad y facilidad de uso
---------------------------------------------

Cuando especifique una directiva de revocación en una plantilla de directiva de permisos, compare la necesidad de proporcionar mayor seguridad para los documentos con la posibilidad de que los usuarios experimenten problemas cuando utilicen contenido, como se describe en el siguiente ejemplo.

Como parte de la configuración de una lista de revocaciones en una plantilla de directiva de permisos, especifique también un intervalo de actualización para la lista de revocaciones. Para utilizar contenido que se publique utilizando esta plantilla de directiva de permisos, debe existir una lista de revocaciones en el equipo del usuario y ésta no debe ser más antigua que el intervalo de actualización especificado. Por ejemplo, si el intervalo de actualización es 10, la lista de revocaciones debe haberse creado en los últimos 10 días. Si no existe una lista de revocaciones en el equipo cliente o si la fecha de creación de la lista es anterior al intervalo de actualización, la aplicación compatible con RMS obtendrá la lista de revocaciones más reciente de la ubicación que haya especificado en la licencia de uso. Sin embargo, es posible que un usuario que no esté conectado a la red no pueda obtener una lista de revocaciones actual y, por tanto, no pueda utilizar el contenido.

Las siguientes sugerencias pueden ayudarle a mitigar este problema:

-   Tenga cuidado cuando especifique el intervalo de actualización para una lista de revocaciones y tome medidas para asegurarse de que la lista de revocaciones actualizada resulte siempre accesible para los usuarios.
-   Mantenga las listas de revocaciones en direcciones URL accesibles tanto dentro como fuera de la red corporativa.
-   Utilice Microsoft® Systems Management Server (SMS) u otro mecanismo similar para distribuir las copias actualizadas de las listas de revocaciones a todos los equipos cliente en un intervalo determinado, por ejemplo, todas las noches.
-   Requiera la revocación únicamente para los tipos de documento más confidenciales.
