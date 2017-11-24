---
TOCTitle: Planeamiento de usuarios externos de RMS
Title: Planeamiento de usuarios externos de RMS
ms:assetid: '107e1338-4dcf-4ed5-a49d-e875cc883db1'
ms:contentKeyID: 18127691
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720190(v=WS.10)'
---

Planeamiento de usuarios externos de RMS
========================================

En esta sección se describen las topologías que puede implementar para permitir a su organización y a los usuarios externos compartir contenido protegido con RMS por Internet.

Puede implementar clústeres de RMS para uso tanto interno como externo mediante una de las opciones siguientes:

-   Establecer una URL del clúster de certificación raíz a una URL accesible desde Internet. Asegúrese de que esta dirección URL se resuelve en la intranet para servidores de RMS del mismo clúster. Al hacerlo, la dirección URL de licencias de publicación que utilizan los equipos de usuarios finales para la adquisición de licencias funciona en la intranet y en Internet.
-   Configure un clúster diferente de RMS específicamente para la publicación en Internet. Cualquier contenido que deba obtener una licencia de Internet debe publicarse en este clúster. Si el contenido debe estar disponible interna y externamente, debe publicarse en ambas ubicaciones. De forma alternativa, los usuarios deben poder ponerse en contacto con el servidor de Internet.

Permitir usuarios externos
--------------------------

Puede incluir usuarios externos en la instalación de RMS si crea cuentas internas para esos usuarios y permite que obtengan acceso a su red corporativa a través de una red privada virtual (VPN). La cuenta puede tener un buzón interno o una dirección de correo electrónico que apunta a un buzón externo.

Si utiliza un buzón interno, los autores internos deben especificar la dirección de correo electrónico asociada con ese buzón interno (en lugar de una dirección de correo electrónico que el usuario externo tenga fuera de la organización) cuando publican contenido protegido con RMS. Si utiliza un buzón externo, los autores internos deben tener cuidado de especificar la dirección de correo electrónico externa de la cuenta cuando publican contenido protegido con RMS.

Para proporcionar seguridad de red y permitir el acceso a la red de usuarios externos, puede crear un bosque de Active Directory separado para las cuentas de asociados. Con esta topología, puede crear un clúster de certificación raíz separado para la parte de Internet del sistema Windows RMS. Esto permite a los usuarios externos recibir certificados de equipo de RMS y certificados de cuenta de permisos desde este clúster de certificación para Internet la primera vez que obtienen acceso al contenido protegido con RMS.

Si decide implementar un bosque separado para socios externos que contendrá las cuentas de asociados, RMS debe estar instalado en ese bosque. En ese caso puede utilizar la característica de dominio de publicación de confianza de RMS para establecer confianza entre los dos servidores de RMS. También necesita tener los registros DNS externos para identificar la URL de clúster externo de la instalación de RMS en el bosque creado para los socios externos. Crear esta relación de confianza permitirá al servidor de RMS externo conceder licencias de uso para todo el contenido publicado por el sistema interno de RMS y viceversa.

Como alternativa a la configuración de un servidor de RMS en el bosque externo, se puede utilizar un servidor, como ISA, para filtrar el tráfico de entrada y utilizar un proxy inverso para redirigir las solicitudes de licencias de RMS al servidor interno de RMS.

Uso de certificados externos
----------------------------

Se puede permitir a usuarios externos tener acceso a contenido protegido con RMS si se configura un servidor separado de RMS como servidor de licencias para Internet, se publica el contenido desde ese servidor de licencias y después se especifican las relaciones de confianza en ese servidor.

La parte de Internet de la implementación de RMS es un servidor de licencias separado que está dedicado al uso en Internet. Forma parte del mismo clúster que la instalación de licencias interna y utiliza la misma base de datos y la misma dirección URL que la instalación de licencias interna; es el único servidor que puede aceptar tráfico de Internet entrante.

Cuando los usuarios externos soliciten una licencia de uso de este servidor de licencias de RMS, utilizarán un certificado de cuenta de permisos de otro servicio de certificación de RMS que sea de confianza de este servidor de licencias.

#### Confianza en certificados de cuenta de permisos basados en Passport

Una organización puede elegir confiar en certificados de cuenta de permisos basados en las credenciales de Microsoft .NET Passport. Estos certificados de cuenta requieren que los usuarios obtengan certificados de cuenta de permisos directamente del servicio de certificación de Microsoft ubicado en Internet.

En este modelo, los usuarios externos reciben certificados de equipo de RMS y certificados de cuenta de permisos de Microsoft. Cuando se publica el contenido, la cuenta de Microsoft .NET Passport del usuario externo debe recibir el nombre del destinatario de la licencia de publicación.

La cuenta de Microsoft® .NET Passport debe coincidir con la cuenta de .NET Passport que se utilizó cuando el usuario descargó el certificado de cuenta de permisos de Microsoft. El autor debe especificar esta cuenta cuando agregue destinatarios a la aplicación compatible con RMS. Si las cuentas no coinciden, el contenido no se puede utilizar.

#### Confianza en otros certificados externos

Si la compañía del usuario externo también tiene una implementación de RMS, puede decidir establecer una relación de confianza con esa compañía. Para ello, pídale a la compañía que exporte su certificado emisor de licencias de servidor de RMS y se lo envíe. A continuación, puede importar el certificado utilizando la consola de administración de RMS para el servidor de licencias para Internet.