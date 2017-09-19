---
TOCTitle: Uso del grupo de superusuarios
Title: Uso del grupo de superusuarios
ms:assetid: '0febcb3e-7124-4e51-971a-1013b928d33b'
ms:contentKeyID: 18127728
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720198(v=WS.10)'
---

Uso del grupo de superusuarios
==============================

Durante el establecimiento de los servicios en línea, RMS crea un grupo especial de superusuarios que posee control total sobre todo el contenido protegido con permisos. Se conceden permisos de propiedad completos a los miembros del grupo de superusuarios en todas las licencias de uso emitidas por el servidor o clúster de RMS donde esté configurado el grupo de superusuarios. Esto quiere decir que los miembros de este grupo pueden descifrar todos los archivos de contenido protegido y quitar esta protección. Por ejemplo, un miembro de este grupo puede quitar la protección de archivos que un antiguo empleado haya publicado, de forma que el nuevo propietario pueda publicarlos y administrarlos.

De manera predeterminada, el grupo de superusuarios no contiene ningún miembro, ni siquiera administradores. En el sitio Web de administración, puede especificar un grupo de seguridad de Active Directory para utilizarlo como grupo de superusuarios para RMS. Puede utilizar un grupo de Active Directory existente o crear uno nuevo para este fin. El grupo debe existir en el mismo bosque de Active Directory que la instalación de RMS. A todas las cuentas de usuario que formen parte del grupo que especifique como grupo de superusuarios de RMS se les conceden automáticamente los permisos del grupo de superusuarios.

Para obtener más información acerca de cómo especificar un grupo de superusuarios para RMS, vea "[Para configurar un grupo de superusuarios](https://technet.microsoft.com/f2ef847e-2824-471f-9079-5c343094aba8)", más adelante en este tema.

| ![](images/Cc720198.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes de designar un grupo como grupo de superusuarios para RMS, el grupo debe existir en el mismo bosque de Active Directory que la instalación de RMS. Las propiedades de este grupo deben incluir una dirección de correo electrónico, incluido un nombre de dominio completo que sea igual al nombre de la cuenta. La dirección de correo electrónico debe tener el formato *nombre\_grupo*@*nombre\_dominio*. |
