---
TOCTitle: Supervisión mediante Microsoft Operations Manager
Title: Supervisión mediante Microsoft Operations Manager
ms:assetid: 'ce372598-7421-4f1f-b8eb-f62da26e85d1'
ms:contentKeyID: 18127966
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747758(v=WS.10)'
---

Supervisión mediante Microsoft Operations Manager
=================================================

RMS incluye un paquete de administración (Management Pack) que puede utilizar con Microsoft® Operations Manager (MOM). MOM puede ayudarle a administrar el funcionamiento de los servidores de su organización realizando las siguientes acciones:

-   Supervisión de sucesos que Windows RMS coloca en el registro de sucesos de aplicación.
-   Resaltado de sucesos que pueden indicar posibles interrupciones de servicio o problemas de configuración para poder tomar acciones preventivas o correctoras rápidamente.
-   Emisión de alertas de advertencias y errores, como la caducidad del certificado emisor de licencias de servidor o el error de un servicio Web.

RMS Management Pack (RMS\_MOMPack.akm) se instala con Windows RMS en la carpeta %programfiles%\\Windows Rights Management Services\\Tools.

Este paquete de administración contiene los siguientes conjuntos de reglas, que pueden utilizarse para ayudar al administrador de RMS a controlar la implementación del servidor RMS.

**Reglas del MOM Management Pack de RMS**

1.  Medida PMC - Errores totales del proxy de activación
2.  Medida PMC - Tiempo total del proxy de activación
3.  Medida PMC - Tiempo de procesamiento total de activación
4.  Medida PMC - Requisitos totales de activación
5.  Medida PMC - Requisitos totales del proxy de activación
6.  Medida PMC - Accesos a la caché de Active Directory (caché de DB)
7.  Medida PMC - Accesos no conseguidos a la caché de Active Directory (caché de DB)
8.  Medida PMC - Tiempo medio de procesamiento de licencia
9.  Suceso - Información de configuración dañada
10. Medida PMC - Conexiones de catálogo global interrumpidas
11. Medida PMC - Errores de inscripción
12. Suceso - Error general
13. Suceso - Error de inicialización
14. Suceso - El certificado emisor de licencias ha caducado
15. Suceso - Error en la solicitud de certificado emisor de licencias
16. Suceso - Error de servicio de registro
17. Medida PMC - Máximo de conexiones de catálogo global disponibles
18. Suceso - Falta el complemento de generación de punto de adquisición de licencia
19. Medida PMC - Longitud de la cola MSMQ en todos los servidores de RM
20. Suceso - No hay catálogos globales disponibles
21. Suceso - Error de inicialización de complemento
22. Suceso - Ha cambiado la contraseña de protección PrivateKey
23. Suceso - Cierre del servidor de RM
24. Suceso - Error de cierre del servidor de RM
25. Suceso - Error de inicio del servidor de RM
26. Medida PMC - Errores de subinscripción
27. Suceso - Se ha invocado el privilegio de reemplazo del superusuario
28. Umbral de PMC - Demasiados errores de GetLicensorCert
29. Suceso - El certificado emisor de licencias está a punto de caducar - 1 Mes
30. Suceso - El certificado emisor de licencias está a punto de caducar - 1 Semana

Para obtener más información acerca de cómo implementar paquetes de administración para MOM en su organización, consulte el [sitio Web de Microsoft](http://www.microsoft.com/) (http://www.microsoft.com/).
