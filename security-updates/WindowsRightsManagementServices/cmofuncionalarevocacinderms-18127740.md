---
TOCTitle: Cómo funciona la revocación de RMS
Title: Cómo funciona la revocación de RMS
ms:assetid: '469e3938-a59b-4c92-9779-ead64e724d00'
ms:contentKeyID: 18127740
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720263(v=WS.10)'
---

Cómo funciona la revocación de RMS
==================================

La revocación funciona impidiendo el vínculo, es decir, el proceso que permite a los usuarios utilizar contenido, cuando una entidad revocada participa en la solicitud de vínculo. La revocación se implementa mediante listas que se distribuyen a los equipos cliente. Estas listas son archivos XrML firmados que especifican el contenido, las aplicaciones, los usuarios u otras entidades principales revocadas por la entidad principal que emite la lista.

Siempre que un usuario intenta utilizar contenido protegido, la aplicación compatible con RMS asociada envía una solicitud para obtener el permiso adecuado, incluida en una solicitud de vínculo, al cliente de RMS. Por ejemplo, si el usuario intenta abrir un archivo, la aplicación solicita un permiso de visualización que permita abrir el archivo. Si el usuario intenta modificar el archivo, la aplicación solicita un permiso de edición.

Mientras procesa la solicitud de vínculo, el cliente de RMS realiza estos procesos:

1.  Evalúa la licencia de uso para ver si existen requisitos de alguna lista de revocaciones.
2.  Si la licencia de uso requiere revocación, el componente cliente comprueba si la lista de revocaciones está presente, registrada y actualizada según el intervalo de actualización especificado en la licencia de uso.
3.  Comprueba que la entidad principal que firmó la lista de revocaciones está especificado en la licencia de uso como una entidad principal autorizada para revocar la licencia.
4.  Si estas comprobaciones son satisfactorias, el componente cliente determina si se ha revocado alguna de las entidades principales involucradas en la solicitud de vínculo original. Si es así, deniega la solicitud de vínculo.

El administrador puede distribuir las listas de revocaciones a los equipos cliente, o se pueden descargar al equipo mediante una aplicación compatible con RMS cuando lo requiera una licencia de uso. Cuando se usa una lista de revocaciones para enlazar un fragmento de contenido, se registra y se puede utilizar para enlazar solicitudes con otras licencias de uso, siempre y cuando la aplicación permanezca abierta. Una vez que se cierra la aplicación, se elimina el registro de la lista.

En el diagrama siguiente, se muestra el proceso de vínculo y cómo funciona la revocación en dicho proceso.

![](images/Cc720263.81aa2d70-d261-49ad-b446-96a2eddba1a5(WS.10).gif)

La revocación es opcional. El administrador de RMS puede requerir una revocación especificándola en una o varias de las plantillas de directiva de permisos de la compañía. Cuando se requiere la revocación, las licencias no pueden enlazarse a no ser que la lista de revocaciones necesaria esté presente, registrada en el equipo del usuario, y no sea más antigua que el intervalo de actualización especificado en la licencia de uso.

Sin embargo, es importante tener en cuenta que la revocación puede aún estar en vigor para una licencia de uso dada, incluso cuando la licencia de uso no lo requiera. La revocación entra en vigor siempre que cualquier emisor de cualquier certificado de la cadena de confianza involucrada en la solicitud de vínculo haya emitido una lista de revocaciones que esté registrada en un equipo cliente. En este caso, la lista de revocaciones se usa para procesar las solicitudes de vínculo, aunque las licencias de uso participantes no requieran revocación. Esto es así hasta que se cierra la aplicación compatible con RMS, momento en que se elimina el registro de la lista de revocaciones.

Por ejemplo, si un usuario intenta utilizar un fragmento de contenido cuya licencia de uso, emitida por la entidad A, requiera una lista de revocaciones emitida por la entidad A, la aplicación compatible con RMS obtiene la lista de revocaciones de la dirección URL especificada en la licencia de uso y, a continuación, la registra. Al procesar la solicitud de vínculo, el cliente de RMS comprueba la lista de revocaciones para ver si existe alguna revocación.

El usuario deja abierta la aplicación compatible con RMS e intenta utilizar un segundo fragmento de contenido cuya licencia de uso fue emitida también por la entidad A. Aunque esta licencia de uso no incluye una condición de revocación, la lista de revocaciones de la entidad A está actualmente registrada en el equipo del usuario. En esta situación, el componente cliente examina la lista de revocaciones antes de procesar la solicitud de vínculo.

Posteriormente, el usuario intenta utilizar un fragmento de contenido cuya licencia de uso fue emitida por la entidad C. La licencia de uso no incluye una condición de revocación. Puesto que la única lista de revocaciones registrada en el equipo cliente es la emitida por la entidad A, y esta entidad no está en la cadena de confianza de la licencia de uso, ninguna revocación entra en vigor para el vínculo.

Finalmente, el usuario cierra la aplicación compatible con RMS y, a continuación, abre el segundo fragmento de contenido que no incluía una condición de revocación. Puesto que se eliminó el registro de la lista de revocaciones emitida por la entidad A al cerrar la aplicación, el cliente de RMS no la examina para procesar la solicitud de vínculo.
