---
TOCTitle: Expansión de la infraestructura básica para permitir los clústeres
Title: Expansión de la infraestructura básica para permitir los clústeres
ms:assetid: '78f0f2f0-a075-409c-9f46-26eb62d1d05b'
ms:contentKeyID: 18127822
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747567(v=WS.10)'
---

Expansión de la infraestructura básica para permitir los clústeres
==================================================================

Si va a implementar clústeres para instalaciones de mayor tamaño, asegúrese de que la infraestructura esté configurada para cumplir los requisitos de la agrupación en clúster. Sus planes de implementación deben incluir los elementos siguientes.

Registro de DNS
---------------

Asegúrese de que todo registro de DNS que se haga para exponer la dirección IP virtual a la extranet también expone la dirección a la intranet.

Si no se realiza el registro de DNS para la intranet, no se aceptarán las solicitudes internas de licencia de cliente. Si no puede modificar la configuración de DNS, puede modificar la tabla de hosts de cada servidor del clúster para asignar la dirección URL del clúster a la dirección IP virtual del clúster. Debe realizarse el registro de DNS antes de establecer los servicios en línea; si ya ha establecido los servicios en línea, debe eliminar RMS del servidor y a continuación repetir el proceso de establecimiento de los servicios en línea.

Equilibrio de carga
-------------------

Configure el hardware y el software necesarios para habilitar la implementación del equilibrio de carga entre servidores, el servicio de equilibrio de carga de red o el equilibrio de carga de hardware, según sea necesario, para distribuir las solicitudes por el clúster.
