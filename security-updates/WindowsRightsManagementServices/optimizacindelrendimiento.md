---
TOCTitle: Optimización del rendimiento
Title: Optimización del rendimiento
ms:assetid: '24dc9ca4-652b-41a6-9a99-95fdeca9120b'
ms:contentKeyID: 18127757
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720220(v=WS.10)'
---

Optimización del rendimiento
============================

Los temas de esta sección proporcionan información sobre la optimización del rendimiento de la implementación de Windows RMS.

Optimización del rendimiento de los servicios de directorio
-----------------------------------------------------------

Puede supervisar los contadores de rendimiento de servicios de directorio que se incluyen con RMS. Si es necesario, puede optimizar el rendimiento modificando la configuración del Registro que controla los atributos de la caché de Active Directory.

La configuración del Registro controla los siguientes atributos de la caché de Active Directory:

-   Número máximo de entidades principales que se copiarán en la caché.
-   Período de validez de la información que se copia en la caché para entidades principales
-   Número máximo de grupos que se copiarán en la caché
-   Período de validez de la información que se copia en la caché para grupos
-   Número máximo de entradas de pertenencia a grupos
-   Período de validez de la información que se copia en la caché para pertenencia a grupos

En general, cuanto mayor sea el período de validez de la información almacenada en la caché o cuantas más entradas haya en la caché, con mayor rapidez RMS podrá responder a las solicitudes que deban obtener información de servicios de directorio. Si la información está almacenada en la caché de Active Directory, no es necesario que Active Directory realice un recorrido de ida y vuelta para la consulta. Esto reduce el tiempo de espera para la solicitud.

Como contrapartida al almacenamiento de más información en la caché de Active Directory, es necesario utilizar más recursos de memoria del sistema. Otro aspecto que debe considerarse al configurar los valores del Registro es que, cuanto más prolongado sea el período de validez especificado para un elemento, tanto mayor será la probabilidad de que algunos de los resultados que se devuelvan desde la caché de Active Directory no sean válidos. Esto puede ocurrir si se cambia la información en Active Directory, pero el cambio todavía no aparece reflejado en la caché de Active Directory. Si Active Directory cambia con frecuencia, es posible que desee especificar un período de validez más corto para la información almacenada en la caché, que refleje esta frecuencia.

Los contadores de rendimiento de servicios de directorio se describen en “[Contadores de rendimiento de RMS: DirectoryServices](https://technet.microsoft.com/37afea1d-f320-4040-96d8-57c0b45e6d46)”, más adelante en este tema. Para obtener instrucciones sobre cómo usarlos, vea “[Uso de contadores de rendimiento](https://technet.microsoft.com/096c3b17-c082-46c4-939c-4373af0c9dec)”, anteriormente en este tema. Los contadores que se deben supervisar son los accesos conseguidos en comparación con los no conseguidos. RMS debe realizar una búsqueda en Active Directory por cada acceso no conseguido.

Para obtener información detallada sobre la configuración del Registro e instrucciones sobre cómo modificarla, vea “[Modificación de la configuración de caché de Active Directory](https://technet.microsoft.com/8789a7a5-2065-4fae-9104-e0a70f1f2fb6)”, más adelante en este tema.

Optimización de la configuración del grupo de conexiones de Active Directory
----------------------------------------------------------------------------

Para mejorar el rendimiento del sistema, puede agregar y modificar claves del Registro que controlen la configuración del grupo de conexiones del Protocolo ligero de acceso a directorios (LDAP) de Active Directory. La configuración de las claves del Registro se describe en “[Modificación de la configuración del registro del grupo de conexiones](https://technet.microsoft.com/c61d91db-a1ad-4ca5-a492-015da629afbc)”, más adelante en este tema.

RMS está diseñado para optimizar las conexiones LDAP. Establece una conexión para cada catálogo global de Active Directory y cada conexión puede servir para varios subprocesos. Para proporcionar solidez, mantiene un grupo de conexiones para utilizarlo con las solicitudes. A fin de evitar una carga demasiado grande sobre un único catálogo global, RMS utiliza un algoritmo que distribuye las solicitudes llevando a cabo un equilibrio de carga entre los catálogos globales que se encuentran en la lista de catálogos globales para consultar. También administra automáticamente los errores de LDAP y vuelve a enrutar las solicitudes a un catálogo global diferente, según sea necesario.

RMS crea una lista de catálogos globales para consultar utilizando el algoritmo de detección de topologías. Puede especificar el número mínimo y máximo de catálogos globales disponibles que el algoritmo de detección de topologías debe localizar antes de que puedan iniciarse los servicios de RMS. En primer lugar, el algoritmo descubre los catálogos globales que se encuentren en el sitio actual. Si se precisan más catálogos globales, los busca en otros sitios. También debe especificar el número máximo de conexiones que pueden dejar de estar disponibles antes de que RMS deje de aceptar solicitudes. Si uno o varios catálogos globales de la lista de consulta dejan de estar disponibles posteriormente, el algoritmo de detección de topologías comienza a buscar catálogos globales sustitutos para agregarlos a la lista de consulta.

Como alternativa, puede crear una lista de los catálogos globales que desea que RMS utilice. En este caso, el algoritmo de detección de topologías no busca catálogos globales para agregarlos a la lista de consulta.

También puede configurar opciones para el modo en que RMS lleva a cabo el equilibrio de carga entre los catálogos globales. Puede especificar la importancia (relativa) de las siguientes consideraciones al decidir si se envía una solicitud concreta a un catálogo global determinado:

-   **Operación por turnos (WtRoundRobin)**. Este parámetro especifica la importancia relativa del equilibrio de carga que utiliza lógica de operación por turnos. La configuración de peso predeterminada es 1, lo que significa que es la consideración de menor importancia que el servidor tendrá en cuenta al seleccionar un catálogo global.
-   **Número de subprocesos durante la conexión (WtThreadCount)**. Este parámetro especifica la importancia relativa del número de subprocesos que se asignan a una conexión. La configuración de peso predeterminada es 100, lo que significa que es cien veces más importante el hecho de que el número de subprocesos de un catálogo global sea bajo para que se seleccione una conexión que equilibrar la carga utilizando lógica de operación por turnos.
-   **Conexión lenta (WtSlow)**. Este parámetro especifica la importancia relativa de una conexión lenta. La configuración de peso predeterminada es 1.000, lo que significa que es diez veces más importante que una conexión a un catálogo global no sea lenta para que se seleccione que el hecho de que el número de subprocesos sea bajo.
