---
TOCTitle: Inscripción en el servidor de certificación raíz
Title: Inscripción en el servidor de certificación raíz
ms:assetid: '3f69d25e-ecae-447f-b741-a819c8cf6227'
ms:contentKeyID: 18127716
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720250(v=WS.10)'
---

Inscripción en el servidor de certificación raíz
================================================

Todas las instalaciones de RMS deben incluir al menos un servidor de certificación raíz y pueden incluir opcionalmente servidores de certificación raíz en un clúster. El primer servidor de certificación raíz que instale debe inscribirse con el servicio de inscripción de Microsoft para obtener un certificado emisor de licencias de servidor raíz. Este certificado sirve de base para la jerarquía de confianza en una implementación de RMS.

Puede obtenerse un certificado emisor de licencias de servidor raíz utilizando uno de los siguientes métodos. Puede seleccionar qué método utilizará cuando complete la información de establecimiento para su servidor de RMS:

-   **Inscripción en línea**. Si el servidor de certificación raíz tiene la posibilidad de conectarse a Internet, puede obtener un certificado emisor de licencias de servidor de forma automática durante el establecimiento de servicios en línea. Es el método predeterminado.

-   **Inscripción fuera de línea**. Si el servidor de certificación no tiene acceso a Internet, puede realizar la inscripción manualmente cuando finalice el proceso de establecimiento de servicios en línea. Para ello, exporte una solicitud de inscripción de este servidor a un archivo que se pueda trasladar a otro equipo que disponga de conexión a Internet y, a continuación, enviar al servicio de inscripción de Microsoft para obtener un certificado emisor de licencias de servidor. Si se selecciona la inscripción fuera de línea en el momento del establecimiento de servicios en línea, RMS realizará el proceso de establecimiento de servicios en línea, pero no podrá utilizarse hasta que el certificado emisor de licencias de servidor que ha obtenido el otro servidor se haya importado. Para obtener más información, vea "[Para inscribir manualmente un servidor de certificación raíz](https://technet.microsoft.com/aecdebb5-b28b-4b58-937a-392bb6ce9643)", más adelante en este tema.

La solicitud de inscripción incluye la siguiente información:

-   Información de revocación Si la instalación de RMS utilizará revocación estándar o personalizada (de terceros). Si se utiliza revocación Microsoft de terceros, se incluye la clave pública de la entidad de revocación.

-   Clave pública de certificado Clave pública del certificado emisor de licencias de servidor. Esta clave pública se genera en el servidor de RMS y se envía al servicio de inscripción de Microsoft para obtener el certificado emisor de licencias de servidor.

-   SKU Referencia de almacén RMS oficial.

-   Versión Número de versión del ensamblado RMS.

-   URL Dirección URL de base del clúster de servidor de RMS.

Cuando el servicio de inscripción de Microsoft responde la solicitud de inscripción, devuelve la siguiente información al servidor de RMS en formato XML:

-   Certificado emisor de licencias de servidor

-   Cadena de certificados de entidades de firma.

Se transfiere la misma información tanto si el servidor de certificación raíz de RMS se ha inscrito siguiendo el método en línea o sin conexión. No se recopila información adicional cuando se utiliza alguno de estos dos métodos.

> [!NOTE]
> Si ha seleccionado utilizar la inscripción fuera de línea y va a utilizar un equipo que disponga de una configuración de seguridad de navegador ampliada, como un equipo con Windows Server 2003 o Windows XP Service Pack 2, para conectarse a Internet y solicitar un certificado emisor de licencias de servidor, asegúrese de agregar la dirección URL del sitio Web de servicio de inscripción a la zona de sitios de confianza para permitir la descarga del certificado emisor de licencias de servidor. Esta dirección URL es https://activation.drm.microsoft.com. Si va a utilizar el proceso de inscripción fuera de línea, asegúrese de que el equipo que utilice para enviar la solicitud de inscripción al servicio de inscripción de Microsoft tenga todas las actualizaciones de certificados más recientes instaladas. El certificado SSL de los servicios de inscripción de Microsoft es GTE Cyber Trust Root CA, en el que se confía de manera predeterminada en todos los equipos con Windows Server 2003. Si va a utilizar el proceso de inscripción fuera de línea, debe asegurarse de que los clientes de RMS no intenten conectarse al servidor de RMS para obtener licencias hasta que haya tenido lugar la inscripción. Si los clientes intentan conectarse a un servidor de RMS que no está inscrito, los servicios Web darán un error que no permitirá utilizarlos. Si no puede garantizar que los clientes no intenten conectarse al servidor de RMS, lo mejor es restablecer IIS después de realizar la inscripción para eliminar las condiciones de error que se hayan podido generar.