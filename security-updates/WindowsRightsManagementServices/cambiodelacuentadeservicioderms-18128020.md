---
TOCTitle: Cambio de la cuenta de servicio de RMS
Title: Cambio de la cuenta de servicio de RMS
ms:assetid: 'f257d66d-b823-41e4-bcb7-7c90eb295238'
ms:contentKeyID: 18128020
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747736(v=WS.10)'
---

Cambio de la cuenta de servicio de RMS
======================================

Durante la instalación, RMS crea el grupo de servicio de RMS en el equipo local y le otorga los permisos adecuados en todos los recursos que sean necesarios para el funcionamiento de RMS. Cuando se establecen los servicios en línea de RMS en un servidor, se define la cuenta de servicio de RMS utilizando una cuenta de dominio. La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS. Dicha cuenta pasa a formar parte del grupo de servicio de RMS y se le otorgan los permisos asociados con este grupo. Durante el funcionamiento habitual, RMS se ejecuta con la cuenta de servicio de RMS.

Puede cambiar la cuenta de servicio de RMS en cualquier momento. Cuando lo haga, la cuenta anteriormente especificada se quitará automáticamente del grupo de servicio de RMS y la nueva cuenta pasará a formar parte de él.

| ![](images/Cc747736.Important(WS.10).gif)Importante                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Por seguridad, se recomienda que cree una cuenta de usuario especial para utilizarla únicamente como cuenta de servicio de RMS y para ningún otro fin. Además, no debe otorgar a esta cuenta ningún permiso adicional. |

| ![](images/Cc747736.note(WS.10).gif)Nota                                                     |
|---------------------------------------------------------------------------------------------------------------------------|
| La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS con Service Pack 1. |
