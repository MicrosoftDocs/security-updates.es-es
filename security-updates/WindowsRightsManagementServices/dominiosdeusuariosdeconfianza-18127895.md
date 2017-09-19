---
TOCTitle: Dominios de usuarios de confianza
Title: Dominios de usuarios de confianza
ms:assetid: 'a09b883f-f455-4c46-a4fd-d37b689e1d24'
ms:contentKeyID: 18127895
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747618(v=WS.10)'
---

Dominios de usuarios de confianza
=================================

De forma predeterminada, RMS no emite licencias de uso para los usuarios cuyos certificados de cuenta de permisos fueron emitidos por un dominio de usuario distinto. Los dominios de usuarios son instalaciones de RMS que se componen de un clúster de certificación raíz, servidores o clústeres de licencias opcionales y las bases de datos asociadas.

RMS puede configurarse para procesar este tipo de solicitudes importando el certificado emisor de licencias de servidor de otro dominio de usuario y agregándolo a la lista de dominios de usuarios de confianza. Al hacer esto, los usuarios cuyos certificados de cuenta fueron emitidos por el dominio de usuario de confianza pueden enviar solicitudes de licencias de uso a su instalación. Estas licencias de uso serán procesadas como si provinieran de usuarios internos.

| ![](images/Cc747618.note(WS.10).gif)Nota                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El clúster de certificación raíz está automáticamente en la lista de dominios de usuarios de confianza de todos los servidores de RMS que estén en la misma instalación. |

Se puede permitir a los usuarios de otros dominios compartir contenido protegido. Este proceso se describe en los ejemplos siguientes:

-   La organización trabaja estrechamente con otra organización en documentos confidenciales que se desean compartir y proteger. En la otra organización también se utiliza RMS. Las dos organizaciones pueden agregar la instalación de RMS de la otra a su lista de dominios de usuarios de confianza, de modo que los usuarios que estén en ambas organizaciones puedan trabajar juntos en contenido protegido e intercambiarlo a través de Internet o de una extranet.
-   Sólo se puede tener una instalación de RMS en cada bosque de Active Directory. Sin embargo, su organización ha implementado más de un bosque de Active Directory y en cada uno de ellos se ejecuta RMS. Los usuarios quieren compartir contenido protegido con otros usuarios sin importar en qué bosque se encuentren. Para permitir esto, se puede agregar la instalación de RMS de otros bosques a la lista de dominios de usuarios de confianza que existe en cada bosque.
-   Los usuarios de su organización trabajan con usuarios de otra organización en documentos confidenciales que desean proteger. En la otra organización no se utiliza RMS. Los usuarios que están en la otra organización pueden establecer cuentas de .NET Passport, y .NET Passport se puede agregar a lista de dominios de usuarios de confianza para la instalación de RMS. Así, los usuarios de ambas empresas pueden ahora trabajar en contenido protegido e intercambiarlo a través de Internet.

Para obtener más información acerca de las instrucciones paso a paso y los dominios de usuarios de confianza, vea "Adición y desinstalación de dominios de usuarios de confianza" y "Establecimiento de directivas de confianza" en "Operación de un servidor de RMS", en esta recopilación de documentación.
