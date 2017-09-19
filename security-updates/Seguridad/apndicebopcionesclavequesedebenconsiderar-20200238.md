---
TOCTitle: 'Apéndice B: Opciones clave que se deben considerar'
Title: 'Apéndice B: Opciones clave que se deben considerar'
ms:assetid: '22b7ca9a-8713-4a2a-8255-3666a82da9ee'
ms:contentKeyID: 20200238
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163102(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Apéndice B: Opciones clave que se deben considerar

Actualizado: 27/12/05

Aunque en esta guía se tratan numerosas contramedidas y opciones de configuración de seguridad, tenga en cuenta que algunas son especialmente importantes. Este apéndice describe esas opciones de configuración; tal vez desee consultar el capítulo correspondiente para ver una explicación de la función y el motivo por el que es importante una opción de configuración.

La decisión sobre qué opciones de configuración se pueden incluir en esta lista puede ser objeto de un amplio debate. De hecho, este tema fue tratado ampliamente por un grupo de expertos de seguridad de Microsoft. Es posible que le parezca que faltan algunas opciones de configuración o que algunas de las incluidas no deberían estar en la lista. Puesto que cada organización tiene un entorno distinto y unas necesidades empresariales únicas, es previsible que existan opiniones diversas sobre los problemas de seguridad. No obstante, esta lista puede serle útil para establecer una prioridad de las tareas relacionadas con la seguridad de los equipos que ejecutan Microsoft® Windows®.

Entre las contramedidas importantes que no son opciones de configuración de seguridad se incluyen las siguientes:

-   Mantener actualizados los equipos con los Service Pack y las revisiones mediante las herramientas automáticas de pruebas e implementación.

-   Instalar y configurar software de servidor de seguridad distribuido o directivas IPSec organizativas.

-   Implementar y mantener un software antivirus.

-   Implementar y mantener programas contra software espía en los equipos utilizados para explorar sitios web.

-   Utilizar una cuenta no administrativa para las tareas diarias. Use únicamente una cuenta con privilegios de administrador para realizar las tareas que requieran privilegios elevados.

Entre las principales opciones de configuración de seguridad que están disponibles en Microsoft Windows se incluyen las siguientes:

-   Directiva de contraseñas (se explica en el capítulo 3, "Directiva de dominio")

    -   Forzar el historial de contraseñas

    -   Vigencia máxima de la contraseña

    -   Longitud mínima de la contraseña

    -   Las contraseñas deben cumplir los requerimientos de complejidad

    -   Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio

-   Derechos de usuario (se explican en el capítulo 4, "Directiva de línea de base de servidores miembro")

    -   Tener acceso a este equipo desde la red

    -   Actuar como parte del sistema operativo

    -   Permitir el inicio de sesión local

    -   Permitir inicio de sesión a través de Servicios de Terminal Server

-   Opciones de seguridad (se explican en el capítulo 4, "Directiva de línea de base de servidores miembro")

    -   Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola

    -   Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)

    -   Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)

    -   Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)

    -   Miembro de dominio: requerir clave de sesión protegida (Windows* *2000 o más reciente)

    -   Acceso de red: permitir traducción SID/nombre anónima

    -   Acceso de red: no permitir enumeraciones anónimas de cuentas SAM

    -   Acceso de red: no permitir enumeraciones de cuentas y recursos compartidos SAM

    -   Acceso de red: permitir la aplicación de los permisos Todos a usuarios anónimos

    -   Acceso de red: rutas de Registro accesibles remotamente

    -   Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos

    -   Acceso de red: recursos compartidos accesibles anónimamente

    -   Acceso de red: modelo de seguridad y recursos compartidos para cuentas locales

    -   Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña

    -   Seguridad de red: nivel de autenticación de LAN Manager

-   Configuración adicional del Registro (se explica en el capítulo 4, "Directiva de línea de base de servidores miembro")

    -   Modo seguro de búsqueda de DLL

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
