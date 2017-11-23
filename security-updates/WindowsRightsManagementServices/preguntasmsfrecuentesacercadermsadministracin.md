---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Administración'
Title: 'Preguntas más frecuentes acerca de RMS: Administración'
ms:assetid: '43f77336-5e62-4405-9efb-55417a402d62'
ms:contentKeyID: 18127794
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747547(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Administración
======================================================

Preguntas más frecuentes acerca de la administración de RMS
-----------------------------------------------------------

-   [¿Cuál es la mejor forma de revocar los permisos sobre documentos a un usuario que deja una organización?](#bkmk_1)
-   [Cuando se establecen confianzas entre dos organizaciones para intercambiar contenido de RMS, ¿necesita el certificado de licencia XrML que se pasa a la compañía de confianza algún trato especial?](#bkmk_2)
-   [¿Cómo trata RMS a los perfiles móviles de usuarios?](#bkmk_3)
-   [¿Por qué querría una organización retirar RMS?](#bkmk_4)
-   [¿En qué consiste el proceso de retiro?](#bkmk_5)
-   [¿Se puede retirar un servidor de RMS de modo que sólo algunos usuarios puedan recuperar documentos?](#bkmk_6)
-   [¿Qué significa el mensaje que indica que el servidor no puede tener acceso al directorio de aplicaciones?](#bkmk_7)
-   [¿Se puede realizar un seguimiento con el servidor de RMS?](#bkmk_8)
-   [¿Qué es la desviación del reloj y cómo puede corregirse?](#bkmk_9)

#### ¿Cuál es la mejor forma de revocar los permisos sobre documentos a un usuario que deja una organización?

En general, es mejor obtener la licencia de los documentos para los grupos de usuarios definidos en Active Directory en lugar de para cuentas de usuario individuales. Esto es recomendable para que cuando un usuario deje una organización, se le pueda quitar del grupo de Active Directory y el usuario no pueda leer documentos enviados a ese grupo. No obstante, el usuario todavía podrá leer documentos que tengan licencias de uso existentes, a menos que los documentos tuvieran establecidos permisos para que el usuario obtuviera una licencia de uso cada vez que se abriera el documento. Si este permiso no está definido, la única forma de impedir que el usuario abra documentos con licencias de uso existentes es eliminar el almacén de licencias del usuario en el equipo del usuario.

#### Cuando se establecen confianzas entre dos organizaciones para intercambiar contenido de RMS, ¿necesita el certificado de licencia XrML que se pasa a la compañía de confianza algún trato especial?

Al establecer un dominio de usuario de confianza o un dominio de publicación de confianza, permite a la organización asociada participar en el sistema de administración de permisos. Por lo tanto, está asumiendo como riesgo calculado que la otra organización no comprometerá su información. Es aconsejable solicitar que la organización asociada envíe su certificado emisor de licencias de servidor de RMS a través de un canal autenticado, como el correo electrónico S/MIME, para mitigar el riesgo de que alguien altere el certificado emisor de licencias de servidor antes de que lo importe a su servidor de RMS.

#### ¿Cómo trata RMS a los perfiles móviles de usuarios?

Los certificados de cuenta de permisos (RAC) que se utilizan para identificar a los usuarios son específicos de cada equipo. Al utilizar perfiles móviles, el primer uso de RMS en un equipo creará un nuevo RAC para el usuario en ese equipo.

#### ¿Por qué querría una organización retirar RMS?

Al retirar RMS se elimina el servidor de RMS de la infraestructura y proporciona a los usuarios una forma de guardar sin protección el contenido protegido por derechos. Las organizaciones lo hacen básicamente por tres razones:

-   Simplificar el diseño de la arquitectura, por ejemplo consolidando los servidores en un clúster.
-   Migrar una prueba de concepto de entorno piloto a un entorno de producción.
-   Fusionar servidores de RMS, por ejemplo después de una adquisición.

#### ¿En qué consiste el proceso de retiro?

El proceso de retiro se inicia desde el clúster raíz de RMS, habilitando el servicio de retiro. Cuando el servicio de retiro está habilitado, se deshabilitan todos los demás servicios, como por ejemplo las licencias y la certificación. A continuación, las aplicaciones compatibles con RMS de todos los usuarios deben conectarse al servicio de retiro cuando se utiliza una característica de RMS. Microsoft Office 2003 es un ejemplo de aplicación compatible con RMS. En Office 2003, se dirige al cliente de RMS a los servicios de RMS mediante claves de Registro. Una clave de registro específica identifica el servicio de retiro. Una vez que la clave está configurada para dirigir al cliente al servicio de retiro, el clúster de RMS otorga licencias de uso que conceden al usuario permisos completos (lectura, escritura, copia, impresión, modificación, etc.) sobre ese contenido, independientemente de si el usuario tenía o no esos permisos originalmente. A continuación, los usuarios deben quitar toda protección de derechos de los documentos que deseen conservar después de retirar completamente el clúster de RMS. Una vez hecho esto, se puede retirar el clúster de RMS del servicio por completo.

Si necesita recuperar un documento protegido por derechos una vez retirado el clúster de RMS, es recomendable realizar una copia de seguridad de la base de datos de configuración de RMS. Sin la clave privada del clúster raíz de RMS, sólo el autor del documento podrá abrir el contenido protegido por derechos una vez quitado el servidor.

#### ¿Se puede retirar un servidor de RMS de modo que sólo algunos usuarios puedan recuperar documentos?

Puede aplicar una lista de control de acceso (ACL) al servicio web de retiro (decommission.asmx) para controlar el acceso al servicio de retiro con el fin de que sólo ciertos usuarios puedan obtener la clave de descifrado para el contenido protegido por derechos.

#### ¿Qué significa el mensaje que indica que el servidor no puede tener acceso al directorio de aplicaciones?

Este error aparece a veces la primera vez que intenta abrir el sitio Web de administración de RMS después de instalar RMS. Después de recibir este error, no puede configurar o administrar RMS.

Este error aparece habitualmente cuando los Servicios de Internet Information Server (IIS) están en ejecución en el modo aislado de IIS 5.0. Utilice el procedimiento siguiente para deshabilitar esta opción en el servidor y reiniciar IIS para resolver este problema.

**Para deshabilitar el modo aislado de IIS 5.0**
1.  Inicie sesión en el servidor de RMS como miembro del grupo Administradores local.

2.  Haga clic en **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.

3.  En el **Administrador IIS**, expanda el equipo local, haga clic con el botón secundario del mouse en **Sitios Web** y, a continuación, haga clic en **Propiedades**.

4.  Haga clic en la ficha **Servicio**, desactive la casilla de verificación **Ejecutar el servicio WWW en el Modo aislado de IIS 5.0** y haga clic en **Aceptar**.

5.  Este cambio requiere que se reinicie el servicio IIS. Cuando se le pida si desea reiniciar el servicio IIS, haga clic en **Sí**.

#### ¿Se puede realizar un seguimiento con el servidor de RMS?

Dado que los Servicios de Rights Management se crearon utilizando Microsoft® .NET Framework, puede habilitar la opción de seguimiento para mantener un control de los sucesos del sistema y solucionar problemas.

Para implementar el seguimiento, debe modificar el archivo Web.config o Machine.config. Si implementa el seguimiento en el archivo Machine.config, se realiza un seguimiento de todos los componentes de software del equipo; sin embargo, si implementa el seguimiento en el archivo Web.config, sólo se realizará un seguimiento de los sucesos que se produzcan en los servicios Web.

**Para habilitar el seguimiento**

1.  Abra el archivo Machine.config o Web.config y, a continuación, agregue las siguientes líneas en la sección &lt;system.diagnostics&gt; del archivo:

```
<system.diagnostics>
<switches>
<add name="Microsoft Windows Rights Management Services-Global" value="4" />
<add name="Microsoft Windows Rights Management Services-TimeStamps" value="1" /> 
<add name="Microsoft Windows Rights Management Services-Indents" value="0" /> 
</switches>
<trace autoflush="false" indentsize="4"/>
</system.diagnostics>
```

2.  Para reiniciar IIS, ejecute IISRESET desde un símbolo del sistema.

3.  Una vez que haya recopilado los datos necesarios, quite las líneas del archivo .config que agregó en el paso 1.

4.  Para reiniciar IIS, ejecute IISRESET desde un símbolo del sistema.

> [!IMPORTANT]
> Cuando se realiza un seguimiento de un servidor de RMS, pueden producirse problemas de rendimiento, como mayores demoras en la adquisición de licencias de uso y la emisión de certificados de cuenta de permisos. Sólo deberá utilizar la opción de seguimiento en circunstancias muy concretas para ayudarle a diagnosticar y solucionar problemas. 

#### ¿Qué es la desviación del reloj y cómo puede corregirse?

La desviación del reloj se produce cuando la hora del reloj de un equipo es ligeramente diferente a la hora del reloj de otro equipo. Está pérdida es tan común como que los relojes de dos personas en una sala muestren horas ligeramente diferentes. La desviación del reloj puede causar problemas siempre que se especifique un período de validez en una licencia.

El período de validez de una licencia se establece de acuerdo con el reloj del publicador. La desviación del reloj respecto a estos períodos puede causar problemas en dos etapas del ciclo de publicación y utilización:

-   Cuando una aplicación intenta adquirir una licencia de uso mediante una licencia de publicación cuyo período de validez termina en el pasado o comienza en el futuro, según el reloj del servidor de RMS. En este caso, no se acepta la solicitud. Esto puede ocurrir cuando un usuario final solicita una licencia de uso o cuando una aplicación intenta obtener una licencia preliminar de un documento (para adquirir una licencia de uso en nombre de un usuario).
-   Si el período de validez de la licencia ha caducado (o aún no ha comenzado), no funcionará la licencia. De lo contrario, los únicos permisos que no estarán disponibles serán aquellos que hayan caducado (o que aún no sean válidos).

Por ejemplo, si el reloj de un equipo de publicación lleva 15 minutos de retraso respecto al reloj de un equipo de uso y el publicador crea una licencia que caduca en 15 minutos, el usuario recibirá del servidor una licencia de uso que no podrá utilizar, ya que los permisos de visualización del contenido que otorga la licencia de uso ya habrán caducado.

No existe una solución perfecta para los problemas de desviaciones del reloj. Una buena solución es establecer la hora de inicio del período de validez de un permiso de forma que sea anterior a la hora actual para usuarios cuyos relojes vayan retrasados respecto al suyo y, si es posible, ampliar el período de validez de la licencia para los usuarios cuyos relojes vayan adelantados. Es recomendable tener en cuenta el impacto que puede tener la desviación del reloj, especialmente al crear licencias con períodos de validez cortos.
