---
TOCTitle: Publicación en línea
Title: Publicación en línea
ms:assetid: '962c4e83-cf34-4c61-9589-31d24b0299fb'
ms:contentKeyID: 18127880
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747694(v=WS.10)'
---

Publicación en línea
====================

En el diagrama siguiente, se explica el proceso de publicación en línea.

![](images/Cc747694.897e47b6-fffe-4b11-bc9f-be58539b9f19(WS.10).gif)

El proceso de publicación en línea implica los siguientes pasos:

1.  El autor del contenido crea un documento y usa la aplicación compatible con RMS para especificar los usuarios y aplicar permisos y condiciones al contenido.
2.  La aplicación compatible con RMS genera una clave de contenido simétrica y solicita una licencia de publicación al servidor de certificación o al servidor de licencias. La solicitud incluye la clave del contenido y la configuración de uso.
3.  El servidor de licencias genera la licencia de publicación, cifra la clave de contenido con la clave pública del servidor y, a continuación, devuelve la licencia de publicación a la aplicación compatible con RMS.
4.  La aplicación cifra el archivo con la clave de contenido y enlaza la licencia de publicación con el archivo.
5.  La aplicación compatible con RMS del equipo del usuario del contenido envía una solicitud, que incluye el certificado de cuenta de permisos del usuario, al servidor de RMS (que emitió la licencia de publicación) para solicitar una licencia de uso del documento.
6.  El servidor de RMS comprueba las credenciales del usuario. Si el usuario se valida correctamente, se genera una licencia de uso y se devuelve a la aplicación compatible con RMS del equipo del usuario del contenido.
7.  La aplicación compatible con RMS abre el documento y otorga los permisos de usuario según los parámetros definidos en la licencia de uso.
