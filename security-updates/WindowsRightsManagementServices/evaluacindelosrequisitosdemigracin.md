---
TOCTitle: Evaluación de los requisitos de migración
Title: Evaluación de los requisitos de migración
ms:assetid: 'cec07f45-dc52-4004-860b-5cc33e5fc209'
ms:contentKeyID: 18127970
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747759(v=WS.10)'
---

Evaluación de los requisitos de migración
=========================================

Las organizaciones que implementan RMS deben establecer un plan de migración que minimice el tiempo de inactividad del servidor para permitir el mantenimiento del servidor y actualizaciones sin interrumpir el acceso de los usuarios al contenido protegido con RMS. Dado que RMS puede utilizar las bases de datos de configuración y registro anteriores, la migración de RMS de un servidor a otro debe tener un impacto mínimo en la organización si se utilizan los procedimientos adecuados. En el escenario de migración se supone que desea utilizar las bases de datos existentes; de lo contrario, llevaría a cabo una nueva instalación de RMS.

Si el servidor de RMS que está reemplazando utiliza un módulo de seguridad de hardware (HSM), como nCipher, debe transferir la configuración de HSM al nuevo servidor antes de instalar y establecer los servicios en línea de RMS en el servidor. Para obtener instrucciones, consulte la documentación del módulo de seguridad de hardware.

Antes de efectuar la migración:

-   Asegurarse de que las bases de datos están disponibles.
-   Decidir qué equipos se utilizarán en la nueva instalación.

Para migrar la instalación de RMS, siga estos pasos:

1.  Realice una copia de seguridad de todos los componentes antes de iniciar la migración, lo que incluye las bases de datos, las claves privadas y el estado del sistema.
2.  Asegúrese de que las bases de datos de la instalación anterior de RMS están presentes en el servidor de base de datos que se utilizará para la nueva implementación.
3.  Instale y establezca los servicios en línea de RMS en los servidores adecuados y especifique la ubicación de las bases de datos.

Un escenario común que origina la migración del servidor de RMS es el traslado de una implementación de RMS piloto a un entorno de producción. Para obtener más información acerca de este escenario de utilización, vea “Migración de una implementación de RMS piloto a una implementación de producción” en “Implementación de RMS”, en esta recopilación de documentación.
