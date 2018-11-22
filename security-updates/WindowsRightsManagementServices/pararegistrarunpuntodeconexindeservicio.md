---
TOCTitle: Para registrar un punto de conexión de servicio
Title: Para registrar un punto de conexión de servicio
ms:assetid: '630cc3c3-9ed9-4423-8874-cbaceb43b353'
ms:contentKeyID: 18127771
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720283(v=WS.10)'
---

Para registrar un punto de conexión de servicio
===============================================

Registro de un punto de conexión de servicio
--------------------------------------------

Si va a registrar un punto de conexión de servicio desde un servidor de RMS en un subdominio, puede recibir un error que indique que el registro de SCP ha dado un error. En muchos casos, el registro ha sido correcto, pero tiene lugar primero en el dominio de nivel superior y tarda un poco en replicarse en el subdominio donde el servidor de RMS busca el objeto de SCP. Tan pronto como SCP se haya replicado en todos los servidores de catálogo global del bosque, el mensaje no volverá a aparecer. Si recibe este mensaje, debe esperar un intervalo de tiempo razonable antes de intentar resolver el problema.

#### Para registrar un punto de conexión de servicio

1.  Inicie sesión en el servidor en el que necesite registrar un punto de conexión de servicio, utilizando una cuenta de dominio con privilegios suficientes para crear un objeto contenedor para el contenedor de servicios del contenedor de configuración del bosque de Active Directory. El grupo de seguridad predefinido, **Administradores de organización**, es un ejemplo de cuenta con los privilegios necesarios.

2.  Abra la página **Administración global** y, a continuación, haga clic en el vínculo **Administrar RMS en este sitio Web**.

3.  En la **página principal de administración**, haga clic en el vínculo **Punto de conexión de servicio de RMS**.

4.  En la página **Punto de conexión de servicio de RMS**, haga clic en el botón **Registrar URL**.
