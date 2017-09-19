---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Acceso interno y externo'
Title: 'Preguntas más frecuentes acerca de RMS: Acceso interno y externo'
ms:assetid: '59c2c51f-6c20-450c-a334-0e1486292074'
ms:contentKeyID: 18127824
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747577(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Acceso interno y externo
================================================================

Preguntas más frecuentes acerca del acceso interno y externo a RMS
------------------------------------------------------------------

-   [¿Qué cambios debo realizar para que el cortafuegos permita que clientes de RMS que se hallan fuera del cortafuegos tengan acceso a servidores de RMS?](#bkmk_37)
-   [¿Cómo funciona el entorno de la extranet?](#bkmk_38)
-   [Si un usuario crea contenido protegido por derechos y se lo da a alguien que no tiene acceso a la instalación de RMS, ¿puede el destinatario usar el contenido?](#bkmk_39)
-   [Si uso Outlook 2003 u Outlook 2007 para enviar un mensaje de correo electrónico protegido por derechos a uno de mis clientes, ¿qué necesita para leer el mensaje?](#bkmk_40)
-   [Si las organizaciones tienen sus propios servidores de RMS, ¿cómo pueden intercambiar contenido protegido por derechos?](#bkmk_41)
-   [Al enviar un mensaje de correo electrónico que se ha protegido con RMS a una organización externa que no es compatible con Outlook, ¿puede el destinatario responder a un mensaje de correo electrónico leído con el Complemento Right Management con Internet Explorer?](#bkmk_42)

<span id="BKMK_37"></span>
#### ¿Qué cambios debo realizar para que el cortafuegos permita que clientes de RMS que se hallan fuera del cortafuegos tengan acceso a servidores de RMS?

El cortafuegos tiene que permitir que los equipos externos realicen solicitudes del protocolo simple de acceso a objetos (SOAP) al servidor de RMS a través de HTTP (puerto TCP 80) o de HTTPS (puerto TCP 443).

<span id="BKMK_38"></span>
#### ¿Cómo funciona el entorno de la extranet?

Hay dos direcciones URL en la licencia de publicación vinculada al contenido. Una es la dirección URL de la intranet establecida cuando se establecen los servicios en línea del clúster de RMS. La segunda es la URL de la extranet que puede establecer el administrador de RMS. Esta URL de extranet permite al cliente obtener licencias de uso fuera del cortafuegos. La dirección URL de la extranet no se puede usar para crear nuevo contenido protegido por derechos. En ese caso, se requiere una anulación del registro de cliente de RMS.

<span id="BKMK_39"></span>
#### Si un usuario crea contenido protegido por derechos y se lo da a alguien que no tiene acceso a la instalación de RMS, ¿puede el destinatario usar el contenido?

Si el usuario no tiene una conexión a la instalación de RMS la primera vez que se abre el contenido protegido, el usuario no puede usar el contenido.

Tenga en cuenta que Office 2003 y posterior obtiene automáticamente licencias de uso para correo electrónico protegido por derechos cuando se sincroniza, de modo que puede leerse el correo electrónico sin conexión de red. Sin embargo, mientras que Outlook 2003 y posterior almacena en caché automáticamente las licencias de uso para un mensaje de correo electrónico, todo documento de Excel 2007, Excel 2003, Word 2007, Word 2003, PowerPoint 2007 y PowerPoint 2003 adjunto al mensaje tendrá los mismos derechos asignados que el mensaje de correo electrónico que los adjunta. No se sincronizan automáticamente cuando se descarga el mensaje de correo electrónico, y hay que abrirlos individualmente cuando se conecta el equipo a la red para obtener una licencia de uso.

<span id="BKMK_40"></span>
#### Si uso Outlook 2003 u Outlook 2007 para enviar un mensaje de correo electrónico protegido a uno de mis clientes, ¿qué necesita para leer el mensaje?

El destinatario necesita usar Outlook 2003, Outlook 2007 o el Complemento Rights Management con Internet Explorer. Si la organización del destinatario ha establecido una relación de confianza entre la instalación de RMS de la organización y la suya, el destinatario puede leer el correo electrónico sin realizar más pasos. La relación de confianza se establece intercambiando certificados emisores de licencias de servidor de RMS, que contienen sus respectivas claves públicas.

Si la organización del destinatario no tiene una infraestructura de RMS o no se ha establecido una relación de confianza, puede pedirle a su cliente que establezca un Windows Live ID y enviar el mensaje de correo electrónico al destinatario especificando los derechos asignados a las credenciales del Windows Live ID del cliente. Este método utiliza el servicio IRM de Microsoft disponible en Internet para obtener una licencia de uso. El servicio IRM está disponible de forma gratuita, así que permite que la gente utilice IRM como prueba y se utilice sólo para probar RMS. Si decide proteger el contenido mediante este servicio, tenga en cuenta que puede quedar suspendido sin aviso previo en el futuro.

<span id="BKMK_41"></span>
#### Si las organizaciones tienen sus propios servidores de RMS, ¿cómo pueden intercambiar contenido protegido por derechos?

RMS utiliza dominios de usuarios de confianza, por medio de los cuales los certificados de usuario generados por una instalación de RMS se consideran de confianza para otra.

<span id="BKMK_42"></span>
#### Al enviar un mensaje de correo electrónico que se ha protegido con RMS a una organización externa que no es compatible con Outlook, ¿puede el destinatario responder a un mensaje de correo electrónico leído con el Complemento Right Management con Internet Explorer?

El destinatario del mensaje puede responder a un mensaje protegido por derechos como lo haría con cualquier mensaje, pero el cuerpo original del mensaje recibido seguirá protegido por derechos para sus destinatarios originales. Cómo se empaqueta ese mensaje dependerá de la aplicación cliente. El mensaje original puede adjuntarse a la respuesta como datos adjuntos cifrados o puede eliminarse, como hace Outlook 2003 u Outlook 2007, por ejemplo.
