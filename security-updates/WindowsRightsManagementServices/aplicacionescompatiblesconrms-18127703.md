---
TOCTitle: Aplicaciones compatibles con RMS
Title: Aplicaciones compatibles con RMS
ms:assetid: '30bb5565-81d3-43d9-a64d-cf0c5b990712'
ms:contentKeyID: 18127703
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720231(v=WS.10)'
---

Aplicaciones compatibles con RMS
================================

Para crear o utilizar contenido protegido con RMS, los usuarios deben tener instalada una aplicación compatible con RMS, como se explica en este tema. Asimismo, el cliente de RMS debe estar instalado y los equipos que utilicen deben estar activados. Para obtener más información, vea "[Cliente de RMS](https://technet.microsoft.com/03294fa2-8350-430d-b4b0-03d5169937c2)" y "[Activación de equipo RMS](https://technet.microsoft.com/09a0d631-9860-477f-9d10-df61b3bfe125)", más adelante en este tema.

Las aplicaciones compatibles con RMS permiten a los autores de contenido adjuntar permisos de uso, en forma de licencias de publicación, a los archivos que crean para controlar el modo en que se utiliza el contenido. Las aplicaciones compatibles con RMS también procesan la información del archivo cifrado y permiten a los usuarios utilizar el contenido según los permisos que se hayan definido en la licencia de publicación.

Con el SDK del cliente de los Servicios de Rights Management, los desarrolladores pueden crear aplicaciones compatibles con RMS capaces de otorgar licencias, y publicar y utilizar contenido protegido con RMS. Las aplicaciones compatibles con RMS pueden desarrollarse para equipos que ejecuten Microsoft® Windows® 98 Second Edition o versiones posteriores del sistema operativo.

Los desarrolladores también pueden crear aplicaciones de servidor compatibles con RMS mediante el SDK del cliente de los Servicios de Rights Management. Estas aplicaciones podrán publicar, pero no utilizar, contenido.

Los usuarios que no tengan otra aplicación compatible con RMS para utilizar contenido protegido de correo electrónico y páginas Web pueden obtener el Complemento Rights Management para Microsoft® Internet Explorer. Por ejemplo, los clientes de Outlook Web Access (OWA) pueden usar este complemento para utilizar mensajes de correo electrónico protegidos con RMS.

El Complemento Rights Management para Internet Explorer se puede descargar del [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=14450) (http://go.microsoft.com/fwlink/?LinkId=14450).

> [!NOTE]
> Si va a utilizar el Complemento Rights Management para Internet Explorer con Windows XP Service Pack 2, la configuración de seguridad mejorada puede generar algunos problemas de compatibilidad con las aplicaciones. 

Si la dirección URL de la conexión extranet de todos los dominios de la compañía no se agrega a los sitios de Intranet local en Internet Explorer, los usuarios que utilicen el Complemento Rights Management para Internet Explorer recibirán mensajes repetidas veces preguntando si están seguros de querer conectarse a los sitios. En caso de responder incorrectamente a estos mensajes, puede suceder que el cliente de RMS obtenga un nuevo certificado de cuenta de permisos para la cuenta de usuario.

Para establecer estos sitios correctamente en una compañía, utilice una secuencia de comandos para escribir las direcciones URL necesarias en el Registro como parte de la zona de Intranet local. De forma predeterminada, la zona de Intranet local proporciona un nivel de seguridad suficientemente alto para eliminar los mensajes.
