---
TOCTitle: Desinstalación y anulación de los servicios en línea de RMS
Title: Desinstalación y anulación de los servicios en línea de RMS
ms:assetid: 'cae1ed5b-f716-41f0-8e14-7cbfef405331'
ms:contentKeyID: 18127959
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747753(v=WS.10)'
---

Desinstalación y anulación de los servicios en línea de RMS
===========================================================

Por diversas razones, es posible que desee quitar RMS de un servidor. Para un servidor de certificación raíz, el primer paso es anular los servicios en línea de RMS en el servidor. Puede realizar esta tarea desde la página **Administración global** del servidor en el que desee anular los servicios en línea, haciendo clic en **Quitar RMS de este sitio Web**. No es necesario anular los servicios en línea en un servidor de licencias antes de desinstalar RMS.

| ![](images/Cc747753.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cuando anule los servicios en línea en el último servidor de certificación raíz de un bosque de Active Directory, el objeto de punto de conexión de servicio se quita de Active Directory. Si no anula los servicios en línea en este servidor antes de desinstalar RMS, no podrá establecer los servicios en línea en un nuevo servidor de certificación raíz en dicho bosque hasta que quite manualmente de Active Directory el objeto de punto de conexión de servicio. |

A continuación, desinstale RMS.

Cuando se anulan los servicios en línea y se desinstala RMS de un servidor independiente o del el último servidor de un clúster, se quita la base de datos de servicios de directorio. No se quitan las bases de datos de registro y de configuración; no obstante, si actualiza o reinstala RMS en el servidor, se sobrescribirá la base de datos de registro con una nueva.

Cuando anule los servicios en línea y desinstale RMS de un servidor que forme parte de un clúster, no se quitarán las bases de datos de servicios de directorio, registro y configuración del clúster. Sin embargo, la tabla DRMS\_ClusterServer de la base de datos de configuración se actualizará para mostrar que se ha quitado el servidor del clúster.

Para obtener más información acerca del retiro de servidores y los problemas que pueden surgir, vea “[Retiro de servidores](https://technet.microsoft.com/52005e2e-9563-4ba0-906c-3cc76f9c378f)”, anteriormente en este tema.
