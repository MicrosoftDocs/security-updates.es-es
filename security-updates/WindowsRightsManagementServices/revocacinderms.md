---
TOCTitle: Revocación de RMS
Title: Revocación de RMS
ms:assetid: '72689f90-f3c5-4b61-94ea-d825f3199b3b'
ms:contentKeyID: 18127808
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747622(v=WS.10)'
---

Revocación de RMS
=================

La revocación es un mecanismo que cancela una credencial, como un certificado o licencia, que ya se había emitido. La finalidad primordial de la revocación es evitar que entidades que ya no se consideran de confianza participen en un sistema RMS. La revocación se puede aplicar, por ejemplo, en los casos siguientes:

-   Para evitar que se utilice contenido cuando una entidad principal o una identidad de la cadena de confianza se encuentra en una situación comprometida, como cuando un individuo deja la organización y deja por tanto de poder ver el contenido protegido con RMS.

-   Para evitar que una aplicación compatible con RMS determinada abra un fragmento de contenido si dicha aplicación ya no se considera de confianza.

-   Para evitar que se utilice un fragmento de contenido censurable que ya se ha distribuido y para el que ya se ha emitido la licencia de uso.

La revocación funciona en el cliente y evita que los usuarios utilicen un fragmento de contenido, aunque se haya emitido ya una licencia de uso. Cuando se habilita, la revocación está vigente siempre que un usuario intenta utilizar el contenido protegido, tanto si dicho usuario tiene una copia de la licencia de uso almacenada localmente como si solicita una nueva licencia de uso del servidor de RMS en el momento en que intenta utilizarlo.

En esta sección, se proporciona información general sobre la revocación. Para obtener información acerca de cómo utilizar la revocación con RMS, vea "Administración de revocaciones" en "Operación de un servidor de RMS", en esta recopilación de documentación.

Se tratan los siguientes temas:

-   [Cómo funciona la revocación de RMS](https://technet.microsoft.com/469e3938-a59b-4c92-9779-ead64e724d00)
-   [Listas de revocaciones de RMS](https://technet.microsoft.com/688d4dfa-c928-4b2f-8116-2f9e87d2b6f7)
-   [Revocación en plantillas de directiva de permisos](https://technet.microsoft.com/287c5b92-fcb5-4295-9c2b-4e37e643beb2)
-   [Revocación y autores desconectados](https://technet.microsoft.com/a9cf0541-9101-4e90-9c56-7c1b9a8deca6)