---
TOCTitle: Determinación de los requisitos de acceso
Title: Determinación de los requisitos de acceso
ms:assetid: 'eb2ce9a5-0430-4811-bd40-4a94a84426a8'
ms:contentKeyID: 18128016
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747790(v=WS.10)'
---

Determinación de los requisitos de acceso
=========================================

Durante esta parte de la fase de planeamiento, debe haber identificado el ámbito de la implementación de RMS. Al evaluar la seguridad de su sistema RMS, debería plantear métodos con los que pueda limitar el ámbito de los usuarios y asegurarse de que los datos que están protegiendo con RMS también están protegidos utilizando procedimientos de seguridad de la información recomendados tradicionalmente. También debería asegurarse de que el acceso al servidor de RMS para la administración y configuración esté restringido a sólo administradores de confianza. Los métodos de seguridad en el acceso que puede utilizar con RMS incluyen los siguientes:

-   **Listas de control de acceso (ACL)**. Los servicios Web de RMS y el sitio Web de administración pueden protegerse mediante ACL. Para asegurarse de que sólo los usuarios autorizados utilicen el servicio RMS puede utilizar listas de control de acceso para restringir la posibilidad de que los usuarios se conecten a los servicios de certificación y licencia de RMS. Esto puede resultar útil si sólo desea que ciertos grupos puedan crear contenido protegido o si desea permitir que sólo ciertos grupos obtengan licencias para contenido protegido.

-   **Autenticación del cliente**. También puede hacer que se pidan tarjetas inteligentes u otros tipos de autenticación del cliente cuando un usuario intente adquirir una licencia o un certificado de uso. Esto puede ayudar a mitigar el potencial de un usuario no autorizado a abrir contenido utilizando una sesión de usuario autorizado.

-   **Capa de sockets seguros**. Para proporcionar una capa de protección adicional, también puede requerir una conexión SSL entre los clientes de RMS y el servidor de RMS. Es recomendable que habilite SSL y que requiera el cifrado de 128 bits en cada uno de los archivos de los servicios Web de RMS. Estos archivos tienen la extensión de nombre de archivo .asmx y se encuentran en los directorios virtuales Licensing, Certification y Admin. Si desea abrir las páginas Web de **administración de RMS** desde un explorador instalado en un equipo remoto, debe habilitar SSL. Sin embargo, incluso con SSL habilitada, no puede abrir la página **Administración global** desde un equipo remoto.

    Para obtener más información sobre la configuración de SSL en servidores, vea la Ayuda de IIS.

En algunas organizaciones se requiere un sistema de licencias departamental que esté aislado de los otros departamentos y protegido. En un caso así se puede utilizar un servidor de RMS para proporcionar una forma de establecer directivas de administración de derechos de información. Si tiene un departamento o bien otra rama de la organización que controla contenidos extremadamente confidenciales, considere la configuración de un servidor de licencias o clúster de licencias separado para administrar las licencias y la publicación del contenido de forma separada del resto de la organización. Un servidor de licencias está subinscrito con el servidor (o clúster) de certificación raíz, que proporciona certificación y otros servicios para cada servidor de licencias. No obstante, los servidores de licencias proporcionan sus propios servicios de publicación y emisión de licencias.

Las cuentas de usuario, las ACL y la seguridad física son elementos críticos de la implementación. Antes de implementar RMS en un entorno de producción, asegúrese de evaluar e implementar los procedimientos y el modelo de seguridad, según sea necesario.
