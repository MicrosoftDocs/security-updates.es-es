---
TOCTitle: Alternativas al retiro de RMS
Title: Alternativas al retiro de RMS
ms:assetid: '4d32f35e-997d-4d10-ab66-efe217e853f7'
ms:contentKeyID: 18127748
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720268(v=WS.10)'
---

Alternativas al retiro de RMS
=============================

Si todavía tiene previsto utilizar RMS en su organización, pero por alguna razón necesita dejar de utilizar ciertos servidores de RMS, considere el uso de las siguientes alternativas al retiro.

**Configuración de un dominio de publicación de confianza**

Toda la información protegida con RMS está cifrada con la clave privada del servidor de RMS. Un dominio de publicación de confianza permite importar la clave privada de un servidor de RMS a otro servidor de RMS. Esto permite que un servidor de RMS emita licencias de uso utilizando licencias de publicación que hayan sido emitidas por otro servidor de RMS. Una vez exportada la clave, puede anularse y desinstalarse el servidor.

**Configuración de un grupo de superusuarios**

Si no puede abrirse el contenido protegido con RMS porque ningún usuario tiene derechos para el contenido, puede concederle al grupo de superusuarios control total sobre todo el contenido protegido con RMS que se publica en ese servidor. Se conceden permisos de propiedad completos a los miembros del grupo de superusuarios en todas las licencias de uso emitidas por el servidor o clúster de RMS donde esté configurado el grupo de superusuarios. Esto quiere decir que los miembros de este grupo pueden descifrar todos los archivos de contenido protegido y quitar esta protección. Por ejemplo, un miembro de este grupo puede quitar la protección de archivos que un antiguo empleado haya publicado, de forma que el nuevo propietario pueda publicarlos y administrarlos.

El grupo de superusuarios no incluye automáticamente ningún miembro, ni siquiera administradores. Este grupo debe existir dentro de Active Directory como grupo de distribución con un atributo de dirección de correo electrónico del mismo valor que el nombre del grupo, con el formato "*nombre\_grupo*@*nombre\_dominio*.com." El nombre de grupo debe coincidir exactamente con el atributo de dirección de correo electrónico, y distinguir entre mayúsculas y minúsculas.
