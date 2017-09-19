---
TOCTitle: Realización de cambios en la base de datos de configuración
Title: Realización de cambios en la base de datos de configuración
ms:assetid: '6a7bec73-09e4-4060-b551-5990836df4bc'
ms:contentKeyID: 18127793
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747606(v=WS.10)'
---

Realización de cambios en la base de datos de configuración
===========================================================

Los cambios de configuración que realice desde el sitio Web de administración aparecen reflejados en la base de datos de configuración del servidor o clúster. Se recomienda encarecidamente que cambie los valores de configuración desde el sitio Web de administración, en lugar de cambiar datos manualmente en la base de datos de configuración. No obstante, existen dos situaciones en las que puede ser necesario realizar cambios manuales en la base de datos:

-   **Traslado de la base de datos de registro a un servidor diferente.**De forma predeterminada, la base de datos de registro está instalada en el mismo servidor que la base de datos de configuración. Si decide trasladar la base de datos de registro a un servidor diferente, debe modificar la base de datos de configuración para que haga referencia a la nueva ubicación. Para obtener más información acerca del traslado de una base de datos de registro, incluido cómo actualizar la base de datos de configuración con la nueva ubicación, vea “[Reubicación de la base de datos de registro](https://technet.microsoft.com/34ea8045-dc94-422e-9601-29927cfc1534)”, anteriormente en este tema.
-   **Eliminación de claves de usuario asociadas con certificados de cuenta de permisos**. Cuando quita una cuenta de usuario de Active Directory o excluye o revoca un certificado de cuenta de permisos desde el sitio Web de administración, las claves de usuario asociadas al certificado de cuenta de permisos no se quitan de la base de datos de configuración. Debe quitar manualmente las claves de usuario inactivas de la base de datos de configuración, en parte por seguridad, pero también para facilitar el seguimiento del número de licencias de acceso de cliente (CAL). Para obtener más información sobre cómo quitar claves de usuario de la base de datos de configuración, vea “[Eliminación de cuentas de usuario](https://technet.microsoft.com/bf73b141-d4d1-4807-a773-3aaff58b0db6)”, anteriormente en este tema. Para obtener más información acerca del seguimiento, vea “[Seguimiento de certificados de cuenta de permisos](https://technet.microsoft.com/5bb0f3cf-fc44-4e60-a93f-c789d6f8a902)”, anteriormente en este tema.

Si debe realizar cambios directamente en una base de datos de configuración, póngase en contacto con el administrador del servidor de bases de datos.
