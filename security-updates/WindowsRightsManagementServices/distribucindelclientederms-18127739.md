---
TOCTitle: Distribución del cliente de RMS
Title: Distribución del cliente de RMS
ms:assetid: '4b8dd930-4105-4e73-918c-12d2b05d5fb5'
ms:contentKeyID: 18127739
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720266(v=WS.10)'
---

Distribución del cliente de RMS
===============================

El cliente RMS está integrado en el sistema operativo Windows Vista® de modo que el cliente RMS ya no requiera una instalación independiente. Los sistemas operativos anteriores a Windows Vista requieren la instalación y posterior activación del software de cliente RMS.

El proceso de activación establece una caja de seguridad y un certificado de equipo para el usuario que actualmente tenga una sesión iniciada. La activación es un proceso local y no requiere una conexión de red. Una vez realizada con éxito la activación, la primera solicitud de licencia de uso por parte de una aplicación compatible con RMS obtiene un certificado de usuario para el usuario. Puede instalarse el cliente de RMS en cada uno de los equipos cliente de la organización utilizando una directiva de grupo, Windows Update o un comando administrativo.

> [!NOTE]
> Independientemente del método de distribución del cliente que se utilice, el puerto predeterminado es el 80 o el 443 para comunicarse con el servidor RMS. Debería asegurarse de que el equipo cliente puede realizar solicitudes de salida al clúster raíz de RMS y de sólo licencias en esos puertos. 

**Uso de directivas de grupo**

Si su organización distribuye software mediante una directiva de grupo, puede utilizar este método para distribuir el cliente RMS a través de privilegios elevados. Si el cliente RMS se distribuye así, el usuario no requiere privilegios de administrador y puede instalar el cliente RMS mediante **Agregar o quitar programas** en el **Panel de control** o abriendo contenido protegido con derechos con una aplicación compatible con RMS.

**Uso de Windows Update**

Windows Update proporciona la forma más sencilla de instalar un cliente de RMS en un equipo. Este método tiene la ventaja de utilizar un mecanismo que resulta familiar a los usuarios, pero requiere que el usuario que instala el cliente RMS tenga derechos de administrador local en el equipo.

**Uso de la instalación mediante secuencia de comandos**

Para tener un nivel superior de control sobre el proceso de instalación de cliente, puede adquirir el software y, a continuación, validar su integridad a cada paso del proceso de instalación mediante la ejecución de una secuencia de comandos. Esta secuencia de comandos se puede escribir y agregar a un objeto de directiva de grupo (GPO) como secuencia de comandos de inicio. Con este método, el usuario no tiene que ser administrador local en el equipo y el cliente RMS se instala automáticamente tras reiniciar.

        ```
Para obtener información básica sobre la distribución del cliente RMS utilizando la directiva de grupo, vea [Configuración de SMS o de una directiva de grupo para admitir la implementación de clientes](https://technet.microsoft.com/9e37c27b-8cc1-40c6-adb7-0937aa64c8db), más adelante en este tema.

Para obtener información sobre el proceso de implementación del cliente RMS, vea [Cómo implementar el cliente de RMS](https://technet.microsoft.com/c84f1724-cf71-4385-9003-ff68bc23c927), más adelante en este tema.
