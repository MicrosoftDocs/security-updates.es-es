---
TOCTitle: Compatibilidad con Active Directory para RMS
Title: Compatibilidad con Active Directory para RMS
ms:assetid: '9589127d-19b3-44f1-b7a1-01992e78218a'
ms:contentKeyID: 18127878
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747604(v=WS.10)'
---

Compatibilidad con Active Directory para RMS
============================================

RMS usa Active Directory con los siguientes fines:

-   **Proporcionar autenticación de los usuarios.** Active Directory proporciona los servicios de directorio que se usan para autenticar a los usuarios de RMS. Para obtener más información sobre la autenticación y RMS, vea "[Modelo de seguridad de RMS](https://technet.microsoft.com/665db831-366d-4dca-9bb3-cc2912481fe1)", más adelante en este tema.
-   **Resolver pertenencias a grupos e identidades de cuentas de usuario individuales.** Active Directory proporciona información acerca de la pertenencia a grupos que RMS usa para otorgar licencias de uso de contenido protegido con RMS cuando la licencia de publicación concede permisos a grupos en lugar de a cuentas de usuario individuales. Para reducir el número de consultas LDAP que se hacen a Active Directory, RMS mantiene la información que obtiene en una caché local, así como en una base de datos de servicios de directorio centralizada. Para obtener más información, vea "[Caché de Active Directory de RMS](https://technet.microsoft.com/c721a2eb-2fe9-4346-b426-3cc169b97265)" y "[Base de datos de servicios de directorio de RMS](https://technet.microsoft.com/6f6b8586-5d17-4a40-94a3-4dc738195301)", anteriormente en este tema.
-   **Almacenar la ubicación de detección de servicios de RMS.** Las solicitudes de servicios (como una licencia de uso o de publicación, o la subinscripción de un servidor de licencias) deben enviarse a la dirección URL del módulo ejecutable del servicio Web que concede la solicitud. Todas las solicitudes de servicios comienzan con una consulta a Active Directory en busca de la dirección URL del servicio Web del servidor (Server.asmx) que, a cambio, proporciona la dirección URL correspondiente a la solicitud de servicios. Para obtener más información, vea "[Publicación y detección de servicios de RMS](https://technet.microsoft.com/336c0d55-fd7f-4aa9-b3e6-bfd6565b1086)", más adelante en este tema.
