---
TOCTitle: 'Apéndice A: Opciones clave que se deben considerar'
Title: 'Apéndice A: Opciones clave que se deben considerar'
ms:assetid: '6b4fdfca-4c2c-47f6-8c92-de33a663ea03'
ms:contentKeyID: 20200273
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163065(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Apéndice A: Opciones clave que se deben considerar

Actualizado: 20/10/05

Aunque en esta guía se tratan numerosas contramedidas y opciones de configuración de seguridad, tenga en cuenta que algunas son especialmente importantes. Este apéndice describe esas opciones de configuración; tal vez desee consultar el capítulo correspondiente para ver una explicación de la función y el motivo por el que es importante una opción de configuración.

Las opciones que se deben incluir en esta lista podrían debatirse ampliamente. De hecho, este tema fue tratado ampliamente por un grupo de expertos de seguridad de Microsoft. Es posible que le parezca que faltan algunas opciones de configuración o que algunas de las incluidas no deberían estar en la lista. Puesto que cada organización tiene un entorno distinto y unas necesidades empresariales únicas, es previsible que existan opiniones diversas sobre los problemas de seguridad. No obstante, esta lista puede serle útil para establecer una prioridad de las tareas relacionadas con la seguridad de los equipos que ejecutan Microsoft® Windows®.

##### En esta página

[](#ebaa)[Contramedidas importantes](#ebaa)
[](#eaaa)[Principales opciones de configuración de seguridad](#eaaa)

### Contramedidas importantes

Entre las contramedidas importantes que no están relacionadas con la configuración de seguridad se incluyen las siguientes:

-   Mantener actualizados los equipos con los Service Pack y las revisiones mediante las herramientas automáticas de pruebas e implementación.

-   Instalar y configurar software de servidor de seguridad distribuido o directivas IPSec organizativas.

-   Implementar y mantener un software antivirus.

-   Implementar y mantener programas contra software espía.

-   Utilizar una cuenta sin privilegios para las tareas cotidianas. Use únicamente una cuenta con privilegios de administrador para realizar las tareas que requieran privilegios elevados.

[](#mainsection)[Principio de la página](#mainsection)

### Principales opciones de configuración de seguridad

Entre las principales opciones de configuración de seguridad que están disponibles en Microsoft Windows se incluyen las siguientes:

-   Configuraciones de directiva de contraseñas, que se tratan en el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory:"

    -   Forzar el historial de contraseñas

    -   Vigencia máxima de la contraseña

    -   Longitud mínima de la contraseña

    -   Las contraseñas deben cumplir los requerimientos de complejidad

    -   Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio

-   Configuración de asignaciones de derechos de usuario, que se trata en el capítulo 3, "Configuración de seguridad para clientes Windows XP:"

    -   Tener acceso a este equipo desde la red

    -   Actuar como parte del sistema operativo

    -   Permitir el inicio de sesión local

    -   Permitir inicio de sesión a través de Servicios de Terminal Server

-   Configuración de opciones de seguridad, que se trata en el capítulo 3, "Configuración de seguridad para clientes Windows XP:"

    -   Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola

    -   Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)

    -   Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)

    -   Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)

    -   Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)

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

-   Configuración adicional del Registro, que se trata en el capítulo 3, "Configuración de seguridad para clientes Windows XP", especialmente la opción siguiente:

    -   Modo seguro de búsqueda de DLL

##### Descargar

[![](images/Cc163065.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)

[](#mainsection)[Principio de la página](#mainsection)
