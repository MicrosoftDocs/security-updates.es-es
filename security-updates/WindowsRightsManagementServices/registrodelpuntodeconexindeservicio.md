---
TOCTitle: Registro del punto de conexión de servicio
Title: Registro del punto de conexión de servicio
ms:assetid: '446d83ec-3224-45e2-9697-625e7db338f3'
ms:contentKeyID: 18127727
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720260(v=WS.10)'
---

Registro del punto de conexión de servicio
==========================================

El punto de conexión de servicio (SCP) de RMS identifica la dirección URL de conexión para el servicio de los clientes compatibles con RMS de su organización. Los clientes no pueden detectar RMS para solicitar licencias de uso, licencias de publicación ni certificados de cuenta de permisos sin un SCP válido.

Puede registrar la dirección URL del SCP para el clúster de certificación raíz en la página **Punto de conexión de servicio de RMS** del sitio Web de administración. También puede anular el registro de la dirección URL del SCP en la página **Punto de conexión de servicio de RMS**, si necesita restablecer la dirección URL por cualquier razón. Para registrar o anular el registro de la dirección URL de un SCP, debe iniciar sesión con una cuenta de usuario del dominio válida que posea privilegios suficientes para crear un objeto contenedor en el contenedor de servicios.

En el contenedor de servicios de Active Directory, se crea un nuevo objeto contenedor con el nombre "RightsManagementServices". En este contenedor, se crea un objeto de SCP denominado "MSRMRootCluster". Este objeto SCP tiene dos valores para el atributo de palabras clave:

-   MSRMRootCluster
-   1.0

Éstos son los atributos que los clientes y otros servidores utilizan para buscar la dirección URL del clúster raíz en Active Directory. En el objeto de SCP, serviceBindingInformation contiene la dirección URL del clúster raíz con el formato http://*nombre\_clúster*/\_wmcs/Certification.