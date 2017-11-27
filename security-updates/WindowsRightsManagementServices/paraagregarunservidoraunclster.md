---
TOCTitle: Para agregar un servidor a un clúster
Title: Para agregar un servidor a un clúster
ms:assetid: 'db635238-5528-4bec-9cc6-8244e2b3d733'
ms:contentKeyID: 18127989
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747690(v=WS.10)'
---

Para agregar un servidor a un clúster
=====================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

En cada servidor, puede establecer los servicios en línea de RMS en un solo sitio Web. Si desea establecer los servicios en línea de RMS en un sitio Web diferente del sitio Web predeterminado, utilice el Administrador de servicios de Internet Information Server para agregar el sitio Web antes de iniciar este proceso de establecimiento de servicios en línea. Si el sitio Web en el que desea establecer los servicios en línea no aparece en la lista de sitios Web, cierre la página **Administración global**, agregue el sitio Web y, a continuación, inicie de nuevo el proceso de establecimiento de servicios en línea.

Si está implementando RMS en un entorno en el que el nivel funcional del dominio de Active Directory está establecido en el modo nativo de Windows 2000, es posible que RMS no pueda leer el atributo **memberOf** de los objetos de Active Directory cuando intente ampliar la pertenencia a grupos. Para que RMS pueda leer el atributo **memberOf**, la cuenta de servicio de RMS debe utilizar una cuenta de dominio que sea miembro del grupo Acceso compatible con versiones anteriores de Windows 2000 (integrado) en el bosque.

Adición de un servidor a un clúster
-----------------------------------

#### Para agregar un servidor a un clúster

1.  Después de instalar RMS en un servidor que desee unir a un clúster de certificación raíz o de licencias, abra la página **Administración global**.

2.  Junto al sitio Web en el que desee establecer los servicios en línea de RMS, haga clic en **Agregar este servidor a un clúster**. Puede seleccionar el sitio Web predeterminado u otro sitio Web creado en los Servicios de Internet Information Server (IIS) con este propósito.

    > [!WARNING]
    > No se admite la ejecución de sitios o servicios Web adicionales en el mismo servidor que RMS. Si se hiciera así, muchos servicios y aplicaciones se ejecutarían con la misma cuenta que RMS, lo que podría exponer las claves privadas a operaciones no deseadas. 

3.  En el área **Cuenta de servicio de RMS**, escriba el nombre de cuenta, con el formato nombre\_dominio\\nombre\_usuario y la contraseña de la cuenta de servicio de RMS con la que se ejecutará RMS para la mayoría de las operaciones normales. Debe ser una cuenta de dominio. Todos los servicios de un clúster deben ejecutarse con la misma cuenta de servicio de RMS.

    > [!IMPORTANT]
    > Por razones de seguridad, es recomendable crear una cuenta de usuario de dominio especial para usarla como cuenta de servicio de RMS y no concederle ningún permiso especial. La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS con Service Pack 1. 

4.  En el área **Base de datos de configuración**, especifique el nombre del servidor de base de datos y el nombre de la base de datos de configuración para este clúster. La base de datos seleccionada determina el clúster al que se une este servidor.

5.  En el área **Protección de clave privada**, seleccione el mecanismo utilizado por este clúster para proteger la clave privada. Para la protección de clave privada de software predeterminada, proporcione la contraseña que se utilizó para cifrar la clave privada cuando se establecieron los servicios en línea en el primer servidor de este clúster.

6.  Haga clic en **Enviar**.

    Si aparecen mensajes de error, no cierre la página. En su lugar, corrija los errores, utilice IISReset desde la línea de comandos para iniciar y reiniciar IIS, vuelva a la página anterior y, a continuación, haga clic otra vez en **Enviar**. Si obtiene el error "Tiempo de espera agotado para esta solicitud", cierre la ventana, compruebe que el sistema cumple los requisitos mínimos de hardware e intente establecer los servicios en línea en el servidor otra vez.
