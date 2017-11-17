---
TOCTitle: Revocación de certificados emisores de licencias de servidor
Title: Revocación de certificados emisores de licencias de servidor
ms:assetid: '8020861d-d196-4431-8282-044675ef5616'
ms:contentKeyID: 18127861
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747578(v=WS.10)'
---

Revocación de certificados emisores de licencias de servidor
============================================================

Es posible que una organización deba revocar un certificado emisor de licencias de servidor como consecuencia de circunstancias imprevistas en las que la seguridad del servidor de RMS se vea comprometida. Si no guarda una clave privada en un módulo de seguridad de hardware, será vulnerable a robos. La clave y el certificado emisor de licencias de servidor de una organización podrían verse comprometidos por un pirata informático que se haga con el control del servidor o por un empleado descontento que copie o quite la clave o el certificado. La revocación es un método para limitar los daños y el abuso por parte de usuarios maliciosos.

De forma predeterminada, cualquier licencia o certificado puede ser revocado por la entidad principal que lo emitió. Puesto que los servidores de RMS emiten las licencias y los certificados asociados al contenido protegido, siempre puede revocarlos si es necesario. Si un servidor de licencias se ve comprometido, puede revocar su certificado emisor de licencias de servidor. Cuando revoque un certificado emisor de licencias de servidor, todos los certificados y las licencias que haya emitido quedarán invalidados. Encontrará instrucciones para revocar licencias y certificados en "[Implementación de revocaciones](https://technet.microsoft.com/4735f060-7197-4ae2-830a-f91bcc4de30a)", anteriormente en este tema.

Sin embargo, el clúster de certificación raíz constituye un caso especial. El certificado emisor de licencias de servidor del clúster de certificación raíz es emitido por el servicio de inscripción de Microsoft (Microsoft Enrollment Service) y, de forma predeterminada, sólo éste puede revocarlo.

Microsoft puede revocar el certificado emisor de licencias de un servidor de certificación raíz sólo si así se lo ordena un tribunal y usted proporciona la clave pública del servidor al tribunal. Una vez que el tribunal notifique a Microsoft que debe realizar la revocación, Microsoft especifica el certificado emisor de licencias de servidor por su clave pública en la lista de revocaciones y la pone a disposición pública. Puede solicitar a un tribunal que ordene la revocación si el servidor cuya licencia debe revocarse cumple una de las siguientes condiciones:

-   El servidor es de su propiedad y la seguridad de la clave pública se ha visto comprometida.
-   El contenido que se publica en el servidor es de su propiedad y la publicación de dicho contenido infringe el copyright.

Siga los pasos que se describen en "[Implementación de listas de revocaciones](https://technet.microsoft.com/e331338b-66d4-45e4-8d3f-acccf2302ac4)", anteriormente en esta sección para obtener y distribuir listas de revocaciones de Microsoft que incluyan el certificado emisor de licencias de servidor revocado de un servidor de certificación raíz.

Cuando establezca los servicios en línea en el servidor de certificación raíz, puede especificar una clave pública con la autoridad necesaria para revocar el certificado emisor de licencias de servidor del clúster de certificación raíz. Esta clave pública puede pertenecer a la organización o a una entidad tercera. Una lista de revocaciones firmada con la clave privada correspondiente puede revocar el certificado emisor de licencias de servidor.

Para revocar el certificado emisor de licencias de servidor del servidor de certificación raíz, puede crear una lista de revocaciones que especifique dicho certificado, firmarla con la clave privada de la organización o de una entidad tercera y después distribuir la lista de revocaciones a todos los usuarios. Para obtener instrucciones, vea “Implementación de listas de revocaciones de la organización” en [Implementación de listas de revocaciones](https://technet.microsoft.com/e331338b-66d4-45e4-8d3f-acccf2302ac4), anteriormente en este tema.

Puede revocar un certificado emisor de licencias de servidor en una lista de revocaciones utilizando los siguientes parámetros:

-   **GUID**. Se puede revocar un certificado emisor de licencias de servidor utilizando su identificador único global (GUID). Para obtener información acerca del uso de este parámetro en una lista de revocaciones, vea "Revocación de certificados y licencias basándose en el GUID" en "[Creación de listas de revocaciones](https://technet.microsoft.com/1ef75199-3344-4225-84de-a863a777696a)", anteriormente en este tema.
-   **Valor del algoritmo hash**. Se puede revocar un certificado emisor de licencias de servidor basándose en un algoritmo hash SHA-1 de los caracteres Unicode que se encuentran en el cuerpo del certificado. Para obtener información acerca del uso de este parámetro en una lista de revocaciones, vea "Revocación de certificados y licencias basándose en el valor de un algoritmo hash" en "[Creación de listas de revocaciones](https://technet.microsoft.com/1ef75199-3344-4225-84de-a863a777696a)", anteriormente en este tema.

Para obtener el certificado emisor de licencias de servidor de una instalación de RMS, debe realizar una consulta en la base de datos de configuración de RMS. Los siguientes pasos explican cómo obtener esta información de una base de datos de configuración de SQL y guardarla en un archivo que pueda leerse fácilmente utilizando un explorador.

1.  Abra el Analizador de consultas de SQL y conéctese a la base de datos de configuración del servidor de certificación raíz.
2.  En el menú **Consulta**, haga clic en **Resultados como texto**.
3.  En el menú **Herramientas**, haga clic en **Opciones** para abrir el cuadro de diálogo **Opciones**. Haga clic en la ficha **Resultados** y después establezca **Número máximo de caracteres por columna8192**.
        ```
1.  Copie los resultados de la ventana **Resultados** y péguelos en un editor de texto, como el Bloc de notas. Guarde los resultados en un archivo con la extensión .xml.

Para obtener más información acerca de cómo utilizar esta información en una lista de revocaciones, vea “[Creación de listas de revocaciones](https://technet.microsoft.com/1ef75199-3344-4225-84de-a863a777696a)”, anteriormente en este tema.

Una vez que la información del certificado emisor de licencias de servidor esté guardada como archivo XML, puede extraer la clave pública de él como se indica a continuación:

1.  Abra el archivo XML del certificado emisor de licencias de servidor en un editor de archivos de texto o XML.
2.  En la sección &lt;ISSUEDPRINCIPALS&gt;, copie el elemento &lt;PUBLICKEY&gt;.
3.  Guarde esta información en un archivo que pueda presentar ante el tribunal o colocar en una lista de revocaciones de la organización.

Una vez que se haya revocado el certificado emisor de licencias de servidor del clúster de certificación raíz, todos los certificados y licencias emitidos por la instalación de RMS quedarán invalidados para el contenido que requiera una lista de revocaciones y dicho contenido será inaccesible. Este proceso no se ve afectado por el tipo de licencia que el usuario posea. Para conservar el contenido publicado por el servidor cuya licencia se va a revocar, debe tomar alguna de las siguientes medidas antes de implementar la lista de revocaciones:

-   Guarde el contenido sin protección de RMS.
-   Vuelva a publicar el contenido sin el requisito de una lista de revocaciones.

En ambos escenarios (revocación por Microsoft o por una entidad tercera) la lista de revocaciones surte efecto para todas las solicitudes de vínculo, puesto que se firmó con la clave privada de una entidad principal en la cadena de confianza de la licencia de uso. Por tanto, no se aceptará ninguna de las solicitudes de enlace que utilicen licencias emitidas por la instalación de RMS utilizando el certificado emisor de licencias de servidor revocado.

> [!NOTE]
> Microsoft sólo revocará un certificado emisor de licencias de servidor cuando un tribunal así se lo ordene. 
