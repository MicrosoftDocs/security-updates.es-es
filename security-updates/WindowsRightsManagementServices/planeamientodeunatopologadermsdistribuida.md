---
TOCTitle: Planeamiento de una topología de RMS distribuida
Title: Planeamiento de una topología de RMS distribuida
ms:assetid: '8773a1e0-6ac3-41f5-9866-5890cef08d04'
ms:contentKeyID: 18127867
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747657(v=WS.10)'
---

Planeamiento de una topología de RMS distribuida
================================================

En algunas circunstancias, puede ser necesario implementar uno o varios servidores de licencias que no sean miembros del clúster de certificación raíz. Normalmente, se hace para departamentos que requieren control directo sobre la emisión y de licencias de uso y de publicación, como el departamento legal, con requisitos de seguridad que necesitan un control por departamento. El clúster de certificación raíz proporciona el servicio de certificación de cuentas para los servidores de licencias. La combinación de un clúster de certificación raíz y una o varias instalaciones de servidores de licencias se denomina topología distribuida.

Tenga en cuenta que, al igual que el servidor de certificación raíz, los servidores de licencias también se pueden implementar en un clúster. Asimismo, de igual manera que el clúster de certificación raíz, el clúster de licencias utiliza su propio servicio de equilibrio de carga. Cada servidor o clúster de licencias utiliza una instancia diferente de SQL Server para proporcionar las bases de datos de registro y configuración para ese servidor o clúster particular.

Aunque se puede configurar la instalación de RMS para ejecutar sólo los servicios de certificación desde la instalación raíz, así como ejecutar todo el servicio de licencias desde uno o varios clústeres o servidores de licencias, ésta no es la configuración típica. Normalmente se aumentaría el número de servidores físicos que se encuentran en el clúster de certificación raíz para cumplir los requisitos de redundancia y rendimiento, en lugar de implementar servidores de licencias separados (a menos que necesite controlar licencias por departamentos). El siguiente diagrama ilustra esta implementación.

![](images/Cc747657.01fa5a85-5711-41aa-932a-124049d34186(WS.10).gif)

La creación de una topología distribuida puede aumentar los costos administrativos para la organización, porque este tipo de topología es inherentemente más compleja. Si la organización tiene varios bosques y clústeres de licencias, es posible que necesite llevar a cabo reemplazos del registro en los equipos cliente de RMS para asegurarse de que realizan las solicitudes de licencias desde el servidor de RMS correcto. Además, pueden surgir problemas de confianza entre dominios. Esto hace necesario configurar los dominios para permitir el uso de contenido protegido con RMS.

Puntos de conexión de servicio en una topología distribuida
-----------------------------------------------------------

Cuando se establecen los servicios en línea en un servidor de RMS, se agrega la dirección URL de un clúster al bosque de Active Directory en un punto de conexión de servicio (SCP). Hay un SCP para el clúster de certificación raíz y para cada clúster de licencias para el que haya establecido servicios en línea en el bosque. El SCP debe estar registrado para el clúster de certificación raíz antes de establecer los servicios en línea en un clúster de licencias. Cuando se establecen los servicios en línea en el clúster de licencias, el proceso de subinscripción utiliza esa dirección URL para buscar el clúster de certificación raíz en la red y obtener un certificado emisor de licencias de servidor.

Si implementa un clúster de certificación raíz en lugar de un solo servidor de certificación raíz, cada servidor del clúster debe tener una dirección virtual detrás de una dirección URL compartida.

Existen varias implementaciones de direcciones virtuales, como DNS de operación por turnos, el servicio de equilibrio de carga de red, soluciones de hardware, etc. Las direcciones virtuales proporcionan el equilibrio de carga entre servidores y eliminan la dependencia de cualquier servidor para la emisión de licencias y publicación.

RMS utiliza la dirección URL compartida como URL de adquisición de licencias, así como para el valor publicado que utilizan los equipos de usuarios finales cuando buscan el clúster de RMS en Active Directory o en el registro. Ningún equipo de usuario final requiere acceso directo a ningún servidor que se encuentre en un clúster.