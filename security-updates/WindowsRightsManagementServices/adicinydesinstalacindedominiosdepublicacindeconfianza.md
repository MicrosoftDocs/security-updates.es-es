---
TOCTitle: Adición y desinstalación de dominios de publicación de confianza
Title: Adición y desinstalación de dominios de publicación de confianza
ms:assetid: 'd87b502d-5497-4ccd-badf-f6807d587cee'
ms:contentKeyID: 18127973
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747687(v=WS.10)'
---

Adición y desinstalación de dominios de publicación de confianza
================================================================

De forma predeterminada, un servidor de RMS puede emitir licencias de uso únicamente utilizando las licencias de publicación que dicho servidor, u otro servidor del clúster, haya emitido. Si dispone de contenido que otro servidor de certificación raíz ha publicado en la organización, por ejemplo una organización subsidiaria de otro bosque, o en otra organización independiente, el servidor de RMS puede conceder licencias de usuario para este contenido si se configura un dominio de publicación de confianza en el servidor de RMS. Al agregar un dominio de publicación de confianza se configura una relación de confianza entre el servidor de RMS y el otro servidor de certificación raíz mediante la importación del certificado emisor de licencias de servidor del otro servidor. No existe un límite para el número de dominios de publicación de confianza que se pueden configurar para el servidor.

Puede quitar un dominio de publicación de confianza que haya agregado en cualquier momento quitando su certificado de la lista de certificados para dominios de publicación de confianza.

Para agregar un dominio de publicación de confianza, debe importar el certificado emisor de licencias de servidor, la clave privada (si se almacena en un módulo de seguridad de software, en lugar de hardware) y todas las plantillas de directiva de permisos para el servidor o clúster de RMS que desee agregar. En primer lugar, el administrador debe exportar estos elementos del servidor o clúster en el que desee confiar a un archivo protegido con contraseña y, a continuación, especificar la contraseña necesaria para descifrarlo. El administrador debe colocar el archivo en una carpeta compartida e informarle de la contraseña. A continuación, puede importar el archivo especificando su ubicación y contraseña. Para guardarlo, la cuenta que esté ejecutando el grupo de aplicaciones **Admin** debe poseer permisos para la carpeta compartida.

Para obtener instrucciones paso a paso sobre cómo establecer un dominio de publicación de confianza, vea “[Para agregar un dominio de publicación de confianza](https://technet.microsoft.com/731416d8-ddf4-4d4a-9f1a-bbd1ea48fe3c)”, más adelante en este tema

Si la clave privada se almacena en un módulo de seguridad de hardware, debe transferirla al módulo de seguridad de hardware que se encuentre en el servidor de confianza de acuerdo con las instrucciones de la documentación del módulo. Dependiendo del tipo de módulo de seguridad de hardware que exista en cada servidor y de su configuración, es posible que no pueda transferir la clave privada de un módulo a otro. Consulte la documentación del módulo de seguridad de hardware para determinar si puede transferir la clave privada sin perder los datos presentes en el módulo de seguridad de hardware de destino. Si esto no es posible, no podrá establecer un dominio de publicación de confianza entre ambos servidores.

> [!NOTE]
> Si utiliza un módulo de seguridad de hardware para proteger la clave privada de RMS y desea importar un certificado emisor de licencias de servidor desde una instalación de RMS que utilice protección de clave privada de software, debe especificar una contraseña para la clave privada en la página Configuración de seguridad de cada servidor de RMS del clúster antes de intentar importar el certificado. 
