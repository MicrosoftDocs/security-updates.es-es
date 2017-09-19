---
TOCTitle: Inscripción en RMS
Title: Inscripción en RMS
ms:assetid: '999db3e1-e3ab-4513-87d9-d584ee334c00'
ms:contentKeyID: 18127909
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747698(v=WS.10)'
---

Inscripción en RMS
==================

El proceso de inscripción de servidores crea y entrega certificados emisores de licencias de servidor. Los certificados emisores de licencias de servidor validan la identidad de los servidores que están en la implementación, y proporcionan validación de credenciales durante la utilización de contenido protegido con RMS. El primer servidor de cada uno de los clústeres de licencias se inscribe con el clúster de certificación raíz como parte del proceso de establecimiento de servicios en línea. Los siguientes servidores del clúster no se inscriben de forma independiente.

El servidor inicial de un clúster de certificación raíz (el servidor de certificación raíz) debe inscribirse con el servicio de inscripción de Microsoft. Este proceso puede realizarse automáticamente como parte del establecimiento de servicios en línea si el servidor de certificación raíz está conectado a Internet; el proceso de inscripción puede completarse sin conexión exportando una solicitud a un archivo y, a continuación, enviando el archivo al servicio de inscripción de Microsoft desde otro equipo que tenga conexión a Internet. La solicitud de inscripción devolverá un certificado emisor de licencias de servidor para el servidor de certificación raíz, que puede importarse utilizando las páginas Web de administración de RMS.

La solicitud de inscripción incluye la siguiente información:

-   Información de revocación Si la instalación de RMS utilizará revocación estándar o personalizada (de terceros). Si se utiliza revocación de terceros, se incluye la clave pública de la entidad de revocación.
-   Clave pública de certificado Clave pública del certificado emisor de licencias de servidor. Esta clave pública se genera en el servidor de RMS y se envía al servicio de inscripción del servidor de Microsoft para obtener el certificado emisor de licencias de servidor.
-   SKU Referencia de almacén RMS oficial.
-   Versión Número de versión del ensamblado RMS.
-   URL Dirección URL de base del clúster de servidor de RMS.

Cuando el servicio de inscripción de Microsoft responde a la solicitud de inscripción, devuelve la siguiente información al servidor de RMS en formato XML:

-   Certificado emisor de licencias de servidor
-   Cadena de certificados de entidades de firma.

Se transfiere la misma información independientemente de si el servidor de certificación raíz de RMS se inscribe mediante el método en línea o sin conexión. No se recopila información adicional en ninguno de los dos métodos.

Para obtener más información sobre los pasos a seguir para realizar una inscripción del servidor sin conexión, vea "Para utilizar una inscripción sin conexión para inscribir un servidor de certificación raíz" en "Operación de un servidor de RMS" en esta recopilación de documentación.

El proceso de inscripción de clientes crea y proporciona un certificado emisor de licencias de cliente que permite a un autor publicar contenido protegido con RMS desde un equipo que no esté conectado a la red corporativa. Los autores pueden solicitar un certificado emisor de licencias de cliente en cualquier momento. No es preciso inscribir a los clientes.

Todas las solicitudes de inscripción se registran.

Se tratan los siguientes temas:

-   [Inscripción en el servidor de certificación raíz](https://technet.microsoft.com/f08bc919-f090-4843-b2ce-b40d558012ce)
-   [Subinscripción en el servidor de licencias](https://technet.microsoft.com/7bc63397-9186-464c-8824-867038adce9b)
-   [Inscripción del cliente de RMS](https://technet.microsoft.com/9c1d07bf-7235-4694-8291-ac2e5b221f4a)
-   [Activación de equipo RMS](https://technet.microsoft.com/09a0d631-9860-477f-9d10-df61b3bfe125)
-   [Certificación de cuenta de RMS](https://technet.microsoft.com/c9a385c5-6dbb-47f5-a80f-69718e6f9deb)
