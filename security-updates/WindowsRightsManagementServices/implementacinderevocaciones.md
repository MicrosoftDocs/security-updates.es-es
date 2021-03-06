---
TOCTitle: Implementación de revocaciones
Title: Implementación de revocaciones
ms:assetid: '4735f060-7197-4ae2-830a-f91bcc4de30a'
ms:contentKeyID: 18127798
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747554(v=WS.10)'
---

Implementación de revocaciones
==============================

Los certificados y las licencias pueden ser revocados por cualquier entidad principal que se encuentre en la cadena de confianza del certificado o de la licencia. Un servidor de certificación raíz puede revocar todos los certificados o las licencias que haya emitido. Además, los certificados pueden ser revocados por una entidad tercera que el administrador de RMS haya seleccionado.

Para revocar un certificado o una licencia otorgada por el servidor de RMS, puede crear y distribuir una lista de revocaciones y después requerirla en una plantilla de directiva de permisos, como se describe en los siguientes pasos:

1.  Cree una lista de revocaciones que especifique las entidades principales que deben revocarse. Se trata de un archivo de texto con formato XML que se ajuste al vocabulario de XrML. Para obtener más información, vea “[Creación de listas de revocaciones](https://technet.microsoft.com/1ef75199-3344-4225-84de-a863a777696a)”, más adelante en este tema.
2.  Genere un par de claves para la lista de revocaciones. A continuación, firme el archivo con la clave privada utilizando la herramienta de firma de lista de revocaciones que se proporciona a tal fin. Para obtener instrucciones, vea “Inserción de una firma en una lista de revocaciones”, más adelante en este tema. Debe automatizar este proceso de forma que se produzca regularmente, preferentemente a diario.
3.  Sitúe el archivo de lista de revocaciones en una ubicación que resulte accesible a todos los usuarios que lo necesiten. Es recomendable que sitúe el archivo en una ubicación accesible desde la red e Internet, preferentemente en un sitio Web. Esto garantiza a los usuarios el acceso al archivo tanto desde dentro como desde fuera de la red corporativa.
4.  Cree una plantilla de directiva de permisos que incluya un requisito para la lista de revocaciones. Para obtener más información, vea “[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)”, más adelante en este tema.

También puede revocar el certificado emisor de licencias de servidor del servidor de certificación raíz. Puesto que este certificado fue emitido por el servicio de inscripción de Microsoft (Microsoft Enrollment Service), Microsoft puede revocar el certificado emisor de licencias de servidor de la certificación raíz. Para hacerlo, Microsoft agrega el certificado emisor de licencias de servidor a su lista de revocaciones y la pone a disposición públicamente.

Por otra parte, una entidad tercera puede revocar el certificado emisor de licencias de servidor del servidor de certificación raíz si el administrador de RMS decide habilitar esa opción durante el establecimiento de los servicios en línea. Si utiliza esta opción, se pondrá a disposición de los clientes una lista de revocaciones que incluye este certificado emisor de licencias de servidor y que ha sido firmada con la clave privada de una entidad de terceros. Para obtener más información, vea “[Revocación de certificados emisores de licencias de servidor](https://technet.microsoft.com/8020861d-d196-4431-8282-044675ef5616)”, más adelante en este tema.

> [!CAUTION]
> Tenga cuidado cuando implemente la revocación. Según el intervalo de actualización que especifique, deberá renovar la lista de revocaciones periódicamente o ésta caducará de forma automática, lo que impedirá a los usuarios utilizar el contenido que requiere la lista. Para asegurarse de no impedir inadvertidamente a los usuarios que utilicen contenido, evalúe detenidamente el intervalo que necesita para actualizar la lista de revocaciones. Asimismo, cerciórese de que la lista de revocaciones resulte accesible desde dentro y desde fuera de la red. Para obtener más información, vea “[Definición de directivas de revocación](https://technet.microsoft.com/e2fffe9f-def7-439b-a8aa-43f8a065813d)”, anteriormente en este tema. 
