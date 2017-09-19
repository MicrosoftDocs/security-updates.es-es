---
TOCTitle: Escenarios seleccionados para mejorar la seguridad con Windows Vista
Title: Escenarios seleccionados para mejorar la seguridad con Windows Vista
ms:assetid: 'e64d1259-84c5-4b92-9846-2af50ab35248'
ms:contentKeyID: 20112549
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458727(v=TechNet.10)'
---

Escenarios seleccionados para mejorar la seguridad con Windows Vista
====================================================================

##### En esta página

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Lo nuevo en Seguridad](#ecaa)
[](#ebaa)[Escenarios clave para evaluar las directivas de restricción de software y la protección de cuentas de usuario en su organización](#ebaa)
[](#eaaa)[Repaso de los escenarios de prueba](#eaaa)

### Introducción

Una plataforma de sistema operativo segura es un requisito fundamental para la informática confiable, y Microsoft Windows Vista cumple con este requisito gracias a una infraestructura de seguridad que brinda una experiencia utilizable, coherente y que puede administrarse. Microsoft utiliza las prácticas de ingeniería más adecuadas y herramientas de última generación para asegurar que el sistema operativo Windows Vista sea seguro en entornos domésticos, corporativos y móviles.

Para ayudar a los usuarios a confiar en la seguridad y la privacidad, Windows Vista les ofrece información sobre las opciones de seguridad y privacidad. La seguridad de las aplicaciones también se encuentra integrada para ayudar a brindar escenarios de seguridad de extremo a extremo, y Windows Vista ofrece una propuesta de gran valor para que los editores de aplicaciones amplíen la infraestructura de seguridad y la experiencia. Si desea obtener más información sobre la seguridad de Windows Vista, consulte las características de seguridad de Windows Vista en el sitio Web TechNet de Microsoft.

[](#mainsection)[Principio de la página](#mainsection)

### Lo nuevo en Seguridad

Windows Vista presenta nuevos e importantes avances en cuanto a seguridad, ya que protege mejor los datos personales y corporativos frente a posibles daños, como divulgación y alteración, causados por usuarios o programas malintencionados, a la vez que protege su privacidad.

Microsoft utiliza las prácticas de ingeniería más adecuadas, además de herramientas actualizadas, para asegurar que el diseño del sistema operativo Windows Vista sea seguro. Windows Vista reduce el área de la superficie de ataque, al sumarse al trabajo de Microsoft Windows XP Service Pack 2 (SP2) y Microsoft Windows Server 2003 Service Pack 1 (SP1), y ayuda a las corporaciones a administrar y aislar sus redes de forma segura.

Windows Vista facilita a los clientes la implementación de los escritorios sin que los usuarios finales necesiten derechos administrativos en su equipo, y la nueva tecnología de inicio segura de Windows Vista, pensada para las empresas, protege los datos de equipos basados en Windows que se pierden o son robados.

Esta sección describe características de seguridad seleccionadas, nuevas y actualizadas, de Windows Vista.

#### Beneficios de las características de seguridad nuevas o modificadas

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Área de características</p></th>
<th><p>Beneficio</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Firewall</p></td>
<td style="border:1px solid black;"><p>Mejora el firewall de Windows para que evite de forma activa la propagación de programas malintencionados y que se pongan en riesgo datos personales.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Endurecimiento de Servicios de Windows</p></td>
<td style="border:1px solid black;"><p>Proporciona más resistencia contra ataques de software malintencionado al limitar las acciones que los usuarios o el software pueden realizar después de afectar un servicio de Windows.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Exploración confiable</p></td>
<td style="border:1px solid black;"><p>Proporciona una experiencia más segura y confiable al explorar el Web.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Inicio y ejecución seguros</p></td>
<td style="border:1px solid black;"><p>Asegura que la integridad de Windows Vista esté protegida contra ataques con conexión y sin ella.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cliente de protección de acceso a la red</p></td>
<td style="border:1px solid black;"><p>Permite aislar el equipo y explorar su estado de mantenimiento antes de que se le otorgue acceso a una red corporativa. Esta característica requiere una funcionalidad auxiliar en Windows Vista Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Mejoras en la actualización de seguridad</p></td>
<td style="border:1px solid black;"><p>Permite ver el estado de seguridad utilizando un agente del lado del cliente y reduce la cantidad de reinicios necesarios para las revisiones de seguridad.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Centro de seguridad de Windows</p></td>
<td style="border:1px solid black;"><p>Los usuarios pueden conocer rápidamente el estado de seguridad de su equipo y recibir alertas cuando el equipo se encuentre sin protección.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Protección de cuentas de usuario</p></td>
<td style="border:1px solid black;"><p>Windows Vista facilita la implementación de un equipo con acceso de usuario con el menor número de privilegios, sin que los usuarios finales necesiten poseer derechos administrativos en sus equipos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Autenticación</p></td>
<td style="border:1px solid black;"><p>Proporciona protocolos, proveedores de inicio de sesión y una estructura de autenticación escalable y extensible.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Autorización</p></td>
<td style="border:1px solid black;"><p>Admite la expresión y evaluación de directivas enriquecidas para admitir capacidades de extensibilidad y delegación.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Administración de credenciales</p></td>
<td style="border:1px solid black;"><p>Proporciona servicios de administración de identidades mejorados y que pueden administrarse, provisión de testigos, y administración del ciclo vital.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servicios de criptografía</p></td>
<td style="border:1px solid black;"><p>Ofrece operaciones mejoradas de cifrado y firmas para aplicaciones que deben proteger datos.</p></td>
</tr>  
</tbody>  
</table>
  
#### Impacto de las características de seguridad nuevas o modificadas
  
El siguiente es un escenario de usuario de extremo a extremo que describe las formas en las que Windows Vista detecta posibles amenazas de seguridad y ayuda a protegerse frente a ellas:
  
-   Antes de iniciar un equipo con Windows Vista, el sistema está protegido de los ataques mediante un inicio seguro. Esta característica utiliza un módulo de plataforma de confianza basado en hardware para garantizar que ningún usuario malintencionado pueda iniciar el equipo con un sistema operativo diferente con el fin de afectar la instalación de Windows Vista.
  
-   Una vez que el sistema se está ejecutando, la protección de acceso a la red (NAP, Network Access Protection) comprueba que el equipo, cuando se lo conecta a la red, cuente con las últimas revisiones y firmas de virus actualizadas. NAP también se puede utilizar para examinar muchas otras características que el administrador de red haya dispuesto comprobar. Esta característica requiere la infraestructura NAP, que es parte de Windows Vista Server.
  
-   Si el equipo no cumple con la directiva de la compañía con respecto al mantenimiento del sistema, no se le permitirá el acceso a la red hasta que cumpla con ella.
  
-   El usuario inicia sesión en el equipo y en la red con credenciales estándar de usuario (no como administrador) y de esa forma minimiza el posible impacto de virus o programas malintencionados, y puede personalizar la configuración del equipo y ejecutar aplicaciones heredadas sin problemas.
  
-   Cuando se implementan revisiones en el equipo, el administrador de reinicio reduce la cantidad de reinicios necesarios en comparación con Windows XP.
  
-   Cuando el usuario explora el Web, las características de endurecimiento y privacidad de Internet Explorer ayudan a brindar resistencia contra el software no deseado, como código dañino, y control sobre la información de identificación personal del usuario.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Escenarios clave para evaluar las directivas de restricción de software y la protección de cuentas de usuario en su organización
  
Esta sección describe escenarios básicos de evaluación, en los que el administrador del dominio controla qué aplicaciones puede instalar y ejecutar un usuario en un cliente con Windows Vista.
  
En estos escenarios, el administrador desea controlar las aplicaciones que un usuario puede instalar y ejecutar. Al utilizar una directiva de restricción de software, los administradores controlan qué aplicaciones pueden instalar los usuarios con sus niveles de permiso habituales.
  
El Servicio de información de aplicaciones (AIS, Application Information Service) es un nuevo servicio de Microsoft Windows Vista que implementa Protección de cuentas de usuario (UAP, User Account Protection). Al requerir que los usuarios ejecuten el programa en modo de usuario protegido y al limitar el acceso de administrador sólo a procesos autorizados, UAP ayuda a reducir el impacto del software malintencionado, los kits de raíz, el código dañino y los virus. También permite a las organizaciones acercarse a un escritorio administrado para detener la instalación de aplicaciones no autorizadas por parte de usuarios y cambios involuntarios en la configuración del sistema.
  
**Los siguientes son requisitos mínimos para controlar qué aplicaciones puede instalar o ejecutar un usuario en un equipo cliente de Windows Vista.**
  
-   Crear un dominio.
  
-   Crear un administrador del dominio, por ejemplo, admin1.
  
-   Crear un usuario del dominio, por ejemplo, usuario1.
  
-   Proporcionar una directiva de restricción de software a través de la directiva de grupos a su dominio que permita la instalación de aplicaciones.
  
-   Instalar Microsoft Windows Vista.
  
-   Unir el cliente al dominio.
  
-   Comprobar que el administrador del dominio sea miembro del grupo de administradores locales.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Repaso de los escenarios de prueba
  
Para probar una directiva de restricción de software y la interacción con AIS, se requiere que un usuario del dominio inicie la sesión en un equipo cliente de Windows Vista con UAP habilitado y que intente instalar, ejecutar y desinstalar una aplicación permitida y una no permitida, según lo defina la directiva del dominio.
  
#### Escenario 1: Solicite al usuario del dominio que intente instalar una aplicación permitida.
  
El usuario debería poder instalar la aplicación sin que se le soliciten credenciales de admin1.
  
**Para instalar una aplicación permitida**
  
1.  Inicie sesión como admin1 y publique una aplicación en Active Directory.
  
2.  Inicie sesión como usuario1.
  
3.  Instale la aplicación con Agregar o quitar programas.
  
4.  Compruebe que la aplicación esté instalada y que se pueda usar.
  
#### Escenario 2: Intente instalar una aplicación que el administrador del dominio no haya permitido instalar explícitamente mediante una directiva.
  
El usuario no debería poder instalar la aplicación.
  
**Para intentar instalar una aplicación no permitida**
  
1.  No aplique la configuración de la directiva para la aplicación.
  
2.  Inicie sesión como usuario1.
  
3.  Intente instalar la aplicación.
  
4.  Compruebe que la instalación no se lleve a cabo.
  
#### Escenario 3: Intente ejecutar una aplicación que el administrador del dominio haya permitido que los usuarios ejecuten.
  
El usuario debería poder ejecutar la aplicación.
  
**Para ejecutar una aplicación permitida**
  
1.  Instale una aplicación y márquela para que se permita.
  
2.  Inicie sesión como usuario1.
  
3.  Intente ejecutar la aplicación.
  
#### Escenario 4: Intente ejecutar una aplicación que el administrador de dominio no haya permitido que los usuarios ejecuten.
  
El usuario no debería poder ejecutar la aplicación.
  
**Para intentar ejecutar una aplicación no permitida**
  
1.  Inicie sesión como usuario1.
  
2.  Instale una aplicación.
  
3.  Marque la aplicación para que no se permita.
  
4.  Intente ejecutar la aplicación.
  
#### Escenario 5: Intente desinstalar una aplicación que el administrador del dominio haya permitido que los usuarios puedan desinstalar.
  
**Nota** Esta prueba examina la interacción del Servicio de información de aplicaciones y que el objeto de la directiva del dominio permite a los usuarios quitar aplicaciones sin la necesidad de utilizar credenciales administrativas. En este caso, se aplica configuración de directivas del dominio para permitir al usuario instalar, actualizar y desinstalar aplicaciones.
  
El usuario debe poder desinstalar la aplicación.
  
**Para desinstalar una aplicación permitida**
  
1.  Inicie sesión como usuario1.
  
2.  Instale una aplicación permitida.
  
3.  Desinstale la aplicación.
  
4.  Compruebe que no haya quedado ningún elemento de la aplicación.
  
#### Escenario 6: Intente desinstalar una aplicación que el administrador del dominio no haya permitido que los usuarios puedan desinstalar.
  
**Nota** En este caso, la aplicación ya se encuentra instalada, pero la configuración de directivas del dominio no permite al usuario instalar, actualizar ni quitar aplicaciones.
  
El usuario no debería poder desinstalar la aplicación.
  
**Para intentar desinstalar una aplicación no permitida**
  
1.  Inicie sesión como usuario1.
  
2.  Instale una aplicación.
  
3.  Marque la aplicación para que no se permita.
  
4.  Intente desinstalar la aplicación.
  
**Nota** Las características tratadas en este sitio están sujetas a modificaciones. Es posible que algunas de ellas no se incluyan en el producto final por razones técnicas, de marketing u otras.
  
[](#mainsection)[Principio de la página](#mainsection)
