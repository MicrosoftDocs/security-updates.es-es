---
TOCTitle: Inscripción del cliente de RMS
Title: Inscripción del cliente de RMS
ms:assetid: '9c1d07bf-7235-4694-8291-ac2e5b221f4a'
ms:contentKeyID: 18127892
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747613(v=WS.10)'
---

Inscripción del cliente de RMS
==============================

Los equipos cliente pueden inscribirse con el servicio de publicación de RMS para recibir un certificado emisor de licencias de cliente de RMS, que permite a los autores publicar contenido protegido con RMS cuando sus equipos no están conectados a la red corporativa. En este caso, es el equipo cliente, en lugar del servicio de publicación, el que firma y emite las licencias de publicación que contienen la información sobre los permisos de uso del contenido protegido con RMS publicado desde dicho equipo.

El servicio de publicación de RMS emite certificados emisores de licencias de cliente.

La inscripción de clientes implica los pasos siguientes:

1.  El equipo cliente envía el certificado de cuenta de permisos del usuario en una solicitud de inscripción al servicio de publicación que se ejecuta en el servidor o clúster de certificación raíz, o en un servidor o clúster de licencias.
2.  El servidor comprueba que se permite la inscripción de clientes en función de la configuración del administrador de la red, y que el certificado de cuenta de permisos no se encuentra en una lista de exclusión almacenada en la base de datos de configuración. Para obtener más información acerca de cómo crear listas de exclusión, vea "Administración de directivas de exclusión" en "Operación de un servidor de RMS", en esta recopilación de documentación.
3.  El servicio de publicación crea un par de claves para el equipo cliente y un certificado emisor de licencias de cliente, e incluye la clave pública en el certificado. Después, cifra la clave privada con la clave pública del certificado de cuenta de permisos y, a continuación, la incluye en el certificado.
4.  El servicio de publicación emite un certificado emisor de licencias de cliente para el equipo cliente.
