---
TOCTitle: Restablecimiento de la contraseña de la clave privada
Title: Restablecimiento de la contraseña de la clave privada
ms:assetid: 'ceba927e-a7fd-4b06-bb70-5e5d9d6d099c'
ms:contentKeyID: 18127965
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747675(v=WS.10)'
---

Restablecimiento de la contraseña de la clave privada
=====================================================

Cuando establezca servicios en línea en un servidor, seleccione un método para proteger la clave privada de RMS. Si eligió la opción predeterminada de utilizar protección de clave privada de software, especificó una contraseña segura que se utilizó para cifrar la clave privada del servidor en la base de datos de configuración. Si pierde u olvida la contraseña, un miembro del grupo de superusuarios puede restablecerla, como se describe en "[Para restablecer la contraseña de la clave privada](https://technet.microsoft.com/f71df255-fe19-4e07-810e-87309a5e8e88)", más adelante en este tema.

Si está ejecutando RMS en un entorno de clústeres, deberá restablecer la clave privada en cada servidor de RMS de solicitudes de cliente de la instalación. Si no lo hace, dichos servidores no funcionarán, pues serán incapaces de descifrar la clave de servidor en la base de datos de configuración.

Para obtener más información acerca de las contraseñas seguras, consulte la Ayuda y Soporte técnico de Windows Server 2003.